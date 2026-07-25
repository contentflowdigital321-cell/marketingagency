# Agentic AI Practice Projects

A collection of standalone practice projects built while learning agentic AI development with Claude Code. There is no shared build system, package manager, or test runner — each `PracticeNN_*` folder is a self-contained deliverable with its own code and README.

## Projects

- [Practice01_market-agency-website](Practice01_market-agency-website/) — a single-page marketing consultancy website in vanilla HTML/CSS/JS (no frameworks, no build step). See its [README](Practice01_market-agency-website/README.md) for details and the spec checklist.

## Deployment

Pushes to `main` trigger [.github/workflows/deploy-pages.yml](.github/workflows/deploy-pages.yml), which publishes `Practice01_market-agency-website/` to GitHub Pages.

## Working conventions

- New practice projects each get their own `PracticeNN_<name>` folder — code and notes/docs stay together in that folder rather than scattering files at the repo root.
- These are plain static sites: prefer editing files directly over introducing bundlers, package.json, or frameworks unless a task explicitly calls for it.
