---
title: Optional project tracking patterns
owner: Engineering
status: Active
last_updated: 2026-10-16
---

# Project tracking

Work boards hold state and links; specifications, decisions, source and evidence live in the adopting repository. Start with one board and existing project conventions. Add separate views only when they solve an observed planning problem. This guide consolidates the former Polaris wiki proposal; it does not provision GitHub Projects or establish a live-board inventory.

| Optional view | Useful states or fields |
|---|---|
| Delivery | Backlog, specified, in progress, review, blocked, done |
| Roadmap | Now, next, later, shipped; milestone and target date |
| Launch | Foundation, build, hardening, preparation, launch, observation; go/no-go decision |
| Feature | Context, design, build, quality, delivery, done; link the applicable playbook |
| Bug triage | New, reproduced, root-caused, fixing, verifying, closed; severity and regression evidence |

The earlier proposal named five Axis master projects. Those were reference patterns, not verified resources that a new product must copy. Verify existing boards and fields through the current platform before changing them.

Use an issue/request ID across plans, discipline handoffs, implementation PRs and evidence. Track the responsible owner, scope, acceptance criteria, blockers and relevant review gates. A numerical confidence field never grants authority. Board automation and external writes require their own authorised scope; local planning does not create work items.
