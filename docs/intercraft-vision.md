# intercraft — Vision and Philosophy

**Version:** 0.1.0
**Last updated:** 2026-02-28

## What intercraft Is

intercraft is a domain-specific architecture guidance system for building agent-native applications — software where agents are first-class citizens, not bolt-on features. It encodes 8 core principles (action parity, tools as primitives, context injection, shared workspace, CRUD completeness, UI integration, capability discovery, prompt-native features) as a structured skill with 14 reference documents, a review agent that audits compliance, and a command that runs scored parallel audits across all 8 dimensions. The goal is not a checklist — it is a design vocabulary precise enough to catch the difference between an app that has an agent and an app that is agent-native.

intercraft is a companion to Clavain. Where Clavain handles engineering craft (code quality, testing, safety, performance), intercraft handles a different concern: whether the architectural decisions made during construction treat agents as equal participants. A codebase can pass every Clavain check and still leave agents unable to do half of what users can do. intercraft closes that gap.

## Why This Exists

The failure mode is predictable: developers build UI first, ship it, then add an agent layer that can only do what they remembered to expose. Users ask the agent for something the UI can do in two taps, and the agent apologizes. The root cause is that agent-native architecture requires discipline at design time — not at the end. Catching an orphaned UI action after the fact is expensive; enforcing parity as a design constraint is cheap. Review phases are where the leverage is, and intercraft puts the review at the right point in the process.

## Design Principles

1. **Parity is non-negotiable.** Whatever the user can do through the UI, the agent must be able to achieve through tools. Parity is not a feature — it is the floor. An application that fails this test is not agent-native, regardless of how sophisticated its AI integration is elsewhere.

2. **Tools enable capability; prompts define behavior.** Tools are primitives (read, write, store, move). Features are outcomes described in prompts, achieved by agents operating in a loop. When business logic moves into tools, it moves out of the agent's reach. Keep judgment in the prompt layer, not the tool layer.

3. **Composition beats capability.** Small composable agents with atomic tools outperform monolithic agents with workflow-shaped tools. The same principle that governs Demarch's architecture governs every application built with these patterns — many small pieces composed explicitly, not one large system with hidden dependencies.

4. **Architecture review catches design errors early.** The review agent and audit command exist because architecture decisions are expensive to undo. Scoring compliance across 8 principles at design time surfaces gaps before they calcify into product debt.

5. **Demarch builds itself with these patterns.** The principles intercraft enforces are not hypothetical — they describe how Demarch's own agent infrastructure is designed. Self-building is both a constraint (if these patterns break down internally, that is a signal) and a credibility mechanism (the patterns are tested against real workloads, not just documented).

## Scope

**What intercraft covers:** Design guidance for new agent-native systems; architecture review of existing codebases; scored compliance auditing across 8 principles; reference documentation for 13 specific concerns (tool design, execution patterns, mobile patterns, self-modification, refactoring, and more); agent-to-UI integration patterns; context injection strategies.

**What intercraft does not cover:** General engineering quality (code style, test coverage, performance) — that is Clavain's domain. Model selection or routing. Production infrastructure for running agents. Application-level business logic. intercraft is concerned with structural fitness for agency, not implementation quality.

## Direction

- Extend the audit command to produce machine-readable output so compliance scores can be tracked across sprints and regressions surfaced automatically.
- Add reference documents for multi-agent coordination patterns — when multiple agents share a workspace, parity and shared-workspace principles require additional treatment.
- Formalize the relationship between intercraft principles and Demarch's own architecture so the self-building signal is explicit and measurable.
