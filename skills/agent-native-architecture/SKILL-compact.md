# Agent-Native Architecture (compact)

Design applications where agents are first-class citizens using atomic tools, shared workspaces, and prompt-defined features.

## When to Invoke

User needs help designing autonomous agent systems, creating MCP tools, implementing self-modifying systems, or building apps where features are outcomes achieved by agents in a loop.

## Core Principles

1. **Parity** — Every UI action has a corresponding agent capability
2. **Granularity** — Tools are atomic primitives; features are prompt-defined outcomes
3. **Composability** — New features = new prompts (no new code)
4. **Emergent Capability** — Agent handles requests you didn't explicitly design for
5. **Improvement Over Time** — Context accumulation + prompt refinement

## Workflow

1. **Intake** — Ask which aspect: architecture, tool design, files/workspace, execution patterns, system prompts, context injection, parity, self-modification, product design, mobile, testing, or refactoring
2. **Route** — Read the matching reference doc from `references/`
3. **Apply** — Use the reference patterns against the user's specific context
4. **Verify** — Walk through the Architecture Review Checklist

## Architecture Checklist (key items)

- [ ] Every UI action achievable by agent (parity)
- [ ] Tools are primitives, not workflows (granularity)
- [ ] Dynamic capability discovery for external APIs
- [ ] CRUD completeness for every entity
- [ ] Shared workspace (agent + user same data space)
- [ ] context.md pattern for accumulated knowledge
- [ ] Explicit `complete_task` tool (no heuristic detection)
- [ ] System prompt includes available resources + capabilities

## Anti-Pattern Tests

- "To change behavior, do I edit prose or refactor code?" (should be prose)
- "Can I add a feature by writing a prompt alone?" (should be yes)
- "Can the agent handle an open-ended domain request?" (should be yes)

## Quick Start

```typescript
// 1. Atomic tools
const tools = [read_file, write_file, list_files, complete_task];
// 2. Behavior in system prompt (prose, not code)
// 3. Agent loops until complete_task is called
```

## Reference Files

`references/`: architecture-patterns, files-universal-interface, mcp-tool-design, from-primitives-to-domain-tools, agent-execution-patterns, system-prompt-design, dynamic-context-injection, action-parity-discipline, shared-workspace-architecture, product-implications, agent-native-testing, mobile-patterns, self-modification, refactoring-to-prompt-native

---
*For full principles, anti-patterns, and success criteria, read SKILL.md.*
