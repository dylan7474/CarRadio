# AGENTS.md

Guidance for AI coding agents working in this repository.

## Repository overview
- This project is a static web app.
- Primary application code lives in `index.html` (HTML + CSS + JavaScript).
- Documentation and project metadata live at the repository root.

## Workflow expectations
- Prefer small, focused changes.
- Update docs when behavior or controls change.
- Keep dependencies minimal; avoid introducing build tooling unless explicitly requested.

## Coding conventions
- Preserve the app's touch-first and full-screen UX.
- Keep station-related logic centralized in the `stations` array and station navigation functions.
- Favor readable vanilla JavaScript over framework additions.

## Validation
- For docs-only changes: verify markdown formatting and run `git diff --check`.
- For runtime changes: open the app in a browser and test tap-to-play and swipe station navigation.

## PR hygiene
- Include a concise summary and explicit test/check commands run.
- Call out any environment limitations that prevented validation.
