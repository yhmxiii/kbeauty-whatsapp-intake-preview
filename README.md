# K-beauty WhatsApp Intake Bot Kit - Free Preview

Free public preview for agent builders and automation agencies evaluating a K-beauty / Korea medical-travel WhatsApp intake workflow.

This repo is intentionally limited. It shows the workflow shape, safety boundary, and a lite n8n-style skeleton without publishing the full paid kit.

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

## Safety Boundary

This preview and the paid kit are intake and handoff workflow assets. They do not diagnose, recommend procedures, choose clinics, handle payments, collect credentials, contact clinics autonomously, or share personal/photo/health information without consent and human review.

Clinic-facing drafts in the paid kit are not send-ready by default:

```text
human_review_required=true
send_allowed=false
```

## Public-Repo Use

This folder can be used as a public preview repo only after Captain approval. Do not push, publish, submit, or list it externally without explicit approval for the exact platform and URL.

## Agent Discovery

Agent-readable preview metadata is included for marketplaces and coding agents:

```text
skills.json
llms.txt
```

These files describe the limited preview only. They do not include the full paid schema, clinic drafts, install pack, or implementation notes.