# Workflows 02a, 02b, 02c: PLC opt-in and gift delivery (Dated mode)

Build one workflow per PLC. Replace N with 1, 2 and 3. The three prompts are written out in full below.

## Paste into the Workflow AI Builder: PLC 1

```
Build a workflow named "LE 02a PLC 1 Opt-in and Delivery".
Trigger: Form Submitted. Pick the opt-in form on the funnel page with the slug /plc-1.
Step 1: Add Tag "launch-list".
Step 2: Add Tag "launch-plc-1".
Step 3: Update Contact Field. Set "launch_id_joined" to {{custom_values.launch_id}}.
Step 4: Send Email. Use the existing email template "PLC 1 delivery". Do not write the email inline.
No other steps. Allow re-entry: off.
```

## Paste into the Workflow AI Builder: PLC 2

```
Build a workflow named "LE 02b PLC 2 Opt-in and Delivery".
Trigger: Form Submitted. Pick the opt-in form on the funnel page with the slug /plc-2.
Step 1: Add Tag "launch-list".
Step 2: Add Tag "launch-plc-2".
Step 3: Update Contact Field. Set "launch_id_joined" to {{custom_values.launch_id}}.
Step 4: Send Email. Use the existing email template "PLC 2 delivery". Do not write the email inline.
No other steps. Allow re-entry: off.
```

## Paste into the Workflow AI Builder: PLC 3

```
Build a workflow named "LE 02c PLC 3 Opt-in and Delivery".
Trigger: Form Submitted. Pick the opt-in form on the funnel page with the slug /plc-3.
Step 1: Add Tag "launch-list".
Step 2: Add Tag "launch-plc-3".
Step 3: Update Contact Field. Set "launch_id_joined" to {{custom_values.launch_id}}.
Step 4: Send Email. Use the existing email template "PLC 3 delivery". Do not write the email inline.
No other steps. Allow re-entry: off.
```

## Review checklist

- Each trigger points at the right page form.
- Both tags present, launch-list first.
- Send Email step shows a template name, the body editor is empty.
- launch_id_joined uses the merge field.
