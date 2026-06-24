---
name: bioinformatics-paper-writing
description: Use when drafting or revising bioinformatics, multi-omics, spatial transcriptomics, tumor microenvironment, biomarker, survival-modeling, or translational cancer manuscripts; writing Results from figures or writing Methods from code; learning reusable writing patterns from user-provided papers; or producing bilingual Chinese-English Nature-style prose unless another language or journal style is explicitly requested.
---
# Bioinformatics Paper Writing

## Overview

Use this skill to write or revise bioinformatics papers at a high review standard.
Prioritize biological story coherence, cohort and assay transparency, validation depth, cautious causal language, and clinically meaningful interpretation.
Default writing mode is fixed to bilingual Chinese-English output with Nature-style scientific prose unless the user explicitly overrides it.

This skill can also learn from user-provided literature and persist reusable writing knowledge without rewriting the skill itself.

## Default Output Mode

Default output mode is `manuscript mode`.

In manuscript mode, the skill should write like a submission-ready Nature-family draft rather than a working note.

Use these defaults unless the user explicitly asks for analysis support:

1. Output polished manuscript text first.
2. Use conclusion-like subsection titles instead of tool-style labels.
3. Write continuous paragraphs instead of note-style fragments.
4. Avoid inline process tags such as `discovery`, `validation`, `mechanism`, `implication`, or `limitation` inside the prose.
5. Suppress scaffolding such as panel notes, claim-evidence tables, self-review checklists, and visible-versus-interpretation splits unless the user asks for them.
6. For figure-driven tasks, default to `Results paragraph(s) + concise Nature-style legend`.
7. Apply `strict legend mode` unless the user explicitly requests another legend format.

If the user asks for review support, traceability, or teaching output, switch to `analysis mode` and add the necessary scaffolding after the manuscript text.

## Supported Entry Scenarios

This skill must handle at least these three entry modes:

1. Text-first writing:
   - the user provides an outline, draft, bullet points, or reviewer comments.
2. Figure-first Results writing:
   - the user provides result figures, panel images, heatmaps, volcano plots, Kaplan-Meier curves, boxplots, UMAPs, spatial transcriptomics maps, pathology images, or composite multi-panel figures.
3. Code-first Methods writing:
   - the user provides R scripts, Python scripts, notebooks, workflow files, shell pipelines, or analysis directories and wants Methods written from the actual implementation.
4. Literature-learning mode:
   - the user provides a PDF, DOI, abstract, full text, figure legends, supplementary notes, or pasted paper content and wants the skill to learn reusable writing patterns for future tasks.

## Core Workflow

1. Clarify the central biological or clinical question before sentence-level edits.
2. Build the evidence ladder:
   - discovery cohort,
   - decomposition or mechanism analysis,
   - orthogonal validation,
   - external validation or functional support,
   - translational implication.
3. Load only the section guide needed for the current edit target.
4. Rewrite paragraph-by-paragraph with one message per paragraph and one scientific purpose per paragraph cluster.
5. Check every major claim against explicit evidence from cohorts, assays, models, or experiments.
6. Run a self-correction loop before finalizing:
   - author view: is the story clear,
   - skeptical reviewer view: is the claim overstated,
   - statistician view: is the comparison and validation adequate,
   - translational view: is the clinical implication proportional to evidence.

## Literature Learning Mode

When the user asks the skill to learn from a paper, build reusable local knowledge instead of editing the skill itself.

1. Read only the material needed for the learning goal:
   - PDF,
   - DOI landing content,
   - abstract,
   - main text,
   - figure legends,
   - supplementary methods,
   - notes provided by the user.
2. Extract structured signals:
   - study question,
   - disease context,
   - cohort design,
   - modality stack,
   - Results ladder,
   - evidence language,
   - Methods phrasing,
   - Discussion framing,
   - figure legend patterns,
   - reviewer-risk points.
3. Save the learned content as a structured note under `knowledge/paper-notes/`.
4. Update a cross-paper synthesis under `knowledge/syntheses/` only when at least one stable pattern appears across multiple papers.
5. Reuse saved knowledge in future tasks by loading only the smallest relevant note or synthesis.

