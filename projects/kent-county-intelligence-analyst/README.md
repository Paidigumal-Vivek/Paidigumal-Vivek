# Kent County Sheriff's Office — Intelligence Analyst Assessment

This folder documents a completed **Computer-Aided Dispatch (CAD) Data Analysis** practical exercise for an Intelligence Analyst assessment. The work was designed around the Real Time Intelligence Center context and focused on turning one year of CAD activity into operational intelligence for command staff.

## At a glance

| Area | Result |
|---|---|
| Records analyzed | **71,864 CAD calls** |
| Townships | **26** |
| Incident types | **110** |
| Repeat addresses | **7,192** |
| BI platform | **Microsoft Power BI** |
| Primary analytical lens | Workload, response performance, temporal, geographic, deployment |

## Business / Operational Objective

The assessment asked for a data-driven overview of CAD activity to support strategic planning and resource-allocation discussions. Required baseline measures were top incident types, busiest townships, call-volume trends by date/time, and high-frequency or repeat addresses. The exercise also explicitly encouraged analysis beyond the baseline to identify findings that may warrant leadership attention. fileciteturn5file1

## Deliverables

- `assessment-brief/Practical Exercise.pdf` — original assessment brief
- `data/RAW CAD DATA.xlsx` — source CAD dataset
- `dashboard/VIVEK_Kent_Assesment.pbix` — Power BI dashboard
- `presentation/Vivek Presentation.pptx` — executive presentation
- `docs/METHODOLOGY.md` — analytical workflow and design decisions
- `docs/FINDINGS.md` — operational findings and considerations
- `docs/DATA_DICTIONARY.md` — analytical field documentation
- `docs/DAX_REFERENCE.md` — calculated-column logic and modeling notes

## Dashboard Architecture

### 01 — Executive Operational Overview

A command-level baseline view covering:

- Total calls
- Incident types
- Townships
- Repeat addresses
- Top incident types
- Top townships
- Calls by hour
- Top repeat addresses
- Township filtering

### 02 — Beyond the Baseline

Additional operational intelligence covering:

- Calls by day of week
- Priority distribution
- Response-time distribution
- Response-time groups
- Call sources
- Average response time by township
- Units assigned / deployment intensity

### 03 — Geographic Analysis

A spatial operational view using latitude/longitude with:

- Geographic incident distribution
- Unit-assignment grouping
- Township filtering
- Cross-filtering between visuals
- Dynamic titles
- Geographic drill-down capability

## Executive Findings

- **Traffic Stops** represented the highest service demand.
- **Plainfield Township** demonstrated the highest operational workload among jurisdictions.
- Call demand increased after **7:00 AM** and peaked during the **2:00 PM–8:00 PM** period.
- **Repeat addresses** highlighted recurring service demand and potential problem locations.
- **Priority 5** represented the dominant workload category.
- Most incidents were associated with **one assigned unit**.
- **Land Line, Field Initiated, and 911** were among the dominant call sources.
- Most recorded incidents fell within the shorter response-time categories; operationally meaningful missing timestamps were retained rather than automatically discarded.

## Analytical Principles

1. Start with the operational question, not the visualization.
2. Validate the structure and completeness of the source data before modeling.
3. Preserve missing operational values when missingness may itself have operational meaning.
4. Use row-level calculated columns for grouping/filtering attributes such as hour, day, response-time groups, and unit groups.
5. Combine baseline reporting with exploratory analysis to surface additional operational intelligence.
6. Translate every major finding into an operational implication or consideration.

## Portfolio Note

This repository section intentionally documents **Practical Exercise 1 — CAD / Call for Service analysis only**. The separate vehicle-intelligence exercise is excluded from this portfolio artifact.

## Confidentiality / Responsible Use

The source assessment describes the CAD data as provided for analytical evaluation. Any future public distribution of operational datasets should be reviewed for agency authorization, privacy, and information-security requirements before publication. The repository should be treated as a portfolio case study rather than an operational law-enforcement system.
