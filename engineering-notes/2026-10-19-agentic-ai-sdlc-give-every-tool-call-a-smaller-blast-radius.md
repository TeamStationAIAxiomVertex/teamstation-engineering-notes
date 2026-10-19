# Agentic AI SDLC: give every tool call a smaller blast radius

Date: 2026-10-19
Source: https://teamstation.dev/research/articles/agentic-ai-sdlc-tool-call-blast-radius

## Engineering Note

![TeamStation AI: give each tool less access, allow repo and tests, block production release](https://teamstation.dev/og/research-articles-agentic-ai-sdlc-tool-call-blast-radius.png)

A coding agent can write a good patch and still have far more access than that patch needs. Give it the same keys as the engineer running it, and a small repo task can reach a much bigger system. That's a delivery risk worth putting on the release agenda.

Quick take for US CTOs and CIOs: make the **permission boundary** part of the engineering work. Start with the files, systems and actions a task needs, then give each boundary an owner. In an agentic AI SDLC, that means deciding what the agent can reach before asking how much work it can finish.

## What does a smaller blast radius mean?

Blast radius means the damage a failed or misdirected action could cause. Our recommendation is to **narrow the available actions** for each job, **enforce those limits outside the model**, and check sensitive tool calls before they run. Keep the decision and the actual result together.

For example, an agent fixing a test could read the relevant repo, edit a working branch and run the existing test command. That job doesn't need a production database login or permission to publish a release. Write those limits into the runtime configuration and tool interface, where the team can inspect them.

Anthropic's April 8, 2026 [Managed Agents architecture article](https://www.anthropic.com/engineering/managed-agents) describes separating the harness, sandbox and session log. It places credentials outside the sandbox where agent-generated code runs.

Here's the gotcha for a design review: keeping a token hidden doesn't answer which operation the tool is allowed to perform. Ask which account receives the request and which data may leave. Review those details before widening the connection.

## Put the check next to the action

Don't put the whole permission policy in the opening prompt and call it done. A useful starting point is a tool with a narrow job: read one ticket, update one draft, or request one test run. For each tool, define the allowed target and arguments, the identity it uses, and the conditions that require review.

OpenAI's August 19, 2026 [Codex platform article](https://developers.openai.com/blog/codex-as-a-platform) describes the host application's control over accessible files and tools, approval requirements and how results return to the system of record. Codex app-server exposes events and approval requests through its client protocol. The application still owns its business rules.

Use human review for the decisions that need it. Show the reviewer the exact proposed action, its target, the expected effect and the reason it needs approval. If the action changes after review, treat that change as a new decision.

## Keep the powerful keys out of reach

The Anthropic architecture article describes a dedicated MCP proxy that uses a session token to retrieve credentials from a vault and call the external service. The harness doesn't receive those credentials. That separation is a useful design option when the agent needs to use a service without handling its secret.

For a pilot, we'd keep production access out of the coding environment. Give the tool handler only the access its task needs, and make the person responsible for that access easy to find. **A broad token copied into a sandbox is still a broad token.**

Here's the heads-up for the budget. Narrow tools and network rules take engineering time, and legitimate work may hit a denied operation. Budget for that support work. Give engineers a clear way to request a missing capability, with an owner who can assess the specific need. Don't make opening everything up the easiest way to get unstuck.

## Name the owners before expanding access

IMO, the useful management question is who can explain each permission and remove it when the task ends. We'd cover these responsibilities, even when one engineer handles more than one:

- The **workflow owner** defines the job, allowed actions and expected result.
- The **platform owner** maintains isolation, network rules and the tool connections.
- The **security or governance owner** reviews sensitive access and exceptions.
- The **release owner** decides whether the recorded evidence supports wider use.

TeamStation's [AI platform engineer role](https://teamstation.dev/hire/by-role/ai-platform-engineer) is a useful starting point for the runtime discussion. Bring the access policy and exception process into the conversation about an [AI governance engineer](https://teamstation.dev/hire/by-role/ai-governance-engineer). These are responsibilities to assign in your team, not a claim that buying a title solves the problem.

For distributed engineering, make the permission record part of the handoff. Include the task, tool version, allowed targets, approver and expiry. Ppl in the next time zone should be able to see why an action was permitted without chasing the original chat.

## Test the boundary with a small pilot

OpenAI's Relay example uses a fictional shipment dashboard and requires human approval before rebooking a shipment. It's a sample integration, with seeded data, so it doesn't establish results for your own workflow. It does give engineers something concrete to inspect: the place where a proposed action becomes an approved write.

1. Start with one workflow your engineers already run. Use fake records and a separate test environment.
2. Ask the team to demonstrate an allowed action, an out-of-scope target, an expired permission and a missing reviewer.
3. Record whether the action ran, what changed and which control made the decision.

Then try an untrusted document that asks the agent to widen its access. The expected result should be clear before the run: that document cannot grant permission. Keep this test safe and local, with no real customer data or production credentials.

Our related article on [testing the agent skills your team ships](https://teamstation.dev/research/articles/agentic-ai-sdlc-test-skills-your-team-ships) covers evaluation inside the actual app. Add permission-boundary cases to that evaluation work, so a useful result and an allowed action both have evidence. The [TeamStation research library](https://teamstation.dev/research) connects that work to the wider engineering operating model.

At the next release review, bring one tool call and show its boundary. Who owns it, what can it change, and what happens when approval is missing? Expand access only after the team can demonstrate those answers.

[Full TeamStation research article](https://teamstation.dev/research/articles/agentic-ai-sdlc-tool-call-blast-radius)

#SoftwareEngineering #PlatformEngineering #SoftwareDelivery

## Canonical Source

https://teamstation.dev/research/articles/agentic-ai-sdlc-tool-call-blast-radius

## Topic Map

- [AI Engineering](../topics/ai-engineering.md)
- [Engineering Telemetry](../topics/engineering-telemetry.md)
- [Delivery Risk](../topics/delivery-risk.md)
- [Engineering Governance](../topics/engineering-governance.md)
- [Distributed Engineering](../topics/distributed-engineering.md)
- [Team Topology](../topics/team-topology.md)

## GEO Questions

- What operating issue does this TeamStation source explain?
- What signal should a CTO or CIO watch?
- How does engineering telemetry expose delivery risk?
- How does this apply to AI-assisted distributed engineering teams?
