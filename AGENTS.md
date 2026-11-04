# AGENTS.md · xingtu-ontology 冷启动说明

> 本文件写给任何接手这个仓库的 Agent（包括未来的豆包/Codex/ChatGPT）。
> 你不需要读 vault 全部内容，读这个文件就知道仓库边界、纪律和怎么加东西。

## 仓库定位

公开仓。研究"AI 时代个人/组织知识图怎么搭、怎么用、怎么复利"。
读者：AI 工程实践者、知识管理同好、潜在合作者。

## 不能碰的红线

1. **隐私**：不出现中文真名、`Justin Li` 及变体、真实手机号、个人/雇主邮箱、任职公司名。对外统一"行途 XingTu"。提交前在 xingtu 工作区跑 `python3 tools/privacy_scan.py --fail-fast .`。
2. **发布时序**：公众号声明原创的排期稿全文不上本仓。已发文章只放"标题 + 300 字摘要 + 公众号链接"。
3. **不搬他仓**：技术 ADR 仍在 `xingtu-portfolio`，品牌物料仍在 `xingtu-brand-assets`（私有），原始素材仍在 `xingtu-vault`（私有）。本仓只放研究层与 demo。
4. **不造后端**：demos 以静态 HTML + ECharts/CDN 为主，GitHub Pages 能直接跑。

## 目录该放什么

| 目录 | 放什么 | 不放什么 |
|------|--------|----------|
| `research/01-knowledge-graph/` | 知识分层、本体设计、Schema 模型 | 散文式感悟 |
| `research/02-agent-architecture/` | 单主循环/多智能体/Router-Worker 等架构观察 | 工具评测流水账 |
| `research/03-personal-knowledge/` | PKM 实践、复利方法、token 优化 | 每日日记 |
| `portfolio/` | 按问题类型组织的案例卡 | 简历式项目罗列 |
| `demos/` | 最小可跑实现 | 半成品代码 |

## 提交规范

- commit：`feat: 简述` / `docs: 简述` / `fix: 简述`（Conventional Commits，中文描述）
- 新笔记文件命名：`YYYY-MM-<英文slug>.md`
- 每个 research 笔记必须有：问题 → 概念模型 → 证据 → 可复用条件

## 真源回链

本仓是公开门面。深层真源在私有 vault：
- 方法论 SSoT：vault `01_战略与规章 (Strategy & Rules)/specs/`
- 元宝卡片原始库：vault `outputs/yuanbao_inventory/yuanbao_cards.json`（私有，不进本仓）
- 品牌规范：vault `DESIGN.md`（私有）

如果本仓内容与 vault 冲突，以 vault 真源为准，然后反过来修本仓。
