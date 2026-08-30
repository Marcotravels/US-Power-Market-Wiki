# PJM vs ERCOT：比较性市场设计与经济结果分析

> **前置知识：** [[locational-marginal-pricing]]，[[capacity-market-design]]，[[ercot-rtc-b-market]]，[[ancillary-services-market]]

---

## 1. 制度概述：两种模式，同一目标

PJM Interconnection 和 ERCOT 代表了美国两种差异最大的电力市场设计。理解它们的差异，可以阐明电力市场设计理论中的根本性争论。

| | **PJM** | **ERCOT** |
|-|---------|-----------|
| **市场类型** | RTO，LMP + 容量市场 (RPM) | 独立系统运营商（ISO）；纯能量市场，系统边际价格 |
| **地理覆盖** | 13个州+DC的部分或全部 | 德克萨斯州（仅通过HVDC联络线与东部/西部电网互联） |
| **服务客户** | 约6,500万 | 约2,700万 |
| **峰值负荷（2024）** | 约165,000 MW | 约87,000 MW |
| **发电组合** | 天然气42%，煤炭15%，核电33%，可再生能源约15% | 天然气45%，可再生能源35%，煤炭约5%，核电约12% |
| **批发价格上限** | $2,000/MWh（持续），$5,000/MWh（短期紧急） | $9,000/MWh（现行） |
| **备用市场** | 同步备用 + 容量市场 | 基于ORDC的稀缺定价 + 辅助服务 |
| **FERC管辖权** | 作为RTO完全受FERC管辖 | 有限——ERCOT根据《联邦电力法》享有独特豁免 |
| **互联状态** | 东部互联的一部分 | 电气隔离（仅限直流联络线） |

### 为什么这些差异很重要

PJM的设计反映了RTO/ISO电力市场重组的"标准模型"，通过FERC 888号、2000号命令及后续规则发展而来。ERCOT的设计则反映了德州历史上的独立于联邦监管的传统（"德州例外"——ERCOT先于1935年《联邦电力法》存在，并保留了限制FERC权威的独特司法地位）。

---

## 2. 批发价格比较

### 2.1 年度平均价格

PJM和ERCOT服务不同地区，发电组合也不同，但价格比较很有启发性：

| 年份 | PJM实时平均LMP ($/MWh) | ERCOT实时平均SMP ($/MWh) | 备注 |
|------|------|------|------|
| 2019 | $38-45 | $30-35 | 天然气价格低 |
| 2020 | $28-32 | $22-26 | COVID需求减少 |
| 2021（1-2月） | $50-70 | $150-500+ | Uri在ERCOT飙升 |
| 2021（年均） | $45-55 | $65-80 | 年均受Uri扭曲 |
| 2022 | $70-95 | $75-90 | 天然气价格上涨 |
| 2023 | $55-70 | $50-65 | ERCOT新增太阳能/储能抑制价格尖峰 |
| 2024 | $60-75 | $55-70 | 趋同，ERCOT增加储能 |

**关键观察：** Uri之后（2021年），ERCOT价格向PJM水平趋同，新太阳能和储能增加抑制了价格尖峰，且ERCOT的ORDC改革为火电创造了更稳定的稀缺收入。

### 2.2 价格波动性

价格波动性是市场运行的关键衡量指标：

**PJM波动性：** 日间波动性较低，原因包括：
- 容量市场提供收入确定性 → 减少投资的繁荣-衰退周期
- 大覆盖范围（13个州）提供地理多元化
- 同步备用市场平滑短期价格波动

**ERCOT波动性：** 历史上较高，但正在降低：
- 纯能量 + ORDC → 发电机收入取决于稀缺事件 → 繁荣-衰退周期
- 小覆盖范围（仅德州）→ 地理多元化有限
- 然而：ERCOT 2021-2024年增加了约10 GW电池储能，大幅降低了实时波动性

**极端事件：** ERCOT的$9,000/MWh价格上限高于PJM的约$2,000/MWh软上限——反映了ERCOT对更频繁稀缺定价的容忍度（或预期）。Uri期间，PJM价格达到约$1,500-2,000/MWh；ERCOT价格在延长时间内触及$9,000上限。

