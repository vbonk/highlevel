# AI Nucleus Specification – HighLevel Expert Agent (Minimal Version)  

## 1. Purpose

Provide a **lightweight external AI expert** that helps design and configure HighLevel correctly on the first pass, without overbuilding a massive AI system.

This agent:

- Advises on structure (pipelines, tags, workflows)  
- Helps you avoid common HighLevel pitfalls  
- Enforces conventions and standards  
- Reduces decision fatigue during setup  

It does **not** need:

- Automated ingestion pipelines  
- Full RAG from day one  
- Multi-model orchestration  
- Webhooks or live HL integration  

Those can come later.

---

## 2. Functional Scope (Phase 1)

The AI Nucleus should be able to:

1. Explain HighLevel core objects and best practices in plain language.  
2. Propose clean pipelines and stages for your use cases.  
3. Help define:
   - Tags and taxonomy  
   - Workflow structure and naming  
   - Field usage and organization  
4. Review proposed structures and suggest simplifications.  
5. Help you avoid:
   - "Spaghetti workflows"  
   - Tag bloat  
   - Conflicting triggers  
   - Redundant automations  

---

## 3. Technical Setup

### 3.1 Model

- Use your best available **reasoning-capable model** (e.g., GPT-5.x thinking-class).  
- Configure:  
  - Temperature: moderate (0.3–0.6) to keep it focused and structured.  
  - Max tokens: enough for long-form reasoning (e.g., 4–8k context).  

### 3.2 Memory

Start with a **single canonical memory file** such as:

- `docs/naming-and-standards.md`  
- A dedicated `ai-memory.md` later if needed.  

The model is always primed with:

- System prompt (role + mission)  
- Key standards from memory  

Vector DB / embeddings can be added in a later phase.

---

## 4. System Prompt (Concept Overview)

The system prompt for this agent should:

- Define it as:
  - A HighLevel architecture and workflow design expert  
  - Opinionated but pragmatic  
  - Focused on simplicity, scalability, and revenue generation  
- Instruct it to:
  - Base all suggestions on the defined Velte conventions  
  - Minimize complexity  
  - Avoid over-automation  
  - Explain trade-offs clearly  
- Limit scope:  
  - It should not pretend to have direct access to your HL instance (unless wired later)  
  - It should stay within HighLevel + your conventions  

(We will define a full prompt in a separate `ai-nucleus-prompt` file if needed.)

---

## 5. Inputs & Outputs

### 5.1 Typical Inputs

- "Here is my planned pipeline – critique it."  
- "I want to handle inbound leads from X and Y – how should I structure pipelines and tags?"  
- "I’m thinking about this workflow – is there a better pattern?"  
- "Help me name these workflows and tags in a consistent way."  
- "What is the simplest way to do [use case] in HighLevel?"  

### 5.2 Typical Outputs

- Pipeline diagrams (textual)  
- Tag lists grouped by purpose  
- Workflow naming templates  
- Suggested trigger/action structures  
- Warnings about complexity and maintenance risks  
- Step-by-step implementation guidance  

---

## 6. Constraints

- No direct API calls to HighLevel in Phase 1.  
- No assumption of live data.  
- No attempt to build a fully autonomous system.  
- All suggestions should prefer:  
  - Clarity  
  - Maintainability  
  - Minimum moving parts  

---

## 7. Path to Expansion

In later phases, this nucleus can be expanded into:

- A full VelteAI Architect with:
  - Document ingestion (HighLevel docs, release notes, SOPs)  
  - Vectorized knowledge base  
  - Webhook-driven HL integration  
  - System audits and recommendations  

The current spec deliberately **stops short of that**, so you can ship HL quickly without overbuilding the AI.
