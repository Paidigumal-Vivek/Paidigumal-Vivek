# Methodology

## 1. Assessment framing

The assessment positioned the analyst within a Real Time Intelligence Center and provided one year of CAD data. Command staff requested an evidence-based overview to inform strategic planning and resource allocation. The required baseline measures were top incident types, busiest townships, call-volume trends by date/time, and high-frequency or repeat addresses. fileciteturn5file1

## 2. Data understanding

The first step was to review the available CAD fields and understand what each represented operationally before creating measures or visuals.

## 3. Data validation and preparation

The workflow included:

- Reviewing field completeness.
- Identifying missing dispatch, enroute, and arrival timestamps.
- Checking geographic coordinates for invalid values.
- Standardizing date/time fields.
- Preserving operationally meaningful missing values instead of treating every blank as a data-quality error.

## 4. Feature engineering

The Power BI model was extended with row-level analytical fields:

| Field | Purpose |
|---|---|
| Hour | Analyze intraday demand patterns |
| Month | Analyze monthly workload |
| Month Number | Chronological month sorting |
| Day Name | Weekly workload analysis |
| Day Number | Chronological weekday sorting |
| Week Type | Compare weekday/weekend patterns |
| Dispatch Delay | Measure dispatch-stage timing |
| Travel Time | Measure enroute-to-arrival timing |
| Total Response Time | Assess end-to-end response timing |
| Response Time Groups | Create operational response bands |
| Units Assigned Count | Quantify deployment intensity |
| Units Assigned Group | Compare single- vs. multi-unit activity |

## 5. Response-time grouping

Response-time categories were created to make the distribution easier to interpret operationally:

- 0–30 minutes
- 31–60 minutes
- 1–4 hours
- 4–24 hours
- >24 hours
- Missing

The `Missing` category was retained so that incomplete timestamps remained visible instead of silently disappearing from performance analysis.

## 6. Analytical perspectives

The dashboard was intentionally structured around five perspectives:

1. **Workload** — volume by incident type and township.
2. **Temporal demand** — hour, day, week type, and month patterns.
3. **Response performance** — response-time distribution and township comparisons.
4. **Deployment** — units assigned and assignment groups.
5. **Geography** — spatial concentration and township-level filtering.

## 7. Visualization design

The report used KPI cards for executive orientation, bar/column charts for ranking and distribution, line-style temporal views where appropriate, and a geographic map for spatial analysis. Township slicers and cross-filtering were included to allow leadership to move from county-level patterns to localized questions.

## 8. Intelligence translation

The objective was not simply to report counts. Each major analytical finding was paired with an operational interpretation, such as patrol deployment alignment, recurring-location monitoring, or review of townships with comparatively longer average response times.

## 9. Quality and limitations

This was an assessment dataset and should not be interpreted as a production operational intelligence system. Findings describe patterns in the provided reporting period. Missing timestamps, coordinate quality, and the absence of contextual variables such as staffing levels or incident outcomes limit causal interpretation.

## Reproducibility

The Power BI file contains the completed model, calculated fields, visuals, filters, and interactive report pages. The raw workbook is preserved as a separate source artifact for traceability.
