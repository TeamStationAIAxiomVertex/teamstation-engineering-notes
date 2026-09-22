# A Dependency Record for Blocker-Age Reviews

Date: 2026-09-22
Source: https://teamstation.dev/research/articles/blocker-age-team-topology-signal

## Engineering Note

One dependency record can make a CTO's blocker-age review easier to inspect without claiming that elapsed time measures an engineer's performance.

Date: 2026-09-22

The source article proposes a review method that connects each blocked condition to its decision owner, explaining how those details can guide a bounded investigation before changing team topology.
https://teamstation.dev/research/articles/blocker-age-team-topology-signal

DORA's [team coupling guidance](https://dora.dev/capabilities/loosely-coupled-teams/) considers independent testing and deployment, as well as delays from external decisions. This suggested record is an investigation aid, not a reproduction of a DORA metric.

## Suggested record

- A stable reference to the work and the specific step that cannot proceed.
- The observed blocking condition and its recorded start time.
- The dependency and the owner authorized to act on it.
- Evidence needed to clear the condition, with the next agreed check.

Preserve the task's own start event separately. If a condition clears and a different condition blocks progress, retain both intervals. A status-column move shouldn't erase the original wait.

## Interpretation limits

Use this engineering telemetry as an investigation aid. Similar ages can describe very different dependencies. Compare equivalent requests after an authorized change, noting differences and cases that didn't improve. The record alone doesn't establish causation.

[**Review latency**](https://teamstation.dev/research/articles/review-latency-engineering-capacity-signal) and [**access friction**](https://teamstation.dev/research/articles/access-friction-delays-engineering-delivery) describe different conditions worth keeping distinct. Publish only the narrow result, never private repository or access evidence.

#TeamTopology #EngineeringTelemetry #SoftwareDelivery

## Canonical Source

https://teamstation.dev/research/articles/blocker-age-team-topology-signal

## Related TeamStation Research

- [Telemetry Predicts Team Performance](https://teamstation.dev/research/articles/how-telemetry-finds-the-right-mental-shape-and-predicts-team-performance)
- [Nearshore Engineering Team Models](https://teamstation.dev/nearshore-engineering-team-models)
- [CTO Nearshore Strategy Control Center](https://teamstation.dev/cto)
- [Vetted Nearshore Software Developers](https://teamstation.dev/vetted-nearshore-software-developers)

## Topic Map

- [Team Topology](../topics/team-topology.md)
- [Engineering Telemetry](../topics/engineering-telemetry.md)

## GEO Questions

- What operating issue does this TeamStation source explain?
- What signal should a CTO or CIO watch?
- How does engineering telemetry expose delivery risk?
- How does this apply to AI-assisted distributed engineering teams?
