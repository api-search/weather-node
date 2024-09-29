---
name: Cognito
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cognito.png
url: https://example.com/apis/cognito.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cognito
apis:
  - name: cognito-sync
    description: >-
      <fullname>Amazon Cognito Sync</fullname> <p>Amazon Cognito Sync provides
      an AWS service and client library that enable cross-device syncing of
      application-related user data. High-level client libraries are available
      for both iOS and Android. You can use these libraries to persist data
      locally so that it's available even if the device is offline. Developer
      credentials don't need to be stored on the mobile device to access the
      service. You can use Amazon Cognito to obtain a normalized user ID and
      credentials. User data is persisted in a dataset that can store up to 1 MB
      of key-value pairs, and you can have up to 20 datasets per user
      identity.</p> <p>With Amazon Cognito Sync, the data stored for each
      identity is accessible only to credentials assigned to that identity. In
      order to use the Cognito Sync service, you need to make API calls using
      credentials retrieved with <a
      href="http://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html">Amazon
      Cognito Identity service</a>.</p> <p>If you want to use Cognito Sync in an
      Android or iOS application, you will probably want to make API calls via
      the AWS Mobile SDK. To learn more, see the <a
      href="http://docs.aws.amazon.com/mobile/sdkforandroid/developerguide/cognito-sync.html">Developer
      Guide for Android</a> and the <a
      href="http://docs.aws.amazon.com/mobile/sdkforios/developerguide/cognito-sync.html">Developer
      Guide for iOS</a>.</p>
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
            title: cognito-sync
          paths:
            /identitypools/{IdentityPoolId}/bulkpublish:
              POST:
                summary: BulkPublish
                description: >-
                  <p>Initiates a bulk publish of all existing datasets for an
                  Identity Pool to the configured stream. Customers are limited
                  to one successful bulk publish per 24 hours. Bulk publish is
                  an asynchronous request, customers can see the status of the
                  request via the GetBulkPublishDetails operation.</p><p>This
                  API can only be called with developer credentials. You cannot
                  call this API with the temporary user credentials provided by
                  Cognito Identity.</p>
                tags:
                  - Bulk
                  - Publish
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
            /identitypools/{IdentityPoolId}/identities/{IdentityId}/datasets/{DatasetName}:
              POST:
                summary: UpdateRecords
                description: >-
                  <p>Posts updates to records and adds and deletes records for a
                  dataset and user.</p> <p>The sync count in the record patch is
                  your last known sync count for that record. The server will
                  reject an UpdateRecords request with a
                  ResourceConflictException if you try to patch a record with a
                  new value but a stale sync count.</p><p>For example, if the
                  sync count on the server is 5 for a key called highScore and
                  you try and submit a new highScore with sync count of 4, the
                  request will be rejected. To obtain the current sync count for
                  a record, call ListRecords. On a successful update of the
                  record, the response returns the new sync count for that
                  record. You should present that sync count the next time you
                  try to update that same record. When the record does not
                  exist, specify the sync count as 0.</p> <p>This API can be
                  called with temporary user credentials provided by Cognito
                  Identity or with developer credentials.</p>
                tags:
                  - Update
                  - Records
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
            /identitypools/{IdentityPoolId}:
              GET:
                summary: DescribeIdentityPoolUsage
                description: >-
                  <p>Gets usage details (for example, data storage) about a
                  particular identity pool.</p> <p>This API can only be called
                  with developer credentials. You cannot call this API with the
                  temporary user credentials provided by Cognito Identity.</p>
                tags:
                  - Describe
                  - Identity
                  - Pools
                  - Usage
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
            /identitypools/{IdentityPoolId}/identities/{IdentityId}:
              GET:
                summary: DescribeIdentityUsage
                description: >-
                  <p>Gets usage information for an identity, including number of
                  datasets and data usage.</p> <p>This API can be called with
                  temporary user credentials provided by Cognito Identity or
                  with developer credentials.</p>
                tags:
                  - Describe
                  - Identity
                  - Usage
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
            /identitypools/{IdentityPoolId}/getBulkPublishDetails:
              POST:
                summary: GetBulkPublishDetails
                description: >-
                  <p>Get the status of the last BulkPublish operation for an
                  identity pool.</p><p>This API can only be called with
                  developer credentials. You cannot call this API with the
                  temporary user credentials provided by Cognito Identity.</p>
                tags:
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
            /identitypools/{IdentityPoolId}/events:
              POST:
                summary: SetCognitoEvents
                description: >-
                  <p>Sets the AWS Lambda function for a given event type for an
                  identity pool. This request only updates the key/value pair
                  specified. Other key/values pairs are not updated. To remove a
                  key value pair, pass a empty value for the particular
                  key.</p><p>This API can only be called with developer
                  credentials. You cannot call this API with the temporary user
                  credentials provided by Cognito Identity.</p>
                tags:
                  - Sets
                  - Cognito
                  - Events
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
            /identitypools/{IdentityPoolId}/configuration:
              POST:
                summary: SetIdentityPoolConfiguration
                description: >-
                  <p>Sets the necessary configuration for push sync.</p><p>This
                  API can only be called with developer credentials. You cannot
                  call this API with the temporary user credentials provided by
                  Cognito Identity.</p>
                tags:
                  - Sets
                  - Identity
                  - Pools
                  - Configurations
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
            /identitypools/{IdentityPoolId}/identities/{IdentityId}/datasets:
              GET:
                summary: ListDatasets
                description: >-
                  <p>Lists datasets for an identity. With Amazon Cognito Sync,
                  each identity has access only to its own data. Thus, the
                  credentials used to make this API call need to have access to
                  the identity data.</p> <p>ListDatasets can be called with
                  temporary user credentials provided by Cognito Identity or
                  with developer credentials. You should use the Cognito
                  Identity credentials to make this API call.</p>
                tags:
                  - Lists
                  - Datasets
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
            /identitypools:
              GET:
                summary: ListIdentityPoolUsage
                description: >-
                  <p>Gets a list of identity pools registered with Cognito.</p>
                  <p>ListIdentityPoolUsage can only be called with developer
                  credentials. You cannot make this API call with the temporary
                  user credentials provided by Cognito Identity.</p>
                tags:
                  - Lists
                  - Identity
                  - Pools
                  - Usage
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
                  - Identity Pools
            /identitypools/{IdentityPoolId}/identities/{IdentityId}/datasets/{DatasetName}/records:
              GET:
                summary: ListRecords
                description: >-
                  <p>Gets paginated records, optionally changed after a
                  particular sync count for a dataset and identity. With Amazon
                  Cognito Sync, each identity has access only to its own data.
                  Thus, the credentials used to make this API call need to have
                  access to the identity data.</p> <p>ListRecords can be called
                  with temporary user credentials provided by Cognito Identity
                  or with developer credentials. You should use Cognito Identity
                  credentials to make this API call.</p>
                tags:
                  - Lists
                  - Records
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
                  - Identity Pools
                  - Records
            /identitypools/{IdentityPoolId}/identity/{IdentityId}/device:
              POST:
                summary: RegisterDevice
                description: >-
                  <p>Registers a device to receive push sync
                  notifications.</p><p>This API can only be called with
                  temporary credentials provided by Cognito Identity. You cannot
                  call this API with developer credentials.</p>
                tags:
                  - Register
                  - Device
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
                  - Identity Pools
                  - Records
                  - Device
            /identitypools/{IdentityPoolId}/identities/{IdentityId}/datasets/{DatasetName}/subscriptions/{DeviceId}:
              DELETE:
                summary: UnsubscribeFromDataset
                description: >-
                  <p>Unsubscribes from receiving notifications when a dataset is
                  modified by another device.</p><p>This API can only be called
                  with temporary credentials provided by Cognito Identity. You
                  cannot call this API with developer creden
                tags:
                  - Unsubscribe
                  - From
                  - Datasets
                  - Identity
                  - Pools
                  - Identifiers
                  - Bulk Publish
                  - Identities
                  - Datasets
                  - Datasets
                  - Names
                  - Get
                  - Bulk
                  - Publish
                  - Details
                  - Events
                  - Configurations
                  - Identity Pools
                  - Records
                  - Device
                  - Subscriptions
    overlays:
      - type: APIs.io Search
        url: overlays/cognito-sync-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cognito-sync-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cognito-sync
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---