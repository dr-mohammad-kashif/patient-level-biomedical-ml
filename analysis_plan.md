# Analysis Plan

**Status:** Initial plan — September 2026

This plan is a starting point. If the data or diagnostics require a change, the change should be recorded in `RESEARCH_LOG.md` with the reason.

## 1. Data provenance

- Obtain the dataset from the UCI Machine Learning Repository.
- Record the dataset name, source, DOI, download date, and file identity.
- Do not commit the source dataset to this repository.

## 2. Data understanding

- Confirm the unit of observation.
- Identify the patient identifier and repeated observations.
- Inspect missingness, distributions, ranges, and duplicated records.
- Examine relationships among predictors and the target variables.

## 3. Preprocessing

- Keep preprocessing reproducible and explicit.
- Avoid fitting transformations on the test data.
- Record exclusions and transformations.
- Keep patient identifiers available for grouped evaluation but out of model features.

## 4. Evaluation comparison

At minimum, compare:

1. **Observation-level split:** individual observations are assigned to train/test sets.
2. **Patient-grouped split:** all observations belonging to a patient remain in one partition.

The exact split implementation and random seeds will be recorded in the analysis code.

## 5. Models

Use conventional, interpretable baselines before adding more complex models. Candidate models include:

- mean predictor baseline
- linear regression
- ridge regression
- random forest regression, if justified after initial analysis

The final model set will be determined after inspecting the data and will not be selected solely because it produces a better metric.

## 6. Metrics

Primary regression metrics:

- MAE
- RMSE
- R²

Metrics will be interpreted together with error distributions and patient-level behaviour rather than in isolation.

## 7. Leakage checks

Before interpreting results, check:

- patient overlap between train and test sets
- preprocessing fit boundaries
- identifier leakage
- target-derived variables
- duplicated or near-duplicated observations
- any other feature that could encode information unavailable at prediction time

## 8. Error analysis

Inspect:

- residual distributions
- large-error observations
- performance by patient where appropriate
- whether conclusions are driven by a small number of patients

## 9. Sensitivity / robustness

At least one sensitivity analysis will be performed, such as changing the random split seed or comparing another defensible grouping/evaluation choice. The exact analysis will depend on what the dataset structure supports.

## 10. Interpretation

The conclusion will answer the research question narrowly. It will distinguish:

- what the experiment directly demonstrates;
- what is plausible but uncertain;
- what the dataset cannot establish.
