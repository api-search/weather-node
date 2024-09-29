---
name: Baidu
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/baidu.png
url: https://example.com/apis/baidu.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Baidu
apis:
  - name: pinpoint
    description: <p>Doc Engage API - Amazon Pinpoint API</p>
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
            title: pinpoint
          paths:
            /v1/apps:
              GET:
                summary: GetApps
                description: >-
                  <p>Retrieves information about all the applications that are
                  associated with your Amazon Pinpoint account.</p>
                tags:
                  - Get
                  - Applications
                  - V1
                  - Applications
            /v1/apps/{application-id}/campaigns:
              GET:
                summary: GetCampaigns
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all the campaigns that are associated with
                  an application.</p>
                tags:
                  - Get
                  - Campaigns
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
            /v1/templates/{template-name}/email:
              PUT:
                summary: UpdateEmailTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the email channel.</p>
                tags:
                  - Update
                  - Email
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
            /v1/apps/{application-id}/jobs/export:
              GET:
                summary: GetExportJobs
                description: >-
                  <p>Retrieves information about the status and settings of all
                  the export jobs for an application.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
            /v1/apps/{application-id}/jobs/import:
              GET:
                summary: GetImportJobs
                description: >-
                  <p>Retrieves information about the status and settings of all
                  the import jobs for an application.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
            /v1/templates/{template-name}/inapp:
              PUT:
                summary: UpdateInAppTemplate
                description: >-
                  <p>Updates an existing message template for messages sent
                  through the in-app message channel.</p>
                tags:
                  - Update
                  - In
                  - Applications
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
            /v1/apps/{application-id}/journeys:
              GET:
                summary: ListJourneys
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all the journeys that are associated with
                  an application.</p>
                tags:
                  - Lists
                  - Journeys
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
            /v1/templates/{template-name}/push:
              PUT:
                summary: UpdatePushTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through a push notification channel.</p>
                tags:
                  - Update
                  - Push
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
            /v1/recommenders:
              GET:
                summary: GetRecommenderConfigurations
                description: >-
                  <p>Retrieves information about all the recommender model
                  configurations that are associated with your Amazon Pinpoint
                  account.</p>
                tags:
                  - Get
                  - Recommenders
                  - Configurations
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
            /v1/apps/{application-id}/segments:
              GET:
                summary: GetSegments
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for all the segments that are associated
                  with an application.</p>
                tags:
                  - Get
                  - Segments
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
            /v1/templates/{template-name}/sms:
              PUT:
                summary: UpdateSmsTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the SMS channel.</p>
                tags:
                  - Update
                  - SMS
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
            /v1/templates/{template-name}/voice:
              PUT:
                summary: UpdateVoiceTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the voice channel.</p>
                tags:
                  - Update
                  - Voice
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
            /v1/apps/{application-id}/channels/adm:
              PUT:
                summary: UpdateAdmChannel
                description: >-
                  <p>Enables the ADM channel for an application or updates the
                  status and settings of the ADM channel for an application.</p>
                tags:
                  - Update
                  - ADM
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
            /v1/apps/{application-id}/channels/apns:
              PUT:
                summary: UpdateApnsChannel
                description: >-
                  <p>Enables the APNs channel for an application or updates the
                  status and settings of the APNs channel for an
                  application.</p>
                tags:
                  - Update
                  - Apns
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
            /v1/apps/{application-id}/channels/apns_sandbox:
              PUT:
                summary: UpdateApnsSandboxChannel
                description: >-
                  <p>Enables the APNs sandbox channel for an application or
                  updates the status and settings of the APNs sandbox channel
                  for an application.</p>
                tags:
                  - Update
                  - Apns
                  - Sandbox
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
            /v1/apps/{application-id}/channels/apns_voip:
              PUT:
                summary: UpdateApnsVoipChannel
                description: >-
                  <p>Enables the APNs VoIP channel for an application or updates
                  the status and settings of the APNs VoIP channel for an
                  application.</p>
                tags:
                  - Update
                  - Apns
                  - Voice Over IP
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
            /v1/apps/{application-id}/channels/apns_voip_sandbox:
              PUT:
                summary: UpdateApnsVoipSandboxChannel
                description: >-
                  <p>Enables the APNs VoIP sandbox channel for an application or
                  updates the status and settings of the APNs VoIP sandbox
                  channel for an application.</p>
                tags:
                  - Update
                  - Apns
                  - Voice Over IP
                  - Sandbox
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
            /v1/apps/{application-id}:
              GET:
                summary: GetApp
                description: <p>Retrieves information about an application.</p>
                tags:
                  - Get
                  - Applications
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
            /v1/apps/{application-id}/channels/baidu:
              PUT:
                summary: UpdateBaiduChannel
                description: >-
                  <p>Enables the Baidu channel for an application or updates the
                  status and settings of the Baidu channel for an
                  application.</p>
                tags:
                  - Update
                  - Baidu
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
            /v1/apps/{application-id}/campaigns/{campaign-id}:
              PUT:
                summary: UpdateCampaign
                description: >-
                  <p>Updates the configuration and other settings for a
                  campaign.</p>
                tags:
                  - Update
                  - Campaigns
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
            /v1/apps/{application-id}/channels/email:
              PUT:
                summary: UpdateEmailChannel
                description: >-
                  <p>Enables the email channel for an application or updates the
                  status and settings of the email channel for an
                  application.</p>
                tags:
                  - Update
                  - Email
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
            /v1/apps/{application-id}/endpoints/{endpoint-id}:
              PUT:
                summary: UpdateEndpoint
                description: >-
                  <p>Creates a new endpoint for an application or updates the
                  settings and attributes of an existing endpoint for an
                  application. You can also use this operation to define custom
                  attributes for an endpoint. If an update includes one or more
                  values for a custom attribute, Amazon Pinpoint replaces
                  (overwrites) any existing values with the new values.</p>
                tags:
                  - Update
                  - Endpoints
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
            /v1/apps/{application-id}/eventstream:
              POST:
                summary: PutEventStream
                description: >-
                  <p>Creates a new event stream for an application or updates
                  the settings of an existing event stream for an
                  application.</p>
                tags:
                  - Put
                  - Events
                  - Stream
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
            /v1/apps/{application-id}/channels/gcm:
              PUT:
                summary: UpdateGcmChannel
                description: >-
                  <p>Enables the GCM channel for an application or updates the
                  status and settings of the GCM channel for an application.</p>
                tags:
                  - Update
                  - Gcm
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
            /v1/apps/{application-id}/journeys/{journey-id}:
              PUT:
                summary: UpdateJourney
                description: >-
                  <p>Updates the configuration and other settings for a
                  journey.</p>
                tags:
                  - Update
                  - Journeys
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
            /v1/recommenders/{recommender-id}:
              PUT:
                summary: UpdateRecommenderConfiguration
                description: >-
                  <p>Updates an Amazon Pinpoint configuration for a recommender
                  model.</p>
                tags:
                  - Update
                  - Recommenders
                  - Configurations
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
            /v1/apps/{application-id}/segments/{segment-id}:
              PUT:
                summary: UpdateSegment
                description: >-
                  <p>Creates a new segment for an application or updates the
                  configuration, dimension, and other settings for an existing
                  segment that's associated with an application.</p>
                tags:
                  - Update
                  - Segments
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
            /v1/apps/{application-id}/channels/sms:
              PUT:
                summary: UpdateSmsChannel
                description: >-
                  <p>Enables the SMS channel for an application or updates the
                  status and settings of the SMS channel for an application.</p>
                tags:
                  - Update
                  - SMS
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
            /v1/apps/{application-id}/users/{user-id}:
              GET:
                summary: GetUserEndpoints
                description: >-
                  <p>Retrieves information about all the endpoints that are
                  associated with a specific user ID.</p>
                tags:
                  - Get
                  - Users
                  - Endpoints
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
            /v1/apps/{application-id}/channels/voice:
              PUT:
                summary: UpdateVoiceChannel
                description: >-
                  <p>Enables the voice channel for an application or updates the
                  status and settings of the voice channel for an
                  application.</p>
                tags:
                  - Update
                  - Voice
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
            /v1/apps/{application-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetApplicationDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  metric that applies to an application.</p>
                tags:
                  - Get
                  - Applications
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
            /v1/apps/{application-id}/settings:
              PUT:
                summary: UpdateApplicationSettings
                description: <p>Updates the settings for an application.</p>
                tags:
                  - Update
                  - Applications
                  - Settings
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
            /v1/apps/{application-id}/campaigns/{campaign-id}/activities:
              GET:
                summary: GetCampaignActivities
                description: >-
                  <p>Retrieves information about all the activities for a
                  campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Activities
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
            /v1/apps/{application-id}/campaigns/{campaign-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetCampaignDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  metric that applies to a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
            /v1/apps/{application-id}/campaigns/{campaign-id}/versions/{version}:
              GET:
                summary: GetCampaignVersion
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for a specific version of a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/campaigns/{campaign-id}/versions:
              GET:
                summary: GetCampaignVersions
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all versions of a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/channels:
              GET:
                summary: GetChannels
                description: >-
                  <p>Retrieves information about the history and status of each
                  channel for an application.</p>
                tags:
                  - Get
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/jobs/export/{job-id}:
              GET:
                summary: GetExportJob
                description: >-
                  <p>Retrieves information about the status and settings of a
                  specific export job for an application.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
            /v1/apps/{application-id}/jobs/import/{job-id}:
              GET:
                summary: GetImportJob
                description: >-
                  <p>Retrieves information about the status and settings of a
                  specific import job for an application.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
            /v1/apps/{application-id}/endpoints/{endpoint-id}/inappmessages:
              GET:
                summary: GetInAppMessages
                description: >-
                  <p>Retrieves the in-app messages targeted for the provided
                  endpoint ID.</p>
                tags:
                  - Get
                  - In
                  - Applications
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
            /v1/apps/{application-id}/journeys/{journey-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetJourneyDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  engagement metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
            /v1/apps/{application-id}/journeys/{journey-id}/activities/{journey-activity-id}/execution-metrics:
              GET:
                summary: GetJourneyExecutionActivityMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  execution metric that applies to a journey activity.</p>
                tags:
                  - Get
                  - Journeys
                  - Execution
                  - Activity
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
            /v1/apps/{application-id}/journeys/{journey-id}/execution-metrics:
              GET:
                summary: GetJourneyExecutionMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  execution metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Execution
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
            /v1/apps/{application-id}/journeys/{journey-id}/runs/{run-id}/activities/{journey-activity-id}/execution-metrics:
              GET:
                summary: GetJourneyRunExecutionActivityMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard run
                  execution metric that applies to a journey activity.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - Execution
                  - Activity
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/journeys/{journey-id}/runs/{run-id}/execution-metrics:
              GET:
                summary: GetJourneyRunExecutionMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard run
                  execution metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - Execution
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/journeys/{journey-id}/runs:
              GET:
                summary: GetJourneyRuns
                description: <p>Provides information about the runs of a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/jobs/export:
              GET:
                summary: GetSegmentExportJobs
                description: >-
                  <p>Retrieves information about the status and settings of the
                  export jobs for a segment.</p>
                tags:
                  - Get
                  - Segments
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/jobs/import:
              GET:
                summary: GetSegmentImportJobs
                description: >-
                  <p>Retrieves information about the status and settings of the
                  import jobs for a segment.</p>
                tags:
                  - Get
                  - Segments
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/versions/{version}:
              GET:
                summary: GetSegmentVersion
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for a specific version of a segment that's
                  associated with an application.</p>
                tags:
                  - Get
                  - Segments
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/versions:
              GET:
                summary: GetSegmentVersions
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for all the versions of a specific segment
                  that's associated with an application.</p>
                tags:
                  - Get
                  - Segments
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags (keys and values) from an
                  application, campaign, message template, or segment.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
            /v1/templates/{template-name}/{template-type}/versions:
              GET:
                summary: ListTemplateVersions
                description: >-
                  <p>Retrieves information about all the versions of a specific
                  message template.</p>
                tags:
                  - Lists
                  - Templates
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
            /v1/templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Retrieves information about all the message templates that
                  are associated with your Amazon Pinpoint account.</p>
                tags:
                  - Lists
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
            /v1/phone/number/validate:
              POST:
                summary: PhoneNumberValidate
                description: <p>Retrieves information about a phone number.</p>
                tags:
                  - Phone
                  - Numbers
                  - Validate
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
            /v1/apps/{application-id}/events:
              POST:
                summary: PutEvents
                description: >-
                  <p>Creates a new event to record for endpoints, or creates or
                  updates endpoint data that existing events are associated
                  with.</p>
                tags:
                  - Put
                  - Events
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
            /v1/apps/{application-id}/attributes/{attribute-type}:
              PUT:
                summary: RemoveAttributes
                description: >-
                  <p>Removes one or more custom attributes, of the same
                  attribute type, from the application. Existing endpoints still
                  have the attributes but Amazon Pinpoint will stop capturing
                  new or changed values for these attributes.</p>
                tags:
                  - Removes
                  - Attributes
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
            /v1/apps/{application-id}/messages:
              POST:
                summary: SendMessages
                description: <p>Creates and sends a direct message.</p>
                tags:
                  - Send
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
            /v1/apps/{application-id}/otp:
              POST:
                summary: SendOTPMessage
                description: <p>Send an OTP message</p>
                tags:
                  - Send
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/users-messages:
              POST:
                summary: SendUsersMessages
                description: <p>Creates and sends a message to a list of users.</p>
                tags:
                  - Send
                  - Users
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/endpoints:
              PUT:
                summary: UpdateEndpointsBatch
                description: >-
                  <p>Creates a new batch of endpoints for an application or
                  updates the settings and attributes of a batch of existing
                  endpoints for an application. You can also use this operation
                  to define custom attributes for a batch of endpoints. If an
                  update includes one or more values for a custom attribute,
                  Amazon Pinpoint replaces (overwrites) any existing values with
                  the new values.</p>
                tags:
                  - Update
                  - Endpoints
                  - Batches
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/journeys/{journey-id}/state:
              PUT:
                summary: UpdateJourneyState
                description: <p>Pause, resume or cancels (stops) a journey.</p>
                tags:
                  - Update
                  - Journeys
                  - States
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
            /v1/templates/{template-name}/{template-type}/active-version:
              PUT:
                summary: UpdateTemplateActiveVersion
                description: >-
                  <p>Changes the status of a specific version of a message
                  template to <i>active</i>.</p>
                tags:
                  - Update
                  - Templates
                  - Active
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
                  - Active
            /v1/apps/{application-id}/verify-otp:
              POST:
                summary: VerifyOTPMessage
                description: <p>Verify
                tags:
                  - Verify
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
                  - Active
                  - Veri
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---