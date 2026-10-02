# DOE Lab 06: Screen Five Factors with a Resolution V Half Fraction

**Alignment:** LO3
**NovaDOE method:** NovaDOE fractional factorial
**Scenario:** A polymer extrusion team has five controllable factors but only 16 safe pilot runs.

## Goal

Generate a defensible 2^(5-1) design, interpret aliases and plan confirmation.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Select Fractional Factorial in NovaDOE.** Add five numeric factors with safe low/high limits.
2. **Choose a 16-run fraction and record the displayed resolution.** Target Resolution V where supported.
3. **Generate and export the design CSV.** Save the NovaDOE setup in browser storage as well.
4. **Import the mock response and code factor levels.** Lower defect rate is better.
5. **Calculate main-effect contrasts.** Rank absolute effects and retain signs.
6. **Write the generator and alias interpretation in the workbook.** If NovaDOE does not display aliases, document the assumed generator from the exported matrix.
7. **Select factors for a confirmation experiment.** Use magnitude, feasibility and engineering plausibility.
8. **Plan confirmation and possible foldover runs.** Define expected improvement and acceptance threshold.

## Acceptance test

The design has 16 unique runs, five factor columns, a stated resolution/alias assumption and a confirmation plan that does not overclaim aliased effects.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
