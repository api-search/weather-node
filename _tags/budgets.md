---
name: Budgets
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/budgets.png
url: https://example.com/apis/budgets.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Budgets
apis:
  - name: cleanrooms
    description: >-
      <p>Welcome to the <i>Clean Rooms API Reference</i>.</p> <p>Clean Rooms is
      an Amazon Web Services service that helps multiple parties to join their
      data together in a secure collaboration workspace. In the collaboration,
      members who can query and receive results can get insights into the
      collective datasets without either party getting access to the other
      party's raw data.</p> <p>To learn more about Clean Rooms concepts,
      procedures, and best practices, see the <a
      href="https://docs.aws.amazon.com/clean-rooms/latest/userguide/what-is.html">Clean
      Rooms User Guide</a>.</p> <p>To learn more about SQL commands, functions,
      and conditions supported in Clean Rooms, see the <a
      href="https://docs.aws.amazon.com/clean-rooms/latest/sql-reference/sql-reference.html">Clean
      Rooms SQL Reference</a>.</p>
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
            title: cleanrooms
          paths:
            /collaborations/{collaborationIdentifier}/batch-analysistemplates:
              POST:
                summary: BatchGetCollaborationAnalysisTemplate
                description: >-
                  <p>Retrieves multiple analysis templates within a
                  collaboration by their Amazon Resource Names (ARNs).</p>
                tags:
                  - Batches
                  - Get
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
            /collaborations/{collaborationIdentifier}/batch-schema:
              POST:
                summary: BatchGetSchema
                description: <p>Retrieves multiple schemas by their identifiers.</p>
                tags:
                  - Batches
                  - Get
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
            /memberships/{membershipIdentifier}/analysistemplates:
              GET:
                summary: ListAnalysisTemplates
                description: <p>Lists analysis templates that the caller owns.</p>
                tags:
                  - Lists
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
            /collaborations:
              GET:
                summary: ListCollaborations
                description: >-
                  <p>Lists collaborations the caller owns, is active in, or has
                  been invited to.</p>
                tags:
                  - Lists
                  - Collaborations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
            /memberships/{membershipIdentifier}/configuredaudiencemodelassociations:
              GET:
                summary: ListConfiguredAudienceModelAssociations
                description: >-
                  <p>Lists information about requested configured audience model
                  associations.</p>
                tags:
                  - Lists
                  - Configured
                  - Audience
                  - Models
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
            /configuredTables:
              GET:
                summary: ListConfiguredTables
                description: <p>Lists configured tables.</p>
                tags:
                  - Lists
                  - Configured
                  - Tables
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
            /configuredTables/{configuredTableIdentifier}/analysisRule:
              POST:
                summary: CreateConfiguredTableAnalysisRule
                description: >-
                  <p>Creates a new analysis rule for a configured table.
                  Currently, only one analysis rule can be created for a given
                  configured table.</p>
                tags:
                  - Create
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
            /memberships/{membershipIdentifier}/configuredTableAssociations:
              GET:
                summary: ListConfiguredTableAssociations
                description: <p>Lists configured table associations for a membership.</p>
                tags:
                  - Lists
                  - Configured
                  - Tables
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
            /memberships:
              GET:
                summary: ListMemberships
                description: >-
                  <p>Lists all memberships resources within the caller's
                  account.</p>
                tags:
                  - Lists
                  - Memberships
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
            /memberships/{membershipIdentifier}/privacybudgettemplates:
              GET:
                summary: ListPrivacyBudgetTemplates
                description: >-
                  <p>Returns detailed information about the privacy budget
                  templates in a specified membership.</p>
                tags:
                  - Lists
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
            /memberships/{membershipIdentifier}/analysistemplates/{analysisTemplateIdentifier}:
              PATCH:
                summary: UpdateAnalysisTemplate
                description: <p>Updates the analysis template metadata.</p>
                tags:
                  - Update
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
            /collaborations/{collaborationIdentifier}:
              PATCH:
                summary: UpdateCollaboration
                description: >-
                  <p>Updates collaboration metadata and can only be called by
                  the collaboration owner.</p>
                tags:
                  - Update
                  - Collaboration
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
            /memberships/{membershipIdentifier}/configuredaudiencemodelassociations/{configuredAudienceModelAssociationIdentifier}:
              PATCH:
                summary: UpdateConfiguredAudienceModelAssociation
                description: >-
                  <p>Provides the details necessary to update a configured
                  audience model association.</p>
                tags:
                  - Update
                  - Configured
                  - Audience
                  - Models
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
            /configuredTables/{configuredTableIdentifier}:
              PATCH:
                summary: UpdateConfiguredTable
                description: <p>Updates a configured table.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
            /configuredTables/{configuredTableIdentifier}/analysisRule/{analysisRuleType}:
              PATCH:
                summary: UpdateConfiguredTableAnalysisRule
                description: <p>Updates a configured table analysis rule.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
            /memberships/{membershipIdentifier}/configuredTableAssociations/{configuredTableAssociationIdentifier}:
              PATCH:
                summary: UpdateConfiguredTableAssociation
                description: <p>Updates a configured table association.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
            /collaborations/{collaborationIdentifier}/member/{accountId}:
              DELETE:
                summary: DeleteMember
                description: >-
                  <p>Removes the specified member from a collaboration. The
                  removed member is placed in the Removed status and can't
                  interact with the collaboration. The removed member's data is
                  inaccessible to active members of the collaboration.</p>
                tags:
                  - Delete
                  - Members
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
            /memberships/{membershipIdentifier}:
              PATCH:
                summary: UpdateMembership
                description: <p>Updates a membership.</p>
                tags:
                  - Update
                  - Membership
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
            /memberships/{membershipIdentifier}/privacybudgettemplates/{privacyBudgetTemplateIdentifier}:
              PATCH:
                summary: UpdatePrivacyBudgetTemplate
                description: >-
                  <p>Updates the privacy budget template for the specified
                  membership.</p>
                tags:
                  - Update
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
            /collaborations/{collaborationIdentifier}/analysistemplates/{analysisTemplateArn}:
              GET:
                summary: GetCollaborationAnalysisTemplate
                description: <p>Retrieves an analysis template within a collaboration.</p>
                tags:
                  - Get
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /collaborations/{collaborationIdentifier}/configuredaudiencemodelassociations/{configuredAudienceModelAssociationIdentifier}:
              GET:
                summary: GetCollaborationConfiguredAudienceModelAssociation
                description: >-
                  <p>Retrieves a configured audience model association within a
                  collaboration.</p>
                tags:
                  - Get
                  - Collaboration
                  - Configured
                  - Audience
                  - Models
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /collaborations/{collaborationIdentifier}/privacybudgettemplates/{privacyBudgetTemplateIdentifier}:
              GET:
                summary: GetCollaborationPrivacyBudgetTemplate
                description: >-
                  <p>Returns details about a specified privacy budget
                  template.</p>
                tags:
                  - Get
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /memberships/{membershipIdentifier}/protectedQueries/{protectedQueryIdentifier}:
              PATCH:
                summary: UpdateProtectedQuery
                description: <p>Updates the processing of a currently running query.</p>
                tags:
                  - Update
                  - Protected
                  - Queries
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
            /collaborations/{collaborationIdentifier}/schemas/{name}:
              GET:
                summary: GetSchema
                description: >-
                  <p>Retrieves the schema for a relation within a
                  collaboration.</p>
                tags:
                  - Get
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/schemas/{name}/analysisRule/{type}:
              GET:
                summary: GetSchemaAnalysisRule
                description: <p>Retrieves a schema analysis rule.</p>
                tags:
                  - Get
                  - Schemas
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/analysistemplates:
              GET:
                summary: ListCollaborationAnalysisTemplates
                description: <p>Lists analysis templates within a collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/configuredaudiencemodelassociations:
              GET:
                summary: ListCollaborationConfiguredAudienceModelAssociations
                description: >-
                  <p>Lists configured audience model associations within a
                  collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Configured
                  - Audience
                  - Models
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/privacybudgettemplates:
              GET:
                summary: ListCollaborationPrivacyBudgetTemplates
                description: >-
                  <p>Returns an array that summarizes each privacy budget
                  template in a specified collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/privacybudgets:
              GET:
                summary: ListCollaborationPrivacyBudgets
                description: >-
                  <p>Returns an array that summarizes each privacy budget in a
                  specified collaboration. The summary includes the
                  collaboration ARN, creation time, creating account, and
                  privacy budget details.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
            /collaborations/{collaborationIdentifier}/members:
              GET:
                summary: ListMembers
                description: <p>Lists all members within a collaboration.</p>
                tags:
                  - Lists
                  - Members
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/privacybudgets:
              GET:
                summary: ListPrivacyBudgets
                description: >-
                  <p>Returns detailed information about the privacy budgets in a
                  specified membership.</p>
                tags:
                  - Lists
                  - Privacy
                  - Budgets
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/protectedQueries:
              POST:
                summary: StartProtectedQuery
                description: >-
                  <p>Creates a protected query that is started by Clean
                  Rooms.</p>
                tags:
                  - Start
                  - Protected
                  - Queries
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /collaborations/{collaborationIdentifier}/schemas:
              GET:
                summary: ListSchemas
                description: <p>Lists the schemas for relations within a collaboration.</p>
                tags:
                  - Lists
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag or list of tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/previewprivacyimpact:
              POST:
                summary: PreviewPrivacyImpact
                description: >-
                  <p>An estimate of the number of aggregation functions that the
                  member who can query can run given epsilon and noise param
                tags:
                  - Preview
                  - Privacy
                  - Impact
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
                  - Preview Privacy
    overlays:
      - type: APIs.io Search
        url: overlays/cleanrooms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cleanrooms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cleanrooms
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---