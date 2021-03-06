| USCDI v1 Summary of Data Classes and Data Elements| US Core Profile | FHIR Resource|
|---|---|---|
| Allergies and Intolerances: | ||
| Substance (Medication) | [US Core Allergies Profile]| AllergyIntolerance |
| Substance (Drug Class) | [US Core Allergies Profile]| AllergyIntolerance |
| Reaction | [US Core Allergies Profile]| AllergyIntolerance |
| Assessment and Plan of Treatment| [US Core CarePlan Profile]| CarePlan |
| Care Team Members | [US Core CareTeam Profile]| CareTeam |
| Clinical Notes: | ||
| Consultation Note | [US Core DocumentReference Profile] | DocumentReference|
| Discharge | [US Core DocumentReference Profile] | DocumentReference|
| Summary Note| [US Core DocumentReference Profile] | DocumentReference|
| History & Physical| [US Core DocumentReference Profile] | DocumentReference |
| Imaging Narrative | [US Core DocumentReference Profile],[US Core DiagnosticReport Profile for Report and Note exchange] | DocumentReference,DiagnosticReport |
| Laboratory Report Narrative | [US Core DocumentReference Profile],[US Core DiagnosticReport Profile for Report and Note exchange] | DocumentReference,DiagnosticReport |
| Pathology Report Narrative| [US Core DocumentReference Profile],[US Core DiagnosticReport Profile for Report and Note exchange] | DocumentReference,DiagnosticReport |
| Procedure Note| [US Core DocumentReference Profile],[US Core DiagnosticReport Profile for Report and Note exchange] | DocumentReference,DiagnosticReport |
| Progress Note | [US Core DocumentReference Profile] | DocumentReference|
| Consultation Note | [US Core DocumentReference Profile] | DocumentReference|
| Goals:| ||
| Patient Goals | [US Core Goal Profile]| Goal |
| Health Concerns | [US Core Condition Profile] | Condition|
| Immunizations | [US Core Immunization Profile]| Immunization |
| Laboratory: | ||
| Tests | [US Core Laboratory Result Observation Profile], [US Core DiagnosticReport Profile for Laboratory Results Reporting]| Observation, DiagnosticReport ||
| Values/Results| [US Core Laboratory Result Observation Profile], [US Core DiagnosticReport Profile for Laboratory Results Reporting]| Observation, DiagnosticReport|
| Medications:| ||
| Medications | [US Core Medication Profile], <!--[US Core Medication Statement Profile],--> [US Core Medication Request Profile]| Medication,<!-- MedicationStatement,--> MedicationRequest |
| Medication Allergies| [US Core Allergies Profile] | AllergyIntolerance |
|Patient Demographics:| ||
| First Name| [US Core Patient Profile] | Patient.name.given |
| Last Name | [US Core Patient Profile] | Patient.name.family|
| Previous Name | [US Core Patient Profile] | Patient.name |
| Middle Name (including middle initial)| [US Core Patient Profile] | Patient.name.given |
| Suffix| [US Core Patient Profile] | Patient.name.suffix|
| Birth Sex | [US Core Patient Profile] | US Core Birth Sex Extension|
| Date of Birth | [US Core Patient Profile] | Patient.birthDate|
| Race| [US Core Patient Profile] | US Core Race Extension |
| Ethnicity | [US Core Patient Profile] | US Core Ethnicity Extension|
| Preferred Language| [US Core Patient Profile] | Patient.communication|
| Address | [US Core Patient Profile] | Patient.address|
| Phone Number| [US Core Patient Profile] | Patient.telecom|
| Problems| [US Core Condition Profile] | Condition|
| Procedures| [US Core Procedure Profile] | Procedure|
| Provenance: | [US Core Provenance Profile] |Provenance|
| Author Time Stamp | [US Core Provenance Profile] | Provenance.recorded|
| Author Organization | [US Core Provenance Profile] | Provenance.agent|
| Smoking Status| [US Core Smoking Status Observation Profile]| Observation|
| Unique Device Identifier(s) for a Patient's Implantable Device(s) | [US Core Implantable Device Profile]| Device |
| Vital Signs:| ||
| Diastolic blood pressure| [Blood pressure systolic and diastolic] (FHIR Core Profile) | Observation|
| Systolic blood pressure | [Blood pressure systolic and diastolic] (FHIR Core Profile) | Observation|
| Body height | [Body height] (FHIR Core Profile) | Observation|
| Body weight | [Body weight] (FHIR Core Profile) | Observation|
| Heart rate| [Heart rate] (FHIR Core Profile)| Observation|
| Respiratory rate| [Respiratory rate] (FHIR Core Profile)| Observation|
| Body temperature| [Body temperature] (FHIR Core Profile)| Observation|
| Pulse oximetry| [US Core Pulse Oximetry Profile] (Builds on FHIR Core Profile) | Observation|
| Inhaled oxygen concentration| [US Core Pulse Oximetry Profile] (Builds on FHIR Core Profile)| Observation|
| BMI Percentile (2-20 years old) | [US Core Pediatric BMI for Age Observation Profile] (Builds on FHIR Core Profile) | Observation|
| Weight-for-length Percentile (Birth - 36 months)| [US Core Pediatric Weight for Height Observation Profile] (Builds on FHIR Core Profile)| Observation|
| Occipital-frontal Head Circumference Percentile (Birth - 36 months)| [US Core Pediatric Head Occipital Frontal Circumference Observation Profile] (Builds on FHIR Core Profile)| Observation|
