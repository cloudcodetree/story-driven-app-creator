# Project Status — Story-Driven App Creator

Generate a VS Code-style tree view of the project with clickable GitHub links.

## Instructions

1. Detect the GitHub repo and current branch:
   - Run `git remote get-url origin` to extract the org/repo (e.g., `cloudcodetree/story-driven-app-creator`)
   - Run `git branch --show-current` to get the current branch
   - Build the base URL: `https://github.com/{org}/{repo}/blob/{branch}`

2. Scan ALL project directories and files. Build a tree view that mimics VS Code's explorer sidebar. Use box-drawing characters for the tree structure. Every file should be a clickable markdown link to its GitHub blob URL.

3. Output format — render like this example:

```
story-driven-app-creator
├── [.claude/](github-tree-link)
│   ├── [commands/](github-tree-link)
│   │   ├── [refine.md](github-blob-link) — Idea refinement slash command
│   │   └── [status.md](github-blob-link) — This command
│   └── [settings.json](github-blob-link) — Project permissions
├── [bible/](github-tree-link)
│   ├── [principles.md](github-blob-link) — Product thinking principles
│   └── [refinement-framework.md](github-blob-link) — Refinement stages & rules
├── [sessions/](github-tree-link)
│   └── [idea-name/](github-tree-link)
│       └── [context.md](github-blob-link) — Stage: Market Reality
├── [specs/](github-tree-link)
│   └── [dead-signal.md](github-blob-link) — Secure offline communication
└── [README.md](github-blob-link)
```

4. Rules:
   - Use `├──` for items with siblings below, `└──` for the last item in a group
   - Use `│   ` for vertical continuation, `    ` for empty space
   - Directories get a trailing `/` and link to the GitHub tree URL (not blob)
   - Files link to the GitHub blob URL
   - Add a brief description after each file (based on first heading or purpose)
   - For session context.md files, read the Status section and show the current stage
   - Skip .git/ and node_modules/
   - Sort: directories first, then files, alphabetically within each group

5. After the tree, add:

```
Quick Links:
  [Browse on GitHub](repo-link) · [Open in Codespaces](codespaces-link)
```
