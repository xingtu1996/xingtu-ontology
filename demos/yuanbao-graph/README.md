# yuanbao-graph · 元宝卡片主题图

L1 Raw 层的可视化。2643 张元宝卡片按月份、按主题聚成两张图。

## 跑法

本地直接打开 `index.html`，或起一个静态服务：

```bash
cd demos/yuanbao-graph
python3 -m http.server 8000
# 浏览器开 http://localhost:8000
```

GitHub Pages 部署后也能直接跑（只用 ECharts CDN，无后端）。

## 数据口径

- `data/monthly.json`：按月计数（2025-09 ~ 2026-11）
- `data/meta.json`：主题分布（基于 1473 张分析卡的盘点口径）
- **脱敏**：只含月份与计数，不含任何卡片原文、标题、链接

## 为什么放这个 demo

三层知识模型（Raw/Wiki/Schema）的第一篇研究笔记用了"2643 张卡"这个数字，但光说数字没体感。这个 demo 让人一眼看到：
- Raw 层是怎么随时间长起来的（2026-09 单月 615 张）
- 主题分布是不是真的围绕 AI（三大 AI 主题合计约 60%）

真源：`outputs/yuanbao_inventory/`（私有，不进本仓）
