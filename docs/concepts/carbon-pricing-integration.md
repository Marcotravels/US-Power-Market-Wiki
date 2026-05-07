# Carbon Pricing Integration in US Wholesale Electricity Markets

> **English:** Carbon Pricing Integration in Wholesale Electricity Markets
> **Prerequisites:** [[locational-marginal-pricing]], [[ancillary-services-market]], [[electricity-markets-day-ahead-real-time]]

---

## 1. Overview: Why Carbon Pricing Matters for Electricity Markets

Carbon pricing represents the most economically efficient approach to internalizing CO₂ externalities in wholesale electricity markets. Unlike technology mandates or renewable portfolio standards—which prescribe *how* to reduce emissions—a carbon price lets the market discover the *lowest-cost* abatement pathway through the dispatch merit order.

The fundamental mechanism: a carbon price adds `C × emission_factor` (USD/MMBtu × tons CO₂/MMBtu) to every generator's marginal cost. This shifts the dispatch merit order, retires high-emitting units at the margin, and creates explicit incentives for gas-to-renewable fuel switching. The elegance is that every generator, every hour, responds to the same price signal without requiring case-by-case regulatory intervention.

### Two Structural Approaches

| | Cap-and-Trade (Market-Based) | Carbon Tax (Price-Based) |
|-|---|---|
| **Examples** | CA cap-and-trade, RGGI, Regional Clean Electricity甲 | None currently at US state level |
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

RGGI is the oldest mandatory CO₂ cap-and-trade program in the US — covering electricity sector emissions since 2009 across 11 Northeast/Mid-Atlantic states: CA, CT, DE, ME, MD, MA, NH, NJ, NY, RI, VT, VA.

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
|--------|-----------|------|-----------------|
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

*Document created: 2026-05-07*
*Related: [[ferc-jurisdiction-carbon]], [[social-cost-carbon-dispatch]], [[state-rps-effectiveness]]*
