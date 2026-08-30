# Wiki Schema

## 领域 / Domain
美国电力电网（U.S. Electric Power Grid）- 建设、运营、输配电

## 规范 / Conventions
- **文件名**：小写字母、连字符、无空格（如 `power-grid-overview.md`）
- 每个页面以 YAML frontmatter 开头
- 使用 `[[wikilinks]]` 建立页面间链接（每页至少2个外链）
- 更新页面时必须更新 `updated` 日期
- 新页面必须添加到 `index.md`
- 所有操作追加到 `log.md`

## Frontmatter 结构 / Frontmatter
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

## 标签体系 / Tag Taxonomy
- **基础概念 / Basics**：grid-basics, terminology, history
- **电网结构 / Grid Structure**：generation, transmission, distribution, interconnection
- **运营主体 / Organizations**：ferc, nerc, rto, iso, utility-company
- **技术术语 / Technical Terms**：voltage, load, frequency, reliability, blackout
- **当前议题 / Current Topics**：renewable-integration, aging-infrastructure, energy-storage, grid-modernization
- **区域 / Regions**：eastern-interconnection, western-interconnection, ercot

## 页面创建阈值 / Page Thresholds
- **创建页面**：概念/实体在 2+ 来源中出现，或在一个来源中为核心内容
- **添加到现有页面**：来源提到的内容已有页面覆盖
- **不创建页面**：仅一次性提及、minor details、或超出领域范围
- **拆分页面**：超过 200 行时拆分为子主题
- **归档页面**：内容完全过时 → 移至 `_archive/`

## 实体页面 / Entity Pages
每个 notable 实体一个页面，包含：
- 概述/定义
- 关键事实和日期
- 与其他实体的关系（[[wikilinks]]）
- 来源引用

## 概念页面 / Concept Pages
每个概念/主题一个页面，包含：
- 定义/解释
- 当前知识状态
- 开放问题或争议
- 相关概念（[[wikilinks]]）

## 对比页面 / Comparison Pages
并列分析，包含：
- 比较对象及原因
- 比较维度（表格格式）
- 结论或综合
- 来源

## 更新政策 / Update Policy
新信息与现有内容冲突时：
1. 检查日期 — 新来源通常覆盖旧来源
2. 如确实矛盾，记录双方立场及日期和来源
3. 在 frontmatter 标记：`contradictions: [page-name]`
4. 在 lint 报告中标记供用户审核

---

# English Version

## Domain
U.S. Electric Power Grid — construction, operation, transmission and distribution.

## Conventions
- **Filenames**: lowercase, hyphens, no spaces (e.g., `power-grid-overview.md`)
- Every page starts with YAML frontmatter
- Use `[[wikilinks]]` to link pages (minimum 2 external links per page)
- Must update `updated` date when editing
- New pages must be added to `index.md`
- All operations appended to `log.md`

## Frontmatter
```yaml
---
title: Page title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [choose from tag library below]
sources: [raw/articles/source-file.md]
---
```

## Tag Taxonomy
- **Basics**: grid-basics, terminology, history
- **Grid Structure**: generation, transmission, distribution, interconnection
- **Organizations**: ferc, nerc, rto, iso, utility-company
- **Technical Terms**: voltage, load, frequency, reliability, blackout
- **Current Topics**: renewable-integration, aging-infrastructure, energy-storage, grid-modernization
- **Regions**: eastern-interconnection, western-interconnection, ercot

## Page Thresholds
- **Create a page**: Concept/entity appears in 2+ sources, or is core content in one source
- **Add to existing page**: Content is already covered by an existing page
- **Do not create**: One-off mentions, minor details, or out-of-scope content
- **Split page**: Split into subtopics when exceeding 200 lines
- **Archive page**: Content fully outdated → move to `_archive/`

## Entity Pages
One page per notable entity, containing:
- Overview/definition
- Key facts and dates
- Relationships with other entities ([[wikilinks]])
- Source citations

## Concept Pages
One page per concept/topic, containing:
- Definition/explanation
- Current state of knowledge
- Open questions or controversies
- Related concepts ([[wikilinks]])

## Comparison Pages
Side-by-side analysis, containing:
- What is being compared and why
- Comparison dimensions (table format)
- Conclusion or synthesis
- Sources

## Update Policy
When new information conflicts with existing content:
1. Check dates — newer sources typically override older ones
2. If genuinely contradictory, record both positions with dates and sources
3. Tag in frontmatter: `contradictions: [page-name]`
4. Flag in lint report for user review
