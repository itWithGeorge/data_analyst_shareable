# Manufactoring dashboard — BI Analytics in Looker Studio

[![Made with Looker Studio](https://img.shields.io/badge/Made%20with-Looker%20Studio-1a73e8.svg)](#)
[![Data Source: CSV/Sheets](https://img.shields.io/badge/Data-CSV%20%7C%20Sheets-4caf50.svg)](#)

<!-- Optional hero image -->
<!-- ![Dashboard cover](./manufactoring_plant.jpg) -->

## 📄 Report (PDF)
**View the report:** 👉 [REPORT](./looker_csv_manufacturing_demo.pdf)

---

## 📝 Description
This project showcases a compact, production-minded **BI analytics pack** for a plastics manufacturer (5bn+ HUF turnover, exports to 50+ countries).  
It includes **ready-to-use datasets** and **Looker Studio** visuals covering **operations (OEE & downtime)**, **sales & market performance**, **profitability & cost-to-serve**, and a **lightweight workforce view**—all aligned to the same date range for clean slicing and storytelling.

**Scope highlights**
- **Operations:** OEE trend, downtime Pareto, scrap vs OEE bubble.
- **Sales:** Country revenue map, SKU/category Pareto (80/20), customer concentration.
- **Profitability:** **Revenue → EBITDA waterfall**, margin scatter (volume vs margin %, bubble=revenue).
- **Workforce:** Active labor cost and leave composition without blending.

---

## 🧰 Technologies Used
- **Looker Studio** (interactive dashboards, Pareto & waterfall, drill-down treemap)
- **CSV / Google Sheets** (demo data sources; easy to swap to a database)
- *(Optional in production)* **BigQuery / SQL** (for refreshable pipelines and governance)

---

## 📊 Featured Visuals
- **Sales & Market Performance**
  - *Revenue map (country)* — color by `SUM(revenue_huf)`; tooltip shows `SUM(quantity_kg)`.
  - *SKU / Category Pareto* — bars = revenue, line = cumulative % (80/20 line).
  - *Customer concentration* — top-N ring chart or treemap.
- **Profitability & Cost-to-Serve**
  - *Revenue → EBITDA waterfall* — simple daily filter; labels in HUF.
  - *Margin scatter* — X=volume (kg), Y=margin %, bubble=revenue (SKU & Customer views).
- **Operations**
  - *OEE snapshot & trend* — availability, performance, quality, OEE.
  - *Downtime Pareto* — minutes by reason with cumulative%.
  - *Scrap vs OEE bubble* — prioritize hotspots quickly.
- **Workforce**
  - *Active labor cost* — per employee (HUF).
  - *Leave composition* — 100% stacked (regular vs sick).

---

