# Scientific Figure Review Checklist

Use this checklist when creating or revising paper and presentation figures. Treat the first section as hard failure conditions.

## Hard failure conditions

- Do not plot a quantity whose scientific meaning, source scope, or relation to the model/output path has not been verified.
- Do not compare panels or methods that use different rows, dates, masks, units, denominators, model versions, or split protocols without making the difference the explicit subject of the figure.
- Do not choose or redefine a metric, case, transformation, or scale solely to force a preferred ranking.
- Do not put an overall title or `suptitle` inside a scientific figure. Put the title in the manuscript caption or slide text layer.
- Do not put footer prose, provenance sentences, method notes, sample-count sentences, outlier notes, limitations, or conclusion sentences inside the plotted canvas.
- Do not use tiny low-contrast gray text to carry information needed to interpret the figure.
- Do not let any label, legend, colorbar, inset, histogram, metric block, date, or unit overlap another element or leave the canvas.
- Do not distort a map projection or geometry to force alignment.
- Do not deliver a figure that has not been inspected at original raster resolution.

## Information boundary

Keep inside the figure only:

- panel identifiers such as `(a)` and `(b)`;
- short panel or variable names when axes alone are insufficient;
- axis labels, units, ticks, legends, colorbar labels, and essential compact metrics;
- short point or event labels that directly identify plotted data.

Move outside the figure into the caption, slide, README, evidence table, or companion Markdown:

- the overall figure title;
- data provenance and time-period descriptions;
- split, sample-size, preprocessing, outlier, bootstrap, or significance-method sentences;
- interpretation, caveats, conclusions, and causal qualifications;
- long symbol definitions or methodological formulas not directly required to read an axis.

## Evidence and semantic contract

- State the panel's scientific question and evidence type before layout work.
- Verify the source model/product version, split, period, sample count, spatial support, unit, and aggregation.
- Trace internal diagnostics to their exact definition and downstream role. Distinguish detached diagnostics, forward gates, counterfactual differences, latent corrections, attribution values, and final outputs.
- Validate new metrics against known limits, identities, or negative controls and retain the formula in a companion artifact.
- Use one common eligible sample set for direct model comparison. Record any intentional mismatch as a limitation, not a footnote hidden by styling.
- Check cross-figure invariants: band/category order, denominator, annualization, variable names, model names, palette semantics, and registry status.

## Layout and geometry

- Give the primary evidence the largest area. Do not enlarge auxiliary panels merely to fill whitespace.
- Align comparable axis boxes exactly; use consistent row and column gaps.
- Keep related panels closer than unrelated groups.
- Avoid overly tall composites and large unused margins. Recompose or split when the narrative becomes hard to scan.
- Preserve projection and equal-axis geometry where scientifically required.
- Use shared outer labels when repeated labels add clutter.
- Check the actual axes rectangles, not only the outer canvas or successful `tight_layout` result.

## Typography and annotations

- Use one font family throughout the figure.
- Size every layer for the final insertion size, including ticks, legends, metrics, colorbars, and geographic labels.
- Scale typography coherently; do not enlarge only titles or panel letters.
- Use plain panel identifiers without colored or opaque backing unless contrast over data makes a small white backing unavoidable.
- Keep metric blocks unboxed and aligned when possible.
- Remove redundant headers such as `Model`, `Observed`, or `Predicted` when color and a shared legend already encode them.

## Axes, units, and number formatting

- Put units in axis or colorbar labels, not prose annotations.
- Use the correct variable-specific units in residuals and secondary axes.
- Show a shared-origin zero once and format it as `0` unless additional precision is meaningful.
- Prefer rounded, readable ticks. Use integers when possible, one decimal for correlation-like scales, and two decimals only when necessary.
- Use independent residual axes when residual and concentration ranges differ, but expose repeated right-axis decoration only on useful outer panels.

## Color and colorbars

- Use stable variable and model colors across a figure family.
- Give comparable methods the same border treatment; do not privilege one method with an unexplained black outline.
- Choose scale bounds from metric meaning and observed data. Do not force zero or a full theoretical range when it destroys contrast.
- Use continuous color when fine differences matter; use discrete levels only when meaningful thresholds exist.
- Keep colorbars centered on and no longer than their owning panel group.
- Prevent colorbars from colliding with geographic ticks, shared labels, or adjacent panels.
- Prefer low-saturation, colorblind-aware palettes with clear semantic direction.

## Maps

- Keep boundaries thin and subordinate to the data.
- Put longitude and latitude labels only on appropriate outer rows and columns.
- Use readable rounded geographic ticks.
- Do not place histograms or metric insets over important mapped data.
- Keep per-map annotations compact, normally a metric name and value only.
- Use polygon masks for named regions when analysis is intended to be limited to the region, rather than relying only on a bounding rectangle.

## Time series, distributions, and trajectories

- Use stable observation and prediction colors and one shared legend.
- Keep residuals visually subordinate and on a scientifically appropriate scale.
- Make phase or event backgrounds cover the full plotting interval without unexplained gaps.
- When trajectories overlap, split them into aligned facets with shared axes before trying exotic coordinates or dense matrices.
- Preserve equal axis scaling for direction or vector interpretation.
- Place date labels with collision-aware offsets; establish month context once and avoid repeated long dates.
- Make boxplot or violin categories readable at final size; shorten, wrap, rotate, or change layout rather than allowing adjacent labels to merge.

## Model comparison and structural diagnostics

- Apply identical geometry and styling to all compared methods.
- Distinguish overall evaluation from individual-case evaluation.
- Ensure adjacent panels answer different questions rather than repeating the same ranking.
- Replace dense annotated heatmaps with matrices, distributions, faceted paths, compact tables, or selected values when slide readability suffers.
- Make nodes large enough to contain labels and keep sign, magnitude, and model encodings consistent.

## Output and review gate

Before showing a preview:

1. Search the plotting code for `suptitle`, `fig.text`, long annotation strings, footer axes, and prose-like text. Remove any item not essential to reading plotted data.
2. Inspect panel alignment, gaps, clipping, and primary-to-auxiliary area ratios.
3. Inspect fonts at expected paper or slide scale.
4. Check units, tick precision, scale bounds, model/variable order, and color semantics.
5. Inspect the PNG at original resolution.
6. Export only the requested formats. Keep unapproved versions outside the final figure directory.
7. Confirm companion CSV/JSON statistics reproduce the displayed values and that any cache matches the current source contract.
8. Confirm the caption or slide note states evidence scope and interpretation limits without duplicating them inside the canvas.
