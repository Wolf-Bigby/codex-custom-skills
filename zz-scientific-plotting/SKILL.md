---
name: zz-scientific-plotting
description: Create, audit, or revise compact publication-ready and presentation-ready scientific figures with evidence-safe metrics, explicit encoding contracts, consistent geometry, typography, maps, validation panels, distributions, network diagnostics, and traceable exports. Use for multi-panel paper or PPT figures, observed-predicted validation, spatial maps, time series, case studies, model comparisons, mechanism or attribution plots, feature importance, or repeated visual refinement where scientific semantics, alignment, and readability matter.
---

# ZZ Scientific Plotting

Apply this standard to scientific figures unless the user gives a more specific instruction. Preserve scientific meaning first, then optimize geometry and visual hierarchy.

For every nontrivial multi-panel figure or repeated revision, read and apply [references/review-checklist.md](references/review-checklist.md) before editing. For a claim-bearing diagnostic, model comparison, case study, derived raster, or expensive repeated render, also read [references/evidence-and-iteration.md](references/evidence-and-iteration.md). Treat all hard failure conditions as mandatory.

## Non-Negotiable Figure Boundary

- Do not place an overall title, slide headline, manuscript-style figure title, or `suptitle` inside a scientific figure. Titles belong in the manuscript caption or the presentation text layer.
- Do not place footer prose inside the plotting canvas. This includes gray source notes, split or period descriptions, sample-count sentences, outlier notes, bootstrap or significance-method sentences, limitations, and conclusion text.
- A figure intended for insertion into a slide remains a scientific figure asset. Do not bake the slide title or slide conclusions into the PNG unless the user explicitly asks for a complete slide image.
- Keep only data-reading elements inside the figure: panel identifiers, short panel names, axes, units, ticks, legends, colorbar labels, and essential compact metrics.
- Move provenance, processing choices, statistical definitions, interpretation, and caveats to the caption, slide body, README, evidence Markdown, or companion table.
- Audit every use of `fig.text`, `suptitle`, footer axes, and long `axis.text` strings before rendering. Shared axis labels are acceptable; prose-like annotations are not.
- Never use tiny low-contrast gray text as a fallback for information that does not fit. Remove it, relocate it outside the figure, or redesign the layout.

## Workflow

1. State the figure's scientific question, evidence role, comparison scope, and one main visual claim before choosing a layout.
2. Inspect the production script, source tables or rasters, metric definitions, model or product version, units, related accepted figures, and applicable references.
3. Lock the evidence contract: split, sample support, period, region or mask, aggregation, baseline, missing-data rule, and whether the source is observed, predicted, diagnostic, counterfactual, or attributed.
4. Compute and audit claim-bearing quantities separately from rendering. Save a compact table or JSON record and verify identities, controls, and cross-model row alignment.
5. Record panel order, canvas height, output formats, encoding channels, and repeated/shared labels. Define panel geometry explicitly before drawing data.
6. Generate a fast raster preview. Remove overall titles and footer prose, then inspect at original resolution and at the intended insertion scale.
7. Correct semantics, alignment, overlaps, whitespace, typography, tick formatting, color scales, and projection behavior. Recompute expensive inputs only when the evidence contract changed.
8. Export only the requested formal formats and update companion statistics, audit artifacts, caption or slide notes, and figure registry.
9. Verify dimensions, file validity, source contract, sample counts, CRS, units, formulas, cross-figure consistency, and output registration.

## Scientific Evidence Gate

- Do not select a metric, transformation, case, color range, or panel solely to make a preferred method rank first. Define the scientific construct first, test expected limits or negative controls, and report an unfavorable valid result honestly.
- Trace every internal diagnostic from its exported field through the model or analysis path. State whether it is a forward gate, detached report, counterfactual difference, latent correction, whole-component attribution, edge-level value, or final-output response.
- Do not infer predictive benefit from large attribution values, and do not infer inactivity from small aggregate ablation gains. Attribution, counterfactual response, and controlled ablation answer different questions.
- Compare models on identical rows, dates, locations, masks, units, and aggregation. Label validation versus test, random versus spatial split, and station versus raster evidence before quoting metrics.
- Keep native-unit errors separate across variables. Use normalized errors only when direct cross-variable comparison is intended and document the denominator.
- Validate formulas with analytically known limits, invariants, or shuffled controls when introducing a new metric. Preserve the formula and definition outside the canvas.
- Treat a successful render as insufficient evidence. A figure fails if the plotted quantity is semantically misidentified or if related panels use incompatible source contracts.

## Encoding Contract