---

## 3. 2021年冬季风暴：决定性的自然实验

2021年2月10-20日的冬季风暴Uri为两种市场设计提供了最重要的实证比较。

### 3.1 发生了什么

**ERCOT：**
- 约450万客户断电，部分持续长达4天
- 约246人死亡（官方）；学术估计高达700人
- 估计经济损失：$230-1,350亿（范围反映方法论差异）
- 市场价格连续约3天触及$9,000/MWh上限
- 天然气井冻结 → 天然气供应故障级联到发电故障
- 风电（未除冰）峰值寒冷期间仅产出约3-4%容量
- 估计：峰值需求时30-50 GW发电不可用

**PJM：**
- 约35万客户断电（对比ERCOT的数百万）
- 无死亡归因于发电故障
- PJM的容量市场确保了更多发电可用
- 部分时期价格飙升至约$1,500-2,000/MWh
- 无ERCOT经历的规模性结构故障

### 3.2 为什么ERCOT失败得更严重

**制度因素：**

1. **无容量市场：** ERCOT缺乏远期容量承诺机制。2020-2021年冬季，天然气价格低且ERCOT有剩余容量——因此市场价格低。当Uri来袭时，需求激增造成即时容量短缺，但没有机制确保远期容量采购。

2. **无法接入东部互联：** PJM可以从东部互联进口电力；ERCOT不能。ERCOT与东部互联之间的直流联络线（约1,100 MW总量）不足以进行紧急进口。

3. **防冰标准不足：** PJM的市场规则和FERC监督强制要求防冰标准；ERCOT的标准在Uri改革前是自愿性的。

4. **天然气供应相互依赖：** 在ERCOT，天然气发电是冬季峰值期间的边际机组。当天然气井冻结时，向发电机的天然气供应失败——这是ERCOT高度依赖天然气的独特级联故障。PJM的煤炭 + 核电基荷提供了ERCOT缺乏的缓冲。

### 3.3 反事实问题

一个关键研究问题：在能源-only市场中，PJM会表现得更好吗？还是容量市场的远期承诺是关键差异？

**容量市场重要的论点：**
- PJM清算了约180 GW容量 vs. 约130 GW峰值需求 → 强劲备用裕度
- 远期容量承诺意味着发电机有财务激励维持可用性和燃料供应合同
- 容量绩效产品（2018年后）惩罚非绩效，加强了激励

**ERCOT失败是特定而非结构性的论点：**
- Uri是百年一遇事件——不是设计失败而是极端场景
- ERCOT的ORDC和稀缺定价对"正常"稀缺事件按设计运行
- 没有防冰标准，PJM的容量市场同样无法防止类似极端场景中的失败

---

## 4. 消费者福利分析

### 4.1 批发价格影响

**短期消费者福利：** Uri前ERCOT平均价格较低，为德州消费者提供了较低的短期电力成本。ERCOT的零售重组（1999年）使工业和住宅客户能够选择零售商，引入竞争。

**长期消费者福利：** 这正是分析变得复杂的地方：
- ERCOT的纯能量模型在正常年份保持低批发价格，但在稀缺时产生巨大价格尖峰 → 未套保的消费者在Uri期间支付极端价格
- PJM的容量市场在消费者账单上增加约$30-50/kW-年 → 较高的基线成本但更稳定的长期价格

**消费者的套保选择：**
- ERCOT：消费者可以购买固定价格零售合同（零售商通过ERCOT期货/远期合同套保）或让自己暴露于实时现货价格
- PJM：类似的零售选择 + PJM的容量市场成本通过监管费率分摊 → 所有消费者都支付容量费用，无论套保选择

### 4.2 谁承担极端天气风险？

| 消费者群体 | ERCOT纯能量市场 | PJM容量市场 |
|---|---|---|
| 住宅（固定价格零售） | 低平均成本，中等风险 | 中等平均成本，低风险 |
| 住宅（现货暴露） | 极端风险 | 有限（价格上限） |
| 工业（套保老手） | 可通过远期合同管理 | 可通过零售合同管理 |
| 工业（未套保） | 极端暴露 | 中等暴露 |
| 低收入（零售选择有限） | 高脆弱性 | 较低脆弱性 |

