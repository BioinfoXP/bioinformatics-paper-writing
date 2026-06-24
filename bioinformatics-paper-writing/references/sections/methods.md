# Method Writing Guide

## Goal

Write Methods so reviewers can reconstruct:

1. where samples came from,
2. how data were generated or collected,
3. how each computational analysis was performed,
4. how models were trained and validated,
5. how statistics were handled.

When the user provides code or notebooks, pair this file with `references/by-input/methods-from-code.md`.

## Recommended Method Sections

Use these blocks as needed:

1. Cohorts, specimens, and ethics.
2. Data generation or data sources.
3. Preprocessing and quality control.
4. Cell annotation, deconvolution, or feature derivation.
5. Interaction, pathway, spatial, or risk-model analyses.
6. Validation datasets or orthogonal assays.
7. Statistical analysis.

## Section Writing Rules

1. Open each subsection with what was analyzed and why.
2. Then describe the exact pipeline in execution order.
3. End with key thresholds, software, or statistical settings.
4. Keep biological labels and computational labels consistent.

## Cohort and Assay Clarity

Always specify:

1. sample source,
2. specimen type,
3. cohort size,
4. inclusion or exclusion logic,
5. sequencing or staining platform,
6. validation resource.

## Computational Analysis Pattern

For each major analysis block:

1. Input data.
2. Filtering and normalization.
3. Feature extraction or model-building.
4. Comparison groups or endpoint.
5. Output used in Results.

If code is available, recover these steps from the implementation before writing prose.

## Model and Signature Writing Rule

When the paper contains a risk score, classifier, signature, or biomarker panel:

1. Describe feature selection.
2. Describe training strategy.
3. Describe cutoff definition.
4. Describe internal and external validation separately.
5. Describe evaluation metrics and endpoints explicitly.

## Weak Methods Writing to Avoid

1. Hiding cohort definitions in supplementary material when they are central to the story.
2. Listing software packages without explaining analytical logic.
3. Describing validation as if it were discovery.
4. Mixing preprocessing with biological interpretation.

## Checklist

1. Can a reviewer reconstruct sample flow from cohort to output?
2. Are discovery and validation analyses clearly separated?
3. Are model-building and cutoff rules explicit?
4. Are statistics tied to concrete comparisons?
