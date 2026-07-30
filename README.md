# E-Commerce Returns & Refund Loss Analysis

## Problem Statement
Rising product returns and refunds were impacting net revenue. This project 
identifies the key drivers behind returns and recommends data-backed actions 
to reduce return-driven revenue leakage.

## Dataset
Raw e-commerce order dataset (~2,900 records) containing intentional real-world 
data issues: mixed date formats, inconsistent text casing, currency-formatted 
numbers, duplicate rows, and missing values.

## Tools Used
Power Query, Power BI, DAX

## Data Cleaning (Power Query)
- Parsed OrderDate, DeliveryDate, and RefundDate from 5 mixed text formats into 
  a standard date type using conditional custom columns
- Standardized inconsistent casing/spacing across Category, OrderStatus, Channel
- Extracted numeric values from currency-formatted price fields
- Removed duplicate and fully blank rows
- Flagged invalid Quantity and Discount values instead of silently deleting them

## Key Insights
- Overall return rate: 19.1%
- Return rate fluctuates monthly (16%–22%) rather than trending steadily worse
- Beauty and Home & Kitchen categories have the highest return share
- 30%+ of returns have no logged reason, caused by an optional form field
- Returns are spread across cities without strong regional concentration

## Recommendations
- Make return-reason selection mandatory (dropdown, not free text)
- Focus quality checks on Beauty and Home & Kitchen categories
- Track return rate (%) monthly, not raw count, to avoid misreading volume 
  spikes as a worsening trend

## Data Limitation
Refunded and Returned status counts matched exactly in some periods, likely 
indicating overlapping status definitions in the source data — noted here for 
transparency.