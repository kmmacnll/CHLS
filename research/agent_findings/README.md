# Agent Findings — Protocol

One file per investigation: `P<phase>_<role>_<topic>.md`. Files are append-only records; never overwrite another agent's file.

## Rules for every specialist agent

1. **Never fabricate** data, sources, statistics, quotes, or findings. Every empirical claim needs a source (paper, government publication, dataset) with URL.
2. Verify sources by web search in this session. Anything recalled from memory but not confirmed is tagged `[unverified]`. Numbers without a confirmed source are not allowed.
3. Distinguish **prediction / association / causal effect**. State the identification strategy behind any causal estimate you cite.
4. Prefer Canadian evidence; use international evidence where it supplies variation Canada lacks.
5. Record evidence **against** each claim as carefully as evidence for it. Do not assume any hypothesis is correct.
6. Independence: do not read other agents' files unless your brief says so.
7. Concise research-log style. No preamble, no conversational filler. Hard cap in brief.
8. Write only your assigned file. Do not commit, push, or edit other files.
9. Tools: use WebSearch (load via ToolSearch `select:WebSearch` if needed). Direct HTTP (curl/WebFetch) to most hosts is blocked by the sandbox proxy; do not spend time on it.

## Hypothesis record (Phase 1)

```
### <ROLE-PREFIX>-<n> — Short title
- Mechanism:
- Predicted effect (sign, rough magnitude if literature supports one):
- Unit of analysis:
- Required variables:
- Potential datasets:
- Existing literature (citations + URLs; key estimates):
- Evidence against / competing explanations:
- Likely identification strategy:
- Expected difficulty (low/med/high + why):
- Novelty (low/med/high + why):
- Policy importance (low/med/high + why):
- Proposed class: A well established | B partially understood | C contested | D under-researched | E potentially novel
```

## Investigation record (all phases) — end every file with

```
## Summary
- Claims (each with confidence: high/med/low):
- Supporting evidence:
- Sources:
- Uncertainty:
- Assumptions:
- Contradictions found:
- Recommended next investigations:
```