**分配发现：** 纯能量市场将极端天气风险集中于最无力管理的人（未套保的住宅和小商业消费者）。容量市场通过容量费用将这种风险社会化给所有消费者——以不同方式造成累退（按kW征收的固定容量费用对低收入家庭比例上更高）。

---

## 5. 投资激励与结果

### 5.1 发电投资

**ERCOT（纯能量）：**
- 收入堆叠：能源市场（ORDC驱动的稀缺）+ 辅助服务 + 新容量奖金（Uri后HCSP、HSRP）
- 峰时电厂经济学：依赖每年100-300小时、$5,000-9,000/MWh的稀缺定价 → 需要高价格上限才能生存
- 新建：2020-2024年新增约15 GW太阳能（由ITC经济学驱动，非ERCOT稀缺）；2021-2024年新增约5 GW电池储能；新增天然气极少

**PJM（LMP + 容量）：**
- 收入堆叠：能源市场（LMP）+ 容量市场支付 + 辅助服务
- 峰时电厂经济学：约$100-150/MW-天的容量支付 + 能源市场 → 更稳定、更低风险的收入
- 新建：2015-2022年适度新增天然气；大型可再生能源建设（太阳能/海上风电）；容量市场保持价格更稳定

**关键投资差异：** PJM的容量市场吸引了约25 GW需求侧资源和储能；ERCOT的太阳能/储能完全由能源市场 + ITC经济学吸引。

### 5.2 储能投资

ERCOT的电池储能建设（2021-2024：约5 GW/10 GWh）驱动力：
- ERCOT的实时价格波动创造套利机会（太阳能淹没市场时以约$0-20/MWh充电，在晚间峰值时以$100-500/MWh放电）
- "5分钟调度"规则使电池能够捕获快速响应价值
- 联邦ITC适用于储能

PJM的电池建设较慢（截至2024年约2 GW），因为：
- 容量市场提供收入底线，减少了优化实时套利的紧迫性
- 更平稳的PJM价格（无ERCOT式$9,000尖峰）→ 套利价差较小
- 更有限的实时波动性创造了更少的电池机会

---

## 6. 资源充足性结果

### 6.1 负荷损失期望（LOLE）

两个市场都目标LOLE < 0.1天/年（即，平均而言，系统不应有每10年超过一次切负荷风险）。

**PJM：** 通过远期容量市场实现 → 提前3年清算，备用裕度目标约15-16%。LOLE可靠地 < 0.1。

**ERCOT：** 无正式LOLE目标。通过ORDC稀缺定价 + Uri后改革（HCSP、HSRP）实现。ERCOT的ORDC设计使预期稀缺定价随时间推移为足够峰值容量提供资金。然而：
- 2021年Uri失败表明这对于极端天气是不够的
- Uri后：ERCOT增加了约4 GW可靠容量承诺（防寒要求）

### 6.2 相关性问题

一个关键差异：**相关性发电机故障**

在PJM，13个州的发电机可能在极端天气期间同时故障，但地理多元化降低了同时全部故障的概率。

在ERCOT，单一天气事件（冬季风暴）可以同时影响几乎所有德州发电。风力涡轮机冻结，天然气井冻结，一切都是相关的。这意味着ERCOT冬季峰值期间的有效容量远低于铭牌容量——这是ERCOT市场设计未能充分定价的事实。

**Uri后改革：** ERCOT现在要求"冬季准备声明"，可以调用触发更高ORDC价格的"紧急能源警报"条件。关键变化：ERCOT现在在其规划备用裕度计算中考虑相关性停电风险。

---

## 7. 证据说明什么？

### 支持PJM模式的论点
- 极端天气期间维护更好的可靠性（Uri比较）
- 容量市场提供可预测的收入 → 新建项目资本成本更低
- 更大的地理覆盖范围提供天气事件多元化
- FERC监督提供监管一致性

