# Vaccination

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
		
## Field: sending_facility
- Category: Facility
- Field Type: text
- Prevalence in US data: sometimes
- Description: Name of the organization that provided the vaccine data	always

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

## Field: vaccine_record_id
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: unique id for vaccination record

## Field: vaccine_administration_facility_id
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: 

## Field: vaccine_administration_facility_id_qualifier
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: 

## Field: vaccine_administration_facility_name
- Category: Vaccination
- Field Type: text
- Prevalence in US data: sometimes
- Description: where the vaccine was administered; facility/site name

## Field: vaccine_administration_state_province_region
- Category: Vaccination
- Field Type: text; [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)
- Prevalence in US data: sometimes
- Description: where the vaccine was administered; state/province/region

## Field: vaccine_administration_postalcode
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: always
- Description: where the vaccine was administered; postal code

## Field: vaccine_administration_country
- Category: Vaccination
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: sometimes
- Description: where the vaccine was administered; country

## Field: vaccine_administration_date
- Category: Vaccination
- Field Type: Unix timestamp UTC
- Prevalence in US data: always
- Description: date of vaccine administration

## Field: vaccine_dose_number
- Category: Vaccination
- Field Type: numeric
- Prevalence in US data: sometimes
- Description: which shot number, important for series vaccines

## Field: vaccine_series_complete
- Category: Vaccination
- Field Type: True/False
- Prevalence in US data: sometimes/calculated
- Description: is recommended vaccine series completed?

## Field: vaccine_lot_number
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: sometimes
- Description: lot/batch number from vaccine administered

## Field: vaccine_code
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: always
- Description: identifing code for the vaccination

## Field: vaccine_code_qualifier
- Category: Vaccination
- Field Type: text
- Prevalence in US data: always
- Description: code standard affiliated with the code; i.e., CVX, NDC, MVX

## Field: vaccine_code_name
- Category: Vaccination
- Field Type: text
- Prevalence in US data: sometimes
- Description: vaccine name

## Field: vaccine_manufacturer_code
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: identifing code for the vaccination manufacturer

## Field: vaccine_manufacturer_code_qualifier
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: code standard affiliated with the code; i.e., CVX, NDC, MVX

## Field: vaccine_manufacturer_code_name
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: identifing code for the disease

## Field: vaccine_disease_target_code
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: identifing code for the disease

## Field: vaccine_disease_target_code_qualifier
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: code standard affiliated with the disease

## Field: vaccine_disease_target_name
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: disease name

## Field: vaccine_administration_provider_id
- Category: Vaccination
- Field Type: Alpha-Numeric
- Prevalence in US data: 
- Description: identifing code for the provider

## Field: vaccine_administration_provider_id_qualifier
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: 

## Field: vaccine_administration_provider_fullname
- Category: Vaccination
- Field Type: text
- Prevalence in US data: 
- Description: provider name

## Field: vaccine_education_reference_material
- Category: Vaccination
- Field Type: text
- Prevalence in US data: never
- Description: URL reference for vaccine education materials for the patient.  DO not rely on the contents of this URL to be static, this is educational reference only, not intended to be part of assertions/claims for the credential

## Field: certificate_original_issuer
- Category: credential
- Field Type: text
- Prevalence in US data:
- Description: Organization originally issuing vaccine information; paper or other digital cred

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
  "schema_name": "Vaccination",
  "schema_version": "1.4",
  "attributes": [
    "mpid",
    "patient_local_id",
    "sending_facility",
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
    "vaccine_record_id",
    "vaccine_administration_facility_id",
    "vaccine_administration_facility_id_qualifier",
    "vaccine_administration_facility_name",
    "vaccine_administration_state_province_region",
    "vaccine_administration_postalcode",
    "vaccine_administration_country",
    "vaccine_administration_date",
    "vaccine_dose_number",
    "vaccine_series_complete",
    "vaccine_lot_number",
    "vaccine_code",
    "vaccine_code_qualifier",
    "vaccine_code_name",
    "vaccine_manufacturer_code",
    "vaccine_manufacturer_code_qualifier",
    "vaccine_manufacturer_code_name",
    "vaccine_disease_target_code",
    "vaccine_disease_target_code_qualifier",
    "vaccine_disease_target_name",
    "vaccine_administration_provider_id",
    "vaccine_administration_provider_id_qualifier",
    "vaccine_administration_provider_fullname",
    "vaccine_education_reference_material",
    "certificate_original_issuer",
    "certificate_original_identifier",
    "credential_issuer_name",
    "credential_issue_date"
  ]
}
```