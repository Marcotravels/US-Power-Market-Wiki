# Capacity Market Design and Resource Adequacy in Energy Transition

> **English:** Capacity Market Design and Resource Adequacy
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

**High Conditional Sparsity Price (HCSP):** For when dispatchable thermal capacity is scarce relative to renewables:

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

**Option  capacity (Reliability Option):**
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

*Document created: 2026-05-07*
*Related: [[ercot-rtc-b-market]], [[pjm-vs-ercot]], [[storage-economics]], [[demand-response-economics]]*
