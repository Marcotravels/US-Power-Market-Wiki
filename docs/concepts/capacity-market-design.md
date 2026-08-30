# 容量市场设计与资源充足性

> **English:** Capacity Market Design and Resource Adequacy
> **前置条件：** [[locational-marginal-pricing]]，[[electricity-markets-day-ahead-real-time]]，[[ercot-rtc-b-market]]

---

## 1. 缺钱问题（The Missing Money Problem）

批发电力市场——无论是PJM的LMP+容量市场还是ERCOT的纯能量市场——必须同时完成两件事：

1. **能量市场：** 以最低成本实时调度现有机组
2. **容量市场/投资信号：** 吸引足够的发电投资，以确保未来需求的资源充足性

**缺钱问题是重组电力市场的根本挑战：** 仅靠能量市场无法为系统可靠性所需的发电容量投资提供足够的收入，而这些容量只在少数高峰时段需要。

**为什么会发生这种情况？**
- 批发电力市场按边际成本（燃料+可变运维）定价
- 高峰时段发生频率较低（大多数市场每年100-400小时）
- 建设调峰机组（燃气燃烧涡轮机）成本高昂（$600-800/kW），但只在这些高峰时段赚钱
- 当高峰时段市场价格飙升时，投资者希望从数百小时的高价中收回年度固定成本——但竞争压力和价格上限限制了价格能涨多高
- **缺钱** = 固定容量成本 - 能量市场能够盈利回收的部分

**可靠性与再调度的权衡：**
- 纯能量市场（ERCOT）依赖稀缺定价——在高峰时段出现非常高的价格，理论上为调峰机组提供资金并激励需求响应
- 容量市场（PJM、NYISO、ISO-NE）提供单独的容量支付，无论能量市场结果如何都能确保固定成本回收

---

## 2. PJM的可靠性定价模型（RPM）

PJM运营着世界上最大的容量市场——**可靠性定价模型（Reliability Pricing Model, RPM）**，该模型于2007年实施，通过多轮基线剩余拍卖（BRA）进行了修改。

### 2.1 拍卖结构

PJM的RPM使用在交付年前三年的**集中式远期容量拍卖**：

```
交付年 t → 拍卖在 t-3 年举行（即"BRA"）
```

**关键拍卖参数：**
- **基线剩余拍卖（BRA）：** 主要拍卖清算机制
- **增量拍卖（IA）：** 在交付年前20、10和3个月举行，以根据需求预测变化和容量增减进行调整
- **趋势备用容量：** PJM目标备用容量高于峰值负荷约15-16%
- **容量清算价格：** 向所有清算容量支付（同一节点交付区内的所有MW获得相同清算价格）

**价格确定：**
- RPM使用**需求曲线**（而非垂直需求曲线）——随着清算数量超过可靠性要求，价格下降
- 这降低了价格波动，同时仍提供投资信号
- 对于PSEG/新泽西地区（受约束区域），适用单独的清算价格

### 2.2 实际拍卖结果和清算价格

| 交付年 | PJM RPM 清算价格 ($/MW-day) | 趋势 |
|--------|---------------------------|------|
| 2012-2014 | $28-80/MW-day | 低价天然气 → 低价格 |
| 2015-2016 | $45-120/MW-day | 中等 |
| 2017-2018 | $100-175/MW-day | 容量退役，需求增加 |
| 2019-2020 | $80-140/MW-day | 稳定 |
| 2021-2022 | $50-270/MW-day（各LDA差异大） | 冬季风暴影响 |
| 2023-2024 | $60-180/MW-day | ORDC增加，可靠性担忧 |

**容量承诺价值：** $100/MW-day ≈ $36,500/MW-year

**PJM自身分析：** 以$100/MW-day的清算价格，新的燃气调峰机组勉强经济（$700/kW资本成本 + 固定运维，回收期约7-10年）。这就是"缺钱"——容量市场提供了收入桥梁。

### 2.3 容量资源性能测试（CRPT）

2014年"极地漩涡"之后，PJM在2018年实施了**容量性能（Capacity Performance）**范式（取代了旧的"基本容量"产品）：

- 资源必须在紧急情况下表现，否则面临严厉处罚
- **非性能收费：** 未按承诺交付的容量收取$5,000/MWh
- **性能支付：** 对超出承诺容量的超额表现给予奖励

