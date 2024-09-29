---
name: Anomalous
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anomalous.png
url: https://example.com/apis/anomalous.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anomalous
apis:
  - name: devops-guru
    description: >-
      <p> Amazon DevOps Guru is a fully managed service that helps you identify
      anomalous behavior in business critical operational applications. You
      specify the Amazon Web Services resources that you want DevOps Guru to
      cover, then the Amazon CloudWatch metrics and Amazon Web Services
      CloudTrail events related to those resources are analyzed. When anomalous
      behavior is detected, DevOps Guru creates an <i>insight</i> that includes
      recommendations, related events, and related metrics that can help you
      improve your operational applications. For more information, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html">What
      is Amazon DevOps Guru</a>. </p> <p> You can specify 1 or 2 Amazon Simple
      Notification Service topics so you are notified every time a new insight
      is created. You can also enable DevOps Guru to generate an OpsItem in
      Amazon Web Services Systems Manager for each insight to help you manage
      and track your work addressing insights. </p> <p> To learn about the
      DevOps Guru workflow, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html#how-it-works">How
      DevOps Guru works</a>. To learn about DevOps Guru concepts, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/concepts.html">Concepts
      in DevOps Guru</a>. </p>
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
            title: devops-guru
          paths:
            /channels:
              POST:
                summary: ListNotificationChannels
                description: >-
                  <p> Returns a list of notification channels configured for
                  DevOps Guru. Each notification channel is used to notify you
                  when DevOps Guru generates an insight that contains
                  information about how to improve your operations. The one
                  supported notification channel is Amazon Simple Notification
                  Service (Amazon SNS). </p>
                tags:
                  - Lists
                  - Notifications
                  - Channels
                  - Channels
            /insights/{Id}:
              GET:
                summary: DescribeInsight
                description: >-
                  <p> Returns details about an insight that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Insight
                  - Channels
                  - Identifiers
            /accounts/health:
              GET:
                summary: DescribeAccountHealth
                description: >-
                  <p> Returns the number of open reactive insights, the number
                  of open proactive insights, and the number of metrics analyzed
                  in your Amazon Web Services account. Use these numbers to
                  gauge the health of operations in your Amazon Web Services
                  account. </p>
                tags:
                  - Describe
                  - Account
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
            /accounts/overview:
              POST:
                summary: DescribeAccountOverview
                description: >-
                  <p> For the time range passed in, returns the number of open
                  reactive insight that were created, the number of open
                  proactive insights that were created, and the Mean Time to
                  Recover (MTTR) for all closed reactive insights. </p>
                tags:
                  - Describe
                  - Account
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /anomalies/{Id}:
              GET:
                summary: DescribeAnomaly
                description: >-
                  <p> Returns details about an anomaly that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Anomaly
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /event-sources:
              PUT:
                summary: UpdateEventSourcesConfig
                description: >-
                  <p>Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon CodeGuru Profiler, which
                  can produce proactive recommendations which can be stored and
                  viewed in DevOps Guru.</p>
                tags:
                  - Update
                  - Events
                  - Sources
                  - Configurations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
            /feedback:
              PUT:
                summary: PutFeedback
                description: >-
                  <p> Collects customer feedback about the specified insight.
                  </p>
                tags:
                  - Put
                  - Feedback
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
            /organization/health:
              POST:
                summary: DescribeOrganizationHealth
                description: >-
                  <p>Returns active insights, predictive insights, and resource
                  hours analyzed in last hour.</p>
                tags:
                  - Describe
                  - Organizations
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/overview:
              POST:
                summary: DescribeOrganizationOverview
                description: >-
                  <p>Returns an overview of your organization's history based on
                  the specified time range. The overview includes the total
                  reactive and proactive insights.</p>
                tags:
                  - Describe
                  - Organizations
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/health/resource-collection:
              POST:
                summary: DescribeOrganizationResourceCollectionHealth
                description: >-
                  <p>Provides an overview of your system's health. If additional
                  member accounts are part of your organization, you can filter
                  those accounts using the <code>AccountIds</code> field.</p>
                tags:
                  - Describe
                  - Organizations
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
            /accounts/health/resource-collection/{ResourceCollectionType}:
              GET:
                summary: DescribeResourceCollectionHealth
                description: >-
                  <p> Returns the number of open proactive insights, open
                  reactive insights, and the Mean Time to Recover (MTTR) for all
                  closed insights in resource collections in your account. You
                  specify the type of Amazon Web Services resources collection.
                  The two types of Amazon Web Services resource collections
                  supported are Amazon Web Services CloudFormation stacks and
                  Amazon Web Services resources that contain the same Amazon Web
                  Services tag. DevOps Guru can be configured to analyze the
                  Amazon Web Services resources that are defined in the stacks
                  or that are tagged using the same tag <i>key</i>. You can
                  specify up to 500 Amazon Web Services CloudFormation stacks.
                  </p>
                tags:
                  - Describe
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
            /service-integrations:
              PUT:
                summary: UpdateServiceIntegration
                description: >-
                  <p> Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon Web Services Systems
                  Manager, which can be used to create an OpsItem for each
                  generated insight. </p>
                tags:
                  - Update
                  - Services
                  - Integrations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
            /cost-estimation:
              PUT:
                summary: StartCostEstimation
                description: >-
                  <p>Starts the creation of an estimate of the monthly cost to
                  analyze your Amazon Web Services resources.</p>
                tags:
                  - Start
                  - Cost
                  - Estimation
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /resource-collections/{ResourceCollectionType}:
              GET:
                summary: GetResourceCollection
                description: >-
                  <p> Returns lists Amazon Web Services resources that are of
                  the specified resource collection type. The two types of
                  Amazon Web Services resource collections supported are Amazon
                  Web Services CloudFormation stacks and Amazon Web Services
                  resources that contain the same Amazon Web Services tag.
                  DevOps Guru can be configured to analyze the Amazon Web
                  Services resources that are defined in the stacks or that are
                  tagged using the same tag <i>key</i>. You can specify up to
                  500 Amazon Web Services CloudFormation stacks. </p>
                tags:
                  - Get
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /anomalies/insight/{InsightId}:
              POST:
                summary: ListAnomaliesForInsight
                description: >-
                  <p> Returns a list of the anomalies that belong to an insight
                  that you specify using its ID. </p>
                tags:
                  - Lists
                  - Anomalies
                  - For
                  - Insight
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
            /list-log-anomalies:
              POST:
                summary: ListAnomalousLogGroups
                description: >-
                  <p> Returns the list of log groups that contain log anomalies.
                  </p>
                tags:
                  - Lists
                  - Anomalous
                  - Logs
                  - Groups
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
            /events:
              POST:
                summary: ListEvents
                description: >-
                  <p> Returns a list of the events emitted by the resources that
                  are evaluated by DevOps Guru. You can use filters to specify
                  which events are returned. </p>
                tags:
                  - Lists
                  - Events
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
            /insights:
              POST:
                summary: ListInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time and status (<code>ONGOING</code>,
                  <code>CLOSED</code>, or <code>ANY</code>). </p>
                tags:
                  - Lists
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
            /monitoredResources:
              POST:
                summary: ListMonitoredResources
                description: >-
                  <p> Returns the list of all log groups that are being
                  monitored and tagged by DevOps Guru. </p>
                tags:
                  - Lists
                  - Monitored
                  - Resources
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /organization/insights:
              POST:
                summary: ListOrganizationInsights
                description: >-
                  <p>Returns a list of insights associated with the account or
                  OU Id.</p>
                tags:
                  - Lists
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /recommendations:
              POST:
                summary: ListRecommendations
                description: >-
                  <p> Returns a list of a specified insight's recommendations.
                  Each recommendation includes a list of related metrics and a
                  list of related events. </p>
                tags:
                  - Lists
                  - Recommendations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /channels/{Id}:
              DELETE:
                summary: RemoveNotificationChannel
                description: >-
                  <p> Removes a notification channel from DevOps Guru. A
                  notification channel is used to notify you when DevOps Guru
                  generates an insight that contains information about how to
                  improve your operations. </p>
                tags:
                  - Removes
                  - Notifications
                  - Channels
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /insights/search:
              POST:
                summary: SearchInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time, one or more statuses (<code>ONGOING</code> or
                  <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /organization/insights/search:
              POST:
                summary: SearchOrganizationInsights
                description: >-
                  <p> Returns a list of insights in your organization. You can
                  specify which insights are returned by their start time, one
                  or more statuses (<code>ONGOING</code>, <code>CLOSED</code>,
                  and <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /resource-collections:
              PUT:
                summary: UpdateResourceCollection
                description: >-
                  <p> Updates the collection of resources that DevOps Guru
                  analyzes. The two types of Amazon Web Services resource
                  collections supported are Amazon Web Services CloudFormation
                  stacks and Amazon Web Services resources that contain the same
                  Amazon Web Services tag. DevOps Guru can be configured to
                  analyze the Amazon Web Services resources that are defined in
                  the stacks or that are tagged using the same tag <i>key</i>.
                  You can specify up to 500 Amazon Web Services CloudFormation
                  stacks. This method also creates the IAM role required for you
                  to use DevOps 
                tags:
                  - Update
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
                  - Collections
    overlays:
      - type: APIs.io Search
        url: overlays/devops-guru-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/devops-guru-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:devops-guru
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---