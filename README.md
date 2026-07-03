# Procurement KPI Analysis
**Google Data Analytics Professional Certificate — Capstone Project**

## Project Overview
This project analyzes procurement performance data for 5 suppliers across 5 product categories from 2022 to 2024 (777 orders). The goal is to identify supplier risks, fulfillment patterns, cost saving opportunities, and data quality issues to support data-driven procurement decisions.

**Dataset:** [Procurement KPI Analysis Dataset](https://www.kaggle.com/datasets/vivek1johari/procurement-kpi-analysis) — Kaggle 
**Tool:** Microsoft Excel 
**Skills:** Data cleaning, pivot tables, data visualization, KPI analysis

---

## Business Questions
- Which suppliers pose the highest delivery and quality risk?
- Are there seasonal patterns in fulfillment performance?
- How effective is price negotiation across suppliers and categories?
- What is the financial impact of unfulfilled orders?

---

## Analysis Structure

| Tab | Description |
|-----|-------------|
| 1. Overview | Executive dashboard — key KPIs and summary findings |
| 2. Fulfillment Trend | Monthly trend and seasonal pattern analysis |
| 3. Performance Matrix | Supplier × Category risk heatmap and detailed scorecard |
| 4. Cost Savings | Price negotiation impact by supplier and category |
| 5. Unfulfilled Orders | Cancellation risk and root cause analysis |
| 7. Working Data | Cleaned data with helper columns |
| 8. Raw Data | Original dataset |

---

## Key Findings
- **Overall fulfillment rate: 72.1%** — nearly 1 in 4 orders is not fully delivered
- **Alpha_Inc** is the best-performing supplier — highest fulfillment (75.9%), lowest defect rate (1.8%), best savings rate (8.1%)
- **Delta_Logistics** is the highest-risk supplier — lowest fulfillment (70.2%), highest defect rate (10.8%), lowest compliance (60.8%)
- **May shows a recurring fulfillment dip** — 60.0% in both 2022 and 2023, suggesting a systemic seasonal issue
- **$3.93M saved** through price negotiation (8.0% savings rate) across $49.3M in spend
- **$3.59M at risk** from 63 cancelled orders

---

## Data Quality Notes
- Negative lead times detected (min: −5 days) — likely data entry errors, excluded from lead time analysis
- Pending orders with recorded delivery dates identified — delivery dates excluded for pending status records
- Defect units recorded for cancelled orders — likely reflects partial receipt prior to cancellation; defect rates consistent across all order statuses (5.4%–6.5%)
- Quantity field for partially delivered orders does not distinguish ordered vs. received quantity

---

## Risk Scoring Methodology
Supplier risk scores are calculated using a weighted model:

**Risk Score = (1 − Fulfillment Rate) × 40 + Defect Rate × 35 + (1 − Compliance Rate) × 25**

Weights reflect operational priorities: fulfillment (40%) directly impacts operations, defect rate (35%) captures quality costs, compliance (15%) reflects process reliability. Thresholds: Low < 10 · Medium 10–16 · High > 16.

*Note: This is an analyst-defined scoring model, not an industry-standard formula. Weights are adjustable based on organizational priorities.*