## Self-Evolution Boundaries

This skill supports persistent learning, but only within strict boundaries.

Allowed:

1. Learn writing structures, evidence phrasing, section logic, figure legend style, Methods reproducibility patterns, and reviewer-facing caution from user-provided literature.
2. Save those patterns to the local knowledge base for reuse in later sessions.
3. Record conflicts between new papers and existing knowledge for later review.

Not allowed:

1. Do not automatically rewrite `SKILL.md`.
2. Do not silently overwrite earlier knowledge notes.
3. Do not treat one paper as a universal rule.
4. Do not turn biological conclusions from a single study into general writing guidance without marking the scope.

When a new paper conflicts with existing knowledge, return:

1. `conflict point`
2. `older note`
3. `new paper`
4. `recommended manual decision`

## Scenario-Specific Workflow

### A. When the user provides result figures

1. Inspect the image carefully before writing prose.
2. Identify figure type, comparison groups, panel order, signal direction, and likely statistical message.
3. Separate observation from interpretation:
   - observation: what the figure visibly shows,
   - interpretation: what the figure may mean biologically.
4. Draft Results in panel order only if panel order matches the scientific logic; otherwise rewrite into scientific order.
5. Mark uncertain elements explicitly instead of inventing labels or statistics.
6. Anchor each major statement to the relevant figure panels using figure references such as `Fig. 6A`, `Fig. 6B, C`, or `Fig. 6A-J` when the support spans multiple panels.
7. Use `references/by-input/results-from-figures.md` and `references/sections/figure-legends.md`.

### B. When the user provides code or notebooks

1. Read the codebase before drafting Methods.
2. Recover the actual analysis flow:
   - inputs,
   - preprocessing,
   - filtering,
   - normalization,
   - model-building or statistical testing,
   - outputs.
3. Distinguish what the code truly does from what the authors may wish it did.
4. Convert implementation details into Methods prose while preserving reproducibility.
5. Surface ambiguities or missing steps rather than fabricating them.
6. Use `references/by-input/methods-from-code.md` and `references/sections/methods.md`.

### C. When the user provides literature to learn from

1. Identify whether the goal is:
   - style transfer,
   - paper decomposition,
   - section learning,
   - figure legend learning,
   - Methods phrasing learning,
   - reviewer-risk learning.
2. Extract stable writing patterns instead of copying paper-specific claims.
3. Separate:
   - transferable writing pattern,
   - domain-specific scientific finding,
   - uncertain or non-generalizable preference.
4. Save the structured note to `knowledge/paper-notes/`.
5. Use `references/by-input/learning-from-literature.md`.

## Global Principles

1. Keep one paragraph for one message only.
2. State the paragraph message in the first sentence.
3. Make nouns self-contained; define signatures, cell states, risk groups, and cohorts before reuse.
4. Maintain sentence-to-sentence flow through cause, contrast, consequence, refinement, or validation.
5. Make every major claim traceable to a concrete evidence source.
6. Separate discovery from validation in both structure and wording.
7. Move from observation to mechanism to implication; do not jump directly from signal to promise.
8. Use cautious verbs for observational evidence:
   - `was associated with`,
   - `was enriched in`,
   - `correlated with`,
   - `suggests`.
9. Reserve strong verbs such as `drives`, `promotes`, or `determines` for evidence with real mechanistic support.
10. Default to bilingual Chinese-English delivery:
   - Chinese version first for fast understanding,
   - English version second for manuscript use.
11. Default to Nature-style prose:
   - concise,
   - high information density,
   - claim-first paragraphs,
   - restrained hype,
   - explicit biological implication.
12. Default to Nature-style formatting:
   - conclusion-like subsection titles,
   - paragraph-based body text,
   - minimal list usage in final manuscript output,
   - no visible drafting labels inside the prose,
   - no unnecessary line breaks between closely linked sentences.
