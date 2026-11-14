# P1 — Data / ML Researcher: Canadian housing data landscape audit

**Verification status.** The search tool hit a usage limit after about 8 successful searches. Only items marked [V] were confirmed by search this session. Everything else comes from memory and is tagged [unverified]. This includes most table numbers, coverage dates and quality caveats. Nothing here is cited as a number unless a source is given. Table numbers must be confirmed on statcan.gc.ca before use.

## 1. Dataset inventory

Access codes: O = open, R = registration or API key, P = paid or licensed, RDC = Statistics Canada Research Data Centre or restricted.

### 1a. CMHC

| Dataset | Identifier / publisher | Measures | Unit / geography | Frequency / span | Access | Quality issues | Linkage keys | Panel/causal use |
|---|---|---|---|---|---|---|---|---|
| Starts & Completions Survey (SCS) | CMHC; mirrored in StatCan **34-10-0134-01** (annual, selected CMAs) and **34-10-0154-01** (monthly, selected CMAs) [V, search listing]. National/provincial table 34-10-0135-01 is a quarterly all-areas table [V], so it is not the CMA table. | Starts, under construction, completions. Also absorptions and intended market (freehold, condo, rental, co-op), by dwelling type [unverified detail]. | Surveyed to census-tract and neighbourhood level on the CMHC portal [unverified]. StatCan mirror is CMA. | Monthly, long history [unverified start year]. Since 1 Jan 2023, completions are collected only in CMAs [V]. | O | The 2023 completions-scope change creates a break for non-CMA places [V]. Intended-market is surveyor-assigned and can be reclassified [unverified]. Starts are counted at foundation or footing stage, so they are not permit-linked [unverified]. | CMA code (SGC); CMHC zone/neighbourhood to CT crosswalk [unverified]; CMHC-specific geography is not identical to StatCan CMA vintages [unverified]. | **High.** Best open outcome series for supply: CMA×month and CMA×year, with finer CT×year available on request. |
| CMHC Housing Market Information Portal (HMIP) | CMHC, cmhc-schl.gc.ca | Same SCS, Rental Market Survey (RMS), absorptions, prices, in one UI. | CMA, zone, neighbourhood, CT. | Monthly/annual | O (UI plus export); a bulk API is not confirmed [unverified] | Small-cell suppression at fine geography [unverified]. Zone boundaries are revised over time [unverified]. | Zone IDs, CT. | High for within-CMA variation. Scraping is manual. |
| Rental Market Survey (RMS) | CMHC; StatCan mirrors e.g. 34-10-0127-01 (vacancy) [unverified] | Primary-market purpose-built rental universe (structures with 3+ units): vacancy, average rent, rent change, availability, universe counts. | CMA, zone, CT. | Annual (October), plus a spring survey in some CMAs [unverified]. | O | Excludes the secondary market (condos, houses, basement suites). Average rent is a stock average, not asking rent, and is affected by turnover and rent control. | CMA, zone. | High for rent-stock panels (CMA×year). |
| Secondary Rental Market Survey (SRMS) | CMHC | Condo and other secondary rentals: rent, vacancy, share rented. | CMA, annual. | Annual [unverified: not all CMAs every year]. | O | Sample-based. Rules for sample and CMA coverage have changed [unverified]. | CMA | Medium. |
| Housing Supply Reports / Housing Supply Gap | CMHC | Modelled projections of supply required for affordability by 2030, 2035. | Province, a few CMAs. | Irregular | O (reports) | The model is CMHC's own and is not reproducible from public inputs [unverified]. | None | Benchmark only. |
| Construction duration | CMHC publishes starts-to-completions timing studies; no standard open table [unverified] | Time from start to completion. | CMA | One-off | O (report) | Can be derived from SCS, but the unit-level file is restricted [unverified]. | | Medium. |
| Housing Accelerator Fund (HAF) data | CMHC progress report and rounds data pages [V] | Funded municipalities, funding, targeted units, initiatives; progress tracker by intake year and region [V]. | Municipality (about 544 applications and 179 signed agreements as of April 2024 per OpenCouncil [V]) | Rolling since 2023 | O | Self-reported commitments. Third-party trackers (OpenCouncil, centre.support) [V]. Treatment is non-random: municipalities applied and were selected. | CSD name or code (a crosswalk is needed) | High for a staggered DiD design, subject to the selection problem. |

