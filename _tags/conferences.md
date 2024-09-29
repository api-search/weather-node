---
name: Conferences
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/conferences.png
url: https://example.com/apis/conferences.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Conferences
apis:
  - aid: twilio:twilio-insights-api
    name: Twilio Insights API
    description: Needs description.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/docs/
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/docs/
      - type: OpenAPI
        data:
          info:
            title: Twilio - Insights
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Voice/Settings:
              description: 'TODO: Resource-level docs'
              get:
                description: Get the Voice Insights Settings.
                tags:
                  - Voice
                  - Settings
              post:
                description: Update a specific Voice Insights Setting.
                tags:
                  - Voice
                  - Settings
            /v1/Voice/{CallSid}/Annotation:
              description: 'TODO: Resource-level docs'
              post:
                description: Update an Annotation for a specific Call.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
              get:
                description: Get the Annotation for a specific Call.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
            /v1/Voice/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
            /v1/Voice/Summaries:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of Call Summaries.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
            /v1/Conferences/{ConferenceSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a specific Conference Summary.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
            /v1/Conferences:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of Conference Summaries.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
            /v1/Conferences/{ConferenceSid}/Participants/{ParticipantSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Get a specific Conference Participant Summary for a
                  Conference.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
            /v1/Conferences/{ConferenceSid}/Participants:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Get a list of Conference Participants Summaries for a
                  Conference.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
            /v1/Voice/{CallSid}/Events:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of Call Insight Events for a Call.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
            /v1/Voice/{CallSid}/Metrics:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of Call Metrics for a Call.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
            /v1/Voice/{CallSid}/Summary:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a specific Call Summary.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
                  - Summary
            /v1/Video/Rooms/{RoomSid}/Participants/{ParticipantSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Get Video Log Analyzer data for a Room Participant.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
                  - Summary
                  - Video
                  - Rooms
                  - Room
            /v1/Video/Rooms/{RoomSid}/Participants:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of room participants.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
                  - Summary
                  - Video
                  - Rooms
                  - Room
            /v1/Video/Rooms/{RoomSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Get Video Log Analyzer data for a Room.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
                  - Summary
                  - Video
                  - Rooms
                  - Room
            /v1/Video/Rooms:
              description: 'TODO: Resource-level docs'
              get:
                description: Get a list of Programmable Video Rooms.
                tags:
                  - Voice
                  - Settings
                  - Call
                  - Sid
                  - Annotation
                  - Summaries
                  - Conferences
                  - Conference
                  - Participants
                  - Participant
                  - Events
                  - Metrics
                  - Summary
                  - Video
                  - Rooms
                  - Room
          tags:
            - name: InsightsV1Annotation
            - name: InsightsV1Call
            - name: InsightsV1CallSummaries
            - name: InsightsV1CallSummary
            - name: InsightsV1Conference
            - name: InsightsV1ConferenceParticipant
            - name: InsightsV1Event
            - name: InsightsV1Metric
            - name: InsightsV1Participant
            - name: InsightsV1Room
            - name: InsightsV1Setting
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. Use it with caution.
            - name: Preview
              description: >-
                PLEASE NOTE that this is a Preview product that is subject to
                change. Use it with caution. If you currently do not have
                developer preview access, please contact https://www.twilio
    overlays:
      - type: APIs.io Search
        url: overlays/insights-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/insights-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---