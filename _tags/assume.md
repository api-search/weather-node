---
name: Assume
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/assume.png
url: https://example.com/apis/assume.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Assume
apis:
  - name: eks-auth
    description: >-
      <p>The Amazon EKS Auth API and the <code>AssumeRoleForPodIdentity</code>
      action are only used by the EKS Pod Identity Agent.</p>
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
            title: eks-auth
          paths:
            /clusters/{clusterName}/assume-role-for-pod-identity:
              POST:
                summary: AssumeRoleForPodIdentity
                description: >-
                  <p>The Amazon EKS Auth API and the
                  <code>AssumeRoleForPodIdentity</code> action are only used by
                  the EKS Pod Identity Agent.</p> <p>We recommend that
                  applications use the Amazon Web Services SDKs to connect to
                  Amazon Web Services services; if credentials from an EKS Pod
                  Identity association are available in the pod, the latest
                  versions of the SDKs use them automati
                tags:
                  - Assume
                  - Roles
                  - For
                  - Pods
                  - Identity
                  - Names
                  - Assume
                  - Roles
                  - For
                  - Pods
                  - Identi
    overlays:
      - type: APIs.io Search
        url: overlays/eks-auth-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/eks-auth-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:eks-auth
  - name: lakeformation
    description: >-
      <fullname>Lake Formation</fullname> <p>Defines the public endpoint for the
      Lake Formation service.</p>
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
            title: lakeformation
          paths:
            /AddLFTagsToResource:
              POST:
                summary: AddLFTagsToResource
                description: <p>Attaches one or more LF-tags to an existing resource.</p>
                tags:
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
            /AssumeDecoratedRoleWithSAML:
              POST:
                summary: AssumeDecoratedRoleWithSAML
                description: >-
                  <p>Allows a caller to assume an IAM role decorated as the SAML
                  user specified in the SAML assertion included in the request.
                  This decoration allows Lake Formation to enforce access
                  policies against the SAML users and groups. This API operation
                  requires SAML federation setup in the caller’s account as it
                  can only be called with valid SAML assertions. Lake Formation
                  does not scope down the permission of the assumed role. All
                  permissions attached to the role via the SAML federation setup
                  will be included in the role session. </p> <p> This decorated
                  role is expected to access data in Amazon S3 by getting
                  temporary access from Lake Formation which is authorized via
                  the virtual API <code>GetDataAccess</code>. Therefore, all
                  SAML roles that can be assumed via
                  <code>AssumeDecoratedRoleWithSAML</code> must at a minimum
                  include <code>lakeformation:GetDataAccess</code> in their role
                  policies. A typical IAM policy attached to such a role would
                  look as follows: </p>
                tags:
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
            /BatchGrantPermissions:
              POST:
                summary: BatchGrantPermissions
                description: <p>Batch operation to grant permissions to the principal.</p>
                tags:
                  - Batches
                  - Grant
                  - Permissions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
            /BatchRevokePermissions:
              POST:
                summary: BatchRevokePermissions
                description: >-
                  <p>Batch operation to revoke permissions from the
                  principal.</p>
                tags:
                  - Batches
                  - Revoke
                  - Permissions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
            /CancelTransaction:
              POST:
                summary: CancelTransaction
                description: >-
                  <p>Attempts to cancel the specified transaction. Returns an
                  exception if the transaction was previously committed.</p>
                tags:
                  - Cancel
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
            /CommitTransaction:
              POST:
                summary: CommitTransaction
                description: >-
                  <p>Attempts to commit the specified transaction. Returns an
                  exception if the transaction was previously aborted. This API
                  action is idempotent if called multiple times for the same
                  transaction.</p>
                tags:
                  - Commit
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
            /CreateDataCellsFilter:
              POST:
                summary: CreateDataCellsFilter
                description: >-
                  <p>Creates a data cell filter to allow one to grant access to
                  certain columns on certain rows.</p>
                tags:
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
            /CreateLFTag:
              POST:
                summary: CreateLFTag
                description: <p>Creates an LF-tag with the specified name and values.</p>
                tags:
                  - Create
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
            /CreateLakeFormationIdentityCenterConfiguration:
              POST:
                summary: CreateLakeFormationIdentityCenterConfiguration
                description: >-
                  <p>Creates an IAM Identity Center connection with Lake
                  Formation to allow IAM Identity Center users and groups to
                  access Data Catalog resources.</p>
                tags:
                  - Create
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
            /CreateLakeFormationOptIn:
              POST:
                summary: CreateLakeFormationOptIn
                description: >-
                  <p>Enforce Lake Formation permissions for the given databases,
                  tables, and principals.</p>
                tags:
                  - Create
                  - Lakes
                  - Formation
                  - Opt
                  - In
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
            /DeleteDataCellsFilter:
              POST:
                summary: DeleteDataCellsFilter
                description: <p>Deletes a data cell filter.</p>
                tags:
                  - Delete
                  - Data
                  - Cells
                  - Filter
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
            /DeleteLFTag:
              POST:
                summary: DeleteLFTag
                description: >-
                  <p>Deletes the specified LF-tag given a key name. If the input
                  parameter tag key was not found, then the operation will throw
                  an exception. When you delete an LF-tag, the
                  <code>LFTagPolicy</code> attached to the LF-tag becomes
                  invalid. If the deleted LF-tag was still assigned to any
                  resource, the tag policy attach to the deleted LF-tag will no
                  longer be applied to the resource.</p>
                tags:
                  - Delete
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
            /DeleteLakeFormationIdentityCenterConfiguration:
              POST:
                summary: DeleteLakeFormationIdentityCenterConfiguration
                description: >-
                  <p>Deletes an IAM Identity Center connection with Lake
                  Formation.</p>
                tags:
                  - Delete
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
            /DeleteLakeFormationOptIn:
              POST:
                summary: DeleteLakeFormationOptIn
                description: >-
                  <p>Remove the Lake Formation permissions enforcement of the
                  given databases, tables, and principals.</p>
                tags:
                  - Delete
                  - Lakes
                  - Formation
                  - Opt
                  - In
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
            /DeleteObjectsOnCancel:
              POST:
                summary: DeleteObjectsOnCancel
                description: >-
                  <p>For a specific governed table, provides a list of Amazon S3
                  objects that will be written during the current transaction
                  and that can be automatically deleted if the transaction is
                  canceled. Without this call, no Amazon S3 objects are
                  automatically deleted when a transaction cancels. </p> <p> The
                  Glue ETL library function
                  <code>write_dynamic_frame.from_catalog()</code> includes an
                  option to automatically call
                  <code>DeleteObjectsOnCancel</code> before writes. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/lake-formation/latest/dg/transactions-data-operations.html#rolling-back-writes">Rolling
                  Back Amazon S3 Writes</a>. </p>
                tags:
                  - Delete
                  - Objects
                  - 'On'
                  - Cancel
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
            /DeregisterResource:
              POST:
                summary: DeregisterResource
                description: >-
                  <p>Deregisters the resource as managed by the Data
                  Catalog.</p> <p>When you deregister a path, Lake Formation
                  removes the path from the inline policy attached to your
                  service-linked role.</p>
                tags:
                  - Deregister
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
            /DescribeLakeFormationIdentityCenterConfiguration:
              POST:
                summary: DescribeLakeFormationIdentityCenterConfiguration
                description: >-
                  <p>Retrieves the instance ARN and application ARN for the
                  connection.</p>
                tags:
                  - Describe
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
            /DescribeResource:
              POST:
                summary: DescribeResource
                description: >-
                  <p>Retrieves the current data access role for the given
                  resource registered in Lake Formation.</p>
                tags:
                  - Describe
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
            /DescribeTransaction:
              POST:
                summary: DescribeTransaction
                description: <p>Returns the details of a single transaction.</p>
                tags:
                  - Describe
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
            /ExtendTransaction:
              POST:
                summary: ExtendTransaction
                description: >-
                  <p>Indicates to the service that the specified transaction is
                  still active and should not be treated as idle and
                  aborted.</p> <p>Write transactions that remain idle for a long
                  period are automatically aborted unless explicitly
                  extended.</p>
                tags:
                  - Extend
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
            /GetDataCellsFilter:
              POST:
                summary: GetDataCellsFilter
                description: <p>Returns a data cells filter.</p>
                tags:
                  - Get
                  - Data
                  - Cells
                  - Filter
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
            /GetDataLakeSettings:
              POST:
                summary: GetDataLakeSettings
                description: >-
                  <p>Retrieves the list of the data lake administrators of a
                  Lake Formation-managed data lake. </p>
                tags:
                  - Get
                  - Data
                  - Lakes
                  - Settings
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
            /GetEffectivePermissionsForPath:
              POST:
                summary: GetEffectivePermissionsForPath
                description: >-
                  <p>Returns the Lake Formation permissions for a specified
                  table or database resource located at a path in Amazon S3.
                  <code>GetEffectivePermissionsForPath</code> will not return
                  databases and tables if the catalog is encrypted.</p>
                tags:
                  - Get
                  - Effective
                  - Permissions
                  - For
                  - Paths
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
            /GetLFTag:
              POST:
                summary: GetLFTag
                description: <p>Returns an LF-tag definition.</p>
                tags:
                  - Get
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
            /GetQueryState:
              POST:
                summary: GetQueryState
                description: >-
                  <p>Returns the state of a query previously submitted. Clients
                  are expected to poll <code>GetQueryState</code> to monitor the
                  current state of the planning before retrieving the work
                  units. A query state is only visible to the principal that
                  made the initial call to <code>StartQueryPlanning</code>.</p>
                tags:
                  - Get
                  - Queries
                  - States
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
            /GetQueryStatistics:
              POST:
                summary: GetQueryStatistics
                description: >-
                  <p>Retrieves statistics on the planning and execution of a
                  query.</p>
                tags:
                  - Get
                  - Queries
                  - Statistics
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
            /GetResourceLFTags:
              POST:
                summary: GetResourceLFTags
                description: <p>Returns the LF-tags applied to a resource.</p>
                tags:
                  - Get
                  - Resources
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
            /GetTableObjects:
              POST:
                summary: GetTableObjects
                description: >-
                  <p>Returns the set of Amazon S3 objects that make up the
                  specified governed table. A transaction ID or timestamp can be
                  specified for time-travel queries.</p>
                tags:
                  - Get
                  - Tables
                  - Objects
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
            /GetTemporaryGluePartitionCredentials:
              POST:
                summary: GetTemporaryGluePartitionCredentials
                description: >-
                  <p>This API is identical to
                  <code>GetTemporaryTableCredentials</code> except that this is
                  used when the target Data Catalog resource is of type
                  Partition. Lake Formation restricts the permission of the
                  vended credentials with the same scope down policy which
                  restricts access to a single Amazon S3 prefix.</p>
                tags:
                  - Get
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
            /GetTemporaryGlueTableCredentials:
              POST:
                summary: GetTemporaryGlueTableCredentials
                description: >-
                  <p>Allows a caller in a secure environment to assume a role
                  with permission to access Amazon S3. In order to vend such
                  credentials, Lake Formation assumes the role associated with a
                  registered location, for example an Amazon S3 bucket, with a
                  scope down policy which restricts the access to a single
                  prefix.</p>
                tags:
                  - Get
                  - Temporary
                  - Glue
                  - Tables
                  - Credentials
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
            /GetWorkUnitResults:
              POST:
                summary: GetWorkUnitResults
                description: >-
                  <p>Returns the work units resulting from the query. Work units
                  can be executed in any order and in parallel. </p>
                tags:
                  - Get
                  - Work
                  - Units
                  - Results
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
            /GetWorkUnits:
              POST:
                summary: GetWorkUnits
                description: >-
                  <p>Retrieves the work units generated by the
                  <code>StartQueryPlanning</code> operation.</p>
                tags:
                  - Get
                  - Work
                  - Units
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
            /GrantPermissions:
              POST:
                summary: GrantPermissions
                description: >-
                  <p>Grants permissions to the principal to access metadata in
                  the Data Catalog and data organized in underlying data storage
                  such as Amazon S3.</p> <p>For information about permissions,
                  see <a
                  href="https://docs.aws.amazon.com/lake-formation/latest/dg/security-data-access.html">Security
                  and Access Control to Metadata and Data</a>.</p>
                tags:
                  - Grant
                  - Permissions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
            /ListDataCellsFilter:
              POST:
                summary: ListDataCellsFilter
                description: <p>Lists all the data cell filters on a table.</p>
                tags:
                  - Lists
                  - Data
                  - Cells
                  - Filter
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
            /ListLFTags:
              POST:
                summary: ListLFTags
                description: >-
                  <p>Lists LF-tags that the requester has permission to view.
                  </p>
                tags:
                  - Lists
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
            /ListLakeFormationOptIns:
              POST:
                summary: ListLakeFormationOptIns
                description: >-
                  <p>Retrieve the current list of resources and principals that
                  are opt in to enforce Lake Formation permissions.</p>
                tags:
                  - Lists
                  - Lakes
                  - Formation
                  - Opt
                  - Ins
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
            /ListPermissions:
              POST:
                summary: ListPermissions
                description: >-
                  <p>Returns a list of the principal permissions on the
                  resource, filtered by the permissions of the caller. For
                  example, if you are granted an ALTER permission, you are able
                  to see only the principal permissions for ALTER.</p> <p>This
                  operation returns only those permissions that have been
                  explicitly granted.</p> <p>For information about permissions,
                  see <a
                  href="https://docs.aws.amazon.com/lake-formation/latest/dg/security-data-access.html">Security
                  and Access Control to Metadata and Data</a>.</p>
                tags:
                  - Lists
                  - Permissions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
            /ListResources:
              POST:
                summary: ListResources
                description: >-
                  <p>Lists the resources registered to be managed by the Data
                  Catalog.</p>
                tags:
                  - Lists
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
            /ListTableStorageOptimizers:
              POST:
                summary: ListTableStorageOptimizers
                description: >-
                  <p>Returns the configuration of all storage optimizers
                  associated with a specified table.</p>
                tags:
                  - Lists
                  - Tables
                  - Storage
                  - Optimizers
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
            /ListTransactions:
              POST:
                summary: ListTransactions
                description: >-
                  <p>Returns metadata about transactions and their status. To
                  prevent the response from growing indefinitely, only
                  uncommitted transactions and those available for time-travel
                  queries are returned.</p> <p>This operation can help you
                  identify uncommitted transactions or to get information about
                  transactions.</p>
                tags:
                  - Lists
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
            /PutDataLakeSettings:
              POST:
                summary: PutDataLakeSettings
                description: >-
                  <p>Sets the list of data lake administrators who have admin
                  privileges on all resources managed by Lake Formation. For
                  more information on admin privileges, see <a
                  href="https://docs.aws.amazon.com/lake-formation/latest/dg/lake-formation-permissions.html">Granting
                  Lake Formation Permissions</a>.</p> <p>This API replaces the
                  current list of data lake admins with the new list being
                  passed. To add an admin, fetch the current list and add the
                  new admin to that list and pass that list in this API.</p>
                tags:
                  - Put
                  - Data
                  - Lakes
                  - Settings
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
            /RegisterResource:
              POST:
                summary: RegisterResource
                description: >-
                  <p>Registers the resource as managed by the Data Catalog.</p>
                  <p>To add or update data, Lake Formation needs read/write
                  access to the chosen Amazon S3 path. Choose a role that you
                  know has permission to do this, or choose the
                  AWSServiceRoleForLakeFormationDataAccess service-linked role.
                  When you register the first Amazon S3 path, the service-linked
                  role and a new inline policy are created on your behalf. Lake
                  Formation adds the first path to the inline policy and
                  attaches it to the service-linked role. When you register
                  subsequent paths, Lake Formation adds the path to the existing
                  policy.</p> <p>The following request registers a new location
                  and gives Lake Formation permission to use the service-linked
                  role to access that location.</p> <p> <code>ResourceArn =
                  arn:aws:s3:::my-bucket UseServiceLinkedRole = true</code> </p>
                  <p>If <code>UseServiceLinkedRole</code> is not set to true,
                  you must provide or set the <code>RoleArn</code>:</p> <p>
                  <code>arn:aws:iam::12345:role/my-data-access-role</code> </p>
                tags:
                  - Register
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
            /RemoveLFTagsFromResource:
              POST:
                summary: RemoveLFTagsFromResource
                description: >-
                  <p>Removes an LF-tag from the resource. Only database, table,
                  or tableWithColumns resource are allowed. To tag columns, use
                  the column inclusion list in <code>tableWithColumns</code> to
                  specify column input.</p>
                tags:
                  - Removes
                  - Tags
                  - From
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
            /RevokePermissions:
              POST:
                summary: RevokePermissions
                description: >-
                  <p>Revokes permissions to the principal to access metadata in
                  the Data Catalog and data organized in underlying data storage
                  such as Amazon S3.</p>
                tags:
                  - Revoke
                  - Permissions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
            /SearchDatabasesByLFTags:
              POST:
                summary: SearchDatabasesByLFTags
                description: >-
                  <p>This operation allows a search on <code>DATABASE</code>
                  resources by <code>TagCondition</code>. This operation is used
                  by admins who want to grant user permissions on certain
                  <code>TagConditions</code>. Before making a grant, the admin
                  can use <code>SearchDatabasesByTags</code> to find all
                  resources where the given <code>TagConditions</code> are valid
                  to verify whether the returned resources can be shared.</p>
                tags:
                  - Search
                  - Databases
                  - By
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
            /SearchTablesByLFTags:
              POST:
                summary: SearchTablesByLFTags
                description: >-
                  <p>This operation allows a search on <code>TABLE</code>
                  resources by <code>LFTag</code>s. This will be used by admins
                  who want to grant user permissions on certain LF-tags. Before
                  making a grant, the admin can use
                  <code>SearchTablesByLFTags</code> to find all resources where
                  the given <code>LFTag</code>s are valid to verify whether the
                  returned resources can be shared.</p>
                tags:
                  - Search
                  - Tables
                  - By
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
            /StartQueryPlanning:
              POST:
                summary: StartQueryPlanning
                description: >-
                  <p>Submits a request to process a query statement.</p> <p>This
                  operation generates work units that can be retrieved with the
                  <code>GetWorkUnits</code> operation as soon as the query state
                  is WORKUNITS_AVAILABLE or FINISHED.</p>
                tags:
                  - Start
                  - Queries
                  - Planning
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
            /StartTransaction:
              POST:
                summary: StartTransaction
                description: >-
                  <p>Starts a new transaction and returns its transaction ID.
                  Transaction IDs are opaque objects that you can use to
                  identify a transaction.</p>
                tags:
                  - Start
                  - Transactions
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
            /UpdateDataCellsFilter:
              POST:
                summary: UpdateDataCellsFilter
                description: <p>Updates a data cell filter.</p>
                tags:
                  - Update
                  - Data
                  - Cells
                  - Filter
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
            /UpdateLFTag:
              POST:
                summary: UpdateLFTag
                description: >-
                  <p>Updates the list of possible values for the specified
                  LF-tag key. If the LF-tag does not exist, the operation throws
                  an EntityNotFoundException. The values in the delete key
                  values will be deleted from list of possible values. If any
                  value in the delete key values is attached to a resource, then
                  API errors out with a 400 Exception - "Update not allowed".
                  Untag the attribute before deleting the LF-tag key's value.
                  </p>
                tags:
                  - Update
                  - Tags
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
            /UpdateLakeFormationIdentityCenterConfiguration:
              POST:
                summary: UpdateLakeFormationIdentityCenterConfiguration
                description: <p>Updates the IAM Identity Center connection parameters.</p>
                tags:
                  - Update
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
            /UpdateResource:
              POST:
                summary: UpdateResource
                description: >-
                  <p>Updates the data access role used for vending access to the
                  given (registered) resource in Lake Formation. </p>
                tags:
                  - Update
                  - Resources
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
            /UpdateTableObjects:
              POST:
                summary: UpdateTableObjects
                description: >-
                  <p>Updates the manifest of Amazon S3 objects that make up the
                  specified governed table.</p>
                tags:
                  - Update
                  - Tables
                  - Objects
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
            /UpdateTableStorageOptimizer:
              POST:
                summary: UpdateTableStorageOptimizer
                description: <p>Updates the configuration of the storage optimizers for a
                tags:
                  - Update
                  - Tables
                  - Storage
                  - Optimizers
                  - Add
                  - Tags
                  - To
                  - Resources
                  - Assume
                  - Decorated
                  - Roles
                  - With
                  - Batches
                  - Grant
                  - Permissions
                  - Revoke
                  - Cancel
                  - Transactions
                  - Commit
                  - Create
                  - Data
                  - Cells
                  - Filter
                  - Tags
                  - Lakes
                  - Formation
                  - Identity
                  - Center
                  - Configurations
                  - Opt
                  - In
                  - Delete
                  - Objects
                  - 'On'
                  - Deregister
                  - Describe
                  - Extend
                  - Get
                  - Settings
                  - Effective
                  - For
                  - Paths
                  - Queries
                  - States
                  - Statistics
                  - Tables
                  - Temporary
                  - Glue
                  - Partition
                  - Credentials
                  - Work
                  - Units
                  - Results
                  - Units
                  - Lists
                  - Ins
                  - Resources
                  - Storage
                  - Optimizers
                  - Transactions
                  - Put
                  - Register
                  - Removes
                  - From
                  - Search
                  - Databases
                  - By
                  - Tables
                  - Start
                  - Planning
                  - Update
                  - Optimizations
    overlays:
      - type: APIs.io Search
        url: overlays/lakeformation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lakeformation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lakeformation
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---