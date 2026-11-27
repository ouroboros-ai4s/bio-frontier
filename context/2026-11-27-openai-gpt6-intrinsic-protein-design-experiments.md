---
tags:
  - conclusion
---

# GPT-6 Intrinsic Protein Design: Experimental Methods, Wet-Lab Validation, and Evidence

> 本文从 OpenAI 发布的 [GPT-6 Models Demonstrate Intrinsic Protein-Design Capabilities](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) 出发, 配和研究论文 [GPT-6 as a Universal Foundation Model for Protein Biology: Beyond Specialized Models](https://cdn.openai.com/pdf/gpt-6-a-universal-foundation-model-for-protein-biology.pdf) 作为主要原始证据来源, 进行阅读和分析, 旨在研究: 通用智能是否正在获得足以理解、推理和设计生物分子的内在能力, 并最终取代 AlphaFold、ESM、RFdiffusion 等面向特定任务的专业模型, 成为下一代 Protein AI 的核心基础, 并最终泛化到整个生物学智能.

OpenAI 的 blog 中讲述了三类湿实验验证:

1. **Designing Small Proteins that Bind to a Target**: GPT 负责设计三维骨架, 专用模型补齐序列并协助筛选; 湿实验检测成品能否结合靶标.
2. **Designing New Sequences for 3D Protein Structures**: 骨架已给定, GPT 负责提出新的氨基酸序列; 湿实验检测用这些新序列制成的蛋白能否结合原靶标.
3. **Redesigning the Parts of an Antibody that Bind to a Target**: GPT 只改写已有抗体的结合环序列; 湿实验检测改写后是否保留结合能力.
