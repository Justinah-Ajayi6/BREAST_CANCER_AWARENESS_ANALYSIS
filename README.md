# Breast Cancer Awareness & Screening Dashboard — Nigeria

An interactive Power BI dashboard exploring breast cancer awareness, self-examination behavior, and mammogram screening uptake across a synthetic patient dataset representative of Nigeria. The dashboard uncovers a core insight: **awareness does not reliably translate into screening action** — and shows where that gap is widest.

![Dashboard Preview](dashboard-preview.png)

## Overview

Using a 100-patient synthetic dataset, this project examines the relationship between breast cancer awareness, knowledge of breast self-examination (BSE), actual screening behavior (BSE practice and mammogram history), and the barriers patients report to accessing screening — broken down by education level, state, and demographic factors.

**Live narrative:** *Awareness ≠ Action* — mapping the gap between knowing and screening for breast cancer in Nigeria.

## Key Insights

- **Knowledge-to-action gap:** 69% of patients know about breast self-examination, but only 38% actually perform it — a 31-point gap between awareness and practice.
- **Education drives screening access more than awareness does:** Mammogram uptake rises sharply with education — 23% (Primary) → 35% (Secondary) → 52% (Tertiary) — even though patients with only primary education reported the *highest* average awareness scores. Awareness alone does not predict access.
- **Cost and access dominate as barriers** for less-educated patients, while more educated patients more often cite fear as their reason for avoiding screening — pointing to different intervention needs across groups.
- **State-level patterns vary:** Lagos leads on both awareness and mammogram uptake. Rivers state shows the highest average awareness score but comparatively lower mammogram uptake — awareness campaigns alone haven't closed the action gap there.
- Diagnosis rates are low overall (10%) and concentrated among Moderate/High risk patients, as expected from the risk model.

## Tools Used

- **Power BI** — data modeling (star schema), DAX measures, interactive visualization
- **Excel** — data cleaning, star-schema workbook preparation (Fact/Dimension tables)
- **DAX** — custom measures for awareness, screening behavior, and diagnosis rates

## Dashboard Structure

**KPI Summary**
- Average Awareness Score
- % Knows Breast Self-Examination (BSE)
- % Performs BSE
- % Ever Had a Mammogram
- % Diagnosed

**Visuals**
1. **Screening Journey: Awareness to Action** — funnel chart showing patient distribution across not-aware, aware-only, BSE-practicing, and mammogram-screened stages
2. **Mammogram Uptake by Education** — bar chart showing the socioeconomic gradient in screening access
3. **Screening Barriers by Education Level** — stacked bar chart showing which barriers (cost, access, fear, being busy) dominate at each education level
4. **Awareness Score by State** and **Mammogram Uptake by State** — state-level comparison across the dataset

## Data Model

The dataset is structured as a star schema for efficient querying and clean relationships in Power BI:

| Table | Description |
|---|---|
| `Fact_Patient` | Core patient-level records: demographics, risk factors, awareness, screening behavior, symptoms, diagnosis |
| `Dim_State` | Nigerian states represented in the dataset |
| `Dim_Education` | Education level lookup |
| `Dim_RiskCategory` | Clinical risk category lookup |

See the included `Data_Dictionary` sheet in the Excel workbook for full field definitions.

## Files in This Repository

- `breast_cancer_awareness_star_schema.xlsx` — cleaned, star-schema-structured source data with data dictionary and DAX measure reference
- `breast_cancer_awareness_dashboard.pbix` — the Power BI dashboard file
- `dashboard-preview.png` — full dashboard screenshot
- `README.md` — this file

## Note on Data

This project uses a **synthetic dataset** built to reflect realistic patterns in breast cancer awareness and screening behavior in Nigeria. It does not represent real patient records and was created for portfolio and analytical demonstration purposes.

## Author

**Justinah Ajayi**
Data Analyst | Human Physiology
[LinkedIn](https://www.linkedin.com/in/justinah-ajayi-9220a0360) · [GitHub](https://github.com/Justinah-Ajayi6)
