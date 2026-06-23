---
id: TRACE-MATRIX
artifact_type: traceability_matrix
title: Traceability Matrix
status: draft
source_refs:
  - SRC-0001
  - SRC-0002
  - SRC-0003
linked_artifacts:
  - USER-0001
  - USER-0002
  - USER-0003
evidence_strength: unknown
created_by: codex
created_with_ai: true
review_status: needs_review
last_reviewed: null
version: 0.1
confidence: low
assumptions: []
open_questions:
  - Human review of AI-created source/profile links is still pending.
change_reason: Added source-to-profile links and user-profile derivation links.
---

# Traceability Matrix

| From | To | Link Type | Rationale | Review Status |
|---|---|---|---|---|
| USER-0001 | SRC-0001 | references | HCP profile content was transcribed from the HCP source screenshot metadata record. | needs_review |
| USER-0002 | SRC-0002 | references | Nurse profile content was transcribed from the nurse source screenshot metadata record. | needs_review |
| USER-0003 | SRC-0003 | references | Registered nurse profile content was transcribed from the registered nurse source screenshot metadata record. | needs_review |
| USER-0002 | USER-0001 | refines | Nurse is a role-specific profile derived from the broader HCP profile. | needs_review |
| USER-0003 | USER-0002 | refines | Registered nurse is a role-specific profile derived from the broader nurse profile. | needs_review |

## Notes

All links above are AI-created and require human review before acceptance.
