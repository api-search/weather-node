---
name: Chinese
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/chinese.png
url: https://example.com/apis/chinese.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Chinese
apis:
  - name: FactSet Entity API
    description: ' FactSet’s Entity API provides access to FactSet’s complete security and entity level symbology, comprehensive entity reference data, and all of the necessary relationships and connections to create a foundation that tightly correlates disparate sources o'
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-entity-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-entity-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-entity-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-entity-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-entity-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-entity-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Entity API
          tags:
            - name: Entity Reference
              description: >-
                Retrieve Entity Reference information for a list of securities,
                such as Parent Equity and Business Descriptions.
            - name: Entity Securities
              description: >-
                Retrieve the related equity or fixed income securities for a
                given list of ids
            - name: Entity Structure
              description: >-
                Retrieve the Entities corporate structure, its subsidiaries and
                related entity ids.
            - name: Entity Reference Chinese
            - name: Historical Credit Parent
          paths:
            /factset-entity/v1/entity-references:
              get:
                summary: Returns an entity reference profiles for an individual entity
                description: >
                  Returns an Entity reference profile for the requested Entity
                  Id(s). Data points include - Ultimate Parent Id, Credit Parent
                  Id, Headquarters location details, Website URL, and Business
                  Description.
                tags:
                  - Returns
                  - An
                  - Entity
                  - Reference
                  - Profiles
                  - For
                  - Individual
                  - Factset
                  - Entity
                  - V1
                  - References
              post:
                summary: Returns an entity reference data for a list of ids.
                description: >
                  Returns an entity reference object for the requested entity
                  ids. Data points include - ultimate parent id, headquarters
                  location details, credit parent id, website, and business
                  description.
                tags:
                  - Returns
                  - An
                  - Entity
                  - Reference
                  - Data
                  - For
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Entity
                  - V1
                  - References
            /factset-entity/v1/entity-securities:
              get:
                summary: >-
                  Returns all Equity Exchange Listings and all debt instruments
                  issued for the requested entity.
                description: >
                  Returns all Equity Exchange Listings (ticker-exchange) and all
                  debt instruments (cusips) issued for the requested entity.
                tags:
                  - Returns
                  - All
                  - Equity
                  - Exchange
                  - Listings
                  - And
                  - Debt
                  - Instruments
                  - Issued
                  - For
                  - The
                  - Requested
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
              post:
                summary: >-
                  Returns all Equity Exchange Listings and all debt instruments
                  issued for the requested entity.
                description: >
                  Returns all Equity Exchange Listings (ticker-exchange) and all
                  debt instruments (cusips) issued for the requested entity.
                tags:
                  - Returns
                  - All
                  - Equity
                  - Exchange
                  - Listings
                  - And
                  - Debt
                  - Instruments
                  - Issued
                  - For
                  - The
                  - Requested
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
            /factset-entity/v1/entity-structures:
              get:
                summary: >-
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                description: >
                  Returns all active or inactive entities below the requested
                  entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - And
                  - Respective
                  - Levels
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
              post:
                summary: >-
                  Returns all active or inactive entities below the requested
                  entity id.
                description: >
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
            /factset-entity/v1/ultimate-entity-structures:
              get:
                summary: >-
                  Returns the full ultimate parent entity hiearachy. Control
                  levels and active status of underlying entities.
                description: >
                  Returns full ultimate entity structure including ultimate
                  parent and all subordinates. Will accept entity from any level
                  of entity structure or active vs. inactive status of entity.
                tags:
                  - Returns
                  - The
                  - Full
                  - Ultimate
                  - Parent
                  - Entity
                  - Hiearachy.
                  - Control
                  - Levels
                  - And
                  - Active
                  - Status
                  - Of
                  - Underlying
                  - Entities.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
              post:
                summary: >-
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                description: >
                  Returns all active or inactive entities and respective levels
                  below the requested entity id.
                tags:
                  - Returns
                  - All
                  - Active
                  - Or
                  - Inactive
                  - Entities
                  - And
                  - Respective
                  - Levels
                  - Below
                  - The
                  - Requested
                  - Entity
                  - Id.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
            /factset-entity/v1/entity-reference-chi:
              get:
                summary: >-
                  Returns entity reference data in Chinese for an individual
                  entity.
                description: >
                  Returns entity reference data in Chinese for the requested
                  Id(s). Data points include Business Description and Entity
                  Name in both simplified and traditional Chinese.
                tags:
                  - Returns
                  - Entity
                  - Reference
                  - Data
                  - In
                  - Chinese
                  - For
                  - An
                  - Individual
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
              post:
                summary: >-
                  Returns entity reference data in Chinese for an individual
                  entity.
                description: >
                  Returns entity reference data in Chinese for the requested
                  Id(s). Data points include Business Description and Entity
                  Name in both simplified and traditional Chinese.
                tags:
                  - Returns
                  - Entity
                  - Reference
                  - Data
                  - In
                  - Chinese
                  - For
                  - An
                  - Individual
                  - Entity.
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
            /factset-entity/v1/hist-credit-parent:
              get:
                summary: Returns historical credit parents for the requested id(s).
                description: >
                  Returns the credit parent for requested fixed income ids.
                  Point in time credit parent retrieval is

                  also available if an asOfDate is provided. The full credit
                  parent history of a security is returned if

                  no asOfDate is provided.


                  This endpoint uses a seven day calendar to account for changes
                  that occur on all seven days of the week.
                tags:
                  - Returns
                  - Historical
                  - Credit
                  - Parents
                  - For
                  - The
                  - Requested
                  - Id(s).
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
                  - Hist
                  - Credit
                  - Parent
              post:
                summary: Returns historical credit parents for the requested id(s).
                description: >
                  Returns the credit parent for requested fixed income ids.
                  Point in time credit parent retrieval is

                  also available if an asOfDate is provided. The full credit
                  parent history of a security is returned if

                  no asOfDate is provided.


                  This endpoint uses a seven day calendar to account for changes
                  that occur on all seven days of the week.
                tags:
                  - Returns
                  - Historical
                  - Credit
                  - Parents
                  - For
                  - The
                  - Requested
                  - Id(s).
                  - Factset
                  - Entity
                  - V1
                  - References
                  - Securities
                  - Structures
                  - Ultimate
                  - Reference
                  - Chi
                  - Hist
                  - Credit
                  - Pare
    overlays:
      - type: APIs.io Search
        url: overlays/entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/entity-openapi-api-evangelist-ratings.yml
    aid: factset:factset-entity-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---