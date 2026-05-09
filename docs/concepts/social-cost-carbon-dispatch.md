# 社会碳成本在电力调度中的应用

> **Prerequisites:** [[carbon-pricing-integration]], [[locational-marginal-pricing]], [[environmental-justice-energy]]

---

## 1. 概述：为何将SCC纳入调度？

**社会碳成本（SCC）** 是对排放一吨CO₂所造成的经济损失的估计。与碳税或总量管制与交易的配额价格不同，SCC是一个*监管核算工具*——用于评估将气候影响纳入考量后，法规、基础设施投资或市场规则是否具有社会效益。

**它填补的缺口：** 私营市场主体（发电商、公用事业、消费者）基于私人成本——燃料、资本、运营维护——做出调度和投资决策。他们无需为其决策所排放的CO₂的社会成本买单。将SCC纳入调度算法可以在市场层面纠正这一外部性。

**关键区别：**
- **碳合规成本**（加州总量管制与交易35-45美元/吨，RGGI 22-30美元/吨）：发电商实际支付的费用
- **社会碳成本**（中央估计值51美元/吨，2023年EPA更新）：社会为每吨排放实际承担的成本

合规成本与SCC之间的差距代表了未定价的外部性——市场价格系统性地低估了化石燃料发电的真实成本。

---

## 2. 社会碳成本：方法论与估计

### 2.1 SCC如何计算

SCC源自综合评估模型（IAM）——结合以下要素的框架：
1. **气候模块：** 模拟CO₂浓度、辐射强迫、温度响应、海平面上升
2. **经济模块：** 模拟温度变化与经济产出（GDP增长、分部门损害）之间的关系
3. **折现：** 将未来损害以现值衡量

**SCC计算的三个关键组成部分：**

**气候损害 D(T)：** IAM将经济损失估计为全球平均温度升高T(°C)的函数：
- D(T) = α × T² × 世界GDP
- 二次方形式反映了随温度升高而递增的边际损害
- 1°C时：约0.1-0.3%的GDP损失
- 3°C时：约2-5%的GDP损失
- 5°C时：约10-20%的GDP损失

**损害函数估计差异很大：**
- Nordhaus（DICE模型）：中等损害
- Stern（斯恩回顾）：高损害（使用较低折现率）
- Hope（PAGE模型）：高损害，尾部不确定性较大

**折现率：**
折现率的选择是SCC估计中最具争议的参数：
- 低折现率（1-2%）：高度重视未来世代；SCC更高
- 高折现率（3-5%）：更重视当前消费；SCC更低
- EPA 2023年更新：使用2%折现率作为中央估计

### 2.2 当前SCC估计

**EPA 2023年技术support文件更新：**

| 折现率 | SCC估计（2020年美元/吨CO₂） |
|---|---|
| 5%（高） | 约14美元/吨 |
| 3%（中） | 约28美元/吨 |
| 2.5%（中） | 约38美元/吨 |
| 2%（中央） | 约51美元/吨 |
| 1.5%（低） | 约76美元/吨 |
| 1%（极低） | 约120美元/吨 |

**关键不确定性：** 第95百分位SCC（高损害、低折现率）约200+美元/吨——是中央估计的10倍以上。这种尾部风险对监管分析至关重要，但为市场设计创造了巨大的不确定性。

**SCC轨迹：**
- EPA 2023年SCC（2%折现率51美元/吨）高于2021年估计（2021年曾为40美元/吨）——不是因为更新了科学，而是因为更新了经济预测
- SCC随时间增长：2%折现率下2030年SCC：约55-65美元/吨；2050年SCC：约70-85美元/吨
- 这种增长反映了累积排放造成的损害增加以及有限的剩余减排机会

### 2.3 代际折现问题

**为什么折现率如此重要：** 折现率的选择反映了一个基本的伦理问题：当前世代应该为未来世代牺牲多少？

**纯时间偏好率（ρ）：** 如果ρ=0，我们平等地重视今天活着的人和100年后活着的人的福利。如果ρ=3%，我们实际上是说今天的1美元福利相当于100年后的95美元福利。

**Stern与Nordhaus的争论：**
- Stern（2006年）：ρ = 0.1-0.5%，SCC约200-300美元/吨——未来气候损害是灾难性的
- Nordhaus（2008年）：ρ = 3%，SCC约20-40美元/吨——经济增长将使未来世代更富有、更有能力适应

**SCC的Ramsey方程：** SCC = 一吨CO₂的边际损害 = D'(T) + 气候反馈 × 灾难概率

---

## 3. SCC如何进入经济调度

### 3.1 调度算法

经济调度在满足输电约束的条件下最小化满足负荷的总成本：

```
最小化：Σ [MC_g × Q_g]  （所有发电商的加总）

约束条件：
  Σ Q_g = 负荷 + 损耗
  Q_g ≤ Q_g^max  对所有g
  满足输电约束
```

