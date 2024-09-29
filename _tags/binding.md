---
name: Binding
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/binding.png
url: https://example.com/apis/binding.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Binding
apis:
  - name: schemas
    description: <p>Amazon EventBridge Schema Registry</p>
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
            title: schemas
          paths:
            /v1/discoverers:
              GET:
                summary: ListDiscoverers
                description: <p>List the discoverers.</p>
                tags:
                  - Lists
                  - Discoverers
                  - V1
                  - Discoverers
            /v1/registries/name/{registryName}:
              PUT:
                summary: UpdateRegistry
                description: <p>Updates a registry.</p>
                tags:
                  - Update
                  - Registries
                  - V1
                  - Discoverers
                  - Names
            /v1/registries/name/{registryName}/schemas/name/{schemaName}:
              PUT:
                summary: UpdateSchema
                description: >-
                  <p>Updates the schema definition</p> <note><p>Inactive schemas
                  will be deleted after two years.</p></note>
                tags:
                  - Update
                  - Schemas
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
            /v1/discoverers/id/{discovererId}:
              PUT:
                summary: UpdateDiscoverer
                description: <p>Updates the discoverer</p>
                tags:
                  - Update
                  - Discoverers
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
            /v1/policy:
              PUT:
                summary: PutResourcePolicy
                description: <p>The name of the policy.</p>
                tags:
                  - Put
                  - Resources
                  - Policies
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
            /v1/registries/name/{registryName}/schemas/name/{schemaName}/version/{schemaVersion}:
              DELETE:
                summary: DeleteSchemaVersion
                description: <p>Delete the schema version definition</p>
                tags:
                  - Delete
                  - Schemas
                  - Versions
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
            /v1/registries/name/{registryName}/schemas/name/{schemaName}/language/{language}:
              POST:
                summary: PutCodeBinding
                description: <p>Put code binding URI</p>
                tags:
                  - Put
                  - Code
                  - Binding
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
            /v1/registries/name/{registryName}/schemas/name/{schemaName}/language/{language}/source:
              GET:
                summary: GetCodeBindingSource
                description: <p>Get the code binding source URI.</p>
                tags:
                  - Get
                  - Code
                  - Binding
                  - Source
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
            /v1/discover:
              POST:
                summary: GetDiscoveredSchema
                description: >-
                  <p>Get the discovered schema that was generated based on
                  sampled events.</p>
                tags:
                  - Get
                  - Discovered
                  - Schemas
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
            /v1/registries:
              GET:
                summary: ListRegistries
                description: <p>List the registries.</p>
                tags:
                  - Lists
                  - Registries
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
            /v1/registries/name/{registryName}/schemas/name/{schemaName}/versions:
              GET:
                summary: ListSchemaVersions
                description: >-
                  <p>Provides a list of the schema versions and related
                  information.</p>
                tags:
                  - Lists
                  - Schemas
                  - Versions
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
            /v1/registries/name/{registryName}/schemas:
              GET:
                summary: ListSchemas
                description: <p>List the schemas.</p>
                tags:
                  - Lists
                  - Schemas
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
                  - Tags
                  - Resources
                  - ARN
            /v1/registries/name/{registryName}/schemas/search:
              GET:
                summary: SearchSchemas
                description: <p>Search the schemas</p>
                tags:
                  - Search
                  - Schemas
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
                  - Tags
                  - Resources
                  - ARN
                  - Search
            /v1/discoverers/id/{discovererId}/start:
              POST:
                summary: StartDiscoverer
                description: <p>Starts the discoverer</p>
                tags:
                  - Start
                  - Discoverers
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
                  - Tags
                  - Resources
                  - ARN
                  - Search
                  - Start
            /v1/discoverers/id/{discovererId}/stop:
              POST:
                summary: StopDiscoverer
                description: <p>Stops the discoverer</p>
                tags:
                  - Stop
                  - Discoverers
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
                  - Tags
                  - Resources
                  - ARN
                  - Search
                  - Start
                  - Stop
            /v1/registries/name/{registryName}/schemas/name/{schemaName}/export:
              GET:
                summary: ExportSchema
                description: <p>Exports a schema to a different specific
                tags:
                  - Export
                  - Schemas
                  - V1
                  - Discoverers
                  - Names
                  - Schemas
                  - Schemas
                  - Identifiers
                  - Policies
                  - Versions
                  - Languages
                  - Source
                  - Discover
                  - Registries
                  - Versions
                  - Tags
                  - Resources
                  - ARN
                  - Search
                  - Start
                  - Stop
                  - Expo
    overlays:
      - type: APIs.io Search
        url: overlays/schemas-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/schemas-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:schemas
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---