# Learner Guide: Data Visualisation with Tableau

Course Code: TGS-2020503177  
Version: v17.0 (15 August 2026)

## Learning Outcomes

- LO1: Apply basic Tableau features for displaying information.
- LO2: Synthesise various plots to present data visually.
- LO3: Transform data to create informative and dynamic data displays.
- LO4: Create dashboards and scorecards to display internal and external benchmark data.
- LO5: Apply calculations and parameters to create interactive graphics, visuals and technical features.
- LO6: Perform analytics and communicate data limitations and interpretations of findings.

## How to Use This Guide

The PowerPoint deck is concept-led. This guide contains the detailed procedures for the ten self-contained labs. Keep the supplied Excel workbook and Tableau files together, reconcile every result, and retain your own evidence.

## Topic 01: Basic Tableau Features

Alignment: K1 · A1 · LO1

- **Visual analysis cycle:** Connect, explore, explain and refine around a decision question.
- **Dimensions and measures:** Dimensions slice the view; measures are aggregated to quantify it.
- **Discrete and continuous:** Blue headers create categories; green axes create a continuous range.
- **Workbook structure:** Worksheets build views; dashboards combine them; stories sequence insights.
- **Fields and metadata:** Names, types, roles, aliases and default properties shape every view.
- **Hierarchy:** Ordered levels let users drill from overview to operational detail.

### Lab 1: Connect and Profile Service Operations Data

**Scenario:** A customer-experience manager needs a first reliable view of service tickets across channels and regions.

**Expected output:** A connected Tableau workbook with validated field roles and a service-volume view by region and channel.

#### Detailed procedure

1. **Inspect the Scenario and Data Dictionary sheets.** Confirm the analytical grain: one row per service ticket.
2. **Connect Tableau to the Tickets sheet.** Select the supplied Excel workbook and preview field types.
3. **Correct data roles.** Set Opened Date to Date, Resolution Hours and Satisfaction Score to measures, and Ticket ID to a dimension.
4. **Create folders.** Organise Customer, Service, Location and Outcome fields.
5. **Build Service Volume by Region.** Place Region on Rows, COUNTD(Ticket ID) on Columns and Channel on Colour.
6. **Add useful context.** Show the record count, date range and a concise tooltip.
7. **Reconcile the view.** Compare Tableau's total to the Excel Control sheet.
8. **Save evidence.** Save a packaged workbook and capture the final view.

**Acceptance test:** The workbook connects without broken fields; dates and numbers have correct roles; the view reconciles to the Excel record count.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

### Lab 2: Build Hierarchies and Drill Paths

**Scenario:** Retail leaders need to move from national performance to region, outlet and department detail without losing context.

**Expected output:** A geographic and product hierarchy with a drillable sales-and-margin view.

#### Detailed procedure

1. **Connect to the Retail_Data table.** Review geography and product levels before building the view.
2. **Create Geography hierarchy.** Region > District > Outlet Name.
3. **Create Product hierarchy.** Category > Subcategory > Product Name.
4. **Create a folder structure.** Group identifiers, geography, product, commercial measures and controls.
5. **Build Sales and Profit by Geography.** Use the Geography hierarchy and drill one level at a time.
6. **Add Profit Ratio.** Use the supplied Profit and Sales measures without changing the source grain.
7. **Test drill behaviour.** Verify totals remain stable while lower levels reveal detail.
8. **Document the hierarchy purpose.** State who uses each drill path and what decision it supports.

**Acceptance test:** Both hierarchies drill in the correct order and totals remain stable at every displayed level.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Topic 02: Data Sources and Visualisation

Alignment: K3 · A2 · LO2

- **Connection strategy:** Choose live or extract by freshness, performance and governance needs.
- **Relationships:** Preserve each table's grain and combine data at analysis time.
- **Joins:** Physically combine rows; cardinality and unmatched keys determine the result.
- **Visual encoding:** Position and length usually support more accurate comparisons than area or colour.
- **Chart purpose:** Use bars for comparison, lines for time, scatterplots for relationship and treemaps for hierarchy.
- **Aggregation:** SUM, AVG, COUNT and distinct count answer different business questions.

### Lab 3: Relate Orders, Products and Returns

**Scenario:** Meridian Retail SG stores orders, product master data, outlets and returns at different grains.

**Expected output:** A governed multi-table data model plus an extract and reconciliation sheet.

#### Detailed procedure

1. **Review the four source tables.** Orders, Products, Outlets and Returns have different grains.
2. **Relate Orders to Products.** Use Product ID with many Orders to one Product.
3. **Relate Orders to Outlets.** Use Outlet ID with many Orders to one Outlet.
4. **Relate Orders to Returns.** Use Order ID and preserve the order grain.
5. **Check unmatched keys.** Use the Control sheet and a Tableau null check.
6. **Compare with an inner join.** Observe how unmatched rows and duplicated rows would affect totals.
7. **Create an extract.** Save a local extract and run a refresh.
8. **Reconcile.** Confirm Sales and Order Count match the Excel controls.

**Acceptance test:** Order totals are not duplicated, unmatched keys are visible, and the extract refreshes from the supplied workbook.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