这显著提高了清算容量的质量——基于性能的区别化取代了先前类似大宗商品的容量产品。

### 2.4 容量信用与ELCC

对于间歇性资源（太阳能、风能）和储能，容量价值不是其铭牌额定值：

**有效承载容量（ELCC）：**
- ELCC衡量一个资源可靠地替代传统发电机的容量MW数
- PJM中太阳能ELCC：约为铭牌容量的38-50%（取决于容量因子和夏季高峰重合度）
- PJM中风能ELCC：约为铭牌容量的10-20%
- 电池储能ELCC：约为50-80%（4小时电池在高渗透率水平下）

**为什么ELCC对容量市场设计很重要：**
- 如果太阳能获得全部容量信用，容量市场将过度认购，价格将崩溃
- 在高可再生能源渗透率下，每个额外单位的ELCC下降（"先到先得"的收益递减问题）
- 这创造了一个反常的动态：随着太阳能增加，其容量信用下降，需要从其他来源获得更多容量

---

## 3. ERCOT：纯能量市场

ERCOT是美国大型纯能量市场的主要案例（与澳大利亚NEM和阿尔伯塔AESO并列）。

### 3.1 ERCOT的稀缺定价机制

在没有容量市场的情况下，ERCOT依赖**基于敏感度的定价**在稀缺时期发出投资信号：

**ORDC（运营备用需求曲线）：**
- 当备用水平低于阈值时，ERCOT向运营备用增加影子价格
- 随着备用下降，ORDC在系统边际价格上增加高达$9,000/MWh
- 这创造了价格飙升，理论上为调峰机组提供资金并吸引投资

**高持续备用价格（HSRP）：** 2021年冬季风暴后增加：
- 在紧急情况下，高于峰值需求75%的可用容量的每MW收取$2,000/MW
- 为热能发电机提供更可预测的收入来源

**高条件稀缺价格（HCSP）：** 当可调度热能容量相对于可再生能源稀缺时适用。

### 3.2 2021年冬季风暴考验

ERCOT的纯能量市场在2021年2月的冬季风暴Uri期间受到了严峻考验：
- 约450万客户断电
- 现货价格达到$9,000/MWh的价格上限
- 估计经济损失：$230-1350亿（取决于计算方法）
- 设法运行的发电机获得了非凡利润；未能运行的发电机面临固定成本但没有收入

**性能差距：** 一些燃气机组被冻住，揭示了ERCOT市场设计未能充分将防冻的*保险*价值纳入定价。$9,000/MWh的价格上限对消费者在紧急期间"太高"，但可能仍然不足以在事前充分为防冻投资提供资金。

**Uri后改革：**
- 发电资产强制防冻标准（PUCT）
- 新热能电厂的容量贡献因子要求
- 增加ORDC价格加项（HCSP、HSRP）
- ERCOT紧急警报系统全面改革

### 3.3 纯能量市场 vs. 容量市场：证据

**支持纯能量市场（ERCOT）的论点：**
- 避免消费者为他们不需要的容量过度采购
- 更高效的调度（没有容量支付扭曲能量市场）
- 避免容量市场操纵和价格压制
- 通过价格信号自然激励需求响应

**支持容量市场（PJM）的论点：**
- 防止纯能量市场系统性产生的投资不足（缺钱问题）
- 提供收入确定性，降低新建设的资本成本
- 性能激励（PJM的容量性能）比纯能量市场更好地解决停电风险
- 更可预测的资源充足性结果——可以直接针对电力不足期望（LOLE）

**学术证据：**
- Creti & Fabra（2007年，*RAND Journal of Economics*）：在中等需求弹性下，纯能量市场往往投资不足
- Bidwell（2021）：ERCOT的纯能量市场在2002-2019年吸引了$110亿新发电投资，同时保持了可靠性——但Uri显示了局限性
- Joskow（2008年，*能源市场经济学*）：当需求弹性低且可靠性事件可能造成灾难性后果时，容量市场是正当的

---

## 4. 高可再生能源系统中的容量机制

随着可再生能源渗透率提高，传统容量市场设计面临新的挑战。

### 4.1 新的缺钱问题

随着可再生能源增长：
- 在高可再生能源时段，批发能源价格下降（接近零或负LMP）
- 传统发电机在其运行时段从能源销售中获得的收入减少
- 热能发电机的"缺钱"问题恶化——甚至超出容量市场目前所能解决的范围
- 调峰机组可能只需要在少数冬季早晨或夏季下午时段运行——从能源中获得的收入更少

