# 需求响应经济学与电网灵活性市场

> **English:** Demand Response Economics and Grid Flexibility
> **前置条件：** [[locational-marginal-pricing]]，[[capacity-market-design]]，[[storage-economics]]

---

## 1. 概述：需求响应作为一种电网资源

需求响应（Demand Response, DR）是指最终用户根据价格信号或可靠性事件改变电力消费的行为。DR不是通过建设更多发电容量来满足峰值需求，而是减少或转移负荷——以更低的成本实现相同的可靠性结果。

**基本洞察：** 电力无法以合理的成本大量存储（储能设备除外）。电网必须实时平衡供需。用发电满足峰值需求的成本为$500-1,000/kW（调峰资本+燃料）。通过DR实现相同的峰值削减成本为$100-300/kW（要求客户减少几小时用电的成本）——通常DR是更便宜的选择。

**经济价值主张：**
- 减少峰值需求 → 避免建设昂贵的调峰机组
- 提供频率调节 → 支持电网稳定（如电池）
- 将负荷转移到非高峰时段 → 降低供电平均成本
- 减少批发价格波动 → 降低公用事业采购成本

---

## 2. 需求响应的类型

### 2.1 基于价格的需求响应

基于价格的DR使用可变电价来激励客户转移消费：

**分时电价（TOU）：**
- 高峰时段（如工作日下午4-9点）价格较高
- 非高峰时段（夜间、周末）价格较低
- 减少峰值需求3-8%（客户对可预测的价格信号做出反应）
- 常见于：加州、纽约、大多数具有高级计量基础设施的重组市场

**关键峰值定价（CPP）：**
- 大多数时候按正常TOU价格
- 在关键事件（炎热天气、电网压力）期间，价格飙升到$0.50-1.00/kWh，持续4-8小时
- 使用者：加州公用事业、AEP俄亥俄州、杜克能源卡罗来纳州
- 通常在关键事件期间实现5-15%的负荷削减

**实时定价（RTP）：**
- 随批发市场价格条件变化的每小时（或亚小时）价格
- 客户实时看到实际电力成本
- 需要间隔计量表和自动化才能有效
- 在PJM：大型工商业客户（需求>300 kW）可以选择RTP
- 在高价时段减少需求5-15%

### 2.2 基于激励的需求响应

基于激励的DR向客户支付费用，要求其按需减少负荷：

**紧急/可削减负荷响应：**
- 客户签订合同，在电网紧急情况下减少负荷
- 支付：容量支付（$/kW-月）+ 事件能源支付（$/kWh削减量）
- 不合规处罚
- 在PJM：约有5,000 MW的可削减/紧急DR在容量市场中清算

**负荷竞价/拍卖：**
- 客户像发电机一样将负荷削减出价进入批发市场
- 被接受的出价在稀缺事件期间被调用
- 在CAISO和MISO市场中可用
- CAISO需求响应：约有1,000-2,000 MW可用

**辅助服务需求响应：**
- DR提供向上/向下调节（如电池）
- 比传统DR更快（1-5分钟响应 vs 10-30分钟）
- 在ERCOT："可调度需求"可与电池一起提供Reg-D服务
- PJM：需求资源可提供一级（同步备用）和二级（非同步备用）

### 2.3 电表后端 vs. 电表前端

**电表后端（BTM）：**
- 屋顶太阳能+储能+智能恒温器自动化
- 客户减少其电网消耗而公用事业不知情
- "鸭子曲线"部分由BTM太阳能减少下午峰值需求驱动
- BTM资源除非聚合，否则对批发市场不可见

**电表前端（FTM）：**
- 公用事业规模的需求响应项目
- 聚合商签约客户并提供需求削减作为产品
- 聚合商代表小型客户群体（住宅+小型商业）在批发市场中
- FTM DR可由RTO/ISO调度

---

## 3. 需求响应的经济学

### 3.1 成本效益分析

**需求响应的成本：**

DR的"全成本"包括：
- 项目管理：$10-30/kW-年（公用事业管理费用、客户注册、验证）
- 客户激励：$50-200/kW-年（客户削减意愿的报酬）
- 监测/验证：$5-15/kW-年（计量、基线计算）
- 客户设备（智能恒温器、自动化）：$20-100/kW（如果尚未安装）

