# Evidence-Safe Figure Development

Read this reference for model diagnostics, attributions, ablations, case studies, derived raster applications, or any figure whose rendering depends on expensive computation.

## 1. Lock the evidence contract

Record before computation:

- scientific question and intended claim;
- source artifact and model/product version;
- validation/test or other split protocol;
- date range, spatial domain, polygon mask, and aggregation unit;
- eligible rows or pixels and common-support rule;
- variables, units, band/category order, missing-data rule, and denominator;
- metric formula and whether higher or lower is better;
- output state: exploratory, audited candidate, approved, final, or archived.

If two panels differ on any field, make the difference explicit and scientifically purposeful.

## 2. Audit diagnostic semantics

For an internal model value, trace:

1. where it is computed;
2. whether it affects the forward prediction;
3. whether gradients reach it;
4. whether it is normalized or detached;
5. what reference or counterfactual it uses;
6. whether it is node-, edge-, graph-, component-, or output-level;
7. whether native-unit interpretation is valid.

Use the narrowest truthful label. A graph-minus-base counterfactual is not automatically a causal mechanism contribution. A whole-component Shapley value is not an edge reaction rate. A large attribution is not proof of improved accuracy.

## 3. Design and validate metrics

- Define the scientific construct independently of model ranking.
- Check identical, opposite, orthogonal, zero-magnitude, and shuffled cases when relevant.
- Separate marginal retrieval fidelity, pairwise association recovery, joint-state reconstruction, direction, and magnitude; do not hide several constructs inside an unexplained synthetic score.
- Preserve an unfavorable but valid aggregate result and explain why a complementary metric answers a different question.
- Store formulas, controls, sensitivity variants, and complete model/pair summaries outside the plot.

## 4. Separate compute from render

Use two stages:

1. `compute/audit`: produce full-data CSV, JSON, GeoTIFF, or tagged cache and verify identities;
2. `render`: read the audited artifact and change only layout, labels, colors, and geometry.

Tag expensive caches with source identifier or hash, period, grid, band order, units, algorithm version, and creation status. Reject incompatible tags. Use deterministic subsampling only for visible points or density estimation; calculate displayed statistics from all eligible data.

## 5. Select cases without outcome shopping

- Build candidates from observations or domain/regime criteria first.
- Use common station-date and pixel support for all models.
- Apply named-region polygon masks; use rectangles only for display extents.
- Rank candidates with a bounded set of preregistered criteria and retain rejection reasons.
- Keep overall model accuracy separate from case-specific accuracy.
- State whether the case is explanatory, validation, or application evidence.

## 6. Iterate efficiently

- Archive before a material redesign; do not proliferate active filenames.
- Batch related user feedback into one render pass.
- Use a low-resolution preview for geometry and an original-resolution render for acceptance.
- Reuse audited caches for layout changes and rerun computation only when the evidence contract changes.
- Inspect logs at completion or state changes rather than continuously polling routine renders.
- Maintain a compact handoff with active source, locked metrics, current candidate, rejected designs, and unresolved decision.

## 7. Acceptance record

Record:

- compute and render entrypoints;
- source and companion artifact paths;
- model/product and split;
- sample or pixel counts;
- figure dimensions and formats;
- semantic, statistical, visual, and file-validity checks;
- remaining claim limitation;
- promotion or archive decision.
