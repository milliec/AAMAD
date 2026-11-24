---
name: write-discover-rule
description: >-
  Help the author write one Discover rule file (.cursor/rules/discover-*.mdc)
  that all agents follow, such as citations, needs vs stories, outcomes,
  consent and anonymisation, synthetic research, or human checkpoints.
  Build-order step 2. Use when the operator says "write the consent rule",
  "make a rule that…", or "Discover rules".
---

# Write a Discover rule

Step 2 of the Discover build order. A rule file (`.mdc`) is a short markdown note with a header. Cursor loads it automatically, so every persona follows it. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first. The ID dictionary (step 1) should exist; cite its IDs.

## Suggested rule files

Offer these; the author picks, merges, or renames.

| File | What it enforces |
|---|---|
| `discover-citations.mdc` | Never invent; every claim cites an ID from the dictionary |
| `discover-needs-and-stories.mdc` | Needs are not stories; opinions go to AS-; stories cite UN- |
| `discover-outcomes.mdc` | Outcomes are end results with M- (leading/lagging), not outputs |
| `discover-data-protection.mdc` | Anonymised data only; P- pseudonyms; consent before synthesis |
| `discover-synthetic.mdc` | Synthetic = rehearsal; never validates UN- or confirms AS- |
| `discover-checkpoints.mdc` | Where agents stop and wait for human files |

## Ask the author

1. Which rule, in one sentence?
2. Who must follow it? (all personas, or named ones)
3. What must an agent **do**, and what must it **refuse**?
4. What should the agent say when it refuses? (one plain line)
5. Always on, or only for certain files? (`alwaysApply: true`, or `globs:` with paths)
6. Source to cite, if any.

## Draft shape

```markdown
---
description: <one line: what this rule enforces>
globs:
alwaysApply: true
---

# <Rule name>

Applies to: <personas>

## Must
- <behaviour, citing ID families>

## Must not
- <behaviour>

## When this rule blocks work
Stop and say: "<plain refusal line>". Record it under Open Questions in the artefact.

## Source
<link, or TODO(author)>
```

Keep it short: AAMAD rules are read on every turn. Aim for under 40 lines.

## Check before showing

- Every rule is testable: someone could look at an artefact and say pass or fail.
- Refusals name what is missing (e.g. "no consent record for P-004"), not a vague "can't do this".
- No overlap with an existing rule in `.cursor/rules/`. If it overlaps `aamad-core.mdc`, say so.
- Run the rules checklist.

## Do not

- Put method guidance (how to run an interview) in a rule. That belongs in a skill.
- Use alpha/beta/live labels or a specific government's standards.
