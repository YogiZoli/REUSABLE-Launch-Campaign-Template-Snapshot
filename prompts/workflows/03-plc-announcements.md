# Workflow 03: PLC announcements (Dated mode)

Workflow name: `LE 03 PLC Announcements`. One workflow, three dated waits.
Phase 6 test: confirm the Wait step accepts a custom value date. If it does not, fallback is a
date custom field on the contact, copied from the custom value at entry (documented in the test plan).

## Paste into the Workflow AI Builder

```
Build a workflow named "LE 03 PLC Announcements".
Trigger: Contact Tag added, tag "launch-list".
Step 1: Wait until a specific date and time. Use the custom value {{custom_values.launch_plc_1_date}}. If that date is already in the past, continue right away.
Step 2: Send Email. Use the existing email template "PLC 1 announcement".
Step 3: Wait until the date and time {{custom_values.launch_plc_2_date}}. If it is in the past, continue right away.
Step 4: Send Email. Use the existing email template "PLC 2 announcement".
Step 5: Wait until the date and time {{custom_values.launch_plc_3_date}}. If it is in the past, continue right away.
Step 6: Send Email. Use the existing email template "PLC 3 announcement".
No other steps. Allow re-entry: off. Do not write any email inline.
```

## Review checklist

- Trigger is the tag launch-list, so every PLC opt-in enters once.
- Three Wait steps, each reading its own launch_plc_N_date.
- Past date behavior: continue, do not skip the email.
- Three Send Email steps, each with a template.
