---
name: Background
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/background.png
url: https://example.com/apis/background.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Background
apis:
  - name: FactSet Real-Time Quotes API
    description: >-
      The Quotes API combines endpoints for retrieving security end-of-day,
      delayed, and realtime prices with performance key figures and basic
      reference data on the security and market level.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-quotes-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Quotes API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /basic/assetClass/list:
              get:
                tags:
                  - List
                  - Of
                  - Asset
                  - Classes.
                  - Class
                  - List
                description: List of asset classes as defined by FactSet Digital Solutions.
                summary: List of asset classes.
            /basic/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                summary: List of background text types.
                description: List of background text types.
            /basic/benchmark/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Benchmark
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                summary: List of benchmark types.
                description: List of benchmark types.
            /basic/delivery/list:
              post:
                tags:
                  - List
                  - Of
                  - Deliveries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                summary: List of deliveries.
                description: List of deliveries.
            /basic/frequency/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Frequency
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                summary: List of frequency types.
                description: List of frequency types.
            /basic/language/get:
              get:
                tags:
                  - Details
                  - For
                  - Language.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                description: Details for a language.
                summary: Details for a language.
            /basic/language/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Language
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: Details for a language identified by code.
                summary: Details for a language identified by code.
            /basic/language/list:
              get:
                tags:
                  - List
                  - Of
                  - Languages.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: List of languages.
                summary: List of languages.
            /basic/market/get:
              get:
                tags:
                  - Details
                  - Of
                  - Market.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: Details of a market.
                summary: Details of a market.
            /basic/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: List of markets.
                summary: List of markets.
            /basic/market/group/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Groups.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market groups.
                summary: List of market groups.
            /basic/market/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market types.
                summary: List of market types.
            /basic/media/kind/list:
              get:
                tags:
                  - List
                  - Of
                  - Media
                  - Kinds.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                summary: List of media kinds.
                description: List of media kinds.
            /basic/media/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Internet
                  - Media
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                description: >-
                  List of Internet media types. See
                  http://www.iana.org/assignments/media-types/ for further
                  details. Not all such Internet media types are available on
                  the MDG.
                summary: List of Internet media types.
            /basic/mic/operating/list:
              post:
                tags:
                  - List
                  - Of
                  - Operating
                  - Market
                  - Identifier
                  - Codes
                  - C).
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                summary: List of operating market identifier codes (MIC).
                description: List of operating market identifier codes (MIC).
            /basic/region/get:
              get:
                tags:
                  - Details
                  - For
                  - Region.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: Details for a region.
                description: Details for a geographic, political, or economic region.
            /basic/region/list:
              get:
                tags:
                  - List
                  - Of
                  - Regions.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: List of regions.
                description: List of geographic, political, and economic regions.
            /basic/region/continent/get:
              get:
                tags:
                  - Details
                  - For
                  - Continent.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: Details for a continent.
                description: Details for a continent.
            /basic/region/continent/list:
              get:
                tags:
                  - List
                  - Of
                  - Continents.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: List of continents.
                description: List of continents.
            /basic/region/country/get:
              get:
                tags:
                  - Details
                  - For
                  - Country.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country.
                description: Details for a country.
            /basic/region/country/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Country
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country identified by code.
                description: Details for a country identified by code.
            /basic/region/country/list:
              get:
                tags:
                  - List
                  - Of
                  - Countries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: List of countries.
                description: List of countries.
            /basic/timezone/get:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                description: >-
                  Details of a timezone identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone.
            /basic/timezone/getByName:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone
                  - Identified
                  - By
                  - Name.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  Details of a timezone identified by name, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone identified by name.
            /basic/timezone/list:
              post:
                tags:
                  - List
                  - Of
                  - Timezones.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  List of timezones identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: List of timezones.
            /basic/valueUnit/get:
              get:
                tags:
                  - Details
                  - Of
                  - Value
                  - Unit.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: Details of a value unit.
                description: Details of a value unit.
            /basic/valueUnit/list:
              post:
                tags:
                  - List
                  - Of
                  - Value
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: List of value units.
                description: List of value units.
            /basic/valueUnit/alternative/list:
              get:
                tags:
                  - List
                  - Of
                  - Alternative
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                description: List of alternative units.
                summary: List of alternative units.
            /basic/valueUnit/currency/list:
              post:
                tags:
                  - List
                  - Of
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                summary: List of currencies.
                description: List of currencies.
            /basic/valueUnit/currency/fractional/get:
              get:
                tags:
                  - Details
                  - Of
                  - Fractional
                  - Currency.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: Details of a fractional currency.
                description: Details of a fractional currency.
            /basic/valueUnit/currency/fractional/list:
              get:
                tags:
                  - List
                  - Of
                  - Fractional
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: List of fractional currencies.
                description: List of fractional currencies.
            /basic/valueUnit/currency/main/list:
              post:
                tags:
                  - List
                  - Of
                  - Main
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                summary: List of main currencies.
                description: List of main currencies.
            /category/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: Details of a category.
                description: Details of a category.
            /category/list:
              get:
                tags:
                  - List
                  - Of
                  - Categories.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: List of categories.
                description: List of categories.
            /category/listByLevel:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                summary: List of categories assigned to a category level.
                description: List of categories assigned to a category level.
            /category/listBySystem:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                summary: List of categories assigned to a category system.
                description: List of categories assigned to a category system.
            /category/dataset/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Datasets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                summary: List of entitled category datasets.
                description: List of entitled category datasets.
            /category/instrument/list:
              get:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Where
                  - Specific
                  - Dataset
                  - Has
                  - Assigned
                  - Given
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
                description: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
            /category/level/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: Details of a category level.
                description: Details of a category level.
            /category/path/get:
              get:
                tags:
                  - Path
                  - From
                  - The
                  - First
                  - Level
                  - To
                  - Of
                  - Specific
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Path from the first level to the level of a specific category.
                description: Path from the first level to the level of a specific category.
            /category/system/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Entitled
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Details of an entitled category system.
                description: Details of an entitled category system.
            /category/system/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Systems.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of entitled category systems.
                description: List of entitled category systems.
            /category/system/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Category
                  - System
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of category system types.
                description: List of category system types.
            /instrument/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/getByNotation:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/backgroundText/list:
              get:
                tags:
                  - Background
                  - Texts
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: Background texts of an instrument.
                description: Background texts of an instrument.
            /instrument/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of background text types for instruments.
                description: List of background text types for instruments.
            /instrument/benchmark/list:
              post:
                tags:
                  - List
                  - Of
                  - Benchmarks
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of benchmarks of a financial instrument.
                description: >-
                  Provides a list of benchmark notations for a selected
                  financial instrument, optionally restricted to specific
                  benchmark types.
            /instrument/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Instrument
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see.
                description: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
            /instrument/complianceProperty/list:
              post:
                tags:
                  - List
                  - Of
                  - Compliance
                  - Properties
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: List of compliance properties for instruments.
                description: List of compliance properties for instruments.
            /instrument/complianceProperty/listByInstrument:
              get:
                tags:
                  - Compliance
                  - Properties
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: Compliance properties of an instrument.
                description: Compliance properties of an instrument.
            /instrument/composite/get:
              get:
                tags:
                  - Composite
                  - Instrument
                  - And
                  - Its
                  - Components.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                summary: Composite instrument and its components.
                description: Composite instrument and its components.
            /instrument/coupon/list:
              get:
                tags:
                  - List
                  - Of
                  - Coupons
                  - For
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                summary: List of coupons for an interest-bearing instrument.
                description: >-
                  List of coupons for an interest-bearing instrument; any other
                  instrument yields empty values. The endpoint provides details
                  regarding the coupon period, the respective interest rate, and
                  payable amount (the latter only for instruments with a fixed
                  nominal value). The list of coupons is generally not available
                  for a perpetual, i.e. without a predefined maturity date,
                  interst-bearing instrument. 


                  If there is no entitled provider supplying a full list of
                  coupons, the list will be synthesized from summary data
                  available from entitled suppliers (if any). Since the exact
                  product terms are not known, e.g. the handling of holidays and
                  weekends, the list may be imprecise.
            /instrument/coupon/dayCountConvention/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Day
                  - Count
                  - Convention
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                summary: List of day count convention types.
                description: List of day count convention types.
            /instrument/coupon/interestRate/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Interest
                  - Rate
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                summary: List of interest rate types.
                description: List of interest rate types.
            /instrument/coupon/keyData/get:
              get:
                tags:
                  - Interest
                  - Rate
                  - Details
                  - For
                  - Selected
                  - Periods
                  - Of
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                summary: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument.
                description: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument; any other instrument yields empty
                  values.
            /instrument/crossReference/getByISIN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given ISIN to the respective most recent
                  instrument identifier, retrieved from the Cross Reference
                  Service.
                summary: Translate ISIN to instrument.
            /instrument/crossReference/getByWKN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given WKN to the respective most recent instrument
                  identifier, retrieved from the Cross Reference Service.
                summary: Translate WKN to instrument.
            /instrument/crossReference/listByISIN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of ISINs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of ISINs to instruments.
            /instrument/crossReference/listByWKN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of WKNs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of WKNs to instruments.
            /instrument/crossReference/history/getByISIN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given ISIN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: ISIN to instrument translation history.
            /instrument/crossReference/history/getByWKN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given WKN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: WKN to instrument translation history.
            /instrument/exchangeRate/get:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the
                  identifier of the main currencies represented by that exchange
                  rate. 

                   An error is returned if one of the provided parameters is invalid or if no instrument is associated with the given combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/exchangeRate/getByISOCode:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the ISO
                  4217 code of the main currencies represented by that exchange
                  rate. 


                  An error is returned if one of the provided parameters is
                  invalid or if no instrument is associated with the given
                  combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/legalEntity/backgroundText/list:
              get:
                tags:
                  - Role-specific
                  - Background
                  - Texts
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                summary: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
                description: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
            /instrument/legalEntity/complianceProperty/list:
              get:
                tags:
                  - Role-specific
                  - Compliance
                  - Properties
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                summary: >-
                  Role-specific compliance properties of legal entities related
                  to an instrument.
                description: >-
                  Role-specic compliance properties of legal entities related to
                  an instrument.
            /instrument/mifid/get:
              get:
                tags:
                  - Mi
                  - Data
                  - For
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                description: >-
                  MiFID II data for a specified financial instrument. The
                  instruments governed by MiFID II are called "investment
                  products".
                summary: MiFID II data for a financial instrument.
            /instrument/notation/list:
              post:
                tags:
                  - List
                  - Of
                  - Active,
                  - Entitled
                  - Notations
                  - For
                  - Set
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                summary: List of active, entitled notations for a set of instruments.
                description: >-
                  List of active, entitled notations for a set of instruments.
                  By default the list of notations (per instrument) is sorted
                  descending by the trading volume, averaged over one month. All
                  identifiers used as parameters must be valid and entitled.
            /instrument/rating/grade/list:
              post:
                tags:
                  - List
                  - Of
                  - Rating
                  - Grades
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  List of rating grades for a list of instruments. The list can
                  be restricted to rating grades belonging to particular rating
                  systems.
                summary: List of rating grades for a list of instruments.
            /instrument/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Instrument-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: Set of custom instrument-level selection lists.
                summary: Set of custom instrument-level selection lists.
            /instrument/selectionList/listByInstrument:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Instrument,
                  - Returns
                  - The
                  - Instrument-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Instrument
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
                summary: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
            /instrument/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Belonging
                  - To
                  - An
                  - Instrument-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                summary: >-
                  List of instruments belonging to an instrument-level selection
                  list.
                description: >-
                  List of instruments belonging to an instrument-level selection
                  list.
            /notation/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a notation.
                summary: Basic data for a notation.
            /notation/list:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a list of notations.
                summary: Basic data for a list of notations.
            /notation/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Notation
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
                summary: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see.
            /notation/crossReference/getByFactSetMarketSymbol:
              get:
                tags:
                  - Translate
                  - Fact
                  - Set
                  - Market
                  - Symbol
                  - To
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: Translate a FactSet market symbol to a notation.
                description: >-
                  Translate a FactSet market symbol to a notation. This symbol
                  is also known as TICKER_EXCHANGE.
            /notation/crossReference/listByInstrument:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listByISIN:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listBySymbol:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: >-
                  List of entitled notations. Symbols are not globally unique;
                  therefore, a given symbol interpreted in different markets
                  might refer to different instruments.
            /notation/crossReference/factSetIdentifier/get:
              get:
                tags:
                  - Retrieve
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve FactSet identifiers for a given notation.
                description: >-
                  <p>Retrieve FactSet identifiers for a given notation. Security
                  and listing-level identifiers are always included, regional
                  level identifiers are included, if available.
            /notation/crossReference/factSetIdentifier/listByFactSetIdentifier:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Notations
                  - For
                  - Given
                  - Fact
                  - Set
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of notations for a given FactSet identifier.
                description: >-
                  <p>Retrieve a list of notations for a given FactSet
                  identifier, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>See the group
                  description for more information about the security's primary
                  listing.</p>
            /notation/crossReference/factSetIdentifier/listByInstrument:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of FactSet identifiers for a given instrument.
                description: >-
                  <p>Retrieve a list of FactSet identifiers for a given
                  instrument, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>The result
                  contains only notations that have at least one FactSet
                  identifier (see
                  <big><tt>listing.permanentIdentifier</tt></big>,
                  <big><tt>listing.tickerExchange</tt></big>).</p><p>See the
                  group description for more information about the security's
                  primary listing.</p>
            /notation/keyFigures/year/10/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: End-of-day (EOD) key figures for the time range of ten years.
                description: End-of-day (EOD) key figures for the time range of ten years.
            /notation/keyFigures/year/10/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
            /notation/keyFigures/month/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: End-of-day (EOD) key figures for the time range of one month.
                description: End-of-day (EOD) key figures for the time range of one month.
            /notation/keyFigures/month/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
            /notation/keyFigures/week/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one week.
                description: End-of-day (EOD) key figures for the time range of one week.
            /notation/keyFigures/week/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
            /notation/keyFigures/year/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one year.
                description: End-of-day (EOD) key figures for the time range of one year.
            /notation/keyFigures/year/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
            /notation/keyFigures/month/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
            /notation/keyFigures/month/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
            /notation/keyFigures/year/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
            /notation/keyFigures/year/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
            /notation/keyFigures/year/5/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of five years.
                description: End-of-day (EOD) key figures for the time range of five years.
            /notation/keyFigures/year/5/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
            /notation/keyFigures/month/6/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of six months.
                description: End-of-day (EOD) key figures for the time range of six months.
            /notation/keyFigures/month/6/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
            /notation/keyFigures/year/7/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
            /notation/keyFigures/year/7/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
            /notation/keyFigures/yearToDate/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D)..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD)..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD). The time range YTD begins with the last trading day of
                  the previous calendar year for which EOD prices are available
                  and ends with the most recent trading day of the current
                  calendar year for which EOD prices are available..
            /notation/keyFigures/yearToDate/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D),
                  - List
                  - Of
                  - Notations..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations. The time range YTD begins with
                  the last trading day of the previous calendar year for which
                  EOD prices are available and ends with the most recent
                  tradingday of the current calendar year for which EOD prices
                  are available..
            /notation/keyFigures/tradingDay/average/get:
              get:
                tags:
                  - Average
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - Different
                  - Trading
                  - Days
                  - Periods.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods. A trading day is a calendar day on that trading
                  of the notation was possible.
                summary: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods.
            /notation/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets
                  - With
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  List of markets with entitled notations. The list contains
                  only markets with at least one active and entitled notation. 

                  All identifiers used as parameters must be valid and entitled.
                summary: List of markets with entitled notations.
            /notation/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Notation-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: Set of custom notation-level selection lists.
                summary: Set of custom notation-level selection lists.
            /notation/selectionList/listByNotation:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Notation,
                  - Returns
                  - The
                  - Notation-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Notation
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
                summary: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
            /notation/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Notations
                  - Belonging
                  - To
                  - Notation-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                summary: >-
                  List of notations belonging to a notation-level selection
                  list.
                description: >-
                  List of notations belonging to a notation-level selection
                  list.
            /notation/status/get:
              get:
                tags:
                  - Intraday
                  - Trading
                  - Status
                  - Of
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                description: >-
                  Intraday trading status of a notation.<br>The endpoint is
                  subscribable to provide push updates. See attribute
                  `_subscriptionMinimalInterval` for valid update rates.
                summary: Intraday trading status of a notation.
            /prices/get:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/list:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
            /prices/bidAsk/get:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/bidAsk/list:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
            /prices/orderbook/aggregated/get:
              get:
                tags:
                  - Orderbook
                  - Aggregated
                  - By
                  - Price.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                summary: Orderbook aggregated by price.
                description: Orderbook aggregated by price.
            /prices/orderbook/full/get:
              get:
                tags:
                  - Full
                  - Orderbook
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                summary: Full orderbook
                description: Full orderbook
            /prices/tradingSchedule/event/list:
              post:
                tags:
                  - Sequence
                  - Of
                  - Market-related
                  - Events.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Sequence of market-related events.
                description: >-
                  Sequence of market-related events like the opening time or
                  closing time of a market of a specific
                  notation.<br><br>Pagination to a previous page is not
                  supported and `pagination.previous` is always `null`.
            /prices/tradingSchedule/event/type/list:
              get:
                tags:
                  - Trading
                  - Schedule
                  - Event
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Trading schedule event types.
                description: >-
                  Trading schedule event types define the events which may occur
                  during any period of trading. Types of trading schedule events
                  are for instance OPEN, CLOSE, END_OF_DAY.
            /instrument/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for instruments.
                description: >-
                  Search for instruments whose ISIN, specified NSINs, or name
                  match the search value according to a tolerant full-text match
                  algorithm. Better matching results appear in the response
                  before less relevant matches.
            /notation/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for notations.
                description: >-
                  Search for a notation whose ISIN, specified NSINs, name, or
                  symbol match the search value according to a tolerant
                  full-text match algorithm. If more than one notation of an
                  instrument matches, only the notation with the highest
                  monetary trading volume, averaged over one month, is
                  considered. Better matching results appear in the response
                  before less relevant matches. If the parameter popularity is
                  set to true, the popularity of the notation is the primary
                  sort criterion. Popularity is affected mostly by the request
                  frequency of the notation.
            /notation/searchByText:
              post:
                tags:
                  - Text-based
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Text-based search for notations.
                description: >-
                  Text-based search for notations in selected identifier and
                  name attributes according to a tolerant full-text match
                  algorithm. The results satisfy all selected filters; sorting
                  by various attributes is possible. If more than one notation
                  of an instrument matches, only the notation with the best
                  market priority (according to the parameter `market.priority`)
                  or, in the absence of market priorities, only the notation
                  with the highest trading volume, averaged over one month, is
                  considered.     
                   All identifiers used as parameters must be valid and entitled.
          tags:
            - name: basic
              description: basic endpoints
            - name: category
              description: category endpoints
            - name: instrument
              description: instrument endpoints
            - name: notation
              description: notation endpoints
            - name: prices
              description: prices endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-quotes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-quotes-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-quotes-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---