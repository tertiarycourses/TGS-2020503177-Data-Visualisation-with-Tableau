# Lab 5: Clean, Split and Pivot Campaign Data

**Alignment:** LO3 · K4 · A3  
**Scenario:** A campaign export contains banner rows, compound location codes and monthly measures spread across columns.

## Files

- `lab-05-messy-campaign-data.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-05-transformation.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-05-transformation.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-05-messy-campaign-data.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

An analysis-ready long table with clean location fields and documented transformation checks.

## Detailed procedure

1. **Open the messy workbook.** Note banner rows, merged cells, compound fields and monthly columns.
2. **Use Data Interpreter.** Select the detected campaign table and verify headers.
3. **Split Location Code.** Separate Region and District with a custom split on |.
4. **Create a clean Campaign Name.** Trim spaces and standardise aliases.
5. **Pivot monthly columns.** Pivot Jan 2025 through Dec 2025 into Month and Spend.
6. **Set field types.** Month is Date; Spend and Conversions are measures.
7. **Filter unusable records.** Exclude only documented blank campaign keys.
8. **Reconcile transformation.** Match the long-table spend total to the Excel Control sheet.

## Acceptance test

The transformed data has one row per campaign-month, clean location fields, no blank campaign key and reconciled spend totals.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
