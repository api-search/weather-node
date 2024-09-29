---
name: Acting
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/acting.png
url: https://example.com/apis/acting.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Acting
apis:
  - name: Symphony Agent API
    description: >-
      The Symphony Agent is responsible for encryption and decryption of
      messages and content sent to and from a bot.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/overview-of-rest-api/agent-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.developers.symphony.com/bots/overview-of-rest-api/agent-api
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Agent API
          paths:
            /v3/health:
              get:
                tags:
                  - Checks
                  - Health
                  - Status
                  - V3
                  - Health
                summary: Checks health status
                description: >
                  _Available on Agent 2.57.0 and above._


                  Returns the connectivity status of your Agent server. If your
                  Agent server is started and running, the status value will be
                  `UP`
            /v3/health/extended:
              get:
                tags:
                  - Checks
                  - Health
                  - Status
                  - Of
                  - Services
                  - And
                  - Users
                  - V3
                  - Health
                  - Extended
                summary: Checks health status of services and users
                description: >
                  _Available on Agent 2.57.0 and above._


                  Returns the connectivity status of the Agent services
                  (**pod**, **key manager** and **datafeed**) as well as users

                  connectivity (**agentservice** and **ceservice**).


                  The global status will be set to `DOWN` if at least one of the
                  sub-status is also `DOWN`.
            /v4/message/import:
              post:
                tags:
                  - Import
                  - Messages
                  - From
                  - Other
                  - Systems
                  - Into
                  - Symphony.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                summary: Import messages from other systems into Symphony.
                description: >
                  Sends a message to be imported into the system.

                  Allows you to override the timestamp and author of the message
                  with your desired values.

                  The requesting user must have the Content Management role.

                  The user that the message is intended to have come from must
                  also be present in the conversation.

                  The intended message timestamp must be a valid time from the
                  past. It cannot be a future timestamp.

                  Optionally the original message ID can be specified to
                  identify the imported message for the purpose of repeat
                  imports.
            /v4/message/blast:
              post:
                tags:
                  - Post
                  - Message
                  - To
                  - Multiple
                  - Existing
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                summary: Post a message to multiple existing streams.
                description: >
                  Post a new message to the given list of streams. The stream
                  can be a chatroom,

                  an IM or a multiparty IM.


                  You may include an attachment on the message.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  If the message is in MessageML and fails schema validation a
                  client error results


                  This endpoint is idempotent, it means that a 200 response will
                  be returned even if the message has not been

                  delivered to some streams. Check the `errors` map from the
                  response in order to see on which stream(s) the

                  message has not been delivered.


                  The maximum number of streams where the message can be sent is
                  limitted to 100.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.
            /v1/message/{id}:
              get:
                tags:
                  - Get
                  - Message
                  - By
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                summary: Get a message by ID
            /v1/message/search:
              get:
                tags:
                  - Search
                  - Messages
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                summary: Search messages
                description: >
                  Search messages according to the specified criteria. The
                  "query" parameter takes a search query defined as

                  "field:value" pairs combined by the operator "AND" (e.g.
                  "text:foo AND autor:bar"). Supported fields are
                   (case-insensitive): "text", "author", "hashtag", "cashtag", "mention", "signal", "fromDate", "toDate",
                   "streamId", "streamType".
                   "text" search requires a "streamId" to be specified.
                   "streamType" accepts one of the following values: "chat" (IMs and MIMs), "im", "mim", "chatroom", "post".
                   "signal" queries can only be combined with "fromDate", "toDate", "skip" and "limit" parameters.
              post:
                tags:
                  - Search
                  - Messages
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                summary: Search messages
                description: Search messages according to the specified criteria.
            /v1/stream/{sid}/attachment:
              get:
                tags:
                  - Download
                  - An
                  - Attachment.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                summary: Download an attachment.
                description: >-
                  Downloads the attachment body by the attachment ID, stream ID,
                  and message ID.
            /v4/stream/{sid}/message:
              get:
                tags:
                  - Get
                  - Messages
                  - From
                  - An
                  - Existing
                  - Stream.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                summary: Get messages from an existing stream.
                description: >
                  A caller can fetch all unseen messages by passing the
                  timestamp of

                  the last message seen as the since parameter and the number of
                  messages

                  with the same timestamp value already seen as the skip
                  parameter. This

                  means that every message will be seen exactly once even in the
                  case that

                  an additional message is processed with the same timestamp as
                  the last

                  message returned by the previous call, and the case where
                  there are

                  more than maxMessages with the same timestamp value.


                  This method is intended for historic queries and is generally
                  reliable

                  but if guaranteed delivery of every message in real time is
                  required

                  then the equivilent firehose method should be called.
            /v4/stream/{sid}/message/create:
              post:
                tags:
                  - Post
                  - Message
                  - To
                  - One
                  - Existing
                  - Stream.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                summary: Post a message to one existing stream.
                description: >
                  Post a new message to the given stream. The stream can be a
                  chatroom,,an IM or a multiparty IM.


                  You may include an attachment on the message.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  If the message is in MessageML and fails schema validation a
                  client error will be returned.


                  If the message is sent then 200 is returned.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.
            /v4/stream/{sid}/message/{mid}/update:
              post:
                tags:
                  - Update
                  - An
                  - Existing
                  - Message.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                summary: Update an existing message.
                description: >
                  Update an existing message. The existing message must be a
                  valid social message, that has not been deleted.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.


                  Starting with SBE v24.1, attachments are supported.
            /v3/stream/{sid}/share:
              post:
                tags:
                  - Share
                  - Piece
                  - Of
                  - Content
                  - Into
                  - Symphony
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                summary: PROVISIONAL -  Share a piece of content into Symphony
                description: >
                  Given a 3rd party content (eg. news article), it can share to
                  the given stream.

                  The stream can be a chatroom, an IM or a multiparty IM.
            /v1/util/echo:
              post:
                tags:
                  - Test
                  - Endpoint,
                  - Returns
                  - Input.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                summary: Test endpoint, returns input.
            /v1/signals/list:
              get:
                tags:
                  - List
                  - Signals
                  - For
                  - The
                  - Requesting
                  - User.
                  - This
                  - Includes
                  - That
                  - User
                  - Has
                  - Created
                  - And
                  - Public
                  - |-
                    Signals
                    to
                  - Which
                  - They
                  - |
                    Subscribed.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                summary: >
                  List signals for the requesting user. This includes signals
                  that the user has created and public signals

                  to which they subscribed.
            /v1/signals/{id}/get:
              get:
                tags:
                  - Get
                  - Details
                  - Of
                  - The
                  - Requested
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Get details of the requested signal.
            /v1/signals/create:
              post:
                tags:
                  - Create
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Create a signal.
            /v1/signals/{id}/update:
              post:
                tags:
                  - Update
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Update a signal.
            /v1/signals/{id}/delete:
              post:
                tags:
                  - Delete
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                summary: Delete a signal.
            /v1/signals/{id}/subscribe:
              post:
                tags:
                  - Subscribe
                  - To
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                summary: Subscribe to a Signal.
            /v1/signals/{id}/unsubscribe:
              post:
                tags:
                  - Unsubscribe
                  - To
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                summary: Unsubscribe to a Signal.
            /v1/signals/{id}/subscribers:
              get:
                tags:
                  - Get
                  - The
                  - Subscribers
                  - Of
                  - Signal
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                summary: Get the subscribers of a signal
            /v1/info:
              get:
                tags:
                  - Get
                  - Information
                  - About
                  - The
                  - Agent
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                summary: Get information about the Agent
            /v1/dlp/policies:
              get:
                tags:
                  - Get
                  - All
                  - Policies
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Get all policies
                description: Get all policies
              post:
                tags:
                  - Creates
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Creates a policy
                description: >
                  Creates a new policy with dictionary references.


                  At the time of policy creation, the caller should only provide
                  - contentTypes, name, scopes and type. The rest of the
                  information is populated automatically.


                  Note - You need to enable the policy after creation to start
                  enforcing the policy.
            /v1/dlp/policies/{policyId}:
              get:
                tags:
                  - Get
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Get a policy
                description: Get a policy
              put:
                tags:
                  - Updates
                  - Policy.
                  - Cannot
                  - Be
                  - Used
                  - For
                  - Creation.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Updates a policy. Cannot be used for creation.
                description: >
                  Update the policy (name, type, contentTypes, scopes) and also
                  the dictionaries for a policy.

                  Warning: If you send empty list of dictionaries during the
                  update operation, then all the

                  dictionaries for this policy are deleted and policy is
                  automatically disabled.

                  Note: The policy should already exist.
              delete:
                tags:
                  - Delete
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Delete a policy
                description: |
                  Delete a policy.
                  Note: Only disabled policy can be deleted
            /v1/dlp/policies/{policyId}/enable:
              post:
                tags:
                  - Enables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                summary: Enables a policy.
                description: Enables a policy.
            /v1/dlp/policies/{policyId}/disable:
              post:
                tags:
                  - Disables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                summary: Disables a policy.
                description: Disables a policy.
            /v1/dlp/dictionaries:
              get:
                tags:
                  - Get
                  - All
                  - Dictionary
                  - Metadatas
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Get all dictionary metadatas
                description: >
                  Get all dictionary metadatas with the latest version. Each
                  dictionary object will only contain meta data of the content.
              post:
                tags:
                  - Create
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Create a dictionary
                description: >
                  Creates a dictionary with basic metadata and no content. Only
                  "name" and "type" field is used to create a new dictionary
                  entry.
            /v1/dlp/dictionaries/{dictId}:
              get:
                tags:
                  - Get
                  - Dictionary
                  - Metadata
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Get dictionary metadata
                description: Get basic information for a dictionary.
              put:
                tags:
                  - Updates
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Updates a dictionary
                description: |
                  Updates the dictionary's basic metadata without content.
                  This API cannot be used for creating a new dictionary.
                  In case of update only "name" can be changed.
                  Note: All related policies will also have versions updated.
              delete:
                tags:
                  - Delete
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Delete a dictionary
                description: |
                  Deletes a dictionary.
                  Note: All related policies will be affected.
            /v1/dlp/dictionaries/{dictId}/data/download:
              get:
                tags:
                  - Downloads
                  - Base
                  - '64'
                  - Encoded
                  - Dictionary
                  - Content.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                summary: Downloads Base 64 encoded dictionary content.
                description: Downloads Base 64 encoded dictionary content.
            /v1/dlp/dictionaries/{dictId}/data/upload:
              post:
                tags:
                  - Override
                  - Dictionary
                  - Content
                  - With
                  - Provided
                  - Content.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                summary: Override dictionary content with provided content.
                description: Override dictionary content with provided content.
            /v1/dlp/violations/message:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Messages.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                summary: Get violations as a result of policy enforcement on messages.
            /v1/dlp/violations/stream:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                summary: Get violations as a result of policy enforcement on streams.
            /v1/dlp/violations/signal:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Signals.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on signals.
            /v3/dlp/policies:
              get:
                tags:
                  - Get
                  - All
                  - Policies
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get all policies
                description: Get all policies
              post:
                tags:
                  - Creates
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Creates a policy
                description: >
                  Creates a new policy with dictionary references.

                  At the time of policy creation, the caller should only provide
                  - contentTypes, name, scopes and type.

                  The rest of the information is populated automatically.

                  Note - You need to enable the policy after creation to start
                  enforcing the policy.
            /v3/dlp/policies/{policyId}:
              get:
                tags:
                  - Get
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get a policy
                description: Get a policy
            /v3/dlp/policies/{policyId}/update:
              post:
                tags:
                  - Updates
                  - Policy.
                  - Cannot
                  - Be
                  - Used
                  - For
                  - Creation.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Updates a policy. Cannot be used for creation.
                description: >
                  Update the policy (name, type, contentTypes, scopes) and also
                  the dictionaries for a policy.

                  Warning: If you send empty list of dictionaries during the
                  update operation, then all the

                  dictionaries for this policy are deleted and policy is
                  automatically disabled.

                  Note: The policy should already exist.
            /v3/dlp/policies/{policyId}/delete:
              post:
                tags:
                  - Delete
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Delete a policy
                description: |
                  Delete a policy.
                  Note: Only disabled policy can be deleted
            /v3/dlp/policies/{policyId}/enable:
              post:
                tags:
                  - Enables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Enables a policy.
                description: Enables a policy.
            /v3/dlp/policies/{policyId}/disable:
              post:
                tags:
                  - Disables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Disables a policy.
                description: Disables a policy.
            /v3/dlp/violations/message:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Messages.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on messages.
                description: >-
                  Retrieves DLP v3 message related violations for a given time
                  range
            /v3/dlp/violations/stream:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on streams.
                description: >-
                  Retrieves DLP v3 signal related violations for a given time
                  range
            /v3/dlp/violations/signal:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Signals.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on signals.
                description: >-
                  Retrieves DLP v3 signal related violations for a given time
                  range
            /v3/dlp/violation/attachment:
              get:
                tags:
                  - Get
                  - Attachments
                  - That
                  - Were
                  - Sent
                  - As
                  - Part
                  - Of
                  - Messages
                  - Flagged
                  - By
                  - The
                  - System.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                summary: >-
                  Get attachments that were sent as part of messages that were
                  flagged by the DLP System.
                description: >-
                  Retrieves attachments from related message violations as a
                  base64 encoded String.
            /v1/audittrail/privilegeduser:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Actions
                  - Performed
                  - By
                  - Privileged
                  - Account
                  - Acting
                  - As
                  - User
                  - Given
                  - Period
                  - Time.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                summary: >-
                  Get a list of  actions performed by a privileged account
                  acting as privileged user given a period of time.
                description: >-
                  Get a list of actions performed by a privileged account acting
                  as privileged user given a period of time.
            /v5/datafeeds:
              get:
                tags:
                  - Read
                  - List
                  - Of
                  - Real
                  - Time
                  - Messages
                  - Events
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: Read list of real time messages / events stream ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the [Real Time Events](./docs/real-time-events.md)
                  list.


                  Returns the list of the datafeeds for the user.

                  Any datafeed ID of the list can then be used as input to the
                  Read Messages/Events Stream v4 endpoint.
              post:
                tags:
                  - Create
                  - New
                  - Real
                  - Time
                  - Messages
                  - Events
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: Create a new real time messages / events stream ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Returns the ID of the datafeed that has just been created.

                  This ID should then be used as input to the Read
                  Messages/Events Stream v4 endpoint.
            /v5/datafeeds/{datafeedId}:
              delete:
                tags:
                  - Delete
                  - The
                  - Specified
                  - Real
                  - Time
                  - Message
                  - Event
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: >-
                  Delete the specified real time message / event stream
                  ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Delete the specified datafeed.
            /v5/datafeeds/{datafeedId}/read:
              post:
                tags:
                  - Read
                  - The
                  - Specified
                  - Real
                  - Time
                  - Message
                  - Event
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                  - Read
                summary: >-
                  Read the specified real time message / event stream
                  ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Read the specified datafeed.


                  The ackId sent as parameter can be empty for the first call.
                  In the response an ackId will be sent back and it can be used
                  for

                  the next call: in this way you acknowledge that you have
                  received the events that came with that ackId; datafeed will
                  remove the events

                  associated with that ackId from your queue
            /v5/events/read:
              post:
                tags:
                  - Read
                  - Real
                  - Time
                  - Events
                  - From
                  - An
                  - Event
                  - Stream
                  - (aka
                  - Datafeed)
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                  - Read
                  - Events
                summary: Read Real Time Events from an event stream (aka datafeed)
                description: >
                  _Available on Agent 22.5.1 and above.This endpoint provides

                  messages and events from all conversations that the user is in
                  or events

                  from the whole pod depending on the "type" field value.

                  When "type":"fanout" is provided in the body, then only events
                  from streams 

                  the accountbelongs to are returned. Otherwise, if "type":
                  "datahose" is provided

                  in the body, then events returned are not limited to the
                  streams user

                  belongs to. In this case, at least one event type must be
                  provided in the

                  "filters" field. In case you are using a datahose feed and
                  retrieving

                  SOCIALMESSAGE events, ceservice account must be properly
                  configured in

                  the Agent.The types of events returned can be found in the
                  Real Time

                  Events list (see definition on top of the file). The ackId
                  sent as parameter

                  can be empty for the first call. In the response an ackId will
                  be sent back

                  and it can be used for the next call: in this way you
                  acknowledge that

                  you have received the events that came with that ackId.

                  If you have several instances of the same bot, they must share
                  the same feed so 

                  that events are spread across all bot instances. To do so, you
                  must: share the same 

                  service account provide the same "tag" and same "filte
    aid: symphony:symphony-agent-api
    overlays:
      - type: APIs.io Search
        url: overlays/agent-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---