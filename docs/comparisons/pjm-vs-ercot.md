# PJM vs ERCOT: Comparative Market Design Analysis

> **English:** PJM vs ERCOT — Comparative Market Design and Economic Outcomes
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
| 2023 | $55-70 | $50-65 | ERCOT additions of solar/battery |
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
- Wind turbines (with de-icing) produced ~3-4% of capacity during peak cold
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
- New build: Modest new gas build 2015-2022; major renewable build (solar/ offshore wind); capacity market kept prices more stable

**Key investment difference:** PJM's capacity market attracted ~25 GW of demand-side resources and storage; ERCOT attracted solar/ storage purely on energy market + ITC economics.

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

In PJM, generators across 13 states may fail simultaneously during extreme weather, but geographic diversification reduces the probability that all fail at once.

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
