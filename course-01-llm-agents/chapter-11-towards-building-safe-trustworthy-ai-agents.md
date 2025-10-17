# Chapter 11: Towards Building Safe & Trustworthy AI Agents

## 官方资源

- 主讲人：Dawn Song（UC Berkerley）
- 课件：[dawn-agent-safety.pdf](https://rdi.berkeley.edu/llm-agents/assets/dawn-agent-safety.pdf)

## 共学计划

- 时间：2025年10月16日 21:00-22:30
- 共学地点：腾讯会议
- 主讲人：王金戈（[Bilibili](https://space.bilibili.com/69217382)）
- 课程回放：[LLM Agents共学计划第11节：Towards Building Safe & Trustworthy AI Agents](https://www.bilibili.com/video/BV1CXWCzuE85/)

## 核心内容

+ **AI Safety vs AI Security**
  + *Safety* 是防止 AI 对外部环境造成伤害
  + *Security* 是保护 AI 系统本身不被恶意攻击利用

+ **三类AI Risk**
  + 滥用（Misuse/Malicious Use）：虚假信息、诈骗、网络攻击、生物武器
  + 故障（Malfunction）：偏见、幻觉、失控
  + 系统性风险（Systemic Risks）：大规模失业、环境破坏

+ **Agentic AI 的攻击面更广**
  + 作为行动者的代理（agent）集成感知、规划、工具调用、反馈环节，整个系统较纯 LLM 更复杂、更易受攻击
  + 常见攻击形式包括 Prompt Injection（直接/间接）、SQL 注入、远程代码执行（RCE）、后门、数据中毒 / 知识库污染等

* **防御原则与机制**
  + **Defense-in-Depth**（深度防御）：多层防线组合使用
  + **最小权限 / 权限隔离**：每个子模块只拥有完成其职能所必需的权限
  + **安全设计 / 可验证性**：从设计阶段保证安全属性、尽可能采用形式化验证（formal verification）


## 课后习题

1. **What is the difference between AI Safety and AI Security?**
A) AI Safety focuses on preventing external actors from attacking the system, while AI Security ensures the system makes ethical decisions
B) AI Safety involves preventing the system from causing harm to the environment, whereas AI Security focuses on protecting the system from external threats
C) AI Safety addresses system robustness, and AI Security deals with ensuring fairness in AI models
D) AI Safety is about preventing technical failures, while AI Security is about preventing data breaches
Correct Answer: B

2. **How are adversarial examples designed to fool deep learning image classifiers?**
A) By increasing the resolution of the image to overwhelm the model’s ability to process fine details
B) By training the model on mislabeled data to reduce its classification accuracy over time
C) By introducing subtle, imperceptible changes to an image that significantly alter the model’s prediction
D) By replacing parts of the image with entirely different objects to confuse the classifier
Correct Answer: C

3. **How is LLM Agent Safety different from typical LLM Safety?**
A) LLM Agent Safety involves safeguarding actions that an agent can take in the real world, whereas typical LLM Safety is concerned with the content of the model's outputs
B) LLM Agent Safety focuses on preventing harmful text generation, while typical LLM Safety addresses ethical biases in model training
C) LLM Agent Safety deals with securing the model from external attacks, while typical LLM Safety focuses on user privacy
D) LLM Agent Safety monitors the accuracy of generated outputs, while typical LLM Safety ensures models are unbiased
Correct Answer: A

5. **Explain the asymmetry between Attacks and Defenses in AI Safety?**
A) Attacks are more difficult to execute but have fewer consequences, while defenses are simple to implement but resource-intensive
B) Attacks focus on using existing security mechanisms, while defenses create entirely new systems to prevent exploitation
C) Attacks target AI models with low-risk consequences, while defenses are more focused on theoretical vulnerabilities
D) Attacks have a high tolerance for failure and can be easily scaled, while defenses require reliability and are resource-heavy with low tolerance for failure
Correct Answer: D


## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTUtpSHd3RVdkV29V)

宣传海报：![第11节预告](../assets/LLMAgents共学计划/第11节预告.png)

总结海报：![第11节总结](../assets/LLMAgents共学计划/第11节总结.png)