# Figures and Legends Guide

## Goal

Use figures to carry the scientific argument. In bioinformatics papers, figures are often the fastest way reviewers judge whether the story is coherent.

When the figure itself is the primary user input, pair this file with `references/by-input/results-from-figures.md`.

## Typical Figure Order

1. Study design and cohort overview.
2. Main discovery figure.
3. Cellular, pathway, or interaction decomposition.
4. Orthogonal validation or spatial confirmation.
5. Clinical association, survival, or model performance.
6. Mechanistic or translational summary.

## Panel Logic

Within one figure, prefer this sequence:

1. orient the reader,
2. show the main pattern,
3. zoom into interpretation,
4. end with validation or impact.

Do not mix unrelated analyses into one crowded figure.

## Figure Legend Pattern

For each figure legend:

1. Default to a concise, manuscript-ready Nature-style legend unless the user asks for a longer explanatory version.
2. Start with `Figure X.` followed by one sentence stating the figure's scientific message.
3. Insert one blank line after the opening sentence.
4. Walk panel-by-panel in order.
5. Write each panel on its own line using `(A)`, `(B)`, `(C)` and so on.
6. End every panel sentence with a period.
7. End with abbreviations only if necessary.

## Nature-Style Legend Default

Use these defaults unless the user requests otherwise:

1. Keep the legend compact and submission-ready rather than tutorial in tone.
2. Prefer one short opening sentence plus one full sentence per panel.
3. Describe what each panel shows without re-explaining the full biological interpretation already covered in Results.
4. Mention statistics only when they are visibly shown or explicitly provided.
5. Include abbreviations only when needed for readability.
6. Use periods, not semicolons, between panel descriptions.
7. Preserve the line break pattern exactly:
   - opening sentence,
   - blank line,
   - one panel per line.

## Strict Legend Template

Use this template by default:

```text
Figure X. One-sentence message of the figure.

(A) Description of panel A.
(B) Description of panel B.
(C) Description of panel C.
```

Do not switch to `A, ...; B, ...; C, ...` formatting unless the user explicitly requests it.

When the user wants Results text, not just a legend:

1. Start from the scientific message, not from panel lettering.
2. Convert panel order into logical result order when needed.
3. Separate direct visual observation from downstream interpretation.

## Visualization Writing Rule

1. Do not let words like `UMAP`, `heatmap`, or `Kaplan-Meier curve` substitute for a biological conclusion.
2. Translate each visualization into a biological statement.

## Survival and Risk Model Figure Rule

When figures contain survival curves, ROC curves, calibration, or nomograms:

1. State the cohort and endpoint.
2. Name the split rule or model source.
3. Clarify whether the panel is discovery, internal validation, or external validation.
4. Avoid implying clinical readiness unless validation is strong.
