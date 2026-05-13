# K-beauty WhatsApp Intake Bot Kit - Free Preview

Free public preview for agent builders and automation agencies evaluating a K-beauty / Korea medical-travel WhatsApp intake workflow.

This repo is intentionally limited. It shows the workflow shape, safety boundary, and a lite n8n-style skeleton without publishing the full paid kit.

Live landing page:

```text
https://elaborate-pie-7c781f.netlify.app
```

## Buyer Path

1. Inspect this public preview to confirm the niche, safety boundary, and workflow shape.
2. Read the live landing page for the full offer, deliverables, and current buying options.
3. Buy the $19 kit when you want the complete implementation assets in one ZIP.
4. Use the $149 custom setup option when you want one intake path adapted for a real client workflow.

## Who This Is For

- AI agent builders packaging vertical workflow offers
- automation agencies serving WhatsApp, LINE, Instagram, or web-form inquiry flows
- freelancers building intake and handoff systems for K-beauty, Korea medical travel, or concierge travel clients
- builders who want a concrete niche workflow instead of a generic chatbot demo

## Try The Preview

Use this sample traveler message with `SKILL.md`:

```text
Hi, I am visiting Seoul next month. I want help planning skincare clinic chats.
I have sensitive skin and want to avoid medical advice. Can you ask what info
you need from me first?
```

Expected behavior:

```text
Extract low-risk logistics only, ask one safe next intake question, and route
medical/procedure/clinic-choice/payment issues to human review.
```

## What This Preview Helps You Test

- inbound WhatsApp-style message capture
- safe field normalization
- placeholder classification
- JSON parse / validation placeholder
- human handoff routing
- next-question reply preparation
- storage placeholder
- no medical advice, clinic choice, payment handling, credential collection, or autonomous outreach

## Included Free Files

```text
SKILL.md
skills.json
llms.txt
kbeauty_whatsapp_intake_lite.n8n.json
demo_input_output.md
PAID_KIT.md
SECURITY.md
mcplug_listing.md
LICENSE.md
```

## Paid Kit

The full $19 agent-ready kit includes:

- production SKILL.md
- reusable agent prompt
- agent-readable metadata
- skills.json
- llms.txt
- install notes
- handoff JSON schema
- WhatsApp intake flow
- builder integration spec
- bilingual clinic inquiry drafts
- demo input/output
- safety boundaries

Checkout:

```text
https://kbeautytrip.lemonsqueezy.com/checkout/buy/4e42febb-e84d-4598-b5c2-0d7b35ff664b
```

Custom setup:

```text
https://kbeautytrip.lemonsqueezy.com/checkout/buy/a48de118-81aa-4ae4-af8f-2e3bd9bdce6d
```

## Why Buy The Paid Kit

Buy the paid kit when you want to stop reverse-engineering the preview and start assembling a sellable automation offer. The preview proves the public workflow shape; the paid ZIP gives you the production prompt, full handoff schema, install notes, bilingual clinic inquiry draft library, builder integration spec, demo outputs, and safety boundary files needed to package the workflow for client delivery.

For builders and agencies, the paid kit is useful because it turns a narrow vertical idea into concrete implementation material:

- a reusable intake agent prompt instead of a loose chatbot brief
- a handoff schema your automation can validate and store
- bilingual clinic inquiry drafts kept behind human review
- implementation notes for adapting WhatsApp, LINE, Instagram, web forms, or concierge inboxes
- agent-readable metadata for marketplaces, coding agents, and buyer evaluation

## Safety Boundary

This preview and the paid kit are intake and handoff workflow assets. They do not diagnose, recommend procedures, choose clinics, handle payments, collect credentials, contact clinics autonomously, or share personal/photo/health information without consent and human review.

Clinic-facing drafts in the paid kit are not send-ready by default:

```text
human_review_required=true
send_allowed=false
```

## Public Preview Use

This repo is the free public preview. Use it to inspect the workflow shape, safety boundary, agent metadata, and lite automation skeleton before buying the full kit. For the buyer-facing offer page, use:

```text
https://elaborate-pie-7c781f.netlify.app
```

## Agent Discovery

Agent-readable preview metadata is included for marketplaces and coding agents:

```text
skills.json
llms.txt
```

These files describe the limited preview only. They do not include the full paid schema, clinic drafts, install pack, or implementation notes.

## License

Files in this public preview repository are MIT licensed. The paid kit materials are not included in this repository and are not covered by this preview license.
