---
name: Checkout Spam Protection
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/checkout-spam-protection.png
url: https://example.com/apis/checkout-spam-protection.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Checkout Spam Protection
apis:
  - aid: bigcommerce:storefront-checkouts
    name: Storefront Checkouts
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
          openapi: 3.0.1
          info:
            title: Storefront Checkouts
            version: ''
          tags:
            - name: Checkout
            - name: Checkout Billing Address
            - name: Checkout Cart Items
            - name: Checkout Consignments
            - name: Checkout Coupons
            - name: Checkout Gift Certificates
            - name: Checkout Spam Protection
            - name: Checkout Store Credit
          paths:
            /checkouts/{checkoutId}:
              get:
                tags:
                  - Get
                  - Checkout
                  - Id
                summary: Get a Checkout
                description: >-
                  Returns a *Checkout*.


                  The cart ID and checkout ID are the same.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
              put:
                tags:
                  - Update
                  - Customer
                  - Messages
                  - Id
                summary: Update Customer Messages
                description: >-
                  Updates *Checkout* customer messages.


                  **Limits**


                  * 2000 character limit


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/carts/{cartId}/items/{itemId}:
              put:
                tags:
                  - Update
                  - Line
                  - Item
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                summary: Update a Line Item
                description: >-
                  Updates a *Checkout Line Item*. Updates an existing, single
                  line item in the cart.


                  If a variant needs to be changed or updated, the product will
                  need to be removed and re-added to the cart with the correct
                  variants using the [Add Cart Line
                  Items](/docs/rest-storefront/carts/cart-items#add-cart-line-items)
                  endpoint or the [GraphQL Storefront
                  API](/docs/storefront/cart-checkout/guide/graphql-storefront).


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
              delete:
                tags:
                  - Delete
                  - Line
                  - Item
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                summary: Delete a Line Item
                description: >-
                  Deletes a *Line Item* from the *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/billing-address:
              post:
                tags:
                  - Add
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                summary: Add Checkout Billing Address
                description: >-
                  Adds a billing address to an existing *Checkout*.


                  **Required Fields**

                  * country_code



                  > #### Note

                  > * The `email` property is only required if the customer is a
                  guest shopper. Otherwise, it is set automatically.

                  > * Sending `email` property as a payload in POST request
                  triggers the abandoned cart notification process.

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/billing-address/{addressId}:
              put:
                tags:
                  - Update
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                summary: Update Checkout Billing Address
                description: >-
                  Updates an existing billing address on *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/consignments:
              post:
                tags:
                  - Create
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                summary: Create a Consignment
                description: >
                  Adds a new *Consignment* to *Checkout*.


                  Perform the following two steps to define the fulfillment of
                  the items in the cart.
                    ### For **shipping** consignments:
                      1. Add a new Consignment to Checkout.
                          * Send a `POST` request to `/consignments` with each shipping address, line item IDs, and quantities. Each address can have its own line item IDs.
                          * Provide a full valid customer address before placing the order. If provided, the order placement will succeed. 
                          * As part of the request URL make sure to add `include=consignments.availableShippingOptions` to return the available shipping options based on the items, the address, and the shipping location. This will return `availableShippingOptions` in the response.

                        * Required Fields:
                          * `shipping_address` (deprecated) or `address`
                          * `lineItems`
                      2. Update the Consignment with Shipping Options using the [REST Storefront API](/checkouts/checkout-consignments#update-a-consignment), the [REST Management API](/docs/rest-management/checkouts/checkout-consignments#update-checkout-consignment) or the [GraphQL Storefront API](/docs/storefront/cart-checkout/guide/graphql-storefront).
                            
                    ### For **pickup** consignments:
                      1. Create a new consignment object. 
                        - Send a `POST` request to `/consignments` with line item IDs and quantities.
                        - Provide a `pickupMethodId`. This is the `id` of the Pickup Method provided in the response body of the Storefront Pickup Options API.
                        - Required Fields:
                            * `pickupOption`
                            * `lineItems`

                  To learn more about creating a Checkout Consignment, see the
                  [Carts and Checkouts
                  Tutorial](/docs/storefront/cart-checkout/guide/rest-storefront).


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
            /checkouts/{checkoutId}/consignments/{consignmentId}:
              put:
                tags:
                  - Update
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Update a Consignment
                description: >-
                  Updates an existing consignment. An update is either one of
                  the following:


                  1. Updates the consignment address and/or line items.

                  2. Selects a specific fulfillment option.


                  ### Update the consignment address and line items

                  For this type of update, the payload is the same as when
                  creating a new consignment.         Update each *Consignment*
                  `shippingOptionId` (shipping address and line items) with the
                  `availableShippingOption > id` from the POST `/consignment`
                  response. 


                  **Note:**

                  Updating a consignment could invalidate the value for
                  `selectedShippingOption` and `selectedPickupOption`.


                  ### Select a specific fulfillment option

                  Before placing an order, each consignment must have a
                  `selectedShippingOption` or a `selectedPickupOption`.


                  If the consignment already has a pick-up option selected and a
                  shipping option is provided, the pick-up option will be
                  deselected and the shipping option will be selected instead
                  (and vice versa). The `PUT` request will fail if it contains a
                  shipping option ID and a pickup option ID.


                  Required Fields:

                  * `shippingOptionId` or `pickupOptionId`

                  * `lineItems`


                  To learn more about creating a Checkout Consignment see
                  [Checkout Consignment
                  API](/docs/storefront/cart-checkout/guide/consignments).


                  > #### Notes

                  > * You cannot pass both an `address` and a `shippingOptionId`
                  because the shipping option may not be available for the new
                  address 

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
              delete:
                tags:
                  - Delete
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Delete a Consignment
                description: >-
                  Removes an existing *Consignment* from *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/gift-certificates:
              post:
                tags:
                  - Add
                  - Gift
                  - Certificate
                  - To
                  - Checkout
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                summary: Add Gift Certificate to Checkout
                description: >-
                  Adds a *Gift Certificate Code* to *Checkout*.


                  > #### Note

                  > * *Gift Certificates* are treated as a payment methods.

                  > * You are not able to purchase a gift certificate with a
                  gift certificate.

                  > * The rate limit is 20/hour (only for unique
                  gift-certificate codes).

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/gift-certificates/{giftCertificateCode}:
              delete:
                tags:
                  - Delete
                  - Gift
                  - Certificate
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                summary: Delete Gift Certificate
                description: >-
                  Deletes an existing *Gift Certificate*.


                  This removes the *Gift Certificate* payment method.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/coupons:
              post:
                tags:
                  - Add
                  - Coupon
                  - To
                  - Checkout
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                summary: Add Coupon to Checkout
                description: >-
                  Adds a *Coupon Code* to *Checkout*.


                  **Required Fields**

                  * couponCode


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/coupons/{couponCode}:
              delete:
                tags:
                  - Delete
                  - Checkout
                  - Coupon
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                summary: Delete Checkout Coupon
                description: >
                  Deletes a *Coupon Code* from *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/store-credit:
              post:
                tags:
                  - Add
                  - Store
                  - Credit
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                summary: Add Store Credit
                description: >-
                  Applies any available store credit to a checkout. As on the
                  storefront, all available store credit will be used (up to the
                  value of the order) and no amount need be specified.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.
              delete:
                tags:
                  - Remove
                  - Store
                  - Credit
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                summary: Remove Store Credit
                description: >-
                  Removes store credit from a checkout.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/spam-protection:
              post:
                tags:
                  - Checkout
                  - Spam
                  - Protection
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                  - Spam
                  - Protection
                summary: Checkout Spam Protection
                description: >-
                  Verifies if checkout is created by human.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-checkouts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-checkouts-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---