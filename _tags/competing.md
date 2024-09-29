---
name: Competing
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/competing.png
url: https://example.com/apis/competing.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Competing
apis:
  - name: FactSet ETF Profile and Prices API
    description: >-
      Access FactSet-collected profile data and pricing for Exchange Traded
      Funds (ETFs).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/etf-profile-and-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#changelog
      - type: OpenAPI
        data:
          host: api.factset.com
          swagger: '2.0'
          consumes:
            - application/json
          produces:
            - application/json
          paths:
            /factset/etf/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Profile
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                description: >-
                  An ETP can be profiled by defining several common attributes
                  such as issuer, fund description, and benchmark.
                summary: Retrieve basic profile information for a specified ETP.
            /factset/etf/allocation/asset/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Asset
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  asset class. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's asset allocations.
            /factset/etf/allocation/country/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Country
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  country names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's country allocations.
            /factset/etf/allocation/currency/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Currency
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  currency. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's currency allocations.
            /factset/etf/allocation/economicDevelopment/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Economic
                  - Development
                  - Status.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  List of allocations classified by a holding's economic
                  development status (e.g. developed market, frontier market,
                  emerging market).
                summary: >-
                  List of allocations classified by a holding's economic
                  development status.
            /factset/etf/allocation/exchange/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Exchange
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  exchanges. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's exchange allocations.
            /factset/etf/allocation/industry/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Industry
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  industry. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's industry allocations.
            /factset/etf/allocation/marketCapitalization/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Total
                  - Market
                  - Capitalization.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  List of allocations classified by a holding's total market
                  capitalization (e.g. Small Cap, Mid Cap, Large Cap). Response
                  will be sorted by weight in descending order.
                summary: >-
                  List of allocations classified by a holding's total market
                  capitalization.
            /factset/etf/allocation/region/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Region
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  region names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's region allocations.
            /factset/etf/allocation/sector/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Sector
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  sector names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's sector allocations.
            /factset/etf/analytics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Analytics
                  - Datapoints
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet's proprietary analytical datapoints include ETP
                  attributes specific to lending, corporate actions, and
                  benchmarks.
                summary: FactSet proprietary analytics datapoints for ETPs.
            /factset/etf/analytics/holdings/statistics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Portfolio
                  - Statistics
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates several proprietary portfolio statistics
                  for ETPs including average maturity, credit quality,
                  price/book ratio, price/earnings ratio, and dividend yield.
                summary: FactSet's portfolio statistics for ETPs.
            /factset/etf/analytics/score/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Rankings.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates various proprietary fund rankings including
                  unique scores, fund grades, segment averages, and
                  recommendations.
                summary: FactSet proprietary ETP rankings.
            /factset/etf/analytics/trade/getBySymbol:
              get:
                tags:
                  - Trade
                  - Statistics
                  - For
                  - Specific
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  Various metrics of an ETP's liquidity including creation
                  metrics, premium/discount, spread, and tracking error
                  statistics.
                summary: Trade statistics for specific ETP.
            /factset/etf/characteristics/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Characteristic
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  An ETP has many unique characteristics specific to its
                  composition that differentiate it from other products. This
                  includes details on leverage, hedging, derivatives, and
                  service providers.
                summary: Retrieve basic characteristic information for a specified ETP.
            /factset/etf/class/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Classification
                  - Specific
                  - To
                  - Asset
                  - Class,
                  - Geography,
                  - Or
                  - Investment
                  - Strategy.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  ETP classification is divided into three categories: Asset
                  Class, Geography, and Investment Strategy. Asset class is
                  determined based on the various asset types held by the fund,
                  A fund's geography can be classified by region (e.g.
                  Asia-Pac), specific geography (e.g. China) or economic
                  development (e.g. BRIC). An ETP's investment strategy is
                  classified in broad categories (e.g. Large Cap) and more
                  granular categorizations.
                summary: >-
                  Retrieve an ETP's classification specific to asset class,
                  geography, or investment strategy.
            /factset/etf/class/category/broad/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Broad
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                description: List of ETP class broad categories.
                summary: List of ETP class broad categories.
            /factset/etf/class/category/focus/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Focus
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                description: List of ETP class focus categories.
                summary: List of ETP class focus categories.
            /factset/etf/class/category/niche/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Niche
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                description: List of ETP class niche categories.
                summary: List of ETP class niche categories.
            /factset/etf/class/geography/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Geographies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: List of ETP class geographies.
                summary: List of ETP class geographies.
            /factset/etf/competitors/listBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Proprietary
                  - List
                  - Of
                  - Competing
                  - Companies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  FactSet defines and maintains a proprietary list of competing
                  companies based on a number of attributes specific to a fund.
                summary: FactSet's proprietary list of competing companies.
            /factset/etf/distribution/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Current
                  - Distribution
                  - Details.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  Retrieve distribution-related details for a specific ETP
                  including dividend and capital gain distribution details.
                summary: Retrieve an ETP's current distribution details.
            /factset/etf/fundFlows/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Cash
                  - Inflow/outflows
                  - For
                  - Various
                  - Time
                  - Periods.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                description: >-
                  Retrieve the amount invested or divested in a specific ETP
                  over various time periods including one-day, one-week,
                  one-month, one-year, and YTD.
                summary: >-
                  Retrieve an ETP's cash inflow/outflows for various time
                  periods.
            /factset/etf/growthOfTenK/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Growth
                  - Of
                  - '10'
                  - Calculated
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Growth of 10K (or growth of 10,000) is a commonly used chart
                  that highlights the change in the value of an initial 10,000
                  investment in the ETP during a given period of time. Often,
                  this period of time is either since inception or the
                  calculation between the pre-defined range.
                summary: >-
                  This endpoint returns selected ETP's Growth of 10K calculated
                  values.
            /factset/etf/holdings/listBySymbol:
              get:
                tags:
                  - Holdings
                  - Details
                  - For
                  - An
                  - Individual
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Retrieve an ETP's holdings information including security,
                  shares held, and weight.
                summary: Holdings details for an individual ETP.
            /factset/etf/marketAggregates/getBySymbol:
              get:
                tags:
                  - Market
                  - Aggregate
                  - Data
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                description: >-
                  Market Aggregates combines FactSet Estimates, FactSet
                  Fundamentals, and FactSet Prices data to derive ratios and per
                  share values on an aggregate level. The resulting index values
                  can be used to identify market trends and compare a
                  combination of portfolios, benchmarks, and individual
                  securities.
                summary: Market aggregate data for ETPs.
            /factset/etf/premiumDiscount/summary/listBySymbol:
              get:
                tags:
                  - Summary
                  - Of
                  - Premium
                  - Discount
                  - Data.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: Summary of ETP premium discount data.
                summary: Summary of ETP premium discount data.
            /factset/etf/price/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  Retrieve an ETP's historical NAV and shares outstanding for a
                  specified time range.
                summary: Retrieve historical ETP NAV values.
            /factset/etf/returns/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Total
                  - Return
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  An ETP's total return data can be returned for various time
                  frames including 1-month, 3-month, YTD, 1-year, 3-year, and
                  5-year. Total return calculations include price performance
                  plus reinvested and compounded distributions. Market price is
                  used to calcualte market returns. Portfolio nav is used to
                  calcualte nav returns.
                summary: Retrieve total return data for a specified ETP.
            /factset/etf/strategy/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Various
                  - Classification
                  - Details
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  ETP's can be classified in many different ways including
                  investment strategy, security weightings, and fund
                  composition.
                summary: Retrieve various classification details for a specified ETP.
            /factset/etf/strategy/segment/list:
              get:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Strategy
                  - Segments.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve the various segments assigned to a specific ETP.
                  Segment data is used to group funds for comparison and
                  relative performance analyses.
                summary: Retrieve a list of ETP strategy segments.
            /factset/etf/structure/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Basic
                  - Structure
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve details on a fund's structure including its type,
                  investment style (active/passive), and legal structure.
                summary: Retrieve the basic structure information for a specified ETP.
            /factset/etf/taxesAndFees/us/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Tax
                  - And
                  - Fee
                  - Related
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                description: >-
                  Retrieve various fee and tax related details on a specified
                  ETP including expense ratio and tax treatment for dividends
                  and capital gains.
                summary: >-
                  Retrieve the tax and fee related information for a specified
                  ETP.
            /factset/etf/timeSeries/listBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                  - Series
                description: >-
                  Retrieve the historical NAV data and the respective fund flows
                  and shares outstanding for a specified fund and time period.
                  Please refer currency.fund in /factset/etf/getBySymbol for
                  currency value.
                summary: Retrieve historical NAV data for a specified ETP.
          info:
            title: Prime Developer Trial
          x-interface-version: 1
          x-documenter-version: 5.38.1
          x-api-version: 2.9.1
          tags:
            - name: factset
              description: factset endpoints
          responses:
            ErrorResponse:
              description: Generic error response for all errors (400 ... 599 error codes)
              schema:
                type: object
                properties:
                  meta:
                    $ref: '#/definitions/ErrorMetaObject'
                  errors:
                    $ref: '#/definitions/ErrorObject'
          definitions:
            ErrorMetaObject:
              type: object
              properties:
                status:
                  $ref: '#/definitions/StatusObject'
            ErrorObject:
              type: array
              description: >-
                The errors member contains additional information about a failed
                request.
              items:
                type: object
                properties:
                  details:
                    type: string
                    description: >-
                      A human-readable, unstructured explanation specific to
                      this occurrence of the failure.
                  encryptedDetails:
                    type: string
                    description: >-
                      Base64-encoded, internal details about the error, in
                      addition to "details".
                  type:
                    type: number
                    format: int32
                    description: Internal error type of the Foundation API protocol.
                  attribute:
                    type: array
                    description: >-
                      For a validation error, a reference to the request
                      parameter that failed validation; otherwise, an empty
                      array.
                    items:
                      type: object
                      properties:
                        name:
                          type: string
                          description: Element of the path denoting the request parameter.
                        index:
                          type: number
                          format: int32
                          description: >-
                            If the attribute "name" designates an array, index
                            of the array element; otherwise the special value
                            -1.
                      x-property-sort:
                        - name
                        - index
                x-property-sort:
                  - detail
                  - encryptedDetails
                  - type
                  - attribute
            AttributesMember:
              type: array
              description: >-
                Limit the attributes returned in the response to the specified
                set.
              items:
                type: string
                maxLength: 100
                exclusiveMaximum: false
              maxItems: 50
              uniqueItems: true
            LanguageMember:
              type: string
              format: isoLanguage
              description: ISO 639-1 code of the language.
              maxLength: 2
              minLength: 2
              exclusiveMinimum: false
              exclusiveMaximum: false
            StatusObject:
              type: object
              properties:
                code:
                  type: number
                  format: int32
                  description: >-
                    The HTTP status code of the response, mirroring the code
                    from the Status-Line of the HTTP response message (see
                    [RFC2616] section 6.1).
              description: The status member contains the status code of the response.
              required:
                - code
            CursorBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the cursor-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of `total` is estimated.
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - total
                - isEstimatedTotal
                - next
                - previous
              x-property-sort:
                - total
                - isEstimatedTotal
                - next
                - previous
            CursorBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the cursor-based pagination strategy;
                a total element count is not supported.
              properties:
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - next
                - previous
              x-property-sort:
                - next
                - previous
            OffsetBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the offset-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of "total" is estimated.
              required:
                - total
                - isEstimatedTotal
              x-property-sort:
                - total
                - isEstimatedTotal
            OffsetBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the offset-based pagination strategy;
                a total element count is not supported.
              properties:
                hasNext:
                  type: boolean
                  description: >-
                    Flag indicating that a subsequent request with the same
                    parameters, except that the parameter `pagination.offset` is
                    incremented by `pagination.limit`, would yield additional
                    results.
              required:
                - hasNext
              x-property-sort:
                - hasNext
            PartialOutputObject:
              type: object
              properties:
                isPartial:
                  type: boolean
                  description: >-
                    Flag indicating that the response is a possibly incomplete
                    array or an object containing a possibly incomplete array,
                    due to hitting a processing time limit. If `true`, some
                    matching results might be missing from the array, or
                    elements for matching results might be incorrectly included
                    (for example, when priority sorting would have removed the
                    element). Depending on the use case, such a response may be
                    unsuitable.
              description: >-
                Object denoting that the endpoint response is possibly
                incomplete.
              required:
                - isPartial
              x-property-sort:
                - isPartial
          basePath: /wealth/v1
          schemes:
            - https
          securityDefinitions:
            Basic:
              type: nu
    overlays:
      - type: APIs.io Search
        url: overlays/etf-profile-and-prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/etf-profile-and-prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-etf-profile-and-prices-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---