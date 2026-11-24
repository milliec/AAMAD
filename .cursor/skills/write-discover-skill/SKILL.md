---
name: write-discover-skill
description: >-
  Help the author write one Discover skill (.cursor/skills/<name>/SKILL.md)
  for @user.researcher, @service.designer or @product-mgr. Each skill teaches
  one research or service-design method. Build-order step 4. Use when the
  operator says "write the journey-map skill", "write the synthesis skill",
  or "turn this method into a skill".
---

# Write a Discover skill

Step 4 of the Discover build order. A skill is the **method** a persona follows (how to plan research, how to map a journey, how to synthesise needs). Rules say what must be true. Templates hold the output. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first, then [method-notes.md](method-notes.md) for suggested skills and craft principles to embed.

Follow the AAMAD skill shape (see `.cursor/skills/product-design/SKILL.md`): YAML header with `name` and `description`, a one-line purpose, `Invocation:`, who runs it, numbered steps, and a "Do not" list. Move long detail into a `reference.md` beside it.

## Ask the author

1. Which skill, and which persona runs it?
2. Which suggested skill from [method-notes.md](method-notes.md)? (Or a different method?)
3. Which template (step 3) does it fill in, and which IDs does it create or cite?
4. Where must it **stop for a human**? (e.g. waiting for consent records or anonymised transcripts)
5. What should it refuse to do?
6. Which command starts it? (e.g. `*plan-research`)

## How to write the skill

1. Start with the method steps from [method-notes.md](method-notes.md) for the chosen skill, or ask the author to describe the method.
2. List the steps. For each, confirm with the author: **keep**, **change** or **drop**.
3. Translate loose citations to IDs: interviews → EV- from S-/P-; assumptions → AS-; pain points → PP-; journey steps → STAGE; opportunities → OP-.
4. Embed craft principles from method-notes.md: behaviour over opinion, workarounds reveal needs, "if this didn't exist", findings checkpoint, multiple prototypes for competing hypotheses.
5. Add the required Discover gates: consent check before synthesis, anonymised input only, synthetic = rehearsal, prototypes are throwaway, draft-only for consent decisions.
6. Keep language generic: provider (not MDA), user (not citizen), prototype (not alpha).

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
```

## Check before showing

- Every output step names the ID it creates and the IDs it must cite.
- Synthesis steps check consent for each cited P- first and refuse with the missing P- named.
- Research-assistant skills never recruit, decide consent, run a live session, or make the final judgement.
- Prototype skills say "throwaway; never handed to `@frontend.eng` as code".
- Run the rules checklist.

## Do not

- Invent method steps. Ask the author or use the suggested steps from method-notes.md.
- Skip the human checkpoints (consent, anonymisation, findings review, draft-only decisions).
- Use upstream framework names or link to skills AAMAD does not have.
