---
name: Containt
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/containt.png
url: https://example.com/apis/containt.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Containt
apis:
  - name: Symphony Pod API
    description: >-
      The Symphony Pod API is used to build tools in order to manage and
      administer Symphony for your organization. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Pod API
          host: yourpodURL.symphony.com
          basePath: /pod
          paths:
            /v1/companycert/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
            /v2/companycert/create:
              post:
                summary: >-
                  Create a company trusted or untrusted certificate. Different
                  from V1 in that we reject expired certificates.
                tags:
                  - Create
                  - Company
                  - Trusted
                  - Or
                  - Untrusted
                  - Certificate.
                  - Different
                  - From
                  - V1
                  - In
                  - That
                  - We
                  - Reject
                  - Expired
                  - Certificates.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
            /v1/companycert/delete:
              post:
                summary: Delete a company certificate
                tags:
                  - Delete
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
            /v1/companycert/{fingerPrint}/get:
              get:
                summary: Get the details of a company certificate
                tags:
                  - Get
                  - The
                  - Details
                  - Of
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
            /v1/companycert/{fingerPrint}/update:
              post:
                summary: Update a company certificate
                tags:
                  - Update
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
            /v1/companycert/{fingerPrint}/issuedBy:
              get:
                summary: >
                  Return a list of all certificates which were verified to the
                  cert whose

                  fingerprint is passed.
                tags:
                  - Return
                  - List
                  - Of
                  - All
                  - Certificates
                  - Which
                  - Were
                  - Verified
                  - To
                  - The
                  - Cert
                  - |-
                    Whose
                    fingerprint
                  - Is
                  - |
                    Passed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
            /v1/companycert/podmanaged/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
            /v1/companycert/type/list:
              post:
                summary: List all certs of the given types
                tags:
                  - List
                  - All
                  - Certs
                  - Of
                  - The
                  - Given
                  - Types
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
            /v1/podcert:
              get:
                summary: >
                  Retrieve the pod certificate that can be use to validate
                  signed JWT tokens generated from the pod
                tags:
                  - Retrieve
                  - The
                  - Pod
                  - Certificate
                  - That
                  - Can
                  - Be
                  - Use
                  - To
                  - Validate
                  - Signed
                  - Tokens
                  - Generated
                  - From
                  - |
                    Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
            /v1/connection/list:
              get:
                summary: List of requesting user's connection
                description: >
                  This retrieves all connections of the requesting user. (i.e.
                  both connections in which the requesting user is the sender
                  and those

                  in which the requesting user is the inivtee) By default, if
                  you haven't specified the connection status to filter on, this
                  call will only

                  return results for both "pending_incoming" and
                  "pending_outgoing". You can optionally filter by userIds to
                  further restrict the results of

                  a specific connection status. If the users are in the same
                  private pod, the users have an implicit connection status of
                  "accepted". Those

                  users will not be returned in the response if you don't
                  specify the connection status as "accepted" (default is
                  "pending")

                  and the explicit userIds in the request.
                tags:
                  - List
                  - Of
                  - Requesting
                  - User's
                  - Connection
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/create:
              post:
                summary: Sends an invitation to connect with another user
                tags:
                  - Sends
                  - An
                  - Invitation
                  - To
                  - Connect
                  - With
                  - Another
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/accept:
              post:
                summary: Accept the connection request for the requesting user
                tags:
                  - Accept
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
            /v1/connection/reject:
              post:
                summary: Reject the connection request for the requesting user.
                description: >
                  Reject the connection between the requesting user and request
                  sender. If both users are in the same private pod,

                  an error will be returned because both users have an implicit
                  connection which cannot be rejected.
                tags:
                  - Reject
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
            /v1/connection/user/{userId}/info:
              get:
                summary: The status of the connection invitation to another user.
                tags:
                  - The
                  - Status
                  - Of
                  - Connection
                  - Invitation
                  - To
                  - Another
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
            /v1/connection/user/{uid}/remove:
              post:
                summary: Removes a connection with a user.
                tags:
                  - Removes
                  - Connection
                  - With
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
            /v1/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation between the caller and specified users.
                description: >
                  At least one user ID must be provided or

                  an error response will be sent.


                  The caller is implicitly included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.


                  This method was incorrectly specified to take a query
                  parameter in

                  version 1.0 of this specification but now expects a JSON array
                  of

                  user IDs in the body of the request.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - Between
                  - The
                  - Caller
                  - And
                  - Specified
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/update:
              post:
                summary: Update the attributes of an existing IM.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/info:
              get:
                summary: Get information about a partcular IM.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/presence/feed/create:
              post:
                summary: Create Presence status feed.
                description: >
                  Create a new stream capturing presence status changes
                  ("presence feed").

                  When read from, the feed will return the current presence
                  status of company (pod) users

                  if it has changed since the last read.


                  Returns the ID of the presence feed to be used in subsequent
                  read operations.
                tags:
                  - Create
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
            /v1/presence/feed/{feedId}/read:
              get:
                summary: Read a presence status feed.
                description: >
                  Returns the current presence status of company (pod) users

                  if it has changed since the last read. Returns up to 500
                  records at a time.
                tags:
                  - Read
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v1/presence/feed/{feedId}/delete:
              post:
                summary: Delete a presence status feed.
                description: |
                  Returns the ID of the deleted feed.
                tags:
                  - Delete
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v3/room/create:
              post:
                summary: Create a new chatroom.
                description: >
                  Create a new chatroom.


                  If no  attributes are specified, the room is created as a
                  private chatroom.
                tags:
                  - Create
                  - New
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
            /v3/room/search:
              post:
                summary: Search rooms according to the specified criteria.
                tags:
                  - Search
                  - Rooms
                  - According
                  - To
                  - The
                  - Specified
                  - Criteria.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v3/room/{id}/info:
              get:
                summary: Get information about a partcular chatroom.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v1/room/{id}/setActive:
              post:
                summary: >-
                  Deactivate or reactivate a chatroom. At creation, a new
                  chatroom is active.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom.
                  - At
                  - Creation,
                  - New
                  - Chatroom
                  - Is
                  - Active.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v3/room/{id}/update:
              post:
                summary: Update the attributes of an existing chatroom.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v1/room/{id}/membership/add:
              post:
                summary: Adds new member to an existing room.
                tags:
                  - Adds
                  - New
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/remove:
              post:
                summary: Removes member from an existing room.
                tags:
                  - Removes
                  - Member
                  - From
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/promoteOwner:
              post:
                summary: Promotes user to owner.
                tags:
                  - Promotes
                  - User
                  - To
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v1/room/{id}/membership/demoteOwner:
              post:
                summary: Demotes room owner.
                tags:
                  - Demotes
                  - Room
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/room/{id}/membership/list:
              get:
                summary: Lists current members of an existing room.
                tags:
                  - Lists
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/sessioninfo:
              get:
                summary: Get information about the current user's session.
                tags:
                  - Get
                  - Information
                  - About
                  - The
                  - Current
                  - User's
                  - Session.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v2/user:
              get:
                summary: Get user information
                tags:
                  - Get
                  - User
                  - Information
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v3/users:
              get:
                summary: |
                  Search users by emails or ids.
                  Only one of the search lists should be informed at a time.
                  Search lists may containt up to 100 elements.
                tags:
                  - Search
                  - Users
                  - By
                  - Emails
                  - Or
                  - |
                    Ids.
                  - Only
                  - One
                  - Of
                  - The
                  - Lists
                  - Should
                  - Be
                  - Informed
                  - At
                  - |
                    Time.
                  - May
                  - Containt
                  - Up
                  - To
                  - '100'
                  - |
                    Elements.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
            /v1/user/presence/register:
              post:
                summary: Register interest in a user's presence status
                tags:
                  - Register
                  - Interest
                  - In
                  - User's
                  - Presence
                  - Status
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/user/presence:
              get:
                summary: Get presence information about the requesting user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - The
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
              post:
                summary: Set the presence of the requesting user.
                tags:
                  - Set
                  - The
                  - Presence
                  - Of
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/{uid}/presence:
              get:
                summary: Get presence information about a particular user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/users/presence:
              get:
                summary: Get presence information about all company (pod) users.
                description: >
                  The returned data is taken from the in-memory cache for
                  performance

                  reasons which means inactive users may be omitted from the
                  response.


                  All non-inactive users WILL be returned and some inactive
                  users MAY

                  be included. Any omitted user IS inactive.


                  Returned records are sorted by user ID, ascending.


                  This method is expensive. It pulls ALL records from the cache,
                  sorts them and then only uses a subset.

                  For large numbers of users, this can be very inefficient both
                  due to sorting

                  and due to the cache being distributed across many nodes.


                  Addiionally, there is the potential to miss users if they
                  become active

                  after the page in which their user ID falls has already been
                  read by the client.

                  To avoid this situation, a presence feed should be created
                  (and optionally read from)

                  first to capture presence changes of users who get reactivated
                  during a paged call to this endpoint.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - All
                  - Company
                  - (pod)
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/presence:
              post:
                summary: Set presence information for a particular user.
                tags:
                  - Set
                  - Presence
                  - Information
                  - For
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/user/search:
              post:
                summary: Search for users by name or email address
                tags:
                  - Search
                  - For
                  - Users
                  - By
                  - Name
                  - Or
                  - Email
                  - Address
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/streams/list:
              post:
                summary: >
                  Retrieve a list of all streams of which the requesting user is
                  a member,

                  sorted by creation date (ascending).
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - The
                  - Requesting
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - |
                    (ascending).
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
            /v1/admin/user/{uid}/streams/list:
              post:
                summary: |
                  Retrieve a list of all streams of which this user is a member,
                  sorted by creation date (ascending). Since SBE 20.16.
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - This
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - (ascending).
                  - Since
                  - |
                    20.16.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
            /v2/streams/{sid}/info:
              get:
                summary: Get information about a partcular stream.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
            /v1/streams/{sid}/attachments:
              get:
                summary: Get attachments in a particular stream.
                tags:
                  - Get
                  - Attachments
                  - In
                  - Particular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
            /v1/admin/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for the company
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
              post:
                summary: Update the application entitlements for the company
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
            /v1/admin/disclaimer/{did}:
              get:
                summary: Get a disclaimer by disclaimer id
                tags:
                  - Get
                  - Disclaimer
                  - By
                  - Id
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/list:
              get:
                summary: List all disclaimers for the company (pod)
                tags:
                  - List
                  - All
                  - Disclaimers
                  - For
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/{did}/users:
              get:
                summary: List all users assigned to this disclaimer
                tags:
                  - List
                  - All
                  - Users
                  - Assigned
                  - To
                  - This
                  - Disclaimer
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/group/list:
              get:
                summary: Get a list of all Information Barrier Groups
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Information
                  - Barrier
                  - Groups
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
            /v1/admin/group/{gid}/membership/list:
              get:
                summary: Get the list of userids in this Information Barrier Group
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Userids
                  - In
                  - This
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/add:
              post:
                summary: Add members to an Information Barrier group.
                tags:
                  - Add
                  - Members
                  - To
                  - An
                  - Information
                  - Barrier
                  - Group.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/remove:
              post:
                summary: Remove members from an Information Barrier group
                tags:
                  - Remove
                  - Members
                  - From
                  - An
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation
                description: >
                  At least two user IDs must be provided or

                  an error response will be sent.


                  The caller is not included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/messagesuppression/{id}/suppress:
              post:
                summary: Suppress a message
                tags:
                  - Suppress
                  - Message
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
            /v1/admin/policy/list:
              get:
                summary: Get all Information Policies
                tags:
                  - Get
                  - All
                  - Information
                  - Policies
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/setActive:
              post:
                summary: Deactivate or reactivate a chatroom via AC Portal.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom
                  - Via
                  - Portal.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/list:
              get:
                summary: Lists current and previous members of an existing room.
                tags:
                  - Lists
                  - Current
                  - And
                  - Previous
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/add:
              post:
                summary: Add a member to an existing room.
                tags:
                  - Add
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/remove:
              post:
                summary: Remove a member from a room.
                tags:
                  - Remove
                  - Member
                  - From
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v2/admin/user/list:
              get:
                summary: Retrieve a list of all users in the company (pod)
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Users
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/user/find:
              post:
                summary: Find a user based on attributes
                tags:
                  - Find
                  - User
                  - Based
                  - 'On'
                  - Attributes
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
            /v1/admin/user/{uid}/roles/add:
              post:
                summary: Add a role to a user
                tags:
                  - Add
                  - Role
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/roles/remove:
              post:
                summary: Remove a role from a user
                tags:
                  - Remove
                  - Role
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for this user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              post:
                summary: Update the application entitlements for this user
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              patch:
                summary: >-
                  Update unique entitlement of an app for this user. Entitlement
                  can be installation, visibility or product
                tags:
                  - Update
                  - Unique
                  - Entitlement
                  - Of
                  - An
                  - App
                  - For
                  - This
                  - User.
                  - Can
                  - Be
                  - Installation,
                  - Visibility
                  - Or
                  - Product
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/avatar:
              get:
                summary: Get the URL of the avatar of a particular user
                tags:
                  - Get
                  - The
                  - Of
                  - Avatar
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/avatar/update:
              post:
                summary: Update the avatar of a particular user
                tags:
                  - Update
                  - The
                  - Avatar
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer:
              get:
                summary: Get the disclaimer assigned to a user
                tags:
                  - Get
                  - The
                  - Disclaimer
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
              delete:
                summary: Unassign a disclaimer from a user
                tags:
                  - Unassign
                  - Disclaimer
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer/update:
              post:
                summary: Assign a disclaimer to a user
                tags:
                  - Assign
                  - Disclaimer
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/delegates:
              get:
                summary: Get the delegates assigned to a user
                tags:
                  - Get
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/delegates/update:
              post:
                summary: Update the delegates assigned to a user
                tags:
                  - Update
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/features:
              get:
                summary: >-
                  Get the list of Symphony feature entitlements enabled for a
                  particular user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - Enabled
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/admin/user/{uid}/features/update:
              post:
                summary: >-
                  Update the list of Symphony feature entitlements for a
                  particular user
                tags:
                  - Update
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/user/{uid}/follow:
              post:
                summary: Make a list of users start following a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Start
                  - Following
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
            /v1/user/{uid}/unfollow:
              post:
                summary: Make a list of users unfollowing a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Unfollowing
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
            /v1/user/{uid}/followers:
              get:
                summary: Returns the list of followers for a specific user
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Followers
                  - For
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
            /v1/user/{uid}/following:
              get:
                summary: Returns the list of users that a specific user is following
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Users
                  - That
                  - Specific
                  - User
                  - Is
                  - Following
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
            /v1/user/manifest/own:
              post:
                summary: Update own service account manifest
                tags:
                  - Update
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
              get:
                summary: Get own service account manifest
                tags:
                  - Get
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
            /v1/admin/user/{uid}/status:
              get:
                summary: Get the status, active or inactive, for a particular user
                tags:
                  - Get
                  - The
                  - Status,
                  - Active
                  - Or
                  - Inactive,
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/user/{uid}/status/update:
              post:
                summary: Update the status of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v2/admin/streams/list:
              post:
                summary: >
                  Retrieve all the streams across the enterprise where the
                  membership of the stream has been modified between a given
                  time range
                tags:
                  - Retrieve
                  - All
                  - The
                  - Streams
                  - Across
                  - Enterprise
                  - Where
                  - Membership
                  - Of
                  - Stream
                  - Has
                  - Been
                  - Modified
                  - Between
                  - Given
                  - Time
                  - |
                    Range
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/stream/{id}/membership/list:
              get:
                summary: >-
                  List the current members of an existing stream.  The stream
                  can be of type IM, MIM, or ROOM
                tags:
                  - List
                  - The
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Stream.
                  - Stream
                  - Can
                  - Be
                  - Type
                  - M,
                  - Or
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
            /v1/admin/system/features/list:
              get:
                summary: Get the full set of Symphony features available for this pod
                tags:
                  - Get
                  - The
                  - Full
                  - Set
                  - Of
                  - Symphony
                  - Features
                  - Available
                  - For
                  - This
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
            /v1/admin/system/protocols/list:
              get:
                summary: Get a list of all URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v2/system/protocols:
              get:
                summary: Get a list of URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols:
              post:
                summary: Add an entry to URI protocols supported by the company (pod)
                tags:
                  - Add
                  - An
                  - Entry
                  - To
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols/{scheme}:
              delete:
                summary: >-
                  Remove an entry from URI protocols supported by the company
                  (pod)
                tags:
                  - Remove
                  - An
                  - Entry
                  - From
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/admin/system/roles/list:
              get:
                summary: Get a list of all roles available in the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Roles
                  - Available
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/message/{mid}/status:
              get:
                summary: Get the read status of a particular message.
                tags:
                  - Get
                  - The
                  - Read
                  - Status
                  - Of
                  - Particular
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/create:
              post:
                summary: Creates a new app
                tags:
                  - Creates
                  - New
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/update:
              post:
                summary: Updates a app
                tags:
                  - Updates
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/delete:
              post:
                summary: Deletes a app
                tags:
                  - Deletes
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/get:
              get:
                summary: Gets a app
                tags:
                  - Gets
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/messages:
              post:
                summary: Fetch message details
                tags:
                  - Fetch
                  - Message
                  - Details
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/create:
              post:
                summary: Create a new V2 User
                tags:
                  - Create
                  - New
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}/update:
              post:
                summary: Update an existing V2 User
                tags:
                  - Update
                  - An
                  - Existing
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}:
              get:
                summary: Retrieve V2 User details for a particular user
                tags:
                  - Retrieve
                  - V2
                  - User
                  - Details
                  - For
                  - Particular
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v1/files/allowedTypes:
              get:
                summary: Get supported attachment types for the pod
                tags:
                  - Get
                  - Supported
                  - Attachment
                  - Types
                  - For
                  - The
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
            /file_ext/v1/allowed_extensions:
              get:
                summary: Allows iteration of all file extensions supported for upload
                description: >
                  Provides a RESTful API to iterate all file extensions
                  configured by the tenant admin

                  that are allowed for the upload.  Pagination of this list is
                  managed through a

                  combination of the optional request parameters and
                  service-side managed maximums.


                  Pagination of the results is provided through the before or
                  after input paramters

                  and presented through the opaque cursor values provided as
                  output from a previous

                  response.  Only one of before or after or neither may be
                  provided.


                  DO NOT store cursors. Cursors can quickly become invalid if
                  items are added or deleted.

                  Use them only during a short-period of time that you are
                  traversing the list.
                tags:
                  - Allows
                  - Iteration
                  - Of
                  - All
                  - File
                  - Extensions
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
            /file_ext/v1/allowed_extensions/{extension}:
              put:
                summary: >-
                  Allows replacement or creation of a specific file extension
                  supported for upload
                description: >
                  Provides a method to create or replace a specific file
                  extension configured for upload

                  support via an admin. The API treats the file extension in the
                  path case-insensitively

                  by converting it to lowecase.
                tags:
                  - Allows
                  - Replacement
                  - Or
                  - Creation
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
              delete:
                summary: >-
                  Allows deletion of a specific file extension supported for
                  upload
                description: >
                  Provides a method to delete a specific file extension
                  configured for upload

                  support via an admin. The file extension identifying the
                  resource is treated

                  case-insensitively by the API.
                tags:
                  - Allows
                  - Deletion
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
            /v1/admin/messages/{messageId}/receipts:
              get:
                summary: Fetch receipts details from a specific message.
                tags:
                  - Fetch
                  - Receipts
                  - Details
                  - From
                  - Specific
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
            /v1/languages:
              get:
                summary: Lists available languages for the pod.
                tags:
                  - Lists
                  - Available
                  - Languages
                  - For
                  - The
                  - Pod.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
            /v1/admin/messages/{messageId}/metadata/relationships:
              get:
                summary: Get the message metadata relationship
                tags:
                  - Get
                  - The
                  - Message
                  - Metadata
                  - Relationship
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
            /v1/admin/user/{userId}/suspension/update:
              put:
                summary: Update the status of suspension of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Suspension
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
                  - Suspension
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                  example: 401
                message:
                  type: string
                  example: Invalid session
            CompanyCert:
              type: object
              properties:
                pem:
                  type: string
                  description: An X509 certificate in PEM format
                  example: '--BEGIN CERTIFICATE--MIIH/TC...p9DBiB/--END CERTIFICATE--'
                attributes:
                  $ref: '#/definitions/CompanyCertAttributes'
            CompanyCertDetail:
              type: object
              properties:
                companyCertAttributes:
                  $ref: '#/definitions/CompanyCertAttributes'
                companyCertInfo:
                  $ref: '#/definitions/CompanyCertInfo'
                certInfo:
                  $ref: '#/definitions/CertInfo'
            CompanyCertInfoList:
              type: array
              items:
                type: object
                properties:
                  companyCertAttributes:
                    $ref: '#/definitions/CompanyCertAttributes'
                  companyCertInfo:
                    $ref: '#/definitions/CompanyCertInfo'
                example:
                  - companyCertAttributes:
                      name: agentservice
                      type:
                        type: USER
                      status:
                        type: TRUSTED
                    companyCertInfo:
                      fingerPrint: 300a...
                      lastSeen: 0
                      updatedAt: 0
                      updatedBy: 0
                      commonName: agentservice
                      expiryDate: 1781886755000
            CompanyCertType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - USERSIGNING
                    - USER
                    - OPERATIONSSIGNING
                    - OPERATIONSUSER
                  example: USER
            CompanyCertTypeList:
              type: array
              items:
                $ref: '#/definitions/CompanyCertType'
            CompanyCertStatus:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - TRUSTED
                    - KNOWN
                    - REVOKED
                    - DISABLED
                  example: TRUSTED
            CompanyCertAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Friendly name assigned by administrator
                  example: agentservice
                type:
                  $ref: '#/definitions/CompanyCertType'
                status:
                  $ref: '#/definitions/CompanyCertStatus'
            CompanyCertInfo:
              type: object
              properties:
                fingerPrint:
                  type: string
                  description: Unique identifier
                  example: 300a...
                issuerFingerPrint:
                  type: string
                  description: Unique identifier of issuer cert if known
                  example: 450s...
                lastSeen:
                  type: integer
                  format: int64
                  description: Date when we last saw this certificate presented
                  example: 0
                updatedAt:
                  type: integer
                  format: int64
                  description: Date when this cert was last updated by administrator
                  example: 0
                updatedBy:
                  type: integer
                  format: int64
                  description: User ID of administrator who last updated this cert
                  example: 0
                commonName:
                  type: string
                  description: >-
                    The Symphony account name which this certificate
                    authenticates
                  example: agentservice
                expiryDate:
                  type: integer
                  format: int64
                  description: Expiry date of this cert
                  example: 1781886755000
            CertInfo:
              type: array
              items:
                $ref: '#/definitions/CertInfoItem'
              example:
                - name: Validity
                  attributes:
                    - name: Not Before
                      value: Mon Jan 15 20:56:05 UTC 2018
                    - name: Not After
                      value: Thu Jan 15 20:56:05 UTC 2026
                - name: Public Key
                  attributes:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            CertInfoItem:
              type: object
              properties:
                name:
                  type: string
                  example: Public Key
                attributes:
                  type: array
                  items:
                    $ref: '#/definitions/NameValuePair'
                  example:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            PodCertificate:
              type: object
              properties:
                certificate:
                  description: Certificate in PEM format
                  type: string
                  example: PEM_CERTIFICATE
            NameValuePair:
              type: object
              properties:
                name:
                  type: string
                  example: Algorithm
                value:
                  type: string
                  example: RSA
            Stream:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            UserError:
              description: User error information
              type: object
              properties:
                error:
                  type: string
                  description: Error code informing what is wrong
                  example: invalid.format
                email:
                  type: string
                  description: >-
                    Email with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidemail
                id:
                  type: string
                  description: >-
                    Id with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidid
            UserV2:
              description: User record version 2
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7696581394433
                emailAddress:
                  type: string
                  format: email
                  example: admin@symphony.com
                firstName:
                  type: string
                  example: Symphony
                lastName:
                  type: string
                  example: Admin
                displayName:
                  type: string
                  example: Symphony Admin
                title:
                  type: string
                  example: Administrator
                company:
                  type: string
                  example: Acme
                username:
                  type: string
                  example: admin@symphony.com
                location:
                  type: string
                  example: California
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                avatars:
                  $ref: '#/definitions/AvatarList'
                workPhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33901020304'
                mobilePhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33601020304'
                jobFunction:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Sales
                department:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: APIs
                division:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Partnerships
                roles:
                  $ref: '#/definitions/StringList'
                  example:
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            V2UserList:
              description: List of User record version 2
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  description: List of all users found with the search
                  example:
                    - id: 15942919536460
                      emailAddress: technicalwriter@symphony.com
                      firstName: Technical
                      lastName: Writer
                      displayName: Technical Writer
                      title: Technical Writer
                      company: Symphony
                      department: Marketing // if internal user
                      username: tw
                      accountType: NORMAL
                      location: France // if internal user
                      mobilePhoneNumber: 33601020304
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                    - id: 15942919536461
                      emailAddress: serviceaccount@symphony.com
                      firstName: null
                      lastName: null
                      displayName: Service Account
                      title: null
                      company: pod232
                      department: Marketing // if internal user
                      username: SA
                      location: France // if internal user
                      accountType: SYSTEM
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/UserError'
                  description: List of all errors found with the informed search criteria
                  example:
                    - error: invalid.format
                      email: notavalidemail
                    - error: invalid.format
                      id: 654321
            UserSearchResults:
              type: object
              properties:
                count:
                  description: The total number of users which matched the search criteria.
                  type: integer
                  format: int64
                  example: 1
                skip:
                  description: The number of skipped results.
                  type: integer
                  format: int64
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  format: int64
                  example: 1
                searchQuery:
                  $ref: '#/definitions/UserSearchQuery'
                users:
                  description: A list of users which matched by the search criteria.
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  example:
                    - null
            UserSearchFilter:
              type: object
              properties:
                accountTypes:
                  $ref: '#/definitions/StringList'
                  description: type of user used to search
                  example: NORMAL
                title:
                  type: string
                  description: user's job title
                  example: Sales Manager
                company:
                  type: string
                  description: company name
                  example: Symphony
                location:
                  type: string
                  description: city of the user's job location
                  example: Marseille
                marketCoverage:
                  type: string
                  description: geographic area the user works with
                  example: EMEA
                responsibility:
                  type: string
                  description: user's responsibility
                  example: BAU
                function:
                  type: string
                  description: user's function
                  example: Trade Management
                instrument:
                  type: string
                  description: higher level instrument for the Asset Classes
                  example: Securities
            UserSearchQuery:
              type: object
              properties:
                query:
                  type: string
                  description: >-
                    search / query term.  This can be firstname, lastname,
                    displayname or email
                  example: jane
                filters:
                  $ref: '#/definitions/UserSearchFilter'
            UserNameList:
              type: array
              items:
                type: object
                $ref: '#/definitions/UserName'
            UserName:
              type: object
              properties:
                username:
                  type: string
                  example: dpayet
            UserIdList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 7215545058313
                - 7215545078461
            UserId:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058313
            StringId:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                description:
                  type: string
                  description: Room description.
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
            V3RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                keywords:
                  type: array
                  description: Keywords for search to use to find this room
                  items:
                    $ref: '#/definitions/RoomTag'
                  example:
                    - key: region
                      value: EMEA
                    - key: lead
                      value: Daffy Duck
                description:
                  type: string
                  description: Room description.
                  example: Created via the API
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                  example: true
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
                  example: false
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                  example: false
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                  example: false
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
                  example: false
                crossPod:
                  type: boolean
                  description: If true, this room is a cross pod room
                  example: false
                viewHistory:
                  type: boolean
                  description: >-
                    If true, new members can view the room chat history of the
                    room.
                  example: false
                multiLateralRoom:
                  type: boolean
                  description: >-
                    If true, this is a multi lateral room where we can find
                    users belonging to more than 2 companies.
                  example: false
                scheduledMeeting:
                  type: boolean
                  description: If true, this room is for a scheduled meeting.
                  example: false
                subType:
                  type: string
                  description: >-
                    This field is ignored when creating a new room as it was
                    only used for email integration which is now sunset.
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the room. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
                groupChat:
                  type: boolean
                  description: >-
                    If true, this room is a group chat. Note: this parameter is
                    ignored for creating rooms. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              properties:
                query:
                  description: The search query. Matches the room name and description.
                  type: string
                  example: automobile
                labels:
                  description: A list of room tag labels whose values will be queried.
                  type: array
                  items:
                    type: string
                  example:
                    - industry
                active:
                  description: >-
                    Restrict the search to active/inactive rooms. If
                    unspecified, search all rooms.
                  type: boolean
                  example: true
                private:
                  description: >-
                    Restrict the search to private rooms. If unspecified, search
                    all rooms.
                  type: boolean
                  example: true
                owner:
                  $ref: '#/definitions/UserId'
                creator:
                  $ref: '#/definitions/UserId'
                member:
                  $ref: '#/definitions/UserId'
                sortOrder:
                  description: >
                    Sort algorithm to be used. Supports two values: "BASIC"
                    (legacy algorithm)

                    and "RELEVANCE" (enhanced algorithm).
                  type: string
                  enum:
                    - BASIC
                    - RELEVANCE
                  example: RELEVANCE
              required:
                - query
            V2RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              allOf:
                - $ref: '#/definitions/RoomSearchCriteria'
                - type: object
                  properties:
                    subType:
                      description: >-
                        Restrict the search to the specific room subtype. Valid
                        values are: EMAIL
                      type: string
                      example: EMAIL
            V3RoomSearchResults:
              description: A list of search results and counts per search parameter.
              properties:
                count:
                  description: The total number of rooms matched by the search.
                  type: integer
                  format: int64
                  example: 2
                skip:
                  description: The number of skipped results.
                  type: integer
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  example: 10
                query:
                  $ref: '#/definitions/V2RoomSearchCriteria'
                rooms:
                  description: A list of rooms matched by the query.
                  type: array
                  items:
                    $ref: '#/definitions/V3RoomDetail'
                  example:
                    - roomAttributes:
                        name: Automobile Industry Room
                        description: Room to discuss car companies
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: tzwvAZIdDMG3ZPRxv+xsgH///qr+JJkWdA==
                        creationDate: 1464615003895
                        createdByUserId: 7696581411197
                        active: true
                    - roomAttributes:
                        name: Tesla Room
                        keywords:
                          - key: industry
                            value: automobile
                        description: Discussions on TSLA
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: o6UkQ1TEmU0Tf/DHUlZrCH///qr+JQowdA==
                        creationDate: 1464614974947
                        createdByUserId: 7696581411197
                        active: true
                facetedMatchCount:
                  description: Detailed counts of matched rooms per search criterion.
                  type: array
                  items:
                    $ref: '#/definitions/FacetedMatchCount'
                  example:
                    - facet: industry
                      count: 1
            RoomTag:
              description: >-
                Room Tag object. A key:value pair describing additional
                properties of the room.
              properties:
                key:
                  description: A unique label of the Tag.
                  type: string
                  example: region
                value:
                  description: The value of this Tag's label.
                  type: string
                  example: EMEA
              required:
                - key
                - value
            FacetedMatchCount:
              description: An object respresenting the result count of faceted search.
              properties:
                facet:
                  description: The matched query.
                  type: string
                count:
                  description: The result count.
                  type: integer
            RoomSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: bjHSiY4iz3ar4iIh6-VzCX___peoM7cPdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1547661232368
                createdByUserId:
                  type: integer
                  format: int64
                  example: 14362370637825
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ImmutableRoomAttributes:
              type: object
              description: >-
                These attributes cannot be changed once the room has been
                created
              properties:
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
            RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                immutableRoomAttributes:
                  $ref: '#/definitions/ImmutableRoomAttributes'
            V3RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/V3RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                groups:
                  description: List of groups (aka SDLs) that were added to the room.
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            GroupItem:
              type: object
              properties:
                id:
                  description: The ID of the added group (aka SDL).
                  type: integer
                  format: int64
                  example: 68719476744
                addedBy:
                  description: The user ID who added the group to the room.
                  type: integer
                  format: int64
                  example: 68719476743
            SuccessResponse:
              type: object
              properties:
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
                message:
                  type: string
                  example: Success
            AvatarUpdate:
              type: object
              properties:
                image:
                  description: Base64 encoded image. Original image must be less than 2MB.
                  type: string
                  example: >-
                    iVBORw0KGgoAAAANSUhEUgAAAJgAAAAoCAMAAAA11sNmAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAX1QTFRFAAAAVVVVZmZmc8bmd3d3jMyMmZmZ+cxA////VVVVZmZmc8bmd3d3jMyM8oCZ+cxA////VVVVZmZmc8bmd3d3jMyM////VVVVZmZmc8bmd3d3jMyMmZmZ8oCZ+cxA////ZmZmjMyM////VVVVd3d3jMyM+cxA////VVVVZmZmc8bmd3d3jMyMmZmZnMyB8oCZ+cxA////ZmZmc8bmd3d3jMyMmZmZ+cxA////d3d3jMyM8oCZ+cxA////VVVVZmZmdm1RjMyM8oCZ+cxA////ZmZmmZmZ+cxA////W1tbZmZmc8bmdpGcd3d3jMyMmZmZ8oCZ////d3d3jMyMmZmZx3iJ+cxA////VVVVZmZmc8bmd3d3jMyMuIOVyqpG////VVVVZmZmbW1td3d3jMyMmZmZ+cxA////VVVVX1xUZmZmb46ac8bmdZ+vd3d3fnNQjMyMkpeGlqaWmJyYmZmZnYlMp5FLsZhJvJ9Iz3qM0K5F78VB8oCZ+cxA////9laq9wAAAGh0Uk5TABAQEBAQEBAQICAgICAgICAwMDAwMDBAQEBAQEBAQEBQUFBgYGBgYHBwcHBwcHBwcHCAgICAgICAj4+Pj4+fn5+fn5+fr6+vr7+/v7+/v7+/v8/Pz8/Pz9/f39/f39/f7+/v7+/v7+/qia/hAAADQ0lEQVRYw+2Xa1fTQBCGV0WJCBIvxEq10YoEVNQoaLxURKNWUHRRqYgaUSC1QkWsNzT7252Z3W1TWpCjX+I5fT/ksrM782T2Tc4JYy211NL/oJ50Ot2TRLD5FdTkma6kgU2uSB1PGtiY5HqZuK0ckWAjiQNLS7CdiQPrIq6xpGHtGnr0eRXA0gnjGlqoVCoA9kTe9rfXQob1r8ntv1mUmjlGYBUJdhJv2u9FlzWVHwohAt9kBuc+Dfk8zxjnWRnn3GHM4lKuAUM5nsMIjNETOQVM4NJstQpCzKxL10TjpdJ4B5zvEtg8Wj+zGEVRtwxjVpLFckIAA8sKAVWECBGCeUJ40BI9qwCDXHBqkxDYKT8WwVWWDDFMh5QOpWtURwk0dwE8toBgV2HoeoQ6T2GL6rJsAZ7OCBAGjgUqIbAvptBgNggo/XVgMJQ3mZmHk1wVGArMCPEajrxpwwZLpJkUO4JgXax7mriiaaay1xyWRQhPjsgmAoQGk9uCVeJg1bo+TafW6enxdI26U1Ia3X6psjrJ+hcjJQpjRwLOPYf2DZ7blp2iEhxz14FxCRZ4IB/BbLlflMjDVQVsqprOKZ3HNrKY0tzg09Wzt4Ho59r3NThlKO6E0iLkDTNUe4EloLAb4FGCIUuebrg2HIB5ihgXEJgNZI4Ci6XbDKxUevvp9bcvH98Xi8WvVTAo6no5yBbgtSt0B6AEAoRGM/PXOuZUd0qDgUeFxnWFfEGaaX8q9eyH0qsP998USTczmUx7/BPkqlSByOs6NrwY8EJpMPxa+E51P5XHTL1VLj0RDlm0B6w+XVPd+kV6fHRieWrbwHMEO6FjDr5TMTCuLYElctjGOo+x9WC4r0hrh9RyGsrWwPhGDiOdk1js4tJy+Qpjh24Ui/t0LIceJ/PkG8GM0P4jGPqogFYILQ2GxtsS2F7CYoeXAKzcCwO7B2rBrPrCcqMRrOadjcHgCy/NZ8VW+VsDY9cAi+14QWDv2tZHLcfzXP2tsWxTvRK2oS9gxLBjHrZsmm3oKZbreVbdqur0arpNtGeCwMoPk/czcuDUAwArn07gf9IwgpUPJhVsqi2hYLOdiQSb7Uugx3qH+zpZSy211FJNvwFNoXAncdBvawAAAABJRU5ErkJggg==
            Avatar:
              type: object
              properties:
                size:
                  description: The Avatar Size
                  type: string
                  example: original
                url:
                  description: Url of the image
                  type: string
                  example: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
            AvatarList:
              type: array
              items:
                $ref: '#/definitions/Avatar'
              example:
                - size: original
                  url: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
                - size: small
                  url: >-
                    ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8_small.png
            UserStatus:
              type: object
              properties:
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
            UserFilter:
              type: object
              properties:
                role:
                  type: string
                  description: The user role
                  example: INDIVIDUAL
                feature:
                  type: string
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
            PasswordReset:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - EMAIL
                  example: EMAIL
            FeatureList:
              type: array
              items:
                $ref: '#/definitions/Feature'
              example:
                - entitlment: canCreatePublicRoom
                  enabled: true
                - entitlment: isExternalRoomEnabled
                  enabled: false
                - entitlment: canUpdateAvatar
                  enabled: true
            Feature:
              description: Entitlement feature record.
              type: object
              properties:
                entitlment:
                  type: string
                  example: canCreatePublicRoom
                enabled:
                  type: boolean
                  description: Whether this entitlement is enabled for the user.
                  example: true
            Group:
              description: Information Barrier Group record.
              type: object
              properties:
                id:
                  type: string
                  example: 571db1f2e4b027c4f055a594
                name:
                  type: string
                  example: Group 1
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 1
                policies:
                  type: array
                  items:
                    type: string
                  example:
                    - 571db2e4e4b012df6341f393
                createdDate:
                  type: integer
                  format: int64
                  example: 1461563890135
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461563926812
            Product:
              description: Application Product
              type: object
              required:
                - name
                - type
                - subscribed
              properties:
                appId:
                  type: string
                  description: App ID for the Product
                  maxLength: 256
                  minLength: 1
                  example: selerity
                name:
                  type: string
                  minLength: 1
                  maxLength: 50
                  description: Product Name
                  example: Premium
                sku:
                  type: string
                  minLength: 1
                  maxLength: 100
                  description: Product SKU
                  example: AcDccU53SsY
                subscribed:
                  type: boolean
                  description: indicate whether the product is subscribed or not
                  example: false
                type:
                  type: string
                  description: Product Type (default or premium)
                  example: premium
            ProductList:
              type: array
              items:
                $ref: '#/definitions/Product'
              example:
                - appId: selerity
                  name: Standard
                  subscribed: true
                  type: default
                - appId: selerity
                  name: Premium
                  sku: AcDccU53SsY
                  subscribed: false
                  type: premium
            PolicyList:
              type: array
              items:
                $ref: '#/definitions/Policy'
              example:
                - id: 56e9df05e4b00737e3d3b82d
                  policyType: BLOCK
                  active: true
                  groups:
                    - 56e9def8e4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                  createdDate: 1458167557358
                  modifiedDate: 1458330606752
                - id: 571cd64de4b042aaf06d2d8b
                  policyType: BLOCK
                  active: true
                  groups:
                    - 571cd646e4b042aaf06d2d84
                    - 571cd64ce4b042aaf06d2d8a
                  createdDate: 1461507661146
                  modifiedDate: 1461507661146
            Policy:
              description: Information Barrier Policy record.
              type: object
              properties:
                id:
                  type: string
                  example: 56e9df05e4b00737e3d3b82d
                policyType:
                  type: string
                  enum:
                    - BLOCK
                    - ALLOW
                  example: BLOCK
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 3
                groups:
                  type: array
                  items:
                    type: string
                  example:
                    - 56e9deffe4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                createdDate:
                  type: integer
                  format: int64
                  example: 1458167557358
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1458330606752
            UserAppEntitlement:
              description: Application Entitlements for the user
              type: object
              required:
                - appId
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Selerity Context
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    this user.  Otherwise, this application will be hidden in
                    the appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, it indicate this application is installed for this
                    user.  Otherwise, this user does not have this application
                    installed.
                  example: true
                products:
                  $ref: '#/definitions/ProductList'
            PodAppEntitlement:
              description: Application Entitlements for the company
              type: object
              required:
                - appId
                - appName
                - enable
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: djApp
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Dow Jones
                enable:
                  type: boolean
                  example: true
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    everyone.  Otherwise, this application will be hidden in the
                    appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, the entitlement is set to automatic for the
                    company.  Otherwise, it is set to manual.
                  example: true
            Role:
              description: Role record.
              type: object
              properties:
                id:
                  type: string
                  format: long
                name:
                  type: string
                description:
                  type: string
            RoleDetailList:
              type: array
              items:
                $ref: '#/definitions/RoleDetail'
              example:
                - id: CONTENT_MANAGEMENT
                  name: Content Management
                  userTypes:
                    - SYSTEM
                    - NORMAL
                  optionalActions:
                    - MONITOR_ROOMS
                - id: COMPLIANCE_OFFICER
                  name: Compliance Officer
                  userTypes:
                    - NORMAL
                  optionalActions:
                    - BAN_AND_UNBAN_ROOM_MEMBER
                    - LOCK_AND_UNLOCK_ROOM
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            RoleDetail:
              description: Role detailed.
              type: object
              properties:
                id:
                  type: string
                  example: CONTENT_MANAGEMENT
                name:
                  type: string
                  example: Content Management
                userTypes:
                  type: array
                  items:
                    type: string
                  example:
                    - NORMAL
                    - SYSTEM
                optionalActions:
                  type: array
                  items:
                    type: string
                  example:
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            GroupList:
              type: array
              items:
                $ref: '#/definitions/Group'
              example:
                - id: 571db1f2e4b027c4f055a594
                  name: Group 1
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563890135
                  modifiedDate: 1461563926812
                - id: 571db20ae4b012df6341f391
                  name: Group 2
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563914581
                  modifiedDate: 1461564112286
            UserAppEntitlementsPatchList:
              description: Array of app entitlements to patch for a user
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlementPatch'
            UserAppEntitlementPatchEnum:
              type: object
              default: KEEP
              description: null
              properties:
                type:
                  type: string
                  enum: &ref_0
                    - 'TRUE'
                    - 'FALSE'
                    - KEEP
                    - REMOVE
                  description: |
                    UserAppEntitlementPatchEnum type :
                     * TRUE - The parameter should be set to true.
                     * FALSE - The parameter should be set to false.
                     * KEEP - The parameter should not be updated, the current value will be kept.
                     * REMOVE - The parameter should be reverted to tenant level's value.
                  example: KEEP
            UserAppEntitlementPatch:
              description: Application Entitlements to patch for the user
              type: object
              required:
                - appId
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                listed:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be listed in the appstore
                    for this user. If "FALSE", this application will be hidden
                    in the appstore. If "KEEP" or not set, the current value is
                    kept. If "REMOVE", it will be removed from user settings and
                    the pod level setting's value will be used.
                  example: KEEP
                install:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be installed for this user.
                    If "FALSE", this application will not be installed for this
                    user. If "KEEP" or not set, the current value is kept. If
                    "REMOVE", it will be removed from user settings and the pod
                    level setting's value will be used.
                  example: true
                product:
                  $ref: '#/definitions/Product'
            UserAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  listed: true
                  install: true
                  products:
                    - appId: selerity
                      name: Standard
                      subscribed: true
                      type: default
                    - appId: selerity
                      name: Premium
                      sku: AcDccU53SsY
                      subscribed: false
                      type: premium
            PodAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/PodAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  enable: true
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  enable: false
                  listed: true
                  install: true
            RoleList:
              type: array
              items:
                $ref: '#/definitions/Role'
            IntegerList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 1461508270000
                - 7215545057281
            StringList:
              type: array
              items:
                type: string
              example:
                - ftp
                - mailto
                - fdsup
                - skype
            DisclaimerList:
              type: array
              items:
                $ref: '#/definitions/Disclaimer'
              example:
                - id: 571d2052e4b042aaf06d2e7a
                  name: Enterprise Disclaimer
                  content: This is a disclaimer for the enterprise.
                  frequencyInHours: 24
                  isDefault: false
                  isActive: true
                  createdDate: 1461526610846
                  modifiedDate: 1461526610846
                - id: 571d20dae4b042aaf06d2e7c
                  name: New Enterprise Disclaimer
                  content: This is a second enterprise disclaimer.
                  frequencyInHours: 168
                  isDefault: false
                  isActive: true
                  createdDate: 1461526746875
                  modifiedDate: 1461526746875
            Disclaimer:
              type: object
              properties:
                id:
                  type: string
                  example: 571d20dae4b042aaf06d2e7c
                name:
                  type: string
                  example: New Enterprise Disclaimer
                content:
                  type: string
                  example: This is a second enterprise disclaimer.
                frequencyInHours:
                  type: integer
                  format: int32
                  example: 168
                isDefault:
                  type: boolean
                  example: false
                isActive:
                  type: boolean
                  example: true
                createdDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
            DelegateAction:
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 7215545078461
                action:
                  type: string
                  enum:
                    - ADD
                    - REMOVE
                  example: ADD
            UserInfo:
              description: User record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
            UserAttributes:
              description: User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: janedoe@symphony.com
                firstName:
                  type: string
                  example: Jane
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: jane.doe
                displayName:
                  type: string
                  example: Jane Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+12349999999'
                mobilePhoneNumber:
                  type: string
                  example: '+12349999999'
                smsNumber:
                  type: string
                  example: '+12349999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Commodities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Financials
                    - Services
            V2UserDetail:
              description: V2 Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            V2UserAttributes:
              description: V2 User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: johndoe@symphony.com
                firstName:
                  type: string
                  example: John
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: johndoe
                displayName:
                  type: string
                  example: John Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+15419999999'
                mobilePhoneNumber:
                  type: string
                  example: '+15419999999'
                twoFactorAuthPhone:
                  type: string
                  example: '+15419999999'
                smsNumber:
                  type: string
                  example: '+15419999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                recommendedLanguage:
                  type: string
                  example: english
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Healthcare
                    - Technology
                marketCoverage:
                  type: array
                  items:
                    type: string
                  example:
                    - EMEA
                responsibility:
                  type: array
                  items:
                    type: string
                  example:
                    - BAU
                function:
                  type: array
                  items:
                    type: string
                  example:
                    - Trade Processing
                instrument:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                currentKey:
                  $ref: '#/definitions/V2UserKeyRequest'
                previousKey:
                  $ref: '#/definitions/V2UserKeyRequest'
            V2UserKeyRequest:
              description: User RSA key information.
              type: object
              properties:
                key:
                  description: User RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1467562406219
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the user's
                    active RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the user's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            V2UserCreate:
              description: >
                V2 User Creation Object.

                After creation, modify roles, features etc via the specific API
                calls.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                password:
                  $ref: '#/definitions/Password'
                roles:
                  type: array
                  items:
                    type: string
                  example:
                    - INDIVIDUAL
                    - COMPLIANCE_OFFICER
            V2UserDetailList:
              type: array
              items:
                $ref: '#/definitions/V2UserDetail'
              example:
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: admin@mail.com
                    firstName: admin
                    lastName: admin
                    userName: admin@mail.com
                    displayName: Admin Admin
                    companyName: Company Name
                    department: Departament
                    division: Division
                    title: Administrator
                    twoFactorAuthPhone: '+15419999999'
                    workPhoneNumber: '+15419999999'
                    mobilePhoneNumber: '+15419999999'
                    accountType: NORMAL
                    assetClasses:
                      - Currencies
                    industries:
                      - Technology
                  userSystemInfo:
                    id: 7696581394433
                    status: ENABLED
                    suspended: false
                    createdDate: 1438054194000
                    lastUpdatedDate: 1527532171729
                    lastLoginDate: 1523912043015
                  roles:
                    - SUPER_COMPLIANCE_OFFICER
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            UserSystemInfo:
              description: User Status Information.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545078461
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
                createdDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                createdBy:
                  type: string
                  example: '7215545057281'
                lastUpdatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastLoginDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastPasswordReset:
                  type: integer
                  format: int64
                  example: 1461508270000
                deactivatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
            UserDetailList:
              type: array
              items:
                $ref: '#/definitions/UserDetail'
              example:
                - userAttributes:
                    emailAddress: janedoe@symphony.com
                    firstName: Jane
                    lastName: Doe
                    userName: jane.doe
                    displayName: Jane Doe
                    accountType: NORMAL
                    assetClasses:
                      - Commodities
                    industries:
                      - Financials
                      - Healthcare
                  userSystemInfo:
                    id: 9826885173258
                    status: ENABLED
                    suspended: true
                    suspensionReason: The user will be OOO due to a mandatory leave
                    suspendedUntil: 1601546400
                    createdDate: 1499347606000
                    createdBy: '9826885173252'
                    lastUpdatedDate: 1499348554853
                    lastLoginDate: 1504839044527
                  roles:
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
            UserDetail:
              description: Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            Password:
              description: >-
                Password. Stored as derived password in both the Pod and the Key
                Manager using PBKDF2 function. Number of iterations should be
                10000 and desired length 256 bits.
              type: object
              properties:
                hSalt:
                  description: Pod password salt used for PBKDF2 derivation.
                  type: string
                  example: hsalt
                hPassword:
                  description: Pod password derived with PBKDF2.
                  type: string
                  example: hpassword
                khSalt:
                  description: Key Manager password salt used for PBKDF2 derivation.
                  type: string
                  example: khsalt
                khPassword:
                  description: Key Manager password derived with PBKDF2.
                  type: string
                  example: khpassword
            MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7078106103810
                owner:
                  type: boolean
                  example: true
                joinDate:
                  type: integer
                  format: int64
                  example: 1461426797833
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            MembershipList:
              description: List of members in a room.
              type: array
              items:
                $ref: '#/definitions/MemberInfo'
              example:
                - id: 7078106103900
                  owner: false
                  joinDate: 1461430710531
                - id: 7078106103809
                  owner: true
                  joinDate: 1461426797875
                - id: 7078106103810
                  owner: true
                  joinDate: 1461426797833
                  addedThroughGroups:
                    - 68719476744
            V2MemberUserDetail:
              description: User detail information for stream membership
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 13537736917013
                email:
                  type: string
                  example: dpayet@om.fr
                firstName:
                  type: string
                  example: Dimitri
                lastName:
                  type: string
                  example: Payet
                displayName:
                  type: string
                  description: Display name for the user
                  example: Dimitri Payet
                company:
                  type: string
                  description: Company name
                  example: Mars
                companyId:
                  type: integer
                  description: Company ID
                  example: 13
                isExternal:
                  type: boolean
                  description: true indicate that this user belong to another company
                  example: true
            V2MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/V2MemberUserDetail'
                isOwner:
                  type: boolean
                  description: true if this is an owner of the room
                  example: true
                isCreator:
                  type: boolean
                  description: true if this is the creator of the room
                  example: true
                joinDate:
                  description: unix timestamp for join date
                  type: integer
                  format: int64
                  example: 1604494574047
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            V2MemberInfoList:
              type: array
              items:
                $ref: '#/definitions/V2MemberInfo'
              example:
                - user:
                    userId: 13537736917000
                    email: john.doe@symphony.com
                    firstName: John
                    lastName: Doe
                    displayName: John Doe
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: true
                  isCreator: true
                  joinDate: 1604494574047
                - user:
                    userId: 13537736917001
                    email: bot@symphony.com
                    displayName: User Provisioning Bot
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: false
                  isCreator: false
                  joinDate: 1604494605272
                  addedThroughGroups:
                    - 68719476744
            V2MembershipList:
              description: List of members in the stream.
              type: object
              properties:
                count:
                  type: integer
                  description: total members count
                  example: null
                skip:
                  type: integer
                  description: number of items to skip from the request
                  example: null
                limit:
                  type: integer
                  description: maximum number of items to return
                  example: null
                members:
                  $ref: '#/definitions/V2MemberInfoList'
            MessageSuppressionResponse:
              description: The suppression state of a message
              type: object
              properties:
                messageId:
                  type: string
                  example: _Gj13MiR-5IrVtrmPNl6fn___qvWCYI_dA
                suppressed:
                  type: boolean
                  example: true
                suppressionDate:
                  type: integer
                  format: int64
                  description: The date when this message was suppressed.
                  example: 1461565603191
            BulkActionResult:
              description: >
                The results of list based bulk action. The list contains the
                result messages

                in the same order as submitted. The message will be an empty
                string if the action

                was successful for item in that index.
              properties:
                overallResult:
                  type: string
                  enum:
                    - SUCCESS
                    - FAIL
                  example: SUCCESS
                results:
                  type: array
                  items:
                    type: string
                  example:
                    - ''
            UserConnectionRequest:
              type: object
              description: Request body for the Connection APIs
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
            UserConnection:
              type: object
              description: Connection status between two users
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
                status:
                  type: string
                  description: >-
                    Connection status between the requesting user and the
                    request sender
                  enum:
                    - PENDING_INCOMING
                    - PENDING_OUTGOING
                    - ACCEPTED
                    - REJECTED
                  example: ACCEPTED
                firstRequestedAt:
                  type: integer
                  format: int64
                  description: unix timestamp when the first request was made
                  example: 1470018073812
                updatedAt:
                  type: integer
                  format: int64
                  description: unix timestamp on the last updated date
                  example: 1471018076255
                requestCounter:
                  type: integer
                  format: int32
                  description: number of requests made
                  example: 1
            UserConnectionList:
              type: array
              items:
                $ref: '#/definitions/UserConnection'
              example:
                - userId: 769658112378
                  status: PENDING_OUTGOING
                  firstRequestedAt: 1470018073812
                  updatedAt: 1471018076255
                  requestCounter: 1
                - userId: 7078106103809
                  status: ACCEPTED
            StreamList:
              description: A list of streams of which the requesting user is a member.
              type: array
              items:
                $ref: '#/definitions/StreamAttributes'
            StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                active:
                  type: boolean
                  description: If true, this stream is active.
                streamType:
                  $ref: '#/definitions/StreamType'
                streamAttributes:
                  $ref: '#/definitions/ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/RoomSpecificStreamAttributes'
            StreamType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - IM
                    - MIM
                    - ROOM
                    - POST
                  example: ROOM
            ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
            StreamFilter:
              description: Stream filtering parameters.
              properties:
                streamTypes:
                  description: Types of streams to search for.
                  type: array
                  items:
                    $ref: '#/definitions/StreamType'
                  example:
                    - type: IM
                    - type: ROOM
                includeInactiveStreams:
                  description: Whether to include inactive streams in the list of results.
                  type: boolean
                  example: 'false'
            V2StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                  example: BZQYepoT0Zf4vL_jpeMPqn___oEWvVy3dA
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                active:
                  type: boolean
                  description: If true, this stream is active.
                  example: true
                lastMessageDate:
                  type: integer
                  format: int64
                  description: unix timestamp of the last message sent in the stream
                  example: 1644590972696
                streamType:
                  description: >-
                    The type of the stream (IM = IM, multi-IM = MIM, chat room =
                    ROOM, user wall = POST).
                  $ref: '#/definitions/V2StreamType'
                streamAttributes:
                  $ref: '#/definitions/V2ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/V2RoomSpecificStreamAttributes'
            V2StreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            V2ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            V2RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                groups:
                  description: >-
                    List of groups (aka SDLs) that were added to the room. Since
                    SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            V2AdminStreamFilter:
              description: stream filter criteria
              type: object
              properties:
                streamTypes:
                  description: type of streams to search for
                  type: array
                  items:
                    description: Valid values are IM, MIM or ROOM
                    $ref: '#/definitions/V2AdminStreamType'
                  example:
                    - type: IM
                    - type: ROOM
                scope:
                  description: >
                    Scope of the room. Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    scope
                  type: string
                  example: INTERNAL
                origin:
                  description: >
                    Origin of the room. It indicates whether the room was
                    created by a user within the company by another company.

                    Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    origin
                  type: string
                  example: INTERNAL
                status:
                  description: >
                    Status of the room.

                    Valid values are ACTIVE or INACTIVE.

                    If not specified, it will include both Active and Inactive
                    status
                  type: string
                  example: ACTIVE
                privacy:
                  description: >
                    Privacy setting of the stream.

                    Valid values are PUBLIC or PRIVATE.

                    If not specified, it will include both public and private
                    streams
                  type: string
                  example: PRIVATE
                startDate:
                  description: Start date in unix timestamp in millseconds
                  type: integer
                  format: int64
                  example: 1481575056047
                endDate:
                  description: >-
                    End date in unix timestamp in millseconds.  If not
                    specified, it assume to be current time.
                  type: integer
                  format: int64
                  example: 1483038089833
            V2AdminStreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            AdminJustifiedUserAction:
              type: object
              properties:
                userId:
                  description: The userId of the target user.
                  type: integer
                  format: int64
                justification:
                  description: The reason for the requested action.
                  type: string
            AdminJustifiedAction:
              type: object
              properties:
                justification:
                  description: The reason for the requested action.
                  type: string
            MessageStatusUser:
              type: object
              properties:
                userId:
                  type: string
                  example: 7078106103901
                firstName:
                  type: string
                  example: Gustav
                lastName:
                  type: string
                  example: Mahler
                displayName:
                  type: string
                  example: Gustav Mahler
                email:
                  type: string
                  example: gustav.mahler@music.org
                userName:
                  type: string
                  example: gmahler
                timestamp:
                  type: string
                  example: 1531968487845
            MessageStatus:
              description: >
                Holds the status of a particular message, indicating which user
                the message has been sent, delivered or read.
              type: object
              properties:
                author:
                  description: User who has sent the message.
                  type: object
                  $ref: '#/definitions/MessageStatusUser'
                read:
                  description: >-
                    All users who have read that message, in any Symphony
                    client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                delivered:
                  description: >
                    All users who have at least one Symphony client to which the
                    message has been delivered, and not read yet.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                sent:
                  description: >
                    All users to whom the message has been sent and received by
                    the Symphony system,

                    but not yet delivered to any user's Symphony client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                  example:
                    - userId: 7078106103904
                      firsName: Benjamin
                      lastName: Britten
                      displayName: Benjamin Britten
                      email: benjamin.britten@music.org
                      userName: bbritten
                      timestamp: 1484156123000
                    - userId: 7078106103901
                      firsName: Gustav
                      lastName: Mahler
                      displayName: Gustav Mahler
                      email: gmahler@music.org
                      userName: gmahler
                      timestamp: 1531968487845
            ApplicationInfo:
              description: |
                Required information for creating an application.
              type: object
              properties:
                appId:
                  description: An unique id for the application.
                  type: string
                  maxLength: 256
                  minLength: 1
                name:
                  description: User defined name for the application.
                  type: string
                appUrl:
                  description: The url for the app. Must start with "https://".
                  type: string
                domain:
                  description: Domain for app, that must match app url domain.
                  type: string
                publisher:
                  description: The publisher for this application.
                  type: string
              example:
                appId: my-test-app
                name: my-test-app
                appUrl: https://joe.mydomain.com
                domain: mydomain.com
                publisher: Joe Smith
            ApplicationDetail:
              description: Detailed record of application.
              type: object
              properties:
                applicationInfo:
                  $ref: '#/definitions/ApplicationInfo'
                iconUrl:
                  description: Url to a icon to use for app. Must start with "https://".
                  type: string
                  example: https://myiconUrl.com
                description:
                  description: Description of the application.
                  type: string
                  example: a test app
                allowOrigins:
                  description: >
                    The permitted domains to send or receive a request from.

                    The field is for the purpose of CORS which set the app
                    specific "ALLOW-ORIGIN-DOMAINS" header in HTTP.
                  type: string
                  example: mydomain.com
                permissions:
                  description: >
                    List of application permissions provisioned for the
                    application.

                    In addition to the known ones, custom permissions are
                    accepted.

                    A custom permission should only contain upper case
                    alphanumeric characters and underscore.

                    It should not be empty or only contain spaces and its length
                    is limited to 64 characters.


                    Known permissions:
                      - SEND_MESSAGES
                      - GET_USER_CONNECTIONS
                      - REQUEST_USER_CONNECTIONS
                      - SET_PRESENCE
                      - GET_PRESENCE
                      - GET_BASIC_USER_INFO
                      - GET_EXTENDED_USER_INFO
                      - GET_BASIC_CONTACT_INFO
                      - GET_EXTENDED_CONTACT_INFO
                      - ACT_AS_USER
                      - MANAGE_SIGNALS
                      - MANAGE_USER_FOLLOWING
                      - TRUST_APP
                  type: array
                  items:
                    type: string
                    maxLength: 64
                    minLength: 1
                  example:
                    - ACT_AS_USER
                    - SEND_MESSAGES
                cert:
                  description: The app public certificate in pem format.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                authenticationKeys:
                  $ref: '#/definitions/AppAuthenticationKeys'
                notification:
                  $ref: '#/definitions/AppNotification'
                properties:
                  $ref: '#/definitions/AppProperties'
            V2PresenceList:
              type: array
              items:
                $ref: '#/definitions/V2Presence'
              example:
                - category: AVAILABLE
                  userId: 14568529068038
                  timestamp: 1533928483800
                - category: OFFLINE
                  userId: 974217539631
                  timestamp: 1503286226030
            V2Presence:
              allOf:
                - $ref: '#/definitions/V2UserPresence'
                - type: object
                  properties:
                    timestamp:
                      type: integer
                      format: int64
                      description: >-
                        The time, in milliseconds since Jan 1 1970, when the
                        presence state was set.
                      example: 1533928483800
            V2UserPresence:
              allOf:
                - $ref: '#/definitions/V2PresenceStatus'
                - type: object
                  properties:
                    userId:
                      type: integer
                      format: int64
                      description: The ID of the user to whom the presence state relates.
                      example: 14568529068038
            V2PresenceStatus:
              type: object
              properties:
                category:
                  type: string
                  description: |
                    Presence status. Possible values are:
                      - UNDEFINED
                      - AVAILABLE
                      - BUSY
                      - DO_NOT_DISTURB
                      - ON_THE_PHONE
                      - BE_RIGHT_BACK
                      - IN_A_MEETING
                      - AWAY
                      - OUT_OF_OFFICE
                      - OFF_WORK
                      - OFFLINE
                  example: AWAY
              required:
                - category
            V2AdminStreamList:
              description: list of streams info
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  description: total number of streams which match the filter criteria
                  example: 4
                skip:
                  type: integer
                  description: number of streams skipped
                  example: 0
                limit:
                  type: integer
                  description: maximum number of streams return
                  example: 50
                filter:
                  $ref: '#/definitions/V2AdminStreamFilter'
                streams:
                  $ref: '#/definitions/V2AdminStreamInfoList'
            V2AdminStreamInfoList:
              type: array
              description: list of stream info
              items:
                $ref: '#/definitions/V2AdminStreamInfo'
              example:
                - id: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                  isExternal: false
                  isActive: true
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Active Internal Private Room
                    roomDescription: Active Internal Private Room
                    createdByUserId: 8933531975689
                    createdDate: 1481575056047
                    lastModifiedDate: 1481575056047
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 1
                    lastMessageDate: 1516699467959
                - id: _KnoYrMkhEn3H2_8vE0kl3___qb5SANQdA
                  isExternal: true
                  isActive: false
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Inactive External Room
                    roomDescription: Inactive External Room
                    createdByUserId: 8933531975686
                    createdDate: 1481876438194
                    lastModifiedDate: 1481876438194
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 2
                    lastMessageDate: 1516699467959
            V2AdminStreamInfo:
              description: Stream information
              type: object
              properties:
                id:
                  type: string
                  description: stream id
                  example: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                isExternal:
                  type: boolean
                  description: >-
                    true indicate this stream has the scope of external and
                    false indictate this stream has the scope of internal.
                    Deprecated, use origin
                  example: false
                isActive:
                  type: boolean
                  description: >-
                    true indicate that this stream has the status of active and
                    false indicate this stream has the scope of inactive
                  example: true
                isPublic:
                  type: boolean
                  description: >-
                    true indicate that this stream has a privacy setting of
                    public.  This only apply a ROOM stream type.
                  example: false
                type:
                  type: string
                  description: type of stream (IM, MIM, ROOM)
                  example: ROOM
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                attributes:
                  $ref: '#/definitions/V2AdminStreamAttributes'
            V2AdminStreamAttributes:
              description: additional optional properties for the stream
              type: object
              properties:
                roomName:
                  type: string
                  description: room name (room only)
                  example: API room
                roomDescription:
                  type: string
                  description: description of the room (room only)
                  example: Room created via API
                members:
                  type: array
                  description: list of userid who is member of the stream - im or mim only
                  items:
                    type: integer
                    format: int64
                  example:
                    - 8933531975686
                    - 8933531975689
                createdByUserId:
                  type: integer
                  format: int64
                  description: creator user id
                  example: 8933531975689
                createdDate:
                  type: integer
                  format: int64
                  description: created date
                  example: 1481575056047
                lastModifiedDate:
                  type: integer
                  format: int64
                  description: last modified date
                  example: 1481575056047
                originCompany:
                  type: string
                  description: company name of the creator
                  example: Symphony
                originCompanyId:
                  type: integer
                  description: company id of the creator
                  example: 130
                membersCount:
                  type: integer
                  description: total number of members in the stream
                  example: 1
                lastMessageDate:
                  type: integer
                  format: int64
                  description: last date a message was sent in this stream
                  example: 1516699467959
                groupChat:
                  type: boolean
                  description: whether a stream is a group chat or not. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            FileExtension:
              type: object
              required:
                - extension
              properties:
                extension:
                  type: string
                  description: >
                    The file extension that this specific record is for.  This
                    is a unique ID

                    that allows this record to be referenced in the URI.
                  example: .txt
                scope_internal:
                  type: boolean
                  description: |
                    File extension allowed for internal scope
                scope_external:
                  type: boolean
                  description: |
                    File extension allowed for external scope
                scope_xpod:
                  type: boolean
                  description: |
                    File extension allowed to be received from another POD
                  x-since: 24.2
                source:
                  type: string
                  description: >
                    File extension with metadata understood by the system or
                    file extension created by a customer
                  enum:
                    - SYSTEM
                    - CUSTOMER
            Pagination:
              type: object
              required:
                - cursors
              properties:
                cursors:
                  type: object
                  required:
                    - before
                  properties:
                    before:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        start of the page of data

                        that has been returned.
                      example: MTAxNTExOTQ1MjAwNzI5NDE=
                    after:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        end of the page of data

                        that has been returned.
                      example: NDMyNzQyODI3OTQw
                previous:
                  type: string
                  description: >
                    API endpoint that will return the previous page of data. If
                    not included, this is

                    the first page of data.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&before=MTAxNTExOTQ1MjAwNzI5NDE=
                next:
                  type: string
                  description: >
                    API endpoint that will return the next page of data. If not
                    included, this is the

                    last page of data. Due to how pagination works with
                    visibility and privacy, it is

                    possible that a page may be empty but contain a 'next'
                    paging link. Stop paging when

                    the 'next' link no longer appears.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&after=NDMyNzQyODI3OTQw
            FileExtensionsResponse:
              type: object
              required:
                - data
                - paging
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/FileExtension'
            Protocol:
              type: object
              required:
                - scheme
              properties:
                scheme:
                  type: string
                  description: 'URI protocol scheme (example: http, https, ftp)'
                  example: skype
            AppAuthenticationKeys:
              description: App RSA keys information.
              type: object
              properties:
                current:
                  $ref: '#/definitions/AppAuthenticationKey'
                previous:
                  $ref: '#/definitions/AppAuthenticationKey'
            AppAuthenticationKey:
              description: App RSA key information.
              type: object
              properties:
                key:
                  description: Application RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1700815176000
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the app's active
                    RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the app's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            AppNotification:
              type: object
              description: Application callback information
              properties:
                url:
                  type: string
                  description: callback URL
                  example: https://some.url
                apiKey:
                  type: string
                  description: >-
                    apiKey sent into every callback request, using the X-API-KEY
                    header
                  example: test123456
            AppProperties:
              type: array
              description: >-
                Application configuration properties that are shared with the
                extension application, client side. Do not store sensitive
                information here. Since SBE 20.14.
              x-since: 20.14
              items:
                $ref: '#/definitions/AppProperty'
              example:
                - key: port
                  value: 4000
                - key: url
                  value: https://someother.url
            AppProperty:
              type: object
              description: >-
                Application configuration property that is shared with the
                extension application, client side. Do not store sensitive
                information here.
              properties:
                key:
                  type: string
                  description: >-
                    Name of an application configuration property. It cannot be
                    null or empty and its length is limited to 1024 characters.
                    Keys are unique.
                value:
                  type: string
                  description: >-
                    Value of an application configuration property. It cannot be
                    null and its length is limited to 4096 characters. It can be
                    empty.
              example:
                key: port
                value: 4000
            StreamAttachmentResponse:
              type: array
              items:
                $ref: '#/definitions/StreamAttachmentItem'
            StreamAttachmentItem:
              description: File attachments for a message in a stream
              type: object
              properties:
                messageId:
                  type: string
                  example: PYLHNm/1K6p...peOpj+FbQ
                ingestionDate:
                  type: integer
                  format: int64
                  example: 1548089933946
                userId:
                  type: integer
                  format: int64
                  example: 14568529068038
                fileId:
                  type: string
                  description: The attachment File ID.
                  example: internal_14362
                name:
                  type: string
                  description: The file name.
                  example: butterfly.jpg
                size:
                  type: integer
                  format: int64
                  description: Size in bytes.
                  example: 70186
                content-type:
                  type: string
                  example: image/jpeg
                previews:
                  type: array
                  items:
                    $ref: '#/definitions/AttachmentPreview'
            AttachmentPreview:
              description: Preview file for image attachments
              type: object
              properties:
                fileId:
                  type: string
                  description: The preview file ID
                  example: internal_14362
                width:
                  type: integer
                  description: The preview image width
                  example: 600
            UserGroupCreate:
              description: Body for group creation
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
              required:
                - name
                - type
            UserGroupResponse:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group ID
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: An optional string attribute used for categorizing groups
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group status
                  type: boolean
                createdDate:
                  description: Date of group creation
                  type: integer
                  format: int64
                modifiedDate:
                  description: Date of group last update
                  type: integer
                  format: int64
                memberCount:
                  description: Number of group members
                  type: integer
                  format: int64
                assigneeCount:
                  description: Number of group assignees
                  type: integer
                  format: int64
            UserGroupResponseList:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupResponse'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupUpdate:
              description: Body for group update
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                active:
                  description: Group status
                  type: boolean
            UserGroupMembershipResponseData:
              description: User object response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            GroupRoleScope:
              description: User Group info to include in other models
              type: object
              properties:
                id:
                  type: string
                  description: Group ID
                name:
                  type: string
                  description: Group name
                area:
                  type: string
                  description: An optional string attribute used for categorizing groups
                type:
                  type: string
                  description: Group type
                active:
                  type: boolean
                  description: Group status
            UserCompp:
              description: Basic user information to include in other models
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  description: User ID
                  example: 7215545058329
                username:
                  type: string
                  description: Username
                  example: dpayet
                firstName:
                  type: string
                  description: User first name
                  example: Dimitri
                lastName:
                  type: string
                  description: User last name
                  example: Payet
                emailAddress:
                  type: string
                  description: User email addressIntegrationUserManagerTest
                  example: dpayet@om.fr
            UserGroupMembershipRequest:
              description: Body for user group membership creation
              type: object
              properties:
                active:
                  type: boolean
            UserGroupMembershipData:
              description: Body for user group membership response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                userId:
                  type: integer
                  format: int64
                group:
                  type: object
                  $ref: '#/definitions/UserGroupData'
                user:
                  type: object
                  $ref: '#/definitions/MembershipData'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            MembershipData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                userName:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupData:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group Id
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group Status
                  type: boolean
            UserGroupMembershipResponse:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupMembershipResponseData'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssignee:
              description: User group assignee object
              type: object
              properties:
                id:
                  description: Assignee id
                  type: string
                groupId:
                  type: string
                group:
                  description: Group
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                lastAddedDate:
                  description: Last added
                  type: integer
                  format: int64
                lastRemovedDate:
                  description: Last removed
                  type: integer
                  format: int64
            UserData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupAssigneeResponse:
              description: response
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupAssignee'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssigneeUpdate:
              description: Body for user group assignee update
              type: object
              properties:
                current:
                  description: Assignee status
                  type: boolean
              required:
                - current
            UserGroupMembershipUpdate:
              description: User Group membership update object
              type: object
              properties:
                active:
                  description: Group membership status
                  type: boolean
            UserGroupAssignmentResponse:
              description: User Group assignment response object
              type: object
              properties:
                id:
                  type: string
                  description: Assignment ID
                groupId:
                  type: string
                  description: Group ID
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                  description: User ID
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                  description: Group membership status
                lastAddedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last added
                lastRemovedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last removed
            DownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: Untitled Document.txt
                timestamp:
                  type: integer
                  format: int64
                  example: 1552999335740
            MessageReceiptDetail:
              description: Message receipt details response object
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserCompp'
                deliveryReceiptTimestamp:
                  description: Timestamp of message delivery receipts
                  type: integer
                  format: int64
                  example: 1552999333784
                readReceiptTimestamp:
                  description: Timestamp of message read receipts
                  type: integer
                  format: int64
                  example: 1552999335114
                emailNotificationTimestamp:
                  description: Timestamp of message email notifications
                  type: integer
                  format: int64
                  example: 1552999335114
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/DownloadReceiptCount'
                  example:
                    - fileName: Untitled Document.txt
                      timestamp: 1552999335740
            MessageReceiptDetailResponse:
              description: List of Message receipt details
              type: object
              properties:
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                  example: 1552999333141
                deliveryReceiptCount:
                  type: integer
                  example: 1
                readReceiptCount:
                  type: integer
                  example: 1
                emailNotificationCount:
                  type: integer
                  example: 1
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
                  example:
                    - fileName: internal_70781
                      count: 1
                MessageReceiptDetail:
                  type: array
                  items:
                    $ref: '#/definitions/MessageReceiptDetail'
                  example:
                    - user:
                        id: 7215545058329
                        username: dpayet
                        firstName: Dimitri
                        lastName: Payet
                        emailAddress: dpayet@om.fr
                      deliveryReceiptTimestamp: 1552999333784
                      readReceiptTimestamp: 1552999335114
                      emailNotificationTimestamp: 1552999335114
                      downloadReceiptCounts:
                        - fileName: Untitled Document.txt
                          timestamp: 1552999335740
                pagination:
                  $ref: '#/definitions/Pagination'
            MessageUser:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058329
                name:
                  type: string
                  example: User Test
            MessageStream:
              type: object
              properties:
                id:
                  type: string
                  example: lFpyw0ATFmji+Cc/cSzbk3///pZkWpe1dA==
                name:
                  type: string
                  example: Test Room
                streamType:
                  type: string
                  example: ROOM
            MessageDownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: internal_707810
                count:
                  type: integer
                  format: int64
                  example: 1
            MessageDetail:
              description: Message detail
              type: object
              properties:
                messageId:
                  description: message id
                  type: string
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                deliveryReceiptCount:
                  type: integer
                  format: int64
                readReceiptCount:
                  type: integer
                  format: int64
                emailNotificationCount:
                  type: integer
                  format: int64
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
            MessageDetails:
              description: Message details
              type: array
              items:
                $ref: '#/definitions/MessageDetail'
            MessageIds:
              type: object
              properties:
                messageIds:
                  $ref: '#/definitions/StringList'
            AssigneeCandidate:
              description: Assignee Candidate
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                surname:
                  type: string
                emailAddress:
                  type: string
                canBeAssigned:
                  type: boolean
                roles:
                  $ref: '#/definitions/StringList'
            AssigneeCandidates:
              description: List of assignee candidate
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/AssigneeCandidate'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            Languages:
              description: List of languages
              type: object
              properties:
                languages:
                  $ref: '#/definitions/StringList'
            MessageMetadataResponse:
              description: Message metadata
              type: object
              properties:
                messageId:
                  type: string
                parent:
                  type: object
                  properties:
                    messageId:
                      type: string
                      description: Id of the parent message queried
                    relationshipType:
                      type: string
                      enum:
                        - REPLY_FORM
                        - REPLY
                        - FORWARD
                replies:
                  type: array
                  items:
                    type: string
                forwards:
                  type: array
                  items:
                    type: string
                formReplies:
                  type: array
                  items:
                    type: string
            UserSuspension:
              type: object
              properties:
                suspended:
                  type: boolean
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  example: 1601546400
                suspensionReason:
                  type: string
                  example: The user will be OOO due to a mandatory leave
            FollowersList:
              type: object
              properties:
                followers:
                  $ref: '#/definitions/UserIdList'
            FollowersListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                followers:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            FollowingListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                following:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            V1IMAttributes:
              type: object
              properties:
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the IM. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
            V1IMDetail:
              type: object
              properties:
                V1IMAttributes:
                  $ref: '#/definitions/V1IMAttributes'
                IMSystemInfo:
                  $ref: '#/definitions/IMSystemInfo'
            IMSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: usnBKBkH_BVrGOiVpaupEH___okFfE7QdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1610520703317
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ServiceAccountManifest:
              type: object
              properties:
                manifest:
                  type: string
                  maxLength: 6144
                  description: >-
                    Manifest containing commands supported by the service
                    account. Must be valid JSON.
              required:
                - nu
    aid: symphony:symphony-pod-api
    overlays:
      - type: APIs.io Search
        url: overlays/pod-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---