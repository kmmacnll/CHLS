# P1 — Housing Economist: Hypothesis discovery (prefix ECON)

Research-log note: the search tool hit a usage limit after 7 of ~15 planned searches. Items marked [unverified] come from memory or secondary summaries and were not confirmed against primary sources. Several key estimates (city-level elasticities, Canadian rate pass-through magnitudes, PBO report details) could not be retrieved and are flagged as gaps.

## Sources actually confirmed this session (via search result snippets)
- Paixão (2021), BoC SAN 2021-21, Canadian housing supply elasticities. https://www.bankofcanada.ca/wp-content/uploads/2021/09/san2021-21.pdf (method confirmed: Guren et al. 2021 proxy from price sensitivity to regional cycles, extending Giannone et al. 2020; city values NOT retrieved).
- Rao & Wang (2026), BoC Staff Analytical Paper 2026-2, "Channels of Transmission: How Mortgage Rates Affect House Prices and Rents in Canada". https://www.bankofcanada.ca/2026/02/staff-analytical-paper-2026-2/
- Surprenant (2026), BoC SAP 2026-52 (demand responds faster than supply to monetary policy). https://www.bankofcanada.ca/wp-content/uploads/2026/10/sap2026-52.pdf (only the summary seen).
- Luu et al. (2023), BoC SAN 2023-17, how newcomers affect the economy (qualitative). https://www.bankofcanada.ca/wp-content/uploads/2023/12/san2023-17.pdf
- Cabral & Steingress (2024), BoC SWP 2024-40, immigration and US shelter prices. https://econpapers.repec.org/RePEc:bca:bocawp:24-40
- IRCC, Immigration and housing prices across municipalities in Canada. https://www.canada.ca/en/immigration-refugees-citizenship/corporate/reports-statistics/research/immigration-housing-prices-municipalities-canada.html
- CMHC, Housing shortages in Canada: updating how much we need by 2030. https://www.cmhc-schl.gc.ca/professionals/housing-markets-data-and-research/housing-research/research-reports/accelerate-supply/housing-shortages-canada-updating-how-much-we-need-by-2030 ; 2025 update coverage: https://www.cbc.ca/lite/story/1.7565525
- CMHC 2025 Rental Market Report coverage: https://www.bnnbloomberg.ca/business/2025/12/11/rent-growth-slowed-in-2025-as-national-vacancy-rate-continued-to-rise-cmhc/
- Desjardins (Feb 2026) citing PBO suppressed households. https://www.desjardins.com/content/dam/pdf/en/personal/savings-investment/economic-studies/housing-market-households-february-26-2026.pdf
- Lauster / von Bergmann (MountainMath). https://doodles.mountainmath.ca/posts/2022-05-06-estimating-suppressed-household-formation/ ; counter-view: https://www.torontomu.ca/centre-urban-research-land-development/blog/blogentry103-when-household-size-doesnt-fall-torontos-housing-supply-shortfall-explained/

---

