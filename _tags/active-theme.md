---
name: Active Theme
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/active-theme.png
url: https://example.com/apis/active-theme.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Active Theme
apis:
  - aid: bigcommerce:channels
    name: Channels
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
          openapi: 3.0.0
          info:
            version: ''
            title: Channels
          tags:
            - name: Batch metafields
            - name: Channels
            - name: Metafields
            - name: Menus
            - name: Active Theme
            - name: Currency Assignments
            - name: Listings
            - name: Site
            - name: Site Checkout URL
          paths:
            /channels:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Channels
                summary: Get All Channels
                description: >-
                  Returns a list of *Channels*.


                  Will always return the default BigCommerce storefront with an
                  ID of `1`. This storefront is created by default when you
                  provision a BigCommerce store.
              post:
                tags:
                  - Create
                  - Channel
                  - Channels
                summary: Create a Channel
                description: Creates a *Channel*.
            /channels/{channel_id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Channels
                  - Channel_id
                summary: Get a Channel
                description: >-
                  Returns a *Channel*. Channel ID `1` returns the default
                  BigCommerce storefront.
              put:
                tags:
                  - Update
                  - Channel
                  - Channels
                  - Channel_id
                summary: Update a Channel
                description: >-
                  Updates a *Channel*.


                  ## Updatable Fields


                  The following fields can be updated.

                  * `name`

                  * `external_id`

                  * `status`

                  * `is_listable_from_ui`

                  * `is_visible`

                  * `config_meta`



                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * `platform` and `type` cannot be updated after a channel is
                  created.

                  > * A channel with status `deleted` or `terminated` cannot be
                  updated.
            /channels/{channel_id}/active-theme:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Active
                  - Theme
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                summary: Get a Channel Active Theme
                description: |-
                  Returns details of the theme active on the specified channel.
                  Does not support active Blueprint (legacy) themes.
            /channels/currency-assignments:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get All Channels Currency Assignments
                description: Returns a list of currency assignments for all channels.
              post:
                tags:
                  - Create
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Multiple Channels Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Multiple Channels Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
            /channels/{channel_id}/currency-assignments:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get Channel Currency Assignments
                description: Returns a list of currency assignments for a specific channel.
              post:
                tags:
                  - Create
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Channel Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Channel Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              delete:
                tags:
                  - Delete
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Delete Channel Currency Assignments
                description: >-
                  Deletes currency assignments for a specific channel. Once
                  done, this channel will inherit the store’s currency settings.
            /channels/{channel_id}/listings:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Get Channel Listings
                description: >-
                  Returns a list of all *Channel Listings* for a specific
                  channel. Note that if the *Channel* is not found or there is
                  no listing associated to the *Channel*, it will return a 200
                  response with empty data.
              post:
                tags:
                  - Create
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Create Channel Listings
                description: Creates one or more *Channel Listings* for a specific channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Update Channel Listings
                description: >-
                  Updates one or more *Channel Listings* for a specific channel.


                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * If a new variant is provided, the API will append the
                  variant to the list. If a variant already exists, the API will
                  update the existing variant. Other variants that are not
                  provided in the payload remains unchanged.

                  > * If `listing_id` does not exist, the API will return a 200
                  response with empty data.

                  > * `listing_id` is required and cannot be less than or equal
                  to zero.

                  > * `product_id` cannot be updated after a channel listing is
                  created.

                  > * `product_id` of a variant must match the `product_id` of
                  the channel listing.
            /channels/{channel_id}/listings/{listing_id}:
              parameters:
                - null
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listing
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                summary: Get a Channel Listing
                description: Returns a *Channel Listing* for a specific channel.
            /channels/{channel_id}/site/checkout-url:
              parameters:
                - null
                - null
              put:
                summary: Upsert a Siteʼs Checkout URL
                tags:
                  - Upsert
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Creates or updates (upserts) a siteʼs checkout URL
              delete:
                summary: Delete a Siteʼs Checkout URL
                description: >-
                  Deletes a siteʼs checkout URL. After deletion, a shared
                  checkout URL is used.
                tags:
                  - Delete
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
            /channels/{channel_id}/site:
              parameters:
                - null
                - null
              get:
                summary: Get a Channel Site
                description: |
                  Alias of `GET /sites?channel_id=channel_id`

                  Returns site data for the specified channel.
                tags:
                  - Get
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
              put:
                summary: Update a Channel Site
                tags:
                  - Update
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Updates a site for provided channel.
              post:
                summary: Create a Channel Site
                tags:
                  - Create
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Alias of POST `/sites`. Creates a site for provided channel.
              delete:
                description: Deletes the Channelʼs site.
                tags:
                  - Delete
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                summary: Delete a Channel Site
            /channels/{channel_id}/channel-menus:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Menus
                description: >
                  Returns list of Control Panel side navigation menus for a
                  channel.
                tags:
                  - Get
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
              post:
                summary: Create Channel Menus
                tags:
                  - Create
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                description: >-
                  Creates or replaces list of control panel side navigation
                  menus for a channel.
              delete:
                description: Deletes control panel side navigation menus for a channel.
                tags:
                  - Delete
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                summary: Delete Channel Menus
            /channels/{channel_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Metafields
                tags:
                  - Get
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Returns a list of metafields on a channel. Optional filter
                  parameters can be passed in.
              post:
                summary: Create a Channel Metafield
                tags:
                  - Create
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Creates a channel metafield.


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, channel, or brand is 250
                  per client ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
            /channels/{channel_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Channel Metafield
                tags:
                  - Get
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Returns a single channel metafield.
              put:
                summary: Update a Channel Metafield
                tags:
                  - Update
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a single channel metafield.


                  **Usage Notes**

                  * Attempting to modify `namespace`, `key`, and
                  `permission_set` fields using a client ID different from the
                  one used to create those metafields will result in a `403`
                  error message. 
              delete:
                summary: Delete a Channel Metafield
                tags:
                  - Delete
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Deletes a single channel metafield.
            /channels/metafields:
              get:
                summary: Get All Channel Metafields
                tags:
                  - Get
                  - All
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Get all channel metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Delete all channel
    overlays:
      - type: APIs.io Search
        url: overlays/channels-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/channels-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---