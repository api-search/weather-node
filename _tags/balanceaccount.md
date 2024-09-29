---
name: Balanceaccount
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/balanceaccount.png
url: https://example.com/apis/balanceaccount.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Balanceaccount
apis:
  - name: Adyen Configuration Webhooks API
    description: >-
      Adyen sends webhooks to inform your system about events that occur in your
      platform. These events include, for example, when an account holders
      capabilities are updated, or when a sweep configuration is created or
      updated. When an event occurs, Adyen makes an HTTP POST request to a URL
      on your server and includes the details of the event in the request body.
      You can use these webhooks to build your implementation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/balanceplatform-webhooks/1/overview
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/api-explorer/balanceplatform-webhooks/1/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Configuration webhooks
          tags:
            - name: Account holder
            - name: Balance Accounts
            - name: Payment instrument
            - name: Card Orders
          x-staticResponse: response.json
          webhooks:
            balancePlatform.accountHolder.created:
              post:
                tags:
                  - Account holder
                summary: Account holder created
                description: >-
                  Adyen sends this webhook when you successfully [create an
                  account
                  holder](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/accountHolders).
                operationId: post-balancePlatform.accountHolder.created
                x-sortIndex: 1
                x-methodName: accountHolderCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-accountHolder-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.created-balancePlatform-accountHolder-created
                        balancePlatform-accountHolder-created-lem-v3:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.created-balancePlatform-accountHolder-created-lem-v3
                      schema:
                        $ref: '#/components/schemas/AccountHolderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-accountHolder-created:
                            $ref: '#/components/examples/WebhookAck'
                          balancePlatform-accountHolder-created-lem-v3:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.accountHolder.updated:
              post:
                tags:
                  - Account holder
                summary: Account holder updated
                description: >-
                  Adyen sends this webhook when you successfully [update an
                  account
                  holder](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/accountHolders/_id_).
                operationId: post-balancePlatform.accountHolder.updated
                x-sortIndex: 2
                x-methodName: accountHolderUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-accountHolder-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.updated-balancePlatform-accountHolder-updated
                        balancePlatform-accountHolder-updated-lem-v3:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.updated-balancePlatform-accountHolder-updated-lem-v3
                      schema:
                        $ref: '#/components/schemas/AccountHolderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-accountHolder-updated:
                            $ref: '#/components/examples/WebhookAck'
                          balancePlatform-accountHolder-updated-lem-v3:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccount.created:
              post:
                tags:
                  - Balance account
                summary: Balance account created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  balance
                  account](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/balanceAccounts).
                operationId: post-balancePlatform.balanceAccount.created
                x-sortIndex: 1
                x-methodName: balanceAccountCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-balanceAccount-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccount.created-balancePlatform-balanceAccount-created
                      schema:
                        $ref: '#/components/schemas/BalanceAccountNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-balanceAccount-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccount.updated:
              post:
                tags:
                  - Balance account
                summary: Balance account updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  balance
                  account](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/balanceAccounts/_id_).
                operationId: post-balancePlatform.balanceAccount.updated
                x-sortIndex: 2
                x-methodName: balanceAccountUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-balanceAccount-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccount.updated-balancePlatform-balanceAccount-updated
                      schema:
                        $ref: '#/components/schemas/BalanceAccountNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-balanceAccount-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.created:
              post:
                tags:
                  - Balance account
                summary: Sweep created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/balanceAccounts/_balanceAccountId_/sweeps).
                operationId: post-balancePlatform.balanceAccountSweep.created
                x-sortIndex: 3
                x-methodName: sweepCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.created-balancePlatform-sweep-created
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.deleted:
              post:
                tags:
                  - Balance account
                summary: Sweep deleted
                description: >-
                  Adyen sends this webhook when you successfully [delete a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/delete/balanceAccounts/_balanceAccountId_/sweeps/_sweepId_).
                operationId: post-balancePlatform.balanceAccountSweep.deleted
                x-sortIndex: 5
                x-methodName: sweepDeleted
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-deleted:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.deleted-balancePlatform-sweep-deleted
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-deleted:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.updated:
              post:
                tags:
                  - Balance account
                summary: Sweep updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/balanceAccounts/_balanceAccountId_/sweeps/_sweepId_).
                operationId: post-balancePlatform.balanceAccountSweep.updated
                x-sortIndex: 4
                x-methodName: sweepUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.updated-balancePlatform-sweep-updated
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.cardorder.created:
              post:
                tags:
                  - Card order
                summary: Card order created
                description: >-
                  Adyen sends this webhook to indicate a successful creation of
                  a card order after you create a [payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments)
                  of `type` **card** and `formFactor` **physical**.
                operationId: post-balancePlatform.cardorder.created
                x-sortIndex: 1
                x-methodName: cardOrderCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/CardOrderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.cardorder.updated:
              post:
                tags:
                  - Card order
                summary: Card order updated
                description: >-
                  Adyen sends this webhook when there is an update in card order
                  status.
                operationId: post-balancePlatform.cardorder.updated
                x-sortIndex: 2
                x-methodName: cardOrderUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/CardOrderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.paymentInstrument.created:
              post:
                tags:
                  - Payment instrument
                summary: Payment instrument created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments). 

                  >The webhook does not include the card number when creating
                  virtual cards. You can only get the card number in the
                  response of the POST
                  [/paymentInstruments](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments#responses-200-card-number)
                  request.
                operationId: post-balancePlatform.paymentInstrument.created
                x-sortIndex: 1
                x-methodName: paymentInstrumentCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-paymentInstrument-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.paymentInstrument.created-balancePlatform-paymentInstrument-created
                      schema:
                        $ref: '#/components/schemas/PaymentNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-paymentInstrument-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.paymentInstrument.updated:
              post:
                tags:
                  - Payment instrument
                summary: Payment instrument updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/paymentInstruments/_id_). 
                operationId: post-balancePlatform.paymentInstrument.updated
                x-sortIndex: 2
                x-methodName: paymentInstrumentUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-paymentInstrument-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.paymentInstrument.updated-balancePlatform-paymentInstrument-updated
                      schema:
                        $ref: '#/components/schemas/PaymentNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-paymentInstrument-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeede
    overlays:
      - type: APIs.io Search
        url: overlays/configuration-webhooks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/configuration-webhooks-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-configuration-webhooks-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---