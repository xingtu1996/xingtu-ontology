# AGENTS.md · xingtu-ontology 冷启动说明

> 写给任何接手这个仓的 Agent。这是一个实验场，不是生产仓。

## 仓库定位

公开仓，Research Preview。AI 知识图方向的 playground，对标 XSA：先跑原型，跑通了独立成仓，跑不通留记录。

## 不能碰的红线

1. **隐私**：不出现中文真名、英文名及变体（SAF-010 禁用）、真实手机号、个人/雇主邮箱、任职公司名。对外统一"行途 XingTu"。提交前在 xingtu 工作区跑 `python3 tools/privacy_scan.py --fail-fast .`。
2. **发布时序**：公众号声明原创的排期稿全文不上本仓。已发文章只放"标题 + 300 字摘要 + 公众号链接"。
3. **不搬他仓**：方法论在 xingtu-ai-engineering，ADR 在 xingtu-portfolio，真源素材在私有 vault。本仓只放脱敏实验样本。
4. **不造后端**：demos 以静态 HTML + ECharts/CDN 为主，GitHub Pages 能直接跑。

## 实验状态标注

每个实验/ demo 开头必须标状态：
- `design`：只有想法，没动手
- `mock`：离线原型，跑过但没真用
- `verified`：有可核对证据（数字、截图、链接）
- `production`：真在生产跑

写实验笔记时诚实标，不要把 mock 当 production 吹。

## 目录该放什么

| 目录 | 放什么 | 不放什么 |
|------|--------|----------|
| `experiments/` | 实验想法、踩坑、结论、状态 | 散文式感悟、未验证的大词 |
| `demos/` | 最小可跑原型 | 半成品代码、需要后端的东西 |
| `docs/` | 实验过程记录、决策日志 | 日常笔记 |

## 跑通了怎么办

某个实验如果长成独立项目：
1. 从本仓拆出去，单独建仓（走 05_项目立项SOP）
2. 本仓 experiments/ 里留一篇"实验记录"，链接到新仓
3. 不硬留代码在本仓——本仓是实验场，不是长期家

## 提交规范

- commit：`feat: 简述` / `docs: 简述` / `fix: 简述`（中文描述）
- 实验笔记：`YYYY-MM-<英文slug>.md`
- 每个实验笔记必须有：问题 → 假设 → 做了什么 → 状态 → 下一步

## 真源回链

本仓是公开实验场。深层真源在私有 vault：
- 方法论 SSoT：vault `01_战略与规章 (Strategy & Rules)/specs/`
- 元宝卡片原始库：vault `outputs/yuanbao_inventory/`（私有，不进本仓）
- 品牌规范：vault `DESIGN.md`（私有）

如果本仓与 vault 冲突，以 vault 真源为准，反过来修本仓。
