# Learner Guide — Design of Experiment (DOE) Masterclass

Course Code: C950  
Version: v1.0 · 2 October 2026

## How to use this guide

The slide deck is concept-led and visual. This guide contains the detailed procedures for all NovaDOE activities.

- NovaDOE: https://alfredang.github.io/novadoe/
- LMS: https://lms-tms.tertiaryinfotech.com/
- Repository: https://github.com/tertiarycourses/C950-Design-of-Experiment-DOE-Masterclass

## Learning outcomes

- LO1: Analyse process interactions to characterise key factors influencing performance in Design of Experiments.
- LO2: Select suitable factorial DoE projects by evaluating relevant performance metrics.
- LO3: Define the scope and execute fractional factorial DoE projects using problem-solving techniques.
- LO4: Evaluate the effectiveness of DoE projects and recommend follow-up actions.


## Topic 01: Fundamentals of Design of Experiments

Questions, variables, variation, hypothesis tests and one-way ANOVA

### Key concepts

- **Engineering experiments:** Learn efficiently from controlled variation. Reduce development time; improve performance; quantify uncertainty; build robust products. *Decision lens:* A useful experiment changes a decision, not merely a chart.
- **DoE lifecycle:** Plan before collecting data. State problem; choose factors and levels; select response; choose design; run; analyse; conclude. *Decision lens:* Pre-register the response and decision rule.
- **Factor, level, treatment, response:** Name the experimental structure. Factor is controlled input; level is setting; treatment is combination; response is measured output. *Decision lens:* Units and permissible ranges belong in the factor table.
- **Independent and dependent variables:** Separate inputs from outcomes. Independent variables are manipulated; dependent variables respond; nuisance variables are controlled or blocked. *Decision lens:* Do not call an observed association an intervention.
- **OFAT versus DoE:** Interactions require coordinated changes. OFAT is intuitive but inefficient; factorial DoE estimates several effects; interactions are visible; prediction covers the region. *Decision lens:* Use OFAT only for safe preliminary range-finding.
- **Randomisation, replication and blocking:** Protect inference from bias and noise. Randomise run order; replicate treatments; block known nuisance sources; retain run-order evidence. *Decision lens:* Repeats measure equipment precision; replicates estimate process variation.
- **Measurement systems:** Bad measurements cannot be rescued statistically. Define method; verify resolution; control calibration; use consistent units; record missingness. *Decision lens:* Measurement error can hide real effects or create false ones.
- **Hypothesis testing:** Translate evidence into a decision rule. Write null and alternative; choose statistic; calculate p-value; compare with alpha; interpret. *Decision lens:* A p-value is conditional on the null and assumptions.
- **Type I and Type II errors:** Balance false alarms and missed effects. Type I rejects a true null; Type II misses a real effect; power depends on effect, noise and sample size. *Decision lens:* Choose risk thresholds from consequence, not habit.
- **Two-sample comparisons:** Match the test to the sampling design. Independent groups differ from paired measurements; inspect variance; report effect and uncertainty. *Decision lens:* Statistical significance does not guarantee practical value.
- **One-way ANOVA:** Compare more than two treatment means. Partition total variation; estimate between and within variation; compute F ratio; test equal means. *Decision lens:* Follow a significant omnibus test with planned comparisons.
- **Sum-of-squares decomposition:** Account for where variation comes from. SST equals model plus error; degrees of freedom scale mean squares; F compares signal to noise. *Decision lens:* Balanced designs make decomposition easier to audit.

### DOE Lab 01: Characterise a Composite Cure Process

**Alignment:** LO1  
**Method:** NovaDOE full factorial planning workspace  
**Scenario:** A materials team must reduce cure-cycle variation before testing a new composite panel.

**Goal:** Frame a measurable DoE project and distinguish factors, levels, responses and nuisance variables.

**Expected output:** A signed experiment charter, factor table, 2² design CSV and run-order evidence.

#### Detailed procedure

1. **Open NovaDOE and choose Full Factorial.** Use the course NovaDOE URL; do not enter response values yet.
2. **Create the two numeric factors.** Set temperature 160–180 °C and time 45–75 min.
3. **Generate the four-run design and inspect coded levels.** Confirm every low/high combination occurs once.
4. **Export the design as CSV into the lab folder.** Name it learner-design.csv.
5. **Complete the charter sheet in the workbook.** State problem, response, unit, objective, constraints, nuisance variables and decision rule.
6. **Assign a random run order and record planned evidence.** Do not overwrite StandardOrder.
7. **Review the design with a peer before execution.** Use the scope, safety and measurement checklist.

