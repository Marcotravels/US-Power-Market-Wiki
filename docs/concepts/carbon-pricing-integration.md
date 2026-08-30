# 美国批发电力市场中的碳定价整合

> **English:** Carbon Pricing Integration in US Wholesale Electricity Markets
> **前置条件：** [[locational-marginal-pricing]]，[[ancillary-services-market]]，[[electricity-markets-day-ahead-real-time]]

---

## 1. 概述：为什么碳定价对电力市场重要

碳定价是使CO₂外部性内部化到批发电力市场中最经济有效的方法。与技术强制规定或可再生能源组合标准不同——它们规定*如何*减少排放——碳价格让市场通过调度优先顺序发现*最低成本*的减排路径。

基本机制：碳价格将`C × emission_factor`（美元/MMBtu × 吨CO₂/MMBtu）加到每个发电机的边际成本上。这改变了调度优先顺序，使高排放机组退出边际，创造了对燃气向可再生能源燃料转换的明确激励。其精妙之处在于，每个发电机、每个小时都响应相同的价格信号，无需逐案监管干预。

### 两种结构方法

| | 总量管制与交易（市场化） | 碳税（价格化） |
|-|---|---|
| **示例** | 加州总量管制与交易、RGGI、区域清洁电力 | 目前美国州级无 |
| **价格确定性** | 低（配额价格波动性） | 高 |
| **数量确定性** | 高（配额按计划下降） | 低 |
| **排放结果** | 由配额保证 | 取决于价格水平 |
| **政治可行性** | 较低（免费分配争议） | 较高（更简单） |

美国没有联邦电力碳定价。州级项目是主要机制。这创造了一个**分散的碳定价格局**——11个RGGI州加上加州——以复杂的方式与批发电力市场互动。

---

## 2. 州碳定价项目

### 2.1 加州总量管制与交易（AB 398）

加州的总量管制与交易项目，根据AB 32（2006年）建立并通过AB 398（2017年）延长，是北美最全面的碳市场。

**项目结构：**
- **配额轨迹：** 2013年启动 → 2030年比1990年水平低40%（AB 398目标）
- **年度配额下降：** 2013年至2030年每年下降约3%
- **覆盖范围：** 约占全州GHG排放的80%，包括从其他州进口的电力
- **市场参与者：** 涵盖实体（工业设施、电力零售商）必须交出与排放量相等的配额
- **链接：** 自2014年起与魁北克总量管制与交易链接

**配额供应机制：**
- 约60-70%的配额通过拍卖
- 约30-40%通过免费分配（逐渐减少）
- 价格下限：约$22.71/吨（2020年），每年上涨约5%+CPI
- 当前成交价格（2024-2025年）：**$35-45/吨CO₂**（拍卖结果）

**电力行业影响：**
- 州内发电机：面临直接合规成本
- 进口：进口到加州的电力面临"上游"合规义务（自AB 398起执行）
- 进口合规机制意味着为加州消费燃烧的州外煤电厂面临碳成本
- 天然气：约53 kg CO₂/MMBtu；在$35-45/吨时增加约$18-24/MMBtu
- 对燃气联合循环边际成本的影响：约$18-24/MMBtu × 7,000 BTU/kWh的热耗率 = **$126-168/MWh**增加到燃气边际成本

**NEM 3.0相互作用：** 2023年向太阳能产消者净计量电价（Net Billing Tariff）过渡创造了并行定价信号。面临低出口电价的产消者越来越多地转向自用和储能——与惩罚化石燃料来源电网消费的碳价格信号一致。

### 2.2 RGGI（区域温室气体倡议）

RGGI是美国最古老的强制性CO₂总量管制与交易项目——自2009年起覆盖11个东北/中大西洋州：CA、CT、DE、ME、MD、MA、NH、NJ、NY、RI、VT、VA。

**项目结构：**
- 配额：到2030年每年下降2.5%，此后到2040年每年下降3%
- 覆盖范围：>25 MW的发电厂
- 配额分配：约60%拍卖，约40%免费分配（逐渐减少）
- 成本控制： containment储备（年度配额的2%在$XX/吨触发价格时释放）

**RGGI配额价格：**
- 2014-2016年：$4-8/吨（供应过剩、低天然气价格）
- 2019年：$4-6/吨（历史低点）
- 2021年：约$13/吨
- 2022年：约$13/吨
- 2023年：约$15-17/吨
- 2024-2025年：**$22-30/吨**（由配额收紧和HFO市场效应驱动的显著价格上涨）

