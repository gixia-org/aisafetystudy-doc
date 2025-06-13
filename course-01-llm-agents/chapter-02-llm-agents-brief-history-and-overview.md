# Chapter 2: LLM Agents: Brief History and Overview

## 官方资源

- 主讲人：Shunyu Yao（OpenAI）
- 课件：[llm_agent_history.pdf](https://rdi.berkeley.edu/llm-agents-mooc/slides/llm_agent_history.pdf)

## 共学计划

- 时间：2025年6月2日 14:30-16:00
- 共学地点：腾讯会议
- 主讲人：Rain（江南大学，[Bilibili](https://space.bilibili.com/675025557)）
- 课程回放：[LLM Agents共学计划第2节：LLM Agents: Brief History and Overview](https://www.bilibili.com/video/BV1ef78zKEBD)

## 核心内容

- **智能体（Agent）定义**：指能与环境互动的智能系统，环境可为物理、数字或人类。
- **发展阶段**：
  - **文本智能体（Text Agent）**：如 ELIZA，基于规则，功能有限。
  - **LLM智能体（LLM Agent）**：利用大型语言模型执行任务，如 SayCan。
  - **推理智能体（Reasoning Agent）**：结合推理与行动能力，如 ReAct 和 AutoGPT。
- **关键技术**：
  - **ReAct框架**：融合推理与行动，提升任务处理能力。
  - **工具使用（Tool Use）**：集成搜索引擎、计算器等外部工具。
  - **记忆机制**：引入长期记忆（如 Reflexion）以增强学习与适应性。
- **未来挑战**：
  - **训练方法**：开发适用于代理的专用训练策略。
  - **接口设计**：优化代理与环境的交互方式。
  - **鲁棒性**：确保在现实应用中的稳定表现。
  - **人机协作**：提升代理与人类的协同工作能力。
  - **评估标准**：建立有效的性能评估指标。

## 课后习题

1. **What is an LLM agent?**
A) A neural network specifically designed to handle unsupervised learning tasks and generate training data for LLMs
B) A software agent that uses reinforcement learning to autonomously optimize large language models for different applications
C) A system that leverages a large language model to interpret instructions, perform tasks, and interact with its environment based on natural language inputs
D) An algorithm that primarily focuses on fine-tuning LLMs using self-supervised techniques to improve their language understanding
Correct Answer: C

2. **How does RAG (Retrieval-Augmented Generation) work?**
A) It uses an LLM to retrieve answers directly from a database without any additional data processing
B) It trains an LLM by augmenting its dataset with generated examples to improve its retrieval accuracy
C) It randomly generates text from multiple sources and combines them into a single output
D) It enhances an LLM by retrieving documents from external sources to generate more accurate responses
Correct Answer: D

3. **What is a key insight about the interaction between reasoning and acting in dynamic environments like the web?**
A) Reasoning and acting are completely independent and should be treated as such
B) Reasoning should always follow action, never preceding it
C) The best approach is a continuous cycle where reasoning informs action and action informs further reasoning
D) Actions should only occur after the entire reasoning process is complete
Correct Answer: C

4. **What is the primary distinction between long-term and short-term memory?**
A) Short-term memory stores factual knowledge, while long-term memory stores language rules
B) Long-term memory enables the model to retain information across sessions, while short-term memory does not persist over new tasks
C) Short-term memory is where models store training data, while long-term memory stores user inputs
D) Long-term memory limits a model’s ability to adapt to new data, while short-term memory enhances its adaptability
Correct Answer: B

5. **In web-based tasks, what is a potential limitation when language models do not incorporate real-time feedback from their actions?**
A) They become too dependent on user input for further actions
B) They struggle to adapt to dynamic content and user interactions
C) They tend to focus only on reasoning without taking any action
D) They perform better since feedback adds unnecessary complexity
Correct Answer: B

