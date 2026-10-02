# DOE Lab 03: Reduce Order-Processing Time with a 2² Factorial

**Alignment:** LO2
**NovaDOE method:** NovaDOE full factorial
**Scenario:** A distribution centre tests Current/New ordering systems and Packing A/B to minimise processing hours.

## Goal

Estimate two main effects and their interaction from a replicated 2² experiment.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Select Full Factorial in NovaDOE.** Add two categorical factors with two levels each.
2. **Set three replicates and generate the design.** If the UI has no replicate field, export once and duplicate treatment combinations in Excel.
3. **Export CSV and join the provided Hours values by standard order.** Never join by the random run number.
4. **Calculate treatment means and high-minus-low effects.** Use formulas and show the sign convention.
5. **Create a main-effects chart.** Keep the vertical scale identical across panels.
6. **Create an interaction chart.** Compare slopes and explain non-parallel lines.
7. **Fit a coded model including A, B and A×B.** Retain hierarchy if the interaction is kept.
8. **Recommend the lowest-time combination with evidence.** Include a confirmation-run plan.

## Acceptance test

All four combinations have three independent replicates and the recommendation cites both the predicted response and interaction risk.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
