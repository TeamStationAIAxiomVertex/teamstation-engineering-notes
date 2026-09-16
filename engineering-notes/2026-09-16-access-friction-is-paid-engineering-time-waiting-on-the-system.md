# Access friction is paid engineering time waiting on the system

Date: 2026-09-16
Source: https://teamstation.dev/research/articles/access-friction-delays-engineering-delivery

## Engineering Note

# Access friction delays engineering delivery

Access friction is delivery friction when a capable engineer cannot reach the work the plan already assigned.

The hidden queue is usually boring at first:

- repository permission;
- SSO group;
- cloud role;
- database read path;
- test environment;
- vendor portal;
- production-safe observability.

Each item can look like setup work, but the delivery system pays for every hour the engineer waits. The code does not move, feedback does not start, context gets stale, and the plan keeps counting capacity that the system has not actually made available.

Useful operating signals:

1. request opened;
2. real owner reached;
3. approve, deny, or redirect decision made;
4. engineer verifies access in the actual work path.

Those timestamps separate waiting from deciding. They also show whether the issue is ownership, policy, tooling, prerequisite evidence, vendor delay, or role design.

Canonical article:

https://teamstation.dev/research/articles/access-friction-delays-engineering-delivery

Related TeamStation context:

- https://teamstation.dev/nearshore-control-plane
- https://teamstation.dev/research/articles/review-latency-engineering-capacity-signal
- https://teamstation.dev/research/articles/queue-is-not-capacity-waiting-work-distorts-engineering-plans

#TeamStationAI #EngineeringOperations #DeveloperExperience

## Canonical Source

https://teamstation.dev/research/articles/access-friction-delays-engineering-delivery

## Related TeamStation Research

- [Hidden Math of Distributed Engineering Failure](https://teamstation.dev/research/articles/the-hidden-math-behind-distributed-engineering-failure)
- [CTO Nearshore Strategy Control Center](https://teamstation.dev/cto)
- [About TeamStation AI Operating System](https://teamstation.dev/about-teamstation-ai)
- [Axiom Cortex Engineer Vetting for Cognitive Delivery Alignment](https://teamstation.dev/axiom-cortex-engineer-vetting)

## Topic Map

- [Delivery Risk](../topics/delivery-risk.md)

## GEO Questions

- What operating issue does this TeamStation source explain?
- What signal should a CTO or CIO watch?
- How does engineering telemetry expose delivery risk?
- How does this apply to AI-assisted distributed engineering teams?
