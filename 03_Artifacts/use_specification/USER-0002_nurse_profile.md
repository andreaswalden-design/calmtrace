---
id: USER-0002
artifact_type: user_profile
title: Nurse profile
status: draft
source_refs:
  - SRC-0002
derived_from: USER-0001
linked_artifacts:
  - USER-0001
links:
  - from: USER-0002
    to: USER-0001
    link_type: refines
    rationale: Nurse is a role-specific profile derived from the broader HCP profile.
    created_with_ai: true
    review_status: needs_review
  - from: USER-0002
    to: SRC-0002
    link_type: references
    rationale: Nurse profile content was transcribed from the source screenshot metadata record.
    created_with_ai: true
    review_status: needs_review
evidence_strength: unknown
created_by: codex
created_with_ai: true
review_status: needs_review
last_reviewed: null
version: 0.1
product_area: null
user_group: Nurse
use_environment: Clinical departments and outpatient care
research_method: null
session_id: null
participant_id: null
risk_ids: []
requirement_ids: []
report_section_ids: []
confidence: low
assumptions:
  - Nurse is treated as a derived profile of the HCP profile USER-0001.
open_questions:
  - Confirm source record SRC-0002 against the original nurse profile table.
  - Confirm whether "divers" should remain as written or be localized for the intended report language.
  - Confirm the intended value for official or unofficial profile, which was blank in the provided table.
change_reason: Created nurse profile derived from USER-0001 using user-provided example table.
---

# USER-0002 - Nurse Profile

## Profile Summary

This profile describes nurses as a primary clinical user group derived from the broader HCP profile [[USER-0001_hcp_profile|USER-0001]]. Nurses provide regular patient care, monitor patients, clean monitors, and may provide emotional support to families across clinical departments and outpatient care settings.

## Derivation

This profile is derived from [[USER-0001_hcp_profile|USER-0001]] and refines the broader HCP profile with nurse-specific responsibilities, work environments, equipment, and accessibility considerations.

## Inherited Characteristics

Unless profile-specific evidence overrides them, this profile inherits the following characteristics from [[USER-0001_hcp_profile|USER-0001]]:

- Primary clinical user role
- Frequent-use expectation
- Broad sex or gender considerations
- Nationality not restricted
- General professional-life age span
- Baseline vision, hearing, age-related motor or sensory, and high-stress considerations
- Clinical clothing, PPE, and communication equipment categories

## Profile-Specific Refinements

- User group is narrowed from healthcare professional to nurse.
- Minimum training expectation is stated as at least 1 year.
- Responsibilities emphasize regular patient care, patient monitoring, monitor cleaning, and emotional support to families.
- Accessibility considerations add body size constraints for devices mounted high up towards the ceiling.

## User Profile

| Field | Description | Source Refs | Review Status |
|---|---|---|---|
| User | Nurse | SRC-0002 | needs_review |
| Alternative names | Not specified. | SRC-0002 | needs_review |
| User type | Primary user | SRC-0002 | needs_review |
| Usage frequency | Frequent user | SRC-0002 | needs_review |
| Sexes or gender considerations | Female, male, divers | SRC-0002 | needs_review |
| Age span | Start of professional life (~17-23 years) to end of professional life (~65/67 years) | SRC-0002 | needs_review |
| Nationality, language, or regional considerations | Not restricted | SRC-0002 | needs_review |
| Potential cognitive, sensory, or physical constraints | See Accessibility and Use Considerations. | SRC-0002 | needs_review |
| Training or qualification | Healthcare professional with several years of vocational training, minimum 1 year. Different level of domain knowledge, novice to expert. Inexperienced and experienced with similar devices. | SRC-0002 | needs_review |
| Country-specific training description | Not specified. | SRC-0002 | needs_review |
| Responsibilities | Healthcare professional providing regular care to patient and emotional support to the family. They are monitoring the patients and also cleaning the monitors. | SRC-0002 | needs_review |
| Work environment | See Work Environment Details. | SRC-0002 | needs_review |
| Work equipment | See Work Equipment Details. | SRC-0002 | needs_review |
| Official or unofficial profile | Not specified. | SRC-0002 | needs_review |

## Work Environment Details

Nurses work in different clinical departments, for example:

- Cardiac Ward
- Cath Lab or other diagnostic areas
- Diagnostic Imaging
- Emergency Department (ED) / Emergency Trauma
- Emergency Medical Services (EMS)
- General Ward (GW)
- Holding Area / Induction Room
- Home (Outpatient Care)
- Intermediate Care Unit (IMCU) / Step Down Unit (SDU)
- Intensive Care Unit (ICU)
- Labor Room (DLR)
- Medical ICU (MICU) / Cardiac ICU
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

## Accessibility and Use Considerations

- Vision impairment, including glasses and dyschromatopsia
- Hearing impairment, including hearing aid
- Body size, especially if devices are mounted high up towards the ceiling
- Age-related motor and sensory disabilities
- High stress level

## Linked Artifacts

| Artifact ID | Relationship | Rationale | Review Status |
|---|---|---|---|
| USER-0001 | refines | Nurse is a role-specific profile derived from the broader HCP profile. | needs_review |
| SRC-0002 | references | Nurse profile content was transcribed from this source metadata record. | needs_review |

## Evidence Notes

This profile was created from a user-provided screenshot of a nurse profile table in the current Codex conversation and is linked to [[USER-0001_hcp_profile|USER-0001]] as a derived HCP profile. The screenshot is represented by source metadata record [[SRC-0002_nurse_profile_source|SRC-0002]], but the source and transcription still require human review.

## Assumptions and Open Questions

- Nurse is treated as a derived profile of the HCP profile [[USER-0001_hcp_profile|USER-0001]].
- Confirm source record [[SRC-0002_nurse_profile_source|SRC-0002]] against the original nurse profile table.
- Confirm whether "divers" should remain as written or be localized for the intended report language.
- Confirm the intended value for official or unofficial profile, which was blank in the provided table.
- Confirm whether the responsibility statement should preserve the source wording "cleaning the monitors" or be rewritten for the target report.

## Review Notes

Review the transcribed content against the original source table before accepting this profile or linking it to requirements, risks, or report sections.