其中 `MC_g` = 发电商g的边际成本

**将SCC纳入会在边际成本中加入碳项：**

```
MC_g_with_SCC = MC_g + (排放率_g × SCC)
```

对于天然气联合循环燃气轮机（CCGT）：
- MC_g（燃料+变动运维）：约20-35美元/MWh
- 排放率：0.053 t CO₂/MMBtu × 7,000 BTU/kWh = 0.371 t CO₂/MWh
- SCC项：0.371 × 51美元 = **18.91美元/MWh**
- 总MC：约38-54美元/MWh

对于燃煤机组：
- MC_g：约25-40美元/MWh
- 排放率：0.093 t CO₂/MMBtu × 10,000 BTU/kWh = 0.93 t CO₂/MWh
- SCC项：0.93 × 51美元 = **47.43美元/MWh**
- 总MC：约72-87美元/MWh

**对调度的影响：** SCC使煤的边际成本比天然气高出25-35美元/MWh——足以在许多天然气已经具有竞争力的时段将煤推出调度优先顺序。

### 3.2 对市场清算价格的影响

**SCC在LMP中的作用：**

将SCC纳入调度会通过两种方式改变市场清算价格：

1. **直接效应：** 发电商的边际成本按其排放率×SCC上升→所有LMP上升
2. **调度效应：** 更清洁的发电商被优先调度→在许多时段边际机组从煤转向燃气或可再生能源→这些时段的LMP可能实际上下降

**按小时类型的净效应：**

| 小时类型 | 无SCC | 有SCC（51美元/吨） | 备注 |
|---|---|---|---|
| 煤在边际 | LMP = MC_煤 | LMP = MC_煤 + 47美元/MWh | 大幅上涨 |
| 气在边际 | LMP = MC_气 | LMP = MC_气 + 19美元/MWh | 中等上涨 |
| 光/风在边际 | LMP ≈ 0美元 | LMP ≈ 0美元（无变化） | 零边际成本可再生能源不受影响 |
| 储能套利 | 低 | 中等上涨 | 储能充电更清洁，放电也更清洁 |

**反直觉结果：** SCC可能会高可再生能源渗透率市场的平均LMP*降低*——因为更多光/风被调度，减少了燃气CCGT处于边际的小时数。但在煤电占比高的市场（MISO、SPP），SCC会大幅推高价格。

### 3.3 动态效率效应

超越静态调度，SCC的纳入创造了动态投资激励：

**短期（1-5年）：**
- 调度立即转向燃气和可再生能源
- 本来处于边际的煤电机组变得次边际
- 部分煤电机组退役加速

**中期（5-15年）：**
- 新投资决策偏向燃气CCGT和可再生能源而非煤
- 储能更具吸引力（从燃气充电，在高峰时段放电）
- 需求响应价值增加（减少化石机组运行的时段）

**长期（15-30年）：**
- 发电组合实质性转向零碳资源
- SCC增长轨迹（随时间上升）创造了化石资产早期退役的日益增强的激励
- 新化石投资"搁浅资产"风险急剧增加

---

## 4. SCC与现有碳定价计划的比较

### 4.1 SCC与合规碳价格之间的差距

美国电力市场碳定价最显著的事实：合规碳价格远低于SCC：

| 碳价格来源 | 价格（美元/吨CO₂） | vs. SCC（51美元/吨） |
|---|---|---|
| 加州总量管制与交易（2024-25年） | 35-45 | SCC的约70-90% |
| RGGI配额（2024-25年） | 22-30 | SCC的约45-60% |
| 欧盟ETS配额（2024年） | 60-80 | SCC的约120-160% |
| SCC中央估计 | 51 | 100%（按定义） |
| SCC第95百分位 | 约200 | 合规价格的400% |

**含义：** 即使是最积极的美国碳定价计划（加州）也只将碳价定在SCC的70-90%。RGGI只有45-60%。差距意味着大量未定价的外部性仍然存在。

### 4.2 SCC作为监管工具vs.市场价格

**SCC作为监管核算工具：** 联邦机构使用SCC根据第12866号行政命令（监管规划与审查）评估法规。任何重大联邦法规（清洁空气规则、燃油经济标准、电力法规）都必须使用SCC量化效益。

**SCC使用示例：**
- EPA的《清洁电力计划》（2015年）使用SCC估算CO₂减排的气候效益
- CAFE燃油经济标准使用SCC证明更严格标准的合理性
- FERC基础设施批准（天然气管道、LNG终端）使用SCC评估上游排放

**SCC作为市场设计工具：** 将SCC直接纳入批发电力市场调度算法是另一种用途：
- 它将SCC从监管核算工具转变为*运营市场信号*
- 每个发电商的边际成本都将反映SCC
- 市场将自动内化外部性
- 这是经济学家普遍优于命令控制式法规的选择

