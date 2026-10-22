# Module: Evergreen mode (build after Dated mode works)

Same templates, same tags. Time counts from the contact's own join date instead of the launch dates.
Keep these workflows in Draft while a Dated launch runs.

## Paste into the Workflow AI Builder: evergreen announcements

```
Build a workflow named "LE 03E Evergreen PLC Sequence". Keep it in Draft.
Trigger: Contact Tag added, tag "launch-list".
Step 1: Wait 1 day. Send Email, template "PLC 1 announcement".
Step 2: Wait 2 days. Send Email, template "PLC 2 announcement".
Step 3: Wait 2 days. Send Email, template "PLC 3 announcement".
Step 4: Wait 2 days. Add the contact to workflow "LE 04E Evergreen Open Cart".
Allow re-entry: off. Do not write any email inline.
```

## Paste into the Workflow AI Builder: evergreen open cart

```
Build a workflow named "LE 04E Evergreen Open Cart". Keep it in Draft.
Trigger: added by another workflow only.
Add a Goal Event: Contact Tag added "launch-buyer", then exit.
Before every Send Email step add an If/Else: if the contact has the tag "launch-buyer", end the workflow.
Send Email "Open Cart 1". Wait 1 day. "Open Cart 2". Wait 1 day. "Open Cart 3". Wait 1 day. "Open Cart 4".
Wait 2 days. "Open Cart 5". Wait 12 hours. "Open Cart 6". Wait 9 hours. "Open Cart 7". Wait 2 hours. "Open Cart 8".
Allow re-entry: off. Do not write any email inline.
```

## Module slot

"WhatsApp (pull model)": empty, parked. No templates, no flow.
