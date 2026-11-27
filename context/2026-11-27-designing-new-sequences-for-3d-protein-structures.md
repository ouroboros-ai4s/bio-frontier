---
tags:
  - evidence
---

# Designing New Sequences for 3D Protein Structures

> [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 原文摘录:
>
> We tested whether GPT‑6.2 could design the sequences itself. We gave it three-dimensional models of how existing minibinders fit against their targets, withheld the original amino acid sequences, and asked it to propose new ones. Specialized models helped us choose which proteins to make and test in the lab.  
> 我们测试了 GPT-6.2 能否自行设计氨基酸序列. 我们向它提供了现有小型结合蛋白与各自靶蛋白结合的三维模型, 省去小型结合蛋白的原始氨基酸序列, 让它提出新序列. 随后, 我们借助专用模型选出要在实验室中制备和测试的蛋白质.  
>
> For three targets, we started with computationally predicted structures of confirmed minibinders whose sequences Onava had collected from earlier studies. In our initial lab screens, we saw binding in 75 of 88 designs for MDM2 (85%), 26 of 42 for VEGF-A (62%), and 8 of 59 for PD-1 (14%). The amino acid sequences proposed by GPT‑6.2 also often differed significantly from the original minibinder sequences, with a median of 50% for VEGF-A, 43% for MDM2, and 15% for PD-1.  
> 针对其中 3 个靶点, 我们以已证实能够结合的现有小型结合蛋白为起点. Onava 从以往研究中收集了这些蛋白质的序列, 我们使用的是计算预测得到的结构. 在初步实验筛查中, 针对 MDM2 的 88 个设计中有 75 个检出结合 (85%), 针对 VEGF-A 的 42 个设计中有 26 个检出结合 (62%), 针对 PD-1 的 59 个设计中有 8 个检出结合 (14%). GPT-6.2 提出的序列也常与原序列有较大差异. 按不同残基位置所占的比例计算, 差异的中位数在 VEGF-A、MDM2 和 PD-1 三组中分别为 50%、43% 和 15%.  
>
> We also asked GPT‑6.2 to design new sequences for three unpublished minibinder shapes it had generated earlier: two targeting PD-L1 and one targeting IL-7Rα. A specialized model, ProteinMPNN, had already supplied one sequence for each shape, and proteins made from those sequences had shown binding in the lab. Of the 107 proteins made from GPT‑6.2's new sequences, 14 (13.1%) showed binding.  
> 我们还让 GPT-6.2 为它此前生成的 3 种尚未发表的小型结合蛋白骨架设计新序列, 其中 2 种针对 PD-L1, 1 种针对 IL-7Rα. 专用模型 ProteinMPNN 此前已为每种骨架各设计了一条序列, 按这些序列制备的蛋白质均在实验室中检出了结合. 按 GPT-6.2 的新序列制备的 107 个蛋白质中, 有 14 个检出了结合 (13.1%).  
>
> Given an unpublished structure, GPT‑6.2 had come up with two substantially different sequences that both showed signs of binding to the same target. For the same PD-L1 minibinder structure, GPT‑6.2 designed two sequences different from the original in 52 and 58 out of 90 total amino acids. The two also differed from each other at 44 positions, nearly half the sequence.  
> 给定同一个尚未发表的小型结合蛋白结构, GPT-6.2 设计了两条差异很大的序列, 按这两条序列制备的蛋白质都显示出与同一靶蛋白结合的迹象. 对于这个靶向 PD-L1 的设计, 两条新序列全长均为 90 个氨基酸, 与原序列相比分别有 52 个和 58 个位置不同. 两条新序列彼此也有 44 个位置不同, 接近全长的一半.  
>
> The unpublished structures and substantial differences in sequence give us strong evidence that GPT‑6.2's capabilities extend beyond memorization. The results also suggest we could use GPT‑6.2 to intrinsically design both a minibinder's structure and its sequence.  
> 实验使用了尚未发表的结构, 生成的序列与原序列也有较大差异, 这两点为 GPT-6.2 具备超出记忆复现的设计能力提供了有力证据. 结果还表明, 我们有望用 GPT-6.2 自行设计小型结合蛋白的三维结构和氨基酸序列.  

这次给 GPT-6.2 的输入是 **minibinder-target** **complex structure (复合物结构)**. 结构里已经给出了 minibinder 的骨架形状, 以及它相对靶蛋白的位置和朝向. GPT-6.2 要为这个给定的骨架设计一条新的 minibinder sequence. 论文明确说省去的是 minibinder 的原始序列, target 的序列是否也省去, §3.3.1 没有交代. §3.3.1, p. 22. `Specialized models helped us choose which proteins to make and test in the lab.` 对每条候选 minibinder 序列, 团队用 ESMFold2、Boltz-2 和 OpenDDE 分别预测它与靶蛋白的复合物结构, 详情见 [[2026-11-27-designing-small-proteins-that-bind-to-a-target]]. §3.3.1, p. 22 · §8.3, p. 49.

> PD-L1、IL-7Rα 用的是 GPT-6.2 先前生成的骨架. PD-1、VEGF-A、MDM2 用的是 ESMFold2 根据 Onava 此前识别的小型结合蛋白预测出的复合物结构. 这三组里, 原 minibinder 序列用于上游结构预测, 到 GPT-6.2 设计新序列时才被省去. §3.3.1, p. 22.

`For three targets, we started with computationally predicted structures of confirmed minibinders ...` 这三个 target 是 PD-1、VEGF-A 和 MDM2. 这三组用的是 Onava **从以往研究中收集的、已证实能结合的 minibinder**. 论文写 "we used ESMFold2 to predict complex structures from binders previously identified by Onava." 这次实验中, GPT-6.2 为这些复合物里的 minibinder backbone 设计新 sequence. §3.3.1, p. 22.

> 所以 VEGF-A 虽然出现在两项实验里, 两组数字对应的是不同的候选. 第一项测试的是 GPT-6.2 从头设计骨架的 46 个候选, 8 个检出结合. 第二项测试的是 GPT-6.2 根据已有骨架设计新序列的 42 个候选, 26 个检出结合. 第二项里沿用 GPT-6.2 先前设计骨架的是 PD-L1 和 IL-7Rα 两组. §2.5, p. 16 · §3.3.1, p. 22.
