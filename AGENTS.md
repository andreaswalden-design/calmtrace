# AGENTS.md — CalmTrace Codex Project

## 1. Project purpose

CalmTrace is a traceability and report-generation workspace for UX researchers, designers, and usability / human factors engineers working on medical and non-medical products.

The core value is not generic AI writing. The core value is a reviewable artifact graph that connects source evidence to usability artifacts, risks, requirements, design decisions, validation evidence, and report sections.

CalmTrace should help teams move from scattered research evidence to traceable, review-ready artifacts without losing the rationale behind decisions.

Primary internal pilot context: a Philips project may be used to validate workflow pain and usefulness. Do not bake Philips-specific templates, confidential data, naming, or process assumptions into reusable product code unless explicitly isolated in a local pilot-only area.

## 2. Product positioning

CalmTrace is:

- a traceability layer for UX, usability, and human factors work
- an evidence-to-artifact workspace
- a report-generation assistant with source grounding
- a single source of truth for usability engineering artifacts
- a review workflow for AI-assisted artifact creation

CalmTrace is not:

- an automatic compliance engine
- a replacement for accountable human review
- a generic research repository
- a generic note-taking system
- a full QMS or requirements-management system
- a tool that claims to prove IEC 62366, FDA HFE, ISO 14971, or other regulatory compliance

Use cautious language. Prefer “supports review,” “helps generate,” “links evidence,” and “identifies gaps.” Avoid “ensures compliance,” “proves safety,” or “automatically validates.”

## 3. Target users

Design for these primary users:

- UX researchers who collect observations, interview notes, and study findings
- Product designers who need design rationale and decision traceability
- Usability engineers / human factors engineers who create usability engineering artifacts
- Regulated product teams that need evidence-backed documentation
- Non-medical product teams with safety-relevant or complex UX workflows

Assume users are overloaded and skeptical of new tooling. The first-week experience must reduce hunting, rework, and traceability gaps.

## 4. Core thesis

Folders, Obsidian, GitHub, and Codex are implementation tools. The product is the artifact graph.

Every important generated statement must be connected to:

- a source or evidence item
- an artifact ID
- a confidence or evidence-strength indicator
- a review status
- a version or change history

A generated report section without source links is not done.

## 5. First pilot scope

Do not build the full lifecycle first. Prioritize one end-to-end slice:

```text
Raw source material
→ Evidence Items
→ Known Use Problems
→ User Needs
→ Use Scenarios / Critical Tasks
→ Use-Related Risks
→ User Requirements
→ Formative Findings
→ Report Sections
→ Traceability Dashboard
```

Defer full summative validation report generation, full UEF automation, and enterprise integrations until the traceable slice works.

## 6. Core artifact types

Use stable IDs. Do not rename IDs casually. Human-readable titles may change; IDs should not.

Recommended prefixes:

| Prefix | Artifact type |
|---|---|
| `SRC` | Source document or raw input |
| `EV` | Evidence item |
| `UP` | Known use problem / use error / pain point |
| `UN` | User need |
| `US` | Use scenario |
| `CT` | Critical task |
| `RISK` | Use-related risk |
| `REQ` | User requirement or usability requirement |
| `UI` | User interface specification item |
| `FF` | Formative finding |
| `SF` | Summative finding |
| `RS` | Report section |
| `DEC` | Design, research, or risk decision |

## 7. Required metadata

Every structured artifact markdown file should include YAML frontmatter.

Minimum fields:

```yaml
---
id: EV-0001
artifact_type: evidence_item
title: Short descriptive title
status: draft
source_refs: []
linked_artifacts: []
evidence_strength: unknown
created_by: human
created_with_ai: false
review_status: needs_review
last_reviewed: null
version: 0.1
---
```

Preferred additional fields when relevant:

