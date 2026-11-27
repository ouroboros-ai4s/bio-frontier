---
tags:
  - conclusion
---

# GPT-6 Intrinsic Protein Design: Experimental Methods, Wet-Lab Validation, and Evidence

> 本文从 OpenAI **2026.11.24** 基于 **GPT-6.2** 的研究, 发布的 [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 出发, 配和研究论文 [GPT-6 as a Universal Foundation Model for Protein Biology: Beyond Specialized Models](https://cdn.openai.com/pdf/gpt-6-a-universal-foundation-model-for-protein-biology.pdf) 作为主要原始证据来源, 进行阅读和分析, 旨在研究: **通用智能是否正在获得足以理解、推理和设计生物分子的内在能力, 并最终取代 AlphaFold、ESM、RFdiffusion 等面向特定任务的专业模型, 成为下一代生物学智能的核心基础**.

OpenAI 讲述了三类 **wet-lab validation (湿实验验证)**:

1. **Designing Small Proteins that Bind to a Target**: GPT 负责设计三维骨架, 专用模型补齐序列并协助筛选; wet-lab 检测成品能否结合靶标.
2. **Designing New Sequences for 3D Protein Structures**: 骨架已给定, GPT 负责提出新的氨基酸序列; wet-lab 检测用这些新序列制成的蛋白能否结合原靶标.
3. **Redesigning the Parts of an Antibody that Bind to a Target**: GPT 只改写已有抗体的结合环序列; wet-lab 检测改写后是否保留结合能力.

## Designing Small Proteins that Bind to a Target

[[2026-11-27-designing-small-proteins-that-bind-to-a-target]] 笔记梳理了 OpenAI 的 **minibinder 设计实验**. 研究人员给 GPT-6.2 提供 **5 种靶蛋白的三维结构**, 并标出**希望结合的热点残基位置**. GPT-6.2 **编写脚本生成 minibinder 的三维骨架**, **SolubleMPNN** 再为每个骨架设计 8 条候选氨基酸序列. 计算评估用同一套判据比较 GPT-6.2 和 RFdiffusion 的设计, 检查小蛋白的折叠形状、相对靶蛋白的结合姿态和预测界面的可信度. 湿实验前, 团队用 **ESMFold2、Boltz-2 和 OpenDDE 筛选候选**, 最终用 **BLI** 测试了 322 个, 其中 35 个检出结合, **命中率为 10.9%**. 这个比例取决于哪些候选被选去测, 以及实验用什么标准判定结合阳性.

## Designing New Sequences for 3D Protein Structures

[[2026-11-27-designing-new-sequences-for-3d-protein-structures]] 笔记梳理了 OpenAI 的 **minibinder inverse-folding 实验**. 研究人员给 GPT-6.2 提供 **minibinder 与靶蛋白的复合物骨架**, 隐去原 minibinder 序列, 让它根据骨架设计新序列. 输入骨架来自两处, 一组由 ESMFold2 根据已有结合蛋白预测, 另一组是 GPT-6.2 此前设计的 3 个未公开骨架. 团队用 ESMFold2、Boltz-2 和 OpenDDE 筛选候选, 再用 BLI 测试结合. 给定 **同一个未公开的 minibinder backbone**, GPT-6.2 设计出两条与原序列差异较大、彼此也明显不同的新序列.

## Redesigning the Parts of an Antibody that Bind to a Target

[[2026-11-27-redesigning-the-parts-of-an-antibody-that-bind-to-a-target]] 笔记梳理了 OpenAI 的 **抗体结合环重设计实验**. 研究人员先隐去 VHH 的原始重链互补决定区 (HCDR) 序列, 让 GPT-6.2 根据抗原序列和抗体框架为这些环设计新序列. 随后, 他们提供治疗性抗体的原始序列, 要求模型按指定幅度修改 HCDR, 并保留环外序列. 两项实验都在实验室中测试了改造后的抗体片段能否继续结合各自的原靶标.
