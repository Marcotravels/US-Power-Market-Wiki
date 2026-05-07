# Demand Response Economics and Grid Flexibility Markets

> **English:** Demand Response Economics and Grid Flexibility
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
- PJM: Demand Resources can provide Tier 1 ( synchronized reserves) and Tier 2 (non-synchronized reserves)

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

*Document created: 2026-05-07*
*Related: [[storage-economics]], [[capacity-market-design]], [[locational-marginal-pricing]], [[environmental-justice-energy]]*
