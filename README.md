

# NIFTY 50 ESG Dashboard


## Problem Statement

This dashboard enables investors, policymakers, and researchers to assess the **ESG (Environmental, Social, Governance) performance** of India's top 50 publicly traded companies (NIFTY 50). The dashboard provides a granular view of company-level ESG risk, controversy exposure, and comparative scoring. Stakeholders can identify key risk areas, benchmark performance, and inform sustainability strategies using these insights.

## Database Description

**NIFTY 50 ESG Dataset**: This dataset provides a comprehensive evaluation of ESG performance for the top 50 companies listed on the National Stock Exchange (NSE). It tracks:

- **ESG Risk Scores** (numerical quantification)
- **Controversy Levels** (risk intensity)
- **ESG Risk Level**
- **ESG Risk Management**
- **Current vs predicted ESG scores**

Ideal for risk analysts, sustainability consultants, and financial professionals focusing on ESG-oriented investment and operational decision-making.

## Steps Followed

- **Step 1**: Imported raw ESG dataset into Power BI.
- **Step 2**: Activated Power Query features for column profiling, data quality, and error checks, ensuring accurate metrics.
- **Step 3**: Built slicers enabling filtering and deep dives for each NIFTY 50 company.
- **Step 4**: Added visuals for ESG Risk Score, Controversy Level, and ESG Risk Level—displaying company-wise risk using bar charts and pie/donut charts.
- **Step 5**: Modeled “ESG Risk Management” into a donut chart showing proportion of companies with strong vs average controls.
- **Step 6**: Created comparison line chart for “Predicted ESG Score vs Current ESG Score” to flag possible improvement or deterioration in future ESG performance.
- **Step 7**: Incorporated DAX measures for custom aggregations (see below).

## DAX Logic & Calculations

DAX expressions used:

- **Risk Level Assignment (Calculated Column)**
```DAX
ESG Risk Level = 
SWITCH(
  TRUE(),
  ESG_Score < 20, "Low",
  ESG_Score < 35, "Medium",
  ESG_Score < 50, "High",
  "Severe"
)
```


## Dashboard Components

- **Slicer:** Filters results for each NIFTY 50 company.
- **Bar Chart:** Top NIFTY 50 companies by ESG risk score. Highlights leaders and laggards; e.g., Oil & Natural Gas Corp (52.2), Coal India (45.5), NTPC Ltd (39.4).
- **Controversy Level Table:** Shows how many companies fall into moderate, significant, and high controversy categories.
- **Pie Chart (ESG Risk Level):** Distribution- 44% medium risk, 26% high, 22% low, 8% severe.
- **Donut Chart (Risk Management):** 54% strong, 46% average management in mitigating ESG risks.
- **Line Chart (Predicted vs Current ESG):** Visualizes actual scores vs model-predicted scores for each company, indicating deviation and improvement trends.

## Insights from Dashboard

### 1. ESG Risk Distribution
- **Medium risk** is the most common among NIFTY 50 companies (44%), followed by high (26%), low (22%), and severe (8%).
- This suggests a moderate overall ESG risk, but notable outliers require closer scrutiny.

### 2. Management Strength
- **54%** of companies display strong ESG risk management practices, while 46% are average.
- Indicates robust governance for over half the index, but substantial room for improvement remains.

### 3. Controversy Exposure
- The dataset enables analysis of controversy levels, with several companies facing significant or high controversy events, raising stakeholder concerns.

### 4. Company-wise ESG Risk (Leaders & Laggards)
- Highest risk scores: Oil & Natural Gas Corp (52.2), Coal India Ltd (45.5), Grasim Industries (43.1).
- Lowest risk scores: Cipla Ltd (28.4), Nestle India Ltd (28.3).
- Companies with high scores may face greater regulatory, reputational, and operational risks.

### 5. Predicted vs Current ESG Scores
- Notable gaps are visible for some companies between predicted and current scores.
- Outliers with sharp increases or decreases suggest evolving risk profiles, signaling future opportunities or threats for investors and management.

***

# Snapshot of Dashboard
<img width="1373" height="728" alt="Screenshot 2025-08-12 140540" src="https://github.com/user-attachments/assets/e7cb0a7e-5044-48fa-89a9-3a1b88676178" />


***

## Summary

This Power BI dashboard delivers actionable ESG risk intelligence for NIFTY 50 companies. It unveils key distribution patterns, controversy clusters, management effectiveness, and predictive ESG trends, supporting informed sustainability strategy, investment, and reporting initiatives for India’s largest corporates.