### 1b. Statistics Canada

| Dataset | Identifier | Measures | Geography | Frequency / span | Access | Quality issues | Keys | Panel/causal use |
|---|---|---|---|---|---|---|---|---|
| Building Permits Survey | Subject page [V]. Current monthly value tables are **34-10-0292-01** and **34-10-0285-01** [V, listed on the building permits subject page]. The older monthly table 34-10-0066-01 existed in releases from 2019 to 2023 [V], and its current status is unclear [V]. | Number of units and value of construction by type of structure and work. | Province, CMA, CSD (municipality) [unverified for CSD tables]. | Monthly, from 1990s [unverified]. | O | Permit value is declared at issuance. Permits are issued at different stages in different municipalities. Non-issuance paths (e.g. development agreements) are not captured [unverified]. Coverage varies by municipality [unverified]. | CSD (SGC code), CMA | **High.** CSD×month is the finest open panel. |
| New Housing Price Index (NHPI) | **18-10-0205-01** [V]: monthly since Jan 1981, base Dec 2016=100, covers Canada, regions, provinces, CMAs and CAs [V]. Companion percent-change table 18-10-0205-02 [V]. Annual weights 18-10-0210-01 [V]. | Constant-quality contractor-reported selling price of new houses. Separate land and structure indexes. | CMA/CA | Monthly | O | Excludes condos [unverified: separate series]. Contractor-reported. | CMA | High for new-home price panels. |
| Building Construction Price Index | Quarterly [unverified table number] | Cost of non-residential and residential construction. | CMA (selected) | Quarterly | O | Based on contractor surveys [unverified]. | CMA | Medium for the cost side. |
| Investment in building construction | Monthly [unverified table number] | Investment values, derived from permits. | Province, CMA | Monthly | O | **Mechanically derived from permits**, so it is not independent evidence (leakage risk). | | Low independent value. |
| Canadian Housing Statistics Program (CHSP) | Table series 46-10-xxxx, for example **46-10-0030-01** (owners by ownership type, residency and number of properties), **46-10-0069-01** (owners by investor status), **46-10-0054-01** (non-resident ownership rates) [V from search results]. | Ownership, investors, non-residents, assessed value, number of properties. | Province, CMA, CSD for some tables [unverified]. | Annual, from about 2018. Jurisdiction coverage grew over time [V, via search results mentioning Nova Scotia, Ontario, BC in 2018 and 2019]. | O (tables); microdata via RDC | Built on assessment rolls, which differ by province. Coverage is not national in early years [unverified]. The assessed-value basis differs by province. | CSD, CMA | High for ownership and investor panels. Vacant land is included in some releases [unverified]. |
| Census / NHS housing (shelter cost, core housing need, dwelling type, tenure, period of construction) | Census 1981 to 2021; 2016 and 2021 profile tables [unverified IDs] | Housing stock, tenure, rent/shelter cost, affordability, suitability, adequacy, core housing need. | DA / CT / CSD / CMA | 5-year (1981-2021). 2011 NHS was voluntary, which breaks comparability with other years. | O | Boundary changes. Random rounding and suppression. NHS 2011 non-response bias. Core need is defined from 1991 and was revised [unverified]. | Census geography UIDs | **High** for the long-run stock panel, but only 5 time points. |
| Population estimates and NPR | Annual and quarterly estimates (table 17-10-xxxx), including non-permanent residents (NPRs) at provincial level quarterly [unverified]. NPR at CMA/CSD is annual and has revision issues [unverified: search for this failed]. | Population components. | Province quarterly, CMA/CSD annual. | | O | NPR estimation is revised often. CMA/CSD estimates are model-based. | | High (demand shifter) but measurement-limited. |
| Labour Force Survey (LFS) and Job Vacancy and Wage Survey (JVWS) | LFS monthly by CMA, NAICS construction. JVWS quarterly vacancies for construction [unverified table numbers]. | Employment, hours, vacancies by industry. | Province, CMA (LFS); province, some CMA (JVWS) | Monthly/quarterly | O | LFS CMA sampling error is large for construction. JVWS vacancy coverage is thin below province. | | Medium (labour-constraint studies). |
| Construction productivity | Productivity accounts (industry-level) [unverified] | Labour productivity by industry. | National | Annual | O | Industry level only. | | Low spatial value. |
| Municipal Land Use and Regulation Survey (MLURS) | I could not verify the existence or scope of a StatCan MLURS [search for it failed]. A CMHC "Municipal Land Use and Regulation Index" built from more than 400 municipalities is mentioned in trade press [V, secondary source]. | Fees, timelines, planning requirements, opposition. | Municipality | Single wave [unverified] | Unknown | The underlying data release is not found [V: dataset not located]. | | Potentially very high but access unknown. |
| Canadian Housing Survey | StatCan, biennial [unverified] | Household-level housing need, satisfaction, affordability. | Household, province | 2018, 2021, 2022 [unverified] | RDC / PUMF [unverified] | Small sample below province. | | Low for spatial supply work. |
| Financial Information Returns / municipal finance | Provincial FIR (Ontario FIR via Ministry of Municipal Affairs; BC Local Government Statistics; Alberta MFIS) [unverified details]. StatCan municipal tables 10-10-0020-01 style [unverified]. | Revenue by source (property tax, DCs, permits), reserves, debt. | Municipality | Annual | O | Definitions differ by province. DC revenue is sometimes reported in deferred reserves, not revenue. Amalgamations. | Municipal ID (provincial), CSD | High for the fiscal-incentive panel (CSD×year in Ontario). |
| Residential Property Price Index / Teranet-type | StatCan has developed a residential property price index [unverified table]. | Resale price index. | CMA | Monthly | O | | | |

