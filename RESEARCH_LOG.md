# Research Log

A chronological record of decisions, observations, failures, and changes in the study. The log is intentionally kept close to the reasoning rather than only preserving polished final results.

## 2026-09-16 — Repository initialized

**Question:**
How does patient-level dependence change the estimated performance and error profile of conventional machine-learning models on repeated biomedical observations?

**Hypothesis:**
Because the dataset contains repeated observations from the same patients, random observation-level train/test splits may produce more optimistic performance estimates than patient-grouped evaluation. The study will test this rather than assume it is true.

**Data version/source:**
UCI Parkinsons Telemonitoring dataset; official UCI source. Dataset files have not yet been downloaded into the repository. Provenance is recorded separately under `data/provenance/`.

**Method / setup:**
Locked the primary research question, selected the initial dataset, and created the repository structure before beginning the analysis. The planned comparison is between conventional observation-level evaluation and patient-grouped evaluation using simple, auditable models.

**Result / observation:**
No analytical result yet.

**Failure / uncertainty:**
The study has not yet reached data inspection or model fitting. The actual dataset version/file and evaluation results still need to be recorded.

**Interpretation:**
The study is at the setup stage. No performance claim or conclusion is justified yet.

**Next decision:**
Download and record the dataset, verify the Python environment, inspect the repeated-patient structure, and begin the first notebook.

## Working rules

- Record important methodological changes rather than silently replacing earlier choices.
- Keep provenance separate from interpretation.
- Prefer simple models and explicit evaluation over unnecessary complexity.
- Treat patient grouping as a methodological issue to test, not as a predetermined conclusion.
- Do not turn exploratory findings into clinical claims.
- Do not report a final conclusion before the planned evaluation and error analysis are complete.

## Log template

### YYYY-MM-DD — Short decision title

**Question:** What were you trying to understand?

**Hypothesis:** What did you expect, and why?

**Data version/source:** What data/code version did you use?

**Method:** What did you actually do?

**Result / observation:** What did you observe?

**Failure / uncertainty:** What went wrong or remains unclear?

**Interpretation:** What does the observation support, and what does it not support?

**Next decision:** What changes because of this?
