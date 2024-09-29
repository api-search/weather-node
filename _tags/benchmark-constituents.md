---
name: Benchmark Constituents
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/benchmark-constituents.png
url: https://example.com/apis/benchmark-constituents.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Benchmark Constituents
apis:
  - name: FactSet Benchmarks API
    description: >-
      Returns Benchmark Constituent data including weights, price, and market
      value for a specified date.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-benchmarks-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Benchmarks API
          paths:
            /factset-benchmarks/v1/constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.  
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.
            /factset-benchmarks/v1/fixed-income-constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Fixed
                  - Income
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
            /factset-benchmarks/v1/index-snapshot:
              get:
                summary: >-
                  Index Level Prices, Returns, and related information as of a
                  single date.
                tags:
                  - Index
                  - Level
                  - Prices,
                  - Returns,
                  - And
                  - Related
                  - Information
                  - As
                  - Of
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  specific date. Simply submit a valid Benchmark ID (you can use
                  the /id-list endpoint for a sample list of ids), and date and
                  retrieve Index Level Prices, Returns, and related information.
              post:
                summary: >-
                  Retrieves the Index Level Snapshot of Prices and Returns
                  information for a given identifier and single date.
                tags:
                  - Retrieves
                  - The
                  - Index
                  - Level
                  - Snapshot
                  - Of
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - Given
                  - Identifier
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/index-history:
              get:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  date range requested. Simply submit a valid Benchmark ID (you
                  can use the /id-list endpoint for a sample list of ids), and
                  date range to retrieve Index Level Prices, Returns, and
                  related information.
              post:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/ratios:
              get:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines fundamental, estimates, and pricing content to derive
                  ratios and per share values for global equity market indexes
                  and commercial benchmark vendors. The constituents of the
                  index are fetched on rolling basis over time period requested,
                  and then the metric requested is aggregated up to the index
                  level. To learn more about FMA, visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
              post:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines FactSet Fundamental, FactSet Estimates, and FactSet
                  Pricing content to derive ratios and per share values for
                  global equity market indexes and commercial benchmark vendors.
                  The constituents of the index are fetched on rolling basis
                  over time period requested, and then the metric requested is
                  aggregated up to the index level. To learn more about FMA,
                  visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
            /factset-benchmarks/v1/id-list:
              get:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to FactSet Support. *</p>
              post:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to F
    overlays:
      - type: APIs.io Search
        url: overlays/benchmarks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/benchmarks-openapi-api-evangelist-ratings.yml
    aid: factset:factset-benchmarks-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---