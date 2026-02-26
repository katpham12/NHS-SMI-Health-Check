# **Closing the 20-Year Mortality Gap: Strategic Analysis of NHS England Physical Health Checks for Severe Mental Illness**

## **Project Background**
In the UK, people living with severe mental illness (SMI)—such as schizophrenia and bipolar disorder—face a staggering health inequality: they die **15 to 20 years earlier** than the general population. Two-thirds of these premature deaths are caused by preventable physical conditions like cardiovascular disease and diabetes. 

To address this, the **NHS Long Term Plan** mandated a **60% national target** for comprehensive annual physical health checks (the "Core Standard") for all patients on the SMI register. As a Strategy and Operations Analyst, this project evaluates five years of performance data (2018–2024) across **106 Sub-Integrated Care Boards (Sub-ICBs)** to identify regional "care deserts" and provide actionable recommendations to reach the updated **75% coverage goal**.

> [!TIP]
> **Primary KPI:** The Physical Health Check Completion Rate measures the % of patients receiving all six core clinical elements: Weight, Blood Pressure, Blood Lipids, Blood Glucose, Alcohol Assessment, and Smoking Status.

---

## **Interactive Performance Dashboard**
This analysis is supported by an interactive Tableau dashboard designed for senior stakeholders to track national progress and regional variance.

**[📊 View the Full Interactive Dashboard on Tableau Public](https://public.tableau.com/app/profile/kat.pham/viz/NHS_17696098251970/Dashboard1)**

*The dashboard includes executive KPI cards, national trend lines with COVID-19 annotations, and a geographic performance map of England’s Sub-ICBs.*

---

## **Executive Summary**
**National performance has plateaued below mandate, driven by extreme geographic inequality.** 
While national completion rates grew from **32% in 2018/19 to 51% in Q4 2023/24**, progress remains 9 percentage points below the 60% mandate. The COVID-19 pandemic caused a sharp **18-percentage-point decline** in Q2 2020, leading to a care backlog of ~180,000 missed checks. Current analysis reveals a massive **74-percentage-point performance gap** between the highest (89%) and lowest (15%) performing regions.

---

## **Insights Deep Dive**

### **1. National Trends & The "Post-Pandemic Plateau"**
*   **Disrupted Momentum:** Before 2020, completion rates grew at **+2.1pp per quarter**. Post-pandemic recovery has slowed to **+0.6pp per quarter**, meaning the 60% target will not be met until **late 2027** without strategic intervention.
*   **The Year-End Surge:** Data reveals a consistent seasonal pattern where Q4 completion rates are **8pp higher than Q1**. This suggests reactive service delivery to meet March financial year-end targets rather than consistent, year-round care.

### **2. Geographic Inequality & Care Deserts**
*   **The Urban-Rural Divide:** Urban centers average **53% completion**, while rural Sub-ICBs lag at **41%**. Geographic barriers, such as travel distance to GP surgeries and lower mental health service density, contribute to this 12-point gap.
*   **Systemic Underperformance:** **27 Sub-ICBs** currently perform below **30%**, proving that a quarter of the country functions as a "care desert" for SMI patients.
*   **Proven Capability:** Conversely, the top 10 performers average **82% completion**, demonstrating that high performance is operationally achievable through dedicated SMI clinics.

### **3. Data Integrity: The "Double Deficit"**
*   **Correlation of Errors:** Regions with the lowest clinical performance (below 40%) were **2.3 times more likely** to submit missing or inconsistent "experimental" data. 
*   **Visibility Gaps:** A persistent **22% non-submission rate** in certain regions hides the true health status of approximately **12,000 patients**.

---

## **Strategic Recommendations**
1.  **Paired Improvement Collaboratives:** Establish a 12-month program pairing the **27 bottom-quartile Sub-ICBs** with top-decile performers to scale successful clinical blueprints.
2.  **Quarterly Accountability Framework:** Replace annual targets with **quarterly performance reviews** to eliminate the "year-end surge" and smooth clinical capacity across the financial year.
3.  **National Acceleration Initiative:** Triple the quarterly improvement trajectory to **+1.5pp** through time-limited workforce funding for lagging regions.
4.  **Rural Care Delivery Models:** Deploy **mobile health check clinics** and utilize community pharmacies to bridge the 12-point geographic equity gap.
5.  **Automated Data Extraction:** Finalize the transition to **GPES automated systems** to eliminate the 22% non-reporting gap and reduce the administrative burden on clinicians.

---

## **Technical Summary & Assumptions**
*   **Tools Used:** Microsoft Excel (Cleaning), SQL (Performance Metrics), Tableau (Visualization).
*   **Data Structure:** Quarterly extracts covering **21 reporting periods** across **106 Sub-ICBs**.
*   **Normalization:** Completion rates exceeding 100% (data entry errors) were **normalized to 100%**.
*   **Exclusion:** Non-reporting Sub-ICBs were excluded from national averages to provide a realistic baseline of active participants.

---
*Created by Kat Schmand — Strategy & Operations Analyst Portfolio*.
