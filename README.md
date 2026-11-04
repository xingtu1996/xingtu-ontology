# xingtu-ontology · AI 知识图研究与作品集

> 行途 XingTu · 一线 AI 工程化实践者 · 把"个人/组织知识如何被 AI 用起来"当成一个研究问题来做

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 这是什么

这不是又一个"AI 工具合集"仓库。

过去两年我在自媒体和工程实践里反复碰到同一个问题：**一个人/一个组织攒了那么多对话、笔记、文档、代码，为什么 AI 还是用不起来？**

元宝对话攒了 2600 多张卡片、素材库沉淀了上百张卡、Harness 里跑着 40 多个 skill——但如果换一个 AI、换一个 Agent，它冷启动时能读懂多少？

这个仓库把这件事当成一个正经的研究方向来做：

- **研究层**（`research/`）：知识分层、Agent 架构、个人知识管理的方法论笔记，不写散文，写概念模型
- **作品集**（`portfolio/`）：按"解决过哪类问题"组织的案例，不按时间，不按客户
- **Demo**（`demos/`）：能直接跑起来的最小实现，静态页面为主，不依赖后端

## 目录结构

```
xingtu-ontology/
├── research/           # 研究笔记
│   ├── 01-knowledge-graph/    # 知识图分层与组织
│   ├── 02-agent-architecture/ # Agent 架构观察（单主循环/Super-agent 等）
│   └── 03-personal-knowledge/  # 个人知识管理实践
├── portfolio/           # 按问题类型组织的案例
├── demos/               # 可跑 demo
│   └── yuanbao-graph/  # 元宝卡片主题图（静态 HTML）
└── assets/              # 图片与示意图
```

## 快速开始

1. 读 `research/01-knowledge-graph/` 下最新一篇笔记，5 分钟看懂三层模型
2. 打开 `demos/yuanbao-graph/index.html`，看 2600+ 张元宝卡片按主题/月份聚成什么样
3. 翻 `portfolio/`，找和你手头问题最像的案例

## 怎么更新

- 新研究笔记：`research/<topic>/YYYY-MM-<slug>.md`
- 新 demo：`demos/<name>/`，必须含 README 说明跑法
- 改之前先读 `AGENTS.md`——给后续接手的 Agent（包括未来的我）留的冷启动说明

## 避坑提醒

- 本仓不放未发布公众号文章全文；已发文章只放摘要 + 公众号链接
- 本仓不出现真实姓名、雇主信息、手机号、邮箱（对外统一"行途 XingTu"）
- 技术决策类 ADR 不在本仓，在 [xingtu-portfolio](https://github.com/xingtu1996/xingtu-portfolio)

## 许可

MIT — 随便用，留个链接就行。

---

行途 XingTu · 一线 AI 工程化实践者 · [公众号：行途](https://mp.weixin.qq.com/)
