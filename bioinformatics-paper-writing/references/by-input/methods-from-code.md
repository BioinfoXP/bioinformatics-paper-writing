# Methods from Code Guide

## Goal

Write Methods from actual code, notebooks, or pipelines rather than from memory or wishful summaries.
Default output should be bilingual Chinese-English, with the English version written in Nature style unless the user explicitly requests otherwise.

## When to Use

Use this file when the user provides:

1. R scripts,
2. Python scripts,
3. Jupyter notebooks,
4. Snakemake or Nextflow workflows,
5. shell pipelines,
6. analysis directories with source files.

## Core Rule

Describe what the code actually does.
If a step is missing, ambiguous, or only implied, mark it as uncertain instead of inventing a clean workflow.

## Recovery Workflow

1. Identify entry scripts or notebooks.
2. Recover the pipeline in execution order:
   - inputs,
   - quality control,
   - filtering,
   - normalization,
   - transformation,
   - integration,
   - model-building,
   - statistical testing,
   - plotting or export.
3. Record concrete parameters that matter scientifically.
4. Separate reusable implementation detail from manuscript-level Methods prose.

## What to Extract from Code

1. Data sources and file types.
2. Sample inclusion logic.
3. Preprocessing thresholds.
4. Packages, models, and key functions.
5. Group definitions and comparison logic.
6. Statistical tests and multiple-testing corrections.
7. Risk-score or model formulas.
8. Output artifacts used in figures or tables.

## Manuscript Conversion Rule

Translate code into Methods with this order:

1. What data were analyzed.
2. How data were preprocessed.
3. How features or cell states were defined.
4. How associations or models were tested.
5. How outputs were validated and visualized.

Do not dump raw function names unless they are scientifically important.

## Ambiguity Rule

If the code leaves an important detail unclear, report it in one of two ways:

1. `explicit in code`: directly observed.
2. `inferred from context`: likely but not fully explicit.

## Weak Patterns to Avoid

1. Writing a polished Methods section that ignores what the code actually implements.
2. Hiding missing preprocessing or threshold choices.
3. Mixing plotting code details with core analytical logic.
4. Confusing exploratory scripts with the final reproducible pipeline.

## Output Checklist

1. Did I recover the true analysis order?
2. Did I distinguish explicit code behavior from inference?
3. Did I preserve reproducible thresholds and tests?
4. Did I convert implementation into manuscript-ready prose without losing scientific accuracy?
5. Did I provide both Chinese and English Methods text by default?
