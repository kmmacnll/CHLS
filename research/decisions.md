# Decisions

Major research decisions and rejected approaches. Append-only; newest last. ID format `DEC-###`.

| ID | Date | Decision | Alternatives rejected | Rationale |
|----|------|----------|-----------------------|-----------|
| DEC-001 | 2026-11-14 | Adopt multi-agent STORM method per `research/charter.md`; Lead Agent synthesizes, specialists investigate independently. | Single-perspective investigation. | Owner instruction; reduces anchoring and confirmation bias. |
| DEC-002 | 2026-11-14 | Phase 1 run as 7 parallel independent specialist investigations with no leading hypothesis supplied; adversarial reviewer held back until a shortlist exists. | (a) Lead agent drafts hypotheses first then asks specialists to comment — rejected: anchors specialists. (b) Adversarial review in round 1 — rejected: nothing yet to attack. | Charter "Agent independence". |
| DEC-003 | 2026-11-14 | Domain specialists run on a lower-cost model; causal-inference specialist, adversarial reviewer, and all synthesis run on the top model at high effort. | Top model for all agents. | Charter "Cost control". |
| DEC-004 | 2026-11-14 | Phases 1–3 are literature/desk research only: no data downloads or modelling. Sandbox egress to statcan.gc.ca and cmhc-schl.gc.ca is blocked; sources verified via web search only. | Attempting ingestion now. | Charter forbids expensive modelling before Phase 3 approval; network access must be granted before Phase 4. |
