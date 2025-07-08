# Law-Firm-Performance-Analytics
This project simulates a complete Business Intelligence (BI) solution for a personal injury law firm. As the BI Developer/Analyst, I designed and built an end-to-end analytics dashboard in Microsoft Power BI to provide the firm's leadership with a 360-degree view of their operations.

# End-to-End Law Firm Performance Dashboard in Power BI

**Author:** [Alonso Villalobos]  
**LinkedIn:** [https://www.linkedin.com/in/alonso-villalobos-lara-7297641b/]  
---

## 🚀 Project Summary

This repository documents the end-to-end creation of a comprehensive Business Intelligence solution for a fictional personal injury law firm. The project's goal was to move the firm from a state of scattered, raw data to a centralized, interactive analytics ecosystem.

As the sole BI Developer, I was responsible for the entire project lifecycle: from defining business requirements and preparing the data, through ETL, data modeling, DAX measure creation, and finally, designing a suite of four strategic dashboards in **Microsoft Power BI**. This project showcases a deep understanding of both the technical BI stack and the specific business drivers of a professional services firm.

## 🎯 The Business Problem & Strategic Goals

The law firm's leadership faced a common but critical challenge: a lack of data-driven visibility into their operations. Their data was fragmented across various systems (case management software, accounting spreadsheets, marketing reports), making it impossible to answer fundamental strategic questions:

1.  **Financial Performance:** Which types of cases are truly the most profitable after accounting for expenses? Are certain attorneys consistently generating more revenue?
2.  **Operational Efficiency:** What is the average time it takes to resolve a case? Where are the bottlenecks in our case lifecycle? Is our attorney workload balanced?
3.  **Marketing Effectiveness:** What is our Return on Investment (ROI) for marketing campaigns? Which channels bring in the most valuable clients, not just the most leads?
4.  **Client Satisfaction:** How can we quantitatively measure client happiness? Is there a link between how we operate and how clients feel about our service?

The goal was to build a "single source of truth" to answer these questions and empower data-informed decision-making at every level of the firm.

## 🛠️ My Step-by-Step Development Process

I followed a structured BI development methodology, broken down into distinct, logical phases.

```mermaid

    A[<b>Phase 1: Data Sourcing & Preparation</b><br>Define & Generate Realistic Datasets] --> B;

Phase 1: Data Sourcing & Preparation
To build a realistic prototype, I first defined the necessary data entities and then generated sample datasets. The data was structured to mirror what a real law firm would produce.
The following tables were created as CSV/Excel files:
Fact_Cases: The central transactional table containing one row per legal case, with all key metrics.
Dim_PracticeArea: A lookup table for case types (e.g., "Car Accident", "Medical Malpractice").
Dim_Attorney: A lookup table for attorneys and their seniority.
Dim_CaseStatus: Describes the stages of a case lifecycle (e.g., "Open", "Negotiation", "Settled").
Dim_LeadSource: A lookup table for marketing channels.
Dim_Client: A list of clients.
To see the full sample data used in this project, please expand the section below.
<details>
<summary>Click to view Sample Data (30 records per table)</summary>

Fact_Cases Data Snippet:
CaseID	ClientID	LeadAttorneyID	PracticeAreaID	StatusID	LeadSourceID	DateOpened	DateClosed	SettlementAmount	LegalFees	CaseExpenses	MarketingSpend	ClientSatisfactionScore
1001	101	1	1	5	3	2022-01-15	2022-08-20	150000	50000	7500	1500	5
1002	102	2	4	5	1	2022-02-01	2023-01-10	500000	165000	25000	0	4

(The full, raw data files can be found in the /data directory of this repository.)
</details>
    B[<b>Phase 2: ETL - Extract, Transform, Load</b><br>Clean & Shape Data in Power Query] --> C;
    C[<b>Phase 3: Data Modeling</b><br>Build a Robust Star Schema] --> D;
    D[<b>Phase 4: DAX Implementation</b><br>Develop KPIs & Business Logic] --> E;
    E[<b>Phase 5: Visualization & Dashboarding</b><br>Design 4 Strategic Dashboards] --> F;
    F[<b>Phase 6: Insights & Deployment</b><br>Derive Actionable Recommendations];
