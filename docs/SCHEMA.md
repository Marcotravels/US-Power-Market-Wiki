# Wiki Schema

## Domain
美国电力电网（U.S. Electric Power Grid）- 建设、运营、输配电

## Conventions
- 文件名：小写字母、连字符、无空格（如 `power-grid-overview.md`）
- 每个页面以 YAML frontmatter 开头
- 使用 `[[wikilinks]]` 建立页面间链接（每页至少2个外链）
- 更新页面时必须更新 `updated` 日期
- 新页面必须添加到 `index.md`
- 所有操作追加到 `log.md`

## Frontmatter
```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [从下方标签库选择]
sources: [raw/articles/来源文件.md]
---
```

## Tag Taxonomy
- **基础概念**: grid-basics, terminology, history
- **电网结构**: generation, transmission, distribution, interconnection
- **运营主体**: ferc, nerc, rto, iso, utility-company
- **技术术语**: voltage, load, frequency, reliability, blackout
- **当前议题**: renewable-integration, aging-infrastructure, energy-storage, grid-modernization
- **区域**: eastern-interconnection, western-interconnection, ercot

## Page Thresholds
- **创建页面**: 概念/实体在 2+ 来源中出现，或在一个来源中为核心内容
- **添加到现有页面**: 来源提到的内容已有页面覆盖
- **不创建页面**: 仅一次性提及、 minor details、或超出领域范围
- **拆分页面**: 超过 200 行时拆分为子主题
- **归档页面**: 内容完全过时 → 移至 `_archive/`

## Entity Pages
每个 notable 实体一个页面，包含：
- 概述/定义
- 关键事实和日期
- 与其他实体的关系（[[wikilinks]]）
- 来源引用

## Concept Pages
每个概念/主题一个页面，包含：
- 定义/解释
- 当前知识状态
- 开放问题或争议
- 相关概念（[[wikilinks]]）

## Comparison Pages
并列分析，包含：
- 比较对象及原因
- 比较维度（表格格式）
- 结论或综合
- 来源

## Update Policy
新信息与现有内容冲突时：
1. 检查日期 — 新来源通常覆盖旧来源
2. 如确实矛盾，记录双方立场及日期和来源
3. 在 frontmatter 标记：`contradictions: [page-name]`
4. 在 lint 报告中标记供用户审核