RGGI价格明显低于加州价格，反映了不同的配额、分配方法以及PJM/MISO覆盖范围内低成本天然气的竞争压力。

**与加州的关键区别：** RGGI**不**在其合规机制中包括电力进口——这是一个关键区别，意味着为RGGI州负荷服务的州外化石燃料发电通常逃避碳定价。这是正在诉讼中的核心法律漏洞。

### 2.3 互补州碳定价

- **华盛顿州：** 清洁能源转型法案（2019年）要求2025年前实现无煤电力，2030年前实现净零——不是直接碳定价，但具有约束力的可再生能源/无煤标准
- **纽约州：** 气候领导力和社区保护法案（CLCPA）——积极的可再生能源强制要求（2030年70%，2040年100%）加上"碳上限与投资"项目下的拟议碳定价机制（截至2025年仍在开发中）
- **俄勒冈州：** 2021年通过总量管制与投资立法（清洁能源目标和交易）

---

## 3. 碳成本如何进入调度并影响LMP

### 3.1 机制：优先顺序中的碳成本

每个可调度发电机由以下部分组成边际成本：

```
MC_g = fuel_cost_g + VOM_g + startup_cost/cycle + carbon_cost_g
```

其中 `carbon_cost_g = emission_rate_g × carbon_price`

对于天然气联合循环燃气轮机：
- 燃料成本：约$2.50/MMBtu
- 热耗率：7,000 BTU/kWh
- 燃料MC：约$17.5/MWh
- 排放率：0.053 t CO₂/MMBtu（天然气）
- 在$40/吨CO₂时：碳MC：0.053 × $40 = **$2.12/MMBtu → $14.84/MWh**

对于燃煤机组：
- 燃料成本：约$2.00/MMBtu
- 热耗率：10,000 BTU/kWh
- 排放率：0.093 t CO₂/MMBtu（烟煤）
- 在$40/吨CO₂时：碳MC：0.093 × $40 = **$3.72/MMBtu → $37.20/MWh**

**对优先顺序的影响：** 碳成本不成比例地提高燃煤边际成本，通常使其在调度堆叠中高于燃气联合循环。在$40-50/吨CO₂时，碳成本可能给燃煤增加$40-80/MWh的边际成本——在许多小时内足以完全将煤电推出市场。

### 3.2 对批发电价LMP的传导率

一个关键的实证问题：**碳成本中有多少传导到批发电价（LMP）？**

传导率取决于市场条件、发电机组合和剩余需求曲线：

- **在燃气在边际的竞争市场中：** 燃气发电机的碳成本按比例传导到LMP（传导率≈1.0）
- **在有大量煤炭退役的市场中：** 当煤电退出堆叠时，竞争基准转向燃气+碳成本 → 传导率更高
- **在PJM/ERCOT（纯能量）中：** 传导是即时的——碳成本简单地加到边际成本上
- **在CAISO（高可再生能源）中：** 在可再生能源定价的小时内（负LMP），热机组的碳成本可能不会出现在现货价格中——但容量价值和后备角色保持经济意义

**学术证据：**
- Cullen & Mansur（2017年，《环境与资源经济学家杂志》）：利用RGGI，估计$10/吨碳价格使RGGI州的批发电价上涨约$6-8/MWh——短期内传导率为60-80%
- 碳成本的其余部分被超额租金变化（退役发电机的沉没成本）和更清洁调度带来的消费者账单减少所吸收
- LaRiviere & Wilson（2022年）：发现加州总量管制与交易使CAISO批发价格上涨约$5-10/MWh，在燃气处于边际的小时内完全传导
- Novan（2015年，《环境经济与管理杂志》）：发现NOₓ和SO₂配额价格对电价的传导显著但不完整，位置和小时不同存在异质性

### 3.3 对LMP组成部分的影响

回想[[locational-marginal-pricing]]中，LMP有三个组成部分：

```
LMP = Energy Component + Congestion Component + Loss Component
```

碳定价与所有三个部分相互作用：

- **能量部分：** 主要影响——碳成本改变边际机组，在化石燃料机组处于边际的小时内提高市场出清价格
- **拥堵部分：** 碳成本可以改变跨输电约束的潮流，可能会改善或恶化拥堵模式。靠近负荷中心的高碳发电机可能被低碳远程发电机替代，改变哪些约束条件绑定
- **损耗部分：** 通过改变的发电调度模式的间接二次影响

**加州进口影响：** 加州的进口合规机制意味着煤炭进口面临碳成本。这提高了南加州进口受限地区的LMP，在历史上部分电力来自州外煤电——但影响嵌入在CAISO的进口定价规则中。

---

## 4. 经济框架

### 4.1 批发市场中外部性的内部化

确定性下的一阶最优结果：**边际损害定价**——将碳价格设定为等于CO₂排放的边际外部损害。市场然后自动找到最低成本的减排。

然而，几个复杂因素使其成为二阶最优问题：

1. **SCC的不确定性：** 我们不知道真正的边际损害。 current估计范围从$20/吨（低）到$200+/吨（高，IAM尾部风险）
2. **泄漏：** 没有边境碳调整或进口等价物，一个司法管辖区的碳定价将排放转移到不受监管的司法管辖区（"碳泄漏"）
3. **与现有法规的相互作用：**许多化石燃料发电机已经面临Title IV SO₂/NOₓ酸雨法规、新污染源审查等——碳定价叠加在现有合规成本之上
4. **市场力：** 在输电受限节点，LMP的拥堵部分可能已经向买家收取超额剩余——受限网络上的碳定价可能加剧这一点

### 4.2 碳税的发生率

谁在电力市场中承担碳定价的负担？

**生产者发生率：** 高排放发电机（煤、老式燃气蒸汽轮机）承担初始成本冲击。如果它们无法传导，就会退出。这已经戏剧性地发生——美国燃煤发电从2008年占总发电量的约50%下降到2023年的约17%，碳定价在廉价天然气之外发挥了加速作用。

**消费者发生率：** 电力相对**价格无弹性**（短期弹性：-0.1至-0.3），意味着大部分负担落在消费者身上。然而：
- 通过免费分配的交叉补贴可以保护现有发电机
- 家庭层面影响是累退的：低收入家庭将更高比例的收入用于电力，因此碳定价是累退的，除非收入作为人均回扣回收（"股息"方法）

**电力市场内的分配效应：**
- 拥有屋顶太阳能+储能的住宅消费者可以部分豁免自己（自用避免电网电价和碳成本）
- 煤电厂附近低收入社区不成比例地从退役中受益（当地PM₂.₅、NOₓ减少）
- 依赖煤炭采矿就业的社区面临集中的经济危害——一个重大政治经济挑战

### 4.3 分散的碳定价：州 vs. 联邦

美国没有联邦碳价格。州项目创造了一个补丁程序：

**问题：不平等的竞争环境**

一个有碳定价的州（加州、RGGI州）对州内发电机施加合规成本，使它们相对于没有碳定价的邻州（德州、路易斯安那州、乔治亚州）提高批发电价。这创造了：

1. 碳定价州产业（电力密集型制造商）的**竞争劣势**
2. **跨州电力流**套利碳价格：电力从低碳价格流向高碳价格地区，可能增加总系统排放（一种通过电力贸易的"碳泄漏"形式）
3. 通过投资的**排放泄漏**：新燃气发电投资被吸引到无碳定价州，增加其在未来发电中的份额

**理论框架——Jones（2019年，《环境经济学与政策评论》）：**
在一个有竞争性批发市场的州实行碳定价导致从邻州进口电力增加，定价州批发价格降低——"边境碳"效应部分抵消了环境效益。

**提出的解决方案：**
- **联邦碳价格**（一阶最优修复，政治上受阻）
- **州项目区域链接**（加州-魁北克模式，RGGI扩张）
- **进口边境碳调整**（加州对进口的方法）
- **清洁电力标准**作为替代的联邦强制的数量方法

---

## 5. 休眠商业条款问题

美国宪法 dormant commerce clause（DCC）禁止州歧视或过度负担州际贸易。这为适用于进口电力的州碳定价创造了根本性的法律紧张。

**核心问题：** 加州的AB 398进口合规机制要求州外发电机为进口到加州的电力交出加州碳配额。挑战者（包括Sempra/美国公用事业空气监管组织联盟）认为这是对州际贸易的不宪法负担。

**关键法律论据：**

*反对进口机制（DCC挑战）：*
- 州不能治外法权（排放发生在加州以外）
- 该机制歧视州际贸易（州内发电机获得免费分配，州外发电机没有）
- 它对进口施加比同等州内发电更高的负担

*支持进口机制（加州的辩护）：*
- 合规义务在进口商（加州实体），不在州外发电机
- "效果测试"：加州可以规范在加州做出的消费决策的环境影响
- 市场参与者原则：购买电力的加州公用事业是市场参与者

**当前状态（2025年）：** 诉讼进行中。对挑战者有利的裁决将显著削弱加州的碳定价设计，并可能削弱RGGI的无进口结构。

**博士研究空白：** DCC-碳定价相互作用是一个丰富的研究领域。关键问题：
- DCC doctrine在什么条件下适用于环境进口费？
- 联邦碳价格会优先于州进口机制吗？
- 法律不确定性本身的福利成本是多少（减少双边合同、对冲投资）？

---

## 6. 定量数据摘要

| 指标 | 加州 | RGGI | 联邦（如有） |
|------|------|------|-------------|
| 配额价格（2024-2025年） | $35-45/吨 | $22-30/吨 | 不适用 |
| 配额轨迹 | 2030年比1990年低40% | 到2030年每年下降2.5% | 不适用 |
| 进口合规 | 是（AB 398） | 否 | 不适用 |
| 收入回收 | 25%用于消费者回扣，20%用于清洁能源 | 40-60%用于消费者项目 | 不适用 |
| 已实现CO₂减排 | 约35%低于1990年（2023年） | 约50%低于2005年（2023年） | 不适用 |
| 电力行业覆盖 | 约占加州排放的60% | 约占RGGI排放的75% | 不适用 |

**排放减少结果：**
- 加州总量管制与交易：加州电力行业CO₂从约100 MMT（峰值）降至约55 MMT（2023年）——由燃气联合循环替代和可再生能源建设驱动
- RGGI：RGGI州电力行业CO₂从约165 MMT（2009年）降至约65 MMT（2023年）——由廉价天然气价格+RGGI碳价格加速的煤炭退役驱动的60%下降

**收入回收效应：** 两个项目都将收益部分返还给电力消费者，部分资助清洁能源项目。实证问题是价格效应（更高的电价）是否完全抵消了回扣（净发生率）。

---

## 7. 博士开放研究问题

1. **传导异质性：** 碳成本对LMP的传导率如何随日内时间、季节和年份变化？随着可再生能源渗透率增长（边际机组从燃气变为可再生能源+碳），传导率会增加吗？
2. **泄漏量化：** 碳定价的州内减排中有多少比例被邻州排放增加所抵消？估计范围为10-50%——该范围反映了关于反事实的基本方法论分歧。
3. **DCC +碳定价：** 适用于进口的州碳定价的宪法边界是什么？州能否根据Dormant Commerce Clause法理学实施符合宪法的边境碳调整？
4. **碳价格与容量市场相互作用：** 如果PJM或CAISO正式将碳成本整合到调度中（如一些经济学家所提议），容量市场出清价格会发生什么？答案取决于容量认证是否考虑了碳成本驱动的燃料转换。
5. **一般均衡效应：** 区域碳定价创造了驱动产业重新布局的电力价格差异。这种"竞争力"关切是真实的，还是被主导的生产者剩余损失所捕获？加州与德州特定碳定价的CGE建模可以量化这一点。
6. **碳价格不确定性下的投资：** 配额价格波动如何影响燃气调峰与储能 vs. 可再生能源的新建决策？碳价格不确定性下投资的实物期权估值。

---

## 8. 关键参考文献

- Cullen, J.A. & Mansur, E.T. (2017). "Inferring Carbon Abatement Costs from Electricity Market Prices." *Journal of the Association of Environmental and Resource Economists* 4(3).
- LaRiviere, J. & Wilson, R. (2022). "The Incidence of Carbon Pricing in Electricity Markets." *Journal of Environmental Economics and Management* 114.
- Novan, K. (2015). "Valuation of Local Air Quality in Electricity Markets." *Journal of Environmental Economics and Management* 72.
- Jones, L.E. (2019). "Carbon Pricing in the United States." *Review of Environmental Economics and Policy* 13(1).
- Murray, B., & Sobin, N. (2023). "Carbon Leakage and the Electricity Sector." *Energy Economics*.
- Fowlie, M., & Reguant, M. (2023). "Edge-of-Rock: Energy Markets and Climate Policy." *Journal of Economic Perspectives* 37(4).
- CAISO (2024). *Annual Market Performance Report* — 包括碳成本传导分析
- RGGI Inc. (2024). *RGGI Program Review — Auction Results and Emissions Data*
- EPA (2023). *eGRID* — 按发电机和地区的排放率

---

*最后更新：2026-05-07*
*相关：[[ferc-jurisdiction-carbon]]，[[social-cost-carbon-dispatch]]，[[state-rps-effectiveness]]*

---

# English Version

# Carbon Pricing Integration in US Wholesale Electricity Markets

> **Prerequisites:** [[locational-marginal-pricing]], [[ancillary-services-market]], [[electricity-markets-day-ahead-real-time]]

---

