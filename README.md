# Closing the 20-Year Mortality Gap: NHS England Physical Health Checks for Severe Mental Illness

**Tools Used:** SQL, Tableau, Excel, AI Research Tools (Claude, NotebookLM)
**Stakeholder:** NHS England Regional Directors and Sub-ICB Performance Leads
**Dataset:** 21 quarterly reporting periods across 106 Sub-Integrated Care Boards (Q3 2018/19 – Q4 2023/24)

---

## Project Background

People living with severe mental illness (SMI) — including schizophrenia and bipolar disorder — die 15 to 20 years earlier than the general population. Two-thirds of those deaths are caused by preventable physical conditions: cardiovascular disease, diabetes, and respiratory illness.

To close this gap, the NHS Long Term Plan mandated a **60% national target** for annual physical health checks across all patients on the SMI register. This project evaluates five years of performance data to identify regional care deserts, quantify the post-pandemic recovery gap, and deliver actionable recommendations for NHS leadership targeting an updated 75% coverage goal.

Insights and recommendations are provided on the following key areas:

- **National Trends:** Pre- vs. post-COVID trajectory and the post-pandemic plateau effect
- **Geographic Inequality:** Urban-rural divide and regional care desert identification
- **Data Integrity:** Non-reporting patterns and their correlation with clinical underperformance
- **Strategic Recommendations:** Scalable interventions modeled on top-decile performers

The SQL queries used to clean and aggregate performance data can be found [here](link). Targeted SQL queries addressing regional benchmarking and trend analysis can be found [here](link). The interactive Tableau dashboard used to explore national and regional performance can be found [here](https://public.tableau.com).

---

## Data Structure and Initial Checks

The primary dataset consists of quarterly NHS extracts from NHS Digital, structured across three reporting dimensions:

- **Sub-ICB Performance Table:** Sub-ICB code, organization name, quarter, completion rate (%), patient register count, and data submission status — 2,226 records across 106 Sub-ICBs and 21 quarters
- **Clinical Elements Table:** Six core check components per record — Weight, Blood Pressure, Blood Lipids, Blood Glucose, Alcohol Assessment, Smoking Status
- **Geographic Reference Table:** Sub-ICB classification by region, urban/rural designation, and deprivation index

[Entity Relationship Diagram here]

**Data quality flags addressed during cleaning:**
- Completion rates exceeding 100% (data entry errors) were normalized to 100%
- Non-reporting Sub-ICBs were excluded from national averages to prevent downward distortion
- "Experimental" data flags were tracked separately to quantify submission inconsistency by region

---

## Executive Summary

National SMI physical health check performance has plateaued 9 percentage points below the 60% mandate, driven by extreme geographic inequality and a post-pandemic recovery that has stalled at roughly one-third the pre-COVID growth rate. While the national average rose from 32% in 2018/19 to 51% in Q4 2023/24, 27 Sub-ICBs remain below 30% — functioning as effective care deserts for vulnerable patients. The top 10 performers average 82%, proving high performance is operationally achievable; the challenge is scale, not capability.

![Dashboard Snapshot](dashboard_screenshot.png)

---

## Insights Deep Dive

### 1. National Trends and the Post-Pandemic Plateau

- **Disrupted pre-COVID momentum.** Before Q2 2020, completion rates grew at +2.1 percentage points per quarter. The COVID-19 lockdowns caused an 18pp single-quarter decline as in-person clinical checks were suspended, creating an estimated backlog of ~180,000 missed checks.
- **Recovery has stalled at one-third of pre-pandemic velocity.** Post-pandemic growth has slowed to +0.6pp per quarter. At this trajectory, the 60% mandate will not be reached until late 2027 without targeted intervention.
- **Year-end surge signals reactive, not proactive, service delivery.** Q4 completion rates are consistently 8pp higher than Q1, indicating that Sub-ICBs are responding to March financial year-end targets rather than maintaining consistent quarterly capacity. This pattern compresses clinical delivery and introduces preventable care gaps.
- **The updated 75% goal requires a structural shift.** Reaching 75% by 2026 requires tripling the current quarterly improvement rate to +1.5pp — not achievable through organic recovery alone.

[National Trend Line Visualization]

---

### 2. Geographic Inequality and Care Deserts

- **A 74-percentage-point performance gap exists across the country.** The highest-performing Sub-ICB reached 89% completion in Q4 2023/24; the lowest reached 15%. This gap is not a data artifact — it reflects structural differences in SMI service infrastructure and commissioning priorities.
- **Urban centers outperform rural Sub-ICBs by 12 points.** Urban regions average 53% completion versus 41% in rural areas. Geographic barriers — travel distance to GP surgeries, lower mental health service density — are measurable drivers of this gap.
- **27 Sub-ICBs function as care deserts.** A quarter of all Sub-ICBs currently perform below 30%, meaning tens of thousands of SMI patients are receiving no or minimal annual physical health monitoring.
- **Top-decile performance proves the model works.** The top 10 Sub-ICBs average 82% completion, driven by dedicated SMI clinics and proactive outreach models. These are scalable blueprints, not outliers.

[Geographic Performance Map]

---

### 3. Data Integrity: The Double Deficit

- **Low clinical performance correlates with low data quality.** Sub-ICBs performing below 40% were 2.3x more likely to submit missing or flagged "experimental" data, creating a compounding visibility problem: the regions most in need are also the least measurable.
- **22% non-submission rate in certain regions masks true patient risk.** Persistent non-reporting hides the health status of approximately 12,000 patients. Any national performance figure that includes non-reporters as zero is systematically understating the problem.
- **Manual data extraction is a structural bottleneck.** Current reliance on GP-submitted manual extracts introduces inconsistency at the source. The transition to GPES automated extraction is not yet complete, leaving data quality dependent on individual practice capacity.
- **Experimental data flags are geographic, not random.** Non-reporting clusters in specific regions, suggesting systemic infrastructure gaps rather than isolated compliance failures.

[Data Integrity Correlation Chart]

---

## Recommendations

Based on regional performance benchmarking and trend analysis, the following recommendations are directed at NHS England Regional Directors and Sub-ICB Performance Leads:

- **27 Sub-ICBs are below 30% with no clear recovery trajectory.** Establish a 12-month Paired Improvement Collaborative program matching bottom-quartile Sub-ICBs with top-decile performers to replicate proven SMI clinic blueprints and commissioning models.
- **The year-end surge reveals a capacity management failure, not a delivery one.** Replace annual targets with quarterly performance review cycles and rolling accountability metrics to smooth clinical delivery and eliminate reactive Q4 overloads.
- **Rural Sub-ICBs are structurally disadvantaged by geography.** Deploy mobile health check units and authorize community pharmacy delivery models for the 18 rural Sub-ICBs averaging below 41% — addressing the access barrier without requiring new GP infrastructure.
- **The 22% non-submission rate is a patient safety issue, not just a reporting one.** Accelerate GPES automated data extraction across all remaining manual-submission Sub-ICBs and set a hard non-submission threshold of 5% as a performance KPI starting FY2025/26.
- **Top-decile performers offer a replicable model, not just a benchmark.** Commission a formal capability transfer program — structured site visits, shared staffing models, and documented outreach protocols — from the top 10 Sub-ICBs to the bottom 27.

---

## Assumptions and Caveats

- **Completion rate normalization:** Rates exceeding 100% were normalized to 100% and flagged as data entry errors. These accounted for fewer than 1% of records.
- **Non-reporting exclusion:** Sub-ICBs that did not submit data in a given quarter were excluded from national average calculations. Inclusion would suppress national figures by an estimated 3-5pp.
- **Patient count proxy:** Total SMI register size was used as the denominator for all completion rate calculations; actual eligible-patient counts were not available at the Sub-ICB level for all periods.
- **COVID impact period:** Q2 2020 through Q4 2021 was treated as a disrupted recovery period and analyzed separately from pre-pandemic trend modeling to avoid skewing trajectory projections.
- **Urban/rural classification:** Designation was applied using NHS Digital's standard Sub-ICB geographic classification; some suburban Sub-ICBs may carry urban classifications despite mixed delivery challenges.
