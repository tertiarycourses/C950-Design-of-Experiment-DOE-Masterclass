# DOE Lab 07: Screen Eleven Battery-Process Factors

**Alignment:** LO3
**NovaDOE method:** NovaDOE Plackett-Burman
**Scenario:** A battery lab must screen eleven formulation and process factors in twelve runs.

## Goal

Use a Plackett-Burman design to reduce a long factor list before modelling interactions.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Select Plackett-Burman in NovaDOE.** Create eleven two-level numeric factors.
2. **Generate a 12-run design.** Confirm the summary reports 12 runs and 11 factors.
3. **Export the design and join mock capacity-retention results.** Keep factors in the same order.
4. **Calculate each main-effect contrast.** Use the high-level average minus low-level average.
5. **Create a ranked effect chart.** Show absolute magnitude and sign.
6. **Assess interaction contamination risk.** Use process knowledge to identify plausible two-factor interactions.
7. **Choose three or four factors for follow-up.** Balance evidence, controllability, safety and cost.
8. **Draft a full or fractional factorial confirmation.** Do not optimise from the PB model alone.

## Acceptance test

All eleven main effects are ranked and the report explicitly states that interactions are not separately estimable in the screening design.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
