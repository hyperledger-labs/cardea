# Lab Result

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
- Field Type: Unix timestamp UTC
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

## Field: lab_observation_date_time
- Category: Result
- Field Type: Unix timestamp UTC
- Prevalence in US data: always
- Description: Date/Time of lab test result

## Field: lab_specimen_collected_date
- Category: Result
- Field Type: Unix timestamp UTC
- Prevalence in US data: sometimes
- Description: Date/Time of the lab sample being taken

## Field: lab_specimen_type
- Category: Result
- Field Type: text
- Prevalence in US data: 
- Description: Blood, saliva, etc 

## Field: lab_result_status
- Category: Result
- Field Type: text
- Prevalence in US data: always
- Description: F for Final, C for Corrected result

## Field: lab_coding_qualifier
- Category: Result
- Field Type: LOINC/LOCAL
- Prevalence in US data: always
- Description: label for lab test coding system,  "local" if lab system does not have properly LOINC'd tests.  If local check lab_description to determine test validity

## Field: lab_code
- Category: Result
- Field Type: Alpha-Numeric
- Prevalence in US data: always
- Description: standard LOINC code value, or local code value

## Field: lab_description
- Category: Result
- Field Type: text
- Prevalence in US data: always
- Description: lab test name description

## Field: lab_order_id
- Category: Result
- Field Type: Alpha-Numeric
- Prevalence in US data: always
- Description: unique id for lab test instance

## Field: lab_normality
- Category: Result
- Field Type: text
- Prevalence in US data: 
- Description: Indication of whether status is normal, or outside the reference range, provided by the lab who performed the test, not an interpretation

## Field: lab_result
- Category: Result
- Field Type: text
- Prevalence in US data: always
- Description: outcome of the test

## Field: lab_comment
- Category: Result
- Field Type: text
- Prevalence in US data: sometimes
- Description: free text comment provided by the performing lab

## Field: lab_performed_by
- Category: Result
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: ordering_facility_id
- Category: Ordering Facility
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description:

## Field: ordering_facility_id_qualifier
- Category: Ordering Facility
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: ordering_facility_name
- Category: Ordering Facility
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: ordering_facility_state_province_region
- Category: Ordering Facility
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: 
- Description:

## Field: ordering_facility_postalcode
- Category: Ordering Facility
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: 

## Field: ordering_facility_country
- Category: Ordering Facility
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: 
- Description: 

## Field: performing_laboratory_id
- Category: Performing Lab
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description:

## Field: performing_laboratory_id_qualifier
- Category: Performing Lab
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: performing_laboratory_name
- Category: Performing Lab
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: performing_laboratory_state_province_region
- Category: Performing Lab
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: 
- Description:

## Field: performing_laboratory_postalcode
- Category: Performing Lab
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: 

## Field: performing_laboratory_country
- Category: Performing Lab
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: 
- Description: 

## Field: credential_issuer_name
- Category: Credential
- Field Type: text
- Prevalence in US data: 
- Description:

## Field: credential_issue_date
- Category: Credential
- Field Type: Unix timestamp UTC
- Prevalence in US data: 
- Description:

## Attributes are part of the Credential Protocol see [ARIES RFC 0036](https://github.com/hyperledger/aries-rfcs/tree/main/features/0036-issue-credential)

Some attributes are part of the underlying ARIES Credential Protocol. For example the following values are associated with the credential

- "schema_id": string, identifier of schema
- "cred_def_id": string, identifier of credential definition, which includes the issuer's DID

## Example ARIES Schema:
```
{
  "schema_name": "Lab_Result",
  "schema_version": "1.4",
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
    "lab_observation_date_time",
    "lab_specimen_collected_date",
    "lab_specimen_type",
    "lab_result_status",
    "lab_coding_qualifier",
    "lab_code",
    "lab_description",
    "lab_order_id",
    "lab_normality",
    "lab_result",
    "lab_comment",
    "ordering_facility_id",
    "ordering_facility_id_qualifier",
    "ordering_facility_name",
    "ordering_facility_state_province_region",
    "ordering_facility_postalcode",
    "ordering_facility_country",
    "performing_laboratory_id",
    "performing_laboratory_id_qualifier",
    "performing_laboratory_name",
    "performing_laboratory_state_province_region",
    "performing_laboratory_postalcode",
    "performing_laboratory_country",
    "lab_performed_by",
    "credential_issuer_name",
    "credential_issue_date"
  ]
}

```

## Network Schema Ids

Indicio Test: RuuJwd3JMffNwZ43DcJKN1:2:Lab_Result:1.4
Sovrin Staging: RuuJwd3JMffNwZ43DcJKN1:2:Lab_Result:1.4