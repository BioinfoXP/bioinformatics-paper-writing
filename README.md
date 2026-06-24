```markdown
# bioinformatics-paper-writing

A Codex skill for writing and revising bioinformatics manuscripts at a high review standard.

**简要说明**：这是一个面向生物信息学论文写作的 Codex 技能，支持根据结果图、分析代码和用户提供文献生成或修改论文内容。默认输出偏向 Nature 风格，并强调证据链、图文一致性和审稿友好性。

---

## 🚀 What this skill does

`bioinformatics-paper-writing` helps turn bioinformatics analyses into publication-ready manuscript text. It is designed for workflows where the writing must stay tightly aligned with figures, code, cohorts, assays, validation logic, and reviewer expectations.

The skill is especially useful for:
*   Bioinformatics and computational biology manuscripts
*   Multi-omics and spatial transcriptomics studies
*   Tumor microenvironment and translational cancer papers
*   Results writing from figures
*   Methods writing from code or notebooks
*   Literature-guided writing refinement
*   Figure legend drafting in a strict, manuscript-ready format

---

## 🧠 Core capabilities

### 1. Results from figures
The skill can read multi-panel scientific figures and convert them into reviewer-friendly Results text.

It is built to handle:
*   Heatmaps, Volcano plots, UMAP or t-SNE plots
*   Kaplan-Meier curves, Boxplots, and violin plots
*   Spatial transcriptomics maps
*   Immunofluorescence, pathology, and microscopy images
*   Composite multi-panel figures

**For figure-driven writing, the skill emphasizes:**
*   Clear biological meaning rather than panel-by-panel narration.
*   Explicit figure anchors such as `Fig. 6A` or `Fig. 6B-D`.
*   Cautious interpretation when statistics or labels are incomplete.
*   Logical scientific flow instead of visual order when needed.

### 2. Methods from code
The skill can read code, notebooks, or pipelines and reconstruct a Methods section from the actual implementation. 

**It helps recover:**
*   Inputs, Preprocessing steps, Filtering strategy
*   Normalization, Statistical testing
*   Model-building steps, Outputs and analysis flow

> **Note:** This is especially useful when the manuscript draft and the real code have drifted apart.

### 3. Literature learning
The skill can learn reusable writing patterns from user-provided literature without rewriting the skill itself.

**Supported literature inputs include:**
*   PDFs, DOI-linked papers, Abstracts, Full text
*   Figure legends, Supplementary methods, User notes

It can persist structured knowledge under the local `knowledge/` directory for later reuse.

### 4. Strict figure legends
The skill includes a strict legend mode for manuscript-ready figure legends.

**Default legend rules:**
1.  Start with `Figure X.` and one short message sentence.
2.  Insert one blank line after the opening sentence.
3.  Write one panel per line.
4.  Use `(A)`, `(B)`, `(C)` formatting.
5.  End each panel sentence with a period.
6.  Avoid semicolon-chained panel descriptions.

This keeps legend formatting stable and submission-friendly.

---

## 🔄 Supported workflows

The skill is designed around four main entry modes:

1.  **Text-first writing** 
    Drafting or revising manuscript text from outlines, bullets, drafts, or reviewer comments.
2.  **Figure-first Results writing** 
    Writing Results paragraphs directly from figures.
3.  **Code-first Methods writing** 
    Writing Methods from analysis scripts, notebooks, or workflow folders.
4.  **Literature-learning mode** 
    Extracting reusable writing patterns from papers and storing them for future use.

---

## ✍️ Writing style defaults

Unless explicitly overridden by the user, the skill defaults to:
*   Bilingual Chinese-English output (Chinese first, English second)
*   Nature-style scientific prose
*   Claim-first paragraph structure
*   Cautious causal language
*   Strong emphasis on claim-evidence alignment
*   Explicit figure anchors in figure-based Results writing

---

## 📂 Repository structure

```text
bioinformatics-paper-writing/
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
├─ references/
│  ├─ by-input/
│  │  ├─ results-from-figures.md
│  │  ├─ methods-from-code.md
│  │  └─ learning-from-literature.md
│  ├─ core/
│  │  ├─ study-design.md
│  │  └─ story-patterns.md
│  ├─ quality/
│  │  ├─ paper-review.md
│  │  ├─ validation.md
│  │  └─ writing-flow.md
│  └─ sections/
│     ├─ abstract.md
│     ├─ introduction.md
│     ├─ related-work.md
│     ├─ results.md
│     ├─ methods.md
│     ├─ figure-legends.md
│     ├─ discussion.md
│     └─ conclusion.md
└─ knowledge/
   ├─ README.md
   ├─ paper-notes/
   └─ syntheses/

```

---

## 🛠️ How to use

In Codex, invoke the skill when you want manuscript-quality bioinformatics writing support.

### Example prompts

* **Figure-based Results**
> `Use $bioinformatics-paper-writing to write bilingual Nature-style Results from this multi-panel figure. Anchor each major claim to the relevant panels.`


* **Code-based Methods**
> `Use $bioinformatics-paper-writing to reconstruct a reproducible Methods section from this notebook and analysis script directory.`


* **Literature-guided revision**
> `Use $bioinformatics-paper-writing to learn from this paper and then revise my Results section using the extracted writing patterns.`


* **Reviewer-facing refinement**
> `Use $bioinformatics-paper-writing to revise this Discussion section for stronger claim-evidence alignment and lower over-interpretation risk.`


* **Draft a figure legend**
> `Use $bioinformatics-paper-writing to write a strict Nature-style figure legend for this figure.`



---

## 📊 Output behavior

### Manuscript mode

By default, the skill writes like manuscript copy rather than a working memo. Typical output includes:

* A conclusion-like subsection title when needed
* A Chinese manuscript block
* An English manuscript block
* A strict figure legend when figure input is provided

### Analysis mode

If the user explicitly asks for review support, teaching, or traceability, the skill can additionally provide:

* Compact section outlines
* Observation-versus-interpretation splits
* Claim-evidence maps
* Review-oriented checks

---

## 📐 Design principles

This skill is optimized around a few writing principles:

* One paragraph should carry one main message.
* Results should read as biological answers, not analysis logs.
* Discovery and validation should be clearly separated.
* Mechanistic claims should be proportionate to the evidence.
* Figure-based writing should stay anchored to visible support.
* Writing should remain useful to skeptical reviewers.

---

## ⚠️ Limitations

This skill **does not** replace domain judgment. It is strongest when figure labels are readable, comparison groups are visible, code is complete, and the user supplies missing context.

It will intentionally **avoid** inventing:

* Missing statistics
* Unseen labels
* Unsupported mechanism claims
* General rules from a single paper without qualification

---

## 📝 Notes

* The skill supports persistent local learning through the `knowledge/` directory.
* It does not automatically rewrite its own `SKILL.md`.
* Conflicts between new literature and existing learned patterns should be surfaced rather than silently overwritten.

## 📄 License

[MIT]

```

```
