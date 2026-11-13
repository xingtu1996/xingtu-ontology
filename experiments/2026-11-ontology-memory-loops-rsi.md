# Ontology × Memory × Loops × RSI：从知识实验到可验证改进

> 状态：`mock`（跨仓 Python 离线原型已在本地完成 10 项测试）；远端新仓与 DSH 实际接入均为 `design`。
> 2026-11-13 · 行途 XingTu

## 问题

Coding Agent 每次从零理解项目：代码定位成功却误用业务语义；上一轮 Bug 已修复，下一轮仍在不适用条件下套用旧经验。单纯积累对话 Memory 无法证明下一轮行为真正改善。

## 假设

- 本体提供 `concept_id`、业务约束、适用范围与反例，让经验定位到明确语义对象。
- Memory 保存来源、任务、条件、根因和验证证据，不把原始上下文直接当真理。
- Loops 将每轮 Task / 输入版本 / 测试 / Receipt 关联起来，向 Memory 产出候选经验。
- RSI 用固定任务集重放候选改进，禁止删样例刷分、禁止旧成功任务退化；只提交人工审核。

## 做了什么（已核实 vs 未完成）

1. 核实 `xingtu-ontology` 已存在并保持 research preview。新名称决议：`xingtu-loops` 用复数，因为支持 Coding、Debug、Review、Knowledge 等多类闭环。
2. 构造了 **本地** 3 个独立 Python 标准库原型：`xingtu-memory`、`xingtu-loops`、`xingtu-rsi`，含 SQLite 经验状态机、mock Task/Receipt 与受限回归评估。
3. 本地 `unittest` 10 项通过（3+3+4）；合成案例演示“显式空列表 ≠ 未传参数”。没有通过真实 Coding Agent / DSH 运行，也尚未提交这三仓代码至 GitHub。
4. XSA 跨仓建仓与验证追踪： https://github.com/xingtu1996/xingtu-super-agent/issues/13 。

## 目标协作边界

| 仓库 | 责任 | 禁止越权 |
|---|---|---|
| `xingtu-ontology`（本仓） | 本体概念、领域关系、成立条件、脱敏样本 | 私有原始知识与执行引擎 |
| `xingtu-memory`（待建） | 有证据、有适用范围的项目经验 | 定义所有业务规则、自动提权 |
| `xingtu-loops`（待建） | 多种 Execute/Verify/Learn 流程与回执 | 重做 XSA 全局调度 |
| `xingtu-rsi`（待建） | 策略候选、基准重放和非退化门禁 | 自动修改 Policy/Mandate 和基准 |
| `xingtu-super-agent` | 授权、跨 Agent 编排、Task/Receipt 规范 | 用 Loop 替代现有执行器 |
| DSH（外部上游） | 插件式 Agent runtime 与执行 | 宣称现阶段已兼容 |

## 验收建议

1. 本体节点的 `concept_id` 能追踪到经验来源和适用条件，且能提供不适用反例。
2. 未验证、版本错误或项目不匹配的经验一律不召回。
3. 同一 Task+Revision 的输入冲突必须拒绝，Receipts 必须可追踪输入 SHA。
4. RSI 冻结评测样例：有真增益且无退化才能进入人工审核；不自动推广。
5. DSH 接入应通过独立 Cordis 适配器、受限授权和只读沙箱验证，不能直接修改上游核心。

## 状态与下一步

- `mock`：本地测试通过（产物在 ChatGPT 当前会话可下载；GitHub 尚无对应新仓代码，不能视作 GitHub CI 证据）。
- `design`：建 3 个新仓、真实 Cordis 插件、跨仓线上 E2E、生产能力。
- **下一步**：使用有建仓权限的执行端按 XSA issue 建仓并推送独立代码、运行 CI；本仓保留研究记录，不硬留新仓实现。

## 来源

- TencentDB Agent Memory：https://github.com/TencentCloud/TencentDB-Agent-Memory
- DSH 架构：https://github.com/deepseek-ai/deepseek-harness/blob/master/docs/architecture.md
- DSH Superagent 领域模型：https://github.com/deepseek-ai/dsh-superagent-prototype/blob/main/docs/001-domain.md

**证据边界**：来源文章中“58%→65%”没有在本实验中复现或独立核实方法与样本规模，不能作为行途工程效果。
