# DOE Lab 08: Design a Robust Golf-Ball Process with Taguchi Logic

**Alignment:** LO4
**NovaDOE method:** NovaDOE full/fractional matrix used as an orthogonal-array proxy
**Scenario:** A golf-equipment team tests four two-level control factors under Driver and 5-Iron noise conditions.

## Goal

Separate control and noise factors and recommend robust rather than merely high-mean settings.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Generate an eight-run balanced two-level matrix in NovaDOE.** Use Fractional Factorial for four control factors.
2. **Export CSV and verify level balance.** Each level should occur equally often per factor.
3. **Join Driver and 5-Iron distance responses.** Treat club as a planned noise condition.
4. **Calculate run mean and standard deviation.** Use formulas and consistent units.
5. **Calculate larger-the-better S/N ratio.** Use -10*LOG10(AVERAGE(1/y²)).
6. **Create factor-response tables for mean and S/N.** Rank delta across levels.
7. **Choose settings that maximise S/N, then tune mean.** Explain any trade-off.
8. **Propose a confirmation trial across both noise conditions.** Set robustness acceptance criteria.

## Acceptance test

The recommended settings are justified by S/N ratio and mean response, with a confirmation plan across both club conditions.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
