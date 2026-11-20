# Jarvis HQ

Personal orchestration layer for Jake Owen's side-hustle ventures. This repo is the
"brain" — it holds agent definitions, skills, and per-venture notes. It does not hold
venture product code; each venture lives in its own repo (linked below) or, if truly
tiny, under `ventures/<name>/`.

## Operator

- Jake Owen (github: jbone91) — senior data engineer, Bakersfield CA. Day job is
  full-time; this is evenings/weekends work. Assume limited time budget per venture
  unless told otherwise.

## Active ventures

| Venture | Repo | Stage | Notes |
|---|---|---|---|
| _none yet_ | | | Add a row here once we pick the first idea to prototype |

## How to work in this repo

- Each venture gets a short brief in `ventures/<name>/BRIEF.md` (problem, target
  customer, current stage, next milestone) before any subagent is dispatched against it.
- Use the `researcher`, `coder`, and `marketer` subagents in `.claude/agents/` for
  venture work. Don't do deep multi-step venture work in the main thread — dispatch to
  the right subagent so context stays clean per role.
- Recurring/autonomous work (daily scans, status rollups) should be defined as Skills
  under `.claude/skills/` and triggered via `/loop` or scheduled cron agents, not
  re-explained from scratch each session.
- Keep secrets (API keys, credentials) out of this repo entirely — use environment
  variables or a local untracked `.env`, never commit them.

## Conventions

- Commit messages: short, imperative (`add researcher agent`, not `Added...`).
- New venture = new row in the table above + its own `ventures/<name>/BRIEF.md`.
