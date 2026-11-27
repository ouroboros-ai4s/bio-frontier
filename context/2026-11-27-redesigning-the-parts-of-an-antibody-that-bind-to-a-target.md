---
tags:
  - evidence
---

# Redesigning the Parts of an Antibody that Bind to a Target

> [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 原文摘录:
>
> Researchers often redesign an antibody's binding loops to help it grip its target more tightly, a process called affinity maturation. They may also want it to bind more selectively, so it's less likely to attach to similar proteins. We tested a first step toward those goals by asking our models to design new loop sequences that preserved binding to the original target.  
> 研究人员常通过重新设计抗体的结合环来提高它对靶标的亲和力, 这一过程称为亲和力成熟. 他们有时也会提高抗体的结合选择性, 以减少它与相似蛋白质结合的可能性. 作为迈向这些目标的第一步, 我们让模型设计新的结合环序列, 并检验改造后的抗体能否保留与原靶标结合的能力.  
>
> We started with six small antibodies (VHHs) that bind to the same protein, IL-4Rα. For each antibody, we gave GPT‑6.2 its predicted three-dimensional structure and most of its amino acid sequence, leaving out the three loops that help the antibody grip its target. We asked the model to design new sequences for them. Of the 182 designs we tested, 128 (70%) showed signs of binding to IL-4Rα.  
> 我们选取了 6 种都能与 IL-4Rα 结合的单域抗体 (VHH). 对每种抗体, 我们向 GPT-6.2 提供预测的三维结构和大部分氨基酸序列, 隐去三个结合环的原序列, 让模型为这三个环设计新序列. 在测试的 182 个设计中, 有 128 个 (70%) 显示出与 IL-4Rα 结合的迹象.  
>
> We then tested how precisely we could guide the model's changes to existing therapeutic antibodies. This time, we gave the model the original sequences and asked it to change about half the amino acids in each of three binding loops while keeping the rest of the sequence intact. We tested the redesigned portions of the antibodies as fragments in the lab. Of 272 fragments based on five therapeutic antibodies, 179 (66%) showed binding to the original target, PD-1 or PD-L1.  
> 随后, 我们测试了能在多大程度上精确控制模型对现有治疗性抗体的改动. 这次我们提供原始序列, 要求模型在三个结合环中各改变约一半的氨基酸, 其余序列保持不变. 我们将重新设计的部分制成抗体片段, 并在实验室中测试其结合能力. 在基于 5 种治疗性抗体设计的 272 个片段中, 有 179 个 (66%) 检出与各自原来的靶标 PD-1 或 PD-L1 结合.  

**Affinity Maturation (亲和力成熟)**: 指提高 antibody 对同一 target 的结合亲和力的过程. 在抗体工程中, 可以通过改变结合环的序列来实现. 在相同测量条件下, 改造后的抗体如果具有更低的解离常数 $K_D$, 就说明它与靶标结合得更紧.  
**Binding Selectivity (结合选择性)**: 指 antibody 有多偏好与预定 target binding, 相比之下与其他分子的结合有多弱. 判断选择性需要比较同一个抗体对不同蛋白的结合表现.  
**Loop Sequence (环序列)**: 指构成一段抗体结合环的 amino acid 按顺序排列得到的序列. 这里的结合环指 **CDR (互补决定区)**.**「环序列」**描述每个位置是什么氨基酸, **「环结构」**描述这些残基在三维空间中怎么排布.
**VHH (单域抗体)**: VHH 是骆驼科动物的重链抗体中负责识别抗原的可变结构域, 也常称为纳米抗体 (nanobody). 单个 VHH 就能独立结合抗原, 其结合表面主要由 CDR1、CDR2 和 CDR3 三个环组成.

这里第一项 VHH 实验隐藏 CDR1、CDR2 和 CDR3 的原序列, 让 GPT-6.2 为三个环各设计一条新序列, 测试与 IL-4Rα 的结合; 后一项治疗性抗体实验提供原序列, 要求 GPT-6.2 在三个结合环中各替换约一半的 residue, 并保留环外序列, 随后用改造后的抗体片段测试是否仍能结合各自原来的靶标 PD-1 或 PD-L1. §3.3.3, pp. 29-30.

> 5 种原始 antibody 分别贡献了 $92 + 92 + 31 + 54 + 3 = 272$ 个受测变体.
