# Changelog

All notable changes to Claude Plugin Builder are documented here.

---

## [1.0.0] — 2026-03-16

### Added
- Initial release.
- **23-step guided pipeline** covering the full lifecycle from idea to deployed plugin:
  - Phase 1 — Discovery (Steps 1–7): vision, audience, goals, inputs, outputs, open source research, platform target
  - Phase 2 — Design (Steps 8–10): output template, trigger phrases, plugin name and tagline
  - Phase 3 — Classify (Steps 11–13): auto-classification (Skill / Agent / Skill+Agent / Skill+Commands), dependency check, SEO generation
  - Phase 4 — Generate (Steps 14–19): SKILL.md, agent file, scripts, plugin.json, marketplace.json, README.md
  - Phase 5 — Review + Push (Steps 20–23): file tree review, privacy flag, error scenarios, GitHub push
- **Platform detection**: automatically switches between Claude Code mode (writes files, pushes to GitHub) and claude.ai mode (outputs copy-paste shell script).
- **Auto-classify rules**: deterministic logic that selects the right plugin type based on what the plugin needs to do.
- **SEO auto-generation**: infers GitHub topics, repo description, and marketplace description from the user's answers.
- **Privacy flag**: warns before push if the plugin handles names, emails, health, financial, or location data.
- **Windows compatibility**: uses `python` instead of `python3`, backslash path guidance for script stubs.
- **Never-skip confirmation gates** at classification, file review, and push steps.
