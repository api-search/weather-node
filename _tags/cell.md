---
name: Cell
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cell.png
url: https://example.com/apis/cell.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cell
apis:
  - name: route53-recovery-readiness
    description: <p>Recovery readiness</p>
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
            title: route53-recovery-readiness
          paths:
            /cells:
              GET:
                summary: ListCells
                description: <p>Lists the cells for an account.</p>
                tags:
                  - Lists
                  - Cells
                  - Cells
            /crossaccountauthorizations:
              GET:
                summary: ListCrossAccountAuthorizations
                description: >-
                  <p>Lists the cross-account readiness authorizations that are
                  in place for an account.</p>
                tags:
                  - Lists
                  - Cross
                  - Account
                  - Authorization
                  - Cells
                  - Cross Account Authorizations
            /readinesschecks:
              GET:
                summary: ListReadinessChecks
                description: <p>Lists the readiness checks for an account.</p>
                tags:
                  - Lists
                  - Readiness
                  - Checks
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
            /recoverygroups:
              GET:
                summary: ListRecoveryGroups
                description: <p>Lists the recovery groups in an account.</p>
                tags:
                  - Lists
                  - Recovery
                  - Groups
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
            /resourcesets:
              GET:
                summary: ListResourceSets
                description: <p>Lists the resource sets in an account.</p>
                tags:
                  - Lists
                  - Resources
                  - Sets
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
            /cells/{cellName}:
              PUT:
                summary: UpdateCell
                description: >-
                  <p>Updates a cell to replace the list of nested cells with a
                  new list of nested cells.</p>
                tags:
                  - Update
                  - Cell
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
            /crossaccountauthorizations/{crossAccountAuthorization}:
              DELETE:
                summary: DeleteCrossAccountAuthorization
                description: <p>Deletes cross account readiness authorization.</p>
                tags:
                  - Delete
                  - Cross
                  - Account
                  - Authorization
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
            /readinesschecks/{readinessCheckName}:
              PUT:
                summary: UpdateReadinessCheck
                description: <p>Updates a readiness check.</p>
                tags:
                  - Update
                  - Readiness
                  - Checks
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
            /recoverygroups/{recoveryGroupName}:
              PUT:
                summary: UpdateRecoveryGroup
                description: <p>Updates a recovery group.</p>
                tags:
                  - Update
                  - Recovery
                  - Group
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
            /resourcesets/{resourceSetName}:
              PUT:
                summary: UpdateResourceSet
                description: <p>Updates a resource set.</p>
                tags:
                  - Update
                  - Resources
                  - Sets
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
            /recoverygroups/{recoveryGroupName}/architectureRecommendations:
              GET:
                summary: GetArchitectureRecommendations
                description: >-
                  <p>Gets recommendations about architecture designs for
                  improving resiliency for an application, based on a recovery
                  group.</p>
                tags:
                  - Get
                  - Architecture
                  - Recommendations
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
            /cellreadiness/{cellName}:
              GET:
                summary: GetCellReadinessSummary
                description: >-
                  <p>Gets readiness for a cell. Aggregates the readiness of all
                  the resources that are associated with the cell into a single
                  value.</p>
                tags:
                  - Get
                  - Cell
                  - Readiness
                  - Summaries
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
            /readinesschecks/{readinessCheckName}/resource/{resourceIdentifier}/status:
              GET:
                summary: GetReadinessCheckResourceStatus
                description: >-
                  <p>Gets individual readiness status for a readiness check. To
                  see the overall readiness status for a recovery group, that
                  considers the readiness status for all the readiness checks in
                  the recovery group, use GetRecoveryGroupReadinessSummary.</p>
                tags:
                  - Get
                  - Readiness
                  - Checks
                  - Resources
                  - Status
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
                  - Resources
                  - Identifiers
                  - Status
            /readinesschecks/{readinessCheckName}/status:
              GET:
                summary: GetReadinessCheckStatus
                description: >-
                  <p>Gets the readiness status for an individual readiness
                  check. To see the overall readiness status for a recovery
                  group, that considers the readiness status for all the
                  readiness checks in a recovery group, use
                  GetRecoveryGroupReadinessSummary.</p>
                tags:
                  - Get
                  - Readiness
                  - Checks
                  - Status
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
                  - Resources
                  - Identifiers
                  - Status
            /recoverygroupreadiness/{recoveryGroupName}:
              GET:
                summary: GetRecoveryGroupReadinessSummary
                description: >-
                  <p>Displays a summary of information about a recovery group's
                  readiness status. Includes the readiness checks for resources
                  in the recovery group and the readiness status of each
                  one.</p>
                tags:
                  - Get
                  - Recovery
                  - Group
                  - Readiness
                  - Summaries
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
                  - Resources
                  - Identifiers
                  - Status
            /rules:
              GET:
                summary: ListRules
                description: >-
                  <p>Lists all readiness rules, or lists the readiness rules for
                  a specific resource type.</p>
                tags:
                  - Lists
                  - Rules
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
                  - Resources
                  - Identifiers
                  - Status
                  - Rules
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from a res
                tags:
                  - Untag
                  - Resources
                  - Cells
                  - Cross Account Authorizations
                  - Readiness Checks
                  - Recovery Groups
                  - Resource Sets
                  - Names
                  - Account
                  - Authorization
                  - Checks
                  - Group
                  - Sets
                  - Architecture
                  - Recommendations
                  - Resources
                  - Identifiers
                  - Status
                  - Rules
                  - Tags
                  - A
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-readiness-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-recovery-readiness-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-readiness
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---