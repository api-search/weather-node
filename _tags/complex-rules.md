---
name: Complex Rules
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/complex-rules.png
url: https://example.com/apis/complex-rules.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Complex Rules
apis:
  - aid: bigcommerce:catalog-products
    name: Catalog - Products
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
            title: Catalog - Products
            version: ''
          tags:
            - name: Batch metafields
            - name: Products
            - name: Bulk Pricing Rules
            - name: Complex Rules
            - name: Custom Fields
            - name: Images
            - name: Metafields
            - name: Reviews
            - name: Videos
            - name: Channel Assignments
            - name: Category Assignments
            - name: Summary
          paths:
            /catalog/products:
              get:
                tags:
                  - Get
                  - All
                  - Products
                  - Catalog
                  - Products
                summary: Get All Products
                description: >-
                  Returns a list of **Products**. Optional filter parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Products
                  - Batch)
                  - Catalog
                  - Products
                summary: Update Products (Batch)
                description: >-
                  Updates products in batches. Batches are limited to 10
                  products.


                  **Required Fields**

                  * `id` - product `id` is required for batch updates to
                  products.


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`
              post:
                tags:
                  - Create
                  - Product
                  - Catalog
                  - Products
                summary: Create a Product
                description: >-
                  Creates a *Product*. Only one product can be created at a
                  time; however, you can create multiple product variants using
                  the `variants` array.


                  **Required Fields:**

                  - `name`

                  - `type`

                  - `weight`

                  - `price`


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`


                  **Limits**

                  - 250 characters product name length.

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Usage Notes**

                  * You can create multiple product variants using the
                  `variants` array.

                  * This endpoint accepts a `video` array. To create a product
                  video that accepts a `video` object, see [Create a Product
                  Video](/docs/rest-catalog/products/videos#create-a-product-video)
                  for information.
              delete:
                tags:
                  - Delete
                  - Products
                  - Catalog
                  - Products
                summary: Delete Products
                description: >-
                  To delete *Product* objects, you must include a filter. This
                  prevents inadvertently deleting all *Product* objects in a
                  store.


                  > #### Note

                  > The maximum number of products you can delete at one time is
                  250.


                  **Example**:

                  To delete products with IDs 1,2 and 3, use `DELETE
                  /v3/catalog/products?id:in=1,2,3`.
              parameters:
                - null
            /catalog/products/{product_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Get a Product
                description: >-
                  Returns a single *Product*. Optional parameters can be passed
                  in.
              put:
                tags:
                  - Update
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Update a Product
                description: >
                  Updates a *Product*.


                  **Limits**

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Read-Only Fields**

                  - id

                  - date_created

                  - date_modified

                  - calculated_price

                  - base_variant_id
              delete:
                tags:
                  - Delete
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Delete a Product
                description: Deletes a *Product*.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Images
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Get All Product Images
                description: >-
                  Returns a list of *Product Images*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Create a Product Image
                description: >-
                  Creates a *Product Image*.

                   **Required Fields**
                  - `image_file`, or

                  - `image_url`


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - For file uploads, use the `multipart/form-data` media type.

                  - You can create only one image at a time. A product can have
                  up to 1000 images.

                  - Supported image file types are BMP, GIF, JPEG, PNG, WBMP,
                  XBM, and WEBP.

                  - Each image file or image uploaded by URL can be up to 8 MB.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images/{image_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Get a Product Image
                description: >-
                  Returns a single *Product Image*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Update a Product Image
                description: >-
                  Updates a *Product Image*.


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - Each image file or image uploaded by URL can be up to 8 MB.

                  - For file uploads, send a POST request using the
                  `multipart/form-data` media type
              delete:
                tags:
                  - Delete
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Delete a Product Image
                description: Deletes a *Product Image*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/videos:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Videos
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Get All Product Videos
                description: >-
                  Returns a list of *Product Videos*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Create a Product Video
                description: |-
                  Creates a *Product Video*.

                  **Required Fields**
                  * video_id

                  **Read-Only Fields**
                  * id

                  Publicly accessible URLs are valid parameters.
                  Videos must be loaded through YouTube at this time.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/videos/{id}:
              get:
                tags:
                  - Get
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Get a Product Video
                description: >-
                  Returns a single *Product Video*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Update a Product Video
                description: |-
                  Updates a *Product Video.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Delete a Product Video
                description: Deletes a *Product Video*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/complex-rules:
              get:
                tags:
                  - Get
                  - Complex
                  - Rules
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Get Complex Rules
                description: >-
                  Returns a list of all product *Complex Rules*. Optional
                  parameters may be passed in.
              post:
                tags:
                  - Create
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Create a Complex Rule
                description: |-
                  Creates a product *Complex Rule*.

                  **Required Fields**
                  - modifier_id
                  - modifier_value_id
                  - variant_id

                  **Read-Only Fields**
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/complex-rules/{complex_rule_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Get a Product Complex Rule
                description: >-
                  Returns a single *Complex Rule*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Update a Product Complex Rule
                description: |-
                  Updates a *Complex Rule*.

                  **Required Fields**:
                  - none

                  **Read-Only Fields**:
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              delete:
                tags:
                  - Delete
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Delete a Product Complex Rule
                description: Deletes a product *Complex Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/custom-fields:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Fields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Get Product Custom Fields
                description: >-
                  Returns a list of product *Custom Fields*. You can pass in
                  optional parameters.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              post:
                tags:
                  - Create
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Create a Product Custom Field
                description: >-
                  Creates a *Custom Field*.


                  **Required Fields:**

                  - name

                  - value


                  **Name-Value Pair Uniqueness**

                  - Every name-value pair must be unique inside a product.


                  **Read-Only:**

                  - id


                  **Limits**

                  - 200 custom fields per product limit.

                  - 250 characters per custom field limit.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
            /catalog/products/{product_id}/custom-fields/{custom_field_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Get a Product Custom Field
                description: >
                  Returns a *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              put:
                tags:
                  - Update
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Update a Product Custom Field
                description: |-
                  Updates a *Custom Field*.

                  **Required Fields**
                  - none

                  **Name-Value Pair Uniqueness**
                  - Every name-value pair must be unique inside a product.

                  **Read-Only**
                  - id

                   **Limits**
                  - 200 custom fields per product limit.
                  - 250 characters per custom field limit.
                  - 40 concurrent requests default rate limit.
              delete:
                tags:
                  - Delete
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Delete a Product Custom Field
                description: >-
                  Deletes a product *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/bulk-pricing-rules/{bulk_pricing_rule_id}:
              get:
                tags:
                  - Get
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Get a Bulk Pricing Rule
                description: >-
                  Returns a single *Bulk Pricing Rule*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Update a Bulk Pricing Rule
                description: |-
                  Updates a *Bulk Pricing Rule*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  - id
              delete:
                tags:
                  - Delete
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Delete a Bulk Pricing Rule
                description: Deletes a *Bulk Pricing Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/metafields:
              get:
                tags:
                  - Get
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Get Product Metafields
                description: >-
                  Returns a list of *Product Metafields*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Create a Product Metafield
                description: >-
                  Creates a *Product Metafield*.


                  **Required Fields:**

                  * permission_set

                  * namespace

                  * key

                  * value


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Get a Product Metafield
                description: >-
                  Returns a single *Product Metafield*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Update a Product Metafield
                description: "Updates a *Product Metafield*.\n\n**Required Fields**\n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified using the API account that created the metafield:\n\t* `namespace`\n\t* `key`\n\t* `permission_set`\n\t* `value`\n\n**Usage Notes**\n* Attempting to modify the `namespace`, `key`, `permission_set`, or `value` field using an API account different from the one used to create those metafields will result in a `403` error message. "
              delete:
                tags:
                  - Delete
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Product Metafield
                description: Deletes a *Product Metafield*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/reviews:
              get:
                tags:
                  - Get
                  - Product
                  - Reviews
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Get Product Reviews
                description: >-
                  Returns a list of all *Product Reviews*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Create a Product Review
                description: |-
                  Creates a *Product Review*.

                  **Required Fields**
                  - title
                  - date_reviewed

                  **Read-Only Fields**
                  * id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/reviews/{review_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Get a Product Review
                description: >-
                  Returns a single *Product Review*. Optional parameters maybe
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Update a Product Review
                description: |-
                  Updates a *Product Review*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Delete a Product Review
                description: Deletes a *Product Review*.
              parameters:
                - null
                - null
                - null
            /catalog/products/channel-assignments:
              get:
                summary: Get Products Channel Assignments
                description: Returns a list of products channel assignments.
                tags:
                  - Get
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              put:
                summary: Create Products Channel Assignments
                description: Creates products channel assignments.
                tags:
                  - Create
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              delete:
                summary: Delete Products Channel Assignments
                description: >-
                  Delete products channel assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              parameters:
                - null
            /catalog/products/category-assignments:
              get:
                summary: Get Products Category Assignments
                description: Returns a list of products category assignments.
                tags:
                  - Get
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              put:
                summary: Create Products Category Assignments.
                description: Creates products category assignments.
                tags:
                  - Create
                  - Products
                  - Category
                  - Assignments.
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              delete:
                summary: Delete Products Category Assignments
                description: >-
                  Deletes products category assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              parameters:
                - null
            /catalog/summary:
              get:
                tags:
                  - Get
                  - Catalog
                  - Summary
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                summary: Get a Catalog Summary
                description: >-
                  Returns a lightweight inventory summary from the BigCommerce
                  Catalog.


                  The inventory summary includes:

                  * "inventory_count"

                  * "variant_count"

                  * "inventory_value"

                  * "highest_variant_price"

                  * "average_variant_price"

                  * "lowest_variant_price"

                  * "oldest_variant_date"

                  * "newest_variant_date"

                  * "primary_category_id"

                  * "primary_category_name"
              parameters:
                - null
            /catalog/products/metafields:
              get:
                summary: Get All Product Metafields
                tags:
                  - Get
                  - All
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Get all product metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Delete all product
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-products-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-products-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---