### 4.3 为什么不直接用SCC代替碳合规市场？

**使用基于SCC的调度而非合规市场的论据：**
1. **统一价格信号：** SCC将统一适用于所有发电商，消除了加州总量管制与交易州与非碳定价州之间的竞争扭曲
2. **正确幅度：** SCC反映实际社会成本；合规市场可能定价过低（或过高）
3. **无泄漏：** 在RTO/ISO调度中强制实施联邦SCC将消除跨州泄漏问题

**反对意见（实施案例）：**
1. **SCC不确定性：** 范围（14-200+美元/吨）巨大——错误的SCC可能导致过度或不足投资
2. **法律权威：** FERC缺乏明确法定授权，在无国会行动的情况下强制实施基于SCC的碳费（见[[ferc-jurisdiction-carbon]]）
3. **政治接受度：** 基于SCC的电价将面临政治争议——"隐藏碳税"框架
4. **需要更新：** SCC估计每隔几年更新一次；基于SCC的市场设计将需要定期重新校准

---

## 5. 基于SCC调度的总体均衡效应

### 5.1 电力部门vs.整体经济效应

基于SCC的调度改变电力部门行为，但总体均衡效应很重要：

**直接效应：** 更清洁调度的CO₂减排
- 估计美国电力部门在51美元/吨SCC调度下10年内减排20-35%

**间接效应：**
1. **回弹效应：** 更低电价（来自更多可再生能源调度）→增加电力消费→部分抵消CO₂减排
2. **燃料价格效应：** 减少的燃气/煤需求→降低燃料价格→增加其他部门的燃气消费
3. **投资效应：** 更低电价吸引更多电力密集型产业（数据中心、电动车、回流制造业）→增加电力需求
4. **资本重新配置：** 减少化石发电投资→搁浅资产→金融部门敞口

### 5.2 宏观经济效应

**GDP影响：** 大多数估计发现，SCC水平的碳定价对GDP的负面影响较小（10年内1-3%）——但这些估计高度依赖于收入如何回收：
- 收入中性回收（人均股息）：最小GDP影响
- 收入用于一般政府支出：小的负面GDP效应
- 收入用于企业减税：小的正面GDP效应

**索洛增长模型视角：** 气候变化本身就是长期经济增长的拖累。以SCC水平定价碳减少了这种拖累——当气候损害被完全计入时，对长期GDP的净效应可能是正的。

---

## 6. SCC在容量充足性中的应用

### 6.1 SCC如何影响容量决策

容量充足性决策（我们应该建设新的燃气调峰机组吗？）取决于预期的未来收入流。SCC改变了这些计算：

**没有SCC：** 燃气调峰机组的收入需求 = 资本成本 + 固定运维 + 燃料成本
- 如果预期能源市场收入覆盖这一成本→建设它

**有SCC（51美元/吨）：** 燃气调峰机组运行时排放0.371 t CO₂/MWh
- 每MWh的SCC成本 = 0.371 × 51美元 = 18.91美元/MWh
- 这实际上是一种必须回收的额外"燃料成本"
- 相对于电池，峰值机组变得不那么经济

**"经SCC调整的"调峰经济性：** 一台100 MW燃气调峰机组每年运行300小时，能源100美元/MWh + SCC 19美元/MWh = 119美元/MWh
- 对比：4小时电池在20美元/MWh充电，在80美元/MWh放电（无SCC）
- 如果电池能够获得足够的价格价差，电池在总成本基础上获胜

### 6.2 SCC与最优储备裕度

SCC改变了最优储备裕度：

**直觉：** 更多发电容量→更少的发电稀缺→更低的批发电价→每单位发电的SCC损害更低（因为边际机组排放更少）
- 但更多容量也意味着更多资本成本
- 最优储备裕度在资本成本与经SCC调整的稀缺风险之间取得平衡

**复杂之处：** SCC是全球总体损害度量。一单位额外MWh发电的边际损害取决于该发电发生的地点（电网状况）和时间（决定被替代的边际机组）。一个地点/时间特定的SCC将比统一全国SCC更准确。

---

## 7. 与现有州碳定价的互动

### 7.1 重复计算问题

如果发电商已在加州总量管制与交易（35-45美元/吨）中，SCC（51美元/吨）也被加入调度，这是否重复计算了碳成本？

**解决方案：** 这两种成本衡量的是不同的事物：
- **加州总量管制与交易：** 发电商为其CO₂排放*支付*多少（私人成本）
- **SCC：** 社会为CO₂排放的外部损害*支付*多少（社会成本）

51美元（SCC）与40美元（加州价格）之间的差距 = 11美元/吨——这是在加州总量管制与交易之后仍存在的未定价外部性。SCC加法捕捉了这一剩余差距。