#### Acceptance test

The factor table, four treatment combinations, response definition, random run order and go/no-go rule are all present.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 02: Compare Coating Cure Temperatures with One-Way ANOVA

**Alignment:** LO1  
**Method:** NovaDOE full factorial (one 4-level categorical factor) + Excel ANOVA  
**Scenario:** A coating line compares four cure temperatures using adhesion strength from replicated coupons.

**Goal:** Separate between-treatment and within-treatment variation and interpret an ANOVA decision.

**Expected output:** A randomised 4-level design, replicated response dataset, ANOVA table and engineering interpretation.

#### Detailed procedure

1. **Choose Full Factorial in NovaDOE.** Create a categorical factor with 140, 150, 160 and 170 °C levels.
2. **Generate the design and export CSV.** Retain the level labels.
3. **Open mock-data.csv and inspect the five replicates per level.** Flag any missing or impossible values.
4. **Paste or link the data into the workbook Raw_Data sheet.** Keep the source table unchanged.
5. **Calculate group count, mean and standard deviation.** Use Excel formulas in the Analysis sheet.
6. **Run Data Analysis > ANOVA: Single Factor.** Use alpha = 0.05 and include labels.
7. **Interpret F, p-value and practical difference.** State whether follow-up comparisons are warranted.

#### Acceptance test

The ANOVA uses 20 observations, reports the correct factor levels and gives a conclusion that separates statistical from practical significance.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

## Topic 02: Factorial Design of Experiments

Main effects, interactions, regression, ANOVA, blocks and confounding

### Key concepts

- **Factorial design:** Test combinations rather than isolated changes. All combinations estimate main effects; interaction estimates become possible; one dataset supports prediction. *Decision lens:* Keep the experimental region safe and relevant.
- **The 2^2 design:** Two factors at low and high levels. Four treatment combinations; coded levels -1 and +1; geometric square; balanced contrasts. *Decision lens:* Add replicates or centre points when pure error or curvature matters.
- **Main effects:** Average response change across another factor. Compare high versus low means; sign gives direction; magnitude gives practical influence; uncertainty qualifies the estimate. *Decision lens:* Averaging can conceal a strong interaction.
- **Interactions:** The effect of one factor depends on another. Non-parallel interaction lines; product term in regression; hierarchy principle; joint settings drive the decision. *Decision lens:* Never interpret main effects alone when interaction is material.
- **Coded regression model:** Connect design geometry to prediction. Intercept is grand mean; coefficients represent half-effects; product term models interaction; residuals test adequacy. *Decision lens:* Decode recommendations back to engineering units.
- **ANOVA for factorial designs:** Test model terms against residual noise. Degrees of freedom follow effects; mean square divides SS by df; F and p assess evidence; lack-of-fit needs replication. *Decision lens:* Report effect size and confidence intervals alongside p-values.
- **The 2^3 cube:** Three factors reveal two- and three-way interactions. Eight corners; three main effects; three two-way interactions; one three-way interaction. *Decision lens:* A high-order interaction is hard to explain and needs engineering evidence.
- **General 2^k designs:** Run count doubles with every factor. 2^k treatment combinations; orthogonal effect estimates; effect hierarchy guides model reduction; cost grows exponentially. *Decision lens:* Use fractional designs when screening many factors.
- **Pareto and normal effect plots:** Prioritise candidate effects. Standardised effects show magnitude; reference line guides screening; normal plot separates signal from noise. *Decision lens:* Plots support, but do not replace, model assumptions.
- **Centre points and curvature:** Check whether a straight plane is adequate. Centre runs estimate local curvature; replicated centres provide pure error; significant curvature motivates RSM. *Decision lens:* A centre point does not identify which quadratic term matters.
- **Replication strategy:** Create an honest error term. Independent replicates capture process variation; duplicate measurements capture measurement variation; power increases with information. *Decision lens:* Do not treat repeated readings from one specimen as independent runs.
- **Blocking:** Remove known nuisance variation. Group homogeneous runs; randomise within blocks; estimate block effect; preserve treatment balance. *Decision lens:* A block should not be confused with a factor of scientific interest.
- **Confounding in blocks:** Trade an interaction for practical run groups. Choose defining contrast; aliases follow; high-order terms are typical sacrifices; document the alias structure. *Decision lens:* Never confound an effect that stakeholders consider critical.

