# HighLevel Setup Blueprint

This document outlines the core structure for configuring a HighLevel account according to the MVP-AIM plan. It provides guidance on pipelines, tags, workflows, account structure, and content templates.

## Pipelines & Stages

Define a lifecycle-based pipeline that maps a lead from initial contact through conversion. Example stages:
- **New Lead** – incoming leads captured via forms or integrations.
- **Contacted** – leads that have received an initial email/SMS/phone call.
- **Qualified** – leads determined to fit the ideal customer profile.
- **Booked** – appointments scheduled or demos booked.
- **Closed Won** – successful sale or sign-up.
- **Closed Lost** – leads that did not convert.

Keep the number of pipelines minimal; separate pipelines only when processes differ significantly (e.g., different products or services).

## Tags & Taxonomy

Use tags as flags rather than data storage. Establish a naming convention such as:
- `src:` prefix for lead source (e.g., `src:website`, `src:referral`).
- `stage:` prefix for lifecycle tags if needed (e.g., `stage:new`, `stage:qualified`).
- `interest:` prefix for product/service interest.
- Avoid creating tags on the fly; document new tags in your conventions guide.

## Workflows

Structure workflows in a modular manner:
- **Naming**: Use a consistent prefix like `WF -` followed by the purpose (e.g., `WF - Lead Nurture`).
- **Triggers**: Base triggers on form submissions, tag application, stage changes, or appointment bookings.
- **Actions**: Send emails, SMS, assign tasks, apply/remove tags, move pipeline stages.
- **Organization**: Group related workflows into folders (e.g., Lead Nurture, Onboarding, Re-Engagement).
- **Simplicity**: Avoid excessive branching; create separate workflows for distinct paths.

## Account Structure

Key elements to configure:
- **Custom Fields**: Create only fields you need; use proper data types (text, date, dropdown).
- **Forms & Surveys**: Build forms that map directly to custom fields; embed them in funnels or websites.
- **Calendars**: Set up one or more calendars for booking, with correct availability and time zone settings.
- **Funnels/Websites**: Design landing pages and steps that align with your pipeline stages; include CTAs.
- **Integrations**: Connect Mailgun/Twilio for emails/SMS, Stripe for payments, and any necessary webhooks.

## Content Templates

Prepare reusable templates:
- **Email templates** for initial contact, follow-ups, booking confirmations, and post-appointment sequences.
- **SMS templates** for quick updates and reminders.
- **Voicemail drops** if using phone integrations.

Store these templates in the appropriate HighLevel sections so workflows can reference them.

## Folder & Naming Conventions

- **Pipelines**: `PIPE - {Purpose}` (e.g., `PIPE - Sales`).
- **Workflows**: `WF - {Area} - {Purpose}` (e.g., `WF - Onboarding - Welcome Sequence`).
- **Forms**: `FORM - {Purpose}`.
- **Calendars**: `CAL - {Owner/Team} - {Purpose}`.

Consistent naming helps maintain order as you scale.

---

This blueprint should be used alongside the AI nucleus to make specific decisions. Update it as your processes evolve and once your external AI system expands.
