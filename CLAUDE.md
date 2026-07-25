# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This is a collection of standalone practice projects, not a single application. There is no shared build system, package manager, or test runner — each `PracticeNN_*` folder is a self-contained deliverable.

## Practice01_market-agency-website

A single-page marketing consultancy website built in vanilla HTML/CSS/JS (no frameworks, no build step).

- `Practice01_market-agency-website/index.html` — everything: markup, CSS in a `<style>` block, JS in a `<script>` block.
- `Practice01_market-agency-website/README.md` — spec checklist and verification notes for this project.

**Running it**: open `index.html` directly in a browser (`Start-Process index.html` on Windows). There is no dev server, build step, linter, or test suite.

**Enquiry form**: submits via `fetch()` as JSON to `https://formspree.io/f/{YOUR_FORM_ID}` with `Accept: application/json`. The form ID is a placeholder (`YOUR_FORM_ID`) — submissions will 404 until it's replaced with a real Formspree form ID.

## Working conventions

- New practice projects should each get their own `PracticeNN_<name>` folder — keep a project's code and its notes/docs together in that folder rather than scattering files at the repo root.
- These are plain static sites: prefer editing the single HTML file directly over introducing bundlers, package.json, or frameworks unless a task explicitly calls for it.
