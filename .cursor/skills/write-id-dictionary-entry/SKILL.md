---
name: write-id-dictionary-entry
description: >-
  Help the author write one entry in the Discover ID dictionary
  (.cursor/rules/discover-id-dictionary.mdc): what an ID family means, its
  fields, its links, who creates it, and its rules. Build-order step 1. Use
  when the operator says "add the EV- entry", "define UN-", "write the ID
  dictionary", or names any Discover ID prefix.
---

# Write an ID dictionary entry

Step 1 of the Discover build order. The dictionary is the one place every persona looks up what an ID means. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first.

## Ask the author

1. Which ID family? (e.g. EV-)
2. In one plain sentence, what is it?
3. Which fields does it carry? Which are required?
4. What does it link to, and in which direction? (e.g. "EV- comes from S- or SRC-")
5. Which persona creates it? Which may edit it?
6. Allowed status values, if any, and what changes them.
7. Any special rule (e.g. "never deleted, only retired").

If they are unsure, offer the starting point from the reference table and mark it `TODO(author): confirm`.

## Draft shape

Use this shape for every entry, so the dictionary stays consistent:

```markdown
## EV- Evidence
What: <one plain sentence>
Fields: id (EV-NNN), <field> (<allowed values>), …  — required fields first
Links to: <ID> (<direction, e.g. "comes from S-">); …
Created by: @<persona>   Edited by: @<persona>
Status: <values> — <what changes it>   (or "none")
Rules: <one rule per line>
Example: TODO(author): one made-up example clearly labelled "example only"
```

If the dictionary file does not exist yet, create it with this header and add the entry under it:

```markdown
---
description: Discover phase ID dictionary. Definitions, fields and links for every Discover ID family. All Discover personas cite IDs from here.
alwaysApply: true
---

# Discover ID dictionary

TODO(author): one-paragraph intro and the trace chain OUTPUT → US- → UN- → OUT- → M-.
```

## Check before showing

- Links match the other entries in both directions. If EV- says "comes from S-", the S- entry should say "produces EV-". Flag any one-way link as `TODO(author)`.
- Run the rules checklist. Extra checks for these families:
  - **UN-**: solution-free; "I need … so that …"; needs a non-synthetic EV-; retired, never deleted.
  - **US-**: must cite UN-; has AC-.
  - **OUT-**: end result, not an output, goal, or solution; needs an M-.
  - **EV-**: type must be one of observed / said / data / synthetic; synthetic cannot back a UN-.
  - **P-**: pseudonym only; consent field required.
  - **AS-**: status untested / confirmed / disproved; only a TS- with non-synthetic EV- changes it.
- Examples are labelled "example only" and contain no real participant data.

## Do not

- Invent fields the author did not give or confirm.
- Write more than one entry per turn unless the author asks.
