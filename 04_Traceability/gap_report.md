---
id: TRACE-GAP-REPORT
artifact_type: gap_report
title: Gap Report
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
  - Confirm whether these review gaps should remain open after source validation.
change_reason: Added initial profile review gaps after creating stable source records.
---

# Gap Report

| Gap ID | Area | Description | Linked Artifacts | Review Status |
|---|---|---|---|---|
| GAP-0001 | Source validation | Source metadata records point to screenshots provided in the Codex conversation, but the screenshots and transcriptions still need human validation. | SRC-0001, SRC-0002, SRC-0003, USER-0001, USER-0002, USER-0003 | needs_review |
| GAP-0002 | Terminology | Confirm whether "divers" should remain as written or be localized for the intended report language. | USER-0001, USER-0002, USER-0003 | needs_review |
| GAP-0003 | Profile status | Confirm official or unofficial profile value for nurse and registered nurse profiles. | USER-0002, USER-0003 | needs_review |
| GAP-0004 | Work environment terminology | Confirm whether "NSF" in the HCP source should remain as written or be corrected to "SNF". | USER-0001 | needs_review |
| GAP-0005 | Responsibility wording | Confirm accepted wording for monitor cleaning, patient nutrition, and healthcare-professional abbreviation in nurse-derived profiles. | USER-0002, USER-0003 | needs_review |

## Notes

Review gaps should be closed only after source validation and reviewer acceptance.
