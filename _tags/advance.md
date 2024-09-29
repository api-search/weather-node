---
name: Advance
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/advance.png
url: https://example.com/apis/advance.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Advance
apis:
  - aid: stripe:stripe-test-helpers-api
    name: Stripe Test Helpers API
    description: >-
      Stripe provides a number of resources for testing your integration. Make
      sure to test the following use cases before launch, and use our Postman
      collection to make the testing process simpler.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/implementation-guides/billing/testing
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/implementation-guides/billing/testing
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Test Helpers API
          paths:
            /v1/test_helpers/customers/{customer}/fund_cash_balance:
              post:
                description: <p>Create an incoming testmode bank transfer</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
            /v1/test_helpers/issuing/authorizations:
              post:
                description: <p>Create a test-mode authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
            /v1/test_helpers/issuing/authorizations/{authorization}/capture:
              post:
                description: <p>Capture a test-mode authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
            /v1/test_helpers/issuing/authorizations/{authorization}/expire:
              post:
                description: <p>Expire a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
            /v1/test_helpers/issuing/authorizations/{authorization}/increment:
              post:
                description: <p>Increment a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
            /v1/test_helpers/issuing/authorizations/{authorization}/reverse:
              post:
                description: <p>Reverse a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
            /v1/test_helpers/issuing/cards/{card}/shipping/deliver:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>delivered</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
            /v1/test_helpers/issuing/cards/{card}/shipping/fail:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>failure</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
            /v1/test_helpers/issuing/cards/{card}/shipping/return:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>returned</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
            /v1/test_helpers/issuing/cards/{card}/shipping/ship:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>shipped</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
            /v1/test_helpers/issuing/transactions/create_force_capture:
              post:
                description: >-
                  <p>Allows the user to capture an arbitrary amount, also known
                  as a forced capture.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
            /v1/test_helpers/issuing/transactions/create_unlinked_refund:
              post:
                description: >-
                  <p>Allows the user to refund an arbitrary amount, also known
                  as a unlinked refund.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
            /v1/test_helpers/issuing/transactions/{transaction}/refund:
              post:
                description: <p>Refund a test-mode Transaction.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
            /v1/test_helpers/refunds/{refund}/expire:
              post:
                description: >-
                  <p>Expire a refund with a status of
                  <code>requires_action</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
            /v1/test_helpers/terminal/readers/{reader}/present_payment_method:
              post:
                description: >-
                  <p>Presents a payment method on a simulated reader. Can be
                  used to simulate accepting a payment, saving a card or
                  refunding a transaction.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
            /v1/test_helpers/test_clocks:
              get:
                description: <p>Returns a list of your test clocks.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
              post:
                description: >-
                  <p>Creates a new test clock that can be attached to new
                  customers and quotes.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
            /v1/test_helpers/test_clocks/{test_clock}:
              delete:
                description: <p>Deletes a test clock.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
              get:
                description: <p>Retrieves a test clock.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
            /v1/test_helpers/test_clocks/{test_clock}/advance:
              post:
                description: >-
                  <p>Starts advancing a test clock to a specified time in the
                  future. Advancement is done when status changes to
                  <code>Ready</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
            /v1/test_helpers/treasury/inbound_transfers/{id}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created InboundTransfer to the
                  <code>failed</code> status. The InboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
            /v1/test_helpers/treasury/inbound_transfers/{id}/return:
              post:
                description: >-
                  <p>Marks the test mode InboundTransfer object as returned and
                  links the InboundTransfer to a ReceivedDebit. The
                  InboundTransfer must already be in the <code>succeeded</code>
                  state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
            /v1/test_helpers/treasury/inbound_transfers/{id}/succeed:
              post:
                description: >-
                  <p>Transitions a test mode created InboundTransfer to the
                  <code>succeeded</code> status. The InboundTransfer must
                  already be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
            /v1/test_helpers/treasury/outbound_payments/{id}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>failed</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
            /v1/test_helpers/treasury/outbound_payments/{id}/post:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>posted</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
            /v1/test_helpers/treasury/outbound_payments/{id}/return:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>returned</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>failed</code> status. The OutboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/post:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>posted</code> status. The OutboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/return:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>returned</code> status. The OutboundTransfer must
                  already be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/received_credits:
              post:
                description: >-
                  <p>Use this endpoint to simulate a test mode ReceivedCredit
                  initiated by a third party. In live mode, you can’t directly
                  create ReceivedCredits initiated by third parties.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
                  - Received_credits
            /v1/test_helpers/treasury/received_debits:
              post:
                description: >-
                  <p>Use this endpoint to simulate a test mode ReceivedDebit
                  initiated by a third party. In live mode, you can’t directly
                  create ReceivedDebits initiated by third pa
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
                  - Received_credits
                  - Received_debi
    overlays:
      - type: APIs.io Search
        url: overlays/test-helpers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/test-helpers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---