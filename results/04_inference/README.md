# Reaction-time inference results

## Methods

The independent unit was the mouse. Trial RTs were summarized by the median within each session, contrast, and congruency condition; paired session differences were averaged within mouse. For each contrast, the median mouse-level incongruent-minus-congruent difference received a 95% percentile bootstrap confidence interval from 20,000 whole-mouse resamples (seed 2026). Directional consistency was tested with a two-sided exact sign test, with Holm correction across the three co-primary contrasts. These procedures were specified after descriptive inspection and were not preregistered.

## Primary all-choice results

- **0% contrast:** median I−C +20.1 ms (95% mouse-bootstrap CI +12.3 to +26.1 ms; 95/139 positive mice; two-sided exact sign test Holm-adjusted p=1.82e-05); statistically significant.
- **6.25% contrast:** median I−C +18.7 ms (95% mouse-bootstrap CI +12.1 to +23.1 ms; 103/139 positive mice; two-sided exact sign test Holm-adjusted p=2.27e-08); statistically significant.
- **12.5% contrast:** median I−C +14.0 ms (95% mouse-bootstrap CI +10.8 to +19.5 ms; 111/139 positive mice; two-sided exact sign test Holm-adjusted p=2.04e-12); statistically significant.

## Correct-only sensitivity

- **0% contrast:** median I−C +46.5 ms (95% mouse-bootstrap CI +34.2 to +73.1 ms; 100/132 positive mice; two-sided exact sign test Holm-adjusted p=4.86e-09); statistically significant.
- **6.25% contrast:** median I−C +21.5 ms (95% mouse-bootstrap CI +13.0 to +30.5 ms; 102/139 positive mice; two-sided exact sign test Holm-adjusted p=3.22e-08); statistically significant.
- **12.5% contrast:** median I−C +13.5 ms (95% mouse-bootstrap CI +8.7 to +18.7 ms; 107/139 positive mice; two-sided exact sign test Holm-adjusted p=3.62e-10); statistically significant.

At 0%, seven mice were excluded because none of their sessions contained both correct congruent and correct incongruent trials. This sensitivity analysis changes the estimand and does not replace the primary all-choice result.

## Contrast dependence

The repeated-measures Friedman test did not detect a contrast-dependent difference (χ²=1.68, p=0.431); the abstract must not claim that the effect changes with contrast.

See `contrast_effect_tests.csv` for the omnibus and Holm-adjusted paired comparisons.

## Abstract-ready interpretation

Across 139 mice, choices opposing the current block prior were associated with slower movement initiation at 0%, 6.25%, and 12.5% visual contrast. Report the contrast-specific median effects, 95% CIs, and Holm-adjusted p-values above. The result is associative rather than causal, and the correct-only analysis is a secondary sensitivity analysis.

## Reporting limitations

- The analysis was specified after the descriptive results were inspected and was not preregistered.
- Correctness differs between congruency groups; the correct-only sensitivity changes the target population and has reduced 0% coverage.
- Trial counts are unequal, sessions receive equal weight within mouse, and mice receive equal cohort weight.
- No trial-level mixed-effects model is included in this robust-core analysis.
