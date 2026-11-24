---
name: discover-authoring
description: >-
  Start here when writing any file for the AAMAD Discover phase (the phase
  before Define). Routes the author to the right writing skill in the agreed
  build order, and holds the shared rules every Discover file must pass. Use
  when the operator says "write the Discover files", "what's next for
  Discover", or opens any write-* Discover skill.
---

# Discover authoring

These skills help a human author **write** the Discover phase files. The author decides. The agent asks, drafts for review, checks the agreed rules, and leaves `TODO(author):` markers instead of inventing anything.

Read [reference.md](reference.md) before drafting. It holds the agreed decisions, the ID families, the rules checklist, and the file locations.

## Build order (agreed)

| Step | What gets written | Skill |
|---|---|---|
| 1 | ID dictionary (one entry per ID family) | [write-id-dictionary-entry](../write-id-dictionary-entry/SKILL.md) |
| 2 | Rule files (`.mdc`) | [write-discover-rule](../write-discover-rule/SKILL.md) |
| 3 | Templates for Discover artefacts | [write-discover-template](../write-discover-template/SKILL.md) |
| 4 | Discover skills, adapted from bimstack | [write-discover-skill](../write-discover-skill/SKILL.md) |
| 5 | Personas (six-part anatomy) | [write-persona](../write-persona/SKILL.md) |
| 6 | Wiring: crew overview, epics index, `aamad.config.yml`, go/stop gate as a required PRD input | `TODO(author):` no skill yet; do by hand with the agent |
| 7 | Dry run on a small real problem; check one story traces back to a quote | `TODO(author):` no skill yet |

Work in order. A later step may cite only IDs and files that an earlier step has defined. If the author wants to skip ahead, say which earlier file is missing and leave a `TODO(author):` where it is needed.

## Every session

1. Ask which step and which single file. One file per session.
2. Ask for the inputs that skill lists. Do not fill gaps from general knowledge.
3. Draft the file. Mark every gap `TODO(author): <what is needed>`.
4. Run the rules checklist in [reference.md](reference.md). Show each failed check with its line.
5. Wait for the author to approve or edit. Write only what they approved.
6. Remind them: after any change under `.cursor/`, run `python scripts/update_bundle.py` before committing, or `tests/test_bundle_freshness.py` fails. Do not run it yourself unless asked.

## Do not

- Write final Discover artefacts (real needs, outcomes, findings). Those come from real research, written by people.
- Use phase labels from other methods (alpha, beta, live) or name a specific government standard as a requirement.
- Copy text from bimstack without crediting it in `NOTICES`.
