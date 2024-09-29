---
name: Broker Detail
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/broker-detail.png
url: https://example.com/apis/broker-detail.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Broker Detail
apis:
  - name: FactSet Estimates API
    description: >-
      20+ years of comprehensive estimates and statistics on a wide variety of
      financial statement items as well as industry-specific metrics. FactSet’s
      consensus estimates are aggregated from a wide base of contributors and
      cover over 19,000 active…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-estimates-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Estimates
          tags:
            - name: Consensus
              description: >-
                The consensus or nest of all Estimates items aggregated by a
                statistic such as mean or median.
            - name: Broker Detail
              description: >-
                The Broker-Level detail of Estimates items. Entitlements with
                Brokers are required.
            - name: Ratings
              description: >-
                The Consensus and Broker-Level Ratings detail for Buy, Hold,
                Sell, Overweight, Underweight.
            - name: Surprise
              description: >-
                The Surprise Events reflecting the company's reported financials
                against the broker's estimates.
            - name: Segments
              description: The Product or Geographic Segment Estimates
            - name: Data Items
              description: >-
                Available Data Item Catalog to be used as input to the metrics
                parameters
          paths:
            /factset-estimates/v2/rolling-consensus:
              get:
                tags:
                  - Retrieves
                  - Consensus
                  - Estimates
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Rolling
                  - Fiscal
                  - Periods.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                summary: >-
                  Retrieves consensus estimates for a requested list of ids and
                  rolling fiscal periods.
                description: >
                  Returns FactSet Estimates consensus data using rolling fiscal
                  dates. <p>The rolling behavior causes fiscal year to
                  automatically roll from one year to the next as the historical
                  perspective date changes. The fiscal period rolls forward as
                  of each period end. This endpoint is optimized to allow the
                  request to simply include a relative fiscal period (e.g. use
                  relativeFiscalStart integer 1 and periodicity ANN for next
                  unreported fiscal year end), and then see what the consensus
                  thought the "next fiscal year" estimates were through time as
                  you "roll" back your perspective dates. This differs from
                  locking down an absolute estimate period such as explicitly
                  stating Fiscal Year 2019. This can be done in the
                  fixed-consensus endpoint.</p>
              post:
                tags:
                  - Retrieves
                  - Consensus
                  - Estimates
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Rolling
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                summary: >-
                  Retrieves consensus estimates for a requested list of ids and
                  rolling fiscal periods
                description: >
                  Returns FactSet Estimates consensus data using rolling fiscal
                  dates. <p>The rolling behavior causes fiscal year to
                  automatically roll from one year to the next as the historical
                  perspective date changes. The fiscal period rolls forward as
                  of each period end. This endpoint is optimized to allow the
                  request to simply include a relative fiscal period (e.g. use
                  relativeFiscalStart integer 1 and periodicity ANN for next
                  unreported fiscal year end), and then see what the consensus
                  thought the "next fiscal year" estimates were through time as
                  you "roll" back your perspective dates. This differs from
                  locking down an absolute estimate period such as explicitly
                  stating Fiscal Year 2019. This can be done in the
                  fixed-consensus endpoint.</p>
            /factset-estimates/v2/fixed-consensus:
              get:
                tags:
                  - Retrieves
                  - Consensus
                  - Estimates
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Fixed
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                summary: >-
                  Retrieves consensus estimates for a requested list of ids and
                  fixed fiscal periods
                description: >
                  Returns FactSet Estimates consensus data using fixed fiscal
                  dates. For example, if the company's current unreported year
                  is 12/2020, all data returned by formulas that specify as the
                  period/report basis will be for 12/2005 regardless of what
                  perspective dates (startDate/endDate) are used. The fixed
                  dates are "locked" in time and all estimated values are for
                  that explicit date. If you are requesting that the estimated
                  periods can change with the perspective date, please use the
                  rolling-consensus endpoint.
              post:
                tags:
                  - Fact
                  - Set
                  - Consensus
                  - Estimates
                  - For
                  - Fixed
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                summary: FactSet consensus estimates for fixed fiscal periods
                description: >
                  Returns FactSet Estimates consensus data using fixed fiscal
                  dates. For example, if the company's current unreported year
                  is 12/2020, all data returned by formulas that specify as the
                  period/report basis will be for 12/2005 regardless of what
                  perspective dates (startDate/endDate) are used. The fixed
                  dates are "locked" in time and all estimated values are for
                  that explicit date. If you are requesting that the estimated
                  periods can change with the perspective date, please use the
                  rolling-consensus endpoint.
            /factset-estimates/v2/rolling-detail:
              get:
                tags:
                  - Fact
                  - Set
                  - Estimates
                  - Detail
                  - Data
                  - For
                  - Rolling
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                summary: FactSet estimates detail data for rolling fiscal periods
                description: >
                  Updated intraday, the FactSet detail estimates apis provide
                  individual broker-level estimates collected from over 800
                  sell-side analysts. This database contains 20+ years of broker
                  history across more than 59,000 global companies. Content is
                  provided for "rolling" fiscal periods.     
              post:
                tags:
                  - Fact
                  - Set
                  - Estimates
                  - Detail
                  - Data
                  - For
                  - Rolling
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                summary: FactSet estimates detail data for rolling fiscal periods
                description: >
                  Updated intraday, the FactSet detail estimates apis provide
                  individual broker-level estimates collected from over 800
                  sell-side analysts. This database contains 20+ years of broker
                  history across more than 59,000 global companies. Content is
                  provided for "rolling" fiscal periods.
            /factset-estimates/v2/fixed-detail:
              get:
                tags:
                  - Estimates
                  - Detail
                  - Data
                  - For
                  - Fixed
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                summary: Estimates detail data for fixed fiscal periods
                description: >
                  Updated intraday, the FactSet detail estimates apis provide
                  individual broker-level estimates collected from over 800
                  sell-side analysts. This database contains 20+ years of broker
                  history across more than 59,000 global companies. Content is
                  provided for "fixed" fiscal periods.
              post:
                tags:
                  - Estimates
                  - Detail
                  - Data
                  - For
                  - Fixed
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                summary: Estimates detail data for fixed fiscal periods
                description: >
                  Updated intraday, the FactSet detail estimates apis provide
                  individual broker-level estimates collected from over 800
                  sell-side analysts. This database contains 20+ years of broker
                  history across more than 59,000 global companies. Content is
                  provided for "fixed" fiscal periods.
            /factset-estimates/v2/consensus-ratings:
              get:
                tags:
                  - Ratings
                  - Consensus
                  - Estimates
                  - To
                  - Fetch
                  - Buy,
                  - Overweight,
                  - Hold,
                  - Underweight,
                  - And
                  - Sell.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                summary: >-
                  Ratings consensus estimates to fetch Buy, Overweight, Hold,
                  Underweight, and Sell.
                description: >
                  Returns ratings from the FactSet Estimates database for
                  current and historical for an individual security using
                  rolling fiscal dates as of a specific date.
              post:
                tags:
                  - Ratings
                  - Consensus
                  - Estimates
                  - To
                  - Fetch
                  - Buy,
                  - Overweight,
                  - Hold,
                  - Underweight,
                  - And
                  - Sell.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                summary: >-
                  Ratings consensus estimates to fetch Buy, Overweight, Hold,
                  Underweight, and Sell.
                description: >
                  Returns ratings from the FactSet Estimates database for
                  current and historical for an individual security using
                  rolling fiscal dates as of a specific date.
            /factset-estimates/v2/detail-ratings:
              get:
                tags:
                  - Broker
                  - Detail
                  - Estimates
                  - To
                  - Fetch
                  - Buy,
                  - Overweight,
                  - Hold,
                  - Underweight,
                  - And
                  - Sell.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                summary: >-
                  Broker Detail estimates to fetch Buy, Overweight, Hold,
                  Underweight, and Sell.
                description: >
                  Retrieves the Broker Level ratings for the requested Id and
                  date range. Ratings include Buy, Hold, Sell, Overweight, and
                  Underweight.

                  <p>The `startDate` and `endDate` parameters controls the range
                  of perspective dates. By default, the service will return the
                  range of estimateDates within the latest company's reporting
                  period. As you expand the date range, additional full
                  historical reporting periods and all ratings estimateDates per
                  broker will be returned.</p>
              post:
                tags:
                  - Broker
                  - Detail
                  - Estimates
                  - To
                  - Fetch
                  - Buy,
                  - Overweight,
                  - Hold,
                  - Underweight,
                  - And
                  - Sell.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                summary: >-
                  Broker Detail estimates to fetch Buy, Overweight, Hold,
                  Underweight, and Sell.
                description: >
                  Retrieves the Broker Level ratings for the requested Id and
                  date range. Ratings include Buy, Hold, Sell, Overweight, and
                  Underweight.

                  <p>The `startDate` and `endDate` parameters controls the range
                  of perspective dates. By default, the service will return the
                  range of estimateDates within the latest company's reporting
                  period. As you expand the date range, additional full
                  historical reporting periods and all ratings estimateDates per
                  broker will be returned.</p>
            /factset-estimates/v2/surprise:
              get:
                tags:
                  - Surprise
                  - Estimates
                  - For
                  - Rolling
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                summary: Surprise estimates for rolling fiscal periods
                description: >
                  Returns FactSet Estimates surprise data using rolling fiscal
                  dates.
              post:
                tags:
                  - Surprise
                  - Estimates
                  - For
                  - Rolling
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                summary: Surprise estimates for rolling fiscal periods
                description: >
                  Returns FactSet Estimates surprise data using rolling fiscal
                  dates.
            /factset-estimates/v2/segments:
              get:
                tags:
                  - Retrieves
                  - Product
                  - Geographic
                  - Segment
                  - Estimates
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                  - Segments
                summary: >-
                  Retrieves product & geographic segment estimates for a
                  requested list of ids and fiscal periods
                description: >
                  Returns FactSet Estimates Consensus Data for the segments
                  gathered from the Business, Geographical, or Actual
                  Reconciliation (ADJUSTMENT) classifications by using fiscal
                  periods with a reporting frequency. 
              post:
                tags:
                  - Retrieves
                  - Product
                  - Segment
                  - Estimates
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Fiscal
                  - Periods
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                  - Segments
                summary: >-
                  Retrieves product segment estimates for a requested list of
                  ids and fiscal periods
                description: >
                  Returns FactSet Estimates Data for the segments gathered from
                  the Business, Geographical, or Actual Reconciliation
                  (ADJUSTMENT) classifications by using fiscal periods with a
                  reporting frequency. 
            /factset-estimates/v2/metrics:
              get:
                summary: Available Estimate metrics
                tags:
                  - Available
                  - Estimate
                  - Metrics
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                  - Segments
                  - Metrics
                description: >
                  Returns list of available Estimate metrics that can be used in
                  the `metrics` parameter of related endpoints.

                  **By default, Factset provides Estimated items in millions.
                  For specific metric methodology definitions, reference the
                  `OAurl` response items to launch the available methodology
                  page.** 
              post:
                summary: Available Estimate metrics or ratios.
                tags:
                  - Available
                  - Estimate
                  - Metrics
                  - Or
                  - Ratios.
                  - Factset
                  - Estimates
                  - V2
                  - Rolling
                  - Consensus
                  - Fixed
                  - Detail
                  - Ratings
                  - Surprise
                  - Segments
                  - Metrics
                description: >
                  Returns list of available Estimate metrics that can be used in
                  the `metrics` parameter of related endpoints.

                  **By default, Factset provides Estimated items in millions.
                  For specific metric methodology definitions, reference the
                  `OAurl` response items to launch the available 
    overlays:
      - type: APIs.io Search
        url: overlays/estimates-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/estimates-openapi-api-evangelist-ratings.yml
    aid: factset:factset-estimates-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---