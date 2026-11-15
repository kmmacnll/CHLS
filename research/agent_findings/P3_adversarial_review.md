# P3 — Adversarial review of provisional choice C1 (tax-wedge elasticity, rental GST/HST rebate)

Date: 2026-11-15. 22 web searches, snippets only; no primary full text read. Tags: [V] = seen in a search result this session; [unverified] = memory or not confirmed; "arith." = my arithmetic on [V] inputs. P3_independent_ranking.md not read.

## 0. Verdict
**ADOPT WITH CHANGES.** No design-based evaluation exists and the data are open, but the design as framed cannot answer its own headline question ("net new supply or tenure shift"), and the claim that it yields the parameter governing $8.8B of DC cuts is not supportable. Reframe, demote, and pre-register (§4–5).

## 1. Fact check: is there usable cross-province variation?

| Prov. | Rule (status) | Consequence |
|---|---|---|
| ON | 100% of 8-pt provincial part, no cap, federal window; announced 1 Nov 2023 [V]. Pre-existing rebate 75% of provincial part, max $24,000/unit, still applies to non-qualifying projects [V] | **Incremental dose = 8%×FMV − $24k** (arith.): $16k on a $500k unit = 3.2% of value, not 8 points. The Minister's "$40,000 on a $500,000 unit" [V] is gross relief |
| NS, NL | 100% of provincial part, federal window (CRA) [V]. No prior provincial rental rebate known [unverified] | ~10-pt dose (NS 9 after HST cut 1 Apr 2025), in two CMAs (Halifax, St. John's) [CMA count unverified] |
| NB | 100% of 10 pts, construction begun from 15 Nov 2024 to end-2027; CRA and GNB dates differ [V] | Late switch-on; short window invites pull-forward |
| PEI | 100% of 10 pts **capped $35,000/unit**, start ≥14 Sep 2023, complete before 2029 [V] | No CMA [unverified]; tiny |
| QC | Declined; QST rebate stays 36% with unit-value limit <$225k [V] | Clean non-matcher; rental bears nearly full 9.975% QST |
| BC | No HST. "Removing PST from certain construction costs": one 2023 law-firm line, not confirmed. Real measures: property-transfer-tax exemptions for purpose-built rental (Jan 2024; Jan 2025–2030) [V] | Not "partial PST relief"; contaminated control |
| MB | Rental Housing Construction Tax Credit, up to $8,500/unit ($13,500 affordable), Budget 2024 [V] | Contaminated control |
| SK | Nothing confirmed. AB: no PST | Federal-only |

- Federal increment is itself heterogeneous: old 36% rebate phased out between $350k and $450k unit value [V] → increment 3.2 pts (cheap units) to 5 pts (arith.).
- Anticipation: 2015 Liberal pledge, abandoned; NDP call ~Mar 2023 [V]; no leak found before 14 Sep. **Matching intent was public within a day** (NAIOP, 15 Sep 2023, names ON, BC, NL) [V]. Information date ≈ 14 Sep everywhere; no staggered timing except NB.
- Shares by group: provincial rental-start counts **not retrieved** (gap). Qualitative [V]: TD (Jan 2026) starts at/above long-run average everywhere **except Ontario**; Quebec's purpose-built rental share of starts ~20% (2012) → ~90% (2025); Montréal >80% rental in 2025; record 2025 rental starts in Calgary, Edmonton, Montréal, Ottawa, Halifax. The rental boom is at least as strong in non-matching provinces.
- Unresolved: KPMG (Apr 2026) snippet says Ontario is "eliminating its HST rebate for new homes and new residential rental properties in 2027" [unverified, ambiguous]. Must be read before design freeze.

## 2. Objections

| # | Objection | Severity | Evidence / reasoning | Required fix |
|---|---|---|---|---|
| O1 | **Condo is not a control; it is the displaced unit.** If relief moves projects from condo to rental, rental−condo double-counts the shift. The DDD estimand = rental gain + condo loss. The "net new" question is then answered only by a province-level DiD on total starts, with no tenure differencing and 3 treated provinces | Serious (fatal for the headline as framed) | Logic. Urbanation: 61 projects / 27,320 units switched condo application to rental in 2025; 4,064 cancelled condo units converted 2024–Q1 2026 [V] | Report rental, condo, and total multi-unit effects separately; ground-oriented freehold as **placebo**, not control; state that additionality rests on the total-starts contrast and its inference |
| O2 | **Ontario-specific condo collapse** is a tenure×province×time shock unrelated to tax; it inflates rental−condo in Ontario and depresses Ontario total starts | Serious | GTHA condo starts −63% (2025), sales lowest since 1991, 28 projects cancelled [V]; BC condo construction "surprisingly resilient" (TD) [V] | Interact with pre-2022 presale-condo exposure (C2 arm); estimates with and without Toronto CMA; non-GTHA Ontario CMAs as separate arm |
| O3 | **Effectively one treated unit.** Treatment varies by province: ON (most treated CMAs), NS, NL; NB late; PEI capped | Serious | 10 provinces choose 3 = 120 assignments (arith.): randomization inference is valid but weak, and cannot remove Ontario-only shocks | Present as comparative case studies: synthetic control per treated province with placebo distribution; Conley–Taber-type intervals; leave-one-province-out |
| O4 | **Dose mis-stated and small where the data are.** Ontario increment ≈2–4% of value for $400–600k units; the 10-pt doses sit in two small CMAs; Quebec's untouched ~10-pt wedge coexists with a rental boom | Serious | §1 arith.; TD/CMHC on Quebec [V] | Build per-unit dose by province × value band; dose-response ordering test; power simulation on 2015–22 data before touching post-period outcomes |
| O5 | **Start-date mismatch.** CRA: construction begins at **excavation** (Notice 336) [V]; CMHC start = concrete poured for the full footings (CMHC 2017 wording) [V]. CMHC starts in late 2023–24 include ineligible pre-14-Sep excavations; eligible ones appear months later [gap length unverified] | Manageable–serious | Skyrise/UTPro (Jan 2025): Toronto rental share of starts tripled the quarter after announcement, back to pre-break level by end-2024 [V] — pattern fits retiming/relabelling, not a level shift. Eligibility uncertain: stalled-and-restarted projects (CBA–CRA roundtable 2025 Q9), CRA auditing and denying claims [V] | Quarterly event time; donut for Sep 2023–mid 2024; treat first year as transition; no bunching claims on CMHC dates |
| O6 | **Benefit arrives years after the start.** Under self-supply the tax falls due at substantial completion/first occupancy on fair market value [unverified this session]; rebate window runs to 2030 starts, so no deadline disciplines timing | Manageable | Reasoning | Interpret as effect of expected after-tax return; do not compare timing to DC payment at permit |
| O7 | **Endogenous tenure label.** Intended market is recorded at start; rebate and financing reward the rental label; "rental" may include student, seniors and non-market units [unverified] | Manageable | Urbanation conversions [V] | All-apartment starts as an outcome; rental share as mechanism only |
| O8 | **Federal effect unidentified; transport to DCs unjustified.** Tenure×time absorbs the 5-pt federal part, so "did the GST rebate add supply" is not answered. DCs differ in payer, timing (permit, or occupancy after Bill 17), tenure, permanence and benefit side (they fund servicing). Incidence: a null cannot separate "inelastic" from "capitalised into land" without land prices, which are not open | Serious for claimed value | P2_development_charges §4–5; logic | Drop the "$8.8B parameter" claim. Estimand: effect of provincial HST matching on rental and total multi-unit starts |
| O9 | Ottawa–Gatineau is one lumpy pair whose sign flips yearly | Manageable | Gatineau starts +33% (2024), −38% (Jan–Oct 2025), +66% (Jan–Apr 2026); Ottawa record 2025, −12% early 2026 [V] | Illustrative only |
| O10 | Data not yet confirmed at the needed grain | Manageable | SCSS monthly to census tract by intended market per `cmhc` package author [V]; history to 2015 and the Ontario/Quebec split of Ottawa–Gatineau not confirmed | Phase 4 gate: pull and audit before methodology is fixed |

### Tenure-specific × province-specific confounders (survive the triple difference)
| Confounder | Damage |
|---|---|
| MLI Select / ACLP: share of rental apartment starts supported rose ~5% (2017) → ~90% (2024) (TD) [V]; take-up by province not public [unverified] | **Serious.** Dominant rental-specific shock; any provincial tilt loads on the estimate. Cannot be separated without CMHC program data |
| Ontario rental DC discount 15/20/25% from 28 Nov 2022 [V]; Toronto rental DC discounts 40–60% and rental incentive stream (2026 staff reports) [V]; federal–Ontario DC programme from 30 Mar 2026 | **Serious.** Ontario- and rental-specific, starts 10 months pre-treatment |
| Ontario HST relief on new ownership homes, agreements 1 Apr 2026–31 Mar 2027 [V] | Treats the control tenure in the treated province. **End the post-window at Mar 2026** |
| Student cap / NPR cuts, hardest in ON, BC, NS (P2_demand_rental) | **Serious.** Rental-demand shock concentrated in treated provinces during the post-period; biases toward zero |
| Ontario post-2018 rent-control exemption | Manageable; time-invariant rule but its value moves with expected rents |
| NS HST cut (Apr 2025), rent cap [unverified]; BC PTT exemptions, BC Builds; QC lease/rent-setting changes [unverified]; MB credit | Manageable by exclusion (BC, MB) and dose recoding (NS) |
| Alberta: no PST, migration-driven rental record | Manageable; report with and without |

### Has it been done?
Three searches: no causal evaluation (CMHC, PBO, banks, C.D. Howe, academic). Found only PBO costing, descriptive Skyrise/UTPro, Urbanation, TD, CMHC, and unsupported claims ("sparked a wave"). Novelty holds; absence is search-limited.

## 3. Is another candidate stronger?
- On the project's order (validity > reproducibility > identification), C1's weakness is identification of its headline claim, not data.
- **C2 viability arm** (rate shock × pre-shock presale exposure) has ~35 CMA clusters and a continuous exposure, versus C1's three treated provinces, and it models the very shock (O2) that C1 must control. It is the stronger backbone.
- C4 has sharper dates and more clusters but a narrow estimand; C3 has the best internal validity but one city; C5, C6 remain worse.
- **Reformulation:** one CMA×quarter multi-unit starts panel, 2015–Mar 2026. Primary: viability/financing exposure (C2 arm). Pre-registered secondary: provincial HST-matching contrast, labelled a few-cluster comparative case study. Question: "What moved multi-unit starts in 2022–26 — financing viability or the tax wedge — and did provincial tax relief add units or relabel them?"

## 4. Required changes
1. Replace "wedge elasticity" with the estimand actually identified (provincial matching increment); remove the DC/HST transport claim.
2. Make C2's viability arm co-primary; C1 contrast secondary.
3. Recode treatment as per-unit dose; correct BC, PEI, MB, Ontario's prior $24k rebate; exclude BC and MB from clean controls.
4. Condo as outcome, not control; freehold as placebo.
5. Synthetic-control / leave-one-out inference; no cluster-robust standard errors on three treated provinces.
6. Post-window ends Mar 2026; first 12 months flagged as transition.
7. Power simulation and data audit before any post-period outcome is examined.
8. Verify from primary texts: CRA/provincial rules, Ontario 2027 change, CMHC start definition, self-supply timing.

## 5. Falsification criteria to pre-commit
- F1 Pre-trends: joint test on 2019–Aug 2023 leads rejects, or synthetic-control pre-fit exceeds a preset error → no causal claim.
- F2 Placebo tenure: freehold shows a similar "effect" → provincial shock, design fails.
- F3 Leave-one-out: result vanishes without Ontario, or without Toronto → reported as case study, no elasticity.
- F4 Dose ordering: NS/NL > ON > capped PEI, and NB breaks at Nov 2024, not Sep 2023. Wrong ordering → not a tax effect.
- F5 Placebo dates (Sep 2021, Sep 2022) and placebo provinces give the p-value; α fixed in advance.
- F6 Additionality claimed only if the total multi-unit effect excludes zero **and** the condo effect excludes full offset; otherwise "shift or undetermined".
- F7 If the simulated minimum detectable effect exceeds a pre-stated plausible effect, the module is declared uninformative; a null is not reported as "no effect".
- F8 If Quebec's rental starts rise as much as Ontario's without QST relief, record it as evidence against H40.

## Summary
- Claims (each with confidence):
  - The triple difference cannot separate net new supply from tenure shift, because the control tenure is the displaced one (high; logic).
  - Ontario's incremental provincial relief is ~2–4% of unit value, not 8 points, given the prior $24,000 rebate (med; arithmetic on snippet-level facts).
  - Usable variation is ON, NS, NL vs QC, AB, SK; BC and MB are contaminated; PEI capped; NB late (med-high).
  - Non-matching provinces, Quebec above all, show a rental boom at least as strong as Ontario's (med; qualitative, counts not retrieved).
  - CRA (excavation) and CMHC (footings) start definitions differ, blurring the event date (med-high).
  - MLI Select/ACLP, Ontario rental DC discounts, the Ontario condo collapse and the student cap are tenure×province confounders that survive the design (med-high).
  - No causal evaluation of the rebate exists (med; search-limited).
  - Transport of a rental-tax response to development charges is unjustified (med-high; reasoning).
- Supporting evidence: §1–2.
- Sources: canada.ca CRA PBRH rebate page, RC4231, Notice 336; gnb.ca hst-rebate-rental-housing; bdo.ca gst-relief-announced-for-new-residential-rental-properties; revenuquebec.ca rental rebate pages; cbc.ca 1.7014884 (Ontario); constructioncanada.net, atlantic.ctvnews.ca (PEI); gov.bc.ca purpose-built-rental-exemption; mltaikins.com (Manitoba credit); newswire.ca NAIOP 15 Sep 2023; ctvnews.ca 1.6561315; thor.ca ?p=6944; cba.org CRA–CBA roundtable 2025 Q9; mondaq 1714388; cmhc-schl.gc.ca survey methodology page and Housing Information Monthly Apr 2017; doodles.mountainmath.ca 2022-06-12; economics.td.com ca-regional-divide-in-homebuilding; storeys.com condo-rental-pivot-momentum-gta; toronto.skyrisecities.com 2025/01; osler.com ontarios-new-hst-rebate-key-details and Bill 23 update; assets.kpmg.com 2026/04; ctvnews.ca, obj.ca (Ottawa, Gatineau); toronto.ca backgroundfile-288661.
- Uncertainty: snippet-level only; provincial rental-start counts, MLI/ACLP take-up by province, CMA counts, NS/NL announcement dates, excavation-to-footing lag, self-supply timing and Ontario's 2027 change are unverified.
- Assumptions: Ontario's prior $24,000 rebate applied to typical rental units without a value phase-out; CMHC's 2017 start definition still holds.
- Contradictions found: brief's "8–10 point provincial increment" vs Ontario's ~2–4%; "BC partial PST relief" vs BC property-transfer-tax measures; PEI is capped but on the federal start date; "wedge is binding" vs Quebec's rental boom with no QST relief; Toronto's post-announcement rental spike faded within a year.
- Recommended next investigations: (1) pull CMHC starts by intended market, CMA×month, 2015–2026, and tabulate rental starts by province group; (2) read CRA Notice 336, RC4231, provincial regulations and the Ontario 2026 budget text; (3) request CMHC MLI Select/ACLP units by province and year; (4) power simulation on pre-2023 data; (5) confirm CMHC start definition and typical excavation-to-footing lag.
