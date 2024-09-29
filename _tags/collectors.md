---
name: Collectors
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/collectors.png
url: https://example.com/apis/collectors.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Collectors
apis:
  - name: migrationhubstrategy
    description: >-
      <p><fullname>Migration Hub Strategy Recommendations</fullname> <p>This API
      reference provides descriptions, syntax, and other details about each of
      the actions and data types for Migration Hub Strategy Recommendations
      (Strategy Recommendations). The topic for each action shows the API
      request parameters and the response. Alternatively, you can use one of the
      AWS SDKs to access an API that is tailored to the programming language or
      platform that you're using. For more information, see <a
      href="http://aws.amazon.com/tools/#SDKs">AWS SDKs</a>.</p></p>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: migrationhubstrategy
          paths:
            /get-applicationcomponent-details/{applicationComponentId}:
              GET:
                summary: GetApplicationComponentDetails
                description: <p> Retrieves details about an application component. </p>
                tags:
                  - Get
                  - Applications
                  - Components
                  - Details
                  - Components
                  - Identifiers
            /get-applicationcomponent-strategies/{applicationComponentId}:
              GET:
                summary: GetApplicationComponentStrategies
                description: >-
                  <p> Retrieves a list of all the recommended strategies and
                  tools for an application component running on a server. </p>
                tags:
                  - Get
                  - Applications
                  - Components
                  - Strategies
                  - Components
                  - Identifiers
            /get-assessment/{id}:
              GET:
                summary: GetAssessment
                description: <p> Retrieves the status of an on-going assessment. </p>
                tags:
                  - Get
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
            /get-import-file-task/{id}:
              GET:
                summary: GetImportFileTask
                description: <p> Retrieves the details about a specific import task. </p>
                tags:
                  - Get
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
            /get-latest-assessment-id:
              GET:
                summary: GetLatestAssessmentId
                description: <p>Retrieve the latest ID of a specific assessment task.</p>
                tags:
                  - Get
                  - Latest
                  - Assessments
                  - Identifiers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
            /get-portfolio-preferences:
              GET:
                summary: GetPortfolioPreferences
                description: >-
                  <p> Retrieves your migration and modernization preferences.
                  </p>
                tags:
                  - Get
                  - Portfolio
                  - Preferences
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
            /get-portfolio-summary:
              GET:
                summary: GetPortfolioSummary
                description: >-
                  <p> Retrieves overall summary including the number of servers
                  to rehost and the overall number of anti-patterns. </p>
                tags:
                  - Get
                  - Portfolio
                  - Summaries
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
            /get-recommendation-report-details/{id}:
              GET:
                summary: GetRecommendationReportDetails
                description: >-
                  <p> Retrieves detailed information about the specified
                  recommendation report. </p>
                tags:
                  - Get
                  - Recommendations
                  - Reports
                  - Details
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /get-server-details/{serverId}:
              GET:
                summary: GetServerDetails
                description: >-
                  <p> Retrieves detailed information about a specified server.
                  </p>
                tags:
                  - Get
                  - Server
                  - Details
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /get-server-strategies/{serverId}:
              GET:
                summary: GetServerStrategies
                description: >-
                  <p> Retrieves recommended strategies and tools for the
                  specified server. </p>
                tags:
                  - Get
                  - Server
                  - Strategies
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
            /list-analyzable-servers:
              POST:
                summary: ListAnalyzableServers
                description: >-
                  <p>Retrieves a list of all the servers fetched from customer
                  vCenter using Strategy Recommendation Collector.</p>
                tags:
                  - Lists
                  - Analyzable
                  - Servers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
            /list-applicationcomponents:
              POST:
                summary: ListApplicationComponents
                description: >-
                  <p> Retrieves a list of all the application components
                  (processes). </p>
                tags:
                  - Lists
                  - Applications
                  - Components
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
            /list-collectors:
              GET:
                summary: ListCollectors
                description: <p> Retrieves a list of all the installed collectors. </p>
                tags:
                  - Lists
                  - Collectors
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /list-import-file-task:
              GET:
                summary: ListImportFileTask
                description: <p> Retrieves a list of all the imports performed. </p>
                tags:
                  - Lists
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /list-servers:
              POST:
                summary: ListServers
                description: <p> Returns a list of all the servers. </p>
                tags:
                  - Lists
                  - Servers
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
            /put-portfolio-preferences:
              POST:
                summary: PutPortfolioPreferences
                description: >-
                  <p> Saves the specified migration and modernization
                  preferences. </p>
                tags:
                  - Put
                  - Portfolio
                  - Preferences
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
            /start-assessment:
              POST:
                summary: StartAssessment
                description: <p> Starts the assessment of an on-premises environment. </p>
                tags:
                  - Start
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
            /start-import-file-task:
              POST:
                summary: StartImportFileTask
                description: <p> Starts a file import. </p>
                tags:
                  - Start
                  - Import
                  - File
                  - Tasks
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
            /start-recommendation-report-generation:
              POST:
                summary: StartRecommendationReportGeneration
                description: <p> Starts generating a recommendation report. </p>
                tags:
                  - Start
                  - Recommendations
                  - Reports
                  - Generation
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
            /stop-assessment:
              POST:
                summary: StopAssessment
                description: <p> Stops the assessment of an on-premises environment. </p>
                tags:
                  - Stop
                  - Assessments
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
            /update-applicationcomponent-config/:
              POST:
                summary: UpdateApplicationComponentConfig
                description: >-
                  <p> Updates the configuration of an application component.
                  </p>
                tags:
                  - Update
                  - Applications
                  - Components
                  - Configurations
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
                  - Update
                  - Application Components
                  - Configurations
            /update-server-config/:
              POST:
                summary: UpdateServerConfig
                description: <p> Updates the configuration of the specified s
                tags:
                  - Update
                  - Server
                  - Configurations
                  - Components
                  - Identifiers
                  - Get
                  - Assessments
                  - Import
                  - File
                  - Tasks
                  - Latest
                  - Portfolio
                  - Preferences
                  - Summaries
                  - Recommendations
                  - Reports
                  - Details
                  - Lists
                  - Analyzable
                  - Servers
                  - Application Components
                  - Collectors
                  - Put
                  - Start
                  - Generation
                  - Stop
                  - Update
                  - Application Components
                  - Configurations
                  - Serv
    overlays:
      - type: APIs.io Search
        url: overlays/migrationhubstrategy-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/migrationhubstrategy-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:migrationhubstrategy
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---