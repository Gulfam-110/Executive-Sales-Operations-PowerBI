# Executive Sales & Operational Performance Dashboard (Power BI)

An enterprise-grade, 3-page interactive Power BI reporting solution designed to bridge high-level C-suite revenue monitoring with granular operational risk detection. This report tracks order velocity, regional market density, and SKU-level defect root causes.

---

## Dashboard Previews

### Page 1: Executive Sales & Operational Performance
![Executive Overview](Executive%20Sales%20%26%20Operational%20Performance.png)

### Page 2: Customer Geographic & Regional Performance
![Customer Deep-Dive](Customer%20Geographic%20%26%20Regional%20Performance.png)

### Page 3: Product & Inventory Quality Analytics
![Product Analytics](Product%20%26%20Inventory%20Analytics.png)

---

## Executive Summary & Business Problem

Leadership often faces a disconnect between top-line revenue figures and underlying operational leakages:
1. **Revenue Masking Quality Issues:** Strong gross sales figures can conceal escalating return rates that erode operating margins.
2. **Regional Blind Spots:** Without unified geographic tiering, marketing and supply chain teams cannot allocate regional inventory efficiently.
3. **SKU-Level Vulnerabilities:** High-volume product lines can obscure specific high-margin items suffering from quality defects.

This project solves these challenges by implementing an interactive, cross-synchronized three-tier analytics framework:
* **Page 1: Executive Overview** — Macro-level financial KPIs, monthly seasonality, and customer tier profitability.
* **Page 2: Customer Deep-Dive** — Global geographical footprint, regional order volume, and tier concentration.
* **Page 3: Product & Inventory Analytics** — 2×2 quad analysis isolating return root causes and high-velocity SKU performance.

---

## Report Architecture & Page Walkthrough

### Page 1: Executive Sales & Operational Performance
* **C-Suite KPI Strip:** Delivers instant clarity on **Net Revenue ($740.86K)**, **Total Orders (1,500)**, **Average Order Value ($493.90)**, and **Return Rate % (1.22%)**.
* **Monthly Velocity vs. Defect Rate:** A dual-axis combo chart tracking revenue generation against return percentage by month to spot seasonal spikes.
* **Customer Tier Breakdown:** A financial matrix evaluating order distribution and AOV across Tier 1, Tier 2, and Tier 3 clients.
* **Store City Distribution:** A donut chart showing store order volume led by New York (31.63%), Houston, Miami, London, and Los Angeles.
* **Slicer Panel:** Dynamic button tiles filtering transaction data across operational years (2023 | 2024) and product categories.

### Page 2: Customer Geographic & Regional Performance
* **Full-Canvas Geographic Density Map:** Bubble size represents total sales volume, visually mapping distribution across North America, EMEA, LATAM, and the Middle East.
* **Multi-Select Region & Tier Slicers:** Clean, customized button ribbons enabling instant filtering by customer tier (`Tier 1`, `Tier 2`, `Tier 3`) and sales region without visual clutter.

### Page 3: Product & Inventory Quality Analytics (2×2 Matrix)
* **Top-Left (Category Financial & Quality Matrix):** Multi-metric grid breaking down Orders, Net Revenue, Return Units, and Return Rate % across 5 core categories (`Fasteners`, `Hand Tools`, `Measurement`, `Power Tools`, `Safety Equipment`) with soft-alert conditional formatting.
* **Top-Right (Orders vs. Returns Column Chart):** Compares total order volume directly against returned units by category, isolating where operational returns are concentrated.
* **Bottom-Left (Category Net Revenue Share):** Donut chart highlighting category revenue distribution, led by Power Tools ($446.78K / 60.31%).
* **Bottom-Right (Top 10 Products by Net Revenue):** Horizontal clustered bar chart highlighting flagship revenue drivers (led by Heavy-Duty Impact Wrench 20V at $207K and Industrial Drill 750W at $140K).

---

## Data Architecture & Modeling

The data model follows an optimized **Star Schema** to ensure fast DAX calculation speeds, eliminate circular dependencies, and prevent many-to-many ambiguity:
