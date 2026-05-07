# Wiki Log

> 所有 wiki 操作的 chronology 记录。Append-only。
> 格式: `## [YYYY-MM-DD] action | subject`
> 操作: ingest, update, query, lint, create, archive, delete

## [2026-04-15] create | Wiki initialized
- Domain: 美国电力电网（U.S. Electric Power Grid）- 建设、运营、输配电
- Structure created with SCHEMA.md, index.md, log.md
- Goal: 快速 crash course 补上知识缺口

## [2026-04-15] ingest | EIA 电力入门文章
- Source: EIA Energy Explained (eia.gov)
- Files added:
  - raw/articles/eia-delivery-to-consumers.md
  - raw/articles/eia-how-electricity-is-generated.md

## [2026-04-15] create | 概念页面 (5个)
Created concepts based on ingested sources:
- concepts/power-grid-overview.md - 电网概述
- concepts/three-major-interconnections.md - 三大互联系统
- concepts/power-generation.md - 发电
- concepts/power-transmission.md - 输电
- concepts/power-distribution.md - 配电

## [2026-04-15] update | index.md
- Added 5 concept pages to the index
- Total pages: 5

## [2026-04-17] ingest | ERCOT核电与天然气发电政策
- Source: ERCOT官网调研（ercot.com, ercot.com/mktrules, ercot.com/news）
- Files added:
  - concepts/ercot-nuclear-gas-generation-policy.md
- 内容摘要：
  - ERCOT核电现状（仅South Texas Project，约2,700 MW）
  - 天然气发电燃料供应保障要求（NPRR1275）
  - 辅助服务市场参与机制
  - RMR（Reliability Must Run）机制
  - 关键政策动态（RTC+B上线、长期负荷预测等）
- 总页面数: 14

## [2026-04-17] ingest | ERCOT太阳能并网流程
- Source: ERCOT官网调研（ercot.com/services/rq/integration）
- Files added:
  - concepts/ercot-solar-interconnection-process.md
- 内容摘要：
  - GINR五阶段并网流程（申请→可行性→系统影响→设施→并网协议）
  - 太阳能电站技术标准（LVRT低电压穿越、FRT频率穿越、功率因数控制）
  - QSA（Qualified Scheduling Entity）要求
  - 分布式vs大型太阳能并网区别
  - ERCOT Planning Guide关键章节
- 总页面数: 15

## [2026-04-15] update | ERCOT长期负荷预测与NPRR规则
- ERCOT 2032初步负荷预测（2026年4月15日发布）：367,790 MW
- 2023年创纪录负荷：85,508 MW（夏季峰值）
- 新增市场规则：
  - NPRR1275：Firm Fuel Supply Service Phase 3
  - NPRR1278：Advanced Grid Support Service
  - NPRR1309/1310：Dispatchable Reliability Reserve Service
- 更新文件：
  - concepts/ercot-nuclear-gas-generation-policy.md
  - concepts/ercot-rtc-b-market.md