**DR总成本范围：$100-300/kW-年的承诺容量**

**需求响应的规避成本：**
DR避免了以下需要：
- 调峰发电：约$600-1,000/kW资本+燃料成本
- 输配电升级：$500-2,000/kW（取决于地点）
- 容量市场成本：在PJM为$30-80/kW-年

**效益成本比：** 研究一致发现DR项目的BCR为2:1到8:1：
- CPUC估计加州DR项目：每年约$15-30亿的净效益
- Brattle Group（2021年）：到2030年，国家的DR潜力为60-100 GW，成本为$50-150/kW-年
- 关键不确定性：有多少"规避成本"是真实的（替代实际容量投资）vs重复计算（计算无论如何都会发生的好处）

### 3.2 基线问题

**我们如何衡量DR表现？**

关键计量问题：**如果没有DR事件，客户会消耗多少？**

```
DR表现 = 基线消耗 - 事件期间实际消耗
```

**基线方法：**
- **最近5个类似日的平均值：** 最常见；取最近5个非事件工作日的平均消耗
- **调整：** 天气标准化、星期几调整、客户特定因素
- **无基线（Calipless）：** 无基线调整；按事件期间计量消耗支付

**操纵问题：**
如果客户知道可能会发生DR事件，他们可能会提前给建筑物降温或提前运行设备——人为地夸大基线。当事件开始时，看起来他们削减得比实际多。这是操纵，而非效率。

**搭便车问题：**
有些客户在DR事件期间本来就会减少消耗（例如，因为天气炎热，他们自然会少用）。这些"搭便车者"因他们本来就会做出的削减而获得报酬。DR项目难以衡量和排除搭便车者。

### 3.3 客户细分和DR潜力

| 细分市场 | 负荷形状 | DR潜力 | 响应性 |
|---|---|---|---|
| 住宅（HVAC） | 高傍晚峰值 | 中等（5-15%削减） | 恒温器自动化 |
| 住宅（热水器） | 夜间峰值（燃气） | 电热低 | 智能热水器控制 |
| 小型商业 | 日间峰值 | 中等 | 自动化EMS |
| 大型商业 | 24/7有峰值日 | 高（10-30%） | 楼宇自动化、工艺转移 |
| 工业 | 工艺依赖 | 非常高（15-40%） | 转移生产、现场发电 |
| 数据中心 | 24/7 | 高（20-50%） | 负荷转移、UPS管理 |

**自动化革命：**
早期DR需要客户手动操作（关灯、调节恒温器）。现代DR使用：
- 智能恒温器（Nest、EcoBee）：自动化、预编程响应
- 楼宇管理系统（BMS）：无需人工干预的自动化需求削减
- 工业过程控制：围绕DR事件自动安排生产

这种自动化显著降低了客户摩擦并提高了DR表现。

---

## 4. 批发市场中的需求响应

### 4.1 PJM的需求资源项目

PJM拥有美国最成熟的DR框架：

**容量市场参与：**
- 需求资源可以在PJM的RPM拍卖中提供容量
- 必须在容量年峰值期间承诺负荷削减
- DR的ELCC：类似于储能；注册MW的10-15%计为可靠容量
- 截至2024年：约有8,000-10,000 MW的DR注册在PJM容量市场

**紧急和可削减项目：**
- PJM约有5,000 MW的"紧急负荷响应"
- 参与者获得容量支付 + 事件期间能源支付
- PJM每年最多可调度紧急负荷响应100小时
- 事件通常持续1-6小时

**LMP中的价格响应需求：**
PJM的大型工商业客户（>300 kW）可选择暴露于实时LMP
- 这创造了自动DR：当实时价格飙升时，自动化系统削减负荷
- 然而，只有约10-15%的符合条件客户选择实时定价（其余偏好固定费率）

### 4.2 CAISO需求响应

CAISO的DR框架反映了加州的电网挑战：