**"鸭子曲线"动态：**
在CAISO，鸭子曲线意味着燃气机组必须在太阳能下降的傍晚快速增加出力——它们每天只运行2-3小时。纯能量市场无法支持仅靠每天2-3小时收入来投资燃气联合循环电厂。容量市场有助于弥合这一差距。

### 4.2 提议的改革

**容量期权（可靠性期权）：**
- 不是_flat容量支付，而是发电机出售"期权"——获得可用性支付，被调用时按能源市场价格结算
- 比容量市场更高效：对能源市场扭曲较小，仍能解决缺钱问题
- 在新英格兰的按性能付费机制中以某种形式实施

**认证改革：**
- 随着更多容量来自非可靠资源（太阳能、风能、储能），容量认证方法必须改变
- 基于ELCC的认证取代基于铭牌的认证
- 这需要对重合容量贡献进行详细概率建模

**储能特定容量认证：**
- 4小时电池：在中等渗透率下ELCC约为铭牌的50-80%，在更高渗透率下下降
- 8小时电池：更高的ELCC，更适合多小时冬季峰值削峰
- 关键问题：如何认证能够跨时段转移能量的储能（在太阳能过剩期间充电，在傍晚高峰期间放电）？

### 4.3 可靠 vs. 非可靠容量

一个根本性的设计问题：容量市场中是否应将所有资源一视同仁？

**可靠（可调度）容量：** 燃气联合循环、水电、需求响应——可以高置信度地被调用

**非可靠容量：** 太阳能（仅白天）、风能（可变）、电池（有限时长）

PJM和CAISO现在对非可靠资源使用基于ELCC的认证，这在技术上是正确的，但在政治上有争议——太阳能/储能公司偏好更高的认证，因为它能获得更高的容量市场收入。

---

## 5. 定量比较

| 指标 | PJM RPM | ERCOT 纯能量 |
|------|---------|-------------|
| 备用容量目标 | ~15-16% | 不适用（隐含） |
| 2024年平均清算价格 | $80-140/MW-day | 不适用 |
| 年度容量支付（典型） | $30-50/kW-year | $0（纯能量） |
| 可靠性指标 | LOLE < 0.1天/年 | 相同（通过ORDC隐含） |
| 2021年冬季风暴表现 | 基本保持 | 重大失败（Uri） |
| 热能容量保留比例 | 约为2000年水平的60% | 约为2000年水平的50% |
| 可再生能源渗透率（2024） | 约15%发电量 | 约35%发电量 |
| 缺钱问题 | 部分解决 | 严重 |

---

## 6. 开放研究问题

1. **高可再生能源系统的最优容量机制：** 在50%+可再生能源渗透率下，容量市场还有意义吗？还是储能 + 需求响应 + 互联互通能够在没有热能容量的情况下提供足够的资源充足性？
2. **性能评估：** 如何设计对极端天气事件（如2021年德州冻结）稳健的性能激励，同时不在正常年份施加过度成本？
3. **ELCC建模改进：** 当前ELCC方法假设不相关的停电事件——但在冬季风暴期间，许多热能发电机同时故障。容量认证应如何考虑相关的尾部风险？
4. **跨境容量分配：** PJM和MISO共享一些容量——它们的容量市场应如何互动？单一合并容量市场与有互联互通的独立市场会造成复杂的定价问题。
5. **容量市场 vs. 可靠性期权：** 哪种工具在保持可靠性的同时提供更低的消费者成本？使用CAISO和PJM数据的实证比较。

---

## 7. 关键参考文献

- Joskow, P.L. (2008). "Competitive Electricity Markets and Investment." *Journal of Economic Perspectives* 22(1).
- Creti, A. & Fabra, N. (2007). "Supply Security and Capacity Mechanisms." *RAND Journal of Economics* 38(3).
- Bidwell, M. (2021). "Resource Adequacy and the ERCOT Energy-Only Market." *Electricity Journal* 34(7).
- PJM (2024). *PJM Manual 18: PJM Capacity Market* — 详细RPM机制
- CAISO (2024). *Capacity Accreditation Forum* — ELCC方法论发展
- FERC (2023). *Order on Capacity Performance Audits* — 性能激励机制
- New England Power Pool (2024). *Pay-for-Performance Final Proposal*

