---
name: Bootstrap
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bootstrap.png
url: https://example.com/apis/bootstrap.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bootstrap
apis:
  - name: kafka
    description: <p>The operations for managing an Amazon MSK cluster.</p>
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
            title: kafka
          paths:
            /v1/clusters/{clusterArn}/scram-secrets:
              GET:
                summary: ListScramSecrets
                description: >-
                  <p>Returns a list of the Scram Secrets associated with an
                  Amazon MSK cluster.</p>
                tags:
                  - Lists
                  - Scram
                  - Secrets
                  - ARN
                  - Scram
                  - Secrets
            /v1/clusters:
              GET:
                summary: ListClusters
                description: >-
                  <p>Returns a list of all the MSK clusters in the current
                  Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
            /api/v2/clusters:
              GET:
                summary: ListClustersV2
                description: >-
                  <p>Returns a list of all the MSK clusters in the current
                  Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
            /replication/v1/replicators:
              GET:
                summary: ListReplicators
                description: <p>Lists the replicators.</p>
                tags:
                  - Lists
                  - Replicators
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
            /v1/configurations:
              GET:
                summary: ListConfigurations
                description: >-
                  <p>Returns a list of all the MSK configurations in this
                  Region.</p>
                tags:
                  - Lists
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
            /v1/vpc-connection:
              POST:
                summary: CreateVpcConnection
                description: <p>Creates a new Amazon MSK VPC connection.</p>
                tags:
                  - Create
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
            /v1/clusters/{clusterArn}:
              GET:
                summary: DescribeCluster
                description: >-
                  <p>Returns a description of the MSK cluster whose Amazon
                  Resource Name (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Cluster
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
            /v1/clusters/{clusterArn}/policy:
              PUT:
                summary: PutClusterPolicy
                description: >-
                  <p>Creates or updates the specified MSK cluster policy. If
                  updating the policy, the currentVersion field is required in
                  the request payload.</p>
                tags:
                  - Put
                  - Cluster
                  - Policies
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/configurations/{arn}:
              PUT:
                summary: UpdateConfiguration
                description: >-
                  <p>Updates an existing MSK configuration. The configuration
                  must be in the Active state.</p>
                tags:
                  - Update
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /replication/v1/replicators/{replicatorArn}:
              GET:
                summary: DescribeReplicator
                description: >-
                  <p>Returns a description of the Kafka Replicator whose Amazon
                  Resource Name (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Replicators
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/vpc-connection/{arn}:
              GET:
                summary: DescribeVpcConnection
                description: >-
                  <p>Displays information about the specified Amazon MSK VPC
                  connection.</p>
                tags:
                  - Describe
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /api/v2/clusters/{clusterArn}:
              GET:
                summary: DescribeClusterV2
                description: >-
                  <p>Returns a description of the MSK cluster of either the
                  provisioned or the serverless type whose Amazon Resource Name
                  (ARN) is specified in the request.</p>
                tags:
                  - Describe
                  - Cluster
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
            /v1/operations/{clusterOperationArn}:
              GET:
                summary: DescribeClusterOperation
                description: >-
                  <p>Returns a description of the cluster operation specified by
                  the ARN.</p>
                tags:
                  - Describe
                  - Cluster
                  - Operation
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
            /api/v2/operations/{clusterOperationArn}:
              GET:
                summary: DescribeClusterOperationV2
                description: >-
                  <p>Returns a description of the cluster operation specified by
                  the ARN.</p>
                tags:
                  - Describe
                  - Cluster
                  - Operation
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
            /v1/configurations/{arn}/revisions/{revision}:
              GET:
                summary: DescribeConfigurationRevision
                description: >-
                  <p>Returns a description of this revision of the
                  configuration.</p>
                tags:
                  - Describe
                  - Configurations
                  - Revisions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
            /v1/clusters/{clusterArn}/bootstrap-brokers:
              GET:
                summary: GetBootstrapBrokers
                description: >-
                  <p>A list of brokers that a client application can use to
                  bootstrap.</p>
                tags:
                  - Get
                  - Bootstrap
                  - Brokers
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
            /v1/compatible-kafka-versions:
              GET:
                summary: GetCompatibleKafkaVersions
                description: >-
                  <p>Gets the Apache Kafka versions to which you can update the
                  MSK cluster.</p>
                tags:
                  - Get
                  - Compatible
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
            /v1/clusters/{clusterArn}/client-vpc-connections:
              GET:
                summary: ListClientVpcConnections
                description: <p>Displays a list of client VPC connections.</p>
                tags:
                  - Lists
                  - Client
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
            /v1/clusters/{clusterArn}/operations:
              GET:
                summary: ListClusterOperations
                description: >-
                  <p>Returns a list of all the operations that have been
                  performed on the specified MSK cluster.</p>
                tags:
                  - Lists
                  - Cluster
                  - Operations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /api/v2/clusters/{clusterArn}/operations:
              GET:
                summary: ListClusterOperationsV2
                description: >-
                  <p>Returns a list of all the operations that have been
                  performed on the specified MSK cluster.</p>
                tags:
                  - Lists
                  - Cluster
                  - Operations
                  - V2
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/configurations/{arn}/revisions:
              GET:
                summary: ListConfigurationRevisions
                description: >-
                  <p>Returns a list of all the revisions of an MSK
                  configuration.</p>
                tags:
                  - Lists
                  - Configurations
                  - Revisions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/kafka-versions:
              GET:
                summary: ListKafkaVersions
                description: <p>Returns a list of Apache Kafka versions.</p>
                tags:
                  - Lists
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
            /v1/clusters/{clusterArn}/nodes:
              GET:
                summary: ListNodes
                description: <p>Returns a list of the broker nodes in the cluster.</p>
                tags:
                  - Lists
                  - Nodes
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes the tags associated with the keys that are provided
                  in the query.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/vpc-connections:
              GET:
                summary: ListVpcConnections
                description: <p>Displays a list of Amazon MSK VPC connections.</p>
                tags:
                  - Lists
                  - VPC
                  - Connections
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
            /v1/clusters/{clusterArn}/reboot-broker:
              PUT:
                summary: RebootBroker
                description: <p>Executes a reboot on a broker.</p>
                tags:
                  - Reboot
                  - Brokers
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
            /v1/clusters/{clusterArn}/nodes/count:
              PUT:
                summary: UpdateBrokerCount
                description: >-
                  <p>Updates the number of broker nodes in the cluster. You can
                  use this operation to increase the number of brokers in an
                  existing cluster. You can't decrease the number of
                  brokers.</p>
                tags:
                  - Update
                  - Brokers
                  - Count
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
            /v1/clusters/{clusterArn}/nodes/type:
              PUT:
                summary: UpdateBrokerType
                description: >-
                  <p>Updates all the brokers in the cluster to the specified
                  type.</p>
                tags:
                  - Update
                  - Brokers
                  - Types
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
            /v1/clusters/{clusterArn}/nodes/storage:
              PUT:
                summary: UpdateBrokerStorage
                description: <p>Updates the EBS storage associated with MSK brokers.</p>
                tags:
                  - Update
                  - Brokers
                  - Storage
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
            /v1/clusters/{clusterArn}/connectivity:
              PUT:
                summary: UpdateConnectivity
                description: >-
                  <p>Updates the connectivity configuration for the MSK
                  cluster.</p>
                tags:
                  - Update
                  - Connectivity
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
            /v1/clusters/{clusterArn}/configuration:
              PUT:
                summary: UpdateClusterConfiguration
                description: >-
                  <p>Updates the cluster with the configuration that is
                  specified in the request body.</p>
                tags:
                  - Update
                  - Cluster
                  - Configurations
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
            /v1/clusters/{clusterArn}/version:
              PUT:
                summary: UpdateClusterKafkaVersion
                description: <p>Updates the Apache Kafka version for the cluster.</p>
                tags:
                  - Update
                  - Cluster
                  - Kafka
                  - Versions
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
            /v1/clusters/{clusterArn}/monitoring:
              PUT:
                summary: UpdateMonitoring
                description: >-
                  <p>Updates the monitoring settings for the cluster. You can
                  use this operation to specify which Apache Kafka metrics you
                  want Amazon MSK to send to Amazon CloudWatch. You can also
                  specify settings for open monitoring with Prometheus.</p>
                tags:
                  - Update
                  - Monitoring
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
            /replication/v1/replicators/{replicatorArn}/replication-info:
              PUT:
                summary: UpdateReplicationInfo
                description: <p>Updates replication info of a replicator.</p>
                tags:
                  - Update
                  - Replication
                  - Info
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
            /v1/clusters/{clusterArn}/security:
              PATCH:
                summary: UpdateSecurity
                description: >-
                  <p>You can use this operation to update the encrypting and
                  authentication settings for an existing cluster.</p>
                tags:
                  - Update
                  - Security
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
                  - Security
            /v1/clusters/{clusterArn}/storage:
              PUT:
                summary: UpdateStorage
                description: >-
                  <p>Updates cluster broker volume size (or) sets cluster
                  storage mode to T
                tags:
                  - Update
                  - Storage
                  - ARN
                  - Scram
                  - Secrets
                  - V1
                  - Clusters
                  - APIs
                  - V2
                  - Replication
                  - Replicators
                  - Configurations
                  - VPC
                  - Connections
                  - Policies
                  - Operation
                  - Revisions
                  - Revisions
                  - Bootstrap
                  - Brokers
                  - Compatible
                  - Kafka
                  - Versions
                  - Client
                  - Connections
                  - Operations
                  - Nodes
                  - Reboot
                  - Brokers
                  - Count
                  - Types
                  - Storage
                  - Connectivity
                  - Configurations
                  - Versions
                  - Monitoring
                  - Info
                  - Securi
    overlays:
      - type: APIs.io Search
        url: overlays/kafka-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kafka-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kafka
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---