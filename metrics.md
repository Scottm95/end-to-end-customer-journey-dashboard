

# KPI Dictionary (E2E Customer Journey MI Suite)

Definitions are written in business terms; KPI logic is implemented as DAX measures to keep calculations consistent across pages.  
**Grain:** `Fact_E2E` is one row per audited journey/case (`ID`). Date filtering uses `Created`.

| KPI | Definition | Calculation notes (plain English) | Used on page(s) |
|---|---|---|---|
| Total Accounts (Audited) | Number of audited journeys/cases. | Distinct count of `ID`. | Summary, Payments |
| % Customers in Arrears | % of audited cases that are in arrears at the time of audit. | Numerator: cases flagged “in arrears”. Denominator: total audited cases (`ID`). | Summary, Payments |
| Average Days to Enter Arrears | Average number of days taken to enter arrears (where applicable). | Average over valid records only (exclude blanks / N/A). | Payments |
| % Customers in Repeat Arrears | % of audited cases with repeat arrears. | Numerator: cases flagged repeat arrears. Denominator: total audited cases (`ID`). | Payments |
| % Vulnerable Customers | % of audited cases flagged as vulnerable. | Numerator: vulnerable flag = Yes. Denominator: total audited cases (`ID`). | Summary, Vulnerability |
| % Vulnerable and in Arrears | % of audited cases that are both vulnerable and in arrears. | Numerator: vulnerable = Yes AND in arrears = Yes. Denominator: total audited cases (`ID`). | Summary, Vulnerability, Payments |
| % in Financial Difficulty at Time of Sale | % of audited cases where financial difficulty was present at point of sale. | Numerator: financial difficulty at sale = Yes. Denominator: total audited cases (`ID`). | Vulnerability |
| % Emails Sent | % of required email communications successfully sent. | Denominator excludes N/A / “not required” cases. | Communications |
| % SMS Sent | % of required SMS communications successfully sent. | Denominator excludes N/A / “not required” cases. | Communications |
| % System Communications Updated | % of applicable cases where system communications were correctly updated. | Denominator excludes N/A / “not applicable” cases. | Communications |
| % Statutory Comms Sent | % of required statutory comms sent (e.g., NOD/NOSIA/NOT). | Denominator excludes N/A / “not required” cases. | Communications |
| Payment Arrangement Pass Rate % | % of payment arrangements adhered to (pass). | Denominator excludes N/A (cases with no applicable arrangement). | Payments |
| Promise to Pay Pass Rate % | % of promises to pay fulfilled (pass). | Denominator excludes N/A (cases with no applicable PTP). | Payments |
| Remediation Rate % | % of audited cases requiring remediation. | Numerator: remediation required = Yes. Denominator: total audited cases (`ID`). | Summary, Remediation |
| % of Open Complaints | % of audited cases with an open complaint at the time of audit. | Numerator: open complaint = Yes. Denominator: total audited cases (`ID`). | Summary, Outcomes |

