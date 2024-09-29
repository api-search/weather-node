---
name: Backups
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/backups.png
url: https://example.com/apis/backups.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Backups
apis:
  - name: nimble
    description: >-
      <p>Welcome to the Amazon Nimble Studio API reference. This API reference
      provides methods, schema, resources, parameters, and more to help you get
      the most out of Nimble Studio.</p> <p>Nimble Studio is a virtual studio
      that empowers visual effects, animation, and interactive content teams to
      create content securely within a scalable, private cloud service.</p>
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
            title: nimble
          paths:
            /2020-08-01/studios/{studioId}/eula-acceptances:
              GET:
                summary: ListEulaAcceptances
                description: <p>List EULA acceptances.</p>
                tags:
                  - Lists
                  - EULA
                  - Acceptances
                  - Identifiers
                  - EULA
                  - Acceptances
            /2020-08-01/studios/{studioId}/launch-profiles:
              GET:
                summary: ListLaunchProfiles
                description: <p>List all the launch profiles a studio.</p>
                tags:
                  - Lists
                  - Launch
                  - Profiles
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
            /2020-08-01/studios/{studioId}/streaming-images:
              GET:
                summary: ListStreamingImages
                description: >-
                  <p>List the streaming image resources available to this
                  studio.</p> <p>This list will contain both images provided by
                  Amazon Web Services, as well as streaming images that you have
                  created in your studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Images
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
            /2020-08-01/studios/{studioId}/streaming-sessions:
              GET:
                summary: ListStreamingSessions
                description: <p>Lists the streaming sessions in a studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/streams:
              POST:
                summary: CreateStreamingSessionStream
                description: >-
                  <p>Creates a streaming session stream for a streaming
                  session.</p> <p>After invoking this API, invoke
                  GetStreamingSessionStream with the returned streamId to poll
                  the resource until it is in the <code>READY</code> state.</p>
                tags:
                  - Create
                  - Streaming
                  - Sessions
                  - Stream
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
            /2020-08-01/studios:
              GET:
                summary: ListStudios
                description: >-
                  <p>List studios in your Amazon Web Services accounts in the
                  requested Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Studios
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
            /2020-08-01/studios/{studioId}/studio-components:
              GET:
                summary: ListStudioComponents
                description: <p>Lists the <code>StudioComponents</code> in a studio.</p>
                tags:
                  - Lists
                  - Studios
                  - Components
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}:
              PATCH:
                summary: UpdateLaunchProfile
                description: <p>Update a launch profile.</p>
                tags:
                  - Update
                  - Launch
                  - Profiles
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/membership/{principalId}:
              PATCH:
                summary: UpdateLaunchProfileMember
                description: <p>Update a user persona in launch profile membership.</p>
                tags:
                  - Update
                  - Launch
                  - Profiles
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
            /2020-08-01/studios/{studioId}/streaming-images/{streamingImageId}:
              PATCH:
                summary: UpdateStreamingImage
                description: <p>Update streaming image.</p>
                tags:
                  - Update
                  - Streaming
                  - Images
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}:
              GET:
                summary: GetStreamingSession
                description: >-
                  <p>Gets StreamingSession resource.</p> <p>Invoke this
                  operation to poll for a streaming session state while creating
                  or deleting a session.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}:
              PATCH:
                summary: UpdateStudio
                description: >-
                  <p>Update a Studio resource.</p> <p>Currently, this operation
                  only supports updating the displayName of your studio.</p>
                tags:
                  - Update
                  - Studios
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
            /2020-08-01/studios/{studioId}/studio-components/{studioComponentId}:
              PATCH:
                summary: UpdateStudioComponent
                description: <p>Updates a studio component resource.</p>
                tags:
                  - Update
                  - Studios
                  - Components
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/studios/{studioId}/membership/{principalId}:
              GET:
                summary: GetStudioMember
                description: <p>Get a user's membership in a studio.</p>
                tags:
                  - Get
                  - Studios
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/eulas/{eulaId}:
              GET:
                summary: GetEula
                description: <p>Get EULA.</p>
                tags:
                  - Get
                  - EULA
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/details:
              GET:
                summary: GetLaunchProfileDetails
                description: >-
                  <p>Launch profile details include the launch profile resource
                  and summary information of resources that are used by, or
                  available to, the launch profile. This includes the name and
                  description of all studio components used by the launch
                  profiles, and the name and description of streaming images
                  that can be used with this launch profile.</p>
                tags:
                  - Get
                  - Launch
                  - Profiles
                  - Details
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/init:
              GET:
                summary: GetLaunchProfileInitialization
                description: <p>Get a launch profile initialization.</p>
                tags:
                  - Get
                  - Launch
                  - Profiles
                  - Initialization
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
            /2020-08-01/studios/{studioId}/streaming-session-backups/{backupId}:
              GET:
                summary: GetStreamingSessionBackup
                description: >-
                  <p>Gets <code>StreamingSessionBackup</code> resource.</p>
                  <p>Invoke this operation to poll for a streaming session
                  backup while stopping a streaming session.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Backup
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/streams/{streamId}:
              GET:
                summary: GetStreamingSessionStream
                description: >-
                  <p>Gets a StreamingSessionStream for a streaming session.</p>
                  <p>Invoke this operation to poll the resource after invoking
                  <code>CreateStreamingSessionStream</code>.</p> <p>After the
                  <code>StreamingSessionStream</code> changes to the
                  <code>READY</code> state, the url property will contain a
                  stream to be used with the DCV streaming client.</p>
                tags:
                  - Get
                  - Streaming
                  - Sessions
                  - Stream
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
            /2020-08-01/eulas:
              GET:
                summary: ListEulas
                description: <p>List EULAs.</p>
                tags:
                  - Lists
                  - Eulas
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/launch-profiles/{launchProfileId}/membership:
              POST:
                summary: PutLaunchProfileMembers
                description: >-
                  <p>Add/update users with given persona to launch profile
                  membership.</p>
                tags:
                  - Put
                  - Launch
                  - Profiles
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/streaming-session-backups:
              GET:
                summary: ListStreamingSessionBackups
                description: <p>Lists the backups of a streaming session in a studio.</p>
                tags:
                  - Lists
                  - Streaming
                  - Sessions
                  - Backups
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/studios/{studioId}/membership:
              POST:
                summary: PutStudioMembers
                description: >-
                  <p>Add/update users with given persona to studio
                  membership.</p>
                tags:
                  - Put
                  - Studios
                  - Members
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
            /2020-08-01/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deletes the tags for a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/start:
              POST:
                summary: StartStreamingSession
                description: >-
                  <p>Transitions sessions from the <code>STOPPED</code> state
                  into the <code>READY</code> state. The
                  <code>START_IN_PROGRESS</code> state is the intermediate state
                  between the <code>STOPPED</code> and <code>READY</code>
                  states.</p>
                tags:
                  - Start
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
            /2020-08-01/studios/{studioId}/sso-configuration:
              PUT:
                summary: StartStudioSSOConfigurationRepair
                description: >-
                  <p>Repairs the IAM Identity Center configuration for a given
                  studio.</p> <p>If the studio has a valid IAM Identity Center
                  configuration currently associated with it, this operation
                  will fail with a validation error.</p> <p>If the studio does
                  not have a valid IAM Identity Center configuration currently
                  associated with it, then a new IAM Identity Center application
                  is created for the studio and the studio is changed to the
                  <code>READY</code> state.</p> <p>After the IAM Identity Center
                  application is repaired, you must use the Amazon Nimble Studio
                  console to add administrators and users to your studio.</p>
                tags:
                  - Start
                  - Studios
                  - Configurations
                  - Repair
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
                  - SSO
                  - Configurations
            /2020-08-01/studios/{studioId}/streaming-sessions/{sessionId}/stop:
              POST:
                summary: StopStreamingSession
                description: >-
                  <p>Transitions sessions from the <code>READY</code> state into
                  the <code>STOPPED</code> state. The
                  <code>STOP_IN_PROGRESS</code> state is the intermediate state
                  between the <code>READY</code> and <code>STOPPED</code> s
                tags:
                  - Stop
                  - Streaming
                  - Sessions
                  - Identifiers
                  - EULA
                  - Acceptances
                  - Launch
                  - Profiles
                  - Streaming
                  - Images
                  - Sessions
                  - Sessions
                  - Streams
                  - '2020'
                  - '08'
                  - '01'
                  - Studios
                  - Studios
                  - Components
                  - Profiles
                  - Membership
                  - Principals
                  - Images
                  - Components
                  - Details
                  - Initialize
                  - Backups
                  - Backup
                  - Stream
                  - Eulas
                  - ARN
                  - Start
                  - SSO
                  - Configurations
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/nimble-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/nimble-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:nimble
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---