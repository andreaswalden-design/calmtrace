---
id: USER-0003
artifact_type: user_profile
title: Registered nurse profile
status: draft
source_refs:
  - SRC-0003
derived_from: USER-0002
linked_artifacts:
  - USER-0002
links:
  - from: USER-0003
    to: USER-0002
    link_type: refines
    rationale: Registered nurse is a role-specific profile derived from the broader nurse profile.
    created_with_ai: true
    review_status: needs_review
  - from: USER-0003
    to: SRC-0003
    link_type: references
    rationale: Registered nurse profile content was transcribed from the source screenshot metadata record.
    created_with_ai: true
    review_status: needs_review
evidence_strength: unknown
created_by: codex
created_with_ai: true
review_status: needs_review
last_reviewed: null
version: 0.1
product_area: null
user_group: Registered nurse
use_environment: Clinical departments and outpatient care
research_method: null
session_id: null
participant_id: null
risk_ids: []
requirement_ids: []
report_section_ids: []
confidence: low
assumptions:
  - Registered nurse is treated as a derived profile of the nurse profile USER-0002.
open_questions:
  - Confirm source record SRC-0003 against the original registered nurse profile table.
  - Confirm whether "divers" should remain as written or be localized for the intended report language.
  - Confirm the intended value for official or unofficial profile, which was blank in the provided table.
change_reason: Created registered nurse profile derived from USER-0002 using user-provided example table.
---

# USER-0003 - Registered Nurse Profile

## Profile Summary

This profile describes registered nurses as a primary clinical user group derived from the broader nurse profile [[USER-0002_nurse_profile|USER-0002]]. Registered nurses provide regular patient care, monitor and interpret measured values, administer medication, check alarms, support patient nutrition, hygiene, and overall wellbeing, and clean monitors.

## Derivation

This profile is derived from [[USER-0002_nurse_profile|USER-0002]] and refines the broader nurse profile with registered-nurse-specific training, alternate names, responsibilities, work environments, and equipment.

## Inherited Characteristics

Unless profile-specific evidence overrides them, this profile inherits the following characteristics from [[USER-0002_nurse_profile|USER-0002]]:

- Primary nurse user role
- Frequent-use expectation
- Broad sex or gender considerations
- Nationality not restricted
- Nurse work contexts across clinical departments and outpatient care
- Baseline vision, hearing, body-height, age-related motor or sensory, and high-stress considerations
- Nurse clothing, PPE, and communication equipment categories

## Profile-Specific Refinements

- User group is narrowed from nurse to registered nurse.
- Age span starts at approximately 18 years.
- Training is refined with general and country-specific registered-nurse qualification expectations.
- Responsibilities add interpreting measured values, administering medication, checking alarms, and caring for patient nutrition, hygiene, and overall wellbeing.
- Pagers are listed as explicit work equipment.

## User Profile

| Field | Description | Source Refs | Review Status |
|---|---|---|---|
| User | Nurse (Registered Nurse) | SRC-0003 | needs_review |
| Alternative names | Also: Staff nurse, PACU Nurse, NICU Nurse, Cathlab Nurse, Labor & delivery nurse, Holding Nurse, OR Nurse, caregiver, hospital nurse, health practitioner. CA/US: Registered Nurse RN; D: Krankenpfleger/-in. | SRC-0003 | needs_review |
| User type | Primary user | SRC-0003 | needs_review |
| Usage frequency | Frequent user | SRC-0003 | needs_review |
| Sexes or gender considerations | Female, male, divers | SRC-0003 | needs_review |
| Age span | Start of professional life (~18 years) to end of professional life (~65/67 years) | SRC-0003 | needs_review |
| Nationality, language, or regional considerations | Not restricted | SRC-0003 | needs_review |
| Potential cognitive, sensory, or physical constraints | See Accessibility and Use Considerations. | SRC-0003 | needs_review |
| Training or qualification | General description: 3 years of training with final grade health care professional/nurse. Different level of domain knowledge, novice to expert. Inexperienced and experienced with similar devices. | SRC-0003 | needs_review |
| Country-specific training description | See Country-Specific Training Details. | SRC-0003 | needs_review |
| Responsibilities | Healthcare professional providing regular care to patient and emotional support to the family. Monitoring and interpreting the measured values, administering and giving medication, checking alarms, caring for patient nutrition, hygiene, and overall wellbeing. They are also cleaning the monitors. | SRC-0003 | needs_review |
| Work environment | See Work Environment Details. | SRC-0003 | needs_review |
| Work equipment | See Work Equipment Details. | SRC-0003 | needs_review |
| Official or unofficial profile | Not specified. | SRC-0003 | needs_review |

## Country-Specific Training Details

- CA: 4 years baccalaureate degree in nursing from a Canadian university or its international equivalent. Specialized areas may include surgery, obstetrics, psychiatry, pediatrics, community health, occupational health, emergency, rehabilitation, or oncology.
- US: Bachelor of Science in Nursing (4-5 years).
- D: 3 years of training at a state accredited nursing school.

## Work Environment Details

Registered nurses work in different clinical departments, for example:

- Intensive Care Unit (ICU)
- Emergency Department (ED) / Emergency Trauma
- Operating Room (OR)
- Recovery Room (RR)
- Post Anesthetic Care Unit (PACU)
- General Ward (GW)
- Emergency Medical Services (EMS)
- Neonatal ICU (NICU)
- Cath Lab or other diagnostic areas
- Medical ICU (MICU)
- Cardiac Ward
- Intermediate Care Unit (IMCU) / Step Down Unit (SDU)
- Home (Outpatient Care)
- Nursing Home / Skilled Nursing Facility (SNF)
- Holding Area
- MRI Room
- Labor Room (DLR)
- Obstetric Ward

## Work Equipment Details

- Working clothes, including working scrubs, aprons, OR scrubs, and uniforms
- Gloves
- Masks
- Caps
- Phones
- Pagers

## Accessibility and Use Considerations

- Vision impairment, including glasses and dyschromatopsia
- Hearing impairment, including hearing aid
- Body height, especially if devices are mounted high up towards the ceiling
- Age-related motor and sensory disabilities
- High stress level

## Linked Artifacts

| Artifact ID | Relationship | Rationale | Review Status |
|---|---|---|---|
| USER-0002 | refines | Registered nurse is a role-specific profile derived from the broader nurse profile. | needs_review |
| SRC-0003 | references | Registered nurse profile content was transcribed from this source metadata record. | needs_review |

## Evidence Notes

This profile was created from a user-provided screenshot of a registered nurse profile table in the current Codex conversation and is linked to [[USER-0002_nurse_profile|USER-0002]] as a derived nurse profile. The screenshot is represented by source metadata record [[SRC-0003_registered_nurse_profile_source|SRC-0003]], but the source and transcription still require human review.

Source wording normalized in the main profile:

- "HC Professional" was expanded to "Healthcare professional."
- "patients food" was normalized to "patient nutrition."

## Assumptions and Open Questions

- Registered nurse is treated as a derived profile of the nurse profile [[USER-0002_nurse_profile|USER-0002]].
- Confirm source record [[SRC-0003_registered_nurse_profile_source|SRC-0003]] against the original registered nurse profile table.
- Confirm whether "divers" should remain as written or be localized for the intended report language.
- Confirm the intended value for official or unofficial profile, which was blank in the provided table.
- Confirm whether accepted content should keep "patient nutrition" or preserve the source wording "patients food."
- Confirm whether accepted content should keep "Healthcare professional" or preserve the source abbreviation "HC Professional."

## Review Notes

Review the transcribed content against the original source table before accepting this profile or linking it to requirements, risks, or report sections.
