---
layout: page
title: OM 621 — Assignments (Python + Power BI)
permalink: /om621-assignments/
description: Transportation Cost Estimation & Forecasting — combined A2+A3 notebook, plots, and Power BI demo.
---

> Single, cohesive page for my OM 621 work. Focus: **invoice delay** and **invoice time-series by mode** for the Transportation Cost Estimation & Forecasting case.

### Repo
- **GitHub repo:** <https://github.com/Brendalaime/om621_assignments>
- **Combined notebook:** <https://github.com/Brendalaime/om621_assignments/blob/main/notebooks/OM621_A2_A3_Combined.ipynb>
- **Dataset:** <https://github.com/Brendalaime/om621_assignments/blob/main/data/tr_data_22_24.csv>
- **Power BI:** <https://github.com/Brendalaime/om621_assignments/blob/main/pbi/OM621_Assignment4.pbix>

---

## 3–5 minute video (coming soon)
I’ll add a short walkthrough mixing slides + a quick notebook run + a fast Power BI demo.

---

## What’s inside (quick tour)
- **A2 foundations:** delay feature from dates; sanity checks; site/mode/region visuals.
- **A3 deep dive:** ordered horizontal **delay-by-mode** boxplot; **monthly lines grouped by year** faceted by mode; clearer seasonality & trend.
- **Takeaways:** container modes trend up with wider tails; parcel/air flatter. Forecast per-mode; sum to total. Use **median delay per mode** for accrual timing; buffer containers.

### Plots (thumbnails)
<p>
  <a href="https://github.com/Brendalaime/om621_assignments/blob/main/plots/delay_dist_by_mode.png">
    <img src="https://raw.githubusercontent.com/Brendalaime/om621_assignments/main/plots/delay_dist_by_mode.png" alt="Delay by Mode" width="420">
  </a>
  <a href="https://github.com/Brendalaime/om621_assignments/blob/main/plots/invoice_ts_by_mode.png">
    <img src="https://raw.githubusercontent.com/Brendalaime/om621_assignments/main/plots/invoice_ts_by_mode.png" alt="Invoice TS by Mode" width="420">
  </a>
</p>

---

## Story (my words)
- **Business pain:** late, uneven invoices make monthly close and forecasting messy.
- **Questions:** Are **delays** mode-dependent? Do **invoice amounts** show seasonality/trend we can use?
- **Findings:** yes—containers (LCL/FCL) are slower + wider tails; parcel/air are fast/tight. Containers show a rising cost trend; parcel stays flatter.
- **Action:** forecast **each mode** separately (seasonal baseline + recent trend); use **median delay per mode** for accrual timing; add buffers for container tails.

---

## How to reproduce
1. Clone the repo above.
2. Ensure the CSV is at `data/tr_data_22_24.csv`.
3. Run the combined notebook top-to-bottom; PNGs save to `plots/`.

**Python:** `pandas`, `numpy`, `plotnine` (Python ≥ 3.10).

---

## References
Karimi (2025) course materials — Storytelling with Data; Grammar of Graphics; Refinement.  
McKinney (2017) *Python for Data Analysis*.  
Course dataset `tr_data_22_24.csv` (2022–2024).
