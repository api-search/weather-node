---
name: Acquisition
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/acquisition.png
url: https://example.com/apis/acquisition.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Acquisition
apis:
  - name: Adyen Terminal API
    description: >-
      The Adyen Terminal API lets you make payments, issue refunds, collect
      shopper information, and perform other shopper-terminal interactions using
      a payment terminal supplied by Adyen.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Adyen Terminal API
          paths:
            /login:
              post:
                description: >-
                  It conveys Information related to the session (period between
                  a Login and the following Logout) to process. Content of the
                  Login Request message.
                summary: Login Request
                tags:
                  - Login
                  - Request
                  - Login
            /logout:
              post:
                description: Empty. Content of the Logout Request message.
                summary: Logout Request
                tags:
                  - Logout
                  - Request
                  - Login
                  - Logout
            /enableservice:
              post:
                description: >-
                  It conveys the services that will be enabled for the  POI
                  Terminal without the request of the Sale System, and a
                  possible invitation for the Customer to start the services.
                  Content of the Enable Service Request message.
                summary: EnableService Request
                tags:
                  - Enable
                  - Services
                  - Request
                  - Login
                  - Logout
                  - Enable Service
            /admin:
              post:
                description: Empty. Content of the Custom Admin Request message.
                summary: Admin Request
                tags:
                  - Administrative
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
            /payment:
              post:
                description: >-
                  Request sent to terminal to initiate payment.  It conveys
                  Information related to the Payment transaction to process.
                  Content of the Payment Request message.
                summary: Payment Request
                tags:
                  - Payments
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
            /cardacquisition:
              post:
                description: >-
                  It conveys Information related to the payment and loyalty
                  cards to read and analyse. This message pair is usually
                  followed by a message pair (e.g. payment or loyalty) which
                  refers to this Card Acquisition message pair. Content of the
                  Card Acquisition Request message.
                summary: CardAcquisition Request
                tags:
                  - Cards
                  - Acquisition
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
            /loyalty:
              post:
                description: >-
                  It conveys Information related to the Loyalty transaction to
                  process. Content of the Loyalty Request message.
                summary: Loyalty Request
                tags:
                  - Loyalty
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
            /storedvalue:
              post:
                description: >-
                  It conveys Information related to the Stored Value transaction
                  to process. Content of the Stored Value Request message.
                summary: StoredValue Request
                tags:
                  - Stored
                  - Value
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
            /reversal:
              post:
                description: >-
                  It conveys Information related to the reversal of a previous
                  payment or a loyalty transaction. Content of the Reversal
                  Request message.
                summary: Reversal Request
                tags:
                  - Reversals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
            /reconciliation:
              post:
                description: >-
                  It conveys Information related to the Reconciliation requested
                  by the Sale System. Content of the Reconciliation Request
                  message.
                summary: Reconciliation Request
                tags:
                  - Reconciliation
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
            /gettotals:
              post:
                description: >-
                  It conveys information from the Sale System related to the
                  scope and the format of the totals to be computed by the POI
                  System. Content of the Get Totals Request message.
                summary: GetTotals Request
                tags:
                  - Get
                  - Totals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
            /balanceinquiry:
              post:
                description: >-
                  It conveys Information related to the account for which a
                  Balance Inquiry is requested. Content of the Balance Inquiry
                  Request message.
                summary: BalanceInquiry Request
                tags:
                  - Balance
                  - Inquiries
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
            /transactionstatus:
              post:
                description: >-
                  It conveys Information requested for status of the last or
                  current Payment, Loyalty or Reversal transaction. Content of
                  the TransactionStatus Request message.
                summary: TransactionStatus Request
                tags:
                  - Transactions
                  - Status
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
            /diagnosis:
              post:
                description: >-
                  It conveys Information related to the target POI for which the
                  diagnosis is requested. Content of the Diagnosis Request
                  message.
                summary: Diagnosis Request
                tags:
                  - Diagnosis
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
            /display:
              post:
                description: >-
                  It conveys the data to display and the way to process the
                  display. It contains the complete content to display. It might
                  contain an operation (the DisplayOutput element) per Display
                  Device type. Content of the Display Request message.
                summary: Display Request
                tags:
                  - Display
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
            /input:
              post:
                description: >-
                  It conveys data to display and the way to process the display,
                  and contains the complete content to display. In addition to
                  the display on the Input Device, it might contain an operation
                  (the DisplayOutput element) per Display Device type. Content
                  of the Input Request message.
                summary: Input Request
                tags:
                  - Inputs
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
            /print:
              post:
                description: >-
                  It conveys the data to print and the way to process the print.
                  It contains the complete content to print. Content of the
                  Print Request message.
                summary: Print Request
                tags:
                  - Print
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
            /cardreaderapdu:
              post:
                description: >-
                  It contains the APDU request to send to the chip of the card,
                  and a possible invitation message to display on the
                  CashierInterface or the CustomerInterface. Content of the Card
                  Reader APDU Request message.
                summary: CardReaderAPDU Reque
                tags:
                  - Cards
                  - Readers
                  - Reque
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
                  - Card Reader Applications
    overlays:
      - type: APIs.io Search
        url: overlays/terminal-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/terminal-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-terminal-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---