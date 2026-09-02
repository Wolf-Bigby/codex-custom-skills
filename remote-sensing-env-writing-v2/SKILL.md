---
name: remote-sensing-env-writing-v2
description: Use when drafting, rewriting, polishing, diagnosing, or responding to reviews for remote sensing environmental science SCI manuscripts, especially White Group style work on PM2.5, AOD, methane, air quality, data fusion, gap-free datasets, RSE, ISPRS, ESSD, AMT, or Environmental Pollution papers.
---

# Remote Sensing Environmental Science Writing Skill v2.0

## Overview
Use this skill to write, revise, and diagnose English SCI manuscripts in the White Group remote sensing environmental science style. Prioritize scientific logic, reproducibility, figure-centered results, evidence-bounded discussion, and conservative claims.

## First Decision
Before rewriting, identify four labels:

1. **Task type**: draft, rewrite, polish, compress, expand, diagnose, translate-to-English, response letter.
2. **Manuscript type**: method innovation, dataset/product, spatiotemporal analysis, review/synthesis, application case.
3. **Target style**: RSE/ISPRS method paper, ESSD data paper, AMT measurement method paper, Environmental Pollution application paper, generic SCI.
4. **Section**: Title, Abstract, Introduction, Data, Methods, Results, Discussion, Conclusion, Response Letter.

If any label is missing, infer it from the text. If inference would change scientific meaning, state the assumption before revising.

## Reference Loading
Load only the reference needed for the task:

- Read `references/source-corpus.md` when checking the representative corpus or explaining style origins.
- Read `references/core-writing-rules.md` before broad manuscript revision, quality audit, or full-section rewriting.
- Read `references/introduction-methods-results-discussion.md` for Introduction, Methods, Results, or Discussion work.
- Read `references/rse-vs-essd-style.md` when the target journal style is RSE, ISPRS, ESSD, AMT, or when choosing between method-paper and dataset-paper rhetoric.
- Read `references/sentence-templates.md` when drafting from Chinese notes, expanding rough bullet points, or needing style-consistent sentence options.
- Read `references/response-letter.md` for editor/reviewer replies, rebuttal letters, point-by-point responses, or response-to-reviewer sections.
- Read `references/ai-revision-protocol.md` when asked to automatically revise, diagnose, score, or produce a structured edit report.

## Default Workflow
1. Preserve facts first: variables, units, comparisons, sign, magnitude, region, period, and method names.
2. Diagnose the logic chain before polishing sentences.
3. Fix section function: Introduction builds the gap; Methods enables reproduction; Results reports figure-centered evidence; Discussion explains mechanism and limits.
4. Select the journal style: RSE/ISPRS emphasizes method novelty and validation; ESSD emphasizes data lineage, uncertainty, access, and reuse.
5. Revise with controlled strength: use `may`, `likely`, `suggest`, `indicate`, and `within the context of` when evidence is partial.
6. Return the revised text first. Add a short note only when logic was changed, assumptions were made, or risks remain.

## Non-Negotiable Rules
- Do not invent datasets, mechanisms, results, citations, equations, validation settings, section numbers, or reviewer actions.
- Do not convert a weak result into a strong causal claim.
- Do not report new quantitative values unless provided by the user.
- Do not move deep mechanism speculation into Results.
- Do not use promotional language such as `revolutionary`, `unprecedented` without concrete evidence and journal fit.
- Do not erase uncertainty, boundary conditions, or data limitations.
- Do not over-standardize voice: use active voice for study actions and passive voice for data processing.

## Output Formats

For rewriting:

```text
Revised text:
[polished section]

Notes:
- [Only include if logic, evidence, or assumptions need explanation.]

Scientific risks:
- [Only include if a claim lacks evidence, a mechanism is unsupported, or data/method details are missing.]
```

For diagnosis:

```text
Diagnosis:
- Logic:
- Section function:
- Evidence:
- Style:

Recommended revision:
[actionable rewrite plan or revised text]
```

For response letters:

```text
Response:
[polite, evidence-based reply]

Revision evidence needed:
- [Section/Figure/Table/citation/experiment if missing.]
```

## White Group Style In One Paragraph
Write in a formal, restrained, technically dense, evidence-led style. Open from a scientific or operational need, move through existing progress, define a concrete limitation and consequence, introduce the study response, then support claims through data, validation, figures, comparisons, uncertainty analysis, and bounded interpretation. Prefer explicit logical connectors over abrupt transitions. Make methods reproducible, results figure-centered, and discussion explanatory but cautious.
