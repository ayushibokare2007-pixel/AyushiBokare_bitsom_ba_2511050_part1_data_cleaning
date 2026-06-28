# Business Data Cleaning, Validation and Reporting Project

## Problem Summary

The retail sales dataset contained inconsistencies, missing values, duplicate records, invalid discounts, mixed date formats, and business rule violations. The objective was to clean and validate the data to create an analysis-ready dataset for reporting and business decision-making.

---

## Dataset Description

The dataset contains:

* Order information
* Customer information
* Product details
* Geographic information
* Shipping information
* Sales and profit metrics
* Payment and order status information

---

## Tools Used

* Microsoft Excel
* Pivot Tables
* Conditional Formatting
* Data Validation
* Excel Functions (TRIM, PROPER, IF, COUNTIF, YEAR, MONTH)

---

## Cleaning Steps Performed

1. Standardized text fields.
2. Removed leading and trailing spaces.
3. Corrected capitalization inconsistencies.
4. Standardized categories and status values.
5. Converted dates into a consistent format.
6. Calculated shipping delay days.
7. Handled missing values.
8. Identified duplicate records.
9. Applied business rules.
10. Created calculated columns.
11. Generated data quality reports.
12. Created pivot summary reports.

---

## Business Rules Applied

* Missing Region → Unknown
* Missing Ship Mode → Unknown
* Missing Discount → 0
* Negative Discount → Invalid
* Invalid Shipping Records → Flagged
* Failed Payments → Excluded from completed sales
* Cancelled Orders → Excluded from completed sales
* Refunded Orders → Reported separately

---

## Data Quality Issues Found

* Missing Region values
* Missing Ship Mode values
* Missing Discount values
* Exact duplicate rows
* Duplicate Order IDs
* Negative discounts
* Mixed date formats
* Invalid shipping records

---

## Calculated Columns Created

* cleaned_discount
* calculated_sales
* calculated_profit
* profit_margin
* shipping_delay_days
* order_month
* order_year
* data_quality_flag

---

## Pivot Reports Created

### Sales and Profit by Region

Used to compare regional business performance.

### Sales and Profit by Category and Sub-Category

Used to identify top-performing product groups.

### Order Count by Ship Mode

Used to analyze shipping preferences.

### Profit Margin by Customer Segment

Used to compare profitability across customer segments.

### Refunded / Cancelled / Failed Orders by Region

Used to evaluate operational risks.

### Monthly Sales Trend

Used to identify sales seasonality.

---

## Key Business Insights

* Completed orders generated the majority of revenue.
* Certain regions contributed significantly more sales than others.
* Technology and Furniture categories contributed a large share of revenue.
* Standard Class shipping was the most frequently used shipping mode.
* Cancelled and failed payment orders reduced realized revenue.
* Data quality improvements significantly increased reporting reliability.

---

## Assumptions

* Unknown values were retained instead of removing records.
* Duplicate Order IDs were flagged instead of deleted.
* Missing discount values were treated as zero when valid.

---

## Limitations

* Duplicate Order IDs may require manual review.
* Source-system errors cannot be independently verified.
* Some business decisions may require additional context beyond the dataset.

---

## Screenshots Included

* raw_data_preview.png
* cleaned_data_preview.png
* pivot_summary_1.png
* pivot_summary_2.png