13. When the user asks for a figure legend, default to a concise, manuscript-ready Nature-style legend unless the user explicitly asks for an expanded or explanatory version.
14. When the user asks the skill to learn from literature, persist reusable patterns to the local knowledge base and make the saved path visible in the response.
15. In figure-driven Results writing, include explicit figure anchors in the prose so each major claim is tied to its supporting panel or panel group.

## Strict Legend Mode

When writing figure legends, use a fixed output format unless the user explicitly requests another style.

Required structure:

1. Start with `Figure X.` followed by one short sentence stating the figure's main message.
2. Insert one blank line after the opening sentence.
3. Write each panel on its own new line using parenthesized capitals:
   - `(A) ... .`
   - `(B) ... .`
   - `(C) ... .`
4. Use full sentences for each panel.
5. End each panel with a period, not a semicolon.
6. Do not merge multiple panels into a single run-on sentence.
7. Keep line breaks stable:
   - one panel per line,
   - no wrapped bullet formatting,
   - no paragraph-style legend blocks when panelized legends are appropriate.

Content rules:

1. Describe what the panel shows, not the full downstream interpretation already covered in Results.
2. Mention cohort, assay, model, comparison group, and quantification only when needed for clarity.
3. Mention statistics only when visibly shown in the figure or explicitly provided by the user.
4. Put scale bars at the end of the relevant panel sentence, for example `Scale bar, 100 μm.`
5. Put abbreviation definitions only at the end of the legend and only when necessary.
6. Keep the opening sentence compact and conclusion-like rather than descriptive of layout alone.

## Writing Patterns from the Source Papers

The source papers share a stable high-level pattern:

1. Open with an unmet biological or clinical need, not with software or algorithm details.
2. Introduce the modality stack early and justify why each modality is needed.
3. Build Results as a ladder:
   - cohort and workflow overview,
   - discovery of a major spatial, immune, molecular, or prognostic pattern,
   - decomposition into cell states, ligand-receptor programs, or genomic drivers,
   - orthogonal validation with a second modality, pathology, or independent dataset,
   - clinical or therapeutic implication.
4. Use declarative Results subsection titles that already state the finding.
5. Write Discussion as synthesis:
   - what was discovered,
   - why combined modalities matter,
   - what the translational meaning is,
   - what remains uncertain.

## Result Paragraph Pattern

Use this structure for most Results paragraphs:

1. State the local scientific question.
2. Name the cohort, modality, or assay used to answer it.
3. Report the key result with direction, contrast group, and important statistic when available.
4. Cite the supporting panel or panel group directly in the sentence, for example `Fig. 6A` or `Fig. 6B-D`.
5. Interpret the meaning of the result.
6. Bridge to the next question.

Avoid these failure modes:

1. Writing Results as a methods log.
2. Reporting p-values without effect direction or biological meaning.
3. Mixing discovery, validation, and interpretation in one overloaded paragraph.
4. Claiming mechanism from correlation alone.
5. Writing figure-based Results without explicit figure anchors.

## Paragraph Clarity Check

Use this quick test whenever the user asks whether a paragraph flows or is clear.

1. Read as an external reader:
   - Does this paragraph have one explicit message?
   - Does the first sentence state what this paragraph will do?
   - Are all key nouns readable without hidden context?
   - Does each sentence connect to the previous one with a clear relation?
2. Run reverse outlining for the current section:
   - thesis or local conclusion,
   - paragraph topic sentence,
   - evidence points under that paragraph,
   - mapping from evidence to paragraph claim and from paragraph claim to section claim.
3. If flow is still weak, add temporary transition phrases during revision, then remove unnecessary scaffolding.

Source reference for this check:

- `references/quality/writing-flow.md`

## Reference Map

Load only the smallest relevant reference set for the current task.

### 1. Core framing

- Study design and modality logic: `references/core/study-design.md`
- Bioinformatics story patterns: `references/core/story-patterns.md`

### 2. Entry-mode references

- Results from figures: `references/by-input/results-from-figures.md`
- Methods from code: `references/by-input/methods-from-code.md`
- Learning from literature: `references/by-input/learning-from-literature.md`

### 3. Section-specific guides