**但是：** 支付加州总量管制与交易价格的发电商不应在批发电力市场中额外支付SCC费用——那是重复计算。正确的实施是：
- 对于加州发电商：SCC加法 - 加州配额价格 = 额外加法
- 对于非加州、非碳定价州的发电商：全额SCC加法

### 7.2 碳价格增长轨迹

**SCC轨迹：** EPA中央SCC实际增长约2%/年（反映气候损害增长）

**合规碳价格轨迹：**
- 加州总量管制与交易：配额减少约3%/年→预期配额价格将上升
- RGGI：配额到2030年减少2.5%/年→预期价格将上升
- 欧盟ETS：随着配额收紧，价格趋势向上

SCC与合规价格之间的差距可能随着碳市场收紧而缩小——或者如果SCC更新反映新的损害科学，可能扩大。

---

## 8. 定量情景

### 8.1 调度模拟结果

**情景：51美元/吨SCC应用于所有美国RTO/ISO调度（2024年）**

**估计年度CO₂减排：电力部门排放的25-40%**
- 基础：2024年电力部门CO₂ ≈ 16亿吨/年
- 减排估计：4-6.4亿吨/年

**平均批发电价影响：**
- 全国平均LMP上涨：+5-15美元/MWh
- 这相当于零售电价上涨约1-3美分/kWh
- 取决于传导率和当地发电组合

**福利分析：**
- 气候效益：51美元/吨 × 4-6.4亿吨 = 每年避免气候损害20-330亿美元
- 消费者成本增加：约5-15美元/MWh × 4,000太瓦时 = 每年200-600亿美元
- 净福利：取决于SCC准确性；如果SCC正确，净福利为正

### 8.2 区域差异

| 区域 | CO₂强度 | SCC影响（美元/MWh） | 预期价格上涨 |
|---|---|---|---|
| MISO（煤电为主） | 约800 kg/MWh | 约40美元/MWh | +15-25美元/MWh |
| SPP（煤电为主） | 约700 kg/MWh | 约36美元/MWh | +12-20美元/MWh |
| PJM（混合） | 约450 kg/MWh | 约23美元/MWh | +8-15美元/MWh |
| ERCOT（气电为主） | 约400 kg/MWh | 约20美元/MWh | +7-12美元/MWh |
| CAISO（清洁） | 约200 kg/MWh | 约10美元/MWh | +3-8美元/MWh |

*SCC影响 = 区域CO₂强度 × 51美元/吨；平均价格上涨取决于化石燃料处于边际的小时比例*

---

## 9. 开放研究问题

1. **地点/时间特定的SCC：** SCC是否应根据地点（反映区域气候脆弱性）和时间（反映高峰需求时段边际损害更高）而变化？当前统一SCC可能不准确。
2. **SCC折现率共识：** 经济学家能否就气候政策适当折现率达成共识？折现率选择导致的SCC 3-5倍差异是最大的不确定性来源。
3. **SCC可信度：** 如果SCC被纳入市场调度，估计必须可信、透明并定期更新。谁负责更新SCC——EPA、FERC还是独立委员会？
4. **与容量市场互动：** 能源市场纳入SCC是否改变最优容量市场设计？容量认证是否也应该反映经SCC调整的排放？
5. **不确定性下的SCC：** 鉴于SCC估计范围广泛（14-200+美元/吨），市场设计应如何处理这种不确定性？鲁棒优化方法vs.点估计。
6. **国际碳定价协调：** 如果美国将SCC纳入调度，对国际竞争力和碳泄漏有什么影响？国内SCC是否需要边境碳调节？

---

## 10. 关键参考文献

- EPA（2023年）。*社会碳成本技术support文件* — 当前联邦SCC估计
- Nordhaus, W.D.（2017年）。"DICE模型" — 诺贝尔奖获奖综合评估模型
- Stern, N.（2006年）。*气候变化经济学* — 斯恩回顾
- Acemoglu, D., et al.（2012年）。"环境与定向技术变革"。《美国经济评论》102(1)。
- Golosov, M., et al.（2014年）。"化石燃料最优税收的一般均衡"。《计量经济学》82(1)。
- van den Bremer, T. & van der Ploeg, F.（2019年）。"风险气候变化与最优碳价格"。《环境与资源经济学家杂志》6(6)。
- Carleton, T. & Greenstone, M.（2022年）。"更新联邦政府的气候核算"。《经济展望杂志》36(4)。

---

*Document created: 2026-05-07*
*Related: [[carbon-pricing-integration]], [[locational-marginal-pricing]], [[ferc-jurisdiction-carbon]], [[environmental-justice-energy]]*

---

# English Version

# The Social Cost of Carbon in Electricity Dispatch

> **English:** Social Cost of Carbon in Economic Dispatch
> **Prerequisites:** [[carbon-pricing-integration]], [[locational-marginal-pricing]], [[environmental-justice-energy]]