---

*最后更新：2026-05-07*
*相关：[[ercot-rtc-b-market]]，[[pjm-vs-ercot]]，[[storage-economics]]，[[demand-response-economics]]*

---

# English Version

# Capacity Market Design and Resource Adequacy in Energy Transition

> **Prerequisites:** [[locational-marginal-pricing]], [[electricity-markets-day-ahead-real-time]], [[ercot-rtc-b-market]]

---

## 1. The Missing Money Problem

Wholesale electricity markets — whether PJM's LMP + capacity market or ERCOT's energy-only system marginal price — must accomplish two things simultaneously:

1. **Energy market:** Dispatch the existing fleet at minimum cost in real-time
2. **Capacity market/investment signal:** Attract sufficient generation investment to ensure resource adequacy for future demand

The **missing money problem** is the fundamental challenge in restructured electricity markets: the energy market alone does not provide sufficient revenue to justify investment in generation capacity that the system needs for reliability during a small number of peak hours.

**Why does this happen?**
- Wholesale electricity markets price energy at marginal cost (fuel + variable O&M)
- Peak hours occur infrequently (100-400 hours/year in most markets)
- Building a peaker (gas combustion turbine) is expensive ($600-800/kW) but it earns money only during those peak hours
- When market prices spike during peak hours, investors hope to recover annual fixed costs from a few hundred hours of high prices — but competitive pressure and price caps limit how high prices can go
- The **missing money** = fixed capacity costs minus what the energy market can profitably recover

**The reliability-redispatch tradeoff:**
- Energy-only markets (ERCOT) rely on scarcity pricing — very high prices during peaks that, in theory, fund peakers and incentivize demand response
- Capacity markets (PJM, NYISO, ISO-NE) provide a separate capacity payment that ensures fixed cost recovery regardless of energy market outcomes

---

## 2. PJM's Reliability Pricing Model (RPM)

PJM operates the largest capacity market in the world — the **Reliability Pricing Model (RPM)**, implemented in 2007 and modified through multiple Base Residual Auction (BRA) cycles.

### 2.1 Auction Structure

PJM's RPM uses a **centralized forward capacity auction** three years ahead of the delivery year:

```
Delivery Year t → Auction held in Year t-3 (also known as "BRA")
```

**Key auction parameters:**
- **Base Residual Auction (BRA):** The primary auction clearing mechanism
- **Incremental Auction (IA):** Held 20, 10, and 3 months before delivery year to adjust for demand forecast changes and capacity additions/retirements
- **Trending reserve margin:** PJM targets ~15-16% above peak load as reserve margin
- **Capacity Clearing Price:** Paid to all cleared capacity (every MW at the same clearing price in a Locational Deliverability Area)

**Price determination:**
- RPM uses a **demand curve** (not a vertical demand curve) — the price declines as quantity cleared increases above the reliability requirement
- This reduces price volatility while still providing investment signals
- For PSEG/New Jersey areas (constrained zones), separate clearing prices apply

### 2.2 Real Auction Results and Clearing Prices

| Delivery Year | PJM RPM Clearing Price ($/MW-day) | Trend |
|---|---|---|
| 2012-2014 | $28-80/MW-day | Low gas prices → low prices |
| 2015-2016 | $45-120/MW-day | Moderate |
| 2017-2018 | $100-175/MW-day | Capacity retirements, higher demand |
| 2019-2020 | $80-140/MW-day | Stabilization |
| 2021-2022 | $50-270/MW-day (high variance by LDA) | Winter storm impacts |
| 2023-2024 | $60-180/MW-day | ORDC additions, reliability concerns |

**Capacity commitment value:** $100/MW-day ≈ $36,500/MW-year

**PJM's own analysis:** At $100/MW-day clearing price, new gas peakers are barely economical (payback ~7-10 years at $700/kW capital cost + fixed O&M). This is the "missing money" — capacity market provides the revenue bridge.

### 2.3 Capacity Resource Performance Test (CRPT)

PJM implemented the **Capacity Performance** paradigm in 2018 (replacing the older "Base Capacity" product) following the 2014 Polar Vortex:

- Resources must perform during emergencies or face severe penalties
- **Non-Performance Charge:** $5,000/MWh for capacity that doesn't deliver when called
- **Performance Payment:** Bonus payment for over-performance above committed capacity

