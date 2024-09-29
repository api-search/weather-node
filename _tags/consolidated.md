---
name: Consolidated
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/consolidated.png
url: https://example.com/apis/consolidated.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Consolidated
apis:
  - name: wellarchitected
    description: >-
      <fullname>Well-Architected Tool</fullname> <p>This is the
      <i>Well-Architected Tool API Reference</i>. The WA Tool API provides
      programmatic access to the <a
      href="http://aws.amazon.com/well-architected-tool">Well-Architected
      Tool</a> in the <a
      href="https://console.aws.amazon.com/wellarchitected">Amazon Web Services
      Management Console</a>. For information about the Well-Architected Tool,
      see the <a
      href="https://docs.aws.amazon.com/wellarchitected/latest/userguide/intro.html">Well-Architected
      Tool User Guide</a>.</p>
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
            title: wellarchitected
          paths:
            /workloads/{WorkloadId}/associateLenses:
              PATCH:
                summary: AssociateLenses
                description: >-
                  <p>Associate a lens to a workload.</p> <p>Up to 10 lenses can
                  be associated with a workload in a single API operation. A
                  maximum of 20 lenses can be associated with a workload.</p>
                  <note> <p> <b>Disclaimer</b> </p> <p>By accessing and/or
                  applying custom lenses created by another Amazon Web Services
                  user or account, you acknowledge that custom lenses created by
                  other users and shared with you are Third Party Content as
                  defined in the Amazon Web Services Customer Agreement. </p>
                  </note>
                tags:
                  - Associate
                  - Lenses
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
            /workloads/{WorkloadId}/associateProfiles:
              PATCH:
                summary: AssociateProfiles
                description: <p>Associate a profile with a workload.</p>
                tags:
                  - Associate
                  - Profiles
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
            /lenses/{LensAlias}/shares:
              GET:
                summary: ListLensShares
                description: <p>List the lens shares associated with the lens.</p>
                tags:
                  - Lists
                  - Lens
                  - Shares
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
            /lenses/{LensAlias}/versions:
              POST:
                summary: CreateLensVersion
                description: >-
                  <p>Create a new lens version.</p> <p>A lens can have up to 100
                  versions.</p> <p>Use this operation to publish a new lens
                  version after you have imported a lens. The
                  <code>LensAlias</code> is used to identify the lens to be
                  published. The owner of a lens can share the lens with other
                  Amazon Web Services accounts and users in the same Amazon Web
                  Services Region. Only the owner of a lens can delete it. </p>
                tags:
                  - Create
                  - Lens
                  - Versions
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
            /workloads/{WorkloadId}/milestones:
              POST:
                summary: CreateMilestone
                description: <p>Create a milestone for an existing workload.</p>
                tags:
                  - Create
                  - Milestones
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
            /profiles:
              POST:
                summary: CreateProfile
                description: <p>Create a profile.</p>
                tags:
                  - Create
                  - Profiles
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
            /profiles/{ProfileArn}/shares:
              GET:
                summary: ListProfileShares
                description: <p>List profile shares.</p>
                tags:
                  - Lists
                  - Profiles
                  - Shares
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
            /reviewTemplates:
              GET:
                summary: ListReviewTemplates
                description: <p>List review templates.</p>
                tags:
                  - Lists
                  - Reviews
                  - Templates
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
            /templates/shares/{TemplateArn}:
              GET:
                summary: ListTemplateShares
                description: <p>List review template shares.</p>
                tags:
                  - Lists
                  - Templates
                  - Shares
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
            /workloads:
              POST:
                summary: CreateWorkload
                description: >-
                  <p>Create a new workload.</p> <p>The owner of a workload can
                  share the workload with other Amazon Web Services accounts,
                  users, an organization, and organizational units (OUs) in the
                  same Amazon Web Services Region. Only the owner of a workload
                  can delete it.</p> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/wellarchitected/latest/userguide/define-workload.html">Defining
                  a Workload</a> in the <i>Well-Architected Tool User
                  Guide</i>.</p> <important> <p>Either <code>AwsRegions</code>,
                  <code>NonAwsRegions</code>, or both must be specified when
                  creating a workload.</p> <p>You also must specify
                  <code>ReviewOwner</code>, even though the parameter is listed
                  as not being required in the following section. </p>
                  </important> <p>When creating a workload using a review
                  template, you must have the following IAM permissions:</p>
                  <ul> <li> <p> <code>wellarchitected:GetReviewTemplate</code>
                  </p> </li> <li> <p>
                  <code>wellarchitected:GetReviewTemplateAnswer</code> </p>
                  </li> <li> <p>
                  <code>wellarchitected:ListReviewTemplateAnswers</code> </p>
                  </li> <li> <p>
                  <code>wellarchitected:GetReviewTemplateLensReview</code> </p>
                  </li> </ul>
                tags:
                  - Create
                  - Workloads
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
            /workloads/{WorkloadId}/shares:
              GET:
                summary: ListWorkloadShares
                description: <p>List the workload shares associated with the workload.</p>
                tags:
                  - Lists
                  - Workloads
                  - Shares
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
            /lenses/{LensAlias}:
              GET:
                summary: GetLens
                description: <p>Get an existing lens.</p>
                tags:
                  - Get
                  - Lens
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
            /lenses/{LensAlias}/shares/{ShareId}:
              DELETE:
                summary: DeleteLensShare
                description: >-
                  <p>Delete a lens share.</p> <p>After the lens share is
                  deleted, Amazon Web Services accounts, users, organizations,
                  and organizational units (OUs) that you shared the lens with
                  can continue to use it, but they will no longer be able to
                  apply it to new workloads.</p> <note> <p> <b>Disclaimer</b>
                  </p> <p>By sharing your custom lenses with other Amazon Web
                  Services accounts, you acknowledge that Amazon Web Services
                  will make your custom lenses available to those other
                  accounts. Those other accounts may continue to access and use
                  your shared custom lenses even if you delete the custom lenses
                  from your own Amazon Web Services account or terminate your
                  Amazon Web Services account.</p> </note>
                tags:
                  - Delete
                  - Lens
                  - Share
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /profiles/{ProfileArn}:
              PATCH:
                summary: UpdateProfile
                description: <p>Update a profile.</p>
                tags:
                  - Update
                  - Profiles
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /profiles/{ProfileArn}/shares/{ShareId}:
              DELETE:
                summary: DeleteProfileShare
                description: <p>Delete a profile share.</p>
                tags:
                  - Delete
                  - Profiles
                  - Share
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /reviewTemplates/{TemplateArn}:
              PATCH:
                summary: UpdateReviewTemplate
                description: <p>Update a review template.</p>
                tags:
                  - Update
                  - Reviews
                  - Templates
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /templates/shares/{TemplateArn}/{ShareId}:
              DELETE:
                summary: DeleteTemplateShare
                description: >-
                  <p>Delete a review template share.</p> <p>After the review
                  template share is deleted, Amazon Web Services accounts,
                  users, organizations, and organizational units (OUs) that you
                  shared the review template with will no longer be able to
                  apply it to new workloads.</p>
                tags:
                  - Delete
                  - Templates
                  - Share
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /workloads/{WorkloadId}:
              PATCH:
                summary: UpdateWorkload
                description: <p>Update an existing workload.</p>
                tags:
                  - Update
                  - Workloads
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /workloads/{WorkloadId}/shares/{ShareId}:
              PATCH:
                summary: UpdateWorkloadShare
                description: <p>Update a workload share.</p>
                tags:
                  - Update
                  - Workloads
                  - Share
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
            /workloads/{WorkloadId}/disassociateLenses:
              PATCH:
                summary: DisassociateLenses
                description: >-
                  <p>Disassociate a lens from a workload.</p> <p>Up to 10 lenses
                  can be disassociated from a workload in a single API
                  operation.</p> <note> <p>The Amazon Web Services
                  Well-Architected Framework lens (<code>wellarchitected</code>)
                  cannot be removed from a workload.</p> </note>
                tags:
                  - Disassociate
                  - Lenses
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
            /workloads/{WorkloadId}/disassociateProfiles:
              PATCH:
                summary: DisassociateProfiles
                description: <p>Disassociate a profile from a workload.</p>
                tags:
                  - Disassociate
                  - Profiles
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
            /lenses/{LensAlias}/export:
              GET:
                summary: ExportLens
                description: >-
                  <p>Export an existing lens.</p> <p>Only the owner of a lens
                  can export it. Lenses provided by Amazon Web Services (Amazon
                  Web Services Official Content) cannot be exported.</p>
                  <p>Lenses are defined in JSON. For more information, see <a
                  href="https://docs.aws.amazon.com/wellarchitected/latest/userguide/lenses-format-specification.html">JSON
                  format specification</a> in the <i>Well-Architected Tool User
                  Guide</i>.</p> <note> <p> <b>Disclaimer</b> </p> <p>Do not
                  include or gather personal identifiable information (PII) of
                  end users or other identifiable individuals in or via your
                  custom lenses. If your custom lens or those shared with you
                  and used in your account do include or collect PII you are
                  responsible for: ensuring that the included PII is processed
                  in accordance with applicable law, providing adequate privacy
                  notices, and obtaining necessary consents for processing such
                  data.</p> </note>
                tags:
                  - Export
                  - Lens
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
            /workloads/{WorkloadId}/lensReviews/{LensAlias}/answers/{QuestionId}:
              PATCH:
                summary: UpdateAnswer
                description: >-
                  <p>Update the answer to a specific question in a workload
                  review.</p>
                tags:
                  - Update
                  - Answers
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
            /consolidatedReport:
              GET:
                summary: GetConsolidatedReport
                description: >-
                  <p>Get a consolidated report of your workloads.</p> <p>You can
                  optionally choose to include workloads that have been shared
                  with you.</p>
                tags:
                  - Get
                  - Consolidated
                  - Reports
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
            /workloads/{WorkloadId}/lensReviews/{LensAlias}:
              PATCH:
                summary: UpdateLensReview
                description: <p>Update lens review for a particular workload.</p>
                tags:
                  - Update
                  - Lens
                  - Reviews
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
            /workloads/{WorkloadId}/lensReviews/{LensAlias}/report:
              GET:
                summary: GetLensReviewReport
                description: <p>Get lens review report.</p>
                tags:
                  - Get
                  - Lens
                  - Reviews
                  - Reports
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
            /lenses/{LensAlias}/versionDifference:
              GET:
                summary: GetLensVersionDifference
                description: <p>Get lens version differences.</p>
                tags:
                  - Get
                  - Lens
                  - Versions
                  - Difference
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
            /workloads/{WorkloadId}/milestones/{MilestoneNumber}:
              GET:
                summary: GetMilestone
                description: <p>Get a milestone for an existing workload.</p>
                tags:
                  - Get
                  - Milestones
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /profileTemplate:
              GET:
                summary: GetProfileTemplate
                description: <p>Get profile template.</p>
                tags:
                  - Get
                  - Profiles
                  - Templates
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /reviewTemplates/{TemplateArn}/lensReviews/{LensAlias}/answers/{QuestionId}:
              PATCH:
                summary: UpdateReviewTemplateAnswer
                description: <p>Update a review template answer.</p>
                tags:
                  - Update
                  - Reviews
                  - Templates
                  - Answers
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /reviewTemplates/{TemplateArn}/lensReviews/{LensAlias}:
              PATCH:
                summary: UpdateReviewTemplateLensReview
                description: <p>Update a lens review associated with a review template.</p>
                tags:
                  - Update
                  - Reviews
                  - Templates
                  - Lens
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /importLens:
              PUT:
                summary: ImportLens
                description: >-
                  <p>Import a new custom lens or update an existing custom
                  lens.</p> <p>To update an existing custom lens, specify its
                  ARN as the <code>LensAlias</code>. If no ARN is specified, a
                  new custom lens is created.</p> <p>The new or updated lens
                  will have a status of <code>DRAFT</code>. The lens cannot be
                  applied to workloads or shared with other Amazon Web Services
                  accounts until it's published with
                  <a>CreateLensVersion</a>.</p> <p>Lenses are defined in JSON.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/wellarchitected/latest/userguide/lenses-format-specification.html">JSON
                  format specification</a> in the <i>Well-Architected Tool User
                  Guide</i>.</p> <p>A custom lens cannot exceed 500 KB in
                  size.</p> <note> <p> <b>Disclaimer</b> </p> <p>Do not include
                  or gather personal identifiable information (PII) of end users
                  or other identifiable individuals in or via your custom
                  lenses. If your custom lens or those shared with you and used
                  in your account do include or collect PII you are responsible
                  for: ensuring that the included PII is processed in accordance
                  with applicable law, providing adequate privacy notices, and
                  obtaining necessary consents for processing such data.</p>
                  </note>
                tags:
                  - Import
                  - Lens
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /workloads/{WorkloadId}/lensReviews/{LensAlias}/answers:
              GET:
                summary: ListAnswers
                description: <p>List of answers for a particular workload and lens.</p>
                tags:
                  - Lists
                  - Answers
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
            /workloads/{WorkloadId}/checks:
              POST:
                summary: ListCheckDetails
                description: >-
                  <p>List of Trusted Advisor check details by account related to
                  the workload.</p>
                tags:
                  - Lists
                  - Checks
                  - Details
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
            /workloads/{WorkloadId}/checkSummaries:
              POST:
                summary: ListCheckSummaries
                description: >-
                  <p>List of Trusted Advisor checks summarized for all accounts
                  related to the workload.</p>
                tags:
                  - Lists
                  - Checks
                  - Summaries
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
            /workloads/{WorkloadId}/lensReviews/{LensAlias}/improvements:
              GET:
                summary: ListLensReviewImprovements
                description: <p>List lens review improvements.</p>
                tags:
                  - Lists
                  - Lens
                  - Reviews
                  - Improvements
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
            /workloads/{WorkloadId}/lensReviews:
              GET:
                summary: ListLensReviews
                description: <p>List lens reviews for a particular workload.</p>
                tags:
                  - Lists
                  - Lens
                  - Reviews
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
            /lenses:
              GET:
                summary: ListLenses
                description: <p>List the available lenses.</p>
                tags:
                  - Lists
                  - Lenses
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
            /workloads/{WorkloadId}/milestonesSummaries:
              POST:
                summary: ListMilestones
                description: <p>List all milestones for an existing workload.</p>
                tags:
                  - Lists
                  - Milestones
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
            /notifications:
              POST:
                summary: ListNotifications
                description: <p>List lens notifications.</p>
                tags:
                  - Lists
                  - Notifications
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
            /profileNotifications/:
              GET:
                summary: ListProfileNotifications
                description: <p>List profile notifications.</p>
                tags:
                  - Lists
                  - Profiles
                  - Notifications
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
            /profileSummaries:
              GET:
                summary: ListProfiles
                description: <p>List profiles.</p>
                tags:
                  - Lists
                  - Profiles
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
            /reviewTemplates/{TemplateArn}/lensReviews/{LensAlias}/answers:
              GET:
                summary: ListReviewTemplateAnswers
                description: <p>List the answers of a review template.</p>
                tags:
                  - Lists
                  - Reviews
                  - Templates
                  - Answers
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
            /shareInvitations:
              GET:
                summary: ListShareInvitations
                description: >-
                  <p>List the share invitations.</p> <p>
                  <code>WorkloadNamePrefix</code>, <code>LensNamePrefix</code>,
                  <code>ProfileNamePrefix</code>, and
                  <code>TemplateNamePrefix</code> are mutually exclusive. Use
                  the parameter that matches your
                  <code>ShareResourceType</code>.</p>
                tags:
                  - Lists
                  - Share
                  - Invitations
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
            /tags/{WorkloadArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Deletes specified tags from a resource.</p> <note> <p>The
                  WorkloadArn parameter can be a workload ARN, a custom lens
                  ARN, a profile ARN, or review template ARN.</p> </note> <p>To
                  specify multiple tags, use separate <b>tagKeys</b> parameters,
                  for example:</p> <p> <code>DELETE
                  /tags/WorkloadArn?tagKeys=key1&amp;tagKeys=key2</code> </p>
                tags:
                  - Untag
                  - Resources
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
            /workloadsSummaries:
              POST:
                summary: ListWorkloads
                description: <p>Paginated list of workloads.</p>
                tags:
                  - Lists
                  - Workloads
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
            /global-settings:
              PATCH:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates whether the Amazon Web Services account is opted
                  into organization sharing and discovery integration
                  features.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
                  - Global
                  - Settings
            /shareInvitations/{ShareInvitationId}:
              PATCH:
                summary: UpdateShareInvitation
                description: >-
                  <p>Update a workload or custom lens share invitation.</p>
                  <note> <p>This API operation can be called independently of
                  any resource. Previous documentation implied that a workload
                  ARN must be specified.</p> </note>
                tags:
                  - Update
                  - Share
                  - Invitation
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
                  - Global
                  - Settings
                  - Invitation
            /workloads/{WorkloadId}/lensReviews/{LensAlias}/upgrade:
              PUT:
                summary: UpgradeLensReview
                description: <p>Upgrade lens review for a particular workload.</p>
                tags:
                  - Upgrade
                  - Lens
                  - Reviews
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
                  - Global
                  - Settings
                  - Invitation
                  - Upgrade
            /workloads/{WorkloadId}/profiles/{ProfileArn}/upgrade:
              PUT:
                summary: UpgradeProfileVersion
                description: <p>Upgrade a profile.</p>
                tags:
                  - Upgrade
                  - Profiles
                  - Versions
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
                  - Global
                  - Settings
                  - Invitation
                  - Upgrade
            /reviewTemplates/{TemplateArn}/lensReviews/{LensAlias}/upgrade:
              PUT:
                summary: UpgradeReviewTemplateLensReview
                description: <p>Upgrade the lens review of a review tem
                tags:
                  - Upgrade
                  - Reviews
                  - Templates
                  - Lens
                  - Workloads
                  - Identifiers
                  - Associate
                  - Lenses
                  - Profiles
                  - Lens
                  - Alias
                  - Shares
                  - Versions
                  - Milestones
                  - Profiles
                  - ARN
                  - Templates
                  - Templates
                  - Workloads
                  - Share
                  - Disassociate
                  - Export
                  - Reviews
                  - Answers
                  - Questions
                  - Reports
                  - Versions
                  - Difference
                  - Milestones
                  - Numbers
                  - Checks
                  - Checks
                  - Summaries
                  - Improvements
                  - Notifications
                  - Invitations
                  - Global
                  - Settings
                  - Invitation
                  - Upgra
    overlays:
      - type: APIs.io Search
        url: overlays/wellarchitected-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/wellarchitected-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:wellarchitected
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---