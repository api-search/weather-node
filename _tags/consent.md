---
name: Consent
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/consent.png
url: https://example.com/apis/consent.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Consent
apis:
  - aid: bigcommerce:storefront-cookie-consent
    name: Storefront Cookie Consent
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
            title: Storefront Cookie Consent
          tags:
            - name: Consent
          paths:
            /consent:
              post:
                summary: Set Cookie Consent Preferences
                tags:
                  - Set
                  - Cookie
                  - Consent
                  - Preferences
                  - Consent
                description: >
                  Sets the status of a customer's consent to allow data
                  collection by cookies and scripts according to the following
                  consent categories:


                    2. Analytics — These cookies provide statistical information on site usage so the store owner can improve the website over time.  
                    3. Functional — These cookies enable enhanced functionality, such as videos and live chat. If a shopper does not allow these, then some or all of these functions may not work properly. 
                    4. Targeting; Advertising — These cookies allow merchants to create profiles or personalize content to enhance users' shopping experience.
                    
                    
                  This endpoint only works if the cookie consent feature is
                  enabled. It is assumed the shopper has not consented to
                  anything until a value is explicitly set. The request body
                  must be populated with a complete set of allowed and denied
                  categories.


                  Once set, consent preferences will be saved as a cookie for
                  guest shoppers. Consent preferences will be persisted to a
                  shopper's account to be used for future sessions once they
                  have logged in. Consent preferences can also be managed using
                  the [Update customer
                  consent](/docs/rest-management/customers/customer-consent#update-customer-consent)
                  endpoint.   


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 
              parameters: nu
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-cookie-consent-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-cookie-consent-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:customers
    name: Customers
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
            title: Customers V3
          tags:
            - name: Customers
            - name: Consent
            - name: Validate Credentials
            - name: Metafields
            - name: Customer Metafields
            - name: Customer Batch Metafields
            - name: Addresses
            - name: Attributes
            - name: Attribute Values
            - name: Form Fields
            - name: Form Field Values
            - name: Stored Instruments
            - name: Global Settings
            - name: Channel Settings
          paths:
            /customers:
              get:
                description: >-
                  Returns a list of Customers. Optional filter parameters can be
                  passed in.


                  **Notes**


                  Attribute names are not available on the customer object.
                summary: Get All Customers
                tags:
                  - Get
                  - All
                  - Customers
                  - Customers
              post:
                description: >-
                  Creates Customers. Create up to 10 customers in one call.


                  **Required Fields**

                  * last_name

                  * first_name

                  * email


                  **Required Fields Customer Address**

                  * first_name

                  * city

                  * country_code

                  * last_name

                  * address1


                  **Required Fields Attributes**

                  * Attributes must be
                  [created](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute)
                  **BEFORE** creating a customer.

                  * attribute_id

                  * attribute_value -- This is input as a string, regardless of
                  the
                  [Type](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute).


                  **Notes**


                  A customer can be created with global access or
                  channel-specific access.

                  * **Global access:**
                    * Make sure the channel has `allow_global_logins` enabled. This is on by default only for the default storefront. Find more info at [Customer Settings > Channel](/docs/rest-management/customers/customer-settings-channel).
                    * Omit `channel_ids` field, or provide `channel_ids: null`.
                  * **Channel-specific access:**
                    * Provide a `channel_ids` array containing the channels accessible by the customer. This array cannot be empty.
                summary: Create Customers
                tags:
                  - Create
                  - Customers
                  - Customers
              put:
                description: >-
                  Updates Customers. Subresource updates are not supported. Up
                  to 10 customers can be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer* This must be included in the
                  request body


                  **Read Only Fields**

                  * id

                  * registration_ip_address

                  * date_created

                  * date_modified



                  **Notes**


                  * Attributes Values can not be updated using Update a
                  Customer. Use the [Update customer attribute
                  values](/docs/rest-management/customers/customer-attribute-values#upsert-customer-attribute-values)
                  endpoint.

                  * channel_ids -- Updating the list of channels a customer can
                  access may create some side effects in a multi-storefront
                  situation. This list determines which customer account we will
                  use to authenticate a shopper given a channel.
                summary: Update Customers
                tags:
                  - Update
                  - Customers
                  - Customers
              delete:
                description: >-
                  Deletes Customers.


                  **Required Query**

                  * id:in -- ID of the customer


                  **Notes**


                  A query is required to delete customers. If not provided, a
                  204 is returned, with no changes to the data.
                summary: Delete Customers
                tags:
                  - Delete
                  - Customers
                  - Customers
            /customers/addresses:
              get:
                description: >-
                  Returns a list of Customer Addresses. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Addresses
                tags:
                  - Get
                  - All
                  - Customer
                  - Addresses
                  - Customers
                  - Addresses
              post:
                description: >-
                  Creates a Customer Address. Multiple customer addresses can be
                  created in one call.


                  **Required Fields**

                  * **customer_id**

                  * **first_name**

                  * **last_name**

                  * **city**

                  * **country_code**

                  * **address1**


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **customer_id**
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to create an address that already exists will
                  result in no change to the address or custom form field
                  values, an HTTP 200 return code, and the address will be
                  absent from the response body.

                  * The default rate limit for this endpoint is 10 concurrent
                  requests.
                summary: Create a Customer Address
                tags:
                  - Create
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              put:
                description: >-
                  Updates a Customer Address. Multiple customer addresses can be
                  updated in one call.


                  **Required Fields**

                  * **id** -- ID of the *Customer Address*


                  **Limits**

                  * Limit of **3** concurrent requests.


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to update an address such that it becomes
                  identical to another address that already exists will result
                  in no change to the target address or custom form field
                  values. The response will have an HTTP 200 return code, and
                  the address will be absent from the response body.
                summary: Update a Customer Address
                tags:
                  - Update
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              delete:
                description: |-
                  Deletes a Customer Address.

                  **Required Query**
                  * id:in -- ID of the *Customer Address*
                summary: Delete a Customer Address
                tags:
                  - Delete
                  - Customer
                  - Address
                  - Customers
                  - Addresses
            /customers/validate-credentials:
              post:
                tags:
                  - Validate
                  - Customer
                  - Credentials
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                description: >-
                  Validate a customer credentials - This endpoint has special
                  rate limiting protections to protect against abuse.
                summary: Validate a customer credentials
            /customers/settings:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Returns the global-level customer settings.
                summary: Get Customer Settings
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Updates the customer settings on the global level.
                summary: Update Customer Settings
            /customers/settings/channels/{channel_id}:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: |-
                  Returns the customer settings per channel.

                  **Notes**

                   * `null` indicates that there is no override per given channel and values are inherited from the global level.
                summary: Get Customer Settings per Channel
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: >-
                  Update the customer settings per channel


                  **Required Fields**


                  * `channel_id`: Provide a `channel_id` array containing one or
                  more channel IDs. Customers will have access to these channels
                  and no others. This array cannot be empty.


                  **Notes**


                  * Setting `null` will delete override per given channel, and
                  values will be inherited from the global level. Make sure the
                  channel has `allow_global_logins` enabled.
                summary: Update Customer Settings per Channel
              parameters:
                - null
            /customers/attributes:
              get:
                description: >-
                  Returns a list of Customer Attributes. You can pass in
                  optional filter parameters.
                summary: Get All Customer Attributes
                tags:
                  - Get
                  - All
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              post:
                description: >-
                  Creates a Customer Attribute. Multiple customer attributes can
                  be created in one call.


                  **Required Fields**

                  * name

                  * type


                  **Limits**

                  * Limit of 3 concurrent requests.


                  **Notes**


                  Once the data type is set, it cannot be changed. The attribute
                  will need to be deleted then created again with the new data
                  type. This will also delete it from the customer.


                  Customer attributes are created separately from the customer.
                  After the name and type are created, then the attributes can
                  be added to the customer.


                  A store cannot have more than 50 customer attributes.
                summary: Create a Customer Attribute
                tags:
                  - Create
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              put:
                description: >-
                  Updates a Customer Attribute. Multiple customer attributes can
                  be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer Attribute*


                  Once the data type is set, it can not be changed. The
                  attribute will need to be deleted then created again with the
                  new data type. This will also delete it from the customer.


                  **Limits**

                  * Limit of 3 concurrent requests.
                summary: Update a Customer Attribute
                tags:
                  - Update
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              delete:
                description: |-
                  Deletes Customer Attributes from the store.

                  **Required Query**
                  * id:in -- ID of the *Customer Attribute*
                summary: Delete Customer Attributes
                tags:
                  - Delete
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
            /customers/attribute-values:
              get:
                description: >-
                  Returns a list of Customer Attribute Values. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Attribute Values
                tags:
                  - Get
                  - All
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              put:
                description: >-
                  Upserts Customer Attribute Values. Updates the attribute
                  values on the Customer. Multiple customer attribute values can
                  be updated in one call.


                  Upsert checks for an existing record. If there is none, it
                  creates the record, if there is a matching record, it updates
                  that record.


                  **Limits**

                  * 10 per call limit.
                summary: Upsert Customer Attribute Values
                tags:
                  - Upsert
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              delete:
                description: >-
                  Deletes Customer Attribute Values. Deletes the attribute value
                  from the customer.


                  **Required Query**

                  * id:in - ID of the *Customer Attribute Value*
                summary: Delete Customer Attribute Values
                tags:
                  - Delete
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
            /customers/form-field-values:
              get:
                summary: Get Customer Form Field Values
                description: >-
                  Returns a list of form field values for the Customer or
                  Customer Address object.


                  To learn about adding and managing form fields, see [Adding
                  and Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).
                tags:
                  - Get
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
              put:
                summary: Upsert Customer Form Field Values
                description: >-
                  Updates form field values on the Customer or Customer Address
                  objects. Multiple form field values can be updated in one
                  call.


                  Upsert checks for an existing record, if there is none it
                  creates the record, if there is a matching record it updates
                  that record.


                  To learn more about editing form fields, see [Adding and
                  Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).


                  **Limits**

                  * Limit of 10 concurrent requests.
                tags:
                  - Upsert
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
            /customers/{customerId}/consent:
              get:
                description: >-
                  Gets the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Get Customer Consent
                tags:
                  - Get
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              put:
                description: >-
                  Updates the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Update Customer Consent
                tags:
                  - Update
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              parameters:
                - null
            /customers/{customerId}/stored-instruments:
              get:
                summary: Get Stored Instruments
                tags:
                  - Get
                  - Stored
                  - Instruments
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                description: >-
                  Lists all available stored instruments for a customer. This
                  list will include all types of stored instruments namely card,
                  account and bank_account instruments
              parameters:
                - null
            /customers/{customerId}/metafields:
              get:
                summary: Get Customer Metafields
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Gets customer metafields by passing the `customerId` in the
                  query parameters.
              post:
                summary: Create Customer Metafields
                tags:
                  - Create
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Creates Customer metafields by passing the `customerId` in the
                  query parameters.
            /customers/{customerId}/metafields/{metafieldId}:
              get:
                summary: Get Customer Metafields List
                description: >
                  Lists available metafields for a customer. To retrieve the
                  list, use `customerId` and `metafieldId` in the query
                  parameters.
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - List
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >-
                  Updates customer metafields. To update the customer
                  metafields, use 'customerId' and 'metafield' in the query
                  parameters.
              delete:
                summary: Delete Customer Metafields
                tags:
                  - Delete
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >
                  Deletes customer metafields. To delete customer metafields,
                  use 'customerId' and 'metafieldId' in the query parameters.
            /customers/metafields:
              get:
                summary: Get All Customer Metafields
                tags:
                  - Get
                  - All
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Get all customer metafields.
              post:
                summary: Create Multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              put:
                summary: Update Multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Delete all customer
    overlays:
      - type: APIs.io Search
        url: overlays/customers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customers-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:customers
    name: Customers
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
            title: Customers V3
          tags:
            - name: Customers
            - name: Consent
            - name: Validate Credentials
            - name: Metafields
            - name: Customer Metafields
            - name: Customer Batch Metafields
            - name: Addresses
            - name: Attributes
            - name: Attribute Values
            - name: Form Fields
            - name: Form Field Values
            - name: Stored Instruments
            - name: Global Settings
            - name: Channel Settings
          paths:
            /customers:
              get:
                description: >-
                  Returns a list of Customers. Optional filter parameters can be
                  passed in.


                  **Notes**


                  Attribute names are not available on the customer object.
                summary: Get All Customers
                tags:
                  - Get
                  - All
                  - Customers
                  - Customers
              post:
                description: >-
                  Creates Customers. Create up to 10 customers in one call.


                  **Required Fields**

                  * last_name

                  * first_name

                  * email


                  **Required Fields Customer Address**

                  * first_name

                  * city

                  * country_code

                  * last_name

                  * address1


                  **Required Fields Attributes**

                  * Attributes must be
                  [created](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute)
                  **BEFORE** creating a customer.

                  * attribute_id

                  * attribute_value -- This is input as a string, regardless of
                  the
                  [Type](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute).


                  **Notes**


                  A customer can be created with global access or
                  channel-specific access.

                  * **Global access:**
                    * Make sure the channel has `allow_global_logins` enabled. This is on by default only for the default storefront. Find more info at [Customer Settings > Channel](/docs/rest-management/customers/customer-settings-channel).
                    * Omit `channel_ids` field, or provide `channel_ids: null`.
                  * **Channel-specific access:**
                    * Provide a `channel_ids` array containing the channels accessible by the customer. This array cannot be empty.
                summary: Create Customers
                tags:
                  - Create
                  - Customers
                  - Customers
              put:
                description: >-
                  Updates Customers. Subresource updates are not supported. Up
                  to 10 customers can be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer* This must be included in the
                  request body


                  **Read Only Fields**

                  * id

                  * registration_ip_address

                  * date_created

                  * date_modified



                  **Notes**


                  * Attributes Values can not be updated using Update a
                  Customer. Use the [Update customer attribute
                  values](/docs/rest-management/customers/customer-attribute-values#upsert-customer-attribute-values)
                  endpoint.

                  * channel_ids -- Updating the list of channels a customer can
                  access may create some side effects in a multi-storefront
                  situation. This list determines which customer account we will
                  use to authenticate a shopper given a channel.
                summary: Update Customers
                tags:
                  - Update
                  - Customers
                  - Customers
              delete:
                description: >-
                  Deletes Customers.


                  **Required Query**

                  * id:in -- ID of the customer


                  **Notes**


                  A query is required to delete customers. If not provided, a
                  204 is returned, with no changes to the data.
                summary: Delete Customers
                tags:
                  - Delete
                  - Customers
                  - Customers
            /customers/addresses:
              get:
                description: >-
                  Returns a list of Customer Addresses. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Addresses
                tags:
                  - Get
                  - All
                  - Customer
                  - Addresses
                  - Customers
                  - Addresses
              post:
                description: >-
                  Creates a Customer Address. Multiple customer addresses can be
                  created in one call.


                  **Required Fields**

                  * **customer_id**

                  * **first_name**

                  * **last_name**

                  * **city**

                  * **country_code**

                  * **address1**


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **customer_id**
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to create an address that already exists will
                  result in no change to the address or custom form field
                  values, an HTTP 200 return code, and the address will be
                  absent from the response body.

                  * The default rate limit for this endpoint is 10 concurrent
                  requests.
                summary: Create a Customer Address
                tags:
                  - Create
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              put:
                description: >-
                  Updates a Customer Address. Multiple customer addresses can be
                  updated in one call.


                  **Required Fields**

                  * **id** -- ID of the *Customer Address*


                  **Limits**

                  * Limit of **3** concurrent requests.


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to update an address such that it becomes
                  identical to another address that already exists will result
                  in no change to the target address or custom form field
                  values. The response will have an HTTP 200 return code, and
                  the address will be absent from the response body.
                summary: Update a Customer Address
                tags:
                  - Update
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              delete:
                description: |-
                  Deletes a Customer Address.

                  **Required Query**
                  * id:in -- ID of the *Customer Address*
                summary: Delete a Customer Address
                tags:
                  - Delete
                  - Customer
                  - Address
                  - Customers
                  - Addresses
            /customers/validate-credentials:
              post:
                tags:
                  - Validate
                  - Customer
                  - Credentials
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                description: >-
                  Validate a customer credentials - This endpoint has special
                  rate limiting protections to protect against abuse.
                summary: Validate a customer credentials
            /customers/settings:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Returns the global-level customer settings.
                summary: Get Customer Settings
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Updates the customer settings on the global level.
                summary: Update Customer Settings
            /customers/settings/channels/{channel_id}:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: |-
                  Returns the customer settings per channel.

                  **Notes**

                   * `null` indicates that there is no override per given channel and values are inherited from the global level.
                summary: Get Customer Settings per Channel
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: >-
                  Update the customer settings per channel


                  **Required Fields**


                  * `channel_id`: Provide a `channel_id` array containing one or
                  more channel IDs. Customers will have access to these channels
                  and no others. This array cannot be empty.


                  **Notes**


                  * Setting `null` will delete override per given channel, and
                  values will be inherited from the global level. Make sure the
                  channel has `allow_global_logins` enabled.
                summary: Update Customer Settings per Channel
              parameters:
                - null
            /customers/attributes:
              get:
                description: >-
                  Returns a list of Customer Attributes. You can pass in
                  optional filter parameters.
                summary: Get All Customer Attributes
                tags:
                  - Get
                  - All
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              post:
                description: >-
                  Creates a Customer Attribute. Multiple customer attributes can
                  be created in one call.


                  **Required Fields**

                  * name

                  * type


                  **Limits**

                  * Limit of 3 concurrent requests.


                  **Notes**


                  Once the data type is set, it cannot be changed. The attribute
                  will need to be deleted then created again with the new data
                  type. This will also delete it from the customer.


                  Customer attributes are created separately from the customer.
                  After the name and type are created, then the attributes can
                  be added to the customer.


                  A store cannot have more than 50 customer attributes.
                summary: Create a Customer Attribute
                tags:
                  - Create
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              put:
                description: >-
                  Updates a Customer Attribute. Multiple customer attributes can
                  be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer Attribute*


                  Once the data type is set, it can not be changed. The
                  attribute will need to be deleted then created again with the
                  new data type. This will also delete it from the customer.


                  **Limits**

                  * Limit of 3 concurrent requests.
                summary: Update a Customer Attribute
                tags:
                  - Update
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              delete:
                description: |-
                  Deletes Customer Attributes from the store.

                  **Required Query**
                  * id:in -- ID of the *Customer Attribute*
                summary: Delete Customer Attributes
                tags:
                  - Delete
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
            /customers/attribute-values:
              get:
                description: >-
                  Returns a list of Customer Attribute Values. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Attribute Values
                tags:
                  - Get
                  - All
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              put:
                description: >-
                  Upserts Customer Attribute Values. Updates the attribute
                  values on the Customer. Multiple customer attribute values can
                  be updated in one call.


                  Upsert checks for an existing record. If there is none, it
                  creates the record, if there is a matching record, it updates
                  that record.


                  **Limits**

                  * 10 per call limit.
                summary: Upsert Customer Attribute Values
                tags:
                  - Upsert
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              delete:
                description: >-
                  Deletes Customer Attribute Values. Deletes the attribute value
                  from the customer.


                  **Required Query**

                  * id:in - ID of the *Customer Attribute Value*
                summary: Delete Customer Attribute Values
                tags:
                  - Delete
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
            /customers/form-field-values:
              get:
                summary: Get Customer Form Field Values
                description: >-
                  Returns a list of form field values for the Customer or
                  Customer Address object.


                  To learn about adding and managing form fields, see [Adding
                  and Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).
                tags:
                  - Get
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
              put:
                summary: Upsert Customer Form Field Values
                description: >-
                  Updates form field values on the Customer or Customer Address
                  objects. Multiple form field values can be updated in one
                  call.


                  Upsert checks for an existing record, if there is none it
                  creates the record, if there is a matching record it updates
                  that record.


                  To learn more about editing form fields, see [Adding and
                  Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).


                  **Limits**

                  * Limit of 10 concurrent requests.
                tags:
                  - Upsert
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
            /customers/{customerId}/consent:
              get:
                description: >-
                  Gets the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Get Customer Consent
                tags:
                  - Get
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              put:
                description: >-
                  Updates the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Update Customer Consent
                tags:
                  - Update
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              parameters:
                - null
            /customers/{customerId}/stored-instruments:
              get:
                summary: Get Stored Instruments
                tags:
                  - Get
                  - Stored
                  - Instruments
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                description: >-
                  Lists all available stored instruments for a customer. This
                  list will include all types of stored instruments namely card,
                  account and bank_account instruments
              parameters:
                - null
            /customers/{customerId}/metafields:
              get:
                summary: Get Customer Metafields
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Gets customer metafields by passing the `customerId` in the
                  query parameters.
              post:
                summary: Create Customer Metafields
                tags:
                  - Create
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Creates Customer metafields by passing the `customerId` in the
                  query parameters.
            /customers/{customerId}/metafields/{metafieldId}:
              get:
                summary: Get Customer Metafields List
                description: >
                  Lists available metafields for a customer. To retrieve the
                  list, use `customerId` and `metafieldId` in the query
                  parameters.
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - List
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >-
                  Updates customer metafields. To update the customer
                  metafields, use 'customerId' and 'metafield' in the query
                  parameters.
              delete:
                summary: Delete Customer Metafields
                tags:
                  - Delete
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >
                  Deletes customer metafields. To delete customer metafields,
                  use 'customerId' and 'metafieldId' in the query parameters.
            /customers/metafields:
              get:
                summary: Get All Customer Metafields
                tags:
                  - Get
                  - All
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Get all customer metafields.
              post:
                summary: Create Multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              put:
                summary: Update Multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Delete all customer
    overlays:
      - type: APIs.io Search
        url: overlays/customers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---