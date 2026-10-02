# DOE Lab 05: Block a Replicated Seal-Strength Experiment

**Alignment:** LO2
**NovaDOE method:** NovaDOE full factorial + blocked run sheet
**Scenario:** Seal trials span morning and afternoon shifts whose ambient conditions differ.

## Goal

Use blocking to remove shift-to-shift variation without sacrificing treatment balance.

## Files

- `README.md` — this self-contained lab brief
- `mock-data.csv` — supplied experimental responses
- `DOE-Lab-Workbook.xlsx` — learner workbook with instructions, data, analysis and evidence sheets
- `expected-results.md` — acceptance criteria and interpretation prompts

## Detailed procedure

1. **Generate a 2² full factorial in NovaDOE.** Export the four standard treatments.
2. **Duplicate the design into two blocks.** Name blocks AM and PM; do not change factor combinations.
3. **Randomise the four runs independently inside each block.** Use a fixed recorded seed or Excel RAND with values frozen.
4. **Import the response dataset.** Check every block has each treatment once.
5. **Estimate treatment and block means.** Use formulas with visible denominators.
6. **Compare models with and without the block term.** Explain what variation the block absorbs.
7. **Review the deviation log.** Decide whether any run needs investigation, not silent deletion.

## Acceptance test

Each block contains all four treatments, run order is randomised within block and the block-adjusted conclusion is documented.

## Evidence to submit

- Exported NovaDOE design CSV (`learner-design.csv`).
- Completed workbook with formulas and interpretation.
- Screenshot of the NovaDOE design summary and results table.
- Short recommendation with limitations and follow-up action.

NovaDOE: https://alfredang.github.io/novadoe/
