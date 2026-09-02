# Introduction, Methods, Results, and Discussion Strategies

## Introduction Strategy

The Introduction should move from environmental importance to remote-sensing opportunity, then to a precise limitation and consequence. Use four paragraphs unless the journal format requires compression.

### Paragraph 1: Importance
Write the target variable as a scientific and societal problem. For PM2.5, connect monitoring to exposure, health, climate, and policy. For methane, connect detection and quantification to emission mitigation and carbon-cycle constraints. For AOD or air pollutants, connect data continuity to environmental management and Earth system analysis.

### Paragraph 2: Progress
Group prior work by data source, algorithm family, scale, or product type. Avoid one-paper-per-sentence chronology. The goal is to show that the field has advanced enough for a sharper unresolved problem.

### Paragraph 3: Gap
Write the gap as `limitation + consequence`. Examples: sparse monitoring reduces spatial transferability; cloud contamination causes discontinuity; coarse reanalysis weakens local gradients; complex terrain produces spectral interference; existing products lack uncertainty documentation or recent updates.

### Paragraph 4: Response
State the study response, differentiator, and objectives. For method papers, emphasize the mechanism or design. For dataset papers, emphasize data lineage, coverage, resolution, validation, and reuse. For analysis papers, emphasize the unresolved spatial, temporal, or mechanistic question.

## Methods Strategy

The Methods section must let another researcher reproduce the study.

### Overall framework
Begin with a compact overview: objective, inputs, main procedures, outputs, and validation design. Then move to modules.

### Dataset description
For each dataset, state source, version, period, spatial/temporal resolution, variables, quality control, preprocessing, and role in the study. Do not mix data description with claims about model performance.

### Module writing
For each module, use `motivation -> design -> formulation or operation -> expected effect`. If using graph learning, explain nodes, edges, attributes, attention, and how scene similarity or spatial dependency reduces error. If using spectral reconstruction, explain what signal is reconstructed and why it helps detection. If using data fusion, explain how missingness, scale mismatch, and uncertainty are handled.

### Validation design
Define cross-validation, spatial holdout, temporal holdout, independent validation, baselines, ablations, and metrics before Results. Make clear whether validation tests interpolation, extrapolation, temporal robustness, spatial transfer, or product consistency.

## Results Strategy

Results should be figure-centered and claim-limited.

### Overall performance
State validation protocol, primary metrics, and comparison object. Then interpret what the metric means for the scientific or mapping task.

### Spatial patterns
Describe gradients, hotspots, low-value regions, urban-rural contrasts, terrain effects, or emission-related patterns as observations. Use mechanism only as a preliminary explanation unless tested.

### Temporal patterns
State period, trend direction, seasonality, turning points, and regional heterogeneity. Avoid saying `changed significantly` without scale and direction.

### Benchmark and ablation
State the controlled condition. Report where the method improves most and connect that improvement to the removed or added component.

### Uncertainty and sensitivity
Report how uncertainty changes across space, time, data conditions, or parameter settings. Explain why this matters for interpretation or reuse.

## Discussion Strategy

Discussion should explain, position, and bound the results.

### Why it works
Connect the result to model design, data complementarity, physical consistency, scene similarity, spectral separation, or temporal constraints.

### Why it fails
Discuss sparse observations, terrain complexity, surface heterogeneity, cloud gaps, label uncertainty, sensor bias, retrieval artifacts, and domain shift.

### Literature comparison
Compare with previous work under comparable conditions. Avoid `better than previous studies` unless the comparison is controlled. Prefer `extends`, `complements`, `differs from`, or `is consistent with`.

### Applicability and limitations
State where the method or dataset can be used, where caution is required, and what future validation is needed. For ESSD, include data access, versioning, and uncertainty. For RSE/ISPRS, include generalization and robustness.

## Results vs Discussion Boundary

Use this rule: Results answers `what was observed under what evaluation`; Discussion answers `why it may have occurred, how it compares, and where it applies`. If a sentence contains `because`, `likely arises from`, or `may be attributed to`, it usually belongs in Discussion unless it is a brief preliminary explanation.
