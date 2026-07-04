# MEMORY.md — Stable Automation Knowledge

This file stores stable knowledge, working preferences, repeated lessons, and reusable automation patterns for Mervin's AI automation work.

Use this file as a long-term reference for Codex, n8n workflow planning, project documentation, and future automation builds.

---

## Memory Rules

Only save information here when it is stable, reusable, and helpful for future work.

Good memory examples:

- Preferred workflow architecture
- Repeated project patterns
- n8n node naming rules
- CRM logic standards
- API mapping lessons
- Debugging lessons learned
- Portfolio writing preferences
- Common field names and data structures
- Tool preferences

Do not save:

- API keys
- Passwords
- Access tokens
- Private credentials
- Temporary errors
- One-time notes
- Client secrets
- Sensitive personal data
- Random experiments that are not reusable

---

## User Working Style

- Keep responses simple, direct, and practical.
- Prefer copy-paste ready prompts and code.
- Avoid unnecessary theory unless requested.
- When explaining automation, use step-by-step workflow maps.
- For Codex prompts, be specific about what to inspect, update, preserve, and verify.
- Do not remove working logic unless explicitly asked.
- Do not touch credentials or secret values.
- Prefer clean, maintainable workflows over complex designs.

---

## Main Professional Positioning

Mervin's preferred positioning:

**n8n AI Automation Specialist and Workflow Systems Builder**

Primary focus:

- n8n automation
- AI agents
- API integrations
- Airtable CRM
- Supabase systems
- Google Sheets automation
- Slack and Telegram workflows
- Facebook Graph API automation
- Voice AI workflows
- Dashboards and reporting
- Workflow documentation

---

## Default n8n Workflow Standards

For n8n workflows, use these default standards:

1. Start with clear trigger logic.
2. Validate incoming data early.
3. Normalize data before saving or sending to APIs.
4. Check for existing records before creating new records.
5. Use clear node names.
6. Keep each node focused on one purpose.
7. Add error handling for API failures and missing fields.
8. Add logging for important results.
9. Use fallback logic when AI output is invalid.
10. Keep workflows easy to understand and maintain.\n11. After any multi-item fan-out, reduce back to one item before one-time actions such as follow-up tasks, notifications, logs, and webhook responses.\n12. For file-intake workflows, reuse a CRM-stored folder link before creating a folder, and make the no-file branch output one item so downstream processing still completes.\n13. When processing multiple uploaded documents, keep each file linked to its source document item through download and upload branches so the returned file URL and ID update the correct database row.

Preferred node naming examples:

- Validate Incoming Data
- Normalize Lead Data
- Check Existing CRM Record
- Create CRM Record
- Update Existing CRM Record
- Generate AI Summary
- Parse AI Output
- Send Slack Notification
- Log Workflow Result
- Handle API Error

Avoid vague node names like:

- Code
- Set
- Test
- Node 1
- New Node

---

## CRM Automation Pattern

Default CRM workflow logic:

1. Receive lead or customer data from form, webhook, or bot.
2. Normalize name, email, phone, source, and notes.
3. Search CRM for existing contact using email and phone.
4. If existing contact is found, update the record.
5. If no contact is found, create a new record.
6. Add status, owner, source, timestamp, and workflow notes.
7. Notify team in Slack or Telegram.
8. Log the result in Google Sheets, Airtable, or Supabase.

Use this pattern for Airtable CRM, Supabase CRM, and lead intake systems.

---

## AI Workflow Pattern

Default AI workflow logic:

1. Prepare clean input data.
2. Send only necessary context to the AI model.
3. Ask for strict JSON output when the next step needs parsing.
4. Parse the AI response safely.
5. Add fallback values when output is missing or invalid.
6. Log AI confidence or reason when useful.
7. Never let AI overwrite critical business data without validation.

Preferred AI JSON format example:

```json
{
  "summary": "",
  "status": "",
  "next_action": "",
  "confidence": ""
}
```

---

## Project Documentation Pattern

Use this format for portfolio and GitHub project documentation:

- Project Name
- Problem
- Solution
- Tools Used
- Workflow Summary
- Business Result
- Demo or Video Link

Keep project descriptions practical and business-focused.

---

## Preferred Tool Choices

Use these defaults unless the project requires something else:

- n8n for automation orchestration
- Airtable for lightweight CRM and operations database
- Supabase for structured backend/database apps
- Google Sheets for logs, queues, and reporting
- Slack for team alerts and approvals
- Telegram for personal bot commands and notifications
- Tally for forms and lead intake
- Retool for internal dashboards
- Looker Studio for reporting dashboards
- Vapi.ai or Retell AI for voice agents
- OpenAI, Claude, OpenRouter, or Mimo for AI workflows
- React, Vite, Tailwind CSS, and Vercel for web projects

---

## Known Project Patterns

### Solar Lead Automation CRM

Pattern:

- Lead form submission
- Store in Airtable CRM
- Check if customer already exists
- AI lead qualification
- Slack notification
- Status tracking

### Submission Tracking System

Pattern:

- Intake form
- Store record in Supabase
- Status tracking
- Review notification
- Escalation workflow
- Dashboard visibility

### Renewal Management System

Pattern:

- Track renewal date
- Send reminders
- Update status
- Escalate overdue renewals
- Show dashboard overview

### Facebook Auto Post System

Pattern:

- Product intake
- Google Sheets queue
- AI caption generation
- Image handling
- Facebook Graph API posting
- First comment or auto-reply logic
- Posting logs and status tracking

### OLJ Job Scraper and Cover Letter Generator

Pattern:

- Telegram receives job URL
- Scrape job details
- Analyze fit
- Generate tailored cover letter
- Save to Google Sheets
- Send result back to Telegram

---

## Safe Memory Update Process

When new information should be saved:

1. Decide if it is stable or temporary.
2. If temporary, do not save it.
3. If stable and reusable, add it to the correct section of this file.
4. If it changes default behavior, consider updating `AGENTS.md` too.
5. If it is a new skill, update `SKILLS.md` and `skills.json`.
6. Never store secrets or private credentials.
7. Avoid duplicate memory entries.
8. Use simple, clear wording.

---

## Future Memory Ideas

Add more details over time for:

- Reusable n8n node templates
- Airtable CRM field standards
- Supabase table naming standards
- Common API error fixes
- Preferred Slack message templates
- Telegram bot command patterns
- Portfolio case study examples
- AI prompt templates
- Testing checklists
