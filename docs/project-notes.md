# Project notes and validation checklist

## Data checks performed on the supplied workbook

- Raw data shape: 1500 rows × 31 columns.
- Duplicate full rows: 0.
- Duplicate transaction IDs: 0.
- `Previous_Segment` has 924 blanks. Investigate whether blanks are expected for first-time buyers/non-repeat buyers before filling or removing them.
- The dataset includes records in years 2019–2024 with unequal row counts by year. Prefer percentage share for comparing segment mix across years.
- No source/methodology note was present in the supplied workbook, so do not describe the records as official national market statistics without verifying provenance.

## Useful questions to investigate

1. How did the segment mix change year by year?
2. How do segment preferences differ across age groups and city tiers?
3. Which buying reasons are most common within each segment?
4. How do fuel preferences differ by year and segment?
5. How do financing, test-drive behaviour, satisfaction, and recommendation intent relate?
6. Do satisfaction differences persist after segment/price/customer filters are applied?

## Before publishing

- [ ] Confirm permission to share the dataset publicly.
- [ ] Confirm whether the dataset is synthetic, anonymized, or sourced from a real provider; disclose that accurately.
- [ ] Validate all dashboard measures against the CSV.
- [ ] Add dashboard screenshots to `images/`.
- [ ] Add the `.pbix` file only if size and data-sharing permissions allow it.
- [ ] Ensure the Power BI link works for the intended audience.
- [ ] Avoid presenting associations as causal findings.