**代理需求资源（PDR）：**
- 聚合商可将DR作为供电侧资源在CAISO市场中提供
- PDR参与日前和实时市场
- 截至2024年：CAISO约有2,000-3,000 MW的PDR
- 结算：基于调度期间计量负荷削减

**需求响应拍卖机制（DRAM）：**
- CPUC通过年度拍卖采购需求响应
- 聚合商以最低价格提供需求削减的竞争
- 约有1,000-2,000 MW通过DRAM采购

**CA鸭子曲线给DR带来的挑战：**
CAISO的鸭子曲线意味着关键峰值现在是傍晚时段（下午6-9点），此时太阳能产出已崩溃。早间峰值的DR（曾经是挑战）变得不那么重要；傍晚峰值DR更有价值，但客户更难提供（HVAC仍在运行、烹饪等）。

### 4.3 ERCOT需求响应

ERCOT的需求响应是独特的：

**紧急和需求响应（EDR）：**
- ERCOT有紧急需求响应项目
- 参与者因在ERCOT紧急情况下减少负荷而获得报酬
- Uri（2021年）之后，ERCOT扩大了EDR并创建了"作为资源的负荷"（LOADRES）
- 目前：ERCOT约有1,500-2,500 MW的需求响应可用

**可调度需求：**
- 大型工商业客户（>10 MW）可注册为"可调度需求"
- 这些客户可以像发电机一样被调度——既减少也增加负荷
- 这使其能够参与ERCOT的辅助服务市场

**市场设计差距：**
与PJM和CAISO不同，ERCOT的需求响应项目不太发达，因为：
- ERCOT历史上依赖价格信号（ORDC）而非明确的DR调度
- 德州零售选择意味着客户有固定零售费率，与实时批发价格绝缘
- 聚合商在为住宅/小型工商业客户签约DR项目方面机会较少

---

## 5. 需求响应 vs. 储能：比较分析

### 5.1 功能等价性

DR和储能为电网提供许多相同的服务：

| 服务 | 储能 | 需求响应 |
|---|---|---|
| 峰值削减 | 是（放电） | 是（削减） |
| 能源时间转移 | 是（充电/放电） | 是（负荷转移） |
| 频率调节 | 是（快速响应） | 是（较慢、不太精确） |
| 备用（旋转/非旋转） | 是 | 是（有限） |
| 容量价值 | 是（基于ELCC） | 是（基于ELCC） |

### 5.2 成本比较

| | 4小时电池（100 MW / 400 MWh） | 100 MW 需求响应 |
|---|---|---|
| 资本成本 | 约$1.4亿 | 约$500-1500万（项目管理+客户激励） |
| 运维成本 | $5-800万/年 | $500-1500万/年 |
| 能源成本 | $0（从电网充电） | 客户承担机会成本 |
| 可靠性 | 可按信号调度 | 需要客户配合 |
| 灵活性 | 充电 AND 放电 | 只能削减 |
| 寿命 | 10-15年 | 无限期（持续项目成本） |

**储能优势：**
- 可调度（您控制它）
- 还可以充电并提供向上灵活性
- 可参与频率调节

**DR优势：**
- 更便宜（"虚拟"容量无资本成本）
- 无充电能源成本
- 可通过项目设计扩大/缩小

**关键洞察：** DR和储能是互补的，不是替代品。电网两者都需要。DR减少总容量需求；储能解决时长和可调度性差距。

### 5.3 最优组合

**DR的布雷斯悖论：**
如果部署过多DR，实际上可能以意想不到的方式增加峰值价格：
- DR在高价格时段减少需求
- 但如果DR参与者同时削减，剩余负荷更平稳
- 这降低了价格波动，降低了储能套利收入，降低了储能投资
- 如果DR项目设计不当，对系统成本的净影响可能是负面的

**正确的框架：** 按总系统成本比较DR和储能，而非仅按单个项目成本。

---

## 6. 需求响应参与的障碍

### 6.1 市场和监管障碍

**RTO/ISO市场规则：**
- 一些市场限制小型DR聚合（最低规模要求）
- FERC Order 719（2008年）要求RTO接受DR出价，但实施各异
- FERC Order 2222（2020年）要求DER聚合商（包括DR）参与批发市场——全面实施正在进行中