### Lab 4: Choose and Build Decision Charts

**Scenario:** A commercial director needs comparison, trend, relationship and portfolio views for one monthly review.

**Expected output:** Four fit-for-purpose worksheets: ranked bar, quarterly line, profit-sales scatterplot and category treemap.

#### Detailed procedure

1. **Read the four management questions.** Identify comparison, trend, relationship and composition purposes.
2. **Create a ranked bar chart.** Sales by Market, coloured by Category.
3. **Create a quarterly line chart.** Sales by Order Date quarter, coloured by Category.
4. **Create a scatterplot.** Sales versus Profit by Outlet with Size by Orders.
5. **Create a treemap.** Sales by Category and Subcategory.
6. **Remove chart clutter.** Use truthful axes, readable labels and focused tooltips.
7. **Annotate one insight per view.** Separate what is observed from why it may have occurred.
8. **Validate and save.** Reconcile displayed values to the Control sheet.

**Acceptance test:** Every chart answers its stated question, uses truthful axes, and includes enough context to interpret the marks.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Topic 03: Data Transformation

Alignment: K4 · A3 · LO3

- **Analysis-ready structure:** One row is one observation; one column is one variable; one table is one grain.
- **Data Interpreter:** Removes presentation clutter from spreadsheets while preserving the underlying evidence.
- **Split and pivot:** Separate compound fields and reshape wide columns into analysis-ready rows.
- **Filter order:** Extract, source, context, dimension and measure filters do not behave identically.
- **Groups:** Combine members into a stable business category.
- **Sets:** Define a dynamic in/out population that can drive comparisons and actions.

### Lab 5: Clean, Split and Pivot Campaign Data

**Scenario:** A campaign export contains banner rows, compound location codes and monthly measures spread across columns.

**Expected output:** An analysis-ready long table with clean location fields and documented transformation checks.

#### Detailed procedure

1. **Open the messy workbook.** Note banner rows, merged cells, compound fields and monthly columns.
2. **Use Data Interpreter.** Select the detected campaign table and verify headers.
3. **Split Location Code.** Separate Region and District with a custom split on |.
4. **Create a clean Campaign Name.** Trim spaces and standardise aliases.
5. **Pivot monthly columns.** Pivot Jan 2025 through Dec 2025 into Month and Spend.
6. **Set field types.** Month is Date; Spend and Conversions are measures.
7. **Filter unusable records.** Exclude only documented blank campaign keys.
8. **Reconcile transformation.** Match the long-table spend total to the Excel Control sheet.

**Acceptance test:** The transformed data has one row per campaign-month, clean location fields, no blank campaign key and reconciled spend totals.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

### Lab 6: Filter, Group and Set Customer Segments

**Scenario:** The loyalty team wants a stable business grouping plus a dynamic high-value customer cohort.

**Expected output:** A segment view using context filters, grouped categories and a top-customer set.

#### Detailed procedure

1. **Connect to Customer_Orders.** Review customer, period, segment and profitability fields.
2. **Create Business Segment group.** Combine Micro and Small into SME; retain Mid-Market and Enterprise.
3. **Create a date filter.** Limit analysis to a selected rolling period.
4. **Create a context filter.** Make the selected Region the context for Top N analysis.
5. **Create High-Value Customer set.** Top 20 customers by Sales within the context.
6. **Compare IN versus OUT.** Show Profit Ratio and Order Frequency by set membership.
7. **Add a measure filter.** Exclude customers with non-material sales only when justified.
8. **Explain the cohort.** Document how filter order affects membership.

**Acceptance test:** The high-value set responds to the selected period and the business grouping is explainable from the source fields.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Topic 04: Dashboards and Stories

Alignment: K5 · A4 · LO4

- **Four Ws:** Who is the audience, what decision, when is it used and where is action taken?
- **Dashboard hierarchy:** Lead with decision KPIs, then trends, drivers and diagnostic detail.
- **Layout containers:** Tiled containers create predictable alignment; floating objects need deliberate control.
- **Actions:** Filter, highlight, URL, navigation, parameter and set actions create purposeful interaction.
- **Benchmark context:** Targets, prior periods and peer ranges turn values into performance signals.
- **Stories:** A sequence of story points communicates change, evidence and decision.

### Lab 7: Build an Executive Performance Dashboard

**Scenario:** Executives need one screen to monitor sales, margin, returns and target attainment across outlets.

**Expected output:** A 16:9 scorecard dashboard with KPI tiles, trend, ranked outlets, benchmark context and visible filter state.

#### Detailed procedure

1. **Define the executive decisions.** Monitor performance, locate exceptions and assign follow-up.
2. **Build KPI sheets.** Sales, Profit, Profit Ratio, Return Rate and Target Attainment.
3. **Build the trend view.** Monthly Actual versus Target with clear reference context.
4. **Build ranked outlets.** Sort outlets by target variance and highlight material exceptions.
5. **Assemble a 16:9 dashboard.** Use tiled containers and a clear visual hierarchy.
6. **Add filters.** Region, Channel and Month with visible filter state.
7. **Test device layout.** Confirm the presentation view remains readable.
8. **Run the acceptance checklist.** Reconcile totals and remove every object without a decision purpose.

