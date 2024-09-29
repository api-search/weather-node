---
name: Cores
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cores.png
url: https://example.com/apis/cores.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cores
apis:
  - name: greengrass
    description: >-
      AWS IoT Greengrass seamlessly extends AWS onto physical devices so they
      can act locally on the data they generate, while still using the cloud for
      management, analytics, and durable storage. AWS IoT Greengrass ensures
      your devices can respond quickly to local events and operate with
      intermittent connectivity. AWS IoT Greengrass minimizes the cost of
      transmitting data to the cloud by allowing you to author AWS Lambda
      functions that execute locally.
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
            title: greengrass
          paths:
            /greengrass/groups/{GroupId}/role:
              GET:
                summary: GetAssociatedRole
                description: Retrieves the role associated with a particular group.
                tags:
                  - Get
                  - Associated
                  - Roles
                  - Group
                  - Identifiers
                  - Roles
            /greengrass/servicerole:
              GET:
                summary: GetServiceRoleForAccount
                description: Retrieves the service role that is attached to your account.
                tags:
                  - Get
                  - Services
                  - Roles
                  - For
                  - Account
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
            /greengrass/definition/connectors:
              GET:
                summary: ListConnectorDefinitions
                description: Retrieves a list of connector definitions.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions:
              GET:
                summary: ListConnectorDefinitionVersions
                description: >-
                  Lists the versions of a connector definition, which are
                  containers for connectors. Connectors run on the Greengrass
                  core and contain built-in integration with local
                  infrastructure, device protocols, AWS, and other cloud
                  services.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
            /greengrass/definition/cores:
              GET:
                summary: ListCoreDefinitions
                description: Retrieves a list of core definitions.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
            /greengrass/definition/cores/{CoreDefinitionId}/versions:
              GET:
                summary: ListCoreDefinitionVersions
                description: Lists the versions of a core definition.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
            /greengrass/groups/{GroupId}/deployments:
              GET:
                summary: ListDeployments
                description: Returns a history of deployments for the group.
                tags:
                  - Lists
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
            /greengrass/definition/devices:
              GET:
                summary: ListDeviceDefinitions
                description: Retrieves a list of device definitions.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
            /greengrass/definition/devices/{DeviceDefinitionId}/versions:
              GET:
                summary: ListDeviceDefinitionVersions
                description: Lists the versions of a device definition.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
            /greengrass/definition/functions:
              GET:
                summary: ListFunctionDefinitions
                description: Retrieves a list of Lambda function definitions.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions:
              GET:
                summary: ListFunctionDefinitionVersions
                description: Lists the versions of a Lambda function definition.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
            /greengrass/groups:
              GET:
                summary: ListGroups
                description: Retrieves a list of groups.
                tags:
                  - Lists
                  - Groups
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
            /greengrass/groups/{GroupId}/certificateauthorities:
              GET:
                summary: ListGroupCertificateAuthorities
                description: Retrieves the current CAs for a group.
                tags:
                  - Lists
                  - Group
                  - Certificates
                  - Authorities
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/groups/{GroupId}/versions:
              GET:
                summary: ListGroupVersions
                description: Lists the versions of a group.
                tags:
                  - Lists
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/definition/loggers:
              GET:
                summary: ListLoggerDefinitions
                description: Retrieves a list of logger definitions.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions:
              GET:
                summary: ListLoggerDefinitionVersions
                description: Lists the versions of a logger definition.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
            /greengrass/definition/resources:
              GET:
                summary: ListResourceDefinitions
                description: Retrieves a list of resource definitions.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
            /greengrass/definition/resources/{ResourceDefinitionId}/versions:
              GET:
                summary: ListResourceDefinitionVersions
                description: Lists the versions of a resource definition.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
            /greengrass/updates:
              POST:
                summary: CreateSoftwareUpdateJob
                description: >-
                  Creates a software update for a core or group of cores
                  (specified as an IoT thing group.) Use this to update the OTA
                  Agent as well as the Greengrass core software. It makes use of
                  the IoT Jobs feature which provides additional commands to
                  manage a Greengrass core software update job.
                tags:
                  - Create
                  - Software
                  - Update
                  - Jobs
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
            /greengrass/definition/subscriptions:
              GET:
                summary: ListSubscriptionDefinitions
                description: Retrieves a list of subscription definitions.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions:
              GET:
                summary: ListSubscriptionDefinitionVersions
                description: Lists the versions of a subscription definition.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/connectors/{ConnectorDefinitionId}:
              PUT:
                summary: UpdateConnectorDefinition
                description: Updates a connector definition.
                tags:
                  - Update
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/cores/{CoreDefinitionId}:
              PUT:
                summary: UpdateCoreDefinition
                description: Updates a core definition.
                tags:
                  - Update
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/devices/{DeviceDefinitionId}:
              PUT:
                summary: UpdateDeviceDefinition
                description: Updates a device definition.
                tags:
                  - Update
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/functions/{FunctionDefinitionId}:
              PUT:
                summary: UpdateFunctionDefinition
                description: Updates a Lambda function definition.
                tags:
                  - Update
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/groups/{GroupId}:
              PUT:
                summary: UpdateGroup
                description: Updates a group.
                tags:
                  - Update
                  - Group
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/loggers/{LoggerDefinitionId}:
              PUT:
                summary: UpdateLoggerDefinition
                description: Updates a logger definition.
                tags:
                  - Update
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/resources/{ResourceDefinitionId}:
              PUT:
                summary: UpdateResourceDefinition
                description: Updates a resource definition.
                tags:
                  - Update
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}:
              PUT:
                summary: UpdateSubscriptionDefinition
                description: Updates a subscription definition.
                tags:
                  - Update
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/bulk/deployments/{BulkDeploymentId}/status:
              GET:
                summary: GetBulkDeploymentStatus
                description: Returns the status of a bulk deployment.
                tags:
                  - Get
                  - Bulk
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
            /greengrass/things/{ThingName}/connectivityInfo:
              PUT:
                summary: UpdateConnectivityInfo
                description: >-
                  Updates the connectivity information for the core. Any devices
                  that belong to the group which has this core will receive this
                  information in order to find the location of the core and
                  connect to it.
                tags:
                  - Update
                  - Connectivity
                  - Info
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions/{ConnectorDefinitionVersionId}:
              GET:
                summary: GetConnectorDefinitionVersion
                description: >-
                  Retrieves information about a connector definition version,
                  including the connectors that the version contains. Connectors
                  are prebuilt modules that interact with local infrastructure,
                  device protocols, AWS, and other cloud services.
                tags:
                  - Get
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/cores/{CoreDefinitionId}/versions/{CoreDefinitionVersionId}:
              GET:
                summary: GetCoreDefinitionVersion
                description: Retrieves information about a core definition version.
                tags:
                  - Get
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/deployments/{DeploymentId}/status:
              GET:
                summary: GetDeploymentStatus
                description: Returns the status of a deployment.
                tags:
                  - Get
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/devices/{DeviceDefinitionId}/versions/{DeviceDefinitionVersionId}:
              GET:
                summary: GetDeviceDefinitionVersion
                description: Retrieves information about a device definition version.
                tags:
                  - Get
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions/{FunctionDefinitionVersionId}:
              GET:
                summary: GetFunctionDefinitionVersion
                description: >-
                  Retrieves information about a Lambda function definition
                  version, including which Lambda functions are included in the
                  version and their configurations.
                tags:
                  - Get
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/certificateauthorities/{CertificateAuthorityId}:
              GET:
                summary: GetGroupCertificateAuthority
                description: >-
                  Retreives the CA associated with a group. Returns the public
                  key of the CA.
                tags:
                  - Get
                  - Group
                  - Certificates
                  - Authority
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
            /greengrass/groups/{GroupId}/certificateauthorities/configuration/expiry:
              PUT:
                summary: UpdateGroupCertificateConfiguration
                description: Updates the Certificate expiry time for a group.
                tags:
                  - Update
                  - Group
                  - Certificates
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/groups/{GroupId}/versions/{GroupVersionId}:
              GET:
                summary: GetGroupVersion
                description: Retrieves information about a group version.
                tags:
                  - Get
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions/{LoggerDefinitionVersionId}:
              GET:
                summary: GetLoggerDefinitionVersion
                description: Retrieves information about a logger definition version.
                tags:
                  - Get
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/resources/{ResourceDefinitionId}/versions/{ResourceDefinitionVersionId}:
              GET:
                summary: GetResourceDefinitionVersion
                description: >-
                  Retrieves information about a resource definition version,
                  including which resources are included in the version.
                tags:
                  - Get
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions/{SubscriptionDefinitionVersionId}:
              GET:
                summary: GetSubscriptionDefinitionVersion
                description: Retrieves information about a subscription definition version.
                tags:
                  - Get
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/things/{ThingName}/runtimeconfig:
              PUT:
                summary: UpdateThingRuntimeConfiguration
                description: Updates the runtime configuration of a thing.
                tags:
                  - Update
                  - Things
                  - Runtime
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
            /greengrass/bulk/deployments/{BulkDeploymentId}/detailed-reports:
              GET:
                summary: ListBulkDeploymentDetailedReports
                description: >-
                  Gets a paginated list of the deployments that have been
                  started in a bulk deployment operation, and their current
                  deployment status.
                tags:
                  - Lists
                  - Bulk
                  - Deployments
                  - Detailed
                  - Reports
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /greengrass/bulk/deployments:
              POST:
                summary: StartBulkDeployment
                description: >-
                  Deploys multiple groups in one operation. This action starts
                  the bulk deployment of a specified set of group versions. Each
                  group version deployment will be triggered with an adaptive
                  rate that has a fixed upper limit. We recommend that you
                  include an ''X-Amzn-Client-Token'' token in every
                  ''StartBulkDeployment'' request. These requests are idempotent
                  with respect to the token and the request parameters.
                tags:
                  - Start
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: Remove resource tags from a Greengrass Resource.
                tags:
                  - Untag
                  - Resources
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
            /greengrass/groups/{GroupId}/deployments/$reset:
              POST:
                summary: ResetDeployments
                description: Resets a group's deployments.
                tags:
                  - Reset
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
            /greengrass/bulk/deployments/{BulkDeploymentId}/$stop:
              PUT:
                summary: StopBulkDeployment
                description: >-
                  Stops the execution of a bulk deployment. This action returns
                  a status of ''Stopping'' until the deployment is stopped. You
                  cannot start a new bulk deployment while a previous deployment
                  is in the ''Stopping'' state. This action doesn't rollback
                  completed deployments or cancel pending de
                tags:
                  - Stop
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/greengrass-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrass-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrass
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---