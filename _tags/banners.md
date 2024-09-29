---
name: Banners
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/banners.png
url: https://example.com/apis/banners.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Banners
apis:
  - aid: bigcommerce:marketing
    name: Marketing
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
            title: Marketing
            version: ''
          tags:
            - name: Banners
            - name: Coupons
            - name: Gift Certificates
          paths:
            /coupons:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Coupons
                  - Coupons
                summary: Get All Coupons
                description: >-
                  Returns a list of *Coupons*. Default sorting is by
                  coupon/discount id, from lowest to highest. You can pass in
                  optional filter parameters. We recommended using
                  `?min_id=x&limit=y` to paginate through a large set of data
                  because it offers better performance.


                  ## Usage Notes


                  Available types for `type` and `exclude_type` filters:


                  |Type|

                  |-|

                  |`per_item_discount`|

                  |`percentage_discount`|

                  |`per_total_discount`|

                  |`shipping_discount`|

                  |`free_shipping`|

                  |`promotion`|


                  Coupons with `type=promotion` will not populate usable data
                  for the following fields but instead be set to the following
                  default values:


                  ```json

                  ...

                  amount : 0.0000

                  min_purchase: 0.0000

                  applies_to

                  restricted_to: []

                  shipping_methods : null

                  ...

                  ```
              post:
                tags:
                  - Create
                  - New
                  - Coupon
                  - Coupons
                summary: Create a New Coupon
                description: >-
                  Creates a *Coupon*.


                  **Required Fields**

                  *   `name`

                  *   `code`

                  *   `type`

                  *   `amount`

                  *   `applies_to`


                  **Read Only Fields**

                  *   `id`

                  *   `num_uses`


                  **Notes**


                  The coupon type can be one of the following:


                  *   `per_item_discount`

                  *   `per_total_discount`

                  *   `shipping_discount`

                  *   `free_shipping`

                  *   `percentage_discount`


                  Legacy coupon codes only work with the store's default
                  currency. Applying a coupon with any other currency other than
                  the store's default will result in the error: "Coupons only
                  apply to default currency."
              delete:
                tags:
                  - Delete
                  - All
                  - Coupons
                  - Coupons
                summary: Delete All Coupons
                description: >
                  ## Usage Notes

                  * Deleting a coupon via this endpoint will delete the coupon
                  but not the promotion it is attached to
            /coupons/count:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Count
                  - Of
                  - Coupons
                  - Coupons
                  - Count
                summary: Get a Count of Coupons
                description: Returns a count of all *Coupons* in the store.
            /coupons/{id}:
              parameters:
                - null
                - null
              put:
                tags:
                  - Update
                  - Coupon
                  - Coupons
                  - Count
                  - Id
                summary: Update a Coupon
                description: >-
                  Updates a *Coupon*.



                  **Read Only Fields**


                  * `id`

                  * `num_uses`

                  * `date_created`


                  **Notes**


                  If the `applies_to` value is cleared, you can restore it to
                  the coupon by reapplying the `applies_to` value in a new `PUT`
                  request.
              delete:
                tags:
                  - Delete
                  - Coupon
                  - Coupons
                  - Count
                  - Id
                summary: Delete a Coupon
                description: Deletes a *Coupon*.
            /banners:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Banners
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Get All Banners
                description: >-
                  Returns a list of *Banners*. Default sorting is by banner id,
                  from lowest to highest.
              post:
                tags:
                  - Create
                  - Banner
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Create a Banner
                description: |-
                  Creates a *Banner*.

                  **Required Fields**
                  * name
                  * content
                  * page
                  * location
                  * date_type

                  **Read Only Fields**
                  * date_created
                  * id
              delete:
                tags:
                  - Delete
                  - All
                  - Banners
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Delete All Banners
                description: By default, it deletes all *Banners*.
            /banners/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Banner
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Get a Banner
                description: Returns a single *Banner*
              put:
                tags:
                  - Update
                  - Banner
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Update a Banner
                description: |-
                  Updates a *Banner*.

                  **Read Only Fields**
                  * date_created
                  * id
              delete:
                tags:
                  - Delete
                  - Banner
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Delete a Banner
                description: Deletes a *Banner*.
            /banners/count:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Count
                  - Of
                  - Store
                  - Banners
                  - Coupons
                  - Count
                  - Id
                  - Banners
                summary: Get a Count of Store Banners
                description: Returns a count of *Banners*.
            /gift_certificates/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Gift
                  - Certificate
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Get a Gift Certificate
                description: Returns a single *Gift Certificate*.
              put:
                tags:
                  - Update
                  - Gift
                  - Certificate
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Update a Gift Certificate
                description: |-
                  Updates a *Gift Certificate*.

                  **Read Only Fields**
                  * id
                  * order_id
              delete:
                tags:
                  - Delete
                  - Gift
                  - Certificate
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Delete a Gift Certificate
                description: Deletes a *Gift Certificate*.
            /gift_certificates:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Gift
                  - Certificates
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Get All Gift Certificates
                description: >-
                  Returns a list of *Gift Certificates*. Optional filter
                  parameters can be passed in.


                  Default sorting is by gift-certificate id, from lowest to
                  highest.


                  The maximum limit is 250. If a limit isn’t provided, up to 50
                  gift_certificates are returned by default.
              post:
                tags:
                  - Create
                  - Gift
                  - Certificate
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Create a Gift Certificate
                description: >-
                  Creates a *Gift Certificate*.



                  **Required Fields**

                  * to_name

                  * to_email

                  * from_name

                  * from_email

                  * amount


                  **Read Only Fields**

                  * id

                  * order_id


                  **Notes**


                  When a gift certificate is created through the API, no email
                  notification is triggered to the specified recipient.
              delete:
                tags:
                  - Delete
                  - All
                  - Gift
                  - Certificates
                  - Coupons
                  - Count
                  - Id
                  - Banners
                  - Gift_certificates
                summary: Delete All Gift Certificates
                description: By default, it deletes all *Gift Ce
    overlays:
      - type: APIs.io Search
        url: overlays/marketing-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/marketing-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---