---
name: Charge
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/charge.png
url: https://example.com/apis/charge.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Charge
apis:
  - aid: stripe:stripe-charges-api
    name: Stripe Charges API
    description: >-
      The Charge object represents a single attempt to move money into your
      Stripe account. PaymentIntent confirmation is the most common way to
      create Charges, but transferring money to a different Stripe account
      through Connect also creates Charges. Some legacy payment flows create
      Charges directly, which is not recommended for new integrations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/api/charges
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/api/charges
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Charges API
          paths:
            /v1/charges:
              get:
                description: >-
                  <p>Returns a list of charges you’ve previously created. The
                  charges are returned in sorted order, with the most recent
                  charges appearing first.</p>
                tags:
                  - V1
                  - Charges
              post:
                description: >-
                  <p>Use the <a href="/docs/api/payment_intents">Payment Intents
                  API</a> to initiate a new payment instead

                  of using this method. Confirmation of the PaymentIntent
                  creates the <code>Charge</code>

                  object used to request payment, so this method is limited to
                  legacy integrations.</p>
                tags:
                  - V1
                  - Charges
            /v1/charges/search:
              get:
                description: >-
                  <p>Search for charges you’ve previously created using Stripe’s
                  <a href="/docs/search#search-query-language">Search Query
                  Language</a>.

                  Don’t use search in read-after-write flows where strict
                  consistency is necessary. Under normal operating

                  conditions, data is searchable in less than a minute.
                  Occasionally, propagation of new or updated data can be up

                  to an hour behind during outages. Search functionality is not
                  available to merchants in India.</p>
                tags:
                  - V1
                  - Charges
                  - Search
            /v1/charges/{charge}:
              get:
                description: >-
                  <p>Retrieves the details of a charge that has previously been
                  created. Supply the unique charge ID that was returned from
                  your previous request, and Stripe will return the
                  corresponding charge information. The same information is
                  returned when creating or refunding the charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
              post:
                description: >-
                  <p>Updates the specified charge by setting the values of the
                  parameters passed. Any parameters not provided will be left
                  unchanged.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
            /v1/charges/{charge}/capture:
              post:
                description: >-
                  <p>Capture the payment of an existing, uncaptured charge that
                  was created with the <code>capture</code> option set to
                  false.</p>


                  <p>Uncaptured payments expire a set number of days after they
                  are created (<a href="/docs/charges/placing-a-hold">7 by
                  default</a>), after which they are marked as refunded and
                  capture attempts will fail.</p>


                  <p>Don’t use this method to capture a PaymentIntent-initiated
                  charge. Use <a
                  href="/docs/api/payment_intents/capture">Capture a
                  PaymentIntent</a>.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
            /v1/charges/{charge}/dispute:
              get:
                description: <p>Retrieve a dispute for a specified charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
              post:
                description: ''
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
            /v1/charges/{charge}/dispute/close:
              post:
                description: ''
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
            /v1/charges/{charge}/refund:
              post:
                description: >-
                  <p>When you create a new refund, you must specify either a
                  Charge or a PaymentIntent object.</p>


                  <p>This action refunds a previously created charge that’s not
                  refunded yet.

                  Funds are refunded to the credit or debit card that’s
                  originally charged.</p>


                  <p>You can optionally refund only part of a charge.

                  You can repeat this until the entire charge is refunded.</p>


                  <p>After you entirely refund a charge, you can’t refund it
                  again.

                  This method raises an error when it’s called on an
                  already-refunded charge,

                  or when you attempt to refund more money than is left on a
                  charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
            /v1/charges/{charge}/refunds:
              get:
                description: >-
                  <p>You can see a list of the refunds belonging to a specific
                  charge. Note that the 10 most recent refunds are always
                  available by default on the charge object. If you need more
                  than those 10, you can use this API method and the
                  <code>limit</code> and <code>starting_after</code> parameters
                  to page through additional refunds.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
              post:
                description: >-
                  <p>When you create a new refund, you must specify a Charge or
                  a PaymentIntent object on which to create it.</p>


                  <p>Creating a new refund will refund a charge that has
                  previously been created but not yet refunded.

                  Funds will be refunded to the credit or debit card that was
                  originally charged.</p>


                  <p>You can optionally refund only part of a charge.

                  You can do so multiple times, until the entire charge has been
                  refunded.</p>


                  <p>Once entirely refunded, a charge can’t be refunded again.

                  This method will raise an error when called on an
                  already-refunded charge,

                  or when trying to refund more money than is left on a
                  charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
            /v1/charges/{charge}/refunds/{refund}:
              get:
                description: <p>Retrieves the details of an existing refund.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
              post:
                description: <p>Update a specified r
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refun
    overlays:
      - type: APIs.io Search
        url: overlays/charges-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/charges-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---