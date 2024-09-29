---
name: Additionalconfiguration
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/additionalconfiguration.png
url: https://example.com/apis/additionalconfiguration.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Additionalconfiguration
apis:
  - name: Adyen Webhooks API
    description: >-
      We use webhooks to send you updates about payment status updates, newly
      available reports, and other events that you can subscribe to. For more
      information, refer to our
      [documentation](https://docs.adyen.com/development-resources/webhooks).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/development-resources/webhooks
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/development-resources/webhooks
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Webhooks
          tags:
            - name: Standard
            - name: Disputes
            - name: Payouts
            - name: Additional configuration
            - name: Webhooks
          x-staticResponse: response.json
          webhooks:
            /ACH_NOTIFICATION_OF_CHANGE:
              post:
                tags:
                  - Other webhooks
                summary: ACH Notification of Change
                description: >-
                  An ACH Notification of Change was processed regarding changed
                  bank account details.
                operationId: post-ACH_NOTIFICATION_OF_CHANGE
                x-sortIndex: 0
                x-methodName: achNotificationOfChange
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        ach_notification_of_change:
                          $ref: >-
                            #/components/examples/post-ACH_NOTIFICATION_OF_CHANGE-ach_notification_of_change
                      schema:
                        $ref: >-
                          #/components/schemas/AchNotificationOfChangeNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          ach_notification_of_change:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /AUTHORISATION:
              post:
                tags:
                  - Standard
                summary: Result of authorisation request
                description: >-
                  The result of the [authorisation
                  request](https://docs.adyen.com/api-explorer/#/Payment/latest/post/authorise).
                operationId: post-AUTHORISATION
                x-sortIndex: 0
                x-methodName: resultOfAuthorisationRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        authorisation:
                          $ref: >-
                            #/components/examples/post-AUTHORISATION-authorisation
                      schema:
                        $ref: '#/components/schemas/AuthorisationNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          authorisation:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /AUTHORISATION_ADJUSTMENT:
              post:
                tags:
                  - Standard
                summary: Result of payment authorisation adjustment request
                description: >-
                  The result of the request to [adjust the authorised
                  amount](https://docs.adyen.com/online-payments/adjust-authorisation)
                  sent through the
                  [/adjustAuthorisation](https://docs.adyen.com/api-explorer/#/Payment/latest/post/adjustAuthorisation)
                  endpoint.
                operationId: post-AUTHORISATION_ADJUSTMENT
                x-sortIndex: 0
                x-methodName: resultOfPaymentAuthorisationAdjustmentRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        authorisation_adjustment:
                          $ref: >-
                            #/components/examples/post-AUTHORISATION_ADJUSTMENT-authorisation_adjustment
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          authorisation_adjustment:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /AUTORESCUE:
              post:
                tags:
                  - Additional configuration
                summary: Auto Rescue process ended
                description: >-
                  The [Auto Rescue
                  process](https://docs.adyen.com/online-payments/auto-rescue#rescue-process-ended)
                  ended.
                operationId: post-AUTORESCUE
                x-sortIndex: 0
                x-methodName: autoRescueProcessEnded
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        autorescue:
                          $ref: '#/components/examples/post-AUTORESCUE-autorescue'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          autorescue:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CANCELLATION:
              post:
                tags:
                  - Standard
                summary: Result of cancel request
                description: >-
                  The result of the request to [cancel a
                  payment](https://docs.adyen.com/online-payments/cancel).
                operationId: post-CANCELLATION
                x-sortIndex: 0
                x-methodName: resultOfCancelRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        cancellation:
                          $ref: '#/components/examples/post-CANCELLATION-cancellation'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          cancellation:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CANCEL_AUTORESCUE:
              post:
                tags:
                  - Additional configuration
                summary: Auto Rescue process canceled
                description: >-
                  The [Auto Rescue
                  process](https://docs.adyen.com/online-payments/auto-rescue)
                  was canceled.
                operationId: post-CANCEL_AUTORESCUE
                x-sortIndex: 0
                x-methodName: autoRescueProcessCanceled
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        cancel_autorescue:
                          $ref: >-
                            #/components/examples/post-CANCEL_AUTORESCUE-cancel_autorescue
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          cancel_autorescue:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CANCEL_OR_REFUND:
              post:
                tags:
                  - Standard
                summary: Result of cancel or refund request
                description: >-
                  The result of the request to [cancel or refund a
                  payment](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/cancel-or-refund).
                operationId: post-CANCEL_OR_REFUND
                x-sortIndex: 0
                x-methodName: resultOfCancelOrRefundRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        cancel_or_refund:
                          $ref: >-
                            #/components/examples/post-CANCEL_OR_REFUND-cancel_or_refund
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          cancel_or_refund:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CAPTURE:
              post:
                tags:
                  - Standard
                summary: Result of capture request
                description: >-
                  The result of the request to [capture a
                  payment](https://docs.adyen.com/online-payments/capture).
                operationId: post-CAPTURE
                x-sortIndex: 0
                x-methodName: resultOfCaptureRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        capture:
                          $ref: '#/components/examples/post-CAPTURE-capture'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          capture:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CAPTURE_FAILED:
              post:
                tags:
                  - Standard
                summary: Capture request failed due to scheme rejection
                description: >-
                  The capture request [failed due to rejection by the card
                  scheme](https://docs.adyen.com/online-payments/capture#failed-capture).
                operationId: post-CAPTURE_FAILED
                x-sortIndex: 0
                x-methodName: captureRequestFailedDueToSchemeRejection
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        capture_failed:
                          $ref: >-
                            #/components/examples/post-CAPTURE_FAILED-capture_failed
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          capture_failed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CHARGEBACK:
              post:
                tags:
                  - Dispute
                summary: Payment charged back
                description: >-
                  The payment was [charged
                  back](https://docs.adyen.com/risk-management/disputes-api/dispute-notifications#chargeback),
                  and the funds were deducted from your account.
                operationId: post-CHARGEBACK
                x-sortIndex: 0
                x-methodName: paymentChargedBack
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        chargeback:
                          $ref: '#/components/examples/post-CHARGEBACK-chargeback'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          chargeback:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /CHARGEBACK_REVERSED:
              post:
                tags:
                  - Dispute
                summary: Chargeback successfully defended
                description: >-
                  The chargeback was successfully
                  [defended](https://docs.adyen.com/risk-management/understanding-disputes/defense-requirements)
                  towards the issuing bank. This stage is not final. If the
                  issuing bank presents a second chargeback, you can still lose
                  the chargeback case.
                operationId: post-CHARGEBACK_REVERSED
                x-sortIndex: 0
                x-methodName: chargebackSuccessfullyDefended
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        chargeback_reversed:
                          $ref: >-
                            #/components/examples/post-CHARGEBACK_REVERSED-chargeback_reversed
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          chargeback_reversed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /EXPIRE:
              post:
                tags:
                  - Standard
                summary: Authorisation expired
                description: The remaining uncaptured amount expired
                operationId: post-EXPIRE
                x-sortIndex: 0
                x-methodName: authorisationExpired
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        expire:
                          $ref: '#/components/examples/post-EXPIRE-expire'
                      schema:
                        $ref: '#/components/schemas/ExpireNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          expire:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /MANUAL_REVIEW_ACCEPT:
              post:
                tags:
                  - Additional configuration
                summary: Manual review accepted
                description: >-
                  The [manual
                  review](https://docs.adyen.com/risk-management/case-management)
                  was accepted.
                operationId: post-MANUAL_REVIEW_ACCEPT
                x-sortIndex: 0
                x-methodName: manualReviewAccepted
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        manual_review_accept:
                          $ref: >-
                            #/components/examples/post-MANUAL_REVIEW_ACCEPT-manual_review_accept
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          manual_review_accept:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /MANUAL_REVIEW_REJECT:
              post:
                tags:
                  - Additional configuration
                summary: Manual review rejected
                description: >-
                  The [manual
                  review](https://docs.adyen.com/risk-management/case-management)
                  was rejected.
                operationId: post-MANUAL_REVIEW_REJECT
                x-sortIndex: 0
                x-methodName: manualReviewRejected
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        manual_review_reject:
                          $ref: >-
                            #/components/examples/post-MANUAL_REVIEW_REJECT-manual_review_reject
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          manual_review_reject:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /NOTIFICATION_OF_CHARGEBACK:
              post:
                tags:
                  - Dispute
                summary: Dispute process opened
                description: >-
                  The [dispute
                  process](https://docs.adyen.com/risk-management/understanding-disputes/dispute-process-and-flow#dispute-process)
                  was opened. You should investigate the dispute and [supply the
                  defense
                  documents](https://docs.adyen.com/risk-management/disputes-api#supply-dispute-defense-documents).
                operationId: post-NOTIFICATION_OF_CHARGEBACK
                x-sortIndex: 0
                x-methodName: disputeProcessOpened
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        notification_of_chargeback:
                          $ref: >-
                            #/components/examples/post-NOTIFICATION_OF_CHARGEBACK-notification_of_chargeback
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          notification_of_chargeback:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /NOTIFICATION_OF_FRAUD:
              post:
                tags:
                  - Dispute
                summary: Issuer sent fraud alert notification
                description: >-
                  The issuer sent a [fraud alert
                  notification](https://docs.adyen.com/risk-management/understanding-disputes/dispute-process-and-flow#dispute-process)
                  to schemes and to processors. Visa calls them TC40 and
                  Mastercard calls them System to Avoid Fraud Effectively
                  (SAFE). These are informational notifications from Adyen,
                  providing you the opportunity to take action, such as blocking
                  a shopper or issuing a refund before a chargeback happens.
                operationId: post-NOTIFICATION_OF_FRAUD
                x-sortIndex: 0
                x-methodName: issuerSentFraudAlertNotification
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        notification_of_fraud:
                          $ref: >-
                            #/components/examples/post-NOTIFICATION_OF_FRAUD-notification_of_fraud
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          notification_of_fraud:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /OFFER_CLOSED:
              post:
                tags:
                  - Additional configuration
                summary: Offer expired
                description: >-
                  The offer expired, for example, because the shopper abandoned
                  the session. For cards, offers expire after 12 hours by
                  default.
                operationId: post-OFFER_CLOSED
                x-sortIndex: 0
                x-methodName: offerExpired
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        offer_closed:
                          $ref: '#/components/examples/post-OFFER_CLOSED-offer_closed'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          offer_closed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /ORDER_CLOSED:
              post:
                tags:
                  - Standard
                summary: Result of last partial payment for order
                description: >-
                  The result of the last [partial
                  payment](https://docs.adyen.com/online-payments/partial-payments)
                  for the order.
                operationId: post-ORDER_CLOSED
                x-sortIndex: 0
                x-methodName: resultOfLastPartialPaymentForOrder
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        order_closed:
                          $ref: '#/components/examples/post-ORDER_CLOSED-order_closed'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          order_closed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /ORDER_OPENED:
              post:
                tags:
                  - Standard
                summary: First partial payment request for order
                description: >-
                  The first [partial
                  payment](https://docs.adyen.com/online-payments/partial-payments)
                  was made, and the order was created.
                operationId: post-ORDER_OPENED
                x-sortIndex: 0
                x-methodName: firstPartialPaymentRequestForOrder
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        order_opened:
                          $ref: '#/components/examples/post-ORDER_OPENED-order_opened'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          order_opened:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PAIDOUT_REVERSED:
              post:
                tags:
                  - Payout
                summary: Financial institution rejected payout
                description: >-
                  The financial institution [rejected the
                  payout](https://docs.adyen.com/online-payments/online-payouts/payout-notifications).
                  We will return the funds back to your account. 

                  The reason field contains the bank statement description if
                  present.
                operationId: post-PAIDOUT_REVERSED
                x-sortIndex: 0
                x-methodName: financialInstitutionRejectedPayout
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        paidout_reversed:
                          $ref: >-
                            #/components/examples/post-PAIDOUT_REVERSED-paidout_reversed
                      schema:
                        $ref: >-
                          #/components/schemas/PaidoutReversedNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          paidout_reversed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PAYOUT_DECLINE:
              post:
                tags:
                  - Payout
                summary: Payout declined
                description: >-
                  The [payout was
                  declined](https://docs.adyen.com/online-payments/online-payouts/confirm-or-decline-payout).
                operationId: post-PAYOUT_DECLINE
                x-sortIndex: 0
                x-methodName: payoutDeclined
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        payout_decline:
                          $ref: >-
                            #/components/examples/post-PAYOUT_DECLINE-payout_decline
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          payout_decline:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PAYOUT_EXPIRE:
              post:
                tags:
                  - Payout
                summary: Payout expired
                description: >-
                  The [payout
                  expired](https://docs.adyen.com/online-payments/online-payouts/payout-notifications).
                operationId: post-PAYOUT_EXPIRE
                x-sortIndex: 0
                x-methodName: payoutExpired
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        payout_expire:
                          $ref: >-
                            #/components/examples/post-PAYOUT_EXPIRE-payout_expire
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          payout_expire:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PAYOUT_THIRDPARTY:
              post:
                tags:
                  - Payout
                summary: Result of payout request
                description: >-
                  The result of the [payout
                  request](https://docs.adyen.com/online-payments/online-payouts).
                operationId: post-PAYOUT_THIRDPARTY
                x-sortIndex: 0
                x-methodName: resultOfPayoutRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        payout_thirdparty:
                          $ref: >-
                            #/components/examples/post-PAYOUT_THIRDPARTY-payout_thirdparty
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          payout_thirdparty:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /POSTPONED_REFUND:
              post:
                tags:
                  - Additional configuration
                summary: Refund postponed until after payment capture
                description: >-
                  The refund was postponed until after [payment
                  capture](https://docs.adyen.com/online-payments/capture). To
                  enable this notification, contact our [Support
                  Team](https://www.adyen.help/hc/en-us/requests/new).
                operationId: post-POSTPONED_REFUND
                x-sortIndex: 0
                x-methodName: refundPostponedUntilAfterPaymentCapture
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        postponed_refund:
                          $ref: >-
                            #/components/examples/post-POSTPONED_REFUND-postponed_refund
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          postponed_refund:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PREARBITRATION_LOST:
              post:
                tags:
                  - Dispute
                summary: Cardholder's bank declined pre-arbitration case
                description: >-
                  The cardholder's bank declined the
                  [pre-arbitration](https://docs.adyen.com/risk-management/understanding-disputes/dispute-process-and-flow#dispute-process)
                  case.
                operationId: post-PREARBITRATION_LOST
                x-sortIndex: 0
                x-methodName: cardholdersBankDeclinedPrearbitrationCase
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        prearbitration_lost:
                          $ref: >-
                            #/components/examples/post-PREARBITRATION_LOST-prearbitration_lost
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          prearbitration_lost:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /PREARBITRATION_WON:
              post:
                tags:
                  - Dispute
                summary: Cardholder's bank accepted pre-arbitration case
                description: >-
                  The cardholder's bank accepted the
                  [pre-arbitration](https://docs.adyen.com/risk-management/understanding-disputes/dispute-process-and-flow#dispute-process)
                  case.
                operationId: post-PREARBITRATION_WON
                x-sortIndex: 0
                x-methodName: cardholdersBankAcceptedPrearbitrationCase
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        prearbitration_won:
                          $ref: >-
                            #/components/examples/post-PREARBITRATION_WON-prearbitration_won
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          prearbitration_won:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /RECURRING_CONTRACT:
              post:
                tags:
                  - Additional configuration
                summary: Recurring contract created
                description: >-
                  A recurring contract has been created. [Enable this
                  webhook](https://docs.adyen.com/development-resources/webhooks/webhook-types#non-default-event-codes)
                  in your Customer Area.
                operationId: post-RECURRING_CONTRACT
                x-sortIndex: 0
                x-methodName: recurringContractCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        recurring_contract:
                          $ref: >-
                            #/components/examples/post-RECURRING_CONTRACT-recurring_contract
                      schema:
                        $ref: >-
                          #/components/schemas/RecurringContractNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          recurring_contract:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REFUND:
              post:
                tags:
                  - Standard
                summary: Result of refund request
                description: >-
                  The result of the request to [refund a
                  payment](https://docs.adyen.com/online-payments/refund).
                operationId: post-REFUND
                x-sortIndex: 0
                x-methodName: resultOfRefundRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        refund:
                          $ref: '#/components/examples/post-REFUND-refund'
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          refund:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REFUNDED_REVERSED:
              post:
                tags:
                  - Standard
                summary: Refunded amount reversed
                description: >-
                  The refunded amount was
                  [reversed](https://docs.adyen.com/online-payments/refund#refunded-reversed)
                  and returned to your bank account.
                operationId: post-REFUNDED_REVERSED
                x-sortIndex: 0
                x-methodName: refundedAmountReversed
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        refunded_reversed:
                          $ref: >-
                            #/components/examples/post-REFUNDED_REVERSED-refunded_reversed
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          refunded_reversed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REFUND_FAILED:
              post:
                tags:
                  - Standard
                summary: Refund failed due to scheme rejection
                description: >-
                  The refund [failed due to rejection by the card
                  scheme](https://docs.adyen.com/online-payments/refund#refund-failed).
                operationId: post-REFUND_FAILED
                x-sortIndex: 0
                x-methodName: refundFailedDueToSchemeRejection
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        refund_failed:
                          $ref: >-
                            #/components/examples/post-REFUND_FAILED-refund_failed
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          refund_failed:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REFUND_WITH_DATA:
              post:
                tags:
                  - Standard
                summary: Result of refund request with data
                description: >-
                  The result of the request to [refund with
                  data](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/refund#unreferenced-refund).
                operationId: post-REFUND_WITH_DATA
                x-sortIndex: 0
                x-methodName: resultOfRefundRequestWithData
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        refund_with_data:
                          $ref: >-
                            #/components/examples/post-REFUND_WITH_DATA-refund_with_data
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          refund_with_data:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REPORT_AVAILABLE:
              post:
                tags:
                  - Standard
                summary: Report available
                description: The report is generated and ready to be downloaded.
                operationId: post-REPORT_AVAILABLE
                x-sortIndex: 0
                x-methodName: reportAvailable
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        report_available:
                          $ref: >-
                            #/components/examples/post-REPORT_AVAILABLE-report_available
                      schema:
                        $ref: >-
                          #/components/schemas/ReportAvailableNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          report_available:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /REQUEST_FOR_INFORMATION:
              post:
                tags:
                  - Dispute
                summary: Issuer opened Request for Information (RFI)
                description: >-
                  The issuer opened a [Request for Information
                  (RFI)](https://docs.adyen.com/risk-management/understanding-disputes/dispute-process-and-flow#dispute-process).
                  You should [supply defense
                  documents](https://docs.adyen.com/risk-management/disputes-api#supply-dispute-defense-documents)
                  to help shopper understand the charge.
                operationId: post-REQUEST_FOR_INFORMATION
                x-sortIndex: 0
                x-methodName: issuerOpenedRequestForInformationrfi
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        request_for_information:
                          $ref: >-
                            #/components/examples/post-REQUEST_FOR_INFORMATION-request_for_information
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          request_for_information:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /SECOND_CHARGEBACK:
              post:
                tags:
                  - Dispute
                summary: Issuing bank declined chargeback defense
                description: >-
                  The issuing bank declined the material submitted during
                  [defense of the original
                  chargeback](https://docs.adyen.com/risk-management/understanding-disputes/defense-requirements).
                  The disputed amount is deducted from your account.
                operationId: post-SECOND_CHARGEBACK
                x-sortIndex: 0
                x-methodName: issuingBankDeclinedChargebackDefense
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        second_chargeback:
                          $ref: >-
                            #/components/examples/post-SECOND_CHARGEBACK-second_chargeback
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          second_chargeback:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /TECHNICAL_CANCEL:
              post:
                tags:
                  - Standard
                summary: Result of technical cancel request
                description: >-
                  The result of the [technical
                  cancel](https://docs.adyen.com/online-payments/cancel#technical-cancel-webhook)
                  request.
                operationId: post-TECHNICAL_CANCEL
                x-sortIndex: 0
                x-methodName: resultOfTechnicalCancelRequest
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        technical_cancel:
                          $ref: >-
                            #/components/examples/post-TECHNICAL_CANCEL-technical_cancel
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          technical_cancel:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeeded.
            /VOID_PENDING_REFUND:
              post:
                tags:
                  - Standard
                summary: Result of request to cancel POS refund
                description: >-
                  The result of the request to [cancel a POS
                  refund](https://docs.adyen.com/point-of-sale/refund-payment/cancel-a-pos-refund-request).
                operationId: post-VOID_PENDING_REFUND
                x-sortIndex: 0
                x-methodName: resultOfRequestToCancelPosRefund
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        void_pending_refund:
                          $ref: >-
                            #/components/examples/post-VOID_PENDING_REFUND-void_pending_refund
                      schema:
                        $ref: '#/components/schemas/NotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          void_pending_refund:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: '#/components/schemas/NotificationResponse'
                    description: OK - the request has succeede
    overlays:
      - type: APIs.io Search
        url: overlays/webhooks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/webhooks-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-webhooks-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---