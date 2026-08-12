# Threshold, as a Claude Skill

`chatbot-feature-gate/` packages the Threshold gate as a [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills)
— so the same five-stage decision runs *inside* a build workflow (a spec, a PRD, an IDE) at the moment
someone is deciding whether and how to ship a chatbot, not only when they visit the web tool.

```
chatbot-feature-gate/
├── SKILL.md                 # trigger + procedure (the entry point)
├── references/
│   ├── feature-gate.md            # the full five-stage gate
│   ├── harm-directions.md         # 5 questions -> 18+2 harm directions + seed behaviors
│   ├── red-team-template.md       # how to build the test
│   └── worked-example-sweetpause.md
└── scripts/
    └── red_team_csv.py      # optional seeded red-team-CSV generator (Python 3, stdlib)
```

**What it produces:** a `chatbot-gate/` folder in the user's project — a scope decision, the live-harm
list, a pass-behaviors spec, a red-team-set CSV, and a written launch gate.

**What it refuses to do:** grade high-stakes rows or certify a system as "safe." It scaffolds human
judgment; it does not replace it. LLMs under-flag sycophancy and over-flag distress — the exact axes
this framework is about — so the skill hands those rows to human reviewers by design.

## Trying it locally

Copy `chatbot-feature-gate/` into your Claude Code skills directory (e.g. `~/.claude/skills/`) or a
project `.claude/skills/`, then start a session and describe a chatbot you're considering. The skill
should trigger on its own.

Grounded in Suh et al. 2026 (arXiv:2607.25057).
