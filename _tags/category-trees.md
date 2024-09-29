---
name: Category Trees
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/category-trees.png
url: https://example.com/apis/category-trees.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Category Trees
apis:
  - aid: bigcommerce:catalog-category-trees
    name: Catalog - Category Trees
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
            title: Catalog - Category Trees
            version: ''
          tags:
            - name: Category Trees
            - name: Categories
          paths:
            /catalog/trees/categories:
              get:
                summary: Get All Categories
                description: |-
                  Returns a list of categories. 

                  To get a specific category in a tree, provide a category ID.
                tags:
                  - Get
                  - All
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              post:
                summary: Create Categories
                description: |-
                  Creates new categories. 

                  Creating a category requires:
                   - `name`
                   - `tree_id` or `parent_id` 
                tags:
                  - Create
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              put:
                summary: Update Categories
                description: |-
                  Updates existing categories. 

                   To update a specific category in a tree, provide a category id.
                tags:
                  - Update
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              delete:
                summary: Delete Categories
                description: >-
                  Deletes categories. 


                  To delete a specific category in a tree, provide a category
                  ID.
                tags:
                  - Delete
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              parameters:
                - null
            /catalog/trees:
              get:
                summary: Get All Category Trees
                description: Returns a list of *Category Trees*.
                tags:
                  - Get
                  - All
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              put:
                summary: Upsert Category Trees
                description: >
                  Upserts *Category Trees*. 


                  This single endpoint updates and creates category trees. If a
                  tree object contains an ID, it is processed as an update
                  operation using that ID. If you do not provide an ID, a new
                  tree is created. The category tree `name` field is required to
                  create trees, but is not required on the update.


                  **Usage Notes**

                  * `channel_id` is required to create a *Category Tree*. You
                  can assign one `channel_id` to one category tree.
                tags:
                  - Upsert
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              delete:
                summary: Delete Category Trees
                description: >-
                  Deletes *Category Trees*. A filter must be supplied with the
                  endpoint.
                tags:
                  - Delete
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              parameters:
                - null
            /catalog/trees/{tree_id}/categories:
              get:
                summary: Get a Category Tree
                description: Returns a *Category Tree*.
                tags:
                  - Get
                  - Category
                  - Tree
                  - Catalog
                  - Trees
                  - Categories
                  - Tree_id
              parameters:
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-category-trees-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-category-trees-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---