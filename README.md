# xingtu-ontology

> Research Preview · AI 知识图实验场
> 当前阶段是原型与离线实验，不是生产系统。每个实验都标状态：`design`（仅想法）/ `mock`（离线原型）/ `verified`（有可核对证据）/ `production`（真在跑）。请勿把前三种读成第四种。

行途在 AI 知识图方向的 playground。

跟 [XSA](https://github.com/xingtu1996/xingtu-super-agent) 一个性质：**先在这里跑原型，跑通了再独立成仓**。跑不通的，留个记录也不亏。

## 在试什么

一个长期问题：**一个人/一个组织攒了那么多对话、笔记、文档，怎么让 AI 真的用起来，而不是只存着？**

行途自己的 vault 已经是三层（Raw/Wiki/Schema）的实践场，但它是私有的。这个仓把"知识图怎么搭、怎么验证、怎么跑"这件事当成实验来做：

- 概念模型怎么拆
- 脱敏数据怎么可视化
- 一个最小 demo 怎么从真实素材里长出来
- 哪些想法值得独立成仓，哪些该扔掉

## 实验清单

| 实验 | 状态 | 说明 |
|------|------|------|
| [三层知识模型框架](experiments/2026-11-三层知识模型框架.md) | `design` | Raw/Wiki/Schema 分层假设，基于 vault 2643 张元宝卡 / 152 张素材卡 / 40+ skill 实测 |
| [元宝卡片主题图](demos/yuanbao-graph/) | `mock` | 2643 张卡片按月份/主题聚成两张图，静态 ECharts，脱敏只计数 |

## 目录

```
xingtu-ontology/
├── experiments/    # 实验笔记（想法、踩坑、结论）
├── demos/          # 可跑原型（静态为主）
├── docs/           # 实验过程记录
└── assets/         # 图片
```

## 跟其他仓的关系

- **不是方法论仓**：AI 工程化方法论在 [xingtu-ai-engineering](https://github.com/xingtu1996/xingtu-ai-engineering)
- **不是知识库**：真实知识资产在私有 vault，本仓只放脱敏后的实验样本
- **不是 ADR 仓**：技术决策在 [xingtu-portfolio](https://github.com/xingtu1996/xingtu-portfolio)
- **跑通了会独立出去**：某个实验如果长成独立项目，会从本仓拆出去单独建仓，本仓只留实验记录

## 怎么更新

- 新实验：`experiments/YYYY-MM-<slug>.md`，开头标状态（design/mock/verified/production）
- 新 demo：`demos/<name>/`，含 README 说明跑法与脱敏口径
- 改之前读 `AGENTS.md`

## 许可

MIT。

---

行途 XingTu · 一线 AI 工程化实践者
