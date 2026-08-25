# Global Workforce Demographics & Payroll Cost Analysis

An interactive Excel dashboard analyzing employee demographics, payroll distribution, and hiring trends across three countries for **Forms & Styles Group,** built using Power Query and Pivot Tables.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results / Findings](#results--findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

## Project Overview

This project simulates a real-world HR analytics scenario for a fictional company, **Forms & Styles Group**, operating across three countries: the United States, China, and Brazil. Using a workforce dataset of 1,000 employees, the goal was to design an interactive Excel dashboard that gives stakeholders a fast, visual read on headcount, payroll distribution, demographic composition, and hiring momentum, without needing to dig through raw spreadsheet data.

<img width="864" height="486" alt="Screenshot 2026-08-25 025008" src="https://github.com/user-attachments/assets/76ad77bc-a2da-4dff-914f-2189005526bb" />


## Data Sources

The dataset used for this project was provided as part of a data analytics bootcamp exercise. It contains employee-level records including:

- Employee demographics (gender, age, country)
- Department and job role
- Annual salary
- Hire date
- Monthly sales figures

## Tools Used

- **Microsoft Excel**: sole tool for the entire workflow
  - **Power Query**: data import, cleaning, and transformation
  - **PivotTables & PivotCharts**: aggregation and visualization
  - **Slicers**: interactive filtering by country
  - **Dashboard design** — card-based KPI layout combining PivotCharts, shapes, and text boxes

## Data Cleaning and Preparation

- Imported the raw dataset into Excel via Get & Transform Data (Power Query)
- Checked and corrected column data types (e.g., Salary as currency/number, Hire Date as date)
- Removed duplicate records and blank rows
- Standardized categorical fields (e.g., consistent spelling/casing for Department, Country, Gender)
- Created calculated columns where needed, such as:
  - **Age Group**: bucketed from Date of Birth/Age into bands (28–37, 38–47, 48–57, 58–67, 68–77)
  - **Hire Month**: extracted from Hire Date for the hiring trend chart
- Loaded the cleaned table into the Excel Data Model for PivotTable use

## Exploratory Data Analysis

Before building the dashboard, the following questions guided the exploration of the dataset:

1. **How is the workforce distributed across countries?** to understand where headcount is concentrated.
2. **What is the gender balance across the company?** to check for representation gaps.
3. **How is the workforce distributed by age?** to understand generational makeup and future retirement/succession risk.
4. **Which departments carry the highest payroll cost, and does that align with headcount?** to flag cost outliers.
5. **How has hiring changed month-over-month?** to spot growth or slowdown patterns.
6. **How do monthly sales trends compare with hiring trends?** to see whether workforce growth tracks business performance.

Each question was answered by building a corresponding PivotTable, then visualizing it as a PivotChart (pie, donut, bar, or line) on the dashboard canvas.

## Data Analysis

- Average salary per department (Total departmental salary ÷ headcount per department), to distinguish high headcount departments from high individual pay departments
- Year-over-year or month-over-month % change in hiring and sales
- Country-level breakdown of salary distribution (using the slicer) to compare pay costs across the US, China, and Brazil

## Results / Findings

- **Headcount:** The company employs **1,000 staff** total, concentrated mainly in the **United States (643)**, followed by **China (218)** and **Brazil (139)**.
- **Payroll:** Total annual salary across the company is **$113,217,365**.
- **Gender distribution:** Near-balanced, **52% female (518)** vs. **48% male (482)**.
- **Age distribution:** The workforce skews mid-to-late career, the **48–57** age group is the largest segment (281 employees), while **68–77** is the smallest (39), suggesting limited near-retirement risk but a need to track succession planning as the 48–57 cohort ages.
- **Departmental payroll:** **IT has the highest total payroll ($23.6M)**, notably ahead of Engineering ($17.2M) the next highest, followed by Marketing ($15.6M), Sales ($15.5M), HR ($14.8M), Finance ($14.7M), and Accounting, the lowest ($11.8M). IT stands out as a cost concentration point worth further review (e.g., headcount vs. average salary in that department).
- **Hiring trend:** Hiring grew fairly consistently through the year, from 61 hires in January to 112 in December indicating active workforce expansion, with some month-to-month volatility (e.g., a dip in April to 58).
- **Sales trend:** Monthly sales were volatile but trended upward overall, dipping in February ($4.1M) and July ($7.7M), and peaking in November ($14.4M), before a slight pullback in December ($12.4M).

## Recommendations

1. **Investigate IT's payroll concentration** : check average salary per employee by department to see if $23.6M reflects headcount, high individual pay, or both.
2. **Plan for the 48–57 age cohort**: the largest segment (28% of staff); start succession planning for key roles before retirements hit.
3. **Look into the April hiring dip**: determine if it's seasonal, budget-driven, or a temporary freeze.
4. **Test the hiring-sales relationship**: correlate the two trends rather than just comparing them visually.
5. **Break payroll and demographics down by country**: the slicer supports this; not yet analyzed.
6. **Add a headcount-by-department chart**: pairs with the salary chart to show cost efficiency, not just cost volume.

## Limitations

- The dashboard presents aggregated totals, not row-level detail; deeper patterns (e.g., pay equity within age or gender groups) would require further breakdown.
- No visible correlation analysis was performed between hiring trend and sales trend, even though both are shown side-by-side, any relationship stated would be observational, not statistically tested.
- Country-level filtering (via the slicer) affects headcount view but department/salary/age breakdowns per country were not separately analyzed in this write-up.
- As a practice/bootcamp dataset, the data may be synthetic and may not reflect real-world workforce dynamics.

## References

- *Data Analytics Made Accessible* by Anil Maheshwari

---

**Author:** Ebubechukwu Osy-Uzoekwe

Connect on [LinkedIn](#https://www.linkedin.com/in/ebubechukwu-osy-uzoekwe-710720416/)
