# intercraft

Agent-native architecture patterns for Claude Code.

## What this does

The core question intercraft answers: can an agent do everything a user can do? If your application has a button that creates a project but no API endpoint or tool that does the same thing, you've built a human-only feature. Agents are second-class citizens, and that's a design bug.

intercraft provides 8 design principles for agent-native architecture (action parity, tools as primitives, context injection, shared workspace, CRUD completeness, UI integration, capability discovery, prompt-native features), a review agent that evaluates code against those principles, and a scored audit command for comprehensive assessment.

## Installation

First, add the [interagency marketplace](https://github.com/mistakeknot/interagency-marketplace) (one-time setup):

```bash
/plugin marketplace add mistakeknot/interagency-marketplace
```

Then install the plugin:

```bash
/plugin install intercraft
```

## Usage

Run an agent-native architecture audit:

```
/agent-native-audit
```

Or use the skill for design guidance when building new features:

```
"review this PR for agent-native parity"
"design this feature so agents can use it too"
```

## Architecture

```
skills/agent-native-architecture/    14 reference docs + SKILL.md
agents/agent-native-reviewer.md      Review agent for PRs and code changes
commands/agent-native-audit.md       Scored audit command
```

The full knowledge cluster pattern: one skill with all the reference material, one agent that applies it to code review, one command that runs a comprehensive audit.