6. **随着LLM上下文窗口的不断扩大（例如达到千万级别），短期记忆与长期记忆的界限是否会变得更加模糊？** 请简述你的答案和理由。
参考答案：
会，但不会消除两者的差异。
考虑短期记忆与长期记忆的界限：
（1）功能性而非绝对容量： 随着LLM上下文窗口的增长，确实能容纳更多“即时”信息，这在一定程度上模糊了传统意义上基于容量的短/长期记忆划分。然而，正如姚博士在Slide 35中提到的，即使上下文窗口很大（短期记忆），它仍然是“只能追加”、“有限的”，并且“不会随着时间的推移或新任务的出现而持续存在”。它更像是一个高效的“工作台”（working memory），而非真正意义上沉淀、泛化、并能指导未来全新任务的知识库。
（2）质的差异： 真正的长期记忆（如Reflexion中的反思经验，Voyager中的技能库，或CoALA中通过改变神经网络参数实现的学习）强调的是知识的内化、结构化、和泛化能力。它不仅仅是信息的存储，更是经验的总结、技能的形成，以及对世界模型的更新。即使上下文窗口达到千万级别，如果不能有效地从中提炼和巩固知识，它本质上仍是易失的“短期”信息。姚博士的CoALA框架 (Slide 44) 提出用记忆（信息存储）、行动空间（智能体能做什么）和决策过程来表达任何智能体，这提供了一个更侧重功能而非物理界限的视角。

7. **如果一个数字智能体的“内部思考”和“外部行动”（例如在数字工具中读写信息）都表现为语言（文本）的序列操作，那么“内部行动（推理）”与“改变外部环境的行动”之间的本质区别是什么？这种区别对于我们设计和评估高度自主的、能够进行复杂长期规划的数字智能体有何指导意义？**
参考答案：
有区别。
区别在于行动的意图与影响范围。当数字智能体的所有操作都表现为语言序列时，区分这两者的关键可能在于操作的意图和直接影响范围。
（1）对于内部推理来说，其主要目的是改变智能体自身的“认知状态”。例如，形成一个计划、评估一个假设、回忆相关知识、进行自我纠正（如ReAct中的“思考”步骤，或Reflexion中的自我反思）。这些操作主要影响智能体内部的表示和后续决策，而不直接改变其定义下的“外部世界”。姚博士在Slide 32中提到推理是“智能体的内部行动”，它“改变你自己的上下文，改变你的记忆”。 
（2）对于外部行动来说，其主要目的是直接作用于智能体定义下的“外部环境”并引发该环境的状态改变。例如，调用一个API（天气查询、谷歌搜索）、在代码仓库中提交代码、在WebShop中点击购买按钮，或者在ChemCrow中提议合成一个化学物质。这些行动会产生可观测的外部结果或反馈。 
举一个“谷歌文档”的例子 (Slide 44)。智能体在谷歌文档中写入信息，其性质取决于智能体的设计和任务上下文。如果该谷歌文档是智能体规划、存储临时笔记的“草稿纸”，且其内容主要用于指导自身后续步骤，那么这更偏向于一种扩展的内部记忆、推理辅助工具。如果该谷歌文档是智能体需要交付的成果（例如撰写报告给人类用户），或者是多智能体协作中用于信息共享的媒介，那么向其写入信息就更像是一种改变外部环境的行动。
也就是说，智能体的“边界”和“外部环境”在某种程度上是设计者定义的。对于一个纯软件智能体，其“身体”就是其代码和其能访问的数字资源。
对设计高级自主智能体的指导意义包括以下三方面：
（1）清晰的认知架构：设计智能体时，需要明确其内部状态表示、推理机制、记忆模块（短期、长期、以及两者如何交互）以及行动接口。这有助于我们理解智能体的决策逻辑和行为边界。 
（2）元认知与自我调控：高级智能体需要具备元认知能力，即能够“思考自己的思考过程”，区分哪些是内部规划，哪些是需要谨慎执行的外部行动，并根据外部反馈调整内部模型。 
（3）责任与可解释性：清晰界定内部推理与外部行动，对于确定智能体行为的责任归属和提高系统的可解释性至关重要。

## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTXR0WGRCU2tKa1BR)

宣传海报：![第2节预告](../assets/LLMAgents共学计划/第2节预告.png)

总结海报：![第2节总结](../assets/LLMAgents共学计划/第2节总结.png)