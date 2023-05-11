# Trusted Traveler

- Authors: [Keela Shatzkin](keela@shatzkinsystems.com) [Mike Ebert](mike@indicio.tech) [Kim Ebert](kim@indicio.tech)
- Status Note:
- Supersedes:
- Start Date: 2021-07-03

## Field: traveler_surnames

- Category: Traveler
- Field Type: text
- Prevalence in US data: always
- Description: demographics for trusted traveler

## Field: traveler_given_names

- Category: Traveler
- Field Type: text
- Prevalence in US data: always
- Description: demographics for trusted traveler

## Field: traveler_date_of_birth

- Category: Traveler
- Field Type: Unix timestamp UTC
- Prevalence in US data: always
- Description: demographics for trusted traveler

## Field: traveler_gender_legal

- Category: Traveler
- Field Type: text
- Prevalence in US data: always
- Description: demographics for trusted traveler

## Field: traveler_country

- Category: Traveler
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data: sometimes
- Description: demographics for trusted traveler

## Field: traveler_origin_country

- Category: Traveler
- Field Type: text; [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)
- Prevalence in US data:
- Description:

## Field: traveler_email

- Category: Traveler
- Field Type: text
- Prevalence in US data: sometimes
- Description: demographics for trusted traveler

## Field: trusted_traveler_id

- Category: Trusted Info
- Field Type: Alpha-Numeric
- Prevalence in US data:
- Description: unique id for trusted traveler

## Field: trusted_traveler_issue_date_time

- Category: Trusted Info
- Field Type: Unix timestamp UTC
- Prevalence in US data: always
- Description:

## Field: trusted_traveler_expiration_date_time

- Category: Trusted Info
- Field Type: Unix timestamp UTC
- Prevalence in US data: always
- Description: This would need to be managed in predicate proof checks against this info being used to expose other information.

## Field: governance_applied

- Category:
- Field Type: [Hashlink](https://github.com/hyperledger/aries-rfcs/tree/main/features/0641-linking-binary-objects-to-credentials#hashlink)
- Prevalence in US data: always
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
  "schema_name": "Trusted_Traveler",
  "schema_version": "1.4",
  "attributes": [
    "traveler_surnames",
    "traveler_given_names",
    "traveler_date_of_birth",
    "traveler_gender_legal",
    "traveler_country",
    "traveler_origin_country",
    "traveler_email",
    "trusted_traveler_id",
    "trusted_traveler_issue_date_time",
    "trusted_traveler_expiration_date_time",
    "governance_applied",
    "credential_issuer_name",
    "credential_issue_date"
  ]
}
```

## Network Schema Ids

```
Indicio Test: KKsUEwhXon1wxN9jDy4cUT:2:Trusted_Traveler:1.4
Indicio Demo: RuuJwd3JMffNwZ43DcJKN1:2:Trusted_Traveler:1.4
Indicio Live: RuuJwd3JMffNwZ43DcJKN1:2:Trusted_Traveler:1.4
Sovrin Staging: RuuJwd3JMffNwZ43DcJKN1:2:Trusted_Traveler:1.4
```
