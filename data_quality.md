

# Data Preparation & Quality (E2E MI Suite)

Preparation focuses on making SharePoint audit inputs consistent and analysis-ready so KPI logic remains stable across pages and time periods.

## Type enforcement & parsing
- Corrected data types (notably `Created` as date, plus numeric/boolean fields where applicable)
- Extracted numeric values from text fields where required for KPIs

## Standardisation & categorisation
- Standardised category labels to ensure consistent grouping over time
- Created vulnerability groupings to support reporting by vulnerability type/theme

## Data minimisation (portfolio-safe)
- Removed/anonymised confidential identifiers (customer/account identifiers)

## Multi-value fields
- Split and reshaped multi-select audit fields (e.g., fail reasons/categories) into supporting tables for accurate counting

## Free-text handling
- Cleaned free-text remediation notes for consistent display/search (where used)

## Relationship integrity
- Related supporting tables back to `Fact_E2E` via `ID` (1→many) to preserve the main audit grain and avoid duplication
- Set relationships to single-direction filtering from `Fact_E2E` to supporting tables to keep filter behaviour predictable
