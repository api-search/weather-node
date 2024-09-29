---
name: Alternate
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alternate.png
url: https://example.com/apis/alternate.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alternate
apis:
  - name: account
    description: <p>Operations for Amazon Web Services Account Management</p>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: account
          paths:
            /deleteAlternateContact:
              POST:
                summary: DeleteAlternateContact
                description: >-
                  <p>Deletes the specified alternate contact from an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Delete
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
            /disableRegion:
              POST:
                summary: DisableRegion
                description: <p>Disables (opts-out) a particular Region for an account.</p>
                tags:
                  - Disable
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
            /enableRegion:
              POST:
                summary: EnableRegion
                description: <p>Enables (opts-in) a particular Region for an account.</p>
                tags:
                  - Enable
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
            /getAlternateContact:
              POST:
                summary: GetAlternateContact
                description: >-
                  <p>Retrieves the specified alternate contact attached to an
                  Amazon Web Services account.</p> <p>For complete details about
                  how to use the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Get
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
                  - Regions
            /getContactInformation:
              POST:
                summary: GetContactInformation
                description: >-
                  <p>Retrieves the primary contact information of an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the primary contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Update
                  the primary and alternate contact information</a>.</p>
                tags:
                  - Get
                  - Contacts
                  - Information
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
            /getRegionOptStatus:
              POST:
                summary: GetRegionOptStatus
                description: <p>Retrieves the opt-in status of a particular Region.</p>
                tags:
                  - Get
                  - Regions
                  - Opt
                  - Status
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
            /listRegions:
              POST:
                summary: ListRegions
                description: >-
                  <p>Lists all the Regions for a given account and their
                  respective opt-in statuses. Optionally, this list can be
                  filtered by the <code>region-opt-status-contains</code>
                  parameter. </p>
                tags:
                  - Lists
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
            /putAlternateContact:
              POST:
                summary: PutAlternateContact
                description: >-
                  <p>Modifies the specified alternate contact attached to an
                  Amazon Web Services account.</p> <p>For complete details about
                  how to use the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Put
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
            /putContactInformation:
              POST:
                summary: PutContactInformation
                description: >-
                  <p>Updates the primary contact information of an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the primary contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Update
                  the primary and alternate contact informatio
                tags:
                  - Put
                  - Contacts
                  - Information
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
    overlays:
      - type: APIs.io Search
        url: overlays/account-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/account-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:account
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---