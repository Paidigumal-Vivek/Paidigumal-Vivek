# Data Dictionary

## Source dataset

The assessment provided one year of Computer-Aided Dispatch (CAD) data for operational analysis. fileciteturn5file1

## Core fields

| Field | Analytical role |
|---|---|
| Incident # | Unique incident/call identifier |
| Incident Date / Time | Primary temporal field |
| Incident Type | Service-demand classification |
| Address | Location-level demand analysis |
| Township | Jurisdiction/workload analysis |
| Priority | Operational urgency classification |
| Call Source | Intake-channel analysis |
| Latitude | Geographic mapping |
| Longitude | Geographic mapping |
| First Unit Dispatched Time | Dispatch-stage timestamp |
| First Unit Enroute Time | Enroute-stage timestamp |
| First Unit Arrived Time | Arrival-stage timestamp |
| Assigned Unit | Deployment/resource field |

## Derived analytical fields

| Derived field | Definition / use |
|---|---|
| Hour | Hour extracted from incident timestamp |
| Month | Month extracted from incident timestamp |
| Month Number | Numeric month used for chronological sorting |
| Day Name | Day extracted from incident date |
| Day Number | Numeric weekday used for chronological sorting |
| Week Type | Weekday/weekend grouping |
| Dispatch Delay | Dispatch timing interval |
| Travel Time | Enroute-to-arrival interval |
| Total Response Time | Total response interval used for response analysis |
| Response Time Groups | Banded response-time categories |
| Units Assigned Count | Count of assigned units |
| Units Assigned Group | Deployment-intensity grouping |

## Response-time groups

- 0–30 minutes
- 31–60 minutes
- 1–4 hours
- 4–24 hours
- >24 hours
- Missing

## Data-quality notes

The analysis identified missing operational timestamps and coordinate issues. Missing response timestamps were retained where appropriate because missingness may reflect operational circumstances. Invalid geographic coordinates were excluded from geographic visualization so they would not distort the map.