**公用事业阻力：**
- 从资本基础设施中获利的公用事业可能反对DR（它减少了他们的资产基础）
- DR造成的损失收入（如果客户减少消耗）可能无法通过费率调整完全收回
- "收入脱钩"机制旨在解决这一问题——将公用事业利润与销售量分离

**计量和通信基础设施：**
- 准确的DR计量需要间隔计量表（15分钟或更高）
- 并非所有客户都有高级计量基础设施（AMI）
- 调度DR的通信系统必须可靠和安全

### 6.2 客户障碍

**认知和教育：**
- 大多数客户不知道DR项目存在
- 客户不理解他们的行为如何影响电网

**分裂激励（房东-租户）：**
- 建筑业主支付效率升级费用；租户支付电费
- 如果租户获得账单节省，房东就没有动力参与DR项目
- PACE（房产评估清洁能源）项目解决了效率问题但未解决DR

**客户成熟度：**
- 有能源经理和楼宇自动化的大型工商业客户可以轻松参与
- 小型商业和住宅客户缺乏基础设施和专业知识
- 聚合使小客户能够参与——但增加了成本和复杂性

---

## 7. 定量数据摘要

| 指标 | PJM | CAISO | ERCOT | MISO |
|---|---|---|---|---|
| 注册DR（2024年） | 约10,000 MW | 约3,000 MW | 约2,500 MW | 约5,000 MW |
| 主要项目类型 | 容量市场+紧急 | PDR+DRAM | EDR+LOADRES | 紧急+经济 |
| 平均DR成本（$/kW-年） | $100-200 | $150-300 | $100-250 | $80-180 |
| 实现的负荷削减 | 注册量的3-8% | 注册量的5-12% | 注册量的5-10% | 注册量的3-8% |
| 每年最大事件小时 | 100 | 120 | 60 | 100 |
| 平均事件持续时间 | 2-4小时 | 2-6小时 | 2-4小时 | 2-4小时 |
| 渗透率（占峰值） | 约8-10% | 约5-7% | 约3-5% | 约5-8% |

---

## 8. 开放研究问题

1. **最优DR产品设计：** DR项目应设计为容量产品、能源产品还是辅助服务？对于给定电网，最优产品组合是什么？
2. **DR与价格形成：** 当大量DR参与批发市场时，它如何影响价格形成？DR会使价格波动更大还是更小？
3. **住宅DR可扩展性：** 智能恒温器项目（Nest等）能否扩展以提供有意义的电网服务？每个设备的实际负荷削减是多少，它如何随温度和客户行为变化？
4. **基线操纵：** 基线操纵有多显著？能否在不过度增加项目成本的情况下检测和防止？
5. **DR作为输电资产：** DR项目能否用作"非线路替代方案"来推迟输电升级？应如何评估和采购？
6. **DR获取的公平性：** 低收入和EJ社区能否参与DR项目？如果不能，什么针对性项目可以弥合这一差距？
7. **需求响应的长期弹性：** 随着动态定价变得更加普遍，客户的反应会随着时间推移而增强（学习），还是习惯限制长期响应性？

---

## 9. 关键参考文献

- FERC (2024). *Assessment of Demand Response and Energy Efficiency Resources* — 年度报告
- CAISO (2024). *Demand Response and Energy Efficiency Metrics*
- PJM (2024). *PJM Demand Side Response Market Activity Report*
- New York ISO (2024). *Demand Response Program Status*
- Brattle Group (2021). *The National Potential for Demand Response*
- Borenstein, S. (2014). "The Economics of Fixed vs. Variable Electricity Prices." *Journal of Regulatory Economics* 46.
- Wolak, F.A. (2011). "Do Residential Customers Respond to Real-Time Prices?" *American Economic Review* 101(3).
- Jessoe, K. & Rapson, D. (2014). "Commercial and Residential Electricity Prices." *Journal of Law and Economics* 57.

---

*最后更新：2026-05-07*
*相关：[[storage-economics]]，[[capacity-market-design]]，[[locational-marginal-pricing]]，[[environmental-justice-energy]]*

---