### ECON-1 — Population-growth shock outran supply (2022–24 immigration surge)
- Mechanism: Rapid growth in permanent plus non-permanent residents raised household formation faster than completions can adjust, pushing rents and prices up, especially in rental segments where NPRs concentrate.
- Predicted effect: Positive on rents/prices. Rough magnitude from literature: modest nationally, larger in big cities (see below).
- Unit of analysis: CMA-year (or municipality-census period).
- Required variables: PR and NPR inflows by CMA, rents (CMHC, asking), prices, completions, vacancy, instruments (historical enclave shares).
- Potential datasets: StatCan quarterly demographic estimates, IRCC admissions/permit stock, CMHC Rental Market Survey, CREA/Teranet, Census.
- Existing literature: IRCC study (FE-IV on municipal census panel): immigration accounted for about 11% of national house price increase 2006–21, about 21% in large cities; rent elasticity to new immigrants 0.086 (source above; secondary snippet, verify specification). Shift-share Canadian papers exist (U. Alberta ESI provincial panel 2005–21; Ontario 2007–23) [magnitudes not retrieved]. US analogue: Saiz (2007/2010), roughly 1% rent/price rise per 1%-of-population inflow [unverified, from search summary]. Cabral & Steingress: ~2% of US shelter price growth attributable to immigration; prices respond more than rents. BoC SAN 2023-17 argues immigration adds more to demand than supply near-term (qualitative). CMHC scenarios: gap 2030 falls to 3.1M with immigration cut, rises to 4.0M if current pace persists.
- Evidence against: Historical shift-share estimates are for 2006–21 (mostly PR inflows); the 2022–24 surge was NPR-dominated and short-stay, so extrapolation is unsafe. Falling NPR numbers coincided with 2025 vacancy rise (3.1% from 2.2%) and slowing rents, which supports demand sensitivity but is confounded with record rental completions (CMHC). Enclave-based instruments may violate exclusion (enclaves correlate with city growth).
- Likely identification strategy: Shift-share on origin-country enclaves; policy discontinuities (2024 study-permit cap, 2024–25 NPR intake cuts) as event study using CMA exposure to international-student share.
- Expected difficulty: med (data available; NPR stock timing and exclusion restriction hard).
- Novelty: low-med (permanent-resident results exist; NPR-policy event study is newer).
- Policy importance: high.
- Proposed class: C contested.

### ECON-2 — Low long-run supply elasticity in Canada's large CMAs
- Mechanism: Price-inelastic new supply (land, approvals, costs, financing) means demand shocks capitalize into prices rather than quantities.
- Predicted effect: Price response to demand shocks inversely proportional to elasticity; larger in Toronto/Vancouver than Prairie cities.
- Unit of analysis: CMA/census agglomeration-quarter.
- Required variables: Starts/completions, prices, permits, land availability, regulatory indices, shock proxies.
- Potential datasets: CMHC starts, StatCan permits and building-permit values, Teranet, municipal approvals data.
- Existing literature: Paixão (BoC SAN 2021-21) estimates elasticities by census agglomeration using regional-cycle sensitivity (Guren et al. 2021 method); numeric results not retrieved here [gap]. Giannone et al. (2020) [unverified details]. Rao & Wang (2026) find price falls from mortgage-rate rises are largest where supply is inelastic, validating the elasticity proxy as predictive.
- Evidence against: Proxy assumes price-cycle sensitivity reflects only supply elasticity, which the note itself flags as strong; it confounds with demand-side heterogeneity (investor share, income). Saiz-type geographic measures give different rankings [unverified for Canada]. Starts rose strongly in 2021–23 in some metros without price relief.
- Likely identification strategy: Compare quantity vs price response to exogenous demand shocks (rates, immigration) by CMA; instrument with geography/land-constraint measures; validate Guren proxy against Saiz-type measures.
- Expected difficulty: med.
- Novelty: low-med (estimates exist; reconciling methods is open).
- Policy importance: high.
- Proposed class: B partially understood.

### ECON-3 — Interest-rate and credit channel (cheap credit capitalization, then rate shock)
- Mechanism: Lower mortgage rates raise buyers' budget and capitalized values (2020–21 boom); rate hikes reverse ownership demand but push demand into rentals and raise landlord user costs.
- Predicted effect: Prices fall, rents rise after tightening (Rao & Wang); magnitude per 100 bp not retrieved [gap].
- Unit of analysis: CMA-month.
- Required variables: Mortgage rates (posted/contract), monetary shocks, prices, rents, tenure transitions, mortgage-stress-test status.
- Potential datasets: BoC, Teranet, CMHC, Equifax/Bank of Canada credit data, OSFI.
- Existing literature: Rao & Wang (2026): monetary-policy-shock IV for mortgage rates; tighter policy lowers prices, raises rent inflation; rent rises more where fewer renters become owners (paper reports mechanism: higher landlord user cost or relative rental demand). Surprenant (2026): demand responds faster than supply so policy moves prices but little the stock.
- Evidence against: Prices rose in 2024–25 in some markets despite high rates (not confirmed); rate shocks hit prices unevenly (elasticity). Rate channel alone cannot explain multi-decade price/income divergence since the 1990s.
- Likely identification strategy: High-frequency monetary-policy surprises (Rao & Wang approach); regulatory discontinuities (stress test 2018, insured-mortgage rules) via difference-in-differences across borrower segments.
- Expected difficulty: med.
- Novelty: low (central bank topic) except rent-side channel: med.
- Policy importance: high.
- Proposed class: B partially understood.