### 1c. Prices and rents (non-StatCan)

| Dataset | Publisher | Measures / geography / frequency | Access | Issues / keys | Use |
|---|---|---|---|---|---|
| MLS HPI | CREA | Composite/type-specific benchmark prices, CMA/local-board areas, monthly [unverified]. | Free summary, paid detail | Local-board geography does not align with CMAs. Revisions. | CMA×month prices. Boundaries must be reconciled. |
| Teranet–National Bank HPI | Teranet | Repeat-sales price index for 11 CMAs, monthly [unverified]. | Free (summary) | Based on registry transactions. Coverage excludes smaller CMAs. | Medium. |
| Rentals.ca / Urbanation | Rentals.ca, Urbanation | Asking rents (Rentals.ca National Rent Report monthly, about 35 CMAs [unverified]). Urbanation: Toronto/GTA condo and rental pipeline [unverified]. | Report free, data licensed | Asking rents are not stock rents. Listing composition shifts. | Asking-rent panel for CMA×month, with caution. |
| Assessment rolls | MPAC (Ontario), BC Assessment, Alberta municipal rolls | Parcel assessed value, property class and use, year built. | Mostly restricted or paid. BC Assessment has a limited open feed [unverified]. | Valuation date differs by province. | Parcel-level studies. Underlies CHSP. |

### 1d. Municipal and provincial

| Dataset | Notes | Access | Issues |
|---|---|---|---|
| Development application and permit open data: Toronto (Development Applications, Building Permits - Active/Cleared), Vancouver (Issued building permits), Calgary (Development permits), Edmonton, Ottawa (Development applications), Montreal (permits) | Application-level with dates [unverified: exact portal names]. Allows pipeline-stage durations (submission to approval to permit). | O (portals) | Fields differ by city. Status codes are inconsistent. Cities started publishing at different times. Only large cities are covered. |
| Zoning bylaw GIS layers | Toronto, Vancouver, Calgary, Edmonton, Ottawa publish zoning polygons [unverified]. | O for big cities | Only the current vintage is generally available; historical zoning requires archived bylaws. No standard code scheme. |
| Development charge histories | Municipal DC bylaws, background studies; BILD/Altus benchmarking is for the GTA [unverified]. Ontario FIR schedule on DC reserve funds [unverified]. | Bylaws O; BILD report restricted [unverified] | Hand-collection required. DC rates differ by unit type and are indexed. |
| Provincial housing-target tracking | Ontario Municipal Housing Targets (2023-31 for 50 municipalities) and BC Housing Target Orders [unverified]. Ontario tracks starts, not permits, against target, via Ministry data [unverified]. | O (partial) | Short time span (post-2023). Policy-endogenous design. |

### 1e. Regulatory indices and zoning atlases

