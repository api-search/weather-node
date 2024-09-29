---
name: Alexa
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alexa.png
url: https://example.com/apis/alexa.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alexa
apis:
  - name: chime-sdk-voice
    description: >-
      <p>The Amazon Chime SDK telephony APIs in this section enable developers
      to create PSTN calling solutions that use Amazon Chime SDK Voice
      Connectors, and Amazon Chime SDK SIP media applications. Developers can
      also order and manage phone numbers, create and manage Voice Connectors
      and SIP media applications, and run voice analytics.</p>
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
            title: chime-sdk-voice
          paths:
            /voice-connectors/{voiceConnectorId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnector
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  SDK Voice Connector.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
            /voice-connector-groups/{voiceConnectorGroupId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnectorGroup
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  SDK Voice Connector group.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
            /phone-numbers?operation=batch-delete:
              POST:
                summary: BatchDeletePhoneNumber
                description: >-
                  <p> Moves phone numbers into the <b>Deletion queue</b>. Phone
                  numbers must be disassociated from any users or Amazon Chime
                  SDK Voice Connectors before they can be deleted. </p> <p>
                  Phone numbers remain in the <b>Deletion queue</b> for 7 days
                  before they are deleted permanently. </p>
                tags:
                  - Batches
                  - Delete
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
            /phone-numbers?operation=batch-update:
              POST:
                summary: BatchUpdatePhoneNumber
                description: <p>Updates one or more phone numbers.</p>
                tags:
                  - Batches
                  - Update
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
            /phone-number-orders:
              GET:
                summary: ListPhoneNumberOrders
                description: >-
                  <p>Lists the phone numbers for an administrator's Amazon Chime
                  SDK account.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Orders
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
            /voice-connectors/{voiceConnectorId}/proxy-sessions:
              GET:
                summary: ListProxySessions
                description: >-
                  <p>Lists the proxy sessions for the specified Amazon Chime SDK
                  Voice Connector.</p>
                tags:
                  - Lists
                  - Proxy
                  - Sessions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
            /sip-media-applications:
              GET:
                summary: ListSipMediaApplications
                description: >-
                  <p>Lists the SIP media applications under the administrator's
                  AWS account.</p>
                tags:
                  - Lists
                  - SIP
                  - Media
                  - Applications
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
            /sip-media-applications/{sipMediaApplicationId}/calls:
              POST:
                summary: CreateSipMediaApplicationCall
                description: >-
                  <p>Creates an outbound call to a phone number from the phone
                  number specified in the request, and it invokes the endpoint
                  of the specified <code>sipMediaApplicationId</code>.</p>
                tags:
                  - Create
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
            /sip-rules:
              GET:
                summary: ListSipRules
                description: >-
                  <p>Lists the SIP rules under the administrator's AWS
                  account.</p>
                tags:
                  - Lists
                  - SIP
                  - Rules
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
            /voice-connectors:
              GET:
                summary: ListVoiceConnectors
                description: >-
                  <p>Lists the Amazon Chime SDK Voice Connectors in the
                  administrators AWS account.</p>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
            /voice-connector-groups:
              GET:
                summary: ListVoiceConnectorGroups
                description: >-
                  <p>Lists the Amazon Chime SDK Voice Connector groups in the
                  administrator's AWS account.</p>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Groups
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
            /voice-profiles:
              GET:
                summary: ListVoiceProfiles
                description: <p>Lists the voice profiles in a voice profile domain.</p>
                tags:
                  - Lists
                  - Voice
                  - Profiles
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
            /voice-profile-domains:
              GET:
                summary: ListVoiceProfileDomains
                description: >-
                  <p>Lists the specified voice profile domains in the
                  administrator's AWS account. </p>
                tags:
                  - Lists
                  - Voice
                  - Profiles
                  - Domains
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
            /phone-numbers/{phoneNumberId}:
              POST:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates phone number details, such as product type or
                  calling name, for the specified phone number ID. You can
                  update one phone number detail at a time. For example, you can
                  update either the product type or the calling name in one
                  action.</p> <p>For numbers outside the U.S., you must use the
                  Amazon Chime SDK SIP Media Application Dial-In product
                  type.</p> <p>Updates to outbound calling names can take 72
                  hours to complete. Pending updates to outbound calling names
                  must be complete before you can request another update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
            /voice-connectors/{voiceConnectorId}/proxy-sessions/{proxySessionId}:
              POST:
                summary: UpdateProxySession
                description: >-
                  <p>Updates the specified proxy session details, such as voice
                  or SMS capabilities.</p>
                tags:
                  - Update
                  - Proxy
                  - Sessions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
            /sip-media-applications/{sipMediaApplicationId}:
              PUT:
                summary: UpdateSipMediaApplication
                description: >-
                  <p>Updates the details of the specified SIP media
                  application.</p>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
            /sip-rules/{sipRuleId}:
              PUT:
                summary: UpdateSipRule
                description: <p>Updates the details of the specified SIP rule.</p>
                tags:
                  - Update
                  - SIP
                  - Rules
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}:
              PUT:
                summary: UpdateVoiceConnector
                description: >-
                  <p>Updates the details for the specified Amazon Chime SDK
                  Voice Connector.</p>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}/emergency-calling-configuration:
              PUT:
                summary: PutVoiceConnectorEmergencyCallingConfiguration
                description: >-
                  <p>Updates a Voice Connector's emergency calling
                  configuration.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Emergency
                  - Calling
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
            /voice-connector-groups/{voiceConnectorGroupId}:
              PUT:
                summary: UpdateVoiceConnectorGroup
                description: >-
                  <p>Updates the settings for the specified Amazon Chime SDK
                  Voice Connector group.</p>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
            /voice-connectors/{voiceConnectorId}/origination:
              PUT:
                summary: PutVoiceConnectorOrigination
                description: <p>Updates a Voice Connector's origination settings.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Origination
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
            /voice-connectors/{voiceConnectorId}/programmable-numbers/proxy:
              PUT:
                summary: PutVoiceConnectorProxy
                description: >-
                  <p>Puts the specified proxy configuration to the specified
                  Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Proxy
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/streaming-configuration:
              PUT:
                summary: PutVoiceConnectorStreamingConfiguration
                description: >-
                  <p>Updates a Voice Connector's streaming configuration
                  settings.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Streaming
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
            /voice-connectors/{voiceConnectorId}/termination:
              PUT:
                summary: PutVoiceConnectorTermination
                description: <p>Updates a Voice Connector's termination settings.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=delete:
              POST:
                summary: DeleteVoiceConnectorTerminationCredentials
                description: >-
                  <p>Deletes the specified SIP credentials used by your
                  equipment to authenticate during call termination.</p>
                tags:
                  - Delete
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
            /voice-profiles/{VoiceProfileId}:
              PUT:
                summary: UpdateVoiceProfile
                description: >-
                  <p>Updates the specified voice profile’s voice print and
                  refreshes its expiration timestamp.</p> <important> <p>As a
                  condition of using this feature, you acknowledge that the
                  collection, use, storage, and retention of your caller’s
                  biometric identifiers and biometric information (“biometric
                  data”) in the form of a digital voiceprint requires the
                  caller’s informed consent via a written release. Such consent
                  is required under various state laws, including biometrics
                  laws in Illinois, Texas, Washington and other state privacy
                  laws.</p> <p>You must provide a written release to each caller
                  through a process that clearly reflects each caller’s informed
                  consent before using Amazon Chime SDK Voice Insights service,
                  as required under the terms of your agreement with AWS
                  governing your use of the service.</p> </important>
                tags:
                  - Update
                  - Voice
                  - Profiles
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
            /voice-profile-domains/{VoiceProfileDomainId}:
              PUT:
                summary: UpdateVoiceProfileDomain
                description: >-
                  <p>Updates the settings for the specified voice profile
                  domain.</p>
                tags:
                  - Update
                  - Voice
                  - Profiles
                  - Domains
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
            /voice-connectors/{voiceConnectorId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnector
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
            /voice-connector-groups/{voiceConnectorGroupId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnectorGroup
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime SDK Voice Connector group.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
            /settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates global settings for the Amazon Chime SDK Voice
                  Connectors in an AWS account.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
            /phone-number-orders/{phoneNumberOrderId}:
              GET:
                summary: GetPhoneNumberOrder
                description: >-
                  <p>Retrieves details for the specified phone number order,
                  such as the order creation timestamp, phone numbers in E.164
                  format, product type, and order status.</p>
                tags:
                  - Get
                  - Phone
                  - Numbers
                  - Orders
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
            /settings/phone-number:
              PUT:
                summary: UpdatePhoneNumberSettings
                description: >-
                  <p>Updates the phone number settings for the administrator's
                  AWS account, such as the default outbound calling name. You
                  can update the default outbound calling name once every seven
                  days. Outbound calling names can take up to 72 hours to
                  update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Settings
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
            /sip-media-applications/{sipMediaApplicationId}/alexa-skill-configuration:
              PUT:
                summary: PutSipMediaApplicationAlexaSkillConfiguration
                description: >-
                  <p>Updates the Alexa Skill configuration for the SIP media
                  application.</p>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Alexa
                  - Skills
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
            /sip-media-applications/{sipMediaApplicationId}/logging-configuration:
              PUT:
                summary: PutSipMediaApplicationLoggingConfiguration
                description: >-
                  <p>Updates the logging configuration for the specified SIP
                  media application.</p>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Logging
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks/{SpeakerSearchTaskId}:
              GET:
                summary: GetSpeakerSearchTask
                description: >-
                  <p>Retrieves the details of the specified speaker search
                  task.</p>
                tags:
                  - Get
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
            /voice-connectors/{voiceConnectorId}/logging-configuration:
              PUT:
                summary: PutVoiceConnectorLoggingConfiguration
                description: <p>Updates a Voice Connector's logging configuration.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Logging
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
            /voice-connectors/{voiceConnectorId}/termination/health:
              GET:
                summary: GetVoiceConnectorTerminationHealth
                description: >-
                  <p>Retrieves information about the last time a <code>SIP
                  OPTIONS</code> ping was received from your SIP infrastructure
                  for the specified Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Get
                  - Voice
                  - Connectors
                  - Termination
                  - Health
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks/{VoiceToneAnalysisTaskId}:
              GET:
                summary: GetVoiceToneAnalysisTask
                description: <p>Retrieves the details of a voice tone analysis task.</p>
                tags:
                  - Get
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
            /voice-connector-regions:
              GET:
                summary: ListAvailableVoiceConnectorRegions
                description: >-
                  <p>Lists the available AWS Regions in which you can create an
                  Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Lists
                  - Available
                  - Voice
                  - Connectors
                  - Regions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
            /phone-numbers:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Lists the phone numbers for the specified Amazon Chime SDK
                  account, Amazon Chime SDK user, Amazon Chime SDK Voice
                  Connector, or Amazon Chime SDK Voice Connector group.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
            /phone-number-countries:
              GET:
                summary: ListSupportedPhoneNumberCountries
                description: >-
                  <p>Lists the countries that you can order phone numbers
                  from.</p>
                tags:
                  - Lists
                  - Supported
                  - Phone
                  - Numbers
                  - Countries
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
            /tags:
              GET:
                summary: ListTagsForResource
                description: <p>Returns a list of the tags in a given resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
            /voice-connectors/{voiceConnectorId}/termination/credentials:
              GET:
                summary: ListVoiceConnectorTerminationCredentials
                description: >-
                  <p>Lists the SIP credentials for the specified Amazon Chime
                  SDK Voice Connector.</p>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=put:
              POST:
                summary: PutVoiceConnectorTerminationCredentials
                description: <p>Updates a Voice Connector's termination credentials.</p>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
            /phone-numbers/{phoneNumberId}?operation=restore:
              POST:
                summary: RestorePhoneNumber
                description: <p>Restores a deleted phone number.</p>
                tags:
                  - Restore
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
            /search?type=phone-numbers:
              GET:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches the provisioned phone numbers in an
                  organization.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks:
              POST:
                summary: StartSpeakerSearchTask
                description: >-
                  <p>Starts a speaker search task.</p> <important> <p>Before
                  starting any speaker search tasks, you must provide all
                  notices and obtain all consents from the speaker as required
                  under applicable privacy and biometrics laws, and as required
                  under the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks:
              POST:
                summary: StartVoiceToneAnalysisTask
                description: >-
                  <p>Starts a voice tone analysis task. For more information
                  about voice tone analysis, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/pstn-voice-analytics.html">Using
                  Amazon Chime SDK voice analytics</a> in the <i>Amazon Chime
                  SDK Developer Guide</i>.</p> <important> <p>Before starting
                  any voice tone analysis tasks, you must provide all notices
                  and obtain all consents from the speaker as required under
                  applicable privacy and biometrics laws, and as required under
                  the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks/{SpeakerSearchTaskId}?operation=stop:
              POST:
                summary: StopSpeakerSearchTask
                description: <p>Stops a speaker search task.</p>
                tags:
                  - Stop
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks/{VoiceToneAnalysisTaskId}?operation=stop:
              POST:
                summary: StopVoiceToneAnalysisTask
                description: <p>Stops a voice tone analysis task.</p>
                tags:
                  - Stop
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: <p>Adds a tag to the specified resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
            /sip-media-applications/{sipMediaApplicationId}/calls/{transactionId}:
              POST:
                summary: UpdateSipMediaApplicationCall
                description: >-
                  <p>Invokes the AWS Lambda function associated with the SIP
                  media application and transaction ID in an update request. The
                  Lambda function can then return a new set of actions.</p>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - Transactions
            /emergency-calling/address:
              POST:
                summary: ValidateE911Address
                description: >-
                  <p>Validates an address to be used for 911 calls made with
                  Amazon Chime SDK Voice Connectors. You can use validated
                  addresses in a Presence Information Data Format Location
                  Object file that you include in SIP requests. That helps
                  ensure that addresses are routed to the appropriate Public
                  Safety Answering 
                tags:
                  - Validate
                  - E911
                  - Addresses
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Voice
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - Transactions
                  - Addresses''
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-voice-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-voice-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-voice
  - name: kinesis-video-signaling
    description: >-
      <p>Kinesis Video Streams Signaling Service is a intermediate service that
      establishes a communication channel for discovering peers, transmitting
      offers and answers in order to establish peer-to-peer connection in webRTC
      technology.</p>
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
            title: kinesis-video-signaling
          paths:
            /v1/get-ice-server-config:
              POST:
                summary: GetIceServerConfig
                description: >-
                  <p>Gets the Interactive Connectivity Establishment (ICE)
                  server configuration information, including URIs, username,
                  and password which can be used to configure the WebRTC
                  connection. The ICE component uses this configuration
                  information to setup the WebRTC connection, including
                  authenticating with the Traversal Using Relays around NAT
                  (TURN) relay server. </p> <p>TURN is a protocol that is used
                  to improve the connectivity of peer-to-peer applications. By
                  providing a cloud-based relay service, TURN ensures that a
                  connection can be established even when one or more peers are
                  incapable of a direct peer-to-peer connection. For more
                  information, see <a
                  href="https://tools.ietf.org/html/draft-uberti-rtcweb-turn-rest-00">A
                  REST API For Access To TURN Services</a>.</p> <p> You can
                  invoke this API to establish a fallback mechanism in case
                  either of the peers is unable to establish a direct
                  peer-to-peer connection over a signaling channel. You must
                  specify either a signaling channel ARN or the client ID in
                  order to invoke this API.</p>
                tags:
                  - Get
                  - Ice
                  - Server
                  - Configurations
                  - V1
                  - Get
                  - Ice
                  - Server
                  - Configurations
            /v1/send-alexa-offer-to-master:
              POST:
                summary: SendAlexaOfferToMaster
                description: >-
                  <p>This API allows you to connect WebRTC-enabled devices with
                  Alexa display devices. When invoked, it sends the Alexa
                  Session Description Protocol (SDP) offer to the master peer.
                  The offer is delivered as soon as the master is connected to
                  the specified signaling channel. This API returns the SDP
                  answer from the connected master. If the master is not
                  connected to the signaling channel, redelivery requests are
                  made until the message ex
                tags:
                  - Send
                  - Alexa
                  - Offers
                  - To
                  - Master
                  - V1
                  - Get
                  - Ice
                  - Server
                  - Configurations
                  - Send
                  - Alexa
                  - Offers
                  - To
                  - Mast
    overlays:
      - type: APIs.io Search
        url: overlays/kinesis-video-signaling-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kinesis-video-signaling-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kinesis-video-signaling
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---