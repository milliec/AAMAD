# Discover skills to write

Each Discover skill teaches one research or service-design method: how to plan research, analyse transcripts, synthesise needs, map journeys, blueprint services, or test assumptions with prototypes. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first for the ID model, rules and agreed decisions.

## Suggested skills

| Suggested skill | Persona | Purpose | Key steps |
|---|---|---|---|
| `plan-research` | @user.researcher | Draft research plan (RP-) targeting named assumptions (AS-). Write objectives before questions. Max 2–3 objectives. Rewrite opinion → behaviour. Ask "if this didn't exist, what would happen?" Check for leading language and false closes. | 1. List the AS- this plan targets<br>2. Draft objectives (RP-) linked to decisions<br>3. Draft discussion-guide questions<br>4. Review for bias |
| `draft-screener-and-consent` | @user.researcher | Draft screener for recruitment and consent prompts. **Draft only; a human decides.** Record consent: audio? anonymous quotes? right to stop any time? List sensitive topics with "do not ask / do not report" guidance. | 1. Draft screener questions tied to UG-<br>2. Draft consent prompts<br>3. Mark sensitive topics<br>**Human checkpoint: consent records** |
| `analyse-transcript` | @user.researcher | Extract findings (EV-) from one anonymised transcript. Distinguish stated (type: said) vs demonstrated (type: observed). Capture workarounds, friction that changed behaviour, contradictions. Each finding cites session (S-) and participant (P-). Check consent first. Never surface identifying details. | 1. Check consent for P-<br>2. Read front-matter objectives (RP-)<br>3. Extract EV- (said / observed)<br>4. Mark each: confirms / contradicts / new / extends<br>**Human checkpoint: anonymised transcripts only** |
| `synthesise-needs` | @user.researcher | Cluster evidence into themes (TH-), then write user needs (UN-) and pain points (PP-). Read all transcripts, never sample. Tally "N of M participants" per theme. **Findings checkpoint before writing:** review all evidence with the author. Quote policy: clean lightly, never invent. Each UN- cites at least one non-synthetic EV-. Refuse synthesis without consent for each cited P-. | 1. Check consent for every P- cited<br>2. Read all evidence (EV-)<br>3. Cluster into themes (TH-)<br>4. **Findings checkpoint**<br>5. Write UN- and PP-, each citing EV-<br>6. Attribute quotes to P- pseudonym |
| `map-journey` | @service.designer | Map the user journey with evidence per step, or mark as assumption. Start before and end after the service. Show every channel. Record emotions as quoted data only. Current state = what is now, not what should be. Steps → STAGE; evidence → EV-; assumptions → AS-; pain → PP-; opportunities → OP-. | 1. Define SERVICE and stages (STAGE)<br>2. Evidence or assumption per step<br>3. Map all channels<br>4. Record emotions (quoted data)<br>5. Mark pain points (PP-) and opportunities (OP-) |
| `blueprint-service` | @service.designer | Service blueprint with three lines: user interaction (frontstage), line of visibility, internal interaction (backstage). Backstage claims need backstage evidence (staff interviews, process docs). Name the systems. Add time row. Mark failure demand (PP-) and unverified steps (AS-). Add hard vs soft constraints row. Document future-state owners. | 1. Three lines (front/visible/back)<br>2. Name systems<br>3. Time row<br>4. Failure demand → PP-<br>5. Unverified → AS-<br>6. Hard vs soft constraints<br>7. Future owners |
| `map-ecosystem` | @service.designer | Ecosystem map with the need at the centre. Hunt informal actors (friends, brokers, fixers). Map flows, especially informal personal-data flows. Actors become user groups (UG-, including service staff). Flag data-protection concerns. | 1. Put user need at centre<br>2. Map formal and informal actors → UG-<br>3. Map flows<br>4. Flag personal-data flows<br>5. Data-protection note |
| `prototype-assumptions` | @service.designer | Brief for throwaway prototypes that test high-risk assumptions. Always create more than one genuinely different hypothesis. Assumptions panel on each prototype. Test plan (TS-) for each. "This is fake" markers visible. Each prototype tests named AS-; results → EV-. Prototypes are throwaway only, never production code. | 1. List high-risk AS- to test<br>2. Design genuinely different prototypes<br>3. Assumptions panel per prototype<br>4. Test plan (TS-) per prototype<br>5. "This is fake" markers<br>**Prototypes are throwaway** |
| `iterate-prototype` | @service.designer | Iterate a prototype after testing. Review synthesis before changing anything. Changelog: what changed and why. Don't merge candidates. Feedback → EV- from TS-; AS- status updated only from non-synthetic EV-. Check consent on transcripts before using. | 1. Review synthesis first<br>2. List feedback (EV- from TS-)<br>3. Update AS- status<br>4. Changelog (what, why)<br>5. Consent check on transcripts |
| `rehearse-synthetic` | @user.researcher | Generate synthetic personas or scenarios for rehearsal only. Standing disclaimer on every output. Never claim "the user said". Label everything with EV- type `synthetic`. List "test this with real people" topics. Synthetic evidence never validates UN- or confirms AS-. Generic population sources only. | 1. Standing disclaimer<br>2. Generate synthetic personas/scenarios<br>3. Label EV- type `synthetic`<br>4. List real-testing needs<br>**Synthetic = rehearsal only** |

## Craft principles to embed

When writing any Discover skill, fold these into the method steps:

- **Behaviour over opinion.** Ask what someone did, not what they think about it. Rewrite leading questions.
- **Workarounds reveal needs.** If the user built a spreadsheet to track something the system doesn't, that's a pain point (PP-).
- **"If this didn't exist, what would happen?"** Tests whether a feature is load-bearing.
- **Findings checkpoint.** Before writing the synthesis, review all evidence with a human. Never rush from transcripts to needs.
- **Multiple prototypes.** Test competing hypotheses, not one "best" design.
- **Throwaway prototypes.** Prototypes test assumptions (AS-); they never go to `@frontend.eng` as code.
- **Consent gate.** Synthesis checks consent for every cited P- and refuses to run if any are missing.
- **Anonymisation.** Only pseudonyms (P-) reach the agent. No names, contact details, or identifying specifics.
- **Synthetic = rehearsal.** Synthetic evidence (EV- type `synthetic`) never validates a user need (UN-) or confirms an assumption (AS-).

## Gates and checkpoints

Every Discover skill must respect these human gates:

- **Consent check:** Before using any P- in synthesis, verify consent record exists. Refuse with missing P- named.
- **Anonymisation:** Only anonymised transcripts. Agent never sees names, emails, phone numbers.
- **Findings checkpoint:** Before writing needs or themes, review all evidence with the author.
- **Draft only (screener/consent):** The agent drafts; a human decides consent policy and legal compliance.
- **Throwaway prototypes:** Service designer makes clear prototypes are for testing only, never production code.
- **Synthetic disclaimer:** Every synthetic output carries a standing "this is rehearsal" disclaimer and lists what must be tested with real people.

## Author decides

Each suggested name, persona assignment, and method detail is a proposal. The author confirms or changes it. Gaps become `TODO(author):` markers, not invented content.
