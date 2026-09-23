# AI Lead Qualification & Automated Follow-Up

An n8n workflow that captures new enquiries, updates HubSpot, uses Gemini AI to assess lead quality, and routes leads into automated Hot, Warm, or Cold follow-up paths.

## Workflow

![Lead Qualification Workflow](screenshots/lead-qualification-workflow.jpg)

## What it does

- Captures new enquiries through Tally
- Creates or updates contacts in HubSpot
- Uses Gemini AI to analyze lead information such as budget and urgency
- Classifies leads as Hot, Warm, or Cold
- Sends immediate alerts for Hot leads
- Sends scheduled follow-ups for Warm leads
- Places Cold leads into a nurture path
- Reduces manual CRM updates and repetitive follow-up work

## Architecture

Tally → HubSpot → Gemini AI → JavaScript parsing → Lead classification → Follow-up path

## Tech stack

- n8n
- Tally
- HubSpot
- Google Gemini
- JavaScript
- Gmail

## Repository structure

```
workflow/
  lead-qualification.json

screenshots/
  lead-qualification-workflow.jpg

docs/
  architecture.md

SECURITY.md
```

## Public workflow

The workflow JSON in this repository is sanitized for portfolio sharing. Credentials, webhook identifiers, internal workflow metadata, and private connection details have been removed or replaced with placeholders.

## About

Built as an example of how AI and workflow automation can help sales teams respond faster, keep CRM data organized, and prioritize incoming opportunities.

More automation work:

- Portfolio: https://ojo-israel-portfolio.lovable.app
- LinkedIn: https://www.linkedin.com/in/ojo-israel-ai-and-workflow-automation

---

**Built by Ojo Israel — AI & Workflow Automation Specialist**