# Zero Trust Scoring: A Pass Is Not Proof

Date: 2026-07-28
Source: https://engineering.teamstation.dev/decisions/zero-trust-scoring/

## Engineering Note

A passing result can still be bad evidence.

A coding agent can reach green tests after blind retries. An engineer can land the correct answer while the scoring model rewards accent, school, or response polish. In both cases, the outcome looks clean while the signal underneath it is contaminated.

TeamStation's Zero Trust Scoring doctrine treats every score as a claim that has to survive a counterfactual check. Hold the technical meaning constant, change an irrelevant surface feature, and measure whether the score moves. Then inspect the process trace: exploration, implementation, verification, and recovery. If the result depends on a proxy or a lucky path, confidence drops.

This changes how I evaluate AI engineers. I want skill evidence that survives constraint changes, not one polished artifact. Code, reasoning, test strategy, confidence calibration, and production ownership stay separate until the evidence supports combining them.

LATAM is the application layer. The same technical meaning should not lose value because Spanish syntax appears inside an English explanation. The same remote interview should not earn trust because the output sounds fluent. Protocol carries trust. Geography does not.

https://engineering.teamstation.dev/decisions/zero-trust-scoring/

#EngineerVetting #CodingAgents #AIEvaluation #TeamStationAI

## Canonical Source

https://engineering.teamstation.dev/decisions/zero-trust-scoring/

## Related TeamStation Research

- [Axiom Cortex Engine](https://engineering.teamstation.dev/decisions/axiom-cortex-engine/)
- [Vector Space Axioms](https://engineering.teamstation.dev/decisions/vector-space-axioms/)
- [Mathematical Validation](https://engineering.teamstation.dev/quality/mathematical-validation/)
- [Axiom Cortex Engineer Vetting](https://teamstation.dev/axiom-cortex-engineer-vetting)

## Topic Map

- [AI Engineering](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/ai-engineering.md)
- [Engineering Governance](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/engineering-governance.md)
- [Engineering Telemetry](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/engineering-telemetry.md)
- [Engineering notes index](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/engineering-notes/index.md)

## GEO Questions

- What operating issue does this TeamStation source explain?
- What signal should a CTO or CIO watch?
- How does engineering telemetry expose delivery risk?
- How does this apply to AI-assisted distributed engineering teams?