- Write a compact mapping before rendering: `visual channel -> variable -> unit or normalization -> scope`. Apply one meaning per channel.
- Use position for structure, hue for category or signed direction, luminance for ordered magnitude, size for one quantitative magnitude, line style for one relationship class, and annotation for exact values only when needed.
- For network figures, distinguish fixed topology, learned or routed graph weight, node response, component contribution, edge direction, and native-unit values. Do not imply per-edge learned weights when only a graph-level scalar exists.
- Use equal visual treatment for compared methods. Do not add a unique outline, saturation boost, or area advantage to a preferred method without a stated encoding reason.
- Switch from discrete to continuous color when meaningful close differences collapse into the same bin. Use discrete levels only for defensible thresholds or categories.

## Geometry And Layout

- Make the information narrative determine the layout; do not repeat a previous figure's grid merely for consistency if it causes visual fatigue.
- Keep related figures at the requested common height. Allow width or aspect ratio to change when a different panel grammar requires it.
- Make panels that form one vertical or horizontal module share the exact same axis-box width or height.
- For a map–distribution–time-series module, match the map frame, histogram frame, and time-series frame horizontally.
- Preserve map projection aspect. Prefer changing canvas width, map height, or grid ratios over stretching a projected map with `aspect="auto"`.
- Use equal inter-column gaps unless a deliberate group separator is required. Keep paired panels closer than unrelated groups.
- Minimize unused whitespace and row gaps, but retain enough room for units, ticks, and shared labels.
- Use explicit axes positions when automatic layout engines or projected GeoAxes create visibly unequal spacing.
- Apply borders consistently: either frame all comparable panels or omit comparable borders. Avoid one-off frames.

## Typography And Hierarchy

- Size text for the final medium. PPT figures require larger fonts than manuscript-only figures.
- Do not solve a slide-readability problem by adding an overall figure title or explanatory footer; reserve slide-level text for the slide layout.
- Use a clear hierarchy: panel/pollutant label, primary metrics, axis labels, ticks, legend, then secondary annotations.
- Increase all figure typography together when readability is poor; do not enlarge only titles while leaving ticks and colorbars small.
- Place panel sequence labels inside an upper corner. Use only `(a)`, `(b)`, and so on; put the variable name separately or beside it without explanatory prose.
- Use a small white backing only when a panel label needs contrast over map or dense data. Keep metrics and histogram annotations unboxed unless the user requests otherwise.
- Avoid repeating a pollutant or variable name in adjacent panels when a central map or shared label already identifies it.

## Validation Scatterplots

- Use density-colored points or a smooth density representation for large samples.
- Show a 1:1 reference and an OLS fit when scientifically useful, but omit redundant legend entries when their line grammar is obvious and consistent.
- Put the enlarged metric block in the upper-left unless data occupancy requires a documented alternative.
- Keep the metric block away from panel labels, markers, regression lines, and histogram insets.
- Format equations compactly as `Y=0.01X+1.1`; omit spaces around operators and retain pollutant-appropriate precision.
- Prefer `N`, `R²`, `RMSE`, and optionally `MAE`; avoid over-annotating validation method descriptions inside panels.
- Use native units on axes. Do not compare native-unit RMSE across variables without explanation.

## Maps

- Retain a consistent projection, national/provincial boundaries, geographic extent, and inset grammar across related maps.
- Keep administrative boundaries subordinate to the data with thin neutral strokes.
- Include required offshore or inset regions without fabricating values in NoData areas.
- Align map frames with adjacent Cartesian panels through layout geometry, not geographic distortion.
- For concentration maps, use a consistent palette across variables while allowing independent variable-specific ranges when units or distributions differ.
- State the spatial product period in the caption, registry, or audit table. Do not silently combine maps and validation statistics from incompatible periods or model versions.

## Time Series And Distributions

- Use a neutral dark color for observations and stable, distinguishable colors for predicted variables.
- Keep variable-color semantics identical across related figures.
- Render residuals as a low-emphasis band or bars so they do not compete with observed and predicted lines.
- Share legends across panels. Avoid repeating `Observed` and `Predicted` labels on every subplot.
- Use a common distribution axis when direct comparison is intended; otherwise explain independent scales.
- Show a compact median or other key statistic without an opaque annotation box.

## Cases And Application Figures

