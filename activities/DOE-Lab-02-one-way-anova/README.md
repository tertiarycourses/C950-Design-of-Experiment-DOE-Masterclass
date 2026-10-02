# DOE Lab 02: Compare Coating Cure Temperatures with One-Way ANOVA

**Alignment:** LO1
**NovaDOE method:** NovaDOE full factorial (one 4-level categorical factor) + Excel ANOVA
**Scenario:** A coating line compares four cure temperatures using adhesion strength from replicated coupons.

## Goal

Separate between-treatment and within-treatment variation and interpret an ANOVA decision.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Choose Full Factorial in NovaDOE.** Create a categorical factor with 140, 150, 160 and 170 °C levels.
2. **Generate the design and export CSV.** Retain the level labels.
3. **Open mock-data.csv and inspect the five replicates per level.** Flag any missing or impossible values.
4. **Paste or link the data into the workbook Raw_Data sheet.** Keep the source table unchanged.
5. **Calculate group count, mean and standard deviation.** Use Excel formulas in the Analysis sheet.
6. **Run Data Analysis > ANOVA: Single Factor.** Use alpha = 0.05 and include labels.
7. **Interpret F, p-value and practical difference.** State whether follow-up comparisons are warranted.

## Acceptance test

The ANOVA uses 20 observations, reports the correct factor levels and gives a conclusion that separates statistical from practical significance.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