### ECON-4 — Suppressed household formation / demand shortfall relative to need
- Mechanism: High rents/prices relative to income cause young adults to double up; measured demand understates need, so completions needed exceed trend.
- Predicted effect: Missing households concentrated in high-rent CMAs; fall in rent should release formation.
- Unit of analysis: CMA-census year, age cohort.
- Required variables: Headship rates by age, rents, incomes, household composition.
- Potential datasets: Census 1991–2021 PUMF/custom, LFS, CIS, CMHC.
- Existing literature: PBO about 631,000 suppressed households nationally (as cited by Desjardins, Feb 2026; primary PBO report not retrieved). Lauster/von Bergmann: Toronto shortfall 250,000–400,000 dwellings, depending on assumptions; UBC summary reports each $1,000 rise in median rent cuts young-adult own-household share by 23% (secondary, [unverified]). StatCan: 16.3% of 25–39s lived with parents in 2021; Toronto share of 25–29s with parents 21.8% (1991) to 48.6% (2021).
- Evidence against: TMU analysis finds share of young adults at home fell 2003–2023 on survey data, and household size did not fall as expected; counterfactual headship benchmarks are assumption-heavy; cultural/immigrant composition effects confound. Estimates range by factor of >1.5 across methods.
- Likely identification strategy: Cross-CMA panel of headship on rent with supply-shifter IV; quasi-experiments (rent control changes, new supply shocks).
- Expected difficulty: med-high (counterfactual).
- Novelty: med.
- Policy importance: high (determines the housing "target").
- Proposed class: C contested.

### ECON-5 — Housing-shortage estimates are model-dependent (CMHC gap is sensitive to affordability benchmark)
- Mechanism: "Need" computed relative to a past price/income or vacancy benchmark; the headline gap differs under alternative targets and migration assumptions.
- Predicted effect: Not a causal effect; a measurement hypothesis: range of plausible gap is wide, and completions required differ by multiples.
- Unit of analysis: Province/CMA-year projection.
- Required variables: Stock, projected households, benchmark affordability ratio, migration paths.
- Potential datasets: CMHC, StatCan projections, Census, PBO.
- Existing literature: CMHC 2022/2023: 3.5M additional units by 2030 (18.2M total; ~60% in ON and BC; 3.1M–4.0M under alternative immigration scenarios). CMHC June 2025 update: up to 4.8M new homes (430,000–480,000/year) by 2035 to restore 2019 affordability. PBO has produced alternative figures [unverified].
- Evidence against / contradictions: A secondary source cited ~245,000 starts/year by 2035 (projected supply) versus 430–480k needed, i.e. supply-gap not equal to need; some secondary pages report other totals; benchmark year (2019) arbitrary.
- Likely identification strategy: Reconstruct the models and run scenario/sensitivity analysis; compare with elasticity-based price-equilibrium approach.
- Expected difficulty: low-med.
- Novelty: med.
- Policy importance: high (drives targets).
- Proposed class: C contested.

