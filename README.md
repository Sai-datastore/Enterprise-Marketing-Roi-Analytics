# Enterprise Marketing ROI Analytics Platform  
(SQL • Python • Power BI)

## Overview
This project delivers an end-to-end analytics solution that integrates CRM, marketing campaign, and revenue data to provide a unified view of marketing performance and ROI.  
The solution focuses on standardized KPI definitions, data quality validation, and executive-ready dashboards to support data-driven decision-making.

## Business Problem
Enterprise marketing teams often operate with siloed CRM and campaign data, making it difficult to accurately measure ROI, compare channel performance, and understand regional or customer segment impact.  
This project addresses those challenges by designing a scalable data model and analytics pipeline that enables consistent reporting across stakeholders.

## Solution Summary
- Built a full ETL-style workflow using Python and SQL
- Designed a star schema optimized for BI reporting
- Implemented data quality validation checks
- Developed KPI-driven Power BI dashboards for executives and analysts

## Tech Stack
- **SQL:** PostgreSQL / SQL Server  
- **Python:** pandas, NumPy  
- **BI & Visualization:** Power BI (DAX, data modeling)  
- **Version Control:** Git, GitHub  

## Architecture
Raw CSV Files  
→ SQL Staging Tables  
→ Star Schema (Fact & Dimension Tables)  
→ Python Data Quality Validation  
→ Power BI Semantic Model  
→ Executive Dashboards  

## Data Model
**Fact Table**
- `fact_marketing`  
  - impressions  
  - clicks  
  - conversions  
  - spend  
  - revenue  

**Dimension Tables**
- `dim_date`
- `dim_campaign`
- `dim_customer`

The star schema design ensures efficient aggregation and consistent KPI calculations in Power BI.

## Key KPIs
- **CTR (Click-Through Rate):** Clicks / Impressions  
- **CVR (Conversion Rate):** Conversions / Clicks  
- **CPA (Cost per Acquisition):** Spend / Conversions  
- **ROI (%):** (Revenue − Spend) / Spend  
- **Profit:** Revenue − Spend  

## Data Quality Checks
Automated Python checks validate:
- Null and missing values
- Primary key uniqueness
- Logical consistency (impressions ≥ clicks ≥ conversions)
- Negative or invalid metric values

A data quality report is generated to ensure reliability before reporting.

## Dashboard (Power BI)
### Pages Included
1. **Executive Overview**
   - Total Spend, Revenue, Profit, ROI%
   - Monthly performance trends
   - ROI comparison by channel

2. **Campaign Performance**
   - Campaign-level ROI ranking
   - Spend vs Revenue analysis
   - Marketing funnel visualization

3. **Segment & Regional Insights**
   - ROI by region and channel
   - Revenue contribution by customer segment
   - Performance drilldowns using slicers

## How to Run the Project
1. **Install dependencies**
   ```bash
   pip install -r requirements.txt
