---
name: write-discover-template
description: >-
  Help the author write one template for a Discover artefact
  (.cursor/templates/discover-*-template.md), such as the problem statement,
  research plan, participants log, needs register, journey map, or go/pivot/stop
  gate. Build-order step 3. Use when the operator says "write the template for…"
  or "what should the needs register look like".
---

# Write a Discover template

Step 3 of the Discover build order. A template is the empty form a persona fills in. Read [../discover-authoring/reference.md](../discover-authoring/reference.md) first. Field names must match the ID dictionary (step 1).

Follow the shape of existing AAMAD templates (see `.cursor/templates/prd-template.md`, `user-story-template.md`): a short "Context & Instructions", "Input Requirements", then numbered sections to generate.

## Suggested templates

| Template | Owner | IDs it holds |
|---|---|---|
| problem-statement (incl. discovery goal) | @product-mgr | OUT-, AS- |
| goals-and-measures | @product-mgr | OUT-, M- |
| go-stop-gate (go / pivot / stop) | @product-mgr + operator | cites UN-, OUT-, AS- |
| research-plan | @user.researcher | RP- → AS- |
| screener | @user.researcher | UG- |
| discussion-guide | @user.researcher | RP- |
| consent-notes | @user.researcher (draft), human decides | consent record |
| participants-log | human fills | P-, UG-, consent |
| evidence-log | @user.researcher | EV-, S-, SRC- |
| themes (affinity map) | @user.researcher | TH- → EV- |
| needs-register | @user.researcher | UN-, PP-, UG- |
| journey-map | @service.designer | SERVICE, STAGE, PP-, EV- |
| service-blueprint | @service.designer | STAGE, EV-, AS- |
| constraints-and-opportunities | @service.designer | OP- → OUT-, AS- |
| assumptions-register | @product-mgr / @service.designer | AS-, TS- |
| prototype-test | @service.designer + @user.researcher | TS- → EV-, AS- |

## Ask the author

1. Which artefact? Who fills it in, and who reads it next?
2. Which sections must it have?
3. Which fields are required, and which IDs must each row cite?
4. What makes it "done"? (Becomes the template's acceptance checklist.)
5. What is the filled-in file called? It is saved under `project-context/1.discover/` (Define-facing templates: `project-context/2.define/`).

## Draft shape

```markdown
# AAMAD Discover <Artefact> Template

## Context & Instructions
<who fills this in, when, from which inputs. "Do not invent; cite IDs; leave TODO.">

## Input Requirements
**<Input>**: [path or ID range]

## Sections — Generate All Sections Below

### 1. <Section>
| ID | <field> | <field> | Evidence (EV-) | Status |
|---|---|---|---|---|

## Done when
- [ ] <testable check>

## Open Questions
```

## Check before showing

- Every table that makes a claim about users has an evidence column (EV-, SRC-) and a status column where the dictionary defines one.
- Needs register: solution-free wording prompt ("I need … so that …"), a "retired (date, reason)" column, no delete instruction.
- Story-facing templates: a "Serves UN-" column that cannot be empty.
- Outcomes: an "Is this an output or a solution? (must be no)" prompt and an M- column marked leading/lagging.
- Participants log: pseudonym P- only. Add a visible warning: "No names, emails, phone numbers or other identifying details."
- Synthetic rows are labelled `synthetic` and excluded from validation columns.
- Swap government-specific wording (MDA, citizen, alpha) for neutral terms (provider, user, prototype) unless the author wants it.
- Run the rules checklist.

## Do not

- Fill the template with real content. Example rows say "example only".
