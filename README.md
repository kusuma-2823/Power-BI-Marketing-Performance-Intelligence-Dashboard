# 📊 Marketing Performance Intelligence Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-purple?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-Data%20Source-217346?style=for-the-badge\&logo=microsoft-excel\&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-orange?style=for-the-badge)

An interactive **Power BI Marketing Performance Intelligence Dashboard** designed to analyze marketing performance across campaigns, platforms, content types, audiences, and time periods.

The project transforms raw marketing data into an interactive Business Intelligence solution that enables users to monitor KPIs, compare campaign performance, analyze content effectiveness, and evaluate marketing efficiency.

---

# 📌 Table of Contents

* Project Overview
* Business Problem
* Project Objectives
* Dataset Overview
* Data Model
* Data Preparation
* Key Metrics
* Dashboard Pages
* Executive Overview
* Campaign Performance
* Content Intelligence
* Key Insights
* Interactive Features
* Tools and Technologies
* Skills Demonstrated
* Dashboard Design
* Repository Structure
* How to Use
* Future Improvements
* Project Outcome
* Learning Outcomes
* Author

---

# 📌 Project Overview

The **Marketing Performance Intelligence Dashboard** is a three-page Power BI analytics solution developed to provide a comprehensive view of marketing performance.

The dashboard covers the period **2024–2026** and combines campaign, content, platform, audience, and date-level information.

The report follows an executive-to-detail analytical flow:

**Executive Overview → Campaign Performance → Content Intelligence**

This allows users to start with high-level business KPIs and then explore campaign and content-level performance.

---

# 💼 Business Problem

Marketing teams generate large amounts of performance data across different campaigns, platforms, and content formats.

Without a centralized analytics solution, it can be difficult to:

* Monitor overall marketing KPIs
* Compare campaign performance
* Understand marketing spend versus revenue
* Identify high-performing campaigns
* Evaluate Return on Ad Spend
* Understand which content formats generate engagement
* Track performance trends over time
* Compare platform-level performance

This project addresses these challenges by creating a centralized and interactive Power BI dashboard.

---

# 🎯 Project Objectives

The main objectives of this project are:

1. Build an interactive marketing analytics dashboard.
2. Monitor important marketing KPIs.
3. Analyze campaign-level performance.
4. Compare marketing spend and revenue.
5. Analyze Return on Ad Spend (ROAS).
6. Evaluate content performance.
7. Analyze engagement across content types.
8. Track marketing performance over time.
9. Compare platform-level revenue and efficiency.
10. Enable users to filter and explore the data dynamically.

---

# 📊 Dataset Overview

The dataset contains marketing performance information covering the period **2024–2026**.

The analysis includes metrics related to:

### Marketing Performance

* Total Impressions
* Total Reach
* Total Clicks
* Total Engagements
* Total Leads
* Total Revenue
* Total Spend

### Marketing Efficiency

* CTR
* Engagement Rate
* Conversion Rate
* Cost Per Lead
* ROAS

### Dimensions

* Date
* Campaign
* Platform
* Content Type
* Audience Segment
* Age Group
* Gender

---

# 🗂️ Data Model

The Power BI model follows a **dimensional data modeling / star-schema approach**.

## Fact Table

### FactMarketing

The central fact table contains marketing performance metrics.

Key fields include:

* Date
* Campaign ID
* Platform ID
* Content ID
* Audience ID
* Impressions
* Reach
* Clicks
* Engagements
* Leads
* Revenue
* Spend

---

## Dimension Tables

### DimDate

Contains time-related attributes:

* Date
* Day
* Day Name
* Month
* Month Number
* Quarter
* Week Number
* Year
* Year-Month

### DimCampaign

Contains campaign information:

* Campaign ID
* Campaign
* Objective

### DimContent

Contains content information:

* Content ID
* Content Type

Content types analyzed include:

* Reel
* Video
* Carousel
* Static Post
* Story
* Short

### DimPlatform

Contains platform information:

* Platform ID
* Platform

Platforms included in the analysis include:

* Instagram
* YouTube
* Facebook
* LinkedIn
* X

### DimAudience

Contains audience information:

