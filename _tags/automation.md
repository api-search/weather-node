---
name: Automation
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/automation.png
url: https://example.com/apis/automation.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Automation
apis:
  - name: honeycode
    description: >-
      <p> Amazon Honeycode is a fully managed service that allows you to quickly
      build mobile and web apps for teams—without programming. Build Honeycode
      apps for managing almost anything, like projects, customers, operations,
      approvals, resources, and even your team. </p>
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
            title: honeycode
          paths:
            /workbooks/{workbookId}/tables/{tableId}/rows/batchcreate:
              POST:
                summary: BatchCreateTableRows
                description: >-
                  <p> The BatchCreateTableRows API allows you to create one or
                  more rows at the end of a table in a workbook. The API allows
                  you to specify the values to set in some or all of the columns
                  in the new rows. </p> <p> If a column is not explicitly set in
                  a specific row, then the column level formula specified in the
                  table will be applied to the new row. If there is no column
                  level formula but the last row of the table has a formula,
                  then that formula will be copied down to the new row. If there
                  is no column level formula and no formula in the last row of
                  the table, then that column will be left blank for the new
                  rows. </p>
                tags:
                  - Batches
                  - Create
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchdelete:
              POST:
                summary: BatchDeleteTableRows
                description: >-
                  <p> The BatchDeleteTableRows API allows you to delete one or
                  more rows from a table in a workbook. You need to specify the
                  ids of the rows that you want to delete from the table. </p>
                tags:
                  - Batches
                  - Delete
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchupdate:
              POST:
                summary: BatchUpdateTableRows
                description: >-
                  <p> The BatchUpdateTableRows API allows you to update one or
                  more rows in a table in a workbook. </p> <p> You can specify
                  the values to set in some or all of the columns in the table
                  for the specified rows. If a column is not explicitly
                  specified in a particular row, then that column will not be
                  updated for that row. To clear out the data in a specific
                  cell, you need to set the value as an empty string (""). </p>
                tags:
                  - Batches
                  - Update
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchupsert:
              POST:
                summary: BatchUpsertTableRows
                description: >-
                  <p> The BatchUpsertTableRows API allows you to upsert one or
                  more rows in a table. The upsert operation takes a filter
                  expression as input and evaluates it to find matching rows on
                  the destination table. If matching rows are found, it will
                  update the cells in the matching rows to new values specified
                  in the request. If no matching rows are found, a new row is
                  added at the end of the table and the cells in that row are
                  set to the new values specified in the request. </p> <p> You
                  can specify the values to set in some or all of the columns in
                  the table for the matching or newly appended rows. If a column
                  is not explicitly specified for a particular row, then that
                  column will not be updated for that row. To clear out the data
                  in a specific cell, you need to set the value as an empty
                  string (""). </p>
                tags:
                  - Batches
                  - Upsert
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/import/{jobId}:
              GET:
                summary: DescribeTableDataImportJob
                description: >-
                  <p> The DescribeTableDataImportJob API allows you to retrieve
                  the status and details of a table data import job. </p>
                tags:
                  - Describe
                  - Tables
                  - Data
                  - Import
                  - Jobs
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
            /screendata:
              POST:
                summary: GetScreenData
                description: >-
                  <p> The GetScreenData API allows retrieval of data from a
                  screen in a Honeycode app. The API allows setting local
                  variables in the screen to filter, sort or otherwise affect
                  what will be displayed on the screen. </p>
                tags:
                  - Get
                  - Screen
                  - Data
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
            /workbooks/{workbookId}/apps/{appId}/screens/{screenId}/automations/{automationId}:
              POST:
                summary: InvokeScreenAutomation
                description: >-
                  <p> The InvokeScreenAutomation API allows invoking an action
                  defined in a screen in a Honeycode app. The API allows setting
                  local variables, which can then be used in the automation
                  being invoked. This allows automating the Honeycode app
                  interactions to write, update or delete data in the workbook.
                  </p>
                tags:
                  - Invoke
                  - Screen
                  - Automation
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
            /workbooks/{workbookId}/tables/{tableId}/columns:
              GET:
                summary: ListTableColumns
                description: >-
                  <p> The ListTableColumns API allows you to retrieve a list of
                  all the columns in a table in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Columns
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
            /workbooks/{workbookId}/tables/{tableId}/rows/list:
              POST:
                summary: ListTableRows
                description: >-
                  <p> The ListTableRows API allows you to retrieve a list of all
                  the rows in a table in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
            /workbooks/{workbookId}/tables:
              GET:
                summary: ListTables
                description: >-
                  <p> The ListTables API allows you to retrieve a list of all
                  the tables in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p> The UntagResource API allows you to removes tags from an
                  ARN-able resource. Resource includes workbook, table, screen
                  and screen-automation. </p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
            /workbooks/{workbookId}/tables/{tableId}/rows/query:
              POST:
                summary: QueryTableRows
                description: >-
                  <p> The QueryTableRows API allows you to use a filter formula
                  to query for specific rows in a table. </p>
                tags:
                  - Queries
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
                  - Queries
            /workbooks/{workbookId}/tables/{tableId}/import:
              POST:
                summary: StartTableDataImportJob
                description: >-
                  <p> The StartTableDataImportJob API allows you to start an
                  import job on a table. This API will only return the id of the
                  job that was started. To find out the status of the import
                  request, you need to call the DescribeTableDataImportJob
                tags:
                  - Start
                  - Tables
                  - Data
                  - Import
                  - Jobs
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
                  - Que
    overlays:
      - type: APIs.io Search
        url: overlays/honeycode-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/honeycode-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:honeycode
  - name: securityhub
    description: >-
      <p>Security Hub provides you with a comprehensive view of your security
      state in Amazon Web Services and helps you assess your Amazon Web Services
      environment against security industry standards and best practices.</p>
      <p>Security Hub collects security data across Amazon Web Services
      accounts, Amazon Web Services, and supported third-party products and
      helps you analyze your security trends and identify the highest priority
      security issues.</p> <p>To help you manage the security state of your
      organization, Security Hub supports multiple security standards. These
      include the Amazon Web Services Foundational Security Best Practices
      (FSBP) standard developed by Amazon Web Services, and external compliance
      frameworks such as the Center for Internet Security (CIS), the Payment
      Card Industry Data Security Standard (PCI DSS), and the National Institute
      of Standards and Technology (NIST). Each standard includes several
      security controls, each of which represents a security best practice.
      Security Hub runs checks against security controls and generates control
      findings to help you assess your compliance against security best
      practices.</p> <p>In addition to generating control findings, Security Hub
      also receives findings from other Amazon Web Services, such as Amazon
      GuardDuty and Amazon Inspector, and supported third-party products. This
      gives you a single pane of glass into a variety of security-related
      issues. You can also send Security Hub findings to other Amazon Web
      Services and supported third-party products.</p> <p>Security Hub offers
      automation features that help you triage and remediate security issues.
      For example, you can use automation rules to automatically update critical
      findings when a security check fails. You can also leverage the
      integration with Amazon EventBridge to trigger automatic responses to
      specific findings.</p> <p>This guide, the <i>Security Hub API
      Reference</i>, provides information about the Security Hub API. This
      includes supported resources, HTTP methods, parameters, and schemas. If
      you're new to Security Hub, you might find it helpful to also review the
      <a
      href="https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html">
      <i>Security Hub User Guide</i> </a>. The user guide explains key concepts
      and provides procedures that demonstrate how to use Security Hub features.
      It also provides information about topics such as integrating Security Hub
      with other Amazon Web Services.</p> <p>In addition to interacting with
      Security Hub by making calls to the Security Hub API, you can use a
      current version of an Amazon Web Services command line tool or SDK. Amazon
      Web Services provides tools and SDKs that consist of libraries and sample
      code for various languages and platforms, such as PowerShell, Java, Go,
      Python, C++, and .NET. These tools and SDKs provide convenient,
      programmatic access to Security Hub and other Amazon Web Services . They
      also handle tasks such as signing requests, managing errors, and retrying
      requests automatically. For information about installing and using the
      Amazon Web Services tools and SDKs, see <a
      href="http://aws.amazon.com/developer/tools/">Tools to Build on Amazon Web
      Services</a>.</p> <p>With the exception of operations that are related to
      central configuration, Security Hub API requests are executed only in the
      Amazon Web Services Region that is currently active or in the specific
      Amazon Web Services Region that you specify in your request. Any
      configuration or settings change that results from the operation is
      applied only to that Region. To make the same change in other Regions,
      call the same API operation in each Region in which you want to apply the
      change. When you use central configuration, API requests for enabling
      Security Hub, standards, and controls are executed in the home Region and
      all linked Regions. For a list of central configuration operations, see
      the <a
      href="https://docs.aws.amazon.com/securityhub/latest/userguide/central-configuration-intro.html#central-configuration-concepts">Central
      configuration terms and concepts</a> section of the <i>Security Hub User
      Guide</i>.</p> <p>The following throttling limits apply to Security Hub
      API operations.</p> <ul> <li> <p> <code>BatchEnableStandards</code> -
      <code>RateLimit</code> of 1 request per second. <code>BurstLimit</code> of
      1 request per second.</p> </li> <li> <p> <code>GetFindings</code> -
      <code>RateLimit</code> of 3 requests per second. <code>BurstLimit</code>
      of 6 requests per second.</p> </li> <li> <p>
      <code>BatchImportFindings</code> - <code>RateLimit</code> of 10 requests
      per second. <code>BurstLimit</code> of 30 requests per second.</p> </li>
      <li> <p> <code>BatchUpdateFindings</code> - <code>RateLimit</code> of 10
      requests per second. <code>BurstLimit</code> of 30 requests per
      second.</p> </li> <li> <p> <code>UpdateStandardsControl</code> -
      <code>RateLimit</code> of 1 request per second. <code>BurstLimit</code> of
      5 requests per second.</p> </li> <li> <p>All other operations -
      <code>RateLimit</code> of 10 requests per second. <code>BurstLimit</code>
      of 30 requests per second.</p> </li> </ul>
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
            title: securityhub
          paths:
            /administrator:
              GET:
                summary: GetAdministratorAccount
                description: >-
                  <p>Provides the details for the Security Hub administrator
                  account for the current member account.</p> <p>Can be used by
                  both member accounts that are managed using Organizations and
                  accounts that were invited manually.</p>
                tags:
                  - Get
                  - Administrator
                  - Account
                  - Administrator
            /master:
              GET:
                summary: GetMasterAccount
                description: >-
                  <p>This method is deprecated. Instead, use
                  <code>GetAdministratorAccount</code>.</p> <p>The Security Hub
                  console continues to use <code>GetMasterAccount</code>. It
                  will eventually change to use
                  <code>GetAdministratorAccount</code>. Any IAM policies that
                  specifically control access to this function must continue to
                  use <code>GetMasterAccount</code>. You should also add
                  <code>GetAdministratorAccount</code> to your policies to
                  ensure that the correct permissions are in place after the
                  console begins to use
                  <code>GetAdministratorAccount</code>.</p> <p>Provides the
                  details for the Security Hub administrator account for the
                  current member account.</p> <p>Can be used by both member
                  accounts that are managed using Organizations and accounts
                  that were invited manually.</p>
                tags:
                  - Get
                  - Master
                  - Account
                  - Administrator
                  - Master
            /automationrules/delete:
              POST:
                summary: BatchDeleteAutomationRules
                description: <p> Deletes one or more automation rules. </p>
                tags:
                  - Batches
                  - Delete
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
            /standards/deregister:
              POST:
                summary: BatchDisableStandards
                description: >-
                  <p>Disables the standards specified by the provided
                  <code>StandardsSubscriptionArns</code>.</p> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-standards.html">Security
                  Standards</a> section of the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Disable
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
            /standards/register:
              POST:
                summary: BatchEnableStandards
                description: >-
                  <p>Enables the standards specified by the provided
                  <code>StandardsArn</code>. To obtain the ARN for a standard,
                  use the <code>DescribeStandards</code> operation.</p> <p>For
                  more information, see the <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-standards.html">Security
                  Standards</a> section of the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Enable
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
            /automationrules/get:
              POST:
                summary: BatchGetAutomationRules
                description: >-
                  <p> Retrieves a list of details for automation rules based on
                  rule Amazon Resource Names (ARNs). </p>
                tags:
                  - Batches
                  - Get
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
            /configurationPolicyAssociation/batchget:
              POST:
                summary: BatchGetConfigurationPolicyAssociations
                description: >-
                  <p> Returns associations between an Security Hub configuration
                  and a batch of target accounts, organizational units, or the
                  root. Only the Security Hub delegated administrator can invoke
                  this operation from the home Region. A configuration can refer
                  to a configuration policy or to a self-managed configuration.
                  </p>
                tags:
                  - Batches
                  - Get
                  - Configurations
                  - Policies
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
            /securityControls/batchGet:
              POST:
                summary: BatchGetSecurityControls
                description: >-
                  <p> Provides details about a batch of security controls for
                  the current Amazon Web Services account and Amazon Web
                  Services Region. </p>
                tags:
                  - Batches
                  - Get
                  - Security
                  - Controls
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
            /associations/batchGet:
              POST:
                summary: BatchGetStandardsControlAssociations
                description: >-
                  <p> For a batch of security controls and standards, identifies
                  whether each control is currently enabled or disabled in a
                  standard. </p>
                tags:
                  - Batches
                  - Get
                  - Standards
                  - Control
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
            /findings/import:
              POST:
                summary: BatchImportFindings
                description: >-
                  <p>Imports security findings generated by a finding provider
                  into Security Hub. This action is requested by the finding
                  provider to import its findings into Security Hub.</p> <p>
                  <code>BatchImportFindings</code> must be called by one of the
                  following:</p> <ul> <li> <p>The Amazon Web Services account
                  that is associated with a finding if you are using the <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-custom-providers.html#securityhub-custom-providers-bfi-reqs">default
                  product ARN</a> or are a partner sending findings from within
                  a customer's Amazon Web Services account. In these cases, the
                  identifier of the account that you are calling
                  <code>BatchImportFindings</code> from needs to be the same as
                  the <code>AwsAccountId</code> attribute for the finding.</p>
                  </li> <li> <p>An Amazon Web Services account that Security Hub
                  has allow-listed for an official partner integration. In this
                  case, you can call <code>BatchImportFindings</code> from the
                  allow-listed account and send findings from different customer
                  accounts in the same batch.</p> </li> </ul> <p>The maximum
                  allowed size for a finding is 240 Kb. An error is returned for
                  any finding larger than 240 Kb.</p> <p>After a finding is
                  created, <code>BatchImportFindings</code> cannot be used to
                  update the following finding fields and objects, which
                  Security Hub customers use to manage their investigation
                  workflow.</p> <ul> <li> <p> <code>Note</code> </p> </li> <li>
                  <p> <code>UserDefinedFields</code> </p> </li> <li> <p>
                  <code>VerificationState</code> </p> </li> <li> <p>
                  <code>Workflow</code> </p> </li> </ul> <p>Finding providers
                  also should not use <code>BatchImportFindings</code> to update
                  the following attributes.</p> <ul> <li> <p>
                  <code>Confidence</code> </p> </li> <li> <p>
                  <code>Criticality</code> </p> </li> <li> <p>
                  <code>RelatedFindings</code> </p> </li> <li> <p>
                  <code>Severity</code> </p> </li> <li> <p> <code>Types</code>
                  </p> </li> </ul> <p>Instead, finding providers use
                  <code>FindingProviderFields</code> to provide values for these
                  attributes.</p>
                tags:
                  - Batches
                  - Import
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
            /automationrules/update:
              PATCH:
                summary: BatchUpdateAutomationRules
                description: >-
                  <p> Updates one or more automation rules based on rule Amazon
                  Resource Names (ARNs) and input parameters. </p>
                tags:
                  - Batches
                  - Update
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
            /findings/batchupdate:
              PATCH:
                summary: BatchUpdateFindings
                description: >-
                  <p>Used by Security Hub customers to update information about
                  their investigation into a finding. Requested by administrator
                  accounts or member accounts. Administrator accounts can update
                  findings for their account and their member accounts. Member
                  accounts can update findings for their account.</p> <p>Updates
                  from <code>BatchUpdateFindings</code> do not affect the value
                  of <code>UpdatedAt</code> for a finding.</p> <p>Administrator
                  and member accounts can use <code>BatchUpdateFindings</code>
                  to update the following finding fields and objects.</p> <ul>
                  <li> <p> <code>Confidence</code> </p> </li> <li> <p>
                  <code>Criticality</code> </p> </li> <li> <p> <code>Note</code>
                  </p> </li> <li> <p> <code>RelatedFindings</code> </p> </li>
                  <li> <p> <code>Severity</code> </p> </li> <li> <p>
                  <code>Types</code> </p> </li> <li> <p>
                  <code>UserDefinedFields</code> </p> </li> <li> <p>
                  <code>VerificationState</code> </p> </li> <li> <p>
                  <code>Workflow</code> </p> </li> </ul> <p>You can configure
                  IAM policies to restrict access to fields and field values.
                  For example, you might not want member accounts to be able to
                  suppress findings or change the finding severity. See <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/finding-update-batchupdatefindings.html#batchupdatefindings-configure-access">Configuring
                  access to BatchUpdateFindings</a> in the <i>Security Hub User
                  Guide</i>.</p>
                tags:
                  - Batches
                  - Update
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
            /associations:
              GET:
                summary: ListStandardsControlAssociations
                description: >-
                  <p> Specifies whether a control is currently enabled or
                  disabled in each enabled standard in the calling account. </p>
                tags:
                  - Lists
                  - Standards
                  - Control
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
            /actionTargets:
              POST:
                summary: CreateActionTarget
                description: >-
                  <p>Creates a custom action target in Security Hub.</p> <p>You
                  can use custom actions on findings and insights in Security
                  Hub to trigger target actions in Amazon CloudWatch Events.</p>
                tags:
                  - Create
                  - Actions
                  - Target
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
            /automationrules/create:
              POST:
                summary: CreateAutomationRule
                description: <p> Creates an automation rule based on input parameters. </p>
                tags:
                  - Create
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
            /configurationPolicy/create:
              POST:
                summary: CreateConfigurationPolicy
                description: >-
                  <p> Creates a configuration policy with the defined
                  configuration. Only the Security Hub delegated administrator
                  can invoke this operation from the home Region. </p>
                tags:
                  - Create
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
            /findingAggregator/create:
              POST:
                summary: CreateFindingAggregator
                description: >-
                  <p>Used to enable finding aggregation. Must be called from the
                  aggregation Region.</p> <p>For more details about cross-Region
                  replication, see <a
                  href="https://docs.aws.amazon.com/securityhub/latest/userguide/finding-aggregation.html">Configuring
                  finding aggregation</a> in the <i>Security Hub User Guide</i>.
                  </p>
                tags:
                  - Create
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
            /insights:
              POST:
                summary: CreateInsight
                description: >-
                  <p>Creates a custom insight in Security Hub. An insight is a
                  consolidation of findings that relate to a security issue that
                  requires attention or remediation.</p> <p>To group the related
                  findings in the insight, use the
                  <code>GroupByAttribute</code>.</p>
                tags:
                  - Create
                  - Insight
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
            /members:
              GET:
                summary: ListMembers
                description: >-
                  <p>Lists details about all member accounts for the current
                  Security Hub administrator account.</p> <p>The results include
                  both member accounts that belong to an organization and member
                  accounts that were invited manually.</p>
                tags:
                  - Lists
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
            /invitations/decline:
              POST:
                summary: DeclineInvitations
                description: >-
                  <p>Declines invitations to become a member account.</p> <p>A
                  prospective member account uses this operation to decline an
                  invitation to become a member.</p> <p>This operation is only
                  called by member accounts that aren't part of an organization.
                  Organization accounts don't receive invitations.</p>
                tags:
                  - Decline
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
            /actionTargets/{ActionTargetArn+}:
              PATCH:
                summary: UpdateActionTarget
                description: >-
                  <p>Updates the name and description of a custom action target
                  in Security Hub.</p>
                tags:
                  - Update
                  - Actions
                  - Target
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
            /configurationPolicy/{Identifier}:
              PATCH:
                summary: UpdateConfigurationPolicy
                description: >-
                  <p> Updates a configuration policy. Only the Security Hub
                  delegated administrator can invoke this operation from the
                  home Region. </p>
                tags:
                  - Update
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
            /findingAggregator/delete/{FindingAggregatorArn+}:
              DELETE:
                summary: DeleteFindingAggregator
                description: >-
                  <p>Deletes a finding aggregator. When you delete the finding
                  aggregator, you stop finding aggregation.</p> <p>When you stop
                  finding aggregation, findings that were already aggregated to
                  the aggregation Region are still visible from the aggregation
                  Region. New findings and finding updates are not aggregated.
                  </p>
                tags:
                  - Delete
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
            /insights/{InsightArn+}:
              PATCH:
                summary: UpdateInsight
                description: >-
                  <p>Updates the Security Hub insight identified by the
                  specified insight ARN.</p>
                tags:
                  - Update
                  - Insight
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /invitations/delete:
              POST:
                summary: DeleteInvitations
                description: >-
                  <p>Deletes invitations received by the Amazon Web Services
                  account to become a member account.</p> <p>A Security Hub
                  administrator account can use this operation to delete
                  invitations sent to one or more member accounts.</p> <p>This
                  operation is only used to delete invitations that are sent to
                  member accounts that aren't part of an organization.
                  Organization accounts don't receive invitations.</p>
                tags:
                  - Delete
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /members/delete:
              POST:
                summary: DeleteMembers
                description: >-
                  <p>Deletes the specified member accounts from Security
                  Hub.</p> <p>You can invoke this API only to delete accounts
                  that became members through invitation. You can't invoke this
                  API to delete accounts that belong to an Organizations
                  organization.</p>
                tags:
                  - Delete
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /actionTargets/get:
              POST:
                summary: DescribeActionTargets
                description: >-
                  <p>Returns a list of the custom action targets in Security Hub
                  in your account.</p>
                tags:
                  - Describe
                  - Actions
                  - Targets
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
            /accounts:
              PATCH:
                summary: UpdateSecurityHubConfiguration
                description: <p>Updates configuration options for Security Hub.</p>
                tags:
                  - Update
                  - Security
                  - Hub
                  - Configurations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
            /organization/configuration:
              POST:
                summary: UpdateOrganizationConfiguration
                description: >-
                  <p>Updates the configuration of your organization in Security
                  Hub. Only the Security Hub administrator account can invoke
                  this operation.</p>
                tags:
                  - Update
                  - Organizations
                  - Configurations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
            /products:
              GET:
                summary: DescribeProducts
                description: >-
                  <p>Returns information about product integrations in Security
                  Hub.</p> <p>You can optionally provide an integration ARN. If
                  you provide an integration ARN, then the results only include
                  that integration.</p> <p>If you do not provide an integration
                  ARN, then the results include all of the available product
                  integrations. </p>
                tags:
                  - Describe
                  - Products
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
            /standards:
              GET:
                summary: DescribeStandards
                description: >-
                  <p>Returns a list of the available standards in Security
                  Hub.</p> <p>For each standard, the results include the
                  standard ARN, the name, and a description. </p>
                tags:
                  - Describe
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
            /standards/controls/{StandardsSubscriptionArn+}:
              GET:
                summary: DescribeStandardsControls
                description: >-
                  <p>Returns a list of security standards controls.</p> <p>For
                  each control, the results include information about whether it
                  is currently enabled, the severity, and a link to remediation
                  information.</p>
                tags:
                  - Describe
                  - Standards
                  - Controls
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
            /productSubscriptions/{ProductSubscriptionArn+}:
              DELETE:
                summary: DisableImportFindingsForProduct
                description: >-
                  <p>Disables the integration of the specified product with
                  Security Hub. After the integration is disabled, findings from
                  that product are no longer sent to Security Hub.</p>
                tags:
                  - Disable
                  - Import
                  - Findings
                  - For
                  - Products
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
            /organization/admin/disable:
              POST:
                summary: DisableOrganizationAdminAccount
                description: >-
                  <p>Disables a Security Hub administrator account. Can only be
                  called by the organization management account.</p>
                tags:
                  - Disable
                  - Organizations
                  - Administrative
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
            /administrator/disassociate:
              POST:
                summary: DisassociateFromAdministratorAccount
                description: >-
                  <p>Disassociates the current Security Hub member account from
                  the associated administrator account.</p> <p>This operation is
                  only used by accounts that are not part of an organization.
                  For organization accounts, only the administrator account can
                  disassociate a member account.</p>
                tags:
                  - Disassociate
                  - From
                  - Administrator
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /master/disassociate:
              POST:
                summary: DisassociateFromMasterAccount
                description: >-
                  <p>This method is deprecated. Instead, use
                  <code>DisassociateFromAdministratorAccount</code>.</p> <p>The
                  Security Hub console continues to use
                  <code>DisassociateFromMasterAccount</code>. It will eventually
                  change to use
                  <code>DisassociateFromAdministratorAccount</code>. Any IAM
                  policies that specifically control access to this function
                  must continue to use
                  <code>DisassociateFromMasterAccount</code>. You should also
                  add <code>DisassociateFromAdministratorAccount</code> to your
                  policies to ensure that the correct permissions are in place
                  after the console begins to use
                  <code>DisassociateFromAdministratorAccount</code>.</p>
                  <p>Disassociates the current Security Hub member account from
                  the associated administrator account.</p> <p>This operation is
                  only used by accounts that are not part of an organization.
                  For organization accounts, only the administrator account can
                  disassociate a member account.</p>
                tags:
                  - Disassociate
                  - From
                  - Master
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /members/disassociate:
              POST:
                summary: DisassociateMembers
                description: >-
                  <p>Disassociates the specified member accounts from the
                  associated administrator account.</p> <p>Can be used to
                  disassociate both accounts that are managed using
                  Organizations and accounts that were invited manually.</p>
                tags:
                  - Disassociate
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /productSubscriptions:
              GET:
                summary: ListEnabledProductsForImport
                description: >-
                  <p>Lists all findings-generating solutions (products) that you
                  are subscribed to receive findings from in Security Hub.</p>
                tags:
                  - Lists
                  - Enabled
                  - Products
                  - For
                  - Import
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
            /organization/admin/enable:
              POST:
                summary: EnableOrganizationAdminAccount
                description: >-
                  <p>Designates the Security Hub administrator account for an
                  organization. Can only be called by the organization
                  management account.</p>
                tags:
                  - Enable
                  - Organizations
                  - Administrative
                  - Account
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /configurationPolicy/get/{Identifier}:
              GET:
                summary: GetConfigurationPolicy
                description: >-
                  <p> Provides information about a configuration policy. Only
                  the Security Hub delegated administrator can invoke this
                  operation from the home Region. </p>
                tags:
                  - Get
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /configurationPolicyAssociation/get:
              POST:
                summary: GetConfigurationPolicyAssociation
                description: >-
                  <p> Returns the association between a configuration and a
                  target account, organizational unit, or the root. The
                  configuration can be a configuration policy or self-managed
                  behavior. Only the Security Hub delegated administrator can
                  invoke this operation from the home Region. </p>
                tags:
                  - Get
                  - Configurations
                  - Policies
                  - Association
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /standards/get:
              POST:
                summary: GetEnabledStandards
                description: >-
                  <p>Returns a list of the standards that are currently
                  enabled.</p>
                tags:
                  - Get
                  - Enabled
                  - Standards
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /findingAggregator/get/{FindingAggregatorArn+}:
              GET:
                summary: GetFindingAggregator
                description: <p>Returns the current finding aggregation configuration.</p>
                tags:
                  - Get
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
            /findingHistory/get:
              POST:
                summary: GetFindingHistory
                description: >-
                  <p> Returns history for a Security Hub finding in the last 90
                  days. The history includes changes made to any fields in the
                  Amazon Web Services Security Finding Format (ASFF). </p>
                tags:
                  - Get
                  - Findings
                  - History
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /findings:
              PATCH:
                summary: UpdateFindings
                description: >-
                  <p> <code>UpdateFindings</code> is deprecated. Instead of
                  <code>UpdateFindings</code>, use
                  <code>BatchUpdateFindings</code>.</p> <p>Updates the
                  <code>Note</code> and <code>RecordState</code> of the Security
                  Hub-aggregated findings that the filter attributes specify.
                  Any member account that can view the finding also sees the
                  update to the finding.</p>
                tags:
                  - Update
                  - Findings
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /insights/results/{InsightArn+}:
              GET:
                summary: GetInsightResults
                description: >-
                  <p>Lists the results of the Security Hub insight specified by
                  the insight ARN.</p>
                tags:
                  - Get
                  - Insight
                  - Results
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /insights/get:
              POST:
                summary: GetInsights
                description: >-
                  <p>Lists and describes insights for the specified insight
                  ARNs.</p>
                tags:
                  - Get
                  - Insights
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
            /invitations/count:
              GET:
                summary: GetInvitationsCount
                description: >-
                  <p>Returns the count of all Security Hub membership
                  invitations that were sent to the current member account, not
                  including the currently accepted invitation. </p>
                tags:
                  - Get
                  - Invitations
                  - Count
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
            /members/get:
              POST:
                summary: GetMembers
                description: >-
                  <p>Returns the details for the Security Hub member accounts
                  for the specified account IDs.</p> <p>An administrator account
                  can be either the delegated Security Hub administrator account
                  for an organization or an administrator account that enabled
                  Security Hub manually.</p> <p>The results include both member
                  accounts that are managed using Organizations and accounts
                  that were invited manually.</p>
                tags:
                  - Get
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
            /securityControl/definition:
              GET:
                summary: GetSecurityControlDefinition
                description: >-
                  <p> Retrieves the definition of a security control. The
                  definition includes the control title, description, Region
                  availability, parameter definitions, and other details. </p>
                tags:
                  - Get
                  - Security
                  - Control
                  - Definitions
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
            /members/invite:
              POST:
                summary: InviteMembers
                description: >-
                  <p>Invites other Amazon Web Services accounts to become member
                  accounts for the Security Hub administrator account that the
                  invitation is sent from.</p> <p>This operation is only used to
                  invite accounts that do not belong to an organization.
                  Organization accounts do not receive invitations.</p>
                  <p>Before you can use this action to invite a member, you must
                  first use the <code>CreateMembers</code> action to create the
                  member account in Security Hub.</p> <p>When the account owner
                  enables Security Hub and accepts the invitation to become a
                  member account, the administrator account can view the
                  findings generated from the member account.</p>
                tags:
                  - Invite
                  - Members
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
            /automationrules/list:
              GET:
                summary: ListAutomationRules
                description: >-
                  <p> A list of automation rules and their metadata for the
                  calling account. </p>
                tags:
                  - Lists
                  - Automation
                  - Rules
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /configurationPolicy/list:
              GET:
                summary: ListConfigurationPolicies
                description: >-
                  <p> Lists the configuration policies that the Security Hub
                  delegated administrator has created for your organization.
                  Only the delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Lists
                  - Configurations
                  - Policies
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /configurationPolicyAssociation/list:
              POST:
                summary: ListConfigurationPolicyAssociations
                description: >-
                  <p> Provides information about the associations for your
                  configuration policies and self-managed behavior. Only the
                  Security Hub delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Lists
                  - Configurations
                  - Policies
                  - Associations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /findingAggregator/list:
              GET:
                summary: ListFindingAggregators
                description: >-
                  <p>If finding aggregation is enabled, then
                  <code>ListFindingAggregators</code> returns the ARN of the
                  finding aggregator. You can run this operation from any
                  Region.</p>
                tags:
                  - Lists
                  - Findings
                  - Aggregators
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /invitations:
              GET:
                summary: ListInvitations
                description: >-
                  <p>Lists all Security Hub membership invitations that were
                  sent to the current Amazon Web Services account.</p> <p>This
                  operation is only used by accounts that are managed by
                  invitation. Accounts that are managed using the integration
                  with Organizations do not receive invitations.</p>
                tags:
                  - Lists
                  - Invitations
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /organization/admin:
              GET:
                summary: ListOrganizationAdminAccounts
                description: >-
                  <p>Lists the Security Hub administrator accounts. Can only be
                  called by the organization management account.</p>
                tags:
                  - Lists
                  - Organizations
                  - Administrative
                  - Accounts
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
            /securityControls/definitions:
              GET:
                summary: ListSecurityControlDefinitions
                description: >-
                  <p> Lists all of the security controls that apply to a
                  specified standard. </p>
                tags:
                  - Lists
                  - Security
                  - Control
                  - Definitions
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
            /configurationPolicyAssociation/associate:
              POST:
                summary: StartConfigurationPolicyAssociation
                description: >-
                  <p> Associates a target account, organizational unit, or the
                  root with a specified configuration. The target can be
                  associated with a configuration policy or self-managed
                  behavior. Only the Security Hub delegated administrator can
                  invoke this operation from the home Region. </p>
                tags:
                  - Start
                  - Configurations
                  - Policies
                  - Association
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /configurationPolicyAssociation/disassociate:
              POST:
                summary: StartConfigurationPolicyDisassociation
                description: >-
                  <p> Disassociates a target account, organizational unit, or
                  the root from a specified configuration. When you disassociate
                  a configuration from its target, the target inherits the
                  configuration of the closest parent. If there’s no
                  configuration to inherit, the target retains its settings but
                  becomes a self-managed account. A target can be disassociated
                  from a configuration policy or self-managed behavior. Only the
                  Security Hub delegated administrator can invoke this operation
                  from the home Region. </p>
                tags:
                  - Start
                  - Configurations
                  - Policies
                  - Disassociation
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /findingAggregator/update:
              PATCH:
                summary: UpdateFindingAggregator
                description: >-
                  <p>Updates the finding aggregation configuration. Used to
                  update the Region linking mode and the list of included or
                  excluded Regions. You cannot use
                  <code>UpdateFindingAggregator</code> to change the aggregation
                  Region.</p> <p>You must run
                  <code>UpdateFindingAggregator</code> from the current
                  aggregation Region. </p>
                tags:
                  - Update
                  - Findings
                  - Aggregator
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /securityControl/update:
              PATCH:
                summary: UpdateSecurityControl
                description: <p> Updates the properties of a security control. </p>
                tags:
                  - Update
                  - Security
                  - Control
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associate
            /standards/control/{StandardsControlArn+}:
              PATCH:
                summary: UpdateStandardsControl
                description: >-
                  <p>Used to control whether an individual security standard
                  control is enabled or dis
                tags:
                  - Update
                  - Standards
                  - Control
                  - Administrator
                  - Master
                  - Automation Rules
                  - Delete
                  - Standards
                  - Deregister
                  - Register
                  - Get
                  - Policies
                  - Association
                  - Batches
                  - Controls
                  - Batches
                  - Findings
                  - Import
                  - Update
                  - Batches
                  - Associations
                  - Targets
                  - Create
                  - Aggregator
                  - Insights
                  - Members
                  - Invitations
                  - Decline
                  - Actions
                  - Target
                  - ARN
                  - Identifiers
                  - Findings
                  - Insight
                  - Accounts
                  - Organizations
                  - Configurations
                  - Products
                  - Subscriptions
                  - Subscriptions
                  - Products
                  - Administrative
                  - Disable
                  - Disassociate
                  - Enable
                  - History
                  - Count
                  - Control
                  - Definitions
                  - Invite
                  - Lists
                  - Definitions
                  - Resources
                  - ARN
                  - Associa
    overlays:
      - type: APIs.io Search
        url: overlays/securityhub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/securityhub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:securityhub
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---