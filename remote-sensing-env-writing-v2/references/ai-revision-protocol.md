# AI Revision Protocol

Use this protocol for automatic manuscript revision, polishing, or diagnosis.

## Step 1: Classify

Identify the section, manuscript type, target journal style, and task type. If the section is unknown, infer it from function:

- Gap-building and objectives indicate Introduction.
- Data sources, matching, equations, training, and validation design indicate Methods.
- Figure interpretation, metrics, spatial patterns, and trends indicate Results.
- Mechanism, literature comparison, limitations, and future work indicate Discussion.

## Step 2: Preserve Scientific Facts

Lock the following before editing:

- Variable names and units.
- Region, period, scale, and resolution.
- Dataset names and versions.
- Method names, acronyms, and module names.
- Quantitative values and comparison direction.
- Strength of causal evidence.

## Step 3: Diagnose Before Rewriting

Check whether the paragraph has:

- A clear main function.
- A complete logic chain.
- Enough evidence for the claim.
- Proper section placement.
- Consistent terminology.
- Appropriate claim strength.

## Step 4: Revise

Use the minimum intervention that solves the problem:

- If logic is weak, restructure first.
- If evidence is missing, flag the missing evidence.
- If wording is awkward but logic is sound, polish lightly.
- If the paragraph overclaims, downgrade the claim.
- If the paragraph is too vague, make nouns and relationships specific without inventing facts.

## Step 5: Return Evidence-Aware Output

For normal rewriting:

```text
Revised text:
[text]

Notes:
- [Only if needed.]

Scientific risks:
- [Only if needed.]
```

For full diagnosis:

```text
Diagnosis:
- Main issue:
- Section function:
- Evidence gap:
- Recommended fix:

Revised text:
[text]
```

## Automatic Downgrade Rules

- Replace `demonstrates` with `indicates` if evidence is observational.
- Replace `proves` with `suggests` or `supports`.
- Replace `caused by` with `may be associated with` if mechanism is not tested.
- Replace `globally applicable` with `applicable within the evaluated conditions`.
- Replace `eliminates uncertainty` with `reduces uncertainty`.
- Replace `best` with `outperformed [baseline] under [protocol]`.

## Section-Specific Repair

### Introduction
If only background exists, add a gap sentence. If only a gap exists, add consequence. If only objectives exist, add why the problem matters.

### Methods
If the method is a list of steps, add motivation and data flow. If equations appear without purpose, add purpose before the equation. If validation is missing, request split, baseline, and metrics.

### Results
If the paragraph lists numbers, add a main finding. If it repeats a figure, add interpretation. If it explains deep mechanisms, move or soften the sentence.

### Discussion
If Discussion repeats Results, add mechanism, comparison, limitation, or implication. If mechanism is unsupported, use cautious language and flag evidence need.

### Response Letter
If section numbers or revision evidence are absent, provide placeholders and state what evidence is needed.
