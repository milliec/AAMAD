# bimstack → AAMAD Discover map

Checked against https://github.com/govtech-bb/bimstack at commit `4063001` (main, 24 Nov 2026). Licence: MIT, © 2026 GovTech Barbados Limited and contributors. Suggested AAMAD names are proposals; the author decides.

## Structural differences

| bimstack | AAMAD Discover (agreed) |
|---|---|
| Claude Code plugin. Agents are `agents/*.md` with `name / description / tools / model` headers. Skills are namespaced `bimstack:…`. | Cursor-first. Personas use the six-part YAML anatomy (agent, instructions, actions, inputs, outputs, prohibited-actions). Skills live in `.cursor/skills/`. |
| One **service designer** does research *and* mapping *and* leads discovery. | Split: `@user.researcher` (research assistant) and `@service.designer`. `@product-mgr` owns problem, goals, measures and the gate. |
| A **delivery manager** owns phase gates and "monitor and measure". | No delivery manager. `@product-mgr` owns the go/pivot/stop gate and measures, with the operator. |
| Phases: Discovery / Alpha / Beta / Live (GDS). Deliverables cite Barbados Standards and GOV.UK Principles by number. | Generic Discover → Define → Build → Deliver. No alpha/GDS labels, no standards numbering. |
| Loose citations: `[P3 interview]`, `[ASSUMPTION]`, P1…Pn. | Typed IDs (EV-, AS-, P-, S- …) from the ID dictionary. |
| No ID model, no needs register, no outcomes or leading/lagging measures, no screener, no participants log, no consent gate. | All of these are required. They are new work, not adaptation. |
| Prototypes can graduate: `build-for-production` turns a tested prototype into a production front end. | Prototypes are throwaway and never go to `@frontend.eng` as code. |
| Synthetic personas grounded in Barbados census data, Barbadian names. | Generic population sources; EV- type `synthetic`; never validates a need. |
| Iron law "five users minimum" before claiming "users want X". | `TODO(author):` keep, change, or drop? |

## Skill by skill

| bimstack skill (lines) | Suggested AAMAD skill · persona | Keep | Change | Drop |
|---|---|---|---|---|
| `research-planning` (107) | `plan-research` · @user.researcher | Objectives before questions, linked to a decision; max 2–3 objectives; behaviour-not-opinion rewrites; "if this didn't exist"; leading-language check; false close | Objectives become RP- that target named AS-. Guide cites RP-. | Barbados/GOV.UK standard numbers; `plain-language-check` link. Digital-literacy warm-up: `TODO(author)` optional? |
| (none; `discovery-kit` §3 "Ethics and consent", `govtech-research-plans` ethics block) | `draft-screener-and-consent` · @user.researcher | Consent prompts (record audio? anonymous quotes? stop any time?); "do not ask / do not report" for the sensitive topic | Draft only; a human decides. Generic data-protection wording, not BDPA 2019. | Barbados law references |
| `transcript-analysis` (78) | `analyse-transcript` · @user.researcher | Stated vs demonstrated (→ EV- type said vs observed); workarounds; friction that changed behaviour; contradictions; confirms / contradicts / new / extends; coach the human's interpretation; never surface identifying details | Each finding becomes an EV- tied to S- and P-. Front-matter objectives → RP-. Consent check first. | Standard numbers |
| `synthesize-research` (117) | `synthesise-needs` · @user.researcher | Read everything, never sample; "N of M" tally per theme; **findings checkpoint before writing**; quote policy (clean lightly, never invent) | Output TH- (themes), UN- (needs), PP- (pain points), each citing EV-. Quote attribution P-ID. Refuse without consent per cited P-. | docx/pptx deck build, GovTech logos, Mac environment notes, bundled scripts (`TODO(author)`: is `extract_sources.py` worth porting?) |
| `journey-map` (83) | `map-journey` · @service.designer | Evidence per step or mark as assumption; start before and end after the service; every channel; emotions as quoted data; current state = what is | Steps → STAGE; evidence → EV-; `[ASSUMPTION]` → AS-; pain → PP-; opportunities → OP-. "Future state" without "alpha". | GovBB HTML styling |
| `service-blueprint` (78) | `blueprint-service` · @service.designer | Three lines (interaction, visibility, internal interaction); backstage claims need backstage evidence; name the systems; time row; failure demand; future-state owners | Failure points → PP-; unverified → AS-; add a **hard vs soft constraints** row (not in bimstack). | "Alpha onwards"; Standard 7 notes; GovBB HTML |
| `ecosystem-map` (82) | `map-ecosystem` (or fold into constraints/opportunities) · @service.designer | Need at the centre; hunt informal actors; map flows; flag informal personal-data flows | Actors → UG- (incl. service staff); flows of personal data → data-protection note | Standard 7 column; GovBB HTML |
| `brief-to-prototypes` (262) | `prototype-assumptions` · @service.designer | Always more than one genuinely different hypothesis; assumptions panel; "this is fake" markers; test plan | Each prototype tests named high-risk AS-; test plan → TS-; results → EV-. Throwaway only. | GovBB chrome and CSS, alpha banner, Trident ID, link to `build-for-production` |
| `prototype-iteration` (256) | `iterate-prototype` · @service.designer (+ @user.researcher runs sessions) | Review synthesis before iterating; changelog of what changed and why; don't merge candidates | Feedback → EV- from TS-; AS- status updated only from non-synthetic EV-. Consent check on transcripts. | Content-designer + developer agents leading iteration (AAMAD has neither in Discover) |
| `synthetic-research` (241) | `rehearse-synthetic` · @user.researcher | Standing disclaimer; never "the user said"; label everything synthetic; "test this with real people" list | EV- type `synthetic`; can't validate UN- or confirm AS-; generic population sources | Barbados census, Barbadian names, parish |

## Not in the brief but relevant

- `discovery-kit`: problem statement (§1), stakeholder map (§2), research plan (§3), interview guide (§4), discovery report with "Proceed / Redesign / Don't build" (§5). Good model for @product-mgr's problem statement and the go/pivot/stop gate.
- `research-coach`: router across the research cycle. Possible model for how @user.researcher sequences its skills.
- `references/`: mostly GovBB-specific (`barbados-service-standards.md`, `govbb-design-guide.md`, `govbb-design-tokens.yaml`, `house-style.md`, `gds-way-phases.md`). `govuk-design-principles.md` restates GOV.UK content; cite the GOV.UK source directly rather than copying.
- bimstack also points to external plugins (`design:user-research`, `design:research-synthesis`) that are not in the repo.
