# Wiki Log / 维基日志

> 所有 wiki 操作的 chronology 记录。Append-only。
> All wiki operations recorded chronologically. Append-only.
>
> 格式 / Format: `## [YYYY-MM-DD] action | subject`
> 操作 / Actions: ingest, update, query, lint, create, archive, delete

---

## [2026-04-15] create | Wiki initialized / 初始化
- 领域 / Domain: 美国电力电网（U.S. Electric Power Grid）- 建设、运营、输配电
- 创建了 SCHEMA.md、index.md、log.md
- Goal: 快速 crash course 补上知识缺口
- Structure created with SCHEMA.md, index.md, log.md
- Goal: Fast crash course to fill knowledge gaps

## [2026-04-15] ingest | EIA 电力入门文章 / EIA Electricity Basics Articles
- 来源 / Source: EIA Energy Explained (eia.gov)
- 添加文件 / Files added:
  - raw/articles/eia-delivery-to-consumers.md
  - raw/articles/eia-how-electricity-is-generated.md

## [2026-04-15] create | 概念页面 (5个) / Concept Pages (5)
基于摄入来源创建 / Created based on ingested sources:
- concepts/power-grid-overview.md - 电网概述 / Power Grid Overview
- concepts/three-major-interconnections.md - 三大互联系统 / Three Major Interconnections
- concepts/power-generation.md - 发电 / Power Generation
- concepts/power-transmission.md - 输电 / Power Transmission
- concepts/power-distribution.md - 配电 / Power Distribution

## [2026-04-15] update | index.md
- 添加了5个概念页面到索引 / Added 5 concept pages to the index
- 总页面数 / Total pages: 5

## [2026-04-17] ingest | ERCOT核电与天然气发电政策 / ERCOT Nuclear and Gas Generation Policy
- 来源 / Source: ERCOT官网调研（ercot.com, ercot.com/mktrules, ercot.com/news）
- 添加文件 / Files added:
  - concepts/ercot-nuclear-gas-generation-policy.md
- 内容摘要 / Content summary:
  - ERCOT核电现状（仅South Texas Project，约2,700 MW）/ ERCOT nuclear status (only South Texas Project, ~2,700 MW)
  - 天然气发电燃料供应保障要求（NPRR1275）/ Natural gas fuel supply assurance requirements (NPRR1275)
  - 辅助服务市场参与机制 / Ancillary services market participation mechanism
  - RMR（Reliability Must Run）机制
  - 关键政策动态（RTC+B上线、长期负荷预测等）/ Key policy updates (RTC+B launch, long-term load forecast, etc.)
- 总页面数 / Total pages: 14

## [2026-04-17] ingest | ERCOT太阳能并网流程 / ERCOT Solar Interconnection Process
- 来源 / Source: ERCOT官网调研（ercot.com/services/rq/integration）
- 添加文件 / Files added:
  - concepts/ercot-solar-interconnection-process.md
- 内容摘要 / Content summary:
  - GINR五阶段并网流程（申请→可行性→系统影响→设施→并网协议）/ GINR five-stage process (application → feasibility → system impact → facility → interconnection agreement)
  - 太阳能电站技术标准（LVRT低电压穿越、FRT频率穿越、功率因数控制）/ Solar plant technical standards (LVRT, FRT, power factor control)
  - QSA（Qualified Scheduling Entity）要求
  - 分布式vs大型太阳能并网区别 / Distributed vs large-scale solar interconnection differences
  - ERCOT Planning Guide关键章节 / Key chapters from ERCOT Planning Guide
- 总页面数 / Total pages: 15

## [2026-04-15] update | ERCOT长期负荷预测与NPRR规则 / ERCOT Long-term Load Forecast and NPRR Rules
- ERCOT 2032初步负荷预测（2026年4月15日发布）：367,790 MW / ERCOT 2032 preliminary load forecast (April 15, 2026): 367,790 MW
- 2023年创纪录负荷：85,508 MW（夏季峰值）/ 2023 record load: 85,508 MW (summer peak)
- 新增市场规则 / New market rules:
  - NPRR1275：Firm Fuel Supply Service Phase 3
  - NPRR1278：Advanced Grid Support Service
  - NPRR1309/1310：Dispatchable Reliability Reserve Service
- 更新文件 / Updated files:
  - concepts/ercot-nuclear-gas-generation-policy.md
  - concepts/ercot-rtc-b-market.md

## [2026-05-07] create | Gap Analysis + Research Recommendations / 缺口分析与研究建议
- 来源 / Source: 分析了18个现有笔记文件，发现技术扎实但经济分析薄弱 / Analyzed 18 existing notes — technically solid but weak on economic analysis
- 添加文件 / Files added:
  - concepts/RECOMMENDATIONS.md — PhD级研究缺口分析 / PhD-level research gap analysis
  - 识别出12个新研究话题（Tier 1-3）/ Identified 12 new research topics (Tier 1-3)
- 总页面数 / Total pages: 15

## [2026-05-07] create | 8 New Research Topic Documents (Tier 1-3)
新增文档（按优先级）/ New documents (by priority):
- Tier 1-1: concepts/carbon-pricing-integration.md — CA cap-and-trade, RGGI, 碳成本对LMP影响, 联邦主义碎片化问题
- Tier 1-2: concepts/capacity-market-design.md — PJM RPM拍卖, ELCC容量信用, "缺钱"问题, ERCOT比较
- Tier 1-3: comparisons/pjm-vs-ercot.md — 两种市场设计全面比较, Uri极端天气案例研究
- Tier 2-5: concepts/ferc-jurisdiction-carbon.md — FERC法律权威, DCC挑战, 州碳边境措施
- Tier 2-6: comparisons/state-rps-effectiveness.md — CA/TX/NY RPS对比, 成本效益, 方法论问题
- Tier 3-9: concepts/storage-economics.md — 储能收益堆叠, ELCC, 退化模型, 最优duration
- Tier 3-10: concepts/environmental-justice-energy.md — 能源转型公正, DAC太阳能, 程序公正
- Tier 3-11: concepts/demand-response-economics.md — DR经济学, 价格型vs激励型, BTM/FTM
- Tier 3-12: concepts/social-cost-carbon-dispatch.md — SCC方法论, 调度整合, 一般均衡效应
- 商业应用 / Business: concepts/solar-storage-interconnection-ca-tx.md — 加州/德州并网流程+障碍（中国出海企业）
- 更新 / Updated: index.md (总页面数 / Total pages: 27), log.md
- 总页面数 / Total pages: 27

## [2026-05-07] update | 所有文档中文化 / Bilingual Update (CN + EN)
- 将所有32个文档更新为中英文双语格式
- Updated all 32 documents to bilingual Chinese + English format
- 文件内容改为：先全中文，后面再全英文
- Format: full Chinese first, then full English after separator
- 同步更新两个 GitHub repos:
  - Marcotravels/US-Power-Market-Basics- (private, Obsidian vault)
  - Marcotravels/US-Power-Market-Wiki (public, GitHub Pages)