### DOE Lab 03: Reduce Order-Processing Time with a 2² Factorial

**Alignment:** LO2  
**Method:** NovaDOE full factorial  
**Scenario:** A distribution centre tests Current/New ordering systems and Packing A/B to minimise processing hours.

**Goal:** Estimate two main effects and their interaction from a replicated 2² experiment.

**Expected output:** A 12-run replicated design, effect table, interaction interpretation and recommended setting.

#### Detailed procedure

1. **Select Full Factorial in NovaDOE.** Add two categorical factors with two levels each.
2. **Set three replicates and generate the design.** If the UI has no replicate field, export once and duplicate treatment combinations in Excel.
3. **Export CSV and join the provided Hours values by standard order.** Never join by the random run number.
4. **Calculate treatment means and high-minus-low effects.** Use formulas and show the sign convention.
5. **Create a main-effects chart.** Keep the vertical scale identical across panels.
6. **Create an interaction chart.** Compare slopes and explain non-parallel lines.
7. **Fit a coded model including A, B and A×B.** Retain hierarchy if the interaction is kept.
8. **Recommend the lowest-time combination with evidence.** Include a confirmation-run plan.

#### Acceptance test

All four combinations have three independent replicates and the recommendation cites both the predicted response and interaction risk.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 04: Model a 2³ Composite Bonding Experiment

**Alignment:** LO2  
**Method:** NovaDOE full factorial  
**Scenario:** A bonding team studies temperature, pressure and surface preparation to maximise joint strength.

**Goal:** Analyse main and interaction effects in a three-factor design and select a practical model.

**Expected output:** An eight-corner cube design, effect hierarchy, coded regression and predicted optimum.

#### Detailed procedure

1. **Choose Full Factorial and add three factors.** Use two numeric and one categorical factor.
2. **Generate the eight-run design and export CSV.** Verify 2³ = 8 unique treatment combinations.
3. **Join the response values from mock-data.csv.** Preserve RunOrder and StandardOrder.
4. **Code numeric and categorical low/high levels as -1/+1.** Document the coding table.
5. **Calculate A, B, C, AB, AC, BC and ABC contrast estimates.** Use auditable worksheet formulas.
6. **Build a Pareto-style effect chart.** Label effect magnitudes and direction separately.
7. **Fit a hierarchical coded regression model.** Inspect residuals before reducing terms.
8. **Predict and confirm the proposed operating combination.** State limits of the two-level region.

#### Acceptance test

The workbook contains all seven effect estimates, a hierarchical model, residual check and a recommendation in engineering units.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 05: Block a Replicated Seal-Strength Experiment

**Alignment:** LO2  
**Method:** NovaDOE full factorial + blocked run sheet  
**Scenario:** Seal trials span morning and afternoon shifts whose ambient conditions differ.

**Goal:** Use blocking to remove shift-to-shift variation without sacrificing treatment balance.

**Expected output:** Two balanced blocks, randomisation within block, block-adjusted effects and deviation log.

#### Detailed procedure

1. **Generate a 2² full factorial in NovaDOE.** Export the four standard treatments.
2. **Duplicate the design into two blocks.** Name blocks AM and PM; do not change factor combinations.
3. **Randomise the four runs independently inside each block.** Use a fixed recorded seed or Excel RAND with values frozen.
4. **Import the response dataset.** Check every block has each treatment once.
5. **Estimate treatment and block means.** Use formulas with visible denominators.
6. **Compare models with and without the block term.** Explain what variation the block absorbs.
7. **Review the deviation log.** Decide whether any run needs investigation, not silent deletion.

#### Acceptance test

Each block contains all four treatments, run order is randomised within block and the block-adjusted conclusion is documented.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

## Topic 03: Fractional Factorial and Screening Designs

Generators, aliases, resolution, Plackett-Burman and sequential experimentation

### Key concepts

