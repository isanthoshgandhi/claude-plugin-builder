# Santhosh Gandhi Claude Skills

A curated collection of Claude skills and plugins by [Santhosh Gandhi](https://github.com/isanthoshgandhi) — built from real-world experience developing production Claude plugins.

Every skill in this repo works on **claude.ai** and **Claude Code**. Install the entire collection with one command.

---

## Install All Skills

```bash
claude plugin marketplace add https://github.com/isanthoshgandhi/santhosh-gandhi-claude-skills
claude plugin install santhosh-gandhi-claude-skills
```

---

## Skills Collection

| Skill | What It Does | Platform | Version |
|---|---|---|---|
| [claude-plugin-builder](skills/claude-plugin-builder/SKILL.md) | Build a complete Claude plugin in 23 guided steps — from idea to GitHub push | claude.ai + Claude Code | 1.0.0 |

*More skills coming soon.*

---

## Skill Spotlight — Claude Plugin Builder

**The problem:** Building a Claude plugin requires knowing SKILL.md format, agent architecture, `plugin.json`, `marketplace.json`, GitHub structure, SEO topics, trigger phrase engineering — and getting all of it right on the first try.

**The solution:** A 23-step guided interview that takes your raw idea and produces a fully deployed, marketplace-ready Claude plugin.

### What it does
1. Interviews you across 5 phases: Discovery → Design → Classify → Generate → Push
2. Searches GitHub/PyPI for existing open source you can leverage
3. Infers UX flow, data flow, and output template from your answers
4. Auto-classifies: Skill / Agent / Skill+Agent / Commands
5. Auto-generates SEO topics and marketplace descriptions
6. Generates all files: `SKILL.md`, agent `.md`, scripts, `plugin.json`, `marketplace.json`, `README.md`
7. Pushes to your GitHub repo with a single confirmation

### Example trigger phrases
- *"Build me a Claude plugin that..."*
- *"I want to create a Claude skill for..."*
- *"Help me make a new agent"*
- *"How do I structure a Claude plugin?"*
- *"New plugin"*

### Output preview
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLAUDE PLUGIN BUILDER  ·  CLASSIFICATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Type:       SKILL + AGENT
Compatible: claude.ai (Skill) + Claude Code (Agent)
Reason:     Requires Python scripts for file generation and git push

FILES TO BE GENERATED:
├── .claude-plugin/plugin.json
├── .claude-plugin/marketplace.json
├── skills/[name]/SKILL.md
├── agents/[name].md
└── README.md
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✓ PUSHED
Install: claude plugin marketplace add [your-repo]
         claude plugin install [name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Built From Experience

This collection is built from direct experience developing **[foresight-engine](https://github.com/isanthoshgandhi/foresight-engine)** — a 12-step strategic foresight plugin using IFTF methodology.

Key lessons applied to every skill here:
- `description:` frontmatter = activation trigger, not a description
- Output template design matters more than pipeline complexity
- Platform detection (claude.ai vs Claude Code) must be handled explicitly
- Confirmation gates before every irreversible action
- Windows-compatible paths throughout

---

## Adding More Skills

This repo is structured for growth. Each new skill lives in its own folder:

```
santhosh-gandhi-claude-skills/
├── .claude-plugin/
│   ├── plugin.json        ← update version + add skill path
│   └── marketplace.json   ← update version
├── skills/
│   ├── claude-plugin-builder/
│   │   └── SKILL.md
│   └── [next-skill]/      ← add here
│       └── SKILL.md
└── README.md              ← add row to skills table
```

---

## Author

**Santhosh Gandhi** · [github.com/isanthoshgandhi](https://github.com/isanthoshgandhi)

Also check out: [foresight-engine](https://github.com/isanthoshgandhi/foresight-engine) — Strategic foresight plugin using IFTF/STEEEP methodology.