## 1. Overview: Why Carbon Pricing Matters for Electricity Markets

Carbon pricing represents the most economically efficient approach to internalizing CO₂ externalities in wholesale electricity markets. Unlike technology mandates or renewable portfolio standards—which prescribe *how* to reduce emissions—a carbon price lets the market discover the *lowest-cost* abatement pathway through the dispatch merit order.

The fundamental mechanism: a carbon price adds `C × emission_factor` (USD/MMBtu × tons CO₂/MMBtu) to every generator's marginal cost. This shifts the dispatch merit order, retires high-emitting units at the margin, and creates explicit incentives for gas-to-renewable fuel switching. The elegance is that every generator, every hour, responds to the same price signal without requiring case-by-case regulatory intervention.

### Two Structural Approaches

| | Cap-and-Trade (Market-Based) | Carbon Tax (Price-Based) |
|-|---|---|
| **Examples** | CA cap-and-trade, RGGI, Regional Clean Electricity | None currently at US state level |
| **Price certainty** | Low (allowance price volatility) | High |
| **Quantity certainty** | High (caps decline on schedule) | Low |
| **Emission outcome** | Guaranteed by cap | Depends on price level |
| **Political feasibility** | Lower (free allocation debates) | Higher (simpler) |

The US has no federal carbon pricing for electricity. State-level programs are the primary mechanism. This creates a **fragmented carbon pricing landscape** — 11 RGGI states plus California — that interacts with wholesale electricity markets in complex ways.

---

## 2. State Carbon Pricing Programs

### 2.1 California Cap-and-Trade (AB 398)

California's cap-and-trade program, established under AB 32 (2006) and extended through AB 398 (2017), is the most comprehensive carbon market in North America.

**Program Structure:**
- **Cap trajectory:** 2013 startup → 40% below 1990 levels by 2030 (AB 398 target)
- **Annual cap decline:** ~3% per year through 2030
- **Coverage:** ~80% of statewide GHG emissions, including electricity imported from other states
- **Market participants:** Covered entities (industrial facilities, electricity retailers) must surrender allowances equal to emissions
- **Linking:** Linked with Quebec cap-and-trade since 2014

**Allowance Supply Mechanism:**
- ~60-70% of allowances auctioned
- ~30-40% via free allocation (gradually declining)
- Price floor: ~$22.71/ton (2020), rising ~5% + CPI annually
- Current clearing prices (2024-2025): **$35-45/ton CO₂** (auction results)

**Electricity Sector Effects:**
- In-state generators: Face direct compliance costs
- Imports: Face "upstream" compliance obligation for electricity imported into California (enforced since AB 398)
- The import compliance mechanism means out-of-state coal plants burning for CA consumption face carbon costs
- Natural gas: ~53 kg CO₂/MMBtu; adds ~$18-24/MMBtu at $35-45/ton
- Effect on gas CCGT marginal cost: ~$18-24/MMBtu × heat rate of 7,000 BTU/kWh = **$126-168/MWh** added to gas marginal cost

**NEM 3.0 Interaction:** The transition to Net Billing Tariff (2023) for solar prosumers creates a parallel pricing signal. Prosumers facing low export tariffs increasingly shift toward self-consumption and storage — aligning with the carbon price signal that penalizes grid consumption from fossil sources.

### 2.2 RGGI (Regional Greenhouse Gas Initiative)

RGGI is the oldest mandatory CO₂ cap-and-trade program in the US — covering electricity sector emissions since 2009 across 11 Northeast/Mid-Atlantic states: CT, DE, ME, MD, MA, NH, NJ, NY, RI, VT, VA.

**Program Structure:**
- Cap: Declines 2.5% annually through 2030, then 3% annually through 2040
- Coverage: Power plants > 25 MW
- Allowance distribution: ~60% auctioned, ~40% free allocation (declining)
- Cost-containment: Containment Reserve (2% of annual cap released at $XX/ton trigger price)

**RGGI Allowance Prices:**
- 2014-2016: $4-8/ton (oversupply, low natural gas prices)
- 2019: $4-6/ton (historic lows)
- 2021: ~$13/ton
- 2022: ~$13/ton
- 2023: ~$15-17/ton
- 2024-2025: **$22-30/ton** (significant price increase driven by cap tightening and HFO market effects)

RGGI prices are substantially lower than CA prices, reflecting the different caps, allocation methods, and the competitive pressure from low-cost natural gas in the PJM/MISO footprint.

**Key Distinction from CA:** RGGI does NOT include electricity imports in its compliance mechanism — a critical difference that means out-of-state fossil generation serving RGGI state load often escapes carbon pricing. This is the central legal vulnerability being litigated.