```yaml
product_area: null
user_group: null
use_environment: null
research_method: null
session_id: null
participant_id: null
risk_ids: []
requirement_ids: []
report_section_ids: []
confidence: low
assumptions: []
open_questions: []
change_reason: null
```

Allowed review statuses:

```text
needs_review
reviewed
accepted
rejected
superseded
blocked
```

Allowed evidence strength values:

```text
unknown
weak
medium
strong
conflicting
```

## 8. Vault structure

Prefer this default structure unless an existing repository already uses a different structure:

```text
calmtrace-vault/
  00_inbox/
    raw_notes/
    transcripts/
    screenshots/
    exported_tables/

  01_sources/
    interviews/
    observations/
    complaints/
    prior_reports/
    standards_inputs/
    design_inputs/

  02_evidence_items/
    EV-0001.md

  03_artifacts/
    use_specification/
    known_use_errors_use_problems/
    user_needs/
    use_scenarios/
    critical_tasks/
    use_related_risk_analysis/
    user_requirements/
    design_concepts_prototypes/
    ui_specification/
    formative_evaluation_results/
    summative_validation_results/

  04_traceability/
    traceability_matrix.md
    orphaned_items.md
    gap_report.md
    change_impact.md

  05_reports/
    formative_report/
    summative_report/
    usability_engineering_file/

  06_templates/
    evidence_item_template.md
    user_need_template.md
    critical_task_template.md
    risk_template.md
    requirement_template.md
    report_section_template.md

  07_decisions/
    design_decisions/
    research_decisions/
    risk_decisions/

  08_dashboards/
    uef_status.md
    open_gaps.md
    review_queue.md
```

Keep raw source material separate from generated or normalized artifacts.

## 9. Obsidian compatibility

Markdown must remain usable in Obsidian.

Prefer:

- clean Markdown
- YAML frontmatter
- wikilinks where useful, for example `[[EV-0001]]`
- tables only when they remain readable
- Dataview-compatible fields
- short files with stable IDs

Avoid:

- hidden state that only a script can understand
- generated prose with no artifact IDs
- overlong markdown tables that are hard to review
- brittle links based only on titles

## 10. Codex / agent behavior

When working in this repo:

1. Inspect the existing structure before making changes.
2. Prefer small, reviewable diffs.
3. Do not delete or overwrite raw source material.
4. Do not invent sources, quotes, participants, findings, risks, or requirements.
5. If evidence is missing, create an explicit gap or open question.
6. Mark AI-created artifacts with `created_with_ai: true` and `review_status: needs_review`.
7. Preserve provenance from source to artifact to report section.
8. Prefer deterministic scripts over one-off manual transformations.
9. Make scripts idempotent where practical.
10. Add or update tests when changing parsing, schema validation, link generation, or report generation.

If a requested task is ambiguous, choose the safer traceability-preserving option and document assumptions in the output.

## 11. AI generation rules

AI may suggest:

- evidence item extraction
- artifact links
- duplicate detection
- gap detection
- report section drafts
- summaries of reviewed evidence
- change impact analysis

AI must not silently decide:

- final risk acceptability
- final validation outcome
- final regulatory claim
- final requirement approval
- final summative conclusion
- final compliance status

Every generated artifact or report section must include:

- source evidence references
- linked artifact IDs
- assumptions, if any
- confidence level where useful
- review status

Bad output:

```text
Users struggled with alarm configuration.
```

Good output:

```text
Three participants reported difficulty identifying the correct alarm configuration during setup.
Sources: EV-0012, EV-0018, EV-0021.
Linked artifacts: UP-0004, CT-0003, RISK-0011.
Review status: needs_review.
```

## 12. Traceability rules

A useful CalmTrace link has direction, rationale, and review state.

Minimum link representation:

```yaml
links:
  - from: EV-0012
    to: UP-0004
    link_type: supports
    rationale: Participant described confusion during alarm setup.
    created_with_ai: true
    review_status: needs_review
```

Recommended link types:

