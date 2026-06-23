---
id: USER-0001
artifact_type: user_profile
title: HCP profile
status: draft
source_refs:
  - SRC-0001
linked_artifacts: []
links:
  - from: USER-0001
    to: SRC-0001
    link_type: references
    rationale: HCP profile content was transcribed from the source screenshot metadata record.
    created_with_ai: true
    review_status: needs_review
evidence_strength: unknown
created_by: codex
created_with_ai: true
review_status: needs_review
last_reviewed: null
version: 0.1
product_area: null
user_group: Healthcare professional
use_environment: Clinical departments, outpatient care, skilled nursing facilities, and doctors offices
research_method: null
session_id: null
participant_id: null
risk_ids: []
requirement_ids: []
report_section_ids: []
confidence: low
assumptions:
  - HCP is interpreted as Healthcare Professional.
open_questions:
  - Confirm source record SRC-0001 against the original user profile table.
  - Confirm whether NSF should remain as written or be corrected to SNF.
change_reason: Created HCP profile from user-provided example table.
---

# USER-0001 - HCP Profile

## Profile Summary

This profile describes a primary clinical user group: healthcare professionals who provide patient care, perform patient assessment, and support treatment in clinical and outpatient environments.

## User Profile

| Field | Description | Source Refs | Review Status |
|---|---|---|---|
| User | Primary user, clinical personnel | SRC-0001 | needs_review |
| Alternative names | Healthcare Professional, Caregiver, Clinician | SRC-0001 | needs_review |
| User type | Primary user | SRC-0001 | needs_review |
| Usage frequency | Frequent user | SRC-0001 | needs_review |
| Sexes or gender considerations | Female, male, divers | SRC-0001 | needs_review |
| Age span | Start of professional life (~17-23 years) to end of professional life (~65/67 years) | SRC-0001 | needs_review |
| Nationality, language, or regional considerations | Not restricted | SRC-0001 | needs_review |
| Potential cognitive, sensory, or physical constraints | See Accessibility and Use Considerations. | SRC-0001 | needs_review |
| Training or qualification | Healthcare professional with several years of vocational training. Different level of domain knowledge, novice to expert. Inexperienced and experienced with similar devices. | SRC-0001 | needs_review |
| Country-specific training description | Not specified. | SRC-0001 | needs_review |
| Responsibilities | Provide care for the patient, patient assessment and treatment. | SRC-0001 | needs_review |
| Work environment | See Work Environment Details. | SRC-0001 | needs_review |
| Work equipment | See Work Equipment Details. | SRC-0001 | needs_review |
| Official or unofficial profile | Unofficial profile | SRC-0001 | needs_review |

## Work Environment Details

Primary users work in clinical departments and, depending on specification, also outpatient care (home), skilled nursing facilities (NSF), or doctors offices. Examples are:

- Cardiac Ward
- Cath Lab or other diagnostic areas
- Diagnostic Imaging
- Emergency Department (ED) / Emergency Trauma
- Emergency Medical Services (EMS)
- General Ward (GW)
- Gyn. doctors office / practice
- Holding Area / Induction Room
- Home (Outpatient Care)
- Intermediate Care Unit (IMCU) / Step Down Unit (SDU)
- Intensive Care Unit (ICU)
- Labor Room (DLR) / Maternity Ward
- Medical ICU (MICU) / Cardiac ICU / Surgical ICU / Pediatrics ICU ...
- MRI Room
- Neonatal ICU (NICU)
- Nursing Home/Skilled Nursing Facility (SNF)
- Obstetric Ward
- Operating Areas / Ambulatory Surgery
- Operating Room (OR)
- Outpatient surgery centers
- Post Anesthetic Care Unit (PACU)
- Recovery Room (RR)
- Telemetry Unit

## Work Equipment Details

- Working clothes, including working scrubs, aprons, OR scrubs, and uniforms
- Gloves
- Masks
- Caps
- Phones, with some users also using pagers and computers
- Specific clinical instruments/tools

## Accessibility and Use Considerations

- Vision impairment, including glasses and dyschromatopsia
- Hearing impairment, including hearing aid
- Age-related motor and sensory disabilities
- High stress level

## Linked Artifacts

| Artifact ID | Relationship | Rationale | Review Status |
|---|---|---|---|
| SRC-0001 | references | HCP profile content was transcribed from this source metadata record. | needs_review |

## Evidence Notes

This profile was created from a user-provided screenshot of a user profile table in the current Codex conversation. The screenshot is represented by source metadata record [[SRC-0001_hcp_profile_source|SRC-0001]], but the source and transcription still require human review.

## Assumptions and Open Questions

- HCP is interpreted as Healthcare Professional.
- Confirm source record [[SRC-0001_hcp_profile_source|SRC-0001]] against the original user profile table.
- Confirm whether NSF should remain as written from the source table or be corrected to SNF.
- Confirm whether "divers" should remain as written or be localized for the intended report language.

## Review Notes

Review the transcribed content against the original source table before accepting this profile or linking it to requirements, risks, or report sections.
