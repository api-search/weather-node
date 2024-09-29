---
name: Costs
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/costs.png
url: https://example.com/apis/costs.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Costs
apis:
  - name: FactSet Funds API
    description: Reference and Time Series Mutual Fund Data
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-funds-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-funds-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/factset-funds-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-funds-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-funds-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-funds-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Funds API
          tags:
            - name: Reference
              description: >-
                Basic reference data for funds, including summary, status,
                benchmark details, classifications, and more.
            - name: Prices & Returns
              description: Fetch Fund Price (NAV) and Returns over a requested time-series.
            - name: Fund Flows & AUM
              description: Fetch Fund AUM and Fund Flows over a requested time-series.
            - name: Helper
              description: Check the Fund's current status and database availability
          paths:
            /factset-funds/v1/summary:
              get:
                tags:
                  - Get
                  - Basic
                  - Reference
                  - Summary
                  - Data
                  - For
                  - Fund.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                summary: Get basic reference summary data for a Fund.
                description: >
                  Fetch basic reference data for the requested fund(s),
                  including countryDomicile, shrClass, shrClassInceptDate, etc. 
              post:
                tags:
                  - Get
                  - Basic
                  - Reference
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                summary: Get basic reference data for a large list of Fund ids.
                description: >
                  Fetch basic reference data for the requested fund(s),
                  including countryDomicile, shrClass, shrClassInceptDate, etc. 
            /factset-funds/v1/classifications:
              get:
                tags:
                  - Get
                  - Basic
                  - Fund
                  - Classifications
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                summary: Get basic Fund Classifications
                description: >
                  Fetch basic fund classification data, such as Asset Class,
                  Category, Focus, Niche, Region, and more.<p> FactSet Mutual
                  Funds Reference uses FactSet's proprietary Fund Classification
                  System, which categorizes funds using a rules-based system
                  that is derived from seven core classifications. This system
                  evaluates the asset class, economic development level, and
                  geographical region as described in each fund's prospectus and
                  marketing materials. Fund exposure details are presented on
                  successively granular levels- category, then focus, and then
                  niche. Moreover, FactSet Fund Reference captures over 40
                  unique data points for U.S. mutual funds. All data items are
                  grouped in one of two levels, either as a Fund or as a Share
                  Class.</p><p>For more details regarding FactSet's Fund
                  Classification, visit Online Assistant
                  [21436](https://my.apps.factset.com/oa/pages/21436) or
                  download - [FactSet Fund Classification System Rules &
                  Methodology](https://my.apps.factset.com/oa/cms/oaAttachment/4547a2f4-5df5-4ec9-a0d3-7d51610dd637/26837)</p><p>

                  |Classification Type|Description|

                  |||

                  |Asset Class|The asset class of the fund (e.g. Equity, Fixed
                  Income, Currency, Commodities, Asset Allocation, or
                  Alternatives) based on the fund's mandate.|

                  |Category|The 1st of 3 asset-class-specific, hierarchical
                  exposure tiers; the broadest category the fund falls under
                  within its asset class (e.g., Size & Style, Sector, Precious
                  Metals, Absolute Returns); based on the fund's mandate.|

                  |Focus|The 2nd of 3 asset-class-specific, hierarchical
                  exposure tiers; the fund's classification within its category
                  (e.g. Small Cap, Energy, Palladium, Long/Short); based on the
                  fund's mandate.|

                  |Niche|The 3rd of 3 asset-class-specific, hierarchical
                  exposure tiers; The fund's classification within its Focus.
                  Most granular tier of exposure sort (e.g., Growth, Coal,
                  Physically held, Merger Arbitrage); based on the fund's
                  mandate.|

                  |Economic Development Level|The country development level of
                  the fund (Developed, Emerging, Frontier, or Blended) based on
                  the fund's mandate.|

                  |Region|The broad regional exposure of the fund (e.g., Latin
                  America, Asia-Pacific, Global) based on the fund's mandate.|

                  |Specific Geography|The specific geographic exposure of the
                  fund (e.g., Developed Europe, Chile, Asia-Pacific Ex-Japan)
                  based on the fund's mandate.|

                  </p>
              post:
                tags:
                  - Get
                  - Basic
                  - Fund
                  - Classifications
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                summary: Get basic Fund Classifications for a large list of ids.
                description: >
                  Fetch basic fund classification data, such as Asset Class,
                  Category, Focus, Niche, Region, and more.<p> FactSet Mutual
                  Funds Reference uses FactSet's proprietary Fund Classification
                  System, which categorizes funds using a rules-based system
                  that is derived from seven core classifications. This system
                  evaluates the asset class, economic development level, and
                  geographical region as described in each fund's prospectus and
                  marketing materials. Fund exposure details are presented on
                  successively granular levels- category, then focus, and then
                  niche. Moreover, FactSet Fund Reference captures over 40
                  unique data points for U.S. mutual funds. All data items are
                  grouped in one of two levels, either as a Fund or as a Share
                  Class.</p><p>For more details regarding FactSet's Fund
                  Classification, visit Online Assistant
                  [21436](https://my.apps.factset.com/oa/pages/21436) or
                  download - [FactSet Fund Classification System Rules &
                  Methodology](https://my.apps.factset.com/oa/cms/oaAttachment/4547a2f4-5df5-4ec9-a0d3-7d51610dd637/26837)</p><p>

                  |Classification Type|Description|

                  |||

                  |Asset Class|The asset class of the fund (e.g. Equity, Fixed
                  Income, Currency, Commodities, Asset Allocation, or
                  Alternatives) based on the fund's mandate.|

                  |Category|The 1st of 3 asset-class-specific, hierarchical
                  exposure tiers; the broadest category the fund falls under
                  within its asset class (e.g., Size & Style, Sector, Precious
                  Metals, Absolute Returns); based on the fund's mandate.|

                  |Focus|The 2nd of 3 asset-class-specific, hierarchical
                  exposure tiers; the fund's classification within its category
                  (e.g. Small Cap, Energy, Palladium, Long/Short); based on the
                  fund's mandate.|

                  |Niche|The 3rd of 3 asset-class-specific, hierarchical
                  exposure tiers; The fund's classification within its Focus.
                  Most granular tier of exposure sort (e.g., Growth, Coal,
                  Physically held, Merger Arbitrage); based on the fund's
                  mandate.|

                  |Economic Development Level|The country development level of
                  the fund (Developed, Emerging, Frontier, or Blended) based on
                  the fund's mandate.|

                  |Region|The broad regional exposure of the fund (e.g., Latin
                  America, Asia-Pacific, Global) based on the fund's mandate.|

                  |Specific Geography|The specific geographic exposure of the
                  fund (e.g., Developed Europe, Chile, Asia-Pacific Ex-Japan)
                  based on the fund's mandate.|

                  </p>
            /factset-funds/v1/benchmark-details:
              get:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Primary
                  - And
                  - Segment
                  - Benchmark
                  - Details
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                summary: Get the Fund's Primary and Segment Benchmark Details
                description: >
                  Fetch the Fund's Benchmark and Segment Benchmark ids. These
                  ids can be then used in the [Benchmarks
                  API](https://developer.factset.com/api-catalog/factset-benchmarks-api)
                  to fetch index-level prices, returns, constituents data.
              post:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Primary
                  - And
                  - Segment
                  - Benchmark
                  - Details
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                summary: >-
                  Get the Fund's Primary and Segment Benchmark details for large
                  list of ids.
                description: >
                  Fetch the Fund's Benchmark and Segement Benchmark ids. These
                  ids can be then used in the [Benchmarks
                  API](https://developer.factset.com/api-catalog/factset-benchmarks-api)
                  to fetch index-level prices, returns, constituents data.
            /factset-funds/v1/costs-fees:
              get:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Costs,
                  - Investment
                  - Minimums
                  - And
                  - Risk,
                  - Fees.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                summary: Get the Fund's Costs, Investment minimums and Risk, and Fees.
                description: >
                  Fetch the Fund's Costs, Investment minimums and Risk, and
                  Fees. This subcategory includes management fees, 12b-1 fees,
                  expense ratios, and several other data items. The value for
                  each specified share class is expressed as a percentage of the
                  AUM.
              post:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Costs,
                  - Investment
                  - Minimums
                  - And
                  - Risk,
                  - Fees
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                summary: >-
                  Get the Fund's Costs, Investment minimums and Risk, and Fees
                  for large list of ids.
                description: >
                  Fetch the Fund's Costs, Investment minimums and Risk, and
                  Fees. Data Items include Expense Ratios, investment minimums
                  and maximums, swing prices, entry and exit expenses, and more.
            /factset-funds/v1/managers:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Fund
                  - Managers
                  - And
                  - Related
                  - Details
                  - For
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                summary: >-
                  Get a list of Fund Managers and related details for a list of
                  ids.
                description: >
                  Fetch basic Fund manager details, such as Title, Phone, Job Id
                  and Name. NOTE - A subscription to FactSet's Ownership product
                  is required to access formulas in this Asset Managers
                  subcategory.
              post:
                tags:
                  - Get
                  - List
                  - Of
                  - Fund
                  - Managers
                  - And
                  - Related
                  - Details
                  - For
                  - Large
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                summary: >-
                  Get a list of Fund Managers and related details for a large
                  list of ids.
                description: >
                  Fetch basic Fund manager details, such as Title, Phone, Job Id
                  and Name. 
            /factset-funds/v1/related-funds:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Related
                  - Funds
                  - For
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                summary: Get a list of Related Funds for a list of Fund ids.
                description: >
                  Fetch the five related fund share classes. Fund share classes
                  can be related if they belong to the same Fund Classification
                  segment, have the same share class type, have the same legal
                  structure, and have the same country of primary exchange.
                  Beyond the baseline criteria, the five most relevant funds are
                  determined based on whether they follow the same benchmark,
                  have the same maturity, and have the same selection strategy
                  as the specified share class.
              post:
                tags:
                  - Get
                  - List
                  - Of
                  - Related
                  - Funds
                  - For
                  - Large
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                summary: Get a list of Related Funds for a large list of Fund ids.
                description: >
                  Fetch the five related fund share classes. Fund share classes
                  can be related if they belong to the same Fund Classification
                  segment, have the same share class type, have the same legal
                  structure, and have the same country of primary exchange.
                  Beyond the baseline criteria, the five most relevant funds are
                  determined based on whether they follow the same benchmark,
                  have the same maturity, and have the same selection strategy
                  as the specified share class.
            /factset-funds/v1/prices:
              get:
                tags:
                  - Get
                  - Fund
                  - Prices
                  - V)
                  - For
                  - Requested
                  - Time-series
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                summary: Get Fund Prices (NAV) for a requested time-series
                description: >
                  Get Fund Prices (NAV) for a requested date range and list of
                  ids.
              post:
                tags:
                  - Get
                  - Fund
                  - Prices
                  - V)
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                summary: >-
                  Get Fund Prices (NAV) for a requested date range and large
                  list of ids.
                description: >
                  Fetch fund prices (NAV) as of a requested date range and a
                  large list of ids. 
            /factset-funds/v1/returns:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - Requested
                  - Time-series
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                summary: Get Fund Returns for a requested time-series
                description: >
                  Get Fund NAV Returns over a time-series for the requested date
                  range and frequency. <p>The simple Total Return NAV shows the
                  fund's total return level by reinvesting distributions so that
                  ex-date NAVs are increased by the distribution amount and
                  compounded thereafter. Total return NAV compounds daily and is
                  calculated from the first available NAV date of each fund. The
                  total return NAV series reflects the value that an investor
                  would own if it had purchased one share at the inception date
                  and reinvested all dividends on a Gross basis.</p><p> Control
                  the dividends to include or exclude using the dividendAdjust
                  parameter. The first available NAV date of each fund can be
                  found in the /summary endpoint as `priceFristDate`. Visit [OA
                  #21437](https://my.apps.factset.com/oa/pages/21437) for more
                  details.</p>
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - Requested
                  - Time-series
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                summary: >-
                  Get Fund Returns for a requested time-series and large list of
                  ids
                description: >
                  Get Fund NAV Returns over a time-series for the requested date
                  range and frequency. <p>The simple Total Return NAV shows the
                  fund's total return level by reinvesting distributions so that
                  ex-date NAVs are increased by the distribution amount and
                  compounded thereafter. Total return NAV compounds daily and is
                  calculated from the first available NAV date of each fund. The
                  total return NAV series reflects the value that an investor
                  would own if it had purchased one share at the inception date
                  and reinvested all dividends on a Gross basis.</p><p> Control
                  the dividends to include or exclude using the dividendAdjust
                  parameter. The first available NAV date of each fund can be
                  found in the /summary endpoint as `priceFristDate`. Visit [OA
                  #21437](https://my.apps.factset.com/oa/pages/21437) for more
                  details.</p>
            /factset-funds/v1/returns-snapshot:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date.
                description: >
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date. Use the date parameter to set the perspective
                  date, and adjust the return type to include or exclude
                  dividends using the dividendAdjust parameter. Returns Ranges
                  include - 

                  * oneWeek

                  * oneMonth

                  * threeMonth

                  * yearToDate

                  * oneYear

                  * threeYear

                  * threeYearAnnualized

                  * fiveYear

                  * fiveYearAnnualized
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date.
                description: >
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date. Use the date parameter to set the perspective
                  date, and adjust the return type to include or exclude
                  dividends using the dividendAdjust parameter. Returns Ranges
                  include - 

                  * oneWeek

                  * oneMonth

                  * threeMonth

                  * yearToDate

                  * oneYear

                  * threeYear

                  * threeYearAnnualized

                  * fiveYear

                  * fiveYearAnnualized 
            /factset-funds/v1/returns-range:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - User-defined
                  - Date
                  - Range
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                summary: Get Fund Returns for a user-defined date range
                description: >
                  Get Fund Returns between a specified startDate and endDate.
                  The service will compute the return between those two periods
                  to retrieve the single value and does not create a
                  time-series. Control the return type to include or exclude
                  dividends by using the dividendAdjust parameter.
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date
                  - For
                  - Large
                  - List
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date for large list of ids.
                description: >
                  Get Fund Returns between a specified startDate and endDate.
                  The service will compute the return between those two periods
                  to retrieve the single value and does not create a
                  time-series. Control the return type to include or exclude
                  dividends by using the dividendAdjust parameter.
            /factset-funds/v1/aum:
              get:
                tags:
                  - Get
                  - Fund
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                summary: Get Fund AUM for a requested date range and list of ids
                description: >
                  Get the Fund Level or Share Class Level Assets Under
                  Management (AUM). <p>NOTE - AUM can be accessed on a five-day
                  calendar. If a vendor does not provide NAV and shares
                  outstanding on a market holiday, the previous trading day
                  value is used. If a vendor does provide data on a market
                  holiday, that value will be presented, and then fund flows and
                  AUM will be calculated. When you are manually calculating
                  actual AUM on a market holiday or a rolled date, it will
                  differ from the value shown in the FactSet workstation. This
                  is due to the previous day's NAV being used in the manual AUM
                  calculation.</p>
              post:
                tags:
                  - Get
                  - Fund
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                summary: Get Fund AUM for a requested date range and large list of ids
                description: >
                  Get the Fund Level or Share Class Level Assets Under
                  Management (AUM). <p>NOTE - AUM can be accessed on a five-day
                  calendar. If a vendor does not provide NAV and shares
                  outstanding on a market holiday, the previous trading day
                  value is used. If a vendor does provide data on a market
                  holiday, that value will be presented, and then fund flows and
                  AUM will be calculated. When you are manually calculating
                  actual AUM on a market holiday or a rolled date, it will
                  differ from the value shown in the FactSet workstation. This
                  is due to the previous day's NAV being used in the manual AUM
                  calculation.</p>
            /factset-funds/v1/flows:
              get:
                tags:
                  - Get
                  - Fund
                  - Flows
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                summary: Get Fund Flows for a requested date range and list of ids
                description: >
                  Get the Fund Flows. One-day fund flows are calculated by
                  subtracting the shares outstanding at previous close from the
                  shares outstanding one day prior to close, and then
                  multiplying the result by the net asset value (NAV) of one day
                  prior to close.


                  The fund flows calculation breaks down as follows - 

                  (Shares Outstanding T0 - Shares Outstanding T-1) * NAV T-1

                  While NAVs are routinely reported on a trade-day (T0) basis,
                  industry-wide shares outstanding are a mixture of trade-day
                  and next-day values. Trade-day values are not verified, as the
                  actual creation/redemption activity takes place late in the
                  evening, after NAVs and shares outstanding values have been
                  published. The result is that multiple industry flows are
                  calculated using unverified T0 values.

                  FactSet has standardized all shares outstanding reporting on a
                  next-day basis. To ensure that assets under management (AUM)
                  and fund flows are synchronized, FactSet synchronizes shares
                  outstanding values and changes with NAVs reported on the
                  previous day, as the creations and redemptions used the
                  previous day's reported NAVs as a transaction price. <p>For
                  more information on Fund Flows Methodology, Time Windows,
                  Makret Holidays, and Missing Values, visit - [OA
                  #17863](https://my.apps.factset.com/oa/pages/17863#Flows_Calculation)</p>
              post:
                tags:
                  - Get
                  - Fund
                  - Flows
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                summary: >-
                  Get Fund Flows for a requested date range and large list of
                  ids
                description: >
                  Get the Fund Flows. One-day fund flows are calculated by
                  subtracting the shares outstanding at previous close from the
                  shares outstanding one day prior to close, and then
                  multiplying the result by the net asset value (NAV) of one day
                  prior to close.


                  The fund flows calculation breaks down as follows - 

                  (Shares Outstanding T0 - Shares Outstanding T-1) * NAV T-1

                  While NAVs are routinely reported on a trade-day (T0) basis,
                  industry-wide shares outstanding are a mixture of trade-day
                  and next-day values. Trade-day values are not verified, as the
                  actual creation/redemption activity takes place late in the
                  evening, after NAVs and shares outstanding values have been
                  published. The result is that multiple industry flows are
                  calculated using unverified T0 values.

                  FactSet has standardized all shares outstanding reporting on a
                  next-day basis. To ensure that assets under management (AUM)
                  and fund flows are synchronized, FactSet synchronizes shares
                  outstanding values and changes with NAVs reported on the
                  previous day, as the creations and redemptions used the
                  previous day's reported NAVs as a transaction price. <p>For
                  more information on Fund Flows Methodology, Time Windows,
                  Makret Holidays, and Missing Values, visit - [OA
                  #17863](https://my.apps.factset.com/oa/pages/17863#Flows_Calculation)</p>
            /factset-funds/v1/status:
              get:
                tags:
                  - Get
                  - Fund's
                  - Current
                  - Status
                  - And
                  - Database
                  - Availability
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                  - Status
                summary: Get Fund's current status and database availability
                description: >
                  Get the funds active status, share class status, and database
                  availability. Most common use is for coverage checks and id
                  resolution checks.
              post:
                tags:
                  - Get
                  - Fund's
                  - Current
                  - Status
                  - And
                  - Database
                  - Availability
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                  - Status
                summary: >-
                  Get Fund's current status and database availability for large
                  list of ids.
                description: >
                  Get the funds active status, share class status, and database
                  availability. Most common use is for coverage checks and i
    overlays:
      - type: APIs.io Search
        url: overlays/funds-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/funds-openapi-api-evangelist-ratings.yml
    aid: factset:factset-funds-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---