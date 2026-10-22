# Workflow 01: Launch Survey (Dated mode)

Workflow name: `LE 01 Launch Survey`

## Paste into the Workflow AI Builder

```
Build a workflow named "LE 01 Launch Survey".
Trigger: Survey Submitted. Pick the launch survey (the native GHL survey whose link is in the custom value launch_survey_url).
Step 1: Add Tag "launch-survey-done".
Step 2: Update Contact Field. Set the contact field "launch_id_joined" to {{custom_values.launch_id}}.
Do not send any email or SMS. Do not add any other step. Allow re-entry: off.
```

## Review checklist

- Trigger is Survey Submitted with the native survey selected.
- Exactly 2 actions: the tag, then the field update.
- launch_id_joined uses the merge field, not a typed value.
- No email step, no SMS step.
