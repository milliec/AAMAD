# Discover authoring reference

Shared by every `write-*` Discover skill. This is a **briefing** for the author, not the ID dictionary itself. The dictionary is written in step 1 and, once it exists, wins over this file.

## Why the Discover phase exists

It comes before Define → Build → Deliver. It gives a traceable line from evidence to needs to stories to build to tests to outcomes and impact. It must work for any project. Its four principles:

1. Reframe the brief as a problem.
2. Learn about the users and the constraints.
3. Find the opportunities.
4. Test the riskiest assumptions with throwaway prototypes.

Do not use alpha/beta/live labels or name a specific government's standards.

## Who does what (agreed)

| Persona | Discover | Define |
|---|---|---|
| `@product-mgr` (extended) | Problem statement, discovery goal, business goals, success measures (leading and lagging), the go/pivot/stop gate with the operator | Writes the PRD and stories. Every story cites at least one UN-. Refuses a story with no UN- link. |
| `@user.researcher` (new; research **assistant**) | Drafts the research plan, screener, discussion guide, consent/GDPR notes. Affinity clustering. Synthesises needs, pain points, evidence. Runs testing sessions with the service designer's prototypes. | — |
| `@service.designer` (new) | Journey maps, service blueprints (frontstage/backstage, channels, touchpoints), hard vs soft constraints, opportunities, throwaway prototypes that test the riskiest AS- | — |

There is no separate delivery manager or discovery lead.

### Human checkpoints

People recruit, decide consent, run sessions and judge findings. At each checkpoint the agent **stops and waits for files**:

- a participants log with pseudonym P- IDs only (no names, emails, phone numbers)
- consent records for each P-
- anonymised transcripts, one per S- session

Synthesis refuses to run unless every P- it cites has a recorded consent.

## ID families (as agreed; fields are TODO until the dictionary is written)

| Prefix | Means | Key links |
|---|---|---|
| RP- | Research plan | targets AS- |
| (screener) | Screener for recruitment | belongs to RP-. `TODO(author):` prefix? |
| P- | Participant: pseudonym, user group, consent | in UG-; has consent record |
| (consent record) | Consent per P- | `TODO(author):` prefix? |
| S- | Research session | with P-; produces transcript |
| SRC- | Existing source (analytics, call-centre data) | produces EV- |
| EV- | One quote or observation. Type: observed / said / data / synthetic | from S-/P- or SRC- or TS- |
| TH- | Theme (affinity cluster) | groups EV- |
| UG- | User group, including service staff | — |
| UN- | User need | backed by EV-; for UG- |
| PP- | Pain point | backed by EV-; at STAGE |
| SERVICE, STAGE | The service and its journey stages, channels | `TODO(author):` prefixes? |
| OUT- | Outcome: service- or stage-level; user or provider type | measured by M- |
| M- | Measure: leading or lagging | attached to OUT- |
| OP- | Opportunity | contributes to OUT-; relies on AS- |
| AS- | Assumption: untested / confirmed / disproved | tested by TS- |
| TS- | Test (prototype session) | produces EV- |
| US- | User story | serves UN-; has AC- |
| AC- | Acceptance criterion | belongs to US- |
| OUTPUT | Thing built | delivers US-. `TODO(author):` prefix? |

Trace chain: **OUTPUT → US- → UN- → OUT- → M-**, and back down: UN- → EV- → S-/SRC- → P- (with consent).

## Rules checklist (run on every draft)

Mark each `pass`, `fail (line)`, or `n/a`.

**Citations**
- [ ] Every claim about users cites an ID (EV-, UN-, PP-, SRC-…). Nothing is invented.
- [ ] Every cited ID exists in the ID dictionary, or is marked `TODO(author)`.

**Needs are not stories** (gov.uk service manual, "Start by learning user needs")
- [ ] A UN- is solution-free: no screens, buttons, apps, features, or tech.
- [ ] A UN- is in the user's words: "I need … so that …" (optional "As a … / When … / Because …").
- [ ] A UN- is backed by at least one non-synthetic EV-.
- [ ] A UN- is never deleted, only retired (with reason and date).
- [ ] A US- is in the team's words, has AC-, and cites at least one UN-. Needs and stories are many-to-many.
- [ ] Opinions that did not come from users (stakeholders, team, the brief) are AS-, not UN-.

**Outcomes** (Kate Tarling, Home Office 2017)
- [ ] An OUT- is an end result for users or the provider. It is not an output ("launch a portal"), a goal ("be digital first"), or a solution.
- [ ] Each OUT- has at least one M-, marked leading or lagging.

**Data protection**
- [ ] Only anonymised data reaches agents. P- IDs are pseudonyms. No names, contact details, or identifying specifics.
- [ ] Synthesis cites only P- with a recorded consent.
- [ ] Consent/GDPR notes are drafts for a human to decide. The agent never decides consent.

**Synthetic research**
- [ ] Synthetic personas and findings are labelled `synthetic` (EV- type synthetic).
- [ ] Synthetic EV- never validates a UN- or confirms an AS-. It is rehearsal only.

**Prototypes**
- [ ] Prototypes are throwaway and test a named AS-. They are never handed to `@frontend.eng` as code.

**Generic**
- [ ] No alpha/beta/live labels; no specific government's standards as requirements.
- [ ] Gaps are `TODO(author):`, not guesses.

## Where files go (proposed; confirm with the author)

| Kind | Path |
|---|---|
| ID dictionary | `.cursor/rules/discover-id-dictionary.mdc` |
| Rule files | `.cursor/rules/discover-<topic>.mdc` |
| Templates | `.cursor/templates/discover-<artefact>-template.md` |
| Skills | `.cursor/skills/<skill-name>/SKILL.md` (+ `reference.md`) |
| Personas | `.cursor/agents/user-researcher.md`, `.cursor/agents/service-designer.md`; extend `.cursor/agents/product-mgr.md` |
| Discover outputs in a project | `TODO(author):` e.g. `project-context/0.discover/`. Note `project-context/0.review/` is already used by brownfield. |

After any change under `.cursor/`, `python scripts/update_bundle.py` must be run before committing.

## Sources

- bimstack (MIT, © 2026 GovTech Barbados Limited and contributors): https://github.com/govtech-bb/bimstack. Model for the research, mapping and prototyping skills. See [../write-discover-skill/bimstack-map.md](../write-discover-skill/bimstack-map.md).
- GOV.UK Service Manual, "Start by learning user needs": https://www.gov.uk/service-manual/user-research/start-by-learning-user-needs
- Kate Tarling, outcomes work at the Home Office (2017). `TODO(author):` add the exact link you want cited.