# English Version

# Demand Response Economics and Grid Flexibility Markets

> **Prerequisites:** [[locational-marginal-pricing]], [[capacity-market-design]], [[storage-economics]]

---

## 1. Overview: Demand Response as a Grid Resource

Demand response (DR) refers to changes in electricity consumption by end-use customers in response to price signals or reliability events. Rather than building more generation capacity to meet peak demand, DR reduces or shifts load — achieving the same reliability outcome at lower cost.

**The fundamental insight:** Electricity cannot be stored in meaningful quantities at reasonable cost (except storage devices). The grid must balance supply and demand in real-time. Meeting peak demand with generation costs $500-1,000/kW (peaker capital + fuel). Meeting the same peak reduction through DR costs $100-300/kW (the cost of asking customers to reduce for a few hours) — often the cheaper option.

**The economic value proposition:**
- Reduce peak demand → avoid building expensive peakers
- Provide frequency regulation → support grid stability (like a battery)
- Shift load to off-peak hours → reduce average cost of serving load
- Reduce wholesale price volatility → lower procurement costs for utilities

---

## 2. Types of Demand Response

### 2.1 Price-Based Demand Response

Price-based DR uses time-varying electricity prices to incentivize customers to shift consumption:

**Time-of-Use (TOU) Pricing:**
- Higher prices during peak hours (e.g., 4pm-9pm weekdays)
- Lower prices during off-peak hours (nights, weekends)
- Reduces peak demand by 3-8% (customers respond to predictable price signals)
- Common in: California, New York, most restructured markets with advanced metering

**Critical Peak Pricing (CPP):**
- Normal TOU prices most of the time
- During critical events (hot days, grid stress), prices spike to $0.50-1.00/kWh for 4-8 hours
- Used by: California utilities, AEP Ohio, Duke Energy Carolinas
- Typically achieves 5-15% load reduction during critical events

**Real-Time Pricing (RTP):**
- Hourly (or sub-hourly) prices that vary with wholesale market conditions
- Customers see their actual cost of electricity in real-time
- Requires interval meters and automation to be effective
- In PJM: Large C&I customers (>300 kW demand) can choose RTP
- Reduces demand during high-price hours by 5-15%

### 2.2 Incentive-Based Demand Response

Incentive-based DR pays customers to reduce load on demand:

**Emergency/Curtailable Load Response:**
- Customers sign contracts to reduce load during grid emergencies
- Payment: Capacity payment ($/kW-month) + event-based energy payment ($/kWh curtailed)
- Penalties for non-compliance
- In PJM: ~5,000 MW of curtailable/emergency DR cleared in capacity market

**Demand Bidding/Auction:**
- Customers bid load reductions into the wholesale market (like generators)
- Accepted bids are called during scarcity events
- Available in CAISO and MISO markets
- CAISO demand response: ~1,000-2,000 MW available

**Ancillary Services Demand Response:**
- DR providing regulation up/down (like a battery)
- Faster than traditional DR (1-5 minute response vs. 10-30 minute)
- In ERCOT: "Dispatchable Demand" can provide Reg-D services alongside batteries
- PJM: Demand Resources can provide Tier 1 (synchronized reserves) and Tier 2 (non-synchronized reserves)

### 2.3 Behind-the-Meter vs. Front-of-Meter

**Behind-the-Meter (BTM):**
- Rooftop solar + storage + smart thermostat automation
- Customer reduces their grid consumption without the utility's awareness
- The "duck curve" is partially driven by BTM solar reducing afternoon peak demand
- BTM resources are invisible to the wholesale market unless aggregated

**Front-of-Meter (FTM):**
- Utility-scale demand response programs
- Aggregators sign up customers and offer demand reduction as a product
- Aggregators represent groups of small customers (residential + small commercial) in wholesale markets
- FTM DR is dispatchable by the RTO/ISO

---

## 3. The Economics of Demand Response

### 3.1 Cost-Benefit Analysis

**The cost of demand response:**