- Abstract: `references/sections/abstract.md`
- Introduction: `references/sections/introduction.md`
- Related Work: `references/sections/related-work.md`
- Results: `references/sections/results.md`
- Methods: `references/sections/methods.md`
- Figure legends: `references/sections/figure-legends.md`
- Discussion: `references/sections/discussion.md`
- Conclusion: `references/sections/conclusion.md`

### 4. Quality control and revision

- Validation and supplementary analyses: `references/quality/validation.md`
- Writing flow and paragraph coherence: `references/quality/writing-flow.md`
- Reviewer-style paper audit: `references/quality/paper-review.md`

## Loading Routes

Use these defaults to avoid overloading context:

1. Text-first section drafting:
   - load one section guide from `references/sections/`
   - add `references/core/study-design.md` if cohort or modality logic is central
   - add `references/core/story-patterns.md` if the paper lacks a coherent ladder
2. Figure-first Results writing:
   - load `references/by-input/results-from-figures.md`
   - add `references/sections/results.md`
   - add `references/sections/figure-legends.md` only if the user also wants a legend
3. Code-first Methods writing:
   - load `references/by-input/methods-from-code.md`
   - add `references/sections/methods.md`
4. Revision or reviewer-prep:
   - load `references/quality/paper-review.md`
   - add `references/quality/validation.md` for robustness gaps
   - add `references/quality/writing-flow.md` for clarity-only revisions
5. Literature-learning mode:
   - load `references/by-input/learning-from-literature.md`
   - add one section guide from `references/sections/` only if the user wants section-specific learning
   - add one relevant synthesis or paper note from `knowledge/` only if it directly matches the current task

## Knowledge Base

Persistent learning lives under `knowledge/`.

- `knowledge/README.md`: storage rules and note format
- `knowledge/paper-notes/`: one structured note per learned paper
- `knowledge/syntheses/`: cross-paper summaries of stable writing patterns

Use these rules:

1. Load the minimum number of knowledge files needed.
2. Prefer a synthesis note when the task asks for a broad style.
3. Prefer a paper note when the task points to a specific learned paper.
4. If no saved knowledge is relevant, continue with the core references and state that no matching learned note was used.

## High-Standard Revision Loop

Before finalizing any major section, ask and answer these questions:

1. Biological question:
   - Is the paper answering one memorable question, or only listing analyses?
2. Evidence hierarchy:
   - Which claims are discovery only?
   - Which claims are orthogonally validated?
   - Which claims have functional or mechanistic support?
3. Statistical adequacy:
   - Are comparison groups explicit?
   - Are validation cohorts distinct?
   - Are effect sizes and directions stated?
4. Translational discipline:
   - Are biomarker or therapeutic claims stronger than the data justify?
5. Reviewer simulation:
   - What is the strongest plausible objection, and is it already addressed in text?

## Execution Rules

1. Build a mini-outline before drafting prose.
2. For each subsection, explicitly state the scientific question, data source, key finding, and interpretation.
3. Avoid writing style that reads like a computational notebook export.
4. Distinguish clearly between discovery cohort, internal validation, external validation, and mechanistic support.
5. Keep terminology stable across the full paper.
6. If a claim cannot be supported by results, weaken or remove it.
7. Prefer conclusion-like Results subsection titles.
8. By default, produce both Chinese and English versions in one response unless the user explicitly requests single-language output.
9. The English version should default to Nature-style manuscript phrasing unless the user explicitly requests another venue style.
10. Do not load all section references at once; load only the guide needed for the current task.
11. In literature-learning mode, save reusable patterns to `knowledge/paper-notes/` before claiming the learning is complete.
12. When updating a synthesis, append or revise only the smallest necessary section and preserve prior note provenance.
13. In manuscript mode, present the final writing as clean manuscript copy first and move any optional analysis material after it.
14. Do not expose internal drafting roles, paragraph-function labels, or audit scaffolds unless the user explicitly asks for them.
15. When writing Results from figures, do not default to a panel-by-panel report; convert the figure into a logical scientific narrative and add a concise legend.
16. In strict legend mode, format legends with `Figure X.` plus one opening sentence, followed by one panel sentence per line using `(A)`, `(B)`, `(C)` and terminal periods.
17. In figure-driven Results text, explicitly anchor major claims to the supporting panels using `Fig. X` references.

