# Phase 2-3 synthesis — audit, ranking, adversarial review

Lead agent, 2026-11-15. Inputs: `agent_findings/P2_*.md` (four cluster audits), `synthesis/P3_candidates.md`, `agent_findings/P3_independent_ranking.md`, `agent_findings/P3_adversarial_review.md`. Decision: `research/research_decision.md`.

## Phase 2 — what the audits changed

| Cluster | Audit verdict | Effect on ranking |
|---------|--------------|-------------------|
| Development charges | Retiming feasible; level effect not (≤8 months post, controls vanish after Mar 2026, Bill 17 changed payment timing); incidence not feasible without paid land data | Down: narrow estimand |
| Upzoning | Parcel DiD on permits feasible in Calgary/Edmonton; feasibility-vs-permission not identifiable; pre-reform parcel zoning unverified | Down: single-city, unverified treatment assignment |
| Demand / rental | Student-cap design weak (exposure ≈ province, concurrent completions and rate cuts); Ontario rent-control RD infeasible | Down |
| Pipeline / viability | "Which stage binds" not identifiable; descriptive hazards feasible; rental tax relief is the best-identified part | Up, reframed |

Discrepancies resolved: immigration rent elasticity (0.045 national; 0.086 large municipalities); productivity decline 37.3% (the 38.5 figure not found); CivicAction 1.2M units confirmed, project count not. Still open: HAF agreements 178/179; Calgary effective date 4/6 Aug 2024.

## Phase 3 — two independent analyses

Process: a neutral six-candidate brief was written. One top-model reviewer ranked candidates blind to the lead's preference. A second attacked the lead's provisional choice (C1). Neither read the other.

| Point | Independent ranking | Adversarial review |
|-------|--------------------|--------------------|
| Top candidates | C1 = C2 (29/40); C3 25; C5, C6 24; C4 23 | C1 adoptable only with changes; C2's viability arm the stronger backbone |
| Recommended form | C1′: rental-rebate provincial-dose DiD primary; Ontario ownership rebate, DC bunching, C2 hazards secondary | One CMA × quarter panel; financing exposure primary; tax matching a labelled few-cluster case study |
| Main objection to C1 | Power: large doses only in NS and NL; Ontario dose ~2-4 points | Condo is the displaced tenure, not a control; dose mis-stated; controls contaminated (BC, MB); cannot price DC cuts |
| Verdict | Proceed behind a three-part gate; fall back to C2 descriptive | Adopt with changes; eight falsification criteria |

### Consensus
- Viability questions (C1, C2) outrank C3-C6 under every weighting tried.
- C1 and C2 are complements and should share one panel.
- Ontario's incremental provincial relief is small because of its prior 75% / $24,000 rebate (unverified, both from memory or arithmetic on snippets).
- A pre-outcome gate (data audit, dose table from primary texts, power simulation) is required.
- No causal evaluation of the rental rebate was found.

### Disagreement (preserved)
- **Which arm is primary.** Independent: tax matching, because treatment is statutory and dated; rates the exposure arm's identification 2/5 (exposure correlated with city size, prices, immigration; flows are equilibrium outcomes). Adversarial: financing exposure, because ~35 clusters and continuous exposure beat three treated provinces, and the Ontario condo collapse must be modelled either way.
- **New Brunswick.** Listed as matching from mid-Nov 2024 by one source; the CRA guide lists only NL, NS, ON.

### Unresolved uncertainty
- CMHC intended-market series: history depth and Ontario/Quebec split of Ottawa-Gatineau.
- Provincial rules for BC, PEI, NB; a possible Ontario change in 2027.
- MLI Select / ACLP take-up by province (not public).
- Excavation-to-footing lag between CRA and CMHC start definitions.

### Lead-agent resolution
- The provisional framing ("tax-wedge elasticity", tenure triple difference, relevance to $8.8B of DC cuts) is withdrawn. The adversarial objections O1, O4 and O8 are accepted.
- Selected: the merged viability question, financing-exposure arm primary, tax-matching arm secondary case study, pipeline hazards as descriptive baseline. Reason for ordering: power and cluster count; the tax arm has a low chance of being informative on its own.
- Neither arm is strongly identified. The study is designed so that a failed gate yields an honest descriptive result rather than a forced causal claim.

## Lead ranking after review (1-5 per charter criterion)

| Candidate | Policy | Testable | Data | Novelty | Causal ID | ML | Scalable | Actionable | Total |
|-----------|--------|----------|------|---------|-----------|----|----------|------------|-------|
| **S\* merged viability question (selected)** | 5 | 4 | 4 | 4 | 3 | 3 | 5 | 4 | **32** |
| C2 pipeline stages (descriptive) | 5 | 3 | 3 | 4 | 2 | 4 | 5 | 3 | 29 |
| C1 tax wedge alone | 4 | 3 | 4 | 4 | 2 | 2 | 4 | 3 | 26 |
| C3 upzoning on/off | 5 | 3 | 2 | 4 | 3 | 3 | 2 | 3 | 25 |
| C5 student cap | 3 | 3 | 3 | 4 | 2 | 2 | 4 | 3 | 24 |
| C6 HAF | 4 | 2 | 3 | 4 | 2 | 2 | 4 | 3 | 24 |
| C4 DC retiming | 4 | 3 | 2 | 4 | 3 | 2 | 2 | 3 | 23 |

Scores carry roughly ±1 error. No candidate scores above 3 on causal identification: with open data, Canadian supply-side questions are at best moderately identified.

## Hypothesis updates from Phases 2-3

| ID | Update |
|----|--------|
| H01 | National rent elasticity 0.045, value 0.143; 0.086 is the large-municipality subsample. No NPR-specific estimate exists. |
| H02 | Dose-response unproven: near-campus Toronto rents rose while city fell. Exposure ≈ province. |
| H15, H16 | Calgary counts inflated by reclassification of rezonings as development permits. Edmonton reversion order (Oct 2026) adds a live anticipation test. |
| H17 | Unbuilt-inventory figures (144k / 297k / 1.2M) count different stages; not comparable. |
| H26-H28 | Level effect and incidence not identifiable on open data; retiming is. Bill 17 (2025) moved DC payment timing. |
| H36 | Record construction employment (2023) with weak starts is evidence against labour binding in 2023. |
| H37 | 37.3% decline confirmed at summary level. |
| H40 | Ontario incremental dose ~2-4% of unit value; Quebec rental boom without matching relief is evidence against a strong tax-wedge effect. |
| H42 | RD on first-occupancy date infeasible on open data. |
| H43 | CMHC 2026 filtering study exists (Calgary nearby rents −2-3%); class moves from D toward B. |