---

## 1. Overview: Why Incorporate SCC into Dispatch?

The **Social Cost of Carbon (SCC)** is an estimate of the economic damage caused by one additional ton of CO₂ emissions. Unlike a carbon tax or cap-and-trade allowance price, the SCC is a *regulatory accounting tool* — used to evaluate whether regulations, infrastructure investments, or market rules are socially beneficial when accounting for climate impacts.

**The gap it fills:** Private market actors (generators, utilities, consumers) make dispatch and investment decisions based on private costs — fuel, capital, O&M. They do not pay for the social cost of the CO₂ their decisions emit. Incorporating the SCC into dispatch algorithms corrects this externality at the market level.

**Key distinction:**
- **Carbon compliance cost** (CA cap-and-trade $35-45/ton, RGGI $22-30/ton): What generators actually pay
- **Social Cost of Carbon** ($51/ton central, 2023 EPA update): What society actually pays for each ton of emissions

The gap between compliance costs and SCC represents unpriced externality — market prices systematically undercount the true cost of fossil generation.

---

## 2. The Social Cost of Carbon: Methodology and Estimates

### 2.1 How the SCC Is Calculated

The SCC is derived from Integrated Assessment Models (IAMs) — frameworks that combine:
1. **Climate module:** Models CO₂ concentrations, radiative forcing, temperature response, sea level rise
2. **Economic module:** Models the relationship between temperature change and economic output (GDP growth, sector-specific damages)
3. **Discounting:** Values future damages in present terms

**The three key components of SCC calculation:**

**Climate damages D(T):**
IAMs estimate economic damages as a function of global mean temperature increase T(°C):
- D(T) = α × T² × World GDP
- The quadratic form reflects increasing marginal damages as temperature rises
- At 1°C: ~0.1-0.3% GDP loss
- At 3°C: ~2-5% GDP loss
- At 5°C: ~10-20% GDP loss

**Damage function estimates vary widely:**
- Nordhaus (DICE model): Moderate damages
- Stern (Stern Review): High damages (using lower discount rate)
- Hope (PAGE model): High damages with fat-tailed uncertainty

**Discount rate:**
The choice of discount rate is the most contested parameter in SCC estimation:
- Low discount rate (1-2%): Values future generations heavily; SCC higher
- High discount rate (3-5%): Values present consumption more; SCC lower
- EPA's 2023 update: Uses 2% discount rate for the central estimate

### 2.2 Current SCC Estimates

**EPA's 2023 Technical Support Document update:**

| Discount Rate | SCC Estimate (2020 $/ton CO₂) |
|---|---|
| 5% (high) | ~$14/ton |
| 3% (mid) | ~$28/ton |
| 2.5% (mid) | ~$38/ton |
| 2% (central) | ~$51/ton |
| 1.5% (low) | ~$76/ton |
| 1% (very low) | ~$120/ton |

**Key uncertainty:**
The 95th percentile SCC (high damage, low discount rate) is ~$200+/ton — more than 10× the central estimate. This tail risk is critical for regulatory analysis but creates enormous uncertainty for market design.

**SCC trajectory:**
- EPA's 2023 SCC ($51/ton at 2%) is higher than the 2021 estimate ($51/ton had been $40/ton in 2021) — not because of updated science but because of updated economic projections
- The SCC grows over time: 2030 SCC at 2% discount rate: ~$55-65/ton; 2050 SCC: ~$70-85/ton
- This growth reflects increasing damages from accumulated emissions and limited remaining abatement opportunities

### 2.3 The Intergenerational Discounting Problem

**Why the discount rate matters so much:**
The choice of discount rate reflects a fundamental ethical question: how much should present generations sacrifice for future generations?

**Pure rate of time preference (ρ):**
If ρ = 0, we value equally the welfare of people alive today and people alive in 100 years. If ρ = 3%, we effectively say $1 of welfare today is worth $95 of welfare in 100 years.

**The Stern Review vs. Nordhaus debate:**
- Stern (2006): ρ = 0.1-0.5%, SCC ~$200-300/ton — future climate damages are catastrophic
- Nordhaus (2008): ρ = 3%, SCC ~$20-40/ton — economic growth will make future generations richer and more able to adapt

**The Ramsey equation for SCC:**
The SCC = marginal damage from an extra ton of CO₂ = D'(T) + climate feedback × probability of catastrophe

---

## 3. How SCC Would Enter Economic Dispatch

### 3.1 The Dispatch Algorithm

Economic dispatch minimizes total cost of meeting load subject to transmission constraints:

```
Minimize: Σ [MC_g × Q_g]  (sum over all generators)

Subject to:
  Σ Q_g = Load + Losses
  Q_g ≤ Q_g^max for all g
  Transmission constraints satisfied
```

Where `MC_g` = Marginal Cost of generator g

