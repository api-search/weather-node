---
name: Browser
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/browser.png
url: https://example.com/apis/browser.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Browser
apis:
  - name: workspaces-web
    description: >-
      <p>WorkSpaces Web is a low cost, fully managed WorkSpace built
      specifically to facilitate secure, web-based workloads. WorkSpaces Web
      makes it easy for customers to safely provide their employees with access
      to internal websites and SaaS web applications without the administrative
      burden of appliances or specialized client software. WorkSpaces Web
      provides simple policy tools tailored for user interactions, while
      offloading common tasks like capacity management, scaling, and maintaining
      browser images.</p>
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
            title: workspaces-web
          paths:
            /portals/{portalArn+}/browserSettings:
              DELETE:
                summary: DisassociateBrowserSettings
                description: <p>Disassociates browser settings from a web portal.</p>
                tags:
                  - Disassociate
                  - Browser
                  - Settings
                  - ARN
                  - Browser
                  - Settings
            /portals/{portalArn+}/ipAccessSettings:
              DELETE:
                summary: DisassociateIpAccessSettings
                description: <p>Disassociates IP access settings from a web portal.</p>
                tags:
                  - Disassociate
                  - IP
                  - Access
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
            /portals/{portalArn+}/networkSettings:
              DELETE:
                summary: DisassociateNetworkSettings
                description: <p>Disassociates network settings from a web portal.</p>
                tags:
                  - Disassociate
                  - Networks
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
            /portals/{portalArn+}/trustStores:
              DELETE:
                summary: DisassociateTrustStore
                description: <p>Disassociates a trust store from a web portal.</p>
                tags:
                  - Disassociate
                  - Trust
                  - Store
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
            /portals/{portalArn+}/userAccessLoggingSettings:
              DELETE:
                summary: DisassociateUserAccessLoggingSettings
                description: >-
                  <p>Disassociates user access logging settings from a web
                  portal.</p>
                tags:
                  - Disassociate
                  - Users
                  - Access
                  - Logging
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
            /portals/{portalArn+}/userSettings:
              DELETE:
                summary: DisassociateUserSettings
                description: <p>Disassociates user settings from a web portal.</p>
                tags:
                  - Disassociate
                  - Users
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
            /browserSettings:
              GET:
                summary: ListBrowserSettings
                description: <p>Retrieves a list of browser settings.</p>
                tags:
                  - Lists
                  - Browser
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
            /identityProviders:
              POST:
                summary: CreateIdentityProvider
                description: >-
                  <p>Creates an identity provider resource that is then
                  associated with a web portal.</p>
                tags:
                  - Create
                  - Identity
                  - Providers
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
            /ipAccessSettings:
              GET:
                summary: ListIpAccessSettings
                description: <p>Retrieves a list of IP access settings.</p>
                tags:
                  - Lists
                  - IP
                  - Access
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
            /networkSettings:
              GET:
                summary: ListNetworkSettings
                description: <p>Retrieves a list of network settings.</p>
                tags:
                  - Lists
                  - Networks
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
            /portals:
              GET:
                summary: ListPortals
                description: <p>Retrieves a list or web portals.</p>
                tags:
                  - Lists
                  - Portals
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
            /trustStores:
              GET:
                summary: ListTrustStores
                description: <p>Retrieves a list of trust stores.</p>
                tags:
                  - Lists
                  - Trust
                  - Stores
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
            /userAccessLoggingSettings:
              GET:
                summary: ListUserAccessLoggingSettings
                description: <p>Retrieves a list of user access logging settings.</p>
                tags:
                  - Lists
                  - Users
                  - Access
                  - Logging
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
            /userSettings:
              GET:
                summary: ListUserSettings
                description: <p>Retrieves a list of user settings.</p>
                tags:
                  - Lists
                  - Users
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
            /browserSettings/{browserSettingsArn+}:
              PATCH:
                summary: UpdateBrowserSettings
                description: <p>Updates browser settings.</p>
                tags:
                  - Update
                  - Browser
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
            /identityProviders/{identityProviderArn+}:
              PATCH:
                summary: UpdateIdentityProvider
                description: <p>Updates the identity provider. </p>
                tags:
                  - Update
                  - Identity
                  - Providers
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
            /ipAccessSettings/{ipAccessSettingsArn+}:
              PATCH:
                summary: UpdateIpAccessSettings
                description: <p>Updates IP access settings.</p>
                tags:
                  - Update
                  - IP
                  - Access
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
            /networkSettings/{networkSettingsArn+}:
              PATCH:
                summary: UpdateNetworkSettings
                description: <p>Updates network settings.</p>
                tags:
                  - Update
                  - Networks
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
            /portals/{portalArn+}:
              PUT:
                summary: UpdatePortal
                description: <p>Updates a web portal.</p>
                tags:
                  - Update
                  - Portals
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
            /trustStores/{trustStoreArn+}:
              PATCH:
                summary: UpdateTrustStore
                description: <p>Updates the trust store.</p>
                tags:
                  - Update
                  - Trust
                  - Store
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
            /userAccessLoggingSettings/{userAccessLoggingSettingsArn+}:
              PATCH:
                summary: UpdateUserAccessLoggingSettings
                description: <p>Updates the user access logging settings.</p>
                tags:
                  - Update
                  - Users
                  - Access
                  - Logging
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
            /userSettings/{userSettingsArn+}:
              PATCH:
                summary: UpdateUserSettings
                description: <p>Updates the user settings.</p>
                tags:
                  - Update
                  - Users
                  - Settings
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
            /portalIdp/{portalArn+}:
              GET:
                summary: GetPortalServiceProviderMetadata
                description: <p>Gets the service provider metadata.</p>
                tags:
                  - Get
                  - Portals
                  - Services
                  - Providers
                  - Metadata
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
                  - Idp
                  - Portals
            /trustStores/{trustStoreArn+}/certificate:
              GET:
                summary: GetTrustStoreCertificate
                description: <p>Gets the trust store certificate.</p>
                tags:
                  - Get
                  - Trust
                  - Store
                  - Certificates
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
                  - Idp
                  - Portals
                  - Certificates
            /portals/{portalArn+}/identityProviders:
              GET:
                summary: ListIdentityProviders
                description: >-
                  <p>Retrieves a list of identity providers for a specific web
                  portal.</p>
                tags:
                  - Lists
                  - Identity
                  - Providers
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
                  - Idp
                  - Portals
                  - Certificates
            /tags/{resourceArn+}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
                  - Idp
                  - Portals
                  - Certificates
            /trustStores/{trustStoreArn+}/certificates:
              GET:
                summary: ListTrustStoreCertificates
                description: <p>Retrieves a list of trust store certifi
                tags:
                  - Lists
                  - Trust
                  - Store
                  - Certificates
                  - ARN
                  - Browser
                  - Settings
                  - IP
                  - Access
                  - Networks
                  - Trust
                  - Stores
                  - Users
                  - Logging
                  - Providers
                  - Portals
                  - Identity
                  - Providers
                  - Store
                  - Idp
                  - Portals
                  - Certificates
                  - Certificates
    overlays:
      - type: APIs.io Search
        url: overlays/workspaces-web-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workspaces-web-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workspaces-web
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---