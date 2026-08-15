# Lab 2: Build Hierarchies and Drill Paths

**Alignment:** LO1 · K1 · A1  
**Scenario:** Retail leaders need to move from national performance to region, outlet and department detail without losing context.

## Files

- `lab-02-retail-hierarchy.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-02-hierarchy.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-02-hierarchy.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-02-retail-hierarchy.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

A geographic and product hierarchy with a drillable sales-and-margin view.

## Detailed procedure

1. **Connect to the Retail_Data table.** Review geography and product levels before building the view.
2. **Create Geography hierarchy.** Region > District > Outlet Name.
3. **Create Product hierarchy.** Category > Subcategory > Product Name.
4. **Create a folder structure.** Group identifiers, geography, product, commercial measures and controls.
5. **Build Sales and Profit by Geography.** Use the Geography hierarchy and drill one level at a time.
6. **Add Profit Ratio.** Use the supplied Profit and Sales measures without changing the source grain.
7. **Test drill behaviour.** Verify totals remain stable while lower levels reveal detail.
8. **Document the hierarchy purpose.** State who uses each drill path and what decision it supports.

## Acceptance test

Both hierarchies drill in the correct order and totals remain stable at every displayed level.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