**Incorporating SCC adds a carbon term to marginal cost:**

```
MC_g_with_SCC = MC_g + (emission_rate_g × SCC)
```

For a natural gas CCGT:
- MC_g (fuel + VOM): ~$20-35/MWh
- Emission rate: 0.053 t CO₂/MMBtu × 7,000 BTU/kWh = 0.371 t CO₂/MWh
- At SCC = $51/ton: SCC term = 0.371 × $51 = **$18.91/MWh**
- Total MC: ~$38-54/MWh

For a coal unit:
- MC_g: ~$25-40/MWh
- Emission rate: 0.093 t CO₂/MMBtu × 10,000 BTU/kWh = 0.93 t CO₂/MWh
- At SCC = $51/ton: SCC term = 0.93 × $51 = **$47.43/MWh**
- Total MC: ~$72-87/MWh

**Effect on dispatch:** The SCC raises coal's marginal cost by $25-35/MWh more than gas — enough to push coal out of the dispatch merit order in many hours where gas was already competitive.

### 3.2 Impact on Market Clearing Prices

**The SCC in LMP:**

Incorporating SCC into dispatch changes the market-clearing price in two ways:

1. **Direct effect:** Generators' marginal costs rise by their emission rate × SCC → all LMPs rise
2. **Dispatch effect:** Cleaner generators are dispatched first → the marginal unit in many hours shifts from coal to gas or renewables → LMP may actually fall in those hours

**Net effect by hour type:**

| Hour Type | Without SCC | With SCC ($51/ton) | Notes |
|---|---|---|---|
| Coal on margin | LMP = MC_coal | LMP = MC_coal + $47/MWh | Large increase |
| Gas on margin | LMP = MC_gas | LMP = MC_gas + $19/MWh | Moderate increase |
| Solar/wind on margin | LMP ≈ $0 | LMP ≈ $0 (no change) | Zero-marginal-cost renewables unaffected |
| Storage arbitrage | Low | Moderate increase | Storage charges cleaner, discharges cleaner |

**The counter-intuitive result:** SCC may *lower* average LMP in markets with high renewable penetration — because more solar/wind gets dispatched, reducing the hours when gas CCGT is marginal. But in coal-heavy markets (MISO, SPP), SCC raises prices substantially.

### 3.3 Dynamic Efficiency Effects

Beyond static dispatch, SCC incorporation creates dynamic investment incentives:

**Short-run (1-5 years):**
- Dispatch shifts toward gas and renewables immediately
- Coal plants that were marginal become sub-marginal
- Some coal retirement accelerated

**Medium-run (5-15 years):**
- New investment decisions favor gas CCGT and renewables over coal
- Storage becomes more attractive (charges from gas, discharges during peak)
- Demand response value increases (reducing the hours when fossil units run)

**Long-run (15-30 years):**
- Generation mix shifts materially toward zero-carbon resources
- The SCC's growth trajectory (rising SCC over time) creates increasing incentive for early retirement of fossil assets
- "Stranded asset" risk for new fossil investment increases dramatically

---

## 4. SCC vs. Existing Carbon Pricing Programs

### 4.1 The Gap Between SCC and Compliance Carbon Prices

The most striking fact about carbon pricing in US electricity markets: the compliance carbon prices are far below the SCC:

| Carbon Price Source | Price ($/ton CO₂) | vs. SCC ($51/ton) |
|---|---|---|
| CA cap-and-trade (2024-25) | $35-45 | ~70-90% of SCC |
| RGGI allowance (2024-25) | $22-30 | ~45-60% of SCC |
| EU ETS allowance (2024) | $60-80 | ~120-160% of SCC |
| SCC central estimate | $51 | 100% (by definition) |
| SCC 95th percentile | ~$200 | 400% of compliance prices |

**The implication:** Even the most aggressive US carbon pricing program (CA) prices carbon at only 70-90% of the social cost. RGGI is at only 45-60%. The gap means significant unpriced externality remains.

### 4.2 SCC as a Regulatory Tool vs. Market Price

**SCC as a regulatory accounting tool:**
Federal agencies use SCC to evaluate regulations under Executive Order 12866 (Regulatory Planning and Review). Any major federal regulation (clean air rules, fuel economy standards, electricity regulations) must quantify benefits using the SCC.

**Examples of SCC use:**
- EPA's Clean Power Plan (2015) used SCC to estimate climate benefits of CO₂ reductions
- CAFE fuel economy standards used SCC to justify stricter standards
- FERC infrastructure approval (gas pipelines, LNG terminals) uses SCC to evaluate upstream emissions

**SCC as a market design tool:**
Incorporating SCC directly into wholesale market dispatch algorithms is a different use:
- It would transform SCC from a regulatory accounting tool into an *operational market signal*
- Every generator's marginal cost would reflect SCC
- The market would automatically internalize the externality
- This is what economists generally prefer over command-and-control regulation

