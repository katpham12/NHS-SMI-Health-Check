# **NHS England: Severe Mental Illness (SMI) Health Equity & Operational Performance Analysis**

## **Project Background**
As a Data Analyst at NHS England, this project evaluates the delivery of critical physical health checks for approximately **400,000 patients** living with severe mental illness (SMI). This cohort faces a significant health inequality, with a **life expectancy 15 to 20 years shorter** than the general population due to preventable conditions like cardiovascular disease and diabetes. The **NHS Long Term Plan** originally mandated that **60% of people on the SMI register** receive a comprehensive annual physical health check, a target that has recently been increased to **75% for the 2024/25 period**. This analysis identifies geographic "care deserts" and operational bottlenecks to provide actionable strategies for closing the mortality gap.

> [!IMPORTANT]
> **Key Business Metrics:**
> *   **Completion Rate:** The percentage of patients receiving all six core clinical elements within a 12-month period.
> *   **National Target:** 60% (Policy Mandate) and 75% (Operational Ambition).
> *   **Improvement Trajectory:** The quarterly change in completion percentage, currently averaging +0.6pp but requiring **+1.5pp to meet targets**.

---

## **The "Core Standard" Definition**
To be counted as a completed physical health check, clinicians must record **both a code and a clinical value** for all six of the following elements:
1.  **Weight:** BMI or BMI plus waist circumference.
2.  **Blood Pressure:** Systolic and diastolic recording plus pulse rate.
3.  **Blood Lipids:** Total cholesterol, HDL, and LDL results.
4.  **Blood Glucose:** Hb1Ac test or fasting plasma glucose.
5.  **Alcohol Consumption:** Formal assessment using AUDIT or FAST clusters.
6.  **Smoking Status:** Recording of current habit or ex-smoker status.

---

## **Executive Summary**
**Overview of Findings**
National completion rates have demonstrated long-term growth, rising from **32% in 2018/19 to 51% in Q4 2023/24**, though they remain significantly below the 60% mandate. The COVID-19 pandemic caused a severe **18-percentage-point decline** in Q2 2020, resulting in a cumulative care backlog of **180,000 missed checks**. Analysis reveals extreme geographic variation, with a **74-percentage-point performance gap** between the best (89%) and worst (15%) performing areas, alongside a **12-point divide** between urban and rural care delivery.

<img width="2752" height="1536" alt="unnamed (1)" src="https://github.com/user-attachments/assets/4e4d579f-cbfa-49db-b690-43dde2198d34" />

---

## **Data Structure & Initial Checks**
The dataset consists of quarterly performance extracts covering **21 reporting periods** across **106 Sub-Integrated Care Boards (Sub-ICBs)**. 
*   **Source Data:** Quarterly submissions submitted via the Strategic Data Collection Service (SDCS) and the General Practice Extraction Service (GPES).
*   **Metadata:** Mapping of Sub-ICB codes to geographic names and parent Integrated Care Boards (ICBs).
*   **Data Quality Assessment:**
    *   **Submission Trends:** Reporting completeness improved from **45% in 2018 to 78% in 2024**.
    *   **Anomalies:** Identified and normalized 12 instances where reported completion rates exceeded 100% due to duplicate counting errors.
    *   **Experimental Status:** Data remains marked as "experimental" due to a persistent **22% non-submission rate** in some regions.

---

## **Insights Deep Dive**

### **1. Operational Performance Trajectories**
*   **Post-Pandemic Plateau:** Quarterly improvement slowed from **+2.1pp pre-COVID** to just **+0.6pp currently**, pushing the expected target achievement date to **Q3 2027**.
*   **Seasonal Inefficiency:** A consistent **"year-end surge"** occurs in Q4, where rates average **8pp higher than Q1**, suggesting reactive service delivery to meet annual targets in March.

### **2. Geographic Variation & Equity**
*   **The Urban-Rural Gap:** Urban centers average **53% completion**, while rural Sub-ICBs lag at **41%** due to smaller practice sizes and transport barriers.
*   **Performance Density:** **27 Sub-ICBs** perform below **30%**, leaving roughly **100,000 patients** without adequate physical health monitoring.
*   **Proven Capability:** The top 10 Sub-ICBs average **82% completion**, proving high performance is possible through dedicated SMI clinics and named coordinators.

### **3. Data Quality & Accountability**
*   **The "Double Deficit":** Regions with the lowest completion rates (below 40%) were **2.3 times more likely** to have missing or inconsistent data.
*   **System Transition:** The retirement of manual collections in favor of **GPES automated extraction** is expected to eliminate non-submission gaps and reduce clinical burden.

---

## **Strategic Recommendations**
1.  **Launch Improvement Collaboratives:** Pair the 27 lowest-performing Sub-ICBs with top-decile performers in **12-month best-practice sharing programs**.
2.  **Transition to Quarterly Targets:** Replace annual performance reviews with **quarterly targets** to eliminate March bottlenecks and smooth capacity.
3.  **Accelerate Improvement Rates:** Triple the quarterly trajectory to **+1.5pp** through time-limited funding for workforce capacity in lagging regions.
4.  **Deploy Tailored Rural Solutions:** Close the 12-point geographic gap by utilizing **mobile health check clinics** and **community pharmacies**.
5.  **Enforce Data Accountability:** Implement **executive-level escalation procedures** for repeated non-reporters to ensure full visibility of the SMI cohort.

---

## **Assumptions and Caveats**
*   **Exclusion Policy:** Sub-ICBs that failed to submit data were **excluded from national averages** rather than treated as 0%, providing an optimistic baseline.
*   **Secondary Care Capture:** Physical health checks conducted in secondary care settings are often under-recorded in primary care systems, potentially underestimating performance by **2–5%**.
*   **Register Accuracy:** General Practice SMI registers likely **undercount the true population by 10–15%** due to coding delays or patient unregistered status.

---
## **Tools Used**
*   **Microsoft Excel:** Data cleaning, pivot tables, and exploratory analysis.
*   **SQL:** Advanced queries for trend analysis and geographic performance metrics.
*   **Tableau:** Interactive dashboards for executive-level performance monitoring.

*Created by [Your Name] - Healthcare Business & Strategy Analyst Portfolio*.
