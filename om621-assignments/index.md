---
title: "OM 621 — Assignments"
layout: single
classes: wide
toc: true
toc_label: "On this page"
permalink: /om621-assignments/
description: Delay analysis and cost-forecasting insights from my OM 621 assignments, with a short story, highlights, methods, visuals, and how to run the work.
---

This page summarizes my work for **OM 621 — Advanced Visual Analytics** (Assignments 2 & 3 combined) and links to my GitHub repository and dashboard.

**Repo:** <https://github.com/Brendalaime/om621_assignments>  
**Combined notebook:** [`notebooks/OM621_A2_A3_Combined.ipynb`](https://github.com/Brendalaime/om621_assignments/blob/main/notebooks/OM621_A2_A3_Combined.ipynb)  
**Power BI:** [`pbi/OM621_Assignment4.pbix`](https://github.com/Brendalaime/om621_assignments/blob/main/pbi/OM621_Assignment4.pbix)

---

## 3–5 minute video (coming soon)
I’ll add the link here once I upload my Zoom/YouTube recording.

---

## What this project is
I answer a practical question: **When do invoices actually land, and how does timing/cost differ by mode?**  
This matters for **budgeting**, **accrual timing**, and short-term **cost forecasts**.

The work combines:
- A clean **delay** feature (`invoice_date − shipping_date`, in days)
- **Distribution views** of delay (region, site, mode)
- **Time-series** of invoice amounts (lines grouped by year, faceted by mode)
- A short set of **actionable takeaways** for the supply-chain director and finance

---

## My 3-minute story (condensed)
- **Who cares:** Director of Supply Chain, analysts, and my consulting manager.  
- **Problem:** Invoice timing is uneven and varies by transportation mode → noisy monthly costs.  
- **What I bring:** A clear picture of typical delay and the risk of outliers, plus a mode-aware read of monthly patterns.  
- **So what:** Use **median delay by mode** for accruals, add buffer for LCL/FCL, and **forecast per-mode** before summing totals.

---

## Highlights
- **Delay differs by mode.** Containers (LCL/FCL) have **longer, wider** delays; parcel/air is **faster** and tighter.  
- **Patterns are mode-specific.** With **lines by year** and **facets by mode**, seasonality and trends pop out (containers trend up; parcel flatter).  
- **Budget/forecast recipe:**  
  1) Build a **monthly baseline per mode** (seasonality)  
  2) Adjust with the **recent 3–6 months** (trend)  
  3) Use **median delay by mode** for accruals; add buffer for container tails

---

## Featured figures
- **Delay by Mode**  
  ![Delay by Mode](https://raw.githubusercontent.com/Brendalaime/om621_assignments/main/plots/delay_dist_by_mode.png)
- **Invoice Time Series by Mode**  
  ![Invoice TS by Mode](https://raw.githubusercontent.com/Brendalaime/om621_assignments/main/plots/invoice_ts_by_mode.png)

---

## Methods 
1. **Data**: `data/tr_data_22_24.csv` (site, mode, region, dates, USD amounts)  
2. **Cleaning**: parsed dates; created `delay`; fixed `parcel_grund → parcel_ground`; readable `mode_label`  
3. **Visuals**: ordered horizontal boxplot for delay by mode; densities by region/site; monthly lines grouped by year, faceted by mode  
4. **Refinement**: clear titles/labels; minimal themes; export PNGs to `plots/`

---

## How to run
**Requirements:** Python 3.10+, `pandas`, `numpy`, `plotnine`  

1. Clone the repo and put the CSV at `data/tr_data_22_24.csv`  
2. Open and run `notebooks/OM621_A2_A3_Combined.ipynb` top-to-bottom  
3. Figures export to `plots/` automatically

> **Power BI:** open `pbi/OM621_Assignment4.pbix` to explore with slicers for mode/region/site.

---

## Folder structure (repo)

```text
om621_assignments/
├─ data/
├─ notebooks/
│  └─ OM621_A2_A3_Combined.ipynb
├─ plots/
├─ pbi/
│  └─ OM621_Assignment4.pbix
└─ README.md

---

## References
- Karimi, M. (2025). *Storytelling with Data; Grammar of Graphics; Visualization Refinement.*  
- McKinney, W. (2017). *Python for Data Analysis* (2nd ed.).  
- Course dataset: `tr_data_22_24.csv`.
