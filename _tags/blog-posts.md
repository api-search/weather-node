---
name: Blog Posts
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/blog-posts.png
url: https://example.com/apis/blog-posts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Blog Posts
apis:
  - aid: bigcommerce:content
    name: Content
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
            title: Content
            version: ''
          tags:
            - name: Blog Posts
            - name: Blog Tags
            - name: Pages
            - name: Redirects
          paths:
            /blog/tags:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Blog
                  - Tags
                  - Blog
                  - Tags
                summary: Get All Blog Tags
                description: Returns a list of *Blog Tags*.
            /blog/posts:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Blog
                  - Posts
                  - Blog
                  - Tags
                  - Posts
                summary: Get All Blog Posts
                description: >-
                  Returns all *Blog Posts*. Default sorting is by
                  published_date, beginning with the most recent post.
              post:
                tags:
                  - Create
                  - Blog
                  - Post
                  - Blog
                  - Tags
                  - Posts
                summary: Create a Blog Post
                description: >-
                  Creates a *Blog Post*.


                  **Required Fields**

                  *   `title`

                  *   `body`


                  **Notes**


                  * When including `published_date` in a request, supply it as a
                  flat date string (not an object) in valid <a
                  href="http://tools.ietf.org/html/rfc2822#section-3.3"
                  target="_blank">RFC 2822</a>. The following example request
                  includes a `published_date` in RFC 2822 format.

                  * Blog posts default to draft status. To publish blog posts to
                  the storefront, set the `is_published` property to `true`.

                  * If a custom URL is not provided, the post’s URL will be
                  generated based on the value of `title`.
              delete:
                tags:
                  - Delete
                  - Blog
                  - Posts
                  - Blog
                  - Tags
                  - Posts
                summary: Delete Blog Posts
                description: Deletes a page of `Blog Posts`.
            /blog/posts/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Blog
                  - Post
                  - Blog
                  - Tags
                  - Posts
                  - Id
                summary: Get a Blog Post
                description: Returns a single *Blog Post*.
              put:
                tags:
                  - Update
                  - Blog
                  - Post
                  - Blog
                  - Tags
                  - Posts
                  - Id
                summary: Update a Blog Post
                description: >-
                  Updates a *Blog Post*.


                  **Notes**


                  * To include `published_date` in a request, provide a flat
                  date string (not an object) in valid <a
                  href="http://tools.ietf.org/html/rfc2822#section-3.3"
                  target="_blank">RFC 2822</a>. The following example request
                  includes a `published_date` in RFC 2822 format.


                  * Blog posts default to draft status. To publish blog posts to
                  the storefront, set the `is_published` property to `true`.
              delete:
                tags:
                  - Delete
                  - Blog
                  - Post
                  - Blog
                  - Tags
                  - Posts
                  - Id
                summary: Delete a Blog Post
                description: Deletes a *Blog Post*.
            /blog/posts/count:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Count
                  - Of
                  - All
                  - Blog
                  - Posts
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                summary: Get A Count of All Blog Posts
                description: Returns a count of all *Blog Posts*.
            /pages:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Pages
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                summary: Get All Pages
                description: >
                  Returns a list of *Pages*. Default sorting is by
                  auto-generated ID from oldest to newest.


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To get one or more pages, use Pages V3ʼs [Get
                  pages](/docs/rest-content/pages#get-pages) endpoint. To get a
                  single page, use Pages V3ʼs [Get a
                  page](/docs/rest-content/pages#get-a-page) endpoint.
              post:
                tags:
                  - Create
                  - Page
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                summary: Create a Page
                description: >-
                  Creates a *Page*. The request payload limit is 1MB.


                  **Required Fields**

                  *   `type`

                  *   `name`

                  *   `link` (for a page of `type: link`)

                  *   `feed` (for a page of `type: rss_feed`)

                  *   `body` (for a page of `type: raw`)


                  **Read Only Fields**

                  *   `id`


                  ## Content Type


                  The default value for `content_type` is `text/html`; however,
                  if `page_type` is set to `raw`, `content_type` can be changed
                  to `text/javascript` or `application/json`. Updating this
                  field allows you to place a JavaScript or a JSON file in the
                  root directory.


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To create one or more pages, use Pages V3ʼs [Create
                  pages](/docs/rest-content/pages#create-pages) endpoint. 
            /pages/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Page
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                summary: Get A Page
                description: >
                  Returns a *Page*. 


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To get a single page, use Pages V3ʼs [Get a
                  page](/docs/rest-content/pages#get-a-page) endpoint.
              put:
                tags:
                  - Update
                  - Page
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                summary: Update a Page
                description: >-
                  Updates a *Page*. The request payload limit is 1MB.


                  **Read Only Fields**

                  * id


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To update multiple pages, use Pages V3ʼs [Update
                  pages](/docs/rest-content/pages#update-pages) endpoint. To
                  update a single page, use Pages V3ʼs [Update a
                  page](/docs/rest-content/pages#update-a-page) endpoint.
              delete:
                tags:
                  - Delete
                  - Page
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                summary: Delete a Page
                description: >
                  Deletes a *Page*.


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To delete multiple pages, use Pages V3ʼs [Delete
                  pages](/docs/rest-content/pages#delete-pages) endpoint. To
                  delete a single page, use Pages V3ʼs [Delete a
                  page](/docs/rest-content/pages#delete-a-page) endpoint. 
            /redirects:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Redirects
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Get All Redirects
                description: >-
                  Returns a list all *Redirect URLs*. 


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To get redirect URLs, use Redirects V3ʼs [Get
                  redirects](/docs/rest-management/redirects#get-redirects)
                  endpoint.
              post:
                tags:
                  - Create
                  - Redirect
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Create a Redirect
                description: >-
                  Creates a *Redirect URL*.


                  **Required Fields**

                  *   path

                  *   forward


                  **Read Only**

                  *   url



                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To upsert new redirect data, use Redirects V3ʼs [Upsert
                  redirects](/docs/rest-management/redirects#upsert-redirects)
                  endpoint.
              delete:
                tags:
                  - Delete
                  - All
                  - Redirects
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Delete All Redirects
                description: >-
                  By default, it deletes all *Redirect URLs* in a store. 



                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To delete redirect URLs, use Redirects V3ʼs [Delete
                  redirects](/docs/rest-management/redirects#delete-redirects)
                  endpoint.
            /redirects/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Redirect
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Get a Redirect
                description: >-
                  Returns a single *Redirect URL*.


                  > #### Warning

                  > **Deprecated** 

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To get a redirect URL, use Redirects V3ʼs [Get
                  redirects](/docs/rest-management/redirects#get-redirects)
                  endpoint.
              put:
                tags:
                  - Update
                  - Redirect
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Update a Redirect
                description: >-
                  Updates a *Redirect URL*.


                  **Required Fields**

                  *   path

                  *   forward


                  **Read Only Fields**

                  *   url



                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To update redirect data, use Redirects V3ʼs [Upsert
                  redirects](/docs/rest-management/redirects#upsert-redirects)
                  endpoint.
              delete:
                tags:
                  - Delete
                  - Redirect
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Delete a Redirect
                description: >-
                  Deletes a *Redirect URL*.


                  > #### Warning

                  > **Deprecated** 

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To delete a redirect URL, use Redirects V3ʼs [Delete
                  redirects](/docs/rest-management/redirects#delete-redirects)
                  endpoint.
            /redirects/count:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Count
                  - Of
                  - Redirects
                  - Blog
                  - Tags
                  - Posts
                  - Id
                  - Count
                  - Pages
                  - Redirects
                summary: Get a Count of Redirects
                description: >-
                  Gets a count of *Redirect URLs* in a store.


                  > #### Warning

                  > **Deprecated**

                  > * This API operation is deprecated. Avoid using this API
                  operation if possible. It will be removed in a future version.

                  > * To get a count of redirects, use the `meta` object data
                  returned with the Redirects V3ʼs [Get
                  redirects](/docs/rest-management/redirects#get-redirect
    overlays:
      - type: APIs.io Search
        url: overlays/content-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/content-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---