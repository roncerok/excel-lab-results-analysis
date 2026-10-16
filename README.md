# Laboratory Results Analysis in Excel

An Excel project exploring synthetic laboratory results for 28 fictional patients. Built during a data-analysis course, it combines data preparation, relational modelling, interactive reporting and a single-patient results checker.

**Tools:** Excel · Power Query · Power Pivot · DAX · PivotTables · Slicers · Conditional formatting

## Explore the project

- [Dashboard preview (PDF)](preview/Charts.pdf)
- [Patient checker example (PDF)](preview/Patient_checker.pdf)
- [Project overview (PDF)](preview/Overview.pdf)
- [Excel workbook](Lab_Project.xlsx)

The PDFs provide static previews without requiring Excel.

## Data and questions

The course dataset contains 364 laboratory results: 13 measurements for each of 28 fictional patients. All patient details and test results are synthetic; no real patient data are included.

The analysis addresses four questions:

1. How does the proportion of patients with LDL above 130 mg/dL vary by gender and age group?
2. How does the proportion with haemoglobin below 11 g/dL vary by gender and age group?
3. How does the proportion with ALT above 56 U/L vary by gender and age group?
4. How frequently does low HDL occur among patients with high LDL, compared with those whose LDL is within the supplied range?

## Approach

- Used Power Query to prepare the data and classify results against the supplied reference intervals.
- Built a Power Pivot model linking laboratory results to patient and reference-interval tables.
- Used DAX measures and PivotTables to calculate patient counts and proportions.
- Created charts with age and gender slicers for interactive exploration.
- Applied conditional formatting to highlight results outside the supplied ranges.
- Built a separate checker with input validation and formulas to assess manually entered results.

The sample was divided into two age groups, under 50 and 50+, with 14 patients in each. Although the sample contains equal numbers of women and men overall, their distribution differs between age groups.

## Main findings

| Measure | Finding in the synthetic sample |
| --- | --- |
| High LDL | 42.9% of patients (12/28), with a higher proportion in the 50+ group (78.6%) than the under-50 group (7.1%) |
| Low haemoglobin | 17.9% of patients (5/28); all five were women |
| High ALT | 14.3% of patients (4/28); all four were aged 50+ |
| LDL–HDL relationship | 58.3% of patients with high LDL (7/12) also had low HDL, compared with 0/16 patients with within-range LDL |

These findings describe the synthetic dataset only and cannot be generalised to real patient populations.

## Using the workbook

1. Download the workbook and open it in desktop Excel with Power Pivot support.
2. Start with the **Overview** sheet.
3. Explore **Main measures** and **Charts** using the age and gender slicers. Clear the filters to return to the full sample.
4. In **Patient Checker**, enter values in the blue input cells using the displayed units.

The checker labels results as **Low**, **Within range** or **High**. For HDL, it reports only **Low** or **Not low**, because the supplied upper reference limit remains unresolved.

Checker inputs do not change the analysis dataset, PivotTables or charts. Clear the input cells before entering another example.

### Data refresh

The workbook contains saved data and analysis results. Refreshing Power Query requires access to the original course source files and may require updating their file paths. Those source files are not included in this repository.

## Validation and limitations

- Checked the dataset for duplicate patient–measurement combinations: all 364 combinations were unique.
- Reconciled the headline counts and percentages with the underlying records.
- Checked all saved result classifications against the supplied reference intervals.
- Tested the checker at the LDL and HDL thresholds and confirmed that the chart slicers respond to selections.

This is a small, synthetic training dataset. Differences between groups are descriptive, and the unequal gender distribution within age groups limits comparisons.

Reference intervals are those supplied for the exercise. The workbook and checker demonstrate Excel functionality and are not diagnostic tools.
