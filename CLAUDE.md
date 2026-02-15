# intercraft

Agent-native architecture patterns — design, review, and audit for agent-first applications.

## Overview

1 skill, 1 agent, 1 command, 0 hooks. Companion plugin for Clavain.

## Quick Commands

```bash
python3 -c "import json; json.load(open('.claude-plugin/plugin.json'))"  # Manifest check
ls skills/*/SKILL.md | wc -l  # Should be 1
ls agents/review/*.md | wc -l  # Should be 1
ls commands/*.md | wc -l  # Should be 1
```

## Design Decisions (Do Not Re-Ask)

- Full knowledge cluster: skill (with 14 reference docs) + agent + command
- 8 core principles: action parity, tools as primitives, context injection, shared workspace, CRUD completeness, UI integration, capability discovery, prompt-native features
- Extracted from Clavain — domain-specific architecture concern, not core engineering
