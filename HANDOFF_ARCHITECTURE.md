# Handoff Architecture Preview

This preview explains the workflow shape behind the `WhatsApp Intake + Handoff Kit for Agent Builders`.

It is intentionally not the full paid schema. The goal is to help builders see why the offer is not a generic chatbot prompt.

## Core Idea

A WhatsApp intake agent is useful only if it leaves a human operator with something actionable.

The chat is the surface. The handoff packet is the product.

```text
messy WhatsApp message
  -> normalized intake state
  -> missing-field list
  -> risk and consent flags
  -> one safe next question OR human handoff
  -> coordinator-ready summary
```

## Minimal Handoff Packet

The smallest useful packet has these sections:

| Section | Purpose |
|---|---|
| `captured` | Facts already collected from the conversation |
| `missing` | Fields still needed before a coordinator can act |
| `risk_flags` | Medical, privacy, payment, urgency, or consent issues |
| `confidence` | Field-level confidence rather than one global score |
| `next_question` | One question that reduces operator work |
| `next_human_action` | What a human coordinator should do next |
| `do_not_do` | Actions the agent must not take autonomously |
| `source_trace` | Message snippets or IDs that justify the packet |

## Example Packet Shape

```json
{
  "preview_only": true,
  "captured": {
    "destination": "Seoul",
    "timeline": "next month",
    "interest": "skincare clinic chat planning",
    "user_boundary": "avoid medical advice"
  },
  "missing": [
    "exact_travel_dates",
    "preferred_language",
    "budget_range",
    "preferred_area"
  ],
  "risk_flags": [],
  "confidence": {
    "destination": "high",
    "timeline": "medium",
    "interest": "medium",
    "budget_range": "missing"
  },
  "next_question": "What are your exact travel dates, preferred language, budget range, and preferred Seoul area?",
  "next_human_action": "Wait for one more intake answer, then prepare a coordinator review note.",
  "do_not_do": [
    "do not diagnose",
    "do not recommend procedures",
    "do not choose clinics",
    "do not handle payments",
    "do not contact clinics autonomously"
  ],
  "human_review_required": true,
  "send_allowed": false,
  "source_trace": [
    "Hi, I am visiting Seoul next month...",
    "I have sensitive skin and want to avoid medical advice."
  ]
}
```

## Routing Logic

Use simple routing before trying to make the agent clever.

| Condition | Action |
|---|---|
| Low-risk details are missing | Ask one safe next question |
| Enough logistics are known | Create a coordinator handoff note |
| Medical advice, diagnosis, procedure choice, clinic choice, urgency, payment, refund, private documents, or health data appears | Immediate human review |
| JSON parse or validation fails | Human review |
| Consent is unclear | Ask for consent or hand off |

## Why This Matters

Most demo bots optimize for replies. Real operators care about what happens after the reply.

Weak output:

```text
The user wants skincare help in Seoul. Staff should check.
```

Useful output:

```text
Known: Seoul next month, skincare interest, sensitive skin, wants no medical advice.
Missing: exact dates, language, budget, area, consent.
Risk: medical-adjacent; do not recommend procedures.
Next: ask one logistics question before coordinator review.
```

The second version lets a person continue without rereading the whole chat.

## Implementation Pattern

For n8n, Make, Zapier, Manychat, Voiceflow, Botpress, or a custom worker:

1. Normalize inbound message fields.
2. Pass current message plus known state to the LLM step.
3. Ask for structured output only.
4. Parse and validate the packet.
5. Route by missing fields, risk flags, and consent.
6. Store the packet in a CRM, sheet, database, or ticket.
7. Let a human coordinator approve any clinic-facing draft.

The public preview includes `kbeauty_whatsapp_intake_lite.n8n.json` as a safe placeholder skeleton. It contains no live send node, API key, webhook secret, clinic data, patient data, or production prompt.

## Paid Kit Boundary

The paid kit adds the complete production prompt, full handoff schema, bilingual clinic inquiry draft patterns, install notes, and safety boundary files.

This preview is only enough to evaluate the architecture and decide whether the full implementation pack is useful.
