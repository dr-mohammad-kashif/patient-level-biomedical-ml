# Research Question

## Primary question

**How does patient-level dependence change the estimated performance and error profile of conventional machine-learning models on repeated biomedical observations?**

## Why this question

The dataset contains repeated observations from the same patients. A row-level split treats observations as independent examples, but observations from one patient can be related to one another.

The study therefore compares evaluation strategies that differ in whether the same patient can appear in both training and test data.

## What I want to learn

- How much estimated performance changes when patient identity is respected during evaluation.
- Whether error patterns change alongside the headline metrics.
- Which conclusions remain stable under reasonable sensitivity checks.
- Which limitations matter enough to prevent a stronger interpretation.

## Boundary

This is a methodological study using a public biomedical dataset. It is not a clinical validation study and does not establish clinical usefulness or broad generalization.
