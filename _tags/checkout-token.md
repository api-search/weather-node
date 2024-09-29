---
name: Checkout Token
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/checkout-token.png
url: https://example.com/apis/checkout-token.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Checkout Token
apis:
  - aid: bigcommerce:checkouts
    name: Checkouts
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
            title: Checkouts
          tags:
            - name: Checkout
            - name: Checkout Billing Address
            - name: Checkout Consignments
            - name: Checkout Coupons
            - name: Checkout Discounts
            - name: Checkout Orders
            - name: Checkout Settings
            - name: Checkout Token
          paths:
            /checkouts/{checkoutId}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Checkout
                  - Id
                summary: Get a Checkout
                description: |-
                  Returns a *Checkout*.

                  **Notes**

                  The cart ID and checkout ID are the same.
              put:
                tags:
                  - Update
                  - Customer
                  - Messages
                  - Id
                summary: Update Customer Messages
                description: |-
                  Change customer message pertaining to an existing *Checkout*.

                  **Limits:**
                  * 2000 characters for customer message
            /checkouts/{checkoutId}/discounts:
              post:
                tags:
                  - Add
                  - Discount
                  - To
                  - Checkout
                  - Id
                  - Discounts
                summary: Add Discount to Checkout
                description: >-
                  Adds a discount to an existing *checkout*.


                  This discount only applies to `line_items`. When you call this
                  API, you clear out all existing discounts applied to line
                  items, including product and order-based discounts.


                  This endpoint splits the discount between line items based on
                  the item value.


                  Required Fields

                  * discounted_amount
            /checkouts/{checkoutId}/billing-address:
              post:
                tags:
                  - Add
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Discounts
                  - Billing
                  - Address
                summary: Add Checkout Billing Address
                description: |-
                  Adds a billing address to an existing checkout.

                  **Required Fields**
                  * email
                  * country_code
            /checkouts/{checkoutId}/billing-address/{addressId}:
              put:
                tags:
                  - Update
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Discounts
                  - Billing
                  - Address
                summary: Update Checkout Billing Address
                description: Updates an existing billing address on a checkout.
            /checkouts/{checkoutId}/consignments:
              post:
                tags:
                  - Add
                  - Consignment
                  - To
                  - Checkout
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                summary: Add Consignment to Checkout
                description: >-
                  Adds a new consignment to a checkout.



                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.


                  For more information about working with consignments, see
                  [Checkout
                  consignment](/docs/storefront/cart-checkout/guide/consignments).  


                  Though the only required `address` properties to create a
                  consignment are `email` and `country_code`, to successfully
                  [create an
                  order](/docs/rest-management/checkouts/checkout-orders#create-an-order)
                  the `address` requires the following properties:

                  * `first_name`

                  * `last_name`

                  * `address1`

                  * `city`

                  * `country`

                  * `email`

                  * `country_code`


                  Depending on the country, the following `address` properties
                  may also be required:


                  * `postal_code`

                  * `state_or_province`
            /checkouts/{checkoutId}/consignments/{consignmentId}:
              parameters:
                - null
                - null
                - null
              put:
                tags:
                  - Update
                  - Checkout
                  - Consignment
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Update Checkout Consignment
                description: >-
                  Updates an existing consignment. The address, line item IDs,
                  and shipping option ID can be updated using this endpoint.


                  Use a separate `PUT` request to update the shipping option IDs
                  if you also want to update the address and line item IDs.  


                  To add new shipping options, complete the following steps: 

                  * Use the [Add Consignment to
                  Checkout](/docs/rest-management/checkouts/checkout-consignments#add-consignment-to-checkout)
                  endpoint to add a new [consignment] to a checkout. 

                  * Assign a shipping option to the new consignment by sending a
                  `PUT` request to update the consignment's `shipping_option_id`
                  with a returned value from
                  `data.consignments[N].available_shipping_option[N].id`
                  obtained in the [Add Consignment to
                  Checkout](/docs/rest-management/checkouts/checkout-consignments#add-consignment-to-checkout)
                  endpoint. 


                  To update an existing address and line item IDs, assign a new
                  address and line item IDs by sending a `PUT` request.


                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.



                  2. Assign a shipping option to the new consignment by sending
                  a `PUT` request to update the consignment's
                  `shipping_option_id` with a returned value from
                  `data.consignments[N].available_shipping_option[N].id`
                  obtained in Step One. 
              delete:
                tags:
                  - Delete
                  - Checkout
                  - Consignment
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Delete Checkout Consignment
                description: >-
                  Removes an existing consignment from a checkout.


                  Removing the last consignment will remove the cart from the
                  customer it is assigned to. Create a new redirect URL for the
                  customer so they can access the cart again.
            /checkouts/{checkoutId}/coupons:
              post:
                tags:
                  - Add
                  - Coupon
                  - To
                  - Checkout
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                summary: Add Coupon to Checkout
                description: |-
                  Adds a coupon code to a checkout.

                  **Required Fields**
                  * coupon_code

                  **Limits**
                  * Coupon codes have a 50-character limit. 
            /checkouts/{checkoutId}/coupons/{couponCode}:
              delete:
                tags:
                  - Delete
                  - Checkout
                  - Coupon
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                  - Coupon
                  - Code
                summary: Delete Checkout Coupon
                description: Deletes a coupon code from a checkout.
            /checkouts/{checkoutId}/orders:
              post:
                tags:
                  - Create
                  - An
                  - Order
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                  - Coupon
                  - Code
                  - Orders
                summary: Create an Order
                description: >-
                  Creates an order.


                  ## Usage notes

                  * Orders created will be set to incomplete order status.

                  * You can create as many orders from the same order (cart) as
                  you want.

                  * Order duplication copies the existing order, assigns a new
                  order number, and sets the new order status to `incomplete`.

                  * Once the order is paid, the cart is deleted.

                  * Cart deletion occurs if you are using BigCommerce to accept
                  payments on orders.
            /checkouts/settings:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Checkout
                  - Settings
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                  - Coupon
                  - Code
                  - Orders
                  - Checkouts
                  - Settings
                summary: Get Checkout Settings
                description: Get checkout settings
              put:
                tags:
                  - Update
                  - Checkout
                  - Settings
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                  - Coupon
                  - Code
                  - Orders
                  - Checkouts
                  - Settings
                summary: Update Checkout Settings
                description: Update checkout settings
            /checkouts/{checkoutId}/token:
              parameters:
                - null
                - null
              post:
                tags:
                  - Create
                  - Checkout
                  - Token
                  - Id
                  - Discounts
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Coupons
                  - Coupon
                  - Code
                  - Orders
                  - Checkouts
                  - Settings
                  - Token
                summary: Create Checkout Token
                description: >-
                  Use the checkout token to display a confirmation page for a
                  guest shopper.

                  **Usage Notes** * The response from performing this POST
                  request is a checkout token. * The checkout token is a
                  single-use token that is not order-dependent. You cannot
                  create this token after finalizing an order. * After
                  completing the order, you can redirect the shopper to
                  /order-confirmation/{orderId}?t={checkoutToken}. * After token
                  validation, the /order-confirmation/{orderId} page displays. *
                  The `ORDER_TOKEN` should match the order or the logged-in
                  customer can acces
    overlays:
      - type: APIs.io Search
        url: overlays/checkouts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/checkouts-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---