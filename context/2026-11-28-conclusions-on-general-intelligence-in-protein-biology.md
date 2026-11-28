---
tags:
  - conclusion
---

# Conclusion on General Intelligence in Protein Biology

1. **部分研究者看好「general intelligence 补足 specialist tools 的能力缺口」.** General models 或许能利用更广泛的知识和推理能力, 处理 specialist models 训练较少覆盖的任务. 现有结果支持继续探索这个方向, 但在明确训练数据隔离、使用可比基线的条件下, 替代专用工具仍是预期. [[2026-11-28-watch-out-alphafold-claude-and-chatgpt-s-new-biology-skills-wow-scientists]]

2. **现有证据无法判断 general intelligence 的 protein 能力「有多少来自记忆, 有多少来自泛化」.** Claude 在多个家族的真实序列上优于打乱序列, 在作者估计晚于训练截止日期公开的样本上也有优势. GPT-6.2 则能为未公开的骨架设计与原序列明显不同的新序列. 这些结果削弱了模型只是背诵原序列的解释. 但两家的训练数据都无法独立核查, 模型是否见过测试序列本身或相似的序列、结构, 以及这些已有信息对结果贡献了多少, 仍然不清楚.
[[2026-11-28-claude-opus-5-5-protein-sequence-prediction]] · [[2026-11-28-conclusions-on-openai-gpt6-protein-design]]

3. **当前主流做法依然是「general intelligence 与 specialist tools 协作」.** Nature 报道的常见用法是让通用模型协调专用工具, 节省操作时间. OpenAI 的实验也展示了通用模型直接提出设计, 部分实验仍由专用模型参与序列生成和候选筛选. 湿实验命中率以送检候选为分母, 应理解为整套流程筛选后的结合结果. [[2026-11-28-conclusions-on-openai-gpt6-protein-design]]

4. **潜在范式转变可能是把工作从 GPU 计算的「compute intensive」转为 API 调用的「token intensive」.** 如果通用模型能在设计质量和吞吐量相当的条件下接手算力密集的步骤, 团队就能减少 GPU 采购和维护、专用模型部署和更新的开销. 是否真的更省, 要按每个合格候选的总成本算, 把批量生成、重试和实验验证都计入. 如果项目主要卡在验证环节, 计算成本下降也未必能明显缩短研发周期. [[2026-11-28-inference-on-openai-gpt6-protein-design]]
