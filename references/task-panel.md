# 阶段化任务面板模板

用于把项目拆解结果转成可执行任务，适合前端、项目管理面板或后续路线文档。

## Stage 1：项目流程复原

- 目标：画出从输入到输出的完整流程。
- 输入：项目代码、pipeline 文档、用户说明。
- 任务：
  - 列出原始输入；
  - 列出预处理；
  - 列出表示/特征；
  - 列出模型；
  - 列出后处理；
  - 列出最终输出。
- 输出：
  - `workflow_tree.md`
  - `data_flow_table.tsv`

## Stage 2：失败模式分析

- 目标：找出每一层的核心困难。
- 输入：流程树、已有结果、错误分析。
- 任务：
  - 生成难题树；
  - 标记用户已提出的问题；
  - 补充遗漏问题；
  - 区分已验证和待验证。
- 输出：
  - `problem_tree.md`
  - `failure_mode_report.md`

## Stage 3：对策生成

- 目标：每个难题对应候选模块。
- 输入：难题树。
- 任务：
  - 为每个难题提出 1-3 个对策；
  - 标出需要的数据；
  - 标出需要的 baseline；
  - 标出成功和失败标准。
- 输出：
  - `solution_map.md`
  - `module_hypothesis_table.tsv`

## Stage 4：文献图谱

- 目标：把每个对策放入领域文献和跨领域方法背景。
- 输入：对策树、已有文献、检索结果。
- 任务：
  - 整理本领域 baseline；
  - 整理跨领域来源；
  - 说明继承和区别；
  - 提炼审稿风险。
- 输出：
  - `literature_map.md`
  - `related_work_matrix.tsv`

## Stage 5：论文边界

- 目标：判断哪些方案能写成论文。
- 输入：对策树、文献图谱、实验成熟度。
- 任务：
  - 建立论文边界矩阵；
  - 判断独立论文 / 系统模块 / supplementary / 后续储备；
  - 判断通用化潜力；
  - 判断大论文可能性。
- 输出：
  - `paper_boundary_matrix.md`
  - `paper_priority_list.md`

## Stage 6：最小实验闭环

- 目标：为优先论文定义最少必须实验。
- 输入：论文边界矩阵。
- 任务：
  - 列 baseline；
  - 列 ablation；
  - 列指标；
  - 列图表；
  - 定 go/no-go 标准。
- 输出：
  - `minimal_experiment_plan.md`
  - `go_no_go.md`

## Stage 7：论文骨架

- 目标：进入 manuscript 规划。
- 输入：实验闭环和文献图谱。
- 任务：
  - 写一句话论证；
  - 写贡献列表；
  - 写图表计划；
  - 写章节结构；
  - 写不解决什么。
- 输出：
  - `paper_outline.md`
  - `figure_plan.md`
  - `claim_evidence_map.md`

## 动态增加任务规则

如果分析过程中发现新对策：

1. 先放入对应难题；
2. 判断流程层级；
3. 判断是否已有证据；
4. 判断是否有通用迁移；
5. 再决定进入哪篇论文或保留为后续储备。