This significantly increased the quality of capacity cleared — performance-based differentiation replaced the previous commodity-like capacity product.

### 2.4 Capacity Credit and ELCC

For intermittent resources (solar, wind) and storage, capacity value is not their nameplate rating:

**Effective Load Carrying Capacity (ELCC):**
- ELCC measures how many MW of firm capacity a resource can reliably substitute for a conventional generator
- Solar ELCC in PJM: ~38-50% of nameplate (depending on capacity factor and summer peak coincidence)
- Wind ELCC in PJM: ~10-20% of nameplate
- Battery storage ELCC: ~50-80% (4-hour battery at high penetration levels)

**Why ELCC matters for capacity market design:**
- If solar gets full capacity credit, the capacity market will be oversubscribed and prices collapse
- At very high renewable penetration, ELCC of each additional unit declines (the "first-come-first-served" diminishing returns problem)
- This creates a perverse dynamic: as more solar is added, its capacity credit falls, requiring even more capacity from other sources

---

## 3. ERCOT: Energy-Only Market

ERCOT is the primary US example of a large energy-only market (alongside Australia's NEM and Alberta's AESO).

### 3.1 ERCOT's Scarcity Pricing Mechanism

Without a capacity market, ERCOT relies on **sensitivity-based pricing** during scarcity to signal investment:

**ORDC (Operating Reserve Demand Curve):**
- ERCOT adds a shadow price to operating reserves when reserve levels fall below threshold
- As reserves drop, the ORDC adds up to ~$9,000/MWh to the system marginal price
- This creates price spikes that, in theory, fund peakers and attract investment

**High Sustained Reserve Price (HSRP):** Added after 2021 winter storm:
- $2,000/MW for each MW of available capacity above 75% of peak demand, applied during emergencies
- Provides a more predictable revenue stream for thermal generators

**High Conditional Sparsity Price (HCSP):** For when dispatchable thermal capacity is scarce relative to renewables

### 3.2 The 2021 Winter Storm Test

ERCOT's energy-only model was severely tested during Winter Storm Uri (February 2021):
- ~4.5 million customers lost power
- Spot prices hit the $9,000/MWh price cap
- Estimated economic damage: $23-135 billion (depending on methodology)
- Generators that managed to run earned extraordinary profits; those that failed faced fixed costs with no revenue

**The performance gap:** Some gas plants froze, revealing that ERCOT's market design had not adequately priced the *insurance* value of weatherization. The $9,000/MWh price cap was "too high" for consumers during the emergency but may still have been insufficient to fully fund weatherization investment ex-ante.

**Post-Uri reforms:**
- Mandatory weatherization standards for generation assets (PUCT)
- Capacity contribution factor requirements for new thermal plants
- Increased ORDC price adders (HCSP, HSRP)
- ERCOT's emergency alert system overhaul

### 3.3 Energy-Only vs. Capacity Market: The Evidence

**Arguments for energy-only (ERCOT):**
- Avoids over-procurement of capacity that consumers pay for but never need
- More efficient dispatch (no capacity payments distorting energy market)
- Avoids capacity market gaming and price suppression
- Incentivizes demand response naturally through price signals

**Arguments for capacity market (PJM):**
- Prevents under-investment that energy-only markets systematically produce (the missing money problem)
- Provides revenue certainty that lowers cost of capital for new build
- Performance incentives (Capacity Performance in PJM) address outage risk better than energy-only
- More predictable resource adequacy outcomes — loss of load expectation (LOLE) can be directly targeted

**Academic evidence:**
- Creti & Fabra (2007, *RAND Journal of Economics*): Energy-only markets tend to under-invest relative to the social optimum under moderate demand elasticity
- Bidwell (2021): ERCOT's energy-only market during 2002-2019 attracted $11 billion in new generation investment while maintaining reliability — but Uri showed the limits
- Joskow (2008, *Economics of Energy Markets*): Capacity markets are justified when demand elasticity is low and reliability events are potentially catastrophic

---

## 4. Capacity Mechanisms in High-Renewable Systems

As renewable penetration increases, traditional capacity market design faces new challenges.

### 4.1 The New Missing Money Problem

As renewables grow:
- Wholesale energy prices fall during high-renewable hours (near-zero or negative LMP)
- Conventional generators earn less from energy sales during their operating hours
- The "missing money" problem for thermal generators worsens — even beyond what capacity markets currently address
- Peakers may be needed only for a few winter morning or summer afternoon hours — earning even less from energy

