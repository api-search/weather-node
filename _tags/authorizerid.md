---
name: Authorizer_id
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/authorizerid.png
url: https://example.com/apis/authorizerid.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Authorizer_id
apis:
  - name: apigateway
    description: >-
      <fullname>Amazon API Gateway</fullname> <p>Amazon API Gateway helps
      developers deliver robust, secure, and scalable mobile and web application
      back ends. API Gateway allows developers to securely connect mobile and
      web applications to APIs that run on Lambda, Amazon EC2, or other publicly
      addressable web services that are hosted outside of AWS.</p>
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
            title: apigateway
          paths:
            /apikeys:
              GET:
                summary: GetApiKeys
                description: <p>Gets information about the current ApiKeys resource.</p>
                tags:
                  - Get
                  - APIs
                  - Keys
                  - API Keys
            /restapis/{restapi_id}/authorizers:
              GET:
                summary: GetAuthorizers
                description: <p>Describe an existing Authorizers resource.</p>
                tags:
                  - Get
                  - Authorizers
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
            /domainnames/{domain_name}/basepathmappings:
              GET:
                summary: GetBasePathMappings
                description: <p>Represents a collection of BasePathMapping resources.</p>
                tags:
                  - Get
                  - Base
                  - Paths
                  - Mapping
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
            /restapis/{restapi_id}/deployments:
              GET:
                summary: GetDeployments
                description: <p>Gets information about a Deployments collection.</p>
                tags:
                  - Get
                  - Deployments
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
            /restapis/{restapi_id}/documentation/parts:
              PUT:
                summary: ImportDocumentationParts
                description: <p>Imports documentation parts</p>
                tags:
                  - Import
                  - Documentation
                  - Parts
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
            /restapis/{restapi_id}/documentation/versions:
              GET:
                summary: GetDocumentationVersions
                description: <p>Gets documentation versions.</p>
                tags:
                  - Get
                  - Documentation
                  - Versions
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
            /domainnames:
              GET:
                summary: GetDomainNames
                description: <p>Represents a collection of DomainName resources.</p>
                tags:
                  - Get
                  - Domains
                  - Names
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
            /restapis/{restapi_id}/models:
              GET:
                summary: GetModels
                description: >-
                  <p>Describes existing Models defined for a RestApi
                  resource.</p>
                tags:
                  - Get
                  - Models
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
            /restapis/{restapi_id}/requestvalidators:
              GET:
                summary: GetRequestValidators
                description: >-
                  <p>Gets the RequestValidators collection of a given
                  RestApi.</p>
                tags:
                  - Get
                  - Request
                  - Validators
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
            /restapis/{restapi_id}/resources/{parent_id}:
              POST:
                summary: CreateResource
                description: <p>Creates a Resource resource.</p>
                tags:
                  - Create
                  - Resources
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
            /restapis:
              GET:
                summary: GetRestApis
                description: <p>Lists the RestApis resources for your collection.</p>
                tags:
                  - Get
                  - Rest
                  - APIs
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
            /restapis/{restapi_id}/stages:
              GET:
                summary: GetStages
                description: <p>Gets information about one or more Stage resources.</p>
                tags:
                  - Get
                  - Stages
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
            /usageplans:
              GET:
                summary: GetUsagePlans
                description: <p>Gets all the usage plans of the caller's account.</p>
                tags:
                  - Get
                  - Usage
                  - Plans
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
            /usageplans/{usageplanId}/keys:
              GET:
                summary: GetUsagePlanKeys
                description: >-
                  <p>Gets all the usage plan keys representing the API keys
                  added to a specified usage plan.</p>
                tags:
                  - Get
                  - Usage
                  - Plan
                  - Keys
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
            /vpclinks:
              GET:
                summary: GetVpcLinks
                description: >-
                  <p>Gets the VpcLinks collection under the caller's account in
                  a selected region.</p>
                tags:
                  - Get
                  - VPC
                  - Links
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
            /apikeys/{api_Key}:
              PATCH:
                summary: UpdateApiKey
                description: <p>Changes information about an ApiKey resource.</p>
                tags:
                  - Update
                  - APIs
                  - Keys
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
            /restapis/{restapi_id}/authorizers/{authorizer_id}:
              PATCH:
                summary: UpdateAuthorizer
                description: <p>Updates an existing Authorizer resource.</p>
                tags:
                  - Update
                  - Authorizer
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
            /domainnames/{domain_name}/basepathmappings/{base_path}:
              PATCH:
                summary: UpdateBasePathMapping
                description: <p>Changes information about the BasePathMapping resource.</p>
                tags:
                  - Update
                  - Base
                  - Paths
                  - Mapping
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
            /clientcertificates/{clientcertificate_id}:
              PATCH:
                summary: UpdateClientCertificate
                description: >-
                  <p>Changes information about an ClientCertificate
                  resource.</p>
                tags:
                  - Update
                  - Client
                  - Certificates
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
            /restapis/{restapi_id}/deployments/{deployment_id}:
              PATCH:
                summary: UpdateDeployment
                description: <p>Changes information about a Deployment resource.</p>
                tags:
                  - Update
                  - Deployments
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
            /restapis/{restapi_id}/documentation/parts/{part_id}:
              PATCH:
                summary: UpdateDocumentationPart
                description: <p>Updates a documentation part.</p>
                tags:
                  - Update
                  - Documentation
                  - Part
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
            /restapis/{restapi_id}/documentation/versions/{doc_version}:
              PATCH:
                summary: UpdateDocumentationVersion
                description: <p>Updates a documentation version.</p>
                tags:
                  - Update
                  - Documentation
                  - Versions
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
            /domainnames/{domain_name}:
              PATCH:
                summary: UpdateDomainName
                description: <p>Changes information about the DomainName resource.</p>
                tags:
                  - Update
                  - Domains
                  - Names
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
            /restapis/{restapi_id}/gatewayresponses/{response_type}:
              PATCH:
                summary: UpdateGatewayResponse
                description: >-
                  <p>Updates a GatewayResponse of a specified response type on
                  the given RestApi.</p>
                tags:
                  - Update
                  - Gateway
                  - Responses
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
            /restapis/{restapi_id}/resources/{resource_id}/methods/{http_method}/integration:
              PATCH:
                summary: UpdateIntegration
                description: <p>Represents an update integration.</p>
                tags:
                  - Update
                  - Integrations
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
            /restapis/{restapi_id}/resources/{resource_id}/methods/{http_method}/integration/responses/{status_code}:
              PATCH:
                summary: UpdateIntegrationResponse
                description: <p>Represents an update integration response.</p>
                tags:
                  - Update
                  - Integrations
                  - Responses
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
            /restapis/{restapi_id}/resources/{resource_id}/methods/{http_method}:
              PATCH:
                summary: UpdateMethod
                description: <p>Updates an existing Method resource.</p>
                tags:
                  - Update
                  - Methods
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
            /restapis/{restapi_id}/resources/{resource_id}/methods/{http_method}/responses/{status_code}:
              PATCH:
                summary: UpdateMethodResponse
                description: <p>Updates an existing MethodResponse resource.</p>
                tags:
                  - Update
                  - Methods
                  - Responses
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
            /restapis/{restapi_id}/models/{model_name}:
              PATCH:
                summary: UpdateModel
                description: <p>Changes information about a model.</p>
                tags:
                  - Update
                  - Models
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
            /restapis/{restapi_id}/requestvalidators/{requestvalidator_id}:
              PATCH:
                summary: UpdateRequestValidator
                description: <p>Updates a RequestValidator of a given RestApi.</p>
                tags:
                  - Update
                  - Request
                  - Validators
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
            /restapis/{restapi_id}/resources/{resource_id}:
              PATCH:
                summary: UpdateResource
                description: <p>Changes information about a Resource resource.</p>
                tags:
                  - Update
                  - Resources
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
            /restapis/{restapi_id}:
              PATCH:
                summary: UpdateRestApi
                description: <p>Changes information about the specified API.</p>
                tags:
                  - Update
                  - Rest
                  - APIs
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
            /restapis/{restapi_id}/stages/{stage_name}:
              PATCH:
                summary: UpdateStage
                description: <p>Changes information about a Stage resource.</p>
                tags:
                  - Update
                  - Stage
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
            /usageplans/{usageplanId}:
              PATCH:
                summary: UpdateUsagePlan
                description: <p>Updates a usage plan of a given plan Id.</p>
                tags:
                  - Update
                  - Usage
                  - Plan
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
            /usageplans/{usageplanId}/keys/{keyId}:
              GET:
                summary: GetUsagePlanKey
                description: <p>Gets a usage plan key of a given key identifier.</p>
                tags:
                  - Get
                  - Usage
                  - Plan
                  - Keys
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
            /vpclinks/{vpclink_id}:
              PATCH:
                summary: UpdateVpcLink
                description: <p>Updates an existing VpcLink of a specified identifier.</p>
                tags:
                  - Update
                  - VPC
                  - Link
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
            /restapis/{restapi_id}/stages/{stage_name}/cache/authorizers:
              DELETE:
                summary: FlushStageAuthorizersCache
                description: <p>Flushes all authorizer cache entries on a stage.</p>
                tags:
                  - Flush
                  - Stage
                  - Authorizers
                  - Cache
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
            /restapis/{restapi_id}/stages/{stage_name}/cache/data:
              DELETE:
                summary: FlushStageCache
                description: <p>Flushes a stage's cache.</p>
                tags:
                  - Flush
                  - Stage
                  - Cache
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
            /clientcertificates:
              GET:
                summary: GetClientCertificates
                description: <p>Gets a collection of ClientCertificate resources.</p>
                tags:
                  - Get
                  - Client
                  - Certificates
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
            /account:
              PATCH:
                summary: UpdateAccount
                description: <p>Changes information about the current Account resource.</p>
                tags:
                  - Update
                  - Account
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
            /restapis/{restapi_id}/stages/{stage_name}/exports/{export_type}:
              GET:
                summary: GetExport
                description: >-
                  <p>Exports a deployed version of a RestApi in a specified
                  format.</p>
                tags:
                  - Get
                  - Export
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
            /restapis/{restapi_id}/gatewayresponses:
              GET:
                summary: GetGatewayResponses
                description: >-
                  <p>Gets the GatewayResponses collection on the given RestApi.
                  If an API developer has not added any definitions for gateway
                  responses, the result will be the API Gateway-generated
                  default GatewayResponses collection for the supported response
                  types.</p>
                tags:
                  - Get
                  - Gateway
                  - Responses
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
            /restapis/{restapi_id}/models/{model_name}/default_template:
              GET:
                summary: GetModelTemplate
                description: >-
                  <p>Generates a sample mapping template that can be used to
                  transform a payload into the structure of a model.</p>
                tags:
                  - Get
                  - Models
                  - Templates
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
            /restapis/{restapi_id}/resources:
              GET:
                summary: GetResources
                description: >-
                  <p>Lists information about a collection of Resource
                  resources.</p>
                tags:
                  - Get
                  - Resources
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
            /restapis/{restapi_id}/stages/{stage_name}/sdks/{sdk_type}:
              GET:
                summary: GetSdk
                description: <p>Generates a client SDK for a RestApi and Stage.</p>
                tags:
                  - Get
                  - SDKs
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
            /sdktypes/{sdktype_id}:
              GET:
                summary: GetSdkType
                description: <p>Gets an SDK type.</p>
                tags:
                  - Get
                  - SDKs
                  - Types
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
            /sdktypes:
              GET:
                summary: GetSdkTypes
                description: <p>Gets SDK types</p>
                tags:
                  - Get
                  - SDKs
                  - Types
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
            /tags/{resource_arn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from a given resource.</p>
                tags:
                  - Untag
                  - Resources
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
                  - Tags
                  - Resource_arn
            /usageplans/{usageplanId}/usage:
              GET:
                summary: GetUsage
                description: >-
                  <p>Gets the usage data of a usage plan in a specified time
                  interval.</p>
                tags:
                  - Get
                  - Usage
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
                  - Tags
                  - Resource_arn
                  - Usage
            /apikeys?mode=import:
              POST:
                summary: ImportApiKeys
                description: >-
                  <p>Import API keys from an external source, such as a
                  CSV-formatted file.</p>
                tags:
                  - Import
                  - APIs
                  - Keys
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
                  - Tags
                  - Resource_arn
                  - Usage
                  - Apikeys?mode=import
            /restapis?mode=import:
              POST:
                summary: ImportRestApi
                description: >-
                  <p>A feature of the API Gateway control service for creating a
                  new API from an external API definition file.</p>
                tags:
                  - Import
                  - Rest
                  - APIs
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
                  - Tags
                  - Resource_arn
                  - Usage
                  - Apikeys?mode=import
                  - REST APIs
            /usageplans/{usageplanId}/keys/{keyId}/usage:
              PATCH:
                summary: UpdateUsage
                description: >-
                  <p>Grants a temporary extension to the remaining quota of a
                  usage plan associated with a specified AP
                tags:
                  - Update
                  - Usage
                  - API Keys
                  - REST APIs
                  - Restapi_id
                  - Authorizers
                  - Domain Names
                  - Domain_name
                  - Basepath Mappings
                  - Deployments
                  - Documentation
                  - Parts
                  - Versions
                  - Models
                  - Request Validators
                  - Resources
                  - Parent_id
                  - Stages
                  - Usage Plans
                  - Identifiers
                  - Keys
                  - VPC Links
                  - Keys
                  - Authorizer_id
                  - Base_path
                  - Client Certificates
                  - Clientcertificate_id
                  - Deployment_id
                  - Part_id
                  - Doc_version
                  - Gatewayresponses
                  - Response_type
                  - Resource_id
                  - Methods
                  - Http_method
                  - Integrations
                  - Responses
                  - Status_code
                  - Model_name
                  - Requestvalidator_id
                  - Stage_name
                  - Vpclink_id
                  - Cache
                  - Data
                  - Account
                  - Exports
                  - Export_type
                  - Default_template
                  - SDKs
                  - Sdk_type
                  - SDK Types
                  - Sdktype_id
                  - Tags
                  - Resource_arn
                  - Usage
                  - Apikeys?mode=import
                  - REST APIs
    overlays:
      - type: APIs.io Search
        url: overlays/apigateway-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/apigateway-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:apigateway
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---