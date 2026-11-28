---
tags:
  - source
---

# Watch out, AlphaFold: Claude and ChatGPT's new biology skills wow scientists  

Earlier this month, Xinming Tu set out to test what artificial-intelligence models know about proteins. Tu, a researcher at an AI biology company called Phylo in South San Francisco, California, asked large language models (LLMs) from OpenAI, Anthropic and Google to predict the sequences of obscure bacterial proteins.  
本月早些时候, Xinming Tu 着手测试 AI 模型对蛋白质了解多少. 他在加利福尼亚州南旧金山的一家 AI 生物科技公司 Phylo 担任研究员. 他让 OpenAI、Anthropic 和 Google 的大语言模型 (LLM) 预测一些鲜为人知的细菌蛋白质的序列.

He left the analysis to run overnight and woke up shocked at the results. The latest versions of Anthropic's Claude models had outperformed other LLMs, including specialized protein-language models, which are trained on vast troves of sequence data and designed for such tasks.  
他让分析跑了一整夜, 醒来后对结果大感意外. Anthropic 最新版本的 Claude 表现超过了其他语言模型, 其中包括用海量序列数据训练、专门为这类任务设计的蛋白质语言模型.

When Tu and Leo Chen, a computational biologist at Harvard Medical School in Boston, Massachusetts, shared the results in a 16 November blog post, it set off a frenzy among computational biologists to see what other protein biology LLMs such as Claude could do. For instance, Tu, Chen and others have found that the tool could perform a key step in protein-structure prediction.  
11 月 16 日, Tu 和 Leo Chen 在博客上公布了结果. Chen 是马萨诸塞州波士顿的哈佛医学院计算生物学家. 这篇文章引发了计算生物学界的一波探索, 研究人员纷纷测试 Claude 等大语言模型还能完成哪些蛋白质研究任务. 例如, Tu、Chen 等人发现, Claude 能完成蛋白质结构预测中的一个关键步骤.

And on 24 November, OpenAI announced that its latest language models had successfully designed new proteins, some of which behaved as expected when they were made and tested in the laboratory. The results hint that the latest LLMs might be gaining a sophisticated understanding of protein biology.  
11 月 24 日, OpenAI 宣布, 其最新语言模型成功设计出了新的蛋白质, 其中一些在实验室制备并测试后表现符合预期. 这些结果表明, 最新的大语言模型或许正在加深对蛋白质生物学的理解.

The research has kicked off a debate over the future of biological AI. Some scientists predict that 'general purpose' models such as Claude and ChatGPT will eventually outperform specialist tools such as AlphaFold at tasks including protein-structure prediction and design.  
这些研究引发了一场关于生物学 AI 未来走向的讨论. 一些科学家预测, Claude 和 ChatGPT 这样的"通用"模型最终会在蛋白质结构预测和设计等任务上超越 AlphaFold 等专用工具.

"We want to see a world where a scientist can just describe in natural language what they want a ChatGPT model to do, and the model can just be infinitely flexible and design exactly what the person wants," says Joy Jiao, who leads life-sciences research at OpenAI in San Francisco, California.  
"我们希望有一天, 科学家只需用自然语言描述希望 ChatGPT 做什么, 模型就能极其灵活地按要求完成设计," 在加利福尼亚州旧金山负责 OpenAI 生命科学研究的 Joy Jiao 说.

But some researchers question the extent to which LLMs are learning underlying lessons in protein biology. They suggest that some of the models' abilities could be the result of regurgitating training data.  
不过, 一些研究人员质疑大语言模型在多大程度上掌握了蛋白质生物学的基本规律. 他们认为, 模型展现的部分能力可能来自对训练数据的复述.

## Generalists versus specialists

The unveiling of AlphaFold2, Google DeepMind's blockbuster AI tool for protein-structure prediction, in 2020, launched a revolution in biological AI. There is now a vast ecosystem of software, much of it open source, for modelling different properties of proteins, such as how they interact with potential drugs, and for designing new proteins.  
2020 年, Google DeepMind 发布了备受瞩目的蛋白质结构预测工具 AlphaFold2, 推动了生物学 AI 的快速发展. 如今, 已经有大量软件可用于模拟蛋白质的各种特性, 例如蛋白质如何与候选药物相互作用, 也可用于设计新蛋白质. 其中许多软件是开源的.

Researchers have begun using LLMs to orchestrate these specialist models, but the LLMs have been used mostly as a time-saving measure, says Martin Pačesa, a structural biologist at the University of Zurich in Switzerland. "In most cases, a specialist will always perform better than a generalist for a given task," he says.  
瑞士苏黎世大学的结构生物学家 Martin Pačesa 说, 研究人员已经开始用大语言模型协调这些专用模型, 主要是为了节省时间. "多数情况下, 就某项具体任务而言, 专用模型总会比通用模型表现更好," 他说.