* Audience ID
* Audience Segment
* Age Group
* Gender

### MonthlyTargets

Contains monthly marketing target information used for performance monitoring.

---

# 🔄 Data Preparation

The data was prepared and transformed using **Power Query** before being used for analysis.

The preparation process included:

* Importing the marketing dataset
* Reviewing data types
* Cleaning and organizing columns
* Creating relationships between tables
* Creating a dedicated Date dimension
* Organizing campaign attributes
* Organizing content attributes
* Organizing platform attributes
* Preparing fields for KPI calculations
* Structuring the model for efficient reporting

---

# 🧮 Key Metrics

The dashboard uses DAX measures to calculate important marketing KPIs.

## Total Impressions

Measures the total number of times marketing content was displayed.

```DAX
Total Impressions =
SUM(FactMarketing[Impressions])
```

## Total Reach

Measures the total number of users/accounts reached.

```DAX
Total Reach =
SUM(FactMarketing[Reach])
```

## Total Clicks

Measures the total number of clicks generated.

```DAX
Total Clicks =
SUM(FactMarketing[Clicks])
```

## Total Engagements

Measures the total number of interactions generated by marketing content.

```DAX
Total Engagements =
SUM(FactMarketing[Engagements])
```

## Total Leads

Measures the total number of leads generated.

```DAX
Total Leads =
SUM(FactMarketing[Leads])
```

## Total Revenue

Measures revenue attributed to marketing activity.

```DAX
Total Revenue =
SUM(FactMarketing[Revenue])
```

## Total Spend

Measures total marketing expenditure.

```DAX
Total Spend =
SUM(FactMarketing[Spend])
```

## CTR

Click-Through Rate measures the percentage of impressions that resulted in clicks.

```text
CTR = Total Clicks / Total Impressions
```

## Engagement Rate

Engagement Rate measures the percentage of impressions that resulted in engagements.

```text
Engagement Rate = Total Engagements / Total Impressions
```

## Conversion Rate

Conversion Rate measures the percentage of clicks that resulted in leads.

```text
Conversion Rate = Total Leads / Total Clicks
```

## Cost Per Lead

Cost Per Lead measures the average marketing spend required to generate one lead.

```text
Cost Per Lead = Total Spend / Total Leads
```

## ROAS

Return on Ad Spend measures revenue generated relative to marketing spend.

```text
ROAS = Total Revenue / Total Spend
```

---

# 📑 Dashboard Pages

The report contains three main analytical pages:

1. **Executive Overview**
2. **Campaign Performance**
3. **Content Intelligence**

---

# 1️⃣ Executive Overview

The **Executive Overview** provides a high-level summary of marketing performance between **2024–2026**.

## KPI Cards

The page contains:

* Total Impressions
* Total Reach
* Total Clicks
* Total Engagements
* Total Leads
* Total Revenue
* CTR
* Engagement Rate
* Conversion Rate
* ROAS

## Visualizations

### Monthly Impressions Trend

A time-series visualization showing how total impressions change across months.

### Revenue vs Spend Trend

Compares marketing revenue against marketing spend over time.

### Platform Revenue & ROAS

Compares revenue contribution and ROAS across different marketing platforms.

## Filters

Users can dynamically filter the dashboard using:

* Year
* Platform
* Campaign

---

# 2️⃣ Campaign Performance

The **Campaign Performance** page provides detailed campaign-level analysis.

## Campaign Performance Table

The table contains:

* Campaign
* Total Spend
* Total Revenue
* Total Leads
* CTR
* Conversion Rate
* ROAS

Conditional formatting is used to improve the readability of important metrics.

## Revenue vs Spend by Campaign

A combination chart compares:

* Campaign Revenue
* Campaign Spend

This helps analyze the relationship between marketing investment and revenue generation.

## ROAS by Campaign

A horizontal bar chart compares Return on Ad Spend across campaigns.

This allows users to compare campaign efficiency based on revenue generated relative to spend.

## Filters

The page includes:

* Year
* Platform
* Campaign

These filters dynamically update the table and visualizations.

---

# 3️⃣ Content Intelligence

The **Content Intelligence** page focuses on the performance of different content formats.

