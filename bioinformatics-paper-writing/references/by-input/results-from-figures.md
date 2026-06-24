# Results from Figures Guide

## Goal

Write Results from concrete result figures without hallucinating labels, statistics, or conclusions that are not visually supported.
Default output should be bilingual Chinese-English, with the English version written in Nature style unless the user explicitly requests otherwise.

## When to Use

Use this file when the user gives:

1. multi-panel result figures,
2. heatmaps,
3. volcano plots,
4. UMAP or t-SNE plots,
5. Kaplan-Meier curves,
6. boxplots or violin plots,
7. spatial transcriptomics maps,
8. immunofluorescence, pathology, or microscopy images.

## Workflow

1. Identify the figure type and likely scientific question.
2. Read panel labels, axes, legends, group names, and color keys if visible.
3. Write down only what is directly observable first.
4. Infer biological meaning second, and mark uncertainty when labels or statistics are missing.
5. Reorder the narrative into scientific logic if the panel layout is not the best reading order.

## Observation Template

For each panel:

1. What entity is shown:
   - cells,
   - genes,
   - pathways,
   - survival groups,
   - tissue regions,
   - samples.
2. What groups are compared.
3. What direction is visible:
   - higher,
   - lower,
   - enriched,
   - separated,
   - clustered,
   - co-localized.
4. What statistical annotation is visible, if any.

## Writing Rule

Convert visual signal into prose in two layers:

1. Visible observation:
   - `High-risk tumors showed higher expression of ...`
   - `CD8-positive cells were localized closer to ...`
   - `The survival curve for ... remained below ...`
2. Biological interpretation:
   - `These findings suggest ...`
   - `This pattern is consistent with ...`

Never collapse these two layers into one unsupported sentence.

## Figure-Type Notes

### Heatmap

1. Focus on relative pattern, group contrast, and gene program.
2. Do not describe every gene unless necessary.

### UMAP or t-SNE

1. Describe separation, overlap, and annotated populations.
2. Do not overstate trajectory or lineage unless explicitly supported.

### Kaplan-Meier curve

1. Name the endpoint and risk groups.
2. Describe direction and separation.
3. Do not claim clinical utility from one curve alone.

### Spatial or pathology image

1. Describe region localization, co-localization, exclusion, enrichment, and boundary effects.
2. Separate morphology from molecular interpretation.

## Output Checklist

1. Did I separate visible observation from interpretation?
2. Did I avoid inventing missing statistics?
3. Did I preserve panel order only when it matches scientific logic?
4. Did I write the local conclusion in reviewer-friendly prose?
5. Did I provide both Chinese and English Results text by default?
