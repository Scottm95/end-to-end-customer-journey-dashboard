# End-to-End Customer Journey Dashboard (Power BI)

## Overview
This Power BI dashboard provides a full end-to-end analysis of customer journeys, covering all interactions, behaviours, and key risk indicators across the lifecycle.  
It brings together operational, financial, compliance, and vulnerability insights into a single reporting solution used by QA teams, Compliance, and Senior Leadership.

The dashboard spans seven interactive pages:

1. Summary Overview  
2. Communications  
3. Payments  
4. Vulnerability  
5. Outcomes  
6. Fail Reasons  
7. Remediation Details 


This project represents a complete BI case study: data cleaning, modelling, KPI design, DAX measure creation, and multi-page visual storytelling.


## Business Context
The End-to-End (E2E) audit process reviews every interaction a customer has with the business, including contact history, payments, communications, vulnerability disclosures, and account actions.

The dashboard is used by:
- Quality Assurance teams  
- Compliance teams  
- Senior Leadership  
- Operational managers  
- Customer vulnerability teams  

It provides a holistic view of customer journeys and reveals where processes succeed or fail, enabling targeted improvement and risk reduction.

---



## Purpose of the Dashboard
The dashboard was created to:

- Provide a single source of truth for E2E audit results  
- Identify root causes of failure across multiple categories  
- Highlight operational risks (arrears, complaints, adherence issues)  
- Improve visibility of vulnerable customer handling  
- Measure communication strategy effectiveness  
- Support targeted training and coaching  
- Highlight journeys requiring remediation  
- Enable vulnerability-specific filtering across all pages  

The goal is to support continuous improvement, reduce customer detriment, and monitor performance against regulatory expectations.

---


## Tools & Technologies Used
- Power BI Desktop  
- Power Query (ETL and data transformation)  
- DAX Measures  
- SharePoint (data source)  
- Power BI Data Model  
- Data categorisation schema  

---


## Data Pipeline & Transformation

### 1. Data Source
Operational E2E audit data stored on SharePoint, including:
- Customer/account details  
- Interaction history  
- Communication events  
- Arrears and payment behaviour  
- Vulnerability disclosures  
- Audit scores and outcomes  
- Remediation notes  
- Fail reasons by category  

### 2. Power Query (ETL)
Transformations included:
- Correcting data types  
- Standardising category labels  
- Removing confidential identifiers  
- Splitting multi-select audit fields  
- Merging multiple SharePoint lists  
- Creating vulnerability groupings  
- Extracting numeric fields  
- Cleaning free-text remediation notes  

### 3. Data Model
- Fact table for E2E audit results  
- Lookup tables for categories, outcomes, vulnerability types  
- Relationships defined via account key  
- Hidden technical columns removed  
- Filters designed to propagate correctly between pages  

### 4. Measures (DAX)
DAX used extensively to create KPIs across communications, arrears, payments, vulnerability, fail reasons, and remediation.

---

## DAX Measures

Below are core DAX measures powering the dashboard, grouped by domain.  
These highlight the analytical logic used to generate key insights.

### Customer Status & Arrears

**Total Accounts**  
Counts the number of customer accounts audited.

**% Customers in Arrears**  
Percentage of accounts currently in arrears.  
Used in both the Summary and Payments pages.

**Average Days to Enter Arrears**  
Measures the average time customers take to fall into arrears.

**% Customers in Repeat Arrears**  
Percentage of customers who have fallen into arrears more than once, indicating persistent affordability issues.

### Vulnerability

**% Vulnerable Customers**  
Percentage of audited customers identified as vulnerable.

**% Vulnerable and in Arrears**  
Combines vulnerability and arrears to highlight high-risk groups.

**% in Financial Difficulty at Time of Sale**  
Measures how many customers were already struggling financially at the point of sale.

### Communications

**% Emails Sent**  
Percentage of required emails successfully sent.

**% SMS Sent**  
Percentage of required SMS messages sent.

**% System Communications Updated**  
Measures whether system-generated communications were correctly updated.

**% Statutory Comms Sent**  
Percentage of statutory communications (NOD, NOSIA, NOT) sent when required.

### Payments & Adherence

**Payment Arrangement Pass Rate %**  
Percentage of Payment Arrangements where customers adhered to agreed terms.

**Promise to Pay Pass Rate %**  
Percentage of Promises to Pay that were fulfilled.

### Remediation & Outcomes

**Remediation Rate %**  
Percentage of journeys requiring remediation.

**% of Open Complaints**  
Percentage of customers with an unresolved complaint at the time of audit.

---


## Dashboard Pages & Insights

### 1. Summary Overview
High-level metrics including:
- Last refreshed date  
- Total accounts audited  
- Total arrears balance  
- % vulnerable customers  
- % in arrears  
- Remediation required rate  
- Open complaints  
- Pass rate  
- Account status breakdown  

Designed for operational leads and senior stakeholders.

---


### 2. Communications
Shows whether required communications were completed correctly:
- SMS, email, system comms, and statutory comms percentages  
- Visual breakdown of yes/no/N/A compliance  

Ensures communication strategy and FCA obligations are being met.

---


### 3. Payments
Deep dive into customer payment behaviour:
- Total arrears balance  
- Total PTPs, PAs, and holds  
- Payment adherence rates  
- Average days to enter arrears  
- Repeat arrears rate  
- Status-level breakdown of holds/PTPs/PAs  

Supports improvements in payment handling and collections strategy.

---


### 4. Vulnerability
Understanding customer vulnerability:
- % vulnerable customers  
- % vulnerable & in arrears  
- Vulnerability categories (financial, emotional wellbeing, health, life events, capacity, accessibility)  
- Vulnerability slicer applied across pages  

Used heavily for Consumer Duty/FCA reporting.

---


### 5. Outcomes
Shows whether customers received good outcomes:
- Overall outcome distribution   
- Outcomes by category  

Used to ensure fair treatment and regulatory alignment.

---


### 6. Fail Reasons
Drilldown into common fail reasons:
- Primary fail reasons  
- Fail reasons by category  
- Supports targeted coaching and process redesign  

---


### 7. Remediation Details
Displays all accounts requiring remediation:
- Account reference  
- Remediation required flag  
- Full remediation notes in matrix  
- Remediation proportion metric  

Used for manual follow-up and reducing customer detriment.

---


## Files Included
- 'README.md' - Project overview and documentation
- /img
overview.png
communications.png
payments.png
vulnerability.png
outcomes.png
fail_reasons.png
remediation.png

- 'end to end raw data sample' - Fully anonymised dataset used for building the dashboard.

---



## Key Learnings & Impact
This project demonstrates:

- Multi-page Power BI dashboard design  
- Advanced use of DAX for business KPIs  
- Robust data modelling  
- End-to-end ETL pipeline using Power Query  
- Clear analytical storytelling  
- Strong domain understanding (arrears, vulnerability, Consumer Duty, payments)  
- Ability to communicate insights to technical and non-technical audiences  

The dashboard has supported:
- FCA reporting
- Improved training and coaching  
- Identification of high-risk customer journeys  
- Better monitoring of vulnerable customers  
- More consistent communication and payment handling  
- Faster identification of journeys requiring remediation  

---

