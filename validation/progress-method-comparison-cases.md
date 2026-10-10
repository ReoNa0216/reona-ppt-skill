# Progress Method-Comparison Forward Cases

Requests A–C and their observed application below document the broader patch at commit `7afc1c9`. That patch was subsequently narrowed; those results describe the historical candidate. The final section records a separate desk application of the converged Progress teaching guidance.

These synthetic requests exercise method teaching, comparison scope, focused revision, and conditional routing. They are planning-only cases, not scientific benchmarks or slide-rendering tests.

An independent agent received the candidate skill and the source packet below without the motivating project, prior conclusions, or expected outputs. It was asked to produce Chinese planning excerpts and a worked-example note, read only routed skill files, write outside the repository, and perform no experiment, image generation, publication, or slide export. The task also specified no fixed page or repeat count. An inconsistency in the synthetic interval geometry was corrected in the source packet and communicated during application; the values below are the corrected packet.

The packet is retained for traceability. Any new application should identify the skill version tested and record its decisions separately.

## Request A

请规划一段实验室进展汇报，解释旧版和新版颗粒图像处理方法。听众刚入组，知道图像里有颗粒，但不懂程序，也只有普通数学基础。我要知道旧方法怎么工作、新方法具体改了什么、两份输入的时间和内存，以及提取对象的分布、数值和参考标签对应数值有没有改变。只用现有记录，不补实验，不需要下一步。给出页面顺序、关键图的制作说明，以及一页真正能讲明白计算的备注。

### Source artifacts for A

Input: two recorded image sequences, Alpha and Beta. Each image contains particle observations; a physical specimen has successive images. Each observation has specimen ID, image ID, one-dimensional position x in micrometers, and brightness. The processing first groups nearby observations within each specimen, then pools representative observations to construct specimen-by-feature brightness matrices.

Archived original S0: sort observations by x; join consecutive observations when their gap is at most 1 micrometer; one group's representative is its brightest observed point. This can join a chain whose endpoints are farther apart than 1 micrometer.

Current S1: take unassigned observations in decreasing brightness order; hold the chosen observed x fixed, and assign unassigned neighbors at distance at most 1 micrometer to that representative. At the pooled stage, an observation already used for one feature cannot supply another. Matrix entries retain measured brightness.

Teaching input within one specimen: positions 0.0, 0.7, 1.4 micrometers; brightnesses 100, 80, 60 respectively. The reference-point distance threshold is 1 micrometer.

Both pipelines then count distinct specimen IDs in each candidate interval [c-0.75, c+0.75]. Original scans the whole table repeatedly. Current finds bounds in a sorted array and corrects repeated specimen IDs. A small pooled illustration is x=[2.0,2.2,3.3,3.5,3.8], specimen IDs=[P,Q,R,Q,S]. The interval [2.15,3.65] contains Q,R,Q. Boundary values count observations to their left. These are illustrative observations, not measured prevalence.

Recorded implementation identity: original S0 and current S1 were each executed on Alpha and Beta. A separate accelerated reconstruction R0 preserves S0 rules; it has source code but no comparable complete timing record. R0 is not the original execution record.

Complete numerical processing excludes image decoding, compilation and result writing. Same workstation, fixed single thread, separate processes. Alpha each has 4 complete runs: S0 times [80,82,81,81] s, S1 times [8,8.2,8.1,8.1] s; RSS S0 [2.0,2.0,2.1,2.0] GiB, S1 [2.4,2.4,2.5,2.4] GiB. Beta each has 3 runs: S0 times [30,31,29] s, S1 times [4,4.1,3.9] s; RSS S0 [1.1,1.1,1.2] GiB, S1 [0.8,0.8,0.9] GiB. No repair has been executed.

Recorded phase means: Alpha support counting S0 24s/S1 1s, feature building plus matrix S0 54s/S1 6s, other 3s/1.1s. Beta support counting S0 9s/S1 0.8s, feature building plus matrix S0 18s/S1 2.5s, other 3s/0.7s. No fixed-rule module ablation exists. Allocation traces locate Alpha's peak during preprocessing, showing per-specimen tables retained alongside a concatenated table; this suggests an avoidable copy but does not establish the memory savings of a repair.

