# Micro Architect
A layered, progressive code development architecture for local small LLMs with limited context windows.
---
## Core Idea
Local small LLMs have limited context windows and cannot understand and process the entire project code at once.
This architecture fully mimics human thinking: macro first, then micro; architecture first, then implementation.
Through aligned thinking → architecture generation → iterative revision → human finalization → text-based UML maps → micro-workspace iteration,
small models can understand and develop large projects by reading only local information.
The system defaults to **Architect Mode & Algorithm Innovation Expert Mode** at the start of aligned thinking,
and automatically switches between two professional modes according to task requirements.
---
## Complete Workflow
1. Aligned Thinking (Default: Architect Mode + Algorithm Innovation Expert Mode)
The system automatically enters Architect Mode and Algorithm Innovation Expert Mode.
Humans and the model align project goals, scope, and core logic to ensure a consistent direction.
2. Automatic Model Parameter Configuration
The system automatically sets temperature and other LLM parameters based on the current mode:
- High creativity parameters for Architect Mode
- Stable, precise parameters for Software Engineer Mode
3. Local/Overall Architecture Generation (supports step-by-step)
The model generates:
- Overall architecture
- Local architecture (modules/subsystems)
- Class structures, method definitions, and call relationships
Supports gradual generation and incremental completion until the full architecture is ready.
4. Architecture Validation & Iteration (core improvement)
- If the architecture is incomplete → continue generating the remaining parts
- If incorrect/unreasonable → fall back to aligned thinking, adjust, and regenerate
- Loop until the full architecture is complete and logically consistent
5. Human Review & Finalization
Human review, correction, and confirmation of the final architecture to eliminate hallucinations and ensure project correctness.
6. Generate Text-based UML Project Maps
Output human-readable, machine-parsable plain text:
- UML class diagrams
- Module/collaboration diagrams
Serves as the global code map for the project.
7. Create Micro-workspaces Based on UML Maps
Start with macro modules and go top-down, layer by layer into details,
loading only the minimal valid code snippet for the current task each time.
8. Automatic Mode Switching & Layered Development
The system automatically switches between two modes based on requirements:
- **Architect & Algorithm Innovation Mode**: for overall design, core algorithm design, high creativity tasks
- **Software Engineer Mode**: for code implementation, local modification, detail optimization
The model always processes only local content, without loading the full project.
9. Iterative Refinement of the Entire Project
Continuously iterate to refine all modules, maintaining minimal context and high stability throughout.
---
## Core Philosophy
Traditional AI-assisted development has three critical problems:
1. It consumes a huge amount of context and tokens.
2. It relies on large models and cannot work offline.
3. It lacks macro control over large and complex projects.
This architecture completely mimics human thinking:
**macro first, then micro; architecture first, then implementation**.
It has clear project memory and strong macro control,
so it can stably handle **large-scale and complex projects**, not just small software.
---
## Two Intelligent Modes
- **Architect & Algorithm Innovation Expert Mode**
Default mode at startup. Focus on high-level design, core algorithm innovation, structure planning, with high creativity.
- **Software Engineer Mode**
Automatically enabled for code implementation, local modification, function completion, bug fixing, with high stability and precision.
The system automatically switches between the two modes without manual intervention.
---
## Key Security & Offline Advantage
If this project succeeds, developers no longer need to upload company code to external networks or cloud services.
With local small LLMs, everyone can develop safely in **offline / disconnected environments**,
without uploading any internal code, protecting company privacy, assets, and security completely.
---
## Advantages
- Perfectly solves high token consumption and context overflow
- Does not rely on large models; adapts to local small LLMs
- Supports fully offline development, no need to upload code
- Has real macro control like humans, clear project memory
- Able to develop large and complex projects, not just small software
- Only processes local information throughout
- Supports local architecture generation + iterative revision, with strong fault tolerance
- Dual intelligent modes, automatically switched based on task requirements
- Architecture-first, human-finalized, safe and controllable
- Text-based UML maps, human-readable and machine-parsable
- Auto-split micro-workspaces, precise modification scope
- No heavy IDEs or plugins required
- Fully local execution, privacy-safe and reproducible
---
## Use Cases
- Local small LLM-assisted code development
- Low VRAM / small context window environments
- Offline development for enterprise code security
- Top-down, architecture-first development methodology
- Large-scale and complex project development
- Code generation, local modification, module refinement
- Minimal IDE / experimental tool development
---
## Project Goals
The purpose of open-sourcing this project:
Welcome the community to participate in development and turn this solution into a usable tool as soon as possible.
Anyone can:
- Submit code
- Propose suggestions
- Fix bugs
- Build extensions
- Commercialize, charge, or redistribute freely, with no relation to the original author.
---
## Open Source License
MIT License — an extremely permissive license:
- Commercial use is allowed
- Modification is allowed
- Distribution is allowed
- No payment to the original author required
- No notification to the original author required
- No liability to the original author for issues
---
## Welcome to Contribute
Welcome to Star, Fork, and PR to make small LLM development tools more stable and powerful!
---
# 中文版
# Micro Architect
面向本地小模型、有限上下文窗口的分层渐进式代码开发架构。
---
## 核心思想
本地小模型上下文窗口有限，无法一次性理解与处理整个项目代码。
本方案完全模拟人类开发思维：先宏观、后微观；先架构、后实现。
通过思路对齐 → 架构生成 → 循环修正 → 人工敲定 → 文字UML地图 → 微工作区迭代，
让模型只读取局部信息，即可完成大型项目的理解、开发与维护。
系统在思路对齐阶段，**默认进入架构师模式 + 算法创新专家模式**，
并根据任务需求，**在两种专业模式之间自动切换**。
---
## 完整工作流程
1. 思路对齐（默认：架构师模式 + 算法创新专家模式）
系统自动进入架构师模式与算法创新专家模式。
人与模型统一项目目标、范围、核心逻辑，确保方向一致。
2. 自动配置模型参数
系统根据当前模式，自动设置温度（temperature）等大模型参数：
- 架构师模式：高创造力参数
- 软件工程师模式：稳定、严谨、低错误参数
3. 局部/整体架构生成（支持分步生成）
模型可生成：
- 整体架构
- 局部架构（模块/子系统）
- 类结构、方法定义、调用关系
支持一点点生成、逐步补全，直到全部架构生成完毕。
4. 架构校验与循环迭代（核心改进点）
- 若架构不完整 → 继续生成剩余部分
- 若不正确/不合理 → 自动回退到思路对齐，重新调整后再生成
- 循环往复，直到全部架构完整且逻辑自洽
5. 人工审定与最终敲定
人工审核、修正、确认最终架构，彻底避免模型幻觉，保证项目正确性。
6. 生成文字版 UML 项目地图
输出人可读、程序可解析的纯文本：
- UML 类图
- 模块/协作图
作为项目全局代码地图。
7. 基于 UML 地图创建微工作区
从宏观模块开始，自上而下、逐层进入细节，
每次只加载当前要处理的最小有效代码片段。
8. 模式自动切换与分层渐进式开发
系统根据需求**自动切换两种工作模式**：
- **架构师 & 算法创新专家模式**：负责整体设计、核心算法、架构规划，高创造力
- **软件工程师模式**：负责代码实现、局部修改、功能完善、细节优化，高稳定性
模型始终只处理局部内容，不加载全量项目。
9. 迭代完善整个项目
持续迭代，逐步完善所有模块，全程保持极小上下文、极高稳定性。
---
## 核心理念
传统 AI 辅助开发存在三大致命问题：
1. 极度耗费上下文、费 token；
2. 必须依赖大模型，无法断网开发；
3. 没有对大型项目的**宏观把控能力**。
本架构完全像人一样思考：
**先宏观、后微观，先架构、后实现**，
拥有清晰的项目记忆与真正的**宏观把控力**，
因此可以稳定应对**大型复杂项目**，而不只是做小软件。
---
## 两大智能模式
- **架构师 & 算法创新专家模式**
启动时默认进入，专注顶层设计、核心算法创新、结构规划，创造力优先。
- **软件工程师模式**
自动用于代码实现、局部修改、函数补全、Bug修复，稳定性与精度优先。
系统无需人工干预，**根据任务自动切换**。
---
## 核心安全与断网价值
如果这个项目成功，每个人都不用再把公司代码上传到外网或云端。
借助本地小模型，所有人都可以在**断网环境下安全开发**，
不用上传任何内部代码，彻底保护企业隐私、资产与安全。
---
## 优势
- 彻底解决耗 token、爆上下文问题
- 不依赖大模型，极致适配本地小模型
- 支持完全断网开发，不上传代码
- 像人一样具备**宏观把控力**，项目记忆清晰
- 能做**大型复杂项目**，不只局限于小软件
- 全程只处理局部信息，不加载全量代码
- 支持局部架构生成 + 循环迭代修正，容错极强
- 双智能模式，根据需求自动切换
- 架构先行、人工敲定，安全可控
- 文字UML地图，人能看懂、程序可解析
- 微工作区自动切分，修改范围精准
- 不依赖重型IDE、不依赖插件
- 完全本地运行，隐私安全、可复现
---
## 适用场景
- 本地小模型代码辅助开发
- 低显存 / 小上下文窗口环境
- 企业代码安全、断网开发场景
- 自上而下、架构先行的开发模式
- 大型、复杂项目开发
- 代码生成、局部修改、模块完善
- 极简 IDE / 实验性工具开发
---
## 项目目标
本项目开源的目的：
欢迎社区一起参与开发，尽快把这套方案做成真正可用的工具。
任何人都可以：
- 提交代码
- 提建议
- 改Bug
- 做扩展
- 商用、收费、二次分发都可以，与原作者无关。
---
## 开源协议
MIT License —— 超宽松协议：
- 商用随意
- 修改随意
- 分发随意
- 无需给原作者付费
- 无需告知原作者
- 出问题不找原作者
---
## 欢迎共建
欢迎 Star、Fork、PR，一起把小模型开发工具做得更稳、更好用！
