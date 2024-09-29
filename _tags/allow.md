---
name: Allow
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/allow.png
url: https://example.com/apis/allow.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Allow
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---