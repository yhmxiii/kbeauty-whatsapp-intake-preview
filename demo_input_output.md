# Demo Input / Output

## Sample Inbound WhatsApp Message

```text
Hi, I am visiting Seoul next month. I want help planning skincare clinic chats.
I have sensitive skin and want to avoid medical advice. Can you ask what info
you need from me first?
```

## Expected Handoff JSON

```json
{
  "handoff_required": false,
  "intent": "kbeauty_trip_intake",
  "risk_level": "low",
  "known_fields": {
    "destination": "Seoul",
    "timeline": "next month",
    "skin_note": "sensitive skin",
    "user_boundary": "avoid medical advice"
  },
  "missing_fields": [
    "travel_dates",
    "preferred_language",
    "budget_range",
    "areas_in_seoul",
    "communication_goal"
  ],
  "safety_notes": [
    "Do not diagnose, recommend procedures, choose clinics, or provide medical advice."
  ]
}
```

## Expected Next-Question Reply

```text
Thanks. I can help collect trip and communication details, but I cannot provide
medical advice or recommend procedures. What are your exact travel dates,
preferred language, budget range, and preferred Seoul areas?
```

## Expected Handoff Case

If the user asks for diagnosis, procedure choice, urgent symptoms, payment
handling, or clinic-specific recommendation, set `handoff_required` to `true`
and route to the human handoff placeholder.