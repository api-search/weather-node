---
name: Bucket
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bucket.png
url: https://example.com/apis/bucket.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bucket
apis:
  - name: macie2
    description: >-
      <p>Amazon Macie is a fully managed data security and data privacy service
      that uses machine learning and pattern matching to help you discover and
      protect your sensitive data in AWS. Macie automates the discovery of
      sensitive data, such as PII and intellectual property, to provide you with
      insight into the data that your organization stores in AWS. Macie also
      provides an inventory of your Amazon S3 buckets, which it continually
      monitors for you. If Macie detects sensitive data or potential data access
      issues, it generates detailed findings for you to review and act upon as
      necessary.</p>
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
            title: macie2
          paths:
            /invitations/accept:
              POST:
                summary: AcceptInvitation
                description: >-
                  <p>Accepts an Amazon Macie membership invitation that was
                  received from a specific account.</p>
                tags:
                  - Accept
                  - Invitation
                  - Invitations
                  - Accept
            /custom-data-identifiers/get:
              POST:
                summary: BatchGetCustomDataIdentifiers
                description: >-
                  <p>Retrieves information about one or more custom data
                  identifiers.</p>
                tags:
                  - Batches
                  - Get
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
            /allow-lists:
              GET:
                summary: ListAllowLists
                description: >-
                  <p>Retrieves a subset of information about all the allow lists
                  for an account.</p>
                tags:
                  - Lists
                  - Allow
                  - Lists
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
            /jobs:
              POST:
                summary: CreateClassificationJob
                description: >-
                  <p>Creates and defines the settings for a classification
                  job.</p>
                tags:
                  - Create
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
            /custom-data-identifiers:
              POST:
                summary: CreateCustomDataIdentifier
                description: >-
                  <p>Creates and defines the criteria and other settings for a
                  custom data identifier.</p>
                tags:
                  - Create
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
            /findingsfilters:
              GET:
                summary: ListFindingsFilters
                description: >-
                  <p>Retrieves a subset of information about all the findings
                  filters for an account.</p>
                tags:
                  - Lists
                  - Findings
                  - Filters
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
            /invitations:
              GET:
                summary: ListInvitations
                description: >-
                  <p>Retrieves information about the Amazon Macie membership
                  invitations that were received by an account.</p>
                tags:
                  - Lists
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
            /members:
              GET:
                summary: ListMembers
                description: >-
                  <p>Retrieves information about the accounts that are
                  associated with an Amazon Macie administrator account.</p>
                tags:
                  - Lists
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
            /findings/sample:
              POST:
                summary: CreateSampleFindings
                description: <p>Creates sample findings.</p>
                tags:
                  - Create
                  - Samples
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
            /invitations/decline:
              POST:
                summary: DeclineInvitations
                description: >-
                  <p>Declines Amazon Macie membership invitations that were
                  received from specific accounts.</p>
                tags:
                  - Decline
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
            /allow-lists/{id}:
              PUT:
                summary: UpdateAllowList
                description: <p>Updates the settings for an allow list.</p>
                tags:
                  - Update
                  - Allow
                  - Lists
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /custom-data-identifiers/{id}:
              GET:
                summary: GetCustomDataIdentifier
                description: >-
                  <p>Retrieves the criteria and other settings for a custom data
                  identifier.</p>
                tags:
                  - Get
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /findingsfilters/{id}:
              PATCH:
                summary: UpdateFindingsFilter
                description: >-
                  <p>Updates the criteria and other settings for a findings
                  filter.</p>
                tags:
                  - Update
                  - Findings
                  - Filter
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
            /invitations/delete:
              POST:
                summary: DeleteInvitations
                description: >-
                  <p>Deletes Amazon Macie membership invitations that were
                  received from specific accounts.</p>
                tags:
                  - Delete
                  - Invitations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
            /members/{id}:
              GET:
                summary: GetMember
                description: >-
                  <p>Retrieves information about an account that's associated
                  with an Amazon Macie administrator account.</p>
                tags:
                  - Get
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
            /datasources/s3:
              POST:
                summary: DescribeBuckets
                description: >-
                  <p>Retrieves (queries) statistical data and other information
                  about one or more S3 buckets that Amazon Macie monitors and
                  analyzes for an account.</p>
                tags:
                  - Describe
                  - Buckets
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
            /jobs/{jobId}:
              PATCH:
                summary: UpdateClassificationJob
                description: <p>Changes the status of a classification job.</p>
                tags:
                  - Update
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
            /admin/configuration:
              PATCH:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the Amazon Macie configuration settings for an
                  organization in Organizations.</p>
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
            /macie:
              PATCH:
                summary: UpdateMacieSession
                description: >-
                  <p>Suspends or re-enables Amazon Macie, or updates the
                  configuration settings for a Macie account.</p>
                tags:
                  - Update
                  - Macie
                  - Sessions
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
            /admin:
              GET:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Retrieves information about the delegated Amazon Macie
                  administrator account for an organization in
                  Organizations.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
            /administrator/disassociate:
              POST:
                summary: DisassociateFromAdministratorAccount
                description: >-
                  <p>Disassociates a member account from its Amazon Macie
                  administrator account.</p>
                tags:
                  - Disassociate
                  - From
                  - Administrator
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
            /master/disassociate:
              POST:
                summary: DisassociateFromMasterAccount
                description: >-
                  <p>(Deprecated) Disassociates a member account from its Amazon
                  Macie administrator account. This operation has been replaced
                  by the <link 
                  linkend="DisassociateFromAdministratorAccount">DisassociateFromAdministratorAccount</link>
                  operation.</p>
                tags:
                  - Disassociate
                  - From
                  - Master
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /members/disassociate/{id}:
              POST:
                summary: DisassociateMember
                description: >-
                  <p>Disassociates an Amazon Macie administrator account from a
                  member account.</p>
                tags:
                  - Disassociate
                  - Members
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /administrator:
              GET:
                summary: GetAdministratorAccount
                description: >-
                  <p>Retrieves information about the Amazon Macie administrator
                  account for an account.</p>
                tags:
                  - Get
                  - Administrator
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
            /automated-discovery/configuration:
              PUT:
                summary: UpdateAutomatedDiscoveryConfiguration
                description: >-
                  <p>Enables or disables automated sensitive data discovery for
                  an account.</p>
                tags:
                  - Update
                  - Automated
                  - Discovery
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
            /datasources/s3/statistics:
              POST:
                summary: GetBucketStatistics
                description: >-
                  <p>Retrieves (queries) aggregated statistical data about all
                  the S3 buckets that Amazon Macie monitors and analyzes for an
                  account.</p>
                tags:
                  - Get
                  - Bucket
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
            /classification-export-configuration:
              PUT:
                summary: PutClassificationExportConfiguration
                description: >-
                  <p>Creates or updates the configuration settings for storing
                  data classification results.</p>
                tags:
                  - Put
                  - Classifications
                  - Export
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
            /classification-scopes/{id}:
              PATCH:
                summary: UpdateClassificationScope
                description: >-
                  <p>Updates the classification scope settings for an
                  account.</p>
                tags:
                  - Update
                  - Classifications
                  - Scopes
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
            /findings/statistics:
              POST:
                summary: GetFindingStatistics
                description: >-
                  <p>Retrieves (queries) aggregated statistical data about
                  findings.</p>
                tags:
                  - Get
                  - Findings
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
            /findings/describe:
              POST:
                summary: GetFindings
                description: <p>Retrieves the details of one or more findings.</p>
                tags:
                  - Get
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
            /findings-publication-configuration:
              PUT:
                summary: PutFindingsPublicationConfiguration
                description: >-
                  <p>Updates the configuration settings for publishing findings
                  to Security Hub.</p>
                tags:
                  - Put
                  - Findings
                  - Publication
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
            /invitations/count:
              GET:
                summary: GetInvitationsCount
                description: >-
                  <p>Retrieves the count of Amazon Macie membership invitations
                  that were received by an account.</p>
                tags:
                  - Get
                  - Invitations
                  - Count
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
            /master:
              GET:
                summary: GetMasterAccount
                description: >-
                  <p>(Deprecated) Retrieves information about the Amazon Macie
                  administrator account for an account. This operation has been
                  replaced by the <link 
                  linkend="GetAdministratorAccount">GetAdministratorAccount</link>
                  operation.</p>
                tags:
                  - Get
                  - Master
                  - Account
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
            /resource-profiles:
              PATCH:
                summary: UpdateResourceProfile
                description: <p>Updates the sensitivity score for an S3 bucket.</p>
                tags:
                  - Update
                  - Resources
                  - Profiles
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
            /reveal-configuration:
              PUT:
                summary: UpdateRevealConfiguration
                description: >-
                  <p>Updates the status and configuration settings for
                  retrieving occurrences of sensitive data reported by
                  findings.</p>
                tags:
                  - Update
                  - Reveal
                  - Configurations
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
            /findings/{findingId}/reveal:
              GET:
                summary: GetSensitiveDataOccurrences
                description: >-
                  <p>Retrieves occurrences of sensitive data reported by a
                  finding.</p>
                tags:
                  - Get
                  - Sensitive
                  - Data
                  - Occurrences
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
            /findings/{findingId}/reveal/availability:
              GET:
                summary: GetSensitiveDataOccurrencesAvailability
                description: >-
                  <p>Checks whether occurrences of sensitive data can be
                  retrieved for a finding.</p>
                tags:
                  - Get
                  - Sensitive
                  - Data
                  - Occurrences
                  - Availability
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
            /templates/sensitivity-inspections/{id}:
              PUT:
                summary: UpdateSensitivityInspectionTemplate
                description: ' <p>Updates the settings for the sensitivity inspection template for an account.</p>'
                tags:
                  - Update
                  - Sensitivity
                  - Inspections
                  - Templates
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
            /usage/statistics:
              POST:
                summary: GetUsageStatistics
                description: >-
                  <p>Retrieves (queries) quotas and aggregated usage data for
                  one or more accounts.</p>
                tags:
                  - Get
                  - Usage
                  - Statistics
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
            /usage:
              GET:
                summary: GetUsageTotals
                description: >-
                  <p>Retrieves (queries) aggregated usage data for an
                  account.</p>
                tags:
                  - Get
                  - Usage
                  - Totals
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
            /jobs/list:
              POST:
                summary: ListClassificationJobs
                description: >-
                  <p>Retrieves a subset of information about one or more
                  classification jobs.</p>
                tags:
                  - Lists
                  - Classifications
                  - Jobs
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /classification-scopes:
              GET:
                summary: ListClassificationScopes
                description: >-
                  <p>Retrieves a subset of information about the classification
                  scope for an account.</p>
                tags:
                  - Lists
                  - Classifications
                  - Scopes
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /custom-data-identifiers/list:
              POST:
                summary: ListCustomDataIdentifiers
                description: >-
                  <p>Retrieves a subset of information about all the custom data
                  identifiers for an account.</p>
                tags:
                  - Lists
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /findings:
              POST:
                summary: ListFindings
                description: >-
                  <p>Retrieves a subset of information about one or more
                  findings.</p>
                tags:
                  - Lists
                  - Findings
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
            /managed-data-identifiers/list:
              POST:
                summary: ListManagedDataIdentifiers
                description: >-
                  <p>Retrieves information about all the managed data
                  identifiers that Amazon Macie currently provides.</p>
                tags:
                  - Lists
                  - Managed
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
            /resource-profiles/artifacts:
              GET:
                summary: ListResourceProfileArtifacts
                description: >-
                  <p>Retrieves information about objects that were selected from
                  an S3 bucket for automated sensitive data discovery.</p>
                tags:
                  - Lists
                  - Resources
                  - Profiles
                  - Artifacts
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
            /resource-profiles/detections:
              PATCH:
                summary: UpdateResourceProfileDetections
                description: >-
                  <p>Updates the sensitivity scoring settings for an S3
                  bucket.</p>
                tags:
                  - Update
                  - Resources
                  - Profiles
                  - Detections
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
            /templates/sensitivity-inspections:
              GET:
                summary: ListSensitivityInspectionTemplates
                description: ' <p>Retrieves a subset of information about the sensitivity inspection template for an account.</p>'
                tags:
                  - Lists
                  - Sensitivity
                  - Inspections
                  - Templates
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags (keys and values) from an Amazon
                  Macie resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
            /datasources/search-resources:
              POST:
                summary: SearchResources
                description: >-
                  <p>Retrieves (queries) statistical data and other information
                  about Amazon Web Services resources that Amazon Macie monitors
                  and analyzes.</p>
                tags:
                  - Search
                  - Resources
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
            /custom-data-identifiers/test:
              POST:
                summary: TestCustomDataIdentifier
                description: <p>Tests a custom data identifier.</p>
                tags:
                  - Tests
                  - Custom
                  - Data
                  - Identifiers
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
                  - Tests
            /macie/members/{id}:
              PATCH:
                summary: UpdateMemberSession
                description: >-
                  <p>Enables an Amazon Macie administrator to suspend or
                  re-enable Macie for a member ac
                tags:
                  - Update
                  - Members
                  - Sessions
                  - Invitations
                  - Accept
                  - Custom
                  - Data
                  - Identifiers
                  - Get
                  - Allow
                  - Lists
                  - Jobs
                  - Findings Filter
                  - Members
                  - Findings
                  - Samples
                  - Decline
                  - Identifiers
                  - Delete
                  - Data Source
                  - S3
                  - Administrative
                  - Configurations
                  - Macie
                  - Administrator
                  - Disassociate
                  - Master
                  - Automated
                  - Discovery
                  - Statistics
                  - Classifications
                  - Export
                  - Scopes
                  - Describe
                  - Publication
                  - Count
                  - Resources
                  - Profiles
                  - Reveal
                  - Availability
                  - Templates
                  - Sensitivity
                  - Inspections
                  - Usage
                  - Lists
                  - Managed
                  - Artifacts
                  - Detections
                  - ARN
                  - Search
                  - Resources
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/macie2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/macie2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:macie2
  - name: s3control
    description: >-
      <p> Amazon Web Services S3 Control provides access to Amazon S3 control
      plane actions. </p>
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
            title: s3control
          paths:
            /v20180820/accessgrantsinstance/identitycenter:
              DELETE:
                summary: DissociateAccessGrantsIdentityCenter
                description: >-
                  <p>Dissociates the Amazon Web Services IAM Identity Center
                  instance from the S3 Access Grants instance. </p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:DissociateAccessGrantsIdentityCenter</code>
                  permission to use this operation. </p> </dd> <dt>Additional
                  Permissions</dt> <dd> <p>You must have the
                  <code>sso:DeleteApplication</code> permission to use this
                  operation. </p> </dd> </dl>
                tags:
                  - Dissociate
                  - Access
                  - Grants
                  - Identity
                  - Center
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
            /v20180820/accessgrantsinstance/grant:
              POST:
                summary: CreateAccessGrant
                description: >-
                  <p>Creates an access grant that gives a grantee access to your
                  S3 data. The grantee can be an IAM user or role or a directory
                  user, or group. Before you can create a grant, you must have
                  an S3 Access Grants instance in the same Region as the S3
                  data. You can create an S3 Access Grants instance using the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessGrantsInstance.html">CreateAccessGrantsInstance</a>.
                  You must also have registered at least one S3 data location in
                  your S3 Access Grants instance using <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessGrantsLocation.html">CreateAccessGrantsLocation</a>.
                  </p> <dl> <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:CreateAccessGrant</code> permission to use this
                  operation. </p> </dd> <dt>Additional Permissions</dt> <dd>
                  <p>For any directory identity -
                  <code>sso:DescribeInstance</code> and
                  <code>sso:DescribeApplication</code> </p> <p>For directory
                  users - <code>identitystore:DescribeUser</code> </p> <p>For
                  directory groups - <code>identitystore:DescribeGroup</code>
                  </p> </dd> </dl>
                tags:
                  - Create
                  - Access
                  - Grant
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
            /v20180820/accessgrantsinstance:
              GET:
                summary: GetAccessGrantsInstance
                description: >-
                  <p>Retrieves the S3 Access Grants instance for a Region in
                  your account. </p> <dl> <dt>Permissions</dt> <dd> <p>You must
                  have the <code>s3:GetAccessGrantsInstance</code> permission to
                  use this operation. </p> </dd> </dl>
                tags:
                  - Get
                  - Access
                  - Grants
                  - Instances
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
            /v20180820/accessgrantsinstance/location:
              POST:
                summary: CreateAccessGrantsLocation
                description: >-
                  <p>The S3 data location that you would like to register in
                  your S3 Access Grants instance. Your S3 data must be in the
                  same Region as your S3 Access Grants instance. The location
                  can be one of the following: </p> <ul> <li> <p>The default S3
                  location <code>s3://</code> </p> </li> <li> <p>A bucket -
                  <code>S3://&lt;bucket-name&gt;</code> </p> </li> <li> <p>A
                  bucket and prefix -
                  <code>S3://&lt;bucket-name&gt;/&lt;prefix&gt;</code> </p>
                  </li> </ul> <p>When you register a location, you must include
                  the IAM role that has permission to manage the S3 location
                  that you are registering. Give S3 Access Grants permission to
                  assume this role <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-grants-location.html">using
                  a policy</a>. S3 Access Grants assumes this role to manage
                  access to the location and to vend temporary credentials to
                  grantees or client applications. </p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:CreateAccessGrantsLocation</code> permission to use
                  this operation. </p> </dd> <dt>Additional Permissions</dt>
                  <dd> <p>You must also have the following permission for the
                  specified IAM role: <code>iam:PassRole</code> </p> </dd> </dl>
                tags:
                  - Create
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
            /v20180820/accesspoint/{name}:
              GET:
                summary: GetAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified access point.</p> <p/> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html#API_control_GetAccessPoint_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>GetAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPoint.html">CreateAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPoint.html">DeleteAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListAccessPoints.html">ListAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
            /v20180820/accesspointforobjectlambda/{name}:
              GET:
                summary: GetAccessPointForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified Object Lambda Access Point</p> <p>The
                  following actions are related to
                  <code>GetAccessPointForObjectLambda</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPointForObjectLambda.html">CreateAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointForObjectLambda.html">DeleteAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListAccessPointsForObjectLambda.html">ListAccessPointsForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Access
                  - Points
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
            /v20180820/bucket/{name}:
              GET:
                summary: GetBucket
                description: >-
                  <note> <p>Gets an Amazon S3 on Outposts bucket. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">
                  Using Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <p>If you are using an identity other
                  than the root user of the Amazon Web Services account that
                  owns the Outposts bucket, the calling identity must have the
                  <code>s3-outposts:GetBucket</code> permissions on the
                  specified Outposts bucket and belong to the Outposts bucket
                  owner's account in order to use this action. Only users from
                  Outposts bucket owner account with the right permissions can
                  perform actions on an Outposts bucket. </p> <p> If you don't
                  have <code>s3-outposts:GetBucket</code> permissions or you're
                  not using an identity that belongs to the bucket owner's
                  account, Amazon S3 returns a <code>403 Access Denied</code>
                  error.</p> <p>The following actions are related to
                  <code>GetBucket</code> for Amazon S3 on Outposts:</p> <p>All
                  Amazon S3 on Outposts REST API requests for this action
                  require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucket.html#API_control_GetBucket_Examples">Examples</a>
                  section.</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
            /v20180820/jobs:
              GET:
                summary: ListJobs
                description: >-
                  <p>Lists current S3 Batch Operations jobs as well as the jobs
                  that have ended within the last 30 days for the Amazon Web
                  Services account making the request. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>ListJobs</code> operation, you must have permission to
                  perform the <code>s3:ListJobs</code> action.</p> </dd> </dl>
                  <p>Related actions include:</p> <p/> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobPriority.html">UpdateJobPriority</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Jobs
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
            /v20180820/async-requests/mrap/create:
              POST:
                summary: CreateMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates a Multi-Region Access Point
                  and associates it with the specified buckets. For more
                  information about creating Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CreatingMultiRegionAccessPoints.html">Creating
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This request is asynchronous, meaning that
                  you might receive a response before the command has completed.
                  When this request provides a response, it provides a token
                  that you can use to monitor the status of the request with
                  <code>DescribeMultiRegionAccessPointOperation</code>.</p>
                  <p>The following actions are related to
                  <code>CreateMultiRegionAccessPoint</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
            /v20180820/storagelensgroup:
              GET:
                summary: ListStorageLensGroups
                description: >-
                  <p> Lists all the Storage Lens groups in the specified home
                  Region. </p> <p>To use this operation, you must have the
                  permission to perform the
                  <code>s3:ListStorageLensGroups</code> action. For more
                  information about the required Storage Lens Groups
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about Storage Lens groups errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3LensErrorCodeList">List
                  of Amazon S3 Storage Lens error codes</a>.</p>
                tags:
                  - Lists
                  - Storage
                  - Lens
                  - Groups
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
            /v20180820/accessgrantsinstance/grant/{id}:
              GET:
                summary: GetAccessGrant
                description: >-
                  <p>Get the details of an access grant from your S3 Access
                  Grants instance.</p> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:GetAccessGrant</code> permission to use
                  this operation. </p> </dd> </dl>
                tags:
                  - Get
                  - Access
                  - Grant
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
            /v20180820/accessgrantsinstance/resourcepolicy:
              PUT:
                summary: PutAccessGrantsInstanceResourcePolicy
                description: >-
                  <p>Updates the resource policy of the S3 Access Grants
                  instance. </p> <dl> <dt>Permissions</dt> <dd> <p>You must have
                  the <code>s3:PutAccessGrantsInstanceResourcePolicy</code>
                  permission to use this operation. </p> </dd> </dl>
                tags:
                  - Put
                  - Access
                  - Grants
                  - Instances
                  - Resources
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
            /v20180820/accessgrantsinstance/location/{id}:
              PUT:
                summary: UpdateAccessGrantsLocation
                description: >-
                  <p>Updates the IAM role of a registered location in your S3
                  Access Grants instance.</p> <dl> <dt>Permissions</dt> <dd>
                  <p>You must have the
                  <code>s3:UpdateAccessGrantsLocation</code> permission to use
                  this operation. </p> </dd> <dt>Additional Permissions</dt>
                  <dd> <p>You must also have the following permission:
                  <code>iam:PassRole</code> </p> </dd> </dl>
                tags:
                  - Update
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
            /v20180820/accesspoint/{name}/policy:
              PUT:
                summary: PutAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Associates an access policy with the
                  specified access point. Each access point can have only one
                  policy, so a request made to this API replaces any existing
                  policy associated with the specified access point.</p> <p/>
                  <p>All Amazon S3 on Outposts REST API requests for this action
                  require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutAccessPointPolicy.html#API_control_PutAccessPointPolicy_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutAccessPointPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointPolicy.html">GetAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointPolicy.html">DeleteAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
            /v20180820/accesspointforobjectlambda/{name}/policy:
              PUT:
                summary: PutAccessPointPolicyForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or replaces resource policy
                  for an Object Lambda Access Point. For an example policy, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/olap-create.html#olap-create-cli">Creating
                  Object Lambda Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>PutAccessPointPolicyForObjectLambda</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointPolicyForObjectLambda.html">DeleteAccessPointPolicyForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointPolicyForObjectLambda.html">GetAccessPointPolicyForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Policies
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
            /v20180820/bucket/{name}/lifecycleconfiguration:
              PUT:
                summary: PutBucketLifecycleConfiguration
                description: >-
                  <note> <p>This action puts a lifecycle configuration to an
                  Amazon S3 on Outposts bucket. To put a lifecycle configuration
                  to an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Creates
                  a new lifecycle configuration for the S3 on Outposts bucket or
                  replaces an existing lifecycle configuration. Outposts buckets
                  only support lifecycle configurations that delete/expire
                  objects after a certain period of time and abort incomplete
                  multipart uploads.</p> <p/> <p>All Amazon S3 on Outposts REST
                  API requests for this action require an additional parameter
                  of <code>x-amz-outpost-id</code> to be passed with the
                  request. In addition, you must use an S3 on Outposts endpoint
                  hostname prefix instead of <code>s3-control</code>. For an
                  example of the request syntax for Amazon S3 on Outposts that
                  uses the S3 on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketLifecycleConfiguration.html#API_control_PutBucketLifecycleConfiguration_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketLifecycleConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketLifecycleConfiguration.html">DeleteBucketLifecycleConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Lifecycle
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
            /v20180820/bucket/{name}/policy:
              PUT:
                summary: PutBucketPolicy
                description: >-
                  <note> <p>This action puts a bucket policy to an Amazon S3 on
                  Outposts bucket. To put a policy on an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketPolicy.html">PutBucketPolicy</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Applies
                  an Amazon S3 bucket policy to an Outposts bucket. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>If you are using an identity other than the
                  root user of the Amazon Web Services account that owns the
                  Outposts bucket, the calling identity must have the
                  <code>PutBucketPolicy</code> permissions on the specified
                  Outposts bucket and belong to the bucket owner's account in
                  order to use this action.</p> <p>If you don't have
                  <code>PutBucketPolicy</code> permissions, Amazon S3 returns a
                  <code>403 Access Denied</code> error. If you have the correct
                  permissions, but you're not using an identity that belongs to
                  the bucket owner's account, Amazon S3 returns a <code>405
                  Method Not Allowed</code> error.</p> <important> <p> As a
                  security precaution, the root user of the Amazon Web Services
                  account that owns a bucket can always use this action, even if
                  the policy explicitly denies the root user the ability to
                  perform this action. </p> </important> <p>For more information
                  about bucket policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html">Using
                  Bucket Policies and User Policies</a>.</p> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketPolicy.html#API_control_PutBucketPolicy_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketPolicy.html">GetBucketPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketPolicy.html">DeleteBucketPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
            /v20180820/bucket/{name}/replication:
              PUT:
                summary: PutBucketReplication
                description: >-
                  <note> <p>This action creates an Amazon S3 on Outposts
                  bucket's replication configuration. To create an S3 bucket's
                  replication configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketReplication.html">PutBucketReplication</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Creates
                  a replication configuration or replaces an existing one. For
                  information about S3 replication on Outposts configuration,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsReplication.html">Replicating
                  objects for S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p>It can take a while to propagate
                  <code>PUT</code> or <code>DELETE</code> requests for a
                  replication configuration to all S3 on Outposts systems.
                  Therefore, the replication configuration that's returned by a
                  <code>GET</code> request soon after a <code>PUT</code> or
                  <code>DELETE</code> request might return a more recent result
                  than what's on the Outpost. If an Outpost is offline, the
                  delay in updating the replication configuration on that
                  Outpost can be significant.</p> </note> <p>Specify the
                  replication configuration in the request body. In the
                  replication configuration, you provide the following
                  information:</p> <ul> <li> <p>The name of the destination
                  bucket or buckets where you want S3 on Outposts to replicate
                  objects</p> </li> <li> <p>The Identity and Access Management
                  (IAM) role that S3 on Outposts can assume to replicate objects
                  on your behalf</p> </li> <li> <p>Other relevant information,
                  such as replication rules</p> </li> </ul> <p>A replication
                  configuration must include at least one rule and can contain a
                  maximum of 100. Each rule identifies a subset of objects to
                  replicate by filtering the objects in the source Outposts
                  bucket. To choose additional subsets of objects to replicate,
                  add a rule for each subset.</p> <p>To specify a subset of the
                  objects in the source Outposts bucket to apply a replication
                  rule to, add the <code>Filter</code> element as a child of the
                  <code>Rule</code> element. You can filter objects based on an
                  object key prefix, one or more object tags, or both. When you
                  add the <code>Filter</code> element in the configuration, you
                  must also add the following elements:
                  <code>DeleteMarkerReplication</code>, <code>Status</code>, and
                  <code>Priority</code>.</p> <p>Using
                  <code>PutBucketReplication</code> on Outposts requires that
                  both the source and destination buckets must have versioning
                  enabled. For information about enabling versioning on a
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsManagingVersioning.html">Managing
                  S3 Versioning for your S3 on Outposts bucket</a>.</p> <p>For
                  information about S3 on Outposts replication failure reasons,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/outposts-replication-eventbridge.html#outposts-replication-failure-codes">Replication
                  failure reasons</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p> <b>Handling Replication of Encrypted Objects</b> </p>
                  <p>Outposts buckets are encrypted at all times. All the
                  objects in the source Outposts bucket are encrypted and can be
                  replicated. Also, all the replicas in the destination Outposts
                  bucket are encrypted with the same encryption key as the
                  objects in the source Outposts bucket.</p> <p>
                  <b>Permissions</b> </p> <p>To create a
                  <code>PutBucketReplication</code> request, you must have
                  <code>s3-outposts:PutReplicationConfiguration</code>
                  permissions for the bucket. The Outposts bucket owner has this
                  permission by default and can grant it to others. For more
                  information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsIAM.html">Setting
                  up IAM with S3 on Outposts</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsBucketPolicy.html">Managing
                  access to S3 on Outposts buckets</a>. </p> <note> <p>To
                  perform this operation, the user or role must also have the
                  <code>iam:CreateRole</code> and <code>iam:PassRole</code>
                  permissions. For more information, see <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">Granting
                  a user permissions to pass a role to an Amazon Web Services
                  service</a>.</p> </note> <p>All Amazon S3 on Outposts REST API
                  requests for this action require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketReplication.html#API_control_PutBucketReplication_Examples">Examples</a>
                  section.</p> <p>The following operations are related to
                  <code>PutBucketReplication</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketReplication.html">GetBucketReplication</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketReplication.html">DeleteBucketReplication</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Replication
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
            /v20180820/bucket/{name}/tagging:
              PUT:
                summary: PutBucketTagging
                description: >-
                  <note> <p>This action puts tags on an Amazon S3 on Outposts
                  bucket. To put tags on an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketTagging.html">PutBucketTagging</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Sets
                  the tags for an S3 on Outposts bucket. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>Use tags to organize your Amazon Web
                  Services bill to reflect your own cost structure. To do this,
                  sign up to get your Amazon Web Services account bill with tag
                  key values included. Then, to see the cost of combined
                  resources, organize your billing information according to
                  resources with the same tag key values. For example, you can
                  tag several resources with a specific application name, and
                  then organize your billing information to see the total cost
                  of that application across several services. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Cost
                  allocation and tagging</a>.</p> <note> <p>Within a bucket, if
                  you add a tag that has the same key as an existing tag, the
                  new value overwrites the old value. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">
                  Using cost allocation in Amazon S3 bucket tags</a>.</p>
                  </note> <p>To use this action, you must have permissions to
                  perform the <code>s3-outposts:PutBucketTagging</code> action.
                  The Outposts bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">
                  Permissions Related to Bucket Subresource Operations</a> and
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  access permissions to your Amazon S3 resources</a>.</p> <p>
                  <code>PutBucketTagging</code> has the following special
                  errors:</p> <ul> <li> <p>Error code:
                  <code>InvalidTagError</code> </p> <ul> <li> <p>Description:
                  The tag provided was not a valid tag. This error can occur if
                  the tag did not pass input validation. For information about
                  tag restrictions, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">
                  User-Defined Tag Restrictions</a> and <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/aws-tag-restrictions.html">
                  Amazon Web Services-Generated Cost Allocation Tag
                  Restrictions</a>.</p> </li> </ul> </li> <li> <p>Error code:
                  <code>MalformedXMLError</code> </p> <ul> <li> <p>Description:
                  The XML provided does not match the schema.</p> </li> </ul>
                  </li> <li> <p>Error code: <code>OperationAbortedError </code>
                  </p> <ul> <li> <p>Description: A conflicting conditional
                  action is currently in progress against this resource. Try
                  again.</p> </li> </ul> </li> <li> <p>Error code:
                  <code>InternalError</code> </p> <ul> <li> <p>Description: The
                  service was unable to apply the provided tag to the
                  bucket.</p> </li> </ul> </li> </ul> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketTagging.html#API_control_PutBucketTagging_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketTagging.html">GetBucketTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketTagging.html">DeleteBucketTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
            /v20180820/jobs/{id}/tagging:
              PUT:
                summary: PutJobTagging
                description: >-
                  <p>Sets the supplied tag-set on an S3 Batch Operations
                  job.</p> <p>A tag is a key-value pair. You can associate S3
                  Batch Operations tags with any job by sending a PUT request
                  against the tagging subresource that is associated with the
                  job. To modify the existing tag set, you can either replace
                  the existing tag set entirely, or make changes within the
                  existing tag set by retrieving the existing tag set using <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetJobTagging.html">GetJobTagging</a>,
                  modify that tag set, and use this operation to replace the tag
                  set with the one you modified. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/batch-ops-managing-jobs.html#batch-ops-job-tags">Controlling
                  access and labeling jobs using tags</a> in the <i>Amazon S3
                  User Guide</i>. </p> <note> <ul> <li> <p>If you send this
                  request with an empty tag set, Amazon S3 deletes the existing
                  tag set on the Batch Operations job. If you use this method,
                  you are charged for a Tier 1 Request (PUT). For more
                  information, see <a
                  href="http://aws.amazon.com/s3/pricing/">Amazon S3
                  pricing</a>.</p> </li> <li> <p>For deleting existing tags for
                  your Batch Operations job, a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteJobTagging.html">DeleteJobTagging</a>
                  request is preferred because it achieves the same result
                  without incurring charges.</p> </li> <li> <p>A few things to
                  consider about using tags:</p> <ul> <li> <p>Amazon S3 limits
                  the maximum number of tags to 50 tags per job.</p> </li> <li>
                  <p>You can associate up to 50 tags with a job as long as they
                  have unique tag keys.</p> </li> <li> <p>A tag key can be up to
                  128 Unicode characters in length, and tag values can be up to
                  256 Unicode characters in length.</p> </li> <li> <p>The key
                  and values are case sensitive.</p> </li> <li> <p>For
                  tagging-related restrictions related to characters and
                  encodings, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">User-Defined
                  Tag Restrictions</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p> </li> </ul> </li> </ul> </note> <dl>
                  <dt>Permissions</dt> <dd> <p>To use the
                  <code>PutJobTagging</code> operation, you must have permission
                  to perform the <code>s3:PutJobTagging</code> action.</p> </dd>
                  </dl> <p>Related actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetJobTagging.html">GetJobTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteJobTagging.html">DeleteJobTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Jobs
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
            /v20180820/async-requests/mrap/delete:
              POST:
                summary: DeleteMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Deletes a Multi-Region Access Point.
                  This action does not delete the buckets associated with the
                  Multi-Region Access Point, only the Multi-Region Access Point
                  itself.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This request is asynchronous, meaning that
                  you might receive a response before the command has completed.
                  When this request provides a response, it provides a token
                  that you can use to monitor the status of the request with
                  <code>DescribeMultiRegionAccessPointOperation</code>.</p>
                  <p>The following actions are related to
                  <code>DeleteMultiRegionAccessPoint</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Delete
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
            /v20180820/configuration/publicAccessBlock:
              PUT:
                summary: PutPublicAccessBlock
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies the
                  <code>PublicAccessBlock</code> configuration for an Amazon Web
                  Services account. For this operation, users must have the
                  <code>s3:PutAccountPublicAccessBlock</code> permission. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">
                  Using Amazon S3 block public access</a>.</p> <p>Related
                  actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Public
                  - Access
                  - Blocks
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
            /v20180820/storagelens/{storagelensid}:
              PUT:
                summary: PutStorageLensConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Puts an Amazon S3 Storage Lens
                  configuration. For more information about S3 Storage Lens, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Working
                  with Amazon S3 Storage Lens</a> in the <i>Amazon S3 User
                  Guide</i>. For a complete list of S3 Storage Lens metrics, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html">S3
                  Storage Lens metrics glossary</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p>To use this action, you must have
                  permission to perform the
                  <code>s3:PutStorageLensConfiguration</code> action. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Put
                  - Storage
                  - Lens
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/storagelens/{storagelensid}/tagging:
              PUT:
                summary: PutStorageLensConfigurationTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Put or replace tags on an existing
                  Amazon S3 Storage Lens configuration. For more information
                  about S3 Storage Lens, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Assessing
                  your storage activity and usage with Amazon S3 Storage Lens
                  </a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>To use
                  this action, you must have permission to perform the
                  <code>s3:PutStorageLensConfigurationTagging</code> action. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Put
                  - Storage
                  - Lens
                  - Configurations
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/storagelensgroup/{name}:
              PUT:
                summary: UpdateStorageLensGroup
                description: >-
                  <p> Updates the existing Storage Lens group.</p> <p>To use
                  this operation, you must have the permission to perform the
                  <code>s3:UpdateStorageLensGroup</code> action. For more
                  information about the required Storage Lens Groups
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about Storage Lens groups errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3LensErrorCodeList">List
                  of Amazon S3 Storage Lens error codes</a>.</p>
                tags:
                  - Update
                  - Storage
                  - Lens
                  - Group
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/jobs/{id}:
              GET:
                summary: DescribeJob
                description: >-
                  <p>Retrieves the configuration parameters and status for a
                  Batch Operations job. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>DescribeJob</code> operation, you must have permission
                  to perform the <code>s3:DescribeJob</code> action.</p> </dd>
                  </dl> <p>Related actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobPriority.html">UpdateJobPriority</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Describe
                  - Jobs
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/async-requests/mrap/{request_token+}:
              GET:
                summary: DescribeMultiRegionAccessPointOperation
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Retrieves the status of an
                  asynchronous request to manage a Multi-Region Access Point.
                  For more information about managing Multi-Region Access Points
                  and how asynchronous requests work, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Describe
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Operation
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
            /v20180820/accessgrantsinstance/prefix:
              GET:
                summary: GetAccessGrantsInstanceForPrefix
                description: >-
                  <p>Retrieve the S3 Access Grants instance that contains a
                  particular prefix. </p> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:GetAccessGrantsInstanceForPrefix</code>
                  permission for the caller account to use this operation. </p>
                  </dd> <dt>Additional Permissions</dt> <dd> <p>The prefix owner
                  account must grant you the following permissions to their S3
                  Access Grants instance:
                  <code>s3:GetAccessGrantsInstanceForPrefix</code>. </p> </dd>
                  </dl>
                tags:
                  - Get
                  - Access
                  - Grants
                  - Instances
                  - For
                  - Prefix
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
            /v20180820/accesspointforobjectlambda/{name}/configuration:
              PUT:
                summary: PutAccessPointConfigurationForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Replaces configuration for an Object
                  Lambda Access Point.</p> <p>The following actions are related
                  to
                  <code>PutAccessPointConfigurationForObjectLambda</code>:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointConfigurationForObjectLambda.html">GetAccessPointConfigurationForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Configurations
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
            /v20180820/accesspoint/{name}/policyStatus:
              GET:
                summary: GetAccessPointPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Indicates whether the specified access
                  point currently has a policy that allows public access. For
                  more information about public access through access points,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html">Managing
                  Data Access with Amazon S3 access points</a> in the <i>Amazon
                  S3 User Guide</i>.</p>
                tags:
                  - Get
                  - Access
                  - Points
                  - Policies
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
            /v20180820/accesspointforobjectlambda/{name}/policyStatus:
              GET:
                summary: GetAccessPointPolicyStatusForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the status of the resource
                  policy associated with an Object Lambda Access Point.</p>
                tags:
                  - Get
                  - Access
                  - Points
                  - Policies
                  - Status
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
            /v20180820/bucket/{name}/versioning:
              PUT:
                summary: PutBucketVersioning
                description: >-
                  <note> <p>This operation sets the versioning state for S3 on
                  Outposts buckets only. To set the versioning state for an S3
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketVersioning.html">PutBucketVersioning</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Sets
                  the versioning state for an S3 on Outposts bucket. With S3
                  Versioning, you can save multiple distinct copies of your
                  objects and recover from unintended user actions and
                  application failures.</p> <p>You can set the versioning state
                  to one of the following:</p> <ul> <li> <p> <b>Enabled</b> -
                  Enables versioning for the objects in the bucket. All objects
                  added to the bucket receive a unique version ID.</p> </li>
                  <li> <p> <b>Suspended</b> - Suspends versioning for the
                  objects in the bucket. All objects added to the bucket receive
                  the version ID <code>null</code>.</p> </li> </ul> <p>If you've
                  never set versioning on your bucket, it has no versioning
                  state. In that case, a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketVersioning.html">
                  GetBucketVersioning</a> request does not return a versioning
                  state value.</p> <p>When you enable S3 Versioning, for each
                  object in your bucket, you have a current version and zero or
                  more noncurrent versions. You can configure your bucket S3
                  Lifecycle rules to expire noncurrent versions after a
                  specified time period. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsLifecycleManaging.html">
                  Creating and managing a lifecycle configuration for your S3 on
                  Outposts bucket</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p>If you have an object expiration lifecycle configuration in
                  your non-versioned bucket and you want to maintain the same
                  permanent delete behavior when you enable versioning, you must
                  add a noncurrent expiration policy. The noncurrent expiration
                  lifecycle configuration will manage the deletes of the
                  noncurrent object versions in the version-enabled bucket. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html">Versioning</a>
                  in the <i>Amazon S3 User Guide</i>.</p> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketVersioning.html#API_control_PutBucketVersioning_Examples">Examples</a>
                  section.</p> <p>The following operations are related to
                  <code>PutBucketVersioning</code> for S3 on Outposts.</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketVersioning.html">GetBucketVersioning</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Versioning
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
            /v20180820/accessgrantsinstance/dataaccess:
              GET:
                summary: GetDataAccess
                description: >-
                  <p>Returns a temporary access credential from S3 Access Grants
                  to the grantee or client application. The <a
                  href="https://docs.aws.amazon.com/STS/latest/APIReference/API_Credentials.html">temporary
                  credential</a> is an Amazon Web Services STS token that grants
                  them access to the S3 data. </p> <dl> <dt>Permissions</dt>
                  <dd> <p>You must have the <code>s3:GetDataAccess</code>
                  permission to use this operation. </p> </dd> <dt>Additional
                  Permissions</dt> <dd> <p>The IAM role that S3 Access Grants
                  assumes must have the following permissions specified in the
                  trust policy when registering the location:
                  <code>sts:AssumeRole</code>, for directory users or groups
                  <code>sts:SetContext</code>, and for IAM users or roles
                  <code>sts:SourceIdentity</code>. </p> </dd> </dl>
                tags:
                  - Get
                  - Data
                  - Access
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
            /v20180820/mrap/instances/{name+}:
              GET:
                summary: GetMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified Multi-Region Access Point.</p> <p>This
                  action will always be routed to the US West (Oregon) Region.
                  For more information about the restrictions around managing
                  Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
            /v20180820/mrap/instances/{name+}/policy:
              GET:
                summary: GetMultiRegionAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the access control policy of
                  the specified Multi-Region Access Point.</p> <p>This action
                  will always be routed to the US West (Oregon) Region. For more
                  information about the restrictions around managing
                  Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPointPolicy</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicyStatus.html">GetMultiRegionAccessPointPolicyStatus</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutMultiRegionAccessPointPolicy.html">PutMultiRegionAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
            /v20180820/mrap/instances/{name+}/policystatus:
              GET:
                summary: GetMultiRegionAccessPointPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Indicates whether the specified
                  Multi-Region Access Point has an access control policy that
                  allows public access.</p> <p>This action will always be routed
                  to the US West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPointPolicyStatus</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicy.html">GetMultiRegionAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutMultiRegionAccessPointPolicy.html">PutMultiRegionAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
            /v20180820/mrap/instances/{mrap+}/routes:
              PATCH:
                summary: SubmitMultiRegionAccessPointRoutes
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Submits an updated route configuration
                  for a Multi-Region Access Point. This API operation updates
                  the routing status for the specified Regions from active to
                  passive, or from passive to active. A value of <code>0</code>
                  indicates a passive status, which means that traffic won't be
                  routed to the specified Region. A value of <code>100</code>
                  indicates an active status, which means that traffic will be
                  routed to the specified Region. At least one Region must be
                  active at all times.</p> <p>When the routing configuration is
                  changed, any in-progress operations (uploads, copies, deletes,
                  and so on) to formerly active Regions will continue to run to
                  their final completion state (success or failure). The routing
                  configurations of any Regions that aren’t specified remain
                  unchanged.</p> <note> <p>Updated routing configurations might
                  not be immediately applied. It can take up to 2 minutes for
                  your changes to take effect.</p> </note> <p>To submit routing
                  control changes and failover requests, use the Amazon S3
                  failover control infrastructure endpoints in these five Amazon
                  Web Services Regions:</p> <ul> <li> <p> <code>us-east-1</code>
                  </p> </li> <li> <p> <code>us-west-2</code> </p> </li> <li> <p>
                  <code>ap-southeast-2</code> </p> </li> <li> <p>
                  <code>ap-northeast-1</code> </p> </li> <li> <p>
                  <code>eu-west-1</code> </p> </li> </ul> <note> <p>Your Amazon
                  S3 bucket does not need to be in these five Regions.</p>
                  </note>
                tags:
                  - Submit
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Routes
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
            /v20180820/accessgrantsinstance/grants:
              GET:
                summary: ListAccessGrants
                description: >-
                  <p>Returns the list of access grants in your S3 Access Grants
                  instance.</p> <dl> <dt>Permissions</dt> <dd> <p>You must have
                  the <code>s3:ListAccessGrants</code> permission to use this
                  operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
            /v20180820/accessgrantsinstances:
              GET:
                summary: ListAccessGrantsInstances
                description: >-
                  <p>Returns a list of S3 Access Grants instances. An S3 Access
                  Grants instance serves as a logical grouping for your
                  individual access grants. You can only have one S3 Access
                  Grants instance per Region per account.</p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:ListAccessGrantsInstances</code> permission to use
                  this operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - Instances
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
            /v20180820/accessgrantsinstance/locations:
              GET:
                summary: ListAccessGrantsLocations
                description: >-
                  <p>Returns a list of the locations registered in your S3
                  Access Grants instance.</p> <dl> <dt>Permissions</dt> <dd>
                  <p>You must have the <code>s3:ListAccessGrantsLocations</code>
                  permission to use this operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/accesspoint:
              GET:
                summary: ListAccessPoints
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of the access points
                  that are owned by the current account that's associated with
                  the specified bucket. You can retrieve up to 1000 access
                  points per call. If the specified bucket has more than 1,000
                  access points (or the number specified in
                  <code>maxResults</code>, whichever is less), the response will
                  include a continuation token that you can use to list the
                  additional access points.</p> <p/> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html#API_control_GetAccessPoint_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>ListAccessPoints</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPoint.html">CreateAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPoint.html">DeleteAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html">GetAccessPoint</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/accesspointforobjectlambda:
              GET:
                summary: ListAccessPointsForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns some or all (up to 1,000)
                  access points associated with the Object Lambda Access Point
                  per call. If there are more access points than what can be
                  returned in one call, the response will include a continuation
                  token that you can use to list the additional access
                  points.</p> <p>The following actions are related to
                  <code>ListAccessPointsForObjectLambda</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPointForObjectLambda.html">CreateAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointForObjectLambda.html">DeleteAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointForObjectLambda.html">GetAccessPointForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Access
                  - Points
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/mrap/instances:
              GET:
                summary: ListMultiRegionAccessPoints
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of the Multi-Region
                  Access Points currently associated with the specified Amazon
                  Web Services account. Each call can return up to 100
                  Multi-Region Access Points, the maximum number of Multi-Region
                  Access Points that can be associated with a single
                  account.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>ListMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/bucket:
              GET:
                summary: ListRegionalBuckets
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of all Outposts buckets
                  in an Outpost that are owned by the authenticated sender of
                  the request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>For an example of the request syntax for
                  Amazon S3 on Outposts that uses the S3 on Outposts endpoint
                  hostname prefix and <code>x-amz-outpost-id</code> in your
                  request, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListRegionalBuckets.html#API_control_ListRegionalBuckets_Examples">Examples</a>
                  section.</p>
                tags:
                  - Lists
                  - Regional
                  - Buckets
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/storagelens:
              GET:
                summary: ListStorageLensConfigurations
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Gets a list of Amazon S3 Storage Lens
                  configurations. For more information about S3 Storage Lens,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Assessing
                  your storage activity and usage with Amazon S3 Storage Lens
                  </a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>To use
                  this action, you must have permission to perform the
                  <code>s3:ListStorageLensConfigurations</code> action. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Lists
                  - Storage
                  - Lens
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/tags/{resourceArn+}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p> This operation removes the specified Amazon Web Services
                  resource tags from an S3 resource. Each tag is a label
                  consisting of a user-defined key and value. Tags can help you
                  manage, identify, organize, search for, and filter resources.
                  </p> <note> <p>This operation is only supported for <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-lens-groups.html">S3
                  Storage Lens groups</a> and for <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-grants-tagging.html">S3
                  Access Grants</a>. The tagged resource can be an S3 Storage
                  Lens group or S3 Access Grants instance, registered location,
                  or grant. </p> </note> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:UntagResource</code> permission to use
                  this operation. </p> </dd> </dl> <p>For more information about
                  the required Storage Lens Groups permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about S3 Tagging errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3TaggingErrorCodeList">List
                  of Amazon S3 Tagging error codes</a>.</p>
                tags:
                  - Untag
                  - Resources
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
            /v20180820/async-requests/mrap/put-policy:
              POST:
                summary: PutMultiRegionAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Associates an access control policy
                  with the specified Multi-Region Access Point. Each
                  Multi-Region Access Point can have only one policy, so a
                  request made to this action replaces any existing policy that
                  is associated with the specified Multi-Region Access
                  Point.</p> <p>This action will always be routed to the US West
                  (Oregon) Region. For more information about the restrictions
                  around managing Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>PutMultiRegionAccessPointPolicy</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicy.html">GetMultiRegionAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicyStatus.html">GetMultiRegionAccessPointPolicyStatus</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
            /v20180820/jobs/{id}/priority:
              POST:
                summary: UpdateJobPriority
                description: >-
                  <p>Updates an existing S3 Batch Operations job's priority. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>UpdateJobPriority</code> operation, you must have
                  permission to perform the <code>s3:UpdateJobPriority</code>
                  action.</p> </dd> </dl> <p>Related actions include:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Update
                  - Jobs
                  - Priorities
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
                  - Priorities
            /v20180820/jobs/{id}/status:
              POST:
                summary: UpdateJobStatus
                description: >-
                  <p>Updates the status for the specified job. Use this
                  operation to confirm that you want to run a job or to cancel
                  an existing job. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>UpdateJobStatus</code> operation, you must have
                  permission to perform the <code>s3:UpdateJobStatus</code>
                  action.</p> </dd> </dl> <p>Related actions include:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> <
                tags:
                  - Update
                  - Jobs
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
                  - Priorities
    overlays:
      - type: APIs.io Search
        url: overlays/s3control-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3control-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3control
  - name: s3
    description: <p/>
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
            title: s3
          paths:
            /{Bucket}/{Key+}:
              PUT:
                summary: UploadPartCopy
                description: >-
                  <p>Uploads a part by copying data from an existing object as
                  data source. To specify the data source, you add the request
                  header <code>x-amz-copy-source</code> in your request. To
                  specify a byte range, you add the request header
                  <code>x-amz-copy-source-range</code> in your request. </p>
                  <p>For information about maximum and minimum part sizes and
                  other multipart upload specifications, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/qfacts.html">Multipart
                  upload limits</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <note> <p>Instead of copying data from an existing object as
                  part data, you might use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  action to upload new data as a part of an object in your
                  request.</p> </note> <p>You must initiate a multipart upload
                  before you can upload any part. In response to your initiate
                  request, Amazon S3 returns the upload ID, a unique identifier
                  that you must include in your upload part request.</p> <p>For
                  conceptual information about multipart uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html">Uploading
                  Objects Using Multipart Upload</a> in the <i>Amazon S3 User
                  Guide</i>. For information about copying objects using a
                  single atomic action vs. a multipart upload, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/ObjectOperations.html">Operations
                  on Objects</a> in the <i>Amazon S3 User Guide</i>.</p> <note>
                  <p> <b>Directory buckets</b> - For directory buckets, you must
                  make requests for this API operation to the Zonal endpoint.
                  These endpoints support virtual-hosted-style requests in the
                  format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Authentication and
                  authorization</dt> <dd> <p>All <code>UploadPartCopy</code>
                  requests must be authenticated and signed by using IAM
                  credentials (access key ID and secret access key for the IAM
                  identities). All headers with the <code>x-amz-</code> prefix,
                  including <code>x-amz-copy-source</code>, must be signed. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html">REST
                  Authentication</a>.</p> <p> <b>Directory buckets</b> - You
                  must use IAM credentials to authenticate and authorize your
                  access to the <code>UploadPartCopy</code> API operation,
                  instead of using the temporary security credentials through
                  the <code>CreateSession</code> API operation.</p> <p>Amazon
                  Web Services CLI or SDKs handles authentication and
                  authorization on your behalf.</p> </dd> <dt>Permissions</dt>
                  <dd> <p>You must have <code>READ</code> access to the source
                  object and <code>WRITE</code> access to the destination
                  bucket.</p> <ul> <li> <p> <b>General purpose bucket
                  permissions</b> - You must have the permissions in a policy
                  based on the bucket types of your source bucket and
                  destination bucket in an <code>UploadPartCopy</code>
                  operation.</p> <ul> <li> <p>If the source object is in a
                  general purpose bucket, you must have the <b>
                  <code>s3:GetObject</code> </b> permission to read the source
                  object that is being copied. </p> </li> <li> <p>If the
                  destination bucket is a general purpose bucket, you must have
                  the <b> <code>s3:PubObject</code> </b> permission to write the
                  object copy to the destination bucket. </p> </li> </ul> <p>For
                  information about permissions required to use the multipart
                  upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  Upload and Permissions</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - You must have permissions in a bucket policy
                  or an IAM identity-based policy based on the source and
                  destination bucket types in an <code>UploadPartCopy</code>
                  operation.</p> <ul> <li> <p>If the source object that you want
                  to copy is in a directory bucket, you must have the <b>
                  <code>s3express:CreateSession</code> </b> permission in the
                  <code>Action</code> element of a policy to read the object .
                  By default, the session is in the <code>ReadWrite</code> mode.
                  If you want to restrict the access, you can explicitly set the
                  <code>s3express:SessionMode</code> condition key to
                  <code>ReadOnly</code> on the copy source bucket.</p> </li>
                  <li> <p>If the copy destination is a directory bucket, you
                  must have the <b> <code>s3express:CreateSession</code> </b>
                  permission in the <code>Action</code> element of a policy to
                  write the object to the destination. The
                  <code>s3express:SessionMode</code> condition key cannot be set
                  to <code>ReadOnly</code> on the copy destination. </p> </li>
                  </ul> <p>For example policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-identity-policies.html">Amazon
                  Web Services Identity and Access Management (IAM)
                  identity-based policies for S3 Express One Zone</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <ul> <li> <p> <b>General purpose
                  buckets </b> - For information about using server-side
                  encryption with customer-provided encryption keys with the
                  <code>UploadPartCopy</code> operation, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>.
                  </p> </li> <li> <p> <b>Directory buckets </b> - For directory
                  buckets, only server-side encryption with Amazon S3 managed
                  keys (SSE-S3) (<code>AES256</code>) is supported.</p> </li>
                  </ul> </dd> <dt>Special errors</dt> <dd> <ul> <li> <p>Error
                  Code: <code>NoSuchUpload</code> </p> <ul> <li> <p>Description:
                  The specified multipart upload does not exist. The upload ID
                  might be invalid, or the multipart upload might have been
                  aborted or completed.</p> </li> <li> <p>HTTP Status Code: 404
                  Not Found</p> </li> </ul> </li> <li> <p>Error Code:
                  <code>InvalidRequest</code> </p> <ul> <li> <p>Description: The
                  specified copy source is not supported as a byte-range copy
                  source.</p> </li> <li> <p>HTTP Status Code: 400 Bad
                  Request</p> </li> </ul> </li> </ul> </dd> <dt>HTTP Host header
                  syntax</dt> <dd> <p> <b>Directory buckets </b> - The HTTP Host
                  header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>UploadPartCopy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListMultipartUploads.html">ListMultipartUploads</a>
                  </p> </li> </ul>
                tags:
                  - Uploads
                  - Part
                  - Copy
                  - Bucket
                  - Keys
            /{Bucket}:
              GET:
                summary: ListObjects
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns some or all (up to 1,000) of
                  the objects in a bucket. You can use the request parameters as
                  selection criteria to return a subset of the objects in a
                  bucket. A 200 OK response can contain valid or invalid XML. Be
                  sure to design your application to parse the contents of the
                  response and handle it appropriately.</p> <important> <p>This
                  action has been revised. We recommend that you use the newer
                  version, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>,
                  when developing applications. For backward compatibility,
                  Amazon S3 continues to support <code>ListObjects</code>.</p>
                  </important> <p>The following operations are related to
                  <code>ListObjects</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html">ListBuckets</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - Bucket
                  - Keys
            /{Bucket}/{Key+}?uploads:
              POST:
                summary: CreateMultipartUpload
                description: >-
                  <p>This action initiates a multipart upload and returns an
                  upload ID. This upload ID is used to associate all of the
                  parts in the specific multipart upload. You specify this
                  upload ID in each of your subsequent upload part requests (see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>).
                  You also include this upload ID in the final request to either
                  complete or abort the multipart upload request. For more
                  information about multipart uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html">Multipart
                  Upload Overview</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <note> <p>After you initiate a multipart upload and upload one
                  or more parts, to stop being charged for storing the uploaded
                  parts, you must either complete or abort the multipart upload.
                  Amazon S3 frees up the space used to store the parts and stops
                  charging you for storing them only after you either complete
                  or abort a multipart upload. </p> </note> <p>If you have
                  configured a lifecycle rule to abort incomplete multipart
                  uploads, the created multipart upload must be completed within
                  the number of days specified in the bucket lifecycle
                  configuration. Otherwise, the incomplete multipart upload
                  becomes eligible for an abort action and Amazon S3 aborts the
                  multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html#mpu-abort-incomplete-mpu-lifecycle-config">Aborting
                  Incomplete Multipart Uploads Using a Bucket Lifecycle
                  Configuration</a>.</p> <note> <ul> <li> <p> <b>Directory
                  buckets </b> - S3 Lifecycle is not supported by directory
                  buckets.</p> </li> <li> <p> <b>Directory buckets </b> - For
                  directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> </ul> </note> <dl> <dt>Request
                  signing</dt> <dd> <p>For request signing, multipart upload is
                  just a series of regular requests. You initiate a multipart
                  upload, send one or more requests to upload parts, and then
                  complete the multipart upload process. You sign each request
                  individually. There is nothing special about signing multipart
                  upload requests. For more information about signing, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
                  Requests (Amazon Web Services Signature Version 4)</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Permissions</dt>
                  <dd> <ul> <li> <p> <b>General purpose bucket permissions</b> -
                  For information about the permissions required to use the
                  multipart upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  upload and permissions</a> in the <i>Amazon S3 User Guide</i>.
                  </p> <p>To perform a multipart upload with encryption by using
                  an Amazon Web Services KMS key, the requester must have
                  permission to the <code>kms:Decrypt</code> and
                  <code>kms:GenerateDataKey*</code> actions on the key. These
                  permissions are required because Amazon S3 must decrypt and
                  read data from the encrypted file parts before it completes
                  the multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpuoverview.html#mpuAndPermissions">Multipart
                  upload API and permissions</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  data using server-side encryption with Amazon Web Services
                  KMS</a> in the <i>Amazon S3 User Guide</i>.</p> </li> <li> <p>
                  <b>Directory bucket permissions</b> - To grant access to this
                  API operation on a directory bucket, we recommend that you use
                  the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <ul> <li> <p> <b>General purpose
                  buckets</b> - Server-side encryption is for data encryption at
                  rest. Amazon S3 encrypts your data as it writes it to disks in
                  its data centers and decrypts it when you access it. Amazon S3
                  automatically encrypts all new objects that are uploaded to an
                  S3 bucket. When doing a multipart upload, if you don't specify
                  encryption information in your request, the encryption setting
                  of the uploaded parts is set to the default encryption
                  configuration of the destination bucket. By default, all
                  buckets have a base level of encryption configuration that
                  uses server-side encryption with Amazon S3 managed keys
                  (SSE-S3). If the destination bucket has a default encryption
                  configuration that uses server-side encryption with an Key
                  Management Service (KMS) key (SSE-KMS), or a customer-provided
                  encryption key (SSE-C), Amazon S3 uses the corresponding KMS
                  key, or a customer-provided key to encrypt the uploaded parts.
                  When you perform a CreateMultipartUpload operation, if you
                  want to use a different type of encryption setting for the
                  uploaded parts, you can request that Amazon S3 encrypts the
                  object with a different encryption key (such as an Amazon S3
                  managed key, a KMS key, or a customer-provided key). When the
                  encryption setting in your request is different from the
                  default encryption configuration of the destination bucket,
                  the encryption setting in your request takes precedence. If
                  you choose to provide your own encryption key, the request
                  headers you provide in <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPartCopy.html">UploadPartCopy</a>
                  requests must match the headers you used in the
                  <code>CreateMultipartUpload</code> request.</p> <ul> <li>
                  <p>Use KMS keys (SSE-KMS) that include the Amazon Web Services
                  managed key (<code>aws/s3</code>) and KMS customer managed
                  keys stored in Key Management Service (KMS) – If you want
                  Amazon Web Services to manage the keys used to encrypt data,
                  specify the following headers in the request.</p> <ul> <li>
                  <p> <code>x-amz-server-side-encryption</code> </p> </li> <li>
                  <p> <code>x-amz-server-side-encryption-aws-kms-key-id</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-context</code> </p> </li>
                  </ul> <note> <ul> <li> <p>If you specify
                  <code>x-amz-server-side-encryption:aws:kms</code>, but don't
                  provide
                  <code>x-amz-server-side-encryption-aws-kms-key-id</code>,
                  Amazon S3 uses the Amazon Web Services managed key
                  (<code>aws/s3</code> key) in KMS to protect the data.</p>
                  </li> <li> <p>To perform a multipart upload with encryption by
                  using an Amazon Web Services KMS key, the requester must have
                  permission to the <code>kms:Decrypt</code> and
                  <code>kms:GenerateDataKey*</code> actions on the key. These
                  permissions are required because Amazon S3 must decrypt and
                  read data from the encrypted file parts before it completes
                  the multipart upload. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/mpuoverview.html#mpuAndPermissions">Multipart
                  upload API and permissions</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  data using server-side encryption with Amazon Web Services
                  KMS</a> in the <i>Amazon S3 User Guide</i>.</p> </li> <li>
                  <p>If your Identity and Access Management (IAM) user or role
                  is in the same Amazon Web Services account as the KMS key,
                  then you must have these permissions on the key policy. If
                  your IAM user or role is in a different account from the key,
                  then you must have the permissions on both the key policy and
                  your IAM user or role.</p> </li> <li> <p>All <code>GET</code>
                  and <code>PUT</code> requests for an object protected by KMS
                  fail if you don't make them by using Secure Sockets Layer
                  (SSL), Transport Layer Security (TLS), or Signature Version 4.
                  For information about configuring any of the officially
                  supported Amazon Web Services SDKs and Amazon Web Services
                  CLI, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingAWSSDK.html#specify-signature-version">Specifying
                  the Signature Version in Request Authentication</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> </ul> </note> <p>For
                  more information about server-side encryption with KMS keys
                  (SSE-KMS), see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html">Protecting
                  Data Using Server-Side Encryption with KMS keys</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> <li> <p>Use
                  customer-provided encryption keys (SSE-C) – If you want to
                  manage your own encryption keys, provide all the following
                  headers in the request.</p> <ul> <li> <p>
                  <code>x-amz-server-side-encryption-customer-algorithm</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key</code> </p>
                  </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key-MD5</code>
                  </p> </li> </ul> <p>For more information about server-side
                  encryption with customer-provided encryption keys (SSE-C), see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerSideEncryptionCustomerKeys.html">
                  Protecting data using server-side encryption with
                  customer-provided encryption keys (SSE-C)</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </li> </ul> </li> <li> <p> <b>Directory
                  buckets</b> -For directory buckets, only server-side
                  encryption with Amazon S3 managed keys (SSE-S3)
                  (<code>AES256</code>) is supported.</p> </li> </ul> </dd>
                  <dt>HTTP Host header syntax</dt> <dd> <p> <b>Directory buckets
                  </b> - The HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>CreateMultipartUpload</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListMultipartUploads.html">ListMultipartUploads</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Multipart
                  - Uploads
                  - Bucket
                  - Keys
                  - '?uploads'
            /{Bucket}?session:
              GET:
                summary: CreateSession
                description: >-
                  <p>Creates a session that establishes temporary security
                  credentials to support fast authentication and authorization
                  for the Zonal endpoint APIs on directory buckets. For more
                  information about Zonal endpoint APIs that include the
                  Availability Zone in the request endpoint, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-APIs.html">S3
                  Express One Zone APIs</a> in the <i>Amazon S3 User Guide</i>.
                  </p> <p>To make Zonal endpoint API requests on a directory
                  bucket, use the <code>CreateSession</code> API operation.
                  Specifically, you grant <code>s3express:CreateSession</code>
                  permission to a bucket in a bucket policy or an IAM
                  identity-based policy. Then, you use IAM credentials to make
                  the <code>CreateSession</code> API request on the bucket,
                  which returns temporary security credentials that include the
                  access key ID, secret access key, session token, and
                  expiration. These credentials have associated permissions to
                  access the Zonal endpoint APIs. After the session is created,
                  you don’t need to use other policies to grant permissions to
                  each Zonal endpoint API individually. Instead, in your Zonal
                  endpoint API requests, you sign your requests by applying the
                  temporary security credentials of the session to the request
                  headers and following the SigV4 protocol for authentication.
                  You also apply the session token to the
                  <code>x-amz-s3session-token</code> request header for
                  authorization. Temporary security credentials are scoped to
                  the bucket and expire after 5 minutes. After the expiration
                  time, any calls that you make with those credentials will
                  fail. You must use IAM credentials again to make a
                  <code>CreateSession</code> API request that generates a new
                  set of temporary credentials for use. Temporary credentials
                  cannot be extended or refreshed beyond the original specified
                  interval.</p> <p>If you use Amazon Web Services SDKs, SDKs
                  handle the session token refreshes automatically to avoid
                  service interruptions when a session expires. We recommend
                  that you use the Amazon Web Services SDKs to initiate and
                  manage requests to the CreateSession API. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-optimizing-performance-guidelines-design-patterns.html#s3-express-optimizing-performance-session-authentication">Performance
                  guidelines and design patterns</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <ul> <li> <p>You must make requests for
                  this API operation to the Zonal endpoint. These endpoints
                  support virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.
                  Path-style requests are not supported. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b> <code>CopyObject</code> API
                  operation</b> - Unlike other Zonal endpoint APIs, the
                  <code>CopyObject</code> API operation doesn't use the
                  temporary security credentials returned from the
                  <code>CreateSession</code> API operation for authentication
                  and authorization. For information about authentication and
                  authorization of the <code>CopyObject</code> API operation on
                  directory buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>.</p>
                  </li> <li> <p> <b> <code>HeadBucket</code> API operation</b> -
                  Unlike other Zonal endpoint APIs, the <code>HeadBucket</code>
                  API operation doesn't use the temporary security credentials
                  returned from the <code>CreateSession</code> API operation for
                  authentication and authorization. For information about
                  authentication and authorization of the
                  <code>HeadBucket</code> API operation on directory buckets,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadBucket.html">HeadBucket</a>.</p>
                  </li> </ul> </note> <dl> <dt>Permissions</dt> <dd> <p>To
                  obtain temporary security credentials, you must create a
                  bucket policy or an IAM identity-based policy that grants
                  <code>s3express:CreateSession</code> permission to the bucket.
                  In a policy, you can have the
                  <code>s3express:SessionMode</code> condition key to control
                  who can create a <code>ReadWrite</code> or
                  <code>ReadOnly</code> session. For more information about
                  <code>ReadWrite</code> or <code>ReadOnly</code> sessions, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html#API_CreateSession_RequestParameters">
                  <code>x-amz-create-session-mode</code> </a>. For example
                  policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-identity-policies.html">Amazon
                  Web Services Identity and Access Management (IAM)
                  identity-based policies for S3 Express One Zone</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>To grant cross-account
                  access to Zonal endpoint APIs, the bucket policy should also
                  grant both accounts the <code>s3express:CreateSession</code>
                  permission.</p> </dd> <dt>HTTP Host header syntax</dt> <dd>
                  <p> <b>Directory buckets </b> - The HTTP Host header syntax is
                  <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl>
                tags:
                  - Create
                  - Sessions
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
            /{Bucket}?analytics:
              PUT:
                summary: PutBucketAnalyticsConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets an analytics configuration for
                  the bucket (specified by the analytics configuration ID). You
                  can have up to 1,000 analytics configurations per bucket.</p>
                  <p>You can choose to have storage class analysis export
                  analysis reports sent to a comma-separated values (CSV) flat
                  file. See the <code>DataExport</code> request element. Reports
                  are updated daily and are based on the object filters that you
                  configure. When selecting data export, you specify a
                  destination bucket and an optional destination prefix where
                  the file is written. You can export the data to a destination
                  bucket in a different account. However, the destination bucket
                  must be in the same Region as the bucket that you are making
                  the PUT analytics configuration to. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/analytics-storage-class.html">Amazon
                  S3 Analytics – Storage Class Analysis</a>. </p> <important>
                  <p>You must create a bucket policy on the destination bucket
                  where the exported file is written to grant permissions to
                  Amazon S3 to write objects to the bucket. For an example
                  policy, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html#example-bucket-policies-use-case-9">Granting
                  Permissions for Amazon S3 Inventory and Storage Class
                  Analysis</a>.</p> </important> <p>To use this operation, you
                  must have permissions to perform the
                  <code>s3:PutAnalyticsConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  <code>PutBucketAnalyticsConfiguration</code> has the following
                  special errors:</p> <ul> <li> <ul> <li> <p> <i>HTTP Error:
                  HTTP 400 Bad Request</i> </p> </li> <li> <p> <i>Code:
                  InvalidArgument</i> </p> </li> <li> <p> <i>Cause: Invalid
                  argument.</i> </p> </li> </ul> </li> <li> <ul> <li> <p>
                  <i>HTTP Error: HTTP 400 Bad Request</i> </p> </li> <li> <p>
                  <i>Code: TooManyConfigurations</i> </p> </li> <li> <p>
                  <i>Cause: You are attempting to create a new configuration but
                  have already reached the 1,000-configuration limit.</i> </p>
                  </li> </ul> </li> <li> <ul> <li> <p> <i>HTTP Error: HTTP 403
                  Forbidden</i> </p> </li> <li> <p> <i>Code: AccessDenied</i>
                  </p> </li> <li> <p> <i>Cause: You are not the owner of the
                  specified bucket, or you do not have the
                  s3:PutAnalyticsConfiguration bucket permission to set the
                  configuration on the bucket.</i> </p> </li> </ul> </li> </ul>
                  <p>The following operations are related to
                  <code>PutBucketAnalyticsConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAnalyticsConfiguration.html">GetBucketAnalyticsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketAnalyticsConfiguration.html">DeleteBucketAnalyticsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketAnalyticsConfigurations.html">ListBucketAnalyticsConfigurations</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Analytics
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
            /{Bucket}?cors:
              PUT:
                summary: PutBucketCors
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the <code>cors</code>
                  configuration for your bucket. If the configuration exists,
                  Amazon S3 replaces it.</p> <p>To use this operation, you must
                  be allowed to perform the <code>s3:PutBucketCORS</code>
                  action. By default, the bucket owner has this permission and
                  can grant it to others.</p> <p>You set this configuration on a
                  bucket so that the bucket can service cross-origin requests.
                  For example, you might want to enable a request whose origin
                  is <code>http://www.example.com</code> to access your Amazon
                  S3 bucket at <code>my.example.bucket.com</code> by using the
                  browser's <code>XMLHttpRequest</code> capability.</p> <p>To
                  enable cross-origin resource sharing (CORS) on a bucket, you
                  add the <code>cors</code> subresource to the bucket. The
                  <code>cors</code> subresource is an XML document in which you
                  configure rules that identify origins and the HTTP methods
                  that can be executed on your bucket. The document is limited
                  to 64 KB in size. </p> <p>When Amazon S3 receives a
                  cross-origin request (or a pre-flight OPTIONS request) against
                  a bucket, it evaluates the <code>cors</code> configuration on
                  the bucket and uses the first <code>CORSRule</code> rule that
                  matches the incoming browser request to enable a cross-origin
                  request. For a rule to match, the following conditions must be
                  met:</p> <ul> <li> <p>The request's <code>Origin</code> header
                  must match <code>AllowedOrigin</code> elements.</p> </li> <li>
                  <p>The request method (for example, GET, PUT, HEAD, and so on)
                  or the <code>Access-Control-Request-Method</code> header in
                  case of a pre-flight <code>OPTIONS</code> request must be one
                  of the <code>AllowedMethod</code> elements. </p> </li> <li>
                  <p>Every header specified in the
                  <code>Access-Control-Request-Headers</code> request header of
                  a pre-flight request must match an <code>AllowedHeader</code>
                  element. </p> </li> </ul> <p> For more information about CORS,
                  go to <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html">Enabling
                  Cross-Origin Resource Sharing</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following operations are related to
                  <code>PutBucketCors</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketCors.html">GetBucketCors</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketCors.html">DeleteBucketCors</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTOPTIONSobject.html">RESTOPTIONSobject</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - CORS
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
            /{Bucket}?encryption:
              PUT:
                summary: PutBucketEncryption
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>This action uses the
                  <code>encryption</code> subresource to configure default
                  encryption and Amazon S3 Bucket Keys for an existing
                  bucket.</p> <p>By default, all buckets have a default
                  encryption configuration that uses server-side encryption with
                  Amazon S3 managed keys (SSE-S3). You can optionally configure
                  default encryption for a bucket by using server-side
                  encryption with Key Management Service (KMS) keys (SSE-KMS) or
                  dual-layer server-side encryption with Amazon Web Services KMS
                  keys (DSSE-KMS). If you specify default encryption by using
                  SSE-KMS, you can also configure <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-key.html">Amazon
                  S3 Bucket Keys</a>. If you use PutBucketEncryption to set your
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html">default
                  bucket encryption</a> to SSE-KMS, you should verify that your
                  KMS key ID is correct. Amazon S3 does not validate the KMS key
                  ID provided in PutBucketEncryption requests.</p> <important>
                  <p>This action requires Amazon Web Services Signature Version
                  4. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">
                  Authenticating Requests (Amazon Web Services Signature Version
                  4)</a>. </p> </important> <p>To use this operation, you must
                  have permission to perform the
                  <code>s3:PutEncryptionConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>The following operations
                  are related to <code>PutBucketEncryption</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketEncryption.html">GetBucketEncryption</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketEncryption.html">DeleteBucketEncryption</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Encryption
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
            /{Bucket}?intelligent-tiering:
              PUT:
                summary: PutBucketIntelligentTieringConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Puts a S3 Intelligent-Tiering
                  configuration to the specified bucket. You can have up to
                  1,000 S3 Intelligent-Tiering configurations per bucket.</p>
                  <p>The S3 Intelligent-Tiering storage class is designed to
                  optimize storage costs by automatically moving data to the
                  most cost-effective storage access tier, without performance
                  impact or operational overhead. S3 Intelligent-Tiering
                  delivers automatic cost savings in three low latency and high
                  throughput access tiers. To get the lowest storage cost on
                  data that can be accessed in minutes to hours, you can choose
                  to activate additional archiving capabilities.</p> <p>The S3
                  Intelligent-Tiering storage class is the ideal storage class
                  for data with unknown, changing, or unpredictable access
                  patterns, independent of object size or retention period. If
                  the size of an object is less than 128 KB, it is not monitored
                  and not eligible for auto-tiering. Smaller objects can be
                  stored, but they are always charged at the Frequent Access
                  tier rates in the S3 Intelligent-Tiering storage class.</p>
                  <p>For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html#sc-dynamic-data-access">Storage
                  class for automatically optimizing frequently and infrequently
                  accessed objects</a>.</p> <p>Operations related to
                  <code>PutBucketIntelligentTieringConfiguration</code> include:
                  </p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketIntelligentTieringConfiguration.html">DeleteBucketIntelligentTieringConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketIntelligentTieringConfiguration.html">GetBucketIntelligentTieringConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketIntelligentTieringConfigurations.html">ListBucketIntelligentTieringConfigurations</a>
                  </p> </li> </ul> <note> <p>You only need S3
                  Intelligent-Tiering enabled on a bucket if you want to
                  automatically move objects stored in the S3
                  Intelligent-Tiering storage class to the Archive Access or
                  Deep Archive Access tier.</p> </note> <p>
                  <code>PutBucketIntelligentTieringConfiguration</code> has the
                  following special errors:</p> <dl> <dt>HTTP 400 Bad Request
                  Error</dt> <dd> <p> <i>Code:</i> InvalidArgument</p> <p>
                  <i>Cause:</i> Invalid Argument</p> </dd> <dt>HTTP 400 Bad
                  Request Error</dt> <dd> <p> <i>Code:</i>
                  TooManyConfigurations</p> <p> <i>Cause:</i> You are attempting
                  to create a new configuration but have already reached the
                  1,000-configuration limit. </p> </dd> <dt>HTTP 403 Forbidden
                  Error</dt> <dd> <p> <i>Cause:</i> You are not the owner of the
                  specified bucket, or you do not have the
                  <code>s3:PutIntelligentTieringConfiguration</code> bucket
                  permission to set the configuration on the bucket. </p> </dd>
                  </dl>
                tags:
                  - Put
                  - Bucket
                  - Intelligent
                  - Tiering
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
            /{Bucket}?inventory:
              PUT:
                summary: PutBucketInventoryConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>This implementation of the
                  <code>PUT</code> action adds an inventory configuration
                  (identified by the inventory ID) to the bucket. You can have
                  up to 1,000 inventory configurations per bucket. </p>
                  <p>Amazon S3 inventory generates inventories of the objects in
                  the bucket on a daily or weekly basis, and the results are
                  published to a flat file. The bucket that is inventoried is
                  called the <i>source</i> bucket, and the bucket where the
                  inventory flat file is stored is called the <i>destination</i>
                  bucket. The <i>destination</i> bucket must be in the same
                  Amazon Web Services Region as the <i>source</i> bucket. </p>
                  <p>When you configure an inventory for a <i>source</i> bucket,
                  you specify the <i>destination</i> bucket where you want the
                  inventory to be stored, and whether to generate the inventory
                  daily or weekly. You can also configure what object metadata
                  to include and whether to inventory all object versions or
                  only current versions. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-inventory.html">Amazon
                  S3 Inventory</a> in the Amazon S3 User Guide.</p> <important>
                  <p>You must create a bucket policy on the <i>destination</i>
                  bucket to grant permissions to Amazon S3 to write objects to
                  the bucket in the defined location. For an example policy, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html#example-bucket-policies-use-case-9">
                  Granting Permissions for Amazon S3 Inventory and Storage Class
                  Analysis</a>.</p> </important> <dl> <dt>Permissions</dt> <dd>
                  <p>To use this operation, you must have permission to perform
                  the <code>s3:PutInventoryConfiguration</code> action. The
                  bucket owner has this permission by default and can grant this
                  permission to others. </p> <p>The
                  <code>s3:PutInventoryConfiguration</code> permission allows a
                  user to create an <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-inventory.html">S3
                  Inventory</a> report that includes all object metadata fields
                  available and to specify the destination bucket to store the
                  inventory. A user with read access to objects in the
                  destination bucket can also access all object metadata fields
                  that are available in the inventory report. </p> <p>To
                  restrict access to an inventory report, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html#example-bucket-policies-use-case-10">Restricting
                  access to an Amazon S3 Inventory report</a> in the <i>Amazon
                  S3 User Guide</i>. For more information about the metadata
                  fields available in S3 Inventory, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-inventory.html#storage-inventory-contents">Amazon
                  S3 Inventory lists</a> in the <i>Amazon S3 User Guide</i>. For
                  more information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  related to bucket subresource operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Identity
                  and access management in Amazon S3</a> in the <i>Amazon S3
                  User Guide</i>.</p> </dd> </dl> <p>
                  <code>PutBucketInventoryConfiguration</code> has the following
                  special errors:</p> <dl> <dt>HTTP 400 Bad Request Error</dt>
                  <dd> <p> <i>Code:</i> InvalidArgument</p> <p> <i>Cause:</i>
                  Invalid Argument</p> </dd> <dt>HTTP 400 Bad Request Error</dt>
                  <dd> <p> <i>Code:</i> TooManyConfigurations</p> <p>
                  <i>Cause:</i> You are attempting to create a new configuration
                  but have already reached the 1,000-configuration limit. </p>
                  </dd> <dt>HTTP 403 Forbidden Error</dt> <dd> <p> <i>Cause:</i>
                  You are not the owner of the specified bucket, or you do not
                  have the <code>s3:PutInventoryConfiguration</code> bucket
                  permission to set the configuration on the bucket. </p> </dd>
                  </dl> <p>The following operations are related to
                  <code>PutBucketInventoryConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketInventoryConfiguration.html">GetBucketInventoryConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketInventoryConfiguration.html">DeleteBucketInventoryConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketInventoryConfigurations.html">ListBucketInventoryConfigurations</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Inventory
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
            /{Bucket}?lifecycle:
              PUT:
                summary: PutBucketLifecycleConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates a new lifecycle configuration
                  for the bucket or replaces an existing lifecycle
                  configuration. Keep in mind that this will overwrite an
                  existing lifecycle configuration, so if you want to retain any
                  configuration details, they must be included in the new
                  lifecycle configuration. For information about lifecycle
                  configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html">Managing
                  your storage lifecycle</a>.</p> <note> <p>Bucket lifecycle
                  configuration now supports specifying a lifecycle rule using
                  an object key name prefix, one or more object tags, or a
                  combination of both. Accordingly, this section describes the
                  latest API. The previous version of the API supported
                  filtering based only on an object key name prefix, which is
                  supported for backward compatibility. For the related API
                  description, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycle.html">PutBucketLifecycle</a>.</p>
                  </note> <dl> <dt>Rules</dt> <dd> <p>You specify the lifecycle
                  configuration in your request body. The lifecycle
                  configuration is specified as XML consisting of one or more
                  rules. An Amazon S3 Lifecycle configuration can have up to
                  1,000 rules. This limit is not adjustable. Each rule consists
                  of the following:</p> <ul> <li> <p>A filter identifying a
                  subset of objects to which the rule applies. The filter can be
                  based on a key name prefix, object tags, or a combination of
                  both.</p> </li> <li> <p>A status indicating whether the rule
                  is in effect.</p> </li> <li> <p>One or more lifecycle
                  transition and expiration actions that you want Amazon S3 to
                  perform on the objects identified by the filter. If the state
                  of your bucket is versioning-enabled or versioning-suspended,
                  you can have many versions of the same object (one current
                  version and zero or more noncurrent versions). Amazon S3
                  provides predefined actions that you can specify for current
                  and noncurrent object versions.</p> </li> </ul> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html">Object
                  Lifecycle Management</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/intro-lifecycle-rules.html">Lifecycle
                  Configuration Elements</a>.</p> </dd> <dt>Permissions</dt>
                  <dd> <p>By default, all Amazon S3 resources are private,
                  including buckets, objects, and related subresources (for
                  example, lifecycle configuration and website configuration).
                  Only the resource owner (that is, the Amazon Web Services
                  account that created it) can access the resource. The resource
                  owner can optionally grant access permissions to others by
                  writing an access policy. For this operation, a user must get
                  the <code>s3:PutLifecycleConfiguration</code> permission.</p>
                  <p>You can also explicitly deny permissions. An explicit deny
                  also supersedes any other permissions. If you want to block
                  users or accounts from removing or deleting objects from your
                  bucket, you must deny them permissions for the following
                  actions:</p> <ul> <li> <p> <code>s3:DeleteObject</code> </p>
                  </li> <li> <p> <code>s3:DeleteObjectVersion</code> </p> </li>
                  <li> <p> <code>s3:PutLifecycleConfiguration</code> </p> </li>
                  </ul> <p>For more information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> </dd>
                  </dl> <p>The following operations are related to
                  <code>PutBucketLifecycleConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-configuration-examples.html">Examples
                  of Lifecycle Configuration</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketLifecycle.html">DeleteBucketLifecycle</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Lifecycle
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
            /{Bucket}?metrics:
              PUT:
                summary: PutBucketMetricsConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets a metrics configuration
                  (specified by the metrics configuration ID) for the bucket.
                  You can have up to 1,000 metrics configurations per bucket. If
                  you're updating an existing metrics configuration, note that
                  this is a full replacement of the existing metrics
                  configuration. If you don't include the elements you want to
                  keep, they are erased.</p> <p>To use this operation, you must
                  have permissions to perform the
                  <code>s3:PutMetricsConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>For
                  information about CloudWatch request metrics for Amazon S3,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/cloudwatch-monitoring.html">Monitoring
                  Metrics with Amazon CloudWatch</a>.</p> <p>The following
                  operations are related to
                  <code>PutBucketMetricsConfiguration</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketMetricsConfiguration.html">DeleteBucketMetricsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketMetricsConfiguration.html">GetBucketMetricsConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBucketMetricsConfigurations.html">ListBucketMetricsConfigurations</a>
                  </p> </li> </ul> <p>
                  <code>PutBucketMetricsConfiguration</code> has the following
                  special error:</p> <ul> <li> <p>Error code:
                  <code>TooManyConfigurations</code> </p> <ul> <li>
                  <p>Description: You are attempting to create a new
                  configuration but have already reached the 1,000-configuration
                  limit.</p> </li> <li> <p>HTTP Status Code: HTTP 400 Bad
                  Request</p> </li> </ul> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Metrics
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
            /{Bucket}?ownershipControls:
              PUT:
                summary: PutBucketOwnershipControls
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies
                  <code>OwnershipControls</code> for an Amazon S3 bucket. To use
                  this operation, you must have the
                  <code>s3:PutBucketOwnershipControls</code> permission. For
                  more information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/user-guide/using-with-s3-actions.html">Specifying
                  permissions in a policy</a>. </p> <p>For information about
                  Amazon S3 Object Ownership, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/user-guide/about-object-ownership.html">Using
                  object ownership</a>. </p> <p>The following operations are
                  related to <code>PutBucketOwnershipControls</code>:</p> <ul>
                  <li> <p> <a>GetBucketOwnershipControls</a> </p> </li> <li> <p>
                  <a>DeleteBucketOwnershipControls</a> </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Ownership
                  - Controls
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
            /{Bucket}?policy:
              PUT:
                summary: PutBucketPolicy
                description: >-
                  <p>Applies an Amazon S3 bucket policy to an Amazon S3
                  bucket.</p> <note> <p> <b>Directory buckets </b> - For
                  directory buckets, you must make requests for this API
                  operation to the Regional endpoint. These endpoints support
                  path-style requests in the format
                  <code>https://s3express-control.<i>region_code</i>.amazonaws.com/<i>bucket-name</i>
                  </code>. Virtual-hosted-style requests aren't supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <p>If
                  you are using an identity other than the root user of the
                  Amazon Web Services account that owns the bucket, the calling
                  identity must both have the <code>PutBucketPolicy</code>
                  permissions on the specified bucket and belong to the bucket
                  owner's account in order to use this operation.</p> <p>If you
                  don't have <code>PutBucketPolicy</code> permissions, Amazon S3
                  returns a <code>403 Access Denied</code> error. If you have
                  the correct permissions, but you're not using an identity that
                  belongs to the bucket owner's account, Amazon S3 returns a
                  <code>405 Method Not Allowed</code> error.</p> <important>
                  <p>To ensure that bucket owners don't inadvertently lock
                  themselves out of their own buckets, the root principal in a
                  bucket owner's Amazon Web Services account can perform the
                  <code>GetBucketPolicy</code>, <code>PutBucketPolicy</code>,
                  and <code>DeleteBucketPolicy</code> API actions, even if their
                  bucket policy explicitly denies the root principal's access.
                  Bucket owner root principals can only be blocked from
                  performing these API actions by VPC endpoint policies and
                  Amazon Web Services Organizations policies.</p> </important>
                  <ul> <li> <p> <b>General purpose bucket permissions</b> - The
                  <code>s3:PutBucketPolicy</code> permission is required in a
                  policy. For more information about general purpose buckets
                  bucket policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html">Using
                  Bucket Policies and User Policies</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - To grant access to this API operation, you
                  must have the <code>s3express:PutBucketPolicy</code>
                  permission in an IAM identity-based policy instead of a bucket
                  policy. Cross-account access to this API operation isn't
                  supported. This operation can only be performed by the Amazon
                  Web Services account that owns the resource. For more
                  information about directory bucket policies and permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam.html">Amazon
                  Web Services Identity and Access Management (IAM) for S3
                  Express One Zone</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </li> </ul> </dd> <dt>Example bucket policies</dt> <dd> <p>
                  <b>General purpose buckets example bucket policies</b> - See
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html">Bucket
                  policy examples</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p> <b>Directory bucket example bucket policies</b> - See <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam-example-bucket-policies.html">Example
                  bucket policies for S3 Express One Zone</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </dd> <dt>HTTP Host header syntax</dt>
                  <dd> <p> <b>Directory buckets </b> - The HTTP Host header
                  syntax is
                  <code>s3express-control.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>PutBucketPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Policies
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
            /{Bucket}?replication:
              PUT:
                summary: PutBucketReplication
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p> Creates a replication configuration
                  or replaces an existing one. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html">Replication</a>
                  in the <i>Amazon S3 User Guide</i>. </p> <p>Specify the
                  replication configuration in the request body. In the
                  replication configuration, you provide the name of the
                  destination bucket or buckets where you want Amazon S3 to
                  replicate objects, the IAM role that Amazon S3 can assume to
                  replicate objects on your behalf, and other relevant
                  information. You can invoke this request for a specific Amazon
                  Web Services Region by using the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-requestedregion">
                  <code>aws:RequestedRegion</code> </a> condition key.</p> <p>A
                  replication configuration must include at least one rule, and
                  can contain a maximum of 1,000. Each rule identifies a subset
                  of objects to replicate by filtering the objects in the source
                  bucket. To choose additional subsets of objects to replicate,
                  add a rule for each subset.</p> <p>To specify a subset of the
                  objects in the source bucket to apply a replication rule to,
                  add the Filter element as a child of the Rule element. You can
                  filter objects based on an object key prefix, one or more
                  object tags, or both. When you add the Filter element in the
                  configuration, you must also add the following elements:
                  <code>DeleteMarkerReplication</code>, <code>Status</code>, and
                  <code>Priority</code>.</p> <note> <p>If you are using an
                  earlier version of the replication configuration, Amazon S3
                  handles replication of delete markers differently. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations">Backward
                  Compatibility</a>.</p> </note> <p>For information about
                  enabling versioning on a bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html">Using
                  Versioning</a>.</p> <dl> <dt>Handling Replication of Encrypted
                  Objects</dt> <dd> <p>By default, Amazon S3 doesn't replicate
                  objects that are stored at rest using server-side encryption
                  with KMS keys. To replicate Amazon Web Services KMS-encrypted
                  objects, add the following:
                  <code>SourceSelectionCriteria</code>,
                  <code>SseKmsEncryptedObjects</code>, <code>Status</code>,
                  <code>EncryptionConfiguration</code>, and
                  <code>ReplicaKmsKeyID</code>. For information about
                  replication configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-config-for-kms-objects.html">Replicating
                  Objects Created with SSE Using KMS keys</a>.</p> <p>For
                  information on <code>PutBucketReplication</code> errors, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#ReplicationErrorCodeList">List
                  of replication-related error codes</a> </p> </dd>
                  <dt>Permissions</dt> <dd> <p>To create a
                  <code>PutBucketReplication</code> request, you must have
                  <code>s3:PutReplicationConfiguration</code> permissions for
                  the bucket. </p> <p>By default, a resource owner, in this case
                  the Amazon Web Services account that created the bucket, can
                  perform this operation. The resource owner can also grant
                  others permissions to perform the operation. For more
                  information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <note>
                  <p>To perform this operation, the user or role performing the
                  action must have the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">iam:PassRole</a>
                  permission.</p> </note> </dd> </dl> <p>The following
                  operations are related to
                  <code>PutBucketReplication</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketReplication.html">GetBucketReplication</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketReplication.html">DeleteBucketReplication</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Replication
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
            /{Bucket}?tagging:
              PUT:
                summary: PutBucketTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the tags for a bucket.</p> <p>Use
                  tags to organize your Amazon Web Services bill to reflect your
                  own cost structure. To do this, sign up to get your Amazon Web
                  Services account bill with tag key values included. Then, to
                  see the cost of combined resources, organize your billing
                  information according to resources with the same tag key
                  values. For example, you can tag several resources with a
                  specific application name, and then organize your billing
                  information to see the total cost of that application across
                  several services. For more information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Cost
                  Allocation and Tagging</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">Using
                  Cost Allocation in Amazon S3 Bucket Tags</a>.</p> <note> <p>
                  When this operation sets the tags for a bucket, it will
                  overwrite any current tags the bucket already has. You cannot
                  use this operation to add tags to an existing list of
                  tags.</p> </note> <p>To use this operation, you must have
                  permissions to perform the <code>s3:PutBucketTagging</code>
                  action. The bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  <code>PutBucketTagging</code> has the following special
                  errors. For more Amazon S3 errors see, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html">Error
                  Responses</a>.</p> <ul> <li> <p> <code>InvalidTag</code> - The
                  tag provided was not a valid tag. This error can occur if the
                  tag did not pass input validation. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">Using
                  Cost Allocation in Amazon S3 Bucket Tags</a>.</p> </li> <li>
                  <p> <code>MalformedXML</code> - The XML provided does not
                  match the schema.</p> </li> <li> <p>
                  <code>OperationAborted</code> - A conflicting conditional
                  action is currently in progress against this resource. Please
                  try again.</p> </li> <li> <p> <code>InternalError</code> - The
                  service was unable to apply the provided tag to the
                  bucket.</p> </li> </ul> <p>The following operations are
                  related to <code>PutBucketTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketTagging.html">GetBucketTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketTagging.html">DeleteBucketTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Tagging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
            /{Bucket}?website:
              PUT:
                summary: PutBucketWebsite
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the configuration of the website
                  that is specified in the <code>website</code> subresource. To
                  configure a bucket as a website, you can add this subresource
                  on the bucket with website configuration information such as
                  the file name of the index document and any redirect rules.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html">Hosting
                  Websites on Amazon S3</a>.</p> <p>This PUT action requires the
                  <code>S3:PutBucketWebsite</code> permission. By default, only
                  the bucket owner can configure the website attached to a
                  bucket; however, bucket owners can allow other users to set
                  the website configuration by writing a bucket policy that
                  grants them the <code>S3:PutBucketWebsite</code>
                  permission.</p> <p>To redirect all website requests sent to
                  the bucket's website endpoint, you add a website configuration
                  with the following elements. Because all requests are sent to
                  another website, you don't need to provide index document name
                  for the bucket.</p> <ul> <li> <p>
                  <code>WebsiteConfiguration</code> </p> </li> <li> <p>
                  <code>RedirectAllRequestsTo</code> </p> </li> <li> <p>
                  <code>HostName</code> </p> </li> <li> <p>
                  <code>Protocol</code> </p> </li> </ul> <p>If you want granular
                  control over redirects, you can use the following elements to
                  add routing rules that describe conditions for redirecting
                  requests and information about the redirect destination. In
                  this case, the website configuration must provide an index
                  document for the bucket, because some requests might not be
                  redirected. </p> <ul> <li> <p>
                  <code>WebsiteConfiguration</code> </p> </li> <li> <p>
                  <code>IndexDocument</code> </p> </li> <li> <p>
                  <code>Suffix</code> </p> </li> <li> <p>
                  <code>ErrorDocument</code> </p> </li> <li> <p>
                  <code>Key</code> </p> </li> <li> <p> <code>RoutingRules</code>
                  </p> </li> <li> <p> <code>RoutingRule</code> </p> </li> <li>
                  <p> <code>Condition</code> </p> </li> <li> <p>
                  <code>HttpErrorCodeReturnedEquals</code> </p> </li> <li> <p>
                  <code>KeyPrefixEquals</code> </p> </li> <li> <p>
                  <code>Redirect</code> </p> </li> <li> <p>
                  <code>Protocol</code> </p> </li> <li> <p>
                  <code>HostName</code> </p> </li> <li> <p>
                  <code>ReplaceKeyPrefixWith</code> </p> </li> <li> <p>
                  <code>ReplaceKeyWith</code> </p> </li> <li> <p>
                  <code>HttpRedirectCode</code> </p> </li> </ul> <p>Amazon S3
                  has a limitation of 50 routing rules per website
                  configuration. If you require more than 50 routing rules, you
                  can use object redirect. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html">Configuring
                  an Object Redirect</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p>The maximum request length is limited to 128 KB.</p>
                tags:
                  - Put
                  - Bucket
                  - Websites
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
            /{Bucket}/{Key+}?tagging:
              PUT:
                summary: PutObjectTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the supplied tag-set to an object
                  that already exists in a bucket. A tag is a key-value pair.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-tagging.html">Object
                  Tagging</a>.</p> <p>You can associate tags with an object by
                  sending a PUT request against the tagging subresource that is
                  associated with the object. You can retrieve tags by sending a
                  GET request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>.</p>
                  <p>For tagging-related restrictions related to characters and
                  encodings, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">Tag
                  Restrictions</a>. Note that Amazon S3 limits the maximum
                  number of tags to 10 tags per object.</p> <p>To use this
                  operation, you must have permission to perform the
                  <code>s3:PutObjectTagging</code> action. By default, the
                  bucket owner has this permission and can grant this permission
                  to others.</p> <p>To put tags of any other version, use the
                  <code>versionId</code> query parameter. You also need
                  permission for the <code>s3:PutObjectVersionTagging</code>
                  action.</p> <p> <code>PutObjectTagging</code> has the
                  following special errors. For more Amazon S3 errors see, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html">Error
                  Responses</a>.</p> <ul> <li> <p> <code>InvalidTag</code> - The
                  tag provided was not a valid tag. This error can occur if the
                  tag did not pass input validation. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-tagging.html">Object
                  Tagging</a>.</p> </li> <li> <p> <code>MalformedXML</code> -
                  The XML provided does not match the schema.</p> </li> <li> <p>
                  <code>OperationAborted</code> - A conflicting conditional
                  action is currently in progress against this resource. Please
                  try again.</p> </li> <li> <p> <code>InternalError</code> - The
                  service was unable to apply the provided tag to the
                  object.</p> </li> </ul> <p>The following operations are
                  related to <code>PutObjectTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObjectTagging.html">DeleteObjectTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Objects
                  - Tagging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
            /{Bucket}?delete:
              POST:
                summary: DeleteObjects
                description: >-
                  <p>This operation enables you to delete multiple objects from
                  a bucket using a single HTTP request. If you know the object
                  keys that you want to delete, then this operation provides a
                  suitable alternative to sending individual delete requests,
                  reducing per-request overhead.</p> <p>The request can contain
                  a list of up to 1000 keys that you want to delete. In the XML,
                  you provide the object key names, and optionally, version IDs
                  if you want to delete a specific version of the object from a
                  versioning-enabled bucket. For each key, Amazon S3 performs a
                  delete operation and returns the result of that delete,
                  success or failure, in the response. Note that if the object
                  specified in the request is not found, Amazon S3 returns the
                  result as deleted.</p> <note> <ul> <li> <p> <b>Directory
                  buckets</b> - S3 Versioning isn't enabled and supported for
                  directory buckets.</p> </li> <li> <p> <b>Directory buckets</b>
                  - For directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> </ul> </note> <p>The operation supports
                  two modes for the response: verbose and quiet. By default, the
                  operation uses verbose mode in which the response includes the
                  result of deletion of each key in your request. In quiet mode
                  the response includes only keys where the delete operation
                  encountered an error. For a successful deletion in a quiet
                  mode, the operation does not return any information about the
                  delete in the response body.</p> <p>When performing this
                  action on an MFA Delete enabled bucket, that attempts to
                  delete any versioned objects, you must include an MFA token.
                  If you do not provide one, the entire request will fail, even
                  if there are non-versioned objects you are trying to delete.
                  If you provide an invalid token, whether there are versioned
                  keys in the request or not, the entire Multi-Object Delete
                  request will fail. For information about MFA Delete, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html#MultiFactorAuthenticationDelete">MFA
                  Delete</a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>
                  <b>Directory buckets</b> - MFA delete is not supported by
                  directory buckets.</p> </note> <dl> <dt>Permissions</dt> <dd>
                  <ul> <li> <p> <b>General purpose bucket permissions</b> - The
                  following permissions are required in your policies when your
                  <code>DeleteObjects</code> request includes specific
                  headers.</p> <ul> <li> <p> <b> <code>s3:DeleteObject</code>
                  </b> - To delete an object from a bucket, you must always
                  specify the <code>s3:DeleteObject</code> permission.</p> </li>
                  <li> <p> <b> <code>s3:DeleteObjectVersion</code> </b> - To
                  delete a specific version of an object from a versiong-enabled
                  bucket, you must specify the
                  <code>s3:DeleteObjectVersion</code> permission.</p> </li>
                  </ul> </li> <li> <p> <b>Directory bucket permissions</b> - To
                  grant access to this API operation on a directory bucket, we
                  recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Content-MD5 request header</dt> <dd> <ul> <li> <p>
                  <b>General purpose bucket</b> - The Content-MD5 request header
                  is required for all Multi-Object Delete requests. Amazon S3
                  uses the header value to ensure that your request body has not
                  been altered in transit.</p> </li> <li> <p> <b>Directory
                  bucket</b> - The Content-MD5 request header or a additional
                  checksum request header (including
                  <code>x-amz-checksum-crc32</code>,
                  <code>x-amz-checksum-crc32c</code>,
                  <code>x-amz-checksum-sha1</code>, or
                  <code>x-amz-checksum-sha256</code>) is required for all
                  Multi-Object Delete requests.</p> </li> </ul> </dd> <dt>HTTP
                  Host header syntax</dt> <dd> <p> <b>Directory buckets </b> -
                  The HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>DeleteObjects</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> </ul>
                tags:
                  - Delete
                  - Objects
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
            /{Bucket}?publicAccessBlock:
              PUT:
                summary: PutPublicAccessBlock
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies the
                  <code>PublicAccessBlock</code> configuration for an Amazon S3
                  bucket. To use this operation, you must have the
                  <code>s3:PutBucketPublicAccessBlock</code> permission. For
                  more information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a>.</p> <important> <p>When Amazon S3
                  evaluates the <code>PublicAccessBlock</code> configuration for
                  a bucket or an object, it checks the
                  <code>PublicAccessBlock</code> configuration for both the
                  bucket (or the bucket that contains the object) and the bucket
                  owner's account. If the <code>PublicAccessBlock</code>
                  configurations are different between the bucket and the
                  account, Amazon S3 uses the most restrictive combination of
                  the bucket-level and account-level settings.</p> </important>
                  <p>For more information about when Amazon S3 considers a
                  bucket or an object public, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status">The
                  Meaning of "Public"</a>.</p> <p>The following operations are
                  related to <code>PutPublicAccessBlock</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketPolicyStatus.html">GetBucketPolicyStatus</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">Using
                  Amazon S3 Block Public Access</a> </p> </li> </ul>
                tags:
                  - Put
                  - Public
                  - Access
                  - Blocks
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
            /{Bucket}?accelerate:
              PUT:
                summary: PutBucketAccelerateConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the accelerate configuration of
                  an existing bucket. Amazon S3 Transfer Acceleration is a
                  bucket-level feature that enables you to perform faster data
                  transfers to Amazon S3.</p> <p> To use this operation, you
                  must have permission to perform the
                  <code>s3:PutAccelerateConfiguration</code> action. The bucket
                  owner has this permission by default. The bucket owner can
                  grant this permission to others. For more information about
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a>.</p> <p>
                  The Transfer Acceleration state of a bucket can be set to one
                  of the following two values:</p> <ul> <li> <p> Enabled –
                  Enables accelerated data transfers to the bucket.</p> </li>
                  <li> <p> Suspended – Disables accelerated data transfers to
                  the bucket.</p> </li> </ul> <p>The <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAccelerateConfiguration.html">GetBucketAccelerateConfiguration</a>
                  action returns the transfer acceleration state of a
                  bucket.</p> <p>After setting the Transfer Acceleration state
                  of a bucket to Enabled, it might take up to thirty minutes
                  before the data transfer rates to the bucket increase.</p> <p>
                  The name of the bucket used for Transfer Acceleration must be
                  DNS-compliant and must not contain periods (".").</p> <p> For
                  more information about transfer acceleration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html">Transfer
                  Acceleration</a>.</p> <p>The following operations are related
                  to <code>PutBucketAccelerateConfiguration</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAccelerateConfiguration.html">GetBucketAccelerateConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Accelerate
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
            /{Bucket}?acl:
              PUT:
                summary: PutBucketAcl
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the permissions on an existing
                  bucket using access control lists (ACL). For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/S3_ACLs_UsingACLs.html">Using
                  ACLs</a>. To set the ACL of a bucket, you must have the
                  <code>WRITE_ACP</code> permission.</p> <p>You can use one of
                  the following two ways to set a bucket's permissions:</p> <ul>
                  <li> <p>Specify the ACL in the request body</p> </li> <li>
                  <p>Specify permissions using request headers</p> </li> </ul>
                  <note> <p>You cannot specify access permission using both the
                  body and the request headers.</p> </note> <p>Depending on your
                  application needs, you may choose to set the ACL on a bucket
                  using either the request body or the headers. For example, if
                  you have an existing application that updates a bucket ACL
                  using the request body, then you can continue to use that
                  approach.</p> <important> <p>If your bucket uses the bucket
                  owner enforced setting for S3 Object Ownership, ACLs are
                  disabled and no longer affect permissions. You must use
                  policies to grant access to your bucket and the objects in it.
                  Requests to set ACLs or update ACLs fail and return the
                  <code>AccessControlListNotSupported</code> error code.
                  Requests to read ACLs are still supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html">Controlling
                  object ownership</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </important> <dl> <dt>Permissions</dt> <dd> <p>You can set
                  access permissions by using one of the following methods:</p>
                  <ul> <li> <p>Specify a canned ACL with the
                  <code>x-amz-acl</code> request header. Amazon S3 supports a
                  set of predefined ACLs, known as <i>canned ACLs</i>. Each
                  canned ACL has a predefined set of grantees and permissions.
                  Specify the canned ACL name as the value of
                  <code>x-amz-acl</code>. If you use this header, you cannot use
                  other access control-specific headers in your request. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#CannedACL">Canned
                  ACL</a>.</p> </li> <li> <p>Specify access permissions
                  explicitly with the <code>x-amz-grant-read</code>,
                  <code>x-amz-grant-read-acp</code>,
                  <code>x-amz-grant-write-acp</code>, and
                  <code>x-amz-grant-full-control</code> headers. When using
                  these headers, you specify explicit access permissions and
                  grantees (Amazon Web Services accounts or Amazon S3 groups)
                  who will receive the permission. If you use these ACL-specific
                  headers, you cannot use the <code>x-amz-acl</code> header to
                  set a canned ACL. These parameters map to the set of
                  permissions that Amazon S3 supports in an ACL. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a>.</p> <p>You specify each
                  grantee as a type=value pair, where the type is one of the
                  following:</p> <ul> <li> <p> <code>id</code> – if the value
                  specified is the canonical user ID of an Amazon Web Services
                  account</p> </li> <li> <p> <code>uri</code> – if you are
                  granting permissions to a predefined group</p> </li> <li> <p>
                  <code>emailAddress</code> – if the value specified is the
                  email address of an Amazon Web Services account</p> <note>
                  <p>Using email addresses to specify a grantee is only
                  supported in the following Amazon Web Services Regions: </p>
                  <ul> <li> <p>US East (N. Virginia)</p> </li> <li> <p>US West
                  (N. California)</p> </li> <li> <p> US West (Oregon)</p> </li>
                  <li> <p> Asia Pacific (Singapore)</p> </li> <li> <p>Asia
                  Pacific (Sydney)</p> </li> <li> <p>Asia Pacific (Tokyo)</p>
                  </li> <li> <p>Europe (Ireland)</p> </li> <li> <p>South America
                  (São Paulo)</p> </li> </ul> <p>For a list of all the Amazon S3
                  supported Regions and endpoints, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> <p>For example, the
                  following <code>x-amz-grant-write</code> header grants create,
                  overwrite, and delete objects permission to LogDelivery group
                  predefined by Amazon S3 and two Amazon Web Services accounts
                  identified by their email addresses.</p> <p>
                  <code>x-amz-grant-write:
                  uri="http://acs.amazonaws.com/groups/s3/LogDelivery",
                  id="111122223333", id="555566667777" </code> </p> </li> </ul>
                  <p>You can use either a canned ACL or specify access
                  permissions explicitly. You cannot do both.</p> </dd>
                  <dt>Grantee Values</dt> <dd> <p>You can specify the person
                  (grantee) to whom you're assigning access rights (using
                  request elements) in the following ways:</p> <ul> <li> <p>By
                  the person's ID:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p>DisplayName is optional and
                  ignored in the request</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> <li> <p>By Email address:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;&amp;&lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the CanonicalUser and, in a
                  response to a GET Object acl request, appears as the
                  CanonicalUser. </p> <note> <p>Using email addresses to specify
                  a grantee is only supported in the following Amazon Web
                  Services Regions: </p> <ul> <li> <p>US East (N. Virginia)</p>
                  </li> <li> <p>US West (N. California)</p> </li> <li> <p> US
                  West (Oregon)</p> </li> <li> <p> Asia Pacific (Singapore)</p>
                  </li> <li> <p>Asia Pacific (Sydney)</p> </li> <li> <p>Asia
                  Pacific (Tokyo)</p> </li> <li> <p>Europe (Ireland)</p> </li>
                  <li> <p>South America (São Paulo)</p> </li> </ul> <p>For a
                  list of all the Amazon S3 supported Regions and endpoints, see
                  <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> </dd> </dl> <p>The
                  following operations are related to
                  <code>PutBucketAcl</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAcl.html">GetObjectAcl</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - ACL
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
            /{Bucket}?location:
              GET:
                summary: GetBucketLocation
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the Region the bucket resides
                  in. You set the bucket's Region using the
                  <code>LocationConstraint</code> request parameter in a
                  <code>CreateBucket</code> request. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>.</p>
                  <p>When you use this API operation with an access point,
                  provide the alias of the access point in place of the bucket
                  name.</p> <p>When you use this API operation with an Object
                  Lambda access point, provide the alias of the Object Lambda
                  access point in place of the bucket name. If the Object Lambda
                  access point alias in a request is not valid, the error code
                  <code>InvalidAccessPointAliasError</code> is returned. For
                  more information about
                  <code>InvalidAccessPointAliasError</code>, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#ErrorCodeList">List
                  of Error Codes</a>.</p> <note> <p>We recommend that you use <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadBucket.html">HeadBucket</a>
                  to return the Region that a bucket resides in. For backward
                  compatibility, Amazon S3 continues to support
                  GetBucketLocation.</p> </note> <p>The following operations are
                  related to <code>GetBucketLocation</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - Locations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
            /{Bucket}?logging:
              PUT:
                summary: PutBucketLogging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Set the logging parameters for a
                  bucket and to specify permissions for who can view and modify
                  the logging parameters. All logs are saved to buckets in the
                  same Amazon Web Services Region as the source bucket. To set
                  the logging status of a bucket, you must be the bucket
                  owner.</p> <p>The bucket owner is automatically granted
                  FULL_CONTROL to all logs. You use the <code>Grantee</code>
                  request element to grant access to other people. The
                  <code>Permissions</code> request element specifies the kind of
                  access the grantee has to the logs.</p> <important> <p>If the
                  target bucket for log delivery uses the bucket owner enforced
                  setting for S3 Object Ownership, you can't use the
                  <code>Grantee</code> request element to grant access to
                  others. Permissions can only be granted using policies. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/enable-server-access-logging.html#grant-log-delivery-permissions-general">Permissions
                  for server access log delivery</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </important> <dl> <dt>Grantee Values</dt> <dd>
                  <p>You can specify the person (grantee) to whom you're
                  assigning access rights (by using request elements) in the
                  following ways:</p> <ul> <li> <p>By the person's ID:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p> <code>DisplayName</code> is
                  optional and ignored in the request.</p> </li> <li> <p>By
                  Email address:</p> <p> <code> &lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;&lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the
                  <code>CanonicalUser</code> and, in a response to a
                  <code>GETObjectAcl</code> request, appears as the
                  CanonicalUser.</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> </ul> </dd> </dl> <p>To enable logging, you use
                  <code>LoggingEnabled</code> and its children request elements.
                  To disable logging, you use an empty
                  <code>BucketLoggingStatus</code> request element:</p> <p>
                  <code>&lt;BucketLoggingStatus
                  xmlns="http://doc.s3.amazonaws.com/2006-03-01" /&gt;</code>
                  </p> <p>For more information about server access logging, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerLogs.html">Server
                  Access Logging</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <p>For more information about creating a bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>.
                  For more information about returning the logging status of a
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLogging.html">GetBucketLogging</a>.</p>
                  <p>The following operations are related to
                  <code>PutBucketLogging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLogging.html">GetBucketLogging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Logging
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
            /{Bucket}?notification:
              PUT:
                summary: PutBucketNotificationConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Enables notifications of specified
                  events for a bucket. For more information about event
                  notifications, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Event Notifications</a>.</p> <p>Using this API, you can
                  replace an existing notification configuration. The
                  configuration is an XML file that defines the event types that
                  you want Amazon S3 to publish and the destination where you
                  want Amazon S3 to publish an event notification when it
                  detects an event of the specified type.</p> <p>By default,
                  your bucket has no event notifications configured. That is,
                  the notification configuration will be an empty
                  <code>NotificationConfiguration</code>.</p> <p>
                  <code>&lt;NotificationConfiguration&gt;</code> </p> <p>
                  <code>&lt;/NotificationConfiguration&gt;</code> </p> <p>This
                  action replaces the existing notification configuration with
                  the configuration you include in the request body.</p>
                  <p>After Amazon S3 receives this request, it first verifies
                  that any Amazon Simple Notification Service (Amazon SNS) or
                  Amazon Simple Queue Service (Amazon SQS) destination exists,
                  and that the bucket owner has permission to publish to it by
                  sending a test notification. In the case of Lambda
                  destinations, Amazon S3 verifies that the Lambda function
                  permissions grant Amazon S3 permission to invoke the function
                  from the Amazon S3 bucket. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Notifications for Amazon S3 Events</a>.</p> <p>You can disable
                  notifications by adding the empty NotificationConfiguration
                  element.</p> <p>For more information about the number of event
                  notification configurations that you can create per bucket,
                  see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/s3.html#limits_s3">Amazon
                  S3 service quotas</a> in <i>Amazon Web Services General
                  Reference</i>.</p> <p>By default, only the bucket owner can
                  configure notifications on a bucket. However, bucket owners
                  can use a bucket policy to grant permission to other users to
                  set this configuration with the required
                  <code>s3:PutBucketNotification</code> permission.</p> <note>
                  <p>The PUT notification is an atomic operation. For example,
                  suppose your notification configuration includes SNS topic,
                  SQS queue, and Lambda function configurations. When you send a
                  PUT request with this configuration, Amazon S3 sends test
                  messages to your SNS topic. If the message fails, the entire
                  PUT action will fail, and Amazon S3 will not add the
                  configuration to your bucket.</p> </note> <p>If the
                  configuration in the request body includes only one
                  <code>TopicConfiguration</code> specifying only the
                  <code>s3:ReducedRedundancyLostObject</code> event type, the
                  response will also include the
                  <code>x-amz-sns-test-message-id</code> header containing the
                  message ID of the test notification sent to the topic.</p>
                  <p>The following action is related to
                  <code>PutBucketNotificationConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketNotificationConfiguration.html">GetBucketNotificationConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Notifications
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
            /{Bucket}?policyStatus:
              GET:
                summary: GetBucketPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Retrieves the policy status for an
                  Amazon S3 bucket, indicating whether the bucket is public. In
                  order to use this operation, you must have the
                  <code>s3:GetBucketPolicyStatus</code> permission. For more
                  information about Amazon S3 permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a>.</p> <p> For more information
                  about when Amazon S3 considers a bucket public, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status">The
                  Meaning of "Public"</a>. </p> <p>The following operations are
                  related to <code>GetBucketPolicyStatus</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">Using
                  Amazon S3 Block Public Access</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutPublicAccessBlock.html">PutPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - Policies
                  - Status
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
            /{Bucket}?requestPayment:
              PUT:
                summary: PutBucketRequestPayment
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the request payment configuration
                  for a bucket. By default, the bucket owner pays for downloads
                  from the bucket. This configuration parameter enables the
                  bucket owner (only) to specify that the person requesting the
                  download will be charged for the download. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RequesterPaysBuckets.html">Requester
                  Pays Buckets</a>.</p> <p>The following operations are related
                  to <code>PutBucketRequestPayment</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketRequestPayment.html">GetBucketRequestPayment</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Request
                  - Payments
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
            /{Bucket}?versioning:
              PUT:
                summary: PutBucketVersioning
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Sets the versioning state of an
                  existing bucket.</p> <p>You can set the versioning state with
                  one of the following values:</p> <p> <b>Enabled</b>—Enables
                  versioning for the objects in the bucket. All objects added to
                  the bucket receive a unique version ID.</p> <p>
                  <b>Suspended</b>—Disables versioning for the objects in the
                  bucket. All objects added to the bucket receive the version ID
                  null.</p> <p>If the versioning state has never been set on a
                  bucket, it has no versioning state; a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html">GetBucketVersioning</a>
                  request does not return a versioning state value.</p> <p>In
                  order to enable MFA Delete, you must be the bucket owner. If
                  you are the bucket owner and want to enable MFA Delete in the
                  bucket versioning configuration, you must include the
                  <code>x-amz-mfa request</code> header and the
                  <code>Status</code> and the <code>MfaDelete</code> request
                  elements in a request to set the versioning state of the
                  bucket.</p> <important> <p>If you have an object expiration
                  lifecycle configuration in your non-versioned bucket and you
                  want to maintain the same permanent delete behavior when you
                  enable versioning, you must add a noncurrent expiration
                  policy. The noncurrent expiration lifecycle configuration will
                  manage the deletes of the noncurrent object versions in the
                  version-enabled bucket. (A version-enabled bucket maintains
                  one current and zero or more noncurrent object versions.) For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html#lifecycle-and-other-bucket-config">Lifecycle
                  and Versioning</a>.</p> </important> <p>The following
                  operations are related to
                  <code>PutBucketVersioning</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html">GetBucketVersioning</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Versioning
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
            /{Bucket}/{Key+}?acl:
              PUT:
                summary: PutObjectAcl
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Uses the <code>acl</code> subresource
                  to set the access control list (ACL) permissions for a new or
                  existing object in an S3 bucket. You must have the
                  <code>WRITE_ACP</code> permission to set the ACL of an object.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#permissions">What
                  permissions can I grant?</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This functionality is not supported for
                  Amazon S3 on Outposts.</p> <p>Depending on your application
                  needs, you can choose to set the ACL on an object using either
                  the request body or the headers. For example, if you have an
                  existing application that updates a bucket ACL using the
                  request body, you can continue to use that approach. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <important> <p>If your bucket uses the bucket
                  owner enforced setting for S3 Object Ownership, ACLs are
                  disabled and no longer affect permissions. You must use
                  policies to grant access to your bucket and the objects in it.
                  Requests to set ACLs or update ACLs fail and return the
                  <code>AccessControlListNotSupported</code> error code.
                  Requests to read ACLs are still supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html">Controlling
                  object ownership</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </important> <dl> <dt>Permissions</dt> <dd> <p>You can set
                  access permissions using one of the following methods:</p>
                  <ul> <li> <p>Specify a canned ACL with the
                  <code>x-amz-acl</code> request header. Amazon S3 supports a
                  set of predefined ACLs, known as canned ACLs. Each canned ACL
                  has a predefined set of grantees and permissions. Specify the
                  canned ACL name as the value of <code>x-amz-ac</code>l. If you
                  use this header, you cannot use other access control-specific
                  headers in your request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#CannedACL">Canned
                  ACL</a>.</p> </li> <li> <p>Specify access permissions
                  explicitly with the <code>x-amz-grant-read</code>,
                  <code>x-amz-grant-read-acp</code>,
                  <code>x-amz-grant-write-acp</code>, and
                  <code>x-amz-grant-full-control</code> headers. When using
                  these headers, you specify explicit access permissions and
                  grantees (Amazon Web Services accounts or Amazon S3 groups)
                  who will receive the permission. If you use these ACL-specific
                  headers, you cannot use <code>x-amz-acl</code> header to set a
                  canned ACL. These parameters map to the set of permissions
                  that Amazon S3 supports in an ACL. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html">Access
                  Control List (ACL) Overview</a>.</p> <p>You specify each
                  grantee as a type=value pair, where the type is one of the
                  following:</p> <ul> <li> <p> <code>id</code> – if the value
                  specified is the canonical user ID of an Amazon Web Services
                  account</p> </li> <li> <p> <code>uri</code> – if you are
                  granting permissions to a predefined group</p> </li> <li> <p>
                  <code>emailAddress</code> – if the value specified is the
                  email address of an Amazon Web Services account</p> <note>
                  <p>Using email addresses to specify a grantee is only
                  supported in the following Amazon Web Services Regions: </p>
                  <ul> <li> <p>US East (N. Virginia)</p> </li> <li> <p>US West
                  (N. California)</p> </li> <li> <p> US West (Oregon)</p> </li>
                  <li> <p> Asia Pacific (Singapore)</p> </li> <li> <p>Asia
                  Pacific (Sydney)</p> </li> <li> <p>Asia Pacific (Tokyo)</p>
                  </li> <li> <p>Europe (Ireland)</p> </li> <li> <p>South America
                  (São Paulo)</p> </li> </ul> <p>For a list of all the Amazon S3
                  supported Regions and endpoints, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> <p>For example, the
                  following <code>x-amz-grant-read</code> header grants list
                  objects permission to the two Amazon Web Services accounts
                  identified by their email addresses.</p> <p>
                  <code>x-amz-grant-read: emailAddress="xyz@amazon.com",
                  emailAddress="abc@amazon.com" </code> </p> </li> </ul> <p>You
                  can use either a canned ACL or specify access permissions
                  explicitly. You cannot do both.</p> </dd> <dt>Grantee
                  Values</dt> <dd> <p>You can specify the person (grantee) to
                  whom you're assigning access rights (using request elements)
                  in the following ways:</p> <ul> <li> <p>By the person's
                  ID:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="CanonicalUser"&gt;&lt;ID&gt;&lt;&gt;ID&lt;&gt;&lt;/ID&gt;&lt;DisplayName&gt;&lt;&gt;GranteesEmail&lt;&gt;&lt;/DisplayName&gt;
                  &lt;/Grantee&gt;</code> </p> <p>DisplayName is optional and
                  ignored in the request.</p> </li> <li> <p>By URI:</p> <p>
                  <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="Group"&gt;&lt;URI&gt;&lt;&gt;http://acs.amazonaws.com/groups/global/AuthenticatedUsers&lt;&gt;&lt;/URI&gt;&lt;/Grantee&gt;</code>
                  </p> </li> <li> <p>By Email address:</p> <p> <code>&lt;Grantee
                  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                  xsi:type="AmazonCustomerByEmail"&gt;&lt;EmailAddress&gt;&lt;&gt;Grantees@email.com&lt;&gt;&lt;/EmailAddress&gt;lt;/Grantee&gt;</code>
                  </p> <p>The grantee is resolved to the CanonicalUser and, in a
                  response to a GET Object acl request, appears as the
                  CanonicalUser.</p> <note> <p>Using email addresses to specify
                  a grantee is only supported in the following Amazon Web
                  Services Regions: </p> <ul> <li> <p>US East (N. Virginia)</p>
                  </li> <li> <p>US West (N. California)</p> </li> <li> <p> US
                  West (Oregon)</p> </li> <li> <p> Asia Pacific (Singapore)</p>
                  </li> <li> <p>Asia Pacific (Sydney)</p> </li> <li> <p>Asia
                  Pacific (Tokyo)</p> </li> <li> <p>Europe (Ireland)</p> </li>
                  <li> <p>South America (São Paulo)</p> </li> </ul> <p>For a
                  list of all the Amazon S3 supported Regions and endpoints, see
                  <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region">Regions
                  and Endpoints</a> in the Amazon Web Services General
                  Reference.</p> </note> </li> </ul> </dd> <dt>Versioning</dt>
                  <dd> <p>The ACL of an object is set at the object version
                  level. By default, PUT sets the ACL of the current version of
                  an object. To set the ACL of a different version, use the
                  <code>versionId</code> subresource.</p> </dd> </dl> <p>The
                  following operations are related to
                  <code>PutObjectAcl</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html">CopyObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Objects
                  - ACL
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
            /{Bucket}/{Key+}?attributes:
              GET:
                summary: GetObjectAttributes
                description: >-
                  <p>Retrieves all the metadata from an object without returning
                  the object itself. This operation is useful if you're
                  interested only in an object's metadata. </p> <p>
                  <code>GetObjectAttributes</code> combines the functionality of
                  <code>HeadObject</code> and <code>ListParts</code>. All of the
                  data returned with each of those individual calls can be
                  returned with a single call to
                  <code>GetObjectAttributes</code>.</p> <note> <p> <b>Directory
                  buckets</b> - For directory buckets, you must make requests
                  for this API operation to the Zonal endpoint. These endpoints
                  support virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - To use
                  <code>GetObjectAttributes</code>, you must have READ access to
                  the object. The permissions that you need to use this
                  operation with depend on whether the bucket is versioned. If
                  the bucket is versioned, you need both the
                  <code>s3:GetObjectVersion</code> and
                  <code>s3:GetObjectVersionAttributes</code> permissions for
                  this operation. If the bucket is not versioned, you need the
                  <code>s3:GetObject</code> and
                  <code>s3:GetObjectAttributes</code> permissions. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html">Specifying
                  Permissions in a Policy</a> in the <i>Amazon S3 User
                  Guide</i>. If the object that you request does not exist, the
                  error Amazon S3 returns depends on whether you also have the
                  <code>s3:ListBucket</code> permission.</p> <ul> <li> <p>If you
                  have the <code>s3:ListBucket</code> permission on the bucket,
                  Amazon S3 returns an HTTP status code <code>404 Not
                  Found</code> ("no such key") error.</p> </li> <li> <p>If you
                  don't have the <code>s3:ListBucket</code> permission, Amazon
                  S3 returns an HTTP status code <code>403 Forbidden</code>
                  ("access denied") error.</p> </li> </ul> </li> <li> <p>
                  <b>Directory bucket permissions</b> - To grant access to this
                  API operation on a directory bucket, we recommend that you use
                  the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Encryption</dt> <dd> <note> <p>Encryption request headers,
                  like <code>x-amz-server-side-encryption</code>, should not be
                  sent for <code>HEAD</code> requests if your object uses
                  server-side encryption with Key Management Service (KMS) keys
                  (SSE-KMS), dual-layer server-side encryption with Amazon Web
                  Services KMS keys (DSSE-KMS), or server-side encryption with
                  Amazon S3 managed encryption keys (SSE-S3). The
                  <code>x-amz-server-side-encryption</code> header is used when
                  you <code>PUT</code> an object to S3 and want to specify the
                  encryption method. If you include this header in a
                  <code>GET</code> request for an object that uses these types
                  of keys, you’ll get an HTTP <code>400 Bad Request</code>
                  error. It's because the encryption method can't be changed
                  when you retrieve the object.</p> </note> <p>If you encrypt an
                  object by using server-side encryption with customer-provided
                  encryption keys (SSE-C) when you store the object in Amazon
                  S3, then when you retrieve the metadata from the object, you
                  must use the following headers to provide the encryption key
                  for the server to be able to retrieve the object's metadata.
                  The headers are: </p> <ul> <li> <p>
                  <code>x-amz-server-side-encryption-customer-algorithm</code>
                  </p> </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key</code> </p>
                  </li> <li> <p>
                  <code>x-amz-server-side-encryption-customer-key-MD5</code>
                  </p> </li> </ul> <p>For more information about SSE-C, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerSideEncryptionCustomerKeys.html">Server-Side
                  Encryption (Using Customer-Provided Encryption Keys)</a> in
                  the <i>Amazon S3 User Guide</i>.</p> <note> <p> <b>Directory
                  bucket permissions</b> - For directory buckets, only
                  server-side encryption with Amazon S3 managed keys (SSE-S3)
                  (<code>AES256</code>) is supported.</p> </note> </dd>
                  <dt>Versioning</dt> <dd> <p> <b>Directory buckets</b> - S3
                  Versioning isn't enabled and supported for directory buckets.
                  For this API operation, only the <code>null</code> value of
                  the version ID is supported by directory buckets. You can only
                  specify <code>null</code> to the <code>versionId</code> query
                  parameter in the request.</p> </dd> <dt>Conditional request
                  headers</dt> <dd> <p>Consider the following when using request
                  headers:</p> <ul> <li> <p>If both of the <code>If-Match</code>
                  and <code>If-Unmodified-Since</code> headers are present in
                  the request as follows, then Amazon S3 returns the HTTP status
                  code <code>200 OK</code> and the data requested:</p> <ul> <li>
                  <p> <code>If-Match</code> condition evaluates to
                  <code>true</code>.</p> </li> <li> <p>
                  <code>If-Unmodified-Since</code> condition evaluates to
                  <code>false</code>.</p> </li> </ul> <p>For more information
                  about conditional requests, see <a
                  href="https://tools.ietf.org/html/rfc7232">RFC 7232</a>.</p>
                  </li> <li> <p>If both of the <code>If-None-Match</code> and
                  <code>If-Modified-Since</code> headers are present in the
                  request as follows, then Amazon S3 returns the HTTP status
                  code <code>304 Not Modified</code>:</p> <ul> <li> <p>
                  <code>If-None-Match</code> condition evaluates to
                  <code>false</code>.</p> </li> <li> <p>
                  <code>If-Modified-Since</code> condition evaluates to
                  <code>true</code>.</p> </li> </ul> <p>For more information
                  about conditional requests, see <a
                  href="https://tools.ietf.org/html/rfc7232">RFC 7232</a>.</p>
                  </li> </ul> </dd> <dt>HTTP Host header syntax</dt> <dd> <p>
                  <b>Directory buckets </b> - The HTTP Host header syntax is
                  <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following actions are related to
                  <code>GetObjectAttributes</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAcl.html">GetObjectAcl</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectLegalHold.html">GetObjectLegalHold</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectLockConfiguration.html">GetObjectLockConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectRetention.html">GetObjectRetention</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html">GetObjectTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadObject.html">HeadObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Objects
                  - Attributes
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
            /{Bucket}/{Key+}?legal-hold:
              PUT:
                summary: PutObjectLegalHold
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Applies a legal hold configuration to
                  the specified object. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>.</p> <p>This functionality is not supported for
                  Amazon S3 on Outposts.</p>
                tags:
                  - Put
                  - Objects
                  - Legal
                  - Hold
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
            /{Bucket}?object-lock:
              PUT:
                summary: PutObjectLockConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Places an Object Lock configuration on
                  the specified bucket. The rule specified in the Object Lock
                  configuration will be applied by default to every new object
                  placed in the specified bucket. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>. </p> <note> <ul> <li> <p>The
                  <code>DefaultRetention</code> settings require both a mode and
                  a period.</p> </li> <li> <p>The <code>DefaultRetention</code>
                  period can be either <code>Days</code> or <code>Years</code>
                  but you must select one. You cannot specify <code>Days</code>
                  and <code>Years</code> at the same time.</p> </li> <li> <p>You
                  can enable Object Lock for new or existing buckets. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock-configure.html">Configuring
                  Object Lock</a>.</p> </li> </ul> </note>
                tags:
                  - Put
                  - Objects
                  - Locks
                  - Configurations
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
            /{Bucket}/{Key+}?retention:
              PUT:
                summary: PutObjectRetention
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Places an Object Retention
                  configuration on an object. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Locking
                  Objects</a>. Users or accounts require the
                  <code>s3:PutObjectRetention</code> permission in order to
                  place an Object Retention configuration on objects. Bypassing
                  a Governance Retention configuration requires the
                  <code>s3:BypassGovernanceRetention</code> permission. </p>
                  <p>This functionality is not supported for Amazon S3 on
                  Outposts.</p>
                tags:
                  - Put
                  - Objects
                  - Retention
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
            /{Bucket}/{Key+}?torrent:
              GET:
                summary: GetObjectTorrent
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns torrent files from a bucket.
                  BitTorrent can save you bandwidth when you're distributing
                  large files.</p> <note> <p>You can get torrent only for
                  objects that are less than 5 GB in size, and that are not
                  encrypted using server-side encryption with a
                  customer-provided encryption key.</p> </note> <p>To use GET,
                  you must have READ access to the object.</p> <p>This
                  functionality is not supported for Amazon S3 on Outposts.</p>
                  <p>The following action is related to
                  <code>GetObjectTorrent</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Objects
                  - Torrent
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /:
              GET:
                summary: ListDirectoryBuckets
                description: >-
                  <p>Returns a list of all Amazon S3 directory buckets owned by
                  the authenticated sender of the request. For more information
                  about directory buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/directory-buckets-overview.html">Directory
                  buckets</a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>
                  <b>Directory buckets </b> - For directory buckets, you must
                  make requests for this API operation to the Regional endpoint.
                  These endpoints support path-style requests in the format
                  <code>https://s3express-control.<i>region_code</i>.amazonaws.com/<i>bucket-name</i>
                  </code>. Virtual-hosted-style requests aren't supported. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3express:ListAllMyDirectoryBuckets</code>
                  permission in an IAM identity-based policy instead of a bucket
                  policy. Cross-account access to this API operation isn't
                  supported. This operation can only be performed by the Amazon
                  Web Services account that owns the resource. For more
                  information about directory bucket policies and permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-security-iam.html">Amazon
                  Web Services Identity and Access Management (IAM) for S3
                  Express One Zone</a> in the <i>Amazon S3 User Guide</i>.</p>
                  </dd> <dt>HTTP Host header syntax</dt> <dd> <p> <b>Directory
                  buckets </b> - The HTTP Host header syntax is
                  <code>s3express-control.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl>
                tags:
                  - Lists
                  - Directory
                  - Buckets
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /{Bucket}?uploads:
              GET:
                summary: ListMultipartUploads
                description: >-
                  <p>This operation lists in-progress multipart uploads in a
                  bucket. An in-progress multipart upload is a multipart upload
                  that has been initiated by the
                  <code>CreateMultipartUpload</code> request, but has not yet
                  been completed or aborted.</p> <note> <p> <b>Directory
                  buckets</b> - If multipart uploads in a directory bucket are
                  in progress, you can't delete the bucket until all the
                  in-progress multipart uploads are aborted or completed. </p>
                  </note> <p>The <code>ListMultipartUploads</code> operation
                  returns a maximum of 1,000 multipart uploads in the response.
                  The limit of 1,000 multipart uploads is also the default
                  value. You can further limit the number of uploads in a
                  response by specifying the <code>max-uploads</code> request
                  parameter. If there are more than 1,000 multipart uploads that
                  satisfy your <code>ListMultipartUploads</code> request, the
                  response returns an <code>IsTruncated</code> element with the
                  value of <code>true</code>, a <code>NextKeyMarker</code>
                  element, and a <code>NextUploadIdMarker</code> element. To
                  list the remaining multipart uploads, you need to make
                  subsequent <code>ListMultipartUploads</code> requests. In
                  these requests, include two query parameters:
                  <code>key-marker</code> and <code>upload-id-marker</code>. Set
                  the value of <code>key-marker</code> to the
                  <code>NextKeyMarker</code> value from the previous response.
                  Similarly, set the value of <code>upload-id-marker</code> to
                  the <code>NextUploadIdMarker</code> value from the previous
                  response.</p> <note> <p> <b>Directory buckets</b> - The
                  <code>upload-id-marker</code> element and the
                  <code>NextUploadIdMarker</code> element aren't supported by
                  directory buckets. To list the additional multipart uploads,
                  you only need to set the value of <code>key-marker</code> to
                  the <code>NextKeyMarker</code> value from the previous
                  response. </p> </note> <p>For more information about multipart
                  uploads, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html">Uploading
                  Objects Using Multipart Upload</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p> <b>Directory buckets</b> - For
                  directory buckets, you must make requests for this API
                  operation to the Zonal endpoint. These endpoints support
                  virtual-hosted-style requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - For
                  information about permissions required to use the multipart
                  upload API, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuAndPermissions.html">Multipart
                  Upload and Permissions</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </li> <li> <p> <b>Directory bucket
                  permissions</b> - To grant access to this API operation on a
                  directory bucket, we recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Sorting of multipart uploads in response</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket</b> - In the
                  <code>ListMultipartUploads</code> response, the multipart
                  uploads are sorted based on two criteria:</p> <ul> <li>
                  <p>Key-based sorting - Multipart uploads are initially sorted
                  in ascending order based on their object keys.</p> </li> <li>
                  <p>Time-based sorting - For uploads that share the same object
                  key, they are further sorted in ascending order based on the
                  upload initiation time. Among uploads with the same key, the
                  one that was initiated first will appear before the ones that
                  were initiated later.</p> </li> </ul> </li> <li> <p>
                  <b>Directory bucket</b> - In the
                  <code>ListMultipartUploads</code> response, the multipart
                  uploads aren't sorted lexicographically based on the object
                  keys. </p> </li> </ul> </dd> <dt>HTTP Host header syntax</dt>
                  <dd> <p> <b>Directory buckets </b> - The HTTP Host header
                  syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <p>The following operations are related to
                  <code>ListMultipartUploads</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateMultipartUpload.html">CreateMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_UploadPart.html">UploadPart</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CompleteMultipartUpload.html">CompleteMultipartUpload</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListParts.html">ListParts</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_AbortMultipartUpload.html">AbortMultipartUpload</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Multipart
                  - Uploads
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
            /{Bucket}?versions:
              GET:
                summary: ListObjectVersions
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns metadata about all versions of
                  the objects in a bucket. You can also use request parameters
                  as selection criteria to return metadata about a subset of all
                  the object versions.</p> <important> <p> To use this
                  operation, you must have permission to perform the
                  <code>s3:ListBucketVersions</code> action. Be aware of the
                  name difference. </p> </important> <note> <p> A <code>200
                  OK</code> response can contain valid or invalid XML. Make sure
                  to design your application to parse the contents of the
                  response and handle it appropriately.</p> </note> <p>To use
                  this operation, you must have READ access to the bucket.</p>
                  <p>The following operations are related to
                  <code>ListObjectVersions</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html">ListObjectsV2</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObject.html">DeleteObject</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - Versions
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
            /{Bucket}?list-type=2:
              GET:
                summary: ListObjectsV2
                description: >-
                  <p>Returns some or all (up to 1,000) of the objects in a
                  bucket with each request. You can use the request parameters
                  as selection criteria to return a subset of the objects in a
                  bucket. A <code>200 OK</code> response can contain valid or
                  invalid XML. Make sure to design your application to parse the
                  contents of the response and handle it appropriately. For more
                  information about listing objects, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ListingKeysUsingAPIs.html">Listing
                  object keys programmatically</a> in the <i>Amazon S3 User
                  Guide</i>. To get a list of your buckets, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html">ListBuckets</a>.</p>
                  <note> <p> <b>Directory buckets</b> - For directory buckets,
                  you must make requests for this API operation to the Zonal
                  endpoint. These endpoints support virtual-hosted-style
                  requests in the format
                  <code>https://<i>bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com/<i>key-name</i>
                  </code>. Path-style requests are not supported. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-express-Regions-and-Zones.html">Regional
                  and Zonal endpoints</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <dl> <dt>Permissions</dt> <dd> <ul>
                  <li> <p> <b>General purpose bucket permissions</b> - To use
                  this operation, you must have READ access to the bucket. You
                  must have permission to perform the <code>s3:ListBucket</code>
                  action. The bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </li> <li> <p> <b>Directory
                  bucket permissions</b> - To grant access to this API operation
                  on a directory bucket, we recommend that you use the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a> API operation for
                  session-based authorization. Specifically, you grant the
                  <code>s3express:CreateSession</code> permission to the
                  directory bucket in a bucket policy or an IAM identity-based
                  policy. Then, you make the <code>CreateSession</code> API call
                  on the bucket to obtain a session token. With the session
                  token in your request header, you can make API requests to
                  this operation. After the session token expires, you make
                  another <code>CreateSession</code> API call to generate a new
                  session token for use. Amazon Web Services CLI or SDKs create
                  session and refresh the session token automatically to avoid
                  service interruptions when a session expires. For more
                  information about authorization, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateSession.html">
                  <code>CreateSession</code> </a>.</p> </li> </ul> </dd>
                  <dt>Sorting order of returned objects</dt> <dd> <ul> <li> <p>
                  <b>General purpose bucket</b> - For general purpose buckets,
                  <code>ListObjectsV2</code> returns objects in lexicographical
                  order based on their key names.</p> </li> <li> <p>
                  <b>Directory bucket</b> - For directory buckets,
                  <code>ListObjectsV2</code> does not return objects in
                  lexicographical order.</p> </li> </ul> </dd> <dt>HTTP Host
                  header syntax</dt> <dd> <p> <b>Directory buckets </b> - The
                  HTTP Host header syntax is <code>
                  <i>Bucket_name</i>.s3express-<i>az_id</i>.<i>region</i>.amazonaws.com</code>.</p>
                  </dd> </dl> <important> <p>This section describes the latest
                  revision of this action. We recommend that you use this
                  revised API operation for application development. For
                  backward compatibility, Amazon S3 continues to support the
                  prior version of this API operation, <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjects.html">ListObjects</a>.</p>
                  </important> <p>The following operations are related to
                  <code>ListObjectsV2</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html">CreateBucket</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Objects
                  - V2
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
            /{Bucket}/{Key+}?restore:
              POST:
                summary: RestoreObject
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Restores an archived copy of an object
                  back into Amazon S3</p> <p>This functionality is not supported
                  for Amazon S3 on Outposts.</p> <p>This action performs the
                  following types of requests: </p> <ul> <li> <p>
                  <code>select</code> - Perform a select query on an archived
                  object</p> </li> <li> <p> <code>restore an archive</code> -
                  Restore an archived object</p> </li> </ul> <p>For more
                  information about the <code>S3</code> structure in the request
                  body, see the following:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/S3_ACLs_UsingACLs.html">Managing
                  Access with ACLs</a> in the <i>Amazon S3 User Guide</i> </p>
                  </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html">Protecting
                  Data Using Server-Side Encryption</a> in the <i>Amazon S3 User
                  Guide</i> </p> </li> </ul> <p>Define the SQL expression for
                  the <code>SELECT</code> type of restoration for your query in
                  the request body's <code>SelectParameters</code> structure.
                  You can use expressions like the following examples.</p> <ul>
                  <li> <p>The following expression returns all records from the
                  specified object.</p> <p> <code>SELECT * FROM Object</code>
                  </p> </li> <li> <p>Assuming that you are not using any headers
                  for data stored in the object, you can specify columns with
                  positional headers.</p> <p> <code>SELECT s._1, s._2 FROM
                  Object s WHERE s._3 &gt; 100</code> </p> </li> <li> <p>If you
                  have headers and you set the <code>fileHeaderInfo</code> in
                  the <code>CSV</code> structure in the request body to
                  <code>USE</code>, you can specify headers in the query. (If
                  you set the <code>fileHeaderInfo</code> field to
                  <code>IGNORE</code>, the first row is skipped for the query.)
                  You cannot mix ordinal positions with header column names.
                  </p> <p> <code>SELECT s.Id, s.FirstName, s.SSN FROM S3Object
                  s</code> </p> </li> </ul> <p>When making a select request, you
                  can also do the following:</p> <ul> <li> <p>To expedite your
                  queries, specify the <code>Expedited</code> tier. For more
                  information about tiers, see "Restoring Archives," later in
                  this topic.</p> </li> <li> <p>Specify details about the data
                  serialization format of both the input object that is being
                  queried and the serialization of the CSV-encoded query
                  results.</p> </li> </ul> <p>The following are additional
                  important facts about the select feature:</p> <ul> <li> <p>The
                  output results are new Amazon S3 objects. Unlike archive
                  retrievals, they are stored until explicitly deleted-manually
                  or through a lifecycle configuration.</p> </li> <li> <p>You
                  can issue more than one select request on the same Amazon S3
                  object. Amazon S3 doesn't duplicate requests, so avoid issuing
                  duplicate requests.</p> </li> <li> <p> Amazon S3 accepts a
                  select request even if the object has already been restored. A
                  select request doesn’t return error response
                  <code>409</code>.</p> </li> </ul> <dl> <dt>Permissions</dt>
                  <dd> <p>To use this operation, you must have permissions to
                  perform the <code>s3:RestoreObject</code> action. The bucket
                  owner has this permission by default and can grant this
                  permission to others. For more information about permissions,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">Permissions
                  Related to Bucket Subresource Operations</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  Access Permissions to Your Amazon S3 Resources</a> in the
                  <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Restoring
                  objects</dt> <dd> <p>Objects that you archive to the S3
                  Glacier Flexible Retrieval Flexible Retrieval or S3 Glacier
                  Deep Archive storage class, and S3 Intelligent-Tiering Archive
                  or S3 Intelligent-Tiering Deep Archive tiers, are not
                  accessible in real time. For objects in the S3 Glacier
                  Flexible Retrieval Flexible Retrieval or S3 Glacier Deep
                  Archive storage classes, you must first initiate a restore
                  request, and then wait until a temporary copy of the object is
                  available. If you want a permanent copy of the object, create
                  a copy of it in the Amazon S3 Standard storage class in your
                  S3 bucket. To access an archived object, you must restore the
                  object for the duration (number of days) that you specify. For
                  objects in the Archive Access or Deep Archive Access tiers of
                  S3 Intelligent-Tiering, you must first initiate a restore
                  request, and then wait until the object is moved into the
                  Frequent Access tier.</p> <p>To restore a specific object
                  version, you can provide a version ID. If you don't provide a
                  version ID, Amazon S3 restores the current version.</p>
                  <p>When restoring an archived object, you can specify one of
                  the following data access tier options in the
                  <code>Tier</code> element of the request body: </p> <ul> <li>
                  <p> <code>Expedited</code> - Expedited retrievals allow you to
                  quickly access your data stored in the S3 Glacier Flexible
                  Retrieval Flexible Retrieval storage class or S3
                  Intelligent-Tiering Archive tier when occasional urgent
                  requests for restoring archives are required. For all but the
                  largest archived objects (250 MB+), data accessed using
                  Expedited retrievals is typically made available within 1–5
                  minutes. Provisioned capacity ensures that retrieval capacity
                  for Expedited retrievals is available when you need it.
                  Expedited retrievals and provisioned capacity are not
                  available for objects stored in the S3 Glacier Deep Archive
                  storage class or S3 Intelligent-Tiering Deep Archive tier.</p>
                  </li> <li> <p> <code>Standard</code> - Standard retrievals
                  allow you to access any of your archived objects within
                  several hours. This is the default option for retrieval
                  requests that do not specify the retrieval option. Standard
                  retrievals typically finish within 3–5 hours for objects
                  stored in the S3 Glacier Flexible Retrieval Flexible Retrieval
                  storage class or S3 Intelligent-Tiering Archive tier. They
                  typically finish within 12 hours for objects stored in the S3
                  Glacier Deep Archive storage class or S3 Intelligent-Tiering
                  Deep Archive tier. Standard retrievals are free for objects
                  stored in S3 Intelligent-Tiering.</p> </li> <li> <p>
                  <code>Bulk</code> - Bulk retrievals free for objects stored in
                  the S3 Glacier Flexible Retrieval and S3 Intelligent-Tiering
                  storage classes, enabling you to retrieve large amounts, even
                  petabytes, of data at no cost. Bulk retrievals typically
                  finish within 5–12 hours for objects stored in the S3 Glacier
                  Flexible Retrieval Flexible Retrieval storage class or S3
                  Intelligent-Tiering Archive tier. Bulk retrievals are also the
                  lowest-cost retrieval option when restoring objects from S3
                  Glacier Deep Archive. They typically finish within 48 hours
                  for objects stored in the S3 Glacier Deep Archive storage
                  class or S3 Intelligent-Tiering Deep Archive tier. </p> </li>
                  </ul> <p>For more information about archive retrieval options
                  and provisioned capacity for <code>Expedited</code> data
                  access, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html">Restoring
                  Archived Objects</a> in the <i>Amazon S3 User Guide</i>. </p>
                  <p>You can use Amazon S3 restore speed upgrade to change the
                  restore speed to a faster speed while it is in progress. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/restoring-objects.html#restoring-objects-upgrade-tier.title.html">
                  Upgrading the speed of an in-progress restore</a> in the
                  <i>Amazon S3 User Guide</i>. </p> <p>To get the status of
                  object restoration, you can send a <code>HEAD</code> request.
                  Operations return the <code>x-amz-restore</code> header, which
                  provides information about the restoration status, in the
                  response. You can use Amazon S3 event notifications to notify
                  you when a restore is initiated or completed. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html">Configuring
                  Amazon S3 Event Notifications</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>After restoring an archived object, you can
                  update the restoration period by reissuing the request with a
                  new period. Amazon S3 updates the restoration period relative
                  to the current time and charges only for the request-there are
                  no data transfer charges. You cannot update the restoration
                  period when Amazon S3 is actively processing your current
                  restore request for the object.</p> <p>If your bucket has a
                  lifecycle configuration with a rule that includes an
                  expiration action, the object expiration overrides the life
                  span that you specify in a restore request. For example, if
                  you restore an object copy for 10 days, but the object is
                  scheduled to expire in 3 days, Amazon S3 deletes the object in
                  3 days. For more information about lifecycle configuration,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html">Object
                  Lifecycle Management</a> in <i>Amazon S3 User Guide</i>.</p>
                  </dd> <dt>Responses</dt> <dd> <p>A successful action returns
                  either the <code>200 OK</code> or <code>202 Accepted</code>
                  status code. </p> <ul> <li> <p>If the object is not previously
                  restored, then Amazon S3 returns <code>202 Accepted</code> in
                  the response. </p> </li> <li> <p>If the object is previously
                  restored, Amazon S3 returns <code>200 OK</code> in the
                  response. </p> </li> </ul> <ul> <li> <p>Special errors:</p>
                  <ul> <li> <p> <i>Code: RestoreAlreadyInProgress</i> </p> </li>
                  <li> <p> <i>Cause: Object restore is already in progress.
                  (This error does not apply to SELECT type requests.)</i> </p>
                  </li> <li> <p> <i>HTTP Status Code: 409 Conflict</i> </p>
                  </li> <li> <p> <i>SOAP Fault Code Prefix: Client</i> </p>
                  </li> </ul> </li> <li> <ul> <li> <p> <i>Code:
                  GlacierExpeditedRetrievalNotAvailable</i> </p> </li> <li> <p>
                  <i>Cause: expedited retrievals are currently not available.
                  Try again later. (Returned if there is insufficient capacity
                  to process the Expedited request. This error applies only to
                  Expedited retrievals and not to S3 Standard or Bulk
                  retrievals.)</i> </p> </li> <li> <p> <i>HTTP Status Code:
                  503</i> </p> </li> <li> <p> <i>SOAP Fault Code Prefix: N/A</i>
                  </p> </li> </ul> </li> </ul> </dd> </dl> <p>The following
                  operations are related to <code>RestoreObject</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketNotificationConfiguration.html">GetBucketNotificationConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Restore
                  - Objects
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
            /{Bucket}/{Key+}?select&select-type=2:
              POST:
                summary: SelectObjectContent
                description: "<note> <p>This operation is not supported by directory buckets.</p> </note> <p>This action filters the contents of an Amazon S3 object based on a simple structured query language (SQL) statement. In the request, along with the SQL expression, you must also specify a data serialization format (JSON, CSV, or Apache Parquet) of the object. Amazon S3 uses this format to parse object data into records, and returns only records that match the specified SQL expression. You must also specify the data serialization format for the response.</p> <p>This functionality is not supported for Amazon S3 on Outposts.</p> <p>For more information about Amazon S3 Select, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/selecting-content-from-objects.html\">Selecting Content from Objects</a> and <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-glacier-select-sql-reference-select.html\">SELECT Command</a> in the <i>Amazon S3 User Guide</i>.</p> <p/> <dl> <dt>Permissions</dt> <dd> <p>You must have the <code>s3:GetObject</code> permission for this operation.\_Amazon S3 Select does not support anonymous access. For more information about permissions, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/using-with-s3-actions.html\">Specifying Permissions in a Policy</a> in the <i>Amazon S3 User Guide</i>.</p> </dd> <dt>Object Data Formats</dt> <dd> <p>You can use Amazon S3 Select to query objects that have the following format properties:</p> <ul> <li> <p> <i>CSV, JSON, and Parquet</i> - Objects must be in CSV, JSON, or Parquet format.</p> </li> <li> <p> <i>UTF-8</i> - UTF-8 is the only encoding type Amazon S3 Select supports.</p> </li> <li> <p> <i>GZIP or BZIP2</i> - CSV and JSON files can be compressed using GZIP or BZIP2. GZIP and BZIP2 are the only compression formats that Amazon S3 Select supports for CSV and JSON files. Amazon S3 Select supports columnar compression for Parquet using GZIP or Snappy. Amazon S3 Select does not support whole-object compression for Parquet objects.</p> </li> <li> <p> <i>Server-side encryption</i> - Amazon S3 Select supports querying objects that are protected with server-side encryption.</p> <p>For objects that are encrypted with customer-provided encryption keys (SSE-C), you must use HTTPS, and you must use the headers that are documented in the <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a>. For more information about SSE-C, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerSideEncryptionCustomerKeys.html\">Server-Side Encryption (Using Customer-Provided Encryption Keys)</a> in the <i>Amazon S3 User Guide</i>.</p> <p>For objects that are encrypted with Amazon S3 managed keys (SSE-S3) and Amazon Web Services KMS keys (SSE-KMS), server-side encryption is handled transparently, so you don't need to specify anything. For more information about server-side encryption, including SSE-S3 and SSE-KMS, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html\">Protecting Data Using Server-Side Encryption</a> in the <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd> <dt>Working with the Response Body</dt> <dd> <p>Given the response size is unknown, Amazon S3 Select streams the response as a series of messages and includes a <code>Transfer-Encoding</code> header with <code>chunked</code> as its value in the response. For more information, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/RESTSelectObjectAppendix.html\">Appendix: SelectObjectContent Response</a>.</p> </dd> <dt>GetObject Support</dt> <dd> <p>The <code>SelectObjectContent</code> action does not support the following <code>GetObject</code> functionality. For more information, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a>.</p> <ul> <li> <p> <code>Range</code>: Although you can specify a scan range for an Amazon S3 Select request (see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_SelectObjectContent.html#AmazonS3-SelectObjectContent-request-ScanRange\">SelectObjectContentRequest - ScanRange</a> in the request parameters), you cannot specify the range of bytes of an object to return. </p> </li> <li> <p>The <code>GLACIER</code>, <code>DEEP_ARCHIVE</code>, and <code>REDUCED_REDUNDANCY</code> storage classes, or the <code>ARCHIVE_ACCESS</code> and <code>DEEP_ARCHIVE_ACCESS</code> access tiers of the <code>INTELLIGENT_TIERING</code> storage class: You cannot query objects in the <code>GLACIER</code>, <code>DEEP_ARCHIVE</code>, or <code>REDUCED_REDUNDANCY</code> storage classes, nor objects in the <code>ARCHIVE_ACCESS</code> or <code>DEEP_ARCHIVE_ACCESS</code> access tiers of the <code>INTELLIGENT_TIERING</code> storage class. For more information about storage classes, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html\">Using Amazon S3 storage classes</a> in the <i>Amazon S3 User Guide</i>.</p> </li> </ul> </dd> <dt>Special Errors</dt> <dd> <p>For a list of special errors for this operation, see <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#SelectObjectContentErrorCodeList\">List of SELECT Object Content Error Codes</a> </p> </dd> </dl> <p>The following operations are related to <code>SelectObjectContent</code>:</p> <ul> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html\">GetObject</a> </p> </li> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLifecycleConfiguration.html\">GetBucketLifecycleConfiguration</a> </p> </li> <li> <p> <a href=\"https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html\">PutBucketLifecycleConfiguration</a> </p> </li> </ul>"
                tags:
                  - Select
                  - Objects
                  - Content
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
                  - '?select&select'
            /WriteGetObjectResponse:
              POST:
                summary: WriteGetObjectResponse
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Passes transformed objects to a
                  <code>GetObject</code> operation when using Object Lambda
                  access points. For information about Object Lambda access
                  points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/transforming-objects.html">Transforming
                  objects with Object Lambda access points</a> in the <i>Amazon
                  S3 User Guide</i>.</p> <p>This operation supports metadata
                  that can be returned by <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html">GetObject</a>,
                  in addition to <code>RequestRoute</code>,
                  <code>RequestToken</code>, <code>StatusCode</code>,
                  <code>ErrorCode</code>, and <code>ErrorMessage</code>. The
                  <code>GetObject</code> response metadata is supported so that
                  the <code>WriteGetObjectResponse</code> caller, typically an
                  Lambda function, can provide the same metadata when it
                  internally invokes <code>GetObject</code>. When
                  <code>WriteGetObjectResponse</code> is called by a
                  customer-owned Lambda function, the metadata returned to the
                  end user <code>GetObject</code> call might differ from what
                  Amazon S3 would normally return.</p> <p>You can include any
                  number of metadata headers. When including a metadata header,
                  it should be prefaced with <code>x-amz-meta</code>. For
                  example, <code>x-amz-meta-my-custom-header:
                  MyCustomValue</code>. The primary use case for this is to
                  forward <code>GetObject</code> metadata.</p> <p>Amazon Web
                  Services provides some prebuilt Lambda functions that you can
                  use with S3 Object Lambda to detect and redact personally
                  identifiable information (PII) and decompress S3 objects.
                  These Lambda functions are available in the Amazon Web
                  Services Serverless Application Repository, and can be
                  selected through the Amazon Web Services Management Console
                  when you create your Object Lambda access point.</p>
                  <p>Example 1: PII Access Control - This Lambda function uses
                  Amazon Comprehend, a natural language processing (NLP) service
                  using machine learning to find insights and relationships in
                  text. It automatically detects personally identifiable
                  information (PII) such as names, addresses, dates, credit card
                  numbers, and social security numbers from documents in your
                  Amazon S3 bucket. </p> <p>Example 2: PII Redaction - This
                  Lambda function uses Amazon Comprehend, a natural language
                  processing (NLP) service using machine learning to find
                  insights and relationships in text. It automatically redacts
                  personally identifiable information (PII) such as names,
                  addresses, dates, credit card numbers, and social security
                  numbers from documents in your Amazon S3 bucket. </p>
                  <p>Example 3: Decompression - The Lambda function
                  S3ObjectLambdaDecompression, is equipped to decompress objects
                  stored in S3 in one of six compressed file formats including
                  bzip2, gzip, snappy, zlib, zstandard and ZIP. </p> <p>For
                  information on how to view and use these functions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/olap-examples.html">Using
                  Amazon Web Services built Lambda functions</a> in the
                  <i>Amazon S3 User Guid
                tags:
                  - Write
                  - Get
                  - Objects
                  - Responses
                  - Bucket
                  - Keys
                  - '?uploads'
                  - '?session'
                  - '?analytics'
                  - '?cors'
                  - '?encryption'
                  - '?intelligent'
                  - Tiering
                  - '?inventory'
                  - '?lifecycle'
                  - '?metrics'
                  - '?ownership'
                  - Controls
                  - '?policy'
                  - '?replication'
                  - '?tagging'
                  - '?website'
                  - '?delete'
                  - '?public'
                  - Access
                  - Blocks
                  - '?accelerate'
                  - '?acl'
                  - '?location'
                  - '?logging'
                  - '?notification'
                  - Status
                  - '?request'
                  - Payments
                  - '?versioning'
                  - '?attributes'
                  - '?legal'
                  - Hold
                  - '?object'
                  - Locks
                  - '?retention'
                  - '?torrent'
                  - '?versions'
                  - '?list'
                  - Types
                  - '?restore'
                  - '?select&select'
                  - Write
                  - Get
                  - Objects
                  - Respon
    overlays:
      - type: APIs.io Search
        url: overlays/s3-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---