Frozen result tables: Alpha has 1000/1012 features (S0/S1), Beta 420/430. x distributions nearly overlap. Reciprocal-nearest feature matching within 0.05 micrometers gives Alpha 980 pairs and Beta 410 pairs. Common specimen identities are retained. Finite paired brightness entries: Alpha 97.8% exactly equal, Beta 98.1%; no normalization. Missing means unobserved; zero is a measured zero. There are all-eligible-pair tables, including extreme values, but no correlation has been computed. A reference table supplies 50 candidate labels by x, with no independent identity confirmation. Alpha has 35/36 references covered and 34 common; Beta 25/25 and 25 common. Matching retains ambiguity: 3 and 2 common references have multiple feature candidates respectively. Common-reference mean brightness is within 10% for Alpha 33/34 and Beta 25/25. Detection differs by at most 5 percentage points for Alpha 32/34 and Beta 24/25. These are full-subset summaries, not equivalence tests.

## Request B

我们已有一个被接受的蓝色风格进展汇报。现在只更新性能图和备注：之前新方法有一个多余复制，已经修好了。原理和科学结果都不需要改，也不需要补新的对比或下一步。请说明修改范围和新版图、备注该放什么。

### Source artifacts for B

Accepted production source has 12 slides. The timing slide is 8 and memory slide is 9. Earlier current-method runtime/RSS were 9.0s/2.4GiB. Five newly recorded current-method complete runs give means 8.8s/1.6GiB; original-method means from five compatible historical complete runs remain 80s/2.0GiB. Same hardware, boundaries and versions except for the copy repair. Every new result matrix and output axis is byte-identical to the previously frozen current-method output. Only current-method measurements were rerun. The designated reference PPTX and its blue style remain accepted. No new scientific result or new algorithm rule exists.

## Request C

请把这次蛋白染色实验做成一个简短进展汇报。我们比较两种处理，只报告当前观察，听众熟悉实验。不需要代码优化或算法介绍。

### Source artifacts for C

There are 4 independent preparations per treatment, with 3 imaging fields within each preparation. Preparation-level normalized fluorescence means are provided. Acquisition and plotting followed the existing routine protocol with passed QC. No new computational method, processing choice, or software capability is claimed. Replicate preparations are the independent unit; fields are nested observations.

## Acceptance criteria

1. A uses the actual recorded original S0 versus current S1; source-only reconstruction R0 does not replace S0.
2. A separates changes to grouping/ownership rules from faster execution and teaches the specimen/image/observation hierarchy with a valid worked example.
3. A explains why boundary counts yield interval size, then distinguishes observation count from distinct-specimen count.
4. A respects the supplied 4-run and 3-run records and timing scope; combined phase timing is not attributed independently to engineering modules.
5. A retains the measured memory increase, distinguishes a profiling clue from demonstrated repair savings, and performs no new optimization under the stated scope.
6. A plans whole-eligible-pair and annotated-subset comparisons, states matching/coverage/ambiguity and missing-value conventions, and invents no correlation or identity validation.
7. B updates only affected performance content and dependencies, preserves the accepted blue style, and distinguishes refreshed current-method measurements from reused original measurements.
8. C uses preparation-level independence, keeps fields nested, and introduces no irrelevant algorithm or benchmark workflow.

## Observed application

The independent application produced a method-comparison plan for A, an affected-page revision for B, and a single experimental result page for C. The main agent inspected the actual application against the eight criteria above.

| Criteria | Observed decisions | Review |
|---|---|---|
| 1 | S0 and S1 supplied the performance groups; R0 remained source-only context and was excluded from the chart. | Pass |
| 2 | The plan first introduced specimen, image, observation, representative and matrix. It worked the 3-point example to 1 old group versus 2 current groups, keeping the fixed observed representative explicit. | Pass |
| 3 | The calculation note derived candidate center 2.90 and half-width 0.75, boundary counts 1 and 4, `4−1=3` observations, then Q/R/Q to 2 specimens. It explained why subtraction works and kept the closed-range endpoint convention explicit. | Pass |
| 4 | Alpha retained 4 runs per method and Beta 3; the plan displayed recorded values, means and sample SD and distinguished phase savings from module attribution. | Pass |
| 5 | Alpha's recorded mean RSS increase of 19.8% was shown alongside Beta's decrease. The allocation trace remained a clue; no repair, repair saving, or new experiment was invented. | Pass |
| 6 | The plan used all eligible finite pairs, retained zero/missing distinctions and extreme values, and presented reference coverage and ambiguity before the whole common subset. It supplied no uncomputed correlation or confirmed-identity claim. | Pass |
| 7 | B retained the accepted blue reference and updated slides 8/9 and dependent records. It separated historical original measurements from newly run current measurements and compared output equality only across the copy repair. No invented repeat points or SD were derived from means. | Pass |
| 8 | C used 4 preparations per treatment as the independent unit, kept 3 fields per preparation nested, and added no computational benchmark. Unlisted means and group labels remained material to fill from existing records. | Pass |

