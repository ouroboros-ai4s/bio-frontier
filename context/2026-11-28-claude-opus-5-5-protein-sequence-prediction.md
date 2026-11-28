---
tags:
  - source
---

# Claude was Trained on Protein Sequences at Scale

> [Claude was Trained on Protein Sequences at Scale](https://xinmingtu.cn/blog/2026/claude-opus-5-5-protein-sequences/) 原文摘录:
>
> ## Motivation
>
> Frontier LLMs have started to look good at protein tasks. Atharv Jayprakash showed GPT-6 Astra ranking SOD1 variants as well as ESM-2, and PG-LLM found the same across many proteins. Did these models learn from protein sequence databases such as UniProt, or from what is written about proteins?  
> 前沿大语言模型开始在蛋白质相关任务上表现出色. Atharv Jayprakash 发现, GPT-6 Astra 对 SOD1 变体的排序表现与 ESM-2 相当. PG-LLM 在多种蛋白质上也得出了类似结果. 这些模型的能力究竟来自 UniProt 等数据库里的蛋白质序列, 还是来自关于蛋白质的文字资料?  
>
> Famous proteins can’t tell the two apart: GFP is printed in countless papers, and most frontier models recite it. So we tested proteins that almost nobody writes about.  
> 用知名蛋白质很难区分这两种来源. 绿色荧光蛋白 (GFP) 的序列出现在无数篇论文里, 大多数前沿模型都能背出来. 因此, 我们选了几乎没人撰文研究的蛋白质来测试.  
>
> ## Method: next-amino-acid prediction on little-studied proteins
>
> We give a model the start of a protein and ask for the next amino acids. Then we ask again on a shuffled copy of the same protein. Shuffling keeps the letters and destroys their order, so the difference in accuracy measures what the model knows about the sequence itself.  
> 给模型一段蛋白质序列的开头, 让它预测接下来的氨基酸. 然后打乱同一条序列, 再做一次同样的测试. 打乱只改变氨基酸的排列顺序, 保留每种氨基酸的数量. 两种情况下的预测准确率之差, 衡量的是模型对序列本身的了解程度.  
>
> The test set is 668 bacterial and archaeal proteins from 167 Pfam families of unknown function. No family has a solved structure or more than three papers, and no protein has a close relative in UniProt. Each protein is cut at five points. At each cut the model writes the next 10 amino acids, and we score the first. Thinking is at its lowest setting.  
> 测试集包含 668 种细菌和古菌蛋白质, 来自 167 个功能未知的 Pfam 家族. 这些家族都没有已解析的结构, 相关论文也都不超过 3 篇. 测试集中的每种蛋白质在 UniProt 中都没有近缘蛋白. 每条序列选取 5 个截断位置. 在每个位置, 模型预测紧接着的 10 个氨基酸, 评分时只看第 1 个是否正确. 模型的推理强度设为最低档.  
>
> ## Results: only the latest Claude models predict them
>
> Fable 5.2 gets the next amino acid right 54% of the time on real proteins and 9% on shuffled ones. The gap is there in nearly every family, not just a few easy ones. It appears in Opus 4.7, jumps in Opus 5.5, and jumps again in Fable 5.2. GPT, Gemini and the seven open-weight models (DeepSeek V4.1 Flash, Qwen 3.8, Kimi K3.1 Pro, GLM-5.3, MiniMax M3, gpt-oss-120b and Nemotron 3 Ultra) stay near zero, even when they simply continue raw FASTA text, the way they were trained. The latest Claude models also write runs of correct residues that other models rarely manage.  
> 只有最新几代 Claude 模型能有效预测这些序列. Fable 5.2 在真实序列上的下一氨基酸预测准确率为 54%, 在打乱的序列上为 9%. 几乎每个家族都能看到这一差距, 少数容易预测的家族无法解释整体结果. 这一差距从 Opus 4.7 开始出现, 到 Opus 5.5 明显扩大, 到 Fable 5.2 又进一步扩大. GPT、Gemini 和 7 个开放权重模型 (DeepSeek V4.1 Flash、Qwen 3.8、Kimi K3.1 Pro、GLM-5.3、MiniMax M3、gpt-oss-120b 和 Nemotron 3 Ultra) 在真实序列与打乱序列上的准确率差都接近于零. 即便让它们按训练时的方式直接续写原始 FASTA 文本, 结果也是如此. 最新几代 Claude 模型还能连续预测对多个残基, 其他模型很少做到这一点.  
