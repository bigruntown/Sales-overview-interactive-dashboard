# Sales Overview Interactive Dashboard

An interactive two-page Power BI report that surfaces sales, profit, and units-sold performance across product, segment, and quarter, with a dedicated storytelling page that walks the viewer through the key findings.

## Overview

This dashboard was built to answer the operational question every commercial team faces: **where is our revenue and profit actually coming from, 
and what's the growth story behind the headline numbers?**

The report is structured around a clean star schema (Facts + Dimensions) so that filters propagate cleanly across all visuals. 
It's designed for self-service analysis — a non-technical user can land on the KPI page, slice by Segment or Quarter, and immediately see how the picture changes.

## Tools

- **Microsoft Power BI Desktop** — modeling, DAX measures, report layout
- **DAX** — KPI measures (Total Sales, Total Profit, Units Sold)
- **Data modelling** — Star schema (single fact table joined to dimension tables)

## Dataset

A multi-product retail sales dataset broken into:

- **Facts** table — transactional records with sales, profit, and units sold
- **Dimensions** table(s) — Product, Segment, Quarter

(Public sample dataset used during the Utiva Data Science program.)

## What the report contains

### Page 1 — KPI Dashboard

- Top-line KPI cards: **Total Sales**, **Total Profit**, **Units Sold**
- **Clustered bar / clustered column** charts breaking those KPIs down by **Product** and **Segment**
- **Line chart** showing performance across **Quarters**
- **Donut chart** for share-of-mix analysis (Segment contribution)
- **Scatter chart** to expose the relationship between sales volume and profit at the product level
- **Slicers** for Segment and Quarter so the entire page is filterable

### Page 2 — Story Telling

A guided commentary page that walks the reader through the most important finding from the KPI page. This separation (KPI page for exploration, 
Story page for narrative) is a deliberate dashboard-design choice — too many dashboards mix the two and confuse the audience.

## Key technical work

- Built the **fact-and-dimension star schema** rather than dumping everything in a flat table, which makes filters faster and measures cleaner.
- Authored DAX measures for the three headline KPIs and reused them across multiple visuals so the numbers stay consistent if the source changes.
- Designed a **second page for narrative** instead of cramming everything onto one canvas — recruiters and stakeholders notice this.

## Screenshot
![image alt](https://github.com/bigruntown/Sales-overview-interactive-dashboard/blob/main/KPI%20DASHBOARD%20.png?raw=true)

## How to view this project

1. Download `Sales-overview-Interactive-Dashboard.pbix` from this repo.
2. Open it in **Power BI Desktop** (free download from Microsoft).
3. The report opens with both pages — use the page navigator at the bottom.

---

*Built as part of the Utiva Data Science program (2026).*
