# Core Writing Rules

Use these rules as the default quality standard for White Group remote sensing environmental science manuscripts.

## Logic and argument

1. Start from a concrete scientific or operational need, not from the existence of a model.
2. State the limitation and its consequence in the same paragraph whenever possible.
3. Link every contribution to a previously stated gap.
4. Separate observation, interpretation, and speculation with explicit wording.
5. Use contrastive connectors only when a real contrast exists.
6. Do not let a paragraph contain multiple unrelated main claims.
7. Make each paragraph answer one functional question.
8. Put the study response after the gap, not before it.
9. Avoid listing datasets before explaining why the research problem requires them.
10. End major paragraphs with a sentence that advances the argument.
11. Prefer causal modesty: write `may partly explain` when evidence is indirect.
12. Do not use novelty as the first argument unless the unmet need has already been established.
13. Keep the level of claim proportional to the scale of validation.
14. Use synthesis sentences to connect method design with environmental meaning.
15. Make scope conditions explicit when generalizing from regional evidence.

## Terminology and variables

16. Define every acronym at first use and reuse the same acronym consistently.
17. Keep variable names identical across Abstract, Methods, Results, and figures.
18. Report units with quantitative values when units are available.
19. Do not switch between PM2.5, fine particulate matter, and particulate pollution without reason.
20. Use `retrieval`, `estimation`, `mapping`, and `prediction` according to the actual task.
21. Reserve `validation` for independent or explicitly defined evaluation procedures.
22. Use `benchmark`, `baseline`, and `comparison method` consistently.
23. Distinguish satellite observations from derived products.
24. Distinguish ground measurements from labels or reference data.
25. Name the sensor, product version, period, and resolution when they matter for reproducibility.
26. Avoid vague nouns such as `factor`, `thing`, `situation`, and `aspect` when a technical term exists.
27. Use `uncertainty`, `bias`, `error`, and `noise` with distinct meanings.
28. Avoid redefining a symbol after it is introduced.
29. When translating Chinese notes, preserve the technical noun before improving style.
30. Do not replace a specific product name with a generic category if reproducibility would suffer.

## Tone and claim strength

31. Use formal, restrained, evidence-led language.
32. Avoid promotional intensifiers unless supported by quantified evidence.
33. Prefer `substantial`, `notable`, or `consistent` over `dramatic`.
34. Use `indicate` for empirical evidence and `suggest` for weaker interpretation.
35. Use `demonstrate` only when the validation directly supports the claim.
36. Use `likely` and `may` for mechanism explanations that are not directly tested.
37. Avoid `prove` in empirical environmental remote sensing contexts.
38. Avoid absolute claims such as `always`, `never`, and `fully resolves`.
39. Do not claim global applicability from one-region validation.
40. Do not call a method robust unless robustness has been tested.
41. Use active voice for study decisions: `we develop`, `we evaluate`, `we compare`.
42. Use passive voice for objective processing: `data were resampled`, `samples were filtered`.
43. Keep sentences dense but readable; do not stack more than three subordinate clauses.
44. Use explicit subjects instead of vague `it` when ambiguity is possible.
45. Do not soften a real limitation until it disappears.

## Title and Abstract

46. Put the target variable in the title when the paper is variable-specific.
47. Put scale, region, or period in the title when they are part of the contribution.
48. Use acronym-plus-definition titles only when the acronym names a real method or product.
49. Avoid titles beginning with `A novel study of`.
50. For method papers, include task and mechanism in the title.
51. For dataset papers, include resolution, coverage, period, and variable when possible.
52. Make the Abstract follow background -> gap -> response -> method/data -> key results -> significance.
53. Include at least one quantitative validation result when available.
54. Do not overload the Abstract with all metrics.
55. Define the method or dataset acronym in the Abstract.
56. Report the strongest result only if it is central to the contribution.
57. Do not use the Abstract to introduce unsupported mechanism speculation.
58. End the Abstract with bounded application value, not broad slogans.
59. Keep the first Abstract sentence about the problem, not about the paper.
60. Make the final Abstract sentence match the evidence level of the Results.

## Introduction

