---
tags:
  - evidence
---

# OpenAI GPT-6 蛋白质设计研究的外部反应

OpenAI 于 2026 年 11 月 24 日发布 GPT-6 蛋白质设计研究. 早期公开讨论中, 学界关注任务难度和训练数据, 业界媒体关注研发周期和成本, 开发者社区则追问 GPT 在各项实验里实际产出了什么. [OpenAI 博客](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) · [OpenAI 预印本](https://cdn.openai.com/pdf/gpt-6-a-universal-foundation-model-for-protein-biology.pdf)

## 学界

- **Anthony Gitter, Morgridge Institute for Research.** 他在《Nature》采访中认为, 公开信息不足以判断结果有多少来自训练数据记忆, 有多少来自对新问题的泛化. 在少量未公开骨架上生成明显不同的序列, 削弱了直接复述原序列的解释. 要判断模型是否借用了训练中见过的近邻, 还需要知道训练数据与测试对象之间的相似程度. [《Nature》采访](https://www.nature.com/articles/d41586-026-03836-z) · [DongA Science 的具名转述](https://www.dongascience.com/en/news/81068) · [*§3.3.1, p. 22*](https://cdn.openai.com/pdf/gpt-6-a-universal-foundation-model-for-protein-biology.pdf#page=22)
- **Martin Pačesa, 苏黎世大学结构生物学研究者.** 他在同篇报道里提出, 更有说服力的证据是通用模型能解决现有专用模型做不好的蛋白设计任务. 他的评价针对的是这次展示的任务难度. 他也是 SolubleMPNN 对应论文的共同作者. [《Nature》采访](https://www.nature.com/articles/d41586-026-03836-z) · [DongA Science 的具名转述](https://www.dongascience.com/en/news/81068) · [Computational design of soluble and functional membrane protein analogues (Casper A. Goverde et al, 2024)](https://www.nature.com/articles/s41586-024-07601-y)
- **Xinming Tu 和 Leo Chen 的同期研究.** 两人对通用模型做了蛋白序列预测测试, 并公开了代码、数据和模型回复, 提供了一个可供外部检查的评估实例. 他们测试的是给定部分序列后预测后续氨基酸, 与 OpenAI 的结合蛋白湿实验是不同的任务. [Tu 和 Chen 的原文](https://xinmingtu.cn/blog/2026/claude-opus-5-5-protein-sequences/)

## 业界

- **研发周期和成本.** TechRepublic 从采购和项目周期出发, 指出如果项目主要卡在实验室, 加快设计也未必能明显缩短整体周期. T4 Intelligence 主张以整个研发项目为比较单位, 衡量找到一个有用分子需要多久、失败实验花多少钱、专家需要投入多少. OpenAI 报告的是筛选后候选的结合结果, 项目总成本和总耗时仍待比较. [TechRepublic](https://www.techrepublic.com/article/news-gpt-6-2-protein-design-biotech-it/) · [T4 Intelligence](https://t4intelligence.substack.com/p/protein-design-is-becoming-a-general)
- **自然语言约束与工作流程.** AlphaSignal 和 Unite.AI 关注通用模型能否在多个设计环节理解研究人员用自然语言提出的具体约束. The Terminal 更关注现有流程的分工, 指出专用模型仍参与筛选. 这些报道关注的是不同环节, 即 GPT 提出候选设计的灵活性, 以及结构预测和验证在实际流程中的作用. [AlphaSignal](https://alphasignal.ai/news/openai-s-gpt-6-2-designs-real-proteins-that-bind-drug-targets-in-the-lab) · [Unite.AI](https://www.unite.ai/openai-reports-gpt-6-designs-proteins-with-reasoning-and-code/) · [The Terminal](https://theterminal.space/ai/openai-gpt-6-protein-binders-35-of-322-onava)
- **产业采用与独立复现.** 多篇报道仍依赖 OpenAI 和合作方 Onava 的同一批实验结果. 截至 2026 年 11 月 28 日, 尚未找到非合作药企公开披露采用这套流程后的项目业绩, 或外部实验室独立复现这批候选的报告. [CASRAI](https://casrai.org/news/openai-gpt-6-protein-design-preprint-wet-lab-binders-2026) · [TechQuire](https://tech-quire.com/articles/openai-gpt-protein-design-lab-binding/) · [OpenAI 预印本](https://cdn.openai.com/pdf/gpt-6-a-universal-foundation-model-for-protein-biology.pdf)

## 社区与媒体

- **Hacker News.** 主帖在查看时有 356 分, 评论树有 97 条记录. 有人把模型能自己写代码推进设计视为关键进展, 有人追问第一项实验里 GPT 交付的是骨架还是序列. 一名自述曾在 Baker Lab 攻读博士的评论者看好这一方向, 同时质疑训练与测试数据的隔离和任务难度. 另一名自述从事药物研发的评论者则追问, 即使更容易找到能结合的分子, 后续怎样确认它对疾病有用. 两人的背景均来自评论者自述. [主帖](https://news.ycombinator.com/item?id=50634658) · [代码能力](https://news.ycombinator.com/item?id=50635755) · [骨架和序列](https://news.ycombinator.com/item?id=50635782) · [测试集与任务难度](https://news.ycombinator.com/item?id=50636511) · [药物研发](https://news.ycombinator.com/item?id=50639681)
- **中文报道.** 搜狐转载的文章以「AlphaFold 危矣」为题, 凤凰网科技则强调 OpenAI 报告的 10.9% 低于 RFdiffusion 原研究报告的 19%. 前一标题涉及两个不同任务, 即设计新骨架和从序列预测完整结构. 后一比较需要核对靶点、送检前的筛选和结合阳性判据. [搜狐转载](https://m.sohu.com/a/1106316962_354973) · [凤凰网科技](https://original.ifeng.com/c/8yKUsH5Hmk1) · [OpenAI 博客](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) · [De novo design of protein structure and function with RFdiffusion (Joseph L. Watson et al, 2023)](https://www.nature.com/articles/s41586-023-06415-8)
- **日语报道.** GIGAZINE 讨论了通用模型通过推理和编程生成蛋白设计的能力, 并转述了实验室的结合结果. 报道同时引用 OpenAI 的发布和《Nature》的采访. [GIGAZINE](https://gigazine.net/news/20261125-openai-gpt-6-protein/) · [《Nature》](https://www.nature.com/articles/d41586-026-03836-z)
- **生物安全.** Hacker News 和媒体提及了双重用途风险. 目前能追溯到的公开讨论以一般性评论和 OpenAI 自己的风险评估为主. OpenAI 在博客中表示, 会依据其 Preparedness Framework 评估风险和测试防护措施. [Hacker News 讨论](https://news.ycombinator.com/item?id=50634658) · [TechQuire](https://tech-quire.com/articles/openai-gpt-protein-design-lab-binding/) · [OpenAI 博客](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/)
