# ERCOT 实时共优化加储能 (RTC+B) 市场机制

> **English:** ERCOT Real-Time Co-optimization Plus Batteries (RTC+B) Market Mechanism

## 概述

RTC+B（Real-Time Co-optimization Plus Batteries）是ERCOT电力市场自2010年实时节点市场设计以来最重要的升级，于**2025年12月5日**正式上线运行。该机制允许储能系统同时参与能量市场（energy market）和辅助服务市场（ancillary services market），实现实时共优化调度。

## 背景

### 发展历程
- **2019年：** PUCT指示ERCOT开展实时共优化（RTC）成本效益评估
- **评估结果：** 发现RTC可带来显著的市场效率和可靠性提升
- **市场扩展：** 随着电池储能资源（Battery Energy Storage Resources, BESRs）在ERCOT市场的快速增长，RTC项目扩展为RTC+B项目
- **2025年12月5日：** RTC+B正式上线运行

### 设计目标
1. 提高实时购电效率
2. 优化辅助服务的采购和管理
3. 改进储能的建模和调度
4. 减少人工操作和调度员决策负担

## 核心机制

### 1. 实时共优化（Real-Time Co-optimization）

**传统模式：**
- 能量市场和辅助服务市场分别独立运作
- 储能需要分别在这两个市场中竞争
- 可能导致资源分配效率低下

**RTC+B模式：**
- 在实时市场中同时优化能量和辅助服务的采购
- 系统可以同时考虑储能的所有可用能力
- 自动找到最优的资源组合

### 2. 储能作为单一设备建模（Single Device Modeling）

**关键改进：**
- 将电池储能系统建模为单一设备
- 同时考虑电池的充电状态（State of Charge, SoC）
- 更有效地调度存储的能量

**优势：**
- 更准确的系统状态感知
- 更优化的调度决策
- 更好的可靠性保障

### 3. 辅助服务市场整合

储能可以提供的辅助服务：
- **调频服务（Regulation）：** 快速响应频率变化
- **旋转备用（Spinning Reserve）：** 备用容量
- **非旋转备用（Non-Spinning Reserve）：** 快速启动备用
- **无功功率（Reactive Power）：** 电压支持

## 市场效益

### 经济效益
- **预计年度节省：** 超过10亿美元
- **受益方：** 德州全体电力消费者

### 系统效益
1. **更及时的辅助服务采购和管理**
2. **更好的输电拥塞管理**（利用更多种类的资源）
3. **减少人工操作和调度员决策**
4. **替代低效的补充备用市场**

### 可靠性效益
- 更灵活的系统调度
- 更好的资源利用
- 改进的电池储能建模

## 参与主体

### 市场参与者（Market Participants）
- 电池储能资产所有者
- 储能开发商
- 电力营销商

### 准备工作
- 成立RTC+B任务组（RTC+B Task Force, RTCBTF）
- 与利益相关方密切合作
- 进行全面测试和市场试验
- 发布培训视频解释业务流程变化

## 技术细节

### 市场规模
- 截至2025年12月，ERCOT电网：
  - 55,000+英里输电线路
  - 1,460+发电机组
  - 27 million+ 用户
  - 90% 德州电力负荷

### ERCOT长期负荷预测（2026-2032）
- **发布**：2026年4月15日（初步预测）
- **2032年预测**：367,790 MW
- **2023年记录**：85,508 MW（夏季峰值）
- **驱动因素**：数据中心、加密货币挖矿、工业增长、油气需求

### 新市场规则（NPRR系列）
- **NPRR1275**：Firm Fuel Supply Service Phase 3（扩展Qualifying Pipeline定义）
- **NPRR1278**：Advanced Grid Support Service（先进电网支持服务确立为辅助服务）
- **NPRR1309/1310**：Dispatchable Reliability Reserve Service（可调度可靠性储备服务）

### 储能参与情况
- 2025年12月实时数据显示：
  - 太阳能：0 MW（夜间）
  - 风电：18,442 MW
  - 储能放电：-1,630 MW（负值表示放电）
  - 储能装机容量：17,934 MW

