# NHS England: Severe Mental Illness (SMI) Health Equity & Performance Analysis

## 🎯 Project Background
NHS England manages community mental health services for approximately 400,000 people. This patient group faces a critical health inequality: they die 15 to 20 years earlier than the general population, primarily from treatable physical conditions.

To address this, the **NHS Long Term Plan** mandated a 60% national target for comprehensive annual physical health checks. This project analyzes five years of performance data to identify geographic "healthcare deserts" and provide strategic recommendations to close the equity gap.

### 📊 Key Business Metrics
| Metric | Definition | Target |
| :--- | :--- | :--- |
| **Completion Rate** | % of SMI register receiving all 6 core health checks | 60% |
| **Urban-Rural Gap** | Difference in completion rates by geographic density | < 5% |
| **SMI Register** | Total count of patients with schizophrenia, bipolar, or psychosis | N/A |

> [!TIP]
> **Technical Files:**
> * [SQL Scripts](./scripts/analysis_queries.sql): Data cleaning and metric calculation.
> * [Tableau Dashboard](https://your-link-here.com): Interactive visualization of regional disparities.

---

## 🛠️ Data Structure & Initial Checks
The analysis utilizes quarterly performance extracts (Q3 2018/19 to Q4 2023/24) across 106 Sub-Integrated Care Boards (Sub-ICBs).

### Initial Data Quality Assessment (SQL Audit)
```sql
-- Example of checking for data anomalies (Completion > 100%)
SELECT sub_icb_location_code, count_of_checks, register_size
FROM `bigquery-public-data.cms_medicare.inpatient_charges_2015` -- Replace with your actual table
WHERE (count_of_checks / register_size) > 1;
