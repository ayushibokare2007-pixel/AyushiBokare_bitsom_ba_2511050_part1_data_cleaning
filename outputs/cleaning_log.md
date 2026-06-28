# Data Cleaning Log

## Issues Found

The raw dataset contained multiple data quality issues including:

* Leading and trailing spaces in text fields.
* Inconsistent capitalization.
* Missing Region values.
* Missing Ship Mode values.
* Missing Discount values.
* Mixed date formats in Order Date and Ship Date.
* Exact duplicate records.
* Duplicate Order IDs.
* Negative discount values.
* Invalid shipping records where Ship Date occurred before Order Date.
* Sales and profit calculation inconsistencies.

---

## Cleaning Actions Performed

### Text Standardization

* Applied TRIM() to remove extra spaces.
* Standardized capitalization using PROPER().
* Standardized Region, Segment, Category, Sub-Category, Ship Mode, Payment Status, and Order Status values.
* Removed unwanted special characters where applicable.

### Date Cleaning

* Converted Order Date and Ship Date into a consistent date format.
* Created shipping_delay_days column.
* Flagged invalid shipping records.

### Missing Value Handling

* Missing Region values were replaced with "Unknown".
* Missing Ship Mode values were replaced with "Unknown".
* Missing Discount values were replaced with 0 where business rules allowed.

### Duplicate Handling

* Exact duplicate rows were identified and removed.
* Duplicate Order IDs were retained and flagged for manual review.

### Business Rule Validation

* Negative discounts were flagged as invalid.
* Failed payment orders were excluded from completed sales calculations.
* Cancelled orders were excluded from completed sales calculations.
* Refunded orders were separately summarized.

---

## Business Rules Applied

* Missing Region → Unknown
* Missing Ship Mode → Unknown
* Missing Discount → 0
* Negative Discount → Invalid
* Ship Date before Order Date → Invalid Shipping Record
* Failed Payment → Excluded from completed sales
* Cancelled Order → Excluded from completed sales
* Refunded Order → Separate reporting category

---

## Records Removed

* Exact duplicate records were removed after verification.

## Records Flagged

* Duplicate Order IDs
* Invalid Discounts
* Invalid Shipping Records
* Business Rule Violations

---

## Assumptions

* Unknown values were retained to preserve records.
* Refunded orders remain in the dataset for reporting purposes.
* Duplicate Order IDs require business review.

---

## Limitations

* Some duplicate Order IDs may require manual investigation.
* Source-system errors cannot be independently verified.
* Cleaning decisions were based only on provided business rules.
