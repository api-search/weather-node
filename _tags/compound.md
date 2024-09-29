---
name: Compound
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compound.png
url: https://example.com/apis/compound.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compound
apis:
  - name: FactSet Prices API
    description: >-
      Gain access to comprehensive global coverage for equity prices, returns,
      volume, shares, splits, and dividends. Security types include Common
      Stock, ADR, GDR, Preferred, Closed-ended Fund, Exchange Traded Fund, Unit,
      Open-ended Fund, Exchange…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-prices-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-prices-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Prices API
          paths:
            /factset-prices/v1/prices:
              get:
                tags:
                  - Gets
                  - End-of-day
                  - Open,
                  - High,
                  - Low,
                  - Close
                  - For
                  - List
                  - Of
                  - Securities.
                  - Factset
                  - Prices
                  - V1
                summary: >-
                  Gets end-of-day Open, High, Low, Close for a list of
                  securities.
                description: >
                  Gets security prices, Open, High, Low, Close, Volume, and
                  currency for a specified date range and frequency. Prices are
                  updated and at different times across the different regions
                  around the globe. The Prices API automatically defaults
                  relative price dates to the local region which is determined
                  by the local region of the requested security id. To learn
                  more about relative dates please visit [OA Page
                  4627](https://my.apps.factset.com/oa/pages/4627)


                  */prices* endpoint currently supports Long Running
                  asynchronous requests up to **10 minutes** via `batch`
                  parameter. **Additional Approvals needed for access**. Id
                  limits increased to **5000 ids** per request using batch
                  parameter.
              post:
                tags:
                  - Requests
                  - End-of-day
                  - Open,
                  - High,
                  - Low,
                  - Close
                  - For
                  - Large
                  - List
                  - Of
                  - Securities.
                  - Factset
                  - Prices
                  - V1
                summary: >-
                  Requests end-of-day Open, High, Low, Close for a large list of
                  securities.
                description: >

                  Gets security prices, Open, High, Low, Close, Volume, and
                  currency for a specified date range and frequency.


                  */prices* endpoint currently supports Long Running
                  asynchronous requests up to **10 minutes** via `batch`
                  parameter. **Additional Approvals needed for access**. Id
                  limits increased to **5000 ids** per request using batch
                  parameter.
            /factset-prices/v1/fixed-income:
              get:
                tags:
                  - Gets
                  - Pricing
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                summary: Gets pricing for a list of Fixed Income securities
                description: >
                  Get BID, MID, ASK, and Issuer Entity ID for a list of Fixed
                  Income Securities as of a requested date range. Available for
                  U.S. Corporate, Treasury and Agency bonds, Municipals, and
                  non-U.S. Corporate and Government bonds. To learn more about
                  Fixed Income Prices database, please review
                  [OA:15995](https://my.apps.factset.com/oa/pages/15995)
              post:
                tags:
                  - Requests
                  - Pricing
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities
                  - Date
                  - Range
                  - Requested
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                summary: >-
                  Requests pricing for a list of Fixed Income securities for
                  date range requested
                description: >
                  Get BID, MID, ASK, and Issuer Entity ID for a list of Fixed
                  Income Securities as of a requested date range. Available for
                  U.S. Corporate, Treasury and Agency bonds, Municipals, and
                  non-U.S. Corporate and Government bonds. To learn more about
                  Fixed Income Prices database, please review
                  [OA:15995](https://my.apps.factset.com/oa/pages/15995)
            /factset-prices/v1/references:
              get:
                tags:
                  - Gets
                  - Security
                  - Reference
                  - Details
                  - For
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                summary: Gets security reference details for a list of securities
                description: >
                  Gets security reference details for a list of `ids`, such as
                  Name, Security Type, Currency, Country, Primary Exchange,
                  Local Index, and dates of First and Last Trade.
              post:
                tags:
                  - Requests
                  - Security
                  - Reference
                  - Details
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                summary: Requests security reference details a list of securities
                description: >
                  Gets security reference details for a large list of `ids`,
                  such as Name, Security Type, Currency, Country, Primary
                  Exchange, Local Index, and dates of First and Last Trade.
            /factset-prices/v1/returns:
              get:
                tags:
                  - Gets
                  - Returns
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range
                  - And
                  - Rolling
                  - Period
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                summary: >-
                  Gets Returns for a list of `ids` as of given date range and
                  rolling Period
                description: >-
                  The simple or compound return for the requested frequency
                  and/or rollingPeriod. Depending on the input parameters the
                  return will adjust accordingly. If you simply use frequency
                  and no rollingPeriod, the return value will represent the
                  frequency period. If you use rollingPeriod, the values will be
                  returned in actual period ends (e.g. actual month, actual
                  week, daily, etc.). General Return Calculation Details found
                  on [Online Assistant Page
                  #8748](https://oa.apps.factset.com/pages/8748)
              post:
                tags:
                  - Requests
                  - Security
                  - Returns
                  - For
                  - The
                  - Given
                  - Date
                  - Range
                  - And
                  - Rolling
                  - Period.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                summary: >-
                  Requests security returns for the given date range and
                  rollingPeriod.
                description: >-
                  The simple or compound return for the requested frequency
                  and/or rollingPeriod. Depending on the input parameters the
                  return will adjust accordingly. If you simply use frequency
                  and no rollingPeriod, the return value will represent the
                  frequency period. If you use rollingPeriod, the values will be
                  returned in actual period ends (e.g. actual month, actual
                  week, daily, etc.). General Return Calculation Details found
                  on [Online Assistant Page
                  #8748](https://oa.apps.factset.com/pages/8748)
            /factset-prices/v1/returns-snapshot:
              get:
                tags:
                  - Returns
                  - The
                  - Price
                  - Performance
                  - Of
                  - Security
                  - And
                  - Annualized
                  - Compound
                  - Total
                  - Returns.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                summary: >-
                  Returns the price performance of the security and annualized
                  compound total returns.
                description: >
                  Retrieves various return periods as of a given date for a
                  requested list of securities. This endpoint is very helpful
                  for quickly retrieving a list of pre-calculated returns for
                  application development.<p> Return periods include
                    * oneDay
                    * weekToDate
                    * monthToDate
                    * quarterToDate
                    * yearToDate
                    * oneMonth
                    * threeMonth
                    * sixMonth
                    * nineMonth
                    * oneYear
                    * twoYearAnnualized
                    * threeYearAnnualized
                    * fiveYearAnnualized
                    * tenYearAnnualized
                    * twentyYearAnnualized
                    * thirtyYearAnnualized
                    * ipoToDateAnnualized
                    </p>
              post:
                tags:
                  - Returns
                  - The
                  - Price
                  - Performance
                  - Of
                  - Security
                  - And
                  - Annualized
                  - Compound
                  - Total
                  - Returns.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                summary: >-
                  Returns the price performance of the security and annualized
                  compound total returns.
                description: >
                  Retrieves various return periods as of a given date for a
                  requested list of securities. This endpoint is very helpful
                  for quickly retrieving a list of pre-calculated returns for
                  application development.<p> Return periods include
                    * oneDay
                    * weekToDate
                    * monthToDate
                    * quarterToDate
                    * yearToDate
                    * oneMonth
                    * threeMonth
                    * sixMonth
                    * nineMonth
                    * oneYear
                    * twoYearAnnualized
                    * threeYearAnnualized
                    * fiveYearAnnualized
                    * tenYearAnnualized
                    * twentyYearAnnualized
                    * thirtyYearAnnualized
                    * ipoToDateAnnualized
                    </p>
            /factset-prices/v1/dividends:
              get:
                tags:
                  - Gets
                  - Dividend
                  - Information
                  - For
                  - Given
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                summary: >-
                  Gets dividend information for a given date range and list of
                  securities
                description: >-
                  Get the dividend amounts, dates, types, and flags over a
                  specified date range. You may request future dates to receive
                  information for declared dividends.
              post:
                tags:
                  - Requests
                  - Dividend
                  - Information
                  - For
                  - Given
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                summary: >-
                  Requests dividend information for a given date range and list
                  of securities
                description: >-
                  Get the dividend amounts, dates, types, and flags over a
                  specified date range
            /factset-prices/v1/splits:
              get:
                tags:
                  - Gets
                  - Full
                  - History
                  - Of
                  - Security
                  - Splits
                  - For
                  - List
                  - '`ids`'
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                summary: Gets full history of security Splits for a list of `ids`
                description: >-
                  Gets the entire history of splits for a given list of
                  identifiers. Information returned includes the split factor, a
                  plain text comment regarding the type of split, and the event
                  date.
              post:
                tags:
                  - Requests
                  - Splits
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                summary: Requests splits for a list of `ids`
                description: >-
                  Gets the entire history of splits for a given list of
                  identifiers. Information returned includes the split factor, a
                  plain text comment regarding the type of split, and the event
                  date.
            /factset-prices/v1/shares:
              get:
                tags:
                  - Gets
                  - Shares
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                summary: Gets shares for a list of `ids` as of given date range.
                description: >-
                  Gets security shares for a list of 'ids' and given date range.
                  Share values returned include security-level and
                  company-level.
              post:
                tags:
                  - Requests
                  - Shares
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                summary: Requests shares for a list of `ids` as of given date range.
                description: >-
                  Gets security shares for a list of 'ids' and given date range.
                  Share values returned include security-level and
                  company-level.
            /factset-prices/v1/market-value:
              get:
                tags:
                  - Gets
                  - The
                  - Security
                  - Level
                  - And
                  - Company
                  - Market
                  - Values
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                summary: >-
                  Gets the security level and company level market values for a
                  list of `ids` as of given date range and frequency.
                description: >
                  Gets market capitalization of list of ids for the company
                  level, security level, calendar, frequency, and currency for a
                  specified date range.
              post:
                tags:
                  - Requests
                  - The
                  - Market
                  - Value
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                summary: >-
                  Requests the market value for a list of `ids` as of given date
                  range.
                description: >-
                  Requests the market value for a list of `ids` as of given date
                  range.
            /factset-prices/v1/high-low:
              get:
                tags:
                  - Gets
                  - The
                  - Price
                  - High
                  - And
                  - Low
                  - Of
                  - Securities
                  - For
                  - List
                  - '`ids`'
                  - As
                  - Given
                  - Date,
                  - Period
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                summary: >-
                  Gets the price high and price low of securities for a list of
                  `ids` as of given date, period and frequency.
                description: >
                  For given security(s), gets the high and low prices with the
                  respective dates on which they occurred. This service gives
                  options for fetching the price as of the close or intraday.
              post:
                tags:
                  - Requests
                  - The
                  - Price
                  - High
                  - And
                  - Low
                  - Of
                  - Securities
                  - For
                  - List
                  - '`ids`'
                  - As
                  - Given
                  - Date,
                  - Period
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                summary: >-
                  Requests the price high and price low of securities for a list
                  of `ids` as of given date, period and frequency.
                description: >
                  For given security(s), gets the high and low prices with the
                  respective dates on which they occurred. This service gives
                  options for fetching the price as of the close or intraday.
            /factset-prices/v1/database-rollover:
              get:
                summary: Gets the latest relative rollover date for the database.
                description: >
                  Gets zero relative date and last update time for FactSet
                  databases. The dates represent the date that the rollover
                  event happened; the date and time is in **eastern time
                  zone**.  <p>Depending on the ids requested and their
                  respective regions, a requested startDate or endDate used in
                  the various Prices API may reflect different previous close
                  dates. This relative "zero" date, meaning - as of yesterday's
                  close - will vary across global regions. This API is designed
                  to help production systems account for regional rollover dates
                  to know when to trigger their processes for different regions
                  to reflect the latest close. The response gives context for
                  AMERICAS, ASIA PACIFIC, and EUROPE. </p>
                tags:
                  - Gets
                  - The
                  - Latest
                  - Relative
                  - Rollover
                  - Date
                  - For
                  - Database.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
              post:
                summary: Gets the latest relative rollover date for the database.
                description: >
                  Gets zero relative date and last update time for FactSet
                  databases. The dates represent the date that the rollover
                  event happened; the date and time is in **eastern time
                  zone**.  <p>Depending on the ids requested and their
                  respective regions, a requested startDate or endDate used in
                  the various Prices API may reflect different previous close
                  dates. This relative "zero" date, meaning - as of yesterday's
                  close - will vary across global regions. This API is designed
                  to help production systems account for regional rollover dates
                  to know when to trigger their processes for different regions
                  to reflect the latest close. The response gives context for
                  AMERICAS, ASIA PACIFIC, and EUROPE. </p>
                tags:
                  - Gets
                  - The
                  - Latest
                  - Relative
                  - Rollover
                  - Date
                  - For
                  - Database.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
            /batch/v1/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                summary: Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id.
              post:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                summary: Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id. 
            /batch/v1/result:
              get:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                  - Result
                summary: Returns the response for a Batch Request
                description: >-
                  Returns the response data for the underlying batch request
                  that is specified by the id.
              post:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                  - Result
                summary: Returns the response for a Batch Request
                description: >-
                  Return the response data for the underlying batch request that
                  is s
    overlays:
      - type: APIs.io Search
        url: overlays/prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-prices-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---