## 与其他市场的对比

| 特征 | ERCOT RTC+B | CAISO | PJM |
|------|-------------|-------|-----|
| **储能参与能量市场** | ✓ 实时共优化 | ✓ | ✓ |
| **储能参与辅助服务** | ✓ 实时共优化 | ✓ | 发展中 |
| **储能作为单一设备建模** | ✓ | ✓ | 发展中 |
| **实时共优化** | ✓ | 部分 | 部分 |

## 对光伏+储能的含义

### 优势
1. **更好的经济回报：** 储能可以同时在两个市场中获利
2. **更灵活的调度：** 根据市场价格和系统需求优化充放电策略
3. **更高的系统价值：** 帮助解决光伏间歇性问题

### 商业模式变化
- **Solar Plus Storage项目：** 可以同时参与能量和辅助服务市场
- **收入来源多元化：** 不再依赖单一的能源套利

## 未来发展

### PUCT项目编号
- **Project No. 48540：** "Review of Real-Time Co-optimization in the ERCOT Market"

### 后续计划
- 通过技术顾问委员会（TAC）继续讨论优先推进的举措
- 进一步完善市场设计和规则

## 相关概念

- **Real-Time Nodal Market：** 实时节点市场（ERCOT采用的市场模式）
- **LMP（Locational Marginal Pricing）：** 节点边际定价
- **Ancillary Services：** 辅助服务
- **State of Charge (SoC)：** 电池充电状态
- **BESR（Battery Energy Storage Resource）：** 电池储能资源
- **PUCT：** Public Utility Commission of Texas（德州公共事业委员会）

## 关联页面

- [[ancillary-services-market]] - 辅助服务市场：储能可参与的辅助服务类型
- [[electricity-markets-day-ahead-real-time]] - 电力市场类型：ERCOT 无日前市场的特殊性
- [[interconnection-renewable-comparison]] - 三大互联系统对比：ERCOT 与其他系统的储能政策差异

---
*最后更新：2026-05-07*
*来源：ERCOT, FERC, SEERC, EIA*

---

# English Version

# ERCOT Real-Time Co-optimization Plus Batteries (RTC+B) Market Mechanism

## Overview

RTC+B (Real-Time Co-optimization Plus Batteries) is the most significant upgrade to the ERCOT electricity market since the 2010 Real-Time Nodal market design, officially launched on **December 5, 2025**. This mechanism allows energy storage systems to simultaneously participate in the energy market and the ancillary services market, achieving real-time co-optimized dispatch.

## Background

### Development History
- **2019:** PUCT directed ERCOT to conduct a cost-benefit assessment of Real-Time Co-optimization (RTC)
- **Assessment results:** Found that RTC could bring significant market efficiency and reliability improvements
- **Market expansion:** As Battery Energy Storage Resources (BESRs) grew rapidly in the ERCOT market, the RTC project was expanded to RTC+B
- **December 5, 2025:** RTC+B officially launched

### Design Objectives
1. Improve real-time procurement efficiency
2. Optimize ancillary services procurement and management
3. Improve energy storage modeling and dispatch
4. Reduce manual operations and dispatcher decision burden

## Core Mechanism

### 1. Real-Time Co-optimization

**Traditional model:**
- Energy market and ancillary services market operate independently
- Energy storage needs to compete in these two markets separately
- May lead to inefficient resource allocation

**RTC+B model:**
- Simultaneously optimizes energy and ancillary services procurement in the real-time market
- System can consider all available capabilities of energy storage at once
- Automatically finds the optimal resource combination

### 2. Single Device Modeling for Energy Storage

**Key improvement:**
- Models battery energy storage systems as a single device
- Simultaneously considers the battery's State of Charge (SoC)
- More effectively dispatches stored energy

**Advantages:**
- More accurate system state awareness
- More optimized dispatch decisions
- Better reliability assurance

### 3. Ancillary Services Market Integration

Ancillary services energy storage can provide:
- **Regulation:** Fast response to frequency changes
- **Spinning Reserve:** Backup capacity
- **Non-Spinning Reserve:** Fast-start backup
- **Reactive Power:** Voltage support