**Acceptance test:** The dashboard is readable at presentation size, totals reconcile, active filters are visible and every element supports a named decision.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

### Lab 8: Add Actions and Tell a Performance Story

**Scenario:** Regional managers need to explore a dashboard and then present a concise evidence sequence to leadership.

**Expected output:** A dashboard with filter/highlight/navigation actions and a five-point performance story.

#### Detailed procedure

1. **Open the base performance views.** Identify which sheets are sources and which are targets.
2. **Add a filter action.** Select a Region to filter outlet and category detail.
3. **Add a highlight action.** Hover or select a Category to highlight across related views.
4. **Add a navigation action.** Move from executive summary to diagnostic detail.
5. **Add a safe URL action.** Open the supplied internal-style reference URL field only.
6. **Create five story points.** Situation, trend, exception, driver and recommended action.
7. **Test reset behaviour.** Users must be able to return to the full population.
8. **Record an action statement.** Name owner, next step, trigger and review date.

**Acceptance test:** Actions work from the intended source sheets, preserve context and the story ends with an evidence-backed action.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Topic 05: Calculations and Parameters

Alignment: K2 · A5 · LO5

- **Row-level calculation:** Evaluated for each record before aggregation.
- **Aggregate calculation:** Combines measures at the view's level of detail.
- **Table calculation:** Computed over the marks already returned to the visualisation.
- **Logical design:** IF, IIF and CASE translate business rules into transparent classifications.
- **Parameters:** Single values controlled by the user; pair them with calculations or actions to change behaviour.
- **Dynamic view:** A parameter can switch metrics, thresholds, reference values or dimensions.

### Lab 9: Create Dynamic Profitability Analysis

**Scenario:** Finance wants to switch between sales, profit and margin, and test which products exceed a user-defined threshold.

**Expected output:** A dynamic metric view with calculated fields, parameter controls, table calculations and a threshold filter.

#### Detailed procedure

1. **Review supplied controls.** Excel includes source totals and threshold examples.
2. **Create Profit Ratio.** SUM([Profit]) / SUM([Sales]) with a zero-safe condition.
3. **Create Selected Metric parameter.** Sales, Profit, Profit Ratio and Orders.
4. **Create Dynamic Metric calculation.** Use CASE to return the selected measure.
5. **Create Sales Threshold parameter.** Integer range 0 to 85000 with step 100.
6. **Create threshold filter.** Keep products where SUM([Sales]) is at least the parameter.
7. **Add Percent of Total.** Use a table calculation with explicit addressing.
8. **Create a dynamic title and test.** The title and marks must respond to both controls.

**Acceptance test:** Metric and threshold controls change the view correctly, formulas reconcile to Excel controls and invalid denominator cases are handled.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Topic 06: Analytics and Communication

Alignment: K1 · A6 · LO6

- **Reference context:** Average, median, target and distribution bands help the audience judge performance.
- **Trend models:** A fitted line summarises association; it does not establish causality.
- **Forecast:** Tableau extends a time series under model assumptions and expresses uncertainty.
- **Clustering:** Groups similar marks from selected features; business labels require interpretation.
- **Limitations:** Data coverage, quality, granularity, bias and model assumptions bound the conclusion.
- **Responsible narrative:** Separate observation, interpretation, recommendation and uncertainty.

### Lab 10: Analyse Trends, Forecasts and Clusters

**Scenario:** The strategy team needs a cautious outlook for outlet demand and a segmentation of store operating patterns.

**Expected output:** An analytics workbook with reference context, trend, forecast, clustering and a limitations-led decision narrative.

#### Detailed procedure

1. **Build the monthly outlet trend.** Use at least 24 complete months and show the observed period.
2. **Add average and target lines.** Label the benchmark and avoid ambiguous colours.
3. **Add a trend line.** Describe slope, fit and whether the relationship is only associative.
4. **Create a forecast.** Show prediction intervals and document horizon and seasonality assumptions.
5. **Create clusters.** Use Sales, Profit Ratio, Return Rate and Footfall; inspect cluster summaries.
6. **Name clusters cautiously.** Use business labels only after reviewing the feature profiles.
7. **Write limitations.** Cover missing drivers, aggregation, selection bias and changing conditions.
8. **Publish the decision narrative.** State observation, interpretation, recommendation, uncertainty and monitoring trigger.

**Acceptance test:** The workbook states assumptions and limitations, distinguishes association from causation, and reports at least one action with a monitoring trigger.

Evidence: packaged Tableau workbook, principal-view screenshot, Excel reconciliation, interpretation and limitation.

## Assessment Flow

1. Complete TRAQOM / SSG digital attendance.
2. Complete assessment digital attendance.
3. Sit the 60-minute Written Assessment, then the 60-minute Practical Performance assessment.
4. Upload the completed papers and evidence to the LMS.
5. Sign the Assessment Summary Record.

LMS: https://lms-tms.tertiaryinfotech.com/
