---
name: Cart Items
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cart-items.png
url: https://example.com/apis/cart-items.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cart Items
apis:
  - aid: bigcommerce:storefront-carts
    name: Storefront Carts
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
            title: Storefront Carts
          tags:
            - name: Cart
            - name: Cart Items
            - name: Cart Currency
          paths:
            /carts:
              get:
                tags:
                  - Get
                  - Cart
                  - Carts
                summary: Get a Cart
                description: >-
                  Returns a *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
              post:
                tags:
                  - Create
                  - Cart
                  - Carts
                summary: Create a Cart
                description: >-
                  Creates a *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}:
              delete:
                tags:
                  - Delete
                  - Cart
                  - Carts
                  - Id
                summary: Delete a Cart
                description: >-
                  Deletes a *Cart*. Once a *Cart* has been deleted it can not be
                  recovered.



                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}/items:
              post:
                tags:
                  - Add
                  - Cart
                  - Line
                  - Items
                  - Carts
                  - Id
                  - Items
                summary: Add Cart Line Items
                description: >-
                  Adds a line items to the *Cart*.


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
            /carts/{cartId}/items/{itemId}:
              put:
                tags:
                  - Update
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Item
                summary: Update Cart Line Item
                description: >-
                  Updates a *Cart* line item. Updates an existing, single line
                  item quantity and the price of custom items in a cart.


                  If a modified product or variant needs to be changed or
                  updated, you can remove and re-add the product to the cart
                  with the correct variants using the [Delete Cart Line
                  Item](/docs/rest-storefront/carts/cart-items#delete-cart-line-item)
                  and the [Add Cart Line
                  Items](/docs/rest-storefront/carts/cart-items#add-cart-line-items)
                  endpoints. You can also use carts mutations that are part of
                  the [GraphQL Storefront
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
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Item
                summary: Delete Cart Line Item
                description: >-
                  Deletes a *Cart* line item.


                  Removing the last `line_item` in the *Cart* deletes the
                  *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}/currency:
              post:
                tags:
                  - Update
                  - Cart
                  - Currency
                  - Carts
                  - Id
                  - Items
                  - Item
                  - Currency
                summary: Update Cart Currency
                description: >-
                  Update currency of the *Cart*. 

                  Promotions and gift certificates that don't apply to the new
                  currency will be removed from your cart.

                  You cannot update the cart currency if the draft order cart or
                  the cart contains a manual discount.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-carts-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---