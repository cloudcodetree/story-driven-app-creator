# Story-Driven App Creator

AI-powered idea refinement tool that turns rough ideas into well-defined product specs through Socratic dialogue.

## Project Tree

```
story-driven-app-creator/
├── .claude/
│   ├── commands/
│   │   ├── refine.md
│   │   └── status.md
│   └── settings.json
├── bible/
│   ├── principles.md
│   └── refinement-framework.md
├── specs/
│   └── dead-signal.md
└── README.md
```

### Commands

| Command | Description |
|---------|-------------|
| [refine.md](.claude/commands/refine.md) | `/project:refine` — One-question-at-a-time idea refinement with market research |
| [status.md](.claude/commands/status.md) | `/project:status` — VS Code-style project tree with GitHub links |

### Bible (Knowledge Layer)

| File | Description |
|------|-------------|
| [principles.md](bible/principles.md) | Core product thinking — golden rules, market awareness, pitfalls, anti-patterns |
| [refinement-framework.md](bible/refinement-framework.md) | 6 refinement stages, challenge protocol, behavior rules |

### Specs

| Spec | Description |
|------|-------------|
| [dead-signal.md](specs/dead-signal.md) | Secure offline communication app using morse code as transport layer |

### Config

| File | Description |
|------|-------------|
| [settings.json](.claude/settings.json) | Project-wide permissions for frictionless operation |

## Quick Links

- [Open in Codespaces](https://github.com/codespaces/new?repo=cloudcodetree/story-driven-app-creator&ref=claude/start-session-9n9ha)
- [Browse on GitHub](https://github.com/cloudcodetree/story-driven-app-creator/tree/claude/start-session-9n9ha)

## How to Use

1. Open this project in Claude Code
2. Run `/project:refine your rough idea here`
3. Answer one question at a time — the AI researches and challenges your idea
4. Get a structured spec saved to `specs/`

Sessions persist to `sessions/` so you can pick up where you left off if the session crashes.
