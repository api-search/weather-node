---
name: Confidence
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/confidence.png
url: https://example.com/apis/confidence.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Confidence
apis:
  - name: FactSet Documents Distributor - CallStreet Events
    description: >-
      CallStreet Events contains all the Documents Distributor APIs that offer
      events data such as Events Audio and Near Real-Time Transcripts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/documents-distributor-callstreet-events
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/documents-distributor-callstreet-events#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Documents Distributor - CallStreet Events
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: >-
              https://developer.factset.com/api-catalog/documents-distributor-callstreet-events
          paths:
            /docs-distributor/audio/v1/history-files:
              get:
                summary: >-
                  Retrieve historical audio recordings and related metadata
                  within FactSet coverage.
                tags:
                  - Retrieve
                  - Historical
                  - Audio
                  - Recordings
                  - And
                  - Related
                  - Metadata
                  - Within
                  - Fact
                  - Set
                  - Coverage.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                description: >

                  * Returns the **untrimmed** historical audio recordings and
                  related metadata dating back from May 10, 2011 to Sep 30,
                  2022.


                  * Returns the **trimmed** historical audio recordings and
                  related metadata dating back from May 10, 2011 to Dec 31,
                  2022.




                  Query parameters can be used to filter and narrow down the
                  results.
            /docs-distributor/audio/v1/list-files:
              get:
                summary: >-
                  Retrieve latest audio recordings and related metadata within
                  FactSet coverage.
                tags:
                  - Retrieve
                  - Latest
                  - Audio
                  - Recordings
                  - And
                  - Related
                  - Metadata
                  - Within
                  - Fact
                  - Set
                  - Coverage.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                description: >-
                  Returns the latest audio recordings. Query parameters can be
                  used to filter and narrow down the results.
            /bulk-documents/nrt/v1/calls:
              get:
                summary: Returns the active calls happening at the moment.
                tags:
                  - Returns
                  - The
                  - Active
                  - Calls
                  - Happening
                  - At
                  - Moment.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                description: Returns the active calls happening at the moment
            /bulk-documents/nrt/v1/list-snippets:
              get:
                summary: Returns the latest transcript snippets from an active call.
                tags:
                  - Returns
                  - The
                  - Latest
                  - Transcript
                  - Snippets
                  - From
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                description: Returns the latest snippets from an active call
            /bulk-documents/nrt/v1/speakerids:
              get:
                summary: >-
                  Returns the latest speakerIds with the confidence scores
                  generated for an active call.
                tags:
                  - Returns
                  - The
                  - Latest
                  - Speaker
                  - Ids
                  - With
                  - Confidence
                  - Scores
                  - Generated
                  - For
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                  - Speakerids
                description: >-
                  Returns the latest speakerIds with the cosine
                  scores(confidence scores) generated for an active call.
            /bulk-documents/nrt/v1/indexed-nrt:
              get:
                summary: >-
                  Returns the  indexed transcript data  in small increments
                  throughout the duration of an active call.
                tags:
                  - Returns
                  - The
                  - Indexed
                  - Transcript
                  - Data
                  - In
                  - Small
                  - Increments
                  - Throughout
                  - Duration
                  - Of
                  - An
                  - Active
                  - Call.
                  - Docs
                  - Distributor
                  - Audio
                  - V1
                  - History
                  - Files
                  - List
                  - Bulk
                  - Documents
                  - Nrt
                  - Calls
                  - Snippets
                  - Speakerids
                  - Indexed
                description: >-
                  Returns the  indexed transcript data  in small increments
                  throughout the duration of an active call.
          tags:
            - name: Events Audio
              description: >-
                The Events Audio API provides access to historical as well as
                the latest audio recordings of various company events covered by
                FactSet.
            - name: Near Real-Time Transcripts
              description: >-
                The Near Real-Time Transcripts API enables access to Near
                Real-time Transcripts provided by CallStreet to tim
    overlays:
      - type: APIs.io Search
        url: overlays/documents-distributor-callstreet-events-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/documents-distributor-callstreet-events-openapi-api-evangelist-ratings.yml
    aid: factset:factset-documents-distributor-callstreet-events
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---