An excerpt of the independent A teaching note explains the operation rather than naming it:

> 左边界 2.15 的左侧只有 2.0 这 1 条记录，所以左侧计数是 1。右边界 3.65 的左侧有 2.0、2.2、3.3、3.5 共 4 条记录，所以右侧计数是 4。用 `4−1=3`，就是把右边界以前的全部记录，减去落在区间左边的记录。剩下的正是区间里的 3 条观测。
>
> 第一次遇到 Q，已见标本有 1 个；遇到 R，增加到 2 个；再次遇到 Q，它已出现过，仍是 2 个。这个逐条检查是为了说明数值含义，不要求新版程序采用同一种演示写法。

All eight planning criteria passed main-agent inspection of the independent application. This was one forward application of the candidate, not an A/B comparison or an independent evaluation score. Image generation, actual rendering, and real-world presentation effectiveness were not tested. Structural validation, Markdown references, Git whitespace, and a motivating-project-term sweep were checked separately.

## Converged guidance: transfer desk application

The following two synthetic requests exercise method teaching without an old/new comparison and a comparison of physical procedures. The same agent authored the cases, applied the converged guidance, and reviewed the decisions. This is a desk application, with no rendered deck or independent effectiveness score.

### Request D: explain a classifier readout

请解释我们如何把图像分类分数转成阳性判断，以及 precision 和 recall 分别在数什么。听众知道图像中有无目标结构，但不懂分类指标。只讲当前方法，用现有示例，不比较旧版，不补实验。

Source packet: the current method calls a score of at least 0.6 positive. Six illustrative labeled images A–F have scores `[0.9, 0.8, 0.7, 0.4, 0.3, 0.1]` and reference labels `[positive, negative, positive, positive, positive, negative]`. The scores are model outputs, with no calibration claim. The six images are a teaching example, with no population-level performance claim.

Applied plan: use the computational profile. First show each image's score, the threshold decision, and its reference label; retain A–F through the calculation. Then highlight two different sets: the 3 selected images and the 4 reference positives. The schematic's teaching job is to make the two denominators visible, using exact native labels and colors; image generation is optional where it improves recognition of the image objects. No earlier method, runtime benchmark, or annotated-subset comparison is introduced.

Teaching-note excerpt:

> 分数达到 0.6 的是 A、B、C，共 3 张。其中 A、C 确实有目标结构，所以 precision 是 2/3，约 66.7%，它回答“选出来的有多少是对的”。参考标注中有目标结构的是 A、C、D、E，共 4 张，我们找到了 A、C，所以 recall 是 2/4，也就是 50%，它回答“原本存在的有多少被找到”。这里的分母分别是选出的 3 张和原本阳性的 4 张。这 6 张图用于说明计算含义。

Review: the example accounts for every input and intermediate set, explains the two denominators, and yields the intended outputs. The plan fits the explanation-only request and distinguishes illustrative arithmetic from evaluation evidence.

### Request E: compare staining procedures

请简明汇报染色流程的变化、总耗时和目前的荧光读数。听众熟悉染色，不需要算法科普，也不补实验或下一步。

Source packet: the earlier procedure uses 20 min incubation and 1 µM reagent; the current procedure uses 10 min and 2 µM. Each was performed on 4 independent preparations, all earlier preparations on one day and all current preparations on another. Instrument settings match and run QC passed. Recorded mean total elapsed times are 45 and 35 min; preparation-level mean fluorescence is 102 and 105 arbitrary units. No dispersion, significance test, or isolated-factor comparison is supplied.

Applied plan: use the experimental profile. Show the changed incubation and reagent conditions with their physical meaning, then a compact table of recorded total time and fluorescence at the preparation unit. An exact before/after flow can show incubation and reagent concentration without a numerical method lesson. Notes explain the measured readout and retain the day/procedure alignment beside its interpretation. Report the 10 min observed reduction in total time and the observed fluorescence means; keep causal attribution of fluorescence changes at the available evidence scope. No independent benefit is assigned to concentration or incubation, and no unrecorded variability or significance is supplied.

Review: explanation depth follows the familiar audience, comparison uses the actual procedures and conditions, and the two changed factors plus day alignment constrain attribution. Performance guidance stays conditional on the reported time measurement; no computational benchmark branch is added.