### 2.3 Complementary State Carbon Pricing

- **Washington State:** Clean Energy Transformation Act (2019) mandates coal-free electricity by 2025 and net-zero by 2030 — not a direct carbon price, but binding renewable/car-free standards
- **New York:** Climate Leadership and Community Protection Act (CLCPA) — aggressive renewable mandate (70% by 2030, 100% by 2040) plus a proposed carbon pricing mechanism under the "Carbon Cap-and-Invest" program (under development as of 2025)
- **Oregon:** Cap-and-invest legislation passed in 2021 (Clean Energy Targets and Trade)

---

## 3. How Carbon Costs Enter Dispatch and Affect LMP

### 3.1 The Mechanism: Carbon Cost in Merit Order

Every dispatchable generator has a marginal cost composed of:

```
MC_g = fuel_cost_g + VOM_g + startup_cost/cycle + carbon_cost_g
```

Where `carbon_cost_g = emission_rate_g × carbon_price`

For a natural gas combined-cycle turbine:
- Fuel cost: ~$2.50/MMBtu
- Heat rate: 7,000 BTU/kWh
- Fuel MC: ~$17.5/MWh
- Emission rate: 0.053 t CO₂/MMBtu (natural gas)
- At $40/ton CO₂: carbon MC: 0.053 × $40 = **$2.12/MMBtu → $14.84/MWh**

For a coal unit:
- Fuel cost: ~$2.00/MMBtu
- Heat rate: 10,000 BTU/kWh
- Emission rate: 0.093 t CO₂/MMBtu (bituminous coal)
- At $40/ton CO₂: carbon MC: 0.093 × $40 = **$3.72/MMBtu → $37.20/MWh**

**Effect on merit order:** The carbon cost disproportionately raises coal's marginal cost, often moving it above gas CCGT in the dispatch stack. At $40-50/ton CO₂, the carbon cost can add $40-80/MWh to coal's marginal cost — sufficient in many hours to push coal out of the money entirely.

### 3.2 Pass-Through Rate to Wholesale Electricity Prices

A critical empirical question: **how much of the carbon cost is passed through to wholesale electricity prices (LMP)?**

The pass-through rate depends on market conditions, generator mix, and the residual demand curve:

- **In competitive markets with gas-on-the-margin:** Carbon costs on gas generators pass through to LMP proportionally (pass-through rate ≈ 1.0)
- **In markets with significant coal retirements:** When coal exits the stack, the competitive benchmark shifts to gas + carbon cost → higher pass-through
- **In PJM/ERCOT (energy-only):** Pass-through is immediate — carbon cost is simply added to marginal cost
- **In CAISO (with high renewables):** In hours where renewables set the price (negative LMP), the carbon cost on thermal units may not appear in spot prices — but the capacity value and backstop role retains economic significance

