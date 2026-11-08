# Enterprise Sales Velocity & Operational Risk Intelligence (Power BI)
[![Live Interactive Dashboard](https://img.shields.io/badge/Live_Dashboard-Click_to_View_in_Browser-F2C811?logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiNmVlZjNtMzRiOS00MzdilTk5OTItYWRkYjRlNmE2OWI1IiwidCI6IjgzYTBmZDMxLWE5NzAtNGVhYS05NmU3LWRkNmIzOTk0ZmM0MSJ9)
[![Power BI](https://img.shields.io/badge/Power_BI-Desktop_%26_Service-F2C811?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Architecture](https://img.shields.io/badge/Data_Model-Star_Schema-blue)](#data-architecture--relational-integrity)
[![Logic](https://img.shields.io/badge/DAX-Custom_Measures-orange)](#core-dax-calculation-engine)

---

## 1. Project Background & Executive Problem Statement

In enterprise commerce, top-line revenue growth can be dangerously deceptive. Commercial organizations frequently celebrate gross revenue milestones while remaining blind to operational friction occurring beneath the surface—including localized order churn, skewed regional logistics, and product quality defects.

This project was built to address three specific business challenges:
* **The Return Blindspot:** Gross sales figures often conceal rising product return rates that silently erode operating EBITDA.
* **Geographic Disconnect:** Marketing and logistics teams require visibility into regional customer concentration (North America, EMEA, LATAM, Middle East) to properly position inventory.
* **Category Dependency Risk:** Determining whether total revenue is sustained by a healthy product spread or dangerously concentrated in a single category.

To solve this, I designed and developed an end-to-end, 3-page interactive Power BI reporting suite that unifies high-level financial health monitoring with granular operational risk detection.

---

## 2. Interactive Dashboard Architecture & Visual Walkthrough

### Page 1: Executive Sales & Operational Performance
*Focus: Macro financial health, order velocity, and customer segment profitability.*

![Executive Sales & Operational Performance](Executive%20Sales%20%26%20Operational%20Performance.png)

* **Executive KPI Strip:** Provides instant macro visibility across four core metrics: **$740.86K Net Revenue**, **1,500 Total Orders**, an **Average Order Value (AOV) of $493.90**, and a global **Return Rate of 1.22%**.
* **Monthly Seasonality & Defect Tracking:** A dual-axis line and clustered column visual comparing net revenue trends directly against return percentages across all twelve months.
* **Customer Tier Matrix:** Segregates business revenue into Tier 1 ($323.70K), Tier 2 ($183.58K), and Tier 3 ($201.85K), pinpointing an AOV peak of $518.58 in Tier 2.
* **Store City Distribution:** A donut visual illustrating store delivery volume led by New York (31.63%), followed by Houston (22.94%), Miami (22.94%), London (11.47%), and Los Angeles.
* **Dynamic Slicing:** Responsive button tiles filtering transactions across operational years (2023 | 2024) and product categories.

---

### Page 2: Customer Geographic & Regional Performance
*Focus: Spatial density, market concentration, and regional tier filtering.*

![Customer Geographic & Regional Performance](Customer%20Geographic%20%26%20Regional%20Performance.png)

* **Global Spatial Intelligence:** A dedicated full-canvas bubble map mapping market footprint across North America, Latin America (LATAM), Europe & Africa (EMEA), and the Middle East.
* **Interactive Ribbon Controls:** Compact, zero-clutter button ribbons enabling executive drill-down by customer tier (Tier 1 | Tier 2 | Tier 3) and sales region simultaneously.

---

### Page 3: Product & Inventory Quality Analytics
*Focus: Root-cause defect isolation, category velocity, and SKU contribution.*

![Product & Inventory Analytics](Product%20%26%20Inventory%20Analytics.png)

* **Category Quality Matrix (Top-Left):** Evaluates total orders, net revenue, returned units, and return percentages across 5 categories (`Fasteners`, `Hand Tools`, `Measurement`, `Power Tools`, `Safety Equipment`) with soft-alert conditional formatting.
* **Volume vs. Defect Column Chart (Top-Right):** Highlights order volume directly against returned units, pinpointing operational return exposure.
* **Category Revenue Share (Bottom-Left):** Donut chart identifying revenue concentration, led by Power Tools ($446.78K / 60.31%).
* **Flagship SKU Clustered Bar Chart (Bottom-Right):** Ranks the top revenue-generating SKUs, led by the Heavy-Duty Impact Wrench 20V ($207K) and the Industrial Drill 750W ($140K).

---

## 3. Data Architecture & Relational Integrity

The reporting engine is built on a **Star Schema** to ensure query efficiency, avoid circular dependencies, and prevent ambiguous filtering paths:
