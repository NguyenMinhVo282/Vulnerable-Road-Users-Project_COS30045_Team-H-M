# Vulnerable-Road-Users-Project_COS30045_Team-H-M
# Vulnerable Road Users in Australia: An Interactive Analysis of Road Crash Hospitalisations & Healthcare Burden (2011–2021)

**COS30045 – Data Visualisation Project | Team H&M (Fall Semester 2026)**

## Team Members
* **Vo Nguyen Minh** (`105505636 / SWS01230`) – Data Pipeline (KNIME), Visualisation Design, D3.js Implementation.
* **Truong Viet Hung** (`104775470 / SWS01012`) – Analytical Logic, Visualisation Design & Quality Assurance Lead

## Project Overview & Big Idea
While vehicle safety engineering has significantly improved protection for people inside cars, **Vulnerable Road Users (VRUs)**—**pedestrians, pedal cyclists, and motorcyclists**—lack external physical protection and bear a disproportionate share of severe road trauma.

* **Core Question (Big Idea):** *Who carries the greatest burden of road-related hospitalisations in Australia, and which vulnerable road-user groups warrant greater priority in road safety planning?*
* **Primary Audience:** State and Territory Road Safety Policy Planners.
* **Secondary Audience:** Road Safety Advocacy Organisations.

## Three Connected Research Questions
1. **Temporal Trends (2011–2021):** How have hospitalised road injury patterns and Year-on-Year (YoY) growth rates changed across road-user groups, accounting for 2012 (VIC) and 2017 (NSW) reporting breaks?
2. **Demographic Differences:** Which age groups and gender cohorts experience the greatest burden of hospitalised injuries within each VRU category?
3. **Healthcare Burden:** How does hospital-care duration (`Total Bed Days`, `Average Bed Days per case`) and supplementary in-hospital fatality rate differ between VRUs and car occupants?

## Data Pipeline & Preliminary EDA (KNIME)
* **Source:** Bureau of Infrastructure and Transport Research Economics (BITRE) – *National Hospitalised Injury Dataset (2011–2021)* (`raw` worksheet, 117,919 records).
* **Reproducible Workflow (`/knime`):** Built a 4-stage KNIME Analytics pipeline (Profiling → Cleaning & Feature Engineering → Multi-Branch Aggregation → Validation) isolating **406,646 valid road-user hospitalisation cases** and **1,981,281 total bed days**.
* **Key Insights:**
  * **Pedal Cyclists** surged **+50.97%** (2011–2021), spiking **+14.12%** during 2020 lockdowns while car driver cases fell `-9.61%`.
  * **Older Pedestrians (65+)** account for **23.1%** of all pedestrian hospitalisations (`3,870` cases in the `75+` cohort alone).
  * **Healthcare Burden Paradox:** Pedestrians average **9.01 bed days per case** (nearly 2× car drivers at `4.54` days) and a **1.93%** in-hospital fatality rate (~4× car drivers at `0.49%`).

## Repository Structure
* `data/` – Validated analytical CSV datasets (`q1_temporal_trends.csv`, `q2_demographics.csv`, `q3_healthcare_burden.csv`).
* `knime/` – Reproducible 4-stage KNIME Analytics workflow (`.knwf` with embedded data).
* `docs/` – Stand-up 1 presentation slides and Design Book draft (Sections 1 & 2).
* `css/` & `js/` – Modular D3.js visualisation source code *(in progress – Week 11)*.