```text
supports
contradicts
refines
implements
mitigates
validates
invalidates
supersedes
references
requires_review
```

The gap checker should identify at least:

- evidence items with no artifact link
- user needs without source evidence
- use problems without linked critical tasks
- critical tasks without risk links
- risks without mitigation or usability evidence
- requirements without user need links
- UI specification items without requirement links
- formative findings without linked tasks or requirements
- report claims without source evidence
- AI-generated artifacts still waiting for review

## 13. Report generation rules

Generate report sections, not full reports, until the workflow is validated.

Useful first sections:

- Context of use
- Known use problems / use errors
- User needs
- Use scenarios and critical tasks
- Use-related risk analysis summary
- User requirements summary
- Formative evaluation results
- Open issues and unresolved evidence gaps

Every generated report section should include:

- section purpose
- source artifacts used
- generated narrative
- traceability table or source list
- unresolved gaps
- review status

Do not create polished unsupported prose. Reviewable, sourced prose is better than elegant but unverifiable prose.

## 14. Dashboards to prioritize

The first dashboard should make the value obvious. Prioritize:

- open review queue
- orphaned evidence
- missing links
- weak evidence areas
- unresolved contradictions
- report sections with unsupported claims
- change impact from modified sources
- accepted vs rejected AI suggestions

A dashboard that shows traceability gaps is more valuable than a beautiful generated report.

## 15. Git and version-control expectations

Use GitHub for versioning and review, not as a substitute for formal regulated audit trails.

Recommended branch conventions:

```text
main              stable reviewed vault and code
working/*         active processing or exploration
report/*          report generation work
review/*          human review and correction batches
```

Generated changes should be easy to inspect in pull requests.

Do not commit confidential source data unless the repository is explicitly configured for that purpose.

## 16. Privacy, confidentiality, and IP boundaries

CalmTrace may be piloted internally, but reusable product code and templates must remain generic.

Rules:

- Do not include Philips confidential content in reusable examples.
- Do not convert internal Philips artifacts into public templates.
- Use synthetic or anonymized examples for documentation.
- Keep pilot data in ignored or clearly isolated areas when required.
- Do not infer personal or sensitive participant information unless explicitly present and necessary.
- Do not expose raw interview content in generated reports unless approved.

When in doubt, preserve the data locally and generate only abstracted, anonymized examples.

## 17. Quality bar

A change is not done until it improves at least one of these outcomes:

- faster source retrieval
- stronger traceability
- fewer orphaned artifacts
- clearer review status
- better report generation with evidence links
- easier change impact analysis
- lower manual documentation effort

Definition of done for artifact-generation features:

- schema is documented
- output is deterministic enough for review
- generated items include IDs
- generated items include source references
- generated items are marked as AI-generated when applicable
- generated items are marked `needs_review` by default
- gaps are explicit, not hidden
- tests or validation examples exist

## 18. Useful commands

Exact commands depend on the repository. Before running commands, inspect package files and scripts.

Preferred discovery sequence:

```bash
ls
find . -maxdepth 3 -type f \( -name 'package.json' -o -name 'pyproject.toml' -o -name 'requirements.txt' -o -name 'Makefile' \)
```

If JavaScript / TypeScript is present, check:

```bash
npm run
pnpm run
```

If Python is present, check:

```bash
python -m pytest
python -m ruff check .
python -m mypy .
```

Only run available commands. Do not invent mandatory commands that are not configured.

## 19. First implementation priorities

Build in this order:

1. Markdown/YAML artifact schema
2. Source ingestion and evidence item extraction
3. Traceability link proposal and review status
4. Gap checker
5. Obsidian dashboard generation
6. Report section generation
7. Change impact analysis

Avoid broad platform work until these are useful with a small pilot dataset.

## 20. North-star metric

The core metric is not “Can AI generate a report?”

The core metric is:

> Can a reviewer verify every important claim in less than 30 seconds?

Optimize for that.
