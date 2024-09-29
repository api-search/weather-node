---
name: Air
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/air.png
url: https://example.com/apis/air.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Air
apis:
  - name: backup
    description: >-
      <fullname>Backup</fullname> <p>Backup is a unified backup service designed
      to protect Amazon Web Services services and their associated data. Backup
      simplifies the creation, migration, restoration, and deletion of backups,
      while also providing reporting and auditing.</p>
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
            title: backup
          paths:
            /legal-holds/{legalHoldId}:
              DELETE:
                summary: CancelLegalHold
                description: >-
                  <p>This action removes the specified legal hold on a recovery
                  point. This action can only be performed by a user with
                  sufficient permissions.</p>
                tags:
                  - Cancel
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
            /backup/plans/:
              GET:
                summary: ListBackupPlans
                description: >-
                  <p>Returns a list of all active backup plans for an
                  authenticated account. The list contains information such as
                  Amazon Resource Names (ARNs), plan IDs, creation and deletion
                  dates, version IDs, plan names, and creator request IDs.</p>
                tags:
                  - Lists
                  - Backup
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
            /backup/plans/{backupPlanId}/selections/:
              GET:
                summary: ListBackupSelections
                description: >-
                  <p>Returns an array containing metadata of the resources
                  associated with the target backup plan.</p>
                tags:
                  - Lists
                  - Backup
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
            /backup-vaults/{backupVaultName}:
              GET:
                summary: DescribeBackupVault
                description: >-
                  <p>Returns metadata about a backup vault specified by its
                  name.</p>
                tags:
                  - Describe
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
            /audit/frameworks:
              GET:
                summary: ListFrameworks
                description: >-
                  <p>Returns a list of all frameworks for an Amazon Web Services
                  account and Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Frameworks
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
            /legal-holds/:
              GET:
                summary: ListLegalHolds
                description: >-
                  <p>This action returns metadata about active and previous
                  legal holds.</p>
                tags:
                  - Lists
                  - Legal
                  - Holds
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
            /logically-air-gapped-backup-vaults/{backupVaultName}:
              PUT:
                summary: CreateLogicallyAirGappedBackupVault
                description: >-
                  <p>This request creates a logical container to where backups
                  may be copied.</p> <p>This request includes a name, the
                  Region, the maximum number of retention days, the minimum
                  number of retention days, and optionally can include tags and
                  a creator request ID.</p> <note> <p>Do not include sensitive
                  data, such as passport numbers, in the name of a backup
                  vault.</p> </note>
                tags:
                  - Create
                  - Logically
                  - Air
                  - Gapped
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
            /audit/report-plans:
              GET:
                summary: ListReportPlans
                description: >-
                  <p>Returns a list of your report plans. For detailed
                  information about a single report plan, use
                  <code>DescribeReportPlan</code>.</p>
                tags:
                  - Lists
                  - Reports
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
            /restore-testing/plans:
              GET:
                summary: ListRestoreTestingPlans
                description: <p>Returns a list of restore testing plans.</p>
                tags:
                  - Lists
                  - Restore
                  - Testing
                  - Plans
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /restore-testing/plans/{RestoreTestingPlanName}/selections:
              GET:
                summary: ListRestoreTestingSelections
                description: >-
                  <p>Returns a list of restore testing selections. Can be
                  filtered by <code>MaxResults</code> and
                  <code>RestoreTestingPlanName</code>.</p>
                tags:
                  - Lists
                  - Restore
                  - Testing
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /backup/plans/{backupPlanId}:
              POST:
                summary: UpdateBackupPlan
                description: >-
                  <p>Updates an existing backup plan identified by its
                  <code>backupPlanId</code> with the input document in JSON
                  format. The new version is uniquely identified by a
                  <code>VersionId</code>.</p>
                tags:
                  - Update
                  - Backup
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
            /backup/plans/{backupPlanId}/selections/{selectionId}:
              GET:
                summary: GetBackupSelection
                description: >-
                  <p>Returns selection metadata and a document in JSON format
                  that specifies a list of resources that are associated with a
                  backup plan.</p>
                tags:
                  - Get
                  - Backup
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
            /backup-vaults/{backupVaultName}/access-policy:
              PUT:
                summary: PutBackupVaultAccessPolicy
                description: >-
                  <p>Sets a resource-based policy that is used to manage access
                  permissions on the target backup vault. Requires a backup
                  vault name and an access policy document in JSON format.</p>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Access
                  - Policies
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
            /backup-vaults/{backupVaultName}/vault-lock:
              PUT:
                summary: PutBackupVaultLockConfiguration
                description: >-
                  <p>Applies Backup Vault Lock to a backup vault, preventing
                  attempts to delete any recovery point stored in or created in
                  a backup vault. Vault Lock also prevents attempts to update
                  the lifecycle policy that controls the retention period of any
                  recovery point currently stored in a backup vault. If
                  specified, Vault Lock enforces a minimum and maximum retention
                  period for future backup and copy jobs that target a backup
                  vault.</p> <note> <p>Backup Vault Lock has been assessed by
                  Cohasset Associates for use in environments that are subject
                  to SEC 17a-4, CFTC, and FINRA regulations. For more
                  information about how Backup Vault Lock relates to these
                  regulations, see the <a
                  href="samples/cohassetreport.zip">Cohasset Associates
                  Compliance Assessment.</a> </p> </note>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Locks
                  - Configurations
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
            /backup-vaults/{backupVaultName}/notification-configuration:
              PUT:
                summary: PutBackupVaultNotifications
                description: >-
                  <p>Turns on notifications on a backup vault for the specified
                  topic and events.</p>
                tags:
                  - Put
                  - Backup
                  - Vault
                  - Notifications
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
            /audit/frameworks/{frameworkName}:
              PUT:
                summary: UpdateFramework
                description: >-
                  <p>Updates an existing framework identified by its
                  <code>FrameworkName</code> with the input document in JSON
                  format.</p>
                tags:
                  - Update
                  - Frameworks
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}:
              POST:
                summary: UpdateRecoveryPointLifecycle
                description: >-
                  <p>Sets the transition lifecycle of a recovery point.</p>
                  <p>The lifecycle defines when a protected resource is
                  transitioned to cold storage and when it expires. Backup
                  transitions and expires backups automatically according to the
                  lifecycle that you define.</p> <p>Backups transitioned to cold
                  storage must be stored in cold storage for a minimum of 90
                  days. Therefore, the “retention” setting must be 90 days
                  greater than the “transition to cold after days” setting. The
                  “transition to cold after days” setting cannot be changed
                  after a backup has been transitioned to cold.</p> <p>Resource
                  types that are able to be transitioned to cold storage are
                  listed in the "Lifecycle to cold storage" section of the <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html#features-by-resource">
                  Feature availability by resource</a> table. Backup ignores
                  this expression for other resource types.</p> <p>This
                  operation does not support continuous backups.</p>
                tags:
                  - Update
                  - Recovery
                  - Points
                  - Lifecycle
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /audit/report-plans/{reportPlanName}:
              PUT:
                summary: UpdateReportPlan
                description: >-
                  <p>Updates an existing report plan identified by its
                  <code>ReportPlanName</code> with the input document in JSON
                  format.</p>
                tags:
                  - Update
                  - Reports
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /restore-testing/plans/{RestoreTestingPlanName}:
              PUT:
                summary: UpdateRestoreTestingPlan
                description: >-
                  <p>This request will send changes to your specified restore
                  testing plan. <code>RestoreTestingPlanName</code> cannot be
                  updated after it is created.</p> <p>
                  <code>RecoveryPointSelection</code> can contain:</p> <ul> <li>
                  <p> <code>Algorithm</code> </p> </li> <li> <p>
                  <code>ExcludeVaults</code> </p> </li> <li> <p>
                  <code>IncludeVaults</code> </p> </li> <li> <p>
                  <code>RecoveryPointTypes</code> </p> </li> <li> <p>
                  <code>SelectionWindowDays</code> </p> </li> </ul>
                tags:
                  - Update
                  - Restore
                  - Testing
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /restore-testing/plans/{RestoreTestingPlanName}/selections/{RestoreTestingSelectionName}:
              PUT:
                summary: UpdateRestoreTestingSelection
                description: >-
                  <p>Most elements except the
                  <code>RestoreTestingSelectionName</code> can be updated with
                  this request.</p> <p> <code>RestoreTestingSelection</code> can
                  use either protected resource ARNs or conditions, but not
                  both. That is, if your selection has
                  <code>ProtectedResourceArns</code>, requesting an update with
                  the parameter <code>ProtectedResourceConditions</code> will be
                  unsuccessful.</p>
                tags:
                  - Update
                  - Restore
                  - Testing
                  - Selections
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
            /backup-jobs/{backupJobId}:
              POST:
                summary: StopBackupJob
                description: >-
                  <p>Attempts to cancel a job to create a one-time backup of a
                  resource.</p> <p>This action is not supported for the
                  following services: Amazon FSx for Windows File Server, Amazon
                  FSx for Lustre, FSx for ONTAP , Amazon FSx for OpenZFS, Amazon
                  DocumentDB (with MongoDB compatibility), Amazon RDS, Amazon
                  Aurora, and Amazon Neptune.</p>
                tags:
                  - Stop
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
            /copy-jobs/{copyJobId}:
              GET:
                summary: DescribeCopyJob
                description: >-
                  <p>Returns metadata associated with creating a copy of a
                  resource.</p>
                tags:
                  - Describe
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
            /global-settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates whether the Amazon Web Services account is opted in
                  to cross-account backup. Returns an error if the account is
                  not an Organizations management account. Use the
                  <code>DescribeGlobalSettings</code> API to determine the
                  current settings.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
            /resources/{resourceArn}:
              GET:
                summary: DescribeProtectedResource
                description: >-
                  <p>Returns information about a saved resource, including the
                  last time it was backed up, its Amazon Resource Name (ARN),
                  and the Amazon Web Services service type of the saved
                  resource.</p>
                tags:
                  - Describe
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
            /account-settings:
              PUT:
                summary: UpdateRegionSettings
                description: >-
                  <p>Updates the current service opt-in settings for the
                  Region.</p> <p>Use the <code>DescribeRegionSettings</code> API
                  to determine the resource types that are supported.</p>
                tags:
                  - Update
                  - Regions
                  - Settings
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /audit/report-jobs/{reportJobId}:
              GET:
                summary: DescribeReportJob
                description: >-
                  <p>Returns the details associated with creating a report as
                  specified by its <code>ReportJobId</code>.</p>
                tags:
                  - Describe
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /restore-jobs/{restoreJobId}:
              GET:
                summary: DescribeRestoreJob
                description: >-
                  <p>Returns metadata associated with a restore job that is
                  specified by a job ID.</p>
                tags:
                  - Describe
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/disassociate:
              POST:
                summary: DisassociateRecoveryPoint
                description: >-
                  <p>Deletes the specified continuous backup recovery point from
                  Backup and releases control of that continuous backup to the
                  source service, such as Amazon RDS. The source service will
                  continue to create and retain continuous backups using the
                  lifecycle that you specified in your original backup plan.</p>
                  <p>Does not support snapshot backup recovery points.</p>
                tags:
                  - Disassociate
                  - Recovery
                  - Points
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/parentAssociation:
              DELETE:
                summary: DisassociateRecoveryPointFromParent
                description: >-
                  <p>This action to a specific child (nested) recovery point
                  removes the relationship between the specified recovery point
                  and its parent (composite) recovery point.</p>
                tags:
                  - Disassociate
                  - Recovery
                  - Points
                  - From
                  - Parents
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
            /backup/plans/{backupPlanId}/toTemplate/:
              GET:
                summary: ExportBackupPlanTemplate
                description: >-
                  <p>Returns the backup plan that is specified by the plan ID as
                  a backup template.</p>
                tags:
                  - Export
                  - Backup
                  - Plan
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/plans/{backupPlanId}/:
              GET:
                summary: GetBackupPlan
                description: >-
                  <p>Returns <code>BackupPlan</code> details for the specified
                  <code>BackupPlanId</code>. The details are the body of a
                  backup plan in JSON format, in addition to plan metadata.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/template/json/toPlan:
              POST:
                summary: GetBackupPlanFromJSON
                description: >-
                  <p>Returns a valid JSON document specifying a backup plan or
                  an error.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - From
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup/template/plans/{templateId}/toPlan:
              GET:
                summary: GetBackupPlanFromTemplate
                description: >-
                  <p>Returns the template specified by its
                  <code>templateId</code> as a backup plan.</p>
                tags:
                  - Get
                  - Backup
                  - Plan
                  - From
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /legal-holds/{legalHoldId}/:
              GET:
                summary: GetLegalHold
                description: >-
                  <p>This action returns details for a specified legal hold. The
                  details are the body of a legal hold in JSON format, in
                  addition to metadata.</p>
                tags:
                  - Get
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
            /backup-vaults/{backupVaultName}/recovery-points/{recoveryPointArn}/restore-metadata:
              GET:
                summary: GetRecoveryPointRestoreMetadata
                description: >-
                  <p>Returns a set of metadata key-value pairs that were used to
                  create the backup.</p>
                tags:
                  - Get
                  - Recovery
                  - Points
                  - Restore
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
            /restore-jobs/{restoreJobId}/metadata:
              GET:
                summary: GetRestoreJobMetadata
                description: >-
                  <p>This request returns the metadata for the specified restore
                  job.</p>
                tags:
                  - Get
                  - Restore
                  - Jobs
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
            /restore-testing/inferred-metadata:
              GET:
                summary: GetRestoreTestingInferredMetadata
                description: >-
                  <p>This request returns the minimal required set of metadata
                  needed to start a restore job with secure default settings.
                  <code>BackupVaultName</code> and <code>RecoveryPointArn</code>
                  are required parameters. <code>BackupVaultAccountId</code> is
                  an optional parameter.</p>
                tags:
                  - Get
                  - Restore
                  - Testing
                  - Inferred
                  - Metadata
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
            /supported-resource-types:
              GET:
                summary: GetSupportedResourceTypes
                description: >-
                  <p>Returns the Amazon Web Services resource types supported by
                  Backup.</p>
                tags:
                  - Get
                  - Supported
                  - Resources
                  - Types
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
            /audit/backup-job-summaries:
              GET:
                summary: ListBackupJobSummaries
                description: >-
                  <p>This is a request for a summary of backup jobs created or
                  running within the most recent 30 days. You can include
                  parameters AccountID, State, ResourceType, MessageCategory,
                  AggregationPeriod, MaxResults, or NextToken to filter
                  results.</p> <p>This request returns a summary that contains
                  Region, Account, State, ResourceType, MessageCategory,
                  StartTime, EndTime, and Count of included jobs.</p>
                tags:
                  - Lists
                  - Backup
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
            /backup-jobs/:
              GET:
                summary: ListBackupJobs
                description: >-
                  <p>Returns a list of existing backup jobs for an authenticated
                  account for the last 30 days. For a longer period of time,
                  consider using these <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/monitoring.html">monitoring
                  tools</a>.</p>
                tags:
                  - Lists
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
            /backup/template/plans:
              GET:
                summary: ListBackupPlanTemplates
                description: >-
                  <p>Returns metadata of your saved backup plan templates,
                  including the template ID, name, and the creation and deletion
                  dates.</p>
                tags:
                  - Lists
                  - Backup
                  - Plan
                  - Templates
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
            /backup/plans/{backupPlanId}/versions/:
              GET:
                summary: ListBackupPlanVersions
                description: >-
                  <p>Returns version metadata of your backup plans, including
                  Amazon Resource Names (ARNs), backup plan IDs, creation and
                  deletion dates, plan names, and version IDs.</p>
                tags:
                  - Lists
                  - Backup
                  - Plan
                  - Versions
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
            /backup-vaults/:
              GET:
                summary: ListBackupVaults
                description: >-
                  <p>Returns a list of recovery point storage containers along
                  with information about them.</p>
                tags:
                  - Lists
                  - Backup
                  - Vaults
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
            /audit/copy-job-summaries:
              GET:
                summary: ListCopyJobSummaries
                description: >-
                  <p>This request obtains a list of copy jobs created or running
                  within the the most recent 30 days. You can include parameters
                  AccountID, State, ResourceType, MessageCategory,
                  AggregationPeriod, MaxResults, or NextToken to filter
                  results.</p> <p>This request returns a summary that contains
                  Region, Account, State, RestourceType, MessageCategory,
                  StartTime, EndTime, and Count of included jobs.</p>
                tags:
                  - Lists
                  - Copy
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
            /copy-jobs/:
              GET:
                summary: ListCopyJobs
                description: <p>Returns metadata about your copy jobs.</p>
                tags:
                  - Lists
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
            /resources/:
              GET:
                summary: ListProtectedResources
                description: >-
                  <p>Returns an array of resources successfully backed up by
                  Backup, including the time the resource was saved, an Amazon
                  Resource Name (ARN) of the resource, and a resource type.</p>
                tags:
                  - Lists
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /backup-vaults/{backupVaultName}/resources/:
              GET:
                summary: ListProtectedResourcesByBackupVault
                description: >-
                  <p>This request lists the protected resources corresponding to
                  each backup vault.</p>
                tags:
                  - Lists
                  - Protected
                  - Resources
                  - By
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /backup-vaults/{backupVaultName}/recovery-points/:
              GET:
                summary: ListRecoveryPointsByBackupVault
                description: >-
                  <p>Returns detailed information about the recovery points
                  stored in a backup vault.</p>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Backup
                  - Vault
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /legal-holds/{legalHoldId}/recovery-points:
              GET:
                summary: ListRecoveryPointsByLegalHold
                description: >-
                  <p>This action returns recovery point ARNs (Amazon Resource
                  Names) of the specified legal hold.</p>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Legal
                  - Hold
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /resources/{resourceArn}/recovery-points/:
              GET:
                summary: ListRecoveryPointsByResource
                description: >-
                  <p>Returns detailed information about all the recovery points
                  of the type specified by a resource Amazon Resource Name
                  (ARN).</p> <note> <p>For Amazon EFS and Amazon EC2, this
                  action only lists recovery points created by Backup.</p>
                  </note>
                tags:
                  - Lists
                  - Recovery
                  - Points
                  - By
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /audit/report-jobs:
              GET:
                summary: ListReportJobs
                description: <p>Returns details about your report jobs.</p>
                tags:
                  - Lists
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /audit/restore-job-summaries:
              GET:
                summary: ListRestoreJobSummaries
                description: >-
                  <p>This request obtains a summary of restore jobs created or
                  running within the the most recent 30 days. You can include
                  parameters AccountID, State, ResourceType, AggregationPeriod,
                  MaxResults, or NextToken to filter results.</p> <p>This
                  request returns a summary that contains Region, Account,
                  State, RestourceType, MessageCategory, StartTime, EndTime, and
                  Count of included jobs.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - Summaries
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /restore-jobs/:
              GET:
                summary: ListRestoreJobs
                description: >-
                  <p>Returns a list of jobs that Backup initiated to restore a
                  saved resource, including details about the recovery
                  process.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /resources/{resourceArn}/restore-jobs/:
              GET:
                summary: ListRestoreJobsByProtectedResource
                description: >-
                  <p>This returns restore jobs that contain the specified
                  protected resource.</p> <p>You must include
                  <code>ResourceArn</code>. You can optionally include
                  <code>NextToken</code>, <code>ByStatus</code>,
                  <code>MaxResults</code>,
                  <code>ByRecoveryPointCreationDateAfter</code> , and
                  <code>ByRecoveryPointCreationDateBefore</code>.</p>
                tags:
                  - Lists
                  - Restore
                  - Jobs
                  - By
                  - Protected
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /tags/{resourceArn}/:
              GET:
                summary: ListTags
                description: >-
                  <p>Returns a list of key-value pairs assigned to a target
                  recovery point, backup plan, or backup vault.</p> <p>
                  <code>ListTags</code> only works for resource types that
                  support full Backup management of their backups. Those
                  resource types are listed in the "Full Backup management"
                  section of the <a
                  href="https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html#features-by-resource">
                  Feature availability by resource</a> table.</p>
                tags:
                  - Lists
                  - Tags
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
            /restore-jobs/{restoreJobId}/validations:
              PUT:
                summary: PutRestoreValidationResult
                description: >-
                  <p>This request allows you to send your independent self-run
                  restore test validation results. <code>RestoreJobId</code> and
                  <code>ValidationStatus</code> are required. Optionally, you
                  can input a <code>ValidationStatusMessage</code>.</p>
                tags:
                  - Put
                  - Restore
                  - Validations
                  - Results
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /backup-jobs:
              PUT:
                summary: StartBackupJob
                description: >-
                  <p>Starts an on-demand backup job for the specified
                  resource.</p>
                tags:
                  - Start
                  - Backup
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /copy-jobs:
              PUT:
                summary: StartCopyJob
                description: >-
                  <p>Starts a job to create a one-time copy of the specified
                  resource.</p> <p>Does not support continuous backups.</p>
                tags:
                  - Start
                  - Copy
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /audit/report-jobs/{reportPlanName}:
              POST:
                summary: StartReportJob
                description: >-
                  <p>Starts an on-demand report job for the specified report
                  plan.</p>
                tags:
                  - Start
                  - Reports
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /restore-jobs:
              PUT:
                summary: StartRestoreJob
                description: >-
                  <p>Recovers the saved resource identified by an Amazon
                  Resource Name (ARN).</p>
                tags:
                  - Start
                  - Restore
                  - Jobs
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /tags/{resourceArn}:
              POST:
                summary: TagResource
                description: >-
                  <p>Assigns a set of key-value pairs to a recovery point,
                  backup plan, or backup vault identified by an Amazon Resource
                  Name (ARN).</p>
                tags:
                  - Tags
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
            /untag/{resourceArn}:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes a set of key-value pairs from a recovery point,
                  backup plan, or backup vault identified by an Amazon Resource
                  Name
                tags:
                  - Untag
                  - Resources
                  - Hold
                  - Identifiers
                  - Backup
                  - Plans
                  - Plan
                  - Selections
                  - Vault
                  - Names
                  - Audit
                  - Frameworks
                  - Legal
                  - Holds
                  - Reports
                  - Restore
                  - Testing
                  - Selections
                  - Access
                  - Policies
                  - Locks
                  - Notifications
                  - Configurations
                  - Recovery
                  - Points
                  - Points
                  - ARN
                  - Jobs
                  - Global
                  - Settings
                  - Account
                  - Disassociate
                  - Parents
                  - Association
                  - To
                  - Templates
                  - Metadata
                  - Inferred
                  - Supported
                  - Resources
                  - Types
                  - Summaries
                  - Jobs
                  - Versions
                  - Vaults
                  - Copy
                  - Resources
                  - Validations
    overlays:
      - type: APIs.io Search
        url: overlays/backup-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/backup-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:backup
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---