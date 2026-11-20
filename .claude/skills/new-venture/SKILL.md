---
name: new-venture
description: Use when Jake wants to start tracking a new business idea/venture in Jarvis HQ. Scaffolds a venture brief and registers it in the root CLAUDE.md table. Invoke as /new-venture <short-name>.
---

1. Ask Jake (if not already given) for: the one-line problem/idea, the target
   customer, and the current stage (idea / validating / building / live).
2. Create `ventures/<short-name>/BRIEF.md` with that info plus a "Next milestone"
   line and an empty "Decisions log" section.
3. Add a row for it in the "Active ventures" table in the root `CLAUDE.md`, linking
   to the brief.
4. Suggest which subagent (researcher/coder/marketer) makes sense as the next step
   given the stated stage, and why — don't just default to coder.
5. Do not create a separate git repo for the venture automatically. Only do that if
   Jake confirms the idea is past "validating" and worth its own repo.
