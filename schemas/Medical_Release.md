# Medical Release

- Authors: [Keela Shatzkin](keela@shatzkinsystems.com) [Mike Ebert](mike@indicio.tech) [Kim Ebert](kim@indicio.tech)
- Status Note: 
- Supersedes: 
- Start Date: 2021-07-26

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

## Field: medical_release_id
- Category: medical release
- Field Type: text
- Prevalence in US data: 
- Description: GUID used to link the release to a specific health care system patient

## Field: medical_release_signed_date
- Category: medical release
- Field Type: Unix timestamp UTC
- Prevalence in US data: 
- Description: date the patient/user signed the form

## Field: medical_release_form_location
- Category: medical release
- Field Type: [Hashlink](https://github.com/hyperledger/aries-rfcs/tree/main/features/0641-linking-binary-objects-to-credentials#hashlink)
- Prevalence in US data: 
- Description: link to text user agreed to

## Field: medical_release_covered_data
- Category: medical release
- Field Type: 
- Prevalence in US data: 
- Description: 

## Field: medical_release_covered_party
- Category: medical release
- Field Type: 
- Prevalence in US data: 
- Description: 

## Field: medical_release_purposes
- Category: medical release
- Field Type: text; comma secondary
- Prevalence in US data: 
- Description: 

## Field: medical_release_requestor
- Category: medical release
- Field Type: 
- Prevalence in US data: 
- Description: 

## Field: medical_release_requestor_relationship
- Category: medical release
- Field Type: 
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
  "schema_name": "Medical_Release",
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
    "medical_release_id"
    "medical_release_signed_date",
    "medical_release_form_location",
    "medical_release_covered_data",
    "medical_release_covered_party",
    "medical_release_purposes",
    "medical_release_requestor",
    "medical_release_requestor_relationship",
    "credential_issuer_name",
    "credential_issue_date"
  ]
}
```

## Network Schema Ids

```
Indicio Test: RuuJwd3JMffNwZ43DcJKN1:2:Medical_Release:1.1
Indicio Demo: RuuJwd3JMffNwZ43DcJKN1:2:Medical_Release:1.1
Indicio Live: RuuJwd3JMffNwZ43DcJKN1:2:Medical_Release:1.1
Sovrin Staging: RuuJwd3JMffNwZ43DcJKN1:2:Medical_Release:1.1
```
