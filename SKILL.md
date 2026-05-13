---
name: kbeauty-whatsapp-intake-preview
description: Use when previewing the shape of a K-beauty or Korea medical-travel WhatsApp intake workflow; shows safe next-question and handoff routing logic without the full paid handoff schema, bilingual clinic drafts, metadata, or implementation pack.
author: yhmxiii
version: "0.1.0-preview"
tags:
  - k-beauty
  - whatsapp
  - intake
  - medical-travel
  - automation
allowed-tools: []
argument-hint: "[traveler message or intake notes]"
---

# K-beauty WhatsApp Intake Preview

This is a free limited preview skill for builders evaluating whether a vertical WhatsApp intake workflow fits their agency offer.

Use this preview to:

1. Identify whether a traveler message belongs to K-beauty / Korea medical-travel intake.
2. Extract low-risk logistics fields only.
3. Ask one safe next question when required fields are missing.
4. Route to human review when the message touches diagnosis, procedure choice, clinic choice, urgent symptoms, payments, refunds, complications, allergies, pregnancy, medications, or recovery-flight conflicts.

## Inputs

- traveler message
- conversation notes
- known travel dates
- preferred language
- budget range
- consent status, if already known

## Outputs

- safe next intake question
- missing fields
- basic handoff flag
- safety notes

## Not Included In This Preview

- full handoff JSON schema
- English/Korean clinic inquiry drafts
- quote comparison columns
- complete agent prompt
- install notes for multiple runtimes
- agent-readable metadata
- paid support files

## Safety Rules

- Do not diagnose.
- Do not recommend procedures.
- Do not choose clinics.
- Do not handle deposits, refunds, or payments.
- Do not collect credentials.
- Do not contact clinics autonomously.
- Do not share personal, photo, passport, or health information without explicit consent and human review.

## Output Template

```json
{
  "preview_only": true,
  "intent": "kbeauty_trip_intake",
  "handoff_required": false,
  "missing_fields": [],
  "next_question": "",
  "safety_notes": [
    "No medical advice, diagnosis, procedure recommendation, clinic choice, payment handling, or autonomous outreach."
  ]
}
```

## Full Kit

The paid kit adds the production SKILL.md, agent prompt, handoff JSON schema, bilingual clinic inquiry drafts, metadata, skills.json, llms.txt, install notes, demo outputs, and safety boundaries.

Checkout:

```text
https://kbeautytrip.lemonsqueezy.com/checkout/buy/4e42febb-e84d-4598-b5c2-0d7b35ff664b
```