### ECON-6 — Rental market: supply wave plus NPR outflow explains 2025 softening (and shows demand sensitivity)
- Mechanism: Record purpose-built completions (financing incentives) coincided with reduced NPR intake, raising vacancy and slowing rents; implies rents respond to marginal population change quickly.
- Predicted effect: Vacancy up, asking rents down in student-heavy CMAs.
- Unit of analysis: CMA-year / neighbourhood.
- Required variables: NPR stock change by CMA, purpose-built completions, vacancy, asking vs in-place rents.
- Potential datasets: CMHC RMS, StatCan NPR estimates, Rentals.ca, Zumper [unverified].
- Existing literature: CMHC 2025 Rental Market Report (secondary coverage): national purpose-built vacancy 3.1% (2.2% in 2024); Metro Vancouver vacancy 3.7%, highest since 1988, rent growth at 20-year low; Toronto purpose-built vacancy 3%; Montreal vacancy rose but rents kept rising (reported 7.2%, unverified); asking rents falling while in-place rents still rising.
- Evidence against: Supply and demand effects not separated; in-place rent growth is lagged by rent control and turnover; Montreal contradicts a simple story.
- Likely identification strategy: Event study using CMA exposure to NPR policy shock, controlling for scheduled completions pipeline; separate in-place vs asking rent.
- Expected difficulty: med.
- Novelty: high (very recent).
- Policy importance: high.
- Proposed class: D under-researched.

### ECON-7 — Rent-regulation and tenure-structure lock-in (in-place vs market rent gap)
- Mechanism: Vacancy-decontrol-less provincial regimes (e.g. Ontario pre-2018 units, BC, Quebec) and large gaps between sitting-tenant and market rents reduce mobility, so market-rent renters bear the adjustment; affordability for new households worsens even if average rent growth is moderate.
- Predicted effect: Positive spread in asking vs in-place rents; fewer moves.
- Unit of analysis: Province/CMA-year; household.
- Required variables: Rent by tenure duration, move rates, regulation regime dates.
- Potential datasets: CMHC RMS (turnover/same-sample), Census, SHS/CIS.
- Existing literature: No Canadian estimate retrieved this session [gap]. CMHC Rental Market Report distinguishes same-sample and turnover rent growth [unverified]. International: Diamond, McQuade & Qian (2019) San Francisco rent control reduced rental supply ~15% [unverified, from memory].
- Evidence against: Rent control effects depend on exemptions (new builds); Canada-specific evidence thin.
- Likely identification strategy: DiD around Ontario 2018 new-unit exemption removal / 1991 exemption; border comparisons across provinces.
- Expected difficulty: med-high.
- Novelty: med.
- Policy importance: med-high.
- Proposed class: D under-researched.

### ECON-8 — Investor and non-resident demand (financialization of ownership)
- Mechanism: Investor-purchased condos and non-resident buyers raise owner-occupier prices and shift stock to rental; policy taxes (BC foreign buyers tax 2016, federal foreign buyer ban 2023) test this.
- Predicted effect: Price level effect small nationally; larger locally pre-tax.
- Unit of analysis: Postal-code/CMA-month.
- Required variables: Investor shares, non-resident ownership, prices.
- Potential datasets: StatCan Canadian Housing Statistics Program, BC Property Transfer Tax data, Teranet.
- Existing literature: Not retrieved this session [gap]. Memory-only: BC foreign buyers tax studies (Gorback & Keys on foreign buyers (US/Canada?), Bank of Canada commentary) [unverified]. Federal ban evaluations [unverified].
- Evidence against: Non-resident share small (a few percent in major metros) [unverified]; investor purchases also supply rental stock.
- Likely identification strategy: DiD around policy dates by geography.
- Expected difficulty: med.
- Novelty: low-med.
- Policy importance: med.
- Proposed class: B partially understood.

### ECON-9 — Interprovincial migration and regional price spillovers (ripple/arbitrage)
- Mechanism: High Toronto/Vancouver prices push households and capital to Alberta, Atlantic, Quebec, raising prices there; migration tracks price/income gaps.
- Predicted effect: Net outflow from high-price CMAs; price convergence; Alberta/Atlantic price acceleration.
- Unit of analysis: CMA-year, origin-destination.
- Required variables: Migration flows, price/rent differentials, wages.
- Potential datasets: StatCan taxfiler migration, Teranet, quarterly demography.
- Existing literature: Not retrieved this session [gap]. Memory-only: Atlantic and Alberta price surges 2021–24 correlated with inflows [unverified].
- Evidence against: Wage/job shifts (energy) and remote work confound; price convergence might reflect rate/credit rather than migration.
- Likely identification strategy: Gravity migration model with price gap IV; synthetic control around remote-work shock.
- Expected difficulty: med.
- Novelty: med-high.
- Policy importance: med.
- Proposed class: D under-researched.