### 支持ERCOT模式的论点
- 较低的平均批发价格（Uri前） → 正常年份消费者剩余
- 更简单的市场结构（无容量市场官僚机构）
- 更快的可再生能源建设（ITC经济学，非容量市场博弈）
- 显著的电池储能增加证明了竞争性市场创新

### 学术共识

大多数能源经济学家认为比较并不干净，因为：
1. 德州和PJM服务区域不可比（人口密度、气候、燃料组合）
2. ERCOT与东部互联的隔离是一个独特的风险因素
3. 2021年事件是尾风险场景，不应使纯能量市场在正常运行中失效

**Joskow (2023)：** "ERCOT的失败不是证明纯能量市场行不通的证据——而是证明市场设计必须明确考虑相关性极端天气风险的证据。如果防冰标准不足，PJM的容量市场同样容易受到此类失败影响。"

**Bushnell & Mansur (2022)：** 发现ERCOT在2018-2020年的实时价格波动系统性低于国际可比纯能量市场——表明ERCOT的ORDC对正常稀缺事件运行得当。

---

## 8. 关键数据比较

| 指标 | PJM | ERCOT |
|--------|-----|-------|
| 年度平均批发价格（2024） | $60-75/MWh | $55-70/MWh |
| 价格尖峰上限 | ~$2,000-5,000/MWh | $9,000/MWh |
| 正常年份价格波动性（标准差） | ~$15-20/MWh | ~$20-30/MWh |
| Uri时代总故障小时数 | ~4-8小时（局部） | ~60-70小时（系统性） |
| 归因死亡 | ~0（发电故障） | ~246-700 |
| Uri估计经济损失 | 微小 | $230-1,350亿 |
| 发电容量（2024） | ~195 GW | ~90 GW |
| 可再生能源占比（2024） | ~15-18% | ~35-40% |
| 电池储能（2024） | ~2 GW | ~5 GW |
| 容量市场成本（2024） | ~$30-50/kW-年 | $0 |
| FERC管辖权 | 完全 | 有限 |

---

## 9. 开放研究问题

1. **消费者福利差异的因果归因：** 我们能否从地理位置、燃料组合和客户组合的影响中分离出市场设计（容量市场 vs 纯能量）对消费者福利结果的影响？
2. **最优价格上限设计：** ERCOT的$9,000/MWh上限应该更低（减少现货暴露）还是更高（实现更多投资）？什么上限水平平衡投资激励和消费者保护？
3. **Uri后ERCOT性能：** Uri改革（HCSP、HSRP、防冰强制要求）后，ERCOT的可靠性是否实质性改善？在我们能够测量下一次极端事件之前？
4. **高可再生能源系统的容量市场改革：** 如果PJM达到30-40%可再生能源，其容量市场是否需要根本性重新设计？现有框架是否适应可再生能源容量认证变化？
5. **压力市场中的市场力：** ERCOT和PJM都在Uri和极地涡旋事件期间表现出发电机市场力行使的证据。PJM约束区域中发电集中度是否比ERCOT造成更持久的市场力问题？

---

## 10. 关键参考文献

- Joskow, P.L. (2023). "Electricity Markets and the Energy Transition." *Journal of Economic Perspectives* 37(4).
- Bushnell, J. & Mansur, E.T. (2022). "Market Structure and Competition in Electricity Markets." *Handbook of Energy Economics*.
- Bidwell, M. (2021). "Resource Adequacy and the ERCOT Energy-Only Market." *Electricity Journal* 34(7).
- PJM (2024). *PJM State of the Market Report* — annual reliability and price analysis
- ERCOT (2024). *Annual Report on ERCOT Grid Conditions* — post-Uri reliability metrics
- FERC (2022). *Winter Storm Uri: Report on FERC and NERC Staff Findings*
- Hausman, C. & Wiel, S. (2022). "Death and Property Damage from Extreme Weather Events." *Journal of Environmental Economics and Management* 115.

---
*文档创建日期：2026-05-07*
*相关：[[capacity-market-design]]，[[ercot-rtc-b-market]]，[[carbon-pricing-integration]]，[[environmental-justice-energy]]*

