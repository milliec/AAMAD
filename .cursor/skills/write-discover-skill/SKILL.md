---
name: write-discover-skill
description: >-
  Help the author write one Discover skill (.cursor/skills/<name>/SKILL.md)
  for @user.researcher, @service.designer or @product-mgr, usually by adapting
  a bimstack skill to the Discover ID model and rules. Build-order step 4. Use
  when the operator says "adapt bimstack's journey-map", "write the synthesis
  skill", or "turn this method into a skill".
---

# Write a Discover skill

Step 4 of the Discover build order. A skill is the **method** a persona follows (how to plan research, how to map a journey). Rules say what must be true. Templates hold the output. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first, then [bimstack-map.md](bimstack-map.md) for what to keep, change and drop from each bimstack skill.

Follow the AAMAD skill shape (see `.cursor/skills/product-design/SKILL.md`): YAML header with `name` and `description`, a one-line purpose, `Invocation:`, who runs it, numbered steps, and a "Do not" list. Move long detail into a `reference.md` beside it.

## Ask the author

1. Which skill, and which persona runs it?
2. Start from a bimstack skill? Which one? (Default: the row in [bimstack-map.md](bimstack-map.md).)
3. Which template (step 3) does it fill in, and which IDs does it create or cite?
4. Where must it **stop for a human**? (e.g. waiting for consent records or anonymised transcripts)
5. What should it refuse to do?
6. Which command starts it? (e.g. `*plan-research`)

## How to adapt a bimstack skill

1. Read the bimstack `SKILL.md` in full (clone: `git clone https://github.com/govtech-bb/bimstack`). Do not work from memory.
2. List its steps. For each, mark **keep**, **change** or **drop**, and show the author the list before drafting.
3. Translate loose citations to IDs: `[P3 interview]` → EV- from S-/P-; `[ASSUMPTION]` → AS-; pain points → PP-; steps → STAGE; opportunities → OP-.
4. Remove context-specific material: Barbados standards and their numbers, GovBB styling and chrome, alpha/beta/live, MDA (→ provider), citizen (→ user), Mac-specific environment notes, `bimstack:` skill names.
5. Add the Discover gates the original lacks: consent check before synthesis, anonymised input only, synthetic = rehearsal, prototypes are throwaway.
6. Keep the useful craft (behaviour over opinion, workarounds, "if this didn't exist", the findings checkpoint, multiple prototypes). Credit it: add a line under "Sources" in the new skill naming the bimstack skill it adapts.
7. Add or update the bimstack entry in the repo's `NOTICES`.

## Draft shape

```markdown
---
name: <skill-name>
description: >-
  <what it does, who runs it, when to use it, trigger phrases>
---

# <Skill name>

<one-line purpose>

Invocation: `*<command>`. Run by `@<persona>`. Fills `.cursor/templates/discover-<x>-template.md`.

## Before you start
- Inputs required: <files/IDs>. If missing, stop and say which.

## Steps
1. …

## Human checkpoint
Stop and wait for: <file>. Do not continue until it exists.

## Do not
- …

## Sources
Adapted from bimstack `<skill>` (MIT, © 2026 GovTech Barbados Limited and contributors).
```

## Check before showing

- Every output step names the ID it creates and the IDs it must cite.
- Synthesis steps check consent for each cited P- first and refuse with the missing P- named.
- Research-assistant skills never recruit, decide consent, run a live session, or make the final judgement.
- Prototype skills say "throwaway; never handed to `@frontend.eng` as code".
- Run the rules checklist.

## Do not

- Copy a bimstack skill wholesale. Adapt, cut and credit.
- Keep bimstack's links to its own skills or external plugins (`design:…`) that AAMAD does not have.
