# Lab 3: Relate Orders, Products and Returns

**Alignment:** LO2 · K3 · A2  
**Scenario:** Meridian Retail SG stores orders, product master data, outlets and returns at different grains.

## Files

- `lab-03-related-retail-data.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-03-relationships.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-03-relationships.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-03-related-retail-data.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

A governed multi-table data model plus an extract and reconciliation sheet.

## Detailed procedure

1. **Review the four source tables.** Orders, Products, Outlets and Returns have different grains.
2. **Relate Orders to Products.** Use Product ID with many Orders to one Product.
3. **Relate Orders to Outlets.** Use Outlet ID with many Orders to one Outlet.
4. **Relate Orders to Returns.** Use Order ID and preserve the order grain.
5. **Check unmatched keys.** Use the Control sheet and a Tableau null check.
6. **Compare with an inner join.** Observe how unmatched rows and duplicated rows would affect totals.
7. **Create an extract.** Save a local extract and run a refresh.
8. **Reconcile.** Confirm Sales and Order Count match the Excel controls.

## Acceptance test

Order totals are not duplicated, unmatched keys are visible, and the extract refreshes from the supplied workbook.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