## Output Contract

When asked to rewrite or draft sections, return:

In `manuscript mode`, return:

1. A conclusion-like subsection title when a title is needed.
2. A Chinese Nature-style manuscript version.
3. An English Nature-style manuscript version.
4. A concise Nature-style figure legend when the input is a figure or the user asks for one.
5. When a figure legend is produced, it must follow strict legend mode unless the user explicitly overrides it.
6. The visible section order should remain stable across similar tasks.
7. For figure-driven Results, both Chinese and English prose should contain explicit `Fig. X` anchors for major evidence statements.

In `analysis mode`, additionally return as needed:

1. A compact section outline with 3-7 bullets.
2. Revised paragraphs with explicit roles such as `problem`, `study design`, `discovery`, `validation`, `mechanism`, `implication`, or `limitation`.
3. A short self-review checklist covering clarity, cohort transparency, over-interpretation risk, and missing validation.
4. A claim-evidence map for each major claim using `Claim: ... | Evidence: ... | Status: supported/needs evidence`.
5. Analysis sections should appear after the manuscript text and use consistent labels.

When the input is a figure, additionally return:

In `manuscript mode`:

1. Chinese and English Results text by default.
2. A concise, manuscript-ready Nature-style legend by default.
3. The legend must use strict legend mode with one panel per line and terminal periods.

In `analysis mode`:

1. A panel-by-panel observation list.
2. A distinction between `visible observation` and `biological interpretation`.
3. Chinese and English Results text.
4. A concise, manuscript-ready Nature-style legend unless the user requests otherwise.

When the input is code, additionally return:

1. A recovered analysis pipeline summary.
2. A list of Method details that were explicit in code versus inferred from context.
3. Chinese and English Methods text by default.

When the input is literature for learning, additionally return:

1. A short paper profile with title, disease context, modality stack, and writing use case.
2. A transferable-pattern list split into:
   - story structure,
   - Results phrasing,
   - Methods phrasing,
   - Discussion framing,
   - figure legend style,
   - reviewer-risk notes.
3. A list of what was saved versus what was intentionally not generalized.
4. The saved local path under `knowledge/paper-notes/`.
5. If updated, the saved local path under `knowledge/syntheses/`.

## Formatting Guardrails

Use these formatting rules to keep outputs closer to Nature-family manuscript conventions:

1. Prefer sentence case or conclusion-like subsection titles; avoid report-style headers such as `Panel Notes`, `Self-Review`, `Claim-Evidence Map`, or `Section Outline` in manuscript mode.
2. Keep prose in full paragraphs, typically one idea per paragraph.
3. Avoid excessive bullet lists in manuscript mode unless the user explicitly asks for notes or outlines.
4. Avoid visible markup labels inside manuscript text, including `observation`, `interpretation`, `discovery`, `validation`, or similar tags.
5. Keep figure legends compact:
   - one opening sentence stating the figure message,
   - then one full sentence per panel on its own line.
6. Avoid unnecessary hard line breaks that make the text read like a checklist rather than a manuscript.
7. If bilingual output is requested, keep Chinese and English as two clean manuscript blocks rather than interleaving sentence by sentence.
8. In strict legend mode, line breaks are part of the format and should be preserved between the opening sentence and each panel sentence.
9. Use the same small set of visible section labels across outputs:
   - a subsection title,
   - `中文`,
   - `English`,
   - `Figure legend`,
   - optional analysis labels only in analysis mode.
10. Do not invent decorative headings, emoji, or presentation flourishes that are not manuscript-like.
11. Keep heading depth shallow; in most cases, one subsection title plus 2-3 short labels is sufficient.
12. In figure-driven Results, avoid floating claims without figure anchors; bind each major finding to `Fig. X`, `Fig. X, Y`, or `Fig. X-Y` as appropriate.
