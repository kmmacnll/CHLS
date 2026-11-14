# P1 — Urban / Planning Researcher: Phase 1 Hypothesis Discovery

**Search status:** 5 of ~15–25 planned searches completed before the search tool hit a usage limit (resets 22:40 UTC). Only claims backed by those results carry a confirmed source. Everything else is `[unverified]` (recalled from memory, not checked this session) or marked "to be searched". Do not treat this file as a completed literature review. No hypothesis is assumed correct.

Confirmed-source key (used below):
- S1 BILD/Altus GTA benchmarking 2022: https://bildgta.ca/municipal-benchmarking-study-2022 ; summary https://www.cbc.ca/1.6598176
- S2 CHBA/Altus Municipal Benchmarking 3rd ed. 2024: https://www.chba.ca/assets/pdf/CHBA+Municipal+Benchmarking+Study-3rd+Edition-2024
- S3 Fraser Institute, Residential land-use regulation in the Greater Golden Horseshoe: https://www.fraserinstitute.org/studies/new-homes-and-red-tape-residential-land-use-regulation-ontarios-greater-golden-horseshoe ; and Impact of Land Use Regulation on Housing Supply in Canada: https://www.fraserinstitute.ca/sites/default/files/impact-of-land-use-regulation-on-housing-supply-in-canada.pdf
- S4 Edmonton zoning reform one-year view (Taproot): https://edmonton.taproot.news/news/2025/05/28/one-year-after-zoning-reform-housing-surges-but-sprawl-continues ; U of Alberta Land Institute: https://www.ualberta.ca/alberta-land-institute/news/2025/july/edmonton_zoning_updates.html ; CBC "experts are split": https://www.cbc.ca/lite/story/1.6994951
- S5 Stalled/approved-unbuilt GTHA: https://www.bnnbloomberg.ca/business/real-estate/2025/10/22/stalled-housing-projects-in-gtha-significantly-outnumber-active-projects-report/ ; City of Toronto Development Pipeline: https://www.toronto.ca/city-government/data-research-maps/research-reports/planning-development/development-pipeline/ ; https://therealdeal.com/international/toronto/2025/07/14/toronto-condo-pipeline-plagued-by-scuttled-plans/

Note: search summaries were secondary (news/aggregator text). Primary-document figures should be re-verified against the linked reports before use in analysis.

---