### 4.3 Why Not Just Use SCC Instead of Carbon Compliance Markets?

**Arguments for SCC-based dispatch over compliance markets:**
1. **Uniform price signal:** SCC would apply to all generators uniformly, eliminating competitive distortions between CA-cap-and-trade states and non-carbon-priced states
2. **Correct magnitude:** SCC reflects actual social cost; compliance markets may price too low (or too high)
3. **No leakage:** A federally-imposed SCC in RTO/ISO dispatch would eliminate the cross-state leakage problem

**Arguments against (the implementation case):**
1. **SCC uncertainty:** The range ($14-200+/ton) is enormous — the wrong SCC could cause either over- or under-investment
2. **Legal authority:** FERC lacks clear statutory authority to impose an SCC-based carbon charge without Congressional action (see [[ferc-jurisdiction-carbon]])
3. **Political acceptance:** SCC-based electricity prices would be politically contentious — "hidden carbon tax" framing
4. **Updates required:** SCC estimates are updated every few years; a market design based on SCC would need regular recalibration

---

## 5. General Equilibrium Effects of SCC-Based Dispatch

### 5.1 Electricity Sector vs. Economy-Wide Effects

SCC-based dispatch changes electricity sector behavior, but the general equilibrium effects matter:

**Direct effect:** CO₂ reductions from cleaner dispatch
- Estimated US electricity sector reduction from $51/ton SCC dispatch: 20-35% reduction in CO₂ within 10 years

**Indirect effects:**
1. **Rebound effect:** Lower electricity prices (from more renewables dispatch) → increased electricity consumption → partially offsets CO₂ reductions
2. **Fuel price effects:** Reduced gas/coal demand → lower fuel prices → increased gas consumption in other sectors
3. **Investment effect:** Lower electricity prices attract more electricity-intensive industry (data centers, EVs, reshoring manufacturing) → increased electricity demand
4. **Capital reallocation:** Reduced fossil generation investment → stranded assets → financial sector exposure

### 5.2 Macroeconomic Effects

**GDP impact:**
Most estimates find that carbon pricing at SCC levels has modest negative GDP effects (1-3% over 10 years) — but these estimates depend heavily on how revenue is recycled:
- Revenue-neutral recycling (per-capita dividends): Minimal GDP impact
- Revenue used for general government spending: Small negative GDP effect
- Revenue used for corporate tax cuts: Small positive GDP effect

**The Solow growth model perspective:**
Climate change itself is a drag on long-run economic growth. Pricing carbon at SCC levels reduces this drag — the net effect on long-run GDP is likely positive when climate damages are fully accounted for.

---

## 6. SCC in Capacity Adequacy

### 6.1 How SCC Affects Capacity Decisions

Capacity adequacy decisions (should we build a new gas peaker?) depend on expected future revenue streams. SCC changes these calculations:

**Without SCC:**
A gas peaker's revenue requirement = capital cost + fixed O&M + fuel cost
- If expected energy market revenue covers this → build it

**With SCC ($51/ton):**
The gas peaker generates 0.371 t CO₂/MWh when running
- SCC cost per MWh = 0.371 × $51 = $18.91/MWh
- This is effectively an additional "fuel cost" that must be recovered
- The peaker becomes less economical relative to a battery

**The "SCC-adjusted" peaker economics:**
A 100 MW gas peaker running 300 hours/year at $100/MWh energy + $19/MWh SCC = $119/MWh
- vs. a 4-hour battery charging at $20/MWh, discharging at $80/MWh (no SCC)
- Battery wins on total cost basis if it can capture sufficient price spread

### 6.2 SCC and Optimal Reserve Margin

The SCC changes the optimal reserve margin:

**The intuition:**
- More generation capacity → less generation scarcity → lower wholesale prices → lower SCC damage per unit of generation (because marginal units emit less)
- But more capacity also means more capital cost
- The optimal reserve margin balances capital cost against SCC-adjusted scarcity risk

**The complication:**
The SCC is a global aggregate damage measure. The marginal damage from an extra MWh of generation depends on where that generation occurs (grid conditions) and when (which determines the marginal unit displaced). A location/time-specific SCC would be more accurate than a uniform national SCC.

---

## 7. Interaction with Existing State Carbon Pricing

### 7.1 Double-Counting Problem

If a generator is already in CA cap-and-trade ($35-45/ton) and the SCC ($51/ton) is also added to dispatch, does this double-count the carbon cost?

**The resolution:**
These two costs are measuring different things:
- **CA cap-and-trade:** What generators *pay* for their CO₂ emissions (private cost)
- **SCC:** What society *pays* for the external damage from CO₂ (social cost)

The gap between $51 (SCC) and $40 (CA price) = $11/ton is the unpriced externality remaining even after CA cap-and-trade. The SCC additive captures this remaining gap.

