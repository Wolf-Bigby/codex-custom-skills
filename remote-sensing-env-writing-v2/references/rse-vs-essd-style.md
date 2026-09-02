# RSE / ISPRS vs ESSD Style Rules

## Core Difference

RSE and ISPRS papers usually sell a scientific or technical advance through a method, retrieval strategy, model architecture, validation protocol, and environmental interpretation. ESSD papers sell a community data resource through transparent data lineage, quality control, uncertainty, access, and reuse.

## RSE / ISPRS Method Paper

### What to emphasize
- A concrete remote-sensing or geospatial limitation.
- The proposed framework, algorithm, retrieval strategy, or model module.
- Baseline comparisons, ablations, independent validation, spatial transferability, and robustness.
- Environmental or physical interpretation that explains why the method works.

### Typical structure
1. Problem importance and method gap.
2. Study data and framework.
3. Model design or retrieval method.
4. Validation and comparison.
5. Spatial/temporal application.
6. Mechanism, limitation, and transferability discussion.

### Preferred claim style
- `The proposed framework improves... under...`
- `The gain is most evident in...`
- `This design helps reduce... by...`
- `The method remains subject to...`

### Avoid
- Overemphasizing data availability while underexplaining model design.
- Presenting a dataset as the only contribution when the paper is method-driven.
- Claiming operational readiness without near-real-time or independent validation.

## ESSD Dataset Paper

### What to emphasize
- Dataset name, version, variable, resolution, coverage, and period.
- Data lineage: input products, fusion, gap filling, quality control, uncertainty.
- Validation against ground observations or independent references.
- Data availability, file structure, access link, license, and reuse scenarios.
- Limitations that users must understand before applying the dataset.

### Typical structure
1. Community need for long-term, gap-free, high-resolution data.
2. Existing product limitations.
3. Dataset generation workflow.
4. Product description and validation.
5. Spatial-temporal characteristics and example applications.
6. Data availability, uncertainty, and usage notes.

### Preferred claim style
- `The dataset provides... at... during...`
- `Validation against... indicates...`
- `Users should note that...`
- `The product enables... while remaining subject to...`

### Avoid
- Hiding quality-control details.
- Treating dataset generation as a black-box model.
- Using method-paper hype such as `state-of-the-art` without product-oriented validation.
- Omitting data access and version information.

## AMT Measurement or Gap-Filling Paper

AMT style is procedural and transparent. Emphasize the measurement problem, the practical method, experimental design, reproducibility, and limitations. Show that the method works under controlled missingness, instrument, or observation conditions.

## Environmental Pollution / Application Paper

Application style balances environmental relevance and method adequacy. Emphasize exposure, source, pollution pattern, health or management relevance, and credible validation. Do not overdevelop algorithm details unless they affect interpretation.

## Conversion Rules

1. To convert RSE style to ESSD style, move from `method novelty` toward `product generation, validation, access, and uncertainty`.
2. To convert ESSD style to RSE style, move from `dataset description` toward `methodological challenge, framework design, comparison, and mechanism`.
3. To target ISPRS, strengthen geospatial representation, resolution, scene heterogeneity, mapping quality, and spatial validation.
4. To target AMT, strengthen measurement logic, reproducibility, missing-data tests, and practical constraints.
5. To target Environmental Pollution, strengthen environmental interpretation, pollutant relevance, exposure or management significance, and literature linkage.
