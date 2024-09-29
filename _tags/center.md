---
name: Center
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/center.png
url: https://example.com/apis/center.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Center
apis:
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---