---
name: Business
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/business.png
url: https://example.com/apis/business.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Business
apis:
  - name: Adyen Legal Entity API
    description: >-
      The Legal Entity Management API enables you to manage legal entities that
      contain information required for verification.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Legal Entity Management API
          tags:
            - name: Legal entities
            - name: Transfer instruments
            - name: Business lines
            - name: Documents
            - name: Terms of Service
            - name: Hosted Onboarding
            - name: Questionnaires
          paths:
            /businessLines:
              post:
                tags:
                  - Create
                  - Business
                  - Line
                  - Lines
                summary: Create a business line
                description: >+
                  Creates a business line. 


                  This resource contains information about your user's line of
                  business, including their industry and their source of funds.
                  Adyen uses this information to verify your users as required
                  by payment industry regulations. Adyen informs you of the
                  verification results through webhooks or API responses.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /businessLines/{id}:
              delete:
                tags:
                  - Delete
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Delete a business line
                description: |-
                  Deletes a business line.

                   >If you delete a business line linked to a [payment method](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api), it can affect your merchant account's ability to use the [payment method](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings). The business line is removed from all linked merchant accounts.
              get:
                tags:
                  - Get
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Get a business line
                description: Returns the detail of a business line.
              patch:
                tags:
                  - Update
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Update a business line
                description: Updates a business line.
            /documents:
              post:
                tags:
                  - Uploads
                  - Document
                  - For
                  - Verification
                  - Checks
                  - Lines
                  - Identifiers
                  - Documents
                summary: Upload a document for verification checks
                description: |-
                  Uploads a document for verification checks.

                   Adyen uses the information from the [legal entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities) to run automated verification checks. If these checks fail, you will be notified to provide additional documents.

                   You should only upload documents when Adyen requests additional information for the legal entity.

                   >You can upload a maximum of 15 pages for photo IDs.
            /documents/{id}:
              delete:
                tags:
                  - Delete
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Delete a document
                description: Deletes a document.
              get:
                tags:
                  - Get
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Get a document
                description: Returns a document.
              patch:
                tags:
                  - Update
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Update a document
                description: |-
                  Updates a document.

                   >You can upload a maximum of 15 pages for photo IDs.
            /legalEntities:
              post:
                tags:
                  - Create
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Create a legal entity
                description: >+
                  Creates a legal entity. 


                  This resource contains information about the user that will be
                  onboarded in your platform. Adyen uses this information to
                  perform verification checks as required by payment industry
                  regulations. Adyen informs you of the verification results
                  through webhooks or API responses. 


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}:
              get:
                tags:
                  - Get
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Get a legal entity
                description: Returns a legal entity.
              patch:
                tags:
                  - Update
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Update a legal entity
                description: |-
                  Updates a legal entity.

                   >To change the legal entity type, include only the new `type` in your request. To update the `entityAssociations` array, you need to replace the entire array. For example, if the array has 3 entries and you want to remove 1 entry, you need to PATCH the resource with the remaining 2 entries.
            /legalEntities/{id}/businessLines:
              get:
                tags:
                  - Get
                  - All
                  - Business
                  - Lines
                  - Under
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                summary: Get all business lines under a legal entity
                description: Returns the business lines owned by a legal entity.
            /legalEntities/{id}/checkVerificationErrors:
              post:
                tags:
                  - Checks
                  - Legal
                  - Entities
                  - Verification
                  - Errors
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                summary: Check a legal entity's verification errors
                description: >-
                  Returns the verification errors for a legal entity and its
                  supporting entities.
            /legalEntities/{id}/confirmDataReview:
              post:
                tags:
                  - Confirm
                  - Data
                  - Reviews
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                summary: Confirm data review
                description: >-
                  Confirms that your user has reviewed the data for the legal
                  entity specified in the path. Call this endpoint to inform
                  Adyen that your user reviewed and verified that the data is
                  up-to-date. The endpoint returns the timestamp of when Adyen
                  received the request.
            /legalEntities/{id}/onboardingLinks:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - null
                  - Adyen-hosted
                  - Onboarding
                  - Page
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                summary: Get a link to an Adyen-hosted onboarding page
                description: >+
                  Returns a link to an Adyen-hosted onboarding page where you
                  need to redirect your user.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}/pciQuestionnaires:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Details
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                summary: Get PCI questionnaire details
                description: Get a list of signed PCI questionnaires.
            /legalEntities/{id}/pciQuestionnaires/generatePciTemplates:
              post:
                tags:
                  - Generate
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                summary: Generate PCI questionnaire
                description: >-
                  Generates the required PCI questionnaires based on the user's
                  [salesChannel](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/businessLines__reqParam_salesChannels).
            /legalEntities/{id}/pciQuestionnaires/signPciTemplates:
              post:
                tags:
                  - Sign
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                summary: Sign PCI questionnaire
                description: Signs the required PCI questionnaire.
            /legalEntities/{id}/pciQuestionnaires/{pciid}:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                summary: Get PCI questionnaire
                description: Returns the signed PCI questionnaire.
            /legalEntities/{id}/termsOfService:
              post:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                summary: Get Terms of Service document
                description: Returns the Terms of Service document for a legal entity.
            /legalEntities/{id}/termsOfService/{termsofservicedocumentid}:
              patch:
                tags:
                  - Accept
                  - Terms
                  - Of
                  - Services
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                summary: Accept Terms of Service
                description: Accepts Terms of Service.
            /legalEntities/{id}/termsOfServiceAcceptanceInfos:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Information
                  - For
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                summary: Get Terms of Service information for a legal entity
                description: Returns Terms of Service information for a legal entity.
            /legalEntities/{id}/termsOfServiceStatus:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Status
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                summary: Get Terms of Service status
                description: >-
                  Returns the required types of Terms of Service that need to be
                  accepted by a legal entity.
            /themes:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Hosted
                  - Onboarding
                  - Page
                  - Themes
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get a list of hosted onboarding page themes
                description: >+
                  Returns a list of hosted onboarding page themes.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /themes/{id}:
              get:
                tags:
                  - Get
                  - null
                  - Onboarding
                  - Link
                  - Theme
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get an onboarding link theme
                description: >+
                  Returns the details of the theme identified in the path.>If
                  you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /transferInstruments:
              post:
                tags:
                  - Create
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Create a transfer instrument
                description: >-
                  Creates a transfer instrument. 


                  A transfer instrument is a bank account that a legal entity
                  owns. Adyen performs verification checks on the transfer
                  instrument as required by payment industry regulations. We
                  inform you of the verification results through webhooks or API
                  responses.


                  When the transfer instrument passes the verification checks,
                  you can start sending funds from the balance platform to the
                  transfer instrument (such as payouts).
            /transferInstruments/{id}:
              delete:
                tags:
                  - Delete
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Delete a transfer instrument
                description: Deletes a transfer instrument.
              get:
                tags:
                  - Get
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Get a transfer instrument
                description: Returns the details of a transfer instrument.
              patch:
                tags:
                  - Update
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Update a transfer instrument
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/legal-entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/legal-entity-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-legal-entity-api
  - name: Adyen Legal Entity API
    description: >-
      The Legal Entity Management API enables you to manage legal entities that
      contain information required for verification.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Legal Entity Management API
          tags:
            - name: Legal entities
            - name: Transfer instruments
            - name: Business lines
            - name: Documents
            - name: Terms of Service
            - name: Hosted Onboarding
            - name: Questionnaires
          paths:
            /businessLines:
              post:
                tags:
                  - Create
                  - Business
                  - Line
                  - Lines
                summary: Create a business line
                description: >+
                  Creates a business line. 


                  This resource contains information about your user's line of
                  business, including their industry and their source of funds.
                  Adyen uses this information to verify your users as required
                  by payment industry regulations. Adyen informs you of the
                  verification results through webhooks or API responses.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /businessLines/{id}:
              delete:
                tags:
                  - Delete
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Delete a business line
                description: |-
                  Deletes a business line.

                   >If you delete a business line linked to a [payment method](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api), it can affect your merchant account's ability to use the [payment method](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings). The business line is removed from all linked merchant accounts.
              get:
                tags:
                  - Get
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Get a business line
                description: Returns the detail of a business line.
              patch:
                tags:
                  - Update
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Update a business line
                description: Updates a business line.
            /documents:
              post:
                tags:
                  - Uploads
                  - Document
                  - For
                  - Verification
                  - Checks
                  - Lines
                  - Identifiers
                  - Documents
                summary: Upload a document for verification checks
                description: |-
                  Uploads a document for verification checks.

                   Adyen uses the information from the [legal entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities) to run automated verification checks. If these checks fail, you will be notified to provide additional documents.

                   You should only upload documents when Adyen requests additional information for the legal entity.

                   >You can upload a maximum of 15 pages for photo IDs.
            /documents/{id}:
              delete:
                tags:
                  - Delete
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Delete a document
                description: Deletes a document.
              get:
                tags:
                  - Get
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Get a document
                description: Returns a document.
              patch:
                tags:
                  - Update
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Update a document
                description: |-
                  Updates a document.

                   >You can upload a maximum of 15 pages for photo IDs.
            /legalEntities:
              post:
                tags:
                  - Create
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Create a legal entity
                description: >+
                  Creates a legal entity. 


                  This resource contains information about the user that will be
                  onboarded in your platform. Adyen uses this information to
                  perform verification checks as required by payment industry
                  regulations. Adyen informs you of the verification results
                  through webhooks or API responses. 


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}:
              get:
                tags:
                  - Get
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Get a legal entity
                description: Returns a legal entity.
              patch:
                tags:
                  - Update
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Update a legal entity
                description: |-
                  Updates a legal entity.

                   >To change the legal entity type, include only the new `type` in your request. To update the `entityAssociations` array, you need to replace the entire array. For example, if the array has 3 entries and you want to remove 1 entry, you need to PATCH the resource with the remaining 2 entries.
            /legalEntities/{id}/businessLines:
              get:
                tags:
                  - Get
                  - All
                  - Business
                  - Lines
                  - Under
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                summary: Get all business lines under a legal entity
                description: Returns the business lines owned by a legal entity.
            /legalEntities/{id}/checkVerificationErrors:
              post:
                tags:
                  - Checks
                  - Legal
                  - Entities
                  - Verification
                  - Errors
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                summary: Check a legal entity's verification errors
                description: >-
                  Returns the verification errors for a legal entity and its
                  supporting entities.
            /legalEntities/{id}/confirmDataReview:
              post:
                tags:
                  - Confirm
                  - Data
                  - Reviews
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                summary: Confirm data review
                description: >-
                  Confirms that your user has reviewed the data for the legal
                  entity specified in the path. Call this endpoint to inform
                  Adyen that your user reviewed and verified that the data is
                  up-to-date. The endpoint returns the timestamp of when Adyen
                  received the request.
            /legalEntities/{id}/onboardingLinks:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - null
                  - Adyen-hosted
                  - Onboarding
                  - Page
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                summary: Get a link to an Adyen-hosted onboarding page
                description: >+
                  Returns a link to an Adyen-hosted onboarding page where you
                  need to redirect your user.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}/pciQuestionnaires:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Details
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                summary: Get PCI questionnaire details
                description: Get a list of signed PCI questionnaires.
            /legalEntities/{id}/pciQuestionnaires/generatePciTemplates:
              post:
                tags:
                  - Generate
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                summary: Generate PCI questionnaire
                description: >-
                  Generates the required PCI questionnaires based on the user's
                  [salesChannel](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/businessLines__reqParam_salesChannels).
            /legalEntities/{id}/pciQuestionnaires/signPciTemplates:
              post:
                tags:
                  - Sign
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                summary: Sign PCI questionnaire
                description: Signs the required PCI questionnaire.
            /legalEntities/{id}/pciQuestionnaires/{pciid}:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                summary: Get PCI questionnaire
                description: Returns the signed PCI questionnaire.
            /legalEntities/{id}/termsOfService:
              post:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                summary: Get Terms of Service document
                description: Returns the Terms of Service document for a legal entity.
            /legalEntities/{id}/termsOfService/{termsofservicedocumentid}:
              patch:
                tags:
                  - Accept
                  - Terms
                  - Of
                  - Services
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                summary: Accept Terms of Service
                description: Accepts Terms of Service.
            /legalEntities/{id}/termsOfServiceAcceptanceInfos:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Information
                  - For
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                summary: Get Terms of Service information for a legal entity
                description: Returns Terms of Service information for a legal entity.
            /legalEntities/{id}/termsOfServiceStatus:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Status
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                summary: Get Terms of Service status
                description: >-
                  Returns the required types of Terms of Service that need to be
                  accepted by a legal entity.
            /themes:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Hosted
                  - Onboarding
                  - Page
                  - Themes
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get a list of hosted onboarding page themes
                description: >+
                  Returns a list of hosted onboarding page themes.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /themes/{id}:
              get:
                tags:
                  - Get
                  - null
                  - Onboarding
                  - Link
                  - Theme
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get an onboarding link theme
                description: >+
                  Returns the details of the theme identified in the path.>If
                  you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /transferInstruments:
              post:
                tags:
                  - Create
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Create a transfer instrument
                description: >-
                  Creates a transfer instrument. 


                  A transfer instrument is a bank account that a legal entity
                  owns. Adyen performs verification checks on the transfer
                  instrument as required by payment industry regulations. We
                  inform you of the verification results through webhooks or API
                  responses.


                  When the transfer instrument passes the verification checks,
                  you can start sending funds from the balance platform to the
                  transfer instrument (such as payouts).
            /transferInstruments/{id}:
              delete:
                tags:
                  - Delete
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Delete a transfer instrument
                description: Deletes a transfer instrument.
              get:
                tags:
                  - Get
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Get a transfer instrument
                description: Returns the details of a transfer instrument.
              patch:
                tags:
                  - Update
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Update a transfer instrument
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/legal-entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/legal-entity-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-legal-entity-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---