# Web Analytics (GA4) KPI dashboard — Looker Studio

[![Made with Looker Studio](https://img.shields.io/badge/Made%20with-Looker%20Studio-1a73e8.svg)](#)
[![Data Source: GA4](https://img.shields.io/badge/Data-GA4-ff6f00.svg)](#)

<!-- Optional hero image -->
<!-- ![GA4 KPI dashboard cover](./ga4_kpi_cover.jpg) -->

## 📄 Report (PDF)
**View the report:** 👉 [REPORT](./looker_ga4_KPI_snufi.pdf)

---

## 📝 Description
A practical **GA4 KPI board** built in **Looker Studio** to monitor traffic, content performance, acquisition sources, device mix, and front‑end‑relevant screen profiles. The **Source** dropdown lets you segment all visuals by acquisition origin (e.g., Organic, Direct, Referral) to compare behavior and engagement across channels—ideal for quick performance triage without switching pages.

---

## 🎯 Scope highlights
- **Traffic KPIs:** Views, Users, Avg. session duration with period‑over‑period deltas.
- **Landing Pages:** Ranked table of top content by views; validate SEO and UX hypotheses.
- **Acquisition:** **Session Source** table + **Source filter** for rapid channel attribution.
- **Geography:** City‑level breakdown—useful for local campaigns and capacity planning.
- **Devices:** Device category split (**mobile/desktop/tablet**) to guide mobile‑first priorities.
- **Screen / Viewport:** Distribution of common **viewport resolutions** (e.g., 393×873, 375×812, 1920×1080) to inform responsive breakpoints and FE QA.
- **Screen Size:** Physical screen size buckets (e.g., phone vs tablet vs desktop) that help align design tokens and density decisions.

---

## 📊 Featured Visuals
- **KPI Cards & Trend mini‑charts**
  - *Views*, *Total Users*, *Avg. Session Duration*; period‑over‑period deltas to signal movement at a glance.
- **Landing Page Performance**
  - *Table* with path and views; use to prioritize content fixes and internal linking.
- **Acquisition (Source)**
  - *Source filter (dropdown)* driving all tiles; *Session Source* table for volume and engagement comparisons.
- **Geo (City)**
  - *Table/Map* of sessions by city to surface regional patterns.
- **Device Category**
  - *Pie or stacked bar* for **mobile / desktop / tablet** split; informs mobile UX and performance budgets.
- **Viewport Resolution** *(last on the **left**)*
  - *Bar list* of top **screen resolutions/viewport sizes** (e.g., 393×873, 375×812, 1920×1080); use to set **design breakpoints**, emulate devices, and target asset optimization.
- **Screen Size** *(last on the **right**)*
  - *Distribution chart* of **physical screen size classes**; great for choosing component densities, type scales, and minimum tap targets.

> 💡 **Why this matters for Front‑End development**
> - Focus QA on the **most common viewports** to catch layout regressions earlier.
> - Tune **image sizes and font scaling** for dominant resolutions to improve LCP and CLS.
> - Align **navigation and CTA placement** to mobile‑first usage when the device split skews heavily to phones.

---

## 🔧 Technologies Used
- **Looker Studio** (filters, blended data options, drill‑downs)
- **Google Analytics 4 (GA4)** as the data source

---

## 📬 Contact
For further information reach out via email/LinkedIn.