- **Why fractionate:** Screen many factors with fewer runs. Assume effect sparsity; select a defensible fraction; preserve critical estimates; reserve budget for confirmation. *Decision lens:* A fraction is a strategic information trade, not free efficiency.
- **One-half fractions:** Use a generator to select half the full design. Generator defines included runs; defining relation creates aliases; signs determine fraction; replicate if error is needed. *Decision lens:* Record the generator so the design is reproducible.
- **Alias structure:** Know which effects are inseparable. Multiply effects by defining words; aliases share estimates; resolution summarises shortest word; subject knowledge breaks ambiguity. *Decision lens:* Do not label an aliased estimate as one unique physical cause.
- **Resolution III:** Main effects alias with two-factor interactions. Useful for early screening; smallest run count; strong interaction risk; confirmation essential. *Decision lens:* Accept only when interactions are plausibly negligible.
- **Resolution IV:** Main effects clear of two-factor interactions. Main effects alias with three-factor interactions; two-factor interactions alias in pairs; common screening compromise. *Decision lens:* Escalate ambiguous interaction pairs in a follow-up design.
- **Resolution V:** Main effects and two-factor interactions are separately estimable. Main effects alias with four-factor terms; two-factor interactions alias with three-factor terms; more runs. *Decision lens:* Choose when interactions matter to the decision.
- **One-quarter fractions:** Two generators select one fourth of runs. Two defining words plus their product; alias chains lengthen; resolution depends on generator choice; efficiency increases. *Decision lens:* Generator selection is part of design quality.
- **Foldover designs:** Break targeted aliases in a follow-up. Reverse selected factor signs; combine original and foldover; separate main effects from interactions; retain sequential learning. *Decision lens:* Plan foldover before consuming the entire budget.
- **Plackett-Burman screening:** Estimate many main effects economically. N runs screen up to N-1 factors; orthogonal main-effect columns; interactions are not independently estimable; good for factor reduction. *Decision lens:* Use results to design a factorial confirmation, not to optimise directly.
- **Screening metrics:** Select projects and factors using business evidence. Effect magnitude; signal-to-noise; cost per run; cycle time; safety and specification impact. *Decision lens:* A statistically active factor may still be operationally irrelevant.
- **Sequential experimentation:** Learn, narrow and augment. Screen; confirm; map curvature; optimise; verify at the recommended settings. *Decision lens:* Every phase needs a go/no-go criterion.
- **Design review and run sheet:** Make the experiment executable. Scope; owners; factor table; randomised run order; measurement plan; risks; stop rules. *Decision lens:* Freeze the run sheet before execution and log deviations.

### DOE Lab 06: Screen Five Factors with a Resolution V Half Fraction

**Alignment:** LO3  
**Method:** NovaDOE fractional factorial  
**Scenario:** A polymer extrusion team has five controllable factors but only 16 safe pilot runs.

**Goal:** Generate a defensible 2^(5-1) design, interpret aliases and plan confirmation.

**Expected output:** A 16-run fraction, generator/alias record, screened effects and confirmation plan.

#### Detailed procedure

1. **Select Fractional Factorial in NovaDOE.** Add five numeric factors with safe low/high limits.
2. **Choose a 16-run fraction and record the displayed resolution.** Target Resolution V where supported.
3. **Generate and export the design CSV.** Save the NovaDOE setup in browser storage as well.
4. **Import the mock response and code factor levels.** Lower defect rate is better.
5. **Calculate main-effect contrasts.** Rank absolute effects and retain signs.
6. **Write the generator and alias interpretation in the workbook.** If NovaDOE does not display aliases, document the assumed generator from the exported matrix.
7. **Select factors for a confirmation experiment.** Use magnitude, feasibility and engineering plausibility.
8. **Plan confirmation and possible foldover runs.** Define expected improvement and acceptance threshold.

#### Acceptance test

The design has 16 unique runs, five factor columns, a stated resolution/alias assumption and a confirmation plan that does not overclaim aliased effects.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 07: Screen Eleven Battery-Process Factors

**Alignment:** LO3  
**Method:** NovaDOE Plackett-Burman  
**Scenario:** A battery lab must screen eleven formulation and process factors in twelve runs.

**Goal:** Use a Plackett-Burman design to reduce a long factor list before modelling interactions.

**Expected output:** A 12-run PB matrix, main-effect ranking, risk register and factorial follow-up proposal.

#### Detailed procedure