### ECON-10 — Long-run price/income divergence driven by land-value capitalization (not structure cost)
- Mechanism: Price growth since the 1990s is predominantly land value in large metros, with structure cost growth modest; implies binding land/zoning constraint or demand-driven rent on land, distinguishing supply-side from demand/credit stories.
- Predicted effect: Land share of value rising with metro size/growth; land price elasticity to income/credit higher than structure.
- Unit of analysis: CMA-year; property.
- Required variables: Land vs structure value decomposition, income, rates.
- Potential datasets: StatCan Residential Property Values/Assessment microdata, BC Assessment, MPAC [unverified], Teranet.
- Existing literature: Not retrieved [gap]. Memory-only: Knoll, Schularick & Steger (2017) international land-price decomposition [unverified]; Canadian estimates by BoC and others [unverified].
- Evidence against: Land/structure split is imputed and noisy; condo land share ambiguous.
- Likely identification strategy: Compare land vs structure price response to rate/immigration shocks; discriminates supply-inelasticity (land-binding) from construction-cost explanations.
- Expected difficulty: med-high.
- Novelty: med.
- Policy importance: high.
- Proposed class: D under-researched.

---

## Discriminating tests between the competing core hypotheses (ECON-1/2/3)
- Demand shock (ECON-1): rents/prices rise in proportion to population exposure, quantity response small and slow; reverses when NPRs leave (2025 observed softening is consistent but confounded).
- Supply inelasticity (ECON-2): same demand shock gives larger price rise and smaller quantity response in low-elasticity CMAs; Rao & Wang's heterogeneity result is consistent with this.
- Credit/rate (ECON-3): price changes track mortgage-rate shocks and are strongest in ownership; rent goes the opposite direction after tightening. Test via high-frequency shocks, with elasticity interaction.
- Cross-cutting discriminator: land vs structure price decomposition (ECON-10) and starts response by CMA.

## Summary
- Claims (each with confidence: high/med/low):
  - Mortgage-rate tightening lowers prices and raises rent inflation in Canada, with larger price falls in inelastic-supply cities (med; one BoC paper, summary seen only).
  - Immigration's causal contribution to Canadian prices is modest nationally and larger in big cities (IRCC: ~11%/~21% of 2006–21 price increase) (low-med; secondary snippet).
  - Suppressed household formation exists but its size is method-dependent (PBO ~631k; Toronto 250–400k; contrary evidence) (med).
  - CMHC need estimates (3.5M by 2030; up to 4.8M by 2035) are scenario/benchmark-dependent (high that they are so).
  - 2025 rental softening coincided with NPR outflow and record completions (med).
- Supporting evidence: see sources listed at top.
- Sources: as listed at top; all via search snippets only, no primary full-text read.
- Uncertainty: City elasticity values, Canadian rate pass-through magnitudes (bp to % price), rent-control, investor and land-share estimates were not retrieved. Search budget cut short by a rate limit (7 searches).
- Assumptions: Snippet summaries are accurate; unlabeled-as-unverified numbers come from search snippets and need primary-source verification before use.
- Contradictions found: (1) CMHC/PBO "need" vs TMU finding that young-adult co-residence fell 2003–2023; (2) Paixão proxy assumes elasticity-only variation, vs Saiz geography approach; (3) 2025 Montreal rents rose despite higher vacancy; (4) conflicting secondary totals of CMHC gap and projected starts.
- Recommended next investigations: Retrieve Paixão elasticities and compare with geography-based measures; read full IRCC and Ontario/Alberta shift-share specifications; obtain PBO suppressed-household method; NPR-policy event study on CMA rents; land-vs-structure decomposition; Canadian rent-control and investor-demand evidence; verify all [unverified] items.
