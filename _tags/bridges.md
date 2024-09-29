---
name: Bridges
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bridges.png
url: https://example.com/apis/bridges.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bridges
apis:
  - name: mediaconnect
    description: API for AWS Elemental MediaConnect
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
            title: mediaconnect
          paths:
            /v1/bridges/{bridgeArn}/outputs:
              POST:
                summary: AddBridgeOutputs
                description: Adds outputs to an existing bridge.
                tags:
                  - Add
                  - Bridges
                  - Outputs
                  - ARN
                  - Outputs
            /v1/bridges/{bridgeArn}/sources:
              POST:
                summary: AddBridgeSources
                description: Adds sources to an existing bridge.
                tags:
                  - Add
                  - Bridges
                  - Sources
                  - ARN
                  - Outputs
                  - Sources
            /v1/flows/{flowArn}/mediaStreams:
              POST:
                summary: AddFlowMediaStreams
                description: >-
                  Adds media streams to an existing flow. After you add a media
                  stream to a flow, you can associate it with a source and/or an
                  output that uses the ST 2110 JPEG XS or CDI protocol.
                tags:
                  - Add
                  - Flow
                  - Media
                  - Streams
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
            /v1/flows/{flowArn}/outputs:
              POST:
                summary: AddFlowOutputs
                description: >-
                  Adds outputs to an existing flow. You can create up to 50
                  outputs per flow.
                tags:
                  - Add
                  - Flow
                  - Outputs
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
            /v1/flows/{flowArn}/source:
              POST:
                summary: AddFlowSources
                description: Adds Sources to flow
                tags:
                  - Add
                  - Flow
                  - Sources
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
            /v1/flows/{flowArn}/vpcInterfaces:
              POST:
                summary: AddFlowVpcInterfaces
                description: Adds VPC interfaces to flow
                tags:
                  - Add
                  - Flow
                  - VPC
                  - Interfaces
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
            /v1/bridges:
              GET:
                summary: ListBridges
                description: >-
                  Displays a list of bridges that are associated with this
                  account and an optionally specified Arn. This request returns
                  a paginated result.
                tags:
                  - Lists
                  - Bridges
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
            /v1/flows:
              GET:
                summary: ListFlows
                description: >-
                  Displays a list of flows that are associated with this
                  account. This request returns a paginated result.
                tags:
                  - Lists
                  - Flows
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
            /v1/gateways:
              GET:
                summary: ListGateways
                description: >-
                  Displays a list of gateways that are associated with this
                  account. This request returns a paginated result.
                tags:
                  - Lists
                  - Gateways
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
            /v1/bridges/{bridgeArn}:
              PUT:
                summary: UpdateBridge
                description: Updates the bridge
                tags:
                  - Update
                  - Bridges
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
            /v1/flows/{flowArn}:
              PUT:
                summary: UpdateFlow
                description: Updates flow
                tags:
                  - Update
                  - Flow
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
            /v1/gateways/{gatewayArn}:
              GET:
                summary: DescribeGateway
                description: >-
                  Displays the details of a gateway. The response includes the
                  gateway ARN, name, and CIDR blocks, as well as details about
                  the networks.
                tags:
                  - Describe
                  - Gateway
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
            /v1/gateway-instances/{gatewayInstanceArn}:
              PUT:
                summary: UpdateGatewayInstance
                description: Updates the configuration of an existing Gateway Instance.
                tags:
                  - Update
                  - Gateway
                  - Instances
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
            /v1/flows/{flowArn}/source-metadata:
              GET:
                summary: DescribeFlowSourceMetadata
                description: >-
                  Displays details of the flow's source stream. The response
                  contains information about the contents of the stream and its
                  programs.
                tags:
                  - Describe
                  - Flow
                  - Source
                  - Metadata
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
            /v1/offerings/{offeringArn}:
              POST:
                summary: PurchaseOffering
                description: >-
                  Submits a request to purchase an offering. If you already have
                  an active reservation, you can't purchase another offering.
                tags:
                  - Purchase
                  - Offerings
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
            /v1/reservations/{reservationArn}:
              GET:
                summary: DescribeReservation
                description: >-
                  Displays the details of a reservation. The response includes
                  the reservation name, state, start date and time, and the
                  details of the offering that make up the rest of the
                  reservation (such as price, duration, and outbound bandwidth).
                tags:
                  - Describe
                  - Reservations
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
            /v1/flows/{flowArn}/entitlements:
              POST:
                summary: GrantFlowEntitlements
                description: Grants entitlements to an existing flow.
                tags:
                  - Grant
                  - Flow
                  - Entitlements
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
            /v1/entitlements:
              GET:
                summary: ListEntitlements
                description: >-
                  Displays a list of all entitlements that have been granted to
                  this account. This request returns 20 results per page.
                tags:
                  - Lists
                  - Entitlements
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
            /v1/gateway-instances:
              GET:
                summary: ListGatewayInstances
                description: >-
                  Displays a list of instances associated with the AWS account.
                  This request returns a paginated result. You can use the
                  filterArn property to display only the instances associated
                  with the selected Gateway Amazon Resource Name (ARN).
                tags:
                  - Lists
                  - Gateway
                  - Instances
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
            /v1/offerings:
              GET:
                summary: ListOfferings
                description: >-
                  Displays a list of all offerings that are available to this
                  account in the current AWS Region. If you have an active
                  reservation (which means you've purchased an offering that has
                  already started and hasn't expired yet), your account isn't
                  eligible for other offerings.
                tags:
                  - Lists
                  - Offerings
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
            /v1/reservations:
              GET:
                summary: ListReservations
                description: >-
                  Displays a list of all reservations that have been purchased
                  by this account in the current AWS Region. This list includes
                  all reservations in all states (such as active and expired).
                tags:
                  - Lists
                  - Reservations
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: Deletes specified tags from a resource.
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
            /v1/bridges/{bridgeArn}/outputs/{outputName}:
              PUT:
                summary: UpdateBridgeOutput
                description: Updates an existing bridge output.
                tags:
                  - Update
                  - Bridges
                  - Output
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
            /v1/bridges/{bridgeArn}/sources/{sourceName}:
              PUT:
                summary: UpdateBridgeSource
                description: Updates an existing bridge source.
                tags:
                  - Update
                  - Bridges
                  - Source
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
            /v1/flows/{flowArn}/mediaStreams/{mediaStreamName}:
              PUT:
                summary: UpdateFlowMediaStream
                description: Updates an existing media stream.
                tags:
                  - Update
                  - Flow
                  - Media
                  - Stream
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
            /v1/flows/{flowArn}/outputs/{outputArn}:
              PUT:
                summary: UpdateFlowOutput
                description: Updates an existing flow output.
                tags:
                  - Update
                  - Flow
                  - Output
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
            /v1/flows/{flowArn}/source/{sourceArn}:
              PUT:
                summary: UpdateFlowSource
                description: Updates the source of a flow.
                tags:
                  - Update
                  - Flow
                  - Source
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
            /v1/flows/{flowArn}/vpcInterfaces/{vpcInterfaceName}:
              DELETE:
                summary: RemoveFlowVpcInterface
                description: >-
                  Removes a VPC Interface from an existing flow. This request
                  can be made only on a VPC interface that does not have a
                  Source or Output associated with it. If the VPC interface is
                  referenced by a Source or Output, you must first delete or
                  update the Source or Output to no longer reference the VPC
                  interface.
                tags:
                  - Removes
                  - Flow
                  - VPC
                  - Interfaces
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
                  - Interfaces
            /v1/flows/{flowArn}/entitlements/{entitlementArn}:
              PUT:
                summary: UpdateFlowEntitlement
                description: >-
                  You can change an entitlement's description, subscribers, and
                  encryption. If you change the subscribers, the service will
                  remove the outputs that are are used by the subscribers that
                  are removed.
                tags:
                  - Update
                  - Flow
                  - Entitlements
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
                  - Interfaces
                  - Entitlements
            /v1/flows/start/{flowArn}:
              POST:
                summary: StartFlow
                description: Starts a flow.
                tags:
                  - Start
                  - Flow
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
                  - Interfaces
                  - Entitlements
            /v1/flows/stop/{flowArn}:
              POST:
                summary: StopFlow
                description: Stops a flow.
                tags:
                  - Stop
                  - Flow
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
                  - Interfaces
                  - Entitlements
            /v1/bridges/{bridgeArn}/state:
              PUT:
                summary: UpdateBridgeState
                description: Updates the br
                tags:
                  - Update
                  - Bridges
                  - States
                  - ARN
                  - Outputs
                  - Sources
                  - Media
                  - Streams
                  - Source
                  - VPC
                  - Interfaces
                  - V1
                  - Bridges
                  - Flows
                  - Gateways
                  - Instances
                  - Metadata
                  - Entitlements
                  - Gateway
                  - Instances
                  - Offerings
                  - Reservations
                  - Output
                  - Names
                  - Stream
                  - Interfaces
                  - Entitlements
                  - Sta
    overlays:
      - type: APIs.io Search
        url: overlays/mediaconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediaconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediaconnect
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---