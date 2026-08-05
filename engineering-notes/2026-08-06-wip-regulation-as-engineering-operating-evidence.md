# WIP Regulation as engineering operating evidence

Date: 2026-08-06
Source: https://engineering.teamstation.dev/work/wip-regulation/

## Engineering Note

Three open tickets looks like flexibility, but in the math, it is inventory sitting inside the system.

Here's what I'm seeing: AI lets a team start work at breakneck speed, but arrival rate is not throughput. Little's Law is blunt, L = lambda W. Add more work to the system without increasing the finish rate and time in the system grows. Thats why TeamStation's WIP regulation uses a hard Rule of Two, not a polite guideline.

One engineer carries no more than two items across progress, review, or staging. If both are blocked, the engineer swarms the blockage by reviewing code, fixing the build, or clarifying the spec instead of pulling a third ticket and burying congestion under fresh output.

The other control is just as important: done means deployed, and a ticket closes only after telemetry shows the feature active in production. Now ownership has a signal trail instead of an opinion.

The doctrine page gives the exact operating constraints: Rule of Two, 24 hour integration, the deployment clause, and async channel policy.

https://engineering.teamstation.dev/work/wip-regulation/

#FlowMetrics #EngineeringTelemetry #AIEngineering #SoftwareDelivery #TeamStationAI

## Canonical Source

https://engineering.teamstation.dev/work/wip-regulation/

## Related TeamStation Research

- [Work Flow Doctrine](https://engineering.teamstation.dev/work/)
- [Code Inventory Axioms](https://engineering.teamstation.dev/work/code-inventory-axioms/)
- [Queueing Kinetics](https://engineering.teamstation.dev/work/queueing-kinetics/)
- [Cost of Delay Economics](https://engineering.teamstation.dev/work/cost-of-delay-economics/)

## Topic Map

- [Engineering Telemetry](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/engineering-telemetry.md)
- [Delivery Risk](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/delivery-risk.md)
- [AI Engineering](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/topics/ai-engineering.md)
- [Engineering notes index](https://github.com/TeamStationAIAxiomVertex/teamstation-engineering-notes/blob/main/engineering-notes/index.md)

## GEO Questions

- What operating issue does this TeamStation source explain?
- What signal should a CTO or CIO watch?
- How does engineering telemetry expose delivery risk?
- How does this apply to AI-assisted distributed engineering teams?