- **Fraser Institute survey-based indices** for residential land-use regulation in the Greater Golden Horseshoe, Lower Mainland and Calgary-Edmonton corridor. The Greater Golden Horseshoe study builds a summary index from five components (Approval Timelines, Council and Community, Cost and Fees, Rezoning Prevalence, Timeline Uncertainty). Typical approval timelines range from 13.8 months (Burlington) to 28 months (Clarington) [V]. Based on developer surveys, so it is perception data from an interested party; the sample and weighting need scrutiny. Sources: https://www.fraserinstitute.org/studies/new-homes-and-red-tape-in-ontario-residential-land-use-regulation-in-the-greater-golden-horseshoe and https://www.fraserinstitute.ca/node/9938 [V].
- **CMHC Municipal Land Use and Regulation Index.** More than 400 municipalities surveyed. Results mention approval times rising with city size and community opposition [V, secondary source: https://www.mpamag.com/ca/mortgage-industry/industry-trends/regulatory-red-tape-drives-up-canadian-home-prices-cmhc-study-finds/565375]. Underlying data not found [V: not located].
- **National zoning atlas:** none found. I did not complete a search for Canadian atlas efforts, so this is [unverified].
- Gap: no regularly updated national panel of approval timelines or zoning stringency.

### 1f. Access routes and boundaries

- **StatCan Web Data Service (WDS) API** gives programmatic table access by table ID (vector and coordinate based) [unverified in this session, standard knowledge]. R `cansim`, Python `stats_can` [unverified].
- **CMHC HMIP** has no official public API [unverified]. R `cmhc` (mountainMath) scrapes HMIP [unverified].
- **cancensus** (R) accesses CensusMapper (requires free API key) [unverified in this session].
- **Boundary changes.** CMA definitions are redefined each census (CMAs added or dropped, component CSDs reassigned). CSD amalgamations (e.g. Ontario and Quebec municipal mergers) and renaming occur. Panels must fix a single boundary vintage. For CSD, use the SGC concordance and correspondence files [unverified]. For CT, use the longitudinal CT concordance (tract-to-tract), and note that CT are redrawn every census [unverified].

## 2. Assessment

**(a) Constructible panels (open data), approximate N×T.** N and T are my estimates from general knowledge, not verified counts.
1. **CMA×month:** starts, completions, under construction (SCS), NHPI, permits, LFS employment, NPR (annual interpolated). N is about 35 to 40 CMAs [V that StatCan mirror has 37 geography items], T about 25+ years, so roughly 10,000 to 12,000 obs. Best and cleanest.
2. **CSD×month or year:** permits (units, value). N about 1,000 to 1,500 municipalities with regular permits [unverified]. T 30 years. Many zeros and small-municipality gaps. Combine with Census (5-year) and FIR (annual, province-specific) for CSD×year.
3. **CT×year:** SCS starts and RMS rents, from the CMHC portal. N several thousand CTs in CMAs, T about 20 [unverified]. Needs scraping and CT concordance. Good for within-city variation but suppression is heavy.
4. **Municipality×year with policy treatment:** HAF (staggered from 2023), Ontario 2023 targets, BC 2023 targets. T is short (2018 to 2025), so it is a pre/post design with few post periods.
5. **City application-level pipeline:** Toronto, Vancouver, Calgary, Edmonton, Ottawa. Project-level duration data. N in the tens of thousands, T about 10 to 20 years. Not harmonised.

**(b) Missingness, suppression, measurement.**
- SCS and RMS suppress small cells at fine geography [unverified].
- Completions have been collected only in CMAs since 2023 [V]. Non-CMA completions are lost after that date.
- Permit value is declared and varies by municipality; permit counts do not equal units built because permits lapse or are cancelled [unverified].
- CHSP coverage grows by province over time, so apparent trends can reflect coverage [V in part].
- Census 2011 NHS voluntary. Census data only every 5 years.
- NPR estimates revised. Population in CMAs model-based.
- Rents: RMS excludes the secondary market, asking rents differ from stock rents.
- Starts are counted at a physical stage, permits at a legal stage, so timing differs across municipalities.

**(c) Leakage risks for predictive modelling.**
- **Permits to starts to completions** are mechanically linked with lags. Forecasting completions from permits and starts is a pipeline identity, not a structural prediction. Use only information available at the forecast origin (lagged permits). Do not include starts, units under construction and completions of the same period.
- "Investment in building construction" is derived from permits.
- NHPI, MLS HPI and Teranet contemporaneous prices move with starts via common cycle drivers (rates, population). Contemporaneous controls absorb effects (bad controls).
- Under construction (stock) = prior stock + starts - completions, an accounting identity. Including all three triple-counts.
- Revised vintages: NPR, CHSP and Census estimates are revised, so use real-time vintages for forecasts.
- Spatial autocorrelation across adjacent CMAs/CTs: random K-fold CV leaks. Use blocked or leave-one-CMA-out CV and forward-chaining in time.
- Policy variables measured after the fact (Fraser index timing) are contaminated by the outcome (cities with slow approvals report slower approvals).

**(d) Where ML adds value vs panel models.**
- Panel (two-way fixed effects, event study, Callaway-Sant'Anna or synthetic DiD) suffices for HAF, targets, rent-control and DC changes. The problem is identification, not functional form.
- ML adds value in: (i) nowcasting and forecasting starts/completions from leading indicators with proper time-blocked CV; (ii) text processing of bylaws, council minutes and planning reports to build regulation measures (NLP); (iii) parcel- or application-level duration modelling (survival models, gradient boosting) of approval times; (iv) double/debiased ML for high-dimensional controls in cross-city regressions; (v) heterogeneous treatment effects (causal forests) if a credible treatment exists; (vi) imputing suppressed cells and harmonising boundaries; (vii) zoning-text to zoning-category classification.
- ML adds little for national aggregate series (few observations, strong autocorrelation).

**(e) Biggest data gaps.**
1. A national, time-varying measure of zoning and land-use restriction (allowed density by parcel over time). No national atlas located.
2. Approval timelines at the application level in a harmonised, national form.
3. Development charges and other fees as a historical municipal panel.
4. Project-level pro forma costs (land, soft costs, financing, labour, materials) for new builds, by city. Only indices (BCPI, NHPI) exist.
5. Developer and builder concentration, firm entry and exit. Not measured nationally [unverified].
6. Land supply: serviced and developable land inventories and servicing capacity (water/wastewater) by municipality.
7. Secondary-market rents and tenure conversions (demolitions, conversions, short-term rentals). Demolitions are partly in permits [unverified].
8. Non-permanent resident housing demand at CSD level (see NPR issue).
9. Intergovernmental fiscal flows by municipality in a consistent form.
10. Rent control and tenant-protection policy histories coded by province (hand-built).

## 3. Data/ML-driven hypotheses

### DATA-1 — Pipeline attrition: permit-to-start-to-completion conversion varies systematically by city and explains much of supply variation
- Mechanism: Gap between permits and starts (and starts to completions) reflects financing, costs, and municipal conditions (post-permit approvals, inspections), not only permit issuance.
- Predicted effect: Conversion rates fall when interest rates and costs rise; vary by regulatory environment. Magnitude unknown [unverified].
- Unit of analysis: CMA×quarter or CSD×year.
- Required variables: permits (units), starts, completions, price and cost indices, policy rate, local fees.
- Potential datasets: Building Permits, SCS (34-10-0134/0154), BCPI, Bank of Canada rates.
- Existing literature: not searched in this session [unverified].
- Evidence against / competing explanations: Definitional mismatch (permit unit counts vs. starts), timing lags, permit expiry, units that start without permits in a given period.
- Likely identification strategy: Descriptive decomposition first; then panel regression with CMA and time FE; rate-shock exposure (leveraged-developer or financing-sensitivity) as an instrument or heterogeneity dimension.
- Expected difficulty: low to medium. Open data, but the lag structure needs care.
- Novelty: medium.
- Policy importance: high (shows where the bottleneck lies after permit).
- Proposed class: D under-researched

### DATA-2 — Staggered HAF effects on permits and starts
- Mechanism: HAF funding conditional on local zoning and process reforms should raise permits.
- Predicted effect: positive on permits. Size unknown. CMHC claims 160,585 permits issued under HAF, 22,000 more than expected [V, CMHC Observer 2026]; this is a self-assessment against CMHC's own counterfactual and not an identified causal estimate.
- Unit of analysis: CSD×month.
- Required variables: HAF agreement dates and amounts, permits, population, pre-trends.
- Potential datasets: CMHC HAF rounds data [V], Building Permits, Census.
- Existing literature: PBO update on HAF [V: https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements]. Key estimates in it I did not verify beyond $4.1B committed and 113,817 anticipated units in the Large/Urban stream [V].
- Evidence against: Selection into applying, pre-existing reform intentions, announcement effects, concurrent shocks (rates, immigration cuts), short post period, permits shifted across time.
- Likely identification strategy: Staggered DiD (Callaway-Sant'Anna) with not-yet-treated and rejected-applicant comparison; synthetic DiD.
- Expected difficulty: medium.
- Novelty: medium to high (recent).
- Policy importance: high.
- Proposed class: D under-researched

### DATA-3 — NLP-built zoning and regulatory-stringency index from bylaws, staff reports and minutes
- Mechanism: Binding constraints (minimum lot size, height, parking, rezoning requirements) reduce supply elasticity.
- Predicted effect: negative on permits and starts per household growth, stronger in high-demand cities. Magnitude unknown.
- Unit of analysis: municipality×year.
- Required variables: coded zoning provisions, approval stage dates.
- Potential datasets: municipal bylaw archives, council minutes, open application data, Fraser index (as validation) [V].
- Existing literature: Fraser Institute indices (survey-based) [V]; CMHC index [V, secondary]. Academic Canadian evidence not searched [unverified].
- Evidence against: Text measures capture de jure not de facto rules (variances, discretionary rezoning); stringency is endogenous to demand.
- Likely identification strategy: Reform events (e.g. Minneapolis-style abolitions, Ontario Bill 23, BC SB 7, Vancouver or Toronto reforms) as shocks with the NLP index as a treatment-intensity measure; instrument unclear.
- Expected difficulty: high (data collection, validation).
- Novelty: high.
- Policy importance: high.
- Proposed class: E potentially novel

### DATA-4 — Application-level survival models of approval time, harmonised across 5+ cities
- Mechanism: Time from application to permit acts as a hidden tax through carrying costs and risk.
- Predicted effect: Longer expected time lowers the hazard of start; magnitude unknown.
- Unit of analysis: application or project.
- Required variables: application, approval and permit dates, project size, type, ward and council composition, rezoning vs. as-of-right.
- Potential datasets: open data from Toronto, Vancouver, Calgary, Edmonton, Ottawa [unverified portal names].
- Existing literature: Fraser GGH timelines (survey-reported, 13.8 to 28 months) [V]; administrative-data comparisons not found.
- Evidence against: Selection (hard projects take longer), status-code inconsistency, left and right censoring, applicant-driven delays.
- Likely identification strategy: Survival/competing-risks models with ward or planner-assignment variation; ward-boundary changes or council turnover as shocks; ML (random survival forests) for prediction with causal claims restricted.
- Expected difficulty: medium to high.
- Novelty: medium.
- Policy importance: high.
- Proposed class: D under-researched

### DATA-5 — Municipal fiscal incentives: development-charge dependence and growth
- Mechanism: Municipalities that fund growth-related infrastructure from DCs vs. property taxes face different incentives to approve housing.
- Predicted effect: ambiguous. Higher DC share could reduce approvals (cost to builders) or raise municipal willingness (growth pays for itself).
- Unit of analysis: Ontario municipality×year.
- Required variables: DC rates, DC reserve balances, FIR revenue, permits.
- Potential datasets: Ontario FIR, DC bylaws, Building Permits.
- Existing literature: not searched [unverified].
- Evidence against: DC rates are set endogenously to growth; Bill 23 (2022) DC exemptions provide variation but are province-wide.
- Likely identification strategy: Bill 23 exposure by municipality's pre-reform DC reliance (shift-share style); event study.
- Expected difficulty: medium (FIR cleaning, amalgamations).
- Novelty: medium.
- Policy importance: high.
- Proposed class: B partially understood

### DATA-6 — Time-blocked forecasting benchmark for CMA starts and completions with honest leakage controls
- Mechanism: Leading indicators (permits, rates, population inflows, prices) predict supply with a lag.
- Predicted effect: Prediction only, no causal claim. Gains of ML over a simple AR plus permits model are uncertain [unverified].
- Unit of analysis: CMA×month.
- Required variables: lagged permits, rates, NPR flows, NHPI, labour data.
- Potential datasets: SCS, Building Permits, LFS, NHPI.
- Existing literature: not searched [unverified].
- Evidence against: Strong autocorrelation, short effective sample, structural breaks (2020, 2022 to 2024 rate shock), so ML may not beat naive baselines.
- Likely identification strategy: Not causal. Rolling-origin evaluation, vintage data.
- Expected difficulty: low to medium.
- Novelty: low.
- Policy importance: medium (supports other projects as a benchmark).
- Proposed class: A well established (method), application D

## Summary
- Claims (each with confidence):
  - CMA×month (SCS plus permits plus NHPI) is the cleanest constructible panel; CSD×month permits is the finest open one (med-high).
  - There is no national, time-varying, open measure of zoning stringency or approval timelines (med; one failed search, so non-exhaustive).
  - Permit, starts, under construction and completions are mechanically linked and are a main leakage source (high).
  - The 2023 CMHC completions-scope change to CMAs only creates a break for non-CMA series (high, verified).
  - HAF offers a staggered design but with selection and a short post period (med).
  - ML adds most in text-based regulation measurement, duration modelling and nowcasting; panel econometrics is sufficient for most policy evaluation (med).
- Supporting evidence: StatCan table listings for 34-10-0134-01, 34-10-0154-01, 34-10-0135-01, 18-10-0205-01, 34-10-0292-01, 34-10-0285-01, 46-10-0030-01, 46-10-0054-01, 46-10-0069-01; Fraser GGH indices; CMHC HAF pages and PBO update.
- Sources:
  - https://www150.statcan.gc.ca/n1/en/subjects/construction/building_permits
  - https://www150.statcan.gc.ca/n1/en/catalogue/3410013501
  - https://www150.statcan.gc.ca/t1/tbl1/en/cv.action?pid=3410013501
  - https://www150.statcan.gc.ca/n1/en/cansim/327-0056
  - https://www150.statcan.gc.ca/n1/pub/46-28-0001/2023001/article/00001-eng.htm
  - https://www150.statcan.gc.ca/n1/pub/11-627-m/11-627-m2018048-eng.htm
  - https://www.fraserinstitute.org/studies/new-homes-and-red-tape-in-ontario-residential-land-use-regulation-in-the-greater-golden-horseshoe
  - https://www.mpamag.com/ca/mortgage-industry/industry-trends/regulatory-red-tape-drives-up-canadian-home-prices-cmhc-study-finds/565375
  - https://www.cmhc-schl.gc.ca/professionals/project-funding-and-mortgage-financing/funding-programs/all-funding-programs/housing-accelerator-fund/housing-accelerator-fund-rounds-data
  - https://www.cmhc-schl.gc.ca/en/observer/2026/boosting-housing-supply-housing-accelerator-fund-progress
  - https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements
  - https://opencouncil.ca/housing-accelerator-fund/
- Uncertainty: The search quota ran out after about 8 successful searches (target was 20 to 30). Most table numbers, date ranges, access modes, quality caveats, API availability, city portal names and N×T figures are unverified. The existence and scope of a StatCan MLURS and any national zoning atlas were not confirmed. The status of table 34-10-0066-01 is unclear.
- Assumptions: N×T figures are order-of-magnitude. CMA count of about 37 is from a search listing [V]. Unverified items reflect general knowledge as of training.
- Contradictions found: 34-10-0135-01 is not a CMA table although it is often cited as such (it is a quarterly all-areas table [V]); CMA data are in 34-10-0134-01 and 34-10-0154-01. The HAF claim of "22,000 more permits than expected" is CMHC's own counterfactual, not an independent estimate.
- Recommended next investigations: (1) Re-run the failed verifications (MLURS, NPR by CMA/CSD, cancensus/cmhc/cansim packages, Ontario FIR and DC data, city open-data portals, zoning-atlas efforts, Teranet/CREA access) once quota resets. (2) Pull table metadata through the WDS API to confirm table IDs, coverage and start dates. (3) Prototype the CMA×month panel and a permits-to-completions conversion analysis (DATA-1). (4) Assemble the HAF treatment file with agreement dates and rejected/pending applicants (DATA-2). (5) Test whether application-level open data are harmonisable across cities (DATA-4).