The "all-in" cost of DR includes:
- Program administration: $10-30/kW-year (utility overhead, customer enrollment, verification)
- Customer incentives: $50-200/kW-year (customer payment for willingness to curtail)
- Monitoring/verification: $5-15/kW-year (metering, baseline calculation)
- Customer equipment (smart thermostats, automation): $20-100/kW (if not already installed)

**Total DR cost range: $100-300/kW-year of committed capacity**

**The avoided cost of demand response:**
DR avoids the need for:
- Peaker generation: ~$600-1,000/kW capital + fuel costs
- Transmission/distribution upgrades: $500-2,000/kW depending on location
- Capacity market costs: $30-80/kW-year (in PJM)

**The benefit-cost ratio:** Studies consistently find DR programs have BCRs of 2:1 to 8:1:
- CPUC estimates California DR programs: ~$1.5-3 billion in annual net benefits
- Brattle Group (2021): National DR potential of 60-100 GW by 2030 at $50-150/kW-year
- The key uncertainty: how much of the "avoided cost" is real (displacing actual capacity investment) vs. counted twice (counting benefits that would have occurred anyway)

### 3.2 The Baseline Problem

**How do we measure DR performance?**

The critical measurement issue: **What would the customer have consumed without the DR event?**

```
DR Performance = Baseline Consumption - Actual Consumption During Event
```

**Baseline methodologies:**
- **Average of last 5 similar days:** Most common; takes average consumption of the 5 most recent non-event weekdays
- **Adjustments:** Weather normalization, adjust for day-of-week, customer-specific factors
- **Calipless:** No baseline adjustment; pays based on metered consumption during event

**The gaming problem:**
If customers know a DR event is likely, they may pre-cool their building or run equipment early — artificially inflating the baseline. When the event starts, they look like they're reducing more than they actually are. This is gaming, not efficiency.

**The free-rider problem:**
Some customers would have reduced consumption anyway during a DR event (e.g., because it's a hot day and they'd naturally use less). These "free riders" get paid for reductions they would have made without the program. DR programs struggle to measure and exclude free riders.

### 3.3 Customer Segmentation and DR Potential

| Segment | Load Shape | DR Potential | Responsiveness |
|---|---|---|---|
| Residential (HVAC) | High evening peak | Medium (5-15% reduction) | Thermostat automation |
| Residential (water heating) | Night peak (gas) | Low in electric | Smart water heater control |
| Small Commercial | Daytime peak | Medium | Automated EMS |
| Large Commercial | 24/7 with peak days | High (10-30%) | Building automation, process shifting |
| Industrial | Process-dependent | Very High (15-40%) | Shift production, on-site gen |
| Data Centers | 24/7 | High (20-50%) | Load shifting, UPS management |

**The automation revolution:**
Early DR required manual customer actions (turning off lights, adjusting thermostats). Modern DR uses:
- Smart thermostats (Nest, EcoBee): Automated, pre-programmed responses
- Building Management Systems (BMS): Automated demand shed without human intervention
- Industrial process control: Automated production scheduling around DR events

This automation dramatically reduces customer friction and improves DR performance.

---

## 4. Demand Response in Wholesale Markets

### 4.1 PJM's Demand Resource Programs

PJM has the most mature DR framework in the US:

**Capacity Market Participation:**
- Demand Resources can offer capacity in PJM's RPM auctions
- Must commit to load reduction during capacity-year peaks
- ELCC for DR: Similar to storage; 10-15% of enrolled MW counts as firm capacity
- As of 2024: ~8,000-10,000 MW of DR enrolled in PJM capacity market

**Emergency and Curtailable Programs:**
- ~5,000 MW of "Emergency Load Response" in PJM
- Participants receive capacity payment + energy payment during events
- PJM can dispatch Emergency Load Response up to 100 hours/year
- Events typically last 1-6 hours

**Price-responsive demand in LMP:**
PJM's large C&I customers (>300 kW) can choose to be exposed to real-time LMP
- This creates automatic DR: when real-time prices spike, automated systems shed load
- However, only ~10-15% of eligible customers opt for real-time pricing (the rest prefer fixed rates)

### 4.2 CAISO Demand Response

CAISO's DR framework reflects California's grid challenges:

