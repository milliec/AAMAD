---
name: write-persona
description: >-
  Help the author write or extend one AAMAD persona file (.cursor/agents/*.md)
  in the six-part anatomy: agent, instructions, actions, inputs, outputs,
  prohibited-actions. For Discover: create @user.researcher and
  @service.designer, and extend @product-mgr. Build-order step 5. Use when the
  operator says "write the researcher persona", "extend product-mgr for
  Discover", or "six-part anatomy".
---

# Write a persona

Step 5 of the Discover build order. A persona file tells an agent who it is, what it may do, what it reads and writes, and what it must never do. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first. Personas cite the rules (step 2), templates (step 3) and skills (step 4), so those should exist. Anything missing becomes `TODO(author)`.

Copy the layout of an existing persona, e.g. `.cursor/agents/product-mgr.md`: a YAML header with the six parts, then a body with "Naming convention", "Supported Commands" and "Usage".

## The six parts (plain meaning)

| Part | Means | Example |
|---|---|---|
| `agent` | name, id, one-line role | `id: user-researcher`; role: research assistant |
| `instructions` | standing behaviour, one line each | "Wait for the participants log before synthesis." |
| `actions` | the `*commands` it answers, each with its output path | `plan-research # → <Discover folder>/research-plan.md` |
| `inputs` | files it reads | templates, rules, participants log |
| `outputs` | files it writes | research plan, evidence log, needs register |
| `prohibited-actions` | hard "never" lines | "Recruit participants or decide consent." |

## Ask the author

1. New persona or extend an existing one? Which?
2. Role in one line. What it owns, and what it hands to whom.
3. Its commands, and the skill each one follows.
4. Inputs and outputs (paths). Where does it wait for a human file?
5. What must it never do?
6. Invocation name: dotted (`@user.researcher`) and file id hyphenated (`user-researcher`), matching `dev-crew.md`.

## Agreed content to prompt for

Offer these from the agreed decisions; the author confirms each.

- **@product-mgr (extend):** Discover actions for problem statement + discovery goal, business goals, success measures (OUT- with M-, leading and lagging), and the go/pivot/stop gate with the operator. Define: every story cites at least one UN-; refuse a story without one. Add the gate file as a required input to `*create-prd`. Keep existing brownfield instructions untouched.
- **@user.researcher (new):** research assistant. Drafts research plan (RP- → AS-), screener, discussion guide, consent/GDPR notes; affinity clustering (TH-); synthesis (UN-, PP-, EV-); runs prototype test sessions (TS-) with the service designer. Waits for the participants log (P- pseudonyms only) and anonymised transcripts. Refuses synthesis without consent for each cited P-.
- **@service.designer (new):** journey maps (SERVICE, STAGE), service blueprints (frontstage/backstage, channels, touchpoints), hard vs soft constraints, opportunities (OP- → OUT-, relies on AS-), throwaway prototypes testing the riskiest AS-.

## Prohibited actions to prompt for

- Invent users, quotes, evidence, needs or measures; write anything about users without an ID.
- Read or store names, contact details or other identifying data.
- Recruit, decide consent, run live sessions, or make the final judgement (researcher).
- Treat synthetic research as evidence for a UN- or AS-.
- Hand prototype code to `@frontend.eng` (service designer).
- Write a story with no UN- (product manager).

## Check before showing

- All six parts present; every action has an output path; every output appears in `outputs`.
- Every command points to a skill that exists, or `TODO(author)`.
- No overlap with `@ux.designer` left unexplained. If both could own a task (e.g. journey maps vs `ux.md`), add a `TODO(author)` to settle it.
- Run the rules checklist.

## After approval

Remind the author that step 6 (wiring) is still needed: `dev-crew.md`, `epics-index.mdc`, `aamad.config.yml` template, then `python scripts/update_bundle.py`.

## Do not

- Remove or reword existing `@product-mgr` instructions unless the author asks.
- Give a persona permission to write another persona's outputs.
