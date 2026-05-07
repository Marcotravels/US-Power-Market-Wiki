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
