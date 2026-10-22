# Workflow 05: Buyer Suppression

Workflow name: `LE 05 Buyer Suppression`

## Paste into the Workflow AI Builder

```
Build a workflow named "LE 05 Buyer Suppression".
Trigger: Order Submitted (or Payment Received). Filter: the product is the launch offer product.
Step 1: Add Tag "launch-buyer".
Step 2: Update Contact Field. Set "launch_id_bought" to {{custom_values.launch_id}}.
Step 3: Remove from Workflow: "LE 04 Open Cart".
Step 4: Remove from Workflow: "LE 04E Evergreen Open Cart".
No email in this workflow. Allow re-entry: on (one contact can buy in several launches).
```

## Review checklist

- Trigger is filtered to the offer product, not every order.
- Tag first, then the field, then both removals.
- Re-entry on.
