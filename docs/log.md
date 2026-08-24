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

## [2026-05-16] ingest | AI电力危机文章
- Source: 微信公众平台 (mp.weixin.qq.com)
- Files added:
  - raw/articles/ai-power-grid-crisis-2026.md
  - concepts/ai-power-grid-crisis.md（新建概念页）
- 内容摘要：
  - 2026年AI算力爆发，数据中心电力需求飙升，美国面临10-20%电力缺口
  - 机架功率从2020年13kW→2027年目标600kW（未来目标1MW）
  - 电力已从"后勤问题"变为AI扩张的核心制约因素
  - 应对：自建燃气微电网（xAI 1.9GW）、核电/SMR、东数西算地理迁移、能效提升
  - AI双重角色：电力消费者（60GW/120GW新增需求）+ 电力优化者（3-10%节能）
- 通知：已尝试通知研研学习（sessions_list超时，备用通知方案：Telegram频道）
- 总页面数: 28
- Source: 分析了18个现有笔记文件，发现技术扎实但经济分析薄弱
- 文件添加：
  - concepts/RECOMMENDATIONS.md — PhD级研究缺口分析
  - 识别出12个新研究话题（Tier 1-3）
- 总页面数: 15

## [2026-05-07] create | 8 New Research Topic Documents (Tier 1-3)
- 新增文档（按优先级）：
  - Tier 1-1: concepts/carbon-pricing-integration.md — CA cap-and-trade, RGGI, 碳成本对LMP影响, 联邦主义碎片化问题
  - Tier 1-2: concepts/capacity-market-design.md — PJM RPM拍卖, ELCC容量信用, "缺钱"问题, ERCOT比较
  - Tier 1-3: comparisons/pjm-vs-ercot.md — 两种市场设计全面比较, Uri极端天气案例研究
  - Tier 2-5: concepts/ferc-jurisdiction-carbon.md — FERC法律权威, DCC挑战, 州碳边境措施
  - Tier 2-6: comparisons/state-rps-effectiveness.md — CA/TX/NY RPS对比, 成本效益, 方法论问题
  - Tier 3-9: concepts/storage-economics.md — 储能收益堆叠, ELCC, 退化模型, 最优duration
  - Tier 3-10: concepts/environmental-justice-energy.md — 能源转型公正, DAC太阳能, 程序公正
  - Tier 3-11: concepts/demand-response-economics.md — DR经济学, 价格型vs激励型, BTM/FTM
  - Tier 3-12: concepts/social-cost-carbon-dispatch.md — SCC方法论, 调度整合, 一般均衡效应
  - 商业应用: concepts/solar-storage-interconnection-ca-tx.md — 加州/德州并网流程+障碍（中国出海企业）
- 更新: index.md (总页面数: 27), log.md
- 总页面数: 27
