# Chapter 5: Agents for Software Development

## 官方资源

- 主讲人：Graham Neubig（CMU）
- 课件：[neubig24softwareagents.pdf](https://rdi.berkeley.edu/llm-agents-mooc/slides/neubig24softwareagents.pdf)

## 共学计划

- 时间：2025年7月10日 21:00-22:30
- 共学地点：腾讯会议
- 主讲人：邹一帆（[Bilibili](https://space.bilibili.com/614807456)）
- 课程回放：[LLM Agents共学计划第5节：Agents for Software Development](https://www.bilibili.com/video/BV1q6uKzQEL2)

## 核心内容

**软件开发智能体的六大关键点**
1. **定义环境**：AI智能体需接入和理解多种真实开发环境，以支持任务执行与上下文感知。
2. **设计观察/动作空间**：设计合理的观察（observation）与动作（action）空间是实现有效交互和任务控制的基础。
3. **代码生成**：高质量的代码生成需同时满足语法正确性、语义合理性和可执行性。
4. **文件定位**：智能体需具备准确的文件与函数定位能力，以减少无效搜索和误修改风险。
5. **计划与错误修复**：具备任务分解、执行规划及异常处理能力是实现多步骤自动化的关键。
6. **安全**：确保智能体系统在受控范围内运行，防止误操作和潜在滥用，是落地部署的前提。

## 课后习题

1. **What is not an effective method of file localization?**
A) Creating a map of the repository structure and using it to guide the agent
B) Offloading the task to the user, allowing experienced users to specify which files to use
C) Using search tools to assist the agent in finding relevant files within the repository
D) Manually scanning through every file in the project directory to find relevant files
Correct Answer: D

2. **What does Pass@K measure?**
A) After generating K examples, whether there is at least one of them that satisfies the code specification
B) After generating K examples, calculate the average length of the generated outputs to assess their quality
C) After generating K examples, evaluate their complexity using a predefined scoring rubric to determine how many are valid
D) After generating K examples, count the number of unique outputs produced to measure the diversity of the generated responses
Correct Answer: A

3. **Why is data leakage a big problem when evaluating software agents?**
A) It can lead to overly optimistic performance metrics that do not reflect true generalization
B) It makes the code harder to read and maintain by increasing complexity
C) It prevents agents to learn from a broader range of data, hurting their performance on all tasks
D) It decreases the speed of training and evaluation processes, leading to slower model deployment
Correct Answer: A

4. **What is an example of how not to mitigate safety concerns of coding agents?**
A) Review actions after they have been executed to detect and address any potential security issues or unauthorized activities
B) Use automated code formatting tools to ensure that code generation is neatly organized and is easy to read in order to reduce the likelihood of human error
C) Restricting permissions and managing access tokens to ensure that users and applications only have the minimal level of access necessary
D) Isolate the agent’s execution environment to prevent potentially harmful actions from affecting the broader system
Correct Answer: B

5. **What is “code infilling”?**
A) A technique used to convert comments in code into fully functional methods
B) The method of testing code by filling it with random values to check for errors
C) The process of automatically generating the missing parts of code based on the surrounding context
D) The process of refactoring existing code to improve its readability and maintainability
Correct Answer: C

6. **代码智能体（Code Agents）相较于传统代码补全工具（如 Copilot）有哪些核心能力上的提升？**
参考答案：
代码智能体不仅能生成代码，还能自主完成包括任务理解、文件定位、代码编辑、测试执行和 PR 提交在内的完整开发流程。相较于传统补全工具，智能体具备更强的自主性、多步骤规划能力以及与开发环境的深度集成，能够模拟人类工程师的操作过程，完成复杂的软件工程任务。

7. **为什么构建一个软件开发用的AI智能体不像普通聊天机器人那么简单？**
参考答案：
因为软件开发不仅是“对话”，还需要看懂代码、操作文件、运行命令、修复错误并通过测试。一个开发智能体必须具备多种技能，包括理解任务、修改代码、处理出错情况，还要保证不做危险操作。这些都远比普通的问答复杂得多。

8. **你用过哪些代码智能体？体验如何？你认为有哪些不足？**
参考答案：
我用过GitHub Copilot和Trae，前者属于传统的代码补全AI，后者属于代码智能体。显然，Trae的体验比Copilot好很多，它可以全流程地替我完成编码任务。当我需要开发一个功能时，只需要用自然语言讲清楚需求，Trae就可以自动定位到需要修改的代码，提出修改建议，并在我的批准下完成修改。不过，它仍存在一些不足，对于某些复杂的代码，它的修改偶尔会引入bug，需要人工介入再次修改才行。如果代码智能体可以加入自动测试的功能，应该就可以避免很多这类错误。

## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTWd0Z2RuVGpwZmx3)

宣传海报：![第5节预告](../assets/LLMAgents共学计划/第5节预告.png)

总结海报：![第5节总结](../assets/LLMAgents共学计划/第5节总结.png)