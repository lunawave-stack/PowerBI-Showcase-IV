# PowerBI-Showcase-IV
Power BI DAX Calculations Lab
Course: PL-300: Microsoft Power BI Data Analyst
Lab: 04 – Create DAX Calculations

Overview
This lab demonstrates the creation and implementation of Data Analysis Expressions (DAX) to extend a semantic data model with calculated tables, calculated columns, and measures. Key outcomes include a fiscal-aware Date table, a duplicated Salesperson table for direct sales attribution, and business metrics such as price statistics, order counts, and performance variance against targets.

Key Activities
Calculated Tables:
Created Salesperson (a copy of Salesperson (Performance)) to re-establish a direct relationship with the Sales table.
Built a dynamic fiscal Date table using CALENDARAUTO(6) to align with Adventure Works’ July–June fiscal year.
Calculated Columns:
Added Year, Quarter, and Month columns to support time-based grouping.
Implemented a hidden MonthKey column to enforce chronological sorting of months.
Hierarchies & Model Design:
Defined a Fiscal hierarchy (Year → Quarter → Month) in the Date table.
Marked the Date table as a date table to enable time intelligence.
Hidden raw date columns (OrderDate, TargetMonth) and technical keys to streamline the reporting interface.
Measures:
Created simple aggregation measures:
Pricing: Avg Price, Median Price, Min Price, Max Price (grouped in Pricing display folder).
Volume: Orders (DISTINCTCOUNT), Order Lines (COUNTROWS) (grouped in Counts).
Developed performance measures in the Targets table:
Target (context-sensitive using HASONEVALUE)
Variance and Variance Margin (formatted as currency and percentage, respectively)
Hidden source columns (e.g., Unit Price, TargetAmount) to enforce correct usage via measures.
Outcome
The data model now supports accurate fiscal-year reporting, eliminates ambiguous aggregations, and provides clear, business-ready metrics for sales and performance analysis—all while maintaining a clean and intuitive interface for report authors.

Prepared by: Pang Kah Hwee
December 2025