1. **Select Plackett-Burman in NovaDOE.** Create eleven two-level numeric factors.
2. **Generate a 12-run design.** Confirm the summary reports 12 runs and 11 factors.
3. **Export the design and join mock capacity-retention results.** Keep factors in the same order.
4. **Calculate each main-effect contrast.** Use the high-level average minus low-level average.
5. **Create a ranked effect chart.** Show absolute magnitude and sign.
6. **Assess interaction contamination risk.** Use process knowledge to identify plausible two-factor interactions.
7. **Choose three or four factors for follow-up.** Balance evidence, controllability, safety and cost.
8. **Draft a full or fractional factorial confirmation.** Do not optimise from the PB model alone.

#### Acceptance test

All eleven main effects are ranked and the report explicitly states that interactions are not separately estimable in the screening design.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

## Topic 04: Screening, Modelling and Optimising DoE

Response surfaces, CCD, Box-Behnken, mixtures and Taguchi robustness

### Key concepts

- **Response Surface Methodology:** Model curvature after important factors are known. Fit first- and second-order terms; map a local region; find stationary behaviour; optimise with constraints. *Decision lens:* RSM is local—avoid extrapolation beyond the design space.
- **Quadratic models:** Curvature needs squared terms. Linear terms give slope; interaction terms twist the surface; squared terms create curvature; residuals test adequacy. *Decision lens:* Respect hierarchy when retaining higher-order terms.
- **Central Composite Design:** Augment factorial points with stars and centres. Factorial corners estimate interactions; axial points estimate curvature; centre points estimate pure error; alpha controls geometry. *Decision lens:* CCD supports efficient sequential augmentation.
- **CCD variants and alpha:** Choose geometry for feasibility and prediction. Circumscribed extends beyond factorial range; inscribed keeps axial points within bounds; face-centred uses alpha 1; rotatability stabilises variance. *Decision lens:* Safety limits may rule out circumscribed designs.
- **Box-Behnken design:** Estimate quadratic models without all-factor extremes. Mid-edge treatment combinations; centre points; at least three factors; fewer dangerous corner runs. *Decision lens:* Compare run count and feasible region with CCD.
- **Contour and surface plots:** Translate equations into operating windows. Contours show equal-response lines; surfaces show curvature; overlay multiple requirements; mark the data region. *Decision lens:* A persuasive plot still needs uncertainty and validation.
- **Optimisation and confirmation:** Turn a model into a controlled recommendation. Define target and bounds; optimise desirability; inspect sensitivity; run confirmation trials; compare predicted and observed. *Decision lens:* Do not release settings without confirmation.
- **Mixture designs:** Component proportions sum to one. Changing one component forces others to change; simplex geometry replaces a cube; blends drive the response; process variables can be added. *Decision lens:* Ordinary factorial independence does not apply to proportions.
- **Simplex centroid and extreme vertices:** Cover constrained formulation space. Vertices are pure blends; edges are binary blends; centroid is balanced blend; constraints reshape the feasible region. *Decision lens:* Document lower and upper component bounds.
- **Taguchi robust design:** Reduce sensitivity to uncontrollable noise. Separate control and noise factors; use orthogonal arrays; calculate signal-to-noise ratio; tune mean after stabilising variation. *Decision lens:* Robustness is performance across noise, not merely a high mean.
- **Signal-to-noise ratios:** Match the metric to the engineering goal. Smaller-the-better; larger-the-better; nominal-the-best; logarithmic ratio combines mean and variation. *Decision lens:* State the S/N convention before comparing settings.
- **Evaluate and recommend:** Close the experimental learning loop. Compare objective to achieved effect; check uncertainty and residuals; document limitations; assign actions; monitor control metrics. *Decision lens:* Recommendation strength must match evidence strength.
- **Follow-up action portfolio:** Choose the next experiment intentionally. Confirm promising settings; fold over aliases; augment for curvature; widen or narrow ranges; improve measurement system. *Decision lens:* Capture decision, owner, due date and acceptance test.

### DOE Lab 08: Design a Robust Golf-Ball Process with Taguchi Logic

**Alignment:** LO4  
**Method:** NovaDOE full/fractional matrix used as an orthogonal-array proxy  
**Scenario:** A golf-equipment team tests four two-level control factors under Driver and 5-Iron noise conditions.

**Goal:** Separate control and noise factors and recommend robust rather than merely high-mean settings.

**Expected output:** An orthogonal eight-run control matrix, two noise responses, S/N analysis and robustness recommendation.

#### Detailed procedure

