# Security And Safety Notes

This public preview contains no secrets, API keys, webhook URLs, account IDs, credentials, clinic data, patient data, or live send nodes.

## What The Preview Must Not Do

- Do not send WhatsApp messages.
- Do not contact clinics.
- Do not store personal or health data in a public system.
- Do not provide medical advice.
- Do not recommend procedures.
- Do not choose clinics.
- Do not handle deposits, refunds, or payment disputes.
- Do not collect passwords, API keys, card details, passport scans, or medical records.

## Paid Kit Safety Defaults

The paid kit treats clinic-facing drafts as drafts only:

```text
human_review_required=true
send_allowed=false
```

Any implementation must add its own privacy, consent, provider, and compliance review before handling real traveler data.