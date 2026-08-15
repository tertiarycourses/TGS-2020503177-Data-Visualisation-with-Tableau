# Lab 9: Create Dynamic Profitability Analysis

**Alignment:** LO5 · K2 · A5  
**Scenario:** Finance wants to switch between sales, profit and margin, and test which products exceed a user-defined threshold.

## Files

- `lab-09-calculations-parameters.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-09-dynamic-profitability.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-09-dynamic-profitability.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-09-calculations-parameters.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

A dynamic metric view with calculated fields, parameter controls, table calculations and a threshold filter.

## Detailed procedure

1. **Review supplied controls.** Excel includes source totals and threshold examples.
2. **Create Profit Ratio.** SUM([Profit]) / SUM([Sales]) with a zero-safe condition.
3. **Create Selected Metric parameter.** Sales, Profit, Profit Ratio and Orders.
4. **Create Dynamic Metric calculation.** Use CASE to return the selected measure.
5. **Create Sales Threshold parameter.** Integer range 0 to 85000 with step 100.
6. **Create threshold filter.** Keep products where SUM([Sales]) is at least the parameter.
7. **Add Percent of Total.** Use a table calculation with explicit addressing.
8. **Create a dynamic title and test.** The title and marks must respond to both controls.

## Acceptance test

Metric and threshold controls change the view correctly, formulas reconcile to Excel controls and invalid denominator cases are handled.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
