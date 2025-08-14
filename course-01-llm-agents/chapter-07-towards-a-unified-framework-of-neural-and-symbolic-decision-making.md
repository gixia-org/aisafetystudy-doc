# Chapter 7: Towards a unified framework of Neural and Symbolic Decision Making

## 官方资源

- 主讲人：Yuandong Tian（Meta AI）
- 课件：[Towards a unified framework of Neural and Symbolic Decision Making](https://rdi.berkeley.edu/llm-agents-mooc/slides/102824-yuandongtian.pdf)

## 共学计划

- 时间：2025年7月24日 21:00-22:00
- 共学地点：腾讯会议
- 主讲人：AntiTopQuark（[Bilibili](https://space.bilibili.com/262131733)，[GitHub](https://github.com/AntiTopQuark)）
- 课程回放：[LLM Agents共学计划第7节：Towards a unified framework of Neural and Symbolic Decision Making](https://www.bilibili.com/video/BV1ZdbmzHEjg)
- 课堂文档：[迈向神经网络和符号决策的统计框架](https://docs.qq.com/doc/DUU5ndHBpZXJNRUht)

## 核心内容

大模型在长任务的推理与规划上仍有短板，在TravelPlanner基准中，GPT‑4‑Turbo的可执行计划通过率仅约 0.6%，复杂约束与长上下文让大模型的水平迅速下降。
为了解决上述问题，我们可以使用“LLM+求解器”的方案，同时利用LLM的语义理解能力和求解器的精确规划能力。
+ 第一种路径，用LLM解析自然语言，生成规划任务，再由符号/组合优化求解器（如 MILP）求解，保证获得最优结果和性能。此外，作者提出的SurCo方法让LLM和求解器一起端到端地训练，学习一个线性代理成本，从而让求解器高效近似原始非线性问题。
+ 另一条路是“求解器喂数据给模型”。SearchFormer先模仿再超越A*，DualFormer通过随机删减轨迹同时学会“快/慢思考”，在迷宫与推箱子问题上取得更高最优率和更短的推理路径。
+ 第三种观点来自CoGO研究：简单两层网络在模加的任务上出现傅里叶基等符号化结构，说明神经网络可能收敛到可解释的代数解。

## 课后习题

1. **在 TravelPlanner 基准中，研究者没有使用哪个指标来评估大模型的旅行规划能力？**
A) Delivery Rate（是否在限定步数内输出最终计划）
B) Commonsense Constraint Pass Rate（常识约束通过率）
C) 硬件算力利用率（GPU 使用率）
D) Hard Constraint Pass Rate（硬约束通过率）
E) Final Pass Rate（全部约束满足率）
Correct Answer: C

2. **“混合系统”（Hybrid Systems）思路中，下列哪组描述最符合 To the Globe (TTG) 框架的核心流程？**（多选）
A) 自然语言 → JSON 符号表示 → MILP 求解 → 自然语言呈现
B) 直接由 LLM 生成完整行程，不做任何形式化求解
C) 用 SMT/MILP 等符号求解器保证可行性与最优性，LLM 负责翻译需求与多轮对话收集信息
D) 只用启发式算法（贪心、局部搜索）代替求解器以节省计算时间
Correct Answer: A, C

3. **SearchFormer / DualFormer 的关键改进思路包括**（多选）
A) 用 A* 生成完整搜索轨迹训练模型，再通过自举（bootstrapping）筛选更短轨迹数据继续微调
B) 在训练中对推理轨迹随机丢弃不同片段，让模型学会在信息不完整时仍产出正确解
C) 仅用最终解（solution-only）训练，可显著减少数据需求并获得更优性能
D) 通过控制 token（如 [PLAN]、[REASON]）在推理时切换“快思考”和“慢思考”模式
Correct Answer: A, B, D

4. **SurCo的核心思想是把“非线性+组合约束”的难题转化为“线性代理目标+线性组合求解器”。下列说法哪些正确？**（多选）：
A) SurCo-zero：针对单个实例在线优化线性代理成本 c^，边求解边反向传播
B) SurCo-prior：在大量实例上离线学习y 到 c^，测试时直接预测 c^ 并调用线性求解器
C) SurCo-hybrid：先用 SurCo-prior 给出初值，再用 SurCo-zero 微调，兼顾效率和最优性
D) SurCo只适用于可解析的线性目标函数，无法处理黑盒代价
Correct Answer: A, B, C

## 互动与反馈

课后习题与反馈问卷：[腾讯问卷](https://docs.qq.com/form/page/DTVZ5SVZQcmpoemhT)

宣传海报：![第7节预告](../assets/LLMAgents共学计划/第7节预告.png)

总结海报：![第7节总结](../assets/LLMAgents共学计划/第7节总结.png)