**Proxy Demand Resource (PDR):**
- Aggregators can offer DR as a supply-side resource in CAISO markets
- PDR participates in both day-ahead and real-time markets
- As of 2024: ~2,000-3,000 MW of PDR in CAISO
- Settlement: Based on metered load reduction during dispatch

**Demand Response Auction Mechanism (DRAM):**
- CPUC procures demand response through an annual auction
- Aggregators compete to provide demand reduction at the lowest price
- ~1,000-2,000 MW procured through DRAM

**The CA duck curve challenge for DR:**
CAISO's duck curve means the critical peak is now the evening hours (6-9pm), when solar output has collapsed. DR for morning peak (which used to be the challenge) is less relevant; evening peak DR is more valuable but harder for customers to provide (HVAC is still running, cooking, etc.).

### 4.3 ERCOT Demand Response

ERCOT's demand response is unique:

**Emergency and Demand Response (EDR):**
- ERCOT has an Emergency Demand Response program
- Participants receive payments for load reduction during ERCOT emergencies
- After Uri (2021), ERCOT expanded EDR and created "Load Acting as a Resource" (LOADRES)
- Currently: ~1,500-2,500 MW of demand response available in ERCOT

**Dispatchable Demand:**
- Large C&I customers (>10 MW) can register as "Dispatchable Demand"
- These customers can be dispatched like a generator — both reduce AND increase load
- This enables participation in ERCOT's ancillary services markets

**The market design gap:**
Unlike PJM and CAISO, ERCOT's demand response programs are less well-developed due to:
- ERCOT's historical reliance on price signals (ORDC) rather than explicit DR dispatch
- Texas retail choice means customers have fixed retail rates and are insulated from real-time wholesale prices
- Aggregators have less opportunity to sign up residential/small C&I customers for DR programs

---

## 5. Demand Response vs. Storage: A Comparative Analysis

### 5.1 Functional Equivalence

DR and storage provide many of the same grid services:

| Service | Storage | Demand Response |
|---|---|---|
| Peak reduction | Yes (discharge) | Yes (curtailment) |
| Energy time-shift | Yes (charge/discharge) | Yes (load shifting) |
| Frequency regulation | Yes (fast response) | Yes (slower, less precise) |
| Reserves (spinning/non-spin) | Yes | Yes (limited) |
| Capacity value | Yes (ELCC-based) | Yes (ELCC-based) |

### 5.2 Cost Comparison

| | 4-hour Battery (100 MW / 400 MWh) | 100 MW Demand Response |
|---|---|---|
| Capital cost | ~$140 million | ~$5-15 million (program admin + customer incentives) |
| O&M cost | $5-8M/year | $5-15M/year |
| Energy cost | $0 (charged from grid) | Customer bears opportunity cost |
| Reliability | Dispatchable on signal | Requires customer compliance |
| Flexibility | Charge AND discharge | Only curtail |
| Lifespan | 10-15 years | Indefinite (ongoing program cost) |

**The storage advantage:**
- Dispatchable (you control it)
- Can also charge and provide upward flexibility
- Can participate in frequency regulation

**The DR advantage:**
- Much cheaper (no capital cost for "virtual" capacity)
- No energy costs to charge
- Can be scaled up/down by program design

**The key insight:** DR and storage are complements, not substitutes. The grid needs both. DR reduces the total capacity requirement; storage addresses the duration and dispatchability gap.

### 5.3 The Optimal Mix

**The Braess paradox of DR:**
If too much DR is deployed, it can actually increase peak prices in unexpected ways:
- DR reduces demand during high-price hours
- But if DR participants all reduce at the same time, the remaining load is smoother
- This reduces price volatility, which reduces storage arbitrage revenue, which reduces storage investment
- The net effect on system costs can be negative if DR programs are poorly designed

**The right framework:** Compare DR and storage on a total system cost basis, not just individual program cost basis.

---

## 6. Barriers to Demand Response Participation

### 6.1 Market and Regulatory Barriers

**RTO/ISO market rules:**
- Some markets restrict small DR aggregation (minimum size requirements)
- FERC Order 719 (2008) required RTOs to accept DR bids, but implementation varies
- FERC Order 2222 (2020) required DER aggregators (including DR) to participate in wholesale markets — full implementation ongoing

