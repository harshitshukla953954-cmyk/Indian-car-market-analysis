# Indian Car Market Analysis — Consumer Preferences (2019–2024)

A Power BI portfolio project exploring car-buyer preferences, vehicle-segment mix, customer demographics, purchase behaviour, and satisfaction across the records in the supplied dataset.

> **Data limitation:** This repository contains a dataset supplied for portfolio analysis. The workbook does not establish that these records represent a statistically representative sample of the entire Indian automobile market. Treat findings as patterns in this dataset, not official national market-share estimates. Confirm the dataset's provenance before making external market claims.

## Business question

How do vehicle-segment preferences and purchase behaviours vary by year, customer profile, geography, and buying priorities—and what useful questions can these patterns raise for automobile manufacturers and dealerships?

## Project objectives

- Explore the mix of car segments over time (2019–2024).
- Compare preferences by state, city tier, age group, occupation, and income.
- Review fuel-type, purchase-financing, information-source, and test-drive patterns.
- Examine customer satisfaction and recommendation intent.
- Translate dashboard observations into cautious, evidence-based business questions.

## Dataset at a glance

- **Records:** 1,500
- **Period:** 2019–2024
- **Brands:** 16
- **Car models:** 69
- **States:** 10
- **Cities:** 30
- **Fields:** 31 columns covering transaction identifiers, time, geography, demographics, vehicle attributes, purchase behaviour, and satisfaction.

Files are provided in `data/`:
- `indian_car_market_data.csv` — transaction-level data exported from the workbook's `Raw_Data` sheet.
- `data_dictionary.csv` — field definitions and business relevance from the workbook.

## Initial observations from the supplied dataset

These are descriptive findings from the 1,500 rows—not claims about the whole Indian market:

- SUV records represent **48.6%** of all records in this dataset.
- The SUV share within each year's records changes from **29.6% in 2019** to **61.4% in 2024**. Because the annual row counts differ, use within-year share rather than raw counts for segment comparisons.
- **69.8%** of records are marked as financed purchases.
- The average recorded satisfaction score is **4.03 out of 5**.
- **70.0%** of records indicate a test drive was taken.
- The largest age group by record count is **26-35** (29.3% of records).

Interpretation should account for sample composition, missing values, and the absence of documented sampling methodology.

## Power BI report

[Open the Power BI report](https://app.powerbi.com/groups/me/reports/17816541-9caf-4994-90da-fed8d7bd5d27/7c53b560bf4d650ed509?experience=power-bi)

The link may require the owner's Microsoft account or report permissions. For a public portfolio, add exported dashboard screenshots under `images/` and ensure you have permission to share the report and data publicly.

## Recommended dashboard pages

1. **Market Overview:** transaction count, SUV share, average listed price, satisfaction, segment mix over time, brand distribution.
2. **Customer Profile:** age, income, occupation, family size, and segment preference.
3. **Geography:** state, city, and city-tier comparisons.
4. **Purchase Behaviour:** buying reasons, fuel type, financing, research source, and test-drive behaviour.
5. **Customer Experience:** satisfaction by segment/brand, recommendation intent, and feature-importance ratings.

## Data preparation and modelling

1. Load `data/indian_car_market_data.csv` into Power BI.
2. Check data types and categorical consistency in Power Query.
3. Review `Previous_Segment` missingness before using it for segment-migration analysis; blanks may be expected for non-repeat buyers, but confirm the dataset's coding logic.
4. Create a calendar table and relate it to the transaction year/date field if using time-intelligence measures. The supplied dataset has `Year` and `Quarter`, not a full transaction date, so use a year/quarter key or create a suitable date mapping deliberately.
5. Add the DAX measures in `dax/measures.dax` and validate results against visual totals.
6. Document any transformations and assumptions in the final Power BI report.

## Key measures

Starter measures are supplied in `dax/measures.dax`. These are examples and should be validated in your own model before publication.

## Repository structure

```text
indian-car-market-analysis/
├── README.md
├── data/
│   ├── indian_car_market_data.csv
│   └── data_dictionary.csv
├── dax/
│   └── measures.dax
├── docs/
│   └── project-notes.md
├── images/                  # Add dashboard screenshots before publishing
└── .gitignore
```

## Tools

- Microsoft Power BI Desktop
- Power Query
- DAX
- CSV / Excel

## Business value

The analysis can help structure questions about segment preference, customer profiles, financing behaviour, and satisfaction. Any recommendation should be tied to a visible chart, clearly defined metric, and the limitations of this dataset.

## How to reproduce

1. Download or clone this repository.
2. Open Power BI Desktop and import `data/indian_car_market_data.csv`.
3. Verify column types and blanks; document any changes.
4. Create visuals based on the recommended dashboard pages.
5. Add the DAX measures and validate them against the source data.
6. Save your `.pbix` file locally. If you choose to publish it, only share it after checking data permissions and report access settings.

## Author

Harshit Shukla — MBA, Business Analytics
