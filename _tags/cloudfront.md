---
name: Cloudfront
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cloudfront.png
url: https://example.com/apis/cloudfront.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cloudfront
apis:
  - name: cloudfront
    description: >-
      <fullname>Amazon CloudFront</fullname> <p>Amazon CloudFront is a global
      content delivery network (CDN) service that accelerates delivery of your
      websites, APIs, video content or other web assets. It integrates with
      other Amazon Web Services products to give developers and businesses an
      easy way to accelerate content to end users with no minimum usage
      commitments.</p>
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
            title: cloudfront
          paths:
            /2020-05-31/distribution/{TargetDistributionId}/associate-alias:
              PUT:
                summary: AssociateAlias
                description: >-
                  <p>Associates an alias (also known as a CNAME or an alternate
                  domain name) with a CloudFront distribution.</p> <p>With this
                  operation you can move an alias that's already in use on a
                  CloudFront distribution to a different distribution in one
                  step. This prevents the downtime that could occur if you first
                  remove the alias from one distribution and then separately add
                  the alias to another distribution.</p> <p>To use this
                  operation to associate an alias with a distribution, you
                  provide the alias and the ID of the target distribution for
                  the alias. For more information, including how to set up the
                  target distribution, prerequisites that you must complete, and
                  other restrictions, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html#alternate-domain-names-move">Moving
                  an alternate domain name to a different distribution</a> in
                  the <i>Amazon CloudFront Developer Guide</i>.</p>
                tags:
                  - Associate
                  - Alias
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
            /2020-05-31/distribution/{PrimaryDistributionId}/copy:
              POST:
                summary: CopyDistribution
                description: >-
                  <p>Creates a staging distribution using the configuration of
                  the provided primary distribution. A staging distribution is a
                  copy of an existing distribution (called the primary
                  distribution) that you can use in a continuous deployment
                  workflow.</p> <p>After you create a staging distribution, you
                  can use <code>UpdateDistribution</code> to modify the staging
                  distribution's configuration. Then you can use
                  <code>CreateContinuousDeploymentPolicy</code> to incrementally
                  move traffic to the staging distribution.</p> <p>This API
                  operation requires the following IAM permissions:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GetDistribution.html">GetDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html">CreateDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CopyDistribution.html">CopyDistribution</a>
                  </p> </li> </ul>
                tags:
                  - Copy
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
            /2020-05-31/cache-policy:
              GET:
                summary: ListCachePolicies
                description: >-
                  <p>Gets a list of cache policies.</p> <p>You can optionally
                  apply a filter to return only the managed policies created by
                  Amazon Web Services, or only the custom policies created in
                  your Amazon Web Services account.</p> <p>You can optionally
                  specify the maximum number of items to receive in the
                  response. If the total number of items in the list exceeds the
                  maximum that you specify, or the default maximum, the response
                  is paginated. To get the next page of items, send a subsequent
                  request that specifies the <code>NextMarker</code> value from
                  the current response as the <code>Marker</code> value in the
                  subsequent request.</p>
                tags:
                  - Lists
                  - Cache
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
            /2020-05-31/origin-access-identity/cloudfront:
              GET:
                summary: ListCloudFrontOriginAccessIdentities
                description: <p>Lists origin access identities.</p>
                tags:
                  - Lists
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identities
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
            /2020-05-31/continuous-deployment-policy:
              GET:
                summary: ListContinuousDeploymentPolicies
                description: >-
                  <p>Gets a list of the continuous deployment policies in your
                  Amazon Web Services account.</p> <p>You can optionally specify
                  the maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Continuous
                  - Deployments
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
            /2020-05-31/distribution:
              GET:
                summary: ListDistributions
                description: <p>List CloudFront distributions.</p>
                tags:
                  - Lists
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
            /2020-05-31/distribution?WithTags:
              POST:
                summary: CreateDistributionWithTags
                description: >-
                  <p>Create a new distribution with tags. This API operation
                  requires the following IAM permissions:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html">CreateDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TagResource.html">TagResource</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Distributions
                  - With
                  - Tags
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
            /2020-05-31/field-level-encryption:
              GET:
                summary: ListFieldLevelEncryptionConfigs
                description: >-
                  <p>List all field-level encryption configurations that have
                  been created in CloudFront for this account.</p>
                tags:
                  - Lists
                  - Fields
                  - Levels
                  - Encryption
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
            /2020-05-31/field-level-encryption-profile:
              GET:
                summary: ListFieldLevelEncryptionProfiles
                description: >-
                  <p>Request a list of field-level encryption profiles that have
                  been created in CloudFront for this account.</p>
                tags:
                  - Lists
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
            /2020-05-31/function:
              GET:
                summary: ListFunctions
                description: >-
                  <p>Gets a list of all CloudFront functions in your Amazon Web
                  Services account.</p> <p>You can optionally apply a filter to
                  return only the functions that are in the specified stage,
                  either <code>DEVELOPMENT</code> or <code>LIVE</code>.</p>
                  <p>You can optionally specify the maximum number of items to
                  receive in the response. If the total number of items in the
                  list exceeds the maximum that you specify, or the default
                  maximum, the response is paginated. To get the next page of
                  items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
            /2020-05-31/distribution/{DistributionId}/invalidation:
              GET:
                summary: ListInvalidations
                description: <p>Lists invalidation batches.</p>
                tags:
                  - Lists
                  - Invalidations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
            /2020-05-31/key-group:
              GET:
                summary: ListKeyGroups
                description: >-
                  <p>Gets a list of key groups.</p> <p>You can optionally
                  specify the maximum number of items to receive in the
                  response. If the total number of items in the list exceeds the
                  maximum that you specify, or the default maximum, the response
                  is paginated. To get the next page of items, send a subsequent
                  request that specifies the <code>NextMarker</code> value from
                  the current response as the <code>Marker</code> value in the
                  subsequent request.</p>
                tags:
                  - Lists
                  - Keys
                  - Groups
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
            /2020-05-31/key-value-store/:
              POST:
                summary: CreateKeyValueStore
                description: >-
                  <p>Specifies the Key Value Store resource to add to your
                  account. In your account, the Key Value Store names must be
                  unique. You can also import Key Value Store data in JSON
                  format from an S3 bucket by providing a valid
                  <code>ImportSource</code> that you own.</p>
                tags:
                  - Create
                  - Keys
                  - Value
                  - Store
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
            /2020-05-31/distributions/{DistributionId}/monitoring-subscription/:
              GET:
                summary: GetMonitoringSubscription
                description: >-
                  <p>Gets information about whether additional CloudWatch
                  metrics are enabled for the specified CloudFront
                  distribution.</p>
                tags:
                  - Get
                  - Monitoring
                  - Subscriptions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
            /2020-05-31/origin-access-control:
              GET:
                summary: ListOriginAccessControls
                description: >-
                  <p>Gets the list of CloudFront origin access controls in this
                  Amazon Web Services account.</p> <p>You can optionally specify
                  the maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send another request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the next
                  request.</p>
                tags:
                  - Lists
                  - Origin
                  - Access
                  - Controls
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
            /2020-05-31/origin-request-policy:
              GET:
                summary: ListOriginRequestPolicies
                description: >-
                  <p>Gets a list of origin request policies.</p> <p>You can
                  optionally apply a filter to return only the managed policies
                  created by Amazon Web Services, or only the custom policies
                  created in your Amazon Web Services account.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Origin
                  - Request
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
            /2020-05-31/public-key:
              GET:
                summary: ListPublicKeys
                description: >-
                  <p>List all public keys that have been added to CloudFront for
                  this account.</p>
                tags:
                  - Lists
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
            /2020-05-31/realtime-log-config:
              GET:
                summary: ListRealtimeLogConfigs
                description: >-
                  <p>Gets a list of real-time log configurations.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
            /2020-05-31/response-headers-policy:
              GET:
                summary: ListResponseHeadersPolicies
                description: >-
                  <p>Gets a list of response headers policies.</p> <p>You can
                  optionally apply a filter to get only the managed policies
                  created by Amazon Web Services, or only the custom policies
                  created in your Amazon Web Services account.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Responses
                  - Headers
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
            /2020-05-31/streaming-distribution:
              GET:
                summary: ListStreamingDistributions
                description: <p>List streaming distributions.</p>
                tags:
                  - Lists
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/streaming-distribution?WithTags:
              POST:
                summary: CreateStreamingDistributionWithTags
                description: >-
                  <p>This API is deprecated. Amazon CloudFront is deprecating
                  real-time messaging protocol (RTMP) distributions on December
                  31, 2020. For more information, <a
                  href="http://forums.aws.amazon.com/ann.jspa?annID=7356">read
                  the announcement</a> on the Amazon CloudFront discussion
                  forum.</p>
                tags:
                  - Create
                  - Streaming
                  - Distributions
                  - With
                  - Tags
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/cache-policy/{Id}:
              PUT:
                summary: UpdateCachePolicy
                description: >-
                  <p>Updates a cache policy configuration.</p> <p>When you
                  update a cache policy configuration, all the fields are
                  updated with the values provided in the request. You cannot
                  update some fields independent of others. To update a cache
                  policy configuration:</p> <ol> <li> <p>Use
                  <code>GetCachePolicyConfig</code> to get the current
                  configuration.</p> </li> <li> <p>Locally modify the fields in
                  the cache policy configuration that you want to update.</p>
                  </li> <li> <p>Call <code>UpdateCachePolicy</code> by providing
                  the entire cache policy configuration, including the fields
                  that you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Cache
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/origin-access-identity/cloudfront/{Id}:
              GET:
                summary: GetCloudFrontOriginAccessIdentity
                description: <p>Get the information about an origin access identity.</p>
                tags:
                  - Get
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identity
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/continuous-deployment-policy/{Id}:
              PUT:
                summary: UpdateContinuousDeploymentPolicy
                description: >-
                  <p>Updates a continuous deployment policy. You can update a
                  continuous deployment policy to enable or disable it, to
                  change the percentage of traffic that it sends to the staging
                  distribution, or to change the staging distribution that it
                  sends traffic to.</p> <p>When you update a continuous
                  deployment policy configuration, all the fields are updated
                  with the values that are provided in the request. You cannot
                  update some fields independent of others. To update a
                  continuous deployment policy configuration:</p> <ol> <li>
                  <p>Use <code>GetContinuousDeploymentPolicyConfig</code> to get
                  the current configuration.</p> </li> <li> <p>Locally modify
                  the fields in the continuous deployment policy configuration
                  that you want to update.</p> </li> <li> <p>Use
                  <code>UpdateContinuousDeploymentPolicy</code>, providing the
                  entire continuous deployment policy configuration, including
                  the fields that you modified and those that you didn't.</p>
                  </li> </ol>
                tags:
                  - Update
                  - Continuous
                  - Deployments
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/distribution/{Id}:
              GET:
                summary: GetDistribution
                description: <p>Get the information about a distribution.</p>
                tags:
                  - Get
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/field-level-encryption/{Id}:
              GET:
                summary: GetFieldLevelEncryption
                description: >-
                  <p>Get the field-level encryption configuration
                  information.</p>
                tags:
                  - Get
                  - Fields
                  - Levels
                  - Encryption
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/field-level-encryption-profile/{Id}:
              GET:
                summary: GetFieldLevelEncryptionProfile
                description: <p>Get the field-level encryption profile information.</p>
                tags:
                  - Get
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
            /2020-05-31/function/{Name}:
              PUT:
                summary: UpdateFunction
                description: >-
                  <p>Updates a CloudFront function.</p> <p>You can update a
                  function's code or the comment that describes the function.
                  You cannot update a function's name.</p> <p>To update a
                  function, you provide the function's name and version
                  (<code>ETag</code> value) along with the updated function
                  code. To get the name and version, you can use
                  <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Update
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/key-group/{Id}:
              PUT:
                summary: UpdateKeyGroup
                description: >-
                  <p>Updates a key group.</p> <p>When you update a key group,
                  all the fields are updated with the values provided in the
                  request. You cannot update some fields independent of others.
                  To update a key group:</p> <ol> <li> <p>Get the current key
                  group with <code>GetKeyGroup</code> or
                  <code>GetKeyGroupConfig</code>.</p> </li> <li> <p>Locally
                  modify the fields in the key group that you want to update.
                  For example, add or remove public key IDs.</p> </li> <li>
                  <p>Call <code>UpdateKeyGroup</code> with the entire key group
                  object, including the fields that you modified and those that
                  you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Keys
                  - Group
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/key-value-store/{Name}:
              PUT:
                summary: UpdateKeyValueStore
                description: <p>Specifies the Key Value Store to update.</p>
                tags:
                  - Update
                  - Keys
                  - Value
                  - Store
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/origin-access-control/{Id}:
              GET:
                summary: GetOriginAccessControl
                description: >-
                  <p>Gets a CloudFront origin access control, including its
                  unique identifier.</p>
                tags:
                  - Get
                  - Origin
                  - Access
                  - Control
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/origin-request-policy/{Id}:
              PUT:
                summary: UpdateOriginRequestPolicy
                description: >-
                  <p>Updates an origin request policy configuration.</p> <p>When
                  you update an origin request policy configuration, all the
                  fields are updated with the values provided in the request.
                  You cannot update some fields independent of others. To update
                  an origin request policy configuration:</p> <ol> <li> <p>Use
                  <code>GetOriginRequestPolicyConfig</code> to get the current
                  configuration.</p> </li> <li> <p>Locally modify the fields in
                  the origin request policy configuration that you want to
                  update.</p> </li> <li> <p>Call
                  <code>UpdateOriginRequestPolicy</code> by providing the entire
                  origin request policy configuration, including the fields that
                  you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Origin
                  - Request
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/public-key/{Id}:
              GET:
                summary: GetPublicKey
                description: <p>Gets a public key.</p>
                tags:
                  - Get
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
            /2020-05-31/delete-realtime-log-config/:
              POST:
                summary: DeleteRealtimeLogConfig
                description: >-
                  <p>Deletes a real-time log configuration.</p> <p>You cannot
                  delete a real-time log configuration if it's attached to a
                  cache behavior. First update your distributions to remove the
                  real-time log configuration from all cache behaviors, then
                  delete the real-time log configuration.</p> <p>To delete a
                  real-time log configuration, you can provide the
                  configuration's name or its Amazon Resource Name (ARN). You
                  must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  delete.</p>
                tags:
                  - Delete
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/response-headers-policy/{Id}:
              PUT:
                summary: UpdateResponseHeadersPolicy
                description: >-
                  <p>Updates a response headers policy.</p> <p>When you update a
                  response headers policy, the entire policy is replaced. You
                  cannot update some policy fields independent of others. To
                  update a response headers policy configuration:</p> <ol> <li>
                  <p>Use <code>GetResponseHeadersPolicyConfig</code> to get the
                  current policy's configuration.</p> </li> <li> <p>Modify the
                  fields in the response headers policy configuration that you
                  want to update.</p> </li> <li> <p>Call
                  <code>UpdateResponseHeadersPolicy</code>, providing the entire
                  response headers policy configuration, including the fields
                  that you modified and those that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Responses
                  - Headers
                  - Policies
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/streaming-distribution/{Id}:
              GET:
                summary: GetStreamingDistribution
                description: >-
                  <p>Gets information about a specified RTMP distribution,
                  including the distribution configuration.</p>
                tags:
                  - Get
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
            /2020-05-31/function/{Name}/describe:
              GET:
                summary: DescribeFunction
                description: >-
                  <p>Gets configuration information and metadata about a
                  CloudFront function, but not the function's code. To get a
                  function's code, use <code>GetFunction</code>.</p> <p>To get
                  configuration information and metadata about a function, you
                  must provide the function's name and stage. To get these
                  values, you can use <code>ListFunctions</code>.</p>
                tags:
                  - Describe
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/cache-policy/{Id}/config:
              GET:
                summary: GetCachePolicyConfig
                description: >-
                  <p>Gets a cache policy configuration.</p> <p>To get a cache
                  policy configuration, you must provide the policy's
                  identifier. If the cache policy is attached to a
                  distribution's cache behavior, you can get the policy's
                  identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the cache policy is not
                  attached to a cache behavior, you can get the identifier using
                  <code>ListCachePolicies</code>.</p>
                tags:
                  - Get
                  - Cache
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-access-identity/cloudfront/{Id}/config:
              PUT:
                summary: UpdateCloudFrontOriginAccessIdentity
                description: <p>Update an origin access identity.</p>
                tags:
                  - Update
                  - Cloud
                  - Front
                  - Origin
                  - Access
                  - Identity
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/continuous-deployment-policy/{Id}/config:
              GET:
                summary: GetContinuousDeploymentPolicyConfig
                description: >-
                  <p>Gets configuration information about a continuous
                  deployment policy.</p>
                tags:
                  - Get
                  - Continuous
                  - Deployments
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/distribution/{Id}/config:
              PUT:
                summary: UpdateDistribution
                description: >-
                  <p>Updates the configuration for a CloudFront
                  distribution.</p> <p>The update process includes getting the
                  current distribution configuration, updating it to make your
                  changes, and then submitting an
                  <code>UpdateDistribution</code> request to make the
                  updates.</p> <p> <b>To update a web distribution using the
                  CloudFront API</b> </p> <ol> <li> <p>Use
                  <code>GetDistributionConfig</code> to get the current
                  configuration, including the version identifier
                  (<code>ETag</code>).</p> </li> <li> <p>Update the distribution
                  configuration that was returned in the response. Note the
                  following important requirements and restrictions:</p> <ul>
                  <li> <p>You must rename the <code>ETag</code> field to
                  <code>IfMatch</code>, leaving the value unchanged. (Set the
                  value of <code>IfMatch</code> to the value of
                  <code>ETag</code>, then remove the <code>ETag</code>
                  field.)</p> </li> <li> <p>You can't change the value of
                  <code>CallerReference</code>.</p> </li> </ul> </li> <li>
                  <p>Submit an <code>UpdateDistribution</code> request,
                  providing the distribution configuration. The new
                  configuration replaces the existing configuration. The values
                  that you specify in an <code>UpdateDistribution</code> request
                  are not merged into your existing configuration. Make sure to
                  include all fields: the ones that you modified and also the
                  ones that you didn't.</p> </li> </ol>
                tags:
                  - Update
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/field-level-encryption/{Id}/config:
              PUT:
                summary: UpdateFieldLevelEncryptionConfig
                description: <p>Update a field-level encryption configuration.</p>
                tags:
                  - Update
                  - Fields
                  - Levels
                  - Encryption
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/field-level-encryption-profile/{Id}/config:
              PUT:
                summary: UpdateFieldLevelEncryptionProfile
                description: <p>Update a field-level encryption profile.</p>
                tags:
                  - Update
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/distribution/{DistributionId}/invalidation/{Id}:
              GET:
                summary: GetInvalidation
                description: <p>Get the information about an invalidation.</p>
                tags:
                  - Get
                  - Invalidations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/key-group/{Id}/config:
              GET:
                summary: GetKeyGroupConfig
                description: >-
                  <p>Gets a key group configuration.</p> <p>To get a key group
                  configuration, you must provide the key group's identifier. If
                  the key group is referenced in a distribution's cache
                  behavior, you can get the key group's identifier using
                  <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the key group is not
                  referenced in a cache behavior, you can get the identifier
                  using <code>ListKeyGroups</code>.</p>
                tags:
                  - Get
                  - Keys
                  - Group
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-access-control/{Id}/config:
              PUT:
                summary: UpdateOriginAccessControl
                description: <p>Updates a CloudFront origin access control.</p>
                tags:
                  - Update
                  - Origin
                  - Access
                  - Control
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/origin-request-policy/{Id}/config:
              GET:
                summary: GetOriginRequestPolicyConfig
                description: >-
                  <p>Gets an origin request policy configuration.</p> <p>To get
                  an origin request policy configuration, you must provide the
                  policy's identifier. If the origin request policy is attached
                  to a distribution's cache behavior, you can get the policy's
                  identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the origin request policy is
                  not attached to a cache behavior, you can get the identifier
                  using <code>ListOriginRequestPolicies</code>.</p>
                tags:
                  - Get
                  - Origin
                  - Request
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/public-key/{Id}/config:
              PUT:
                summary: UpdatePublicKey
                description: >-
                  <p>Update public key information. Note that the only value you
                  can change is the comment.</p>
                tags:
                  - Update
                  - Public
                  - Keys
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
            /2020-05-31/get-realtime-log-config/:
              POST:
                summary: GetRealtimeLogConfig
                description: >-
                  <p>Gets a real-time log configuration.</p> <p>To get a
                  real-time log configuration, you can provide the
                  configuration's name or its Amazon Resource Name (ARN). You
                  must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  get.</p>
                tags:
                  - Get
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/response-headers-policy/{Id}/config:
              GET:
                summary: GetResponseHeadersPolicyConfig
                description: >-
                  <p>Gets a response headers policy configuration.</p> <p>To get
                  a response headers policy configuration, you must provide the
                  policy's identifier. If the response headers policy is
                  attached to a distribution's cache behavior, you can get the
                  policy's identifier using <code>ListDistributions</code> or
                  <code>GetDistribution</code>. If the response headers policy
                  is not attached to a cache behavior, you can get the
                  identifier using <code>ListResponseHeadersPolicies</code>.</p>
                tags:
                  - Get
                  - Responses
                  - Headers
                  - Policies
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/streaming-distribution/{Id}/config:
              PUT:
                summary: UpdateStreamingDistribution
                description: <p>Update a streaming distribution.</p>
                tags:
                  - Update
                  - Streaming
                  - Distributions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
            /2020-05-31/conflicting-alias:
              GET:
                summary: ListConflictingAliases
                description: >-
                  <p>Gets a list of aliases (also called CNAMEs or alternate
                  domain names) that conflict or overlap with the provided
                  alias, and the associated CloudFront distributions and Amazon
                  Web Services accounts for each conflicting alias. In the
                  returned list, the distribution and account IDs are partially
                  hidden, which allows you to identify the distributions and
                  accounts that you own, but helps to protect the information of
                  ones that you don't own.</p> <p>Use this operation to find
                  aliases that are in use in CloudFront that conflict or overlap
                  with the provided alias. For example, if you provide
                  <code>www.example.com</code> as input, the returned list can
                  include <code>www.example.com</code> and the overlapping
                  wildcard alternate domain name (<code>*.example.com</code>),
                  if they exist. If you provide <code>*.example.com</code> as
                  input, the returned list can include
                  <code>*.example.com</code> and any alternate domain names
                  covered by that wildcard (for example,
                  <code>www.example.com</code>, <code>test.example.com</code>,
                  <code>dev.example.com</code>, and so on), if they exist.</p>
                  <p>To list conflicting aliases, you provide the alias to
                  search and the ID of a distribution in your account that has
                  an attached SSL/TLS certificate that includes the provided
                  alias. For more information, including how to set up the
                  distribution and certificate, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/CNAMEs.html#alternate-domain-names-move">Moving
                  an alternate domain name to a different distribution</a> in
                  the <i>Amazon CloudFront Developer Guide</i>.</p> <p>You can
                  optionally specify the maximum number of items to receive in
                  the response. If the total number of items in the list exceeds
                  the maximum that you specify, or the default maximum, the
                  response is paginated. To get the next page of items, send a
                  subsequent request that specifies the <code>NextMarker</code>
                  value from the current response as the <code>Marker</code>
                  value in the subsequent request.</p>
                tags:
                  - Lists
                  - Conflicting
                  - Aliases
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
            /2020-05-31/distributionsByCachePolicyId/{CachePolicyId}:
              GET:
                summary: ListDistributionsByCachePolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified cache
                  policy.</p> <p>You can optionally specify the maximum number
                  of items to receive in the response. If the total number of
                  items in the list exceeds the maximum that you specify, or the
                  default maximum, the response is paginated. To get the next
                  page of items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Cache
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByKeyGroupId/{KeyGroupId}:
              GET:
                summary: ListDistributionsByKeyGroup
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that references the specified key group.</p>
                  <p>You can optionally specify the maximum number of items to
                  receive in the response. If the total number of items in the
                  list exceeds the maximum that you specify, or the default
                  maximum, the response is paginated. To get the next page of
                  items, send a subsequent request that specifies the
                  <code>NextMarker</code> value from the current response as the
                  <code>Marker</code> value in the subsequent request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Keys
                  - Group
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByOriginRequestPolicyId/{OriginRequestPolicyId}:
              GET:
                summary: ListDistributionsByOriginRequestPolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified origin
                  request policy.</p> <p>You can optionally specify the maximum
                  number of items to receive in the response. If the total
                  number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Origin
                  - Request
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByRealtimeLogConfig/:
              POST:
                summary: ListDistributionsByRealtimeLogConfig
                description: >-
                  <p>Gets a list of distributions that have a cache behavior
                  that's associated with the specified real-time log
                  configuration.</p> <p>You can specify the real-time log
                  configuration by its name or its Amazon Resource Name (ARN).
                  You must provide at least one. If you provide both, CloudFront
                  uses the name to identify the real-time log configuration to
                  list distributions for.</p> <p>You can optionally specify the
                  maximum number of items to receive in the response. If the
                  total number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByResponseHeadersPolicyId/{ResponseHeadersPolicyId}:
              GET:
                summary: ListDistributionsByResponseHeadersPolicyId
                description: >-
                  <p>Gets a list of distribution IDs for distributions that have
                  a cache behavior that's associated with the specified response
                  headers policy.</p> <p>You can optionally specify the maximum
                  number of items to receive in the response. If the total
                  number of items in the list exceeds the maximum that you
                  specify, or the default maximum, the response is paginated. To
                  get the next page of items, send a subsequent request that
                  specifies the <code>NextMarker</code> value from the current
                  response as the <code>Marker</code> value in the subsequent
                  request.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Responses
                  - Headers
                  - Policies
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
            /2020-05-31/distributionsByWebACLId/{WebACLId}:
              GET:
                summary: ListDistributionsByWebACLId
                description: >-
                  <p>List the distributions that are associated with a specified
                  WAF web ACL.</p>
                tags:
                  - Lists
                  - Distributions
                  - By
                  - Web
                  - Identifiers
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
            /2020-05-31/key-value-store:
              GET:
                summary: ListKeyValueStores
                description: <p>Specifies the Key Value Stores to list.</p>
                tags:
                  - Lists
                  - Keys
                  - Value
                  - Stores
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
            /2020-05-31/tagging:
              GET:
                summary: ListTagsForResource
                description: <p>List tags for a CloudFront resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
            /2020-05-31/function/{Name}/publish:
              POST:
                summary: PublishFunction
                description: >-
                  <p>Publishes a CloudFront function by copying the function
                  code from the <code>DEVELOPMENT</code> stage to
                  <code>LIVE</code>. This automatically updates all cache
                  behaviors that are using this function to use the newly
                  published copy in the <code>LIVE</code> stage.</p> <p>When a
                  function is published to the <code>LIVE</code> stage, you can
                  attach the function to a distribution's cache behavior, using
                  the function's Amazon Resource Name (ARN).</p> <p>To publish a
                  function, you must provide the function's name and version
                  (<code>ETag</code> value). To get these values, you can use
                  <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Publish
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
            /2020-05-31/tagging?Operation=Tag:
              POST:
                summary: TagResource
                description: <p>Add tags to a CloudFront resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
            /2020-05-31/function/{Name}/test:
              POST:
                summary: TestFunction
                description: >-
                  <p>Tests a CloudFront function.</p> <p>To test a function, you
                  provide an <i>event object</i> that represents an HTTP request
                  or response that your CloudFront distribution could receive in
                  production. CloudFront runs the function, passing it the event
                  object that you provided, and returns the function's result
                  (the modified event object) in the response. The response also
                  contains function logs and error messages, if any exist. For
                  more information about testing functions, see <a
                  href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/managing-functions.html#test-function">Testing
                  functions</a> in the <i>Amazon CloudFront Developer
                  Guide</i>.</p> <p>To test a function, you provide the
                  function's name and version (<code>ETag</code> value) along
                  with the event object. To get the function's name and version,
                  you can use <code>ListFunctions</code> and
                  <code>DescribeFunction</code>.</p>
                tags:
                  - Tests
                  - Functions
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
            /2020-05-31/tagging?Operation=Untag:
              POST:
                summary: UntagResource
                description: <p>Remove tags from a CloudFront resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
            /2020-05-31/distribution/{Id}/promote-staging-config:
              PUT:
                summary: UpdateDistributionWithStagingConfig
                description: >-
                  <p>Copies the staging distribution's configuration to its
                  corresponding primary distribution. The primary distribution
                  retains its <code>Aliases</code> (also known as alternate
                  domain names or CNAMEs) and
                  <code>ContinuousDeploymentPolicyId</code> value, but otherwise
                  its configuration is overwritten to match the staging
                  distribution.</p> <p>You can use this operation in a
                  continuous deployment workflow after you have tested
                  configuration changes on the staging distribution. After using
                  a continuous deployment policy to move a portion of your
                  domain name's traffic to the staging distribution and
                  verifying that it works as intended, you can use this
                  operation to copy the staging distribution's configuration to
                  the primary distribution. This action will disable the
                  continuous deployment policy and move your domain's traffic
                  back to the primary distribution.</p> <p>This API operation
                  requires the following IAM permissions:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GetDistribution.html">GetDistribution</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_UpdateDistribution.html">UpdateDistribution</a>
                  </p> </li> </ul>
                tags:
                  - Update
                  - Distributions
                  - With
                  - Staging
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
                  - Promote
                  - Staging
            /2020-05-31/realtime-log-config/:
              PUT:
                summary: UpdateRealtimeLogConfig
                description: >-
                  <p>Updates a real-time log configuration.</p> <p>When you
                  update a real-time log configuration, all the parameters are
                  updated with the values provided in the request. You cannot
                  update some parameters independent of others. To update a
                  real-time log configuration:</p> <ol> <li> <p>Call
                  <code>GetRealtimeLogConfig</code> to get the current real-time
                  log configuration.</p> </li> <li> <p>Locally modify the
                  parameters in the real-time log configuration that you want to
                  update.</p> </li> <li> <p>Call this API
                  (<code>UpdateRealtimeLogConfig</code>) by providing the entire
                  real-time log configuration, including the parameters that you
                  modified and those that you didn't.</p> </li> </ol> <p>You
                  cannot update a real-time log configuration's
                  <code>Name</code> or <code>ARN</
                tags:
                  - Update
                  - Real Time
                  - Logs
                  - Configurations
                  - Target
                  - Distributions
                  - Identifiers
                  - Associate
                  - Alias
                  - Primary
                  - Copy
                  - '2020'
                  - '05'
                  - '31'
                  - Cache
                  - Policies
                  - Origin
                  - Access
                  - Identity
                  - Cloudfront
                  - Continuous
                  - Deployments
                  - With
                  - Tags
                  - Fields
                  - Levels
                  - Encryption
                  - Profiles
                  - Functions
                  - Invalidations
                  - Keys
                  - Group
                  - Value
                  - Store
                  - Monitoring
                  - Subscriptions
                  - Control
                  - Request
                  - Public
                  - Real Time
                  - Logs
                  - Configurations
                  - Responses
                  - Headers
                  - Streaming
                  - Names
                  - Delete
                  - Describe
                  - Get
                  - Conflicting
                  - By
                  - Web
                  - Tagging
                  - Publish
                  - Operations
                  - Tags
                  - Tests
                  - Untag
                  - Promote
                  - Staging
    overlays:
      - type: APIs.io Search
        url: overlays/cloudfront-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudfront-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudfront
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---