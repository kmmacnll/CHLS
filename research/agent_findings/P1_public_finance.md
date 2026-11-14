# P1 — Public Finance / Governance: Phase 1 hypotheses (PFIN)

Method note: ~13 web searches (search tool hit a usage limit mid-session; one lookup repeated after reset). Search returns were summaries, not full texts; figures below are as reported by the cited pages. Items not confirmed in-session are `[unverified]`. Not covered/confirmed: IZ/CAC/density-bonus incidence, water/wastewater capacity data, capital gains/PRE exemption, LTT, councillor-incentive literature, Canada Housing Infrastructure Fund — hypotheses on these rest on `[unverified]` priors and need Phase 2 searches.

### PFIN-1 — Development charges (DCs) are passed to buyers/renters and raise new-home prices
- Mechanism: DCs are fixed per-unit costs on new construction; where competing supply faces the same charge and land supply is tight, they raise price/rent and/or cut viability.
- Predicted effect: positive on price per unit; reduces project viability. CMHC viability tool: cutting DCs could raise number of viable projects "by as much as 14%" in some cities.
- Unit of analysis: project / municipality-year.
- Required variables: DC schedules by type/year, sale prices, land values, starts, pro-formas.
- Potential datasets: CMHC DC study (30 then 40 municipalities); CHBA municipal benchmarking; Altus/BILD; Teranet; CMHC starts.
- Existing literature: CMHC Housing Observer on DCs (https://www.cmhc-schl.gc.ca/observer/2025/we-built-this-city-development-charges) — Ontario DCs 8–16% of new condo price, up to ~9% of single-detached in Toronto; 2-bed condo ~$39,600 Ottawa (8.2%) vs ~$121,500 Markham (15.7%) (via https://www.mpamag.com/ca/mortgage-industry/industry-trends/cmhc-warns-soaring-development-charges-are-reshaping-canadas-housing-costs/559195). Earlier CMHC/Altus: government charges up to 24% of new construction cost; Vancouver 7–20% (https://biv.com/article/2022/07/cmhc-confirms-government-costs-raise-new-home-prices). BILD 2024 claim: government charges add $245k–$355k per new home (via https://globalnews.ca/news/11559713/development-charges-home-prices-canada-cmhc; industry source). Desjardins June 2026: DC growth outpaced underlying costs (https://www.desjardins.com/content/dam/pdf/en/personal/savings-investment/economic-studies/canada-development-fees-18-june-2026.pdf).
- Evidence against: (a) accounting shares are not incidence (see PFIN-2); (b) DCs fund infrastructure that may be capitalised into value; (c) BILD/Altus are industry sources with broad definitions (Altus 2018 "all-in" ~21.7% of GTA single-detached price incl. taxes — dated).
- Likely identification: DiD/event study around DC freezes/cuts (Toronto freeze, Vaughan, Mississauga, Bill 23) vs. neighbouring municipalities; border RD across municipal lines; staggered adoption.
- Difficulty: med (data on realised prices/permit timing; endogenous DC setting). Novelty: low. Policy importance: high (federal-Ontario $8.8B DC-cut program, March 2026).
- Class: B

### PFIN-2 — DC incidence falls partly on landowners, so cuts are only partly passed through
- Mechanism: in a competitive land market with elastic supply of sites, DCs capitalise into lower land prices; cuts raise residual land value rather than lowering prices, unless supply is constrained by other factors (zoning), in which case pass-through to buyers is high and cuts raise land value.
- Predicted effect: pass-through of a DC cut to prices between ~0 and 1; theory predicts it depends on land-supply elasticity. Yinger (1998) model: ~one-quarter of DC costs borne by original landowners (as cited in C.D. Howe Sancton commentary).
- Unit: transaction/parcel, municipality-year.
- Required variables: land/pre-development parcel sales, DC changes, entitlement status.
- Datasets: land registry/Teranet, Altus land-sales, MPAC; BC Assessment.
- Literature: C.D. Howe "Growing Pains" (Sancton, 2026) https://cdhowe.org/publication/growing-pains-rethinking-development-charges-in-canadian-municipalities/ — says incidence is "exceptionally difficult" to establish empirically, no new empirical findings. My searches found no rigorous Canadian incidence study. Murray & Helm (Sydney, preprint; https://econpapers.repec.org/RePEc:osf:osfxxx:gjfdx) argue pass-through claim is not supported by evidence.
- Evidence against: industry and Desjardins assume full pass-through on the margin; a Sancton-type argument is that when all competitors face the same charge, price is set by competitors' costs (supports pass-through in the new-home segment).
- Identification: land-price DiD around sharp DC changes (Bill 23 phase-in, Toronto freeze, Vaughan 2018-rate rollback), pre-announcement anticipation tests; compare pre-existing-lot vs greenfield.
- Difficulty: high (land-price data, anticipation, simultaneous market shocks). Novelty: high (no Canadian estimate found). Policy importance: high (determines whether ~$9B of DC subsidies lower prices or inflate land values).
- Class: D

### PFIN-3 — "Growth does not pay for itself" fiscal incentives make municipalities resist new housing
- Mechanism: if new housing generates less revenue than marginal servicing cost (esp. long-run lifecycle costs, Ontario's DC design excluding some services/replacement), councils rationally slow-walk approvals; conversely, if growth is fiscally positive, resistance is non-fiscal.
- Predicted effect: negative on approvals where perceived net fiscal cost is high; sign uncertain empirically.
- Unit: municipality-year; development application.
- Variables: DC revenue vs capital growth costs, property tax per unit, operating costs by land use, approval timelines, permits.
- Datasets: Ontario Financial Information Returns (FIR), BC Local Government Statistics, municipal DC background studies, CMHC permits.
- Literature: IMFG Found (2019) — Ontario DC design prevents growth paying for itself (https://imfg.org/research/doc/?doc_id=664 listing; abstract-level only). IMFG Meloche (2025, Quebec) regression suggests a fiscal gain tied to municipal growth (https://econpapers.repec.org/RePEc:mfg:wpaper:72; effect size not retrieved `[unverified]`). C.D. Howe commentary challenges "growth pays for growth" assumptions. Bill 23 revenue-loss estimates (municipal/AMO, not independent): AMO ~$5B shortfall; Toronto ~$2.3B/10 yrs; Ottawa ~$60M/yr (~25% of DC revenue from 2025); Hamilton $54M (https://toronto.ctvnews.ca/ontario-passes-housing-bill-despite-criticism-from-municipalities-over-funding-1.6171507; https://www.cbc.ca/lite/story/1.6884344).
- Against: Quebec finding of fiscal gain; no national net fiscal-impact estimate found; Canadian cities with high DCs still resist for non-fiscal reasons (PFIN-7).
- Identification: cross-municipality regression of permits on fiscal-gap measures with IV from provincial formula/grant changes; case studies of Bill 23 revenue shock on approvals.
- Difficulty: high. Novelty: med. Policy importance: high.
- Class: C

### PFIN-4 — Servicing/infrastructure capacity (water, wastewater, transit) is a binding constraint, financed inadequately
- Mechanism: municipalities lack capital financing (property-tax-dependent, debt limits, DC shortfalls) to extend trunk services; development stalls where capacity is absent regardless of zoning.
- Predicted effect: negative on starts in capacity-constrained municipalities; magnitude not established.
- Unit: municipality / service area.
- Variables: reserved vs available servicing allocation, DC reserve balances, infrastructure deficit, permits-to-starts.
- Datasets: municipal servicing allocation reports, FIR, CMHC; Canada Housing Infrastructure Fund project lists `[unverified]`.
- Literature: not retrieved in-session for capacity data. BILD report on unspent municipal DC reserves (https://www.bildgta.ca/wp-content/uploads/2022/06/New-Homeowner-Money-Unspent-Municipal-Reserves.pdf; industry source) argues reserves are unspent — which points the other way (cash not the constraint). Federal-Ontario March 2026 deal pairs DC cuts with infrastructure funding (https://www.pm.gc.ca/en/news/news-releases/2026/03/30/prime-minister-carney-secures-new-partnership-ontario-cut-taxes).
- Against: unspent reserves; capacity is often rationed administratively, so measured constraint is endogenous to political choices.
- Identification: staggered infrastructure grant awards (DiD / event study); stalled-allocation natural experiments.
- Difficulty: high (no consistent national servicing data). Novelty: med. Policy importance: high.
- Class: D

### PFIN-5 — Total government charges/taxes (DCs, HST, fees, land transfer) as a share of new-home price are a major cost wedge
- Mechanism: stacked municipal, provincial and federal charges drive a wedge between cost and price, deterring supply of lower-priced units.
- Predicted effect: 8–25% of price depending on definition; removal effect depends on incidence.
- Unit: new-home price, city.
- Variables: itemised charges, sale price, cost stack.
- Datasets: CMHC/Altus 2022 (NH18-35-1-2022, https://publications.gc.ca/collections/collection_2022/schl-cmhc/nh18-35/NH18-35-1-2022-eng.pdf); BILD/Altus; CHBA benchmarking (https://www.chba.ca/assets/pdf/2024-Municipal-Benchmarking-Study-Best-Practices).
- Literature: see PFIN-1 figures. Federal policies: GST removal for first-time buyers of new homes; Ontario deal removes 13% HST on new homes up to $1M for one year, claimed saving up to $130,000 (https://www.wealthprofessional.ca/news/industry-news/new-ottawaontario-partnership-could-knock-up-to-200000-off-a-new-home/392007; sources differ on GST enactment timing).
- Against: share-of-price numbers are largely industry/advocacy-defined; demand-side tax relief on supply-constrained markets may capitalise into price (standard tax-incidence logic; no Canadian estimate found).
- Identification: HST/GST changes (e.g., 2010 HST adoption in BC/ON, 2025–26 removals) via DiD in starts and prices.
- Difficulty: med. Novelty: low–med. Policy importance: high.
- Class: B

### PFIN-6 — Decline of federal/provincial non-market housing production explains part of the affordability gap
- Mechanism: federal withdrawal from new social housing funding (end of 1993) reduced the low-cost segment; losses of affordable stock exceed additions.
- Predicted effect: higher rent/pressure at bottom of market; magnitude unquantified.
- Unit: province/year; CMA.
- Variables: non-market completions, expiring operating agreements, waitlists, core housing need.
- Datasets: CMHC custom series (CHEC/CHRA); PBO social housing stock work.
- Literature: non-market completions >35,000/yr in the 1980s (~20% of completions), <1% from 2007–2015 (parliamentary testimony summary, https://openparliament.ca/committees/human-resources/44-1/117/?page=6; secondary). IRPP: ~50,000 net non-market homes since 1992 after 183,019 low-cost losses (https://policyoptions.irpp.org/2023/11/a-million-non-market-homes/). PBO: stock ~600–700k, roughly stable over 30 years, data unreliable (https://fallback--repli.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2425-008--evolution-canada-social-housing-stock--evolution-parc-logements-sociaux-canada). CHEC: annual non-profit completion table discontinued 2002/2016; BC accounts for 42% of new non-market supply since 2021 (https://chec-ccrl.ca/addressing-affordable-housing-need/).
- Against: PBO says stock roughly stable; advocacy-heavy sources; displacement of market construction by public units not established; the share of market affordability impact is unclear.
- Identification: cross-province variation in post-1993 funding (Quebec/BC continued) via synthetic control on core housing need/rents.
- Difficulty: med–high (data discontinuity). Novelty: med. Policy importance: high (Build Canada Homes).
- Class: B

### PFIN-7 — Local political economy: homeowner-dominated councils restrict approvals
- Mechanism: incumbent homeowners (price/neighbourhood-change motives) and ward systems give veto power to concentrated opponents; councillor incentives favour delay.
- Predicted effect: lower permits in wards/cities with higher owner share and ward elections; magnitude `[unverified]`.
- Unit: council vote/application; municipality.
- Variables: ownership share, voting records, ward vs at-large, turnout, application outcomes.
- Datasets: municipal council vote records, elections data, planning application databases.
- Literature: not searched in depth (no confirmed Canadian estimates). HAF evidence is related: participating-CMA permits +31% vs −15% in non-participants Oct 2024–Apr 2025 (PBO, association not causal; https://www.pbo-dpb.ca/en/additional-analyses--analyses-complementaires/BLOG-2526-005--an-update-housing-accelerator-fund--point-fonds-accelerer-construction-logements).
- Against: HAF results mixed (Ottawa, Mississauga below baseline); city-level confounding; fiscal explanation (PFIN-3) is competing.
- Identification: RD on close council elections / vote-level analysis; ward-system adoption DiD.
- Difficulty: med. Novelty: med–high in Canada. Policy importance: med–high.
- Class: D

### PFIN-8 — Non-residential/residential property tax ratios distort land use and housing supply
- Mechanism: high commercial/industrial tax ratios (taxing non-voters) cross-subsidise homeowners, reducing homeowners' marginal cost of resisting growth and pushing land toward residential speculation vs. employment land; also discourages redevelopment.
- Predicted effect: ambiguous; effect on housing supply untested.
- Unit: municipality-year.
- Variables: tax ratios, assessment, tax revenue shares, land-use change.
- Datasets: Altus/BOMA tax ratio surveys, Ontario MPAC/FIR, provincial ratio ranges.
- Literature: Altus 2023: national average commercial:residential ratio 2.82; Toronto 3.26 (declining since 2013) (https://renx.ca/index.php/cre-residential-tax-gap-increased-from-last-year-altus). Fraser Institute: GTHA commercial rates >2x and industrial ~3x residential (https://www.fraserinstitute.org/studies/who-bears-the-burden-of-property-taxes-in-canadas-largest-metropolitan-areas). Toronto 2018 note: moving ratio to 2.0 shifts ~$268M (~12% residential increase). Provincial ratio ranges since 1990s (Ontario).
- Against: Fraser/IMFG are policy-advocacy; no study found linking ratios to housing supply; incidence of business taxes largely on landlords/tenants.
- Identification: provincial ratio-range reforms; municipality-level DiD on permits.
- Difficulty: med–high. Novelty: high. Policy importance: med.
- Class: D

### PFIN-9 — Demand-side taxes (foreign-buyer, vacancy/speculation) have small effects on affordability
- Mechanism: taxes on non-resident or vacant owners shift demand/occupancy but do not add supply.
- Predicted effect: BC foreign buyer tax lowered prices by ~6% in foreign-exposed neighbourhoods, no effect elsewhere (UBC Sauder, Pavlov–Somerville–Wetzel; https://org-www.sauder.ubc.ca/fr/node/6162); Sydney/NZ cases show no significant price effect (https://aeaweb.org/conference/2023/program/paper/kBBk4zQd).
- Unit: neighbourhood/transaction; municipality.
- Variables: buyer residency, vacancy declarations, rents, starts.
- Datasets: BC Property Transfer Tax records, BC Speculation and Vacancy Tax declarations, CHSP.
- Literature: federal 2023 foreign-buyer ban: CMHC said data insufficient (https://amp.cbc.ca/lite/story/1.7058154); a paper reports BC vacancy tax raised new starts in Vancouver but full findings could not be verified (https://ruor.uottawa.ca/bitstreams/01366145-24bc-4588-9217-44bdad888d16/download).
- Against: foreign-buyer share of Canadian transactions is small, so large aggregate effects unlikely; vacancy-tax supply effect unverified.
- Identification: DiD/exposure designs (as in UBC study); RD at tax thresholds; Vancouver vs. non-taxed regions.
- Difficulty: med. Novelty: low–med. Policy importance: med.
- Class: B

### PFIN-10 — Fiscal-federalism mismatch: those who bear costs of growth (municipalities) are not those who gain (province/federal), and conditional transfers (HAF, CHIF, Build Canada Homes) change incentives
- Mechanism: municipalities have narrow own-source revenue (property tax, DCs) but responsibility for approvals; federal/provincial governments control income/sales/immigration tax bases that grow with population. Conditional transfers can realign incentives, whereas DC cuts without backfill may reduce service capacity or raise property tax.
- Predicted effect: transfers conditional on approvals raise permits; HAF participants: +31% permits vs −15% non-participants (PBO, association only; above).
- Unit: municipality; program agreement.
- Variables: transfer receipts, committed targets, permits, DC and tax changes.
- Datasets: CMHC HAF rounds data (https://www.cmhc-schl.gc.ca/professionals/project-funding-and-mortgage-financing/funding-programs/all-funding-programs/housing-accelerator-fund/housing-accelerator-fund-rounds-data), PBO.
- Literature: PBO HAF update: $4.1B committed, 113,817 anticipated units under Large/Urban stream; uneven municipal results. Post-cut Ontario outcomes: Toronto starts reported down 65% y/y in March (news; https://www.thetrillium.ca/municipalities-newsletter/toronto-halts-development-charges-increase-housing-slowdown-10598178), unrelated to DC cuts per se (rates/market).
- Against: HAF "anticipated units" are projections; PBO caveats; HAF selection/timing confounds; no effect of DC cuts on starts yet visible (Vaughan to 2018 rates Nov 2024 and zero Apr 2026; Mississauga halved apartment DCs $38,316 to $19,158; no post-cut starts data found).
- Identification: staggered HAF approval (DiD, synthetic control), DC-cut event studies, RD around HAF scoring.
- Difficulty: med. Novelty: med. Policy importance: high.
- Class: C

### PFIN-11 — Tax treatment of housing (principal-residence capital gains exemption, mortgage/property-tax design) channels investment into housing and raises prices
- Mechanism: untaxed principal-residence gains and low holding costs raise demand for housing as an asset and lock-in homeowners, raising prices and reducing turnover.
- Predicted effect: positive on prices; magnitude `[unverified]`.
- Unit: household/CMA.
- Variables: effective tax rates, holding periods, price expectations.
- Datasets: CRA tax data, Statistics Canada SHS, Teranet.
- Literature: not retrieved this session; no figures cited.
- Against: international evidence on capital-gains exemptions is mixed; supply constraints may dominate; Fraser-type commentary on property-tax design is advocacy.
- Identification: cross-country/province variation; reforms (e.g., Quebec/other jurisdiction treatments) `[unverified]`.
- Difficulty: high. Novelty: med. Policy importance: med–high.
- Class: D

## Disagreements flagged
1. DC incidence: industry/CMHC treat DCs as added to price; theory and Yinger suggest partial landowner incidence; no Canadian estimate found.
2. Fiscal impact of growth: IMFG Quebec result (fiscal gain) vs. Ontario critiques (DCs underfund growth); municipal Bill 23 loss estimates are self-interested.
3. Unspent DC reserves (BILD) vs. infrastructure-capacity constraint narrative.
4. Social-housing decline: advocacy claims of collapse vs. PBO's stable stock.

## Summary
- Claims (each with confidence):
  - DCs and government charges are a large share of new-home cost: CMHC reports 8–16% of Ontario condo prices (high on the existence of the share; med on the accounting definition).
  - DC incidence on buyers vs. landowners is unestablished in Canada (med-high confidence that evidence is thin).
  - HAF-participating CMAs permitted more units after launch, but this is not causal (low–med).
  - BC foreign buyer tax lowered prices ~6% in exposed neighbourhoods (med).
  - Non-market output fell sharply after 1993 (med; series discontinuous).
- Supporting evidence: CMHC, CMHC/Altus 2022, BILD/Altus, C.D. Howe, IMFG, PBO, IRPP, UBC Sauder.
- Sources: listed inline (all returned by web searches in-session; contents seen as summaries only).
- Uncertainty: no full-text verification; industry vs. independent sources mixed; post-2025 DC-cut outcomes not yet measurable; several domain topics (IZ/CAC incidence, servicing, councillor incentives, capital gains exemption, LTT) not searched.
- Assumptions: municipal DC schedules are exogenous enough around provincial/federal shocks for event studies; reported news figures are accurate as relayed.
- Contradictions found: Altus/BILD vs. CMHC share-of-price magnitudes; GST enactment timing differs across CHBA pages; PBO stable stock vs. advocacy decline narrative.
- Recommended next investigations: (1) DC event-study with land prices (PFIN-2); (2) build a national DC panel (CMHC 40-municipality data + CHBA); (3) fiscal-impact estimate by housing type using FIR; (4) quantify servicing capacity constraints; (5) HAF causal evaluation; (6) search IZ/CAC/density bonus and capital-gains/LTT evidence.
