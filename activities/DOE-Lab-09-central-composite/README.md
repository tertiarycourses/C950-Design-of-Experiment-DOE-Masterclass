# DOE Lab 09: Optimise Sterile-Package Seal Strength with CCD

**Alignment:** LO4
**NovaDOE method:** NovaDOE Central Composite
**Scenario:** A medical-packaging engineer targets seal strength of 26 N within an acceptable 20–32 N range.

## Goal

Generate a CCD, fit a quadratic response surface and identify a feasible operating window.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Select Central Composite in NovaDOE.** Add three numeric factors with low/high bounds.
2. **Choose face-centred or circumscribed geometry based on safe limits.** Record the chosen CCD type and centre points.
3. **Generate and export the design.** Verify factorial, axial and centre runs are present.
4. **Join mock seal-strength responses.** Flag values outside 20–32 N without deleting them.
5. **Create linear, interaction and squared columns.** Use coded factor levels.
6. **Fit the quadratic model with Excel Regression or LINEST.** Retain hierarchy and inspect residuals.
7. **Create contour-ready prediction grids.** Keep predictions within the experimental region.
8. **Select settings closest to 26 N with low sensitivity.** Balance target achievement and robustness.
9. **Define and evaluate confirmation trials.** Compare observed with predicted interval.

## Acceptance test

The design includes factorial, axial and centre points; the recommendation targets 26 N and includes confirmation evidence.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
