# Chapter 3: Agentic AI Frameworks: AutoGen & LlamaIndex

## 官方资源

- Agentic AI Frameworks & AutoGen
  - 主讲人：Chi Wang（AutoGen-AI）
  - 课件：[llm_agent_history.pdf](https://rdi.berkeley.edu/llm-agents-mooc/slides/llm_agent_history.pdf)
- Building a Multimodal Knowledge Assistant
  - 主讲人：Jerry Liu（LlamaIndex）
  - 课件：[MKA.pdf](https://rdi.berkeley.edu/llm-agents-mooc/slides/MKA.pdf)

## 共学计划

- 时间：2025年6月12日 21:00-22:30
- 共学地点：腾讯会议
- 主讲人：晨夏梦醒（[Bilibili](https://space.bilibili.com/89566407)，[GitHub](https://github.com/xiaomo1128)）
- 课程回放：[LLM Agents共学计划第3节：Agentic AI Frameworks: Autogen & LlamaIndex
](https://www.bilibili.com/video/BV18zM2zQEhp)
- 主讲人整理的资料：[imagined-space/llm-agent-chapter-3](https://github.com/imagined-space/llm-agent-chapter-3)

## 核心内容

Agentic AI框架三大核心

- **多智能体协同 (Multi-Agent Collaboration)**：将复杂任务分解，让多个专用AI智能体通过对话协作，自动完成规划与执行。
- **推理-行动循环 (Reasoning-Action Loop)**：赋予AI自主规划、调用工具（代码、API）、并根据结果自我反思的循环能力，突破传统“输入-输出”限制。
- **系统化编排 (Systematic Orchestration)**：无缝整合 大模型（LLM）、外部工具（Tools）和人类专家（Human）三要素，通过框架统一调度，实现能力融合与放大。

## 课后习题

1. **What is the primary function of LlamaIndex?**
A) It serves as a framework to preprocess large datasets for language model training
B) It acts as an interface between large language models and external data sources to structure and query data
C) It finetunes LLMs using reinforcement learning to improve task-specific performance
D) It provides visualization tools to monitor the performance and accuracy of LLMs during training
Correct Answer: B

2. **How do multimodal knowledge assistants enhance interaction with LLMs?**
A) They integrate different data types like text, images, and audio to provide more comprehensive responses
B) They train multiple language models simultaneously to handle diverse natural language queries
C) They use multimodal transformers to optimize LLMs for specific visual understanding tasks
D) They create separate pipelines for text and image-based queries to ensure accurate response generation
Correct Answer: A

3. **What is the key difference between Unconstrained and Constrained flows in Agentic Retrieval-Augmented Generation (RAG)?**
A) Unconstrained flows allow the model to more freely generate responses without relying on retrieved documents, while constrained flows are more reliable because they limit the model to only use retrieved information in its responses
B) Unconstrained flows use multiple external data sources, whereas constrained flows rely solely on internal datasets for generating responses
C) In unconstrained flows, the retrieval process is skipped entirely, whereas constrained flows force retrieval before generating any response
D) Unconstrained flows prioritize accuracy, while constrained flows focus on generating faster responses by bypassing external data
Correct Answer: A

4. **What are the primary benefits of an Agentic AI Framework?**
A) It enables AI models to independently perform complex tasks without requiring user prompts, increasing automation and efficiency
B) It improves model performance by reducing computational complexity during training
C) It allows AI systems to autonomously plan, retrieve, and act based on goals, enhancing adaptability and decision-making
D) It focuses on reducing biases in language models through supervised learning techniques memory limits a model’s ability to adapt to new data, while short-term memory enhances its adaptability
Correct Answer: C

5. **What is the main purpose of AutoGen in AI systems?**
A) It provides real-time fine-tuning of AI models based on user feedback to improve performance on specific tasks
B) It enables the automatic generation of training datasets for language models by using pre-existing knowledge bases
C) It facilitates the orchestration of multiple LLM agents to collaborate, communicate, and perform complex tasks autonomously
D) It enhances multimodal AI systems by integrating text and image data to generate richer responses
Correct Answer: C

6. **除了AutoGen和LlamaIndex，你还听说过哪些智能体框架？**
参考答案：
    - 代码框架：
      - [LangChain](https://www.langchain.com/)
      - [MetaGPT](https://mgx.dev/)
      - [Mastra](https://mastra.ai/)
      - [CrewAI](https://www.crewai.com/)
   - 低代码框架：
      - [Dify](https://dify.ai/)
      - [扣子](https://www.coze.cn/)
      - [ComfyUI](https://www.comfy.org/)

7. **请用一句话解释为什么我们需要用智能体框架。**
参考答案：
    - 智能体框架将构建AI智能体所需的复杂核心功能（如记忆、规划、工具调用）封装为标准化模块，极大的简化了开发过程，使我们能更快、更轻松地创建出强大的自主AI应用。

## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTVFidG5RVW16RnZ3)

宣传海报：![第3节预告](../assets/LLMAgents共学计划/第3节预告.png)

总结海报：![第3节总结](../assets/LLMAgents共学计划/第3节总结.png)