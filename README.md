# Cardea

## Welcome to the Cardea community!

Cardea is a complete ecosystem for the exchange of privacy-preserving digital credentials, open sourced as a project in Linux Foundation Public Health (LFPH).

This project has begun the process of migration to LFPH. We are beginning community building efforts using the following channels:

<!--- ## Announcements: 

Mark your calendar: The Launch Meeting of the Cardea User Group meeting will take place May 13, 2021, 9am PDT

Zoom information: Topic: Cardea User Group Meeting

Join Zoom Meetinghttps://us02web.zoom.us/j/3933667495?pwd=ZnlPSDJBcnljL0svS1djVGswcS84QT09
Meeting ID:393 366 7495
Passcode: 528433

One tap mobile
+16699009128,,3933667495# US (San Jose)
+12532158782,,3933667495# US (Tacoma)

Dial by your location
+1 669 900 9128 US (San Jose)
+1 253 215 8782 US (Tacoma)
+1 346 248 7799 US (Houston)
+1 646 558 8656 US (New York)
+1 301 715 8592 US (Washington DC)
+1 312 626 6799 US (Chicago)

Meeting ID:393 366 7495

Find your local number:https://us02web.zoom.us/u/kexKOPG9Mr --->

## Get Involved

We are currently looking for contributors of all types! Here are a few ways to get started:

* Join the [LFPH Slack](https://slack.lfph.io) and our channel, #cardea
* Sign up for our [mailing list](https://lists.lfph.io/g/cardea)

## Contributing to open source

If you haven’t been involved in an open source project before, it can be intimidating to start participating. Here are a few tips to get comfortable: 

*Feel free to lurk*

• Seeing how other community members interact will help you adjust and learn the social norms in the community

*[Read our Code of Conduct](https://github.com/lfph/foundation/blob/main/code-of-conduct.md)*

• We’ve set and enforce high standards of professional practice from everyone you’ll be meeting

*No stupid questions*

• Not sure what someone meant? Need help learning to use a tool? Ask lots of questions and let the community support you.

*Don’t wait for an invitation*

• Our tools and meetings are open by default, so jump in and introduce yourself, ask questions and share ideas

## Testing

You can use the following agents to test your setup, implementation, agent, etc.:

Issuer: https://lab.cardea.indiciotech.io/

Holder: https://government.cardea.indiciotech.io/ - Note: For the purposes of this test, holder must send a message so the connection status is considered active. If the holder doesn’t send demographics, the user must also edit the demographics before sending.

Verifier https://restaurant.cardea.indiciotech.io/

## Workflows

### Health Credential Issuance
1. Lab Enterprise Agent displays an invitation
2. Holder Agent connects using the invitation
3. Lab Enterprise Agent requests identity information using the present-proof v. 1 protocol
4. Holder Agent responds with a self-attested identity proof
5. (Optional) Lab Enterprise Agent issues a lab_order credential
6. (Optional) Lab Enterprise Agent checks to make sure a connection (contact) has been issued a lab_order
7. Lab Enterprise Agent issues a lab_result, vaccine, or vaccine_exemption credential to the Holder Agent

### Trusted Traveler Issuance
1. Government Enterprise Agent displays an invitation
2. Holder Agent connects using the invitation
3. Government Enterprise Agent requests identity information using the present-proof v. 1 protocol
4. Holder Agent responds with a self-attested identity proof
5. Government Enterprise Agent requests presentation of a lab_result, vaccine, or vaccine_exemption credential
6. Holder Agent responds with the credential of its choice
7. Government Enterprise Agent verifies the credential cryptographically and validates the following attributes (if you are trying to demonstrate a particular use case, you can validate more):
    a. lab_result must be “Negative” and lab_specimen_collected_date must be a Unix timestamp less than 3 days ago OR lab_result must be “Positive” and lab_specimen_collected_date must be a Unix timestamp more than 28 days ago 
    b. vaccine: vaccine_series_complete must be “true” and vaccine_administration_date must be a Unix timestamp more than 14 days ago
    c. vaccine_exemption: exemption_expiration_date must be a Unix timestamp in the future.
8. Government Enterprise Agent issues a trusted_traveler credential to the Holder Agent

### Trusted Traveler Verification
1. Verifier Agent displays an invitation
2. Holder Agent connects using the invitation
3. Verifier Agent requests presentation of a trusted_traveler credential
4. Holder Agent responds with its trusted_traveler
5. Verifier Agent displays “Approved” or “Not Approved” depending on the result of the cryptographic verification (we recommend verifying trusted_traveler_expiration_date_time (Unix timestamp) is not in the past using a predicate proof).