**However:**
Generators paying CA cap-and-trade prices should not pay an additional SCC charge in wholesale markets — that would be double-counting. The correct implementation is:
- For CA generators: SCC adder - CA allowance price = additional adder
- For non-CA generators in non-carbon-priced states: Full SCC adder

### 7.2 Carbon Price Growth Trajectories

**SCC trajectory:**
The EPA's central SCC grows ~2%/year in real terms (reflecting growing climate damages)

**Compliance carbon price trajectory:**
- CA cap-and-trade: Cap declines ~3%/year → allowance prices expected to rise
- RGGI: Cap declines 2.5%/year through 2030 → prices expected to rise
- EU ETS: Trending toward higher prices as caps tighten

The gap between SCC and compliance prices may narrow over time as carbon markets tighten — or may widen if SCC updates reflect new damage science.

---

## 8. Quantitative Scenarios

### 8.1 Dispatch Simulation Results

**Scenario: $51/ton SCC applied to all US RTO/ISO dispatch (2024)**

**Estimated annual CO₂ reduction: 25-40% of electricity sector emissions**
- Basis: Electricity sector CO₂ ≈ 1,600 MMT/year in 2024
- Reduction estimate: 400-640 MMT/year

**Average wholesale electricity price impact:**
- National average LMP increase: +$5-15/MWh
- This translates to ~1-3 cents/kWh retail rate increase
- Depends on pass-through rate and local generation mix

**Welfare analysis:**
- Climate benefit: $51/ton × 400-640 MMT = $20-33 billion/year in climate damage avoided
- Consumer cost increase: ~$5-15/MWh × 4,000 TWh = $20-60 billion/year
- Net welfare: Depends on SCC accuracy; if SCC is correct, net welfare is positive

### 8.2 Regional Variation

| Region | CO₂ Intensity | SCC Impact ($/MWh) | Expected Price Increase |
|---|---|---|---|
| MISO (coal-heavy) | ~800 kg/MWh | ~$40/MWh | +$15-25/MWh |
| SPP (coal-heavy) | ~700 kg/MWh | ~$36/MWh | +$12-20/MWh |
| PJM (mixed) | ~450 kg/MWh | ~$23/MWh | +$8-15/MWh |
| ERCOT (gas-heavy) | ~400 kg/MWh | ~$20/MWh | +$7-12/MWh |
| CAISO (clean) | ~200 kg/MWh | ~$10/MWh | +$3-8/MWh |

*SC impact = regional CO₂ intensity × $51/ton; average price increase depends on share of hours where fossil is marginal*

---

## 9. Open Research Questions

1. **Location/time-specific SCC:** Should the SCC vary by location (reflecting regional climate vulnerability) and time (reflecting higher marginal damage during peak demand periods when more emissions occur)? Current uniform SCC may be inaccurate.
2. **SCC discount rate consensus:** Can economists reach consensus on the appropriate discount rate for climate policy? The 3-5× variation in SCC from discount rate choice is the single largest source of uncertainty.
3. **SCC credibility:** If SCC is incorporated into market dispatch, the estimate must be credible, transparent, and regularly updated. Who should be responsible for updating the SCC — EPA, FERC, an independent commission?
4. **Interaction with capacity markets:** Does SCC incorporation in energy markets change optimal capacity market design? Should capacity accreditation also reflect SCC-adjusted emissions?
5. **SCC under uncertainty:** Given the wide range of SCC estimates ($14-200+/ton), how should market design handle this uncertainty? Robust optimization approaches vs. point estimates.
6. **International carbon pricing coordination:** If the US incorporates SCC into dispatch, what are the implications for international competitiveness and carbon leakage? Does a domestic SCC require border carbon adjustments?

---

## 10. Key References

- EPA (2023). *Social Cost of Carbon Technical Support Document* — current federal SCC estimates
- Nordhaus, W.D. (2017). "DICE Model" — Nobel Prize-winning integrated assessment model
- Stern, N. (2006). *The Economics of Climate Change* — the Stern Review
- Acemoglu, D., et al. (2012). "The Environment and Directed Technical Change." *American Economic Review* 102(1).
- Golosov, M., et al. (2014). "Optimal Taxes on Fossil Fuel in General Equilibrium." *Econometrica* 82(1).
- van den Bremer, T. & van der Ploeg, F. (2019). "Risky Climate Change and Optimal Carbon Prices." *Journal of the Association of Environmental and Resource Economists* 6(6).
- Carleton, T. & Greenstone, M. (2022). "Updating the Federal Government's Climate Accounting." *Journal of Economic Perspectives* 36(4).

---

*Document created: 2026-05-07*
*Related: [[carbon-pricing-integration]], [[locational-marginal-pricing]], [[ferc-jurisdiction-carbon]], [[environmental-justice-energy]]*
