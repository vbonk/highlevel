# Naming & Standards Guide  

## Purpose  
This document outlines naming conventions and standards to ensure a consistent, scalable HighLevel configuration.  

## General Principles  
- Use clear prefixes to denote object type.  
- Keep names concise but descriptive.  
- Avoid special characters; use spaces or hyphens as shown.  
- Document any new names or tags.  

## Pipelines  
- Format: `PIPE - {Purpose}` (e.g., `PIPE - Sales`).  
- Only create new pipelines for distinctly different processes.  

## Stages  
- Stage names should reflect lifecycle steps (e.g., "New Lead", "Qualified", "Booked", "Won", "Lost").  

## Workflows  
- Format: `WF - {Area} - {Purpose}` (e.g., `WF - Onboarding - Welcome Sequence`).  
- Organize workflows into folders by area (Onboarding, Nurture, Re-engagement).  
- Keep workflows simple and modular.  

## Tags  
- Use tags as flags, not storage.  
- Prefix conventions:  
  - `src:` for lead source (e.g., `src:website`, `src:referral`).  
  - `stage:` for lifecycle stages if needed (e.g., `stage:new`).  
  - `interest:` for interests or products.  
- Document new tags in this guide.  

## Forms and Surveys  
- Format: `FORM - {Purpose}` (e.g., `FORM - Contact Us`).  
- Ensure form fields map directly to custom fields.  

## Calendars  
- Format: `CAL - {Owner/Team} - {Purpose}` (e.g., `CAL - Sales - Discovery`).  
- Configure availability and time zones appropriately.  

## Custom Fields  
- Use snake_case for API names; use human-readable labels in the UI.  
- Group related fields together for clarity.  

## Email & SMS Templates  
- Organize by lifecycle stage or campaign.  
- Use consistent subject lines and salutations.  

## Folder Organization  
- Create folders in Workflows for each major area.  
- Maintain a consistent structure across accounts.  

---  
Adhering to these standards will help maintain order as your HighLevel system grows. Update this document as you introduce new conventions.
