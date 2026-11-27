---
tags:
  - evidence
---

# Designing Small Proteins that Bind to a Target

> [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 原文摘录:
>
> Our first laboratory experiment tested whether GPT‑6.2 could design small proteins that would bind to their intended targets. We compared computational measurements of quality against RFdiffusion, a specialized model for protein design, and found that GPT‑6.2's three-dimensional designs scored slightly lower while our latest internal models scored higher. For the lab experiment, we made proteins based on GPT‑6.2's designs and measured how strongly they bound to their targets.  
> 我们的第一个实验室实验旨在验证 GPT-6.2 是否能够设计出能够结合到目标上的小型蛋白质. 我们对比了基于计算的蛋白质设计质量指标与 RFdiffusion 模型的结果, 发现 GPT-6.2 所设计的蛋白质在三维结构方面略逊于我们的内部模型所设计的蛋白质. 在实验室实验中, 我们依据 GPT-6.2 的设计来制造蛋白质, 并测量了它们与目标的结合强度.  
>
> We gave GPT‑6.2 the three-dimensional structures of five target proteins and marked where we wanted a minibinder to attach. It then wrote code to create three-dimensional designs for potential minibinders, without using specialized protein AI models.  
> 我们向 GPT-6.2 提供了五种目标蛋白质的三维结构, 并标记了希望微型结合剂能够附着的位置. 随后, 它编写了代码来生成潜在微型结合剂的三维结构模型, 而无需使用任何专门的蛋白质 AI 模型.  
>
> To turn GPT‑6.2's three-dimensional designs into proteins we could test in the lab, we needed amino acid sequences that would fold into the proposed structures. We used a specialized AI model called SolubleMPNN to suggest sequences for each design. Other specialized protein models helped us select candidates predicted to fold as designed and bind at the intended site on the target.
> 为了将 GPT-6.2 所提出的三维结构转化为实际蛋白质结构, 我们需要在实验室中测试那些能够折叠成预期结构的氨基酸序列. 我们使用了一种名为 SolubleMPNN 的专用 AI 模型来为每种结构推荐合适的氨基酸序列. 此外, 我们还利用了其他专门的蛋白质模型来帮助筛选出那些能够按照设计意图折叠并在目标位置上结合成蛋白质的候选序列.  
>
> We tested 322 minibinders against 5 targets in the lab. Of those, 35 (10.9%) tested positive for binding to their intended target. We found 5 hits for PD-L1 (a protein some cancers use to evade the immune system), 3 for IL-7Rα, 1 for TrkA, 8 for VEGF-A and 18 for IL-17A. The original RFdiffusion study⁠(opens in a new window) reported higher hit rates, but rates depend heavily on how strictly researchers filter designs before lab validation and their definition of binding. Nevertheless, our results provide early evidence that we can turn GPT‑6.2's three-dimensional designs into proteins that bind to their intended targets in the lab.
> 我们在实验室中测试了 322 种迷你载体, 针对 5 个目标进行了实验. 结果显示, 有 35 种载体 (占 10.9%)与它们的目标蛋白发生了结合. 我们发现, 有 5 种载体能够结合 PD-L1 (某些癌症利用这种蛋白来逃避免疫系统的攻击), 3 种载体能够结合 IL-7Rα, 1 种载体能够结合 TrkA, 8 种载体能够结合 VEGF-A, 而 18 种载体能够结合 IL-17A. 最初的 RFdiffusion 研究报告的命中率更高, 但这一数值很大程度上取决于研究人员在实验室验证之前对设计方案的筛选程度, 以及他们对 "结合" 定义的理解. 不过, 我们的研究结果初步表明, 我们可以将 GPT-6.2 中的三维结构设计转化为能够在实验室中与目标蛋白结合的蛋白质.  

**Target (靶蛋白)**: 研究者事先选定要结合的 protein, 并把它的 3D structure 交给 GPT‑6.2. 论文还区分了 target 和预期结合位点, 前者是整个实验所针对的分子, 后者是研究者希望小蛋白接触的表面区域. §2.1 默认会在 prompt 中指定靶蛋白表面的热点残基来标示这个区域. *论文 §2.1, 第 6 页*.

**Small Protein (小型蛋白质)**: 这里指新设计的那一方, 论文称为 minibinder, 可译作「小型结合蛋白」. §2.1 把设计长度设为 80-120 个 amino acid residue. 这是该任务的长度设定, 论文在这里给出的是实验范围. 实验一中, GPT‑6.2 设计 backbone, SolubleMPNN 为 backbone 生成 sequence, 实验室测试的是按候选序列制成的蛋白. *论文 §2.1, 第 6 页 · 论文 §2.5, 第 14 页*.

**Bind (结合)**: 指小蛋白和靶蛋白发生可测量的物理相互作用. 论文用 **BLI (生物层干涉法)** 记录两者结合和解离时的信号, 先做单浓度筛选, 再对部分命中做多浓度复测并估计亲和力. *论文附录 B.2-B.3, 第 61-62 页*.

"基于计算的蛋白质设计质量指标与 RFdiffusion 模型的结果", 具体指用结构预测来评估 De novo 设计出来的小型结合蛋白骨架. 这一步发生在骨架生成之后. **GPT‑6.2** 和 **RFdiffusion** (RFD1 [De novo design of protein structure and function with RFdiffusion (Joseph L. Watson et al, 2023)](https://www.nature.com/articles/s41586-023-06415-8)) 负责生成骨架, 论文用同一套下游评估流程和判据给两者打分. *论文 §2.1, 第 6 页 · 图 3, 第 8 页*. 对每个提交的 backbone 用 **SolubleMPNN** 生成 8 条候选序列, 再用 **ESMFold2** 预测每条 sequence 与 target 形成的 complex structure. 只要有一条序列的预测结构同时满足以下三项:

| 判据 | 它在问什么 | 通过线 |
| --- | --- | --- |
| 靶蛋白对齐后的 binder RMSD | 把靶蛋白对齐后, 小蛋白是否仍摆在设计的位置和朝向 | < 5 Å |
| 小蛋白单独对齐后的骨架 RMSD | 把小蛋白本身对齐后, 它是否折成设计的形状 | < 3 Å |
| 靶蛋白 → 小蛋白的方向性 ipTM | 结构预测模型对这两条链之间的相对排布有多大信心 | ≥ 0.5 |

这个 backbone 就算计算通过. 论文 §8.2, 第 48–49 页
