# Lab 6: Filter, Group and Set Customer Segments

**Alignment:** LO3 · K4 · A3  
**Scenario:** The loyalty team wants a stable business grouping plus a dynamic high-value customer cohort.

## Files

- `lab-06-customer-segments.xlsx` — learner starter workbook with realistic synthetic data.
- `sample/lab-06-groups-sets-filters.twb` — editable Tableau workbook definition; reconnect if Tableau prompts for the local Excel path.
- `sample/lab-06-groups-sets-filters.twbx` — packaged Tableau sample containing the workbook and a copy of the Excel data.
- `completed/lab-06-customer-segments.xlsx` — completed evidence example and acceptance summary.

All names and transactions are fictional. No personal or operational data is included.

## Business output

A segment view using context filters, grouped categories and a top-customer set.

## Detailed procedure

1. **Connect to Customer_Orders.** Review customer, period, segment and profitability fields.
2. **Create Business Segment group.** Combine Micro and Small into SME; retain Mid-Market and Enterprise.
3. **Create a date filter.** Limit analysis to a selected rolling period.
4. **Create a context filter.** Make the selected Region the context for Top N analysis.
5. **Create High-Value Customer set.** Top 20 customers by Sales within the context.
6. **Compare IN versus OUT.** Show Profit Ratio and Order Frequency by set membership.
7. **Add a measure filter.** Exclude customers with non-material sales only when justified.
8. **Explain the cohort.** Document how filter order affects membership.

## Acceptance test

The high-value set responds to the selected period and the business grouping is explainable from the source fields.

## Evidence to retain

- Packaged Tableau workbook (`.twbx`) with the required sheets/views.
- Screenshot of the principal result with the filter state visible.
- Reconciliation note against the Excel `Control` sheet.
- Two-sentence interpretation: observation, business meaning, limitation and next action.