**The "duck curve" dynamic:**
In CAISO, the duck curve means gas plants must ramp up quickly in the evening as solar output falls — they run for only 2-3 hours per day. A pure energy-only market cannot support gas CCGT investment on 2-3 hours/day of revenue. A capacity market helps bridge this gap.

### 4.2 Proposed Reforms

**Option capacity (Reliability Option):**
- Instead of a flat capacity payment, generators sell "options" — they get paid for being available, and when called they receive energy market prices
- More efficient than capacity market: less distortion to energy market, still solves missing money
- Implemented in some form in New England's pay-for-performance mechanism

**Accreditation reform:**
- As more capacity comes from non-firm resources (solar, wind, storage), capacity accreditation methods must change
- ELCC-based accreditation replaces nameplate-based accreditation
- This requires detailed probabilistic modeling of coincident capacity contribution

**Storage-specific capacity accreditation:**
- 4-hour battery: ELCC ~50-80% of nameplate at moderate penetration, declining at higher penetration
- 8-hour battery: Higher ELCC, better for multi-hour winter peak shaving
- Key question: how to accredit storage that can shift energy across hours (charge during solar oversupply, discharge during evening peak)?

### 4.3 Firm vs. Non-Firm Capacity

A fundamental design question: should all resources be treated the same in capacity markets?

**Firm (dispatchable) capacity:** Gas CCGT, hydro, demand response — can be called on with high confidence

**Non-firm capacity:** Solar (only during day), wind (variable), batteries (limited duration)

PJM and CAISO now use ELCC-based accreditation for non-firm resources, which is technically correct but politically contentious — solar/storage companies prefer higher accreditation because it justifies higher capacity market revenues.

---

## 5. Quantitative Comparison

| Metric | PJM RPM | ERCOT Energy-Only |
|--------|---------|-----------------|
| Reserve margin target | ~15-16% | N/A (implicit) |
| 2024 clearing price (avg.) | $80-140/MW-day | N/A |
| Annual capacity payment (typical) | $30-50/kW-year | $0 (energy only) |
| Reliability metric | LOLE < 0.1 days/year | Same (implicit via ORDC) |
| 2021 winter storm performance | Maintained (mostly) | Major failure (Uri) |
| Share of thermal capacity retained | ~60% of 2000 levels | ~50% of 2000 levels |
| Renewable penetration (2024) | ~15% of generation | ~35% of generation |
| Missing money problem | Partially addressed | Severe |

---

## 6. Open Research Questions

1. **Optimal capacity mechanism for high-renewable systems:** At 50%+ renewable penetration, does a capacity market still make sense, or does storage + demand response + interconnection provide sufficient resource adequacy without thermal capacity?
2. **Performance assessment:** How to design performance incentives that are robust to extreme weather events (like the 2021 Texas freeze) while not imposing excessive costs in normal years?
3. **ELCC modeling improvements:** Current ELCC methods assume uncorrelated outage events — but during winter storms, many thermal generators fail simultaneously. How should capacity accreditation account for correlated tail risk?
4. **Cross-border capacity allocation:** PJM and MISO share some capacity — how should their capacity markets interact? A single merged capacity market vs. separate markets with interconnections creates complex pricing problems.
5. **Capacity market vs. reliability options:** Which instrument provides lower consumer cost while maintaining reliability? Empirical comparison using CAISO and PJM data.

---

## 7. Key References

- Joskow, P.L. (2008). "Competitive Electricity Markets and Investment." *Journal of Economic Perspectives* 22(1).
- Creti, A. & Fabra, N. (2007). "Supply Security and Capacity Mechanisms." *RAND Journal of Economics* 38(3).
- Bidwell, M. (2021). "Resource Adequacy and the ERCOT Energy-Only Market." *Electricity Journal* 34(7).
- PJM (2024). *PJM Manual 18: PJM Capacity Market* — detailed RPM mechanics
- CAISO (2024). *Capacity Accreditation Forum* — ELCC methodology developments
- FERC (2023). *Order on Capacity Performance Audits* — performance incentive mechanisms
- New England Power Pool (2024). *Pay-for-Performance Final Proposal*

---
*Last updated: 2026-05-07*
*Related: [[ercot-rtc-b-market]], [[pjm-vs-ercot]], [[storage-economics]], [[demand-response-economics]]*
