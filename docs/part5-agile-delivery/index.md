# 第五篇：敏捷研发与项目推进篇 —— 从文档到代码的高效交付

> “写出一份完美的 PRD 只是产品管理长征的第一步。如果不能把文档翻译成研发团队心领神会的语言，不能在两周一个 Sprint 的节奏中把控技术债务与交付速率，不能在有限的资源下为几百个需求排定优先级，产品经理就永远只是一个停留在纸面上的空想家。”

---

## 篇章导读

当想法完成了客户验证与初步原型后，产品正式进入“研发实施与交付”的高负荷推进期：
- **开发模式之选**：到底该用敏捷（Agile）还是瀑布（Waterfall）？敏捷真的适合所有场景吗？
- **敏捷双雄的落地**：Scrum 的每日站会为什么经常沦为毫无营养的形式主义？看板（Kanban）的核心机制到底是什么？如何用故事点（Story Points）科学估算团队的交付速率（Velocity）？
- **工业级交付物规范**：史诗需求说明书（Epic Spec Sheet）该怎么写？工程师最痛恨什么样的用户故事（User Story）？验收准则（Acceptance Criteria, AC）如何做到让测试与技术挑不出歧义？
- **残酷的取舍决策**：资源永远短缺，老板、销售、用户都在催，究竟该用什么模型（Kano、BUC、MoSCoW、RWW）决定哪一个需求进当前冲刺、哪一个需求留在 Backlog？

本篇将从软件工程底层的交付范式出发，系统拆解**瀑布与敏捷的本质边界**、**Scrum 与 Kanban 实战仪式流程**、提供全套**工业级需求文档与验收模版**，并构建一套多维度的**需求优先级决策工具箱**。

---

## 本篇知识图谱

```mermaid
mindmap
  root((第五篇: 敏捷研发与推进))
    第12章: 研发模式与生命周期
      敏捷 Agile vs 瀑布 Waterfall
        瀑布特征: 串行大批量、前置设计、适应性低
        瀑布适用场景: 操作系统、建筑、汽车引擎、不可逆硬件
        敏捷特征: 小批量切片、端到端闭环、高频市场反馈
      产品生命周期四阶段
        引入期 Introduction (小范围、低竞争、亏损探索)
        成长期 Growth (市场接受、营收爆发、快速优化)
        成熟期 Maturity (顶峰竞争、利润稳健、精细化维稳)
        衰退期 Decline (功能退市 Sun-setting、平稳收尾)
    第13章: Scrum与看板实战
      Scrum 核心仪式与物件
        Product Backlog vs Sprint Backlog
        Sprint 规划会 (2周周期为王)
        每日站会 Daily Standup (10~15分钟排雷)
        评审会 Review & 回顾会 Retrospective (Good/Bad/Questions)
      看板 Kanban 实操
        状态流动: To do -> In progress -> Done
        核心机制: 在制品限制 (WIP Limit)
      敏捷估算与速率
        故事点 Story Points (相对难度衡量)
        团队速率 Velocity (稳健度量与排期基石)
    第14章: 标准交付物模板
      自上而下的任务拆解链
        Vision -> Goals -> Initiatives -> Epics -> Stories -> Tasks/Bugs
      Epic Spec 史诗规格说明书
        1. 简介 Introduction (目标/背景/指标)
        2. 产品需求 Product Requirements (功能细节)
        3. 设计要求 Design Requirements (原型与交互)
        4. 工程要求 Engineering Requirements (架构/接口/非功能)
      用户故事 User Story
        As a... I want to... So that...
      验收准则 AC 标准
        Given... When... Then...
    第15章: 需求优先级决策模型库
      Kano 模型
        必备属性、期望属性、魅力属性、无差异、反向属性
        动态退化规律与问卷打分
      BUC 价值模型
        Business Benefits + User Benefits - Cost (1~10打分)
      MoSCoW 四分法
        Must 必须做, Should 应该做, Could 可以做, Would 不做
      RWW 商业筛选法
        Real 真需求? Win 能赢吗? Worth 值得做?
```

---

## 章节导航

- **[第 12 章：研发模式对比：敏捷 vs 瀑布与产品生命周期](./12-agile-vs-waterfall-and-lifecycle.md)**
  - 深度对比敏捷与瀑布模式的风险收益边界、瀑布开发不可替代的特定工程场景，以及产品生命周期四阶段的演进与退市管理。
- **[第 13 章：Scrum 与看板（Kanban）实战指南 —— 仪式、速率与在制品限制](./13-scrum-and-kanban-in-practice.md)**
  - 详述 Scrum 四大核心仪式与两类 Backlog 运作、看板（Kanban）流动与在制品限制（WIP）、故事点与团队研发吞吐速率的测算心法。
- **[第 14 章：标准交付物模板与规范 —— Epic Specs, User Stories 与 AC 标准](./14-epic-specs-and-user-stories.md)**
  - 提供大厂级别的 Epic 规格说明书四模块模板、无歧义的用户故事编写准则，以及 `Given-When-Then` 验收标准的编写范例。
- **[第 15 章：需求优先级排序决策模型库 —— Kano, BUC, MoSCoW 与 RWW](./15-prioritization-frameworks.md)**
  - 汇总实战中最经典的四大需求决策工具：Kano 双轴模型、BUC 投入产出公式、MoSCoW 边界划分法与 RWW 商业筛选矩阵。
