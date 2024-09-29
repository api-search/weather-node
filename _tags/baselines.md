---
name: Baselines
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/baselines.png
url: https://example.com/apis/baselines.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Baselines
apis:
  - name: controltower
    description: >-
      <p>These interfaces allow you to apply the Amazon Web Services library of
      pre-defined <i>controls</i> to your organizational units,
      programmatically. In Amazon Web Services Control Tower, the terms
      "control" and "guardrail" are synonyms.</p> <p>To call these APIs, you'll
      need to know:</p> <ul> <li> <p>the <code>controlIdentifier</code> for the
      control--or guardrail--you are targeting.</p> </li> <li> <p>the ARN
      associated with the target organizational unit (OU), which we call the
      <code>targetIdentifier</code>.</p> </li> <li> <p>the ARN associated with a
      resource that you wish to tag or untag.</p> </li> </ul> <p> <b>To get the
      <code>controlIdentifier</code> for your Amazon Web Services Control Tower
      control:</b> </p> <p>The <code>controlIdentifier</code> is an ARN that is
      specified for each control. You can view the
      <code>controlIdentifier</code> in the console on the <b>Control
      details</b> page, as well as in the documentation.</p> <p>The
      <code>controlIdentifier</code> is unique in each Amazon Web Services
      Region for each control. You can find the <code>controlIdentifier</code>
      for each Region and control in the <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-metadata-tables.html">Tables
      of control metadata</a> in the <i>Amazon Web Services Control Tower User
      Guide.</i> </p> <p>A quick-reference list of control identifers for the
      Amazon Web Services Control Tower legacy <i>Strongly recommended</i> and
      <i>Elective</i> controls is given in <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html.html">Resource
      identifiers for APIs and controls</a> in the <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html">Controls
      reference guide section</a> of the <i>Amazon Web Services Control Tower
      User Guide</i>. Remember that <i>Mandatory</i> controls cannot be added or
      removed.</p> <note> <p> <b>ARN format:</b>
      <code>arn:aws:controltower:{REGION}::control/{CONTROL_NAME}</code> </p>
      <p> <b>Example:</b> </p> <p>
      <code>arn:aws:controltower:us-west-2::control/AWS-GR_AUTOSCALING_LAUNCH_CONFIG_PUBLIC_IP_DISABLED</code>
      </p> </note> <p> <b>To get the <code>targetIdentifier</code>:</b> </p>
      <p>The <code>targetIdentifier</code> is the ARN for an OU.</p> <p>In the
      Amazon Web Services Organizations console, you can find the ARN for the OU
      on the <b>Organizational unit details</b> page associated with that
      OU.</p> <note> <p> <b>OU ARN format:</b> </p> <p>
      <code>arn:${Partition}:organizations::${MasterAccountId}:ou/o-${OrganizationId}/ou-${OrganizationalUnitId}</code>
      </p> </note> <p class="title"> <b>Details and examples</b> </p> <ul> <li>
      <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">Control
      API input and output examples with CLI</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/enable-controls.html">Enable
      controls with CloudFormation</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-metadata-tables.html">Control
      metadata tables</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/control-identifiers.html">List
      of identifiers for legacy controls</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/controls.html">Controls
      reference guide</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/controls-reference.html">Controls
      library groupings</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/creating-resources-with-cloudformation.html">Creating
      Amazon Web Services Control Tower resources with Amazon Web Services
      CloudFormation</a> </p> </li> </ul> <p>To view the open source resource
      repository on GitHub, see <a
      href="https://github.com/aws-cloudformation/aws-cloudformation-resource-providers-controltower">aws-cloudformation/aws-cloudformation-resource-providers-controltower</a>
      </p> <p> <b>Recording API Requests</b> </p> <p>Amazon Web Services Control
      Tower supports Amazon Web Services CloudTrail, a service that records
      Amazon Web Services API calls for your Amazon Web Services account and
      delivers log files to an Amazon S3 bucket. By using information collected
      by CloudTrail, you can determine which requests the Amazon Web Services
      Control Tower service received, who made the request and when, and so on.
      For more about Amazon Web Services Control Tower and its support for
      CloudTrail, see <a
      href="https://docs.aws.amazon.com/controltower/latest/userguide/logging-using-cloudtrail.html">Logging
      Amazon Web Services Control Tower Actions with Amazon Web Services
      CloudTrail</a> in the Amazon Web Services Control Tower User Guide. To
      learn more about CloudTrail, including how to turn it on and find your log
      files, see the Amazon Web Services CloudTrail User Guide.</p>
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
            title: controltower
          paths:
            /create-landingzone:
              POST:
                summary: CreateLandingZone
                description: >-
                  <p>Creates a new landing zone. This API call starts an
                  asynchronous operation that creates and configures a landing
                  zone, based on the parameters specified in the manifest JSON
                  file.</p>
                tags:
                  - Create
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
            /delete-landingzone:
              POST:
                summary: DeleteLandingZone
                description: >-
                  <p>Decommissions a landing zone. This API call starts an
                  asynchronous operation that deletes Amazon Web Services
                  Control Tower resources deployed in accounts managed by Amazon
                  Web Services Control Tower.</p>
                tags:
                  - Delete
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
            /disable-baseline:
              POST:
                summary: DisableBaseline
                description: >-
                  <p>Disable an <code>EnabledBaseline</code> resource on the
                  specified Target. This API starts an asynchronous operation to
                  remove all resources deployed as part of the baseline
                  enablement. The resource will vary depending on the enabled
                  baseline.</p>
                tags:
                  - Disable
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
            /disable-control:
              POST:
                summary: DisableControl
                description: >-
                  <p>This API call turns off a control. It starts an
                  asynchronous operation that deletes AWS resources on the
                  specified organizational unit and the accounts it contains.
                  The resources will vary according to the control that you
                  specify. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Disable
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
            /enable-baseline:
              POST:
                summary: EnableBaseline
                description: >-
                  <p>Enable (apply) a <code>Baseline</code> to a Target. This
                  API starts an asynchronous operation to deploy resources
                  specified by the <code>Baseline</code> to the specified
                  Target.</p>
                tags:
                  - Enable
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
            /enable-control:
              POST:
                summary: EnableControl
                description: >-
                  <p>This API call activates a control. It starts an
                  asynchronous operation that creates Amazon Web Services
                  resources on the specified organizational unit and the
                  accounts it contains. The resources created will vary
                  according to the control that you specify. For usage examples,
                  see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Enable
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
            /get-baseline:
              POST:
                summary: GetBaseline
                description: >-
                  <p>Retrieve details about an existing <code>Baseline</code>
                  resource by specifying its identifier.</p>
                tags:
                  - Get
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
            /get-baseline-operation:
              POST:
                summary: GetBaselineOperation
                description: >-
                  <p>Returns the details of an asynchronous baseline operation,
                  as initiated by any of these APIs:
                  <code>EnableBaseline</code>, <code>DisableBaseline</code>,
                  <code>UpdateEnabledBaseline</code>,
                  <code>ResetEnabledBaseline</code>. A status message is
                  displayed in case of operation failure.</p>
                tags:
                  - Get
                  - Baselines
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
            /get-control-operation:
              POST:
                summary: GetControlOperation
                description: >-
                  <p>Returns the status of a particular
                  <code>EnableControl</code> or <code>DisableControl</code>
                  operation. Displays a message in case of error. Details for an
                  operation are available for 90 days. For usage examples, see
                  <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Get
                  - Control
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
            /get-enabled-baseline:
              POST:
                summary: GetEnabledBaseline
                description: >-
                  <p>Retrieve details of an <code>EnabledBaseline</code>
                  resource by specifying its identifier.</p>
                tags:
                  - Get
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-enabled-control:
              POST:
                summary: GetEnabledControl
                description: >-
                  <p>Retrieves details about an enabled control. For usage
                  examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Get
                  - Enabled
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-landingzone:
              POST:
                summary: GetLandingZone
                description: >-
                  <p>Returns details about the landing zone. Displays a message
                  in case of error.</p>
                tags:
                  - Get
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /get-landingzone-operation:
              POST:
                summary: GetLandingZoneOperation
                description: >-
                  <p>Returns the status of the specified landing zone operation.
                  Details for an operation are available for 60 days.</p>
                tags:
                  - Get
                  - Landing
                  - Zones
                  - Operation
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
            /list-baselines:
              POST:
                summary: ListBaselines
                description: <p>Returns a summary list of all available baselines.</p>
                tags:
                  - Lists
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
            /list-enabled-baselines:
              POST:
                summary: ListEnabledBaselines
                description: >-
                  <p>Returns a list of summaries describing
                  <code>EnabledBaseline</code> resources. You can filter the
                  list by the corresponding <code>Baseline</code> or
                  <code>Target</code> of the <code>EnabledBaseline</code>
                  resources.</p>
                tags:
                  - Lists
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
            /list-enabled-controls:
              POST:
                summary: ListEnabledControls
                description: >-
                  <p>Lists the controls enabled by Amazon Web Services Control
                  Tower on the specified organizational unit and the accounts it
                  contains. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Lists
                  - Enabled
                  - Controls
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
            /list-landingzones:
              POST:
                summary: ListLandingZones
                description: >-
                  <p>Returns the landing zone ARN for the landing zone deployed
                  in your managed account. This API also creates an ARN for
                  existing accounts that do not yet have a landing zone ARN.
                  </p> <p>Returns one landing zone ARN.</p>
                tags:
                  - Lists
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes tags from a resource. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i>
                  </a>.</p>
                tags:
                  - Untag
                  - Resources
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
            /reset-enabled-baseline:
              POST:
                summary: ResetEnabledBaseline
                description: >-
                  <p>Re-enables an <code>EnabledBaseline</code> resource. For
                  example, this API can re-apply the existing
                  <code>Baseline</code> after a new member account is moved to
                  the target OU.</p>
                tags:
                  - Reset
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
            /reset-landingzone:
              POST:
                summary: ResetLandingZone
                description: >-
                  <p>This API call resets a landing zone. It starts an
                  asynchronous operation that resets the landing zone to the
                  parameters specified in its original configuration.</p>
                tags:
                  - Reset
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
            /update-enabled-baseline:
              POST:
                summary: UpdateEnabledBaseline
                description: >-
                  <p>Updates an <code>EnabledBaseline</code> resource's applied
                  parameters or version.</p>
                tags:
                  - Update
                  - Enabled
                  - Baselines
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Update
            /update-enabled-control:
              POST:
                summary: UpdateEnabledControl
                description: >-
                  <p> Updates the configuration of an already enabled
                  control.</p> <p>If the enabled control shows an
                  <code>EnablementStatus</code> of SUCCEEDED, supply parameters
                  that are different from the currently configured parameters.
                  Otherwise, Amazon Web Services Control Tower will not accept
                  the request.</p> <p>If the enabled control shows an
                  <code>EnablementStatus</code> of FAILED, Amazon Web Services
                  Control Tower will update the control to match any valid
                  parameters that you supply.</p> <p>If the
                  <code>DriftSummary</code> status for the control shows as
                  DRIFTED, you cannot call this API. Instead, you can update the
                  control by calling <code>DisableControl</code> and again
                  calling <code>EnableControl</code>, or you can run an
                  extending governance operation. For usage examples, see <a
                  href="https://docs.aws.amazon.com/controltower/latest/userguide/control-api-examples-short.html">
                  <i>the Amazon Web Services Control Tower User Guide</i> </a>
                  </p>
                tags:
                  - Update
                  - Enabled
                  - Control
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Update
            /update-landingzone:
              POST:
                summary: UpdateLandingZone
                description: >-
                  <p>This API call updates the landing zone. It starts an
                  asynchronous operation that updates the landing zone based on
                  the new landing zone version, or on the changed parameters
                  specified in the updated manifest
                tags:
                  - Update
                  - Landing
                  - Zones
                  - Create
                  - Landing Zones
                  - Delete
                  - Disable
                  - Baselines
                  - Control
                  - Enable
                  - Get
                  - Operation
                  - Enabled
                  - Lists
                  - Baselines
                  - Controls
                  - Landing Zones
                  - ARN
                  - Reset
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/controltower-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/controltower-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:controltower
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---