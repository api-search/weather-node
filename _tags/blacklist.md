---
name: Blacklist
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/blacklist.png
url: https://example.com/apis/blacklist.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Blacklist
apis:
  - name: pinpoint-email
    description: >-
      <fullname>Amazon Pinpoint Email Service</fullname> <p>Welcome to the
      <i>Amazon Pinpoint Email API Reference</i>. This guide provides
      information about the Amazon Pinpoint Email API (version 1.0), including
      supported operations, data types, parameters, and schemas.</p> <p> <a
      href="https://aws.amazon.com/pinpoint">Amazon Pinpoint</a> is an AWS
      service that you can use to engage with your customers across multiple
      messaging channels. You can use Amazon Pinpoint to send email, SMS text
      messages, voice messages, and push notifications. The Amazon Pinpoint
      Email API provides programmatic access to options that are unique to the
      email channel and supplement the options provided by the Amazon Pinpoint
      API.</p> <p>If you're new to Amazon Pinpoint, you might find it helpful to
      also review the <a
      href="https://docs.aws.amazon.com/pinpoint/latest/developerguide/welcome.html">Amazon
      Pinpoint Developer Guide</a>. The <i>Amazon Pinpoint Developer Guide</i>
      provides tutorials, code samples, and procedures that demonstrate how to
      use Amazon Pinpoint features programmatically and how to integrate Amazon
      Pinpoint functionality into mobile apps and other types of applications.
      The guide also provides information about key topics such as Amazon
      Pinpoint integration with other AWS services and the limits that apply to
      using the service.</p> <p>The Amazon Pinpoint Email API is available in
      several AWS Regions and it provides an endpoint for each of these Regions.
      For a list of all the Regions and endpoints where the API is currently
      available, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/rande.html#pinpoint_region">AWS
      Service Endpoints</a> in the <i>Amazon Web Services General Reference</i>.
      To learn more about AWS Regions, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/rande-manage.html">Managing
      AWS Regions</a> in the <i>Amazon Web Services General Reference</i>.</p>
      <p>In each Region, AWS maintains multiple Availability Zones. These
      Availability Zones are physically isolated from each other, but are united
      by private, low-latency, high-throughput, and highly redundant network
      connections. These Availability Zones enable us to provide very high
      levels of availability and redundancy, while also minimizing latency. To
      learn more about the number of Availability Zones that are available in
      each Region, see <a
      href="http://aws.amazon.com/about-aws/global-infrastructure/">AWS Global
      Infrastructure</a>.</p>
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
            title: pinpoint-email
          paths:
            /v1/email/configuration-sets:
              GET:
                summary: ListConfigurationSets
                description: >-
                  <p>List all of the configuration sets associated with your
                  Amazon Pinpoint account in the current region.</p> <p>In
                  Amazon Pinpoint, <i>configuration sets</i> are groups of rules
                  that you can apply to the emails you send. You apply a
                  configuration set to an email by including a reference to the
                  configuration set in the headers of the email. When you apply
                  a configuration set to an email, all of the rules in that
                  configuration set are applied to the email.</p>
                tags:
                  - Lists
                  - Configurations
                  - Sets
                  - V1
                  - Email
                  - Configurations
                  - Sets
            /v1/email/configuration-sets/{ConfigurationSetName}/event-destinations:
              GET:
                summary: GetConfigurationSetEventDestinations
                description: >-
                  <p>Retrieve a list of event destinations that are associated
                  with a configuration set.</p> <p>In Amazon Pinpoint,
                  <i>events</i> include message sends, deliveries, opens,
                  clicks, bounces, and complaints. <i>Event destinations</i> are
                  places that you can send information about these events to.
                  For example, you can send event data to Amazon SNS to receive
                  notifications when you receive bounces or complaints, or you
                  can use Amazon Kinesis Data Firehose to stream data to Amazon
                  S3 for long-term storage.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
            /v1/email/dedicated-ip-pools:
              GET:
                summary: ListDedicatedIpPools
                description: >-
                  <p>List all of the dedicated IP pools that exist in your
                  Amazon Pinpoint account in the current AWS Region.</p>
                tags:
                  - Lists
                  - Dedicated
                  - IP
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
            /v1/email/deliverability-dashboard/test:
              POST:
                summary: CreateDeliverabilityTestReport
                description: >-
                  <p>Create a new predictive inbox placement test. Predictive
                  inbox placement tests can help you predict how your messages
                  will be handled by various email providers around the world.
                  When you perform a predictive inbox placement test, you
                  provide a sample message that contains the content that you
                  plan to send to your customers. Amazon Pinpoint then sends
                  that message to special email addresses spread across several
                  major email providers. After about 24 hours, the test is
                  complete, and you can use the
                  <code>GetDeliverabilityTestReport</code> operation to view the
                  results of the test.</p>
                tags:
                  - Create
                  - Deliverability
                  - Tests
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
            /v1/email/identities:
              GET:
                summary: ListEmailIdentities
                description: >-
                  <p>Returns a list of all of the email identities that are
                  associated with your Amazon Pinpoint account. An identity can
                  be either an email address or a domain. This operation returns
                  identities that are verified as well as those that aren't.</p>
                tags:
                  - Lists
                  - Email
                  - Identities
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v1/email/configuration-sets/{ConfigurationSetName}:
              GET:
                summary: GetConfigurationSet
                description: >-
                  <p>Get information about an existing configuration set,
                  including the dedicated IP pool that it's associated with,
                  whether or not it's enabled for sending email, and more.</p>
                  <p>In Amazon Pinpoint, <i>configuration sets</i> are groups of
                  rules that you can apply to the emails you send. You apply a
                  configuration set to an email by including a reference to the
                  configuration set in the headers of the email. When you apply
                  a configuration set to an email, all of the rules in that
                  configuration set are applied to the email.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v1/email/configuration-sets/{ConfigurationSetName}/event-destinations/{EventDestinationName}:
              PUT:
                summary: UpdateConfigurationSetEventDestination
                description: >-
                  <p>Update the configuration of an event destination for a
                  configuration set.</p> <p>In Amazon Pinpoint, <i>events</i>
                  include message sends, deliveries, opens, clicks, bounces, and
                  complaints. <i>Event destinations</i> are places that you can
                  send information about these events to. For example, you can
                  send event data to Amazon SNS to receive notifications when
                  you receive bounces or complaints, or you can use Amazon
                  Kinesis Data Firehose to stream data to Amazon S3 for
                  long-term storage.</p>
                tags:
                  - Update
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
            /v1/email/dedicated-ip-pools/{PoolName}:
              DELETE:
                summary: DeleteDedicatedIpPool
                description: <p>Delete a dedicated IP pool.</p>
                tags:
                  - Delete
                  - Dedicated
                  - IP
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
            /v1/email/identities/{EmailIdentity}:
              GET:
                summary: GetEmailIdentity
                description: >-
                  <p>Provides information about a specific identity associated
                  with your Amazon Pinpoint account, including the identity's
                  verification status, its DKIM authentication status, and its
                  custom Mail-From settings.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
            /v1/email/account:
              GET:
                summary: GetAccount
                description: >-
                  <p>Obtain information about the email-sending status and
                  capabilities of your Amazon Pinpoint account in the current
                  AWS Region.</p>
                tags:
                  - Get
                  - Account
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
            /v1/email/deliverability-dashboard/blacklist-report:
              GET:
                summary: GetBlacklistReports
                description: >-
                  <p>Retrieve a list of the blacklists that your dedicated IP
                  addresses appear on.</p>
                tags:
                  - Get
                  - Blacklist
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
            /v1/email/dedicated-ips/{IP}:
              GET:
                summary: GetDedicatedIp
                description: >-
                  <p>Get information about a dedicated IP address, including the
                  name of the dedicated IP pool that it's associated with, as
                  well information about the automatic warm-up process for the
                  address.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/dedicated-ips:
              GET:
                summary: GetDedicatedIps
                description: >-
                  <p>List the dedicated IP addresses that are associated with
                  your Amazon Pinpoint account.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP Addresses
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/deliverability-dashboard:
              PUT:
                summary: PutDeliverabilityDashboardOption
                description: >-
                  <p>Enable or disable the Deliverability dashboard for your
                  Amazon Pinpoint account. When you enable the Deliverability
                  dashboard, you gain access to reputation, deliverability, and
                  other metrics for the domains that you use to send email using
                  Amazon Pinpoint. You also gain the ability to perform
                  predictive inbox placement tests.</p> <p>When you use the
                  Deliverability dashboard, you pay a monthly subscription
                  charge, in addition to any other fees that you accrue by using
                  Amazon Pinpoint. For more information about the features and
                  cost of a Deliverability dashboard subscription, see <a
                  href="http://aws.amazon.com/pinpoint/pricing/">Amazon Pinpoint
                  Pricing</a>.</p>
                tags:
                  - Put
                  - Deliverability
                  - Dashboard
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/deliverability-dashboard/test-reports/{ReportId}:
              GET:
                summary: GetDeliverabilityTestReport
                description: >-
                  <p>Retrieve the results of a predictive inbox placement
                  test.</p>
                tags:
                  - Get
                  - Deliverability
                  - Tests
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
            /v1/email/deliverability-dashboard/campaigns/{CampaignId}:
              GET:
                summary: GetDomainDeliverabilityCampaign
                description: >-
                  <p>Retrieve all the deliverability data for a specific
                  campaign. This data is available for a campaign only if the
                  campaign sent email by using a domain that the Deliverability
                  dashboard is enabled for
                  (<code>PutDeliverabilityDashboardOption</code> operation).</p>
                tags:
                  - Get
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
            /v1/email/deliverability-dashboard/statistics-report/{Domain}:
              GET:
                summary: GetDomainStatisticsReport
                description: >-
                  <p>Retrieve inbox placement and engagement rates for the
                  domains that you use to send email.</p>
                tags:
                  - Get
                  - Domains
                  - Statistics
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
            /v1/email/deliverability-dashboard/test-reports:
              GET:
                summary: ListDeliverabilityTestReports
                description: >-
                  <p>Show a list of the predictive inbox placement tests that
                  you've performed, regardless of their statuses. For predictive
                  inbox placement tests that are complete, you can use the
                  <code>GetDeliverabilityTestReport</code> operation to view the
                  results.</p>
                tags:
                  - Lists
                  - Deliverability
                  - Tests
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
            /v1/email/deliverability-dashboard/domains/{SubscribedDomain}/campaigns:
              GET:
                summary: ListDomainDeliverabilityCampaigns
                description: >-
                  <p>Retrieve deliverability data for all the campaigns that
                  used a specific domain to send email during a specified time
                  range. This data is available for a domain only if you enabled
                  the Deliverability dashboard
                  (<code>PutDeliverabilityDashboardOption</code> operation) for
                  the domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
            /v1/email/tags:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Remove one or more tags (keys and values) from a specified
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
            /v1/email/account/dedicated-ips/warmup:
              PUT:
                summary: PutAccountDedicatedIpWarmupAttributes
                description: >-
                  <p>Enable or disable the automatic warm-up feature for
                  dedicated IP addresses.</p>
                tags:
                  - Put
                  - Account
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
            /v1/email/account/sending:
              PUT:
                summary: PutAccountSendingAttributes
                description: >-
                  <p>Enable or disable the ability of your account to send
                  email.</p>
                tags:
                  - Put
                  - Account
                  - Sending
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
            /v1/email/configuration-sets/{ConfigurationSetName}/delivery-options:
              PUT:
                summary: PutConfigurationSetDeliveryOptions
                description: >-
                  <p>Associate a configuration set with a dedicated IP pool. You
                  can use dedicated IP pools to create groups of dedicated IP
                  addresses for sending specific types of email.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Deliveries
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
            /v1/email/configuration-sets/{ConfigurationSetName}/reputation-options:
              PUT:
                summary: PutConfigurationSetReputationOptions
                description: >-
                  <p>Enable or disable collection of reputation metrics for
                  emails that you send using a particular configuration set in a
                  specific AWS Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Reputation
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v1/email/configuration-sets/{ConfigurationSetName}/sending:
              PUT:
                summary: PutConfigurationSetSendingOptions
                description: >-
                  <p>Enable or disable email sending for messages that use a
                  particular configuration set in a specific AWS Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Sending
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v1/email/configuration-sets/{ConfigurationSetName}/tracking-options:
              PUT:
                summary: PutConfigurationSetTrackingOptions
                description: >-
                  <p>Specify a custom domain to use for open and click tracking
                  elements in email that you send using Amazon Pinpoint.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Tracking
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/dedicated-ips/{IP}/pool:
              PUT:
                summary: PutDedicatedIpInPool
                description: >-
                  <p>Move a dedicated IP address to an existing dedicated IP
                  pool.</p> <note> <p>The dedicated IP address that you specify
                  must already exist, and must be associated with your Amazon
                  Pinpoint account. </p> <p>The dedicated IP pool you specify
                  must already exist. You can create a new pool by using the
                  <code>CreateDedicatedIpPool</code> operation.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - In
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/dedicated-ips/{IP}/warmup:
              PUT:
                summary: PutDedicatedIpWarmupAttributes
                description: <p/>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/identities/{EmailIdentity}/dkim:
              PUT:
                summary: PutEmailIdentityDkimAttributes
                description: >-
                  <p>Used to enable or disable DKIM authentication for an email
                  identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - DKIM
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
            /v1/email/identities/{EmailIdentity}/feedback:
              PUT:
                summary: PutEmailIdentityFeedbackAttributes
                description: >-
                  <p>Used to enable or disable feedback forwarding for an
                  identity. This setting determines what happens when an
                  identity is used to send an email that results in a bounce or
                  complaint event.</p> <p>When you enable feedback forwarding,
                  Amazon Pinpoint sends you email notifications when bounce or
                  complaint events occur. Amazon Pinpoint sends this
                  notification to the address that you specified in the
                  Return-Path header of the original email.</p> <p>When you
                  disable feedback forwarding, Amazon Pinpoint sends
                  notifications through other mechanisms, such as by notifying
                  an Amazon SNS topic. You're required to have a method of
                  tracking bounces and complaints. If you haven't set up another
                  mechanism for receiving bounce or complaint notifications,
                  Amazon Pinpoint sends an email notification when these events
                  occur (even if this setting is disabled).</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Feedback
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
            /v1/email/identities/{EmailIdentity}/mail-from:
              PUT:
                summary: PutEmailIdentityMailFromAttributes
                description: >-
                  <p>Used to enable or disable the custom Mail-From domain
                  configuration for an email identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Mail
                  - From
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
                  - Mail
                  - From
            /v1/email/outbound-emails:
              POST:
                summary: SendEmail
                description: >-
                  <p>Sends an email message. You can use the Amazon Pinpoint
                  Email API to send two types of messages:</p> <ul> <li> <p>
                  <b>Simple</b> – A standard email message. When you create this
                  type of message, you specify the sender, the recipient, and
                  the message body, and Amazon Pinpoint assembles the message
                  for you.</p> </li> <li> <p> <b>Raw</b> – A raw, MIME-formatted
                  email message. When you send this type of email, you have to
                  specify all of the message headers, as well as the message
                  body. You can use this message type to send messages that
                  contain attachments. The message that you specify has to be a
                  valid MIME message.</p> <
                tags:
                  - Send
                  - Email
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Email
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-email-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-email-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint-email
  - name: sesv2
    description: >-
      <fullname>Amazon SES API v2</fullname> <p> <a
      href="http://aws.amazon.com/ses">Amazon SES</a> is an Amazon Web Services
      service that you can use to send email messages to your customers.</p>
      <p>If you're new to Amazon SES API v2, you might find it helpful to review
      the <a
      href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/">Amazon
      Simple Email Service Developer Guide</a>. The <i>Amazon SES Developer
      Guide</i> provides information and code samples that demonstrate how to
      use Amazon SES API v2 features programmatically.</p>
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
            title: sesv2
          paths:
            /v2/email/metrics/batch:
              POST:
                summary: BatchGetMetricData
                description: >-
                  <p>Retrieves batches of metric data collected based on your
                  sending activity.</p> <p>You can execute this operation no
                  more than 16 times per second, and with at most 160 queries
                  from the batches per second (cumulative).</p>
                tags:
                  - Batches
                  - Get
                  - Metrics
                  - Data
                  - V2
                  - Email
                  - Metrics
                  - Batches
            /v2/email/export-jobs/{JobId}/cancel:
              PUT:
                summary: CancelExportJob
                description: <p>Cancels an export job.</p>
                tags:
                  - Cancel
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
            /v2/email/configuration-sets:
              GET:
                summary: ListConfigurationSets
                description: >-
                  <p>List all of the configuration sets associated with your
                  account in the current region.</p> <p> <i>Configuration
                  sets</i> are groups of rules that you can apply to the emails
                  you send. You apply a configuration set to an email by
                  including a reference to the configuration set in the headers
                  of the email. When you apply a configuration set to an email,
                  all of the rules in that configuration set are applied to the
                  email.</p>
                tags:
                  - Lists
                  - Configurations
                  - Sets
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
            /v2/email/configuration-sets/{ConfigurationSetName}/event-destinations:
              GET:
                summary: GetConfigurationSetEventDestinations
                description: >-
                  <p>Retrieve a list of event destinations that are associated
                  with a configuration set.</p> <p> <i>Events</i> include
                  message sends, deliveries, opens, clicks, bounces, and
                  complaints. <i>Event destinations</i> are places that you can
                  send information about these events to. For example, you can
                  send event data to Amazon SNS to receive notifications when
                  you receive bounces or complaints, or you can use Amazon
                  Kinesis Data Firehose to stream data to Amazon S3 for
                  long-term storage.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
            /v2/email/contact-lists/{ContactListName}/contacts:
              GET:
                summary: ListContacts
                description: <p>Lists the contacts present in a specific contact list.</p>
                tags:
                  - Lists
                  - Contacts
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
            /v2/email/contact-lists:
              GET:
                summary: ListContactLists
                description: <p>Lists all of the contact lists available.</p>
                tags:
                  - Lists
                  - Contacts
                  - Lists
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
            /v2/email/custom-verification-email-templates:
              GET:
                summary: ListCustomVerificationEmailTemplates
                description: >-
                  <p>Lists the existing custom verification email templates for
                  your account in the current Amazon Web Services Region.</p>
                  <p>For more information about custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Lists
                  - Custom
                  - Verification
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
            /v2/email/dedicated-ip-pools:
              GET:
                summary: ListDedicatedIpPools
                description: >-
                  <p>List all of the dedicated IP pools that exist in your
                  Amazon Web Services account in the current Region.</p>
                tags:
                  - Lists
                  - Dedicated
                  - IP
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
            /v2/email/deliverability-dashboard/test:
              POST:
                summary: CreateDeliverabilityTestReport
                description: >-
                  <p>Create a new predictive inbox placement test. Predictive
                  inbox placement tests can help you predict how your messages
                  will be handled by various email providers around the world.
                  When you perform a predictive inbox placement test, you
                  provide a sample message that contains the content that you
                  plan to send to your customers. Amazon SES then sends that
                  message to special email addresses spread across several major
                  email providers. After about 24 hours, the test is complete,
                  and you can use the <code>GetDeliverabilityTestReport</code>
                  operation to view the results of the test.</p>
                tags:
                  - Create
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
            /v2/email/identities:
              GET:
                summary: ListEmailIdentities
                description: >-
                  <p>Returns a list of all of the email identities that are
                  associated with your Amazon Web Services account. An identity
                  can be either an email address or a domain. This operation
                  returns identities that are verified as well as those that
                  aren't. This operation returns identities that are associated
                  with Amazon SES and Amazon Pinpoint.</p>
                tags:
                  - Lists
                  - Email
                  - Identities
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v2/email/identities/{EmailIdentity}/policies/{PolicyName}:
              PUT:
                summary: UpdateEmailIdentityPolicy
                description: >-
                  <p>Updates the specified sending authorization policy for the
                  given identity (an email address or a domain). This API
                  returns successfully even if a policy with the specified name
                  does not exist.</p> <note> <p>This API is for the identity
                  owner only. If you have not verified the identity, this API
                  will return an error.</p> </note> <p>Sending authorization is
                  a feature that enables an identity owner to authorize other
                  senders to use its identities. For information about using
                  sending authorization, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/sending-authorization.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Update
                  - Email
                  - Identity
                  - Policies
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
            /v2/email/templates:
              GET:
                summary: ListEmailTemplates
                description: >-
                  <p>Lists the email templates present in your Amazon SES
                  account in the current Amazon Web Services Region.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Lists
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
            /v2/email/export-jobs:
              POST:
                summary: CreateExportJob
                description: >-
                  <p>Creates an export job for a data source and
                  destination.</p> <p>You can execute this operation no more
                  than once per second.</p>
                tags:
                  - Create
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
            /v2/email/import-jobs:
              GET:
                summary: ListImportJobs
                description: <p>Lists all of the import jobs.</p>
                tags:
                  - Lists
                  - Import
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
            /v2/email/configuration-sets/{ConfigurationSetName}:
              GET:
                summary: GetConfigurationSet
                description: >-
                  <p>Get information about an existing configuration set,
                  including the dedicated IP pool that it's associated with,
                  whether or not it's enabled for sending email, and more.</p>
                  <p> <i>Configuration sets</i> are groups of rules that you can
                  apply to the emails you send. You apply a configuration set to
                  an email by including a reference to the configuration set in
                  the headers of the email. When you apply a configuration set
                  to an email, all of the rules in that configuration set are
                  applied to the email.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
            /v2/email/configuration-sets/{ConfigurationSetName}/event-destinations/{EventDestinationName}:
              PUT:
                summary: UpdateConfigurationSetEventDestination
                description: >-
                  <p>Update the configuration of an event destination for a
                  configuration set.</p> <p> <i>Events</i> include message
                  sends, deliveries, opens, clicks, bounces, and complaints.
                  <i>Event destinations</i> are places that you can send
                  information about these events to. For example, you can send
                  event data to Amazon SNS to receive notifications when you
                  receive bounces or complaints, or you can use Amazon Kinesis
                  Data Firehose to stream data to Amazon S3 for long-term
                  storage.</p>
                tags:
                  - Update
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
            /v2/email/contact-lists/{ContactListName}/contacts/{EmailAddress}:
              PUT:
                summary: UpdateContact
                description: >-
                  <p>Updates a contact's preferences for a list. It is not
                  necessary to specify all existing topic preferences in the
                  TopicPreferences object, just the ones that need updating.</p>
                tags:
                  - Update
                  - Contacts
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
            /v2/email/contact-lists/{ContactListName}:
              PUT:
                summary: UpdateContactList
                description: >-
                  <p>Updates contact list metadata. This operation does a
                  complete replacement.</p>
                tags:
                  - Update
                  - Contacts
                  - Lists
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
            /v2/email/custom-verification-email-templates/{TemplateName}:
              PUT:
                summary: UpdateCustomVerificationEmailTemplate
                description: >-
                  <p>Updates an existing custom verification email template.</p>
                  <p>For more information about custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Update
                  - Custom
                  - Verification
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
            /v2/email/dedicated-ip-pools/{PoolName}:
              GET:
                summary: GetDedicatedIpPool
                description: <p>Retrieve information about the dedicated pool.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/identities/{EmailIdentity}:
              GET:
                summary: GetEmailIdentity
                description: >-
                  <p>Provides information about a specific identity, including
                  the identity's verification status, sending authorization
                  policies, its DKIM authentication status, and its custom
                  Mail-From settings.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/templates/{TemplateName}:
              PUT:
                summary: UpdateEmailTemplate
                description: >-
                  <p>Updates an email template. Email templates enable you to
                  send personalized email to one or more destinations in a
                  single API operation. For more information, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-api.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Update
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/suppression/addresses/{EmailAddress}:
              GET:
                summary: GetSuppressedDestination
                description: >-
                  <p>Retrieves information about a specific email address that's
                  on the suppression list for your account.</p>
                tags:
                  - Get
                  - Suppressed
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/account:
              GET:
                summary: GetAccount
                description: >-
                  <p>Obtain information about the email-sending status and
                  capabilities of your Amazon SES account in the current Amazon
                  Web Services Region.</p>
                tags:
                  - Get
                  - Account
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
            /v2/email/deliverability-dashboard/blacklist-report:
              GET:
                summary: GetBlacklistReports
                description: >-
                  <p>Retrieve a list of the blacklists that your dedicated IP
                  addresses appear on.</p>
                tags:
                  - Get
                  - Blacklist
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
            /v2/email/dedicated-ips/{IP}:
              GET:
                summary: GetDedicatedIp
                description: >-
                  <p>Get information about a dedicated IP address, including the
                  name of the dedicated IP pool that it's associated with, as
                  well information about the automatic warm-up process for the
                  address.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/dedicated-ips:
              GET:
                summary: GetDedicatedIps
                description: >-
                  <p>List the dedicated IP addresses that are associated with
                  your Amazon Web Services account.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP Addresses
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard:
              PUT:
                summary: PutDeliverabilityDashboardOption
                description: >-
                  <p>Enable or disable the Deliverability dashboard. When you
                  enable the Deliverability dashboard, you gain access to
                  reputation, deliverability, and other metrics for the domains
                  that you use to send email. You also gain the ability to
                  perform predictive inbox placement tests.</p> <p>When you use
                  the Deliverability dashboard, you pay a monthly subscription
                  charge, in addition to any other fees that you accrue by using
                  Amazon SES and other Amazon Web Services services. For more
                  information about the features and cost of a Deliverability
                  dashboard subscription, see <a
                  href="http://aws.amazon.com/ses/pricing/">Amazon SES
                  Pricing</a>.</p>
                tags:
                  - Put
                  - Deliverability
                  - Dashboard
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard/test-reports/{ReportId}:
              GET:
                summary: GetDeliverabilityTestReport
                description: >-
                  <p>Retrieve the results of a predictive inbox placement
                  test.</p>
                tags:
                  - Get
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard/campaigns/{CampaignId}:
              GET:
                summary: GetDomainDeliverabilityCampaign
                description: >-
                  <p>Retrieve all the deliverability data for a specific
                  campaign. This data is available for a campaign only if the
                  campaign sent email by using a domain that the Deliverability
                  dashboard is enabled for.</p>
                tags:
                  - Get
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
            /v2/email/deliverability-dashboard/statistics-report/{Domain}:
              GET:
                summary: GetDomainStatisticsReport
                description: >-
                  <p>Retrieve inbox placement and engagement rates for the
                  domains that you use to send email.</p>
                tags:
                  - Get
                  - Domains
                  - Statistics
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/identities/{EmailIdentity}/policies:
              GET:
                summary: GetEmailIdentityPolicies
                description: >-
                  <p>Returns the requested sending authorization policies for
                  the given identity (an email address or a domain). The
                  policies are returned as a map of policy names to policy
                  contents. You can retrieve a maximum of 20 policies at a
                  time.</p> <note> <p>This API is for the identity owner only.
                  If you have not verified the identity, this API will return an
                  error.</p> </note> <p>Sending authorization is a feature that
                  enables an identity owner to authorize other senders to use
                  its identities. For information about using sending
                  authorization, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/sending-authorization.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - Policies
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/export-jobs/{JobId}:
              GET:
                summary: GetExportJob
                description: <p>Provides information about an export job.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/import-jobs/{JobId}:
              GET:
                summary: GetImportJob
                description: <p>Provides information about an import job.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/insights/{MessageId}/:
              GET:
                summary: GetMessageInsights
                description: >-
                  <p>Provides information about a specific message, including
                  the from address, the subject, the recipient address, email
                  tags, as well as events associated with the message.</p>
                  <p>You can execute this operation no more than once per
                  second.</p>
                tags:
                  - Get
                  - Messages
                  - Insights
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
            /v2/email/deliverability-dashboard/test-reports:
              GET:
                summary: ListDeliverabilityTestReports
                description: >-
                  <p>Show a list of the predictive inbox placement tests that
                  you've performed, regardless of their statuses. For predictive
                  inbox placement tests that are complete, you can use the
                  <code>GetDeliverabilityTestReport</code> operation to view the
                  results.</p>
                tags:
                  - Lists
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
            /v2/email/deliverability-dashboard/domains/{SubscribedDomain}/campaigns:
              GET:
                summary: ListDomainDeliverabilityCampaigns
                description: >-
                  <p>Retrieve deliverability data for all the campaigns that
                  used a specific domain to send email during a specified time
                  range. This data is available for a domain only if you enabled
                  the Deliverability dashboard for the domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
            /v2/email/list-export-jobs:
              POST:
                summary: ListExportJobs
                description: <p>Lists all of the export jobs.</p>
                tags:
                  - Lists
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
            /v2/email/vdm/recommendations:
              POST:
                summary: ListRecommendations
                description: >-
                  <p>Lists the recommendations present in your Amazon SES
                  account in the current Amazon Web Services Region.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Lists
                  - Recommendations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
            /v2/email/suppression/addresses:
              PUT:
                summary: PutSuppressedDestination
                description: >-
                  <p>Adds an email address to the suppression list for your
                  account.</p>
                tags:
                  - Put
                  - Suppressed
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
            /v2/email/tags:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Remove one or more tags (keys and values) from a specified
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
            /v2/email/account/dedicated-ips/warmup:
              PUT:
                summary: PutAccountDedicatedIpWarmupAttributes
                description: >-
                  <p>Enable or disable the automatic warm-up feature for
                  dedicated IP addresses.</p>
                tags:
                  - Put
                  - Account
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
            /v2/email/account/details:
              POST:
                summary: PutAccountDetails
                description: <p>Update your Amazon SES account details.</p>
                tags:
                  - Put
                  - Account
                  - Details
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
            /v2/email/account/sending:
              PUT:
                summary: PutAccountSendingAttributes
                description: >-
                  <p>Enable or disable the ability of your account to send
                  email.</p>
                tags:
                  - Put
                  - Account
                  - Sending
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/account/suppression:
              PUT:
                summary: PutAccountSuppressionAttributes
                description: >-
                  <p>Change the settings for the account-level suppression
                  list.</p>
                tags:
                  - Put
                  - Account
                  - Suppressions
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/account/vdm:
              PUT:
                summary: PutAccountVdmAttributes
                description: >-
                  <p>Update your Amazon SES account VDM attributes.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Put
                  - Account
                  - Vdm
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/configuration-sets/{ConfigurationSetName}/delivery-options:
              PUT:
                summary: PutConfigurationSetDeliveryOptions
                description: >-
                  <p>Associate a configuration set with a dedicated IP pool. You
                  can use dedicated IP pools to create groups of dedicated IP
                  addresses for sending specific types of email.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Deliveries
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
            /v2/email/configuration-sets/{ConfigurationSetName}/reputation-options:
              PUT:
                summary: PutConfigurationSetReputationOptions
                description: >-
                  <p>Enable or disable collection of reputation metrics for
                  emails that you send using a particular configuration set in a
                  specific Amazon Web Services Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Reputation
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/sending:
              PUT:
                summary: PutConfigurationSetSendingOptions
                description: >-
                  <p>Enable or disable email sending for messages that use a
                  particular configuration set in a specific Amazon Web Services
                  Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Sending
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/suppression-options:
              PUT:
                summary: PutConfigurationSetSuppressionOptions
                description: >-
                  <p>Specify the account suppression list preferences for a
                  configuration set.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Suppressions
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/tracking-options:
              PUT:
                summary: PutConfigurationSetTrackingOptions
                description: >-
                  <p>Specify a custom domain to use for open and click tracking
                  elements in email that you send.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Tracking
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/configuration-sets/{ConfigurationSetName}/vdm-options:
              PUT:
                summary: PutConfigurationSetVdmOptions
                description: >-
                  <p>Specify VDM preferences for email that you send using the
                  configuration set.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Vdm
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/dedicated-ips/{IP}/pool:
              PUT:
                summary: PutDedicatedIpInPool
                description: >-
                  <p>Move a dedicated IP address to an existing dedicated IP
                  pool.</p> <note> <p>The dedicated IP address that you specify
                  must already exist, and must be associated with your Amazon
                  Web Services account. </p> <p>The dedicated IP pool you
                  specify must already exist. You can create a new pool by using
                  the <code>CreateDedicatedIpPool</code> operation.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - In
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/dedicated-ip-pools/{PoolName}/scaling:
              PUT:
                summary: PutDedicatedIpPoolScalingAttributes
                description: >-
                  <p>Used to convert a dedicated IP pool to a different scaling
                  mode.</p> <note> <p> <code>MANAGED</code> pools cannot be
                  converted to <code>STANDARD</code> scaling mode.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Pools
                  - Scaling
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/dedicated-ips/{IP}/warmup:
              PUT:
                summary: PutDedicatedIpWarmupAttributes
                description: <p/>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/identities/{EmailIdentity}/configuration-set:
              PUT:
                summary: PutEmailIdentityConfigurationSetAttributes
                description: >-
                  <p>Used to associate a configuration set with an email
                  identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Configurations
                  - Sets
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/identities/{EmailIdentity}/dkim:
              PUT:
                summary: PutEmailIdentityDkimAttributes
                description: >-
                  <p>Used to enable or disable DKIM authentication for an email
                  identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - DKIM
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
            /v1/email/identities/{EmailIdentity}/dkim/signing:
              PUT:
                summary: PutEmailIdentityDkimSigningAttributes
                description: >-
                  <p>Used to configure or change the DKIM authentication
                  settings for an email domain identity. You can use this
                  operation to do any of the following:</p> <ul> <li> <p>Update
                  the signing attributes for an identity that uses Bring Your
                  Own DKIM (BYODKIM).</p> </li> <li> <p>Update the key length
                  that should be used for Easy DKIM.</p> </li> <li> <p>Change
                  from using no DKIM authentication to using Easy DKIM.</p>
                  </li> <li> <p>Change from using no DKIM authentication to
                  using BYODKIM.</p> </li> <li> <p>Change from using Easy DKIM
                  to using BYODKIM.</p> </li> <li> <p>Change from using BYODKIM
                  to using Easy DKIM.</p> </li> </ul>
                tags:
                  - Put
                  - Email
                  - Identity
                  - DKIM
                  - Signing
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
            /v2/email/identities/{EmailIdentity}/feedback:
              PUT:
                summary: PutEmailIdentityFeedbackAttributes
                description: >-
                  <p>Used to enable or disable feedback forwarding for an
                  identity. This setting determines what happens when an
                  identity is used to send an email that results in a bounce or
                  complaint event.</p> <p>If the value is <code>true</code>, you
                  receive email notifications when bounce or complaint events
                  occur. These notifications are sent to the address that you
                  specified in the <code>Return-Path</code> header of the
                  original email.</p> <p>You're required to have a method of
                  tracking bounces and complaints. If you haven't set up another
                  mechanism for receiving bounce or complaint notifications (for
                  example, by setting up an event destination), you receive an
                  email notification when these events occur (even if this
                  setting is disabled).</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Feedback
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
            /v2/email/identities/{EmailIdentity}/mail-from:
              PUT:
                summary: PutEmailIdentityMailFromAttributes
                description: >-
                  <p>Used to enable or disable the custom Mail-From domain
                  configuration for an email identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Mail
                  - From
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
            /v2/email/outbound-bulk-emails:
              POST:
                summary: SendBulkEmail
                description: <p>Composes an email message to multiple destinations.</p>
                tags:
                  - Send
                  - Bulk
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/outbound-custom-verification-emails:
              POST:
                summary: SendCustomVerificationEmail
                description: >-
                  <p>Adds an email address to the list of identities for your
                  Amazon SES account in the current Amazon Web Services Region
                  and attempts to verify it. As a result of executing this
                  operation, a customized verification email is sent to the
                  specified address.</p> <p>To use this operation, you must
                  first create a custom verification email template. For more
                  information about creating and using custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Send
                  - Custom
                  - Verification
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/outbound-emails:
              POST:
                summary: SendEmail
                description: >-
                  <p>Sends an email message. You can use the Amazon SES API v2
                  to send the following types of messages:</p> <ul> <li> <p>
                  <b>Simple</b> – A standard email message. When you create this
                  type of message, you specify the sender, the recipient, and
                  the message body, and Amazon SES assembles the message for
                  you.</p> </li> <li> <p> <b>Raw</b> – A raw, MIME-formatted
                  email message. When you send this type of email, you have to
                  specify all of the message headers, as well as the message
                  body. You can use this message type to send messages that
                  contain attachments. The message that you specify has to be a
                  valid MIME message.</p> </li> <li> <p> <b>Templated</b> – A
                  message that contains personalization tags. When you send this
                  type of email, Amazon SES API v2 automatically replaces the
                  tags with values that you specify.</p> </li> </ul>
                tags:
                  - Send
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/templates/{TemplateName}/render:
              POST:
                summary: TestRenderEmailTemplate
                description: >-
                  <p>Creates a preview of the MIME content of an email when
                  provided with a template and a set of replacement data.</p>
                  <p>You can execute this operation no more than once per s
                tags:
                  - Tests
                  - Render
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
                  - Rend
    overlays:
      - type: APIs.io Search
        url: overlays/sesv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sesv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sesv2
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---