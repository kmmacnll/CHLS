# P1 — Urban / Planning Researcher: Phase 1 Hypothesis Discovery

Method note: ~14 web searches run. Most figures come from search-result summaries of secondary text (news, government pages), not full primary documents; re-verify against the linked primary source before use. Items not confirmed are tagged `[unverified]`. No hypothesis is assumed correct.

Sources (referenced as S#):
- S1 BILD/Altus GTA benchmarking 2022: https://bildgta.ca/municipal-benchmarking-study-2022 ; https://www.cbc.ca/1.6598176
- S2 CHBA/Altus Municipal Benchmarking 3rd ed. 2024: https://www.chba.ca/assets/pdf/CHBA+Municipal+Benchmarking+Study-3rd+Edition-2024
- S3 Fraser Institute: https://www.fraserinstitute.org/studies/new-homes-and-red-tape-residential-land-use-regulation-ontarios-greater-golden-horseshoe ; https://www.fraserinstitute.ca/sites/default/files/impact-of-land-use-regulation-on-housing-supply-in-canada.pdf
- S4 Edmonton: https://edmonton.taproot.news/news/2025/05/28/one-year-after-zoning-reform-housing-surges-but-sprawl-continues ; https://www.ualberta.ca/alberta-land-institute/news/2025/july/edmonton_zoning_updates.html ; https://www.cbc.ca/lite/story/1.6994951
- S5 Approved-unbuilt: https://www.bnnbloomberg.ca/business/real-estate/2025/10/22/stalled-housing-projects-in-gtha-significantly-outnumber-active-projects-report/ ; https://www.toronto.ca/city-government/data-research-maps/research-reports/planning-development/development-pipeline/
- S6 StatCan/CMHC Municipal Land Use and Regulation Survey (MLURS) 2022: https://www150.statcan.gc.ca/n1/en/surveys/5382 ; CMHC Observer https://www.cmhc-schl.gc.ca/observer/2023/approval-delays-linked-lower-housing-affordability ; CMHC 2026 report https://publications.gc.ca/collections/collection_2026/schl-cmhc/nh18-33/NH18-33-92-2026-eng.pdf
- S7 BC SSMUH: https://www2.gov.bc.ca/gov/content/housing-tenancy/local-governments-and-housing/housing-initiatives/smale-scale-multi-unit-housing ; https://www.castanetkamloops.net/news/Metro-Vancouver/584121/BCs-multiplex-rollout-hits-speed-bumps-as-cities-diverge
- S8 Calgary: https://www.calgary.ca/planning/projects/rezoning.html ; https://www.cbc.ca/lite/story/1.7390095 ; https://livewirecalgary.com/2025/11/21/hundreds-of-land-use-hearings-avoided-through-citywide-rezoning/ ; https://www.ctvnews.ca/calgary/article/calgary-repeals-blanket-rezoning-considers-replacement-rules-for-housing/
- S9 Toronto multiplex monitoring: https://www.toronto.ca/legdocs/mmis/2025/ph/bgrd/backgroundfile-255851.pdf ; https://www.movesmartly.com/articles/what-torontos-multiplex-boom-is-actually-delivering
- S10 Calgary office conversion: https://livewirecalgary.com/2025/11/14/tangible-results-starting-to-show-in-downtown-conversions-mahler/ ; https://www.cbc.ca/1.7480038
- S11 Ontario legislation/OLT: https://www.osler.com/en/insights/updates/fundamental-changes-made-to-planning-act-appeals-as-bill-185-receives-royal-assent/ ; https://olt.gov.on.ca/wp-content/uploads/OLT_2026-2029_Business_Plan.html
- S12 HAF: https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements ; https://www.cmhc-schl.gc.ca/observer/2026/housing-accelerator-fund-building-more-livable-communities
- S13 Zemp (2025), Canadian Planning and Policy: https://erudit.org/en/journals/cpp/2025-v2025-n1-cpp09865/1117589ar.pdf ; US comparator Freemark (Chicago TOD upzoning), summarized at https://planetizen.com/node/102740

---

### PLAN-1 — Approval delay raises cost and cuts supply
- Mechanism: Long, uncertain rezoning/site-plan/permit timelines raise carrying cost and risk premia, shrinking the feasible set and slowing starts.
- Predicted effect: negative on starts, positive on cost; magnitude uncertain.
- Unit of analysis: application; municipality-year.
- Required variables: submission/approval/permit/start dates, application type, units, staffing.
- Potential datasets: Altus/BILD, CHBA benchmarking, MLURS 2022, municipal permit logs, Toronto pipeline.
- Existing literature: BILD 2022 — GTA approval timelines 10–34 months; typical 20–24; +41% vs 2020; <16 months in Milton, Whitby, Barrie, Oakville, Brampton; ≥27 months in Caledon, Toronto, Richmond Hill, Vaughan (S1). BILD attributes up to ~$50,000 added cost per GTA condo to delay growth since 2020 (industry-commissioned). CHBA 2024: 11.2 months average, down 2.1 months, but method changed (municipal-sourced) so not comparable to earlier editions (S2). MLURS/CMHC: the Approval Delay Index is the most important of the surveyed regulatory factors explaining affordability differences across regions (S6). CMHC 2026: a 10% more restrictive regulation score goes with roughly 14% higher house prices, controlling for population, density, growth; framed as causal but identification not confirmed (S6). Association unless identification verified.
- Evidence against / competing: industry-commissioned, non-random samples; delay is endogenous to project size/complexity; fast municipalities are mainly greenfield; approved projects stall for financing reasons (PLAN-8).
- Likely identification strategy: event study around process reforms (Bill 109 fee-refund timelines, Bill 185 rollback); time-to-start hazard models at application level; staffing shocks.
- Expected difficulty: med. Novelty: low–med. Policy importance: high. Proposed class: B

### PLAN-2 — Cross-city regulatory stringency explains price/supply differences
- Mechanism: binding density/height/use limits restrict redevelopment, capitalized into prices.
- Predicted effect: negative on supply elasticity; positive on prices.
- Unit of analysis: municipality/CMA.
- Required variables: MLURS index, permits, prices, demand controls.
- Potential datasets: MLURS 2022 (zoning, fees, approval times, consultation, density limits, environmental assessments; index to rank municipalities), Fraser survey, assessment data.
- Existing literature: MLURS: Greater Toronto and Greater Vancouver highest regulation scores (100, 98); Atlantic, Québec and Prairies 23–34% less regulated than GTA (S6). Fraser GGH index of 23 municipalities (Burlington least, King most regulated; Toronto 20th); reported fees/compliance $21,000 (Hamilton) to $60,500 (Oakville) per home (S3, developer-survey, think tank); Fraser also reports association of regulation with slower housing-stock growth. Zemp (2025) estimates a "zoning effect" on BC prices; results not retrieved (S13).
- Evidence against: high-score cities are also the highest-demand cities, so cross-section confounds demand and regulation; an op-ed (Globe and Mail) argues demand factors (foreign ownership, speculation) dominate `[opinion, unverified]`; US indices may not transfer.
- Likely identification strategy: panel with changes in index (needs a second MLURS wave `[unverified]`); border discontinuities; instruments (historical council composition, provincial mandates).
- Expected difficulty: high. Novelty: low–med. Policy importance: high. Proposed class: C

### PLAN-3 — Citywide upzoning of low-density land increases infill supply
- Mechanism: legalizing multiplexes/rowhouses lifts redevelopment feasibility; effect limited by land and construction costs.
- Predicted effect: positive on infill permits; small/slow in aggregate.
- Unit of analysis: parcel/neighbourhood-quarter; city.
- Required variables: permits by type/location, land value, construction cost.
- Potential datasets: Edmonton, Calgary, Toronto open permit data; BC municipal SSMUH reports.
- Existing literature (all descriptive, no causal study found):
  - Edmonton (2024): record ~18,400 starts in a year per CMHC (year unconfirmed); city credits bylaw partly; sprawl continues; experts split (S4).
  - Calgary: citywide rezoning passed 14 May 2024, effective 6 Aug 2024 (R-CG base in established areas). 189 R-CG permit applications received shortly after passage; 478 development permits enabled that would otherwise have required 460 rezoning hearings; city says attribution of permit increase undetermined (S8). Council repealed citywide rezoning 8 Apr 2026, replacement rules (lower R-CG height/coverage) effective 4 Aug 2026 (S8) — a political-durability finding.
  - Toronto multiplexes (as-of-right 2023): city monitoring May 2023–Nov 2024 — 750 applications, 452 permits issued (2–4 units) (S9); a secondary report cites 2,629 permits/4,880 net homes since 2023 `[unverified]`; 32% of multiplex permits had zero parking (S9).
  - BC SSMUH (Bill 44, bylaws due 30 June 2024): government forecasts up to 130,000 homes in ten years (forecast, not observed); no province-wide permit count found; rollout "speed bumps" as cities diverge; Bill 25 (27 Nov 2025) legislated fixes to implementation (S7). North Vancouver: only 35 lots eligible (eligibility, not permits).
  - US comparator: Chicago TOD upzoning raised property values 15–23% with no added construction in 3–5 years (S13).
- Evidence against: confounded by interest rates, migration, concurrent shocks; permits can displace rather than add; small take-up in Canada so far is plausible though not yet quantified.
- Likely identification strategy: DiD/synthetic control (Edmonton vs. comparators), parcel-level triple differences (upzoned vs. already permissive), BC municipal staggered compliance dates.
- Expected difficulty: med. Novelty: med–high. Policy importance: high. Proposed class: D

### PLAN-4 — Municipal planning capacity and process design drive approval times
- Mechanism: understaffed departments, sequential reviews and consultation requirements create queues independent of the zoning text.
- Predicted effect: negative on throughput; elasticity unknown.
- Unit of analysis: municipality-year.
- Required variables: planner FTEs, application volumes, review-stage durations, budgets.
- Potential datasets: Ontario FIR, municipal budgets, benchmarking studies, HAF action plans.
- Existing literature: wide dispersion across GTA municipalities facing the same provincial rules (S1) is suggestive only. Calgary reports 460 hearings avoided by citywide rezoning (S8), indicating process load from discretionary rezoning. No direct capacity study found `[unverified]`.
- Evidence against: dispersion reflects project mix; capacity is endogenous to growth.
- Likely identification strategy: panel with municipality fixed effects; staffing shocks; HAF/provincial funding.
- Expected difficulty: med. Novelty: high. Policy importance: med. Proposed class: D

### PLAN-5 — Appeals and discretionary rezoning create delay and veto risk
- Mechanism: third-party appeals and political hearings add time and option-value delay.
- Predicted effect: negative; magnitude unknown.
- Unit of analysis: application; project.
- Required variables: appeals filed, outcome, time to decision, units.
- Potential datasets: OLT caseload/annual reports (not retrieved), council minutes.
- Existing literature: Bill 23 dismissed most third-party appeals not already scheduled (before 25 Oct 2022) and gave OLT power to dismiss for undue delay; Bill 185 further restricted third-party appeals and rolled back Bill 109 fee refunds (S11). One commentary notes OLT does not publish third-party appeal statistics (S11). No unit-level estimate found.
- Evidence against: appeals may affect a small share of units; discretion also extracts public benefits.
- Likely identification strategy: survival analysis with policy shocks (Bills 108, 23, 185 as natural experiments).
- Expected difficulty: med–high (data). Novelty: med. Policy importance: med. Proposed class: D

### PLAN-6 — Land-supply boundaries (greenbelt, ALR, urban boundaries, geography) raise land prices
- Mechanism: restricted greenfield supply raises land values and diverts growth to infill.
- Predicted effect: positive on land prices; ambiguous on total supply.
- Unit of analysis: CMA; parcels near boundaries.
- Required variables: developable land inventory, boundary dates, land prices.
- Potential datasets: Greenbelt/Growth Plan GIS, ALR maps, assessment data.
- Existing literature: not retrieved `[unverified]`.
- Evidence against: large approved-but-unbuilt inventories (S5) imply land designation is not binding in the GTA near term; geography is fixed.
- Likely identification strategy: boundary RD; Greenbelt designation as event.
- Expected difficulty: high. Novelty: med. Policy importance: med–high. Proposed class: C

### PLAN-7 — Transit-oriented upzoning is limited by assembly and parcel fragmentation
- Mechanism: density near transit adds capacity only if parcels can be assembled and approved.
- Predicted effect: positive but gated by assembly costs.
- Unit of analysis: station area; parcel.
- Required variables: permitted vs built density, ownership fragmentation, transit service.
- Potential datasets: Ontario MTSA designations, BC TOA designations `[unverified]`, Toronto pipeline.
- Existing literature: none Canadian retrieved; Chicago evidence (S13) shows price capitalization without short-run construction.
- Evidence against: Canadian station-area high-rise activity is already strong in some markets `[unverified]`.
- Likely identification strategy: DiD/RD at station-area boundaries.
- Expected difficulty: med. Novelty: med. Policy importance: med. Proposed class: D

### PLAN-8 — Approved-but-unbuilt inventory: entitlement is not the binding constraint
- Mechanism: when approvals exceed starts, financing, presale thresholds, development charges and demand bind; further approval reform yields little supply.
- Predicted effect: ~zero marginal effect of entitlement reform on starts in high-inventory markets.
- Unit of analysis: CMA-quarter; project.
- Required variables: approved units, starts, presales, cancellations, DC levels.
- Potential datasets: Urbanation, CMHC, Toronto pipeline, CivicAction.
- Existing literature: CivicAction (via BNN Bloomberg): 481 active GTHA projects (Q2 2025) vs more than four times as many approved but on hold; 2,220 stalled projects / 1,218,626 units. Toronto approved an average of >29,700 units/yr (2017–21) vs ~16,000 built/yr; 258,397 approved units awaiting construction (mid-2024) (S5). Secondary reports: >20,000 GTA condo units cancelled/deferred 2024–25; CMHC cites DCs among barriers (S5). Association only.
- Evidence against: approvals are lumpy and some speculative; unbuilt inventory may itself reflect cost-infeasibility caused by regulatory charges (PLAN-9); "approved" differs from as-of-right.
- Likely identification strategy: approval-to-start conversion conditioned on pro forma feasibility; cross-market comparison across rate regimes.
- Expected difficulty: med. Novelty: med. Policy importance: high. Proposed class: B

### PLAN-9 — Fees, development charges and exactions are the effective regulatory burden
- Mechanism: per-unit levies raise feasibility thresholds; incidence on buyers, landowners or builders.
- Predicted effect: negative on marginal-project feasibility.
- Unit of analysis: municipality; project.
- Required variables: DC/CAC/parkland rates, project costs.
- Potential datasets: DC bylaws, BILD/CHBA, Fraser.
- Existing literature: Fraser per-home fee estimates (S3, developer-reported); MLURS includes fees (S6); incidence studies not found `[unverified]`.
- Evidence against: DCs fund enabling infrastructure; incidence may fall on land value.
- Likely identification strategy: DC rate changes (Bill 23 cuts) as DiD; bunching before rate changes. (Public-finance overlap.)
- Expected difficulty: med. Novelty: med. Policy importance: high. Proposed class: C

### PLAN-10 — Office-to-residential conversion adds supply, but small and subsidy-dependent
- Mechanism: underused offices convert at lower land cost, subject to floor-plate/code limits.
- Predicted effect: positive; small relative to national shortfall.
- Unit of analysis: building.
- Required variables: vacancy, floor plate, cost, incentive uptake.
- Potential datasets: Calgary program reports, broker vacancy data.
- Existing literature: Calgary Downtown program ($75/sq ft incentive) reported 21 approved projects, ~2.68M sq ft, ~2,628–2,667 homes (counts differ by source/date); ~$805M outside investment vs $198M city funds (S10). Program reopened mid-2026 with additional $25M (single source, `[unverified]`). Outside Calgary, only small projects found (e.g., a 23-unit conversion in London, ON) (S10).
- Evidence against: Calgary's ~2,600 homes are small against Canadian needs; subsidy cost; feasibility limited to a minority of buildings `[unverified]`.
- Likely identification strategy: building-level feasibility models; program take-up analysis.
- Expected difficulty: low–med. Novelty: med. Policy importance: low–med. Proposed class: D

### PLAN-11 — Housing-type mix, parking and code rules channel production into slow, capital-intensive forms
- Mechanism: parking minimums, code rules and approval structure favour a few project types, limiting small-builder missing-middle.
- Predicted effect: slower responsiveness to price signals; fewer entry-level types.
- Unit of analysis: CMA-year; builder.
- Required variables: starts by type, builder size, parking/code rules.
- Potential datasets: CMHC starts by type, municipal bylaws, Toronto monitoring.
- Existing literature: Toronto monitoring shows 32% of multiplex permits with zero parking (S9), implying parking is not universally binding when permitted; other claims `[unverified]`.
- Evidence against: construction cost/labour (construction specialist domain) and land economics may dominate.
- Likely identification strategy: DiD around parking-minimum removal and code changes.
- Expected difficulty: med. Novelty: high. Policy importance: med. Proposed class: E

### PLAN-12 — Federal incentive conditionality (HAF) induces local zoning change
- Mechanism: tying funds to zoning/process commitments changes municipal behaviour.
- Predicted effect: positive on permits where commitments are binding; unclear net of counterfactual.
- Unit of analysis: municipality-year.
- Required variables: HAF commitments, permits, baseline targets.
- Potential datasets: CMHC HAF progress reports; PBO.
- Existing literature: PBO: Large/Urban stream $4.1B, 113,817 anticipated units; CMHC total ~$4.37B across 230 agreements; 32 municipalities met/exceeded commitments; CMHC "750,000 permitted homes" figure is an expected 10-year estimate, not observed; PBO notes Toronto starts decline driven by economic conditions, so HAF effect not separable (S12).
- Evidence against: targets combine units expected without HAF with HAF-incentivized units (S12), so additionality is unmeasured.
- Likely identification strategy: DiD/synthetic control on HAF vs non-HAF comparable municipalities; staggered agreement dates.
- Expected difficulty: med. Novelty: high. Policy importance: high. Proposed class: D

---

## Key disagreements
1. Delay/stringency narrative (MLURS, BILD, Fraser) vs. unbuilt-pipeline evidence (S5) — may both hold in different market phases.
2. CMHC 2026 claims a causal regulation-price link (14% per 10%); its identification could not be verified, and the survey cross-section confounds demand.
3. Edmonton and Calgary: starts rose after reform but attribution unproven; Calgary reversed reform in 2026.

## Summary
- Claims (confidence):
  - GTA approval timelines vary 10–34 months with dispersion across municipalities (S1): medium.
  - MLURS ranks Greater Toronto/Vancouver most regulated; Approval Delay Index most explanatory of affordability differences (S6): medium (descriptive/association).
  - Large approved-unbuilt inventories exist in the GTHA (S5): medium.
  - Upzoning take-up exists (Toronto 452 permits May 2023–Nov 2024; Calgary 189 R-CG applications early) but causal supply effect unestablished (S8, S9): low.
  - Calgary repealed citywide rezoning in 2026 (S8): medium.
  - Office conversion in Calgary ~2,600 homes (S10): medium; small relative to need.
  - HAF effects not separable from macro conditions (S12): medium.
- Supporting evidence: S1–S13.
- Sources: listed above.
- Uncertainty: no Canadian quasi-experimental upzoning study found; many figures secondary; Greenbelt, TOD, OLT unit-level, Zemp results not retrieved.
- Assumptions: benchmarking samples are representative; news summaries reflect primary documents.
- Contradictions found: delay vs. unbuilt pipeline; CHBA 11.2 months vs BILD 20–24 months (different geography/method); Toronto multiplex permit counts differ (452 vs 2,629 by period/source).
- Recommended next investigations: (1) read the CMHC 2026 MLURS report and Zemp (2025) for identification; (2) obtain MLURS microdata/index; (3) parcel-level capacity-vs-built analysis; (4) application-level time-to-approval and appeal data (OLT); (5) BC SSMUH permit counts by municipality; (6) Greenbelt/ALR and TOD evidence; (7) verify S5 figures against primary sources.