1. **Generate an eight-run balanced two-level matrix in NovaDOE.** Use Fractional Factorial for four control factors.
2. **Export CSV and verify level balance.** Each level should occur equally often per factor.
3. **Join Driver and 5-Iron distance responses.** Treat club as a planned noise condition.
4. **Calculate run mean and standard deviation.** Use formulas and consistent units.
5. **Calculate larger-the-better S/N ratio.** Use -10*LOG10(AVERAGE(1/y²)).
6. **Create factor-response tables for mean and S/N.** Rank delta across levels.
7. **Choose settings that maximise S/N, then tune mean.** Explain any trade-off.
8. **Propose a confirmation trial across both noise conditions.** Set robustness acceptance criteria.

#### Acceptance test

The recommended settings are justified by S/N ratio and mean response, with a confirmation plan across both club conditions.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 09: Optimise Sterile-Package Seal Strength with CCD

**Alignment:** LO4  
**Method:** NovaDOE Central Composite  
**Scenario:** A medical-packaging engineer targets seal strength of 26 N within an acceptable 20–32 N range.

**Goal:** Generate a CCD, fit a quadratic response surface and identify a feasible operating window.

**Expected output:** A CCD export, quadratic model table, contour evidence, optimum and confirmation record.

#### Detailed procedure

1. **Select Central Composite in NovaDOE.** Add three numeric factors with low/high bounds.
2. **Choose face-centred or circumscribed geometry based on safe limits.** Record the chosen CCD type and centre points.
3. **Generate and export the design.** Verify factorial, axial and centre runs are present.
4. **Join mock seal-strength responses.** Flag values outside 20–32 N without deleting them.
5. **Create linear, interaction and squared columns.** Use coded factor levels.
6. **Fit the quadratic model with Excel Regression or LINEST.** Retain hierarchy and inspect residuals.
7. **Create contour-ready prediction grids.** Keep predictions within the experimental region.
8. **Select settings closest to 26 N with low sensitivity.** Balance target achievement and robustness.
9. **Define and evaluate confirmation trials.** Compare observed with predicted interval.

#### Acceptance test

The design includes factorial, axial and centre points; the recommendation targets 26 N and includes confirmation evidence.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

### DOE Lab 10: Optimise a Three-Component Thermal Paste Mixture

**Alignment:** LO4  
**Method:** NovaDOE Latin Hypercube for candidate exploration + simplex filtering  
**Scenario:** A thermal-materials lab blends ceramic filler, binder and additive; proportions must total 100%.

**Goal:** Recognise the mixture constraint, map a simplex design and recommend a constrained follow-up.

**Expected output:** A constrained candidate set, simplex plot table, blend model evidence and validation plan.

#### Detailed procedure

1. **Select Latin Hypercube in NovaDOE.** Generate at least 40 candidate points for three numeric proportions.
2. **Export the candidate design.** Treat the values as proportions, not independent production settings.
3. **Normalise each row so the three components sum to 1.** Use formulas and show the original values.
4. **Filter candidates against component bounds.** Retain the feasibility flag.
5. **Select a balanced subset spanning vertices, edges and centre-like blends.** Document the selection rule.
6. **Join the mock response data for the selected blends.** Do not extrapolate to discarded infeasible candidates.
7. **Fit a simple mixture model and compare predictions.** Avoid an intercept if using canonical mixture terms.
8. **Recommend a blend and follow-up extreme-vertices experiment.** State composition tolerance and validation tests.
9. **Review the full portfolio of ten labs.** Link the outcome to an evaluation of effectiveness and follow-up actions.

#### Acceptance test

Every retained blend sums to 1.000 within tolerance, satisfies bounds and leads to a constrained follow-up recommendation.

#### Evidence to retain

- NovaDOE setup screenshot and exported `learner-design.csv`.
- Completed `DOE-Lab-Workbook.xlsx` with formulas and interpretation.
- A recommendation, limitation and follow-up action.

## Troubleshooting

- **NovaDOE design differs:** Check method, factor type, low/high order, run count and saved setup.
- **CSV joins incorrectly:** Join by StandardOrder; preserve RunOrder as execution evidence.
- **Excel formula error:** Check ranges, numeric types and blank denominators before continuing.
- **Effect direction reverses:** Confirm the high-minus-low sign convention and level coding.
- **Model overfits:** Reduce terms using hierarchy, residual evidence and engineering plausibility.
- **Mixture total is not 1:** Normalise proportions and then re-check component bounds.
