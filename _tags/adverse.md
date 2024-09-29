---
name: Adverse
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/adverse.png
url: https://example.com/apis/adverse.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Adverse
apis:
  - name: FactSet ESG API
    description: FactSet ESG API giving access to SASB & SDG Score data
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-esg-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-esg-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/factset-esg-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-esg-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/factset-esg-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-esg-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet ESG API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/factset-esg-api
          tags:
            - name: SASB
              description: >-
                Get scores and ranks based on the 26 SASB categories for a
                requested list of symbols and date range.
            - name: SDG
              description: >-
                Get scores and ranks based on the 16 SDG goals for a requested
                list of symbols and date range.
            - name: SFDR
              description: >-
                Get the Principle Adverse Impact PAI data supporting the SFDR
                reporting.
            - name: Spotlights
              description: >-
                Get Spotlight data for the most important positive and negative
                ESG events
            - name: Articles
              description: >-
                Get Articles data for the most important positive and negative
                ESG events
          paths:
            /factset-esg/v1/sasb-scores:
              get:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '26'
                  - Categories
                  - Defined
                  - By
                  - Sustainability
                  - Accounting
                  - Standards
                  - Board
                  - B).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  26 ESG categories defined by the Sustainability Accounting
                  Standards Board (SASB).
                description: >
                  FactSet Truvalue Labs SASB Scores provides short-term,
                  long-term, and momentum scores that are generated for 26 ESG
                  categories defined by the Sustainability Accounting Standards
                  Board. FactSet Truvalue also calculates a custom overall score
                  called ALLCATEGORIES, can indicate data volume flow, and the
                  Dynamic Materiality of that data flow.
              post:
                tags:
                  - For
                  - Large
                  - List
                  - Of
                  - Ids,
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '26'
                  - Categories
                  - Defined
                  - By
                  - Sustainability
                  - Accounting
                  - Standards
                  - Board
                  - B).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                summary: >-
                  For a large list of ids, gets short-term, long-term, and
                  momentum scores based on the 26 ESG categories defined by the
                  Sustainability Accounting Standards Board (SASB).
                description: >
                  FactSet Truvalue Labs SASB Scores provides short-term,
                  long-term, and momentum scores that are generated for 26 ESG
                  categories defined by the Sustainability Accounting Standards
                  Board. FactSet Truvalue also calculates a custom overall score
                  called ALLCATEGORIES, can indicate data volume flow, and the
                  Dynamic Materiality of that data flow.
            /factset-esg/v1/sasb-ranks:
              get:
                tags:
                  - Gets
                  - Rankings
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Dates.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                summary: Gets ESG Rankings for a requested list of ids and dates.
                description: >
                  Indicates if a company is a Leader, Above Average, Average,
                  Below Average, or a Laggard; directly mapping from Industry
                  Percentiles (*request IND_PCTL in scores endpoints*). Mapping
                  of ESG Ranks to Industry Percentile Ranges is as follows - 


                  |Rank|Industry Percentile Range (%)|

                  |||

                  |Leader|90 - 100|

                  |Above Average|70 - 89.9|

                  |Average|30 - 69.9|

                  |Below Average|10 - 29.9|

                  |Laggard|0 - 9.9|


                  Industry classifications follow SICS, SASB's Industry
                  Classification System. Using the Adjusted Insight scores,
                  Industry Percentiles are generated for all companies.
                  Companies with five or more articles in a year get ranked in a
                  first pass, then companies with filled-in values are
                  interpolated without forcing the ranking of higher-volume
                  companies up or down.  In the case where a company falls into
                  an industry with fewer than 7 high or medium volume companies
                  the Sector Percentile is inserted in the place of the Industry
                  Percentile score.

                  <p>Only Vaild for ALLCATEGORIES and MATERIALITY
                  categories.</p>
              post:
                tags:
                  - Get
                  - Ranks
                  - For
                  - Large
                  - List
                  - Of
                  - Ids
                  - And
                  - Specified
                  - Date
                  - Range.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                summary: >-
                  Get ESG Ranks for a large list of ids and specified date
                  range.
                description: >
                  Indicates if a company is a Leader, Above Average, Average,
                  Below Average, or a Laggard; directly mapping from Industry
                  Percentiles (*request IND_PCTL in scores endpoints*). Mapping
                  of ESG Ranks to Industry Percentile Ranges is as follows - 


                  |Rank|Industry Percentile Range (%)|

                  |||

                  |Leader|90 - 100|

                  |Above Average|70 - 89.9|

                  |Average|30 - 69.9|

                  |Below Average|10 - 29.9|

                  |Laggard|0 - 9.9|


                  Industry classifications follow SICS, SASB's Industry
                  Classification System. Using the Adjusted Insight scores,
                  Industry Percentiles are generated for all companies.
                  Companies with five or more articles in a year get ranked in a
                  first pass, then companies with filled-in values are
                  interpolated without forcing the ranking of higher-volume
                  companies up or down.  In the case where a company falls into
                  an industry with fewer than 7 high or medium volume companies
                  the Sector Percentile is inserted in the place of the Industry
                  Percentile score.

                  <p>Only Vaild for ALLCATEGORIES and MATERIALITY
                  categories.</p>
            /factset-esg/v1/sasb-scores-all:
              get:
                tags:
                  - Gets
                  - Flat
                  - Key
                  - Value
                  - Array
                  - Of
                  - Scores
                  - For
                  - Named
                  - Categories
                  - The
                  - Input
                  - Score
                  - Type(s).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                summary: >-
                  Gets a flat key value array of scores for named categories of
                  the input scoreType(s).
                description: >
                  **Retrieves a flat array of all categories for the requested
                  scoreType and ids. Unlike the /sasb-scores endpoint the format
                  of the response returns category names as part of the key
                  value.**<p> Gets values for all categories for the selected
                  score type(s) for the requested identifier(s). FactSet
                  Truvalue Labs SASB Scores provides short-term, long-term, and
                  momentum scores that are generated for 26 ESG categories
                  defined by the Sustainability Accounting Standards Board. ESG
                  Ranks are not supported in this Endpoint.
              post:
                tags:
                  - Gets
                  - Flat
                  - Key
                  - Value
                  - Array
                  - Of
                  - Scores
                  - For
                  - Named
                  - Categories
                  - The
                  - Input
                  - Score
                  - Type(s).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                summary: >-
                  Gets a flat key value array of scores for named categories of
                  the input score type(s).
                description: >
                  **Retrieves a flat array of all categories for the requested
                  scoreType and ids. Unlike the /sasb-scores endpoint the format
                  of the response returns category names as part of the key
                  value.**<p> Gets values for all categories for the selected
                  score type(s) for the requested identifier(s). FactSet
                  Truvalue Labs SASB Scores provides short-term, long-term, and
                  momentum scores that are generated for 26 ESG categories
                  defined by the Sustainability Accounting Standards Board. ESG
                  Ranks are not supported in this Endpoint.
            /factset-esg/v1/sdg-scores:
              get:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '16'
                  - Sustainable
                  - Development
                  - Goals
                  - Categories
                  - Defined
                  - By
                  - United
                  - Nations.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  16 Sustainable Development Goals categories defined by the
                  United Nations.
                description: >
                  Truvalue Labs SDG Scores provides short-term, long-term, and
                  momentum scores that are generated for 16 Sustainable
                  Development Goals categories defined by the United Nations.
              post:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '16'
                  - Sustainable
                  - Development
                  - Goals
                  - Categories
                  - Defined
                  - By
                  - United
                  - Nations.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  16 Sustainable Development Goals categories defined by United
                  Nations.
                description: >
                  Truvalue Labs SDG Scores provides short-term, long-term, and
                  momentum scores that are generated for 16 Sustainable
                  Development Goals categories defined by the United Nations.*
            /factset-esg/v1/sfdr-pai:
              get:
                tags:
                  - Gets
                  - Principle
                  - Adverse
                  - Impact
                  - I)
                  - Data
                  - To
                  - Support
                  - Compliant
                  - Sustainable
                  - Finance
                  - Disclosure
                  - Regulation
                  - R)
                  - Reporting
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                summary: >-
                  Gets Principle Adverse Impact (PAI) data to support compliant
                  SFDR Sustainable Finance Disclosure Regulation (SFDR)
                  reporting
                description: >
                  SFDR Principle Adverse Impact (PAI) data is built specifically
                  to support compliant Sustainable Finance Disclosure Regulation
                  (SFDR) reporting. FactSet collects PAI data items from
                  publicly available company-reported information and FactSet
                  databases, such as FactSet Fundamentals, FactSet RBICS with
                  Revenue and FactSet People, which are also based on
                  company-disclosures. FactSet uses Truvalue Labs SASB
                  Spotlights for supplemental OECD & UNGC violation checks where
                  company reporting is sparse. 
              post:
                tags:
                  - Gets
                  - Principle
                  - Adverse
                  - Impact
                  - I)
                  - Data
                  - To
                  - Support
                  - Compliant
                  - Sustainable
                  - Finance
                  - Disclosure
                  - Regulation
                  - R)
                  - Reporting
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                summary: >-
                  Gets Principle Adverse Impact (PAI) data to support compliant
                  SFDR Sustainable Finance Disclosure Regulation (SFDR)
                  reporting
                description: >
                  SFDR Principle Adverse Impact (PAI) data is built specifically
                  to support compliant Sustainable Finance Disclosure Regulation
                  (SFDR) reporting. FactSet collects PAI data items from
                  publicly available company-reported information and FactSet
                  databases, such as FactSet Fundamentals, FactSet RBICS with
                  Revenue and FactSet People, which are also based on
                  company-disclosures. FactSet uses Truvalue Labs SASB
                  Spotlights for supplemental OECD & UNGC violation checks where
                  company reporting is sparse.
            /factset-esg/v1/sasb-spotlights:
              get:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. 
              post:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. reporting is sparse.
            /factset-esg/v1/sdg-spotlights:
              get:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. 
              post:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. reporting is sparse.
            /factset-esg/v1/sasb-articles:
              get:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SASB lens categories from
                  2016-01-01 to previous day.
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
              post:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SASB lens categories from
                  2016-01-01 to previous day
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
            /factset-esg/v1/sdg-articles:
              get:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SDG lens categories from
                  2016-01-01 to previous day.
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
              post:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SDG lens categories from
                  2016-01-01 to previous day
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also
                  transparency 
    overlays:
      - type: APIs.io Search
        url: overlays/esg-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/esg-openapi-api-evangelist-ratings.yml
    aid: factset:factset-esg-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---