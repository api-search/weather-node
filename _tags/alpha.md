---
name: Alpha
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alpha.png
url: https://example.com/apis/alpha.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alpha
apis:
  - aid: twilio:twilio-messaging-api
    name: Twilio Messaging API
    description: >-
      Send and receive messages via SMS, MMS, WhatsApp, Facebook Messenger, and
      more through our Messaging and Conversations APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/en-us/ahoy
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/en-us/messaging
      - type: Pricing
        url: https://www.twilio.com/en-us/sms/pricing/us
      - type: OpenAPI
        data:
          info:
            title: Twilio - Messaging
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Services/{ServiceSid}/AlphaSenders:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/Services/{ServiceSid}/AlphaSenders/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/a2p/BrandRegistrations/{BrandRegistrationSid}/SmsOtp:
              description: >-
                A Messaging Service resource to retry OTP verification for Sole
                Proprietor Brand Registrations.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{Sid}:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings:
              description: A Messaging Service resource to add and get Brand Vettings.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings/{BrandVettingSid}:
              description: A Messaging Service resource to add and get Brand Vettings.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
            /v1/Services/{MessagingServiceSid}/ChannelSenders:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Services/{MessagingServiceSid}/ChannelSenders/{Sid}:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Deactivations:
              description: >-
                A Deactivation resource to retrieve a list of United States
                phone numbers that have been deactivated by mobile carriers on a
                specific date.
              get:
                description: >-
                  Fetch a list of all United States numbers that have been
                  deactivated on a specific date.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
            /v1/LinkShortening/Domains/{DomainSid}/Certificate:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
            /v1/LinkShortening/Domains/{DomainSid}/Config:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/LinkShortening/MessagingService/{MessagingServiceSid}/DomainConfig:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/Services/PreregisteredUsa2p:
              description: >-
                Resource to associate preregistered campaign with Messaging
                Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/Domains/{DomainSid}/MessagingServices/{MessagingServiceSid}:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/MessagingServices/{MessagingServiceSid}/Domain:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/Services/{ServiceSid}/PhoneNumbers:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/PhoneNumbers/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{Sid}:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/ShortCodes:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Services/{ServiceSid}/ShortCodes/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Tollfree/Verifications/{Sid}:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Tollfree/Verifications:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/{Sid}:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/Usecases:
              description: >-
                Messaging Service Use Case resource. Fetch possible use cases
                for service. The Use Cases API returns an empty list if there is
                an issue with the customer's A2P brand registration. This Brand
                cannot register any campaign use cases. Customers are requested
                to contact support with their A2P brand information.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
            /v1/Services/Usecases:
              description: >-
                Use Case resource. Fetch possible use cases for a Messaging
                Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
          tags:
            - name: MessagingV1AlphaSender
            - name: MessagingV1BrandRegistration
            - name: MessagingV1BrandRegistrationOtp
            - name: MessagingV1BrandVetting
            - name: MessagingV1ChannelSender
            - name: MessagingV1Deactivations
            - name: MessagingV1DomainCerts
            - name: MessagingV1DomainConfig
            - name: MessagingV1DomainConfigMessagingService
            - name: MessagingV1ExternalCampaign
            - name: MessagingV1LinkshorteningMessagingService
            - name: MessagingV1LinkshorteningMessagingServiceDomainAssociation
            - name: MessagingV1PhoneNumber
            - name: MessagingV1Service
            - name: MessagingV1ShortCode
            - name: MessagingV1TollfreeVerification
            - name: MessagingV1UsAppToPerson
            - name: MessagingV1UsAppToPersonUsecase
            - name: MessagingV1Usecase
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/messaging-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/messaging-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---