### PLAN-1 — Approval delay raises cost and reduces supply (timeline hypothesis)
- Mechanism: Long, uncertain rezoning/site-plan/permit timelines raise carrying costs, interest and risk premia, cutting the set of feasible projects and slowing starts.
- Predicted effect: Negative on starts and positive on cost per unit; magnitude unestablished. BILD/Altus attributes up to ~$50,000 added cost to a GTA condo apartment from timeline growth since 2020 (industry-commissioned; headline from https://www.bildgta.ca/delays-in-municipal-approval-timeframes-for-new-housing-increased-significantly-since-2020-adding-up-to-50000-to-the-cost-of-a-condominium-apartment/).
- Unit of analysis: municipality-year; application-level.
- Required variables: application submission/approval dates, application type, unit count, starts/completions, municipal staffing.
- Potential datasets: Altus/BILD and CHBA benchmarking; municipal open-data permit logs; CMHC starts; Toronto Development Pipeline.
- Existing literature: BILD 2022: GTA approval timelines 10–34 months by municipality, most application types 20–24 months average, +41% vs 2020 study; fastest (Milton, Whitby, Barrie, Oakville, Brampton) <16 months; slowest (Caledon, Toronto, Richmond Hill, Vaughan) ≥27 months (S1). CHBA 2024: average application 11.2 months, down 2.1 months from prior study; methodology changed to municipal-sourced data so editions are not directly comparable (S2). Halifax 21 months (2022), Winnipeg 5.0 months in CHBA city sheets (https://st.chba.ca/CHBADocs/CHBA/HousingCanada/Government-Role/Municipal-Benchmarking-Halifax_2022.pdf). Association only.
- Evidence against / competing: benchmarking is industry-commissioned, unaudited sample selection; timelines may be endogenous to project complexity (large towers take longer); approved projects stall for financing reasons (PLAN-8). Faster-approving municipalities (e.g., Barrie, Milton) are greenfield/low-density, so speed may reflect project type.
- Likely identification strategy: event study around process reforms (Ontario Bill 109 fee-refund deadlines, pre-/post); staff-turnover or provincial-mandate shocks as instruments; application-level hazard models of time-to-approval and time-to-start.
- Expected difficulty: med (data access to application-level logs).
- Novelty: low–med. Policy importance: high. Proposed class: B

### PLAN-2 — Restrictive zoning/density limits constrain supply and raise prices (stringency hypothesis)
- Mechanism: Binding height/density/use limits cut feasible redevelopment, especially in high-demand cores and low-density neighbourhoods; price reflects a regulatory tax.
- Predicted effect: Negative on supply elasticity; positive on land values/prices. Canadian magnitude unestablished here `[unverified]`.
- Unit of analysis: CMA/municipality; parcel.
- Required variables: zoning capacity (permitted vs. built FSI/units), land values, permits, a stringency index.
- Potential datasets: StatCan/CMHC Municipal Land Use and Regulation Survey (existence/contents `[unverified]`; not retrieved), municipal zoning GIS, assessment data (MPAC/BC Assessment), Fraser surveys.
- Existing literature: Fraser Institute reports find more highly regulated Canadian cities have less housing-stock growth (association, survey-based index) and rank 23 GGH municipalities, Burlington least and King Township most regulated; Toronto 20th of 23; reported compliance costs/fees from ~$21,000 (Hamilton) to ~$60,500 (Oakville) per home (S3). The Fraser index is modelled on Gyourko-Saiz-Summers (2008), a US measure. Neither is a causal Canadian estimate. Further academic Canadian studies (e.g., Hamilton/Mok/Somerville-type work) not searched `[unverified]`.
- Evidence against / competing: Fraser is an advocacy-affiliated think tank using developer surveys (perception bias); cross-city correlations confounded by geography and demand; US evidence (Gyourko et al.) may not transfer.
- Likely identification strategy: parcel-level difference-in-differences around upzonings (Edmonton, Calgary, Toronto multiplex, BC Bill 44); boundary discontinuities in zoning districts; capacity-vs-built gap analysis.
- Expected difficulty: high (no standardized national zoning dataset).
- Novelty: low. Policy importance: high. Proposed class: C

### PLAN-3 — Blanket upzoning (missing-middle legalization) increases supply (reform-effect hypothesis)
- Mechanism: Removing single-family exclusivity raises redevelopment feasibility; effect depends on land cost, construction cost, and lot economics.
- Predicted effect: Positive on infill units, magnitude uncertain and likely small in short run.
- Unit of analysis: parcel/neighbourhood-quarter; city.
- Required variables: permits by type and location pre/post, lot size, land value, construction cost.
- Potential datasets: Edmonton and Calgary open permit data; Toronto multiplex permits; CMHC starts; BC provincial reporting under Bill 44 `[unverified]`.
- Existing literature: Edmonton's bylaw (took effect 2024): record 18,400 starts in a year per CMHC (CBC, year not confirmed), city credits bylaw partly, sprawl continues (S4); Alberta Land Institute says bylaw maintained relatively affordable housing vs. other cities; CBC reports experts split on affordability impact (S4). No peer-reviewed causal evaluation was found. Calgary R-CG blanket rezoning, Toronto multiplex (2023), BC Bill 44/47, Ontario Bills 23/109/185: searches not completed; effects `[unverified]`/to be searched.
- Evidence against: concurrent shocks (Edmonton's cost advantage, interprovincial migration, interest rates) confound simple pre/post; permits may substitute across zones rather than add.
- Likely identification strategy: synthetic control / DiD with comparison cities (Edmonton vs. Calgary/Saskatoon/Winnipeg); parcel-level triple-differences on upzoned vs. already-permissive lots.
- Expected difficulty: med. Novelty: med (young reforms). Policy importance: high. Proposed class: D

### PLAN-4 — Municipal planning staff capacity and process complexity drive approval times
- Mechanism: Underfunded/short-staffed planning departments, sequential multi-department reviews and public-consultation requirements lengthen queues independently of zoning rules.
- Predicted effect: Negative on throughput; elasticity unknown.
- Unit of analysis: municipality-year.
- Required variables: planner FTEs per application, budgets, application counts, review stage durations.
- Potential datasets: municipal budgets, FIR (Ontario Financial Information Returns), benchmarking studies, Housing Accelerator Fund action plans.
- Existing literature: BILD notes wide dispersion in timelines across GTA municipalities facing the same provincial rules (S1) — suggestive of local administrative capacity, not proof. Direct capacity studies not searched `[unverified]`.
- Evidence against: dispersion may reflect project mix; capacity is endogenous to growth.
- Likely identification strategy: panel with municipality fixed effects; staffing shocks; HAF/provincial funding as quasi-experiment.
- Expected difficulty: med. Novelty: med–high (little causal work). Policy importance: med. Proposed class: D

### PLAN-5 — Appeals and discretionary rezoning (OLT, public hearings, NIMBY veto) add delay and uncertainty
- Mechanism: Third-party appeals and discretionary council votes create option-value delay and deter marginal projects.
- Predicted effect: Negative; magnitude unknown.
- Unit of analysis: application; project.
- Required variables: appeal filings, outcome, time to decision, share of units affected.
- Potential datasets: OLT case data (access `[unverified]`), municipal council minutes, BC public-hearing records.
- Existing literature: not retrieved (OLT appeal search failed due to search limit). Ontario's reforms limiting appeals (Bill 23) and BC's removal of public hearings for rezonings consistent with OCP (Bill 44-era) are `[unverified]`.
- Evidence against: appeals may affect small share of units; discretion also yields negotiated benefits (inclusionary zoning, community benefits).
- Likely identification strategy: application-level survival analysis; exploit changes in appeal rights (Bill 108/139/23) as policy shocks.
- Expected difficulty: med. Novelty: med. Policy importance: med. Proposed class: D

### PLAN-6 — Land supply constraints (greenbelts, ALR, urban boundaries, geography) raise prices
- Mechanism: Binding growth boundaries and protected land reduce greenfield supply, shifting demand to infill, raising land values.
- Predicted effect: Positive on land prices; ambiguous on total supply.
- Unit of analysis: CMA; parcel near boundaries.
- Required variables: developable-land inventory, boundary location/date, land prices.
- Potential datasets: Ontario Greenbelt/Growth Plan GIS, BC ALR, StatCan land use, assessment data.
- Existing literature: not retrieved this session. Fraser/other claims about the Ontario Greenbelt `[unverified]`; Ontario's 2023 Greenbelt removal and its reversal `[unverified]`.
- Evidence against: Ontario Growth Plan-designated "whitelands" and approved greenfield lots remain large `[unverified]`; unbuilt approved inventory (S5) suggests land designation is not the binding limiter in the GTA near term. Vancouver/Toronto geographic limits (water, mountains) are fixed.
- Likely identification strategy: boundary regression discontinuity; Greenbelt designation (2005) as event with comparison areas.
- Expected difficulty: high. Novelty: med. Policy importance: med–high. Proposed class: C

### PLAN-7 — Transit-oriented development / station-area upzoning under-delivers supply
- Mechanism: Allowing density near transit raises feasible units; effect depends on land assembly and rezoning speed.
- Predicted effect: Positive on units near stations; unestablished.
- Unit of analysis: station area/MTSA; parcel.
- Required variables: permitted vs. built density, assembly costs, transit service.
- Potential datasets: Ontario MTSA designations, TransLink Area plans, Toronto development pipeline.
- Existing literature: not searched; Ontario Protected Major Transit Station Areas and BC TOA legislation (2023) `[unverified]`.
- Evidence against: land assembly and ownership fragmentation, parking minimums, and market conditions can limit uptake.
- Likely identification strategy: DiD around designations; spatial regression discontinuity at station-area boundaries.
- Expected difficulty: med. Novelty: med. Policy importance: med. Proposed class: D

### PLAN-8 — Approved-but-unbuilt inventory: regulation is not the binding constraint (counter-hypothesis)
- Mechanism: When approvals exceed construction, financing, presale thresholds, development charges and demand—not entitlement—bind. Reducing approval burden would then yield little extra supply.
- Predicted effect: Zero/small effect of further entitlement reform on starts in high-inventory markets.
- Unit of analysis: CMA-quarter; project.
- Required variables: approved units, starts, presale rates, financing terms, DCs, cancellations.
- Potential datasets: Urbanation, CMHC, Toronto Development Pipeline, BILD, CivicAction report.
- Existing literature: CivicAction (via BNN Bloomberg, Oct 2025): 481 active GTHA projects (Q2 2025) vs. more than four times as many approved but on hold; 2,220 stalled projects / 1,218,626 units (S5). Toronto approved average >29,700 units/yr in 2017–2021 vs. ~16,000 built per year; 258,397 units approved awaiting construction as of mid-2024 (Toronto pipeline, S5). Reports of >20,000 GTA condo units cancelled/deferred in 2024–25 and a fivefold rise in Toronto condo cancellations 2022–2025 (secondary reporting; CMHC attribution unverified; S5). Association only.
- Evidence against: approvals are lumpy and some are speculative/entitlement-flipping; unbuilt inventory may reflect cost-feasibility created by past regulation (e.g., DCs, inclusionary requirements, parking); "approved" ≠ "as-of-right".
- Likely identification strategy: decompose starts-to-approval conversion rates by pro forma feasibility; compare approval-to-start lags across markets and rate regimes.
- Expected difficulty: med. Novelty: med. Policy importance: high. Proposed class: B

### PLAN-9 — Fees, development charges and parkland levies act as the effective regulatory burden
- Mechanism: Per-unit exactions raise upfront cost and project feasibility thresholds; incidence falls on buyers, landowners or developers.
- Predicted effect: Negative on marginal-project feasibility.
- Unit of analysis: municipality; project.
- Required variables: DC/CAC/parkland rates by type, project costs, land values.
- Potential datasets: municipal DC bylaws, Altus/BILD, CHBA benchmarking, Fraser surveys.
- Existing literature: Fraser GGH reports estimate fees/compliance costs $21,000–$60,500 per home (S3, developer-reported). CMHC statements on DC stalling ~100,000 approved homes (secondary news summary; unverified at primary; S5). Incidence studies `[unverified]`.
- Evidence against: DCs fund infrastructure that enables growth; incidence may fall on land values, not prices.
- Likely identification strategy: DC rate changes (Bill 23 DC cuts, 2022–23; municipal bylaw updates) as DiD; bunching in application timing before rate changes.
- Expected difficulty: med. Novelty: med. Policy importance: high. Proposed class: C (public finance specialist overlap)

### PLAN-10 — Office-to-residential conversion and adaptive reuse can add meaningful supply
- Mechanism: Underutilized office stock can convert to residential, bypassing land costs, subject to floor-plate and code constraints and subsidy.
- Predicted effect: Positive but small relative to national shortfall.
- Unit of analysis: building; downtown CMA.
- Required variables: vacancy, building floor plates, conversion cost, incentive uptake.
- Potential datasets: Calgary Downtown incentive program reports, CBRE/Colliers vacancy, CMHC.
- Existing literature: search not completed; Calgary downtown conversion program totals, federal Housing Accelerator, and CMHC commentary `[unverified]` — to be searched.
- Evidence against: structural/code/economic constraints typically make only a minority of buildings feasible `[unverified]`; supply is small compared with shortfalls.
- Likely identification strategy: building-level feasibility models; program take-up analysis.
- Expected difficulty: low–med. Novelty: med. Policy importance: low–med. Proposed class: D

### PLAN-11 — Housing-type mix (high-rise concentration) and building-code/parking rules limit production speed
- Mechanism: Policy channels production into a few project types (concrete high-rise, large-lot greenfield) with long, capital-intensive cycles; missing-middle lacks a mature building pathway.
- Predicted effect: Fewer entry-level, small-builder projects; slower responsiveness to price signals.
- Unit of analysis: CMA-year; builder.
- Required variables: starts by structure type, builder size, parking requirements, code requirements (e.g., second egress/elevator rules).
- Potential datasets: CMHC starts by type; permits; municipal code/parking bylaws.
- Existing literature: not retrieved; claims about Canadian missing-middle share and single-stair/elevator rules `[unverified]`.
- Evidence against: construction cost/labour constraints may dominate (construction specialist domain); high-rise dominance reflects land economics in dense cores.
- Likely identification strategy: DiD around parking-minimum removals and code changes.
- Expected difficulty: med. Novelty: high. Policy importance: med. Proposed class: E

---

## Key disagreements/uncertainties noted
1. Industry-commissioned data (BILD, CHBA, Fraser) are the main Canadian measures of regulatory burden; independent, causal Canadian evidence is thin or not yet retrieved.
2. Approved-but-unbuilt inventories (S5) vs. approval-delay claims (S1) point to different binding constraints; they may both be true in different market phases (boom vs. high-rate bust).
3. Edmonton reform attribution: city and press credit the bylaw; no causal study found; experts split (S4).
4. CHBA 2024 timelines (11.2 months national average) not comparable to earlier editions due to method change (S2).

## Summary
- Claims (each with confidence):
  - GTA approval timelines vary widely across municipalities (10–34 months in 2022) and lengthened ~41% from 2020 to 2022 per Altus/BILD: medium (industry study; secondary report).
  - National CHBA average 11.2 months (2022–24), method not comparable to prior editions: medium.
  - Large approved-but-unstarted inventories exist in the GTHA (Toronto ~258,000 units mid-2024; CivicAction ~1.2M units on hold): medium (secondary reports).
  - Fraser Institute surveys find higher fees/regulation associated with lower housing growth in Canadian cities: low–medium (association; advocacy-affiliated, perception-based).
  - Edmonton starts hit a record after bylaw reform but causal attribution unestablished: low.
  - Planning capacity, appeals, greenbelt, TOD, office conversion, housing-type hypotheses: no confirmed Canadian estimates this session: low.
- Supporting evidence: S1–S5 above.
- Sources: see S1–S5 and inline links.
- Uncertainty: only 5 searches completed (rate limit); many policy reforms (BC Bill 44/47, Calgary R-CG, Toronto multiplex, Ontario Bills 23/109/185, HAF, OLT, MLURS, conversion programs) not researched; all remaining claims are `[unverified]`. Search summaries were secondary text, not primary documents.
- Assumptions: that sampled benchmarking is representative; that news summaries of CivicAction/CMHC/Toronto figures reflect the primary reports.
- Contradictions found: approval-delay narrative vs. unbuilt-pipeline evidence; improving average timelines (CHBA) vs. rising costs and falling starts; method change breaks comparability.
- Recommended next investigations: (1) retrieve MLURS and any StatCan/CMHC regulatory data; (2) peer-reviewed Canadian upzoning/regulation causal studies (e.g., from Bank of Canada, CMHC, university economists); (3) BC Bill 44/47, Calgary R-CG, Toronto multiplex uptake data; (4) OLT appeal statistics; (5) office conversion program totals; (6) re-verify S5 figures against primary CivicAction, CMHC, and Toronto documents; (7) Phase 2: parcel-level capacity-vs-built analysis and application-level time-to-approval models.
