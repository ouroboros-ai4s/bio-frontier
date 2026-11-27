---
tags:
  - evidence
---

# Designing New Sequences for 3D Protein Structures

> [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 原文摘录:
>
> We tested whether GPT‑6.2 could design the sequences itself. We gave it three-dimensional models of how existing minibinders fit against their targets, withheld the original amino acid sequences, and asked it to propose new ones. Specialized models helped us choose which proteins to make and test in the lab.  
> 我们测试了 GPT-6.2 是否能够自行设计这些序列。我们向它提供了现有迷你包装器与目标之间的三维模型，并隐藏了原始的氨基酸序列，然后让它提出新的序列。专门的模型帮助我们选择了要在实验室中制造和测试的蛋白质。  
>
> For three targets, we started with computationally predicted structures of confirmed minibinders whose sequences Onava had collected from earlier studies. In our initial lab screens, we saw binding in 75 of 88 designs for MDM2 (85%), 26 of 42 for VEGF-A (62%), and 8 of 59 for PD-1 (14%). The amino acid sequences proposed by GPT‑6.2 also often differed significantly from the original minibinder sequences, with a median of 50% for VEGF-A, 43% for MDM2, and 15% for PD-1.  
> 对于这三个靶点，我们基于之前研究中 Onava 收集到的序列数据，先对这些已确认的迷你结合蛋白的结构进行了计算预测。在初步的实验室筛选中，我们发现：在 88 种 MDM2 设计中有 75 种实现了结合，占比为 85%；在 42 种 VEGF-A 设计中，有 26 种实现了结合，占比为 62%；而在 59 种 PD-1 设计中，有 8 种实现了结合，占比为 14%。此外，GPT-6.2 预测的氨基酸序列与原始迷你结合蛋白的序列也有显著差异，其中 VEGF-A 的序列差异中位数为 50%，MDM2 为 43%，PD-1 为 15%。  
>
> We also asked GPT‑6.2 to design new sequences for three unpublished minibinder shapes it had generated earlier: two targeting PD-L1 and one targeting IL-7Rα. A specialized model, ProteinMPNN, had already supplied one sequence for each shape, and proteins made from those sequences had shown binding in the lab. Of the 107 proteins made from GPT‑6.2's new sequences, 14 (13.1%) showed binding.  
> 我们还请 GPT-6.2 为之前生成的三种尚未发表的迷你包装物结构设计新的序列：两种用于靶向 PD-L1，一种用于靶向 IL-7Rα。一个专门的模型 ProteinMPNN 已经为每种结构提供了相应的序列，从这些序列中生成的蛋白质在实验室中表现出结合活性。在由 GPT-6.2 的新序列生成的 107 种蛋白质中，有 14 种（占 13.1%）表现出结合活性。  
>
> Given an unpublished structure, GPT‑6.2 had come up with two substantially different sequences that both showed signs of binding to the same target. For the same PD-L1 minibinder structure, GPT‑6.2 designed two sequences different from the original in 52 and 58 out of 90 total amino acids. The two also differed from each other at 44 positions, nearly half the sequence.  
> 对于这样一个尚未发表的结构，GPT-6.2 提出了两个截然不同的序列，这两个序列都表现出与同一靶点的结合迹象。对于同一个 PD-L1 迷你结合剂结构，GPT-6.2 设计了两个在 90 个氨基酸中分别有 52 个和 58 个位置不同的序列。这两个序列在 44 个位置上也存在差异，几乎占了整个序列的一半。  
>
> The unpublished structures and substantial differences in sequence give us strong evidence that GPT‑6.2's capabilities extend beyond memorization. The results also suggest we could use GPT‑6.2 to intrinsically design both a minibinder's structure and its sequence.  
> 这些尚未发表的结构以及序列上的显著差异，为我们提供了有力的证据，表明 GPT-6.2 的能力远不止于记忆功能。研究结果还表明，我们可以利用 GPT-6.2 来自主设计迷你绑定器的结构及其序列。  
