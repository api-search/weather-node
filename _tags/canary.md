---
name: Canary
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/canary.png
url: https://example.com/apis/canary.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Canary
apis:
  - name: synthetics
    description: >-
      <fullname>Amazon CloudWatch Synthetics</fullname> <p>You can use Amazon
      CloudWatch Synthetics to continually monitor your services. You can create
      and manage <i>canaries</i>, which are modular, lightweight scripts that
      monitor your endpoints and APIs from the outside-in. You can set up your
      canaries to run 24 hours a day, once per minute. The canaries help you
      check the availability and latency of your web services and troubleshoot
      anomalies by investigating load time data, screenshots of the UI, logs,
      and metrics. The canaries seamlessly integrate with CloudWatch ServiceLens
      to help you trace the causes of impacted nodes in your applications. For
      more information, see <a
      href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ServiceLens.html">Using
      ServiceLens to Monitor the Health of Your Applications</a> in the
      <i>Amazon CloudWatch User Guide</i>.</p> <p>Before you create and manage
      canaries, be aware of the security considerations. For more information,
      see <a
      href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/servicelens_canaries_security.html">Security
      Considerations for Synthetics Canaries</a>.</p>
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
            title: synthetics
          paths:
            /group/{groupIdentifier}/associate:
              PATCH:
                summary: AssociateResource
                description: >-
                  <p>Associates a canary with a group. Using groups can help you
                  with managing and automating your canaries, and you can also
                  view aggregated run results and statistics for all canaries in
                  a group. </p> <p>You must run this operation in the Region
                  where the canary exists.</p>
                tags:
                  - Associate
                  - Resources
                  - Identifiers
                  - Associate
            /canary:
              POST:
                summary: CreateCanary
                description: >-
                  <p>Creates a canary. Canaries are scripts that monitor your
                  endpoints and APIs from the outside-in. Canaries help you
                  check the availability and latency of your web services and
                  troubleshoot anomalies by investigating load time data,
                  screenshots of the UI, logs, and metrics. You can set up a
                  canary to run continuously or just once. </p> <p>Do not use
                  <code>CreateCanary</code> to modify an existing canary. Use <a
                  href="https://docs.aws.amazon.com/AmazonSynthetics/latest/APIReference/API_UpdateCanary.html">UpdateCanary</a>
                  instead.</p> <p>To create canaries, you must have the
                  <code>CloudWatchSyntheticsFullAccess</code> policy. If you are
                  creating a new IAM role for the canary, you also need the
                  <code>iam:CreateRole</code>, <code>iam:CreatePolicy</code> and
                  <code>iam:AttachRolePolicy</code> permissions. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Roles">Necessary
                  Roles and Permissions</a>.</p> <p>Do not include secrets or
                  proprietary information in your canary names. The canary name
                  makes up part of the Amazon Resource Name (ARN) for the
                  canary, and the ARN is included in outbound calls over the
                  internet. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/servicelens_canaries_security.html">Security
                  Considerations for Synthetics Canaries</a>.</p>
                tags:
                  - Create
                  - Canary
                  - Identifiers
                  - Associate
                  - Canary
            /group:
              POST:
                summary: CreateGroup
                description: >-
                  <p>Creates a group which you can use to associate canaries
                  with each other, including cross-Region canaries. Using groups
                  can help you with managing and automating your canaries, and
                  you can also view aggregated run results and statistics for
                  all canaries in a group. </p> <p>Groups are global resources.
                  When you create a group, it is replicated across Amazon Web
                  Services Regions, and you can view it and add canaries to it
                  from any Region. Although the group ARN format reflects the
                  Region name where it was created, a group is not constrained
                  to any Region. This means that you can put canaries from
                  multiple Regions into the same group, and then use that group
                  to view and manage all of those canaries in a single view.</p>
                  <p>Groups are supported in all Regions except the Regions that
                  are disabled by default. For more information about these
                  Regions, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/rande-manage.html#rande-manage-enable">Enabling
                  a Region</a>.</p> <p>Each group can contain as many as 10
                  canaries. You can have as many as 20 groups in your account.
                  Any single canary can be a member of up to 10 groups.</p>
                tags:
                  - Create
                  - Group
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
            /canary/{name}:
              PATCH:
                summary: UpdateCanary
                description: >-
                  <p>Updates the configuration of a canary that has already been
                  created.</p> <p>You can't use this operation to update the
                  tags of an existing canary. To change the tags of an existing
                  canary, use <a
                  href="https://docs.aws.amazon.com/AmazonSynthetics/latest/APIReference/API_TagResource.html">TagResource</a>.</p>
                tags:
                  - Update
                  - Canary
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
            /group/{groupIdentifier}:
              GET:
                summary: GetGroup
                description: >-
                  <p>Returns information about one group. Groups are a global
                  resource, so you can use this operation from any Region.</p>
                tags:
                  - Get
                  - Group
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
            /canaries:
              POST:
                summary: DescribeCanaries
                description: >-
                  <p>This operation returns a list of the canaries in your
                  account, along with full details about each canary.</p>
                  <p>This operation supports resource-level authorization using
                  an IAM policy and the <code>Names</code> parameter. If you
                  specify the <code>Names</code> parameter, the operation is
                  successful only if you have authorization to view all the
                  canaries that you specify in your request. If you do not have
                  permission to view any of the canaries, the request fails with
                  a 403 response.</p> <p>You are required to use the
                  <code>Names</code> parameter if you are logged on to a user or
                  role that has an IAM policy that restricts which canaries that
                  you are allowed to view. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Restricted.html">
                  Limiting a user to viewing specific canaries</a>.</p>
                tags:
                  - Describe
                  - Canaries
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
            /canaries/last-run:
              POST:
                summary: DescribeCanariesLastRun
                description: >-
                  <p>Use this operation to see information from the most recent
                  run of each canary that you have created.</p> <p>This
                  operation supports resource-level authorization using an IAM
                  policy and the <code>Names</code> parameter. If you specify
                  the <code>Names</code> parameter, the operation is successful
                  only if you have authorization to view all the canaries that
                  you specify in your request. If you do not have permission to
                  view any of the canaries, the request fails with a 403
                  response.</p> <p>You are required to use the
                  <code>Names</code> parameter if you are logged on to a user or
                  role that has an IAM policy that restricts which canaries that
                  you are allowed to view. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Restricted.html">
                  Limiting a user to viewing specific canaries</a>.</p>
                tags:
                  - Describe
                  - Canaries
                  - Last
                  - Runs
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
            /runtime-versions:
              POST:
                summary: DescribeRuntimeVersions
                description: >-
                  <p>Returns a list of Synthetics canary runtime versions. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries_Library.html">
                  Canary Runtime Versions</a>.</p>
                tags:
                  - Describe
                  - Runtime
                  - Versions
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
            /group/{groupIdentifier}/disassociate:
              PATCH:
                summary: DisassociateResource
                description: >-
                  <p>Removes a canary from a group. You must run this operation
                  in the Region where the canary exists.</p>
                tags:
                  - Disassociate
                  - Resources
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
            /canary/{name}/runs:
              POST:
                summary: GetCanaryRuns
                description: <p>Retrieves a list of runs for a specified canary.</p>
                tags:
                  - Get
                  - Canary
                  - Runs
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
            /resource/{resourceArn}/groups:
              POST:
                summary: ListAssociatedGroups
                description: >-
                  <p>Returns a list of the groups that the specified canary is
                  associated with. The canary that you specify must be in the
                  current Region.</p>
                tags:
                  - Lists
                  - Associated
                  - Groups
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
            /group/{groupIdentifier}/resources:
              POST:
                summary: ListGroupResources
                description: >-
                  <p>This operation returns a list of the ARNs of the canaries
                  that are associated with the specified group.</p>
                tags:
                  - Lists
                  - Group
                  - Resources
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
                  - Resources
            /groups:
              POST:
                summary: ListGroups
                description: >-
                  <p>Returns a list of all groups in the account, displaying
                  their names, unique IDs, and ARNs. The groups from all Regions
                  are returned.</p>
                tags:
                  - Lists
                  - Groups
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
                  - Resources
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
                  - Resources
            /canary/{name}/start:
              POST:
                summary: StartCanary
                description: >-
                  <p>Use this operation to run a canary that has already been
                  created. The frequency of the canary runs is determined by the
                  value of the canary's <code>Schedule</code>. To see a canary's
                  schedule, use <a
                  href="https://docs.aws.amazon.com/AmazonSynthetics/latest/APIReference/API_GetCanary.html">GetCanary</a>.</p>
                tags:
                  - Start
                  - Canary
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
                  - Resources
                  - Start
            /canary/{name}/stop:
              POST:
                summary: StopCanary
                description: >-
                  <p>Stops the canary to prevent all future runs. If the canary
                  is currently running,the run that is in progress completes on
                  its own, publishes metrics, and uploads artifacts, but it is
                  not recorded in Synthetics as a completed run.</p> <p>You can
                  use <code>StartCanary</code> to start it running again with
                  the canary’s current schedule at any point in the fu
                tags:
                  - Stop
                  - Canary
                  - Identifiers
                  - Associate
                  - Canary
                  - Group
                  - Names
                  - Canaries
                  - Last
                  - Runs
                  - Runtime
                  - Versions
                  - Disassociate
                  - Runs
                  - ARN
                  - Groups
                  - Resources
                  - Start
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/synthetics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/synthetics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:synthetics
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---