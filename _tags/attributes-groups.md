---
name: Attributes Groups
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/attributes-groups.png
url: https://example.com/apis/attributes-groups.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Attributes Groups
apis:
  - name: FactSet Open FactSet Marketplace API
    description: >-
      Access FactSet’s comprehensive catalog of Data Feeds, APIs and Technology
      Solutions available on the Open FactSet Marketplace.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/openfactset-marketplace-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/openfactset-marketplace-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/openfactset-marketplace-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/openfactset-marketplace-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/openfactset-marketplace-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/openfactset-marketplace-api#changelog
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Open:FactSet Marketplace API
            description: Headless CMS API used by the Open:FactSet Marketplace.
            contact:
              name: Open:FactSet Frontend Engineering Team
              email: openfactset-frontend-engineering@factset.com
            license:
              name: Proprietary
            version: v2.3.0
          host: api-sandbox.factset.com
          paths:
            /ofs/v2/attributes/{id}:
              get:
                summary: Retrieve a collection of Attribute records.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: Globally unique identifier (GUID) of an attribute record
                    schema:
                      example: 904eb623-2b58-4dba-8e81-61e2ef889bb5
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    $ref: '#/definitions/GetAttributeDto'
                  '404':
                    description: Attribute record was not found.
                tags:
                  - Attributes
            /ofs/v2/attributes:
              get:
                summary: Retrieve a collection of Attribute records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Attribute records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetAttributeDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Attributes
            /ofs/v2/attributes/search:
              post:
                summary: Retrieve a collection of Attribute records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostAttributeSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Attribute records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetAttributeDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Attributes
            /ofs/v2/attributes/groups/{id}:
              get:
                summary: Retrieve a specific Attributes Group record.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: >-
                      Globally unique identifier (GUID) of an Attributes Group
                      record
                    schema:
                      example: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    description: A JSON representation of an Attributes Group record.
                    schema:
                      $ref: '#/definitions/GetAttributesGroupDto'
                  '404':
                    description: Attributes Group record was not found.
                tags:
                  - Attributes Groups
            /ofs/v2/attributes/groups:
              get:
                summary: Retrieve a collection of Attributes Group records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Attributes Group
                      records. Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetAttributesGroupDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Attributes Groups
            /ofs/v2/attributes/groups/used:
              get:
                summary: Retrieve a collection of Attributes Group records in use.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Attributes Group
                      records. Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetAttributesGroupDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Attributes Groups
            /ofs/v2/attributes/groups/search:
              post:
                summary: Retrieve a collection of Attributes Group records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostAttributesGroupSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Attributes Group
                      records. Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetAttributesGroupDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Attributes Groups
            /ofs/v2/media/download/{namespace}/{scope}/{guid}/{fileName}:
              get:
                summary: Retrieve a specific media file
                parameters:
                  - name: namespace
                    in: path
                    required: true
                    description: The namespace of the media file
                    schema:
                      example: partners
                    type: string
                    pattern: (partners|products|resources)
                    enum:
                      - partners
                      - products
                      - resources
                  - name: scope
                    in: path
                    required: true
                    description: The scope of the media file
                    schema:
                      example: logo
                    type: string
                    pattern: (logo|avatar|documents)
                    enum:
                      - logo
                      - avatar
                      - documents
                  - name: guid
                    in: path
                    required: true
                    description: The GUID of the file being requested
                    schema:
                      example: 774c3a5c-cc77-4e4c-b4a8-224a35cb00ba
                    type: string
                  - name: fileName
                    in: path
                    required: true
                    description: The name you want to show for this file in the uri.
                    schema:
                      example: FactSet.png
                    type: string
                responses:
                  '200':
                    description: OK
                  '404':
                    description: Not Found
                tags:
                  - Media
              head:
                summary: >-
                  Check the existence and retrieve the headers of a spefic media
                  file
                parameters:
                  - name: namespace
                    in: path
                    required: true
                    description: The namespace of the media file
                    schema:
                      example: partners
                    type: string
                    pattern: (partners|products|resources)
                    enum:
                      - partners
                      - products
                      - resources
                  - name: scope
                    in: path
                    required: true
                    description: The scope of the media file
                    schema:
                      example: logo
                    type: string
                    pattern: (logo|avatar|documents)
                    enum:
                      - logo
                      - avatar
                      - documents
                  - name: guid
                    in: path
                    required: true
                    description: The GUID of the file being requested
                    schema:
                      example: 774c3a5c-cc77-4e4c-b4a8-224a35cb00ba
                    type: string
                  - name: fileName
                    in: path
                    required: true
                    description: The name you want to show for this file in the uri.
                    schema:
                      example: FactSet.png
                    type: string
                responses:
                  '200':
                    description: OK
                  '404':
                    description: Not Found
                tags:
                  - Media
            /ofs/v2/partners/{id}:
              get:
                summary: Retrieve a specific Partner record.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: Globally unique identifier (GUID) of a partner record
                    schema:
                      example: caa0ee0f-c0fe-427e-9596-491e6c527b3f
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    $ref: '#/definitions/GetPartnerDto'
                  '404':
                    description: Partner record was not found.
                tags:
                  - Partners
            /ofs/v2/partners:
              get:
                summary: Retrieve a collection of Partner records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Partner records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetPartnerDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Partners
            /ofs/v2/partners/search:
              post:
                summary: Retrieve a collection of Partner records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostPartnerSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Partner records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetPartnerDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Partners
            /ofs/v2/products/{id}:
              get:
                summary: Retrieve a specific Product record.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: Globally unique identifier (GUID) of a Product record
                    schema:
                      example: 89bba0ab-b123-4766-8a7b-9a174a453571
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    description: A JSON representation of a Product record.
                    schema:
                      $ref: '#/definitions/GetProductDto'
                  '404':
                    description: Product record was not found.
                tags:
                  - Products
            /ofs/v2/products/types:
              get:
                summary: >-
                  Retrieve a collection of the available Product Types along
                  with the number of published products per type.
                responses:
                  '200':
                    description: >-
                      A JSON representation a collection of the available
                      Product Types.
                    schema:
                      example:
                        - type: Data Feed
                          total: 0
                        - type: Solution
                          total: 0
                        - type: API
                          total: 0
                      items:
                        properties:
                          type:
                            type: string
                            enum:
                              - Data Feed
                              - API
                              - Solution
                          total:
                            type: integer
                        type: object
                      type: array
                tags:
                  - Products
            /ofs/v2/products:
              get:
                summary: Retrieve a collection of Product records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Product records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetProductDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Products
            /ofs/v2/products/search:
              post:
                summary: Retrieve a collection of Product records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostProductSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Product records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetProductDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Products
            /ofs/v2/resources/{id}:
              get:
                summary: Retrieve a specific Resource record.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: Globally unique identifier (GUID) of a Resource record
                    schema:
                      example: 3d8410df-2b04-45fa-bc33-d2cc5418f293
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    description: A JSON representation of an Resource record.
                    schema:
                      $ref: '#/definitions/GetResourceDto'
                  '404':
                    description: Resource record was not found.
                tags:
                  - Resources
            /ofs/v2/resources:
              get:
                summary: Retrieve a collection of Resource records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Resource records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetResourceDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Resources
            /ofs/v2/resources/search:
              post:
                summary: Retrieve a collection of Resource records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostResourceSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Resource records.
                      Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetResourceDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Resources
            /ofs/v2/resources/sections/{id}:
              get:
                summary: Retrieve a specific Resources Section record.
                parameters:
                  - name: id
                    in: path
                    required: true
                    description: >-
                      Globally unique identifier (GUID) of a Resources Section
                      record
                    schema:
                      example: 4c77e650-372b-4ab4-9acd-bbd237d52b74
                    type: string
                    pattern: >-
                      \{?[a-zA-Z0-9]{8}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{4}-[a-zA-Z0-9]{12}\}?
                responses:
                  '200':
                    description: A JSON representation of a Resources Section record.
                    schema:
                      $ref: '#/definitions/GetResourcesSectionDto'
                  '404':
                    description: Resources Section record was not found.
                tags:
                  - Resources Sections
            /ofs/v2/resources/sections:
              get:
                summary: Retrieve a collection of Resources Section records.
                parameters:
                  - name: limit
                    in: query
                    description: Limit the amount of records per page
                    type: integer
                    default: 10
                  - name: page
                    in: query
                    description: Select which page to show
                    type: integer
                    default: 1
                    minimum: 1
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Resources Section
                      records. Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetResourcesSectionDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Resources Sections
            /ofs/v2/resources/sections/search:
              post:
                summary: Retrieve a collection of Resources Section records.
                parameters:
                  - name: body
                    in: body
                    schema:
                      $ref: '#/definitions/PostResourcesSectionSearchDto'
                    type: json
                responses:
                  '200':
                    description: >-
                      A JSON representation of collection of Resources Section
                      records. Might be empty.
                    schema:
                      items:
                        allOf:
                          - $ref: '#/definitions/GetResourcesSectionDto'
                      type: array
                    headers:
                      X-Pagination:
                        description: >-
                          A JSON containing pagination information. (e.g
                          totalCount,pageSize,currentPage,totalPages,previousPageLink
                          and nextPageLink)
                        type: string
                  '422':
                    description: >-
                      Unprocessable entity. Validation error response containing
                      the errors in a human readable form.
                    schema:
                      items:
                        type: string
                      type: array
                tags:
                  - Resources Sections
          definitions:
            Marking:
              properties:
                state:
                  example: published
                  type: string
              type: object
            Document:
              properties:
                name:
                  type: string
                description:
                  type: string
                fileName:
                  type: string
                url:
                  type: string
                isFile:
                  type: boolean
                isPublic:
                  type: boolean
                order:
                  type: integer
                section:
                  items:
                    properties:
                      id:
                        type: integer
                      name:
                        type: string
                    type: object
                  type: array
              type: object
            PostResourcesSectionSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:asc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,order
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: name:Data
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: order:1
                  type: string
              type: object
            GetResourcesSectionDto:
              description: A Json representation of a Document Category record.
              properties:
                id:
                  example: 4c77e650-372b-4ab4-9acd-bbd237d52b74
                  type: string
                name:
                  example: New Provider Resources
                  type: string
                order:
                  example: 3
                  type: integer
                created:
                  example: 1559578671
                  type: integer
                updated:
                  example: 1559578671
                  type: integer
                documents:
                  example:
                    id: 3d8410df-2b04-45fa-bc33-d2cc5418f293
                    name: Candidate Agreement--Exhibit A
                    fileName: Exhibit A.docx
                    description: >-
                      Template for Exhibit A to the new Candidate Agreement.
                      Fill out this document with a description of the
                      product(s) for the Open=>FactSet marketplace
                    url: >-
                      /media/download/resources/documents/c2e2394c-747e-422f-bc5d-b775b14833bd
                    order: 5
                    isFile: true
                    isPublic: true
                    categoryId: 4c77e650-372b-4ab4-9acd-bbd237d52b74
                    created: 1564487399
                    updated: 1568288463
                  items:
                    $ref: '#/definitions/GetResourceDto'
                  type: array
                meta:
                  example:
                    documentsTotal: 1
                    documentsPrivate: 0
                  items:
                    properties:
                      documentsTotal:
                        type: integer
                      documentsPrivate:
                        type: integer
                    type: object
                  type: array
              type: object
            PostResourceSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:desc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,fileName,isPublic,url
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: description:Template,name:Template,fileName:Template
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: isFile:true
                  type: string
              type: object
            GetResourceDto:
              description: A Json representation of a Document record.
              properties:
                id:
                  example: 3d8410df-2b04-45fa-bc33-d2cc5418f293
                  type: string
                name:
                  example: Candidate Agreement--Exhibit A
                  type: string
                fileName:
                  example: Exhibit A.docx
                  type: string
                description:
                  example: >-
                    Template for Exhibit A to the new Candidate Agreement. Fill
                    out this document with a description of the product(s) for
                    the Open:FactSet marketplace
                  type: string
                url:
                  example: >-
                    /media/download/resources/documents/c2e2394c-747e-422f-bc5d-b775b14833bd
                  type: string
                order:
                  example: 5
                  type: integer
                isFile:
                  example: true
                  type: boolean
                isPublic:
                  example: true
                  type: boolean
                categoryId:
                  example: 4c77e650-372b-4ab4-9acd-bbd237d52b74
                  type: string
                created:
                  example: 1564487399
                  type: integer
                updated:
                  example: 1568288463
                  type: integer
              type: object
            PostAttributesGroupSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:asc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,prodType
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: name:Country,prodType:Data Feed
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: name:Region/Country
                  type: string
              type: object
            GetAttributesGroupDto:
              description: A Json representation of an Attributes Group record.
              properties:
                id:
                  example: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                  type: string
                name:
                  example: Region/Country
                  type: string
                prodType:
                  example: Data Feed
                  type: string
                color:
                  example: tag-color-2
                  type: string
                type:
                  example: checkbox
                  type: string
                selection:
                  example: multi
                  type: string
                created:
                  example: 1531815425
                  type: integer
                updated:
                  example: 1531815425
                  type: integer
                attributes:
                  example:
                    - id: 904eb623-2b58-4dba-8e81-61e2ef889bb5
                      name: Europe
                      groupId: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                      prodType: Data Feed
                      created: 1531815425
                      updated: 1531815425
                      isUsed: true
                    - id: 8edfdf11-ce9a-45e2-831a-e6d7717736c9
                      name: Global
                      groupId: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                      prodType: Data Feed
                      created: 1531815424
                      updated: 1531815424
                      isUsed: true
                  items:
                    properties:
                      name:
                        example: Europe
                        type: string
                      groupId:
                        example: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                        type: string
                      prodType:
                        example: Data Feed
                        type: string
                      id:
                        example: 904eb623-2b58-4dba-8e81-61e2ef889bb5
                        type: string
                      created:
                        example: 1531815425
                        type: integer
                      updated:
                        example: 1531815425
                        type: integer
                      isUsed:
                        example: true
                        type: boolean
                    type: object
                  type: array
              type: object
            PostAttributeSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:asc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,groupId
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: name:Global,name:Europe
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: name:Europe:Global
                  type: string
              type: object
            GetAttributeDto:
              properties:
                id:
                  example: 904eb623-2b58-4dba-8e81-61e2ef889bb5
                  type: string
                name:
                  example: Europe
                  type: string
                groupId:
                  example: fd8f12e9-aa8b-4c2a-9e2e-a212f3ec29e1
                  type: string
                groupName:
                  example: Region/Country
                  type: string
                prodType:
                  example: Data Feed
                  type: string
                created:
                  example: 1531815425
                  type: integer
                updated:
                  example: 1531815425
                  type: integer
              type: object
            PostProductSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:asc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,marking.state,slug,partner
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: name:FactSet,detail:FactSet
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: type:Data Feed:API
                  type: string
              type: object
            GetProductDto:
              description: A Json representation of a Product record.
              properties:
                id:
                  example: 89bba0ab-b123-4766-8a7b-9a174a453571
                  type: string
                marking:
                  $ref: '#/definitions/Marking'
                name:
                  example: FactSet Corporate Governance
                  type: string
                detail:
                  example: >-
                    FactSet’s corporate activism database, SharkRepellent,
                    allows you to monitor and analyze corporate activism with
                    data items related to poison pills, significant activism
                    reported in SEC filings and news sources, and key takeover
                    defenses compiled from articles of incorporation, bylaws,
                    and other publicly available sources.  Data Frequency: 
                    Event;  Update Frequency:  Intraday. 
                  type: string
                dateAdded:
                  example: 1441029240
                  type: integer
                highlight:
                  example:
                    point1: >-
                      Access activism campaign details, including participants,
                      events, defenses, filing dates, and related entities
                    point2: >-
                      Leverage takeover defense and corporate governance data,
                      including bullet proof ratings, charter provisions and
                      amendment details, and appeal/repeal percentage
                      requirements
                    point3: >-
                      Obtain data for all U.S. in-force poison pills, Canadian
                      in-force and ratification pending poison pills, and any
                      other non-U.S. EDGAR filers that adopts a U.S. style
                      poison pill
                  properties:
                    point1:
                      type: string
                    point2:
                      type: string
                    point3:
                      type: string
                  type: object
                coverageTable:
                  example:
                    columns:
                      - field: field1
                        title: region
                        align: left
                        required: true
                      - field: field2
                        title: Count
                        align: left
                        required: true
                      - field: field3
                        title: Type
                        align: left
                        required: false
                      - field: field4
                        title: Start Date
                        align: left
                        required: false
                    rows:
                      - field1: Africa
                        field3: Entities
                        field2: '{40}'
                        field4: '2014'
                      - field1: Asia
                        field3: Entities
                        field2: '{350}'
                        field4: '2000'
                      - field1: Europe
                        field3: Entities
                        field2: '{640}'
                        field4: '1995'
                      - field1: Latin America
                        field3: Entities
                        field2: '{30}'
                        field4: '2006'
                      - field1: Middle East
                        field3: Entities
                        field2: '{70}'
                        field4: '1996'
                      - field1: North America
                        field3: Entities
                        field2: '{11740}'
                        field4: '1984'
                      - field1: Pacific
                        field3: Entities
                        field2: '{370}'
                        field4: '1998'
                  items:
                    properties:
                      columns:
                        items:
                          properties:
                            title:
                              type: string
                            field:
                              type: string
                            align:
                              type: string
                            required:
                              type: boolean
                          type: object
                        type: array
                      rows:
                        items:
                          type: object
                        type: array
                    type: object
                  type: array
                videoUrl:
                  example: https://vimeo.com/320509757
                  type: string
                previewLink:
                  example:
                    linkUrl: >-
                      https://insight.factset.com/resources/at-a-glance-factset-corp-datafeed
                    linkName: FactSet Corporate Governance DataFeed
                  properties:
                    linkUrl:
                      type: string
                    linkName:
                      type: string
                  type: object
                thirdPartyUrls:
                  example:
                    - link: >-
                        https://insight.factset.com/activists-knocking-on-doors-of-big-firms
                      name: Activists Knocking on Doors of Big Firms
                    - link: >-
                        https://advantage.factset.com/analyzing-trends-in-shareholder-activism-webcast
                      name: 'Webcast: 2016 Trends in Shareholder Activism'
                    - link: >-
                        https://insight.factset.com/in-2017-middle-east-ma-activity-dips-value-soars
                      name: In 2017 Middle East M&A Activity Dips, Value Soars
                  items:
                    properties:
                      link:
                        type: string
                      name:
                        type: string
                    type: object
                  type: array
                seoMeta:
                  example:
                    productTitle: FactSet Corporate Governance - Shark Repellent
                    productSummary: >-
                      With FactSet's corporate activism database, monitor and
                      analyze corporate activism campaign details, including
                      participants, events, defenses, and filings.
                  properties:
                    productTitle:
                      type: string
                    productSummary:
                      type: string
                    videoAltText:
                      type: string
                  type: object
                slug:
                  example: factset-corporate-governance
                  type: string
                productStatusAttr:
                  example: Available
                  type: string
                  enum:
                    - Coming Soon
                    - Recently Added
                    - Candidate
                    - In queue
                    - Recently Updated
                    - Available
                    - Available for Testing
                partner:
                  example:
                    name: FactSet
                    logoUrl: >-
                      /media/download/partners/logo/774c3a5c-cc77-4e4c-b4a8-224a35cb00ba
                    slug: factset
                    firmInfo: >-
                      FactSet creates data and technology solutions for
                      investment professionals around the world, providing
                      instant access to financial data and analytics that
                      investors use to make crucial decisions. We combine our
                      unique proprietary datasets, your in-house data, and
                      third-party unstructured data to help you see and seize
                      opportunity sooner.\n
                    videoUrl: https://vimeo.com/320509757
                    companyUrl: https://www.factset.com/
                    socialMedia:
                      linkedin: https://www.linkedin.com/company/factset
                      twitter: https://twitter.com/FactSet
                      facebook: https://www.facebook.com/FactSet/
                    seoMeta:
                      partnerTitle: FactSet
                      partnerSummary: >-
                        FactSet creates data and technology solutions for
                        investment professionals around the world.
                      videoAltText: ''
                    forumTags:
                      - id: factset
                        tag: factset
                    id: caa0ee0f-c0fe-427e-9596-491e6c527b3f
                  properties:
                    id:
                      type: string
                    name:
                      type: string
                    slug:
                      type: string
                    logoUrl:
                      type: string
                    firmInfo:
                      type: string
                    companyUrl:
                      type: string
                    socialMedia:
                      properties:
                        linkedin:
                          type: string
                        facebook:
                          type: string
                        twitter:
                          type: string
                      type: object
                  type: object
                relatedProducts:
                  example:
                    - name: FactSet Ownership
                      id: b7650ba1-519e-4af6-a5d1-8b6cb6ec744c
                      slug: factset-ownership
                    - name: FactSet Mergers
                      id: 8a579d81-ba0e-45c2-9cb9-144c9e7d895c
                      slug: factset-mergers
                    - name: FactSet People
                      id: 168e9bf8-108c-4912-beca-b658083c7c86
                      slug: factset-people
                  items:
                    properties:
                      name:
                        type: string
                      id:
                        type: string
                      slug:
                        type: string
                    type: object
                  type: array
                documents:
                  example:
                    - ref: ofsProductsDataDictionaryFile
                      fileName: >-
                        factset standard datafeed sharkrepellent v1
                        userguide.pdf
                      isFile: true
                      name: Data Dictionary
                      description: ''
                      isPublic: false
                      section:
                        name: Documentation
                        id: 2
                      type: dataDictionary
                      url: >-
                        /media/download/products/documents/4653f3d6-6de1-4e23-b6da-327301c4c860
                      order: 0
                    - fileName: Corporate Governance V1.zip
                      isFile: true
                      name: Starter Kit - Jupyter Notebooks and SQL Queries
                      description: Use case examples and sample code\t
                      isPublic: false
                      section:
                        name: Sample Data
                        id: 1
                      url: >-
                        /media/download/products/documents/5de6b025-d8a3-423b-a8c6-157730abe334
                      order: 1
                    - fileName: >-
                        OFM Sample FactSet Corporate Activism Announced
                        2019.xlsx
                      isFile: true
                      name: Corporate Activism Sample - 2019
                      description: ''
                      isPublic: false
                      section:
                        name: Sample Data
                        id: 1
                      url: >-
                        /media/download/products/documents/b7a73952-c6ed-45fe-bf0d-0ab4b7ceb1e9
                      order: 2
                    - fileName: OFM Sample FactSet Corporate Governance 2019.xlsx
                      isFile: true
                      name: Corporate Governance Sample  - 2019
                      description: ''
                      isPublic: false
                      section:
                        name: Sample Data
                        id: 1
                      url: >-
                        /media/download/products/documents/372ef839-591c-44c4-a668-838bc144cdb1
                      order: 3
                  items:
                    $ref: '#/definitions/Document'
                  type: array
                  default: 'null'
                type:
                  example:
                    - Data Feed
                  items:
                    type: string
                    enum:
                      - Data Feed
                      - API
                      - Solution
                  type: array
                attributesGroups:
                  example:
                    - attributes:
                        - color: tag-color-9
                          created: 1531815428
                          groupId: 5378b993-1057-4197-9a88-92de71d8f55e
                          name: 20+ yrs
                          id: df4b1f7c-58d3-463e-ad9f-55c24cba6f86
                          updated: 1531815428
                      id: 5378b993-1057-4197-9a88-92de71d8f55e
                    - attributes:
                        - color: tag-color-1
                          created: 1531815416
                          groupId: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                          name: Corporate Governance
                          id: ec224c5d-9b20-4af8-9e7c-725ee3cb4aa3
                          updated: 1531815416
                        - color: tag-color-1
                          created: 1531815419
                          groupId: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                          name: Events
                          id: ac310994-b350-48d2-abd4-a779af80f421
                          updated: 1531815419
                        - color: tag-color-1
                          created: 1531815415
                          groupId: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                          name: Corporate Activism
                          id: e2f036fa-c407-4db5-b6b1-0128c739698e
                          updated: 1531815415
                      id: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                  items:
                    properties:
                      id:
                        type: string
                      attributes:
                        items:
                          properties:
                            id:
                              type: string
                            groupId:
                              type: string
                            name:
                              type: string
                            color:
                              type: string
                            created:
                              type: integer
                            updated:
                              type: integer
                          type: object
                        type: array
                    type: object
                  type: array
                previewTags:
                  example:
                    - color: tag-color-1
                      created: 1531815415
                      groupId: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                      name: Corporate Activism
                      id: e2f036fa-c407-4db5-b6b1-0128c739698e
                      updated: 1531815415
                    - color: tag-color-1
                      created: 1531815416
                      groupId: 3bb76ffb-a83c-4b40-ba6b-c4003702f4fe
                      name: Corporate Governance
                      id: ec224c5d-9b20-4af8-9e7c-725ee3cb4aa3
                      updated: 1531815416
                    - color: tag-color-9
                      created: 1531815428
                      groupId: 5378b993-1057-4197-9a88-92de71d8f55e
                      name: 20+ yrs
                      id: df4b1f7c-58d3-463e-ad9f-55c24cba6f86
                      updated: 1531815428
                  items:
                    properties:
                      id:
                        type: string
                      groupId:
                        type: string
                      name:
                        type: string
                      color:
                        type: string
                      created:
                        type: integer
                      updated:
                        type: integer
                    type: object
                  type: array
                updateFrequency:
                  example: ''
                  type: string
                deliveryFrequency:
                  example: ''
                  type: string
                productLabelOverride:
                  example: ''
                  type: string
                created:
                  example: 1565883044
                  type: integer
                updated:
                  example: 1576275398
                  type: integer
                meta:
                  example:
                    documentsTotal: 4
                    documentsPrivate: 4
                  items:
                    properties:
                      documentsTotal:
                        type: integer
                      documentsPrivate:
                        type: integer
                    type: object
                  type: array
                versionSchema:
                  example:
                    major: 1
                    minor: 0
                    patch: 0
                    versionedId: 89bba0ab-b123-4766-8a7b-9a174a453571-1.0.0
                    originalId: 89bba0ab-b123-4766-8a7b-9a174a453571
                  properties:
                    major:
                      type: integer
                    minor:
                      type: integer
                    patch:
                      type: integer
                    versionedId:
                      type: string
                    originalId:
                      type: string
                  type: object
              type: object
            PostPartnerSearchDto:
              properties:
                limit:
                  description: Limit the amount of records per page.
                  example: 10
                  type: integer
                  default: 10
                  maximum: 300
                page:
                  description: Select which page to show.
                  example: 1
                  type: integer
                  default: 1
                  minimum: 1
                sort:
                  description: Sort according to  specific field value.
                  example: name:asc
                  type: string
                  default: name:asc
                fields:
                  description: >-
                    Fetch only specific fields. The fields' names separated by a
                    comma.
                  example: name,marking.state,slug
                  type: string
                search:
                  description: Search for terms in certain fields.
                  example: name:FactSet
                  type: string
                filter:
                  description: Filter against specific field values.
                  example: name:FactSet
                  type: string
              type: object
            GetPartnerDto:
              description: A Json representation of a Partner record.
              properties:
                id:
                  example: caa0ee0f-c0fe-427e-9596-491e6c527b3f
                  type: string
                logoUrl:
                  example: >-
                    /media/download/partners/logo/774c3a5c-cc77-4e4c-b4a8-224a35cb00ba
                  type: string
                forumTags:
                  example:
                    - id: factset
                      tag: factset
                  items:
                    properties:
                      tag:
                        type: string
                      id:
                        type: string
                    type: object
                  type: array
                videoUrl:
                  example: https://vimeo.com/320509757
                  type: string
                firmInfo:
                  example: >-
                    FactSet creates data and technology solutions for investment
                    professionals around the world, providing instant access to
                    financial data and analytics that investors use to make
                    crucial decisions. We combine our unique proprietary
                    datasets, your in-house data, and third-party unstructured
                    data to help you see and seize opportunity sooner.\n
                  type: string
                socialMedia:
                  example:
                    linkedin: https://www.linkedin.com/company/factset
                    twitter: https://twitter.com/FactSet
                    facebook: https://www.facebook.com/FactSet/
                  properties:
                    linkedin:
                      type: string
                    facebook:
                      type: string
                    twitter:
                      type: string
                  type: object
                name:
                  example: FactSet
                  type: string
                firmId:
                  example: 6992
                  type: integer
                companyUrl:
                  example: https://www.factset.com/
                  type: string
                seoMeta:
                  example:
                    partnerTitle: FactSet
                    partnerSummary: >-
                      FactSet creates data and technology solutions for
                      investment professionals around the world.
                    videoAltText: ''
                  properties:
                    productTitle:
                      type: string
                    productSummary:
                      type: string
                  type: object
                publishedDate:
                  example: 1568801114
                  type: integer
                slug:
                  example: factset
                  type: string
                marking:
                  $ref: '#/definitions/Marking'
                created:
                  example: 1518816584
                  type: integer
                updated:
                  example: 1568801114
                  type: integer
                versionSchema:
                  example:
                    major: 1
                    minor: 0
                    patch: 0
                    versionedId: caa0ee0f-c0fe-427e-9596-491e6c527b3f-1.0.0
                    originalId: caa0ee0f-c0fe-427e-9596-491e6c527b3f
                  properties:
                    major:
                      type: integer
                    minor:
                      type: integer
                    patch:
                      type: integer
                    versionedId:
                      type: string
                    originalId:
                      type: string
                  type: object
              type: object
          securityDefinitions:
            Basic:
              type: basic
          security:
            - Basic: []
    overlays:
      - type: APIs.io Search
        url: overlays/open-marketplace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/open-marketplace-openapi-api-evangelist-ratings.yml
    aid: factset:factset-open-factset-marketplace-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---