# End-to-End Customer Journey MI Suite (Power BI)

## Overview
A 7-page Power BI MI suite analysing End-to-End (E2E) customer journey audit results. Built from SharePoint audit data to help QA, Compliance and operational stakeholders monitor outcomes, vulnerability handling, communications and remediation across the journey lifecycle.s

**Pages:** Summary - Communications - Payments - Vulnerability - Outcomes - Fail Reasons - Remediation



## Problem
- Audit results were difficult to monitor end-to-end (data spread across fields with limited drilldown).
- Stakeholders needed consistent KPIs and filtering (date + vulnerable customer flag) across the full journey.
- Remediation and risk themes needed to be surfaced quickly for follow-up and coaching.


## Approach
- **Data prep (Power Query):** cleaned and standardised fields (types, labels, null handling), and reshaped multi-value fields into detail tables for reliable analysis.
- **Model:** central `Fact_E2E` table (one row per audit/case) related to supporting detail tables via `ID` (1→many). Single-direction filtering keeps behaviour predictable.
- **Measures (DAX):** reusable KPI logic for arrears/payment indicators, vulnerability rates, communications coverage, outcomes, fail reasons and remediation rate.

## Tools
- **Power BI**
- **Power Query**
- **DAX**
- **SharePoint**


## Results
- Consolidated E2E audit reporting into a single MI suite with consistent filtering by `Created` date and vulnerable customer flag across all pages.
- Improved consistency and trust in reporting by centralising KPI definitions in DAX measures and applying clear denominator rules (excluding N/A where not applicable).
- Enabled faster identification of remediation-required cases and recurring fail themes through drilldowns by outcome, category and vulnerability grouping.




## Data model (grain & relationships)
![E2E model](https://raw.githubusercontent.com/Scottm95/end-to-end-customer-journey-dashboard/main/img/E2E_Schema.PNG)


- `Fact_E2E`: **one row per audit/case** (`ID`) and the central filtering table.
- Supporting tables capture multi-value attributes (e.g., reasons/categories) at a lower grain (**multiple rows per ID**).
- Relationships are `Fact_E2E[ID] (1) → detail[ID] (*)` with **single-direction filtering**.
- Report slicers (date + vulnerable customer flag) come from `Fact_E2E`.



## Key KPIs
A short KPI dictionary is in `metrics.md` (definitions + notes/edge cases).


## Data quality checks
Checks applied during prep are listed in `data_quality.md`.



## Screenshots
![Overview](img/overview.png)
![Communications](img/communications.png)
![Payments](img/payments.png)
![Vulnerability](img/vulnerability.png)
![Outcomes](img/outcomes.png)
![Fail Reasons](img/fail_reasons.png)
![Remediation](img/remediation.png)


## Files
- `README.md` – overview + approach + results
- `metrics.md` – KPI definitions (short dictionary)
- `data_quality.md` – cleaning/validation checks
- `img/` – screenshots + model diagram
- `data/` – anonymised sample












