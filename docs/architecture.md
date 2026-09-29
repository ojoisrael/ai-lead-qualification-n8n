# Architecture

The workflow connects lead capture, CRM updates, AI analysis, qualification, and follow-up into one n8n automation.

## Flow

```
Tally Trigger
    ↓
HubSpot: Create or Update Contact
    ↓
Gemini AI: Lead Analysis
    ↓
JavaScript: Parse AI Output
    ↓
Switch: Hot / Warm / Cold
    ├── Hot  → Gmail notification
    ├── Warm → Wait → Follow-up email
    └── Cold → Wait → Follow-up email
```

## Step-by-step

1. **Tally Trigger** receives a new enquiry.
2. **HubSpot** creates or updates the lead contact and stores relevant lead fields.
3. **Gemini AI** evaluates the lead using budget and urgency scoring rules.
4. **JavaScript** parses the structured AI response.
5. **Switch** routes the lead based on the returned qualification.
6. **Hot leads** trigger an immediate Gmail notification.
7. **Warm leads** wait before a follow-up email is sent.
8. **Cold leads** follow a separate delayed follow-up path.

## Qualification logic

The workflow uses the following score ranges:

- **80–100:** Hot
- **50–79:** Warm
- **0–49:** Cold

Budget and urgency each contribute to the total score.

## Public workflow

The JSON in `workflow/lead-qualification.json` is a sanitized portfolio version. Live credentials, webhook identifiers, internal workflow metadata, and private connection details are not included.

Before using the workflow in a live n8n instance, reconnect the required services and replace the Tally form placeholder.