**Utility resistance:**
- Utilities that earn a return on capital infrastructure may oppose DR (it reduces their asset base)
- Lost revenue from DR (if customers reduce consumption) may not be fully recovered through rate adjustments
- "Revenue decoupling" mechanisms are designed to address this — separating utility profit from sales volume

**Metering and communication infrastructure:**
- Accurate DR measurement requires interval meters (15-minute or better)
- Not all customers have advanced metering infrastructure (AMI)
- Communication systems to dispatch DR must be reliable and secure

### 6.2 Customer Barriers

**Awareness and education:**
- Most customers don't know DR programs exist
- Customers don't understand how their behavior affects the grid

**Split incentives (landlord-tenant):**
- The building owner pays for efficiency upgrades; the tenant pays for electricity
- The landlord has no incentive to participate in DR programs if the tenant gets the bill savings
- PACE (Property Assessed Clean Energy) programs address this for efficiency but not DR

**Customer sophistication:**
- Large C&I customers with energy managers and building automation can easily participate
- Small commercial and residential customers lack the infrastructure and expertise
- Aggregation enables small customers to participate — but adds cost and complexity

---

## 7. Quantitative Data Summary

| Metric | PJM | CAISO | ERCOT | MISO |
|---|---|---|---|---|
| Enrolled DR (2024) | ~10,000 MW | ~3,000 MW | ~2,500 MW | ~5,000 MW |
| Primary program type | Capacity market + emergency | PDR + DRAM | EDR + LOADRES | Emergency + economic |
| Avg. DR cost ($/kW-yr) | $100-200 | $150-300 | $100-250 | $80-180 |
| Load reduction achieved | 3-8% of enrolled | 5-12% of enrolled | 5-10% of enrolled | 3-8% of enrolled |
| Max event hours/year | 100 | 120 | 60 | 100 |
| Average event duration | 2-4 hours | 2-6 hours | 2-4 hours | 2-4 hours |
| Penetration (% of peak) | ~8-10% | ~5-7% | ~3-5% | ~5-8% |

---

## 8. Open Research Questions

1. **Optimal DR product design:** Should DR programs be designed as capacity products, energy products, or ancillary services? What's the optimal product mix for a given grid?
2. **DR and price formation:** When large amounts of DR participate in wholesale markets, how does it affect price formation? Does DR make prices more or less volatile?
3. **Residential DR scalability:** Can smart thermostat programs (Nest, etc.) scale to provide meaningful grid services? What's the actual load reduction per device, and how does it vary with temperature and customer behavior?
4. **Baseline manipulation:** How significant is baseline gaming? Can it be detected and prevented without imposing excessive program costs?
5. **DR as a transmission asset:** Can DR programs be used as "non-wires alternatives" to defer transmission upgrades? How should this be evaluated and procured?
6. **Equity of DR access:** Are low-income and EJ communities able to participate in DR programs? If not, what targeted programs could address this gap?
7. **Long-run elasticity of demand response:** As dynamic pricing becomes more widespread, do customers' responses strengthen over time (learning), or does habit limit long-run responsiveness?

---

## 9. Key References

- FERC (2024). *Assessment of Demand Response and Energy Efficiency Resources* — annual report
- CAISO (2024). *Demand Response and Energy Efficiency Metrics*
- PJM (2024). *PJM Demand Side Response Market Activity Report*
- New York ISO (2024). *Demand Response Program Status*
- Brattle Group (2021). *The National Potential for Demand Response*
- Borenstein, S. (2014). "The Economics of Fixed vs. Variable Electricity Prices." *Journal of Regulatory Economics* 46.
- Wolak, F.A. (2011). "Do Residential Customers Respond to Real-Time Prices?" *American Economic Review* 101(3).
- Jessoe, K. & Rapson, D. (2014). "Commercial and Residential Electricity Prices." *Journal of Law and Economics* 57.

---
*Last updated: 2026-05-07*
*Related: [[storage-economics]], [[capacity-market-design]], [[locational-marginal-pricing]], [[environmental-justice-energy]]*
