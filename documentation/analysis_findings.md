# ERP Procurement Exception Analysis

## Analysis #1 - Procurement Approval Status

### Objective
Understand procurement approval workflow distribution.

### Findings
- Total purchase orders analysed: 213
- Three approval statuses were identified:
  - APPROVED
  - IN PROCESS
  - INCOMPLETE
- Most purchase orders were successfully approved, with an approval rate of approximately 91%.
- A small number of purchase orders remain in process or incomplete and may require follow-up actions.

### Business Impact
Incomplete purchase orders may delay procurement activities and affect supplier fulfilment timelines.

---

## Analysis #2 - Buyer Workload Distribution

### Objective
Identify workload distribution among buyers.

### Findings
- Top buyer processed 42 purchase orders.
- Second buyer processed 40 purchase orders.
- Third buyer processed 37 purchase orders.
- The top three buyers were responsible for approximately 56% of total purchase orders, indicating a relatively concentrated workload distribution.
- Workload appears relatively concentrated among several key buyers.
- 
### Business Impact
Uneven workload allocation may create approval bottlenecks and increase operational risk during peak procurement periods.

---

## Analysis #3 - Procurement Spend by Currency

### Objective
Analyse procurement spending across different currencies.

### Findings
- Procurement activities were conducted using multiple currencies.
- Spending concentration was identified in major operating currencies.
- Currency exposure should be monitored to understand purchasing trends and exchange-rate impacts.

### Business Impact
Understanding currency-based spending patterns helps support procurement planning and financial reporting.

---

## Analysis #4 - Unapproved Purchase Order Analysis

### Objective
Identify procurement transactions that have not completed the approval process and determine potential operational bottlenecks.

### Findings
* A total of 19 purchase orders were not fully approved.
* The majority of unapproved transactions were classified as IN PROCESS.
* Buyer ID 284 had the highest number of unapproved purchase orders.
* Organisation 128 contained the largest number of unapproved purchase orders; however, this organisation also represented a significant proportion of overall procurement activity.

### Business Impact
Unapproved purchase orders may delay procurement execution and supplier fulfilment. Monitoring approval exceptions can help procurement teams identify workflow bottlenecks and improve processing efficiency.

---

## Analysis #6 - Approval Lead Time Investigation

### Objective
Investigate approval lead times between purchase order creation and approval dates.

### Findings
During the analysis, approval_date values could not be consistently converted into timestamps due to multiple date formats being identified within the dataset.
Examples included:
* MM/DD/YYYY HH:MM:SS
* YYYY/M/D 下午 HH:MM:SS
As a result, approval lead-time calculations could not be completed without additional data cleansing and standardisation.

---

## Technical Challenge

### Looker Studio Integration
While connecting BigQuery datasets to Looker Studio, dataset access errors were encountered despite:
- Successful SQL execution in BigQuery
- Correct IAM permissions
- Successful schema discovery in Looker Studio

Troubleshooting included:
- Dataset permission review
- IAM validation
- View-based testing
- Credential verification

Root cause is suspected to be related to dataset regional configuration and Looker Studio access behaviour.

### Business Impact
Inconsistent date formats can affect reporting accuracy and may lead to unreliable KPI measurements.
Data validation and standardisation should be implemented before performing approval lead-time analysis.

---