---

# English Version

# PJM vs ERCOT: Comparative Market Design and Economic Outcomes Analysis

> **Prerequisites:** [[locational-marginal-pricing]], [[capacity-market-design]], [[ercot-rtc-b-market]], [[ancillary-services-market]]

---

## 1. Institutional Overview: Two Models, One Goal

PJM Interconnection and ERCOT represent the two most divergent electricity market designs in the United States. Understanding their differences illuminates fundamental debates in electricity market design theory.

| | **PJM** | **ERCOT** |
|-|---------|-----------|
| **Market type** | RTO with LMP + Capacity Market (RPM) | Independent System Operator (ISO); energy-only, system marginal price |
| **Geographic footprint** | All or parts of 13 states + DC | Texas (interconnected to Eastern/Western grids only via HVDC ties) |
| **Customers served** | ~65 million | ~27 million |
| **Peak demand (2024)** | ~165,000 MW | ~87,000 MW |
| **Generation mix** | Gas 42%, Coal 15%, Nuclear 33%, Renewables ~15% | Gas 45%, Renewables 35%, Coal ~5%, Nuclear ~12% |
| **Price cap (wholesale)** | $2,000/MWh (sustained), $5,000/MWh (short-term emergency) | $9,000/MWh (current) |
| **Reserve market** | Synchronized reserves + capacity market | ORDC-based scarcity pricing + ancillary services |
| **FERC jurisdiction** | Full FERC jurisdiction as RTO | Limited — ERCOT has unique exemptions under the Federal Power Act |
| **Interconnection** | Part of Eastern Interconnection | Electrically isolated (DC ties only) |

### Why the Differences Matter

PJM's design reflects the "standard model" of RTO/ISO electricity market restructuring, developed through FERC Orders 888, 2000, and subsequent rules. ERCOT's design reflects Texas's historical independence from federal regulation (the "Texas exception" — ERCOT predates the Federal Power Act of 1935 and retains a unique jurisdictional status that limits FERC authority).

---

## 2. Wholesale Price Comparison

### 2.1 Average Annual Prices

PJM and ERCOT serve different regions with different generation mixes, but the price comparison is revealing:

| Year | PJM Real-Time Avg LMP ($/MWh) | ERCOT Real-Time Avg SMP ($/MWh) | Notes |
|------|------|------|------|
| 2019 | $38-45 | $30-35 | Low gas prices |
| 2020 | $28-32 | $22-26 | COVID demand reduction |
| 2021 (Jan-Feb) | $50-70 | $150-500+ | Uri spike in ERCOT |
| 2021 (annual avg.) | $45-55 | $65-80 | Annual distorted by Uri |
| 2022 | $70-95 | $75-90 | Gas price increases |
| 2023 | $55-70 | $50-65 | ERCOT additions of solar/battery moderated price spikes |
| 2024 | $60-75 | $55-70 | Convergence, ERCOT adding storage |

**Key observation:** Post-Uri (2021), ERCOT prices converged toward PJM levels as new solar and storage additions moderated price spikes and as ERCOT's ORDC reforms created more consistent scarcity revenue for thermals.

### 2.2 Price Volatility

Price volatility is a key measure of market functioning:

**PJM volatility:** Lower day-to-day volatility due to:
- Capacity market providing revenue certainty → less boom-bust generation investment
- Large footprint (13 states) provides geographic diversification
- Synch reserves markets smooth short-term price movements

**ERCOT volatility:** Historically higher, but decreasing:
- Energy-only + ORDC → generator revenues depend on scarcity events → boom-bust cycle
- Small footprint (Texas only) → less geographic diversification
- However: ERCOT added ~10 GW of battery storage 2021-2024, dramatically reducing real-time volatility

**Extreme events:** ERCOT's $9,000/MWh price cap is higher than PJM's ~$2,000/MWh soft cap — reflecting ERCOT's tolerance for (or expectation of) more frequent scarcity pricing. During Uri, PJM prices reached ~$1,500-2,000/MWh; ERCOT prices hit the $9,000 cap for extended periods.

---