## Market Benefits

### Economic Benefits
- **Estimated annual savings:** Over $1 billion
- **Beneficiaries:** All Texas electricity consumers

### System Benefits
1. **More timely ancillary services procurement and management**
2. **Better transmission congestion management** (using more types of resources)
3. **Reduced manual operations and dispatcher decisions**
4. **Replaced inefficient supplemental reserve market**

### Reliability Benefits
- More flexible system dispatch
- Better resource utilization
- Improved battery energy storage modeling

## Participating Entities

### Market Participants
- Battery energy storage asset owners
- Energy storage developers
- Power marketers

### Preparation Work
- Established RTC+B Task Force (RTCBTF)
- Close collaboration with stakeholders
- Comprehensive testing and market trials
- Published training videos explaining business process changes

## Technical Details

### Market Scale
- As of December 2025, ERCOT grid:
  - 55,000+ miles of transmission lines
  - 1,460+ generation units
  - 27 million+ customers
  - 90% of Texas electricity load

### ERCOT Long-Term Load Forecast (2026-2032)
- **Published:** April 15, 2026 (preliminary forecast)
- **2032 forecast:** 367,790 MW
- **2023 record:** 85,508 MW (summer peak)
- **Drivers:** Data centers, cryptocurrency mining, industrial growth, oil & gas demand

### New Market Rules (NPRR Series)
- **NPRR1275:** Firm Fuel Supply Service Phase 3 (expanded Qualifying Pipeline definition)
- **NPRR1278:** Advanced Grid Support Service (established as ancillary service)
- **NPRR1309/1310:** Dispatchable Reliability Reserve Service

### Energy Storage Participation
- December 2025 real-time data shows:
  - Solar: 0 MW (nighttime)
  - Wind: 18,442 MW
  - Storage discharge: -1,630 MW (negative indicates discharge)
  - Storage installed capacity: 17,934 MW

## Comparison with Other Markets

| Feature | ERCOT RTC+B | CAISO | PJM |
|---------|-------------|-------|-----|
| **Storage participation in energy market** | ✓ Real-time co-optimized | ✓ | ✓ |
| **Storage participation in ancillary services** | ✓ Real-time co-optimized | ✓ | Developing |
| **Storage as single device modeling** | ✓ | ✓ | Developing |
| **Real-time co-optimization** | ✓ | Partial | Partial |

## Implications for Solar + Storage

### Advantages
1. **Better economic returns:** Energy storage can profit from both markets simultaneously
2. **More flexible dispatch:** Optimize charge/discharge strategies based on market prices and system needs
3. **Higher system value:** Help solve photovoltaic intermittency problems

### Business Model Changes
- **Solar Plus Storage projects:** Can participate in both energy and ancillary services markets simultaneously
- **Diversified revenue sources:** No longer dependent solely on energy arbitrage

## Future Development

### PUCT Project Number
- **Project No. 48540:** "Review of Real-Time Co-optimization in the ERCOT Market"

### Follow-up Plans
- Continue discussing priority initiatives through the Technical Advisory Committee (TAC)
- Further improve market design and rules

## Related Concepts

- **Real-Time Nodal Market:** ERCOT's market model
- **LMP (Locational Marginal Pricing):** Locational Marginal Pricing
- **Ancillary Services:** Ancillary services
- **State of Charge (SoC):** Battery State of Charge
- **BESR (Battery Energy Storage Resource):** Battery Energy Storage Resource
- **PUCT:** Public Utility Commission of Texas

## Related Pages

- [[ancillary-services-market]] - Ancillary Services Market: Types of ancillary services energy storage can participate in
- [[electricity-markets-day-ahead-real-time]] - Electricity Market Types: ERCOT's uniqueness without a day-ahead market
- [[interconnection-renewable-comparison]] - Three Major Interconnections Comparison: ERCOT's energy storage policy differences from other systems

---
*Last updated: 2026-05-07*
*Sources: ERCOT, FERC, SEERC, EIA*