## Content Types

The analysis includes:

* Reel
* Video
* Carousel
* Static Post
* Story
* Short

## KPI Cards

The page displays:

* Total Impressions
* Total Engagements
* Total Clicks
* Total Leads

## Impressions by Content Type

Compares total impressions generated by each content format.

## Engagements by Content Type

Compares total engagement generated by each content format.

## Content Performance Trend

A time-series visualization tracks content performance over time using:

* Total Engagements
* Total Impressions

## Engagement Rate by Content Type

Compares engagement rates across different content formats.

This helps analyze differences in audience interaction between content formats.

## Filters

Users can filter the page using:

* Year
* Platform
* Content Type

---

# 🔍 Key Insights

The dashboard enables several observations from the dataset.

### Content Performance

**Reels generate the highest volume of impressions** among the analyzed content types.

Reels also generate the highest overall engagement volume in the dataset.

### Campaign Performance

Campaigns show variation in:

* Revenue
* Spend
* Leads
* CTR
* Conversion Rate
* ROAS

This demonstrates the importance of evaluating campaigns using multiple KPIs rather than relying on a single metric.

### Marketing Efficiency

ROAS provides a view of how effectively marketing spend translates into revenue.

Campaign-level ROAS analysis allows users to compare marketing efficiency across campaigns.

### Platform Analysis

Platform-level revenue and ROAS analysis provides visibility into how different platforms contribute to overall marketing performance.

### Time-Based Analysis

Monthly trend analysis allows users to identify fluctuations in impressions, engagements, revenue, and spend over time.

> **Note:** Insights are based on the dataset used for this portfolio project.

---

# 🎛️ Interactive Features

The dashboard includes several interactive features.

### Slicers

Users can filter the report by:

* Year
* Platform
* Campaign
* Content Type

### Cross-Filtering

Selecting a campaign, platform, or content type updates related visuals across the report.

### Dynamic KPIs

KPI cards automatically update based on selected filters.

### Conditional Formatting

The campaign performance table uses conditional formatting to make numerical comparisons easier.

### Interactive Navigation

Users can move between:

**Executive Overview → Campaign Performance → Content Intelligence**

to explore the report at different levels of detail.

---

# 🛠️ Tools and Technologies

| Tool / Technology     | Purpose                                         |
| --------------------- | ----------------------------------------------- |
| Power BI              | Dashboard development and visualization         |
| DAX                   | KPI and analytical calculations                 |
| Power Query           | Data transformation and preparation             |
| Microsoft Excel       | Data source and data preparation                |
| Data Modeling         | Relationships between fact and dimension tables |
| Power BI Visuals      | Interactive reporting                           |
| Business Intelligence | Performance analysis and reporting              |

---

# 💡 Skills Demonstrated

## Data Analysis

* KPI Analysis
* Trend Analysis
* Campaign Analysis
* Content Analysis
* Marketing Funnel Analysis
* Performance Analysis
* Comparative Analysis

## Power BI

* Dashboard Development
* Interactive Reports
* Slicers
* KPI Cards
* Tables
* Bar Charts
* Column Charts
* Line Charts
* Combo Charts
* Conditional Formatting
* Cross-Filtering

## DAX

* Measures
* Aggregations
* Ratio Calculations
* KPI Calculations
* CTR
* Engagement Rate
* Conversion Rate
* Cost Per Lead
* ROAS

## Data Modeling

* Fact Tables
* Dimension Tables
* Relationships
* Date Dimension
* Star Schema
* Dimensional Modeling

## Business Intelligence

* Executive Reporting
* Marketing Analytics
* Performance Monitoring
* Business KPI Reporting
* Data-Driven Analysis
* Data Storytelling

---

# 🎨 Dashboard Design

The dashboard was designed using a clean, business-oriented layout.

### Design Principles

* Consistent color palette
* Clear KPI hierarchy
* Minimal visual clutter
* Interactive filters
* Consistent chart formatting
* Executive-friendly presentation
* Clear analytical flow
* Consistent page structure

The report uses a consistent visual design across all three pages to make navigation and interpretation easier.

---

# 📸 Dashboard Preview