To see if an LLM could stand in for specialist protein-design tools, Jiao and her colleagues asked an OpenAI model called GPT-6.2 to design 3D protein structures capable of binding to five biological targets, including proteins implicated in cancer and immune conditions. After the LLMs generated the designs, the researchers used a specialist AI tool to determine a corresponding genetic sequence. Lab experiments confirmed that around 11% of designs were able to bind to their target.  
为了检验大语言模型能否替代专用的蛋白质设计工具, Jiao 和同事让 OpenAI 的 GPT-6.2 设计能与五个生物靶标结合的蛋白质三维结构. 这些靶标包括与癌症和免疫相关疾病有关的蛋白质. 大语言模型生成设计后, 研究人员用专用 AI 工具为设计确定对应的遗传序列. 实验室测试证实, 大约 11% 的设计能够与各自的靶标结合.

In other experiments, the OpenAI team showed that its LLMs could design protein sequences, redesign existing antibodies, and do other tasks typically performed by specialist tools. In some cases, the LLM performed as well as some specialist tools, and in others, such as predicting the 3D structure of proteins, it was far off. OpenAI researchers describe the work in a blog post and technical paper.  
在其他实验中, OpenAI 团队展示了其大语言模型可以设计蛋白质序列、重新设计现有抗体, 以及完成其他通常由专用工具处理的任务. 在部分任务上, 大语言模型的表现与一些专用工具相当. 在蛋白质三维结构预测等任务上, 表现仍相差很远. OpenAI 研究人员在一篇博客文章和一份技术论文中介绍了这项工作.

Jiao emphasizes that the work is a proof of principle, and that specialized AI tools were still needed for key steps. But Masatoshi Uehara, an OpenAI researcher who was part of the effort, thinks that LLMs will only get better at protein biology. "I believe the large language model can technically beat every specialized model in each capability," he says.  
Jiao 强调, 这项工作旨在验证方案的可行性, 关键步骤仍需借助专用 AI 工具. 参与这项工作的 OpenAI 研究员 Masatoshi Uehara 认为, 大语言模型在蛋白质生物学方面还会进步. "我相信, 从技术上讲, 大语言模型可以在每项能力上胜过所有专用模型," 他说.

## Total recall

Anthony Gitter, a computational biologist at Morgridge Institute for Research in Madison, Wisconsin, is excited about the possibility of LLMs having capabilities that are equal to or exceed those of specialist tools. "That might open new doors," he says, for designing and describing proteins and other biomolecules.  
Anthony Gitter 是威斯康星州麦迪逊市莫格里奇研究所的计算生物学家. 他对大语言模型有望达到乃至超越专用工具的能力感到兴奋. 他说, 这或许能为设计和描述蛋白质及其他生物分子"开辟新的可能".

But an open question is whether the LLMs are powerful enough to generalize beyond the data they were trained on, or whether their performance relies mostly on the memorization of training data, says Gitter.  
Gitter 说, 仍有一个问题悬而未决. 大语言模型能否把学到的规律应用到训练数据以外的例子, 还是说它们的表现主要依赖对训练数据的记忆?

With OpenAI's GTP-6.2 protein-design study, "readers don't have the information needed to assess whether these results are from memorization versus generalization," he adds. Another possibility is that OpenAI's GPT models have implemented open-source specialist tools, says Gitter. "We don't know."  
谈到 OpenAI 的 GPT-6.2 蛋白质设计研究, 他补充说, "读者缺少判断这些结果究竟来自记忆还是泛化所需的信息." Gitter 说, 另一种可能是 OpenAI 的 GPT 模型复现了开源专用工具的功能. "我们并不清楚."

Jiao did not say what biological data OpenAI's models were trained on. Her team attempted to rule out memorization by challenging the models to come up with sequence designs for new protein structures that were not in the training data. The GPT models also provided natural language explanations that, Jiao says, point to some understanding of the maths and physics that constrain protein structures. "It's thinking a lot about the geometry of proteins," she says.  
Jiao 没有透露 OpenAI 用了哪些生物学数据来训练模型. 为检验模型是否仅凭记忆完成任务, 她的团队要求模型为训练数据中没有的新蛋白质结构设计序列. GPT 模型还用自然语言解释了自己的设计. Jiao 认为, 这些解释表明模型对约束蛋白质结构的数学和物理规律有一定理解. "它考虑了很多蛋白质几何形态方面的问题," 她说.

Pačesa would like to see evidence that LLMs can design proteins in instances when specialist tools have failed, for example by providing expert knowledge on a specific design goal. "I do not find the reports extremely impressive because they show use cases that are better handled by specialist models," he adds.  
Pačesa 希望看到证据, 证明大语言模型能在专用工具失败的情况下设计出蛋白质, 例如通过运用与特定设计目标有关的专业知识. 他补充说, "这些报告并没有让我特别惊讶, 因为展示的用例由专用模型处理会更好."

Jan Kosinski, a structural modeller at the European Molecular Biology Laboratory in Hamburg, Germany, is open to the possibility that general-purpose LLMs could replace specialist tools in biology. But he, too, would like to know how the models were trained. "It might be a dead end, or it could be the beginnings of something bigger."  
Jan Kosinski 是德国汉堡欧洲分子生物学实验室的结构建模研究员. 他对通用大语言模型有望取代生物学专用工具持开放态度, 也想了解这些模型是如何训练的. "这条路也许走不通, 也可能是更大进展的开端."
