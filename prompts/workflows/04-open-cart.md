# Workflow 04: Open Cart (Dated mode)

Workflow name: `LE 04 Open Cart`. 8 emails. Emails 1 to 4 count from launch_cart_open_date,
emails 5 to 8 count back from launch_cart_close_date. Buyers never get the next email.

## Paste into the Workflow AI Builder

```
Build a workflow named "LE 04 Open Cart".
Trigger: Contact Tag added, tag "launch-list".
Add a Goal Event anywhere in the workflow: Contact Tag added "launch-buyer". When the goal is met, the contact exits the workflow.
Before every Send Email step add an If/Else: if the contact has the tag "launch-buyer", end the workflow, else continue.
Step 1: Wait until the date and time {{custom_values.launch_cart_open_date}}. If it is in the past, continue right away.
Step 2: Send Email, template "Open Cart 1".
Step 3: Wait 1 day. Send Email, template "Open Cart 2".
Step 4: Wait 1 day. Send Email, template "Open Cart 3".
Step 5: Wait 1 day. Send Email, template "Open Cart 4".
Step 6: Wait until 24 hours before {{custom_values.launch_cart_close_date}}. Send Email, template "Open Cart 5".
Step 7: Wait until 12 hours before {{custom_values.launch_cart_close_date}}. Send Email, template "Open Cart 6".
Step 8: Wait until 3 hours before {{custom_values.launch_cart_close_date}}. Send Email, template "Open Cart 7".
Step 9: Wait until 1 hour before {{custom_values.launch_cart_close_date}}. Send Email, template "Open Cart 8".
For every Wait until step: if the time is already in the past, skip that email and continue to the next Wait.
Allow re-entry: off. Do not write any email inline.
```

## Review checklist

- Goal Event on tag launch-buyer is present.
- An If/Else buyer check sits before each of the 8 emails.
- Emails 5 to 8 wait relative to the close date, not the open date.
- Past deadline waits skip the email (nobody gets "24 hours left" with 2 hours left).
- If the builder cannot do "X hours before a custom value date", note it for the phase 6 test.