## Executive Overview

![Executive Overview](Screenshots/Executive_Overview.png)

## Campaign Performance

![Campaign Performance](Screenshots/Campaign_Performance.png)

## Content Intelligence

![Content Intelligence](Screenshots/Content_Intelligence.png)

---

# 📂 Repository Structure

```text
Marketing-Performance-Intelligence/
│
├── README.md
│
├── Dashboard/
│   └── Marketing_Performance_Intelligence.pbix
│
├── Dataset/
│   └── Marketing_Dataset.xlsx
│
├── Screenshots/
│   ├── Executive_Overview.png
│   ├── Campaign_Performance.png
│   └── Content_Intelligence.png
│
└── Documentation/
    └── Project_Documentation.pdf
```

---

# 🚀 How to Use

## Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/Marketing-Performance-Intelligence.git
```

## Step 2: Open the Project

Open the following file using **Power BI Desktop**:

```text
Dashboard/Marketing_Performance_Intelligence.pbix
```

## Step 3: Check the Data Source

If the dataset is included, make sure the Power BI file is connected to the correct dataset location.

## Step 4: Refresh the Data

Open Power BI Desktop and select:

**Home → Refresh**

## Step 5: Explore the Dashboard

Use the available slicers to explore:

* Overall marketing performance
* Campaign performance
* Platform performance
* Content performance
* Marketing efficiency
* Time-based trends

---

# 🔐 Data Privacy

This project is intended for **portfolio and educational purposes**.

If the dataset is synthetic or publicly available, it can be included in the repository.

If the dataset contains confidential or proprietary information, only non-sensitive project documentation and dashboard screenshots should be shared.

---

# 🚀 Future Improvements

Potential future enhancements include:

* Adding monthly target vs actual analysis
* Adding audience segmentation analysis
* Adding platform-level drill-through pages
* Adding campaign drill-through pages
* Adding automated data refresh
* Adding forecasting
* Adding anomaly detection
* Adding customer acquisition cost analysis
* Adding budget allocation analysis
* Adding advanced audience analysis
* Publishing the dashboard to Power BI Service
* Adding automated reporting

---

# 🏆 Project Outcome

This project demonstrates how Power BI can transform raw marketing data into an interactive Business Intelligence solution.

The dashboard provides a centralized view of the marketing funnel:

**Marketing Spend → Impressions → Engagement → Clicks → Leads → Revenue → ROAS**

The project demonstrates practical experience in:

* Data preparation
* Data cleaning
* Data modeling
* DAX
* KPI development
* Dashboard design
* Marketing analytics
* Business intelligence
* Data storytelling
* Interactive reporting

---

# 📚 Learning Outcomes

Through this project, I strengthened my understanding of:

* Building Power BI dashboards from raw datasets
* Creating relationships between multiple tables
* Designing dimensional data models
* Building a star-schema model
* Writing DAX measures
* Creating marketing KPIs
* Building interactive reports
* Using conditional formatting
* Creating business-focused visualizations
* Designing executive-level dashboards
* Translating data into business insights
* Presenting analytical findings effectively

---

# 📌 Project Highlights

| Area      | Analysis                                           |
| --------- | -------------------------------------------------- |
| Marketing | Overall marketing performance                      |
| Campaigns | Spend, revenue, leads, CTR, conversion rate & ROAS |
| Platforms | Revenue & ROAS comparison                          |
| Content   | Impressions, engagements & engagement rate         |
| Time      | Monthly performance trends                         |
| KPIs      | CTR, Conversion Rate, Engagement Rate & ROAS       |
| Reporting | Interactive 3-page Power BI dashboard              |

---

# 👩‍💻 Author

## Kusuma Bavisetti

**Aspiring Data Analyst | Business Analytics | Power BI | SQL | Excel**

Interested in using data analytics and Business Intelligence tools to transform data into meaningful insights and support data-driven decision-making.

---

# 🔗 Connect With Me

### LinkedIn

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kusuma%20Bavisetti-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/kusumabavisetti/)

---

# ⭐ Support

If you found this project useful or interesting, consider giving the repository a ⭐.

Thank you for visiting this project!
