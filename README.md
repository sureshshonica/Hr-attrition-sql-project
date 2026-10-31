# HR Employee Attrition Analysis

## Overview
An end-to-end analysis of the IBM HR Employee Attrition dataset (1,470 employee records), completed in three stages: SQL for querying, Power BI for dashboarding, and Excel for pivot-table analysis. The goal was to find which departments lose the most employees and to compare them fairly using attrition rates instead of raw counts.

## Tools Used
- SQL (SQLite Online): querying and aggregation
- Power BI Desktop: interactive dashboard
- Microsoft Excel: pivot table, pivot chart and rate calculation
- GitHub: project documentation

## Key Queries
-- Employees per department
SELECT Department, COUNT(*) FROM HRE GROUP BY Department;

-- Attrition count per department
SELECT Department, COUNT(*) FROM HRE WHERE Attrition = 'Yes' GROUP BY Department;

-- Average age per department
SELECT Department, AVG(Age) FROM HRE GROUP BY Department;

## Power BI Dashboard
A dashboard with three visuals: a total employee count card, an overall attrition pie chart, and a department-wise attrition bar chart.

## Excel Analysis
A pivot table and pivot chart comparing attrition by department, plus an attrition rate calculation (Yes ÷ Total).

## Key Insight
Research & Development has the highest attrition count (133 of 961), but the lowest attrition rate (13.8%). Sales has the highest rate (20.6%, 92 of 446), followed by Human Resources (19.0%, 12 of 63). Overall attrition is 16.1% (237 of 1,470). Comparing rates instead of raw counts shows where the real retention problem is.

## Files in this Repository
- sql project result.xlsx: SQL query results
- HR_Attrition_Dashboard.pdf: Power BI dashboard
- HR_Attrition_Excel.xlsx: Excel pivot analysis
