---
name: Adjust
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/adjust.png
url: https://example.com/apis/adjust.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Adjust
apis:
  - aid: bigcommerce:tax-provider
    name: Tax Provider
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Tax Provider API
          tags:
            - name: Tax Provider
          paths:
            /estimate:
              post:
                summary: Estimate Taxes
                tags:
                  - Estimate
                  - Taxes
                  - Estimate
                description: >-
                  Submit the quote request to retrieve an estimate from the
                  enabled third-party tax provider. Estimates are not expected
                  to be persisted by the tax provider.


                  > Server URL

                  > - For supporting tax providers, the server URL contains the
                  tax provider's profile field; for example,
                  `your_profile.example.com`.

                  > - The Try it feature is not currently supported for this
                  endpoint.


                  The following actions can trigger tax estimate requests
                  multiple times during a standard checkout on a BigCommerce
                  storefront, depending on the BigCommerce merchant’s settings.


                  - After selecting a Shipping Method during the “Estimate
                  Shipping & Tax” facility on the Cart page.

                  - After specifying a Shipping Address during a Checkout.

                  - After selecting a Shipping Method during a Checkout.

                  - After specifying a Billing Address during a Checkout.


                  The following actions are not expected to trigger estimate
                  requests.


                  - While anonymously browsing a store’s product catalog.

                  - On the Cart page prior to a Shopper selecting a Shipping
                  Method via “Estimate Shipping & Tax”.

                  - On the Checkout page prior to specifying a Shipping Address.

                  - On the Checkout page, when toggling any option related to
                  using the shopper’s Shipping Address as their Billing Address.


                  The following control panel actions can also trigger tax
                  estimate requests.


                  - Order refund.

                  - Edit order.

                  - Test connection feature in Tax Settings.
            /void:
              post:
                summary: Void Tax Quote
                description: >-
                  Invalidate the persisted tax quote as identified by the given
                  unique ID. Relevant to order cancellations, full refunds, or
                  moving an order from a paid status to an unpaid status.


                  > Server URL

                  > - For supporting tax providers, the server URL contains the
                  tax provider's profile field; for example,
                  `your_profile.example.com`.

                  > - The Try it feature is not currently supported for this
                  endpoint.
                tags:
                  - Void
                  - Tax
                  - Quote
                  - Estimate
                  - Void
            /commit:
              post:
                summary: Commit Tax Quote
                description: >-
                  Submit the quote request to be persisted by the enabled
                  third-party tax provider. A commit operation is intended to be
                  submitted once only, when the Order has been confirmed and
                  paid.


                  > Server URL

                  > - For supporting tax providers, the server URL contains the
                  tax provider's profile field; for example,
                  `your_profile.example.com`.

                  > - The Try it feature is not currently supported for this
                  endpoint.
                tags:
                  - Commit
                  - Tax
                  - Quote
                  - Estimate
                  - Void
                  - Commit
            /adjust:
              post:
                summary: Adjust Tax Quote
                description: >-
                  Replace the persisted tax quote (identified by the given
                  unique ID) with the provided quote request (represented by the
                  **AdjustRequest**).


                  Relevant for returns, partial refunds, and other Order
                  modifications where there have been changes to the tax
                  liabilities.


                  The returned **Tax Quote** response is expected to be the same
                  to a response returned by an equivalent response to
                  **estimate** or **commit** methods.


                  > Server URL

                  > - For supporting tax providers, the server URL contains the
                  tax provider's profile field; for example,
                  `your_profile.example.com`.

                  > - The Try it feature is not currently supported for this
                  endpoint.
                tags:
                  - Adjust
                  - Tax
                  - Quote
                  - Estimate
                  - Void
                  - Commit
                  - Adju
    overlays:
      - type: APIs.io Search
        url: overlays/tax-provider-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tax-provider-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---