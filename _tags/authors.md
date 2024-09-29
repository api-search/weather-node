---
name: Authors
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/authors.png
url: https://example.com/apis/authors.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Authors
apis:
  - name: FactSet IRN Configuration API
    description: >-
      Config API allows users to read and update configuration and settings of
      the Internal Research Notes.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-configuration-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/authors:
              get:
                tags:
                  - Get
                  - All
                  - Authors
                  - V1
                  - Authors
                summary: Get all Authors
            /v1/contact-custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Contact
                  - Custom
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                summary: Get all the contact custom fields
              post:
                tags:
                  - Create
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                summary: Create a contact custom field
            /v1/contact-custom-fields/{contactCustomFieldId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Contact
                  - Custom
                  - Field's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Get a specific Contact custom field's details
              patch:
                tags:
                  - Edit
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Edit a contact custom field
              delete:
                tags:
                  - Delete
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Delete a contact custom field
            /v1/contact-roles:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Contact
                  - Roles
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                summary: Get list of the contact roles configured in your group
              post:
                tags:
                  - Create
                  - Contact
                  - Roles
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                summary: Create contact roles
            /v1/contact-types:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Contact
                  - Types
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Get list of the contact types configured in your group
              post:
                tags:
                  - Create
                  - Contact
                  - Types
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Create contact types
            /v1/custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Get all Custom Fields
            /v1/custom-symbol-custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Custom
                  - Symbol
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get all the Custom symbol custom fields
              post:
                tags:
                  - Create
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Create a Custom symbol custom field
            /v1/custom-symbol-custom-fields/{customSymbolCustomFieldId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Custom
                  - Symbol
                  - Field's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get a specific Custom symbol custom field's details
              patch:
                tags:
                  - Edit
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Edit a Custom symbol custom field
              delete:
                tags:
                  - Delete
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Delete a Custom symbol custom field
            /v1/custom-symbol-types:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Custom
                  - Symbol
                  - Types
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get all the custom symbol types
              post:
                tags:
                  - Create
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Create a Custom symbol type
            /v1/custom-symbol-types/{customSymbolTypeId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Custom
                  - Symbol
                  - Type's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Get a specific Custom symbol type's details
              put:
                tags:
                  - Edit
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Edit a Custom symbol type
              delete:
                tags:
                  - Delete
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Delete a Custom symbol type
            /v1/custom-symbol-types/{customSymbolTypeId}/custom-fields:
              get:
                tags:
                  - Get
                  - Custom
                  - Fields
                  - For
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Get Custom fields for Custom Symbol type
            /v1/group:
              get:
                tags:
                  - Get
                  - Group
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                summary: Get Group details
            /v1/group/client-sales-representative:
              get:
                tags:
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
            /v1/phone-number-types:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Phone
                  - Types
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                summary: Get list of the phone types configured in your group
              post:
                tags:
                  - Create
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                summary: Create a phone type
            /v1/recommendations:
              get:
                tags:
                  - Get
                  - All
                  - Recommendations
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                summary: Get all Recommendations
            /v1/relationship-categories:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Relationship
                  - Categories
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                summary: >-
                  Get list of the relationship categories configured in your
                  group
              post:
                tags:
                  - Create
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                summary: Create a relationship category
            /v1/relationships:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Relationships
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                summary: Get list of the relationships configured in your group
              post:
                tags:
                  - Create
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                summary: Create a relationship type
            /v1/sentiments:
              get:
                tags:
                  - Get
                  - All
                  - Sentiments
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                summary: Get all Sentiments
            /v1/subjects:
              get:
                tags:
                  - Get
                  - All
                  - Subjects
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                summary: Get all Subjects
            /v1/subjects/{subjectId}:
              get:
                tags:
                  - Get
                  - Subject
                  - Details
                  - For
                  - The
                  - Given
                  - Id
                  - Provided
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                summary: Get Subject details for the given Id provided
            /v1/symbols-relationships:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Symbols
                  - Relationships
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                summary: Get all the Symbols Relationships
              post:
                tags:
                  - Create
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                summary: Create a symbol relationship
            /v1/teams:
              get:
                tags:
                  - Get
                  - All
                  - Teams
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                summary: Get all Teams
            /v1/teams/{teamId}:
              get:
                tags:
                  - Get
                  - Team
                  - Details
                  - For
                  - The
                  - Given
                  - Id
                  - Provided
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                summary: Get Team details for the given Id provided
            /v1/users:
              get:
                tags:
                  - Get
                  - All
                  - Assigned
                  - Fact
                  - Set
                  - Users
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                summary: Get all assigned FactSet users
            /v1/custom-symbol-types/reorder:
              post:
                tags:
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
            /v1/relationship-categories/reorder:
              post:
                tags:
                  - Reorder
                  - Relationship
                  - Categories
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                summary: Reorder relationship categories
            /v1/contact-roles/{contactRoleId}:
              put:
                tags:
                  - Edit
                  - Contact
                  - Role
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a contact role
              delete:
                tags:
                  - Delete
                  - Contact
                  - Role
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a contact role
            /v1/contact-types/{contactTypeId}:
              put:
                tags:
                  - Edit
                  - Contact
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a contact type
              delete:
                tags:
                  - Delete
                  - Contact
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a contact type
            /v1/phone-number-types/{phoneNumberTypeId}:
              put:
                tags:
                  - Edit
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a phone type
              delete:
                tags:
                  - Delete
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a phone type
            /v1/relationship-categories/{relationshipCategoryId}:
              put:
                tags:
                  - Edit
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a relationship category
              delete:
                tags:
                  - Delete
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a relationship category
            /v1/relationships/{relationshipId}:
              put:
                tags:
                  - Edit
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a relationship type
              delete:
                tags:
                  - Delete
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a relationship type
            /v1/symbols-relationships/{symbolsRelationshipId}:
              put:
                tags:
                  - Edit
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a symbol relationship
              delete:
                tags:
                  - Delete
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a symbol relationship
          tags:
            - name: Contacts - CustomFields
            - name: Contacts - PhoneNumberTypes
            - name: Contacts - Relationship Category
            - name: Contacts - Relationships
            - name: Contacts - Roles
            - name: Contacts - Types
            - name: CustomSymbols - CustomFields
            - name: CustomSymbols - Relationships
            - name: CustomSymbols - Types
            - name: 'N'
    overlays:
      - type: APIs.io Search
        url: overlays/irn-configuration-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-configuration-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-configuration-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---