---
name: Behalf
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/behalf.png
url: https://example.com/apis/behalf.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Behalf
apis:
  - name: Symphony Login API
    description: >-
      Programmatically manage your portfolio lifecycle from creation and update
      to scheduling reports with full control over visibility and sharing.
      Automate your portfolio workflow using our APIs — leaving you to focus on
      the alpha driving decisions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://symphony-1.gitbook.io/restapi
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://symphony-1.gitbook.io/restapi
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Login API
          paths:
            /pubkey/authenticate:
              post:
                summary: Authenticate with public key
                description: >
                  Based on an authentication request token signed by the
                  caller's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid user,

                  malformed authentication token, user's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
            /v1/pubkey/app/authenticate/extensionApp:
              post:
                summary: Authenticate extension app with public key
                description: >
                  Based on an authentication request token signed by the
                  caller's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid user,

                  malformed authentication token, user's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - Extension
                  - App
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
                  - App
            /pubkey/app/authenticate:
              post:
                summary: Authenticate an App with public key
                description: >
                  Based on an authentication request token signed by the
                  application's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid app,

                  malformed authentication token, app's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - An
                  - App
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
                  - App
            /pubkey/app/username/{username}/authenticate:
              post:
                summary: >-
                  Authenticate an application in a delegated context to act on
                  behalf of a user
                tags:
                  - Authenticate
                  - An
                  - Application
                  - In
                  - Delegated
                  - Context
                  - To
                  - Act
                  - 'On'
                  - Behalf
                  - Of
                  - User
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
            /pubkey/app/user/{userId}/authenticate:
              post:
                summary: >-
                  Authenticate an application in a delegated context to act on
                  behalf of a user
                tags:
                  - Authenticate
                  - An
                  - Application
                  - In
                  - Delegated
                  - Context
                  - To
                  - Act
                  - 'On'
                  - Behalf
                  - Of
                  - User
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
            /idm/tokens:
              post:
                summary: >-
                  Returns a valid OAuth2 access token from a given session token
                  to be used for authentication
                tags:
                  - Returns
                  - Valid
                  - Auth2
                  - Access
                  - Token
                  - From
                  - Given
                  - Session
                  - To
                  - Be
                  - Used
                  - For
                  - Authentication
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
                  - Idm
                  - Tokens
            /idm/keys:
              get:
                summary: Returns the Common Access Token (JWT) public keys as a JWKS.
                description: >-
                  This is a public endpoint, no authentication is required. The
                  JWKS can be used to verify JWT issued by the idm/tokens
                  endpoint. Since SBE 20.14.
                tags:
                  - Returns
                  - The
                  - Common
                  - Access
                  - Token
                  - T)
                  - Public
                  - Keys
                  - As
                  - S.
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
                  - Idm
                  - Tokens
                  - Keys
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                message:
                  type: string
            Token:
              type: object
              properties:
                name:
                  description: >
                    The name of the header in which the token should be
                    presented on subsequent API calls.
                  type: string
                token:
                  type: string
                  description: >
                    Authentication token that should be passed as header in each
                    API rest calls.

                    This should be considered opaque data by the client. It is
                    not intended to contain any data interpretable by the

                    client. The format is secret and subject to change without
                    notice.
                authorizationToken:
                  type: string
                  description: >
                    (Beta) Short lived access token built from a user session.
                    This field is still on Beta, please continue using 

                    the returned "token" instead.
            AuthenticateRequest:
              type: object
              description: Request body for pubkey authentication
              properties:
                token:
                  type: string
                  description: >-
                    a JWT containing the caller's username or application
                    appGroupId and an expiration date, signed by the caller's
                    private key.
            AuthenticateExtensionAppRequest:
              type: object
              description: Request body for extension app authentication
              properties:
                appToken:
                  type: string
                  description: application generated token
                authToken:
                  type: string
                  description: >-
                    a JWT containing the caller's username and an expiration
                    date, signed by the caller's private key.
            ExtensionAppTokens:
              type: object
              properties:
                appId:
                  description: Application ID
                  type: string
                appToken:
                  description: >
                    This token generated by the application when calling
                    authentication endpoint
                  type: string
                symphonyToken:
                  type: string
                  description: >
                    This token generated by Symphony and should be used by the
                    application to verify that it's talking to Symphony.
                expireAt:
                  type: integer
                  format: int64
                  description: unix timestamp when the token expired
            JwtToken:
              type: object
              properties:
                token_type:
                  type: string
                  description: Type of token, string "Bearer"
                expires_in:
                  type: integer
                  format: int64
                  description: Duration of time the access token is granted for in seconds
                access_token:
                  type: string
                  description: >
                    A JWT containing the caller's username or application, an
                    expiration date and a set of entitlements related to the

                    specified scope, signed by the caller's private key.
            Jwks:
              type: object
              properties:
                keys:
                  type: array
                  items:
                    $ref: '#/definitions/JwksEntry'
            JwksEntry:
              type: object
              description: >-
                A JWK object as defined in
                https://datatracker.ietf.org/doc/html/rfc7517#section-4.
              additionalProperties:
                type: null
    aid: symphony:symphony-login-api
    overlays:
      - type: APIs.io Search
        url: overlays/login-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---