61. Use a four-part structure: importance, progress, gap, study response.
62. Make the first paragraph establish why the environmental variable matters.
63. Summarize prior work by method family, data source, or limitation class.
64. Do not turn the Introduction into a chronological literature list.
65. Write the gap as limitation plus consequence.
66. Explain why the gap matters for science or application.
67. Avoid `few studies` unless the missing dimension is specified.
68. Do not report detailed results in the Introduction.
69. Use `To address these limitations` only after the limitations are clear.
70. State objectives or science questions near the end.
71. For method papers, identify the design difference from prior approaches.
72. For dataset papers, identify the unmet community data need.
73. For analysis papers, identify the unresolved spatial, temporal, or mechanistic question.
74. Keep contributions concrete and countable.
75. Do not claim a contribution that the Methods or Results cannot support.

## Data and Methods

76. Describe each dataset by source, version, period, resolution, variable, quality control, and study role.
77. Make Study Area justify representativeness or difficulty, not just location.
78. Separate data description from model design.
79. Provide a framework overview before module details.
80. Define inputs, outputs, and data flow before equations.
81. Introduce each module by motivation -> operation -> expected effect.
82. State matching, aggregation, filtering, and resampling procedures.
83. Report training, validation, holdout, cross-validation, and baseline settings.
84. Define metrics in Methods before reporting them in Results.
85. Do not claim superiority in Methods.
86. Use equations only when they clarify an operation or objective.
87. Define all equation symbols immediately.
88. State parameter choices or selection procedures when they affect reproducibility.
89. For machine learning, describe features, labels, split strategy, model tuning, and ablations.
90. For datasets, describe data lineage, versioning, quality control, uncertainty, and availability.

## Results

91. Organize Results around figures, tables, and result questions.
92. Begin each Results subsection with what is being evaluated.
93. Use `Fig. X shows` or equivalent only when followed by interpretation, not figure repetition.
94. Report key metrics with comparison context.
95. Do not list every number from a table.
96. Explain spatial patterns as observations first, not mechanisms.
97. Report temporal trends by period, direction, and heterogeneity.
98. For model comparisons, state the validation protocol and baseline.
99. For ablation studies, connect each performance change to the removed component.
100. For case studies, explain why the case was selected.
101. Keep deep causal explanation for Discussion.
102. Use cautious preliminary explanations at the end of result paragraphs.
103. Mention uncertainty results when they affect interpretation.
104. Do not hide poor-performing regions or conditions.
105. Make the main finding visible before secondary details.

## Discussion and Conclusion

106. Use Discussion to explain why the result occurs and where it may fail.
107. Connect performance gains to specific data, module, or physical constraints.
108. Compare with prior studies by condition and reason, not by vague superiority.
109. Discuss spatial generalization and temporal robustness when relevant.
110. Explain error sources: sparse stations, heterogeneous land cover, cloud gaps, sensor bias, terrain, or label uncertainty.
111. State limitations as real constraints, not defensive afterthoughts.
112. Make future work specific to the limitation.
113. Do not repeat the Results subsection by subsection.
114. Use literature comparison to position the finding, not to inflate it.
115. For dataset papers, discuss use conditions and known uncertainty.
116. For method papers, discuss transferability and failure modes.
117. Keep Conclusion shorter than Discussion.
118. Restate objective, main findings, contribution, and application value.
119. Avoid introducing new evidence in Conclusion.
120. End with a bounded implication or concrete future direction.

## AI revision safety

121. If evidence is missing, flag it instead of inventing it.
122. If a Chinese draft is logically thin, add structure but not new facts.
123. If the user gives numbers, preserve them exactly unless asked to format units.
124. If the comparison direction is unclear, ask or mark uncertainty.
125. If section identity is ambiguous, infer and state the inferred section.
126. If a sentence contains unsupported causality, downgrade to association or possible explanation.
127. If the text overclaims novelty, tie novelty to the concrete capability.
128. If response evidence is missing, provide a fillable response rather than fake section numbers.
129. If a manuscript has conflicting terms, recommend one and list the conflict.
130. If a paragraph mixes Methods and Results, split by function.
131. If Results and Discussion are merged by the journal format, still separate observation from interpretation within paragraphs.
132. If journal target is ESSD, prioritize data availability and uncertainty over method hype.
133. If journal target is RSE or ISPRS, prioritize methodological contribution and rigorous validation.
134. If the user asks for polishing only, still flag major scientific risks briefly.
135. If the input is already strong, minimize edits and preserve author voice.

Total explicit rules: 135.
