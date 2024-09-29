---
name: Anywhere
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anywhere.png
url: https://example.com/apis/anywhere.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anywhere
apis:
  - name: eks
    description: >-
      <p>Amazon Elastic Kubernetes Service (Amazon EKS) is a managed service
      that makes it easy for you to run Kubernetes on Amazon Web Services
      without needing to setup or maintain your own Kubernetes control plane.
      Kubernetes is an open-source system for automating the deployment,
      scaling, and management of containerized applications.</p> <p>Amazon EKS
      runs up-to-date versions of the open-source Kubernetes software, so you
      can use all the existing plugins and tooling from the Kubernetes
      community. Applications running on Amazon EKS are fully compatible with
      applications running on any standard Kubernetes environment, whether
      running in on-premises data centers or public clouds. This means that you
      can easily migrate any standard Kubernetes application to Amazon EKS
      without any code modification required.</p>
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
            title: eks
          paths:
            /clusters/{name}/access-entries/{principalArn}/access-policies:
              GET:
                summary: ListAssociatedAccessPolicies
                description: >-
                  <p>Lists the access policies associated with an access
                  entry.</p>
                tags:
                  - Lists
                  - Associated
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
            /clusters/{name}/encryption-config/associate:
              POST:
                summary: AssociateEncryptionConfig
                description: >-
                  <p>Associates an encryption configuration to an existing
                  cluster.</p> <p>Use this API to enable encryption on existing
                  clusters that don't already have encryption enabled. This
                  allows you to implement a defense-in-depth security strategy
                  without migrating applications to new Amazon EKS clusters.</p>
                tags:
                  - Associate
                  - Encryption
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
            /clusters/{name}/identity-provider-configs/associate:
              POST:
                summary: AssociateIdentityProviderConfig
                description: >-
                  <p>Associates an identity provider configuration to a
                  cluster.</p> <p>If you want to authenticate identities using
                  an identity provider, you can create an identity provider
                  configuration and associate it to your cluster. After
                  configuring authentication to your cluster you can create
                  Kubernetes <code>Role</code> and <code>ClusterRole</code>
                  objects, assign permissions to them, and then bind them to the
                  identities using Kubernetes <code>RoleBinding</code> and
                  <code>ClusterRoleBinding</code> objects. For more information
                  see <a
                  href="https://kubernetes.io/docs/reference/access-authn-authz/rbac/">Using
                  RBAC Authorization</a> in the Kubernetes documentation.</p>
                tags:
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
            /clusters/{name}/access-entries:
              GET:
                summary: ListAccessEntries
                description: <p>Lists the access entries for your cluster.</p>
                tags:
                  - Lists
                  - Access
                  - Entries
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
            /clusters/{name}/addons:
              GET:
                summary: ListAddons
                description: <p>Lists the installed add-ons.</p>
                tags:
                  - Lists
                  - Addons
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
            /clusters:
              GET:
                summary: ListClusters
                description: >-
                  <p>Lists the Amazon EKS clusters in your Amazon Web Services
                  account in the specified Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Clusters
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
            /eks-anywhere-subscriptions:
              GET:
                summary: ListEksAnywhereSubscriptions
                description: <p>Displays the full description of the subscription.</p>
                tags:
                  - Lists
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
            /clusters/{name}/fargate-profiles:
              GET:
                summary: ListFargateProfiles
                description: >-
                  <p>Lists the Fargate profiles associated with the specified
                  cluster in your Amazon Web Services account in the specified
                  Amazon Web Services Region.</p>
                tags:
                  - Lists
                  - Fargate
                  - Profiles
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
            /clusters/{name}/node-groups:
              GET:
                summary: ListNodegroups
                description: >-
                  <p>Lists the managed node groups associated with the specified
                  cluster in your Amazon Web Services account in the specified
                  Amazon Web Services Region. Self-managed node groups aren't
                  listed.</p>
                tags:
                  - Lists
                  - Node Groups
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
            /clusters/{name}/pod-identity-associations:
              GET:
                summary: ListPodIdentityAssociations
                description: >-
                  <p>List the EKS Pod Identity associations in a cluster. You
                  can filter the list by the namespace that the association is
                  in or the service account that the association uses.</p>
                tags:
                  - Lists
                  - Pods
                  - Identity
                  - Associations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}/access-entries/{principalArn}:
              POST:
                summary: UpdateAccessEntry
                description: <p>Updates an access entry.</p>
                tags:
                  - Update
                  - Access
                  - Entry
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}/addons/{addonName}:
              GET:
                summary: DescribeAddon
                description: <p>Describes an Amazon EKS add-on.</p>
                tags:
                  - Describe
                  - Addon
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /clusters/{name}:
              GET:
                summary: DescribeCluster
                description: >-
                  <p>Describes an Amazon EKS cluster.</p> <p>The API server
                  endpoint and certificate authority data returned by this
                  operation are required for <code>kubelet</code> and
                  <code>kubectl</code> to communicate with your Kubernetes API
                  server. For more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/create-kubeconfig.html">Creating
                  or updating a <code>kubeconfig</code> file for an Amazon EKS
                  cluster</a>.</p> <note> <p>The API server endpoint and
                  certificate authority data aren't available until the cluster
                  reaches the <code>ACTIVE</code> state.</p> </note>
                tags:
                  - Describe
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
            /eks-anywhere-subscriptions/{id}:
              POST:
                summary: UpdateEksAnywhereSubscription
                description: >-
                  <p>Update an EKS Anywhere Subscription. Only auto renewal and
                  tags can be updated after subscription creation.</p>
                tags:
                  - Update
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
            /clusters/{name}/fargate-profiles/{fargateProfileName}:
              GET:
                summary: DescribeFargateProfile
                description: <p>Describes an Fargate profile.</p>
                tags:
                  - Describe
                  - Fargate
                  - Profiles
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /clusters/{name}/node-groups/{nodegroupName}:
              GET:
                summary: DescribeNodegroup
                description: <p>Describes a managed node group.</p>
                tags:
                  - Describe
                  - Node Groups
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /clusters/{name}/pod-identity-associations/{associationId}:
              POST:
                summary: UpdatePodIdentityAssociation
                description: >-
                  <p>Updates a EKS Pod Identity association. Only the IAM role
                  can be changed; an association can't be moved between
                  clusters, namespaces, or service accounts. If you need to edit
                  the namespace or service account, you need to delete the
                  association and then create a new association with your
                  desired settings.</p>
                tags:
                  - Update
                  - Pods
                  - Identity
                  - Association
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
            /cluster-registrations/{name}:
              DELETE:
                summary: DeregisterCluster
                description: >-
                  <p>Deregisters a connected cluster to remove it from the
                  Amazon EKS control plane.</p> <p>A connected cluster is a
                  Kubernetes cluster that you've connected to your control plane
                  using the <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-connector.html">Amazon
                  EKS Connector</a>.</p>
                tags:
                  - Deregister
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
            /addons/configuration-schemas:
              GET:
                summary: DescribeAddonConfiguration
                description: <p>Returns configuration options.</p>
                tags:
                  - Describe
                  - Addon
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
            /addons/supported-versions:
              GET:
                summary: DescribeAddonVersions
                description: >-
                  <p>Describes the versions for an add-on.</p> <p>Information
                  such as the Kubernetes versions that you can use the add-on
                  with, the <code>owner</code>, <code>publisher</code>, and the
                  <code>type</code> of the add-on are returned.</p>
                tags:
                  - Describe
                  - Addon
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
            /clusters/{name}/identity-provider-configs/describe:
              POST:
                summary: DescribeIdentityProviderConfig
                description: <p>Describes an identity provider configuration.</p>
                tags:
                  - Describe
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
            /clusters/{name}/insights/{id}:
              GET:
                summary: DescribeInsight
                description: >-
                  <p>Returns details about an insight that you specify using its
                  ID.</p>
                tags:
                  - Describe
                  - Insight
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
            /clusters/{name}/updates/{updateId}:
              GET:
                summary: DescribeUpdate
                description: >-
                  <p>Describes an update to an Amazon EKS resource.</p> <p>When
                  the status of the update is <code>Succeeded</code>, the update
                  is complete. If an update fails, the status is
                  <code>Failed</code>, and an error detail explains the reason
                  for the failure.</p>
                tags:
                  - Describe
                  - Update
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
            /clusters/{name}/access-entries/{principalArn}/access-policies/{policyArn}:
              DELETE:
                summary: DisassociateAccessPolicy
                description: <p>Disassociates an access policy from an access entry.</p>
                tags:
                  - Disassociate
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
            /clusters/{name}/identity-provider-configs/disassociate:
              POST:
                summary: DisassociateIdentityProviderConfig
                description: >-
                  <p>Disassociates an identity provider configuration from a
                  cluster.</p> <p>If you disassociate an identity provider from
                  your cluster, users included in the provider can no longer
                  access the cluster. However, you can still access the cluster
                  with IAM principals.</p>
                tags:
                  - Disassociate
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /access-policies:
              GET:
                summary: ListAccessPolicies
                description: <p>Lists the available access policies. </p>
                tags:
                  - Lists
                  - Access
                  - Policies
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/identity-provider-configs:
              GET:
                summary: ListIdentityProviderConfigs
                description: >-
                  <p>Lists the identity provider configurations for your
                  cluster.</p>
                tags:
                  - Lists
                  - Identity
                  - Providers
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/insights:
              POST:
                summary: ListInsights
                description: >-
                  <p>Returns a list of all insights checked for against the
                  specified cluster. You can filter which insights are returned
                  by category, associated Kubernetes version, and status.</p>
                tags:
                  - Lists
                  - Insights
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deletes specified tags from an Amazon EKS resource.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
            /clusters/{name}/updates:
              POST:
                summary: UpdateClusterVersion
                description: >-
                  <p>Updates an Amazon EKS cluster to the specified Kubernetes
                  version. Your cluster continues to function during the update.
                  The response output includes an update ID that you can use to
                  track the status of your cluster update with the
                  <a>DescribeUpdate</a> API operation.</p> <p>Cluster updates
                  are asynchronous, and they should finish within a few minutes.
                  During an update, the cluster status moves to
                  <code>UPDATING</code> (this status transition is eventually
                  consistent). When the update is complete (either
                  <code>Failed</code> or <code>Successful</code>), the cluster
                  status moves to <code>Active</code>.</p> <p>If your cluster
                  has managed node groups attached to it, all of your node
                  groups’ Kubernetes versions must match the cluster’s
                  Kubernetes version in order to update the cluster to a new
                  Kubernetes version.</p>
                tags:
                  - Update
                  - Cluster
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
            /cluster-registrations:
              POST:
                summary: RegisterCluster
                description: >-
                  <p>Connects a Kubernetes cluster to the Amazon EKS control
                  plane. </p> <p>Any Kubernetes cluster can be connected to the
                  Amazon EKS control plane to view current information about the
                  cluster and its nodes. </p> <p>Cluster connection requires two
                  steps. First, send a <code> <a>RegisterClusterRequest</a>
                  </code> to add it to the Amazon EKS control plane.</p>
                  <p>Second, a <a
                  href="https://amazon-eks.s3.us-west-2.amazonaws.com/eks-connector/manifests/eks-connector/latest/eks-connector.yaml">Manifest</a>
                  containing the <code>activationID</code> and
                  <code>activationCode</code> must be applied to the Kubernetes
                  cluster through it's native provider to provide
                  visibility.</p> <p>After the manifest is updated and applied,
                  the connected cluster is visible to the Amazon EKS control
                  plane. If the manifest isn't applied within three days, the
                  connected cluster will no longer be visible and must be
                  deregistered using <code>DeregisterCluster</code>.</p>
                tags:
                  - Register
                  - Cluster
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
            /clusters/{name}/addons/{addonName}/update:
              POST:
                summary: UpdateAddon
                description: <p>Updates an Amazon EKS add-on.</p>
                tags:
                  - Update
                  - Addon
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/update-config:
              POST:
                summary: UpdateClusterConfig
                description: >-
                  <p>Updates an Amazon EKS cluster configuration. Your cluster
                  continues to function during the update. The response output
                  includes an update ID that you can use to track the status of
                  your cluster update with
                  <code>DescribeUpdate</code>"/&gt;.</p> <p>You can use this API
                  operation to enable or disable exporting the Kubernetes
                  control plane logs for your cluster to CloudWatch Logs. By
                  default, cluster control plane logs aren't exported to
                  CloudWatch Logs. For more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/control-plane-logs.html">Amazon
                  EKS Cluster control plane logs</a> in the <i> <i>Amazon EKS
                  User Guide</i> </i>.</p> <note> <p>CloudWatch Logs ingestion,
                  archive storage, and data scanning rates apply to exported
                  control plane logs. For more information, see <a
                  href="http://aws.amazon.com/cloudwatch/pricing/">CloudWatch
                  Pricing</a>.</p> </note> <p>You can also use this API
                  operation to enable or disable public and private access to
                  your cluster's Kubernetes API server endpoint. By default,
                  public access is enabled, and private access is disabled. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/cluster-endpoint.html">Amazon
                  EKS cluster endpoint access control</a> in the <i> <i>Amazon
                  EKS User Guide</i> </i>.</p> <p>You can also use this API
                  operation to choose different subnets and security groups for
                  the cluster. You must specify at least two subnets that are in
                  different Availability Zones. You can't change which VPC the
                  subnets are from, the subnets must be in the same VPC as the
                  subnets that the cluster was created with. For more
                  information about the VPC requirements, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html">https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html</a>
                  in the <i> <i>Amazon EKS User Guide</i> </i>.</p> <p>Cluster
                  updates are asynchronous, and they should finish within a few
                  minutes. During an update, the cluster status moves to
                  <code>UPDATING</code> (this status transition is eventually
                  consistent). When the update is complete (either
                  <code>Failed</code> or <code>Successful</code>), the cluster
                  status moves to <code>Active</code>.</p>
                tags:
                  - Update
                  - Cluster
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/node-groups/{nodegroupName}/update-config:
              POST:
                summary: UpdateNodegroupConfig
                description: >-
                  <p>Updates an Amazon EKS managed node group configuration.
                  Your node group continues to function during the update. The
                  response output includes an update ID that you can use to
                  track the status of your node group update with the
                  <a>DescribeUpdate</a> API operation. Currently you can update
                  the Kubernetes labels for a node group or the scaling
                  configuration.</p>
                tags:
                  - Update
                  - Node Groups
                  - Configurations
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
            /clusters/{name}/node-groups/{nodegroupName}/update-version:
              POST:
                summary: UpdateNodegroupVersion
                description: >-
                  <p>Updates the Kubernetes version or AMI version of an Amazon
                  EKS managed node group.</p> <p>You can update a node group
                  using a launch template only if the node group was originally
                  deployed with a launch template. If you need to update a
                  custom AMI in a node group that was deployed with a launch
                  template, then update your custom AMI, specify the new ID in a
                  new version of the launch template, and then update the node
                  group to the new version of the launch template.</p> <p>If you
                  update without a launch template, then you can update to the
                  latest available AMI version of a node group's current
                  Kubernetes version by not specifying a Kubernetes version in
                  the request. You can update to the latest AMI version of your
                  cluster's current Kubernetes version by specifying your
                  cluster's Kubernetes version in the request. For information
                  about Linux versions, see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-linux-ami-versions.html">Amazon
                  EKS optimized Amazon Linux AMI versions</a> in the <i>Amazon
                  EKS User Guide</i>. For information about Windows versions,
                  see <a
                  href="https://docs.aws.amazon.com/eks/latest/userguide/eks-ami-versions-windows.html">Amazon
                  EKS optimized Windows AMI versions</a> in the <i>Amazon EKS
                  User Guide</i>. </p> <p>You cannot roll back a node group to
                  an earlier Kubernetes version or AMI version.</p> <p>When a
                  node in a managed node group is terminated due to a scaling
                  action or update, every <code>Pod</code> on that node is
                  drained first. Amazon EKS attempts to drain the nodes
                  gracefully and will fail if it is unable to do so. You can
                  <code>force</code> the update if Amazon EKS is unable to drain
                  the nodes as a result of a <code>Pod</code> disruption budget 
                tags:
                  - Update
                  - Node Groups
                  - Versions
                  - ARN
                  - Access
                  - Policies
                  - Clusters
                  - Names
                  - Encryption
                  - Configurations
                  - Associate
                  - Identity
                  - Providers
                  - Configurations
                  - Entries
                  - Addons
                  - EKS
                  - Anywhere
                  - Subscriptions
                  - Fargate
                  - Profiles
                  - Nodes
                  - Groups
                  - Pods
                  - Associations
                  - Identifiers
                  - Profiles
                  - Cluster
                  - Registrations
                  - Configurations
                  - Schemas
                  - Supported
                  - Versions
                  - Describe
                  - Insights
                  - Policies
                  - Disassociate
                  - Updates
                  - Update
                  - Versions
    overlays:
      - type: APIs.io Search
        url: overlays/eks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/eks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:eks
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---