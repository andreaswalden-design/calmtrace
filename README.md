# CalmTrace

CalmTrace is a traceability and report-generation workspace for UX researchers, designers, usability engineers, and human factors teams.

The product focus is a reviewable artifact graph: source evidence linked to usability artifacts, risks, requirements, design decisions, validation evidence, and report sections. CalmTrace helps teams generate and review evidence-backed artifacts without losing the rationale behind decisions.

CalmTrace supports review. It does not prove compliance, replace accountable human review, or automatically validate safety-critical conclusions.

## Current Focus

The first useful workflow is an end-to-end traceable slice:

```text
Raw source material
-> Evidence Items
-> Known Use Problems
-> User Needs
-> Use Scenarios / Critical Tasks
-> Use-Related Risks
-> User Requirements
-> Formative Findings
-> Report Sections
-> Traceability Dashboard
```

## Repository Principles

- Preserve source provenance from evidence to artifacts and report sections.
- Use stable artifact IDs such as `EV-0001`, `UP-0001`, `REQ-0001`, and `RS-0001`.
- Mark AI-created artifacts with `created_with_ai: true` and `review_status: needs_review`.
- Make gaps and assumptions explicit instead of hiding missing evidence.
- Keep reusable product code and templates generic.
- Keep confidential or pilot-specific source data out of version control unless the repository is explicitly configured for it.

## Recommended Vault Layout

```text
calmtrace-vault/
  00_inbox/
  01_sources/
  02_evidence_items/
  03_artifacts/
  04_traceability/
  05_reports/
  06_templates/
  07_decisions/
  08_dashboards/
```

See `AGENTS.md` for the full project instructions, artifact metadata expectations, and traceability rules.

## GitHub Review Expectations

Generated or transformed artifacts are not done until a reviewer can trace important claims back to source evidence quickly. Pull requests should highlight:

- source evidence used
- generated or updated artifact IDs
- links created or changed
- unresolved gaps or assumptions
- review statuses still needing human action
