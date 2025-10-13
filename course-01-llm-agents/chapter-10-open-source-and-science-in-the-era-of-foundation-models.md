# Chapter 10: Open-Source and Science in the Era of Foundation Models

## 官方资源

- 主讲人：Percy Liang（Stanford University）
- 课件：[percyliang.pdf](https://llmagents-learning.org/slides/percyliang.pdf)

## 共学计划

- 时间：2025年9月18日 21:00-22:00
- 共学地点：腾讯会议
- 主讲人：C（[Bilibili](https://space.bilibili.com/432853094)）
- 课程回放：[LLM Agents共学计划第10节：Cybench：语言模型网络安全能力评估框架](https://www.bilibili.com/video/BV1uBWuzQESN)

特别说明：我们的线上直播课并未完整讲解原课件的完整内容，只介绍了Cybench部分。感兴趣的同学可以自行学习课件中的其他内容，或直接阅读下面的内容总结。

## 核心内容


### 一、基础模型的能力越来越强，但“可访问性”在下降
- **能力飞跃**：从 GPT-2 到 GPT-4，模型性能大幅提升。
- **访问受限**：早期模型（如 GPT-2）公开论文、代码、权重，后期模型（如 GPT-4）只提供 API，不再开源。


### 二、访问级别决定研究方式（类比不同科学家）
| 访问级别     | 类比角色         | 能做什么                             |
|--------------|------------------|--------------------------------------|
| API 访问     | 认知科学家       | 只能观察输入输出，构建智能体（Agent） |
| 开放权重     | 神经科学家       | 可分析内部激活，理解模型机制         |
| 开源         | 计算机科学家     | 可修改模型结构、训练过程等一切内容   |


### 三、API 访问能做什么？—— 构建智能体（Agent）
- 把 API 当作“通用函数”：总结、验证、生成等。
- 可组合多个 API 调用，构建复杂系统（如自动写代码、做实验）。
- 例子：
  - **MLAgentBench**：让语言模型自动做机器学习实验。
  - **Cybench**：评估语言模型在网络安全任务中的能力。


### 四、开放权重能做什么？—— 深入理解模型
- 可分析模型内部结构、机制。
- 支持研究：微调、剪枝、知识蒸馏、模型合并等。
- 例子：
  - **模型独立性检测**：判断两个模型是否是独立训练，还是微调而来。
  - **对抗攻击研究**：发现模型漏洞，提升安全性。


### 五、开源模型的意义与挑战
- **定义**：不仅公开权重，还包括训练数据、代码、参数等。
- **价值**：
  - 可复现、可修改、可研究。
  - 支持教育和科研。
- **挑战**：
  - 数据版权限制（如网页数据不能公开）。
  - 训练成本高，难以完全开源。


### 六、当前研究趋势与建议
- **研究不应只依赖 API 或固定权重**。
- 应探索：
  - 小模型 + 缩放定律（scaling laws）模拟大模型行为。
  - 分布式训练，利用分散算力。
  - 数据选择、优化算法、模型架构等基础问题。
- **目标**：理解模型行为，提升效率与可控性。


### ✅ 一句话总结：
> **模型的“开放程度”决定了我们能研究多深。API 能构建应用，开放权重能深入理解，开源才能彻底掌控。研究要突破限制，回归基础，探索模型的本质。**


## 课后习题

1. **What is NOT an existing level of access for foundational models?**
A) Querying the model via an API without visibility into its internal mechanics
B) Accessing the model’s implementation, including source code and training data
C) Utilizing downloadable, pre-trained weights for customization or fine-tuning
D) Altering the model’s neural parameters directly through hardware-level adjustments
Correct Answer: D

2. **According to the speaker, what was NOT an argument for why open-source access matters?**
A) It allows for the use, study, modification, and sharing of the system for any purpose without permission requirements
B) It ensures that any agent can operate with perfect ethical alignment across all domains
C) It addresses challenges with APIs becoming deprecated, which impacts reproducibility in research
D) It provides researchers the transparency to critically examine and challenge every aspect of the model's design with unrestricted exploration
Correct Answer: B

3. **How can researchers determine if two models are independently trained?**
A) Take the cosine similarity between the weights of the two models
B) Comparing the similarity between model 1 and model 2 against the similarity between model 1 and the permutation of model 2
C) Retrain model 2 many times and compare the cosine similarities between model 1 with each of the model 2 copies
D) Analyze the output distributions of both models without considering their internal structures
Correct Answer: B

4. **What was NOT a suggestion by the speaker to address the “compute problem”?**
A) Reducing the use of GPUs to lower environmental impact
B) Constructing scaling laws to enable smaller-scale experimentation that can generalize to larger scales
C) Leveraging idle GPUs globally through decentralized compute networks
D) Advocating for increased funding for public research initiatives and infrastructure
Correct Answer: A

## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTWhwUWhwYXZzZVhW)

宣传海报：![第10节预告](../assets/LLMAgents共学计划/第10节预告.png)

总结海报：![第10节总结](../assets/LLMAgents共学计划/第10节总结.png)