## 3. The 2021 Winter Storm: The Definitive Natural Experiment

Winter Storm Uri (February 10-20, 2021) provided the most significant empirical comparison of the two market designs.

### 3.1 What Happened

**ERCOT:**
- ~4.5 million customers lost power, some for up to 4 days
- ~246 deaths attributed (official); estimates up to 700 (academic)
- Estimated economic damage: $23-135 billion (range reflects methodology)
- Market prices hit $9,000/MWh cap for ~3 days
- Gas well freeze-offs → gas supply failure cascaded into generation failure
- Wind turbines (without de-icing) produced ~3-4% of capacity during peak cold
- Estimated: 30-50 GW of generation unavailable at peak demand

**PJM:**
- ~350,000 customers lost power (vs. ERCOT's millions)
- No fatalities attributed to generation failure
- PJM's capacity market ensured more generation was available
- Some prices spiked to ~$1,500-2,000/MWh for short periods
- No structural failures of the magnitude ERCOT experienced

### 3.2 Why ERCOT Failed More Severely

**Institutional factors:**

1. **No capacity market:** ERCOT lacks a forward capacity commitment mechanism. During the winter of 2020-2021, gas prices were low and ERCOT had surplus capacity — so market prices were low. When Uri hit, the demand surge created an immediate capacity shortage with no mechanism to ensure forward capacity procurement.

2. **No access to Eastern Interconnection:** PJM could import power from the Eastern Interconnection; ERCOT could not. The DC ties between ERCOT and Eastern Interconnection (~1,100 MW total) are insufficient for emergency import.

3. **Inadequate weatherization standards:** PJM's market rules and FERC oversight impose weatherization standards; ERCOT's standards were voluntary until post-Uri reforms.

4. **Gas supply interdependency:** In ERCOT, gas-fired generators are the marginal units during winter peaks. When gas wells froze, gas supply to generators failed — a cascading failure unique to ERCOT's heavy gas reliance. PJM's coal + nuclear fleet provided baseload that gas-dominated ERCOT lacked.

### 3.3 The Counterfactual Problem

A critical research question: Would PJM have performed better with an energy-only market, or was the capacity market's forward commitment the key difference?

**The case that capacity market mattered:**
- PJM cleared ~180 GW of capacity vs. ~130 GW peak demand → strong reserve margin
- Forward capacity commitments meant generators had financial incentives to maintain availability and fuel supply contracts
- The Capacity Performance product (2018+) penalized non-performance, strengthening incentives

**The case that ERCOT's failure was specific, not structural:**
- Uri was a 1-in-100 year event — not a design failure but an extreme scenario
- ERCOT's ORDC and scarcity pricing worked as designed for "normal" scarcity events
- PJM's capacity market would not have prevented failure in a similar extreme scenario without weatherization mandates

---

## 4. Consumer Welfare Analysis

### 4.1 Wholesale Price Impact

**Short-run consumer welfare:** Lower average prices in ERCOT (pre-Uri) provided lower short-run electricity costs for Texas consumers. ERCOT's retail restructuring (1999) enabled industrial and residential customers to choose retail providers, introducing competition.

**Long-run consumer welfare:** This is where the analysis gets complex:
- ERCOT's energy-only model kept wholesale prices low in normal years but created massive price spikes during scarcity → consumers who didn't hedge paid extreme prices during Uri
- PJM's capacity market adds ~$30-50/kW-year to consumer bills → higher baseline costs but more stable long-run prices

**Hedging options for consumers:**
- ERCOT: Consumers can buy fixed-price retail contracts (retailers hedge via ERCOT futures/forwards) or expose themselves to real-time spot prices
- PJM: Similar retail options + PJM's capacity market costs are socialized through regulated rates → all consumers pay the capacity charge regardless of hedging choice

### 4.2 Who Bears the Extreme Weather Risk?

| Consumer Segment | ERCOT Energy-Only | PJM Capacity Market |
|---|---|---|
| Residential (fixed-rate retail) | Low average cost, moderate risk | Moderate average cost, low risk |
| Residential (spot exposure) | Extreme risk | Limited (price caps) |
| Industrial (hedge-savvy) | Can manage via forwards | Can manage via retail contracts |
| Industrial (unhedged) | Extreme exposure | Moderate exposure |
| Low-income (retail choice limited) | High vulnerability | Less vulnerable |

**The distributional finding:** Energy-only markets concentrate extreme weather risk on those least able to manage it (unhedged residential and small commercial consumers). Capacity markets socialize this risk across all consumers via capacity charges — which is regressive in a different way (flat per-kW charge is proportionally higher for low-income households).

---

## 5. Investment Incentives and Outcomes

### 5.1 Generation Investment

**ERCOT (energy-only):**
- Revenue stack: Energy market (ORDC-driven scarcity) + ancillary services + new capacity bonus (HCSP, HSRP post-Uri)
- Peaker economics: Relies on 100-300 hours/year of scarcity pricing at $5,000-9,000/MWh → requires high price cap for viability
- New build: ~15 GW of solar added 2020-2024 (driven by ITC economics, not ERCOT scarcity); ~5 GW of battery storage added 2021-2024; minimal new gas build

**PJM (LMP + capacity):**
- Revenue stack: Energy market (LMP) + capacity market payment + ancillary services
- Peaker economics: ~$100-150/MW-day capacity payment + energy market → more stable, lower-risk revenue
- New build: Modest new gas build 2015-2022; major renewable build (solar/offshore wind); capacity market kept prices more stable

**Key investment difference:** PJM's capacity market attracted ~25 GW of demand-side resources and storage; ERCOT attracted solar/storage purely on energy market + ITC economics.

### 5.2 Storage Investment

ERCOT's battery storage buildout (2021-2024: ~5 GW/10 GWh) was driven by:
- ERCOT's real-time price volatility creates arbitrage opportunity (charge at ~$0-20/MWh when solar floods the market, discharge at $100-500/MWh during evening peak)
- The "5-minute dispatch" rule enables batteries to capture fast-responding value
- Federal ITC applies to storage

PJM's battery buildout has been slower (~2 GW as of 2024) because:
- Capacity market provides a revenue floor, reducing urgency to optimize real-time arbitrage
- Smoother PJM prices (no ERCOT-style $9,000 spikes) → lower arbitrage spread
- More limited real-time volatility creates less battery opportunity

---

## 6. Resource Adequacy Outcomes

### 6.1 Loss of Load Expectation (LOLE)

Both markets target LOLE < 0.1 days/year (i.e., on average, the system should not be at risk of shedding load more than once per 10 years).

**PJM:** Achieved through forward capacity market → clearing 3 years ahead with reserve margin target ~15-16%. LOLE reliably < 0.1.

**ERCOT:** No formal LOLE target. Achieved through ORDC scarcity pricing + post-Uri reforms (HCSP, HSRP). ERCOT's ORDC is designed so that expected scarcity pricing over time funds sufficient peaker capacity. However:
- The 2021 Uri failure showed this was inadequate for extreme weather
- Post-Uri: ERCOT added ~4 GW of firm capacity commitments (winterization requirements)

### 6.2 The Correlation Problem

A critical difference: **correlated generator failures**

In PJM, generators across 13 states may fail simultaneously during extreme weather, but geographic diversifying reduces the probability that all fail at once.

In ERCOT, a single weather event (winter storm) can affect virtually all Texas generation simultaneously. Wind turbines freeze, gas wells freeze, everything is correlated. This means ERCOT's effective capacity during winter peaks is much lower than nameplate — a fact that ERCOT's market design had not adequately priced.

**Post-Uri reform:** ERCOT now requires "winter preparedness declarations" and can call on "Emergency Energy Alert" conditions that trigger higher ORDC prices. The key change: ERCOT now accounts for correlated outage risk in its planning reserve margin calculations.

---

## 7. What Does the Evidence Say?

### The Case for PJM's Model
- Better maintained reliability during extreme weather (Uri comparison)
- Capacity market provides predictable revenue → lower cost of capital for new build
- Larger geographic footprint provides weather event diversification
- FERC oversight provides regulatory consistency

### The Case for ERCOT's Model
- Lower average wholesale prices (pre-Uri) → consumer surplus in normal years
- Simpler market structure (no capacity market bureaucracy)
- Faster renewable buildout (ITC economics, not capacity market gaming)
- Dramatic battery storage addition demonstrates competitive market innovation

### The Academic Consensus

Most energy economists argue the comparison is not clean because:
1. Texas and PJM service territories are not comparable (population density, climate, fuel mix)
2. ERCOT's isolation from Eastern Interconnection is a unique risk factor
3. The 2021 event was a tail-risk scenario that shouldn't invalidate energy-only markets in normal operations

**Joskow (2023):** "ERCOT's failure was not proof that energy-only markets don't work — it was proof that market design must explicitly account for correlated extreme weather risks. The PJM capacity market is not immune to such failures either if weatherization standards are inadequate."

**Bushnell & Mansur (2022):** Found that ERCOT's real-time price volatility in 2018-2020 was systematically lower than comparable energy-only markets internationally — suggesting ERCOT's ORDC was working adequately for normal scarcity events.

---

## 8. Key Data Comparison

| Metric | PJM | ERCOT |
|--------|-----|-------|
| Annual average wholesale price (2024) | $60-75/MWh | $55-70/MWh |
| Price spike cap | ~$2,000-5,000/MWh | $9,000/MWh |
| Normal-year price volatility (std dev) | ~$15-20/MWh | ~$20-30/MWh |
| Uri-era total failure hours | ~4-8 hours (localized) | ~60-70 hours (systemic) |
| Deaths attributed | ~0 (generation failure) | ~246-700 |
| Estimated Uri economic damage | Minimal | $23-135 billion |
| Generation capacity (2024) | ~195 GW | ~90 GW |
| Renewable share (2024) | ~15-18% | ~35-40% |
| Battery storage (2024) | ~2 GW | ~5 GW |
| Capacity market cost (2024) | ~$30-50/kW-year | $0 |
| FERC jurisdiction | Full | Limited |

---

## 9. Open Research Questions

1. **Causal attribution of consumer welfare differences:** Can we isolate the effect of market design (capacity market vs. energy-only) from the effect of geography, fuel mix, and customer mix on consumer welfare outcomes?
2. **Optimal price cap design:** Should ERCOT's $9,000/MWh cap be lower (reducing spot exposure) or higher (enabling more investment)? What cap level balances investment incentives and consumer protection?
3. **Post-Uri ERCOT performance:** With post-Uri reforms (HCSP, HSRP, weatherization mandates), has ERCOT's reliability materially improved? Can we measure this before another extreme event?
4. **Capacity market reform for high-renewable systems:** If PJM reaches 30-40% renewables, does its capacity market need fundamental redesign? Or does the existing framework accommodate renewable capacity accreditation changes?
5. **Market power in stressed markets:** Both ERCOT and PJM showed evidence of generator market power exercise during Uri and polar vortex events. Does the concentration of generation in PJM's constrained zones create more persistent market power problems than ERCOT?

---

## 10. Key References

- Joskow, P.L. (2023). "Electricity Markets and the Energy Transition." *Journal of Economic Perspectives* 37(4).
- Bushnell, J. & Mansur, E.T. (2022). "Market Structure and Competition in Electricity Markets." *Handbook of Energy Economics*.
- Bidwell, M. (2021). "Resource Adequacy and the ERCOT Energy-Only Market." *Electricity Journal* 34(7).
- PJM (2024). *PJM State of the Market Report* — annual reliability and price analysis
- ERCOT (2024). *Annual Report on ERCOT Grid Conditions* — post-Uri reliability metrics
- FERC (2022). *Winter Storm Uri: Report on FERC and NERC Staff Findings*
- Hausman, C. & Wiel, S. (2022). "Death and Property Damage from Extreme Weather Events." *Journal of Environmental Economics and Management* 115.

---
*Document created: 2026-05-07*
*Related: [[capacity-market-design]], [[ercot-rtc-b-market]], [[carbon-pricing-integration]], [[environmental-justice-energy]]*
