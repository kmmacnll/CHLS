# P1 — Housing Economist: Hypothesis discovery (prefix ECON)

Method note: ~18 searches total. All figures come from search-result snippets, not full-text reads; "(sec.)" marks secondary summaries to verify against the primary source. Untagged-as-sec. items were seen in a snippet attributed to the primary. [unverified] = memory only or not confirmed. The Bank of Canada per-100bp magnitudes for rate pass-through could not be retrieved.

### ECON-1 — Population-growth shock (PR + NPR surge) outran supply
- Mechanism: Faster household formation from permanent and non-permanent residents than completions can absorb raises rents/prices, especially in rental segments NPRs use.
- Predicted effect: Rents/prices up; modest nationally, larger in big metros.
- Unit: CMA-year.
- Variables: PR/NPR inflows and stocks, rents, prices, vacancy, completions, enclave instruments.
- Datasets: StatCan demographic estimates, IRCC permit data, CMHC Rental Market Survey, Teranet, Census.
- Literature: IRCC municipal FE-IV panel: immigration explains about 11% of 2006–21 house price increases nationally, about 21% in large cities; 1% more new immigrants raises rents 0.086% (https://www.canada.ca/en/immigration-refugees-citizenship/corporate/reports-statistics/research/immigration-housing-prices-municipalities-canada.html). Province-level shift-share undergraduate paper (Gala, U. Alberta, 10 provinces 2005–21; headline elasticity not retrieved) (https://journals.library.ualberta.ca/esi/index.php/esi/article/download/1/1). Ontario shift-share 2007–23 (magnitude not retrieved). A summary reports literature spanning 0.1%–1.6% price rise per 1% immigration (sec.; https://fsc-ccf.ca/wp-content/uploads/2025/10/do-immigrants-cause-higher-housing-prices-myths-and-realities-about-immigrants-housing-and-the-labour-market.pdf). Cabral & Steingress (BoC SWP 2024-40, US counties, ancestry IV): about 2% of US shelter price growth from immigration, prices respond more than rents (https://bankofcanada.ca/wp-content/uploads/2024/10/swp2024-40.pdf). BoC SAN 2023-17: immigration adds more to demand than supply near term (qualitative) (https://www.bankofcanada.ca/wp-content/uploads/2023/12/san2023-17.pdf).
- Against: Estimates cover mostly PR inflows pre-2022; surge was NPR-dominated. Enclave instruments may violate exclusion. Range of estimates is wide (0.1–1.6).
- Identification: Shift-share by origin enclaves; event study of 2024 study-permit cap and NPR cuts by CMA student exposure.
- Difficulty: med. Novelty: low-med (NPR event study newer). Policy importance: high.
- Proposed class: C contested.

### ECON-2 — Low supply elasticity in major CMAs
- Mechanism: Inelastic new supply (land, approvals, costs, finance) makes demand shocks capitalize into prices.
- Predicted effect: Price response inversely related to elasticity; Toronto/Vancouver largest.
- Unit: census agglomeration/CMA-quarter.
- Variables: Starts, prices, permits, land constraints, demand shocks.
- Datasets: CMHC starts, StatCan permits, Teranet.
- Literature: Paixão, BoC SAN 2021-21 uses sensitivity of local prices to regional cycles (Guren et al. method) rather than Saiz geography (https://www.bankofcanada.ca/wp-content/uploads/2021/09/san2021-21.pdf). A secondary write-up reports Vancouver 0.63, Toronto 0.89, Winnipeg 4.34 (sec.; https://morehousing.substack.com/p/supply-elasticity); a Calgary policy paper says supply response is low in Vancouver, Toronto, Calgary and large in St. John's, Winnipeg, Guelph (https://journalhosting.ucalgary.ca/index.php/sppp/article/download/79355/57603/254509). Rao & Wang (BoC SAP 2026-2): rate-driven price falls are largest in inelastic cities, a validation of the proxy (https://www.bankofcanada.ca/2026/02/staff-analytical-paper-2026-2/). A Better Dwelling piece titled "BoC researchers say supply alone can't explain home prices" exists (sec.; not read).
- Against: Proxy assumes cross-city price-cycle differences reflect only supply elasticity (the note's own caveat); confounds with demand heterogeneity. Starts rose in 2021–23 without price relief.
- Identification: Quantity vs price response to exogenous demand shocks by CMA; geography IV; compare proxy with Saiz-type measures.
- Difficulty: med. Novelty: low-med. Policy importance: high.
- Proposed class: B partially understood.

### ECON-3 — Interest-rate / credit channel
- Mechanism: Lower mortgage rates capitalize into prices (2020–21); tightening cuts owner demand but raises rents via landlord user cost or rental demand shift.
- Predicted effect: Prices down, rent inflation up after tightening (Rao & Wang); magnitude per 100bp not retrieved.
- Unit: CMA-month; national SVAR.
- Variables: Mortgage rates, policy shocks, prices, CPI-rent, tenure transitions.
- Datasets: BoC, Teranet, StatCan CPI, CMHC, OSFI.
- Literature: Rao & Wang SVAR with monetary-policy shocks (Sekkel, Zhang & Stern 2025) as external instrument; rent rises more where fewer renters become owners (https://ideas.repec.org/p/bca/bocsap/26-2.html). Surprenant BoC SAP 2026-52: demand responds faster than supply, so policy moves prices but little the stock (https://www.bankofcanada.ca/wp-content/uploads/2026/10/sap2026-52.pdf; summary only).
- Against: Cannot explain the multi-decade price/income divergence alone; heterogeneity by elasticity; rent result contradicts "falling rates lower rents" intuition.
- Identification: High-frequency policy surprises; stress-test (2018) DiD across borrower groups.
- Difficulty: med. Novelty: low (rent channel med). Policy importance: high.
- Proposed class: B partially understood.

### ECON-4 — Suppressed household formation
- Mechanism: High rents force doubling-up; observed headship understates need.
- Predicted effect: Missing households concentrated in high-rent CMAs.
- Unit: CMA-census year, age group.
- Variables: Headship by age, rent, income, composition.
- Datasets: Census, LFS, CMHC.
- Literature: PBO: 631,000 suppressed households in 2021 (2024 report); the Aug 2025 PBO report (RP-2526-007-S) splits the 2035 gap of 690,000 (baseline, net of surplus) into excess demographic demand −272,000, suppressed formation 714,000, return to average vacancy 248,000, and states about 3.2M net new units needed by 2035 vs about 2.5M baseline completions (https://www.pbo-dpb.ca/en/publications/RP-2526-007-S--household-formation-housing-stock-estimating-housing-gap-in-2035--formation-menages-stock-logements-estimation-ecart-offre-logements-2035). Lauster/von Bergmann: Toronto shortfall 250,000–400,000 dwellings depending on assumptions (https://doodles.mountainmath.ca/posts/2022-05-06-estimating-suppressed-household-formation/). StatCan: 16.3% of 25–39s lived with parents in 2021; Toronto 25–29s 21.8% (1991) to 48.6% (2021) (sec.).
- Against: TMU analysis finds the young-adult-at-home share fell 2003–2023 on survey data and household size did not fall as expected (https://www.torontomu.ca/centre-urban-research-land-development/blog/blogentry103-when-household-size-doesnt-fall-torontos-housing-supply-shortfall-explained/). Counterfactual headship benchmark is assumption-driven; PBO notes its estimate is not tied to an affordability target (sec.).
- Identification: Cross-CMA headship-on-rent panel with supply-shifter IV.
- Difficulty: med-high. Novelty: med. Policy importance: high.
- Proposed class: C contested.

### ECON-5 — "Housing need" gap estimates are benchmark- and scenario-dependent
- Mechanism: Gap = need under a chosen affordability/vacancy benchmark minus projected stock; headline moves with benchmark and migration paths.
- Predicted effect: Measurement hypothesis; plausible gap range is wide.
- Unit: Province/CMA projection.
- Variables: Stock, household projections, benchmark ratio, migration.
- Datasets: CMHC, PBO, StatCan projections.
- Literature: CMHC 2022/2023: 3.5M additional units by 2030 (18.2M total; ~60% ON+BC; 3.1M under weaker growth/immigration end, 4.0M if immigration continues) (https://www.cmhc-schl.gc.ca/professionals/housing-markets-data-and-research/housing-research/research-reports/accelerate-supply/housing-shortages-canada-updating-how-much-we-need-by-2030). CMHC June 2025: up to 4.8M homes, 430,000–480,000/yr by 2035 to restore 2019 affordability (https://www.cbc.ca/lite/story/1.7565525). PBO: 3.2M by 2035; 2030 gap 658,000 under 2025–27 levels plan (Nov 2024 note) (sec.).
- Against: CMHC target year 2019 is arbitrary; PBO and CMHC differ by roughly 1.6M units for 2035 in definition (sec.; not reconciled here).
- Identification: Replicate and run sensitivity; compare with elasticity-implied price approach.
- Difficulty: low-med. Novelty: med. Policy importance: high.
- Proposed class: C contested.

### ECON-6 — 2025 rental softening: NPR outflow plus record completions
- Mechanism: Reduced NPR intake and record purpose-built completions raised vacancy and slowed rents.
- Predicted effect: Vacancy up, asking rents down in student-heavy CMAs.
- Unit: CMA-year.
- Variables: NPR change, completions, vacancy, asking vs in-place rents.
- Datasets: CMHC RMS, StatCan NPR, Rentals.ca.
- Literature: CMHC 2025 report (secondary coverage): national purpose-built vacancy 3.1% (2.2% in 2024); Metro Vancouver 3.7%, highest since 1988, rent growth 20-year low; Toronto 3%; Montreal vacancy up but rents still rose (https://www.bnnbloomberg.ca/business/2025/12/11/rent-growth-slowed-in-2025-as-national-vacancy-rate-continued-to-rise-cmhc/).
- Against: Supply and demand not separated; in-place rents lag; Montreal anomaly.
- Identification: Event study with CMA student exposure, control for completions pipeline.
- Difficulty: med. Novelty: high. Policy importance: high.
- Proposed class: D under-researched.

### ECON-7 — Rent regulation and tenure lock-in
- Mechanism: Vacancy decontrol gaps between in-place and market rents reduce mobility; exemptions for new units shape supply.
- Predicted effect: Wider asking vs in-place gap; effect on new rental supply ambiguous.
- Unit: Province/CMA-year.
- Variables: Rents by tenure length, moves, regime dates.
- Datasets: CMHC RMS, Census.
- Literature: Ontario exempted units first occupied after Nov 15, 2018; no rigorous post-2018 causal study found. A 2020 CMHC analysis reportedly found no significant difference in rental starts between rent-control and no-control cities (sec., via opinion piece; primary not read). Urbanation attributes some Toronto supply rise to the change but cites other factors (sec.; https://mises.org/wire/toronto-drops-rent-control-so-builders-build-more-housing). Earlier critics: the 1991 exemption mainly expanded condos (sec.). Diamond et al. (2019) SF rent control: reduced rental supply [unverified].
- Against: Exemption coincided with development-charge deferrals and CMHC financing.
- Identification: DiD around 2018 exemption vs other provinces; timing of rental starts.
- Difficulty: med-high. Novelty: med. Policy importance: med-high.
- Proposed class: D under-researched.

### ECON-8 — Investor and non-resident demand
- Mechanism: Investor purchases and non-resident buyers lift owner-occupier prices; investors also add rental stock.
- Predicted effect: Small national price effect; larger locally.
- Unit: Postal area/CMA-month.
- Variables: Investor/non-resident shares, prices.
- Datasets: StatCan Canadian Housing Statistics Program, BC PTT.
- Literature: CHSP: investors owned over a fifth of houses in BC, NB, NS and ON in 2020 (BC 23.3%) (https://www150.statcan.gc.ca/n1/pub/46-28-0001/2023001/article/00001-eng.htm). Non-resident investors 5.6% of owners in NS, 5.5% NB; earlier release: non-residents owned 3.4% of properties in Toronto, 4.8% in Vancouver, year not confirmed (https://www.bnnbloomberg.ca/foreign-ownership-below-5-in-toronto-vancouver-1.947934.amp.html). Price-effect estimates of BC foreign-buyer tax not retrieved.
- Against: Small shares; investor-owned units often rented.
- Identification: DiD around 2016 BC tax, 2023 federal ban.
- Difficulty: med. Novelty: low-med. Policy importance: med.
- Proposed class: B partially understood.

### ECON-9 — Interprovincial migration and affordability arbitrage
- Mechanism: High prices in ON/BC push migrants to AB and Atlantic, raising prices there.
- Predicted effect: Net outflows track price/income gaps; destination price acceleration.
- Unit: Province/CMA-quarter, origin-destination.
- Variables: Flows, price/income gaps, jobs.
- Datasets: StatCan quarterly demography, taxfiler migration, Teranet.
- Literature: Descriptive only: Ontario record net outflows 2021–22; Alberta net gain ~53,000 (BMO) / 45,194 in first three quarters of 2023; ATB (Mar 2026) projects inflow moderating to about 20,000/yr as the price gap narrows (https://www.atb.com/company/insights/the-twenty-four/migration-puzzle-march-24-2026/). Price-to-income ~10 in Atlantic/AB vs more than double in ON/BC (Desjardins 2022, via Global News, sec.). No causal study found.
- Against: Jobs, remote work, taxes confound.
- Identification: Gravity model with price-gap IV; synthetic control around remote-work shock.
- Difficulty: med. Novelty: med-high. Policy importance: med.
- Proposed class: D under-researched.

### ECON-10 — Land value drives long-run price/income divergence
- Mechanism: Price growth reflects land rents (binding land/zoning constraints or demand capitalization), not structure costs.
- Predicted effect: Land share rising with metro size; land responds more to rates/income.
- Unit: CMA-year/property.
- Variables: Observed land prices, structure cost, income, rates.
- Datasets: StatCan NHPI land/structure, assessment data.
- Literature: Stewart (2022, Canadian Journal of Economics, observed land prices): land is dominant driver of price growth in some Canadian cities but not others (sec.; https://www.progress.org/wiki/stewart-canadian-land-house-prices/). Dachis (C.D. Howe) price-cost gap 2011–21: Vancouver detached about $1.3M above build cost, Toronto $350,000 (32%) using assumed 25% land share (sec.; same host). Diewert, Huang & Burnett-Isaacs note land-value data are almost completely lacking (Richmond BC case).
- Against: Land/structure splits mostly imputed; new-build vs resale differ; no BoC/CMHC decomposition found.
- Identification: Compare land vs structure responses to rate/immigration shocks; discriminates land-constraint from cost explanations.
- Difficulty: med-high. Novelty: med. Policy importance: high.
- Proposed class: C contested.

---

## Discriminating tests (ECON-1/2/3)
- Demand shock: price/rent response proportional to population exposure and reversing when NPRs leave; quantity response small. 2025 softening fits but is confounded with completions.
- Supply inelasticity: identical shock yields larger price, smaller quantity response in low-elasticity CMAs (Rao & Wang heterogeneity fits).
- Credit/rate: price changes follow policy shocks, strongest in ownership; rents move opposite. Interact with elasticity.
- Cross-cut: land-vs-structure decomposition and starts response by CMA.

## Summary
- Claims (each with confidence):
  - Tighter mortgage policy lowers prices and raises rent inflation, with larger price falls in inelastic cities (med; one BoC paper).
  - Immigration's causal contribution to Canadian prices is modest nationally, larger in big cities (IRCC ~11%/~21%) (low-med).
  - Suppressed household formation exists but size is method-dependent (PBO 631k in 2021, 714k in 2035 baseline; Toronto 250–400k) (med).
  - Housing-gap headlines (CMHC 3.5M/2030, 4.8M/2035; PBO 3.2M/2035) are benchmark-dependent (high).
  - Vancouver and Toronto have low supply elasticity by the Paixão proxy (0.63, 0.89 via secondary) (low-med).
- Supporting evidence: sources cited inline.
- Sources: inline URLs; all via search snippets only.
- Uncertainty: Rate pass-through magnitudes, Paixão full table, Gala/Ontario shift-share magnitudes, BC foreign-buyer tax effects, Canada-specific rent-control causal evidence not retrieved. Land-share evidence is secondary.
- Assumptions: Snippet attributions to primary documents are accurate.
- Contradictions found: (1) PBO/CMHC need vs TMU finding that co-residence fell 2003–2023; (2) Paixão proxy vs Saiz geography; (3) Montreal rents rose despite higher vacancy; (4) immigration elasticities range 0.1–1.6 across studies; (5) CMHC (4.8M by 2035) vs PBO (3.2M by 2035) gaps.
- Recommended next investigations: Pull Paixão city table and IRCC/Ontario specs; read Rao & Wang impulse responses; reconcile CMHC vs PBO gap models; NPR-policy event study; Ontario 2018 rent-control DiD; land-vs-structure decomposition (Stewart replication); verify all (sec.) and [unverified] items.