**Academic Evidence:**
- Cullen & Mansur (2017, *Journal of the Association of Environmental and Resource Economists*): Using RGGI, estimated that a $10/ton carbon price increased wholesale electricity prices in RGGI states by ~$6-8/MWh — a pass-through rate of 60-80% in the short run
- The remainder of the carbon cost was absorbed by inframarginal rent changes (retired generators' sunk costs) and reduced consumer bills from cleaner dispatch
- LaRiviere & Wilson (2022): Found that CA cap-and-trade increased CAISO wholesale prices by ~$5-10/MWh, with full pass-through in hours where gas sets the margin
- Novan (2015, *Journal of Environmental Economics and Management*): Found significant but incomplete pass-through of NOₓ and SO₂ allowance prices to electricity prices, with heterogeneity by location and hour

### 3.3 Impact on LMP Components

Recall from [[locational-marginal-pricing]] that LMP has three components:

```
LMP = Energy Component + Congestion Component + Loss Component
```

Carbon pricing interacts with all three:

- **Energy Component:** The primary effect — carbon cost shifts the marginal unit, raising the market-clearing price in hours where fossil units are marginal
- **Congestion Component:** Carbon costs can alter flows across transmission constraints, potentially improving or worsening congestion patterns. High-carbon generators near load centers may be displaced by lower-carbon distant generators, changing which constraints bind
- **Loss Component:** Secondary effect via changed generation dispatch patterns

**California Import Effect:** California's import compliance mechanism means that coal imports face carbon costs. This raises the LMP in southern California import-constrained regions where some power historically came from out-of-state coal — but the effect is embedded in CAISO's import pricing rules.

---

## 4. Economic Frameworks

### 4.1 Internalization of Externalities in Wholesale Markets

The first-best outcome under certainty: **marginal damage pricing** — set the carbon price equal to the marginal external damage from CO₂ emissions. The market then automatically finds the least-cost abatement.

However, several complications make this a second-best problem:

1. **Uncertainty about the SCC:** We don't know the true marginal damage. Current estimates range from $20/ton (low) to $200+/ton (high, IAM tail risks)
2. **Leakage:** Without a border carbon adjustment or import equivalent, carbon pricing in one jurisdiction shifts emissions to unregulated jurisdictions ("carbon leakage")
3. **Interaction with existing regulations:** Many fossil generators already face Title IV SO₂/NOₓ acid rain regulations, New Source Review, etc. — carbon pricing layers on top of existing compliance costs
4. **Market power:** In transmission-constrained nodes, the congestion component of LMP may already extract surplus from buyers — carbon pricing on a constrained network can compound this

### 4.2 Incidence of Carbon Taxation

Who bears the burden of carbon pricing in electricity markets?

**Producer incidence:** High-emission generators (coal, older gas steam) bear the initial cost shock. If they cannot pass through, they exit. This has played out dramatically — US coal-fired generation fell from ~50% of total generation in 2008 to ~17% in 2023, with carbon pricing playing an accelerating role alongside cheap gas.

**Consumer incidence:** Electricity is relatively **price-inelastic** (short-run elasticity: -0.1 to -0.3), meaning most of the burden falls on consumers. However:
- Cross-subsidization through free allocation can protect incumbent generators
- Household-level effects are regressive: low-income households spend a higher share of income on electricity, so carbon pricing is regressive unless revenue is recycled as per-capita rebates (the "Dividend" approach)

**Distributional effects within electricity markets:**
- Residential consumers with rooftop solar + storage can partially exempt themselves (self-consumption avoids both grid electricity price and carbon cost)
- Low-income communities near coal plants benefit disproportionately from retirements (reduced local PM₂.₅, NOₓ)
- Communities dependent on coal mining employment face concentrated economic harm — a major political economy challenge

### 4.3 Fragmented Carbon Pricing: State vs. Federal

The US has no federal carbon price. State programs create a patchwork:

**The Problem: Uneven Playing Field**

A state with carbon pricing (CA, RGGI states) imposes compliance costs on in-state generators, raising their wholesale electricity prices relative to neighboring states without carbon pricing (TX, LA, GA). This creates:

1. **Competitive disadvantage** for carbon-priced state industries (electricity-intensive manufacturers)
2. **Cross-state electricity flows** that arbitrage the carbon price: power flows from low-carbon-price to high-carbon-price regions, potentially increasing total system emissions (a form of "carbon leakage" via electricity trade)
3. **Emission leakage** via investment: new gas generation investments are attracted to non-carbon-priced states, increasing their share of future generation

**Theoretic Framework — Jones (2019, *Review of Environmental Economics and Policy*):**
Carbon pricing in one state with a competitive wholesale market leads to higher electricity imports from neighboring states and lower wholesale prices in the pricing state — the "border carbon" effect partially offsets the environmental benefit.

**Solutions proposed:**
- **Federal carbon price** (the first-best fix, politically blocked)
- **Regional linkage** of state programs (CA-Quebec model, RGGI expansion)
- **Border carbon adjustments** for imported electricity (California's approach for imports)
- **Clean electricity standard** as an alternative federally-mandated quantity approach

---

## 5. The Dormant Commerce Clause Problem

The US Constitution's Dormant Commerce Clause (DCC) prohibits states from discriminating against or unduly burdening interstate commerce. This creates a fundamental legal tension with state carbon pricing applied to imported electricity.

**The Core Problem:**
California's AB 398 import compliance mechanism requires out-of-state generators to surrender California carbon allowances for electricity imported into California. Challengers (including the Sempra/US Utility Air Regulatory Group coalition) argue this is an unconstitutional burden on interstate commerce.

**Key Legal Arguments:**

*Against the import mechanism (DCC challenge):*
- States cannot regulate extraterritorially (emissions occur outside CA)
- The mechanism discriminates against interstate commerce (in-state generators receive free allocation, out-of-state generators don't)
- It imposes a higher burden on imports than equivalent in-state generation

*For the import mechanism (CA's defense):*
- The compliance obligation is on the importer (CA entity), not the out-of-state generator
- The "effects test": CA can regulate the environmental effects of consumption decisions made within CA
- The market participant doctrine: CA utilities buying power are market participants

**Current Status (2025):** The litigation is ongoing. A favorable ruling for challengers would significantly weaken CA's carbon pricing design and potentially RGGI's import-free structure.

**PhD Research Gap:** The DCC-carbon pricing interaction is a rich area. Key questions:
- Under what conditions does DCC doctrine apply to environmental import fees?
- Would a federal carbon price preempt state import mechanisms?
- What is the welfare cost of the legal uncertainty itself (reduced investment in bilateral contracts, hedging)?

---

## 6. Quantitative Data Summary

| Metric | California | RGGI | Federal (if any) |
|--------|---|---|---|
| Allowance price (2024-2025) | $35-45/ton | $22-30/ton | N/A |
| Cap trajectory | 40% below 1990 by 2030 | 2.5%/yr decline to 2030 | N/A |
| Import compliance | Yes (AB 398) | No | N/A |
| Revenue recycling | 25% to consumer rebate, 20% to clean energy | 40-60% to consumer programs | N/A |
| CO₂ reduction achieved | ~35% below 1990 (2023) | ~50% below 2005 (2023) | N/A |
| Electricity sector covered | ~60% of CA emissions | ~75% of RGGI emissions | N/A |

**Emission reduction outcomes:**
- CA cap-and-trade: Electricity sector CO₂ in CA fell from ~100 MMT (peak) to ~55 MMT (2023) — driven by gas CCGT displacement and renewable buildout
- RGGI: Power sector CO₂ in RGGI states fell from ~165 MMT (2009) to ~65 MMT (2023) — a 60% reduction driven by coal retirements accelerated by low gas prices + RGGI carbon price

**Revenue recycling effects:** Both programs partially return proceeds to electricity consumers, partially funding clean energy programs. The empirical question is whether the price effect (higher electricity prices) fully offsets the rebate (net incidence).

---

## 7. Open Research Questions for PhD

1. **Pass-through heterogeneity:** How does the carbon cost pass-through rate to LMP vary by time-of-day, season, and year? Does pass-through increase as renewable penetration grows (changing the marginal unit from gas to renewables + carbon)?
2. **Leakage quantification:** What fraction of in-state emission reductions from carbon pricing is offset by increased emissions from neighboring states? Estimates range from 10-50% — the range reflects fundamental methodological disagreements about counterfactuals.
3. **DCC + carbon pricing:** What is the constitutional boundary for state carbon pricing applied to imports? Can states impose border carbon adjustments consistent with Dormant Commerce Clause jurisprudence?
4. **Carbon price interaction with capacity markets:** If PJM or CAISO formally integrates a carbon cost into dispatch (as some economists propose), what happens to capacity market clearing prices? The answer depends on whether capacity accreditation accounts for carbon-cost-driven fuel switching.
5. **General equilibrium effects:** Regional carbon pricing creates electricity price differences that drive industrial relocation. Is this "competitiveness" concern real, or is it captured by producer surplus losses that dominate? CGE modeling of CA- vs. TX-specific carbon pricing could quantify this.
6. **Investment under carbon price uncertainty:** How does allowance price volatility affect new build decisions for gas peakers vs. storage vs. renewables? Real options valuation of investment under carbon price uncertainty.

---

## 8. Key References

- Cullen, J.A. & Mansur, E.T. (2017). "Inferring Carbon Abatement Costs from Electricity Market Prices." *Journal of the Association of Environmental and Resource Economists* 4(3).
- LaRiviere, J. & Wilson, R. (2022). "The Incidence of Carbon Pricing in Electricity Markets." *Journal of Environmental Economics and Management* 114.
- Novan, K. (2015). "Valuation of Local Air Quality in Electricity Markets." *Journal of Environmental Economics and Management* 72.
- Jones, L.E. (2019). "Carbon Pricing in the United States." *Review of Environmental Economics and Policy* 13(1).
- Murray, B., & Sobin, N. (2023). "Carbon Leakage and the Electricity Sector." *Energy Economics*.
- Fowlie, M., & Reguant, M. (2023). "Edge-of-Rock: Energy Markets and Climate Policy." *Journal of Economic Perspectives* 37(4).
- CAISO (2024). *Annual Market Performance Report* — includes carbon cost pass-through analysis
- RGGI Inc. (2024). *RGGI Program Review — Auction Results and Emissions Data*
- EPA (2023). *eGRID* — emissions rates by generator and region

---
*Last updated: 2026-05-07*
*Related: [[ferc-jurisdiction-carbon]], [[social-cost-carbon-dispatch]], [[state-rps-effectiveness]]*
