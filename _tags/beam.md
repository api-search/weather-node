---
name: Beam
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/beam.png
url: https://example.com/apis/beam.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Beam
apis:
  - name: Open FactSet Partners - Documents
    description: 'Access to all job listing files provided by the OFM Partners: LinkUp'
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/openfactset-partners-documents
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/openfactset-partners-documents#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/openfactset-partners-documents#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/openfactset-partners-documents#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/openfactset-partners-documents#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/openfactset-partners-documents#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Open:FactSet - Partners
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: >-
              https://developer.factset.com/api-catalog/openfactset-partners-documents
          paths:
            /linkup/job-listings:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Link
                  - Up.
                  - Up
                  - Provides
                  - Access
                  - To
                  - Job
                  - Listings
                  - Dataset
                  - That
                  - Is
                  - Sourced
                  - Directly
                  - Employer
                  - Webistes
                  - Globally
                  - Delivered
                  - Daily.
                  - Linkup
                  - Job
                  - Listings
                summary: >-
                  Returns the  daily files from Open:FactSet Partner - LinkUp.
                  The LinkUp API provides access to job listings dataset that is
                  sourced directly from employer webistes globally delivered
                  daily.
                description: >-
                  Returns the  daily files from Open:FactSet Partner - LinkUp.
                  The LinkUp API provides access to job listings dataset that is
                  sourced directly from employer webistes globally delivered
                  daily. **This API is no longer being sold for new clients.**
            /orbit/transcripts/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Orbit.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                summary: Returns the daily files from Open:FactSet Partner - Orbit.
                description: Returns the daily files from Open:FactSet Partner - Orbit.
            /orbit/transcripts/history:
              get:
                tags:
                  - Returns
                  - The
                  - History
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Orbit
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                summary: Returns the history files from Open:FactSet Partner - Orbit
                description: >-
                  Returns the historical files from February 28th, 2005 to
                  current date. 
            /ozmosi/clinical-trials/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Clinical
                  - Trial
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                summary: >-
                  Returns the daily files of Clinical Trial Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of Clinical Trial Details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/diseases/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Diseases
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner-
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                summary: >-
                  Returns the daily files of Diseases Details from Open:FactSet
                  Partner- Ozmosi.
                description: >-
                  Returns the daily files of Diseases Details from Open:FactSet
                  Partner- Ozmosi.
            /ozmosi/biomarkers/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Biomarkers
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                summary: >-
                  Returns the daily files of Biomarkers Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of Biomarkers Details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/beam-endpoints/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Beam
                  - Endpoints
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                summary: >-
                  Returns the daily files of Beam Endpoints Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of Beam Endpoints Details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/primaryoutcome/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Primary
                  - Outcome
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                summary: >-
                  Returns the daily files of PrimaryOutcome Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of PrimaryOutcome Details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/orangepurple/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Orange
                  - Purple
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                summary: >-
                  Returns the daily files of OrangePurple Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of OrangePurple Details from
                  Open:FaStset Partner - Ozmosi.
            /ozmosi/intervention/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Intervention
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                summary: >-
                  Returns the daily files of Intervention details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of Intervention details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/sponsors/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Sponsors
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                  - Sponsors
                summary: >-
                  Returns the daily files of Sponsors Details from Open:FactSet
                  Partner - Ozmosi.
                description: >-
                  Returns the daily files of Sponsors Details from Open:FactSet
                  Partner - Ozmosi.
            /ozmosi/collaborators/daily:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - Of
                  - Collaborators
                  - Details
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                  - Sponsors
                  - Collaborators
                summary: >-
                  Returns the daily files of Collaborators Details from
                  Open:FactSet Partner - Ozmosi.
                description: >-
                  Returns the daily files of Collaborators Details from
                  Open:FactSet Partner - Ozmosi.
            /ozmosi/clinical-trials/history:
              get:
                tags:
                  - Returns
                  - The
                  - History
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Ozmosi
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                  - Sponsors
                  - Collaborators
                summary: Returns the history files from Open:FactSet Partner - Ozmosi
                description: >-
                  Returns the historical files from June 23rd, 2005 to current
                  date.
            /luxembourg/green-bonds/daily:
              get:
                tags:
                  - Returns
                  - Daily
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Luxembourg
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                  - Sponsors
                  - Collaborators
                  - Luxembourg
                  - Green
                  - Bonds
                summary: Returns daily files from Open:FactSet Partner - Luxembourg
                description: >
                  Returns XML files and relevant metadata provided by Open:
                  FactSet Partner – Luxembourg.
            /scripts-asia/transcripts:
              get:
                tags:
                  - Returns
                  - The
                  - Daily
                  - Files
                  - From
                  - 'Open:'
                  - Fact
                  - Set
                  - Partner
                  - Scripts
                  - Asia.
                  - Linkup
                  - Job
                  - Listings
                  - Orbit
                  - Transcripts
                  - Daily
                  - History
                  - Ozmosi
                  - Clinical
                  - Trials
                  - Diseases
                  - Biomarkers
                  - Beam
                  - Endpoints
                  - Primaryoutcome
                  - Orangepurple
                  - Intervention
                  - Sponsors
                  - Collaborators
                  - Luxembourg
                  - Green
                  - Bonds
                  - Scripts
                  - Asia
                summary: >-
                  Returns the daily files from Open:FactSet Partner - Scripts
                  Asia.
                description: >-
                  Returns XML files and relevant metadata provided by Open:
                  FactSet Partner – Scripts Asia.

                  - type=delta returns the files from March 1st 2023 to current
                  date.

                  - type=full will returns the files from start of date until
                  Feb 28th 2023.
          tags:
            - name: Luxembourg
              description: >
                <a
                href=https://go.factset.com/marketplace/catalog/product/lgx-datahub>Luxembourg</a>
                API provides access to Green Bonds data. 
            - name: Orbit
              description: >
                <a
                href=https://go.factset.com/marketplace/catalog/product/china-a-shares-transcripts>Orbit</a>
                API covers full universe of almost 4,800 companies since the
                early 2000's. Content covers 3 types, both in Chinese and
                English: 1) Earning Call Transcripts 2) Public disclosures on
                broker onsite research 3) Executive official responses on online
                platforms.
            - name: Ozmosi
              description: >
                <a
                href=https://open.factset.com/partners/ozmosi/en-us>Ozmosi</a>
                API provides access to Clinical Trials data.
            - name: Scripts Asia
              description: >-
                Scripts Asia API provides access to Asia Pacific regional
                collected transcripts.
            - name: LinkUp
              description: >
                <a
                href=https://go.factset.com/marketplace/catalog/product/linkup-raw>LinkUp</a>
                API provides access t
    overlays:
      - type: APIs.io Search
        url: overlays/open-partners-documents-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/open-partners-documents-openapi-api-evangelist-ratings.yml
    aid: factset:open-factset-partners-documents
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---