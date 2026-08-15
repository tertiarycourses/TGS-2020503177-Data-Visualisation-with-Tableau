# Lab 1: Connect and Profile Service Operations Data

**Alignment:** LO1 · K1 · A1  
**Scenario:** A customer-experience manager needs a first reliable view of service tickets across channels and regions.

## Files

- `lab-01-service-operations.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-01-service-profile.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-01-service-profile.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-01-service-operations.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

A connected Tableau workbook with validated field roles and a service-volume view by region and channel.

## Detailed procedure

1. **Inspect the Scenario and Data Dictionary sheets.** Confirm the analytical grain: one row per service ticket.
2. **Connect Tableau to the Tickets sheet.** Select the supplied Excel workbook and preview field types.
3. **Correct data roles.** Set Opened Date to Date, Resolution Hours and Satisfaction Score to measures, and Ticket ID to a dimension.
4. **Create folders.** Organise Customer, Service, Location and Outcome fields.
5. **Build Service Volume by Region.** Place Region on Rows, COUNTD(Ticket ID) on Columns and Channel on Colour.
6. **Add useful context.** Show the record count, date range and a concise tooltip.
7. **Reconcile the view.** Compare Tableau's total to the Excel Control sheet.
8. **Save evidence.** Save a packaged workbook and capture the final view.

## Acceptance test

The workbook connects without broken fields; dates and numbers have correct roles; the view reconciles to the Excel record count.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
