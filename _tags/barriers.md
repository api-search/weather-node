---
name: Barriers
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/barriers.png
url: https://example.com/apis/barriers.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Barriers
apis:
  - aid: box:box-shield-information-barriers-api
    name: Box Shield Information Barriers API
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.box.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.box.com/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Box Shield Information Barriers API
          paths:
            /shield_information_barriers/{shield_information_barrier_id}:
              get:
                summary: Get shield information barrier with specified ID
                tags:
                  - Get
                  - Shield
                  - Information
                  - Barrier
                  - With
                  - Specified
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                description: Get shield information barrier based on provided ID.
            /shield_information_barriers/change_status:
              post:
                summary: >-
                  Add changed status of shield information barrier with
                  specified ID
                tags:
                  - Add
                  - Changed
                  - Status
                  - Of
                  - Shield
                  - Information
                  - Barrier
                  - With
                  - Specified
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: >-
                  Change status of shield information barrier with the specified
                  ID.
            /shield_information_barriers:
              get:
                summary: List shield information barriers
                tags:
                  - List
                  - Shield
                  - Information
                  - Barriers
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: |-
                  Retrieves a list of shield information barrier objects
                  for the enterprise of JWT.
              post:
                summary: Create shield information barrier
                tags:
                  - Create
                  - Shield
                  - Information
                  - Barrier
                  - Shield_information_barriers
                  - Shield_information_barrier_id
                  - Change_status
                description: |-
                  Creates a shield information barrier to
                  separate individuals/groups within the same
                  firm and prevents confidential information passing b
    overlays:
      - type: APIs.io Search
        url: overlays/shield-information-barriers-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/shield-information-barriers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---