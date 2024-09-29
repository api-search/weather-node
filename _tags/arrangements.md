---
name: Arrangements
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/arrangements.png
url: https://example.com/apis/arrangements.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Arrangements
apis:
  - name: Adyen Account API
    description: >-
      This API is used for the classic integration. If you are just starting
      your implementation, refer to our new integration guide instead. The
      Account API provides endpoints for managing account-related entities on
      your platform. These related entities include account holders, accounts,
      bank accounts, shareholders, and verification-related documents. The
      management operations include actions such as creation, retrieval,
      updating, and deletion of them.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/Account/6/overview
    baseURL: https://cal-test.adyen.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/Account/6/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Account API
            x-timestamp: '2023-05-30T15:27:20Z'
          x-groups:
            - Account holders
            - Accounts
            - Verification
          tags:
            - name: Account holders
            - name: Verifications
            - name: Accounts
          paths:
            /checkAccountHolder:
              post:
                tags:
                  - Triggers
                  - Verification
                  - Account
                  - Holders
                summary: Trigger verification
                description: >-
                  Triggers the verification of an account holder even if the
                  checks are not yet required for the volume that they are
                  currently processing.
            /closeAccount:
              post:
                tags:
                  - Close
                  - null
                  - Account
                  - Account
                  - Holders
                summary: Close an account
                description: >-
                  Closes an account. If an account is closed, you cannot process
                  transactions, pay out its funds, or reopen it. If payments are
                  made to a closed account, the payments are sent to your liable
                  account.
            /closeAccountHolder:
              post:
                tags:
                  - Close
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                summary: Close an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  to **Closed**. This state is final. If an account holder is
                  closed, you can't process transactions, pay out funds, or
                  reopen it. If payments are made to an account of an account
                  holder with a **Closed**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status),
                  the payments are sent to your liable account.
            /closeStores:
              post:
                tags:
                  - Close
                  - Stores
                  - Account
                  - Holders
                  - Stores
                summary: Close stores
                description: Closes stores associated with an account holder.
            /createAccount:
              post:
                tags:
                  - Create
                  - null
                  - Account
                  - Account
                  - Holders
                  - Stores
                summary: Create an account
                description: >-
                  Creates an account under an account holder. An account holder
                  can have [multiple
                  accounts](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#create-additional-accounts).
            /createAccountHolder:
              post:
                tags:
                  - Create
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                summary: Create an account holder
                description: >-
                  Creates an account holder that [represents the sub-merchant's
                  entity](https://docs.adyen.com/marketplaces-and-platforms/classic/account-structure#your-platform)
                  in your platform. The details that you need to provide in the
                  request depend on the sub-merchant's legal entity type. For
                  more information, refer to [Account holder and
                  accounts](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#legal-entity-types).
            /deleteBankAccounts:
              post:
                tags:
                  - Delete
                  - Bank
                  - Accounts
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                summary: Delete bank accounts
                description: 'Deletes bank accounts associated with an account holder. '
            /deleteLegalArrangements:
              post:
                tags:
                  - Delete
                  - Legal
                  - Arrangements
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                summary: Delete legal arrangements
                description: >-
                  Deletes legal arrangements and/or legal arrangement entities
                  associated with an account holder.
            /deletePayoutMethods:
              post:
                tags:
                  - Delete
                  - Payouts
                  - Methods
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                summary: Delete payout methods
                description: Deletes payout methods associated with an account holder.
            /deleteShareholders:
              post:
                tags:
                  - Delete
                  - Shareholders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                summary: Delete shareholders
                description: Deletes shareholders associated with an account holder.
            /deleteSignatories:
              post:
                tags:
                  - Delete
                  - Signatories
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                summary: Delete signatories
                description: Deletes signatories associated with an account holder.
            /getAccountHolder:
              post:
                tags:
                  - Get
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                summary: Get an account holder
                description: Returns the details of an account holder.
            /getTaxForm:
              post:
                tags:
                  - Get
                  - Taxes
                  - Forms
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                summary: Get a tax form
                description: >-
                  Generates a tax form for account holders operating in the US.
                  For more information, refer to [Providing tax
                  forms](https://docs.adyen.com/marketplaces-and-platforms/classic/tax-forms).
            /getUploadedDocuments:
              post:
                tags:
                  - Get
                  - Documents
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                summary: Get documents
                description: >
                  Returns documents that were previously uploaded for an account
                  holder. Adyen uses the documents during the [verification
                  process](https://docs.adyen.com/marketplaces-and-platforms/classic/verification-process).
            /suspendAccountHolder:
              post:
                tags:
                  - Suspend
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                summary: Suspend an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  to **Suspended**.
            /unSuspendAccountHolder:
              post:
                tags:
                  - Unsuspend
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Unsuspend an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  from **Suspended** to **Inactive**. 

                  Account holders can have a **Suspended**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status)
                  if you suspend them through the
                  [`/suspendAccountHolder`](https://docs.adyen.com/api-explorer/#/Account/v5/post/suspendAccountHolder)
                  endpoint or if a verification deadline expires.


                  You can only unsuspend account holders if they do not have
                  verification checks with a **FAILED**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status).
            /updateAccount:
              post:
                tags:
                  - Update
                  - null
                  - Account
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Update an account
                description: Updates the description or payout schedule of an account.
            /updateAccountHolder:
              post:
                tags:
                  - Update
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Update an account holder
                description: >+
                  Updates the `accountHolderDetails` and `processingTier` of an
                  account holder, and adds bank accounts and shareholders.


                  When updating `accountHolderDetails`, parameters that are not
                  included in the request are left unchanged except for the
                  following object:


                  * `metadata`: Updating the metadata replaces the entire
                  object. This means that to update an existing key-value pair,
                  you must provide the changes, as well as other existing
                  key-value pairs.


                  When updating any field in the following objects, you must
                  submit all the fields required for validation:

                   * `address`

                  * `fullPhoneNumber`


                  * `bankAccountDetails.BankAccountDetail`


                  * `businessDetails.shareholders.ShareholderContact`

                   For example, to update the `address.postalCode`, you must also submit the `address.country`, `.city`, `.street`, `.postalCode`, and possibly `.stateOrProvince` so that the address can be validated.

                  To add a bank account or shareholder, provide the bank account
                  or shareholder details without a `bankAccountUUID` or a
                  `shareholderCode`.

            /updateAccountHolderState:
              post:
                tags:
                  - Update
                  - Payouts
                  - Or
                  - Processing
                  - States
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                  - States
                summary: Update payout or processing state
                description: >-
                  Disables or enables the processing or payout state of an
                  account holder.
            /uploadDocument:
              post:
                tags:
                  - Uploads
                  - Document
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                  - States
                  - Document
                summary: Upload a document
                description: >-
                  Uploads a document for an account holder. Adyen uses the
                  documents during the [verification
                  process](https://docs.adyen.com/marketplaces-and-platfo
    overlays:
      - type: APIs.io Search
        url: overlays/accounts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/accounts-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-account-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---