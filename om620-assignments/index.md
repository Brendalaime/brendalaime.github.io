---
title: "OM 620 — Assignments Showcase"
layout: single
classes: wide
toc: true
toc_label: "On this page"
---

This page summarizes my work for **OM 620** (Assignments 1 & 2) and links to my GitHub repository.

**Repo:** https://github.com/brendalaime/om620-assignments  
**Combined notebook:** `notebooks/OM620_a1_a2.ipynb`

---

## What I built

- Cleaned a real transactional dataset (fixed column names, NaNs, oddities).
- Focused on **Finished Goods (FG)** and **Make-to-Stock (MTS)** items for safety stock analysis.
- Created SKU-level summary stats (min/max/mean/median/var/std + avg lead time).
- Calculated **safety stock** for **75% / 90% / 95%** service levels (z-score method).
- Added a **non-parametric** safety stock using **empirical quantiles** for robustness.
- Documented every decision in markdown so my work is reproducible and gradable.

---

## Why two methods?

- **z-based** safety stock assumes **normal demand** and is common in practice.
- **Empirical quantile** avoids strong distribution assumptions; it’s safer when demand is skewed or spiky.  
  I compute `quantile(0.95) × sqrt(lead_time)` as an alternative reference.
