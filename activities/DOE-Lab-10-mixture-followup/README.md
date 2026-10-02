# DOE Lab 10: Optimise a Three-Component Thermal Paste Mixture

**Alignment:** LO4
**NovaDOE method:** NovaDOE Latin Hypercube for candidate exploration + simplex filtering
**Scenario:** A thermal-materials lab blends ceramic filler, binder and additive; proportions must total 100%.

## Goal

Recognise the mixture constraint, map a simplex design and recommend a constrained follow-up.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Select Latin Hypercube in NovaDOE.** Generate at least 40 candidate points for three numeric proportions.
2. **Export the candidate design.** Treat the values as proportions, not independent production settings.
3. **Normalise each row so the three components sum to 1.** Use formulas and show the original values.
4. **Filter candidates against component bounds.** Retain the feasibility flag.
5. **Select a balanced subset spanning vertices, edges and centre-like blends.** Document the selection rule.
6. **Join the mock response data for the selected blends.** Do not extrapolate to discarded infeasible candidates.
7. **Fit a simple mixture model and compare predictions.** Avoid an intercept if using canonical mixture terms.
8. **Recommend a blend and follow-up extreme-vertices experiment.** State composition tolerance and validation tests.
9. **Review the full portfolio of ten labs.** Link the outcome to an evaluation of effectiveness and follow-up actions.

## Acceptance test

Every retained blend sums to 1.000 within tolerance, satisfies bounds and leads to a constrained follow-up recommendation.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
