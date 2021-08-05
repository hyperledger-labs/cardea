# Vaccine Exemption

- Authors: [Keela Shatzkin](keela@shatzkinsystems.com) [Mike Ebert](mike@indicio.tech) [Kim Ebert](kim@indicio.tech)
- Status Note: 
- Supersedes: 
- Start Date: 2021-07-03


## Field: mpid
- Category: Patient
- Field Type: Alpha-Numeric
- Prevalence in US data: always
- Description: master patient identifier of source that wrote the record to the ledger

## Field: patient_local_id
- Category: Patient
- Field Type: Alpha-Numeric
- Prevalence in US data: sometimes
- Description: medical record number for the site who performed the test

## Field: patient_surnames
- Category: Patient
- Field Type: text
- Prevalence in US data: always
- Description: demographics collected during test

## Field: patient_given_names
- Category: Patient
- Field Type: text
- Prevalence in US data: always
- Description: demographics collected during test

## Field: patient_date_of_birth
- Category: Patient
- Field Type: YYYY-MM-DD
- Prevalence in US data: always
- Description: demographics collected during test

## Field: patient_gender_legal
- Category: Patient
- Field Type: text
- Prevalence in US data: always
- Description: demographics collected during test

## Field: patient_street_address
- Category: Patient
- Field Type: text
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_city
- Category: Patient
- Field Type: text
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_state_province_region
- Category: Patient
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_postalcode
- Category: Patient
- Field Type: Alpha-Numeric
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_country
- Category: Patient
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_phone
- Category: Patient
- Field Type: numeric
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: patient_email
- Category: Patient
- Field Type: text
- Prevalence in US data: sometimes
- Description: demographics collected during test

## Field: exemption_record_id
- Category: Exemption
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: unique id for exemption record

## Field: exemption_requestor
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: Name of individual who requested exemption; only populate if NOT the patient themselves
- Comments: Added to support documentation of the Guardian who requested exemption

## Field: exemption_requestor_relationship
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: relationship of the requestor to the credential holder/patient

## Field: exemption_issue_date
- Category: Exemption
- Field Type: YYYY-MM-DD
- Prevalence in US data: 
- Description: date the exemption was issued

## Field: exemption_state_province_region
- Category: Exemption
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: 
- Description: sate/province/region where the exemption was issued

## Field: exemption_country
- Category: Exemption
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: 
- Description: country where the exemption was issued

## Field: exemption_type
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: Medical, Philisophical, Religious

## Field: exemption_medical_permanent
- Category: Exemption
- Field Type: True/False
- Prevalence in US data: 
- Description: True if the exemption is permanent

## Field: exemption_note
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: Reason for exemption

## Field: exemption_from_all
- Category: Exemption
- Field Type: True/False
- Prevalence in US data: 
- Description: True for use if person is exempt from all vaccines

## Field: exemption_diseases_code
- Category: Exemption
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: identifing code for the disease

## Field: exemption_disease_code_qualifier
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: code standard affiliated with the code; i.e., ICD-10, Snomed

## Field: exemption_disease_code_name
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: disease name

## Field: exemption_medical_physician_surnames
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: If Medical, physician surname who issued exemption

## Field: exemption_medical_physician_given_names
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: If Medical, physician given name(s) who issued exemption

## Field: exemption_medical_physician_full_name
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: If Medical, physician full name who issued exemption

## Field: exemption_medical_physician_license_number
- Category: Exemption
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: If Medical, physician license who issued exemption

## Field: exemption_medical_physician_license_type
- Category: Exemption
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: If Medical, physician license type who issued exemption

## Field: exemption_medical_physician_license_state_province_region
- Category: Exemption
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: 
- Description: If Medical, physician licensing state/province/region who issued exemption, if applicable

## Field: exemption_medical_physician_license_country
- Category: Exemption
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: 
- Description: If Medical, physician licensing country who issued exemption

## Field: exemption_expiration_date
- Category: Exemption
- Field Type: YYYY-MM-DD
- Prevalence in US data: 
- Description: expiration date of the vaccine exemption, if temporary

## Field: exemption_credential_issuer
- Category: Exemption
- Field Type: text
- Prevalence in US data: 
- Description: Who issued the exemption (Doctor, School, Government)

## Field: certificate_original_issuer
- Category: credential
- Field Type: text
- Prevalence in US data:
- Description: Organization originally issuing vaccine exemption information; paper or other digital cred

## Field: certificate_original_identifier
- Category: credential
- Field Type: text
- Prevalence in US data:
- Description: Unique key for reference to original documentation

## Field: credential_issuer_name
- Category: Credential
- Field Type: text
- Prevalence in US data: 
- Description:

## Example ARIES Schema:
```
{
  "schema_name": "Vaccine_Exemption",
  "schema_version": "1.1",
  "attributes": [
    "mpid",
    "patient_local_id",
    "patient_surnames",
    "patient_given_names",
    "patient_date_of_birth",
    "patient_gender_legal",
    "patient_street_address",
    "patient_city",
    "patient_state_province_region",
    "patient_postalcode",
    "patient_country",
    "patient_phone",
    "patient_email",
    "exemption_record_id",
    "exemption_requestor",
    "exemption_requestor_relationship",
    "exemption_issue_date",
    "exemption_state_province_region",
    "exemption_country",
    "exemption_type",
    "exemption_medical_permanent",
    "exemption_note",
    "exemption_from_all",
    "exemption_diseases_code",
    "exemption_disease_code_qualifier",
    "exemption_disease_code_name",
    "exemption_medical_physician_surnames",
    "exemption_medical_physician_given_names",
    "exemption_medical_physician_full_name",
    "exemption_medical_physician_license_number",
    "exemption_medical_physician_license_type",
    "exemption_medical_physician_license_state_province_region",
    "exemption_medical_physician_license_country",
    "exemption_expiration_date",
    "exemption_credential_issuer",
    "certificate_original_issuer",
    "certificate_original_identifier",
    "credential_issuer_name"
  ]
}
```