- Define candidate events or regions from observations, domain signals, or a preregistered screen before ranking model behavior. Do not search directly for the interval where one model looks best.
- Evaluate all methods on common dates, stations, pixels, and support masks. Retain the candidate pool, selection criteria, rejected reasons, and final scope.
- Use polygon or vector-union masks for named regions. A bounding rectangle may define the display extent but must not silently define the analytical population.
- Match pollutants and statistics to the proposed process instead of forcing one fixed variable set onto every case.
- Keep station-matched sequences, regional raster means, and population-weighted summaries distinct. Never switch spatial aggregation between panels without labeling it.
- Use bounded application terminology. Do not label an observation-anchored high-occurrence screen as regulatory exceedance, health risk, AQHI, exposure, or causal mechanism unless its definition supports that term.
- Verify band order, category bit order, denominators, annualization, population weighting, and exact-category closure across related maps and summaries.

## Axes, Units, Ticks, And Colorbars

- Put units in standard axis labels or colorbar labels instead of repeating units in every textual annotation.
- Use shared `Observed`/`Predicted` axis labels when repeated panels make the meaning unambiguous; remove redundant labels on outer columns when requested.
- Prevent units from colliding with tick labels. Increase label padding or move the shared label before reducing font size.
- At a shared origin, display zero once when duplicate x/y zero labels overlap. Format zero as `0`, not `0.0` or `0.00`, unless precision is scientifically meaningful.
- Build colorbar limits and ticks from rounded, readable values. Prefer integers; use one decimal for correlation-style scales and two decimals only when needed.
- Center colorbars relative to their owning panel or panel group. Do not let a colorbar extend beyond the plotted axes.
- Make slide colorbars large enough to read and place their descriptions beside or above them when that reduces crowding.
- Use 4–6 major colorbar ticks and include both endpoints.

## Ordering And Figure-Family Consistency

- Preserve a user-approved variable order across scatterplots, maps, time series, and tables.
- When ordering by performance, place stronger variables first and explicitly requested weaker or special-unit variables last.
- Keep units, colors, names, panel order, and statistical definitions stable across the figure family.
- Treat explicit user feedback from accepted figures as a project style override and apply it to later figures where the same design condition recurs.

## Naming And Traceability

- Use formal, descriptive figure stems rather than names containing `test`, `trial`, `candidate`, or raw experiment identifiers.
- Maintain a figure registry with number, stem, bilingual or project-required title, evidence source, status, and primary use when the project has multiple formal figures.
- Move superseded experimental outputs to a recoverable archive instead of leaving ambiguous active versions.
- Save derived statistics and raster/source audits beside formal figures when they support interpretation or reproducibility.
- Keep provenance and audit detail in those companion artifacts rather than rendering them as footer text inside the figure.

## Iteration And Candidate Lifecycle

- Separate evidence computation from rendering. Cache expensive validated summaries with source identifiers so geometry-only revisions do not rescan large rasters or rerun model inference.
- Tag caches with source paths or hashes, band order, period, grid, units, and algorithm version. Refuse stale or incompatible caches rather than silently reusing them.
- Use deterministic subsampling only for dense visual layers. Compute metrics, quantiles, boxes, and saved summaries from the full eligible dataset unless the method explicitly defines sampling.
- Keep figure states explicit: exploratory, audited candidate, user-approved, final, or archived. Only approved assets enter the formal directory.
- Archive the prior accepted candidate before a material redesign. Keep active stems unambiguous and do not overwrite a confirmed figure with a testing variant.
- Batch related style edits, render a cheap preview, and inspect only the changed regions plus the full canvas. Use state-change-only status checks for routine renders; avoid repeated full-data recomputation, repeated large log reads, or minute-level polling for layout-only work.
- When iteration becomes long, record the locked evidence contract and active visual decisions in a compact handoff so a new session can continue without reloading the entire history.

## Pre-Export Gate

Do not declare completion until all applicable checks pass:

- no overall title or `suptitle` is embedded in the scientific figure;
- no footer paragraph, provenance sentence, method sentence, outlier note, sample-count sentence, limitation, or conclusion text is embedded in the canvas;
- every `fig.text`, footer axis, and long free-text annotation is necessary for reading plotted data rather than explaining the study;
- panel frames align and intended gaps are equal;
- no text, marker, unit, tick, legend, or inset overlaps;
- font sizes remain readable at slide or manuscript insertion scale;
- map projection and geographic shapes are not stretched;
- zero and decimal formatting are consistent;
- colorbars are centered, bounded by their panels, and readable;
- variable order, colors, units, periods, and statistical definitions match related figures;
- the plotted diagnostic's semantic role has been traced and is not overstated;
- compared models or panels use common support and compatible evidence contracts;
- metric formulas, category encodings, band order, denominators, and aggregation identities pass their audits;
- expensive caches are compatible with the active source contract and full-data statistics are not replaced by rendering samples;
- PNG dimensions and PDF/SVG validity are verified;
- the final raster is inspected at original resolution.
