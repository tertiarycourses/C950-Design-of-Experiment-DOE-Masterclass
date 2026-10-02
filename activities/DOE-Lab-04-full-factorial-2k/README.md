# DOE Lab 04: Model a 2³ Composite Bonding Experiment

**Alignment:** LO2
**NovaDOE method:** NovaDOE full factorial
**Scenario:** A bonding team studies temperature, pressure and surface preparation to maximise joint strength.

## Goal

Analyse main and interaction effects in a three-factor design and select a practical model.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Choose Full Factorial and add three factors.** Use two numeric and one categorical factor.
2. **Generate the eight-run design and export CSV.** Verify 2³ = 8 unique treatment combinations.
3. **Join the response values from mock-data.csv.** Preserve RunOrder and StandardOrder.
4. **Code numeric and categorical low/high levels as -1/+1.** Document the coding table.
5. **Calculate A, B, C, AB, AC, BC and ABC contrast estimates.** Use auditable worksheet formulas.
6. **Build a Pareto-style effect chart.** Label effect magnitudes and direction separately.
7. **Fit a hierarchical coded regression model.** Inspect residuals before reducing terms.
8. **Predict and confirm the proposed operating combination.** State limits of the two-level region.

## Acceptance test

The workbook contains all seven effect estimates, a hierarchical model, residual check and a recommendation in engineering units.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
