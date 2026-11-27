---
tags:
  - evidence
---

# Redesigning the Parts of an Antibody that Bind to a Target

> [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 原文摘录:
>
> Researchers often redesign an antibody's binding loops to help it grip its target more tightly, a process called affinity maturation. They may also want it to bind more selectively, so it's less likely to attach to similar proteins. We tested a first step toward those goals by asking our models to design new loop sequences that preserved binding to the original target.  
> 研究人员通常会重新设计抗体的结合环，以使其能更牢固地吸附目标分子。这一过程被称为亲和力成熟。他们也可能希望抗体能更具选择性地结合目标分子，从而减少与类似蛋白质的结合几率。为了实现这些目标，我们让模型设计出了新的结合环序列，从而保持与原始目标分子的结合能力。  
>
> We started with six small antibodies (VHHs) that bind to the same protein, IL-4Rα. For each antibody, we gave GPT‑6.2 its predicted three-dimensional structure and most of its amino acid sequence, leaving out the three loops that help the antibody grip its target. We asked the model to design new sequences for them. Of the 182 designs we tested, 128 (70%) showed signs of binding to IL-4Rα.  
> 我们从一个由六种小型抗体组成的组合开始，这些抗体都能与相同的蛋白质 IL-4Rα结合。对于每一种抗体，我们提供了其预测的三维结构以及大部分氨基酸序列信息，只是省略了那些有助于抗体吸附目标蛋白的三个环结构。然后我们让模型为这些抗体设计新的氨基酸序列。在测试的 182 种设计中，有 128 种（占 70%）显示出能够结合 IL-4Rα的迹象。  
>
> We then tested how precisely we could guide the model's changes to existing therapeutic antibodies. This time, we gave the model the original sequences and asked it to change about half the amino acids in each of three binding loops while keeping the rest of the sequence intact. We tested the redesigned portions of the antibodies as fragments in the lab. Of 272 fragments based on five therapeutic antibodies, 179 (66%) showed binding to the original target, PD-1 or PD-L1.  
> 然后，我们测试了能够多精确地指导模型对现有治疗性抗体进行修改。这一次，我们给了模型原始的序列，并要求它改变三个结合环中大约一半的氨基酸，同时保持其余序列不变。我们在实验室中测试了这些重新设计的抗体片段。在基于五种治疗性抗体的 272 个片段中，有 179 个（占 66%）能够与原始目标分子 PD-1 或 PD-L1 结合。  
