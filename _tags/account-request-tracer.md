---
name: Account Request Tracer
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/account-request-tracer.png
url: https://example.com/apis/account-request-tracer.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Account Request Tracer
apis:
  - name: Cloudflare API
    description: >-
      Interact with Cloudflare's products and services via the Cloudflare API.
      Using the Cloudflare API requires authentication so that Cloudflare knows
      who is making requests and what permissions you have. Create an API token
      to grant access to the API to perform actions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.cloudflare.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.cloudflare.com/api/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Cloudflare API
            license:
              name: BSD-3-Clause
              url: https://opensource.org/licenses/BSD-3-Clause
          paths:
            /accounts:
              get:
                tags:
                  - Accounts
                summary: List Accounts
                description: List all accounts you have ownership or verified access to.
            /accounts/{account_id}:
              get:
                tags:
                  - Accounts
                summary: Account Details
                description: >-
                  Get information about a specific account that you are a member
                  of.
              put:
                tags:
                  - Accounts
                summary: Update Account
                description: Update an existing account.
            /accounts/{account_id}/addressing/address_maps:
              get:
                tags:
                  - IP Address Management Address Maps
                summary: List Address Maps
                description: List all address maps owned by the account.
              post:
                tags:
                  - IP Address Management Address Maps
                summary: Create Address Map
                description: Create a new address map under the account.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Delete Address Map
                description: >-
                  Delete a particular address map owned by the account. An
                  Address Map must be disabled before it can be deleted.
              get:
                tags:
                  - IP Address Management Address Maps
                summary: Address Map Details
                description: Show a particular address map owned by the account.
              patch:
                tags:
                  - IP Address Management Address Maps
                summary: Update Address Map
                description: Modify properties of an address map owned by the account.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/accounts/{account_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove an account membership from an Address Map
                description: Remove an account as a member of a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add an account membership to an Address Map
                description: Add an account as a member of a particular address map.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/ips/{ip_address}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove an IP from an Address Map
                description: Remove an IP from a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add an IP to an Address Map
                description: >-
                  Add an IP from a prefix owned by the account to a particular
                  address map.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/zones/{zone_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove a zone membership from an Address Map
                description: Remove a zone as a member of a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add a zone membership to an Address Map
                description: Add a zone as a member of a particular address map.
            /accounts/{account_id}/addressing/loa_documents:
              post:
                tags:
                  - IP Address Management Prefixes
                summary: Upload LOA Document
                description: Submit LOA document (pdf format) under the account.
            /accounts/{account_id}/addressing/loa_documents/{loa_document_id}/download:
              get:
                tags:
                  - IP Address Management Prefixes
                summary: Download LOA Document
                description: Download specified LOA document under the account.
            /accounts/{account_id}/addressing/prefixes:
              get:
                tags:
                  - IP Address Management Prefixes
                summary: List Prefixes
                description: List all prefixes owned by the account.
              post:
                tags:
                  - IP Address Management Prefixes
                summary: Add Prefix
                description: Add a new prefix under the account.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}:
              delete:
                tags:
                  - IP Address Management Prefixes
                summary: Delete Prefix
                description: Delete an unapproved prefix owned by the account.
              get:
                tags:
                  - IP Address Management Prefixes
                summary: Prefix Details
                description: List a particular prefix owned by the account.
              patch:
                tags:
                  - IP Address Management Prefixes
                summary: Update Prefix Description
                description: Modify the description for a prefix owned by the account.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/prefixes:
              get:
                tags:
                  - IP Address Management BGP Prefixes
                summary: List BGP Prefixes
                description: >-
                  List all BGP Prefixes within the specified IP Prefix. BGP
                  Prefixes are used to control which specific subnets are
                  advertised to the Internet. It is possible to advertise
                  subnets more specific than an IP Prefix by creating more
                  specific BGP Prefixes.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/prefixes/{bgp_prefix_id}:
              get:
                tags:
                  - IP Address Management BGP Prefixes
                summary: Fetch BGP Prefix
                description: Retrieve a single BGP Prefix according to its identifier
              patch:
                tags:
                  - IP Address Management BGP Prefixes
                summary: Update BGP Prefix
                description: >-
                  Update the properties of a BGP Prefix, such as the on demand
                  advertisement status (advertised or withdrawn).
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/status:
              get:
                tags:
                  - IP Address Management Dynamic Advertisement
                summary: Get Advertisement Status
                description: List the current advertisement state for a prefix.
              patch:
                tags:
                  - IP Address Management Dynamic Advertisement
                summary: Update Prefix Dynamic Advertisement Status
                description: Advertise or withdraw BGP route for a prefix.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bindings:
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: List Service Bindings
                description: >
                  List the Cloudflare services this prefix is currently bound
                  to. Traffic sent to an address within an IP prefix will be
                  routed to the Cloudflare service of the most-specific Service
                  Binding matching the address.

                  **Example:** binding `192.0.2.0/24` to Cloudflare Magic
                  Transit and `192.0.2.1/32` to the Cloudflare CDN would route
                  traffic for `192.0.2.1` to the CDN, and traffic for all other
                  IPs in the prefix to Cloudflare Magic Transit.
              post:
                tags:
                  - IP Address Management Service Bindings
                summary: Create Service Binding
                description: >
                  Creates a new Service Binding, routing traffic to IPs within
                  the given CIDR to a service running on Cloudflare's network.

                  **Note:** This API may only be used on prefixes currently
                  configured with a Magic Transit service binding, and only
                  allows creating service bindings for the Cloudflare CDN or
                  Cloudflare Spectrum.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bindings/{binding_id}:
              delete:
                tags:
                  - IP Address Management Service Bindings
                summary: Delete Service Binding
                description: Delete a Service Binding
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: Get Service Binding
                description: Fetch a single Service Binding
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/delegations:
              get:
                tags:
                  - IP Address Management Prefix Delegation
                summary: List Prefix Delegations
                description: List all delegations for a given account IP prefix.
              post:
                tags:
                  - IP Address Management Prefix Delegation
                summary: Create Prefix Delegation
                description: Create a new account delegation for a given IP prefix.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/delegations/{delegation_id}:
              delete:
                tags:
                  - IP Address Management Prefix Delegation
                summary: Delete Prefix Delegation
                description: Delete an account delegation for a given IP prefix.
            /accounts/{account_id}/addressing/services:
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: List Services
                description: >
                  Bring-Your-Own IP (BYOIP) prefixes onboarded to Cloudflare
                  must be bound to a service running on the Cloudflare network
                  to enable a Cloudflare product on the IP addresses. This
                  endpoint can be used as a reference of available services on
                  the Cloudflare network, and their service IDs.
            /accounts/{account_id}/ai/run/@cf/baai/bge-base-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-base-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/baai/bge-large-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-large-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/baai/bge-small-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-small-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/bytedance/stable-diffusion-xl-lightning:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/bytedance/stable-diffusion-xl-lightning model.
            /accounts/{account_id}/ai/run/@cf/deepseek-ai/deepseek-math-7b-base:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/deepseek-ai/deepseek-math-7b-base model.
            /accounts/{account_id}/ai/run/@cf/deepseek-ai/deepseek-math-7b-instruct:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/deepseek-ai/deepseek-math-7b-instruct model.
            /accounts/{account_id}/ai/run/@cf/defog/sqlcoder-7b-2:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/defog/sqlcoder-7b-2 model.
            /accounts/{account_id}/ai/run/@cf/facebook/bart-large-cnn:
              post:
                tags:
                  - Workers AI Summarization
                summary: Execute @cf/facebook/bart-large-cnn model.
            /accounts/{account_id}/ai/run/@cf/facebook/detr-resnet-50:
              post:
                tags:
                  - Workers AI Object Detection
                summary: Execute @cf/facebook/detr-resnet-50 model.
            /accounts/{account_id}/ai/run/@cf/huggingface/distilbert-sst-2-int8:
              post:
                tags:
                  - Workers AI Text Classification
                summary: Execute @cf/huggingface/distilbert-sst-2-int8 model.
            /accounts/{account_id}/ai/run/@cf/jpmorganchase/roberta-spam:
              post:
                tags:
                  - Workers AI Text Classification
                summary: Execute @cf/jpmorganchase/roberta-spam model.
            /accounts/{account_id}/ai/run/@cf/lykon/dreamshaper-8-lcm:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/lykon/dreamshaper-8-lcm model.
            /accounts/{account_id}/ai/run/@cf/meta/llama-2-7b-chat-fp16:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/meta/llama-2-7b-chat-fp16 model.
            /accounts/{account_id}/ai/run/@cf/meta/llama-2-7b-chat-int8:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/meta/llama-2-7b-chat-int8 model.
            /accounts/{account_id}/ai/run/@cf/meta/m2m100-1.2b:
              post:
                tags:
                  - Workers AI Translation
                summary: Execute @cf/meta/m2m100-1.2b model.
            /accounts/{account_id}/ai/run/@cf/microsoft/phi-2:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/microsoft/phi-2 model.
            /accounts/{account_id}/ai/run/@cf/microsoft/resnet-50:
              post:
                tags:
                  - Workers AI Image Classification
                summary: Execute @cf/microsoft/resnet-50 model.
            /accounts/{account_id}/ai/run/@cf/mistral/mistral-7b-instruct-v0.1:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/mistral/mistral-7b-instruct-v0.1 model.
            /accounts/{account_id}/ai/run/@cf/openai/whisper:
              post:
                tags:
                  - Workers AI Speech Recognition
                summary: Execute @cf/openai/whisper model.
            /accounts/{account_id}/ai/run/@cf/openchat/openchat-3.5-0106:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/openchat/openchat-3.5-0106 model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-0.5b-chat:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-0.5b-chat model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-1.8b-chat:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-1.8b-chat model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-7b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-7b-chat-awq model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-14b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-14b-chat-awq model.
            /accounts/{account_id}/ai/run/@cf/runwayml/stable-diffusion-v1-5-img2img:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/runwayml/stable-diffusion-v1-5-img2img model.
            /accounts/{account_id}/ai/run/@cf/runwayml/stable-diffusion-v1-5-inpainting:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/runwayml/stable-diffusion-v1-5-inpainting model.
            /accounts/{account_id}/ai/run/@cf/stabilityai/stable-diffusion-xl-base-1.0:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/stabilityai/stable-diffusion-xl-base-1.0 model.
            /accounts/{account_id}/ai/run/@cf/thebloke/discolm-german-7b-v1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/thebloke/discolm-german-7b-v1-awq model.
            /accounts/{account_id}/ai/run/@cf/thebloke/yarn-mistral-7b-64k-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/thebloke/yarn-mistral-7b-64k-awq model.
            /accounts/{account_id}/ai/run/@cf/tiiuae/falcon-7b-instruct:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/tiiuae/falcon-7b-instruct model.
            /accounts/{account_id}/ai/run/@cf/tinyllama/tinyllama-1.1b-chat-v1.0:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/tinyllama/tinyllama-1.1b-chat-v1.0 model.
            /accounts/{account_id}/ai/run/@hf/baai/bge-base-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @hf/baai/bge-base-en-v1.5 model.
            /accounts/{account_id}/ai/run/@hf/sentence-transformers/all-minilm-l6-v2:
              post:
                tags:
                  - Workers AI Sentence Similarity
                summary: Execute @hf/sentence-transformers/all-minilm-l6-v2 model.
            /accounts/{account_id}/ai/run/@hf/thebloke/codellama-7b-instruct-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/codellama-7b-instruct-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/deepseek-coder-6.7b-base-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/deepseek-coder-6.7b-base-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/deepseek-coder-6.7b-instruct-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/deepseek-coder-6.7b-instruct-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/llama-2-13b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/llama-2-13b-chat-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/llamaguard-7b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/llamaguard-7b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/mistral-7b-instruct-v0.1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/mistral-7b-instruct-v0.1-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/neural-chat-7b-v3-1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/neural-chat-7b-v3-1-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/openchat_3.5-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/openchat_3.5-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/openhermes-2.5-mistral-7b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/openhermes-2.5-mistral-7b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/orca-2-13b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/orca-2-13b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/starling-lm-7b-alpha-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/starling-lm-7b-alpha-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/zephyr-7b-beta-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/zephyr-7b-beta-awq model.
            /accounts/{account_id}/ai/run/{model_name}:
              post:
                tags:
                  - Workers AI
                summary: Execute AI model
                description: >-
                  This endpoint provides users with the capability to run
                  specific AI models on-demand.


                  By submitting the required input data, users can receive
                  real-time predictions or results generated by the chosen AI

                  model. The endpoint supports various AI model types, ensuring
                  flexibility and adaptability for diverse use cases.


                  Model specific inputs available in [Cloudflare
                  Docs](https://developers.cloudflare.com/workers-ai/models/).
            /accounts/{account_id}/alerting/v3/available_alerts:
              get:
                tags:
                  - Notification Alert Types
                summary: Get Alert Types
                description: >-
                  Gets a list of all alert types for which an account is
                  eligible.
            /accounts/{account_id}/alerting/v3/destinations/eligible:
              get:
                tags:
                  - Notification Mechanism Eligibility
                summary: Get delivery mechanism eligibility
                description: >-
                  Get a list of all delivery mechanism types for which an
                  account is eligible.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty:
              delete:
                tags:
                  - Notification destinations with PagerDuty
                summary: Delete PagerDuty Services
                description: Deletes all the PagerDuty Services connected to the account.
              get:
                tags:
                  - Notification destinations with PagerDuty
                summary: List PagerDuty services
                description: Get a list of all configured PagerDuty services.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty/connect:
              post:
                tags:
                  - Notification destinations with PagerDuty
                summary: Create PagerDuty integration token
                description: Creates a new token for integrating with PagerDuty.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty/connect/{token_id}:
              get:
                tags:
                  - Notification destinations with PagerDuty
                summary: Connect PagerDuty
                description: Links PagerDuty with the account using the integration token.
            /accounts/{account_id}/alerting/v3/destinations/webhooks:
              get:
                tags:
                  - Notification webhooks
                summary: List webhooks
                description: Gets a list of all configured webhook destinations.
              post:
                tags:
                  - Notification webhooks
                summary: Create a webhook
                description: Creates a new webhook destination.
            /accounts/{account_id}/alerting/v3/destinations/webhooks/{webhook_id}:
              delete:
                tags:
                  - Notification webhooks
                summary: Delete a webhook
                description: Delete a configured webhook destination.
              get:
                tags:
                  - Notification webhooks
                summary: Get a webhook
                description: Get details for a single webhooks destination.
              put:
                tags:
                  - Notification webhooks
                summary: Update a webhook
                description: Update a webhook destination.
            /accounts/{account_id}/alerting/v3/history:
              get:
                tags:
                  - Notification History
                summary: List History
                description: >-
                  Gets a list of history records for notifications sent to an
                  account. The records are displayed for last `x` number of days
                  based on the zone plan (free = 30, pro = 30, biz = 30, ent =
                  90).
            /accounts/{account_id}/alerting/v3/policies:
              get:
                tags:
                  - Notification policies
                summary: List Notification policies
                description: Get a list of all Notification policies.
              post:
                tags:
                  - Notification policies
                summary: Create a Notification policy
                description: Creates a new Notification policy.
            /accounts/{account_id}/alerting/v3/policies/{policy_id}:
              delete:
                tags:
                  - Notification policies
                summary: Delete a Notification policy
                description: Delete a Notification policy.
              get:
                tags:
                  - Notification policies
                summary: Get a Notification policy
                description: Get details for a single policy.
              put:
                tags:
                  - Notification policies
                summary: Update a Notification policy
                description: Update a Notification policy.
            /accounts/{account_id}/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get account audit logs
                description: >-
                  Gets a list of audit logs for an account. Can be filtered by
                  who made the change, on which zone, and the timeframe of the
                  change.
            /accounts/{account_id}/brand-protection/submit:
              post:
                tags:
                  - Phishing URL Scanner
                summary: Submit suspicious URL for scanning
            /accounts/{account_id}/brand-protection/url-info:
              get:
                tags:
                  - Phishing URL Information
                summary: Get results for a URL scan
            /accounts/{account_id}/calls/apps:
              get:
                tags:
                  - Calls Apps
                summary: List apps
                description: Lists all apps in the Cloudflare account
              post:
                tags:
                  - Calls Apps
                summary: Create a new app
                description: >-
                  Creates a new Cloudflare calls app. An app is an unique
                  enviroment where each Session can access all Tracks within the
                  app.
            /accounts/{account_id}/calls/apps/{app_id}:
              delete:
                tags:
                  - Calls Apps
                summary: Delete app
                description: Deletes an app from Cloudflare Calls
              get:
                tags:
                  - Calls Apps
                summary: Retrieve app details
                description: Fetches details for a single Calls app.
              put:
                tags:
                  - Calls Apps
                summary: Edit app details
                description: Edit details for a single app.
            /accounts/{account_id}/cfd_tunnel:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Cloudflare Tunnels
                description: Lists and filters Cloudflare Tunnels in an account.
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Create a Cloudflare Tunnel
                description: Creates a new Cloudflare Tunnel in an account.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Delete a Cloudflare Tunnel
                description: Deletes a Cloudflare Tunnel from an account.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel
                description: Fetches a single Cloudflare Tunnel.
              patch:
                tags:
                  - Cloudflare Tunnel
                summary: Update a Cloudflare Tunnel
                description: Updates an existing Cloudflare Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/configurations:
              get:
                tags:
                  - Cloudflare Tunnel configuration
                summary: Get configuration
                description: Gets the configuration for a remotely-managed tunnel
              put:
                tags:
                  - Cloudflare Tunnel configuration
                summary: Put configuration
                description: >-
                  Adds or updates the configuration for a remotely-managed
                  tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/connections:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Clean up Cloudflare Tunnel connections
                description: >-
                  Removes a connection (aka Cloudflare Tunnel Connector) from a
                  Cloudflare Tunnel independently of its current state. If no
                  connector id (client_id) is provided all connectors will be
                  removed. We recommend running this command after rotating
                  tokens.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Cloudflare Tunnel connections
                description: Fetches connection details for a Cloudflare Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/connectors/{connector_id}:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get Cloudflare Tunnel connector
                description: >-
                  Fetches connector and connection details for a Cloudflare
                  Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/management:
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel management token
                description: >-
                  Gets a management token used to access the management
                  resources (i.e. Streaming Logs) of a tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/token:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel token
                description: >-
                  Gets the token used to associate cloudflared with a specific
                  tunnel.
            /accounts/{account_id}/challenges/widgets:
              get:
                tags:
                  - Turnstile
                summary: List Turnstile Widgets
                description: Lists all turnstile widgets of an account.
              post:
                tags:
                  - Turnstile
                summary: Create a Turnstile Widget
                description: Lists challenge widgets.
              parameters:
                - null
                - null
                - null
                - null
                - null
            /accounts/{account_id}/challenges/widgets/{sitekey}:
              delete:
                tags:
                  - Turnstile
                summary: Delete a Turnstile Widget
                description: Destroy a Turnstile Widget.
              get:
                tags:
                  - Turnstile
                summary: Turnstile Widget Details
                description: Show a single challenge widget configuration.
              put:
                tags:
                  - Turnstile
                summary: Update a Turnstile Widget
                description: Update the configuration of a widget.
              parameters:
                - null
                - null
            /accounts/{account_id}/challenges/widgets/{sitekey}/rotate_secret:
              post:
                tags:
                  - Turnstile
                summary: Rotate Secret for a Turnstile Widget
                description: >
                  Generate a new secret key for this widget. If
                  `invalidate_immediately`

                  is set to `false`, the previous secret remains valid for 2
                  hours.


                  Note that secrets cannot be rotated again during the grace
                  period.
              parameters:
                - null
                - null
            /accounts/{account_id}/custom_ns:
              get:
                tags:
                  - Account-Level Custom Nameservers
                summary: List Account Custom Nameservers
                description: List an account's custom nameservers.
              post:
                tags:
                  - Account-Level Custom Nameservers
                summary: Add Account Custom Nameserver
            /accounts/{account_id}/custom_ns/{custom_ns_id}:
              delete:
                tags:
                  - Account-Level Custom Nameservers
                summary: Delete Account Custom Nameserver
            /accounts/{account_id}/custom_ns/availability:
              get:
                tags:
                  - Account-Level Custom Nameservers
                summary: Get Eligible Zones for Account Custom Nameservers
            /accounts/{account_id}/custom_ns/verify:
              post:
                tags:
                  - Account-Level Custom Nameservers
                summary: Verify Account Custom Nameserver Glue Records
            /accounts/{account_id}/d1/database:
              get:
                tags:
                  - D1
                summary: List D1 Databases
                description: Returns a list of D1 databases.
              post:
                tags:
                  - D1
                summary: Create D1 Database
                description: Returns the created D1 database.
            /accounts/{account_id}/devices:
              get:
                tags:
                  - Devices
                summary: List devices
                description: Fetches a list of enrolled devices.
            /accounts/{account_id}/devices/{device_id}:
              get:
                tags:
                  - Devices
                summary: Get device details
                description: Fetches details for a single device.
            /accounts/{account_id}/devices/{device_id}/override_codes:
              get:
                tags:
                  - Devices
                summary: Get an admin override code for a device
                description: >-
                  Fetches a one-time use admin override code for a device. This
                  relies on the **Admin Override** setting being enabled in your
                  device configuration.
            /accounts/{account_id}/devices/dex_tests:
              get:
                tags:
                  - Device DEX Tests
                summary: List Device DEX tests
                description: Fetch all DEX tests.
              post:
                tags:
                  - Device DEX Tests
                summary: Create Device DEX test
                description: Create a DEX test.
            /accounts/{account_id}/devices/dex_tests/{dex_test_id}:
              delete:
                tags:
                  - Device DEX Tests
                summary: Delete Device DEX test
                description: >-
                  Delete a Device DEX test. Returns the remaining device dex
                  tests for the account.
              get:
                tags:
                  - Device DEX Tests
                summary: Get Device DEX test
                description: Fetch a single DEX test.
              put:
                tags:
                  - Device DEX Tests
                summary: Update Device DEX test
                description: Update a DEX test.
            /accounts/{account_id}/devices/networks:
              get:
                tags:
                  - Device Managed Networks
                summary: List your device managed networks
                description: Fetches a list of managed networks for an account.
              post:
                tags:
                  - Device Managed Networks
                summary: Create a device managed network
                description: Creates a new device managed network.
            /accounts/{account_id}/devices/networks/{network_id}:
              delete:
                tags:
                  - Device Managed Networks
                summary: Delete a device managed network
                description: >-
                  Deletes a device managed network and fetches a list of the
                  remaining device managed networks for an account.
              get:
                tags:
                  - Device Managed Networks
                summary: Get device managed network details
                description: Fetches details for a single managed network.
              put:
                tags:
                  - Device Managed Networks
                summary: Update a device managed network
                description: Updates a configured device managed network.
            /accounts/{account_id}/devices/policies:
              get:
                tags:
                  - Devices
                summary: List device settings profiles
                description: Fetches a list of the device settings profiles for an account.
            /accounts/{account_id}/devices/policy:
              get:
                tags:
                  - Devices
                summary: Get the default device settings profile
                description: Fetches the default device settings profile for an account.
              patch:
                tags:
                  - Devices
                summary: Update the default device settings profile
                description: Updates the default device settings profile for an account.
              post:
                tags:
                  - Devices
                summary: Create a device settings profile
                description: >-
                  Creates a device settings profile to be applied to certain
                  devices matching the criteria.
            /accounts/{account_id}/devices/policy/{policy_id}:
              delete:
                tags:
                  - Devices
                summary: Delete a device settings profile
                description: >-
                  Deletes a device settings profile and fetches a list of the
                  remaining profiles for an account.
              get:
                tags:
                  - Devices
                summary: Get device settings profile by ID
                description: Fetches a device settings profile by ID.
              patch:
                tags:
                  - Devices
                summary: Update a device settings profile
                description: Updates a configured device settings profile.
            /accounts/{account_id}/devices/policy/{policy_id}/exclude:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Split Tunnel exclude list for a device settings
                  profile
                description: >-
                  Fetches the list of routes excluded from the WARP client's
                  tunnel for a specific device settings profile.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Split Tunnel exclude list for a device settings
                  profile
                description: >-
                  Sets the list of routes excluded from the WARP client's tunnel
                  for a specific device settings profile.
            /accounts/{account_id}/devices/policy/{policy_id}/fallback_domains:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Local Domain Fallback list for a device settings
                  profile
                description: >-
                  Fetches the list of domains to bypass Gateway DNS resolution
                  from a specified device settings profile. These domains will
                  use the specified local DNS resolver instead.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Local Domain Fallback list for a device settings
                  profile
                description: >-
                  Sets the list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead. This will only apply to the specified device settings
                  profile.
            /accounts/{account_id}/devices/policy/{policy_id}/include:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Split Tunnel include list for a device settings
                  profile
                description: >-
                  Fetches the list of routes included in the WARP client's
                  tunnel for a specific device settings profile.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Split Tunnel include list for a device settings
                  profile
                description: >-
                  Sets the list of routes included in the WARP client's tunnel
                  for a specific device settings profile.
            /accounts/{account_id}/devices/policy/exclude:
              get:
                tags:
                  - Devices
                summary: Get the Split Tunnel exclude list
                description: >-
                  Fetches the list of routes excluded from the WARP client's
                  tunnel.
              put:
                tags:
                  - Devices
                summary: Set the Split Tunnel exclude list
                description: >-
                  Sets the list of routes excluded from the WARP client's
                  tunnel.
            /accounts/{account_id}/devices/policy/fallback_domains:
              get:
                tags:
                  - Devices
                summary: Get your Local Domain Fallback list
                description: >-
                  Fetches a list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead.
              put:
                tags:
                  - Devices
                summary: Set your Local Domain Fallback list
                description: >-
                  Sets the list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead.
            /accounts/{account_id}/devices/policy/include:
              get:
                tags:
                  - Devices
                summary: Get the Split Tunnel include list
                description: >-
                  Fetches the list of routes included in the WARP client's
                  tunnel.
              put:
                tags:
                  - Devices
                summary: Set the Split Tunnel include list
                description: Sets the list of routes included in the WARP client's tunnel.
            /accounts/{account_id}/devices/posture:
              get:
                tags:
                  - Device posture rules
                summary: List device posture rules
                description: Fetches device posture rules for a Zero Trust account.
              post:
                tags:
                  - Device posture rules
                summary: Create a device posture rule
                description: Creates a new device posture rule.
            /accounts/{account_id}/devices/posture/{rule_id}:
              delete:
                tags:
                  - Device posture rules
                summary: Delete a device posture rule
                description: Deletes a device posture rule.
              get:
                tags:
                  - Device posture rules
                summary: Get device posture rule details
                description: Fetches a single device posture rule.
              put:
                tags:
                  - Device posture rules
                summary: Update a device posture rule
                description: Updates a device posture rule.
            /accounts/{account_id}/devices/posture/integration:
              get:
                tags:
                  - Device Posture Integrations
                summary: List your device posture integrations
                description: >-
                  Fetches the list of device posture integrations for an
                  account.
              post:
                tags:
                  - Device Posture Integrations
                summary: Create a device posture integration
                description: Create a new device posture integration.
            /accounts/{account_id}/devices/posture/integration/{integration_id}:
              delete:
                tags:
                  - Device Posture Integrations
                summary: Delete a device posture integration
                description: Delete a configured device posture integration.
              get:
                tags:
                  - Device Posture Integrations
                summary: Get device posture integration details
                description: Fetches details for a single device posture integration.
              patch:
                tags:
                  - Device Posture Integrations
                summary: Update a device posture integration
                description: Updates a configured device posture integration.
            /accounts/{account_id}/devices/revoke:
              post:
                tags:
                  - Devices
                summary: Revoke devices
                description: Revokes a list of devices.
            /accounts/{account_id}/devices/settings:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get device settings for a Zero Trust account
                description: >-
                  Describes the current device settings for a Zero Trust
                  account.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update device settings for a Zero Trust account
                description: Updates the current device settings for a Zero Trust account.
            /accounts/{account_id}/devices/unrevoke:
              post:
                tags:
                  - Devices
                summary: Unrevoke devices
                description: Unrevokes a list of devices.
            /accounts/{account_id}/dex/colos:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List Cloudflare colos
                description: >-
                  List Cloudflare colos that account's devices were connected to
                  during a time period, sorted by usage starting from the most
                  used colo. Colos without traffic are also returned and sorted
                  alphabetically.
            /accounts/{account_id}/dex/fleet-status/devices:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status devices
                description: List details for devices using WARP
            /accounts/{account_id}/dex/fleet-status/live:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status details by dimension
                description: List details for live (up to 60 minutes) devices using WARP
            /accounts/{account_id}/dex/fleet-status/over-time:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status aggregate details by dimension
                description: List details for devices using WARP, up to 7 days
            /accounts/{account_id}/dex/http-tests/{test_id}:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details and aggregate metrics for an http test
                description: >-
                  Get test details and aggregate performance metrics for an http
                  test for a given time period between 1 hour and 7 days.
            /accounts/{account_id}/dex/http-tests/{test_id}/percentiles:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get percentiles for an http test
                description: >-
                  Get percentiles for an http test for a given time period
                  between 1 hour and 7 days.
            /accounts/{account_id}/dex/tests:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List DEX test analytics
                description: List DEX tests
            /accounts/{account_id}/dex/tests/unique-devices:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get count of devices targeted
                description: >-
                  Returns unique count of devices that have run synthetic
                  application monitoring tests in the past 7 days.
            /accounts/{account_id}/dex/traceroute-test-results/{test_result_id}/network-path:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details for a specific traceroute test run
                description: >-
                  Get a breakdown of hops and performance metrics for a specific
                  traceroute test run
            /accounts/{account_id}/dex/traceroute-tests/{test_id}:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details and aggregate metrics for a traceroute test
                description: >-
                  Get test details and aggregate performance metrics for an
                  traceroute test for a given time period between 1 hour and 7
                  days.
            /accounts/{account_id}/dex/traceroute-tests/{test_id}/network-path:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get network path breakdown for a traceroute test
                description: >-
                  Get a breakdown of metrics by hop for individual traceroute
                  test runs
            /accounts/{account_id}/dex/traceroute-tests/{test_id}/percentiles:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get percentiles for a traceroute test
                description: >-
                  Get percentiles for a traceroute test for a given time period
                  between 1 hour and 7 days.
            /accounts/{account_id}/diagnostics/traceroute:
              post:
                tags:
                  - Diagnostics
                summary: Traceroute
                description: Run traceroutes from Cloudflare colos.
            /accounts/{account_id}/dlp/datasets:
              get:
                tags:
                  - DLP Datasets
                summary: Fetch all datasets with information about available versions.
                description: Fetch all datasets with information about available versions.
              post:
                tags:
                  - DLP Datasets
                summary: Create a new dataset.
                description: Create a new dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}:
              delete:
                tags:
                  - DLP Datasets
                summary: Delete a dataset.
                description: |-
                  Delete a dataset.

                  This deletes all versions of the dataset.
              get:
                tags:
                  - DLP Datasets
                summary: >-
                  Fetch a specific dataset with information about available
                  versions.
                description: >-
                  Fetch a specific dataset with information about available
                  versions.
              put:
                tags:
                  - DLP Datasets
                summary: Update details about a dataset.
                description: Update details about a dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}/upload:
              post:
                tags:
                  - DLP Datasets
                summary: Prepare to upload a new version of a dataset.
                description: Prepare to upload a new version of a dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}/upload/{version}:
              post:
                tags:
                  - DLP Datasets
                summary: Upload a new version of a dataset.
                description: Upload a new version of a dataset.
            /accounts/{account_id}/dlp/patterns/validate:
              post:
                tags:
                  - DLP Pattern Validation
                summary: Validate pattern
                description: >-
                  Validates whether this pattern is a valid regular expression.
                  Rejects it if the regular expression is too complex or can
                  match an unbounded-length string. Your regex will be rejected
                  if it uses the Kleene Star -- be sure to bound the maximum
                  number of characters that can be matched.
            /accounts/{account_id}/dlp/payload_log:
              get:
                tags:
                  - DLP Payload Log Settings
                summary: Get settings
                description: Gets the current DLP payload log settings for this account.
              put:
                tags:
                  - DLP Payload Log Settings
                summary: Update settings
                description: Updates the DLP payload log settings for this account.
            /accounts/{account_id}/dlp/profiles:
              get:
                tags:
                  - DLP Profiles
                summary: List all profiles
                description: Lists all DLP profiles in an account.
            /accounts/{account_id}/dlp/profiles/{profile_id}:
              get:
                tags:
                  - DLP Profiles
                summary: Get DLP Profile
                description: >-
                  Fetches a DLP profile by ID. Supports both predefined and
                  custom profiles
            /accounts/{account_id}/dlp/profiles/custom:
              post:
                tags:
                  - DLP Profiles
                summary: Create custom profiles
                description: Creates a set of DLP custom profiles.
            /accounts/{account_id}/dlp/profiles/custom/{profile_id}:
              delete:
                tags:
                  - DLP Profiles
                summary: Delete custom profile
                description: Deletes a DLP custom profile.
              get:
                tags:
                  - DLP Profiles
                summary: Get custom profile
                description: Fetches a custom DLP profile.
              put:
                tags:
                  - DLP Profiles
                summary: Update custom profile
                description: Updates a DLP custom profile.
            /accounts/{account_id}/dlp/profiles/predefined/{profile_id}:
              get:
                tags:
                  - DLP Profiles
                summary: Get predefined profile
                description: Fetches a predefined DLP profile.
              put:
                tags:
                  - DLP Profiles
                summary: Update predefined profile
                description: >-
                  Updates a DLP predefined profile. Only supports
                  enabling/disabling entries.
            /accounts/{account_id}/dns_firewall:
              get:
                tags:
                  - DNS Firewall
                summary: List DNS Firewall Clusters
                description: List configured DNS Firewall clusters for an account.
              post:
                tags:
                  - DNS Firewall
                summary: Create DNS Firewall Cluster
                description: Create a configured DNS Firewall Cluster.
            /accounts/{account_id}/dns_firewall/{dns_firewall_id}:
              delete:
                tags:
                  - DNS Firewall
                summary: Delete DNS Firewall Cluster
                description: Delete a configured DNS Firewall Cluster.
              get:
                tags:
                  - DNS Firewall
                summary: DNS Firewall Cluster Details
                description: Show a single configured DNS Firewall cluster for an account.
              patch:
                tags:
                  - DNS Firewall
                summary: Update DNS Firewall Cluster
                description: Modify a DNS Firewall Cluster configuration.
            /accounts/{account_id}/gateway:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get Zero Trust account information
                description: Gets information about the current Zero Trust account.
              post:
                tags:
                  - Zero Trust accounts
                summary: Create Zero Trust account
                description: >-
                  Creates a Zero Trust account with an existing Cloudflare
                  account.
            /accounts/{account_id}/gateway/app_types:
              get:
                tags:
                  - Zero Trust Gateway application and application type mappings
                summary: List application and application type mappings
                description: Fetches all application and application type mappings.
            /accounts/{account_id}/gateway/audit_ssh_settings:
              get:
                tags:
                  - Zero Trust Audit SSH Settings
                summary: Get Zero Trust Audit SSH settings
                description: Get all Zero Trust Audit SSH settings for an account.
              put:
                tags:
                  - Zero Trust Audit SSH Settings
                summary: Update Zero Trust Audit SSH settings
                description: Updates Zero Trust Audit SSH settings.
            /accounts/{account_id}/gateway/categories:
              get:
                tags:
                  - Zero Trust Gateway categories
                summary: List categories
                description: Fetches a list of all categories.
            /accounts/{account_id}/gateway/configuration:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get Zero Trust account configuration
                description: Fetches the current Zero Trust account configuration.
              patch:
                tags:
                  - Zero Trust accounts
                summary: Patch Zero Trust account configuration
                description: >-
                  Patches the current Zero Trust account configuration. This
                  endpoint can update a single subcollection of settings such as
                  `antivirus`, `tls_decrypt`, `activity_log`, `block_page`,
                  `browser_isolation`, `fips`, `body_scanning`, or
                  `custom_certificate`, without updating the entire
                  configuration object. Returns an error if any collection of
                  settings is not properly configured.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update Zero Trust account configuration
                description: Updates the current Zero Trust account configuration.
            /accounts/{account_id}/gateway/lists:
              get:
                tags:
                  - Zero Trust lists
                summary: List Zero Trust lists
                description: Fetches all Zero Trust lists for an account.
              post:
                tags:
                  - Zero Trust lists
                summary: Create Zero Trust list
                description: Creates a new Zero Trust list.
            /accounts/{account_id}/gateway/lists/{list_id}:
              delete:
                tags:
                  - Zero Trust lists
                summary: Delete Zero Trust list
                description: Deletes a Zero Trust list.
              get:
                tags:
                  - Zero Trust lists
                summary: Get Zero Trust list details
                description: Fetches a single Zero Trust list.
              patch:
                tags:
                  - Zero Trust lists
                summary: Patch Zero Trust list
                description: Appends or removes an item from a configured Zero Trust list.
              put:
                tags:
                  - Zero Trust lists
                summary: Update Zero Trust list
                description: Updates a configured Zero Trust list.
            /accounts/{account_id}/gateway/lists/{list_id}/items:
              get:
                tags:
                  - Zero Trust lists
                summary: Get Zero Trust list items
                description: Fetches all items in a single Zero Trust list.
            /accounts/{account_id}/gateway/locations:
              get:
                tags:
                  - Zero Trust Gateway locations
                summary: List Zero Trust Gateway locations
                description: Fetches Zero Trust Gateway locations for an account.
              post:
                tags:
                  - Zero Trust Gateway locations
                summary: Create a Zero Trust Gateway location
                description: Creates a new Zero Trust Gateway location.
            /accounts/{account_id}/gateway/locations/{location_id}:
              delete:
                tags:
                  - Zero Trust Gateway locations
                summary: Delete a Zero Trust Gateway location
                description: Deletes a configured Zero Trust Gateway location.
              get:
                tags:
                  - Zero Trust Gateway locations
                summary: Get Zero Trust Gateway location details
                description: Fetches a single Zero Trust Gateway location.
              put:
                tags:
                  - Zero Trust Gateway locations
                summary: Update a Zero Trust Gateway location
                description: Updates a configured Zero Trust Gateway location.
            /accounts/{account_id}/gateway/logging:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get logging settings for the Zero Trust account
                description: Fetches the current logging settings for Zero Trust account.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update Zero Trust account logging settings
                description: Updates logging settings for the current Zero Trust account.
            /accounts/{account_id}/gateway/proxy_endpoints:
              get:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Get a proxy endpoint
                description: Fetches a single Zero Trust Gateway proxy endpoint.
              post:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Create a proxy endpoint
                description: Creates a new Zero Trust Gateway proxy endpoint.
            /accounts/{account_id}/gateway/proxy_endpoints/{proxy_endpoint_id}:
              delete:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Delete a proxy endpoint
                description: Deletes a configured Zero Trust Gateway proxy endpoint.
              get:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: List proxy endpoints
                description: Fetches all Zero Trust Gateway proxy endpoints for an account.
              patch:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Update a proxy endpoint
                description: Updates a configured Zero Trust Gateway proxy endpoint.
            /accounts/{account_id}/gateway/rules:
              get:
                tags:
                  - Zero Trust Gateway rules
                summary: List Zero Trust Gateway rules
                description: Fetches the Zero Trust Gateway rules for an account.
              post:
                tags:
                  - Zero Trust Gateway rules
                summary: Create a Zero Trust Gateway rule
                description: Creates a new Zero Trust Gateway rule.
            /accounts/{account_id}/gateway/rules/{rule_id}:
              delete:
                tags:
                  - Zero Trust Gateway rules
                summary: Delete a Zero Trust Gateway rule
                description: Deletes a Zero Trust Gateway rule.
              get:
                tags:
                  - Zero Trust Gateway rules
                summary: Get Zero Trust Gateway rule details
                description: Fetches a single Zero Trust Gateway rule.
              put:
                tags:
                  - Zero Trust Gateway rules
                summary: Update a Zero Trust Gateway rule
                description: Updates a configured Zero Trust Gateway rule.
            /accounts/{account_id}/hyperdrive/configs:
              get:
                tags:
                  - Hyperdrive
                summary: List Hyperdrives
                description: Returns a list of Hyperdrives
              post:
                tags:
                  - Hyperdrive
                summary: Create Hyperdrive
                description: Creates and returns a new Hyperdrive configuration.
            /accounts/{account_id}/hyperdrive/configs/{hyperdrive_id}:
              delete:
                tags:
                  - Hyperdrive
                summary: Delete Hyperdrive
                description: Deletes the specified Hyperdrive.
              get:
                tags:
                  - Hyperdrive
                summary: Get Hyperdrive
                description: Returns the specified Hyperdrive configuration.
              patch:
                tags:
                  - Hyperdrive
                summary: Patch Hyperdrive
                description: >-
                  Patches and returns the specified Hyperdrive configuration.
                  Updates to the origin and caching settings are applied with an
                  all-or-nothing approach.
              put:
                tags:
                  - Hyperdrive
                summary: Update Hyperdrive
                description: Updates and returns the specified Hyperdrive configuration.
            /accounts/{account_id}/images/v1:
              get:
                tags:
                  - Cloudflare Images
                summary: List images
                description: >-
                  List up to 100 images with one request. Use the optional
                  parameters below to get a specific range of images.
              post:
                tags:
                  - Cloudflare Images
                summary: Upload an image
                description: >
                  Upload an image with up to 10 Megabytes using a single HTTP
                  POST (multipart/form-data) request.

                  An image can be uploaded by sending an image file or passing
                  an accessible to an API url.
            /accounts/{account_id}/images/v1/{image_id}:
              delete:
                tags:
                  - Cloudflare Images
                summary: Delete image
                description: >-
                  Delete an image on Cloudflare Images. On success, all copies
                  of the image are deleted and purged from cache.
              get:
                tags:
                  - Cloudflare Images
                summary: Image details
                description: Fetch details for a single image.
              patch:
                tags:
                  - Cloudflare Images
                summary: Update image
                description: >-
                  Update image access control. On access control change, all
                  copies of the image are purged from cache.
            /accounts/{account_id}/images/v1/{image_id}/blob:
              get:
                tags:
                  - Cloudflare Images
                summary: Base image
                description: >-
                  Fetch base image. For most images this will be the originally
                  uploaded file. For larger images it can be a near-lossless
                  version of the original.
            /accounts/{account_id}/images/v1/keys:
              get:
                tags:
                  - Cloudflare Images Keys
                summary: List Signing Keys
                description: >-
                  Lists your signing keys. These can be found on your Cloudflare
                  Images dashboard.
            /accounts/{account_id}/images/v1/keys/{signing_key_name}:
              delete:
                tags:
                  - Cloudflare Images Keys
                summary: Delete Signing Key
                description: >
                  Delete signing key with specified name. Returns all keys
                  available.

                  When last key is removed, a new default signing key will be
                  generated.
              put:
                tags:
                  - Cloudflare Images Keys
                summary: Create a new Signing Key
                description: >-
                  Create a new signing key with specified name. Returns all keys
                  available.
            /accounts/{account_id}/images/v1/stats:
              get:
                tags:
                  - Cloudflare Images
                summary: Images usage statistics
                description: Fetch usage statistics details for Cloudflare Images.
            /accounts/{account_id}/images/v1/variants:
              get:
                tags:
                  - Cloudflare Images Variants
                summary: List variants
                description: Lists existing variants.
              post:
                tags:
                  - Cloudflare Images Variants
                summary: Create a variant
                description: >-
                  Specify variants that allow you to resize images for different
                  use cases.
            /accounts/{account_id}/images/v1/variants/{variant_id}:
              delete:
                tags:
                  - Cloudflare Images Variants
                summary: Delete a variant
                description: >-
                  Deleting a variant purges the cache for all images associated
                  with the variant.
              get:
                tags:
                  - Cloudflare Images Variants
                summary: Variant details
                description: Fetch details for a single variant.
              patch:
                tags:
                  - Cloudflare Images Variants
                summary: Update a variant
                description: >-
                  Updating a variant purges the cache for all images associated
                  with the variant.
            /accounts/{account_id}/images/v2:
              get:
                tags:
                  - Cloudflare Images
                summary: List images V2
                description: >
                  List up to 10000 images with one request. Use the optional
                  parameters below to get a specific range of images.

                  Endpoint returns continuation_token if more images are
                  present.
            /accounts/{account_id}/images/v2/direct_upload:
              post:
                tags:
                  - Cloudflare Images
                summary: Create authenticated direct upload URL V2
                description: >-
                  Direct uploads allow users to upload images without API keys.
                  A common use case are web apps, client-side applications, or
                  mobile devices where users upload content directly to
                  Cloudflare Images. This method creates a draft record for a
                  future image. It returns an upload URL and an image
                  identifier. To verify if the image itself has been uploaded,
                  send an image details request
                  (accounts/:account_identifier/images/v1/:identifier), and
                  check that the `draft: true` property is not present.
            /accounts/{account_id}/intel/asn/{asn}:
              get:
                tags:
                  - ASN Intelligence
                summary: Get ASN Overview
            /accounts/{account_id}/intel/asn/{asn}/subnets:
              get:
                tags:
                  - ASN Intelligence
                summary: Get ASN Subnets
            /accounts/{account_id}/intel/attack-surface-report/{issue_id}/dismiss:
              put:
                tags:
                  - Security Center Insights
                summary: Archive Security Center Insight
            /accounts/{account_id}/intel/attack-surface-report/issue-types:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issues Types
            /accounts/{account_id}/intel/attack-surface-report/issues:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issues
            /accounts/{account_id}/intel/attack-surface-report/issues/class:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Class
            /accounts/{account_id}/intel/attack-surface-report/issues/severity:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Severity
            /accounts/{account_id}/intel/attack-surface-report/issues/type:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Type
            /accounts/{account_id}/intel/dns:
              get:
                tags:
                  - Passive DNS by IP
                summary: Get Passive DNS by IP
            /accounts/{account_id}/intel/domain:
              get:
                tags:
                  - Domain Intelligence
                summary: Get Domain Details
            /accounts/{account_id}/intel/domain-history:
              get:
                tags:
                  - Domain History
                summary: Get Domain History
            /accounts/{account_id}/intel/domain/bulk:
              get:
                tags:
                  - Domain Intelligence
                summary: Get Multiple Domain Details
            /accounts/{account_id}/intel/indicator-feeds:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feeds owned by this account
              post:
                tags:
                  - Custom Indicator Feeds
                summary: Create new indicator feed
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feed metadata
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}/data:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feed data
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}/snapshot:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Update indicator feed data
            /accounts/{account_id}/intel/indicator-feeds/permissions/add:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Grant permission to indicator feed
            /accounts/{account_id}/intel/indicator-feeds/permissions/remove:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Revoke permission to indicator feed
            /accounts/{account_id}/intel/indicator-feeds/permissions/view:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: List indicator feed permissions
            /accounts/{account_id}/intel/ip:
              get:
                tags:
                  - IP Intelligence
                summary: Get IP Overview
            /accounts/{account_id}/intel/ip-list:
              get:
                tags:
                  - IP List
                summary: Get IP Lists
            /accounts/{account_id}/intel/miscategorization:
              post:
                tags:
                  - Miscategorization
                summary: Create Miscategorization
            /accounts/{account_id}/intel/sinkholes:
              get:
                tags:
                  - Sinkhole Config
                summary: List sinkholes owned by this account
            /accounts/{account_id}/intel/whois:
              get:
                tags:
                  - WHOIS Record
                summary: Get WHOIS Record
            /accounts/{account_id}/load_balancers/monitors:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: List Monitors
                description: List configured monitors for an account.
              post:
                tags:
                  - Account Load Balancer Monitors
                summary: Create Monitor
                description: Create a configured monitor.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}:
              delete:
                tags:
                  - Account Load Balancer Monitors
                summary: Delete Monitor
                description: Delete a configured monitor.
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: Monitor Details
                description: List a single configured monitor for an account.
              patch:
                tags:
                  - Account Load Balancer Monitors
                summary: Patch Monitor
                description: >-
                  Apply changes to an existing monitor, overwriting the supplied
                  properties.
              put:
                tags:
                  - Account Load Balancer Monitors
                summary: Update Monitor
                description: Modify a configured monitor.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}/preview:
              post:
                tags:
                  - Account Load Balancer Monitors
                summary: Preview Monitor
                description: >-
                  Preview pools using the specified monitor with provided
                  monitor details. The returned preview_id can be used in the
                  preview endpoint to retrieve the results.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}/references:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: List Monitor References
                description: Get the list of resources that reference the provided monitor.
            /accounts/{account_id}/load_balancers/pools:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: List Pools
                description: List configured pools.
              patch:
                tags:
                  - Account Load Balancer Pools
                summary: Patch Pools
                description: >-
                  Apply changes to a number of existing pools, overwriting the
                  supplied properties. Pools are ordered by ascending `name`.
                  Returns the list of affected pools. Supports the standard
                  pagination query parameters, either `limit`/`offset` or
                  `per_page`/`page`.
              post:
                tags:
                  - Account Load Balancer Pools
                summary: Create Pool
                description: Create a new pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}:
              delete:
                tags:
                  - Account Load Balancer Pools
                summary: Delete Pool
                description: Delete a configured pool.
              get:
                tags:
                  - Account Load Balancer Pools
                summary: Pool Details
                description: Fetch a single configured pool.
              patch:
                tags:
                  - Account Load Balancer Pools
                summary: Patch Pool
                description: >-
                  Apply changes to an existing pool, overwriting the supplied
                  properties.
              put:
                tags:
                  - Account Load Balancer Pools
                summary: Update Pool
                description: Modify a configured pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/health:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: Pool Health Details
                description: Fetch the latest pool health status for a single pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/preview:
              post:
                tags:
                  - Account Load Balancer Pools
                summary: Preview Pool
                description: >-
                  Preview pool health using provided monitor details. The
                  returned preview_id can be used in the preview endpoint to
                  retrieve the results.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/references:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: List Pool References
                description: Get the list of resources that reference the provided pool.
            /accounts/{account_id}/load_balancers/preview/{preview_id}:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: Preview Result
                description: >-
                  Get the result of a previous preview operation using the
                  provided preview_id.
            /accounts/{account_id}/load_balancers/regions:
              get:
                tags:
                  - Load Balancer Regions
                summary: List Regions
                description: List all region mappings.
            /accounts/{account_id}/load_balancers/regions/{region_id}:
              get:
                tags:
                  - Load Balancer Regions
                summary: Get Region
                description: Get a single region mapping.
            /accounts/{account_id}/load_balancers/search:
              get:
                tags:
                  - Account Load Balancer Search
                summary: Search Resources
                description: Search for Load Balancing resources.
            /accounts/{account_id}/logpush/datasets/{dataset_id}/fields:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List fields
                description: >-
                  Lists all fields available for a dataset. The response result
                  is an object with key-value pairs, where keys are field names,
                  and values are descriptions.
            /accounts/{account_id}/logpush/datasets/{dataset_id}/jobs:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List Logpush jobs for a dataset
                description: Lists Logpush jobs for an account for a dataset.
            /accounts/{account_id}/logpush/jobs:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List Logpush jobs
                description: Lists Logpush jobs for an account.
              post:
                tags:
                  - Logpush jobs for an account
                summary: Create Logpush job
                description: Creates a new Logpush job for an account.
            /accounts/{account_id}/logpush/jobs/{job_id}:
              delete:
                tags:
                  - Logpush jobs for an account
                summary: Delete Logpush job
                description: Deletes a Logpush job.
              get:
                tags:
                  - Logpush jobs for an account
                summary: Get Logpush job details
                description: Gets the details of a Logpush job.
              put:
                tags:
                  - Logpush jobs for an account
                summary: Update Logpush job
                description: Updates a Logpush job.
            /accounts/{account_id}/logpush/ownership:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Get ownership challenge
                description: Gets a new ownership challenge sent to your destination.
            /accounts/{account_id}/logpush/ownership/validate:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Validate ownership challenge
                description: Validates ownership challenge of the destination.
            /accounts/{account_id}/logpush/validate/destination/exists:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Check destination exists
                description: Checks if there is an existing job with a destination.
            /accounts/{account_id}/logpush/validate/origin:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Validate origin
                description: Validates logpull origin with logpull_options.
            /accounts/{account_id}/logs/control/cmb/config:
              delete:
                tags:
                  - Logcontrol CMB config for an account
                summary: Delete CMB config
                description: Deletes CMB config.
              get:
                tags:
                  - Logcontrol CMB config for an account
                summary: Get CMB config
                description: Gets CMB config.
              post:
                tags:
                  - Logcontrol CMB config for an account
                summary: Update CMB config
                description: Updates CMB config.
            /accounts/{account_id}/members:
              get:
                tags:
                  - Account Members
                summary: List Members
                description: List all members of an account.
              post:
                tags:
                  - Account Members
                summary: Add Member
                description: Add a user to the list of members for this account.
            /accounts/{account_id}/members/{member_id}:
              delete:
                tags:
                  - Account Members
                summary: Remove Member
                description: Remove a member from an account.
              get:
                tags:
                  - Account Members
                summary: Member Details
                description: Get information about a specific member of an account.
              put:
                tags:
                  - Account Members
                summary: Update Member
                description: Modify an account member.
            /accounts/{account_id}/mtls_certificates:
              get:
                tags:
                  - mTLS Certificate Management
                summary: List mTLS certificates
                description: Lists all mTLS certificates.
              post:
                tags:
                  - mTLS Certificate Management
                summary: Upload mTLS certificate
                description: >-
                  Upload a certificate that you want to use with mTLS-enabled
                  Cloudflare services.
            /accounts/{account_id}/mtls_certificates/{mtls_certificate_id}:
              delete:
                tags:
                  - mTLS Certificate Management
                summary: Delete mTLS certificate
                description: >-
                  Deletes the mTLS certificate unless the certificate is in use
                  by one or more Cloudflare services.
              get:
                tags:
                  - mTLS Certificate Management
                summary: Get mTLS certificate
                description: Fetches a single mTLS certificate.
            /accounts/{account_id}/mtls_certificates/{mtls_certificate_id}/associations:
              get:
                tags:
                  - mTLS Certificate Management
                summary: List mTLS certificate associations
                description: >-
                  Lists all active associations between the certificate and
                  Cloudflare services.
            /accounts/{account_id}/pages/projects:
              get:
                tags:
                  - Pages Project
                summary: Get projects
                description: Fetch a list of all user projects.
              post:
                tags:
                  - Pages Project
                summary: Create project
                description: Create a new project.
            /accounts/{account_id}/pages/projects/{project_name}:
              delete:
                tags:
                  - Pages Project
                summary: Delete project
                description: Delete a project by name.
              get:
                tags:
                  - Pages Project
                summary: Get project
                description: Fetch a project by name.
              patch:
                tags:
                  - Pages Project
                summary: Update project
                description: >-
                  Set new attributes for an existing project. Modify environment
                  variables. To delete an environment variable, set the key to
                  null.
            /accounts/{account_id}/pages/projects/{project_name}/deployments:
              get:
                tags:
                  - Pages Deployment
                summary: Get deployments
                description: Fetch a list of project deployments.
              post:
                tags:
                  - Pages Deployment
                summary: Create deployment
                description: >-
                  Start a new deployment from production. The repository and
                  account must have already been authorized on the Cloudflare
                  Pages dashboard.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}:
              delete:
                tags:
                  - Pages Deployment
                summary: Delete deployment
                description: Delete a deployment.
              get:
                tags:
                  - Pages Deployment
                summary: Get deployment info
                description: Fetch information about a deployment.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/history/logs:
              get:
                tags:
                  - Pages Deployment
                summary: Get deployment logs
                description: Fetch deployment logs for a project.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/retry:
              post:
                tags:
                  - Pages Deployment
                summary: Retry deployment
                description: Retry a previous deployment.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/rollback:
              post:
                tags:
                  - Pages Deployment
                summary: Rollback deployment
                description: >-
                  Rollback the production deployment to a previous deployment.
                  You can only rollback to succesful builds on production.
            /accounts/{account_id}/pages/projects/{project_name}/domains:
              get:
                tags:
                  - Pages Domains
                summary: Get domains
                description: Fetch a list of all domains associated with a Pages project.
              post:
                tags:
                  - Pages Domains
                summary: Add domain
                description: Add a new domain for the Pages project.
            /accounts/{account_id}/pages/projects/{project_name}/domains/{domain_name}:
              delete:
                tags:
                  - Pages Domains
                summary: Delete domain
                description: Delete a Pages project's domain.
              get:
                tags:
                  - Pages Domains
                summary: Get domain
                description: Fetch a single domain.
              patch:
                tags:
                  - Pages Domains
                summary: Patch domain
                description: Retry the validation status of a single domain.
            /accounts/{account_id}/pages/projects/{project_name}/purge_build_cache:
              post:
                tags:
                  - Pages Build Cache
                summary: Purge build cache
                description: Purge all cached build artifacts for a Pages project
            /accounts/{account_id}/pcaps:
              get:
                tags:
                  - Magic PCAP collection
                summary: List packet capture requests
                description: Lists all packet capture requests for an account.
              post:
                tags:
                  - Magic PCAP collection
                summary: Create PCAP request
                description: Create new PCAP request for account.
            /accounts/{account_id}/pcaps/{pcap_id}:
              get:
                tags:
                  - Magic PCAP collection
                summary: Get PCAP request
                description: Get information for a PCAP request by id.
            /accounts/{account_id}/pcaps/{pcap_id}/download:
              get:
                tags:
                  - Magic PCAP collection
                summary: Download Simple PCAP
                description: >-
                  Download PCAP information into a file. Response is a binary
                  PCAP file.
            /accounts/{account_id}/pcaps/ownership:
              get:
                tags:
                  - Magic PCAP collection
                summary: List PCAPs Bucket Ownership
                description: List all buckets configured for use with PCAPs API.
              post:
                tags:
                  - Magic PCAP collection
                summary: Add buckets for full packet captures
                description: Adds an AWS or GCP bucket to use with full packet captures.
            /accounts/{account_id}/pcaps/ownership/{ownership_id}:
              delete:
                tags:
                  - Magic PCAP collection
                summary: Delete buckets for full packet captures
                description: Deletes buckets added to the packet captures API.
            /accounts/{account_id}/pcaps/ownership/validate:
              post:
                tags:
                  - Magic PCAP collection
                summary: Validate buckets for full packet captures
                description: Validates buckets added to the packet captures API.
            /accounts/{account_id}/r2/buckets:
              get:
                tags:
                  - R2 Bucket
                summary: List Buckets
                description: Lists all R2 buckets on your account
              post:
                tags:
                  - R2 Bucket
                summary: Create Bucket
                description: Creates a new R2 bucket.
            /accounts/{account_id}/r2/buckets/{bucket_name}:
              delete:
                tags:
                  - R2 Bucket
                summary: Delete Bucket
                description: Deletes an existing R2 bucket.
              get:
                tags:
                  - R2 Bucket
                summary: Get Bucket
                description: Gets metadata for an existing R2 bucket.
            /accounts/{account_id}/r2/buckets/{bucket_name}/sippy:
              delete:
                tags:
                  - R2 Bucket
                summary: Disable Sippy
                description: Disables Sippy on this bucket
              get:
                tags:
                  - R2 Bucket
                summary: Get Sippy Configuration
                description: Gets configuration for Sippy for an existing R2 bucket.
              put:
                tags:
                  - R2 Bucket
                summary: Enable Sippy
                description: Sets configuration for Sippy for an existing R2 bucket.
            /accounts/{account_id}/registrar/domains:
              get:
                tags:
                  - Registrar Domains
                summary: List domains
                description: List domains handled by Registrar.
            /accounts/{account_id}/registrar/domains/{domain_name}:
              get:
                tags:
                  - Registrar Domains
                summary: Get domain
                description: Show individual domain.
              put:
                tags:
                  - Registrar Domains
                summary: Update domain
                description: Update individual domain.
            /accounts/{account_id}/roles:
              get:
                tags:
                  - Account Roles
                summary: List Roles
                description: Get all available roles for an account.
            /accounts/{account_id}/roles/{role_id}:
              get:
                tags:
                  - Account Roles
                summary: Role Details
                description: Get information about a specific role for an account.
            /accounts/{account_id}/rules/lists:
              get:
                tags:
                  - Lists
                summary: Get lists
                description: Fetches all lists in the account.
              post:
                tags:
                  - Lists
                summary: Create a list
                description: Creates a new list of the specified type.
            /accounts/{account_id}/rules/lists/{list_id}:
              delete:
                tags:
                  - Lists
                summary: Delete a list
                description: Deletes a specific list and all its items.
              get:
                tags:
                  - Lists
                summary: Get a list
                description: Fetches the details of a list.
              put:
                tags:
                  - Lists
                summary: Update a list
                description: Updates the description of a list.
            /accounts/{account_id}/rules/lists/{list_id}/items:
              delete:
                tags:
                  - Lists
                summary: Delete list items
                description: >-
                  Removes one or more items from a list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
              get:
                tags:
                  - Lists
                summary: Get list items
                description: Fetches all the items in the list.
              post:
                tags:
                  - Lists
                summary: Create list items
                description: >-
                  Appends new items to the list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
              put:
                tags:
                  - Lists
                summary: Update all list items
                description: >-
                  Removes all existing items from the list and adds the provided
                  items to the list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
            /accounts/{account_id}/rulesets:
              get:
                tags:
                  - Account Rulesets
                summary: List account rulesets
                description: Fetches all rulesets at the account level.
              post:
                tags:
                  - Account Rulesets
                summary: Create an account ruleset
                description: Creates a ruleset at the account level.
            /accounts/{account_id}/rulesets/{ruleset_id}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset
                description: Deletes all versions of an existing account ruleset.
              get:
                tags:
                  - Account Rulesets
                summary: Get an account ruleset
                description: Fetches the latest version of an account ruleset.
              put:
                tags:
                  - Account Rulesets
                summary: Update an account ruleset
                description: Updates an account ruleset, creating a new version.
            /accounts/{account_id}/rulesets/{ruleset_id}/rules:
              post:
                tags:
                  - Account Rulesets
                summary: Create an account ruleset rule
                description: >-
                  Adds a new rule to an account ruleset. The rule will be added
                  to the end of the existing list of rules in the ruleset by
                  default.
            /accounts/{account_id}/rulesets/{ruleset_id}/rules/{rule_id}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset rule
                description: Deletes an existing rule from an account ruleset.
              patch:
                tags:
                  - Account Rulesets
                summary: Update an account ruleset rule
                description: Updates an existing rule in an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions:
              get:
                tags:
                  - Account Rulesets
                summary: List an account ruleset's versions
                description: Fetches the versions of an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions/{ruleset_version}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset version
                description: Deletes an existing version of an account ruleset.
              get:
                tags:
                  - Account Rulesets
                summary: Get an account ruleset version
                description: Fetches a specific version of an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions/{ruleset_version}/by_tag/{rule_tag}:
              get:
                tags:
                  - Account Rulesets
                summary: List an account ruleset version's rules by tag
                description: >-
                  Fetches the rules of a managed account ruleset version for a
                  given tag.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint:
              get:
                tags:
                  - Account Rulesets
                summary: Get an account entry point ruleset
                description: >-
                  Fetches the latest version of the account entry point ruleset
                  for a given phase.
              put:
                tags:
                  - Account Rulesets
                summary: Update an account entry point ruleset
                description: >-
                  Updates an account entry point ruleset, creating a new
                  version.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions:
              get:
                tags:
                  - Account Rulesets
                summary: List an account entry point ruleset's versions
                description: Fetches the versions of an account entry point ruleset.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions/{ruleset_version}:
              get:
                tags:
                  - Account Rulesets
                summary: Get an account entry point ruleset version
                description: Fetches a specific version of an account entry point ruleset.
            /accounts/{account_id}/rum/site_info:
              post:
                tags:
                  - Web Analytics
                summary: Create a Web Analytics site
                description: Creates a new Web Analytics site.
            /accounts/{account_id}/rum/site_info/{site_id}:
              delete:
                tags:
                  - Web Analytics
                summary: Delete a Web Analytics site
                description: Deletes an existing Web Analytics site.
              get:
                tags:
                  - Web Analytics
                summary: Get a Web Analytics site
                description: Retrieves a Web Analytics site.
              put:
                tags:
                  - Web Analytics
                summary: Update a Web Analytics site
                description: Updates an existing Web Analytics site.
            /accounts/{account_id}/rum/site_info/list:
              get:
                tags:
                  - Web Analytics
                summary: List Web Analytics sites
                description: Lists all Web Analytics sites of an account.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rule:
              post:
                tags:
                  - Web Analytics
                summary: Create a Web Analytics rule
                description: Creates a new rule in a Web Analytics ruleset.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rule/{rule_id}:
              delete:
                tags:
                  - Web Analytics
                summary: Delete a Web Analytics rule
                description: Deletes an existing rule from a Web Analytics ruleset.
              put:
                tags:
                  - Web Analytics
                summary: Update a Web Analytics rule
                description: Updates a rule in a Web Analytics ruleset.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rules:
              get:
                tags:
                  - Web Analytics
                summary: List rules in Web Analytics ruleset
                description: Lists all the rules in a Web Analytics ruleset.
              post:
                tags:
                  - Web Analytics
                summary: Update Web Analytics rules
                description: >-
                  Modifies one or more rules in a Web Analytics ruleset with a
                  single request.
            /accounts/{account_id}/secondary_dns/acls:
              get:
                tags:
                  - Secondary DNS (ACL)
                summary: List ACLs
                description: List ACLs.
              post:
                tags:
                  - Secondary DNS (ACL)
                summary: Create ACL
                description: Create ACL.
            /accounts/{account_id}/secondary_dns/acls/{acl_id}:
              delete:
                tags:
                  - Secondary DNS (ACL)
                summary: Delete ACL
                description: Delete ACL.
              get:
                tags:
                  - Secondary DNS (ACL)
                summary: ACL Details
                description: Get ACL.
              put:
                tags:
                  - Secondary DNS (ACL)
                summary: Update ACL
                description: Modify ACL.
            /accounts/{account_id}/secondary_dns/peers:
              get:
                tags:
                  - Secondary DNS (Peer)
                summary: List Peers
                description: List Peers.
              post:
                tags:
                  - Secondary DNS (Peer)
                summary: Create Peer
                description: Create Peer.
            /accounts/{account_id}/secondary_dns/peers/{peer_id}:
              delete:
                tags:
                  - Secondary DNS (Peer)
                summary: Delete Peer
                description: Delete Peer.
              get:
                tags:
                  - Secondary DNS (Peer)
                summary: Peer Details
                description: Get Peer.
              put:
                tags:
                  - Secondary DNS (Peer)
                summary: Update Peer
                description: Modify Peer.
            /accounts/{account_id}/secondary_dns/tsigs:
              get:
                tags:
                  - Secondary DNS (TSIG)
                summary: List TSIGs
                description: List TSIGs.
              post:
                tags:
                  - Secondary DNS (TSIG)
                summary: Create TSIG
                description: Create TSIG.
            /accounts/{account_id}/secondary_dns/tsigs/{tsig_id}:
              delete:
                tags:
                  - Secondary DNS (TSIG)
                summary: Delete TSIG
                description: Delete TSIG.
              get:
                tags:
                  - Secondary DNS (TSIG)
                summary: TSIG Details
                description: Get TSIG.
              put:
                tags:
                  - Secondary DNS (TSIG)
                summary: Update TSIG
                description: Modify TSIG.
            /accounts/{account_id}/storage/analytics:
              get:
                tags:
                  - Workers KV Request Analytics
                summary: Query Request Analytics
                description: Retrieves Workers KV request metrics for the given account.
            /accounts/{account_id}/storage/analytics/stored:
              get:
                tags:
                  - Workers KV Stored Data Analytics
                summary: Query Stored Data Analytics
                description: >-
                  Retrieves Workers KV stored data metrics for the given
                  account.
            /accounts/{account_id}/storage/kv/namespaces:
              get:
                tags:
                  - Workers KV Namespace
                summary: List Namespaces
                description: Returns the namespaces owned by an account.
              post:
                tags:
                  - Workers KV Namespace
                summary: Create a Namespace
                description: >-
                  Creates a namespace under the given title. A `400` is returned
                  if the account already owns a namespace with this title. A
                  namespace must be explicitly deleted to be replaced.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Remove a Namespace
                description: Deletes the namespace corresponding to the given ID.
              put:
                tags:
                  - Workers KV Namespace
                summary: Rename a Namespace
                description: Modifies a namespace's title.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/bulk:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Delete multiple key-value pairs
                description: >-
                  Remove multiple KV pairs from the namespace. Body should be an
                  array of up to 10,000 keys to be removed.
              put:
                tags:
                  - Workers KV Namespace
                summary: Write multiple key-value pairs
                description: >-
                  Write multiple keys and values at once. Body should be an
                  array of up to 10,000 key-value pairs to be stored, along with
                  optional expiration information. Existing values and
                  expirations will be overwritten. If neither `expiration` nor
                  `expiration_ttl` is specified, the key-value pair will never
                  expire. If both are set, `expiration_ttl` is used and
                  `expiration` is ignored. The entire request size must be 100
                  megabytes or less.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/keys:
              get:
                tags:
                  - Workers KV Namespace
                summary: List a Namespace's Keys
                description: Lists a namespace's keys.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/metadata/{key_name}:
              get:
                tags:
                  - Workers KV Namespace
                summary: Read the metadata for a key
                description: >-
                  Returns the metadata associated with the given key in the
                  given namespace. Use URL-encoding to use special characters
                  (for example, `:`, `!`, `%`) in the key name.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/values/{key_name}:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Delete key-value pair
                description: >-
                  Remove a KV pair from the namespace. Use URL-encoding to use
                  special characters (for example, `:`, `!`, `%`) in the key
                  name.
              get:
                tags:
                  - Workers KV Namespace
                summary: Read key-value pair
                description: >-
                  Returns the value associated with the given key in the given
                  namespace. Use URL-encoding to use special characters (for
                  example, `:`, `!`, `%`) in the key name. If the KV-pair is set
                  to expire at some point, the expiration time as measured in
                  seconds since the UNIX epoch will be returned in the
                  `expiration` response header.
              put:
                tags:
                  - Workers KV Namespace
                summary: Write key-value pair with metadata
                description: >-
                  Write a value identified by a key. Use URL-encoding to use
                  special characters (for example, `:`, `!`, `%`) in the key
                  name. Body should be the value to be stored along with JSON
                  metadata to be associated with the key/value pair. Existing
                  values, expirations, and metadata will be overwritten. If
                  neither `expiration` nor `expiration_ttl` is specified, the
                  key-value pair will never expire. If both are set,
                  `expiration_ttl` is used and `expiration` is ignored.
            /accounts/{account_id}/stream:
              get:
                tags:
                  - Stream Videos
                summary: List videos
                description: >-
                  Lists up to 1000 videos from a single request. For a specific
                  range, refer to the optional parameters.
              post:
                tags:
                  - Stream Videos
                summary: Initiate video uploads using TUS
                description: >-
                  Initiates a video upload using the TUS protocol. On success,
                  the server responds with a status code 201 (created) and
                  includes a `location` header to indicate where the content
                  should be uploaded. Refer to https://tus.io for protocol
                  details.
            /accounts/{account_id}/stream/{identifier}:
              delete:
                tags:
                  - Stream Videos
                summary: Delete video
                description: Deletes a video and its copies from Cloudflare Stream.
              get:
                tags:
                  - Stream Videos
                summary: Retrieve video details
                description: Fetches details for a single video.
              post:
                tags:
                  - Stream Videos
                summary: Edit video details
                description: Edit details for a single video.
            /accounts/{account_id}/stream/{identifier}/audio:
              get:
                tags:
                  - Stream Audio Tracks
                summary: List additional audio tracks on a video
                description: >-
                  Lists additional audio tracks on a video. Note this API will
                  not return information for audio attached to the video upload.
            /accounts/{account_id}/stream/{identifier}/audio/{audio_identifier}:
              delete:
                tags:
                  - Stream Audio Tracks
                summary: Delete additional audio tracks on a video
                description: >-
                  Deletes additional audio tracks on a video. Deleting a default
                  audio track is not allowed. You must assign another audio
                  track as default prior to deletion.
              patch:
                tags:
                  - Stream Audio Tracks
                summary: Edit additional audio tracks on a video
                description: >-
                  Edits additional audio tracks on a video. Editing the default
                  status of an audio track to `true` will mark all other audio
                  tracks on the video default status to `false`.
            /accounts/{account_id}/stream/{identifier}/audio/copy:
              post:
                tags:
                  - Stream Audio Tracks
                summary: Add audio tracks to a video
                description: >-
                  Adds an additional audio track to a video using the provided
                  audio track URL.
            /accounts/{account_id}/stream/{identifier}/captions:
              get:
                tags:
                  - Stream Subtitles/Captions
                summary: List captions or subtitles
                description: >-
                  Lists the available captions or subtitles for a specific
                  video.
            /accounts/{account_id}/stream/{identifier}/captions/{language}:
              delete:
                tags:
                  - Stream Subtitles/Captions
                summary: Delete captions or subtitles
                description: Removes the captions or subtitles from a video.
              put:
                tags:
                  - Stream Subtitles/Captions
                summary: Upload captions or subtitles
                description: >-
                  Uploads the caption or subtitle file to the endpoint for a
                  specific BCP47 language. One caption or subtitle file per
                  language is allowed.
            /accounts/{account_id}/stream/{identifier}/downloads:
              delete:
                tags:
                  - Stream MP4 Downloads
                summary: Delete downloads
                description: Delete the downloads for a video.
              get:
                tags:
                  - Stream MP4 Downloads
                summary: List downloads
                description: Lists the downloads created for a video.
              post:
                tags:
                  - Stream MP4 Downloads
                summary: Create downloads
                description: Creates a download for a video when a video is ready to view.
            /accounts/{account_id}/stream/{identifier}/embed:
              get:
                tags:
                  - Stream Videos
                summary: Retrieve embed Code HTML
                description: >-
                  Fetches an HTML code snippet to embed a video in a web page
                  delivered through Cloudflare. On success, returns an HTML
                  fragment for use on web pages to display a video. On failure,
                  returns a JSON response body.
            /accounts/{account_id}/stream/{identifier}/token:
              post:
                tags:
                  - Stream Videos
                summary: Create signed URL tokens for videos
                description: >-
                  Creates a signed URL token for a video. If a body is not
                  provided in the request, a token is created with default
                  values.
            /accounts/{account_id}/stream/clip:
              post:
                tags:
                  - Stream Video Clipping
                summary: Clip videos given a start and end time
                description: >-
                  Clips a video based on the specified start and end times
                  provided in seconds.
            /accounts/{account_id}/stream/copy:
              post:
                tags:
                  - Stream Videos
                summary: Upload videos from a URL
                description: Uploads a video to Stream from a provided URL.
            /accounts/{account_id}/stream/direct_upload:
              post:
                tags:
                  - Stream Videos
                summary: Upload videos via direct upload URLs
                description: >-
                  Creates a direct upload that allows video uploads without an
                  API key.
            /accounts/{account_id}/stream/keys:
              get:
                tags:
                  - Stream Signing Keys
                summary: List signing keys
                description: >-
                  Lists the video ID and creation date and time when a signing
                  key was created.
              post:
                tags:
                  - Stream Signing Keys
                summary: Create signing keys
                description: >-
                  Creates an RSA private key in PEM and JWK formats. Key files
                  are only displayed once after creation. Keys are created,
                  used, and deleted independently of videos, and every key can
                  sign any video.
            /accounts/{account_id}/stream/keys/{identifier}:
              delete:
                tags:
                  - Stream Signing Keys
                summary: Delete signing keys
                description: >-
                  Deletes signing keys and revokes all signed URLs generated
                  with the key.
            /accounts/{account_id}/stream/live_inputs:
              get:
                tags:
                  - Stream Live Inputs
                summary: List live inputs
                description: >-
                  Lists the live inputs created for an account. To get the
                  credentials needed to stream to a specific live input, request
                  a single live input.
              post:
                tags:
                  - Stream Live Inputs
                summary: Create a live input
                description: >-
                  Creates a live input, and returns credentials that you or your
                  users can use to stream live video to Cloudflare Stream.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}:
              delete:
                tags:
                  - Stream Live Inputs
                summary: Delete a live input
                description: >-
                  Prevents a live input from being streamed to and makes the
                  live input inaccessible to any future API calls.
              get:
                tags:
                  - Stream Live Inputs
                summary: Retrieve a live input
                description: Retrieves details of an existing live input.
              put:
                tags:
                  - Stream Live Inputs
                summary: Update a live input
                description: Updates a specified live input.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}/outputs:
              get:
                tags:
                  - Stream Live Inputs
                summary: List all outputs associated with a specified live input
                description: Retrieves all outputs associated with a specified live input.
              post:
                tags:
                  - Stream Live Inputs
                summary: Create a new output, connected to a live input
                description: >-
                  Creates a new output that can be used to simulcast or restream
                  live video to other RTMP or SRT destinations. Outputs are
                  always linked to a specific live input — one live input can
                  have many outputs.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}/outputs/{output_identifier}:
              delete:
                tags:
                  - Stream Live Inputs
                summary: Delete an output
                description: >-
                  Deletes an output and removes it from the associated live
                  input.
              put:
                tags:
                  - Stream Live Inputs
                summary: Update an output
                description: Updates the state of an output.
            /accounts/{account_id}/stream/storage-usage:
              get:
                tags:
                  - Stream Videos
                summary: Storage use
                description: Returns information about an account's storage use.
            /accounts/{account_id}/stream/watermarks:
              get:
                tags:
                  - Stream Watermark Profile
                summary: List watermark profiles
                description: Lists all watermark profiles for an account.
              post:
                tags:
                  - Stream Watermark Profile
                summary: Create watermark profiles via basic upload
                description: >-
                  Creates watermark profiles using a single `HTTP POST
                  multipart/form-data` request.
            /accounts/{account_id}/stream/watermarks/{identifier}:
              delete:
                tags:
                  - Stream Watermark Profile
                summary: Delete watermark profiles
                description: Deletes a watermark profile.
              get:
                tags:
                  - Stream Watermark Profile
                summary: Watermark profile details
                description: Retrieves details for a single watermark profile.
            /accounts/{account_id}/stream/webhook:
              delete:
                tags:
                  - Stream Webhook
                summary: Delete webhooks
                description: Deletes a webhook.
              get:
                tags:
                  - Stream Webhook
                summary: View webhooks
                description: Retrieves a list of webhooks.
              put:
                tags:
                  - Stream Webhook
                summary: Create webhooks
                description: Creates a webhook notification.
            /accounts/{account_id}/teamnet/routes:
              get:
                tags:
                  - Tunnel route
                summary: List tunnel routes
                description: Lists and filters private network routes in an account.
              post:
                tags:
                  - Tunnel route
                summary: Create a tunnel route
                description: Routes a private network through a Cloudflare Tunnel.
            /accounts/{account_id}/teamnet/routes/{route_id}:
              delete:
                tags:
                  - Tunnel route
                summary: Delete a tunnel route
                description: |
                  Deletes a private network route from an account.
              patch:
                tags:
                  - Tunnel route
                summary: Update a tunnel route
                description: >-
                  Updates an existing private network route in an account. The
                  fields that are meant to be updated should be provided in the
                  body of the request.
            /accounts/{account_id}/teamnet/routes/ip/{ip}:
              get:
                tags:
                  - Tunnel route
                summary: Get tunnel route by IP
                description: Fetches routes that contain the given IP address.
            /accounts/{account_id}/teamnet/routes/network/{ip_network_encoded}:
              delete:
                tags:
                  - Tunnel route
                summary: Delete a tunnel route (CIDR Endpoint)
                description: >
                  Deletes a private network route from an account. The CIDR in
                  `ip_network_encoded` must be written in URL-encoded format. If
                  no virtual_network_id is provided it will delete the route
                  from the default vnet. If no tun_type is provided it will
                  fetch the type from the tunnel_id or if that is missing it
                  will assume Cloudflare Tunnel as default. If tunnel_id is
                  provided it will delete the route from that tunnel, otherwise
                  it will delete the route based on the vnet and tun_type.
              patch:
                tags:
                  - Tunnel route
                summary: Update a tunnel route (CIDR Endpoint)
                description: >-
                  Updates an existing private network route in an account. The
                  CIDR in `ip_network_encoded` must be written in URL-encoded
                  format.
              post:
                tags:
                  - Tunnel route
                summary: Create a tunnel route (CIDR Endpoint)
                description: >-
                  Routes a private network through a Cloudflare Tunnel. The CIDR
                  in `ip_network_encoded` must be written in URL-encoded format.
            /accounts/{account_id}/teamnet/virtual_networks:
              get:
                tags:
                  - Tunnel Virtual Network
                summary: List virtual networks
                description: Lists and filters virtual networks in an account.
              post:
                tags:
                  - Tunnel Virtual Network
                summary: Create a virtual network
                description: Adds a new virtual network to an account.
            /accounts/{account_id}/teamnet/virtual_networks/{virtual_network_id}:
              delete:
                tags:
                  - Tunnel Virtual Network
                summary: Delete a virtual network
                description: Deletes an existing virtual network.
              patch:
                tags:
                  - Tunnel Virtual Network
                summary: Update a virtual network
                description: Updates an existing virtual network.
            /accounts/{account_id}/tunnels:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List All Tunnels
                description: Lists and filters all types of Tunnels in an account.
              post:
                tags:
                  - Argo Tunnel
                summary: Create an Argo Tunnel
                description: Creates a new Argo Tunnel in an account.
            /accounts/{account_id}/tunnels/{tunnel_id}:
              delete:
                tags:
                  - Argo Tunnel
                summary: Delete an Argo Tunnel
                description: Deletes an Argo Tunnel from an account.
              get:
                tags:
                  - Argo Tunnel
                summary: Get an Argo Tunnel
                description: Fetches a single Argo Tunnel.
            /accounts/{account_id}/tunnels/{tunnel_id}/connections:
              delete:
                tags:
                  - Argo Tunnel
                summary: Clean up Argo Tunnel connections
                description: >-
                  Removes connections that are in a disconnected or pending
                  reconnect state. We recommend running this command after
                  shutting down a tunnel.
            /accounts/{account_id}/warp_connector:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Warp Connector Tunnels
                description: Lists and filters Warp Connector Tunnels in an account.
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Create a Warp Connector Tunnel
                description: Creates a new Warp Connector Tunnel in an account.
            /accounts/{account_id}/warp_connector/{tunnel_id}:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Delete a Warp Connector Tunnel
                description: Deletes a Warp Connector Tunnel from an account.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Warp Connector Tunnel
                description: Fetches a single Warp Connector Tunnel.
              patch:
                tags:
                  - Cloudflare Tunnel
                summary: Update a Warp Connector Tunnel
                description: Updates an existing Warp Connector Tunnel.
            /accounts/{account_id}/warp_connector/{tunnel_id}/token:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Warp Connector Tunnel token
                description: >-
                  Gets the token used to associate warp device with a specific
                  Warp Connector tunnel.
            /accounts/{account_id}/workers/account-settings:
              get:
                tags:
                  - Worker Account Settings
                summary: Fetch Worker Account Settings
                description: Fetches Worker account settings for an account.
              put:
                tags:
                  - Worker Account Settings
                summary: Create Worker Account Settings
                description: Creates Worker account settings for an account.
            /accounts/{account_id}/workers/deployments/by-script/{script_id}:
              get:
                tags:
                  - Worker Deployments
                summary: List Deployments
            /accounts/{account_id}/workers/deployments/by-script/{script_id}/detail/{deployment_id}:
              get:
                tags:
                  - Worker Deployments
                summary: Get Deployment Detail
            /accounts/{account_id}/workers/dispatch/namespaces:
              get:
                tags:
                  - Workers for Platforms
                summary: List dispatch namespaces
                description: Fetch a list of Workers for Platforms namespaces.
              post:
                tags:
                  - Workers for Platforms
                summary: Create dispatch namespace
                description: Create a new Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}:
              delete:
                tags:
                  - Workers for Platforms
                summary: Delete dispatch namespace
                description: Delete a Workers for Platforms namespace.
              get:
                tags:
                  - Workers for Platforms
                summary: Fetch dispatch namespace
                description: Fetch a Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}:
              delete:
                tags:
                  - Workers for Platforms
                summary: Delete Worker (Workers for Platforms)
                description: >-
                  Delete a worker from a Workers for Platforms namespace. This
                  call has no response body on a successful delete.
              get:
                tags:
                  - Workers for Platforms
                summary: Worker Details (Workers for Platforms)
                description: >-
                  Fetch information about a script uploaded to a Workers for
                  Platforms namespace.
              put:
                tags:
                  - Workers for Platforms
                summary: Upload Worker Module (Workers for Platforms)
                description: Upload a worker module to a Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/bindings:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Bindings (Workers for Platforms)
                description: >-
                  Fetch script bindings from a script uploaded to a Workers for
                  Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/content:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Content (Workers for Platforms)
                description: >-
                  Fetch script content from a script uploaded to a Workers for
                  Platforms namespace.
              put:
                tags:
                  - Workers for Platforms
                summary: Put Script Content (Workers for Platforms)
                description: >-
                  Put script content for a script uploaded to a Workers for
                  Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/settings:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Settings
                description: >-
                  Get script settings from a script uploaded to a Workers for
                  Platforms namespace.
              patch:
                tags:
                  - Workers for Platforms
                summary: Patch Script Settings
                description: Patch script metadata, such as bindings
            /accounts/{account_id}/workers/domains:
              get:
                tags:
                  - Worker Domain
                summary: List Domains
                description: Lists all Worker Domains for an account.
              put:
                tags:
                  - Worker Domain
                summary: Attach to Domain
                description: Attaches a Worker to a zone and hostname.
            /accounts/{account_id}/workers/domains/{domain_id}:
              delete:
                tags:
                  - Worker Domain
                summary: Detach from Domain
                description: Detaches a Worker from a zone and hostname.
              get:
                tags:
                  - Worker Domain
                summary: Get a Domain
                description: Gets a Worker domain.
            /accounts/{account_id}/workers/durable_objects/namespaces:
              get:
                tags:
                  - Durable Objects Namespace
                summary: List Namespaces
                description: Returns the Durable Object namespaces owned by an account.
            /accounts/{account_id}/workers/durable_objects/namespaces/{id}/objects:
              get:
                tags:
                  - Durable Objects Namespace
                summary: List Objects
                description: Returns the Durable Objects in a given namespace.
            /accounts/{account_id}/workers/queues:
              get:
                tags:
                  - Queue
                summary: List Queues
                description: Returns the queues owned by an account.
              post:
                tags:
                  - Queue
                summary: Create Queue
                description: Creates a new queue.
            /accounts/{account_id}/workers/queues/{name}:
              delete:
                tags:
                  - Queue
                summary: Delete Queue
                description: Deletes a queue.
              get:
                tags:
                  - Queue
                summary: Queue Details
                description: Get information about a specific queue.
              put:
                tags:
                  - Queue
                summary: Update Queue
                description: Updates a queue.
            /accounts/{account_id}/workers/queues/{name}/consumers:
              get:
                tags:
                  - Queue
                summary: List Queue Consumers
                description: Returns the consumers for a queue.
              post:
                tags:
                  - Queue
                summary: Create Queue Consumer
                description: Creates a new consumer for a queue.
            /accounts/{account_id}/workers/queues/{name}/consumers/{consumer_name}:
              delete:
                tags:
                  - Queue
                summary: Delete Queue Consumer
                description: Deletes the consumer for a queue.
              put:
                tags:
                  - Queue
                summary: Update Queue Consumer
                description: >-
                  Updates the consumer for a queue, or creates one if it does
                  not exist.
            /accounts/{account_id}/workers/scripts:
              get:
                tags:
                  - Worker Script
                summary: List Workers
                description: Fetch a list of uploaded workers.
            /accounts/{account_id}/workers/scripts/{script_name}:
              delete:
                tags:
                  - Worker Script
                summary: Delete Worker
                description: >-
                  Delete your worker. This call has no response body on a
                  successful delete.
              get:
                tags:
                  - Worker Script
                summary: Download Worker
                description: >-
                  Fetch raw script content for your worker. Note this is the
                  original script content, not JSON encoded.
              put:
                tags:
                  - Worker Script
                summary: Upload Worker Module
                description: Upload a worker module.
            /accounts/{account_id}/workers/scripts/{script_name}/content:
              put:
                tags:
                  - Worker Script
                summary: Put script content
                description: Put script content without touching config or metadata
            /accounts/{account_id}/workers/scripts/{script_name}/content/v2:
              get:
                tags:
                  - Worker Script
                summary: Get script content
                description: Fetch script content only
            /accounts/{account_id}/workers/scripts/{script_name}/schedules:
              get:
                tags:
                  - Worker Cron Trigger
                summary: Get Cron Triggers
                description: Fetches Cron Triggers for a Worker.
              put:
                tags:
                  - Worker Cron Trigger
                summary: Update Cron Triggers
                description: Updates Cron Triggers for a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/settings:
              get:
                tags:
                  - Worker Script
                summary: Get Script Settings
                description: >-
                  Get script metadata and config, such as bindings or usage
                  model
              patch:
                tags:
                  - Worker Script
                summary: Patch Script Settings
                description: >-
                  Patch script metadata or config, such as bindings or usage
                  model
            /accounts/{account_id}/workers/scripts/{script_name}/tails:
              get:
                tags:
                  - Worker Tail Logs
                summary: List Tails
                description: Get list of tails currently deployed on a Worker.
              post:
                tags:
                  - Worker Tail Logs
                summary: Start Tail
                description: Starts a tail that receives logs and exception from a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/tails/{id}:
              delete:
                tags:
                  - Worker Tail Logs
                summary: Delete Tail
                description: Deletes a tail from a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/usage-model:
              get:
                tags:
                  - Worker Script
                summary: Fetch Usage Model
                description: Fetches the Usage Model for a given Worker.
              put:
                tags:
                  - Worker Script
                summary: Update Usage Model
                description: >-
                  Updates the Usage Model for a given Worker. Requires a Workers
                  Paid subscription.
            /accounts/{account_id}/workers/services/{service_name}/environments/{environment_name}/content:
              get:
                tags:
                  - Worker Environment
                summary: Get script content
                description: Get script content from a worker with an environment
              put:
                tags:
                  - Worker Environment
                summary: Put script content
                description: Put script content from a worker with an environment
            /accounts/{account_id}/workers/services/{service_name}/environments/{environment_name}/settings:
              get:
                tags:
                  - Worker Environment
                summary: Get Script Settings
                description: Get script settings from a worker with an environment
              patch:
                tags:
                  - Worker Environment
                summary: Patch Script Settings
                description: Patch script metadata, such as bindings
            /accounts/{account_id}/workers/subdomain:
              get:
                tags:
                  - Worker Subdomain
                summary: Get Subdomain
                description: Returns a Workers subdomain for an account.
              put:
                tags:
                  - Worker Subdomain
                summary: Create Subdomain
                description: Creates a Workers subdomain for an account.
            /accounts/{account_id}/zerotrust/connectivity_settings:
              get:
                tags:
                  - Zero Trust Connectivity Settings
                summary: Get Zero Trust Connectivity Settings
                description: >-
                  Gets the Zero Trust Connectivity Settings for the given
                  account.
              patch:
                tags:
                  - Zero Trust Connectivity Settings
                summary: Updates the Zero Trust Connectivity Settings
                description: >-
                  Updates the Zero Trust Connectivity Settings for the given
                  account.
            /accounts/{account_identifier}/billing/profile:
              get:
                tags:
                  - Account Billing Profile
                summary: Billing Profile Details
                description: Gets the current billing profile for the account.
            /accounts/{account_identifier}/cloudforce-one/requests:
              post:
                tags:
                  - Request for Information (RFI)
                summary: List Requests
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}:
              delete:
                tags:
                  - Request for Information (RFI)
                summary: Delete a Request
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get a Request
              put:
                tags:
                  - Request for Information (RFI)
                summary: Update a Request
                description: >-
                  Updating a request alters the request in the Cloudforce One
                  queue. This API may be used to update any attributes of the
                  request after the initial submission. Only fields that you
                  choose to update need to be add to the request body
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message:
              post:
                tags:
                  - Request for Information (RFI)
                summary: List Request Messages
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message/{message_identifer}:
              delete:
                tags:
                  - Request for Information (RFI)
                summary: Delete a Request Message
              put:
                tags:
                  - Request for Information (RFI)
                summary: Update a Request Message
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message/new:
              post:
                tags:
                  - Request for Information (RFI)
                summary: Create a New Request Message
                description: >-
                  Creating a request adds the request into the Cloudforce One
                  queue for analysis. In addition to the content, a short title,
                  type, priority, and releasability should be provided. If one
                  is not provided a default will be assigned.
            /accounts/{account_identifier}/cloudforce-one/requests/constants:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Priority, Status, and TLP constants
            /accounts/{account_identifier}/cloudforce-one/requests/new:
              post:
                tags:
                  - Request for Information (RFI)
                summary: Create a New Request
                description: >-
                  Creating a request adds the request into the Cloudforce One
                  queue for analysis. In addition to the content, a short title,
                  type, priority, and releasability should be provided. If one
                  is not provided a default will be assigned.
            /accounts/{account_identifier}/cloudforce-one/requests/priority:
              post:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: List Priority Intelligence Requirements
            /accounts/{account_identifier}/cloudforce-one/requests/priority/{priority_identifer}:
              delete:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Delete a Priority Intelligence Report
              get:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Get a Priority Intelligence Requirement
              put:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Update a Priority Intelligence Requirement
            /accounts/{account_identifier}/cloudforce-one/requests/priority/new:
              post:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Create a New Priority Requirement
            /accounts/{account_identifier}/cloudforce-one/requests/priority/quota:
              get:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Get Priority Intelligence Requirement Quota
            /accounts/{account_identifier}/cloudforce-one/requests/quota:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Quota
            /accounts/{account_identifier}/cloudforce-one/requests/types:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Types
            /accounts/{account_identifier}/custom_pages:
              get:
                tags:
                  - Custom pages for an account
                summary: List custom pages
                description: Fetches all the custom pages at the account level.
            /accounts/{account_identifier}/custom_pages/{identifier}:
              get:
                tags:
                  - Custom pages for an account
                summary: Get a custom page
                description: Fetches the details of a custom page.
              put:
                tags:
                  - Custom pages for an account
                summary: Update a custom page
                description: Updates the configuration of an existing custom page.
            /accounts/{account_identifier}/d1/database/{database_identifier}:
              delete:
                tags:
                  - D1
                summary: Delete D1 Database
                description: Deletes the specified D1 database.
              get:
                tags:
                  - D1
                summary: Get D1 Database
                description: Returns the specified D1 database.
            /accounts/{account_identifier}/d1/database/{database_identifier}/query:
              post:
                tags:
                  - D1
                summary: Query D1 Database
                description: Returns the query result.
            /accounts/{account_identifier}/dns_firewall/{identifier}/dns_analytics/report:
              get:
                tags:
                  - DNS Firewall Analytics
                summary: Table
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /accounts/{account_identifier}/dns_firewall/{identifier}/dns_analytics/report/bytime:
              get:
                tags:
                  - DNS Firewall Analytics
                summary: By Time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /accounts/{account_identifier}/email/routing/addresses:
              get:
                tags:
                  - Email Routing destination addresses
                summary: List destination addresses
                description: Lists existing destination addresses.
              post:
                tags:
                  - Email Routing destination addresses
                summary: Create a destination address
                description: >-
                  Create a destination address to forward your emails to.
                  Destination addresses need to be verified before they can be
                  used.
            /accounts/{account_identifier}/email/routing/addresses/{destination_address_identifier}:
              delete:
                tags:
                  - Email Routing destination addresses
                summary: Delete destination address
                description: Deletes a specific destination address.
              get:
                tags:
                  - Email Routing destination addresses
                summary: Get a destination address
                description: >-
                  Gets information for a specific destination email already
                  created.
            /accounts/{account_identifier}/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for an account
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of an account. These rules apply to
                  all the zones in the account. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - IP Access rules for an account
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for an account. The rule will
                  apply to all zones in the account.


                  Note: To create an IP Access rule that applies to a single
                  zone, refer to the [IP Access rules for a
                  zone](#ip-access-rules-for-a-zone) endpoints.
            /accounts/{account_identifier}/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for an account
                summary: Delete an IP Access rule
                description: >-
                  Deletes an existing IP Access rule defined at the account
                  level.


                  Note: This operation will affect all zones in the account.
              get:
                tags:
                  - IP Access rules for an account
                summary: Get an IP Access rule
                description: >-
                  Fetches the details of an IP Access rule defined at the
                  account level.
              patch:
                tags:
                  - IP Access rules for an account
                summary: Update an IP Access rule
                description: |-
                  Updates an IP Access rule defined at the account level.

                  Note: This operation will affect all zones in the account.
            /accounts/{account_identifier}/magic/cf_interconnects:
              get:
                tags:
                  - Magic Interconnects
                summary: List interconnects
                description: Lists interconnects associated with an account.
              put:
                tags:
                  - Magic Interconnects
                summary: Update multiple interconnects
                description: >-
                  Updates multiple interconnects associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
            /accounts/{account_identifier}/magic/cf_interconnects/{tunnel_identifier}:
              get:
                tags:
                  - Magic Interconnects
                summary: List interconnect Details
                description: Lists details for a specific interconnect.
              put:
                tags:
                  - Magic Interconnects
                summary: Update interconnect
                description: >-
                  Updates a specific interconnect associated with an account.
                  Use `?validate_only=true` as an optional query parameter to
                  only run validation without persisting changes.
            /accounts/{account_identifier}/magic/gre_tunnels:
              get:
                tags:
                  - Magic GRE tunnels
                summary: List GRE tunnels
                description: Lists GRE tunnels associated with an account.
              post:
                tags:
                  - Magic GRE tunnels
                summary: Create GRE tunnels
                description: >-
                  Creates new GRE tunnels. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
              put:
                tags:
                  - Magic GRE tunnels
                summary: Update multiple GRE tunnels
                description: >-
                  Updates multiple GRE tunnels. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
            /accounts/{account_identifier}/magic/gre_tunnels/{tunnel_identifier}:
              delete:
                tags:
                  - Magic GRE tunnels
                summary: Delete GRE Tunnel
                description: >-
                  Disables and removes a specific static GRE tunnel. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
              get:
                tags:
                  - Magic GRE tunnels
                summary: List GRE Tunnel Details
                description: Lists informtion for a specific GRE tunnel.
              put:
                tags:
                  - Magic GRE tunnels
                summary: Update GRE Tunnel
                description: >-
                  Updates a specific GRE tunnel. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels:
              get:
                tags:
                  - Magic IPsec tunnels
                summary: List IPsec tunnels
                description: Lists IPsec tunnels associated with an account.
              post:
                tags:
                  - Magic IPsec tunnels
                summary: Create IPsec tunnels
                description: >-
                  Creates new IPsec tunnels associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
              put:
                tags:
                  - Magic IPsec tunnels
                summary: Update multiple IPsec tunnels
                description: >-
                  Update multiple IPsec tunnels associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels/{tunnel_identifier}:
              delete:
                tags:
                  - Magic IPsec tunnels
                summary: Delete IPsec Tunnel
                description: >-
                  Disables and removes a specific static IPsec Tunnel associated
                  with an account. Use `?validate_only=true` as an optional
                  query parameter to only run validation without persisting
                  changes.
              get:
                tags:
                  - Magic IPsec tunnels
                summary: List IPsec tunnel details
                description: Lists details for a specific IPsec tunnel.
              put:
                tags:
                  - Magic IPsec tunnels
                summary: Update IPsec Tunnel
                description: >-
                  Updates a specific IPsec tunnel associated with an account.
                  Use `?validate_only=true` as an optional query parameter to
                  only run validation without persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels/{tunnel_identifier}/psk_generate:
              post:
                tags:
                  - Magic IPsec tunnels
                summary: Generate Pre Shared Key (PSK) for IPsec tunnels
                description: >-
                  Generates a Pre Shared Key for a specific IPsec tunnel used in
                  the IKE session. Use `?validate_only=true` as an optional
                  query parameter to only run validation without persisting
                  changes. After a PSK is generated, the PSK is immediately
                  persisted to Cloudflare's edge and cannot be retrieved later.
                  Note the PSK in a safe place.
            /accounts/{account_identifier}/magic/routes:
              delete:
                tags:
                  - Magic Static Routes
                summary: Delete Many Routes
                description: Delete multiple Magic static routes.
              get:
                tags:
                  - Magic Static Routes
                summary: List Routes
                description: List all Magic static routes.
              post:
                tags:
                  - Magic Static Routes
                summary: Create Routes
                description: >-
                  Creates a new Magic static route. Use `?validate_only=true` as
                  an optional query parameter to run validation only without
                  persisting changes.
              put:
                tags:
                  - Magic Static Routes
                summary: Update Many Routes
                description: >-
                  Update multiple Magic static routes. Use `?validate_only=true`
                  as an optional query parameter to run validation only without
                  persisting changes. Only fields for a route that need to be
                  changed need be provided.
            /accounts/{account_identifier}/magic/routes/{route_identifier}:
              delete:
                tags:
                  - Magic Static Routes
                summary: Delete Route
                description: Disable and remove a specific Magic static route.
              get:
                tags:
                  - Magic Static Routes
                summary: Route Details
                description: Get a specific Magic static route.
              put:
                tags:
                  - Magic Static Routes
                summary: Update Route
                description: >-
                  Update a specific Magic static route. Use
                  `?validate_only=true` as an optional query parameter to run
                  validation only without persisting changes.
            /accounts/{account_identifier}/magic/sites:
              get:
                tags:
                  - Magic WAN Sites
                summary: List Sites
                description: >-
                  Lists Sites associated with an account. Use
                  connector_identifier query param to return sites where
                  connector_identifier matches either site.ConnectorID or
                  site.SecondaryConnectorID.
              post:
                tags:
                  - Magic WAN Sites
                summary: Create a new Site
                description: Creates a new Site
            /accounts/{account_identifier}/magic/sites/{site_identifier}:
              delete:
                tags:
                  - Magic WAN Sites
                summary: Delete Site
                description: Remove a specific Site.
              get:
                tags:
                  - Magic WAN Sites
                summary: Site Details
                description: Get a specific Site.
              put:
                tags:
                  - Magic WAN Sites
                summary: Update Site
                description: Update a specific Site.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/acls:
              get:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: List Site ACLs
                description: Lists Site ACLs associated with an account.
              post:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Create a new Site ACL
                description: Creates a new Site ACL.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/acls/{acl_identifier}:
              delete:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Delete Site ACL
                description: Remove a specific Site ACL.
              get:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Site ACL Details
                description: Get a specific Site ACL.
              put:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Update Site ACL
                description: Update a specific Site ACL.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/lans:
              get:
                tags:
                  - Magic WAN Connector LANs
                summary: List LANs
                description: Lists LANs associated with an account and site.
              post:
                tags:
                  - Magic WAN Connector LANs
                summary: Create a new LAN
                description: >-
                  Creates a new LAN. If the site is in high availability mode,
                  static_addressing is required along with secondary and virtual
                  address.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/lans/{lan_identifier}:
              delete:
                tags:
                  - Magic WAN Connector LANs
                summary: Delete LAN
                description: Remove a specific LAN.
              get:
                tags:
                  - Magic WAN Connector LANs
                summary: LAN Details
                description: Get a specific LAN.
              put:
                tags:
                  - Magic WAN Connector LANs
                summary: Update LAN
                description: Update a specific LAN.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/wans:
              get:
                tags:
                  - Magic WAN Connector WANs
                summary: List WANs
                description: Lists WANs associated with an account and site.
              post:
                tags:
                  - Magic WAN Connector WANs
                summary: Create a new WAN
                description: Creates a new WAN.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/wans/{wan_identifier}:
              delete:
                tags:
                  - Magic WAN Connector WANs
                summary: Delete WAN
                description: Remove a specific WAN.
              get:
                tags:
                  - Magic WAN Connector WANs
                summary: WAN Details
                description: Get a specific WAN.
              put:
                tags:
                  - Magic WAN Connector WANs
                summary: Update WAN
                description: Update a specific WAN.
            /accounts/{account_identifier}/mnm/config:
              delete:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Delete account configuration
                description: Delete an existing network monitoring configuration.
              get:
                tags:
                  - Magic Network Monitoring Configuration
                summary: List account configuration
                description: Lists default sampling and router IPs for account.
              patch:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Update account configuration fields
                description: Update fields in an existing network monitoring configuration.
              post:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Create account configuration
                description: Create a new network monitoring configuration.
              put:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Update an entire account configuration
                description: >-
                  Update an existing network monitoring configuration, requires
                  the entire configuration to be updated at once.
            /accounts/{account_identifier}/mnm/config/full:
              get:
                tags:
                  - Magic Network Monitoring Configuration
                summary: List rules and account configuration
                description: Lists default sampling, router IPs, and rules for account.
            /accounts/{account_identifier}/mnm/rules:
              get:
                tags:
                  - Magic Network Monitoring Rules
                summary: List rules
                description: Lists network monitoring rules for account.
              post:
                tags:
                  - Magic Network Monitoring Rules
                summary: Create rules
                description: >-
                  Create network monitoring rules for account. Currently only
                  supports creating a single rule per API request.
              put:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update rules
                description: Update network monitoring rules for account.
            /accounts/{account_identifier}/mnm/rules/{rule_identifier}:
              delete:
                tags:
                  - Magic Network Monitoring Rules
                summary: Delete rule
                description: Delete a network monitoring rule for account.
              get:
                tags:
                  - Magic Network Monitoring Rules
                summary: Get rule
                description: List a single network monitoring rule for account.
              patch:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update rule
                description: Update a network monitoring rule for account.
            /accounts/{account_identifier}/mnm/rules/{rule_identifier}/advertisement:
              patch:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update advertisement for rule
                description: Update advertisement for rule.
            /accounts/{account_identifier}/request-tracer/trace:
              post:
                tags:
                  - Account Request Tracer
                summary: Request Trace
            /accounts/{account_identifier}/rules/lists/{list_id}/items/{item_id}:
              get:
                tags:
                  - Lists
                summary: Get a list item
                description: Fetches a list item in the list.
            /accounts/{account_identifier}/rules/lists/bulk_operations/{operation_id}:
              get:
                tags:
                  - Lists
                summary: Get bulk operation status
                description: >-
                  Gets the current status of an asynchronous operation on a
                  list.


                  The `status` property can have one of the following values:
                  `pending`, `running`, `completed`, or `failed`. If the status
                  is `failed`, the `error` property will contain a message
                  describing the error.
            /accounts/{account_identifier}/subscriptions:
              get:
                tags:
                  - Account Subscriptions
                summary: List Subscriptions
                description: Lists all of an account's subscriptions.
              post:
                tags:
                  - Account Subscriptions
                summary: Create Subscription
                description: Creates an account subscription.
            /accounts/{account_identifier}/subscriptions/{subscription_identifier}:
              delete:
                tags:
                  - Account Subscriptions
                summary: Delete Subscription
                description: Deletes an account's subscription.
              put:
                tags:
                  - Account Subscriptions
                summary: Update Subscription
                description: Updates an account subscription.
            /accounts/{account_identifier}/vectorize/indexes:
              get:
                tags:
                  - VectorizeIndex
                summary: List Vectorize Indexes
                description: Returns a list of Vectorize Indexes
              post:
                tags:
                  - VectorizeIndex
                summary: Create Vectorize Index
                description: Creates and returns a new Vectorize Index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}:
              delete:
                tags:
                  - VectorizeIndex
                summary: Delete Vectorize Index
                description: Deletes the specified Vectorize Index.
              get:
                tags:
                  - VectorizeIndex
                summary: Get Vectorize Index
                description: Returns the specified Vectorize Index.
              put:
                tags:
                  - VectorizeIndex
                summary: Update Vectorize Index
                description: Updates and returns the specified Vectorize Index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/delete-by-ids:
              post:
                tags:
                  - VectorizeIndex
                summary: Delete Vectors By Identifier
                description: >-
                  Delete a set of vectors from an index by their vector
                  identifiers.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/get-by-ids:
              post:
                tags:
                  - VectorizeIndex
                summary: Get Vectors By Identifier
                description: >-
                  Get a set of vectors from an index by their vector
                  identifiers.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/insert:
              post:
                tags:
                  - VectorizeIndex
                summary: Insert Vectors
                description: >-
                  Inserts vectors into the specified index and returns the count
                  of the vectors successfully inserted.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/query:
              post:
                tags:
                  - VectorizeIndex
                summary: Query Vectors
                description: Finds vectors closest to a given vector in an index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/upsert:
              post:
                tags:
                  - VectorizeIndex
                summary: Upsert Vectors
                description: >-
                  Upserts vectors into the specified index, creating them if
                  they do not exist and returns the count of values and ids
                  successfully inserted.
            /accounts/{accountId}/urlscanner/scan:
              get:
                tags:
                  - URL Scanner
                summary: Search URL scans
                description: >-
                  Search scans by date and webpages' requests, including full
                  URL (after redirects), hostname, and path. <br/> A successful
                  scan will appear in search results a few minutes after
                  finishing but may take much longer if the system in under
                  load. By default, only successfully completed scans will
                  appear in search results, unless searching by `scanId`. Please
                  take into account that older scans may be removed from the
                  search index at an unspecified time.
              post:
                tags:
                  - URL Scanner
                summary: Create URL Scan
                description: >-
                  Submit a URL to scan. You can also set some options, like the
                  visibility level and custom headers. Accounts are limited to 1
                  new scan every 10 seconds and 8000 per month. If you need
                  more, please reach out.
            /accounts/{accountId}/urlscanner/scan/{scanId}:
              get:
                tags:
                  - URL Scanner
                summary: Get URL scan
                description: Get URL scan by uuid
            /accounts/{accountId}/urlscanner/scan/{scanId}/har:
              get:
                tags:
                  - URL Scanner
                summary: Get URL scan's HAR
                description: >-
                  Get a URL scan's HAR file. See HAR spec at
                  http://www.softwareishard.com/blog/har-12-spec/.
            /accounts/{accountId}/urlscanner/scan/{scanId}/screenshot:
              get:
                tags:
                  - URL Scanner
                summary: Get screenshot
                description: Get scan's screenshot by resolution (desktop/mobile/tablet).
            /accounts/{identifier}/access/apps:
              get:
                tags:
                  - Access applications
                summary: List Access applications
                description: Lists all Access applications in an account.
              post:
                tags:
                  - Access applications
                summary: Add an Access Application
                description: Adds a new application to Access.
            /accounts/{identifier}/access/apps/{app_id}:
              delete:
                tags:
                  - Access applications
                summary: Delete an Access application
                description: Deletes an application from Access.
              get:
                tags:
                  - Access applications
                summary: Get an Access application
                description: Fetches information about an Access application.
              put:
                tags:
                  - Access applications
                summary: Update an Access application
                description: Updates an Access application.
            /accounts/{identifier}/access/apps/{app_id}/revoke_tokens:
              post:
                tags:
                  - Access applications
                summary: Revoke application tokens
                description: Revokes all tokens issued for an application.
            /accounts/{identifier}/access/apps/{app_id}/user_policy_checks:
              get:
                tags:
                  - Access applications
                summary: Test Access policies
                description: >-
                  Tests if a specific user has permission to access an
                  application.
            /accounts/{identifier}/access/apps/{uuid}/ca:
              delete:
                tags:
                  - Access short-lived certificate CAs
                summary: Delete a short-lived certificate CA
                description: Deletes a short-lived certificate CA.
              get:
                tags:
                  - Access short-lived certificate CAs
                summary: Get a short-lived certificate CA
                description: Fetches a short-lived certificate CA and its public key.
              post:
                tags:
                  - Access short-lived certificate CAs
                summary: Create a short-lived certificate CA
                description: Generates a new short-lived certificate CA and public key.
            /accounts/{identifier}/access/apps/{uuid}/policies:
              get:
                tags:
                  - Access policies
                summary: List Access policies
                description: Lists Access policies configured for an application.
              post:
                tags:
                  - Access policies
                summary: Create an Access policy
                description: Create a new Access policy for an application.
            /accounts/{identifier}/access/apps/{uuid1}/policies/{uuid}:
              delete:
                tags:
                  - Access policies
                summary: Delete an Access policy
                description: Delete an Access policy.
              get:
                tags:
                  - Access policies
                summary: Get an Access policy
                description: Fetches a single Access policy.
              put:
                tags:
                  - Access policies
                summary: Update an Access policy
                description: Update a configured Access policy.
            /accounts/{identifier}/access/apps/ca:
              get:
                tags:
                  - Access short-lived certificate CAs
                summary: List short-lived certificate CAs
                description: Lists short-lived certificate CAs and their public keys.
            /accounts/{identifier}/access/bookmarks:
              get:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: List Bookmark applications
                description: Lists Bookmark applications.
            /accounts/{identifier}/access/bookmarks/{uuid}:
              delete:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Delete a Bookmark application
                description: Deletes a Bookmark application.
              get:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Get a Bookmark application
                description: Fetches a single Bookmark application.
              post:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Create a Bookmark application
                description: Create a new Bookmark application.
              put:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Update a Bookmark application
                description: Updates a configured Bookmark application.
            /accounts/{identifier}/access/certificates:
              get:
                tags:
                  - Access mTLS authentication
                summary: List mTLS certificates
                description: Lists all mTLS root certificates.
              post:
                tags:
                  - Access mTLS authentication
                summary: Add an mTLS certificate
                description: Adds a new mTLS root certificate to Access.
            /accounts/{identifier}/access/certificates/{uuid}:
              delete:
                tags:
                  - Access mTLS authentication
                summary: Delete an mTLS certificate
                description: Deletes an mTLS certificate.
              get:
                tags:
                  - Access mTLS authentication
                summary: Get an mTLS certificate
                description: Fetches a single mTLS certificate.
              put:
                tags:
                  - Access mTLS authentication
                summary: Update an mTLS certificate
                description: Updates a configured mTLS certificate.
            /accounts/{identifier}/access/certificates/settings:
              get:
                tags:
                  - Access mTLS authentication
                summary: List all mTLS hostname settings
                description: List all mTLS hostname settings for this account.
              put:
                tags:
                  - Access mTLS authentication
                summary: Update an mTLS certificate's hostname settings
                description: Updates an mTLS certificate's hostname settings.
            /accounts/{identifier}/access/custom_pages:
              get:
                tags:
                  - Access custom pages
                summary: List custom pages
                description: List custom pages
              post:
                tags:
                  - Access custom pages
                summary: Create a custom page
                description: Create a custom page
            /accounts/{identifier}/access/custom_pages/{uuid}:
              delete:
                tags:
                  - Access custom pages
                summary: Delete a custom page
                description: Delete a custom page
              get:
                tags:
                  - Access custom pages
                summary: Get a custom page
                description: Fetches a custom page and also returns its HTML.
              put:
                tags:
                  - Access custom pages
                summary: Update a custom page
                description: Update a custom page
            /accounts/{identifier}/access/groups:
              get:
                tags:
                  - Access groups
                summary: List Access groups
                description: Lists all Access groups.
              post:
                tags:
                  - Access groups
                summary: Create an Access group
                description: Creates a new Access group.
            /accounts/{identifier}/access/groups/{uuid}:
              delete:
                tags:
                  - Access groups
                summary: Delete an Access group
                description: Deletes an Access group.
              get:
                tags:
                  - Access groups
                summary: Get an Access group
                description: Fetches a single Access group.
              put:
                tags:
                  - Access groups
                summary: Update an Access group
                description: Updates a configured Access group.
            /accounts/{identifier}/access/identity_providers:
              get:
                tags:
                  - Access identity providers
                summary: List Access identity providers
                description: Lists all configured identity providers.
              post:
                tags:
                  - Access identity providers
                summary: Add an Access identity provider
                description: Adds a new identity provider to Access.
            /accounts/{identifier}/access/identity_providers/{uuid}:
              delete:
                tags:
                  - Access identity providers
                summary: Delete an Access identity provider
                description: Deletes an identity provider from Access.
              get:
                tags:
                  - Access identity providers
                summary: Get an Access identity provider
                description: Fetches a configured identity provider.
              put:
                tags:
                  - Access identity providers
                summary: Update an Access identity provider
                description: Updates a configured identity provider.
            /accounts/{identifier}/access/keys:
              get:
                tags:
                  - Access key configuration
                summary: Get the Access key configuration
                description: Gets the Access key rotation settings for an account.
              put:
                tags:
                  - Access key configuration
                summary: Update the Access key configuration
                description: Updates the Access key rotation settings for an account.
            /accounts/{identifier}/access/keys/rotate:
              post:
                tags:
                  - Access key configuration
                summary: Rotate Access keys
                description: Perfoms a key rotation for an account.
            /accounts/{identifier}/access/logs/access_requests:
              get:
                tags:
                  - Access authentication logs
                summary: Get Access authentication logs
                description: >-
                  Gets a list of Access authentication audit logs for an
                  account.
            /accounts/{identifier}/access/organizations:
              get:
                tags:
                  - Zero Trust organization
                summary: Get your Zero Trust organization
                description: Returns the configuration for your Zero Trust organization.
              post:
                tags:
                  - Zero Trust organization
                summary: Create your Zero Trust organization
                description: Sets up a Zero Trust organization for your account.
              put:
                tags:
                  - Zero Trust organization
                summary: Update your Zero Trust organization
                description: Updates the configuration for your Zero Trust organization.
            /accounts/{identifier}/access/organizations/revoke_user:
              post:
                tags:
                  - Zero Trust organization
                summary: Revoke all Access tokens for a user
                description: Revokes a user's access across all applications.
            /accounts/{identifier}/access/seats:
              patch:
                tags:
                  - Zero Trust seats
                summary: Update a user seat
                description: >-
                  Removes a user from a Zero Trust seat when both `access_seat`
                  and `gateway_seat` are set to false.
            /accounts/{identifier}/access/service_tokens:
              get:
                tags:
                  - Access service tokens
                summary: List service tokens
                description: Lists all service tokens.
              post:
                tags:
                  - Access service tokens
                summary: Create a service token
                description: >-
                  Generates a new service token. **Note:** This is the only time
                  you can get the Client Secret. If you lose the Client Secret,
                  you will have to rotate the Client Secret or create a new
                  service token.
            /accounts/{identifier}/access/service_tokens/{uuid}:
              delete:
                tags:
                  - Access service tokens
                summary: Delete a service token
                description: Deletes a service token.
              put:
                tags:
                  - Access service tokens
                summary: Update a service token
                description: Updates a configured service token.
            /accounts/{identifier}/access/service_tokens/{uuid}/refresh:
              post:
                tags:
                  - Access service tokens
                summary: Refresh a service token
                description: Refreshes the expiration of a service token.
            /accounts/{identifier}/access/service_tokens/{uuid}/rotate:
              post:
                tags:
                  - Access service tokens
                summary: Rotate a service token
                description: >-
                  Generates a new Client Secret for a service token and revokes
                  the old one.
            /accounts/{identifier}/access/tags:
              get:
                tags:
                  - Access tags
                summary: List tags
                description: List tags
              post:
                tags:
                  - Access tags
                summary: Create a tag
                description: Create a tag
            /accounts/{identifier}/access/tags/{name}:
              delete:
                tags:
                  - Access tags
                summary: Delete a tag
                description: Delete a tag
              get:
                tags:
                  - Access tags
                summary: Get a tag
                description: Get a tag
              put:
                tags:
                  - Access tags
                summary: Update a tag
                description: Update a tag
            /accounts/{identifier}/access/users:
              get:
                tags:
                  - Zero Trust users
                summary: Get users
                description: Gets a list of users for an account.
            /accounts/{identifier}/access/users/{id}/active_sessions:
              get:
                tags:
                  - Zero Trust users
                summary: Get active sessions
                description: Get active sessions for a single user.
            /accounts/{identifier}/access/users/{id}/active_sessions/{nonce}:
              get:
                tags:
                  - Zero Trust users
                summary: Get single active session
                description: Get an active session for a single user.
            /accounts/{identifier}/access/users/{id}/failed_logins:
              get:
                tags:
                  - Zero Trust users
                summary: Get failed logins
                description: Get all failed login attempts for a single user.
            /accounts/{identifier}/access/users/{id}/last_seen_identity:
              get:
                tags:
                  - Zero Trust users
                summary: Get last seen identity
                description: Get last seen identity for a single user.
            /certificates:
              get:
                tags:
                  - Origin CA
                summary: List Certificates
                description: >-
                  List all existing Origin CA certificates for a given zone. Use
                  your Origin CA Key as your User Service Key when calling this
                  endpoint ([see above](#requests)).
              post:
                tags:
                  - Origin CA
                summary: Create Certificate
                description: >-
                  Create an Origin CA certificate. Use your Origin CA Key as
                  your User Service Key when calling this endpoint ([see
                  above](#requests)).
            /certificates/{certificate_id}:
              delete:
                tags:
                  - Origin CA
                summary: Revoke Certificate
                description: >-
                  Revoke an existing Origin CA certificate by its serial number.
                  Use your Origin CA Key as your User Service Key when calling
                  this endpoint ([see above](#requests)).
              get:
                tags:
                  - Origin CA
                summary: Get Certificate
                description: >-
                  Get an existing Origin CA certificate by its serial number.
                  Use your Origin CA Key as your User Service Key when calling
                  this endpoint ([see above](#requests)).
            /ips:
              get:
                tags:
                  - Cloudflare IPs
                summary: Cloudflare/JD Cloud IP Details
                description: >-
                  Get IPs used on the Cloudflare/JD Cloud network, see
                  https://www.cloudflare.com/ips for Cloudflare IPs or
                  https://developers.cloudflare.com/china-network/reference/infrastructure/
                  for JD Cloud IPs.
            /memberships:
              get:
                tags:
                  - User's Account Memberships
                summary: List Memberships
                description: List memberships of accounts the user can access.
            /memberships/{membership_id}:
              delete:
                tags:
                  - User's Account Memberships
                summary: Delete Membership
                description: Remove the associated member from an account.
              get:
                tags:
                  - User's Account Memberships
                summary: Membership Details
                description: Get a specific membership.
              put:
                tags:
                  - User's Account Memberships
                summary: Update Membership
                description: Accept or reject this account invitation.
            /organizations/{organization_id}/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get organization audit logs
                description: >-
                  Gets a list of audit logs for an organization. Can be filtered
                  by who made the change, on which zone, and the timeframe of
                  the change.
            /radar/annotations/outages:
              get:
                tags:
                  - Radar Annotations
                summary: Get latest Internet outages and anomalies.
            /radar/annotations/outages/locations:
              get:
                tags:
                  - Radar Annotations
                summary: Get the number of outages for locations.
            /radar/as112/summary/dnssec:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNSSEC Summary
                description: >-
                  Percentage distribution of DNS queries to AS112 by DNSSEC
                  support.
            /radar/as112/summary/edns:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 EDNS Summary
                description: >-
                  Percentage distribution of DNS queries, to AS112, by EDNS
                  support.
            /radar/as112/summary/ip_version:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 IP Version Summary
                description: >-
                  Percentage distribution of DNS queries to AS112 per IP
                  Version.
            /radar/as112/summary/protocol:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Protocol Summary
                description: Percentage distribution of DNS queries to AS112 per protocol.
            /radar/as112/summary/query_type:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 Query Types Summary
                description: Percentage distribution of DNS queries to AS112 by Query Type.
            /radar/as112/summary/response_codes:
              get:
                tags:
                  - Radar AS112
                summary: Get a summary of AS112 Response Codes
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Response Codes.
            /radar/as112/timeseries:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Queries Time Series
                description: Get AS112 queries change over time.
            /radar/as112/timeseries_groups/dnssec:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNSSEC Support Time Series
                description: >-
                  Percentage distribution of DNS AS112 queries by DNSSEC support
                  over time.
            /radar/as112/timeseries_groups/edns:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 EDNS Support Summary
                description: >-
                  Percentage distribution of AS112 DNS queries by EDNS support
                  over time.
            /radar/as112/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 IP Version Time Series
                description: >-
                  Percentage distribution of AS112 DNS queries by IP Version
                  over time.
            /radar/as112/timeseries_groups/protocol:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Protocol Time Series
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Protocol over time.
            /radar/as112/timeseries_groups/query_type:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 Query Types Time Series
                description: >-
                  Percentage distribution of AS112 DNS queries by Query Type
                  over time.
            /radar/as112/timeseries_groups/response_codes:
              get:
                tags:
                  - Radar AS112
                summary: Get a time series of AS112 Response Codes
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Response Codes over time.
            /radar/as112/top/locations:
              get:
                tags:
                  - Radar AS112
                summary: Get top autonomous systems by AS112 DNS queries
                description: >-
                  Get the top locations by AS112 DNS queries. Values are a
                  percentage out of the total queries.
            /radar/as112/top/locations/dnssec/{dnssec}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations By DNS Queries DNSSEC Support
                description: Get the top locations by DNS queries DNSSEC support to AS112.
            /radar/as112/top/locations/edns/{edns}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations By EDNS Support
                description: Get the top locations, by DNS queries EDNS support to AS112.
            /radar/as112/top/locations/ip_version/{ip_version}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations by DNS Queries IP version
                description: Get the top locations by DNS queries IP version to AS112.
            /radar/attacks/layer3/summary:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks Summary
                description: >-
                  Percentage distribution of network protocols in layer 3/4
                  attacks over a given time period.
            /radar/attacks/layer3/summary/bitrate:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Bitrate Summary
                description: Percentage distribution of attacks by bitrate.
            /radar/attacks/layer3/summary/duration:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Durations Summary
                description: Percentage distribution of attacks by duration.
            /radar/attacks/layer3/summary/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get IP Versions Summary
                description: Percentage distribution of attacks by ip version used.
            /radar/attacks/layer3/summary/protocol:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Protocols Summary
                description: Percentage distribution of attacks by protocol used.
            /radar/attacks/layer3/summary/vector:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Vector Summary
                description: Percentage distribution of attacks by vector.
            /radar/attacks/layer3/timeseries:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attacks By Bytes Summary
                description: Get attacks change over time by bytes.
            /radar/attacks/layer3/timeseries_groups:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Network Protocol Time Series
                description: >-
                  Get a timeseries of the percentage distribution of network
                  protocols in Layer 3/4 attacks.
            /radar/attacks/layer3/timeseries_groups/bitrate:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attacks By Bitrate Time Series
                description: Percentage distribution of attacks by bitrate over time.
            /radar/attacks/layer3/timeseries_groups/duration:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attack By Duration Time Series
                description: Percentage distribution of attacks by duration over time.
            /radar/attacks/layer3/timeseries_groups/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Target Industries Time Series
                description: Percentage distribution of attacks by industry used over time.
            /radar/attacks/layer3/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By IP Version Time Series
                description: >-
                  Percentage distribution of attacks by ip version used over
                  time.
            /radar/attacks/layer3/timeseries_groups/protocol:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Protocol Timeseries
                description: Percentage distribution of attacks by protocol used over time.
            /radar/attacks/layer3/timeseries_groups/vector:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Vector
                description: Percentage distribution of attacks by vector used over time.
            /radar/attacks/layer3/timeseries_groups/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Vertical Time Series
                description: Percentage distribution of attacks by vertical used over time.
            /radar/attacks/layer3/top/attacks:
              get:
                tags:
                  - Radar Attacks
                summary: >-
                  Get top attack pairs (origin and target locations) of Layer 3
                  attacks
                description: >-
                  Get the top attacks from origin to target location. Values are
                  a percentage out of the total layer 3 attacks (with billing
                  country). You can optionally limit the number of attacks per
                  origin/target location (useful if all the top attacks are from
                  or to the same location).
            /radar/attacks/layer3/top/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Industry of attack
                description: Get the Industry of attacks.
            /radar/attacks/layer3/top/locations/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get top origin locations of attack
                description: Get the origin locations of attacks.
            /radar/attacks/layer3/top/locations/target:
              get:
                tags:
                  - Radar Attacks
                summary: Get top target locations of attack
                description: Get the target locations of attacks.
            /radar/attacks/layer3/top/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Verticals of attack
                description: Get the Verticals of attacks.
            /radar/attacks/layer7/summary:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks Summary
                description: >-
                  Percentage distribution of mitigation techniques in Layer 7
                  attacks.
            /radar/attacks/layer7/summary/http_method:
              get:
                tags:
                  - Radar Attacks
                summary: Get HTTP Method Summary
                description: Percentage distribution of attacks by http method used.
            /radar/attacks/layer7/summary/http_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get HTTP Version Summary
                description: Percentage distribution of attacks by http version used.
            /radar/attacks/layer7/summary/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Ip Version Summary
                description: Percentage distribution of attacks by ip version used.
            /radar/attacks/layer7/summary/managed_rules:
              get:
                tags:
                  - Radar Attacks
                summary: Get Managed Rules Summary
                description: Percentage distribution of attacks by managed rules used.
            /radar/attacks/layer7/summary/mitigation_product:
              get:
                tags:
                  - Radar Attacks
                summary: Get Mitigation Product Summary
                description: Percentage distribution of attacks by mitigation product used.
            /radar/attacks/layer7/timeseries:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks Time Series
                description: >-
                  Get a timeseries of Layer 7 attacks. Values represent HTTP
                  requests and are normalized using min-max by default.
            /radar/attacks/layer7/timeseries_groups:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Mitigation Technique Time Series
                description: >-
                  Get a time series of the percentual distribution of mitigation
                  techniques, over time.
            /radar/attacks/layer7/timeseries_groups/http_method:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By HTTP Method Time Series
                description: >-
                  Percentage distribution of attacks by http method used over
                  time.
            /radar/attacks/layer7/timeseries_groups/http_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By HTTP Version Time Series
                description: >-
                  Percentage distribution of attacks by http version used over
                  time.
            /radar/attacks/layer7/timeseries_groups/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Target Industries Time Series
                description: Percentage distribution of attacks by industry used over time.
            /radar/attacks/layer7/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By IP Version Time Series
                description: >-
                  Percentage distribution of attacks by ip version used over
                  time.
            /radar/attacks/layer7/timeseries_groups/managed_rules:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Managed Rules Time Series
                description: >-
                  Percentage distribution of attacks by managed rules used over
                  time.
            /radar/attacks/layer7/timeseries_groups/mitigation_product:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Mitigation Product Time Series
                description: >-
                  Percentage distribution of attacks by mitigation product used
                  over time.
            /radar/attacks/layer7/timeseries_groups/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Vertical Time Series
                description: Percentage distribution of attacks by vertical used over time.
            /radar/attacks/layer7/top/ases/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get Top Origin Autonomous Systems By Layer 7 Attacks
                description: >-
                  Get the top origin Autonomous Systems of and by layer 7
                  attacks. Values are a percentage out of the total layer 7
                  attacks. The origin Autonomous Systems is determined by the
                  client IP.
            /radar/attacks/layer7/top/attacks:
              get:
                tags:
                  - Radar Attacks
                summary: >-
                  Get Top Attack Pairs (origin and target locations) By Layer 7
                  Attacks
                description: >-
                  Get the top attacks from origin to target location. Values are
                  a percentage out of the total layer 7 attacks (with billing
                  country). The attack magnitude can be defined by the number of
                  mitigated requests or by the number of zones affected. You can
                  optionally limit the number of attacks per origin/target
                  location (useful if all the top attacks are from or to the
                  same location).
            /radar/attacks/layer7/top/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Industry of attack
                description: Get the Industry of attacks.
            /radar/attacks/layer7/top/locations/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get Top Origin Locations By Layer 7 Attacks
                description: >-
                  Get the top origin locations of and by layer 7 attacks. Values
                  are a percentage out of the total layer 7 attacks. The origin
                  location is determined by the client IP.
            /radar/attacks/layer7/top/locations/target:
              get:
                tags:
                  - Radar Attacks
                summary: Get layer 7 top target locations
                description: >-
                  Get the top target locations of and by layer 7 attacks. Values
                  are a percentage out of the total layer 7 attacks. The target
                  location is determined by the attacked zone's billing country,
                  when available.
            /radar/attacks/layer7/top/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Verticals of attack
                description: Get the Verticals of attacks.
            /radar/bgp/hijacks/events:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP hijack events
                description: Get the BGP hijack events. (Beta)
            /radar/bgp/leaks/events:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP route leak events
                description: Get the BGP route leak events (Beta).
            /radar/bgp/routes/moas:
              get:
                tags:
                  - Radar BGP
                summary: Get MOASes
                description: >-
                  List all Multi-origin AS (MOAS) prefixes on the global routing
                  tables.
            /radar/bgp/routes/pfx2as:
              get:
                tags:
                  - Radar BGP
                summary: Get prefix-to-origin mapping
                description: Lookup prefix-to-origin mapping on global routing tables.
            /radar/bgp/routes/stats:
              get:
                tags:
                  - Radar BGP
                summary: 'Get BGP routing table stats '
                description: Get the BGP routing table stats (Beta).
            /radar/bgp/routes/timeseries:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP IP space time series
                description: >-
                  Gets time-series data for the announced IP space count,
                  represented as the number of IPv4 /24s and IPv6 /48s, for a
                  given ASN.
            /radar/bgp/timeseries:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP time series
                description: >-
                  Gets BGP updates change over time. Raw values are returned.
                  When requesting updates of an autonomous system (AS), only BGP
                  updates of type announcement are returned.
            /radar/bgp/top/ases:
              get:
                tags:
                  - Radar BGP
                summary: Get top autonomous systems
                description: >-
                  Get the top autonomous systems (AS) by BGP updates
                  (announcements only). Values are a percentage out of the total
                  updates.
            /radar/bgp/top/ases/prefixes:
              get:
                tags:
                  - Radar BGP
                summary: Get list of ASNs ordered by prefix count
                description: >-
                  Get the full list of autonomous systems on the global routing
                  table ordered by announced prefixes count. The data comes from
                  public BGP MRT data archives and updates every 2 hours.
            /radar/bgp/top/prefixes:
              get:
                tags:
                  - Radar BGP
                summary: Get top prefixes
                description: >-
                  Get the top network prefixes by BGP updates. Values are a
                  percentage out of the total BGP updates.
            /radar/connection_tampering/summary:
              get:
                tags:
                  - Radar Connection Tampering
                summary: Get Connection Tampering Summary
                description: >-
                  Distribution of connection tampering types over a given time
                  period.
            /radar/connection_tampering/timeseries_groups:
              get:
                tags:
                  - Radar Connection Tampering
                summary: Get Connection Tampering Time Series
                description: Distribution of connection tampering types over time.
            /radar/datasets:
              get:
                tags:
                  - Radar Datasets
                summary: Get Datasets
                description: Get a list of datasets.
            /radar/datasets/{alias}:
              get:
                tags:
                  - Radar Datasets
                summary: Get Dataset csv Stream
                description: >-
                  Get the csv content of a given dataset by alias or id. When
                  getting the content by alias the latest dataset is returned,
                  optionally filtered by the latest available at a given date.
            /radar/datasets/download:
              post:
                tags:
                  - Radar Datasets
                summary: Get Dataset download url
                description: Get a url to download a single dataset.
            /radar/dns/top/ases:
              get:
                tags:
                  - Radar DNS
                summary: Get Top Autonomous Systems by DNS queries.
                description: >-
                  Get top autonomous systems by DNS queries made to Cloudflare's
                  public DNS resolver.
            /radar/dns/top/locations:
              get:
                tags:
                  - Radar DNS
                summary: Get Top Locations by DNS queries
                description: >-
                  Get top locations by DNS queries made to Cloudflare's public
                  DNS resolver.
            /radar/email/routing/summary/arc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get ARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per ARC
                  validation.
            /radar/email/routing/summary/dkim:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DKIM Validations Summary
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation.
            /radar/email/routing/summary/dmarc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DMARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation.
            /radar/email/routing/summary/encrypted:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Encrypted Summary
                description: Percentage distribution of emails by Encrypted
            /radar/email/routing/summary/ip_version:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Ip Version Summary
                description: Percentage distribution of emails by Ip Version.
            /radar/email/routing/summary/spf:
              get:
                tags:
                  - Radar Email Routing
                summary: Get SPF Validations Summary
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation.
            /radar/email/routing/timeseries_groups/arc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get ARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per Arc
                  validation over time.
            /radar/email/routing/timeseries_groups/dkim:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DKIM Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation over time.
            /radar/email/routing/timeseries_groups/dmarc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DMARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation over time.
            /radar/email/routing/timeseries_groups/encrypted:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Encrypted Time Series
                description: Percentage distribution of emails by Encrypted over time.
            /radar/email/routing/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Ip Version Time Series
                description: Percentage distribution of emails by Ip Version over time.
            /radar/email/routing/timeseries_groups/spf:
              get:
                tags:
                  - Radar Email Routing
                summary: Get SPF Validations Time Series
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation over time.
            /radar/email/security/summary/arc:
              get:
                tags:
                  - Radar Email Security
                summary: Get ARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per ARC
                  validation.
            /radar/email/security/summary/dkim:
              get:
                tags:
                  - Radar Email Security
                summary: Get DKIM Validations Summary
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation.
            /radar/email/security/summary/dmarc:
              get:
                tags:
                  - Radar Email Security
                summary: Get DMARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation.
            /radar/email/security/summary/malicious:
              get:
                tags:
                  - Radar Email Security
                summary: Get MALICIOUS Validations Summary
                description: Percentage distribution of emails classified as MALICIOUS.
            /radar/email/security/summary/spam:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPAM Summary
                description: >-
                  Proportion of emails categorized as either spam or legitimate
                  (non-spam).
            /radar/email/security/summary/spf:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPF Validations Summary
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation.
            /radar/email/security/summary/spoof:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPOOF Summary
                description: >-
                  Proportion of emails categorized as either spoof or legitimate
                  (non-spoof).
            /radar/email/security/summary/threat_category:
              get:
                tags:
                  - Radar Email Security
                summary: Get Threat Categories Summary
                description: >-
                  Percentage distribution of emails classified in Threat
                  Categories.
            /radar/email/security/summary/tls_version:
              get:
                tags:
                  - Radar Email Security
                summary: Get TLS Version Summary
                description: Percentage distribution of emails classified per TLS Version.
            /radar/email/security/timeseries_groups/arc:
              get:
                tags:
                  - Radar Email Security
                summary: Get ARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per Arc
                  validation over time.
            /radar/email/security/timeseries_groups/dkim:
              get:
                tags:
                  - Radar Email Security
                summary: Get DKIM Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation over time.
            /radar/email/security/timeseries_groups/dmarc:
              get:
                tags:
                  - Radar Email Security
                summary: Get DMARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation over time.
            /radar/email/security/timeseries_groups/malicious:
              get:
                tags:
                  - Radar Email Security
                summary: Get MALICIOUS Validations Time Series
                description: >-
                  Percentage distribution of emails classified as MALICIOUS over
                  time.
            /radar/email/security/timeseries_groups/spam:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPAM Validations Time Series
                description: >-
                  Percentage distribution of emails classified as SPAM over
                  time.
            /radar/email/security/timeseries_groups/spf:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPF Validations Time Series
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation over time.
            /radar/email/security/timeseries_groups/spoof:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPOOF Validations Time Series
                description: >-
                  Percentage distribution of emails classified as SPOOF over
                  time.
            /radar/email/security/timeseries_groups/threat_category:
              get:
                tags:
                  - Radar Email Security
                summary: Get Threat Categories Time Series
                description: >-
                  Percentage distribution of emails classified in Threat
                  Categories over time.
            /radar/email/security/timeseries_groups/tls_version:
              get:
                tags:
                  - Radar Email Security
                summary: Get TLS Version Time Series
                description: >-
                  Percentage distribution of emails classified per TLS Version
                  over time.
            /radar/email/security/top/tlds:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Email Messages
                description: >-
                  Get the top TLDs by email messages. Values are a percentage
                  out of the total emails.
            /radar/email/security/top/tlds/malicious/{malicious}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Malicious Classification
                description: Get the TLDs by emails classified as malicious or not.
            /radar/email/security/top/tlds/spam/{spam}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Spam Classification
                description: Get the top TLDs by emails classified as Spam or not.
            /radar/email/security/top/tlds/spoof/{spoof}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Spoof Classification
                description: Get the TLDs by emails classified as spoof or not.
            /radar/entities/asns:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous systems
                description: Gets a list of autonomous systems (AS).
            /radar/entities/asns/{asn}:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous system information by AS number
                description: >-
                  Get the requested autonomous system information. A confidence
                  level below `5` indicates a low level of confidence in the
                  traffic data - normally this happens because Cloudflare has a
                  small amount of traffic from/to this AS). Population estimates
                  come from APNIC (refer to https://labs.apnic.net/?p=526).
            /radar/entities/asns/{asn}/rel:
              get:
                tags:
                  - Radar Entities
                summary: Get AS-level relationships by AS number
                description: Get AS-level relationship for given networks.
            /radar/entities/asns/ip:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous system information by IP address
                description: >-
                  Get the requested autonomous system information based on IP
                  address. Population estimates come from APNIC (refer to
                  https://labs.apnic.net/?p=526).
            /radar/entities/ip:
              get:
                tags:
                  - Radar Entities
                summary: Get IP address
                description: 'Get IP address information. '
            /radar/entities/locations:
              get:
                tags:
                  - Radar Entities
                summary: Get locations
                description: Get a list of locations.
            /radar/entities/locations/{location}:
              get:
                tags:
                  - Radar Entities
                summary: Get location
                description: >-
                  Get the requested location information. A confidence level
                  below `5` indicates a low level of confidence in the traffic
                  data - normally this happens because Cloudflare has a small
                  amount of traffic from/to this location).
            /radar/http/summary/bot_class:
              get:
                tags:
                  - Radar Http
                summary: Get Bot Class Summary
                description: >-
                  Percentage distribution of bot-generated traffic to genuine
                  human traffic, as classified by Cloudflare. Visit
                  https://developers.cloudflare.com/radar/concepts/bot-classes/
                  for more information.
            /radar/http/summary/device_type:
              get:
                tags:
                  - Radar Http
                summary: Get Device Type Summary
                description: >-
                  Percentage of Internet traffic generated by mobile, desktop,
                  and other types of devices, over a given time period.
            /radar/http/summary/http_protocol:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP protocols summary
                description: >-
                  Percentage distribution of traffic per HTTP protocol over a
                  given time period.
            /radar/http/summary/http_version:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP Versions Summary
                description: >-
                  Percentage distribution of traffic per HTTP protocol version
                  over a given time period.
            /radar/http/summary/ip_version:
              get:
                tags:
                  - Radar Http
                summary: Get IP Version Summary
                description: >-
                  Percentage distribution of Internet traffic based on IP
                  protocol versions, such as IPv4 and IPv6, over a given time
                  period.
            /radar/http/summary/os:
              get:
                tags:
                  - Radar Http
                summary: Get Operating Systems Summary
                description: >-
                  Percentage distribution of Internet traffic generated by
                  different operating systems like Windows, macOS, Android, iOS,
                  and others, over a given time period.
            /radar/http/summary/tls_version:
              get:
                tags:
                  - Radar Http
                summary: Get TLS Versions Summary
                description: >-
                  Percentage distribution of traffic per TLS protocol version,
                  over a given time period.
            /radar/http/timeseries_groups/bot_class:
              get:
                tags:
                  - Radar Http
                summary: Get Bot Classes Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  classified as automated or human. Visit
                  https://developers.cloudflare.com/radar/concepts/bot-classes/
                  for more information.
            /radar/http/timeseries_groups/browser:
              get:
                tags:
                  - Radar Http
                summary: Get User Agents Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top user agents.
            /radar/http/timeseries_groups/browser_family:
              get:
                tags:
                  - Radar Http
                summary: Get User Agent Families Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top user agents aggregated in families.
            /radar/http/timeseries_groups/device_type:
              get:
                tags:
                  - Radar Http
                summary: Get Device Types Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per device type.
            /radar/http/timeseries_groups/http_protocol:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP protocols Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per HTTP protocol.
            /radar/http/timeseries_groups/http_version:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per HTTP protocol version.
            /radar/http/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Http
                summary: Get IP Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per IP protocol version.
            /radar/http/timeseries_groups/os:
              get:
                tags:
                  - Radar Http
                summary: Get Operating Systems Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top operating systems.
            /radar/http/timeseries_groups/tls_version:
              get:
                tags:
                  - Radar Http
                summary: Get TLS Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per TLS protocol version.
            /radar/http/top/ases:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Requests
                description: >-
                  Get the top autonomous systems by HTTP traffic. Values are a
                  percentage out of the total traffic.
            /radar/http/top/ases/bot_class/{bot_class}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Bot Class
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested bot class. These two categories use Cloudflare's bot
                  score - refer to [Bot
                  Scores](https://developers.cloudflare.com/bots/concepts/bot-score)
                  for more information. Values are a percentage out of the total
                  traffic.
            /radar/http/top/ases/device_type/{device_type}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Device Type
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested device type. Values are a percentage out of the
                  total traffic.
            /radar/http/top/ases/http_protocol/{http_protocol}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Protocol
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested HTTP protocol. Values are a percentage out of the
                  total traffic.
            /radar/http/top/ases/http_version/{http_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Version
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested HTTP protocol version. Values are a percentage out
                  of the total traffic.
            /radar/http/top/ases/ip_version/{ip_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By IP Version
                description: >-
                  Get the top autonomous systems, by HTTP traffic, of the
                  requested IP protocol version. Values are a percentage out of
                  the total traffic.
            /radar/http/top/ases/os/{os}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Operating System
                description: >-
                  Get the top autonomous systems, by HTTP traffic, of the
                  requested operating systems. Values are a percentage out of
                  the total traffic.
            /radar/http/top/ases/tls_version/{tls_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By TLS Version
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested TLS protocol version. Values are a percentage out of
                  the total traffic.
            /radar/http/top/browser_families:
              get:
                tags:
                  - Radar Http
                summary: Get Top User Agents Families by HTTP requests
                description: >-
                  Get the top user agents aggregated in families by HTTP
                  traffic. Values are a percentage out of the total traffic.
            /radar/http/top/browsers:
              get:
                tags:
                  - Radar Http
                summary: Get Top User Agents By HTTP requests
                description: >-
                  Get the top user agents by HTTP traffic. Values are a
                  percentage out of the total traffic.
            /radar/http/top/locations:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP requests
                description: >-
                  Get the top locations by HTTP traffic. Values are a percentage
                  out of the total traffic.
            /radar/http/top/locations/bot_class/{bot_class}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Bot Class
                description: >-
                  Get the top locations, by HTTP traffic, of the requested bot
                  class. These two categories use Cloudflare's bot score - refer
                  to [Bot
                  scores])https://developers.cloudflare.com/bots/concepts/bot-score).
                  Values are a percentage out of the total traffic.
            /radar/http/top/locations/device_type/{device_type}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Device Type
                description: >-
                  Get the top locations, by HTTP traffic, of the requested
                  device type. Values are a percentage out of the total traffic.
            /radar/http/top/locations/http_protocol/{http_protocol}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP Protocol
                description: >-
                  Get the top locations, by HTTP traffic, of the requested HTTP
                  protocol. Values are a percentage out of the total traffic.
            /radar/http/top/locations/http_version/{http_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested HTTP
                  protocol. Values are a percentage out of the total traffic.
            /radar/http/top/locations/ip_version/{ip_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By IP Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested IP
                  protocol version. Values are a percentage out of the total
                  traffic.
            /radar/http/top/locations/os/{os}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Operating System
                description: >-
                  Get the top locations, by HTTP traffic, of the requested
                  operating systems. Values are a percentage out of the total
                  traffic.
            /radar/http/top/locations/tls_version/{tls_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By TLS Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested TLS
                  protocol version. Values are a percentage out of the total
                  traffic.
            /radar/netflows/timeseries:
              get:
                tags:
                  - Radar Netflows
                summary: Get NetFlows Time Series
                description: >-
                  Get network traffic change over time. Visit
                  https://en.wikipedia.org/wiki/NetFlow for more information on
                  NetFlows. 
            /radar/netflows/top/ases:
              get:
                tags:
                  - Radar Netflows
                summary: Get Top Autonomous Systems By Network Traffic
                description: >-
                  Get the top autonomous systems (AS) by network traffic
                  (NetFlows) over a given time period. Visit
                  https://en.wikipedia.org/wiki/NetFlow for more information.
            /radar/netflows/top/locations:
              get:
                tags:
                  - Radar Netflows
                summary: Get Top Locations By Network Traffic
                description: >-
                  Get the top locations by network traffic (NetFlows) over a
                  given time period. Visit https://en.wikipedia.org/wiki/NetFlow
                  for more information.
            /radar/quality/iqi/summary:
              get:
                tags:
                  - Radar Quality
                summary: Get IQI Summary
                description: >-
                  Get a summary (percentiles) of bandwidth, latency or DNS
                  response time from the Radar Internet Quality Index (IQI).
            /radar/quality/iqi/timeseries_groups:
              get:
                tags:
                  - Radar Quality
                summary: Get IQI Time Series
                description: >-
                  Get a time series (percentiles) of bandwidth, latency or DNS
                  response time from the Radar Internet Quality Index (IQI).
            /radar/quality/speed/histogram:
              get:
                tags:
                  - Radar Quality
                summary: Get Speed Tests Histogram
                description: >-
                  Get an histogram from the previous 90 days of Cloudflare Speed
                  Test data, split into fixed bandwidth (Mbps), latency (ms) or
                  jitter (ms) buckets.
            /radar/quality/speed/summary:
              get:
                tags:
                  - Radar Quality
                summary: Get Speed Tests Summary
                description: >-
                  Get a summary of bandwidth, latency, jitter and packet loss,
                  from the previous 90 days of Cloudflare Speed Test data.
            /radar/quality/speed/top/ases:
              get:
                tags:
                  - Radar Quality
                summary: Get Top Speed Test Autonomous Systems
                description: >-
                  Get the top autonomous systems by bandwidth, latency, jitter
                  or packet loss, from the previous 90 days of Cloudflare Speed
                  Test data.
            /radar/quality/speed/top/locations:
              get:
                tags:
                  - Radar Quality
                summary: Get Top Speed Test Locations
                description: >-
                  Get the top locations by bandwidth, latency, jitter or packet
                  loss, from the previous 90 days of Cloudflare Speed Test data.
            /radar/ranking/domain/{domain}:
              get:
                tags:
                  - Radar Ranking
                summary: Get Domains Rank details
                description: |-
                  Gets Domains Rank details. 
                      Cloudflare provides an ordered rank for the top 100 domains, but for the remainder it only provides ranking buckets
                      like top 200 thousand, top one million, etc.. These are available through Radar datasets endpoints.
            /radar/ranking/timeseries_groups:
              get:
                tags:
                  - Radar Ranking
                summary: Get Domains Rank time series
                description: >-
                  Gets Domains Rank updates change over time. Raw values are
                  returned.
            /radar/ranking/top:
              get:
                tags:
                  - Radar Ranking
                summary: Get Top or Trending Domains
                description: >-
                  Get top or trending domains based on their rank. Popular
                  domains are domains of broad appeal based on how people use
                  the Internet. Trending domains are domains that are generating
                  a surge in interest. For more information on top domains, see
                  https://blog.cloudflare.com/radar-domain-rankings/.
            /radar/search/global:
              get:
                tags:
                  - Radar Search
                summary: Search for locations, autonomous systems (AS) and reports.
                description: >-
                  Lets you search for locations, autonomous systems (AS) and
                  reports.
            /radar/traffic_anomalies:
              get:
                tags:
                  - Radar Traffic Anomalies
                summary: Get latest Internet traffic anomalies.
                description: >-
                  Internet traffic anomalies are signals that might point to an
                  outage,
                          These alerts are automatically detected by Radar and then manually verified by our team.
                          This endpoint returns the latest alerts.
                          
            /radar/traffic_anomalies/locations:
              get:
                tags:
                  - Radar Traffic Anomalies
                summary: Get top locations by total traffic anomalies generated.
                description: >-
                  Internet traffic anomalies are signals that might point to an
                  outage,
                          These alerts are automatically detected by Radar and then manually verified by our team.
                          This endpoint returns the sum of alerts grouped by location.
                          
            /radar/verified_bots/top/bots:
              get:
                tags:
                  - Radar Verified Bots
                summary: Get Top Verified Bots By HTTP Requests
                description: >-
                  Get top verified bots by HTTP requests, with owner and
                  category.
            /radar/verified_bots/top/categories:
              get:
                tags:
                  - Radar Verified Bots
                summary: Get Top Verified Bot Categories By HTTP Requests
                description: >-
                  Get top verified bot categories by HTTP requests, along with
                  their corresponding percentage, over the total verified bot
                  HTTP requests.
            /user:
              get:
                tags:
                  - User
                summary: User Details
              patch:
                tags:
                  - User
                summary: Edit User
                description: Edit part of your user details.
            /user/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get user audit logs
                description: >-
                  Gets a list of audit logs for a user account. Can be filtered
                  by who made the change, on which zone, and the timeframe of
                  the change.
            /user/billing/history:
              get:
                tags:
                  - User Billing History
                summary: Billing History Details
                description: Accesses your billing history object.
            /user/billing/profile:
              get:
                tags:
                  - User Billing Profile
                summary: Billing Profile Details
                description: Accesses your billing profile object.
            /user/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for a user
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of the user. You can filter the
                  results using several optional parameters.
              post:
                tags:
                  - IP Access rules for a user
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for all zones owned by the
                  current user.


                  Note: To create an IP Access rule that applies to a specific
                  zone, refer to the [IP Access rules for a
                  zone](#ip-access-rules-for-a-zone) endpoints.
            /user/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for a user
                summary: Delete an IP Access rule
                description: >-
                  Deletes an IP Access rule at the user level.


                  Note: Deleting a user-level rule will affect all zones owned
                  by the user.
              patch:
                tags:
                  - IP Access rules for a user
                summary: Update an IP Access rule
                description: >-
                  Updates an IP Access rule defined at the user level. You can
                  only update the rule action (`mode` parameter) and notes.
            /user/invites:
              get:
                tags:
                  - User's Invites
                summary: List Invitations
                description: Lists all invitations associated with my user.
            /user/invites/{invite_id}:
              get:
                tags:
                  - User's Invites
                summary: Invitation Details
                description: Gets the details of an invitation.
              patch:
                tags:
                  - User's Invites
                summary: Respond to Invitation
                description: Responds to an invitation.
            /user/load_balancers/monitors:
              get:
                tags:
                  - Load Balancer Monitors
                summary: List Monitors
                description: List configured monitors for a user.
              post:
                tags:
                  - Load Balancer Monitors
                summary: Create Monitor
                description: Create a configured monitor.
            /user/load_balancers/monitors/{monitor_id}:
              delete:
                tags:
                  - Load Balancer Monitors
                summary: Delete Monitor
                description: Delete a configured monitor.
              get:
                tags:
                  - Load Balancer Monitors
                summary: Monitor Details
                description: List a single configured monitor for a user.
              patch:
                tags:
                  - Load Balancer Monitors
                summary: Patch Monitor
                description: >-
                  Apply changes to an existing monitor, overwriting the supplied
                  properties.
              put:
                tags:
                  - Load Balancer Monitors
                summary: Update Monitor
                description: Modify a configured monitor.
            /user/load_balancers/monitors/{monitor_id}/preview:
              post:
                tags:
                  - Load Balancer Monitors
                summary: Preview Monitor
                description: >-
                  Preview pools using the specified monitor with provided
                  monitor details. The returned preview_id can be used in the
                  preview endpoint to retrieve the results.
            /user/load_balancers/monitors/{monitor_id}/references:
              get:
                tags:
                  - Load Balancer Monitors
                summary: List Monitor References
                description: Get the list of resources that reference the provided monitor.
            /user/load_balancers/pools:
              get:
                tags:
                  - Load Balancer Pools
                summary: List Pools
                description: List configured pools.
              patch:
                tags:
                  - Load Balancer Pools
                summary: Patch Pools
                description: >-
                  Apply changes to a number of existing pools, overwriting the
                  supplied properties. Pools are ordered by ascending `name`.
                  Returns the list of affected pools. Supports the standard
                  pagination query parameters, either `limit`/`offset` or
                  `per_page`/`page`.
              post:
                tags:
                  - Load Balancer Pools
                summary: Create Pool
                description: Create a new pool.
            /user/load_balancers/pools/{pool_id}:
              delete:
                tags:
                  - Load Balancer Pools
                summary: Delete Pool
                description: Delete a configured pool.
              get:
                tags:
                  - Load Balancer Pools
                summary: Pool Details
                description: Fetch a single configured pool.
              patch:
                tags:
                  - Load Balancer Pools
                summary: Patch Pool
                description: >-
                  Apply changes to an existing pool, overwriting the supplied
                  properties.
              put:
                tags:
                  - Load Balancer Pools
                summary: Update Pool
                description: Modify a configured pool.
            /user/load_balancers/pools/{pool_id}/health:
              get:
                tags:
                  - Load Balancer Pools
                summary: Pool Health Details
                description: Fetch the latest pool health status for a single pool.
            /user/load_balancers/pools/{pool_id}/preview:
              post:
                tags:
                  - Load Balancer Pools
                summary: Preview Pool
                description: >-
                  Preview pool health using provided monitor details. The
                  returned preview_id can be used in the preview endpoint to
                  retrieve the results.
            /user/load_balancers/pools/{pool_id}/references:
              get:
                tags:
                  - Load Balancer Pools
                summary: List Pool References
                description: Get the list of resources that reference the provided pool.
            /user/load_balancers/preview/{preview_id}:
              get:
                tags:
                  - Load Balancer Monitors
                summary: Preview Result
                description: >-
                  Get the result of a previous preview operation using the
                  provided preview_id.
            /user/load_balancing_analytics/events:
              get:
                tags:
                  - Load Balancer Healthcheck Events
                summary: List Healthcheck Events
                description: List origin health changes.
            /user/organizations:
              get:
                tags:
                  - User's Organizations
                summary: List Organizations
                description: Lists organizations the user is associated with.
            /user/organizations/{organization_id}:
              delete:
                tags:
                  - User's Organizations
                summary: Leave Organization
                description: Removes association to an organization.
              get:
                tags:
                  - User's Organizations
                summary: Organization Details
                description: Gets a specific organization the user is associated with.
            /user/subscriptions:
              get:
                tags:
                  - User Subscription
                summary: Get User Subscriptions
                description: Lists all of a user's subscriptions.
            /user/subscriptions/{identifier}:
              delete:
                tags:
                  - User Subscription
                summary: Delete User Subscription
                description: Deletes a user's subscription.
              put:
                tags:
                  - User Subscription
                summary: Update User Subscription
                description: Updates a user's subscriptions.
            /user/tokens:
              get:
                tags:
                  - User API Tokens
                summary: List Tokens
                description: List all access tokens you created.
              post:
                tags:
                  - User API Tokens
                summary: Create Token
                description: Create a new access token.
            /user/tokens/{token_id}:
              delete:
                tags:
                  - User API Tokens
                summary: Delete Token
                description: Destroy a token.
              get:
                tags:
                  - User API Tokens
                summary: Token Details
                description: Get information about a specific token.
              put:
                tags:
                  - User API Tokens
                summary: Update Token
                description: Update an existing token.
            /user/tokens/{token_id}/value:
              put:
                tags:
                  - User API Tokens
                summary: Roll Token
                description: Roll the token secret.
            /user/tokens/permission_groups:
              get:
                tags:
                  - Permission Groups
                summary: List Permission Groups
                description: Find all available permission groups.
            /user/tokens/verify:
              get:
                tags:
                  - User API Tokens
                summary: Verify Token
                description: Test whether a token works.
            /zones:
              get:
                tags:
                  - Zone
                summary: List Zones
                description: Lists, searches, sorts, and filters your zones.
              post:
                tags:
                  - Zone
                summary: Create Zone
            /zones/{identifier}/access/apps:
              get:
                tags:
                  - Zone-Level Access applications
                summary: List Access Applications
                description: List all Access Applications in a zone.
              post:
                tags:
                  - Zone-Level Access applications
                summary: Add an Access application
                description: Adds a new application to Access.
            /zones/{identifier}/access/apps/{app_id}:
              delete:
                tags:
                  - Zone-Level Access applications
                summary: Delete an Access application
                description: Deletes an application from Access.
              get:
                tags:
                  - Zone-Level Access applications
                summary: Get an Access application
                description: Fetches information about an Access application.
              put:
                tags:
                  - Zone-Level Access applications
                summary: Update an Access application
                description: Updates an Access application.
            /zones/{identifier}/access/apps/{app_id}/revoke_tokens:
              post:
                tags:
                  - Zone-Level Access applications
                summary: Revoke application tokens
                description: Revokes all tokens issued for an application.
            /zones/{identifier}/access/apps/{app_id}/user_policy_checks:
              get:
                tags:
                  - Zone-Level Access applications
                summary: Test Access policies
                description: >-
                  Tests if a specific user has permission to access an
                  application.
            /zones/{identifier}/access/apps/{uuid}/ca:
              delete:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Delete a short-lived certificate CA
                description: Deletes a short-lived certificate CA.
              get:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Get a short-lived certificate CA
                description: Fetches a short-lived certificate CA and its public key.
              post:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Create a short-lived certificate CA
                description: Generates a new short-lived certificate CA and public key.
            /zones/{identifier}/access/apps/{uuid}/policies:
              get:
                tags:
                  - Zone-Level Access policies
                summary: List Access policies
                description: Lists Access policies configured for an application.
              post:
                tags:
                  - Zone-Level Access policies
                summary: Create an Access policy
                description: Create a new Access policy for an application.
            /zones/{identifier}/access/apps/{uuid1}/policies/{uuid}:
              delete:
                tags:
                  - Zone-Level Access policies
                summary: Delete an Access policy
                description: Delete an Access policy.
              get:
                tags:
                  - Zone-Level Access policies
                summary: Get an Access policy
                description: Fetches a single Access policy.
              put:
                tags:
                  - Zone-Level Access policies
                summary: Update an Access policy
                description: Update a configured Access policy.
            /zones/{identifier}/access/apps/ca:
              get:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: List short-lived certificate CAs
                description: Lists short-lived certificate CAs and their public keys.
            /zones/{identifier}/access/certificates:
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: List mTLS certificates
                description: Lists all mTLS certificates.
              post:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Add an mTLS certificate
                description: Adds a new mTLS root certificate to Access.
            /zones/{identifier}/access/certificates/{uuid}:
              delete:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Delete an mTLS certificate
                description: Deletes an mTLS certificate.
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Get an mTLS certificate
                description: Fetches a single mTLS certificate.
              put:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Update an mTLS certificate
                description: Updates a configured mTLS certificate.
            /zones/{identifier}/access/certificates/settings:
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: List all mTLS hostname settings
                description: List all mTLS hostname settings for this zone.
              put:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Update an mTLS certificate's hostname settings
                description: Updates an mTLS certificate's hostname settings.
            /zones/{identifier}/access/groups:
              get:
                tags:
                  - Zone-Level Access groups
                summary: List Access groups
                description: Lists all Access groups.
              post:
                tags:
                  - Zone-Level Access groups
                summary: Create an Access group
                description: Creates a new Access group.
            /zones/{identifier}/access/groups/{uuid}:
              delete:
                tags:
                  - Zone-Level Access groups
                summary: Delete an Access group
                description: Deletes an Access group.
              get:
                tags:
                  - Zone-Level Access groups
                summary: Get an Access group
                description: Fetches a single Access group.
              put:
                tags:
                  - Zone-Level Access groups
                summary: Update an Access group
                description: Updates a configured Access group.
            /zones/{identifier}/access/identity_providers:
              get:
                tags:
                  - Zone-Level Access identity providers
                summary: List Access identity providers
                description: Lists all configured identity providers.
              post:
                tags:
                  - Zone-Level Access identity providers
                summary: Add an Access identity provider
                description: Adds a new identity provider to Access.
            /zones/{identifier}/access/identity_providers/{uuid}:
              delete:
                tags:
                  - Zone-Level Access identity providers
                summary: Delete an Access identity provider
                description: Deletes an identity provider from Access.
              get:
                tags:
                  - Zone-Level Access identity providers
                summary: Get an Access identity provider
                description: Fetches a configured identity provider.
              put:
                tags:
                  - Zone-Level Access identity providers
                summary: Update an Access identity provider
                description: Updates a configured identity provider.
            /zones/{identifier}/access/organizations:
              get:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Get your Zero Trust organization
                description: Returns the configuration for your Zero Trust organization.
              post:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Create your Zero Trust organization
                description: Sets up a Zero Trust organization for your account.
              put:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Update your Zero Trust organization
                description: Updates the configuration for your Zero Trust organization.
            /zones/{identifier}/access/organizations/revoke_user:
              post:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Revoke all Access tokens for a user
                description: Revokes a user's access across all applications.
            /zones/{identifier}/access/service_tokens:
              get:
                tags:
                  - Zone-Level Access service tokens
                summary: List service tokens
                description: Lists all service tokens.
              post:
                tags:
                  - Zone-Level Access service tokens
                summary: Create a service token
                description: >-
                  Generates a new service token. **Note:** This is the only time
                  you can get the Client Secret. If you lose the Client Secret,
                  you will have to create a new service token.
            /zones/{identifier}/access/service_tokens/{uuid}:
              delete:
                tags:
                  - Zone-Level Access service tokens
                summary: Delete a service token
                description: Deletes a service token.
              put:
                tags:
                  - Zone-Level Access service tokens
                summary: Update a service token
                description: Updates a configured service token.
            /zones/{identifier}/dns_analytics/report:
              get:
                tags:
                  - DNS Analytics
                summary: Table
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /zones/{identifier}/dns_analytics/report/bytime:
              get:
                tags:
                  - DNS Analytics
                summary: By Time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /zones/{identifier}/subscription:
              get:
                tags:
                  - Zone Subscription
                summary: Zone Subscription Details
                description: Lists zone subscription details.
              post:
                tags:
                  - Zone Subscription
                summary: Create Zone Subscription
                description: Create a zone subscription, either plan or add-ons.
              put:
                tags:
                  - Zone Subscription
                summary: Update Zone Subscription
                description: Updates zone subscriptions, either plan or add-ons.
            /zones/{zone_id}:
              delete:
                tags:
                  - Zone
                summary: Delete Zone
                description: Deletes an existing zone.
              get:
                tags:
                  - Zone
                summary: Zone Details
              patch:
                tags:
                  - Zone
                summary: Edit Zone
                description: Edits a zone. Only one zone property can be changed at a time.
            /zones/{zone_id}/acm/total_tls:
              get:
                tags:
                  - Total TLS
                summary: Total TLS Settings Details
                description: Get Total TLS Settings for a Zone.
              post:
                tags:
                  - Total TLS
                summary: Enable or Disable Total TLS
                description: Set Total TLS Settings or disable the feature for a Zone.
            /zones/{zone_id}/activation_check:
              put:
                tags:
                  - Zone
                summary: Rerun the Activation Check
                description: >-
                  Triggeres a new activation check for a PENDING Zone. This can
                  be

                  triggered every 5 min for paygo/ent customers, every hour for
                  FREE

                  Zones.
            /zones/{zone_id}/analytics/latency:
              get:
                tags:
                  - Argo Analytics for Zone
                summary: Argo Analytics for a zone
            /zones/{zone_id}/analytics/latency/colos:
              get:
                tags:
                  - Argo Analytics for Geolocation
                summary: Argo Analytics for a zone at different PoPs
            /zones/{zone_id}/api_gateway/configuration:
              get:
                tags:
                  - API Shield Settings
                summary: Retrieve information about specific configuration properties
              put:
                tags:
                  - API Shield Settings
                summary: Set configuration properties
            /zones/{zone_id}/api_gateway/discovery:
              get:
                tags:
                  - API Shield API Discovery
                summary: >-
                  Retrieve discovered operations on a zone rendered as OpenAPI
                  schemas
                description: >-
                  Retrieve the most up to date view of discovered operations,
                  rendered as OpenAPI schemas
            /zones/{zone_id}/api_gateway/discovery/operations:
              get:
                tags:
                  - API Shield API Discovery
                summary: Retrieve discovered operations on a zone
                description: Retrieve the most up to date view of discovered operations
              patch:
                tags:
                  - API Shield API Discovery
                summary: Patch discovered operations
                description: Update the `state` on one or more discovered operations
            /zones/{zone_id}/api_gateway/discovery/operations/{operation_id}:
              patch:
                tags:
                  - API Shield API Discovery
                summary: Patch discovered operation
                description: Update the `state` on a discovered operation
            /zones/{zone_id}/api_gateway/operations:
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve information about all operations on a zone
              post:
                tags:
                  - API Shield Endpoint Management
                summary: Add operations to a zone
                description: >-
                  Add one or more operations to a zone. Endpoints can contain
                  path variables. Host, method, endpoint will be normalized to a
                  canoncial form when creating an operation and must be unique
                  on the zone. Inserting an operation that matches an existing
                  one will return the record of the already existing operation
                  and update its last_updated date.
            /zones/{zone_id}/api_gateway/operations/{operation_id}:
              delete:
                tags:
                  - API Shield Endpoint Management
                summary: Delete an operation
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve information about an operation
            /zones/{zone_id}/api_gateway/operations/{operation_id}/schema_validation:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve operation-level schema validation settings
                description: >-
                  Retrieves operation-level schema validation settings on the
                  zone
              put:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update operation-level schema validation settings
                description: Updates operation-level schema validation settings on the zone
            /zones/{zone_id}/api_gateway/operations/schema_validation:
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update multiple operation-level schema validation settings
                description: >-
                  Updates multiple operation-level schema validation settings on
                  the zone
            /zones/{zone_id}/api_gateway/schemas:
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve operations and features as OpenAPI schemas
            /zones/{zone_id}/api_gateway/settings/schema_validation:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve zone level schema validation settings
                description: >-
                  Retrieves zone level schema validation settings currently set
                  on the zone
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update zone level schema validation settings
                description: Updates zone level schema validation settings on the zone
              put:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update zone level schema validation settings
                description: Updates zone level schema validation settings on the zone
            /zones/{zone_id}/api_gateway/user_schemas:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve information about all schemas on a zone
              post:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Upload a schema to a zone
            /zones/{zone_id}/api_gateway/user_schemas/{schema_id}:
              delete:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Delete a schema
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve information about a specific schema on a zone
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Enable validation for a schema
            /zones/{zone_id}/api_gateway/user_schemas/{schema_id}/operations:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve all operations from a schema.
                description: >-
                  Retrieves all operations from the schema. Operations that
                  already exist in API Shield Endpoint Management will be
                  returned as full operations.
            /zones/{zone_id}/argo/smart_routing:
              get:
                tags:
                  - Argo Smart Routing
                summary: Get Argo Smart Routing setting
              patch:
                tags:
                  - Argo Smart Routing
                summary: Patch Argo Smart Routing setting
                description: Updates enablement of Argo Smart Routing.
            /zones/{zone_id}/argo/tiered_caching:
              get:
                tags:
                  - Tiered Caching
                summary: Get Tiered Caching setting
              patch:
                tags:
                  - Tiered Caching
                summary: Patch Tiered Caching setting
                description: Updates enablement of Tiered Caching
            /zones/{zone_id}/bot_management:
              get:
                tags:
                  - Bot Settings
                summary: Get Zone Bot Management Config
                description: Retrieve a zone's Bot Management Config
              put:
                tags:
                  - Bot Settings
                summary: Update Zone Bot Management Config
                description: >
                  Updates the Bot Management configuration for a zone.


                  This API is used to update:

                  - **Bot Fight Mode**

                  - **Super Bot Fight Mode**

                  - **Bot Management for Enterprise**


                  See [Bot Plans](https://developers.cloudflare.com/bots/plans/)
                  for more information on the different plans
            /zones/{zone_id}/cache/cache_reserve:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Cache Reserve setting
                description: >-
                  Increase cache lifetimes by automatically storing all
                  cacheable files into Cloudflare's persistent object storage
                  buckets. Requires Cache Reserve subscription. Note: using
                  Tiered Cache with Cache Reserve is highly recommended to
                  reduce Reserve operations costs. See the [developer
                  docs](https://developers.cloudflare.com/cache/about/cache-reserve)
                  for more information.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Cache Reserve setting
                description: >-
                  Increase cache lifetimes by automatically storing all
                  cacheable files into Cloudflare's persistent object storage
                  buckets. Requires Cache Reserve subscription. Note: using
                  Tiered Cache with Cache Reserve is highly recommended to
                  reduce Reserve operations costs. See the [developer
                  docs](https://developers.cloudflare.com/cache/about/cache-reserve)
                  for more information.
            /zones/{zone_id}/cache/cache_reserve_clear:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Cache Reserve Clear
                description: >-
                  You can use Cache Reserve Clear to clear your Cache Reserve,
                  but you must first disable Cache Reserve. In most cases, this
                  will be accomplished within 24 hours. You cannot re-enable
                  Cache Reserve while this process is ongoing. Keep in mind that
                  you cannot undo or cancel this operation.
              post:
                tags:
                  - Zone Cache Settings
                summary: Start Cache Reserve Clear
                description: >-
                  You can use Cache Reserve Clear to clear your Cache Reserve,
                  but you must first disable Cache Reserve. In most cases, this
                  will be accomplished within 24 hours. You cannot re-enable
                  Cache Reserve while this process is ongoing. Keep in mind that
                  you cannot undo or cancel this operation.
            /zones/{zone_id}/cache/origin_post_quantum_encryption:
              get:
                tags:
                  - Origin Post-Quantum
                summary: Get Origin Post-Quantum Encryption setting
                description: >-
                  Instructs Cloudflare to use Post-Quantum (PQ) key agreement
                  algorithms when connecting to your origin. Preferred instructs
                  Cloudflare to opportunistically send a Post-Quantum keyshare
                  in the first message to the origin (for fastest connections
                  when the origin supports and prefers PQ), supported means that
                  PQ algorithms are advertised but only used when requested by
                  the origin, and off means that PQ algorithms are not
                  advertised
              put:
                tags:
                  - Origin Post-Quantum
                summary: Change Origin Post-Quantum Encryption setting
                description: >-
                  Instructs Cloudflare to use Post-Quantum (PQ) key agreement
                  algorithms when connecting to your origin. Preferred instructs
                  Cloudflare to opportunistically send a Post-Quantum keyshare
                  in the first message to the origin (for fastest connections
                  when the origin supports and prefers PQ), supported means that
                  PQ algorithms are advertised but only used when requested by
                  the origin, and off means that PQ algorithms are not
                  advertised
            /zones/{zone_id}/cache/regional_tiered_cache:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Regional Tiered Cache setting
                description: >-
                  Instructs Cloudflare to check a regional hub data center on
                  the way to your upper tier. This can help improve performance
                  for smart and custom tiered cache topologies.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Regional Tiered Cache setting
                description: >-
                  Instructs Cloudflare to check a regional hub data center on
                  the way to your upper tier. This can help improve performance
                  for smart and custom tiered cache topologies.
            /zones/{zone_id}/cache/tiered_cache_smart_topology_enable:
              delete:
                tags:
                  - Smart Tiered Cache
                summary: Delete Smart Tiered Cache setting
                description: Remvoves enablement of Smart Tiered Cache
              get:
                tags:
                  - Smart Tiered Cache
                summary: Get Smart Tiered Cache setting
              patch:
                tags:
                  - Smart Tiered Cache
                summary: Patch Smart Tiered Cache setting
                description: Updates enablement of Tiered Cache
            /zones/{zone_id}/cache/variants:
              delete:
                tags:
                  - Zone Cache Settings
                summary: Delete variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
              get:
                tags:
                  - Zone Cache Settings
                summary: Get variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
            /zones/{zone_id}/certificate_authorities/hostname_associations:
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: List Hostname Associations
                description: List Hostname Associations
              put:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Replace Hostname Associations
                description: Replace Hostname Associations
            /zones/{zone_id}/client_certificates:
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: List Client Certificates
                description: >-
                  List all of your Zone's API Shield mTLS Client Certificates by
                  Status and/or using Pagination
              post:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Create Client Certificate
                description: Create a new API Shield mTLS Client Certificate
            /zones/{zone_id}/client_certificates/{client_certificate_id}:
              delete:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Revoke Client Certificate
                description: >-
                  Set a API Shield mTLS Client Certificate to pending_revocation
                  status for processing to revoked status.
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Client Certificate Details
                description: Get Details for a single mTLS API Shield Client Certificate
              patch:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Reactivate Client Certificate
                description: >-
                  If a API Shield mTLS Client Certificate is in a
                  pending_revocation state, you may reactivate it with this
                  endpoint.
            /zones/{zone_id}/custom_certificates:
              get:
                tags:
                  - Custom SSL for a Zone
                summary: List SSL Configurations
                description: >-
                  List, search, and filter all of your custom SSL certificates.
                  The higher priority will break ties across overlapping
                  'legacy_custom' certificates, but 'legacy_custom' certificates
                  will always supercede 'sni_custom' certificates.
              post:
                tags:
                  - Custom SSL for a Zone
                summary: Create SSL Configuration
                description: Upload a new SSL certificate for a zone.
            /zones/{zone_id}/custom_certificates/{custom_certificate_id}:
              delete:
                tags:
                  - Custom SSL for a Zone
                summary: Delete SSL Configuration
                description: Remove a SSL certificate from a zone.
              get:
                tags:
                  - Custom SSL for a Zone
                summary: SSL Configuration Details
              patch:
                tags:
                  - Custom SSL for a Zone
                summary: Edit SSL Configuration
                description: >-
                  Upload a new private key and/or PEM/CRT for the SSL
                  certificate. Note: PATCHing a configuration for sni_custom
                  certificates will result in a new resource id being returned,
                  and the previous one being deleted.
            /zones/{zone_id}/custom_certificates/prioritize:
              put:
                tags:
                  - Custom SSL for a Zone
                summary: Re-prioritize SSL Certificates
                description: >-
                  If a zone has multiple SSL certificates, you can set the order
                  in which they should be used during a request. The higher
                  priority will break ties across overlapping 'legacy_custom'
                  certificates.
            /zones/{zone_id}/custom_hostnames:
              get:
                tags:
                  - Custom Hostname for a Zone
                summary: List Custom Hostnames
                description: List, search, sort, and filter all of your custom hostnames.
              post:
                tags:
                  - Custom Hostname for a Zone
                summary: Create Custom Hostname
                description: >-
                  Add a new custom hostname and request that an SSL certificate
                  be issued for it. One of three validation methods—http, txt,
                  email—should be used, with 'http' recommended if the CNAME is
                  already in place (or will be soon). Specifying 'email' will
                  send an email to the WHOIS contacts on file for the base
                  domain plus hostmaster, postmaster, webmaster, admin,
                  administrator. If http is used and the domain is not already
                  pointing to the Managed CNAME host, the PATCH method must be
                  used once it is (to complete validation).
            /zones/{zone_id}/custom_hostnames/{custom_hostname_id}:
              delete:
                tags:
                  - Custom Hostname for a Zone
                summary: Delete Custom Hostname (and any issued SSL certificates)
              get:
                tags:
                  - Custom Hostname for a Zone
                summary: Custom Hostname Details
              patch:
                tags:
                  - Custom Hostname for a Zone
                summary: Edit Custom Hostname
                description: >-
                  Modify SSL configuration for a custom hostname. When sent with
                  SSL config that matches existing config, used to indicate that
                  hostname should pass domain control validation (DCV). Can also
                  be used to change validation type, e.g., from 'http' to
                  'email'.
            /zones/{zone_id}/custom_hostnames/fallback_origin:
              delete:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Delete Fallback Origin for Custom Hostnames
              get:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Get Fallback Origin for Custom Hostnames
              put:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Update Fallback Origin for Custom Hostnames
            /zones/{zone_id}/custom_ns:
              get:
                tags:
                  - Account-Level Custom Nameservers Usage for a Zone
                summary: Get Account Custom Nameserver Related Zone Metadata
                description: |
                  Get metadata for account-level custom nameservers on a zone.
              put:
                tags:
                  - Account-Level Custom Nameservers Usage for a Zone
                summary: Set Account Custom Nameserver Related Zone Metadata
                description: >
                  Set metadata for account-level custom nameservers on a zone.


                  If you would like new zones in the account to use account
                  custom nameservers by default, use PUT /accounts/:identifier
                  to set the account setting use_account_custom_ns_by_default to
                  true.
            /zones/{zone_id}/dcv_delegation/uuid:
              get:
                tags:
                  - DCV Delegation
                summary: Retrieve the DCV Delegation unique identifier.
                description: >-
                  Retrieve the account and zone specific unique identifier used
                  as part of the CNAME target for DCV Delegation.
            /zones/{zone_id}/dns_records:
              get:
                tags:
                  - DNS Records for a Zone
                summary: List DNS Records
                description: List, search, sort, and filter a zones' DNS records.
              post:
                tags:
                  - DNS Records for a Zone
                summary: Create DNS Record
                description: >
                  Create a new DNS record for a zone.


                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
            /zones/{zone_id}/dns_records/{dns_record_id}:
              delete:
                tags:
                  - DNS Records for a Zone
                summary: Delete DNS Record
              get:
                tags:
                  - DNS Records for a Zone
                summary: DNS Record Details
              patch:
                tags:
                  - DNS Records for a Zone
                summary: Update DNS Record
                description: >
                  Update an existing DNS record.

                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
              put:
                tags:
                  - DNS Records for a Zone
                summary: Overwrite DNS Record
                description: >
                  Overwrite an existing DNS record.

                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
            /zones/{zone_id}/dns_records/export:
              get:
                tags:
                  - DNS Records for a Zone
                summary: Export DNS Records
                description: >-
                  You can export your [BIND
                  config](https://en.wikipedia.org/wiki/Zone_file "Zone file")
                  through this endpoint.


                  See [the
                  documentation](https://developers.cloudflare.com/dns/manage-dns-records/how-to/import-and-export/
                  "Import and export records") for more information.
            /zones/{zone_id}/dns_records/import:
              post:
                tags:
                  - DNS Records for a Zone
                summary: Import DNS Records
                description: >-
                  You can upload your [BIND
                  config](https://en.wikipedia.org/wiki/Zone_file "Zone file")
                  through this endpoint. It assumes that cURL is called from a
                  location with bind_config.txt (valid BIND config) present.


                  See [the
                  documentation](https://developers.cloudflare.com/dns/manage-dns-records/how-to/import-and-export/
                  "Import and export records") for more information.
            /zones/{zone_id}/dns_records/scan:
              post:
                tags:
                  - DNS Records for a Zone
                summary: Scan DNS Records
                description: >-
                  Scan for common DNS records on your domain and automatically
                  add them to your zone. Useful if you haven't updated your
                  nameservers yet.
            /zones/{zone_id}/dnssec:
              delete:
                tags:
                  - DNSSEC
                summary: Delete DNSSEC records
                description: Delete DNSSEC.
              get:
                tags:
                  - DNSSEC
                summary: DNSSEC Details
                description: Details about DNSSEC status and configuration.
              patch:
                tags:
                  - DNSSEC
                summary: Edit DNSSEC Status
                description: Enable or disable DNSSEC.
            /zones/{zone_id}/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for a zone
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of a zone. You can filter the results
                  using several optional parameters.
              post:
                tags:
                  - IP Access rules for a zone
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for a zone.


                  Note: To create an IP Access rule that applies to multiple
                  zones, refer to [IP Access rules for a
                  user](#ip-access-rules-for-a-user) or [IP Access rules for an
                  account](#ip-access-rules-for-an-account) as appropriate.
            /zones/{zone_id}/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for a zone
                summary: Delete an IP Access rule
                description: >-
                  Deletes an IP Access rule defined at the zone level.


                  Optionally, you can use the `cascade` property to specify that
                  you wish to delete similar rules in other zones managed by the
                  same zone owner.
              patch:
                tags:
                  - IP Access rules for a zone
                summary: Update an IP Access rule
                description: >-
                  Updates an IP Access rule defined at the zone level. You can
                  only update the rule action (`mode` parameter) and notes.
            /zones/{zone_id}/firewall/waf/packages/{package_id}/groups:
              get:
                tags:
                  - WAF rule groups
                summary: List WAF rule groups
                description: >-
                  Fetches the WAF rule groups in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/groups/{group_id}:
              get:
                tags:
                  - WAF rule groups
                summary: Get a WAF rule group
                description: >-
                  Fetches the details of a WAF rule group.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF rule groups
                summary: Update a WAF rule group
                description: >-
                  Updates a WAF rule group. You can update the state (`mode`
                  parameter) of a rule group.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/rules:
              get:
                tags:
                  - WAF rules
                summary: List WAF rules
                description: >-
                  Fetches WAF rules in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/rules/{rule_id}:
              get:
                tags:
                  - WAF rules
                summary: Get a WAF rule
                description: >-
                  Fetches the details of a WAF rule in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF rules
                summary: Update a WAF rule
                description: >-
                  Updates a WAF rule. You can only update the mode/action of the
                  rule.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/hold:
              delete:
                tags:
                  - Zone Holds
                summary: Remove Zone Hold
                description: >-
                  Stop enforcement of a zone hold on the zone, permanently or
                  temporarily, allowing the

                  creation and activation of zones with this zone's hostname.
              get:
                tags:
                  - Zone Holds
                summary: Get Zone Hold
                description: >-
                  Retrieve whether the zone is subject to a zone hold, and
                  metadata about the hold.
              post:
                tags:
                  - Zone Holds
                summary: Create Zone Hold
                description: >-
                  Enforce a zone hold on the zone, blocking the creation and
                  activation of zones with this zone's hostname.
            /zones/{zone_id}/hostnames/settings/{setting_id}:
              get:
                tags:
                  - Per-Hostname TLS Settings
                summary: List TLS setting for hostnames
                description: >-
                  List the requested TLS setting for the hostnames under this
                  zone.
            /zones/{zone_id}/hostnames/settings/{setting_id}/{hostname}:
              delete:
                tags:
                  - Per-Hostname TLS Settings
                summary: Delete TLS setting for hostname
                description: Delete the tls setting value for the hostname.
              put:
                tags:
                  - Per-Hostname TLS Settings
                summary: Edit TLS setting for hostname
                description: Update the tls setting value for the hostname.
            /zones/{zone_id}/keyless_certificates:
              get:
                tags:
                  - Keyless SSL for a Zone
                summary: List Keyless SSL Configurations
                description: List all Keyless SSL configurations for a given zone.
              post:
                tags:
                  - Keyless SSL for a Zone
                summary: Create Keyless SSL Configuration
            /zones/{zone_id}/keyless_certificates/{keyless_certificate_id}:
              delete:
                tags:
                  - Keyless SSL for a Zone
                summary: Delete Keyless SSL Configuration
              get:
                tags:
                  - Keyless SSL for a Zone
                summary: Get Keyless SSL Configuration
                description: Get details for one Keyless SSL configuration.
              patch:
                tags:
                  - Keyless SSL for a Zone
                summary: Edit Keyless SSL Configuration
                description: >-
                  This will update attributes of a Keyless SSL. Consists of one
                  or more of the following:  host,name,port.
            /zones/{zone_id}/load_balancers:
              get:
                tags:
                  - Load Balancers
                summary: List Load Balancers
                description: List configured load balancers.
              post:
                tags:
                  - Load Balancers
                summary: Create Load Balancer
                description: Create a new load balancer.
            /zones/{zone_id}/load_balancers/{load_balancer_id}:
              delete:
                tags:
                  - Load Balancers
                summary: Delete Load Balancer
                description: Delete a configured load balancer.
              get:
                tags:
                  - Load Balancers
                summary: Load Balancer Details
                description: Fetch a single configured load balancer.
              patch:
                tags:
                  - Load Balancers
                summary: Patch Load Balancer
                description: >-
                  Apply changes to an existing load balancer, overwriting the
                  supplied properties.
              put:
                tags:
                  - Load Balancers
                summary: Update Load Balancer
                description: Update a configured load balancer.
            /zones/{zone_id}/logpush/datasets/{dataset_id}/fields:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List fields
                description: >-
                  Lists all fields available for a dataset. The response result
                  is an object with key-value pairs, where keys are field names,
                  and values are descriptions.
            /zones/{zone_id}/logpush/datasets/{dataset_id}/jobs:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List Logpush jobs for a dataset
                description: Lists Logpush jobs for a zone for a dataset.
            /zones/{zone_id}/logpush/edge:
              get:
                tags:
                  - Instant Logs jobs for a zone
                summary: List Instant Logs jobs
                description: Lists Instant Logs jobs for a zone.
              post:
                tags:
                  - Instant Logs jobs for a zone
                summary: Create Instant Logs job
                description: Creates a new Instant Logs job for a zone.
            /zones/{zone_id}/logpush/jobs:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List Logpush jobs
                description: Lists Logpush jobs for a zone.
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Create Logpush job
                description: Creates a new Logpush job for a zone.
            /zones/{zone_id}/logpush/jobs/{job_id}:
              delete:
                tags:
                  - Logpush jobs for a zone
                summary: Delete Logpush job
                description: Deletes a Logpush job.
              get:
                tags:
                  - Logpush jobs for a zone
                summary: Get Logpush job details
                description: Gets the details of a Logpush job.
              put:
                tags:
                  - Logpush jobs for a zone
                summary: Update Logpush job
                description: Updates a Logpush job.
            /zones/{zone_id}/logpush/ownership:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Get ownership challenge
                description: Gets a new ownership challenge sent to your destination.
            /zones/{zone_id}/logpush/ownership/validate:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Validate ownership challenge
                description: Validates ownership challenge of the destination.
            /zones/{zone_id}/logpush/validate/destination/exists:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Check destination exists
                description: Checks if there is an existing job with a destination.
            /zones/{zone_id}/logpush/validate/origin:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Validate origin
                description: Validates logpull origin with logpull_options.
            /zones/{zone_id}/managed_headers:
              get:
                tags:
                  - Managed Transforms
                summary: List Managed Transforms
                description: Fetches a list of all Managed Transforms.
              patch:
                tags:
                  - Managed Transforms
                summary: Update status of Managed Transforms
                description: Updates the status of one or more Managed Transforms.
            /zones/{zone_id}/origin_tls_client_auth:
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: List Certificates
              post:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Upload Certificate
                description: >-
                  Upload your own certificate you want Cloudflare to use for
                  edge-to-origin communication to override the shared
                  certificate. Please note that it is important to keep only one
                  certificate active. Also, make sure to enable zone-level
                  authenticated origin pulls by making a PUT call to settings
                  endpoint to see the uploaded certificate in use.
            /zones/{zone_id}/origin_tls_client_auth/{certificate_id}:
              delete:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Delete Certificate
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Get Certificate Details
            /zones/{zone_id}/origin_tls_client_auth/hostnames:
              put:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Enable or Disable a Hostname for Client Authentication
                description: >-
                  Associate a hostname to a certificate and enable, disable or
                  invalidate the association. If disabled, client certificate
                  will not be sent to the hostname even if activated at the zone
                  level. 100 maximum associations on a single certificate are
                  allowed. Note: Use a null value for parameter *enabled* to
                  invalidate the association.
            /zones/{zone_id}/origin_tls_client_auth/hostnames/{hostname}:
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Get the Hostname Status for Client Authentication
            /zones/{zone_id}/origin_tls_client_auth/hostnames/certificates:
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: List Certificates
              post:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Upload a Hostname Client Certificate
                description: >-
                  Upload a certificate to be used for client authentication on a
                  hostname. 10 hostname certificates per zone are allowed.
            /zones/{zone_id}/origin_tls_client_auth/hostnames/certificates/{certificate_id}:
              delete:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Delete Hostname Client Certificate
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Get the Hostname Client Certificate
                description: >-
                  Get the certificate by ID to be used for client authentication
                  on a hostname.
            /zones/{zone_id}/origin_tls_client_auth/settings:
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Get Enablement Setting for Zone
                description: >-
                  Get whether zone-level authenticated origin pulls is enabled
                  or not. It is false by default.
              put:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Set Enablement for Zone
                description: >-
                  Enable or disable zone-level authenticated origin pulls.
                  'enabled' should be set true either before/after the
                  certificate is uploaded to see the certificate in use.
            /zones/{zone_id}/page_shield:
              get:
                tags:
                  - Page Shield
                summary: Get Page Shield settings
                description: Fetches the Page Shield settings.
              put:
                tags:
                  - Page Shield
                summary: Update Page Shield settings
                description: Updates Page Shield settings.
            /zones/{zone_id}/page_shield/connections:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield connections
                description: Lists all connections detected by Page Shield.
            /zones/{zone_id}/page_shield/connections/{connection_id}:
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield connection
                description: Fetches a connection detected by Page Shield by connection ID.
            /zones/{zone_id}/page_shield/policies:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield policies
                description: Lists all Page Shield policies.
              post:
                tags:
                  - Page Shield
                summary: Create a Page Shield policy
                description: Create a Page Shield policy.
            /zones/{zone_id}/page_shield/policies/{policy_id}:
              delete:
                tags:
                  - Page Shield
                summary: Delete a Page Shield policy
                description: Delete a Page Shield policy by ID.
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield policy
                description: Fetches a Page Shield policy by ID.
              put:
                tags:
                  - Page Shield
                summary: Update a Page Shield policy
                description: Update a Page Shield policy by ID.
            /zones/{zone_id}/page_shield/scripts:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield scripts
                description: Lists all scripts detected by Page Shield.
            /zones/{zone_id}/page_shield/scripts/{script_id}:
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield script
                description: Fetches a script detected by Page Shield by script ID.
            /zones/{zone_id}/pagerules:
              get:
                tags:
                  - Page Rules
                summary: List Page Rules
                description: Fetches Page Rules in a zone.
              post:
                tags:
                  - Page Rules
                summary: Create a Page Rule
                description: Creates a new Page Rule.
            /zones/{zone_id}/pagerules/{pagerule_id}:
              delete:
                tags:
                  - Page Rules
                summary: Delete a Page Rule
                description: Deletes an existing Page Rule.
              get:
                tags:
                  - Page Rules
                summary: Get a Page Rule
                description: Fetches the details of a Page Rule.
              patch:
                tags:
                  - Page Rules
                summary: Edit a Page Rule
                description: Updates one or more fields of an existing Page Rule.
              put:
                tags:
                  - Page Rules
                summary: Update a Page Rule
                description: >-
                  Replaces the configuration of an existing Page Rule. The
                  configuration of the updated Page Rule will exactly match the
                  data passed in the API request.
            /zones/{zone_id}/pagerules/settings:
              get:
                tags:
                  - Available Page Rules settings
                summary: List available Page Rules settings
                description: >-
                  Returns a list of settings (and their details) that Page Rules
                  can apply to matching requests.
            /zones/{zone_id}/purge_cache:
              post:
                tags:
                  - Zone
                summary: Purge Cached Content
                description: >
                  ### Purge All Cached Content

                  Removes ALL files from Cloudflare's cache. All tiers can purge
                  everything.


                  ### Purge Cached Content by URL

                  Granularly removes one or more files from Cloudflare's cache
                  by specifying URLs. All tiers can purge by URL.


                  To purge files with custom cache keys, include the headers
                  used to compute the cache key as in the example. If you have a
                  device type or geo in your cache key, you will need to include
                  the CF-Device-Type or CF-IPCountry headers. If you have lang
                  in your cache key, you will need to include the
                  Accept-Language header.


                  **NB:** When including the Origin header, be sure to include
                  the **scheme** and **hostname**. The port number can be
                  omitted if it is the default port (80 for http, 443 for
                  https), but must be included otherwise.


                  ### Purge Cached Content by Tag, Host or Prefix

                  Granularly removes one or more files from Cloudflare's cache
                  either by specifying the host, the associated Cache-Tag, or a
                  Prefix. Only Enterprise customers are permitted to purge by
                  Tag, Host or Prefix.


                  **NB:** Cache-Tag, host, and prefix purging each have a rate
                  limit of 30,000 purge API calls in every 24 hour period. You
                  may purge up to 30 tags, hosts, or prefixes in one API call.
                  This rate limit can be raised for customers who need to purge
                  at higher volume.
            /zones/{zone_id}/rulesets:
              get:
                tags:
                  - Zone Rulesets
                summary: List zone rulesets
                description: Fetches all rulesets at the zone level.
              post:
                tags:
                  - Zone Rulesets
                summary: Create a zone ruleset
                description: Creates a ruleset at the zone level.
            /zones/{zone_id}/rulesets/{ruleset_id}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset
                description: Deletes all versions of an existing zone ruleset.
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone ruleset
                description: Fetches the latest version of a zone ruleset.
              put:
                tags:
                  - Zone Rulesets
                summary: Update a zone ruleset
                description: Updates a zone ruleset, creating a new version.
            /zones/{zone_id}/rulesets/{ruleset_id}/rules:
              post:
                tags:
                  - Zone Rulesets
                summary: Create a zone ruleset rule
                description: >-
                  Adds a new rule to a zone ruleset. The rule will be added to
                  the end of the existing list of rules in the ruleset by
                  default.
            /zones/{zone_id}/rulesets/{ruleset_id}/rules/{rule_id}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset rule
                description: Deletes an existing rule from a zone ruleset.
              patch:
                tags:
                  - Zone Rulesets
                summary: Update a zone ruleset rule
                description: Updates an existing rule in a zone ruleset.
            /zones/{zone_id}/rulesets/{ruleset_id}/versions:
              get:
                tags:
                  - Zone Rulesets
                summary: List a zone ruleset's versions
                description: Fetches the versions of a zone ruleset.
            /zones/{zone_id}/rulesets/{ruleset_id}/versions/{ruleset_version}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset version
                description: Deletes an existing version of a zone ruleset.
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone ruleset version
                description: Fetches a specific version of a zone ruleset.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint:
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone entry point ruleset
                description: >-
                  Fetches the latest version of the zone entry point ruleset for
                  a given phase.
              put:
                tags:
                  - Zone Rulesets
                summary: Update a zone entry point ruleset
                description: Updates a zone entry point ruleset, creating a new version.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions:
              get:
                tags:
                  - Zone Rulesets
                summary: List a zone entry point ruleset's versions
                description: Fetches the versions of a zone entry point ruleset.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions/{ruleset_version}:
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone entry point ruleset version
                description: Fetches a specific version of a zone entry point ruleset.
            /zones/{zone_id}/secondary_dns/force_axfr:
              post:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Force AXFR
                description: Sends AXFR zone transfer request to primary nameserver(s).
            /zones/{zone_id}/secondary_dns/incoming:
              delete:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Delete Secondary Zone Configuration
                description: >-
                  Delete secondary zone configuration for incoming zone
                  transfers.
              get:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Secondary Zone Configuration Details
                description: Get secondary zone configuration for incoming zone transfers.
              post:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Create Secondary Zone Configuration
                description: >-
                  Create secondary zone configuration for incoming zone
                  transfers.
              put:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Update Secondary Zone Configuration
                description: >-
                  Update secondary zone configuration for incoming zone
                  transfers.
            /zones/{zone_id}/secondary_dns/outgoing:
              delete:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Delete Primary Zone Configuration
                description: Delete primary zone configuration for outgoing zone transfers.
              get:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Primary Zone Configuration Details
                description: Get primary zone configuration for outgoing zone transfers.
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Create Primary Zone Configuration
                description: Create primary zone configuration for outgoing zone transfers.
              put:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Update Primary Zone Configuration
                description: Update primary zone configuration for outgoing zone transfers.
            /zones/{zone_id}/secondary_dns/outgoing/disable:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Disable Outgoing Zone Transfers
                description: >-
                  Disable outgoing zone transfers for primary zone and clears
                  IXFR backlog of primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/enable:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Enable Outgoing Zone Transfers
                description: Enable outgoing zone transfers for primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/force_notify:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Force DNS NOTIFY
                description: >-
                  Notifies the secondary nameserver(s) and clears IXFR backlog
                  of primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/status:
              get:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Get Outgoing Zone Transfer Status
                description: Get primary zone transfer status.
            /zones/{zone_id}/settings:
              get:
                tags:
                  - Zone Settings
                summary: Get all Zone settings
                description: Available settings for your user in relation to a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Edit zone settings info
                description: Edit settings for a zone.
            /zones/{zone_id}/settings/0rtt:
              get:
                tags:
                  - Zone Settings
                summary: Get 0-RTT session resumption setting
                description: Gets 0-RTT session resumption setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change 0-RTT session resumption setting
                description: Changes the 0-RTT session resumption setting.
            /zones/{zone_id}/settings/advanced_ddos:
              get:
                tags:
                  - Zone Settings
                summary: Get Advanced DDOS setting
                description: >-
                  Advanced protection from Distributed Denial of Service (DDoS)
                  attacks on your website. This is an uneditable value that is
                  'on' in the case of Business and Enterprise zones.
            /zones/{zone_id}/settings/always_online:
              get:
                tags:
                  - Zone Settings
                summary: Get Always Online setting
                description: >-
                  When enabled, Cloudflare serves limited copies of web pages
                  available from the [Internet Archive's Wayback
                  Machine](https://archive.org/web/) if your server is offline.
                  Refer to [Always
                  Online](https://developers.cloudflare.com/cache/about/always-online)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Always Online setting
                description: >-
                  When enabled, Cloudflare serves limited copies of web pages
                  available from the [Internet Archive's Wayback
                  Machine](https://archive.org/web/) if your server is offline.
                  Refer to [Always
                  Online](https://developers.cloudflare.com/cache/about/always-online)
                  for more information.
            /zones/{zone_id}/settings/always_use_https:
              get:
                tags:
                  - Zone Settings
                summary: Get Always Use HTTPS setting
                description: >-
                  Reply to all requests for URLs that use "http" with a 301
                  redirect to the equivalent "https" URL. If you only want to
                  redirect for a subset of requests, consider creating an
                  "Always use HTTPS" page rule.
              patch:
                tags:
                  - Zone Settings
                summary: Change Always Use HTTPS setting
                description: >-
                  Reply to all requests for URLs that use "http" with a 301
                  redirect to the equivalent "https" URL. If you only want to
                  redirect for a subset of requests, consider creating an
                  "Always use HTTPS" page rule.
            /zones/{zone_id}/settings/automatic_https_rewrites:
              get:
                tags:
                  - Zone Settings
                summary: Get Automatic HTTPS Rewrites setting
                description: Enable the Automatic HTTPS Rewrites feature for this zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change Automatic HTTPS Rewrites setting
                description: Enable the Automatic HTTPS Rewrites feature for this zone.
            /zones/{zone_id}/settings/automatic_platform_optimization:
              get:
                tags:
                  - Zone Settings
                summary: Get Automatic Platform Optimization for WordPress setting
                description: >
                  [Automatic Platform Optimization for
                  WordPress](https://developers.cloudflare.com/automatic-platform-optimization/)

                  serves your WordPress site from Cloudflare's edge network and
                  caches

                  third-party fonts.
              patch:
                tags:
                  - Zone Settings
                summary: Change Automatic Platform Optimization for WordPress setting
                description: >
                  [Automatic Platform Optimization for
                  WordPress](https://developers.cloudflare.com/automatic-platform-optimization/)

                  serves your WordPress site from Cloudflare's edge network and
                  caches

                  third-party fonts.
            /zones/{zone_id}/settings/brotli:
              get:
                tags:
                  - Zone Settings
                summary: Get Brotli setting
                description: >-
                  When the client requesting an asset supports the Brotli
                  compression algorithm, Cloudflare will serve a Brotli
                  compressed version of the asset.
              patch:
                tags:
                  - Zone Settings
                summary: Change Brotli setting
                description: >-
                  When the client requesting an asset supports the Brotli
                  compression algorithm, Cloudflare will serve a Brotli
                  compressed version of the asset.
            /zones/{zone_id}/settings/browser_cache_ttl:
              get:
                tags:
                  - Zone Settings
                summary: Get Browser Cache TTL setting
                description: >-
                  Browser Cache TTL (in seconds) specifies how long
                  Cloudflare-cached resources will remain on your visitors'
                  computers. Cloudflare will honor any larger times specified by
                  your server.
                  (https://support.cloudflare.com/hc/en-us/articles/200168276).
              patch:
                tags:
                  - Zone Settings
                summary: Change Browser Cache TTL setting
                description: >-
                  Browser Cache TTL (in seconds) specifies how long
                  Cloudflare-cached resources will remain on your visitors'
                  computers. Cloudflare will honor any larger times specified by
                  your server.
                  (https://support.cloudflare.com/hc/en-us/articles/200168276).
            /zones/{zone_id}/settings/browser_check:
              get:
                tags:
                  - Zone Settings
                summary: Get Browser Check setting
                description: >-
                  Browser Integrity Check is similar to Bad Behavior and looks
                  for common HTTP headers abused most commonly by spammers and
                  denies access to your page.  It will also challenge visitors
                  that do not have a user agent or a non standard user agent
                  (also commonly used by abuse bots, crawlers or visitors).
                  (https://support.cloudflare.com/hc/en-us/articles/200170086).
              patch:
                tags:
                  - Zone Settings
                summary: Change Browser Check setting
                description: >-
                  Browser Integrity Check is similar to Bad Behavior and looks
                  for common HTTP headers abused most commonly by spammers and
                  denies access to your page.  It will also challenge visitors
                  that do not have a user agent or a non standard user agent
                  (also commonly used by abuse bots, crawlers or visitors).
                  (https://support.cloudflare.com/hc/en-us/articles/200170086).
            /zones/{zone_id}/settings/cache_level:
              get:
                tags:
                  - Zone Settings
                summary: Get Cache Level setting
                description: >-
                  Cache Level functions based off the setting level. The basic
                  setting will cache most static resources (i.e., css, images,
                  and JavaScript). The simplified setting will ignore the query
                  string when delivering a cached resource. The aggressive
                  setting will cache all static resources, including ones with a
                  query string.
                  (https://support.cloudflare.com/hc/en-us/articles/200168256).
              patch:
                tags:
                  - Zone Settings
                summary: Change Cache Level setting
                description: >-
                  Cache Level functions based off the setting level. The basic
                  setting will cache most static resources (i.e., css, images,
                  and JavaScript). The simplified setting will ignore the query
                  string when delivering a cached resource. The aggressive
                  setting will cache all static resources, including ones with a
                  query string.
                  (https://support.cloudflare.com/hc/en-us/articles/200168256).
            /zones/{zone_id}/settings/challenge_ttl:
              get:
                tags:
                  - Zone Settings
                summary: Get Challenge TTL setting
                description: >-
                  Specify how long a visitor is allowed access to your site
                  after successfully completing a challenge (such as a CAPTCHA).
                  After the TTL has expired the visitor will have to complete a
                  new challenge. We recommend a 15 - 45 minute setting and will
                  attempt to honor any setting above 45 minutes.
                  (https://support.cloudflare.com/hc/en-us/articles/200170136).
              patch:
                tags:
                  - Zone Settings
                summary: Change Challenge TTL setting
                description: >-
                  Specify how long a visitor is allowed access to your site
                  after successfully completing a challenge (such as a CAPTCHA).
                  After the TTL has expired the visitor will have to complete a
                  new challenge. We recommend a 15 - 45 minute setting and will
                  attempt to honor any setting above 45 minutes.
                  (https://support.cloudflare.com/hc/en-us/articles/200170136).
            /zones/{zone_id}/settings/ciphers:
              get:
                tags:
                  - Zone Settings
                summary: Get ciphers setting
                description: Gets ciphers setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change ciphers setting
                description: Changes ciphers setting.
            /zones/{zone_id}/settings/development_mode:
              get:
                tags:
                  - Zone Settings
                summary: Get Development Mode setting
                description: >-
                  Development Mode temporarily allows you to enter development
                  mode for your websites if you need to make changes to your
                  site. This will bypass Cloudflare's accelerated cache and slow
                  down your site, but is useful if you are making changes to
                  cacheable content (like images, css, or JavaScript) and would
                  like to see those changes right away. Once entered,
                  development mode will last for 3 hours and then automatically
                  toggle off.
              patch:
                tags:
                  - Zone Settings
                summary: Change Development Mode setting
                description: >-
                  Development Mode temporarily allows you to enter development
                  mode for your websites if you need to make changes to your
                  site. This will bypass Cloudflare's accelerated cache and slow
                  down your site, but is useful if you are making changes to
                  cacheable content (like images, css, or JavaScript) and would
                  like to see those changes right away. Once entered,
                  development mode will last for 3 hours and then automatically
                  toggle off.
            /zones/{zone_id}/settings/early_hints:
              get:
                tags:
                  - Zone Settings
                summary: Get Early Hints setting
                description: >-
                  When enabled, Cloudflare will attempt to speed up overall page
                  loads by serving `103` responses with `Link` headers from the
                  final response. Refer to [Early
                  Hints](https://developers.cloudflare.com/cache/about/early-hints)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Early Hints setting
                description: >-
                  When enabled, Cloudflare will attempt to speed up overall page
                  loads by serving `103` responses with `Link` headers from the
                  final response. Refer to [Early
                  Hints](https://developers.cloudflare.com/cache/about/early-hints)
                  for more information.
            /zones/{zone_id}/settings/email_obfuscation:
              get:
                tags:
                  - Zone Settings
                summary: Get Email Obfuscation setting
                description: >-
                  Encrypt email adresses on your web page from bots, while
                  keeping them visible to humans.
                  (https://support.cloudflare.com/hc/en-us/articles/200170016).
              patch:
                tags:
                  - Zone Settings
                summary: Change Email Obfuscation setting
                description: >-
                  Encrypt email adresses on your web page from bots, while
                  keeping them visible to humans.
                  (https://support.cloudflare.com/hc/en-us/articles/200170016).
            /zones/{zone_id}/settings/fonts:
              get:
                tags:
                  - Zone Settings
                summary: Get Cloudflare Fonts setting
                description: >
                  Enhance your website's font delivery with Cloudflare Fonts.
                  Deliver Google Hosted fonts from your own domain,

                  boost performance, and enhance user privacy. Refer to the
                  Cloudflare Fonts documentation for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Cloudflare Fonts setting
                description: >
                  Enhance your website's font delivery with Cloudflare Fonts.
                  Deliver Google Hosted fonts from your own domain,

                  boost performance, and enhance user privacy. Refer to the
                  Cloudflare Fonts documentation for more information.
            /zones/{zone_id}/settings/h2_prioritization:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP/2 Edge Prioritization setting
                description: |
                  Gets HTTP/2 Edge Prioritization setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP/2 Edge Prioritization setting
                description: |
                  Gets HTTP/2 Edge Prioritization setting.
            /zones/{zone_id}/settings/hotlink_protection:
              get:
                tags:
                  - Zone Settings
                summary: Get Hotlink Protection setting
                description: >-
                  When enabled, the Hotlink Protection option ensures that other
                  sites cannot suck up your bandwidth by building pages that use
                  images hosted on your site. Anytime a request for an image on
                  your site hits Cloudflare, we check to ensure that it's not
                  another site requesting them. People will still be able to
                  download and view images from your page, but other sites won't
                  be able to steal them for use on their own pages.
                  (https://support.cloudflare.com/hc/en-us/articles/200170026).
              patch:
                tags:
                  - Zone Settings
                summary: Change Hotlink Protection setting
                description: >-
                  When enabled, the Hotlink Protection option ensures that other
                  sites cannot suck up your bandwidth by building pages that use
                  images hosted on your site. Anytime a request for an image on
                  your site hits Cloudflare, we check to ensure that it's not
                  another site requesting them. People will still be able to
                  download and view images from your page, but other sites won't
                  be able to steal them for use on their own pages.
                  (https://support.cloudflare.com/hc/en-us/articles/200170026).
            /zones/{zone_id}/settings/http2:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP2 setting
                description: Value of the HTTP2 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP2 setting
                description: Value of the HTTP2 setting.
            /zones/{zone_id}/settings/http3:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP3 setting
                description: Value of the HTTP3 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP3 setting
                description: Value of the HTTP3 setting.
            /zones/{zone_id}/settings/image_resizing:
              get:
                tags:
                  - Zone Settings
                summary: Get Image Resizing setting
                description: >
                  Image Resizing provides on-demand resizing, conversion and
                  optimisation

                  for images served through Cloudflare's network. Refer to the

                  [Image Resizing
                  documentation](https://developers.cloudflare.com/images/)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Image Resizing setting
                description: >
                  Image Resizing provides on-demand resizing, conversion and
                  optimisation

                  for images served through Cloudflare's network. Refer to the

                  [Image Resizing
                  documentation](https://developers.cloudflare.com/images/)

                  for more information.
            /zones/{zone_id}/settings/ip_geolocation:
              get:
                tags:
                  - Zone Settings
                summary: Get IP Geolocation setting
                description: >-
                  Enable IP Geolocation to have Cloudflare geolocate visitors to
                  your website and pass the country code to you.
                  (https://support.cloudflare.com/hc/en-us/articles/200168236).
              patch:
                tags:
                  - Zone Settings
                summary: Change IP Geolocation setting
                description: >-
                  Enable IP Geolocation to have Cloudflare geolocate visitors to
                  your website and pass the country code to you.
                  (https://support.cloudflare.com/hc/en-us/articles/200168236).
            /zones/{zone_id}/settings/ipv6:
              get:
                tags:
                  - Zone Settings
                summary: Get IPv6 setting
                description: >-
                  Enable IPv6 on all subdomains that are Cloudflare enabled. 
                  (https://support.cloudflare.com/hc/en-us/articles/200168586).
              patch:
                tags:
                  - Zone Settings
                summary: Change IPv6 setting
                description: >-
                  Enable IPv6 on all subdomains that are Cloudflare enabled. 
                  (https://support.cloudflare.com/hc/en-us/articles/200168586).
            /zones/{zone_id}/settings/min_tls_version:
              get:
                tags:
                  - Zone Settings
                summary: Get Minimum TLS Version setting
                description: Gets Minimum TLS Version setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Minimum TLS Version setting
                description: Changes Minimum TLS Version setting.
            /zones/{zone_id}/settings/minify:
              get:
                tags:
                  - Zone Settings
                summary: Get Minify setting
                description: >-
                  Automatically minify certain assets for your website. Refer to
                  [Using Cloudflare Auto
                  Minify](https://support.cloudflare.com/hc/en-us/articles/200168196)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Minify setting
                description: >-
                  Automatically minify certain assets for your website. Refer to
                  [Using Cloudflare Auto
                  Minify](https://support.cloudflare.com/hc/en-us/articles/200168196)
                  for more information.
            /zones/{zone_id}/settings/mirage:
              get:
                tags:
                  - Zone Settings
                summary: Get Mirage setting
                description: >
                  Automatically optimize image loading for website visitors on
                  mobile

                  devices. Refer to our [blog
                  post](http://blog.cloudflare.com/mirage2-solving-mobile-speed)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Mirage setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/mirage2-solving-mobile-speed)
                  for more information.
            /zones/{zone_id}/settings/mobile_redirect:
              get:
                tags:
                  - Zone Settings
                summary: Get Mobile Redirect setting
                description: >-
                  Automatically redirect visitors on mobile devices to a
                  mobile-optimized subdomain. Refer to [Understanding Cloudflare
                  Mobile
                  Redirect](https://support.cloudflare.com/hc/articles/200168336)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Mobile Redirect setting
                description: >-
                  Automatically redirect visitors on mobile devices to a
                  mobile-optimized subdomain. Refer to [Understanding Cloudflare
                  Mobile
                  Redirect](https://support.cloudflare.com/hc/articles/200168336)
                  for more information.
            /zones/{zone_id}/settings/nel:
              get:
                tags:
                  - Zone Settings
                summary: Get Network Error Logging setting
                description: |
                  Enable Network Error Logging reporting on your zone. (Beta)
              patch:
                tags:
                  - Zone Settings
                summary: Change Network Error Logging setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/nel-solving-mobile-speed) for
                  more information.
            /zones/{zone_id}/settings/opportunistic_encryption:
              get:
                tags:
                  - Zone Settings
                summary: Get Opportunistic Encryption setting
                description: Gets Opportunistic Encryption setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Opportunistic Encryption setting
                description: Changes Opportunistic Encryption setting.
            /zones/{zone_id}/settings/opportunistic_onion:
              get:
                tags:
                  - Zone Settings
                summary: Get Opportunistic Onion setting
                description: >-
                  Add an Alt-Svc header to all legitimate requests from Tor,
                  allowing the connection to use our onion services instead of
                  exit nodes.
              patch:
                tags:
                  - Zone Settings
                summary: Change Opportunistic Onion setting
                description: >-
                  Add an Alt-Svc header to all legitimate requests from Tor,
                  allowing the connection to use our onion services instead of
                  exit nodes.
            /zones/{zone_id}/settings/orange_to_orange:
              get:
                tags:
                  - Zone Settings
                summary: Get Orange to Orange (O2O) setting
                description: >
                  Orange to Orange (O2O) allows zones on Cloudflare to CNAME to
                  other

                  zones also on Cloudflare.
              patch:
                tags:
                  - Zone Settings
                summary: Change Orange to Orange (O2O) setting
                description: >
                  Orange to Orange (O2O) allows zones on Cloudflare to CNAME to
                  other

                  zones also on Cloudflare.
            /zones/{zone_id}/settings/origin_error_page_pass_thru:
              get:
                tags:
                  - Zone Settings
                summary: Get Enable Error Pages On setting
                description: >-
                  Cloudflare will proxy customer error pages on any 502,504
                  errors on origin server instead of showing a default
                  Cloudflare error page. This does not apply to 522 errors and
                  is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Enable Error Pages On setting
                description: >-
                  Cloudflare will proxy customer error pages on any 502,504
                  errors on origin server instead of showing a default
                  Cloudflare error page. This does not apply to 522 errors and
                  is limited to Enterprise Zones.
            /zones/{zone_id}/settings/origin_max_http_version:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Origin Max HTTP Version Setting
                description: >-
                  Origin Max HTTP Setting Version sets the highest HTTP version
                  Cloudflare will attempt to use with your origin. This setting
                  allows Cloudflare to make HTTP/2 requests to your origin.
                  (Refer to [Enable HTTP/2 to
                  Origin](https://developers.cloudflare.com/cache/how-to/enable-http2-to-origin/),
                  for more information.). The default value is "2" for all plan
                  types except ENT where it is "1"
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Origin Max HTTP Version Setting
                description: >-
                  Origin Max HTTP Setting Version sets the highest HTTP version
                  Cloudflare will attempt to use with your origin. This setting
                  allows Cloudflare to make HTTP/2 requests to your origin.
                  (Refer to [Enable HTTP/2 to
                  Origin](https://developers.cloudflare.com/cache/how-to/enable-http2-to-origin/),
                  for more information.). The default value is "2" for all plan
                  types except ENT where it is "1"
            /zones/{zone_id}/settings/polish:
              get:
                tags:
                  - Zone Settings
                summary: Get Polish setting
                description: >
                  Automatically optimize image loading for website visitors on
                  mobile

                  devices. Refer to our [blog
                  post](http://blog.cloudflare.com/polish-solving-mobile-speed)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Polish setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/polish-solving-mobile-speed)
                  for more information.
            /zones/{zone_id}/settings/prefetch_preload:
              get:
                tags:
                  - Zone Settings
                summary: Get prefetch preload setting
                description: >-
                  Cloudflare will prefetch any URLs that are included in the
                  response headers. This is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change prefetch preload setting
                description: >-
                  Cloudflare will prefetch any URLs that are included in the
                  response headers. This is limited to Enterprise Zones.
            /zones/{zone_id}/settings/proxy_read_timeout:
              get:
                tags:
                  - Zone Settings
                summary: Get Proxy Read Timeout setting
                description: |
                  Maximum time between two read operations from origin.
              patch:
                tags:
                  - Zone Settings
                summary: Change Proxy Read Timeout setting
                description: |
                  Maximum time between two read operations from origin.
            /zones/{zone_id}/settings/pseudo_ipv4:
              get:
                tags:
                  - Zone Settings
                summary: Get Pseudo IPv4 setting
                description: Value of the Pseudo IPv4 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Pseudo IPv4 setting
                description: Value of the Pseudo IPv4 setting.
            /zones/{zone_id}/settings/response_buffering:
              get:
                tags:
                  - Zone Settings
                summary: Get Response Buffering setting
                description: >-
                  Enables or disables buffering of responses from the proxied
                  server. Cloudflare may buffer the whole payload to deliver it
                  at once to the client versus allowing it to be delivered in
                  chunks. By default, the proxied server streams directly and is
                  not buffered by Cloudflare. This is limited to Enterprise
                  Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Response Buffering setting
                description: >-
                  Enables or disables buffering of responses from the proxied
                  server. Cloudflare may buffer the whole payload to deliver it
                  at once to the client versus allowing it to be delivered in
                  chunks. By default, the proxied server streams directly and is
                  not buffered by Cloudflare. This is limited to Enterprise
                  Zones.
            /zones/{zone_id}/settings/rocket_loader:
              get:
                tags:
                  - Zone Settings
                summary: Get Rocket Loader setting
                description: >
                  Rocket Loader is a general-purpose asynchronous JavaScript
                  optimisation

                  that prioritises rendering your content while loading your
                  site's

                  Javascript asynchronously. Turning on Rocket Loader will
                  immediately

                  improve a web page's rendering time sometimes measured as Time
                  to First

                  Paint (TTFP), and also the `window.onload` time (assuming
                  there is

                  JavaScript on the page). This can have a positive impact on
                  your Google

                  search ranking. When turned on, Rocket Loader will
                  automatically defer

                  the loading of all Javascript referenced in your HTML, with no

                  configuration required. Refer to

                  [Understanding Rocket
                  Loader](https://support.cloudflare.com/hc/articles/200168056)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Rocket Loader setting
                description: >
                  Rocket Loader is a general-purpose asynchronous JavaScript
                  optimisation

                  that prioritises rendering your content while loading your
                  site's

                  Javascript asynchronously. Turning on Rocket Loader will
                  immediately

                  improve a web page's rendering time sometimes measured as Time
                  to First

                  Paint (TTFP), and also the `window.onload` time (assuming
                  there is

                  JavaScript on the page). This can have a positive impact on
                  your Google

                  search ranking. When turned on, Rocket Loader will
                  automatically defer

                  the loading of all Javascript referenced in your HTML, with no

                  configuration required. Refer to

                  [Understanding Rocket
                  Loader](https://support.cloudflare.com/hc/articles/200168056)

                  for more information.
            /zones/{zone_id}/settings/security_header:
              get:
                tags:
                  - Zone Settings
                summary: Get Security Header (HSTS) setting
                description: Cloudflare security header for a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change Security Header (HSTS) setting
                description: Cloudflare security header for a zone.
            /zones/{zone_id}/settings/security_level:
              get:
                tags:
                  - Zone Settings
                summary: Get Security Level setting
                description: >-
                  Choose the appropriate security profile for your website,
                  which will automatically adjust each of the security settings.
                  If you choose to customize an individual security setting, the
                  profile will become Custom.
                  (https://support.cloudflare.com/hc/en-us/articles/200170056).
              patch:
                tags:
                  - Zone Settings
                summary: Change Security Level setting
                description: >-
                  Choose the appropriate security profile for your website,
                  which will automatically adjust each of the security settings.
                  If you choose to customize an individual security setting, the
                  profile will become Custom.
                  (https://support.cloudflare.com/hc/en-us/articles/200170056).
            /zones/{zone_id}/settings/server_side_exclude:
              get:
                tags:
                  - Zone Settings
                summary: Get Server Side Exclude setting
                description: >-
                  If there is sensitive content on your website that you want
                  visible to real visitors, but that you want to hide from
                  suspicious visitors, all you have to do is wrap the content
                  with Cloudflare SSE tags. Wrap any content that you want to be
                  excluded from suspicious visitors in the following SSE tags:
                  <!--sse--><!--/sse-->. For example: <!--sse-->  Bad visitors
                  won't see my phone number, 555-555-5555 <!--/sse-->. Note: SSE
                  only will work with HTML. If you have HTML minification
                  enabled, you won't see the SSE tags in your HTML source when
                  it's served through Cloudflare. SSE will still function in
                  this case, as Cloudflare's HTML minification and SSE
                  functionality occur on-the-fly as the resource moves through
                  our network to the visitor's computer.
                  (https://support.cloudflare.com/hc/en-us/articles/200170036).
              patch:
                tags:
                  - Zone Settings
                summary: Change Server Side Exclude setting
                description: >-
                  If there is sensitive content on your website that you want
                  visible to real visitors, but that you want to hide from
                  suspicious visitors, all you have to do is wrap the content
                  with Cloudflare SSE tags. Wrap any content that you want to be
                  excluded from suspicious visitors in the following SSE tags:
                  <!--sse--><!--/sse-->. For example: <!--sse-->  Bad visitors
                  won't see my phone number, 555-555-5555 <!--/sse-->. Note: SSE
                  only will work with HTML. If you have HTML minification
                  enabled, you won't see the SSE tags in your HTML source when
                  it's served through Cloudflare. SSE will still function in
                  this case, as Cloudflare's HTML minification and SSE
                  functionality occur on-the-fly as the resource moves through
                  our network to the visitor's computer.
                  (https://support.cloudflare.com/hc/en-us/articles/200170036).
            /zones/{zone_id}/settings/sort_query_string_for_cache:
              get:
                tags:
                  - Zone Settings
                summary: Get Enable Query String Sort setting
                description: >-
                  Cloudflare will treat files with the same query strings as the
                  same file in cache, regardless of the order of the query
                  strings. This is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Enable Query String Sort setting
                description: >-
                  Cloudflare will treat files with the same query strings as the
                  same file in cache, regardless of the order of the query
                  strings. This is limited to Enterprise Zones.
            /zones/{zone_id}/settings/ssl:
              get:
                tags:
                  - Zone Settings
                summary: Get SSL setting
                description: >-
                  SSL encrypts your visitor's connection and safeguards credit
                  card numbers and other personal data to and from your website.
                  SSL can take up to 5 minutes to fully activate. Requires
                  Cloudflare active on your root domain or www domain. Off: no
                  SSL between the visitor and Cloudflare, and no SSL between
                  Cloudflare and your web server  (all HTTP traffic). Flexible:
                  SSL between the visitor and Cloudflare -- visitor sees HTTPS
                  on your site, but no SSL between Cloudflare and your web
                  server. You don't need to have an SSL cert on your web server,
                  but your vistors will still see the site as being HTTPS
                  enabled. Full:  SSL between the visitor and Cloudflare --
                  visitor sees HTTPS on your site, and SSL between Cloudflare
                  and your web server. You'll need to have your own SSL cert or
                  self-signed cert at the very least. Full (Strict): SSL between
                  the visitor and Cloudflare -- visitor sees HTTPS on your site,
                  and SSL between Cloudflare and your web server. You'll need to
                  have a valid SSL certificate installed on your web server.
                  This certificate must be signed by a certificate authority,
                  have an expiration date in the future, and respond for the
                  request domain name (hostname).
                  (https://support.cloudflare.com/hc/en-us/articles/200170416).
              patch:
                tags:
                  - Zone Settings
                summary: Change SSL setting
                description: >-
                  SSL encrypts your visitor's connection and safeguards credit
                  card numbers and other personal data to and from your website.
                  SSL can take up to 5 minutes to fully activate. Requires
                  Cloudflare active on your root domain or www domain. Off: no
                  SSL between the visitor and Cloudflare, and no SSL between
                  Cloudflare and your web server  (all HTTP traffic). Flexible:
                  SSL between the visitor and Cloudflare -- visitor sees HTTPS
                  on your site, but no SSL between Cloudflare and your web
                  server. You don't need to have an SSL cert on your web server,
                  but your vistors will still see the site as being HTTPS
                  enabled. Full:  SSL between the visitor and Cloudflare --
                  visitor sees HTTPS on your site, and SSL between Cloudflare
                  and your web server. You'll need to have your own SSL cert or
                  self-signed cert at the very least. Full (Strict): SSL between
                  the visitor and Cloudflare -- visitor sees HTTPS on your site,
                  and SSL between Cloudflare and your web server. You'll need to
                  have a valid SSL certificate installed on your web server.
                  This certificate must be signed by a certificate authority,
                  have an expiration date in the future, and respond for the
                  request domain name (hostname).
                  (https://support.cloudflare.com/hc/en-us/articles/200170416).
            /zones/{zone_id}/settings/ssl_recommender:
              get:
                tags:
                  - Zone Settings
                summary: Get SSL/TLS Recommender enrollment setting
                description: >
                  Enrollment in the SSL/TLS Recommender service which tries to
                  detect and

                  recommend (by sending periodic emails) the most secure SSL/TLS
                  setting

                  your origin servers support.
              patch:
                tags:
                  - Zone Settings
                summary: Change SSL/TLS Recommender enrollment setting
                description: >
                  Enrollment in the SSL/TLS Recommender service which tries to
                  detect and

                  recommend (by sending periodic emails) the most secure SSL/TLS
                  setting

                  your origin servers support.
            /zones/{zone_id}/settings/tls_1_3:
              get:
                tags:
                  - Zone Settings
                summary: Get TLS 1.3 setting enabled for a zone
                description: Gets TLS 1.3 setting enabled for a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change TLS 1.3 setting
                description: Changes TLS 1.3 setting.
            /zones/{zone_id}/settings/tls_client_auth:
              get:
                tags:
                  - Zone Settings
                summary: Get TLS Client Auth setting
                description: >-
                  TLS Client Auth requires Cloudflare to connect to your origin
                  server using a client certificate (Enterprise Only).
              patch:
                tags:
                  - Zone Settings
                summary: Change TLS Client Auth setting
                description: >-
                  TLS Client Auth requires Cloudflare to connect to your origin
                  server using a client certificate (Enterprise Only).
            /zones/{zone_id}/settings/true_client_ip_header:
              get:
                tags:
                  - Zone Settings
                summary: Get True Client IP setting
                description: >-
                  Allows customer to continue to use True Client IP (Akamai
                  feature) in the headers we send to the origin. This is limited
                  to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change True Client IP setting
                description: >-
                  Allows customer to continue to use True Client IP (Akamai
                  feature) in the headers we send to the origin. This is limited
                  to Enterprise Zones.
            /zones/{zone_id}/settings/waf:
              get:
                tags:
                  - Zone Settings
                summary: Get Web Application Firewall (WAF) setting
                description: >-
                  The WAF examines HTTP requests to your website.  It inspects
                  both GET and POST requests and applies rules to help filter
                  out illegitimate traffic from legitimate website visitors. The
                  Cloudflare WAF inspects website addresses or URLs to detect
                  anything out of the ordinary. If the Cloudflare WAF determines
                  suspicious user behavior, then the WAF will 'challenge' the
                  web visitor with a page that asks them to submit a CAPTCHA
                  successfully  to continue their action. If the challenge is
                  failed, the action will be stopped. What this means is that
                  Cloudflare's WAF will block any traffic identified as
                  illegitimate before it reaches your origin web server.
                  (https://support.cloudflare.com/hc/en-us/articles/200172016).
              patch:
                tags:
                  - Zone Settings
                summary: Change Web Application Firewall (WAF) setting
                description: >-
                  The WAF examines HTTP requests to your website.  It inspects
                  both GET and POST requests and applies rules to help filter
                  out illegitimate traffic from legitimate website visitors. The
                  Cloudflare WAF inspects website addresses or URLs to detect
                  anything out of the ordinary. If the Cloudflare WAF determines
                  suspicious user behavior, then the WAF will 'challenge' the
                  web visitor with a page that asks them to submit a CAPTCHA
                  successfully  to continue their action. If the challenge is
                  failed, the action will be stopped. What this means is that
                  Cloudflare's WAF will block any traffic identified as
                  illegitimate before it reaches your origin web server.
                  (https://support.cloudflare.com/hc/en-us/articles/200172016).
            /zones/{zone_id}/settings/webp:
              get:
                tags:
                  - Zone Settings
                summary: Get WebP setting
                description: >-
                  When the client requesting the image supports the WebP image
                  codec, and WebP offers a performance advantage over the
                  original image format, Cloudflare will serve a WebP version of
                  the original image.
              patch:
                tags:
                  - Zone Settings
                summary: Change WebP setting
                description: >-
                  When the client requesting the image supports the WebP image
                  codec, and WebP offers a performance advantage over the
                  original image format, Cloudflare will serve a WebP version of
                  the original image.
            /zones/{zone_id}/settings/websockets:
              get:
                tags:
                  - Zone Settings
                summary: Get WebSockets setting
                description: >-
                  Gets Websockets setting. For more information about
                  Websockets, please refer to [Using Cloudflare with
                  WebSockets](https://support.cloudflare.com/hc/en-us/articles/200169466-Using-Cloudflare-with-WebSockets).
              patch:
                tags:
                  - Zone Settings
                summary: Change WebSockets setting
                description: >-
                  Changes Websockets setting. For more information about
                  Websockets, please refer to [Using Cloudflare with
                  WebSockets](https://support.cloudflare.com/hc/en-us/articles/200169466-Using-Cloudflare-with-WebSockets).
            /zones/{zone_id}/settings/zaraz/config:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz configuration
                description: >-
                  Gets latest Zaraz configuration for a zone. It can be preview
                  or published configuration, whichever was the last updated.
                  Secret variables values will not be included.
              put:
                tags:
                  - Zaraz
                summary: Update Zaraz configuration
                description: Updates Zaraz configuration for a zone.
            /zones/{zone_id}/settings/zaraz/default:
              get:
                tags:
                  - Zaraz
                summary: Get default Zaraz configuration
                description: Gets default Zaraz configuration for a zone.
            /zones/{zone_id}/settings/zaraz/export:
              get:
                tags:
                  - Zaraz
                summary: Export Zaraz configuration
                description: >-
                  Exports full current published Zaraz configuration for a zone,
                  secret variables included.
            /zones/{zone_id}/settings/zaraz/history:
              get:
                tags:
                  - Zaraz
                summary: List Zaraz historical configuration records
                description: >-
                  Lists a history of published Zaraz configuration records for a
                  zone.
              put:
                tags:
                  - Zaraz
                summary: Restore Zaraz historical configuration by ID
                description: >-
                  Restores a historical published Zaraz configuration by ID for
                  a zone.
            /zones/{zone_id}/settings/zaraz/history/configs:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz historical configurations by ID(s)
                description: >-
                  Gets a history of published Zaraz configurations by ID(s) for
                  a zone.
            /zones/{zone_id}/settings/zaraz/publish:
              post:
                tags:
                  - Zaraz
                summary: Publish Zaraz preview configuration
                description: Publish current Zaraz preview configuration for a zone.
            /zones/{zone_id}/settings/zaraz/workflow:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz workflow
                description: Gets Zaraz workflow for a zone.
              put:
                tags:
                  - Zaraz
                summary: Update Zaraz workflow
                description: Updates Zaraz workflow for a zone.
            /zones/{zone_id}/speed_api/availabilities:
              get:
                tags:
                  - Observatory
                summary: Get quota and availability
                description: >-
                  Retrieves quota for all plans, as well as the current zone
                  quota.
            /zones/{zone_id}/speed_api/pages:
              get:
                tags:
                  - Observatory
                summary: List tested webpages
                description: Lists all webpages which have been tested.
            /zones/{zone_id}/speed_api/pages/{url}/tests:
              delete:
                tags:
                  - Observatory
                summary: Delete all page tests
                description: >-
                  Deletes all tests for a specific webpage from a specific
                  region. Deleted tests are still counted as part of the quota.
              get:
                tags:
                  - Observatory
                summary: List page test history
                description: Test history (list of tests) for a specific webpage.
              post:
                tags:
                  - Observatory
                summary: Start page test
                description: Starts a test for a specific webpage, in a specific region.
            /zones/{zone_id}/speed_api/pages/{url}/tests/{test_id}:
              get:
                tags:
                  - Observatory
                summary: Get a page test result
                description: Retrieves the result of a specific test.
            /zones/{zone_id}/speed_api/pages/{url}/trend:
              get:
                tags:
                  - Observatory
                summary: List core web vital metrics trend
                description: >-
                  Lists the core web vital metrics trend over time for a
                  specific page.
            /zones/{zone_id}/speed_api/schedule/{url}:
              delete:
                tags:
                  - Observatory
                summary: Delete scheduled page test
                description: Deletes a scheduled test for a page.
              get:
                tags:
                  - Observatory
                summary: Get a page test schedule
                description: Retrieves the test schedule for a page in a specific region.
              post:
                tags:
                  - Observatory
                summary: Create scheduled page test
                description: Creates a scheduled test for a page.
            /zones/{zone_id}/ssl/analyze:
              post:
                tags:
                  - Analyze Certificate
                summary: Analyze Certificate
                description: >-
                  Returns the set of hostnames, the signature algorithm, and the
                  expiration date of the certificate.
            /zones/{zone_id}/ssl/certificate_packs:
              get:
                tags:
                  - Certificate Packs
                summary: List Certificate Packs
                description: For a given zone, list all active certificate packs.
            /zones/{zone_id}/ssl/certificate_packs/{certificate_pack_id}:
              delete:
                tags:
                  - Certificate Packs
                summary: Delete Advanced Certificate Manager Certificate Pack
                description: For a given zone, delete an advanced certificate pack.
              get:
                tags:
                  - Certificate Packs
                summary: Get Certificate Pack
                description: For a given zone, get a certificate pack.
              patch:
                tags:
                  - Certificate Packs
                summary: >-
                  Restart Validation for Advanced Certificate Manager
                  Certificate Pack
                description: >-
                  For a given zone, restart validation for an advanced
                  certificate pack.  This is only a validation operation for a
                  Certificate Pack in a validation_timed_out status.
            /zones/{zone_id}/ssl/certificate_packs/order:
              post:
                tags:
                  - Certificate Packs
                summary: Order Advanced Certificate Manager Certificate Pack
                description: For a given zone, order an advanced certificate pack.
            /zones/{zone_id}/ssl/certificate_packs/quota:
              get:
                tags:
                  - Certificate Packs
                summary: Get Certificate Pack Quotas
                description: For a given zone, list certificate pack quotas.
            /zones/{zone_id}/ssl/universal/settings:
              get:
                tags:
                  - Universal SSL Settings for a Zone
                summary: Universal SSL Settings Details
                description: Get Universal SSL Settings for a Zone.
              patch:
                tags:
                  - Universal SSL Settings for a Zone
                summary: Edit Universal SSL Settings
                description: Patch Universal SSL Settings for a Zone.
            /zones/{zone_id}/ssl/verification:
              get:
                tags:
                  - SSL Verification
                summary: SSL Verification Details
                description: Get SSL Verification Info for a Zone.
            /zones/{zone_id}/ssl/verification/{certificate_pack_id}:
              patch:
                tags:
                  - SSL Verification
                summary: Edit SSL Certificate Pack Validation Method
                description: >-
                  Edit SSL validation method for a certificate pack. A PATCH
                  request will request an immediate validation check on any
                  certificate, and return the updated status. If a validation
                  method is provided, the validation will be immediately
                  attempted using that method.
            /zones/{zone_id}/url_normalization:
              get:
                tags:
                  - URL Normalization
                summary: Get URL normalization settings
                description: Fetches the current URL normalization settings.
              put:
                tags:
                  - URL Normalization
                summary: Update URL normalization settings
                description: Updates the URL normalization settings.
            /zones/{zone_id}/workers/filters:
              get:
                tags:
                  - Worker Filters (Deprecated)
                summary: List Filters
              post:
                tags:
                  - Worker Filters (Deprecated)
                summary: Create Filter
            /zones/{zone_id}/workers/filters/{filter_id}:
              delete:
                tags:
                  - Worker Filters (Deprecated)
                summary: Delete Filter
              put:
                tags:
                  - Worker Filters (Deprecated)
                summary: Update Filter
            /zones/{zone_id}/workers/routes:
              get:
                tags:
                  - Worker Routes
                summary: List Routes
                description: Returns routes for a zone.
              post:
                tags:
                  - Worker Routes
                summary: Create Route
                description: Creates a route that maps a URL pattern to a Worker.
            /zones/{zone_id}/workers/routes/{route_id}:
              delete:
                tags:
                  - Worker Routes
                summary: Delete Route
                description: Deletes a route.
              get:
                tags:
                  - Worker Routes
                summary: Get Route
                description: >-
                  Returns information about a route, including URL pattern and
                  Worker.
              put:
                tags:
                  - Worker Routes
                summary: Update Route
                description: Updates the URL pattern or Worker associated with a route.
            /zones/{zone_id}/workers/script:
              delete:
                tags:
                  - Worker Script (Deprecated)
                summary: Delete Worker
                description: >-
                  Delete your Worker. This call has no response body on a
                  successful delete.
              get:
                tags:
                  - Worker Script (Deprecated)
                summary: Download Worker
                description: >-
                  Fetch raw script content for your worker. Note this is the
                  original script content, not JSON encoded.
              put:
                tags:
                  - Worker Script (Deprecated)
                summary: Upload Worker
                description: Upload a worker, or a new version of a worker.
            /zones/{zone_id}/workers/script/bindings:
              get:
                tags:
                  - Worker Binding (Deprecated)
                summary: List Bindings
                description: List the bindings for a Workers script.
            /zones/{zone_identifier}/analytics/colos:
              get:
                tags:
                  - Zone Analytics (Deprecated)
                summary: Get analytics by Co-locations
                description: >-
                  This view provides a breakdown of analytics data by
                  datacenter. Note: This is available to Enterprise customers
                  only.
            /zones/{zone_identifier}/analytics/dashboard:
              get:
                tags:
                  - Zone Analytics (Deprecated)
                summary: Get dashboard
                description: >-
                  The dashboard view provides both totals and timeseries data
                  for the given zone and time period across the entire
                  Cloudflare network.
            /zones/{zone_identifier}/available_plans:
              get:
                tags:
                  - Zone Rate Plan
                summary: List Available Plans
                description: Lists available plans the zone can subscribe to.
            /zones/{zone_identifier}/available_plans/{plan_identifier}:
              get:
                tags:
                  - Zone Rate Plan
                summary: Available Plan Details
                description: Details of the available plan that the zone can subscribe to.
            /zones/{zone_identifier}/available_rate_plans:
              get:
                tags:
                  - Zone Rate Plan
                summary: List Available Rate Plans
                description: Lists all rate plans the zone can subscribe to.
            /zones/{zone_identifier}/custom_pages:
              get:
                tags:
                  - Custom pages for a zone
                summary: List custom pages
                description: Fetches all the custom pages at the zone level.
            /zones/{zone_identifier}/custom_pages/{identifier}:
              get:
                tags:
                  - Custom pages for a zone
                summary: Get a custom page
                description: Fetches the details of a custom page.
              put:
                tags:
                  - Custom pages for a zone
                summary: Update a custom page
                description: Updates the configuration of an existing custom page.
            /zones/{zone_identifier}/email/routing:
              get:
                tags:
                  - Email Routing settings
                summary: Get Email Routing settings
                description: >-
                  Get information about the settings for your Email Routing
                  zone.
            /zones/{zone_identifier}/email/routing/disable:
              post:
                tags:
                  - Email Routing settings
                summary: Disable Email Routing
                description: >-
                  Disable your Email Routing zone. Also removes additional MX
                  records previously required for Email Routing to work.
            /zones/{zone_identifier}/email/routing/dns:
              get:
                tags:
                  - Email Routing settings
                summary: Email Routing - DNS settings
                description: >-
                  Show the DNS records needed to configure your Email Routing
                  zone.
            /zones/{zone_identifier}/email/routing/enable:
              post:
                tags:
                  - Email Routing settings
                summary: Enable Email Routing
                description: >-
                  Enable you Email Routing zone. Add and lock the necessary MX
                  and SPF records.
            /zones/{zone_identifier}/email/routing/rules:
              get:
                tags:
                  - Email Routing routing rules
                summary: List routing rules
                description: Lists existing routing rules.
              post:
                tags:
                  - Email Routing routing rules
                summary: Create routing rule
                description: >-
                  Rules consist of a set of criteria for matching emails (such
                  as an email being sent to a specific custom email address)
                  plus a set of actions to take on the email (like forwarding it
                  to a specific destination address).
            /zones/{zone_identifier}/email/routing/rules/{rule_identifier}:
              delete:
                tags:
                  - Email Routing routing rules
                summary: Delete routing rule
                description: Delete a specific routing rule.
              get:
                tags:
                  - Email Routing routing rules
                summary: Get routing rule
                description: Get information for a specific routing rule already created.
              put:
                tags:
                  - Email Routing routing rules
                summary: Update routing rule
                description: >-
                  Update actions and matches, or enable/disable specific routing
                  rules.
            /zones/{zone_identifier}/email/routing/rules/catch_all:
              get:
                tags:
                  - Email Routing routing rules
                summary: Get catch-all rule
                description: Get information on the default catch-all routing rule.
              put:
                tags:
                  - Email Routing routing rules
                summary: Update catch-all rule
                description: >-
                  Enable or disable catch-all routing rule, or change action to
                  forward to specific destination address.
            /zones/{zone_identifier}/filters:
              delete:
                tags:
                  - Filters
                summary: Delete filters
                description: Deletes one or more existing filters.
              get:
                tags:
                  - Filters
                summary: List filters
                description: >-
                  Fetches filters in a zone. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - Filters
                summary: Create filters
                description: Creates one or more filters.
              put:
                tags:
                  - Filters
                summary: Update filters
                description: Updates one or more existing filters.
            /zones/{zone_identifier}/filters/{id}:
              delete:
                tags:
                  - Filters
                summary: Delete a filter
                description: Deletes an existing filter.
              get:
                tags:
                  - Filters
                summary: Get a filter
                description: Fetches the details of a filter.
              put:
                tags:
                  - Filters
                summary: Update a filter
                description: Updates an existing filter.
            /zones/{zone_identifier}/firewall/lockdowns:
              get:
                tags:
                  - Zone Lockdown
                summary: List Zone Lockdown rules
                description: >-
                  Fetches Zone Lockdown rules. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - Zone Lockdown
                summary: Create a Zone Lockdown rule
                description: Creates a new Zone Lockdown rule.
            /zones/{zone_identifier}/firewall/lockdowns/{id}:
              delete:
                tags:
                  - Zone Lockdown
                summary: Delete a Zone Lockdown rule
                description: Deletes an existing Zone Lockdown rule.
              get:
                tags:
                  - Zone Lockdown
                summary: Get a Zone Lockdown rule
                description: Fetches the details of a Zone Lockdown rule.
              put:
                tags:
                  - Zone Lockdown
                summary: Update a Zone Lockdown rule
                description: Updates an existing Zone Lockdown rule.
            /zones/{zone_identifier}/firewall/rules:
              delete:
                tags:
                  - Firewall rules
                summary: Delete firewall rules
                description: Deletes existing firewall rules.
              get:
                tags:
                  - Firewall rules
                summary: List firewall rules
                description: >-
                  Fetches firewall rules in a zone. You can filter the results
                  using several optional parameters.
              patch:
                tags:
                  - Firewall rules
                summary: Update priority of firewall rules
                description: Updates the priority of existing firewall rules.
              post:
                tags:
                  - Firewall rules
                summary: Create firewall rules
                description: Create one or more firewall rules.
              put:
                tags:
                  - Firewall rules
                summary: Update firewall rules
                description: Updates one or more existing firewall rules.
            /zones/{zone_identifier}/firewall/rules/{id}:
              delete:
                tags:
                  - Firewall rules
                summary: Delete a firewall rule
                description: Deletes an existing firewall rule.
              get:
                tags:
                  - Firewall rules
                summary: Get a firewall rule
                description: Fetches the details of a firewall rule.
              patch:
                tags:
                  - Firewall rules
                summary: Update priority of a firewall rule
                description: Updates the priority of an existing firewall rule.
              put:
                tags:
                  - Firewall rules
                summary: Update a firewall rule
                description: Updates an existing firewall rule.
            /zones/{zone_identifier}/firewall/ua_rules:
              get:
                tags:
                  - User Agent Blocking rules
                summary: List User Agent Blocking rules
                description: >-
                  Fetches User Agent Blocking rules in a zone. You can filter
                  the results using several optional parameters.
              post:
                tags:
                  - User Agent Blocking rules
                summary: Create a User Agent Blocking rule
                description: Creates a new User Agent Blocking rule in a zone.
            /zones/{zone_identifier}/firewall/ua_rules/{id}:
              delete:
                tags:
                  - User Agent Blocking rules
                summary: Delete a User Agent Blocking rule
                description: Deletes an existing User Agent Blocking rule.
              get:
                tags:
                  - User Agent Blocking rules
                summary: Get a User Agent Blocking rule
                description: Fetches the details of a User Agent Blocking rule.
              put:
                tags:
                  - User Agent Blocking rules
                summary: Update a User Agent Blocking rule
                description: Updates an existing User Agent Blocking rule.
            /zones/{zone_identifier}/firewall/waf/overrides:
              get:
                tags:
                  - WAF overrides
                summary: List WAF overrides
                description: >-
                  Fetches the URI-based WAF overrides in a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              post:
                tags:
                  - WAF overrides
                summary: Create a WAF override
                description: >-
                  Creates a URI-based WAF override for a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/overrides/{id}:
              delete:
                tags:
                  - WAF overrides
                summary: Delete a WAF override
                description: >-
                  Deletes an existing URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              get:
                tags:
                  - WAF overrides
                summary: Get a WAF override
                description: >-
                  Fetches the details of a URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              put:
                tags:
                  - WAF overrides
                summary: Update WAF override
                description: >-
                  Updates an existing URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/packages:
              get:
                tags:
                  - WAF packages
                summary: List WAF packages
                description: >-
                  Fetches WAF packages for a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/packages/{identifier}:
              get:
                tags:
                  - WAF packages
                summary: Get a WAF package
                description: >-
                  Fetches the details of a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF packages
                summary: Update a WAF package
                description: >-
                  Updates a WAF package. You can update the sensitivity and the
                  action of an anomaly detection WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/healthchecks:
              get:
                tags:
                  - Health Checks
                summary: List Health Checks
                description: List configured health checks.
              post:
                tags:
                  - Health Checks
                summary: Create Health Check
                description: Create a new health check.
            /zones/{zone_identifier}/healthchecks/{identifier}:
              delete:
                tags:
                  - Health Checks
                summary: Delete Health Check
                description: Delete a health check.
              get:
                tags:
                  - Health Checks
                summary: Health Check Details
                description: Fetch a single configured health check.
              patch:
                tags:
                  - Health Checks
                summary: Patch Health Check
                description: Patch a configured health check.
              put:
                tags:
                  - Health Checks
                summary: Update Health Check
                description: Update a configured health check.
            /zones/{zone_identifier}/healthchecks/preview:
              post:
                tags:
                  - Health Checks
                summary: Create Preview Health Check
                description: Create a new preview health check.
            /zones/{zone_identifier}/healthchecks/preview/{identifier}:
              delete:
                tags:
                  - Health Checks
                summary: Delete Preview Health Check
                description: Delete a health check.
              get:
                tags:
                  - Health Checks
                summary: Health Check Preview Details
                description: Fetch a single configured health check preview.
            /zones/{zone_identifier}/logs/control/retention/flag:
              get:
                tags:
                  - Logs Received
                summary: Get log retention flag
                description: Gets log retention flag for Logpull API.
              post:
                tags:
                  - Logs Received
                summary: Update log retention flag
                description: Updates log retention flag for Logpull API.
            /zones/{zone_identifier}/logs/rayids/{ray_identifier}:
              get:
                tags:
                  - Logs Received
                summary: Get logs RayIDs
                description: >-
                  The `/rayids` api route allows lookups by specific rayid. The
                  rayids route will return zero, one, or more records (ray ids
                  are not unique).
            /zones/{zone_identifier}/logs/received:
              get:
                tags:
                  - Logs Received
                summary: Get logs received
                description: >-
                  The `/received` api route allows customers to retrieve their
                  edge HTTP logs. The basic access pattern is "give me all the
                  logs for zone Z for minute M", where the minute M refers to
                  the time records were received at Cloudflare's central data
                  center. `start` is inclusive, and `end` is exclusive. Because
                  of that, to get all data, at minutely cadence, starting at
                  10AM, the proper values are:
                  `start=2018-05-20T10:00:00Z&end=2018-05-20T10:01:00Z`, then
                  `start=2018-05-20T10:01:00Z&end=2018-05-20T10:02:00Z` and so
                  on; the overlap will be handled properly.
            /zones/{zone_identifier}/logs/received/fields:
              get:
                tags:
                  - Logs Received
                summary: List fields
                description: >-
                  Lists all fields available. The response is json object with
                  key-value pairs, where keys are field names, and values are
                  descriptions.
            /zones/{zone_identifier}/rate_limits:
              get:
                tags:
                  - Rate limits for a zone
                summary: List rate limits
                description: Fetches the rate limits for a zone.
              post:
                tags:
                  - Rate limits for a zone
                summary: Create a rate limit
                description: >-
                  Creates a new rate limit for a zone. Refer to the object
                  definition for a list of required attributes.
            /zones/{zone_identifier}/rate_limits/{id}:
              delete:
                tags:
                  - Rate limits for a zone
                summary: Delete a rate limit
                description: Deletes an existing rate limit.
              get:
                tags:
                  - Rate limits for a zone
                summary: Get a rate limit
                description: Fetches the details of a rate limit.
              put:
                tags:
                  - Rate limits for a zone
                summary: Update a rate limit
                description: Updates an existing rate limit.
            /zones/{zone_identifier}/snippets:
              get:
                tags:
                  - Zone Snippets
                summary: All Snippets
            /zones/{zone_identifier}/snippets/{snippet_name}:
              delete:
                tags:
                  - Zone Snippets
                summary: Delete Snippet
              get:
                tags:
                  - Zone Snippets
                summary: Snippet
              put:
                tags:
                  - Zone Snippets
                summary: Put Snippet
            /zones/{zone_identifier}/snippets/{snippet_name}/content:
              get:
                tags:
                  - Zone Snippets
                summary: Snippet Content
            /zones/{zone_identifier}/snippets/snippet_rules:
              get:
                tags:
                  - Zone Snippets
                summary: Rules
              put:
                tags:
                  - Zone Snippets
                summary: Put Rules
            /zones/{zone_identifier}/ssl/recommendation:
              get:
                tags:
                  - SSL/TLS Mode Recommendation
                summary: SSL/TLS Recommendation
                description: Retrieve the SSL/TLS Recommender's recommendation for a zone.
            /zones/{zone_identifier}/waiting_rooms:
              get:
                tags:
                  - Waiting Room
                summary: List waiting rooms
                description: Lists waiting rooms.
              post:
                tags:
                  - Waiting Room
                summary: Create waiting room
                description: Creates a new waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete waiting room
                description: Deletes a waiting room.
              get:
                tags:
                  - Waiting Room
                summary: Waiting room details
                description: Fetches a single configured waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch waiting room
                description: Patches a configured waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Update waiting room
                description: Updates a configured waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events:
              get:
                tags:
                  - Waiting Room
                summary: List events
                description: Lists events for a waiting room.
              post:
                tags:
                  - Waiting Room
                summary: Create event
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Creates an event for a waiting room. An event takes place
                  during a specified period of time, temporarily changing the
                  behavior of a waiting room. While the event is active, some of
                  the properties in the event's configuration may either
                  override or inherit from the waiting room's configuration.
                  Note that events cannot overlap with each other, so only one
                  event can be active at a time.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events/{event_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete event
                description: Deletes an event for a waiting room.
              get:
                tags:
                  - Waiting Room
                summary: Event details
                description: Fetches a single configured event for a waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch event
                description: Patches a configured event for a waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Update event
                description: Updates a configured event for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events/{event_id}/details:
              get:
                tags:
                  - Waiting Room
                summary: Preview active event details
                description: >-
                  Previews an event's configuration as if it was active.
                  Inherited fields from the waiting room will be displayed with
                  their current values.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/rules:
              get:
                tags:
                  - Waiting Room
                summary: List Waiting Room Rules
                description: Lists rules for a waiting room.
              post:
                tags:
                  - Waiting Room
                summary: Create Waiting Room Rule
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Creates a rule for a waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Replace Waiting Room Rules
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Replaces all rules for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/rules/{rule_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete Waiting Room Rule
                description: Deletes a rule for a waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch Waiting Room Rule
                description: Patches a rule for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/status:
              get:
                tags:
                  - Waiting Room
                summary: Get waiting room status
                description: "Fetches the status of a configured waiting room. Response fields include:\n1. `status`: String indicating the status of the waiting room. The possible status are:\n\t- **not_queueing** indicates that the configured thresholds have not been met and all users are going through to the origin.\n\t- **queueing** indicates that the thresholds have been met and some users are held in the waiting room.\n\t- **event_prequeueing** indicates that an event is active and is currently prequeueing users before it starts.\n2. `event_id`: String of the current event's `id` if an event is active, otherwise an empty string.\n3. `estimated_queued_users`: Integer of the estimated number of users currently waiting in the queue.\n4. `estimated_total_active_users`: Integer of the estimated number of users currently active on the origin.\n5. `max_estimated_time_minutes`: Integer of the maximum estimated time currently presented to the users."
            /zones/{zone_identifier}/waiting_rooms/preview:
              post:
                tags:
                  - Waiting Room
                summary: Create a custom waiting room page preview
                description: "Creates a waiting room page preview. Upload a custom waiting room page for preview. You will receive a preview URL in the form `http://waitingrooms.dev/preview/<uuid>`. You can use the following query parameters to change the state of the preview:\n1. `force_queue`: Boolean indicating if all users will be queued in the waiting room and no one will be let into the origin website (also known as queueAll).\n2. `queue_is_full`: Boolean indicating if the waiting room's queue is currently full and not accepting new users at the moment.\n3. `queueing_method`: The queueing method currently used by the waiting room.\n\t- **fifo** indicates a FIFO queue.\n\t- **random** indicates a Random queue.\n\t- **passthrough** indicates a Passthrough queue. Keep in mind that the waiting room page will only be displayed if `force_queue=true` or `event=prequeueing` — for other cases the request will pass through to the origin. For our preview, this will be a fake origin website returning \"Welcome\". \n\t- **reject** indicates a Reject queue.\n4. `event`: Used to preview a waiting room event.\n\t- **none** indicates no event is occurring.\n\t- **prequeueing** indicates that an event is prequeueing (between `prequeue_start_time` and `event_start_time`).\n\t- **started** indicates that an event has started (between `event_start_time` and `event_end_time`).\n5. `shuffle_at_event_start`: Boolean indicating if the event will shuffle users in the prequeue when it starts. This can only be set to **true** if an event is active (`event` is not **none**).\n\nFor example, you can make a request to `http://waitingrooms.dev/preview/<uuid>?force_queue=false&queue_is_full=false&queueing_method=random&event=started&shuffle_at_event_start=true`\n6. `waitTime`: Non-zero, positive integer indicating the estimated wait time in minutes. The default value is 10 minutes.\n\nFor example, you can make a request to `http://waitingrooms.dev/preview/<uuid>?waitTime=50` to configure the estimated wait time as 50 minutes."
            /zones/{zone_identifier}/waiting_rooms/settings:
              get:
                tags:
                  - Waiting Room
                summary: Get zone-level Waiting Room settings
              patch:
                tags:
                  - Waiting Room
                summary: Patch zone-level Waiting Room settings
              put:
                tags:
                  - Waiting Room
                summary: Update zone-level Waiting Room settings
            /zones/{zone_identifier}/web3/hostnames:
              get:
                tags:
                  - Web3 Hostname
                summary: List Web3 Hostnames
              post:
                tags:
                  - Web3 Hostname
                summary: Create Web3 Hostname
            /zones/{zone_identifier}/web3/hostnames/{identifier}:
              delete:
                tags:
                  - Web3 Hostname
                summary: Delete Web3 Hostname
              get:
                tags:
                  - Web3 Hostname
                summary: Web3 Hostname Details
              patch:
                tags:
                  - Web3 Hostname
                summary: Edit Web3 Hostname
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list:
              get:
                tags:
                  - Web3 Hostname
                summary: IPFS Universal Path Gateway Content List Details
              put:
                tags:
                  - Web3 Hostname
                summary: Update IPFS Universal Path Gateway Content List
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list/entries:
              get:
                tags:
                  - Web3 Hostname
                summary: List IPFS Universal Path Gateway Content List Entries
              post:
                tags:
                  - Web3 Hostname
                summary: Create IPFS Universal Path Gateway Content List Entry
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list/entries/{content_list_entry_identifier}:
              delete:
                tags:
                  - Web3 Hostname
                summary: Delete IPFS Universal Path Gateway Content List Entry
              get:
                tags:
                  - Web3 Hostname
                summary: IPFS Universal Path Gateway Content List Entry Details
              put:
                tags:
                  - Web3 Hostname
                summary: Edit IPFS Universal Path Gateway Content List Entry
            /zones/{zone}/spectrum/analytics/aggregate/current:
              get:
                tags:
                  - Spectrum Aggregate Analytics
                summary: Get current aggregated analytics
                description: >-
                  Retrieves analytics aggregated from the last minute of usage
                  on Spectrum applications underneath a given zone.
            /zones/{zone}/spectrum/analytics/events/bytime:
              get:
                tags:
                  - Spectrum Analytics (By Time)
                summary: Get analytics by time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.
            /zones/{zone}/spectrum/analytics/events/summary:
              get:
                tags:
                  - Spectrum Analytics (Summary)
                summary: Get analytics summary
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.
            /zones/{zone}/spectrum/apps:
              get:
                tags:
                  - Spectrum Applications
                summary: List Spectrum applications
                description: >-
                  Retrieves a list of currently existing Spectrum applications
                  inside a zone.
              post:
                tags:
                  - Spectrum Applications
                summary: Create Spectrum application using a name for the origin
                description: >-
                  Creates a new Spectrum application from a configuration using
                  a name for the origin.
            /zones/{zone}/spectrum/apps/{app_id}:
              delete:
                tags:
                  - Spectrum Applications
                summary: Delete Spectrum application
                description: Deletes a previously existing application.
              get:
                tags:
                  - Spectrum Applications
                summary: Get Spectrum application configuration
                description: >-
                  Gets the application configuration of a specific application
                  inside a zone.
              put:
                tags:
                  - Spectrum Applications
                summary: >-
                  Update Spectrum application configuration using a name for the
                  origin
                description: >-
                  Updates a previously existing application's configuration that
                  uses a name for the origin.
    contact:
      - FN: Support
        url: https://support.cloudflare.com/
        email: ''
    overlays:
      - type: API Evangelist Ratings
        url: overlays/cloudflare-openapi-api-evangelist-ratings.yml
      - type: APIs.io Search
        url: overlays/cloudflare-openapi-search.yml
    aid: cloudflare:cloudflare-api
  - name: Cloudflare API
    description: >-
      Interact with Cloudflare's products and services via the Cloudflare API.
      Using the Cloudflare API requires authentication so that Cloudflare knows
      who is making requests and what permissions you have. Create an API token
      to grant access to the API to perform actions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.cloudflare.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.cloudflare.com/api/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Cloudflare API
            license:
              name: BSD-3-Clause
              url: https://opensource.org/licenses/BSD-3-Clause
          paths:
            /accounts:
              get:
                tags:
                  - Accounts
                summary: List Accounts
                description: List all accounts you have ownership or verified access to.
            /accounts/{account_id}:
              get:
                tags:
                  - Accounts
                summary: Account Details
                description: >-
                  Get information about a specific account that you are a member
                  of.
              put:
                tags:
                  - Accounts
                summary: Update Account
                description: Update an existing account.
            /accounts/{account_id}/addressing/address_maps:
              get:
                tags:
                  - IP Address Management Address Maps
                summary: List Address Maps
                description: List all address maps owned by the account.
              post:
                tags:
                  - IP Address Management Address Maps
                summary: Create Address Map
                description: Create a new address map under the account.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Delete Address Map
                description: >-
                  Delete a particular address map owned by the account. An
                  Address Map must be disabled before it can be deleted.
              get:
                tags:
                  - IP Address Management Address Maps
                summary: Address Map Details
                description: Show a particular address map owned by the account.
              patch:
                tags:
                  - IP Address Management Address Maps
                summary: Update Address Map
                description: Modify properties of an address map owned by the account.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/accounts/{account_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove an account membership from an Address Map
                description: Remove an account as a member of a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add an account membership to an Address Map
                description: Add an account as a member of a particular address map.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/ips/{ip_address}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove an IP from an Address Map
                description: Remove an IP from a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add an IP to an Address Map
                description: >-
                  Add an IP from a prefix owned by the account to a particular
                  address map.
            /accounts/{account_id}/addressing/address_maps/{address_map_id}/zones/{zone_id}:
              delete:
                tags:
                  - IP Address Management Address Maps
                summary: Remove a zone membership from an Address Map
                description: Remove a zone as a member of a particular address map.
              put:
                tags:
                  - IP Address Management Address Maps
                summary: Add a zone membership to an Address Map
                description: Add a zone as a member of a particular address map.
            /accounts/{account_id}/addressing/loa_documents:
              post:
                tags:
                  - IP Address Management Prefixes
                summary: Upload LOA Document
                description: Submit LOA document (pdf format) under the account.
            /accounts/{account_id}/addressing/loa_documents/{loa_document_id}/download:
              get:
                tags:
                  - IP Address Management Prefixes
                summary: Download LOA Document
                description: Download specified LOA document under the account.
            /accounts/{account_id}/addressing/prefixes:
              get:
                tags:
                  - IP Address Management Prefixes
                summary: List Prefixes
                description: List all prefixes owned by the account.
              post:
                tags:
                  - IP Address Management Prefixes
                summary: Add Prefix
                description: Add a new prefix under the account.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}:
              delete:
                tags:
                  - IP Address Management Prefixes
                summary: Delete Prefix
                description: Delete an unapproved prefix owned by the account.
              get:
                tags:
                  - IP Address Management Prefixes
                summary: Prefix Details
                description: List a particular prefix owned by the account.
              patch:
                tags:
                  - IP Address Management Prefixes
                summary: Update Prefix Description
                description: Modify the description for a prefix owned by the account.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/prefixes:
              get:
                tags:
                  - IP Address Management BGP Prefixes
                summary: List BGP Prefixes
                description: >-
                  List all BGP Prefixes within the specified IP Prefix. BGP
                  Prefixes are used to control which specific subnets are
                  advertised to the Internet. It is possible to advertise
                  subnets more specific than an IP Prefix by creating more
                  specific BGP Prefixes.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/prefixes/{bgp_prefix_id}:
              get:
                tags:
                  - IP Address Management BGP Prefixes
                summary: Fetch BGP Prefix
                description: Retrieve a single BGP Prefix according to its identifier
              patch:
                tags:
                  - IP Address Management BGP Prefixes
                summary: Update BGP Prefix
                description: >-
                  Update the properties of a BGP Prefix, such as the on demand
                  advertisement status (advertised or withdrawn).
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bgp/status:
              get:
                tags:
                  - IP Address Management Dynamic Advertisement
                summary: Get Advertisement Status
                description: List the current advertisement state for a prefix.
              patch:
                tags:
                  - IP Address Management Dynamic Advertisement
                summary: Update Prefix Dynamic Advertisement Status
                description: Advertise or withdraw BGP route for a prefix.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bindings:
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: List Service Bindings
                description: >
                  List the Cloudflare services this prefix is currently bound
                  to. Traffic sent to an address within an IP prefix will be
                  routed to the Cloudflare service of the most-specific Service
                  Binding matching the address.

                  **Example:** binding `192.0.2.0/24` to Cloudflare Magic
                  Transit and `192.0.2.1/32` to the Cloudflare CDN would route
                  traffic for `192.0.2.1` to the CDN, and traffic for all other
                  IPs in the prefix to Cloudflare Magic Transit.
              post:
                tags:
                  - IP Address Management Service Bindings
                summary: Create Service Binding
                description: >
                  Creates a new Service Binding, routing traffic to IPs within
                  the given CIDR to a service running on Cloudflare's network.

                  **Note:** This API may only be used on prefixes currently
                  configured with a Magic Transit service binding, and only
                  allows creating service bindings for the Cloudflare CDN or
                  Cloudflare Spectrum.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/bindings/{binding_id}:
              delete:
                tags:
                  - IP Address Management Service Bindings
                summary: Delete Service Binding
                description: Delete a Service Binding
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: Get Service Binding
                description: Fetch a single Service Binding
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/delegations:
              get:
                tags:
                  - IP Address Management Prefix Delegation
                summary: List Prefix Delegations
                description: List all delegations for a given account IP prefix.
              post:
                tags:
                  - IP Address Management Prefix Delegation
                summary: Create Prefix Delegation
                description: Create a new account delegation for a given IP prefix.
            /accounts/{account_id}/addressing/prefixes/{prefix_id}/delegations/{delegation_id}:
              delete:
                tags:
                  - IP Address Management Prefix Delegation
                summary: Delete Prefix Delegation
                description: Delete an account delegation for a given IP prefix.
            /accounts/{account_id}/addressing/services:
              get:
                tags:
                  - IP Address Management Service Bindings
                summary: List Services
                description: >
                  Bring-Your-Own IP (BYOIP) prefixes onboarded to Cloudflare
                  must be bound to a service running on the Cloudflare network
                  to enable a Cloudflare product on the IP addresses. This
                  endpoint can be used as a reference of available services on
                  the Cloudflare network, and their service IDs.
            /accounts/{account_id}/ai/run/@cf/baai/bge-base-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-base-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/baai/bge-large-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-large-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/baai/bge-small-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @cf/baai/bge-small-en-v1.5 model.
            /accounts/{account_id}/ai/run/@cf/bytedance/stable-diffusion-xl-lightning:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/bytedance/stable-diffusion-xl-lightning model.
            /accounts/{account_id}/ai/run/@cf/deepseek-ai/deepseek-math-7b-base:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/deepseek-ai/deepseek-math-7b-base model.
            /accounts/{account_id}/ai/run/@cf/deepseek-ai/deepseek-math-7b-instruct:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/deepseek-ai/deepseek-math-7b-instruct model.
            /accounts/{account_id}/ai/run/@cf/defog/sqlcoder-7b-2:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/defog/sqlcoder-7b-2 model.
            /accounts/{account_id}/ai/run/@cf/facebook/bart-large-cnn:
              post:
                tags:
                  - Workers AI Summarization
                summary: Execute @cf/facebook/bart-large-cnn model.
            /accounts/{account_id}/ai/run/@cf/facebook/detr-resnet-50:
              post:
                tags:
                  - Workers AI Object Detection
                summary: Execute @cf/facebook/detr-resnet-50 model.
            /accounts/{account_id}/ai/run/@cf/huggingface/distilbert-sst-2-int8:
              post:
                tags:
                  - Workers AI Text Classification
                summary: Execute @cf/huggingface/distilbert-sst-2-int8 model.
            /accounts/{account_id}/ai/run/@cf/jpmorganchase/roberta-spam:
              post:
                tags:
                  - Workers AI Text Classification
                summary: Execute @cf/jpmorganchase/roberta-spam model.
            /accounts/{account_id}/ai/run/@cf/lykon/dreamshaper-8-lcm:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/lykon/dreamshaper-8-lcm model.
            /accounts/{account_id}/ai/run/@cf/meta/llama-2-7b-chat-fp16:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/meta/llama-2-7b-chat-fp16 model.
            /accounts/{account_id}/ai/run/@cf/meta/llama-2-7b-chat-int8:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/meta/llama-2-7b-chat-int8 model.
            /accounts/{account_id}/ai/run/@cf/meta/m2m100-1.2b:
              post:
                tags:
                  - Workers AI Translation
                summary: Execute @cf/meta/m2m100-1.2b model.
            /accounts/{account_id}/ai/run/@cf/microsoft/phi-2:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/microsoft/phi-2 model.
            /accounts/{account_id}/ai/run/@cf/microsoft/resnet-50:
              post:
                tags:
                  - Workers AI Image Classification
                summary: Execute @cf/microsoft/resnet-50 model.
            /accounts/{account_id}/ai/run/@cf/mistral/mistral-7b-instruct-v0.1:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/mistral/mistral-7b-instruct-v0.1 model.
            /accounts/{account_id}/ai/run/@cf/openai/whisper:
              post:
                tags:
                  - Workers AI Speech Recognition
                summary: Execute @cf/openai/whisper model.
            /accounts/{account_id}/ai/run/@cf/openchat/openchat-3.5-0106:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/openchat/openchat-3.5-0106 model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-0.5b-chat:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-0.5b-chat model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-1.8b-chat:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-1.8b-chat model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-7b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-7b-chat-awq model.
            /accounts/{account_id}/ai/run/@cf/qwen/qwen1.5-14b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/qwen/qwen1.5-14b-chat-awq model.
            /accounts/{account_id}/ai/run/@cf/runwayml/stable-diffusion-v1-5-img2img:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/runwayml/stable-diffusion-v1-5-img2img model.
            /accounts/{account_id}/ai/run/@cf/runwayml/stable-diffusion-v1-5-inpainting:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/runwayml/stable-diffusion-v1-5-inpainting model.
            /accounts/{account_id}/ai/run/@cf/stabilityai/stable-diffusion-xl-base-1.0:
              post:
                tags:
                  - Workers AI Text To Image
                summary: Execute @cf/stabilityai/stable-diffusion-xl-base-1.0 model.
            /accounts/{account_id}/ai/run/@cf/thebloke/discolm-german-7b-v1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/thebloke/discolm-german-7b-v1-awq model.
            /accounts/{account_id}/ai/run/@cf/thebloke/yarn-mistral-7b-64k-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/thebloke/yarn-mistral-7b-64k-awq model.
            /accounts/{account_id}/ai/run/@cf/tiiuae/falcon-7b-instruct:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/tiiuae/falcon-7b-instruct model.
            /accounts/{account_id}/ai/run/@cf/tinyllama/tinyllama-1.1b-chat-v1.0:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @cf/tinyllama/tinyllama-1.1b-chat-v1.0 model.
            /accounts/{account_id}/ai/run/@hf/baai/bge-base-en-v1.5:
              post:
                tags:
                  - Workers AI Text Embeddings
                summary: Execute @hf/baai/bge-base-en-v1.5 model.
            /accounts/{account_id}/ai/run/@hf/sentence-transformers/all-minilm-l6-v2:
              post:
                tags:
                  - Workers AI Sentence Similarity
                summary: Execute @hf/sentence-transformers/all-minilm-l6-v2 model.
            /accounts/{account_id}/ai/run/@hf/thebloke/codellama-7b-instruct-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/codellama-7b-instruct-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/deepseek-coder-6.7b-base-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/deepseek-coder-6.7b-base-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/deepseek-coder-6.7b-instruct-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/deepseek-coder-6.7b-instruct-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/llama-2-13b-chat-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/llama-2-13b-chat-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/llamaguard-7b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/llamaguard-7b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/mistral-7b-instruct-v0.1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/mistral-7b-instruct-v0.1-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/neural-chat-7b-v3-1-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/neural-chat-7b-v3-1-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/openchat_3.5-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/openchat_3.5-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/openhermes-2.5-mistral-7b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/openhermes-2.5-mistral-7b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/orca-2-13b-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/orca-2-13b-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/starling-lm-7b-alpha-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/starling-lm-7b-alpha-awq model.
            /accounts/{account_id}/ai/run/@hf/thebloke/zephyr-7b-beta-awq:
              post:
                tags:
                  - Workers AI Text Generation
                summary: Execute @hf/thebloke/zephyr-7b-beta-awq model.
            /accounts/{account_id}/ai/run/{model_name}:
              post:
                tags:
                  - Workers AI
                summary: Execute AI model
                description: >-
                  This endpoint provides users with the capability to run
                  specific AI models on-demand.


                  By submitting the required input data, users can receive
                  real-time predictions or results generated by the chosen AI

                  model. The endpoint supports various AI model types, ensuring
                  flexibility and adaptability for diverse use cases.


                  Model specific inputs available in [Cloudflare
                  Docs](https://developers.cloudflare.com/workers-ai/models/).
            /accounts/{account_id}/alerting/v3/available_alerts:
              get:
                tags:
                  - Notification Alert Types
                summary: Get Alert Types
                description: >-
                  Gets a list of all alert types for which an account is
                  eligible.
            /accounts/{account_id}/alerting/v3/destinations/eligible:
              get:
                tags:
                  - Notification Mechanism Eligibility
                summary: Get delivery mechanism eligibility
                description: >-
                  Get a list of all delivery mechanism types for which an
                  account is eligible.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty:
              delete:
                tags:
                  - Notification destinations with PagerDuty
                summary: Delete PagerDuty Services
                description: Deletes all the PagerDuty Services connected to the account.
              get:
                tags:
                  - Notification destinations with PagerDuty
                summary: List PagerDuty services
                description: Get a list of all configured PagerDuty services.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty/connect:
              post:
                tags:
                  - Notification destinations with PagerDuty
                summary: Create PagerDuty integration token
                description: Creates a new token for integrating with PagerDuty.
            /accounts/{account_id}/alerting/v3/destinations/pagerduty/connect/{token_id}:
              get:
                tags:
                  - Notification destinations with PagerDuty
                summary: Connect PagerDuty
                description: Links PagerDuty with the account using the integration token.
            /accounts/{account_id}/alerting/v3/destinations/webhooks:
              get:
                tags:
                  - Notification webhooks
                summary: List webhooks
                description: Gets a list of all configured webhook destinations.
              post:
                tags:
                  - Notification webhooks
                summary: Create a webhook
                description: Creates a new webhook destination.
            /accounts/{account_id}/alerting/v3/destinations/webhooks/{webhook_id}:
              delete:
                tags:
                  - Notification webhooks
                summary: Delete a webhook
                description: Delete a configured webhook destination.
              get:
                tags:
                  - Notification webhooks
                summary: Get a webhook
                description: Get details for a single webhooks destination.
              put:
                tags:
                  - Notification webhooks
                summary: Update a webhook
                description: Update a webhook destination.
            /accounts/{account_id}/alerting/v3/history:
              get:
                tags:
                  - Notification History
                summary: List History
                description: >-
                  Gets a list of history records for notifications sent to an
                  account. The records are displayed for last `x` number of days
                  based on the zone plan (free = 30, pro = 30, biz = 30, ent =
                  90).
            /accounts/{account_id}/alerting/v3/policies:
              get:
                tags:
                  - Notification policies
                summary: List Notification policies
                description: Get a list of all Notification policies.
              post:
                tags:
                  - Notification policies
                summary: Create a Notification policy
                description: Creates a new Notification policy.
            /accounts/{account_id}/alerting/v3/policies/{policy_id}:
              delete:
                tags:
                  - Notification policies
                summary: Delete a Notification policy
                description: Delete a Notification policy.
              get:
                tags:
                  - Notification policies
                summary: Get a Notification policy
                description: Get details for a single policy.
              put:
                tags:
                  - Notification policies
                summary: Update a Notification policy
                description: Update a Notification policy.
            /accounts/{account_id}/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get account audit logs
                description: >-
                  Gets a list of audit logs for an account. Can be filtered by
                  who made the change, on which zone, and the timeframe of the
                  change.
            /accounts/{account_id}/brand-protection/submit:
              post:
                tags:
                  - Phishing URL Scanner
                summary: Submit suspicious URL for scanning
            /accounts/{account_id}/brand-protection/url-info:
              get:
                tags:
                  - Phishing URL Information
                summary: Get results for a URL scan
            /accounts/{account_id}/calls/apps:
              get:
                tags:
                  - Calls Apps
                summary: List apps
                description: Lists all apps in the Cloudflare account
              post:
                tags:
                  - Calls Apps
                summary: Create a new app
                description: >-
                  Creates a new Cloudflare calls app. An app is an unique
                  enviroment where each Session can access all Tracks within the
                  app.
            /accounts/{account_id}/calls/apps/{app_id}:
              delete:
                tags:
                  - Calls Apps
                summary: Delete app
                description: Deletes an app from Cloudflare Calls
              get:
                tags:
                  - Calls Apps
                summary: Retrieve app details
                description: Fetches details for a single Calls app.
              put:
                tags:
                  - Calls Apps
                summary: Edit app details
                description: Edit details for a single app.
            /accounts/{account_id}/cfd_tunnel:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Cloudflare Tunnels
                description: Lists and filters Cloudflare Tunnels in an account.
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Create a Cloudflare Tunnel
                description: Creates a new Cloudflare Tunnel in an account.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Delete a Cloudflare Tunnel
                description: Deletes a Cloudflare Tunnel from an account.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel
                description: Fetches a single Cloudflare Tunnel.
              patch:
                tags:
                  - Cloudflare Tunnel
                summary: Update a Cloudflare Tunnel
                description: Updates an existing Cloudflare Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/configurations:
              get:
                tags:
                  - Cloudflare Tunnel configuration
                summary: Get configuration
                description: Gets the configuration for a remotely-managed tunnel
              put:
                tags:
                  - Cloudflare Tunnel configuration
                summary: Put configuration
                description: >-
                  Adds or updates the configuration for a remotely-managed
                  tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/connections:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Clean up Cloudflare Tunnel connections
                description: >-
                  Removes a connection (aka Cloudflare Tunnel Connector) from a
                  Cloudflare Tunnel independently of its current state. If no
                  connector id (client_id) is provided all connectors will be
                  removed. We recommend running this command after rotating
                  tokens.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Cloudflare Tunnel connections
                description: Fetches connection details for a Cloudflare Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/connectors/{connector_id}:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get Cloudflare Tunnel connector
                description: >-
                  Fetches connector and connection details for a Cloudflare
                  Tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/management:
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel management token
                description: >-
                  Gets a management token used to access the management
                  resources (i.e. Streaming Logs) of a tunnel.
            /accounts/{account_id}/cfd_tunnel/{tunnel_id}/token:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Cloudflare Tunnel token
                description: >-
                  Gets the token used to associate cloudflared with a specific
                  tunnel.
            /accounts/{account_id}/challenges/widgets:
              get:
                tags:
                  - Turnstile
                summary: List Turnstile Widgets
                description: Lists all turnstile widgets of an account.
              post:
                tags:
                  - Turnstile
                summary: Create a Turnstile Widget
                description: Lists challenge widgets.
              parameters:
                - null
                - null
                - null
                - null
                - null
            /accounts/{account_id}/challenges/widgets/{sitekey}:
              delete:
                tags:
                  - Turnstile
                summary: Delete a Turnstile Widget
                description: Destroy a Turnstile Widget.
              get:
                tags:
                  - Turnstile
                summary: Turnstile Widget Details
                description: Show a single challenge widget configuration.
              put:
                tags:
                  - Turnstile
                summary: Update a Turnstile Widget
                description: Update the configuration of a widget.
              parameters:
                - null
                - null
            /accounts/{account_id}/challenges/widgets/{sitekey}/rotate_secret:
              post:
                tags:
                  - Turnstile
                summary: Rotate Secret for a Turnstile Widget
                description: >
                  Generate a new secret key for this widget. If
                  `invalidate_immediately`

                  is set to `false`, the previous secret remains valid for 2
                  hours.


                  Note that secrets cannot be rotated again during the grace
                  period.
              parameters:
                - null
                - null
            /accounts/{account_id}/custom_ns:
              get:
                tags:
                  - Account-Level Custom Nameservers
                summary: List Account Custom Nameservers
                description: List an account's custom nameservers.
              post:
                tags:
                  - Account-Level Custom Nameservers
                summary: Add Account Custom Nameserver
            /accounts/{account_id}/custom_ns/{custom_ns_id}:
              delete:
                tags:
                  - Account-Level Custom Nameservers
                summary: Delete Account Custom Nameserver
            /accounts/{account_id}/custom_ns/availability:
              get:
                tags:
                  - Account-Level Custom Nameservers
                summary: Get Eligible Zones for Account Custom Nameservers
            /accounts/{account_id}/custom_ns/verify:
              post:
                tags:
                  - Account-Level Custom Nameservers
                summary: Verify Account Custom Nameserver Glue Records
            /accounts/{account_id}/d1/database:
              get:
                tags:
                  - D1
                summary: List D1 Databases
                description: Returns a list of D1 databases.
              post:
                tags:
                  - D1
                summary: Create D1 Database
                description: Returns the created D1 database.
            /accounts/{account_id}/devices:
              get:
                tags:
                  - Devices
                summary: List devices
                description: Fetches a list of enrolled devices.
            /accounts/{account_id}/devices/{device_id}:
              get:
                tags:
                  - Devices
                summary: Get device details
                description: Fetches details for a single device.
            /accounts/{account_id}/devices/{device_id}/override_codes:
              get:
                tags:
                  - Devices
                summary: Get an admin override code for a device
                description: >-
                  Fetches a one-time use admin override code for a device. This
                  relies on the **Admin Override** setting being enabled in your
                  device configuration.
            /accounts/{account_id}/devices/dex_tests:
              get:
                tags:
                  - Device DEX Tests
                summary: List Device DEX tests
                description: Fetch all DEX tests.
              post:
                tags:
                  - Device DEX Tests
                summary: Create Device DEX test
                description: Create a DEX test.
            /accounts/{account_id}/devices/dex_tests/{dex_test_id}:
              delete:
                tags:
                  - Device DEX Tests
                summary: Delete Device DEX test
                description: >-
                  Delete a Device DEX test. Returns the remaining device dex
                  tests for the account.
              get:
                tags:
                  - Device DEX Tests
                summary: Get Device DEX test
                description: Fetch a single DEX test.
              put:
                tags:
                  - Device DEX Tests
                summary: Update Device DEX test
                description: Update a DEX test.
            /accounts/{account_id}/devices/networks:
              get:
                tags:
                  - Device Managed Networks
                summary: List your device managed networks
                description: Fetches a list of managed networks for an account.
              post:
                tags:
                  - Device Managed Networks
                summary: Create a device managed network
                description: Creates a new device managed network.
            /accounts/{account_id}/devices/networks/{network_id}:
              delete:
                tags:
                  - Device Managed Networks
                summary: Delete a device managed network
                description: >-
                  Deletes a device managed network and fetches a list of the
                  remaining device managed networks for an account.
              get:
                tags:
                  - Device Managed Networks
                summary: Get device managed network details
                description: Fetches details for a single managed network.
              put:
                tags:
                  - Device Managed Networks
                summary: Update a device managed network
                description: Updates a configured device managed network.
            /accounts/{account_id}/devices/policies:
              get:
                tags:
                  - Devices
                summary: List device settings profiles
                description: Fetches a list of the device settings profiles for an account.
            /accounts/{account_id}/devices/policy:
              get:
                tags:
                  - Devices
                summary: Get the default device settings profile
                description: Fetches the default device settings profile for an account.
              patch:
                tags:
                  - Devices
                summary: Update the default device settings profile
                description: Updates the default device settings profile for an account.
              post:
                tags:
                  - Devices
                summary: Create a device settings profile
                description: >-
                  Creates a device settings profile to be applied to certain
                  devices matching the criteria.
            /accounts/{account_id}/devices/policy/{policy_id}:
              delete:
                tags:
                  - Devices
                summary: Delete a device settings profile
                description: >-
                  Deletes a device settings profile and fetches a list of the
                  remaining profiles for an account.
              get:
                tags:
                  - Devices
                summary: Get device settings profile by ID
                description: Fetches a device settings profile by ID.
              patch:
                tags:
                  - Devices
                summary: Update a device settings profile
                description: Updates a configured device settings profile.
            /accounts/{account_id}/devices/policy/{policy_id}/exclude:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Split Tunnel exclude list for a device settings
                  profile
                description: >-
                  Fetches the list of routes excluded from the WARP client's
                  tunnel for a specific device settings profile.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Split Tunnel exclude list for a device settings
                  profile
                description: >-
                  Sets the list of routes excluded from the WARP client's tunnel
                  for a specific device settings profile.
            /accounts/{account_id}/devices/policy/{policy_id}/fallback_domains:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Local Domain Fallback list for a device settings
                  profile
                description: >-
                  Fetches the list of domains to bypass Gateway DNS resolution
                  from a specified device settings profile. These domains will
                  use the specified local DNS resolver instead.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Local Domain Fallback list for a device settings
                  profile
                description: >-
                  Sets the list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead. This will only apply to the specified device settings
                  profile.
            /accounts/{account_id}/devices/policy/{policy_id}/include:
              get:
                tags:
                  - Devices
                summary: >-
                  Get the Split Tunnel include list for a device settings
                  profile
                description: >-
                  Fetches the list of routes included in the WARP client's
                  tunnel for a specific device settings profile.
              put:
                tags:
                  - Devices
                summary: >-
                  Set the Split Tunnel include list for a device settings
                  profile
                description: >-
                  Sets the list of routes included in the WARP client's tunnel
                  for a specific device settings profile.
            /accounts/{account_id}/devices/policy/exclude:
              get:
                tags:
                  - Devices
                summary: Get the Split Tunnel exclude list
                description: >-
                  Fetches the list of routes excluded from the WARP client's
                  tunnel.
              put:
                tags:
                  - Devices
                summary: Set the Split Tunnel exclude list
                description: >-
                  Sets the list of routes excluded from the WARP client's
                  tunnel.
            /accounts/{account_id}/devices/policy/fallback_domains:
              get:
                tags:
                  - Devices
                summary: Get your Local Domain Fallback list
                description: >-
                  Fetches a list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead.
              put:
                tags:
                  - Devices
                summary: Set your Local Domain Fallback list
                description: >-
                  Sets the list of domains to bypass Gateway DNS resolution.
                  These domains will use the specified local DNS resolver
                  instead.
            /accounts/{account_id}/devices/policy/include:
              get:
                tags:
                  - Devices
                summary: Get the Split Tunnel include list
                description: >-
                  Fetches the list of routes included in the WARP client's
                  tunnel.
              put:
                tags:
                  - Devices
                summary: Set the Split Tunnel include list
                description: Sets the list of routes included in the WARP client's tunnel.
            /accounts/{account_id}/devices/posture:
              get:
                tags:
                  - Device posture rules
                summary: List device posture rules
                description: Fetches device posture rules for a Zero Trust account.
              post:
                tags:
                  - Device posture rules
                summary: Create a device posture rule
                description: Creates a new device posture rule.
            /accounts/{account_id}/devices/posture/{rule_id}:
              delete:
                tags:
                  - Device posture rules
                summary: Delete a device posture rule
                description: Deletes a device posture rule.
              get:
                tags:
                  - Device posture rules
                summary: Get device posture rule details
                description: Fetches a single device posture rule.
              put:
                tags:
                  - Device posture rules
                summary: Update a device posture rule
                description: Updates a device posture rule.
            /accounts/{account_id}/devices/posture/integration:
              get:
                tags:
                  - Device Posture Integrations
                summary: List your device posture integrations
                description: >-
                  Fetches the list of device posture integrations for an
                  account.
              post:
                tags:
                  - Device Posture Integrations
                summary: Create a device posture integration
                description: Create a new device posture integration.
            /accounts/{account_id}/devices/posture/integration/{integration_id}:
              delete:
                tags:
                  - Device Posture Integrations
                summary: Delete a device posture integration
                description: Delete a configured device posture integration.
              get:
                tags:
                  - Device Posture Integrations
                summary: Get device posture integration details
                description: Fetches details for a single device posture integration.
              patch:
                tags:
                  - Device Posture Integrations
                summary: Update a device posture integration
                description: Updates a configured device posture integration.
            /accounts/{account_id}/devices/revoke:
              post:
                tags:
                  - Devices
                summary: Revoke devices
                description: Revokes a list of devices.
            /accounts/{account_id}/devices/settings:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get device settings for a Zero Trust account
                description: >-
                  Describes the current device settings for a Zero Trust
                  account.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update device settings for a Zero Trust account
                description: Updates the current device settings for a Zero Trust account.
            /accounts/{account_id}/devices/unrevoke:
              post:
                tags:
                  - Devices
                summary: Unrevoke devices
                description: Unrevokes a list of devices.
            /accounts/{account_id}/dex/colos:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List Cloudflare colos
                description: >-
                  List Cloudflare colos that account's devices were connected to
                  during a time period, sorted by usage starting from the most
                  used colo. Colos without traffic are also returned and sorted
                  alphabetically.
            /accounts/{account_id}/dex/fleet-status/devices:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status devices
                description: List details for devices using WARP
            /accounts/{account_id}/dex/fleet-status/live:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status details by dimension
                description: List details for live (up to 60 minutes) devices using WARP
            /accounts/{account_id}/dex/fleet-status/over-time:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List fleet status aggregate details by dimension
                description: List details for devices using WARP, up to 7 days
            /accounts/{account_id}/dex/http-tests/{test_id}:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details and aggregate metrics for an http test
                description: >-
                  Get test details and aggregate performance metrics for an http
                  test for a given time period between 1 hour and 7 days.
            /accounts/{account_id}/dex/http-tests/{test_id}/percentiles:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get percentiles for an http test
                description: >-
                  Get percentiles for an http test for a given time period
                  between 1 hour and 7 days.
            /accounts/{account_id}/dex/tests:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: List DEX test analytics
                description: List DEX tests
            /accounts/{account_id}/dex/tests/unique-devices:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get count of devices targeted
                description: >-
                  Returns unique count of devices that have run synthetic
                  application monitoring tests in the past 7 days.
            /accounts/{account_id}/dex/traceroute-test-results/{test_result_id}/network-path:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details for a specific traceroute test run
                description: >-
                  Get a breakdown of hops and performance metrics for a specific
                  traceroute test run
            /accounts/{account_id}/dex/traceroute-tests/{test_id}:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get details and aggregate metrics for a traceroute test
                description: >-
                  Get test details and aggregate performance metrics for an
                  traceroute test for a given time period between 1 hour and 7
                  days.
            /accounts/{account_id}/dex/traceroute-tests/{test_id}/network-path:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get network path breakdown for a traceroute test
                description: >-
                  Get a breakdown of metrics by hop for individual traceroute
                  test runs
            /accounts/{account_id}/dex/traceroute-tests/{test_id}/percentiles:
              get:
                tags:
                  - DEX Synthetic Application Montitoring
                summary: Get percentiles for a traceroute test
                description: >-
                  Get percentiles for a traceroute test for a given time period
                  between 1 hour and 7 days.
            /accounts/{account_id}/diagnostics/traceroute:
              post:
                tags:
                  - Diagnostics
                summary: Traceroute
                description: Run traceroutes from Cloudflare colos.
            /accounts/{account_id}/dlp/datasets:
              get:
                tags:
                  - DLP Datasets
                summary: Fetch all datasets with information about available versions.
                description: Fetch all datasets with information about available versions.
              post:
                tags:
                  - DLP Datasets
                summary: Create a new dataset.
                description: Create a new dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}:
              delete:
                tags:
                  - DLP Datasets
                summary: Delete a dataset.
                description: |-
                  Delete a dataset.

                  This deletes all versions of the dataset.
              get:
                tags:
                  - DLP Datasets
                summary: >-
                  Fetch a specific dataset with information about available
                  versions.
                description: >-
                  Fetch a specific dataset with information about available
                  versions.
              put:
                tags:
                  - DLP Datasets
                summary: Update details about a dataset.
                description: Update details about a dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}/upload:
              post:
                tags:
                  - DLP Datasets
                summary: Prepare to upload a new version of a dataset.
                description: Prepare to upload a new version of a dataset.
            /accounts/{account_id}/dlp/datasets/{dataset_id}/upload/{version}:
              post:
                tags:
                  - DLP Datasets
                summary: Upload a new version of a dataset.
                description: Upload a new version of a dataset.
            /accounts/{account_id}/dlp/patterns/validate:
              post:
                tags:
                  - DLP Pattern Validation
                summary: Validate pattern
                description: >-
                  Validates whether this pattern is a valid regular expression.
                  Rejects it if the regular expression is too complex or can
                  match an unbounded-length string. Your regex will be rejected
                  if it uses the Kleene Star -- be sure to bound the maximum
                  number of characters that can be matched.
            /accounts/{account_id}/dlp/payload_log:
              get:
                tags:
                  - DLP Payload Log Settings
                summary: Get settings
                description: Gets the current DLP payload log settings for this account.
              put:
                tags:
                  - DLP Payload Log Settings
                summary: Update settings
                description: Updates the DLP payload log settings for this account.
            /accounts/{account_id}/dlp/profiles:
              get:
                tags:
                  - DLP Profiles
                summary: List all profiles
                description: Lists all DLP profiles in an account.
            /accounts/{account_id}/dlp/profiles/{profile_id}:
              get:
                tags:
                  - DLP Profiles
                summary: Get DLP Profile
                description: >-
                  Fetches a DLP profile by ID. Supports both predefined and
                  custom profiles
            /accounts/{account_id}/dlp/profiles/custom:
              post:
                tags:
                  - DLP Profiles
                summary: Create custom profiles
                description: Creates a set of DLP custom profiles.
            /accounts/{account_id}/dlp/profiles/custom/{profile_id}:
              delete:
                tags:
                  - DLP Profiles
                summary: Delete custom profile
                description: Deletes a DLP custom profile.
              get:
                tags:
                  - DLP Profiles
                summary: Get custom profile
                description: Fetches a custom DLP profile.
              put:
                tags:
                  - DLP Profiles
                summary: Update custom profile
                description: Updates a DLP custom profile.
            /accounts/{account_id}/dlp/profiles/predefined/{profile_id}:
              get:
                tags:
                  - DLP Profiles
                summary: Get predefined profile
                description: Fetches a predefined DLP profile.
              put:
                tags:
                  - DLP Profiles
                summary: Update predefined profile
                description: >-
                  Updates a DLP predefined profile. Only supports
                  enabling/disabling entries.
            /accounts/{account_id}/dns_firewall:
              get:
                tags:
                  - DNS Firewall
                summary: List DNS Firewall Clusters
                description: List configured DNS Firewall clusters for an account.
              post:
                tags:
                  - DNS Firewall
                summary: Create DNS Firewall Cluster
                description: Create a configured DNS Firewall Cluster.
            /accounts/{account_id}/dns_firewall/{dns_firewall_id}:
              delete:
                tags:
                  - DNS Firewall
                summary: Delete DNS Firewall Cluster
                description: Delete a configured DNS Firewall Cluster.
              get:
                tags:
                  - DNS Firewall
                summary: DNS Firewall Cluster Details
                description: Show a single configured DNS Firewall cluster for an account.
              patch:
                tags:
                  - DNS Firewall
                summary: Update DNS Firewall Cluster
                description: Modify a DNS Firewall Cluster configuration.
            /accounts/{account_id}/gateway:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get Zero Trust account information
                description: Gets information about the current Zero Trust account.
              post:
                tags:
                  - Zero Trust accounts
                summary: Create Zero Trust account
                description: >-
                  Creates a Zero Trust account with an existing Cloudflare
                  account.
            /accounts/{account_id}/gateway/app_types:
              get:
                tags:
                  - Zero Trust Gateway application and application type mappings
                summary: List application and application type mappings
                description: Fetches all application and application type mappings.
            /accounts/{account_id}/gateway/audit_ssh_settings:
              get:
                tags:
                  - Zero Trust Audit SSH Settings
                summary: Get Zero Trust Audit SSH settings
                description: Get all Zero Trust Audit SSH settings for an account.
              put:
                tags:
                  - Zero Trust Audit SSH Settings
                summary: Update Zero Trust Audit SSH settings
                description: Updates Zero Trust Audit SSH settings.
            /accounts/{account_id}/gateway/categories:
              get:
                tags:
                  - Zero Trust Gateway categories
                summary: List categories
                description: Fetches a list of all categories.
            /accounts/{account_id}/gateway/configuration:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get Zero Trust account configuration
                description: Fetches the current Zero Trust account configuration.
              patch:
                tags:
                  - Zero Trust accounts
                summary: Patch Zero Trust account configuration
                description: >-
                  Patches the current Zero Trust account configuration. This
                  endpoint can update a single subcollection of settings such as
                  `antivirus`, `tls_decrypt`, `activity_log`, `block_page`,
                  `browser_isolation`, `fips`, `body_scanning`, or
                  `custom_certificate`, without updating the entire
                  configuration object. Returns an error if any collection of
                  settings is not properly configured.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update Zero Trust account configuration
                description: Updates the current Zero Trust account configuration.
            /accounts/{account_id}/gateway/lists:
              get:
                tags:
                  - Zero Trust lists
                summary: List Zero Trust lists
                description: Fetches all Zero Trust lists for an account.
              post:
                tags:
                  - Zero Trust lists
                summary: Create Zero Trust list
                description: Creates a new Zero Trust list.
            /accounts/{account_id}/gateway/lists/{list_id}:
              delete:
                tags:
                  - Zero Trust lists
                summary: Delete Zero Trust list
                description: Deletes a Zero Trust list.
              get:
                tags:
                  - Zero Trust lists
                summary: Get Zero Trust list details
                description: Fetches a single Zero Trust list.
              patch:
                tags:
                  - Zero Trust lists
                summary: Patch Zero Trust list
                description: Appends or removes an item from a configured Zero Trust list.
              put:
                tags:
                  - Zero Trust lists
                summary: Update Zero Trust list
                description: Updates a configured Zero Trust list.
            /accounts/{account_id}/gateway/lists/{list_id}/items:
              get:
                tags:
                  - Zero Trust lists
                summary: Get Zero Trust list items
                description: Fetches all items in a single Zero Trust list.
            /accounts/{account_id}/gateway/locations:
              get:
                tags:
                  - Zero Trust Gateway locations
                summary: List Zero Trust Gateway locations
                description: Fetches Zero Trust Gateway locations for an account.
              post:
                tags:
                  - Zero Trust Gateway locations
                summary: Create a Zero Trust Gateway location
                description: Creates a new Zero Trust Gateway location.
            /accounts/{account_id}/gateway/locations/{location_id}:
              delete:
                tags:
                  - Zero Trust Gateway locations
                summary: Delete a Zero Trust Gateway location
                description: Deletes a configured Zero Trust Gateway location.
              get:
                tags:
                  - Zero Trust Gateway locations
                summary: Get Zero Trust Gateway location details
                description: Fetches a single Zero Trust Gateway location.
              put:
                tags:
                  - Zero Trust Gateway locations
                summary: Update a Zero Trust Gateway location
                description: Updates a configured Zero Trust Gateway location.
            /accounts/{account_id}/gateway/logging:
              get:
                tags:
                  - Zero Trust accounts
                summary: Get logging settings for the Zero Trust account
                description: Fetches the current logging settings for Zero Trust account.
              put:
                tags:
                  - Zero Trust accounts
                summary: Update Zero Trust account logging settings
                description: Updates logging settings for the current Zero Trust account.
            /accounts/{account_id}/gateway/proxy_endpoints:
              get:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Get a proxy endpoint
                description: Fetches a single Zero Trust Gateway proxy endpoint.
              post:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Create a proxy endpoint
                description: Creates a new Zero Trust Gateway proxy endpoint.
            /accounts/{account_id}/gateway/proxy_endpoints/{proxy_endpoint_id}:
              delete:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Delete a proxy endpoint
                description: Deletes a configured Zero Trust Gateway proxy endpoint.
              get:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: List proxy endpoints
                description: Fetches all Zero Trust Gateway proxy endpoints for an account.
              patch:
                tags:
                  - Zero Trust Gateway proxy endpoints
                summary: Update a proxy endpoint
                description: Updates a configured Zero Trust Gateway proxy endpoint.
            /accounts/{account_id}/gateway/rules:
              get:
                tags:
                  - Zero Trust Gateway rules
                summary: List Zero Trust Gateway rules
                description: Fetches the Zero Trust Gateway rules for an account.
              post:
                tags:
                  - Zero Trust Gateway rules
                summary: Create a Zero Trust Gateway rule
                description: Creates a new Zero Trust Gateway rule.
            /accounts/{account_id}/gateway/rules/{rule_id}:
              delete:
                tags:
                  - Zero Trust Gateway rules
                summary: Delete a Zero Trust Gateway rule
                description: Deletes a Zero Trust Gateway rule.
              get:
                tags:
                  - Zero Trust Gateway rules
                summary: Get Zero Trust Gateway rule details
                description: Fetches a single Zero Trust Gateway rule.
              put:
                tags:
                  - Zero Trust Gateway rules
                summary: Update a Zero Trust Gateway rule
                description: Updates a configured Zero Trust Gateway rule.
            /accounts/{account_id}/hyperdrive/configs:
              get:
                tags:
                  - Hyperdrive
                summary: List Hyperdrives
                description: Returns a list of Hyperdrives
              post:
                tags:
                  - Hyperdrive
                summary: Create Hyperdrive
                description: Creates and returns a new Hyperdrive configuration.
            /accounts/{account_id}/hyperdrive/configs/{hyperdrive_id}:
              delete:
                tags:
                  - Hyperdrive
                summary: Delete Hyperdrive
                description: Deletes the specified Hyperdrive.
              get:
                tags:
                  - Hyperdrive
                summary: Get Hyperdrive
                description: Returns the specified Hyperdrive configuration.
              patch:
                tags:
                  - Hyperdrive
                summary: Patch Hyperdrive
                description: >-
                  Patches and returns the specified Hyperdrive configuration.
                  Updates to the origin and caching settings are applied with an
                  all-or-nothing approach.
              put:
                tags:
                  - Hyperdrive
                summary: Update Hyperdrive
                description: Updates and returns the specified Hyperdrive configuration.
            /accounts/{account_id}/images/v1:
              get:
                tags:
                  - Cloudflare Images
                summary: List images
                description: >-
                  List up to 100 images with one request. Use the optional
                  parameters below to get a specific range of images.
              post:
                tags:
                  - Cloudflare Images
                summary: Upload an image
                description: >
                  Upload an image with up to 10 Megabytes using a single HTTP
                  POST (multipart/form-data) request.

                  An image can be uploaded by sending an image file or passing
                  an accessible to an API url.
            /accounts/{account_id}/images/v1/{image_id}:
              delete:
                tags:
                  - Cloudflare Images
                summary: Delete image
                description: >-
                  Delete an image on Cloudflare Images. On success, all copies
                  of the image are deleted and purged from cache.
              get:
                tags:
                  - Cloudflare Images
                summary: Image details
                description: Fetch details for a single image.
              patch:
                tags:
                  - Cloudflare Images
                summary: Update image
                description: >-
                  Update image access control. On access control change, all
                  copies of the image are purged from cache.
            /accounts/{account_id}/images/v1/{image_id}/blob:
              get:
                tags:
                  - Cloudflare Images
                summary: Base image
                description: >-
                  Fetch base image. For most images this will be the originally
                  uploaded file. For larger images it can be a near-lossless
                  version of the original.
            /accounts/{account_id}/images/v1/keys:
              get:
                tags:
                  - Cloudflare Images Keys
                summary: List Signing Keys
                description: >-
                  Lists your signing keys. These can be found on your Cloudflare
                  Images dashboard.
            /accounts/{account_id}/images/v1/keys/{signing_key_name}:
              delete:
                tags:
                  - Cloudflare Images Keys
                summary: Delete Signing Key
                description: >
                  Delete signing key with specified name. Returns all keys
                  available.

                  When last key is removed, a new default signing key will be
                  generated.
              put:
                tags:
                  - Cloudflare Images Keys
                summary: Create a new Signing Key
                description: >-
                  Create a new signing key with specified name. Returns all keys
                  available.
            /accounts/{account_id}/images/v1/stats:
              get:
                tags:
                  - Cloudflare Images
                summary: Images usage statistics
                description: Fetch usage statistics details for Cloudflare Images.
            /accounts/{account_id}/images/v1/variants:
              get:
                tags:
                  - Cloudflare Images Variants
                summary: List variants
                description: Lists existing variants.
              post:
                tags:
                  - Cloudflare Images Variants
                summary: Create a variant
                description: >-
                  Specify variants that allow you to resize images for different
                  use cases.
            /accounts/{account_id}/images/v1/variants/{variant_id}:
              delete:
                tags:
                  - Cloudflare Images Variants
                summary: Delete a variant
                description: >-
                  Deleting a variant purges the cache for all images associated
                  with the variant.
              get:
                tags:
                  - Cloudflare Images Variants
                summary: Variant details
                description: Fetch details for a single variant.
              patch:
                tags:
                  - Cloudflare Images Variants
                summary: Update a variant
                description: >-
                  Updating a variant purges the cache for all images associated
                  with the variant.
            /accounts/{account_id}/images/v2:
              get:
                tags:
                  - Cloudflare Images
                summary: List images V2
                description: >
                  List up to 10000 images with one request. Use the optional
                  parameters below to get a specific range of images.

                  Endpoint returns continuation_token if more images are
                  present.
            /accounts/{account_id}/images/v2/direct_upload:
              post:
                tags:
                  - Cloudflare Images
                summary: Create authenticated direct upload URL V2
                description: >-
                  Direct uploads allow users to upload images without API keys.
                  A common use case are web apps, client-side applications, or
                  mobile devices where users upload content directly to
                  Cloudflare Images. This method creates a draft record for a
                  future image. It returns an upload URL and an image
                  identifier. To verify if the image itself has been uploaded,
                  send an image details request
                  (accounts/:account_identifier/images/v1/:identifier), and
                  check that the `draft: true` property is not present.
            /accounts/{account_id}/intel/asn/{asn}:
              get:
                tags:
                  - ASN Intelligence
                summary: Get ASN Overview
            /accounts/{account_id}/intel/asn/{asn}/subnets:
              get:
                tags:
                  - ASN Intelligence
                summary: Get ASN Subnets
            /accounts/{account_id}/intel/attack-surface-report/{issue_id}/dismiss:
              put:
                tags:
                  - Security Center Insights
                summary: Archive Security Center Insight
            /accounts/{account_id}/intel/attack-surface-report/issue-types:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issues Types
            /accounts/{account_id}/intel/attack-surface-report/issues:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issues
            /accounts/{account_id}/intel/attack-surface-report/issues/class:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Class
            /accounts/{account_id}/intel/attack-surface-report/issues/severity:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Severity
            /accounts/{account_id}/intel/attack-surface-report/issues/type:
              get:
                tags:
                  - Security Center Insights
                summary: Get Security Center Issue Counts by Type
            /accounts/{account_id}/intel/dns:
              get:
                tags:
                  - Passive DNS by IP
                summary: Get Passive DNS by IP
            /accounts/{account_id}/intel/domain:
              get:
                tags:
                  - Domain Intelligence
                summary: Get Domain Details
            /accounts/{account_id}/intel/domain-history:
              get:
                tags:
                  - Domain History
                summary: Get Domain History
            /accounts/{account_id}/intel/domain/bulk:
              get:
                tags:
                  - Domain Intelligence
                summary: Get Multiple Domain Details
            /accounts/{account_id}/intel/indicator-feeds:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feeds owned by this account
              post:
                tags:
                  - Custom Indicator Feeds
                summary: Create new indicator feed
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feed metadata
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}/data:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: Get indicator feed data
            /accounts/{account_id}/intel/indicator-feeds/{feed_id}/snapshot:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Update indicator feed data
            /accounts/{account_id}/intel/indicator-feeds/permissions/add:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Grant permission to indicator feed
            /accounts/{account_id}/intel/indicator-feeds/permissions/remove:
              put:
                tags:
                  - Custom Indicator Feeds
                summary: Revoke permission to indicator feed
            /accounts/{account_id}/intel/indicator-feeds/permissions/view:
              get:
                tags:
                  - Custom Indicator Feeds
                summary: List indicator feed permissions
            /accounts/{account_id}/intel/ip:
              get:
                tags:
                  - IP Intelligence
                summary: Get IP Overview
            /accounts/{account_id}/intel/ip-list:
              get:
                tags:
                  - IP List
                summary: Get IP Lists
            /accounts/{account_id}/intel/miscategorization:
              post:
                tags:
                  - Miscategorization
                summary: Create Miscategorization
            /accounts/{account_id}/intel/sinkholes:
              get:
                tags:
                  - Sinkhole Config
                summary: List sinkholes owned by this account
            /accounts/{account_id}/intel/whois:
              get:
                tags:
                  - WHOIS Record
                summary: Get WHOIS Record
            /accounts/{account_id}/load_balancers/monitors:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: List Monitors
                description: List configured monitors for an account.
              post:
                tags:
                  - Account Load Balancer Monitors
                summary: Create Monitor
                description: Create a configured monitor.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}:
              delete:
                tags:
                  - Account Load Balancer Monitors
                summary: Delete Monitor
                description: Delete a configured monitor.
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: Monitor Details
                description: List a single configured monitor for an account.
              patch:
                tags:
                  - Account Load Balancer Monitors
                summary: Patch Monitor
                description: >-
                  Apply changes to an existing monitor, overwriting the supplied
                  properties.
              put:
                tags:
                  - Account Load Balancer Monitors
                summary: Update Monitor
                description: Modify a configured monitor.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}/preview:
              post:
                tags:
                  - Account Load Balancer Monitors
                summary: Preview Monitor
                description: >-
                  Preview pools using the specified monitor with provided
                  monitor details. The returned preview_id can be used in the
                  preview endpoint to retrieve the results.
            /accounts/{account_id}/load_balancers/monitors/{monitor_id}/references:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: List Monitor References
                description: Get the list of resources that reference the provided monitor.
            /accounts/{account_id}/load_balancers/pools:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: List Pools
                description: List configured pools.
              patch:
                tags:
                  - Account Load Balancer Pools
                summary: Patch Pools
                description: >-
                  Apply changes to a number of existing pools, overwriting the
                  supplied properties. Pools are ordered by ascending `name`.
                  Returns the list of affected pools. Supports the standard
                  pagination query parameters, either `limit`/`offset` or
                  `per_page`/`page`.
              post:
                tags:
                  - Account Load Balancer Pools
                summary: Create Pool
                description: Create a new pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}:
              delete:
                tags:
                  - Account Load Balancer Pools
                summary: Delete Pool
                description: Delete a configured pool.
              get:
                tags:
                  - Account Load Balancer Pools
                summary: Pool Details
                description: Fetch a single configured pool.
              patch:
                tags:
                  - Account Load Balancer Pools
                summary: Patch Pool
                description: >-
                  Apply changes to an existing pool, overwriting the supplied
                  properties.
              put:
                tags:
                  - Account Load Balancer Pools
                summary: Update Pool
                description: Modify a configured pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/health:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: Pool Health Details
                description: Fetch the latest pool health status for a single pool.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/preview:
              post:
                tags:
                  - Account Load Balancer Pools
                summary: Preview Pool
                description: >-
                  Preview pool health using provided monitor details. The
                  returned preview_id can be used in the preview endpoint to
                  retrieve the results.
            /accounts/{account_id}/load_balancers/pools/{pool_id}/references:
              get:
                tags:
                  - Account Load Balancer Pools
                summary: List Pool References
                description: Get the list of resources that reference the provided pool.
            /accounts/{account_id}/load_balancers/preview/{preview_id}:
              get:
                tags:
                  - Account Load Balancer Monitors
                summary: Preview Result
                description: >-
                  Get the result of a previous preview operation using the
                  provided preview_id.
            /accounts/{account_id}/load_balancers/regions:
              get:
                tags:
                  - Load Balancer Regions
                summary: List Regions
                description: List all region mappings.
            /accounts/{account_id}/load_balancers/regions/{region_id}:
              get:
                tags:
                  - Load Balancer Regions
                summary: Get Region
                description: Get a single region mapping.
            /accounts/{account_id}/load_balancers/search:
              get:
                tags:
                  - Account Load Balancer Search
                summary: Search Resources
                description: Search for Load Balancing resources.
            /accounts/{account_id}/logpush/datasets/{dataset_id}/fields:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List fields
                description: >-
                  Lists all fields available for a dataset. The response result
                  is an object with key-value pairs, where keys are field names,
                  and values are descriptions.
            /accounts/{account_id}/logpush/datasets/{dataset_id}/jobs:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List Logpush jobs for a dataset
                description: Lists Logpush jobs for an account for a dataset.
            /accounts/{account_id}/logpush/jobs:
              get:
                tags:
                  - Logpush jobs for an account
                summary: List Logpush jobs
                description: Lists Logpush jobs for an account.
              post:
                tags:
                  - Logpush jobs for an account
                summary: Create Logpush job
                description: Creates a new Logpush job for an account.
            /accounts/{account_id}/logpush/jobs/{job_id}:
              delete:
                tags:
                  - Logpush jobs for an account
                summary: Delete Logpush job
                description: Deletes a Logpush job.
              get:
                tags:
                  - Logpush jobs for an account
                summary: Get Logpush job details
                description: Gets the details of a Logpush job.
              put:
                tags:
                  - Logpush jobs for an account
                summary: Update Logpush job
                description: Updates a Logpush job.
            /accounts/{account_id}/logpush/ownership:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Get ownership challenge
                description: Gets a new ownership challenge sent to your destination.
            /accounts/{account_id}/logpush/ownership/validate:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Validate ownership challenge
                description: Validates ownership challenge of the destination.
            /accounts/{account_id}/logpush/validate/destination/exists:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Check destination exists
                description: Checks if there is an existing job with a destination.
            /accounts/{account_id}/logpush/validate/origin:
              post:
                tags:
                  - Logpush jobs for an account
                summary: Validate origin
                description: Validates logpull origin with logpull_options.
            /accounts/{account_id}/logs/control/cmb/config:
              delete:
                tags:
                  - Logcontrol CMB config for an account
                summary: Delete CMB config
                description: Deletes CMB config.
              get:
                tags:
                  - Logcontrol CMB config for an account
                summary: Get CMB config
                description: Gets CMB config.
              post:
                tags:
                  - Logcontrol CMB config for an account
                summary: Update CMB config
                description: Updates CMB config.
            /accounts/{account_id}/members:
              get:
                tags:
                  - Account Members
                summary: List Members
                description: List all members of an account.
              post:
                tags:
                  - Account Members
                summary: Add Member
                description: Add a user to the list of members for this account.
            /accounts/{account_id}/members/{member_id}:
              delete:
                tags:
                  - Account Members
                summary: Remove Member
                description: Remove a member from an account.
              get:
                tags:
                  - Account Members
                summary: Member Details
                description: Get information about a specific member of an account.
              put:
                tags:
                  - Account Members
                summary: Update Member
                description: Modify an account member.
            /accounts/{account_id}/mtls_certificates:
              get:
                tags:
                  - mTLS Certificate Management
                summary: List mTLS certificates
                description: Lists all mTLS certificates.
              post:
                tags:
                  - mTLS Certificate Management
                summary: Upload mTLS certificate
                description: >-
                  Upload a certificate that you want to use with mTLS-enabled
                  Cloudflare services.
            /accounts/{account_id}/mtls_certificates/{mtls_certificate_id}:
              delete:
                tags:
                  - mTLS Certificate Management
                summary: Delete mTLS certificate
                description: >-
                  Deletes the mTLS certificate unless the certificate is in use
                  by one or more Cloudflare services.
              get:
                tags:
                  - mTLS Certificate Management
                summary: Get mTLS certificate
                description: Fetches a single mTLS certificate.
            /accounts/{account_id}/mtls_certificates/{mtls_certificate_id}/associations:
              get:
                tags:
                  - mTLS Certificate Management
                summary: List mTLS certificate associations
                description: >-
                  Lists all active associations between the certificate and
                  Cloudflare services.
            /accounts/{account_id}/pages/projects:
              get:
                tags:
                  - Pages Project
                summary: Get projects
                description: Fetch a list of all user projects.
              post:
                tags:
                  - Pages Project
                summary: Create project
                description: Create a new project.
            /accounts/{account_id}/pages/projects/{project_name}:
              delete:
                tags:
                  - Pages Project
                summary: Delete project
                description: Delete a project by name.
              get:
                tags:
                  - Pages Project
                summary: Get project
                description: Fetch a project by name.
              patch:
                tags:
                  - Pages Project
                summary: Update project
                description: >-
                  Set new attributes for an existing project. Modify environment
                  variables. To delete an environment variable, set the key to
                  null.
            /accounts/{account_id}/pages/projects/{project_name}/deployments:
              get:
                tags:
                  - Pages Deployment
                summary: Get deployments
                description: Fetch a list of project deployments.
              post:
                tags:
                  - Pages Deployment
                summary: Create deployment
                description: >-
                  Start a new deployment from production. The repository and
                  account must have already been authorized on the Cloudflare
                  Pages dashboard.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}:
              delete:
                tags:
                  - Pages Deployment
                summary: Delete deployment
                description: Delete a deployment.
              get:
                tags:
                  - Pages Deployment
                summary: Get deployment info
                description: Fetch information about a deployment.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/history/logs:
              get:
                tags:
                  - Pages Deployment
                summary: Get deployment logs
                description: Fetch deployment logs for a project.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/retry:
              post:
                tags:
                  - Pages Deployment
                summary: Retry deployment
                description: Retry a previous deployment.
            /accounts/{account_id}/pages/projects/{project_name}/deployments/{deployment_id}/rollback:
              post:
                tags:
                  - Pages Deployment
                summary: Rollback deployment
                description: >-
                  Rollback the production deployment to a previous deployment.
                  You can only rollback to succesful builds on production.
            /accounts/{account_id}/pages/projects/{project_name}/domains:
              get:
                tags:
                  - Pages Domains
                summary: Get domains
                description: Fetch a list of all domains associated with a Pages project.
              post:
                tags:
                  - Pages Domains
                summary: Add domain
                description: Add a new domain for the Pages project.
            /accounts/{account_id}/pages/projects/{project_name}/domains/{domain_name}:
              delete:
                tags:
                  - Pages Domains
                summary: Delete domain
                description: Delete a Pages project's domain.
              get:
                tags:
                  - Pages Domains
                summary: Get domain
                description: Fetch a single domain.
              patch:
                tags:
                  - Pages Domains
                summary: Patch domain
                description: Retry the validation status of a single domain.
            /accounts/{account_id}/pages/projects/{project_name}/purge_build_cache:
              post:
                tags:
                  - Pages Build Cache
                summary: Purge build cache
                description: Purge all cached build artifacts for a Pages project
            /accounts/{account_id}/pcaps:
              get:
                tags:
                  - Magic PCAP collection
                summary: List packet capture requests
                description: Lists all packet capture requests for an account.
              post:
                tags:
                  - Magic PCAP collection
                summary: Create PCAP request
                description: Create new PCAP request for account.
            /accounts/{account_id}/pcaps/{pcap_id}:
              get:
                tags:
                  - Magic PCAP collection
                summary: Get PCAP request
                description: Get information for a PCAP request by id.
            /accounts/{account_id}/pcaps/{pcap_id}/download:
              get:
                tags:
                  - Magic PCAP collection
                summary: Download Simple PCAP
                description: >-
                  Download PCAP information into a file. Response is a binary
                  PCAP file.
            /accounts/{account_id}/pcaps/ownership:
              get:
                tags:
                  - Magic PCAP collection
                summary: List PCAPs Bucket Ownership
                description: List all buckets configured for use with PCAPs API.
              post:
                tags:
                  - Magic PCAP collection
                summary: Add buckets for full packet captures
                description: Adds an AWS or GCP bucket to use with full packet captures.
            /accounts/{account_id}/pcaps/ownership/{ownership_id}:
              delete:
                tags:
                  - Magic PCAP collection
                summary: Delete buckets for full packet captures
                description: Deletes buckets added to the packet captures API.
            /accounts/{account_id}/pcaps/ownership/validate:
              post:
                tags:
                  - Magic PCAP collection
                summary: Validate buckets for full packet captures
                description: Validates buckets added to the packet captures API.
            /accounts/{account_id}/r2/buckets:
              get:
                tags:
                  - R2 Bucket
                summary: List Buckets
                description: Lists all R2 buckets on your account
              post:
                tags:
                  - R2 Bucket
                summary: Create Bucket
                description: Creates a new R2 bucket.
            /accounts/{account_id}/r2/buckets/{bucket_name}:
              delete:
                tags:
                  - R2 Bucket
                summary: Delete Bucket
                description: Deletes an existing R2 bucket.
              get:
                tags:
                  - R2 Bucket
                summary: Get Bucket
                description: Gets metadata for an existing R2 bucket.
            /accounts/{account_id}/r2/buckets/{bucket_name}/sippy:
              delete:
                tags:
                  - R2 Bucket
                summary: Disable Sippy
                description: Disables Sippy on this bucket
              get:
                tags:
                  - R2 Bucket
                summary: Get Sippy Configuration
                description: Gets configuration for Sippy for an existing R2 bucket.
              put:
                tags:
                  - R2 Bucket
                summary: Enable Sippy
                description: Sets configuration for Sippy for an existing R2 bucket.
            /accounts/{account_id}/registrar/domains:
              get:
                tags:
                  - Registrar Domains
                summary: List domains
                description: List domains handled by Registrar.
            /accounts/{account_id}/registrar/domains/{domain_name}:
              get:
                tags:
                  - Registrar Domains
                summary: Get domain
                description: Show individual domain.
              put:
                tags:
                  - Registrar Domains
                summary: Update domain
                description: Update individual domain.
            /accounts/{account_id}/roles:
              get:
                tags:
                  - Account Roles
                summary: List Roles
                description: Get all available roles for an account.
            /accounts/{account_id}/roles/{role_id}:
              get:
                tags:
                  - Account Roles
                summary: Role Details
                description: Get information about a specific role for an account.
            /accounts/{account_id}/rules/lists:
              get:
                tags:
                  - Lists
                summary: Get lists
                description: Fetches all lists in the account.
              post:
                tags:
                  - Lists
                summary: Create a list
                description: Creates a new list of the specified type.
            /accounts/{account_id}/rules/lists/{list_id}:
              delete:
                tags:
                  - Lists
                summary: Delete a list
                description: Deletes a specific list and all its items.
              get:
                tags:
                  - Lists
                summary: Get a list
                description: Fetches the details of a list.
              put:
                tags:
                  - Lists
                summary: Update a list
                description: Updates the description of a list.
            /accounts/{account_id}/rules/lists/{list_id}/items:
              delete:
                tags:
                  - Lists
                summary: Delete list items
                description: >-
                  Removes one or more items from a list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
              get:
                tags:
                  - Lists
                summary: Get list items
                description: Fetches all the items in the list.
              post:
                tags:
                  - Lists
                summary: Create list items
                description: >-
                  Appends new items to the list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
              put:
                tags:
                  - Lists
                summary: Update all list items
                description: >-
                  Removes all existing items from the list and adds the provided
                  items to the list.


                  This operation is asynchronous. To get current the operation
                  status, invoke the [Get bulk operation
                  status](/operations/lists-get-bulk-operation-status) endpoint
                  with the returned `operation_id`.
            /accounts/{account_id}/rulesets:
              get:
                tags:
                  - Account Rulesets
                summary: List account rulesets
                description: Fetches all rulesets at the account level.
              post:
                tags:
                  - Account Rulesets
                summary: Create an account ruleset
                description: Creates a ruleset at the account level.
            /accounts/{account_id}/rulesets/{ruleset_id}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset
                description: Deletes all versions of an existing account ruleset.
              get:
                tags:
                  - Account Rulesets
                summary: Get an account ruleset
                description: Fetches the latest version of an account ruleset.
              put:
                tags:
                  - Account Rulesets
                summary: Update an account ruleset
                description: Updates an account ruleset, creating a new version.
            /accounts/{account_id}/rulesets/{ruleset_id}/rules:
              post:
                tags:
                  - Account Rulesets
                summary: Create an account ruleset rule
                description: >-
                  Adds a new rule to an account ruleset. The rule will be added
                  to the end of the existing list of rules in the ruleset by
                  default.
            /accounts/{account_id}/rulesets/{ruleset_id}/rules/{rule_id}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset rule
                description: Deletes an existing rule from an account ruleset.
              patch:
                tags:
                  - Account Rulesets
                summary: Update an account ruleset rule
                description: Updates an existing rule in an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions:
              get:
                tags:
                  - Account Rulesets
                summary: List an account ruleset's versions
                description: Fetches the versions of an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions/{ruleset_version}:
              delete:
                tags:
                  - Account Rulesets
                summary: Delete an account ruleset version
                description: Deletes an existing version of an account ruleset.
              get:
                tags:
                  - Account Rulesets
                summary: Get an account ruleset version
                description: Fetches a specific version of an account ruleset.
            /accounts/{account_id}/rulesets/{ruleset_id}/versions/{ruleset_version}/by_tag/{rule_tag}:
              get:
                tags:
                  - Account Rulesets
                summary: List an account ruleset version's rules by tag
                description: >-
                  Fetches the rules of a managed account ruleset version for a
                  given tag.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint:
              get:
                tags:
                  - Account Rulesets
                summary: Get an account entry point ruleset
                description: >-
                  Fetches the latest version of the account entry point ruleset
                  for a given phase.
              put:
                tags:
                  - Account Rulesets
                summary: Update an account entry point ruleset
                description: >-
                  Updates an account entry point ruleset, creating a new
                  version.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions:
              get:
                tags:
                  - Account Rulesets
                summary: List an account entry point ruleset's versions
                description: Fetches the versions of an account entry point ruleset.
            /accounts/{account_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions/{ruleset_version}:
              get:
                tags:
                  - Account Rulesets
                summary: Get an account entry point ruleset version
                description: Fetches a specific version of an account entry point ruleset.
            /accounts/{account_id}/rum/site_info:
              post:
                tags:
                  - Web Analytics
                summary: Create a Web Analytics site
                description: Creates a new Web Analytics site.
            /accounts/{account_id}/rum/site_info/{site_id}:
              delete:
                tags:
                  - Web Analytics
                summary: Delete a Web Analytics site
                description: Deletes an existing Web Analytics site.
              get:
                tags:
                  - Web Analytics
                summary: Get a Web Analytics site
                description: Retrieves a Web Analytics site.
              put:
                tags:
                  - Web Analytics
                summary: Update a Web Analytics site
                description: Updates an existing Web Analytics site.
            /accounts/{account_id}/rum/site_info/list:
              get:
                tags:
                  - Web Analytics
                summary: List Web Analytics sites
                description: Lists all Web Analytics sites of an account.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rule:
              post:
                tags:
                  - Web Analytics
                summary: Create a Web Analytics rule
                description: Creates a new rule in a Web Analytics ruleset.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rule/{rule_id}:
              delete:
                tags:
                  - Web Analytics
                summary: Delete a Web Analytics rule
                description: Deletes an existing rule from a Web Analytics ruleset.
              put:
                tags:
                  - Web Analytics
                summary: Update a Web Analytics rule
                description: Updates a rule in a Web Analytics ruleset.
            /accounts/{account_id}/rum/v2/{ruleset_id}/rules:
              get:
                tags:
                  - Web Analytics
                summary: List rules in Web Analytics ruleset
                description: Lists all the rules in a Web Analytics ruleset.
              post:
                tags:
                  - Web Analytics
                summary: Update Web Analytics rules
                description: >-
                  Modifies one or more rules in a Web Analytics ruleset with a
                  single request.
            /accounts/{account_id}/secondary_dns/acls:
              get:
                tags:
                  - Secondary DNS (ACL)
                summary: List ACLs
                description: List ACLs.
              post:
                tags:
                  - Secondary DNS (ACL)
                summary: Create ACL
                description: Create ACL.
            /accounts/{account_id}/secondary_dns/acls/{acl_id}:
              delete:
                tags:
                  - Secondary DNS (ACL)
                summary: Delete ACL
                description: Delete ACL.
              get:
                tags:
                  - Secondary DNS (ACL)
                summary: ACL Details
                description: Get ACL.
              put:
                tags:
                  - Secondary DNS (ACL)
                summary: Update ACL
                description: Modify ACL.
            /accounts/{account_id}/secondary_dns/peers:
              get:
                tags:
                  - Secondary DNS (Peer)
                summary: List Peers
                description: List Peers.
              post:
                tags:
                  - Secondary DNS (Peer)
                summary: Create Peer
                description: Create Peer.
            /accounts/{account_id}/secondary_dns/peers/{peer_id}:
              delete:
                tags:
                  - Secondary DNS (Peer)
                summary: Delete Peer
                description: Delete Peer.
              get:
                tags:
                  - Secondary DNS (Peer)
                summary: Peer Details
                description: Get Peer.
              put:
                tags:
                  - Secondary DNS (Peer)
                summary: Update Peer
                description: Modify Peer.
            /accounts/{account_id}/secondary_dns/tsigs:
              get:
                tags:
                  - Secondary DNS (TSIG)
                summary: List TSIGs
                description: List TSIGs.
              post:
                tags:
                  - Secondary DNS (TSIG)
                summary: Create TSIG
                description: Create TSIG.
            /accounts/{account_id}/secondary_dns/tsigs/{tsig_id}:
              delete:
                tags:
                  - Secondary DNS (TSIG)
                summary: Delete TSIG
                description: Delete TSIG.
              get:
                tags:
                  - Secondary DNS (TSIG)
                summary: TSIG Details
                description: Get TSIG.
              put:
                tags:
                  - Secondary DNS (TSIG)
                summary: Update TSIG
                description: Modify TSIG.
            /accounts/{account_id}/storage/analytics:
              get:
                tags:
                  - Workers KV Request Analytics
                summary: Query Request Analytics
                description: Retrieves Workers KV request metrics for the given account.
            /accounts/{account_id}/storage/analytics/stored:
              get:
                tags:
                  - Workers KV Stored Data Analytics
                summary: Query Stored Data Analytics
                description: >-
                  Retrieves Workers KV stored data metrics for the given
                  account.
            /accounts/{account_id}/storage/kv/namespaces:
              get:
                tags:
                  - Workers KV Namespace
                summary: List Namespaces
                description: Returns the namespaces owned by an account.
              post:
                tags:
                  - Workers KV Namespace
                summary: Create a Namespace
                description: >-
                  Creates a namespace under the given title. A `400` is returned
                  if the account already owns a namespace with this title. A
                  namespace must be explicitly deleted to be replaced.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Remove a Namespace
                description: Deletes the namespace corresponding to the given ID.
              put:
                tags:
                  - Workers KV Namespace
                summary: Rename a Namespace
                description: Modifies a namespace's title.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/bulk:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Delete multiple key-value pairs
                description: >-
                  Remove multiple KV pairs from the namespace. Body should be an
                  array of up to 10,000 keys to be removed.
              put:
                tags:
                  - Workers KV Namespace
                summary: Write multiple key-value pairs
                description: >-
                  Write multiple keys and values at once. Body should be an
                  array of up to 10,000 key-value pairs to be stored, along with
                  optional expiration information. Existing values and
                  expirations will be overwritten. If neither `expiration` nor
                  `expiration_ttl` is specified, the key-value pair will never
                  expire. If both are set, `expiration_ttl` is used and
                  `expiration` is ignored. The entire request size must be 100
                  megabytes or less.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/keys:
              get:
                tags:
                  - Workers KV Namespace
                summary: List a Namespace's Keys
                description: Lists a namespace's keys.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/metadata/{key_name}:
              get:
                tags:
                  - Workers KV Namespace
                summary: Read the metadata for a key
                description: >-
                  Returns the metadata associated with the given key in the
                  given namespace. Use URL-encoding to use special characters
                  (for example, `:`, `!`, `%`) in the key name.
            /accounts/{account_id}/storage/kv/namespaces/{namespace_id}/values/{key_name}:
              delete:
                tags:
                  - Workers KV Namespace
                summary: Delete key-value pair
                description: >-
                  Remove a KV pair from the namespace. Use URL-encoding to use
                  special characters (for example, `:`, `!`, `%`) in the key
                  name.
              get:
                tags:
                  - Workers KV Namespace
                summary: Read key-value pair
                description: >-
                  Returns the value associated with the given key in the given
                  namespace. Use URL-encoding to use special characters (for
                  example, `:`, `!`, `%`) in the key name. If the KV-pair is set
                  to expire at some point, the expiration time as measured in
                  seconds since the UNIX epoch will be returned in the
                  `expiration` response header.
              put:
                tags:
                  - Workers KV Namespace
                summary: Write key-value pair with metadata
                description: >-
                  Write a value identified by a key. Use URL-encoding to use
                  special characters (for example, `:`, `!`, `%`) in the key
                  name. Body should be the value to be stored along with JSON
                  metadata to be associated with the key/value pair. Existing
                  values, expirations, and metadata will be overwritten. If
                  neither `expiration` nor `expiration_ttl` is specified, the
                  key-value pair will never expire. If both are set,
                  `expiration_ttl` is used and `expiration` is ignored.
            /accounts/{account_id}/stream:
              get:
                tags:
                  - Stream Videos
                summary: List videos
                description: >-
                  Lists up to 1000 videos from a single request. For a specific
                  range, refer to the optional parameters.
              post:
                tags:
                  - Stream Videos
                summary: Initiate video uploads using TUS
                description: >-
                  Initiates a video upload using the TUS protocol. On success,
                  the server responds with a status code 201 (created) and
                  includes a `location` header to indicate where the content
                  should be uploaded. Refer to https://tus.io for protocol
                  details.
            /accounts/{account_id}/stream/{identifier}:
              delete:
                tags:
                  - Stream Videos
                summary: Delete video
                description: Deletes a video and its copies from Cloudflare Stream.
              get:
                tags:
                  - Stream Videos
                summary: Retrieve video details
                description: Fetches details for a single video.
              post:
                tags:
                  - Stream Videos
                summary: Edit video details
                description: Edit details for a single video.
            /accounts/{account_id}/stream/{identifier}/audio:
              get:
                tags:
                  - Stream Audio Tracks
                summary: List additional audio tracks on a video
                description: >-
                  Lists additional audio tracks on a video. Note this API will
                  not return information for audio attached to the video upload.
            /accounts/{account_id}/stream/{identifier}/audio/{audio_identifier}:
              delete:
                tags:
                  - Stream Audio Tracks
                summary: Delete additional audio tracks on a video
                description: >-
                  Deletes additional audio tracks on a video. Deleting a default
                  audio track is not allowed. You must assign another audio
                  track as default prior to deletion.
              patch:
                tags:
                  - Stream Audio Tracks
                summary: Edit additional audio tracks on a video
                description: >-
                  Edits additional audio tracks on a video. Editing the default
                  status of an audio track to `true` will mark all other audio
                  tracks on the video default status to `false`.
            /accounts/{account_id}/stream/{identifier}/audio/copy:
              post:
                tags:
                  - Stream Audio Tracks
                summary: Add audio tracks to a video
                description: >-
                  Adds an additional audio track to a video using the provided
                  audio track URL.
            /accounts/{account_id}/stream/{identifier}/captions:
              get:
                tags:
                  - Stream Subtitles/Captions
                summary: List captions or subtitles
                description: >-
                  Lists the available captions or subtitles for a specific
                  video.
            /accounts/{account_id}/stream/{identifier}/captions/{language}:
              delete:
                tags:
                  - Stream Subtitles/Captions
                summary: Delete captions or subtitles
                description: Removes the captions or subtitles from a video.
              put:
                tags:
                  - Stream Subtitles/Captions
                summary: Upload captions or subtitles
                description: >-
                  Uploads the caption or subtitle file to the endpoint for a
                  specific BCP47 language. One caption or subtitle file per
                  language is allowed.
            /accounts/{account_id}/stream/{identifier}/downloads:
              delete:
                tags:
                  - Stream MP4 Downloads
                summary: Delete downloads
                description: Delete the downloads for a video.
              get:
                tags:
                  - Stream MP4 Downloads
                summary: List downloads
                description: Lists the downloads created for a video.
              post:
                tags:
                  - Stream MP4 Downloads
                summary: Create downloads
                description: Creates a download for a video when a video is ready to view.
            /accounts/{account_id}/stream/{identifier}/embed:
              get:
                tags:
                  - Stream Videos
                summary: Retrieve embed Code HTML
                description: >-
                  Fetches an HTML code snippet to embed a video in a web page
                  delivered through Cloudflare. On success, returns an HTML
                  fragment for use on web pages to display a video. On failure,
                  returns a JSON response body.
            /accounts/{account_id}/stream/{identifier}/token:
              post:
                tags:
                  - Stream Videos
                summary: Create signed URL tokens for videos
                description: >-
                  Creates a signed URL token for a video. If a body is not
                  provided in the request, a token is created with default
                  values.
            /accounts/{account_id}/stream/clip:
              post:
                tags:
                  - Stream Video Clipping
                summary: Clip videos given a start and end time
                description: >-
                  Clips a video based on the specified start and end times
                  provided in seconds.
            /accounts/{account_id}/stream/copy:
              post:
                tags:
                  - Stream Videos
                summary: Upload videos from a URL
                description: Uploads a video to Stream from a provided URL.
            /accounts/{account_id}/stream/direct_upload:
              post:
                tags:
                  - Stream Videos
                summary: Upload videos via direct upload URLs
                description: >-
                  Creates a direct upload that allows video uploads without an
                  API key.
            /accounts/{account_id}/stream/keys:
              get:
                tags:
                  - Stream Signing Keys
                summary: List signing keys
                description: >-
                  Lists the video ID and creation date and time when a signing
                  key was created.
              post:
                tags:
                  - Stream Signing Keys
                summary: Create signing keys
                description: >-
                  Creates an RSA private key in PEM and JWK formats. Key files
                  are only displayed once after creation. Keys are created,
                  used, and deleted independently of videos, and every key can
                  sign any video.
            /accounts/{account_id}/stream/keys/{identifier}:
              delete:
                tags:
                  - Stream Signing Keys
                summary: Delete signing keys
                description: >-
                  Deletes signing keys and revokes all signed URLs generated
                  with the key.
            /accounts/{account_id}/stream/live_inputs:
              get:
                tags:
                  - Stream Live Inputs
                summary: List live inputs
                description: >-
                  Lists the live inputs created for an account. To get the
                  credentials needed to stream to a specific live input, request
                  a single live input.
              post:
                tags:
                  - Stream Live Inputs
                summary: Create a live input
                description: >-
                  Creates a live input, and returns credentials that you or your
                  users can use to stream live video to Cloudflare Stream.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}:
              delete:
                tags:
                  - Stream Live Inputs
                summary: Delete a live input
                description: >-
                  Prevents a live input from being streamed to and makes the
                  live input inaccessible to any future API calls.
              get:
                tags:
                  - Stream Live Inputs
                summary: Retrieve a live input
                description: Retrieves details of an existing live input.
              put:
                tags:
                  - Stream Live Inputs
                summary: Update a live input
                description: Updates a specified live input.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}/outputs:
              get:
                tags:
                  - Stream Live Inputs
                summary: List all outputs associated with a specified live input
                description: Retrieves all outputs associated with a specified live input.
              post:
                tags:
                  - Stream Live Inputs
                summary: Create a new output, connected to a live input
                description: >-
                  Creates a new output that can be used to simulcast or restream
                  live video to other RTMP or SRT destinations. Outputs are
                  always linked to a specific live input — one live input can
                  have many outputs.
            /accounts/{account_id}/stream/live_inputs/{live_input_identifier}/outputs/{output_identifier}:
              delete:
                tags:
                  - Stream Live Inputs
                summary: Delete an output
                description: >-
                  Deletes an output and removes it from the associated live
                  input.
              put:
                tags:
                  - Stream Live Inputs
                summary: Update an output
                description: Updates the state of an output.
            /accounts/{account_id}/stream/storage-usage:
              get:
                tags:
                  - Stream Videos
                summary: Storage use
                description: Returns information about an account's storage use.
            /accounts/{account_id}/stream/watermarks:
              get:
                tags:
                  - Stream Watermark Profile
                summary: List watermark profiles
                description: Lists all watermark profiles for an account.
              post:
                tags:
                  - Stream Watermark Profile
                summary: Create watermark profiles via basic upload
                description: >-
                  Creates watermark profiles using a single `HTTP POST
                  multipart/form-data` request.
            /accounts/{account_id}/stream/watermarks/{identifier}:
              delete:
                tags:
                  - Stream Watermark Profile
                summary: Delete watermark profiles
                description: Deletes a watermark profile.
              get:
                tags:
                  - Stream Watermark Profile
                summary: Watermark profile details
                description: Retrieves details for a single watermark profile.
            /accounts/{account_id}/stream/webhook:
              delete:
                tags:
                  - Stream Webhook
                summary: Delete webhooks
                description: Deletes a webhook.
              get:
                tags:
                  - Stream Webhook
                summary: View webhooks
                description: Retrieves a list of webhooks.
              put:
                tags:
                  - Stream Webhook
                summary: Create webhooks
                description: Creates a webhook notification.
            /accounts/{account_id}/teamnet/routes:
              get:
                tags:
                  - Tunnel route
                summary: List tunnel routes
                description: Lists and filters private network routes in an account.
              post:
                tags:
                  - Tunnel route
                summary: Create a tunnel route
                description: Routes a private network through a Cloudflare Tunnel.
            /accounts/{account_id}/teamnet/routes/{route_id}:
              delete:
                tags:
                  - Tunnel route
                summary: Delete a tunnel route
                description: |
                  Deletes a private network route from an account.
              patch:
                tags:
                  - Tunnel route
                summary: Update a tunnel route
                description: >-
                  Updates an existing private network route in an account. The
                  fields that are meant to be updated should be provided in the
                  body of the request.
            /accounts/{account_id}/teamnet/routes/ip/{ip}:
              get:
                tags:
                  - Tunnel route
                summary: Get tunnel route by IP
                description: Fetches routes that contain the given IP address.
            /accounts/{account_id}/teamnet/routes/network/{ip_network_encoded}:
              delete:
                tags:
                  - Tunnel route
                summary: Delete a tunnel route (CIDR Endpoint)
                description: >
                  Deletes a private network route from an account. The CIDR in
                  `ip_network_encoded` must be written in URL-encoded format. If
                  no virtual_network_id is provided it will delete the route
                  from the default vnet. If no tun_type is provided it will
                  fetch the type from the tunnel_id or if that is missing it
                  will assume Cloudflare Tunnel as default. If tunnel_id is
                  provided it will delete the route from that tunnel, otherwise
                  it will delete the route based on the vnet and tun_type.
              patch:
                tags:
                  - Tunnel route
                summary: Update a tunnel route (CIDR Endpoint)
                description: >-
                  Updates an existing private network route in an account. The
                  CIDR in `ip_network_encoded` must be written in URL-encoded
                  format.
              post:
                tags:
                  - Tunnel route
                summary: Create a tunnel route (CIDR Endpoint)
                description: >-
                  Routes a private network through a Cloudflare Tunnel. The CIDR
                  in `ip_network_encoded` must be written in URL-encoded format.
            /accounts/{account_id}/teamnet/virtual_networks:
              get:
                tags:
                  - Tunnel Virtual Network
                summary: List virtual networks
                description: Lists and filters virtual networks in an account.
              post:
                tags:
                  - Tunnel Virtual Network
                summary: Create a virtual network
                description: Adds a new virtual network to an account.
            /accounts/{account_id}/teamnet/virtual_networks/{virtual_network_id}:
              delete:
                tags:
                  - Tunnel Virtual Network
                summary: Delete a virtual network
                description: Deletes an existing virtual network.
              patch:
                tags:
                  - Tunnel Virtual Network
                summary: Update a virtual network
                description: Updates an existing virtual network.
            /accounts/{account_id}/tunnels:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List All Tunnels
                description: Lists and filters all types of Tunnels in an account.
              post:
                tags:
                  - Argo Tunnel
                summary: Create an Argo Tunnel
                description: Creates a new Argo Tunnel in an account.
            /accounts/{account_id}/tunnels/{tunnel_id}:
              delete:
                tags:
                  - Argo Tunnel
                summary: Delete an Argo Tunnel
                description: Deletes an Argo Tunnel from an account.
              get:
                tags:
                  - Argo Tunnel
                summary: Get an Argo Tunnel
                description: Fetches a single Argo Tunnel.
            /accounts/{account_id}/tunnels/{tunnel_id}/connections:
              delete:
                tags:
                  - Argo Tunnel
                summary: Clean up Argo Tunnel connections
                description: >-
                  Removes connections that are in a disconnected or pending
                  reconnect state. We recommend running this command after
                  shutting down a tunnel.
            /accounts/{account_id}/warp_connector:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: List Warp Connector Tunnels
                description: Lists and filters Warp Connector Tunnels in an account.
              post:
                tags:
                  - Cloudflare Tunnel
                summary: Create a Warp Connector Tunnel
                description: Creates a new Warp Connector Tunnel in an account.
            /accounts/{account_id}/warp_connector/{tunnel_id}:
              delete:
                tags:
                  - Cloudflare Tunnel
                summary: Delete a Warp Connector Tunnel
                description: Deletes a Warp Connector Tunnel from an account.
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Warp Connector Tunnel
                description: Fetches a single Warp Connector Tunnel.
              patch:
                tags:
                  - Cloudflare Tunnel
                summary: Update a Warp Connector Tunnel
                description: Updates an existing Warp Connector Tunnel.
            /accounts/{account_id}/warp_connector/{tunnel_id}/token:
              get:
                tags:
                  - Cloudflare Tunnel
                summary: Get a Warp Connector Tunnel token
                description: >-
                  Gets the token used to associate warp device with a specific
                  Warp Connector tunnel.
            /accounts/{account_id}/workers/account-settings:
              get:
                tags:
                  - Worker Account Settings
                summary: Fetch Worker Account Settings
                description: Fetches Worker account settings for an account.
              put:
                tags:
                  - Worker Account Settings
                summary: Create Worker Account Settings
                description: Creates Worker account settings for an account.
            /accounts/{account_id}/workers/deployments/by-script/{script_id}:
              get:
                tags:
                  - Worker Deployments
                summary: List Deployments
            /accounts/{account_id}/workers/deployments/by-script/{script_id}/detail/{deployment_id}:
              get:
                tags:
                  - Worker Deployments
                summary: Get Deployment Detail
            /accounts/{account_id}/workers/dispatch/namespaces:
              get:
                tags:
                  - Workers for Platforms
                summary: List dispatch namespaces
                description: Fetch a list of Workers for Platforms namespaces.
              post:
                tags:
                  - Workers for Platforms
                summary: Create dispatch namespace
                description: Create a new Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}:
              delete:
                tags:
                  - Workers for Platforms
                summary: Delete dispatch namespace
                description: Delete a Workers for Platforms namespace.
              get:
                tags:
                  - Workers for Platforms
                summary: Fetch dispatch namespace
                description: Fetch a Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}:
              delete:
                tags:
                  - Workers for Platforms
                summary: Delete Worker (Workers for Platforms)
                description: >-
                  Delete a worker from a Workers for Platforms namespace. This
                  call has no response body on a successful delete.
              get:
                tags:
                  - Workers for Platforms
                summary: Worker Details (Workers for Platforms)
                description: >-
                  Fetch information about a script uploaded to a Workers for
                  Platforms namespace.
              put:
                tags:
                  - Workers for Platforms
                summary: Upload Worker Module (Workers for Platforms)
                description: Upload a worker module to a Workers for Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/bindings:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Bindings (Workers for Platforms)
                description: >-
                  Fetch script bindings from a script uploaded to a Workers for
                  Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/content:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Content (Workers for Platforms)
                description: >-
                  Fetch script content from a script uploaded to a Workers for
                  Platforms namespace.
              put:
                tags:
                  - Workers for Platforms
                summary: Put Script Content (Workers for Platforms)
                description: >-
                  Put script content for a script uploaded to a Workers for
                  Platforms namespace.
            /accounts/{account_id}/workers/dispatch/namespaces/{dispatch_namespace}/scripts/{script_name}/settings:
              get:
                tags:
                  - Workers for Platforms
                summary: Get Script Settings
                description: >-
                  Get script settings from a script uploaded to a Workers for
                  Platforms namespace.
              patch:
                tags:
                  - Workers for Platforms
                summary: Patch Script Settings
                description: Patch script metadata, such as bindings
            /accounts/{account_id}/workers/domains:
              get:
                tags:
                  - Worker Domain
                summary: List Domains
                description: Lists all Worker Domains for an account.
              put:
                tags:
                  - Worker Domain
                summary: Attach to Domain
                description: Attaches a Worker to a zone and hostname.
            /accounts/{account_id}/workers/domains/{domain_id}:
              delete:
                tags:
                  - Worker Domain
                summary: Detach from Domain
                description: Detaches a Worker from a zone and hostname.
              get:
                tags:
                  - Worker Domain
                summary: Get a Domain
                description: Gets a Worker domain.
            /accounts/{account_id}/workers/durable_objects/namespaces:
              get:
                tags:
                  - Durable Objects Namespace
                summary: List Namespaces
                description: Returns the Durable Object namespaces owned by an account.
            /accounts/{account_id}/workers/durable_objects/namespaces/{id}/objects:
              get:
                tags:
                  - Durable Objects Namespace
                summary: List Objects
                description: Returns the Durable Objects in a given namespace.
            /accounts/{account_id}/workers/queues:
              get:
                tags:
                  - Queue
                summary: List Queues
                description: Returns the queues owned by an account.
              post:
                tags:
                  - Queue
                summary: Create Queue
                description: Creates a new queue.
            /accounts/{account_id}/workers/queues/{name}:
              delete:
                tags:
                  - Queue
                summary: Delete Queue
                description: Deletes a queue.
              get:
                tags:
                  - Queue
                summary: Queue Details
                description: Get information about a specific queue.
              put:
                tags:
                  - Queue
                summary: Update Queue
                description: Updates a queue.
            /accounts/{account_id}/workers/queues/{name}/consumers:
              get:
                tags:
                  - Queue
                summary: List Queue Consumers
                description: Returns the consumers for a queue.
              post:
                tags:
                  - Queue
                summary: Create Queue Consumer
                description: Creates a new consumer for a queue.
            /accounts/{account_id}/workers/queues/{name}/consumers/{consumer_name}:
              delete:
                tags:
                  - Queue
                summary: Delete Queue Consumer
                description: Deletes the consumer for a queue.
              put:
                tags:
                  - Queue
                summary: Update Queue Consumer
                description: >-
                  Updates the consumer for a queue, or creates one if it does
                  not exist.
            /accounts/{account_id}/workers/scripts:
              get:
                tags:
                  - Worker Script
                summary: List Workers
                description: Fetch a list of uploaded workers.
            /accounts/{account_id}/workers/scripts/{script_name}:
              delete:
                tags:
                  - Worker Script
                summary: Delete Worker
                description: >-
                  Delete your worker. This call has no response body on a
                  successful delete.
              get:
                tags:
                  - Worker Script
                summary: Download Worker
                description: >-
                  Fetch raw script content for your worker. Note this is the
                  original script content, not JSON encoded.
              put:
                tags:
                  - Worker Script
                summary: Upload Worker Module
                description: Upload a worker module.
            /accounts/{account_id}/workers/scripts/{script_name}/content:
              put:
                tags:
                  - Worker Script
                summary: Put script content
                description: Put script content without touching config or metadata
            /accounts/{account_id}/workers/scripts/{script_name}/content/v2:
              get:
                tags:
                  - Worker Script
                summary: Get script content
                description: Fetch script content only
            /accounts/{account_id}/workers/scripts/{script_name}/schedules:
              get:
                tags:
                  - Worker Cron Trigger
                summary: Get Cron Triggers
                description: Fetches Cron Triggers for a Worker.
              put:
                tags:
                  - Worker Cron Trigger
                summary: Update Cron Triggers
                description: Updates Cron Triggers for a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/settings:
              get:
                tags:
                  - Worker Script
                summary: Get Script Settings
                description: >-
                  Get script metadata and config, such as bindings or usage
                  model
              patch:
                tags:
                  - Worker Script
                summary: Patch Script Settings
                description: >-
                  Patch script metadata or config, such as bindings or usage
                  model
            /accounts/{account_id}/workers/scripts/{script_name}/tails:
              get:
                tags:
                  - Worker Tail Logs
                summary: List Tails
                description: Get list of tails currently deployed on a Worker.
              post:
                tags:
                  - Worker Tail Logs
                summary: Start Tail
                description: Starts a tail that receives logs and exception from a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/tails/{id}:
              delete:
                tags:
                  - Worker Tail Logs
                summary: Delete Tail
                description: Deletes a tail from a Worker.
            /accounts/{account_id}/workers/scripts/{script_name}/usage-model:
              get:
                tags:
                  - Worker Script
                summary: Fetch Usage Model
                description: Fetches the Usage Model for a given Worker.
              put:
                tags:
                  - Worker Script
                summary: Update Usage Model
                description: >-
                  Updates the Usage Model for a given Worker. Requires a Workers
                  Paid subscription.
            /accounts/{account_id}/workers/services/{service_name}/environments/{environment_name}/content:
              get:
                tags:
                  - Worker Environment
                summary: Get script content
                description: Get script content from a worker with an environment
              put:
                tags:
                  - Worker Environment
                summary: Put script content
                description: Put script content from a worker with an environment
            /accounts/{account_id}/workers/services/{service_name}/environments/{environment_name}/settings:
              get:
                tags:
                  - Worker Environment
                summary: Get Script Settings
                description: Get script settings from a worker with an environment
              patch:
                tags:
                  - Worker Environment
                summary: Patch Script Settings
                description: Patch script metadata, such as bindings
            /accounts/{account_id}/workers/subdomain:
              get:
                tags:
                  - Worker Subdomain
                summary: Get Subdomain
                description: Returns a Workers subdomain for an account.
              put:
                tags:
                  - Worker Subdomain
                summary: Create Subdomain
                description: Creates a Workers subdomain for an account.
            /accounts/{account_id}/zerotrust/connectivity_settings:
              get:
                tags:
                  - Zero Trust Connectivity Settings
                summary: Get Zero Trust Connectivity Settings
                description: >-
                  Gets the Zero Trust Connectivity Settings for the given
                  account.
              patch:
                tags:
                  - Zero Trust Connectivity Settings
                summary: Updates the Zero Trust Connectivity Settings
                description: >-
                  Updates the Zero Trust Connectivity Settings for the given
                  account.
            /accounts/{account_identifier}/billing/profile:
              get:
                tags:
                  - Account Billing Profile
                summary: Billing Profile Details
                description: Gets the current billing profile for the account.
            /accounts/{account_identifier}/cloudforce-one/requests:
              post:
                tags:
                  - Request for Information (RFI)
                summary: List Requests
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}:
              delete:
                tags:
                  - Request for Information (RFI)
                summary: Delete a Request
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get a Request
              put:
                tags:
                  - Request for Information (RFI)
                summary: Update a Request
                description: >-
                  Updating a request alters the request in the Cloudforce One
                  queue. This API may be used to update any attributes of the
                  request after the initial submission. Only fields that you
                  choose to update need to be add to the request body
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message:
              post:
                tags:
                  - Request for Information (RFI)
                summary: List Request Messages
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message/{message_identifer}:
              delete:
                tags:
                  - Request for Information (RFI)
                summary: Delete a Request Message
              put:
                tags:
                  - Request for Information (RFI)
                summary: Update a Request Message
            /accounts/{account_identifier}/cloudforce-one/requests/{request_identifier}/message/new:
              post:
                tags:
                  - Request for Information (RFI)
                summary: Create a New Request Message
                description: >-
                  Creating a request adds the request into the Cloudforce One
                  queue for analysis. In addition to the content, a short title,
                  type, priority, and releasability should be provided. If one
                  is not provided a default will be assigned.
            /accounts/{account_identifier}/cloudforce-one/requests/constants:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Priority, Status, and TLP constants
            /accounts/{account_identifier}/cloudforce-one/requests/new:
              post:
                tags:
                  - Request for Information (RFI)
                summary: Create a New Request
                description: >-
                  Creating a request adds the request into the Cloudforce One
                  queue for analysis. In addition to the content, a short title,
                  type, priority, and releasability should be provided. If one
                  is not provided a default will be assigned.
            /accounts/{account_identifier}/cloudforce-one/requests/priority:
              post:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: List Priority Intelligence Requirements
            /accounts/{account_identifier}/cloudforce-one/requests/priority/{priority_identifer}:
              delete:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Delete a Priority Intelligence Report
              get:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Get a Priority Intelligence Requirement
              put:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Update a Priority Intelligence Requirement
            /accounts/{account_identifier}/cloudforce-one/requests/priority/new:
              post:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Create a New Priority Requirement
            /accounts/{account_identifier}/cloudforce-one/requests/priority/quota:
              get:
                tags:
                  - Priority Intelligence Requirements (PIR)
                summary: Get Priority Intelligence Requirement Quota
            /accounts/{account_identifier}/cloudforce-one/requests/quota:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Quota
            /accounts/{account_identifier}/cloudforce-one/requests/types:
              get:
                tags:
                  - Request for Information (RFI)
                summary: Get Request Types
            /accounts/{account_identifier}/custom_pages:
              get:
                tags:
                  - Custom pages for an account
                summary: List custom pages
                description: Fetches all the custom pages at the account level.
            /accounts/{account_identifier}/custom_pages/{identifier}:
              get:
                tags:
                  - Custom pages for an account
                summary: Get a custom page
                description: Fetches the details of a custom page.
              put:
                tags:
                  - Custom pages for an account
                summary: Update a custom page
                description: Updates the configuration of an existing custom page.
            /accounts/{account_identifier}/d1/database/{database_identifier}:
              delete:
                tags:
                  - D1
                summary: Delete D1 Database
                description: Deletes the specified D1 database.
              get:
                tags:
                  - D1
                summary: Get D1 Database
                description: Returns the specified D1 database.
            /accounts/{account_identifier}/d1/database/{database_identifier}/query:
              post:
                tags:
                  - D1
                summary: Query D1 Database
                description: Returns the query result.
            /accounts/{account_identifier}/dns_firewall/{identifier}/dns_analytics/report:
              get:
                tags:
                  - DNS Firewall Analytics
                summary: Table
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /accounts/{account_identifier}/dns_firewall/{identifier}/dns_analytics/report/bytime:
              get:
                tags:
                  - DNS Firewall Analytics
                summary: By Time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /accounts/{account_identifier}/email/routing/addresses:
              get:
                tags:
                  - Email Routing destination addresses
                summary: List destination addresses
                description: Lists existing destination addresses.
              post:
                tags:
                  - Email Routing destination addresses
                summary: Create a destination address
                description: >-
                  Create a destination address to forward your emails to.
                  Destination addresses need to be verified before they can be
                  used.
            /accounts/{account_identifier}/email/routing/addresses/{destination_address_identifier}:
              delete:
                tags:
                  - Email Routing destination addresses
                summary: Delete destination address
                description: Deletes a specific destination address.
              get:
                tags:
                  - Email Routing destination addresses
                summary: Get a destination address
                description: >-
                  Gets information for a specific destination email already
                  created.
            /accounts/{account_identifier}/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for an account
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of an account. These rules apply to
                  all the zones in the account. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - IP Access rules for an account
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for an account. The rule will
                  apply to all zones in the account.


                  Note: To create an IP Access rule that applies to a single
                  zone, refer to the [IP Access rules for a
                  zone](#ip-access-rules-for-a-zone) endpoints.
            /accounts/{account_identifier}/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for an account
                summary: Delete an IP Access rule
                description: >-
                  Deletes an existing IP Access rule defined at the account
                  level.


                  Note: This operation will affect all zones in the account.
              get:
                tags:
                  - IP Access rules for an account
                summary: Get an IP Access rule
                description: >-
                  Fetches the details of an IP Access rule defined at the
                  account level.
              patch:
                tags:
                  - IP Access rules for an account
                summary: Update an IP Access rule
                description: |-
                  Updates an IP Access rule defined at the account level.

                  Note: This operation will affect all zones in the account.
            /accounts/{account_identifier}/magic/cf_interconnects:
              get:
                tags:
                  - Magic Interconnects
                summary: List interconnects
                description: Lists interconnects associated with an account.
              put:
                tags:
                  - Magic Interconnects
                summary: Update multiple interconnects
                description: >-
                  Updates multiple interconnects associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
            /accounts/{account_identifier}/magic/cf_interconnects/{tunnel_identifier}:
              get:
                tags:
                  - Magic Interconnects
                summary: List interconnect Details
                description: Lists details for a specific interconnect.
              put:
                tags:
                  - Magic Interconnects
                summary: Update interconnect
                description: >-
                  Updates a specific interconnect associated with an account.
                  Use `?validate_only=true` as an optional query parameter to
                  only run validation without persisting changes.
            /accounts/{account_identifier}/magic/gre_tunnels:
              get:
                tags:
                  - Magic GRE tunnels
                summary: List GRE tunnels
                description: Lists GRE tunnels associated with an account.
              post:
                tags:
                  - Magic GRE tunnels
                summary: Create GRE tunnels
                description: >-
                  Creates new GRE tunnels. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
              put:
                tags:
                  - Magic GRE tunnels
                summary: Update multiple GRE tunnels
                description: >-
                  Updates multiple GRE tunnels. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
            /accounts/{account_identifier}/magic/gre_tunnels/{tunnel_identifier}:
              delete:
                tags:
                  - Magic GRE tunnels
                summary: Delete GRE Tunnel
                description: >-
                  Disables and removes a specific static GRE tunnel. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
              get:
                tags:
                  - Magic GRE tunnels
                summary: List GRE Tunnel Details
                description: Lists informtion for a specific GRE tunnel.
              put:
                tags:
                  - Magic GRE tunnels
                summary: Update GRE Tunnel
                description: >-
                  Updates a specific GRE tunnel. Use `?validate_only=true` as an
                  optional query parameter to only run validation without
                  persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels:
              get:
                tags:
                  - Magic IPsec tunnels
                summary: List IPsec tunnels
                description: Lists IPsec tunnels associated with an account.
              post:
                tags:
                  - Magic IPsec tunnels
                summary: Create IPsec tunnels
                description: >-
                  Creates new IPsec tunnels associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
              put:
                tags:
                  - Magic IPsec tunnels
                summary: Update multiple IPsec tunnels
                description: >-
                  Update multiple IPsec tunnels associated with an account. Use
                  `?validate_only=true` as an optional query parameter to only
                  run validation without persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels/{tunnel_identifier}:
              delete:
                tags:
                  - Magic IPsec tunnels
                summary: Delete IPsec Tunnel
                description: >-
                  Disables and removes a specific static IPsec Tunnel associated
                  with an account. Use `?validate_only=true` as an optional
                  query parameter to only run validation without persisting
                  changes.
              get:
                tags:
                  - Magic IPsec tunnels
                summary: List IPsec tunnel details
                description: Lists details for a specific IPsec tunnel.
              put:
                tags:
                  - Magic IPsec tunnels
                summary: Update IPsec Tunnel
                description: >-
                  Updates a specific IPsec tunnel associated with an account.
                  Use `?validate_only=true` as an optional query parameter to
                  only run validation without persisting changes.
            /accounts/{account_identifier}/magic/ipsec_tunnels/{tunnel_identifier}/psk_generate:
              post:
                tags:
                  - Magic IPsec tunnels
                summary: Generate Pre Shared Key (PSK) for IPsec tunnels
                description: >-
                  Generates a Pre Shared Key for a specific IPsec tunnel used in
                  the IKE session. Use `?validate_only=true` as an optional
                  query parameter to only run validation without persisting
                  changes. After a PSK is generated, the PSK is immediately
                  persisted to Cloudflare's edge and cannot be retrieved later.
                  Note the PSK in a safe place.
            /accounts/{account_identifier}/magic/routes:
              delete:
                tags:
                  - Magic Static Routes
                summary: Delete Many Routes
                description: Delete multiple Magic static routes.
              get:
                tags:
                  - Magic Static Routes
                summary: List Routes
                description: List all Magic static routes.
              post:
                tags:
                  - Magic Static Routes
                summary: Create Routes
                description: >-
                  Creates a new Magic static route. Use `?validate_only=true` as
                  an optional query parameter to run validation only without
                  persisting changes.
              put:
                tags:
                  - Magic Static Routes
                summary: Update Many Routes
                description: >-
                  Update multiple Magic static routes. Use `?validate_only=true`
                  as an optional query parameter to run validation only without
                  persisting changes. Only fields for a route that need to be
                  changed need be provided.
            /accounts/{account_identifier}/magic/routes/{route_identifier}:
              delete:
                tags:
                  - Magic Static Routes
                summary: Delete Route
                description: Disable and remove a specific Magic static route.
              get:
                tags:
                  - Magic Static Routes
                summary: Route Details
                description: Get a specific Magic static route.
              put:
                tags:
                  - Magic Static Routes
                summary: Update Route
                description: >-
                  Update a specific Magic static route. Use
                  `?validate_only=true` as an optional query parameter to run
                  validation only without persisting changes.
            /accounts/{account_identifier}/magic/sites:
              get:
                tags:
                  - Magic WAN Sites
                summary: List Sites
                description: >-
                  Lists Sites associated with an account. Use
                  connector_identifier query param to return sites where
                  connector_identifier matches either site.ConnectorID or
                  site.SecondaryConnectorID.
              post:
                tags:
                  - Magic WAN Sites
                summary: Create a new Site
                description: Creates a new Site
            /accounts/{account_identifier}/magic/sites/{site_identifier}:
              delete:
                tags:
                  - Magic WAN Sites
                summary: Delete Site
                description: Remove a specific Site.
              get:
                tags:
                  - Magic WAN Sites
                summary: Site Details
                description: Get a specific Site.
              put:
                tags:
                  - Magic WAN Sites
                summary: Update Site
                description: Update a specific Site.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/acls:
              get:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: List Site ACLs
                description: Lists Site ACLs associated with an account.
              post:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Create a new Site ACL
                description: Creates a new Site ACL.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/acls/{acl_identifier}:
              delete:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Delete Site ACL
                description: Remove a specific Site ACL.
              get:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Site ACL Details
                description: Get a specific Site ACL.
              put:
                tags:
                  - Magic WAN Connector Site ACLs
                summary: Update Site ACL
                description: Update a specific Site ACL.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/lans:
              get:
                tags:
                  - Magic WAN Connector LANs
                summary: List LANs
                description: Lists LANs associated with an account and site.
              post:
                tags:
                  - Magic WAN Connector LANs
                summary: Create a new LAN
                description: >-
                  Creates a new LAN. If the site is in high availability mode,
                  static_addressing is required along with secondary and virtual
                  address.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/lans/{lan_identifier}:
              delete:
                tags:
                  - Magic WAN Connector LANs
                summary: Delete LAN
                description: Remove a specific LAN.
              get:
                tags:
                  - Magic WAN Connector LANs
                summary: LAN Details
                description: Get a specific LAN.
              put:
                tags:
                  - Magic WAN Connector LANs
                summary: Update LAN
                description: Update a specific LAN.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/wans:
              get:
                tags:
                  - Magic WAN Connector WANs
                summary: List WANs
                description: Lists WANs associated with an account and site.
              post:
                tags:
                  - Magic WAN Connector WANs
                summary: Create a new WAN
                description: Creates a new WAN.
            /accounts/{account_identifier}/magic/sites/{site_identifier}/wans/{wan_identifier}:
              delete:
                tags:
                  - Magic WAN Connector WANs
                summary: Delete WAN
                description: Remove a specific WAN.
              get:
                tags:
                  - Magic WAN Connector WANs
                summary: WAN Details
                description: Get a specific WAN.
              put:
                tags:
                  - Magic WAN Connector WANs
                summary: Update WAN
                description: Update a specific WAN.
            /accounts/{account_identifier}/mnm/config:
              delete:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Delete account configuration
                description: Delete an existing network monitoring configuration.
              get:
                tags:
                  - Magic Network Monitoring Configuration
                summary: List account configuration
                description: Lists default sampling and router IPs for account.
              patch:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Update account configuration fields
                description: Update fields in an existing network monitoring configuration.
              post:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Create account configuration
                description: Create a new network monitoring configuration.
              put:
                tags:
                  - Magic Network Monitoring Configuration
                summary: Update an entire account configuration
                description: >-
                  Update an existing network monitoring configuration, requires
                  the entire configuration to be updated at once.
            /accounts/{account_identifier}/mnm/config/full:
              get:
                tags:
                  - Magic Network Monitoring Configuration
                summary: List rules and account configuration
                description: Lists default sampling, router IPs, and rules for account.
            /accounts/{account_identifier}/mnm/rules:
              get:
                tags:
                  - Magic Network Monitoring Rules
                summary: List rules
                description: Lists network monitoring rules for account.
              post:
                tags:
                  - Magic Network Monitoring Rules
                summary: Create rules
                description: >-
                  Create network monitoring rules for account. Currently only
                  supports creating a single rule per API request.
              put:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update rules
                description: Update network monitoring rules for account.
            /accounts/{account_identifier}/mnm/rules/{rule_identifier}:
              delete:
                tags:
                  - Magic Network Monitoring Rules
                summary: Delete rule
                description: Delete a network monitoring rule for account.
              get:
                tags:
                  - Magic Network Monitoring Rules
                summary: Get rule
                description: List a single network monitoring rule for account.
              patch:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update rule
                description: Update a network monitoring rule for account.
            /accounts/{account_identifier}/mnm/rules/{rule_identifier}/advertisement:
              patch:
                tags:
                  - Magic Network Monitoring Rules
                summary: Update advertisement for rule
                description: Update advertisement for rule.
            /accounts/{account_identifier}/request-tracer/trace:
              post:
                tags:
                  - Account Request Tracer
                summary: Request Trace
            /accounts/{account_identifier}/rules/lists/{list_id}/items/{item_id}:
              get:
                tags:
                  - Lists
                summary: Get a list item
                description: Fetches a list item in the list.
            /accounts/{account_identifier}/rules/lists/bulk_operations/{operation_id}:
              get:
                tags:
                  - Lists
                summary: Get bulk operation status
                description: >-
                  Gets the current status of an asynchronous operation on a
                  list.


                  The `status` property can have one of the following values:
                  `pending`, `running`, `completed`, or `failed`. If the status
                  is `failed`, the `error` property will contain a message
                  describing the error.
            /accounts/{account_identifier}/subscriptions:
              get:
                tags:
                  - Account Subscriptions
                summary: List Subscriptions
                description: Lists all of an account's subscriptions.
              post:
                tags:
                  - Account Subscriptions
                summary: Create Subscription
                description: Creates an account subscription.
            /accounts/{account_identifier}/subscriptions/{subscription_identifier}:
              delete:
                tags:
                  - Account Subscriptions
                summary: Delete Subscription
                description: Deletes an account's subscription.
              put:
                tags:
                  - Account Subscriptions
                summary: Update Subscription
                description: Updates an account subscription.
            /accounts/{account_identifier}/vectorize/indexes:
              get:
                tags:
                  - VectorizeIndex
                summary: List Vectorize Indexes
                description: Returns a list of Vectorize Indexes
              post:
                tags:
                  - VectorizeIndex
                summary: Create Vectorize Index
                description: Creates and returns a new Vectorize Index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}:
              delete:
                tags:
                  - VectorizeIndex
                summary: Delete Vectorize Index
                description: Deletes the specified Vectorize Index.
              get:
                tags:
                  - VectorizeIndex
                summary: Get Vectorize Index
                description: Returns the specified Vectorize Index.
              put:
                tags:
                  - VectorizeIndex
                summary: Update Vectorize Index
                description: Updates and returns the specified Vectorize Index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/delete-by-ids:
              post:
                tags:
                  - VectorizeIndex
                summary: Delete Vectors By Identifier
                description: >-
                  Delete a set of vectors from an index by their vector
                  identifiers.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/get-by-ids:
              post:
                tags:
                  - VectorizeIndex
                summary: Get Vectors By Identifier
                description: >-
                  Get a set of vectors from an index by their vector
                  identifiers.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/insert:
              post:
                tags:
                  - VectorizeIndex
                summary: Insert Vectors
                description: >-
                  Inserts vectors into the specified index and returns the count
                  of the vectors successfully inserted.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/query:
              post:
                tags:
                  - VectorizeIndex
                summary: Query Vectors
                description: Finds vectors closest to a given vector in an index.
            /accounts/{account_identifier}/vectorize/indexes/{index_name}/upsert:
              post:
                tags:
                  - VectorizeIndex
                summary: Upsert Vectors
                description: >-
                  Upserts vectors into the specified index, creating them if
                  they do not exist and returns the count of values and ids
                  successfully inserted.
            /accounts/{accountId}/urlscanner/scan:
              get:
                tags:
                  - URL Scanner
                summary: Search URL scans
                description: >-
                  Search scans by date and webpages' requests, including full
                  URL (after redirects), hostname, and path. <br/> A successful
                  scan will appear in search results a few minutes after
                  finishing but may take much longer if the system in under
                  load. By default, only successfully completed scans will
                  appear in search results, unless searching by `scanId`. Please
                  take into account that older scans may be removed from the
                  search index at an unspecified time.
              post:
                tags:
                  - URL Scanner
                summary: Create URL Scan
                description: >-
                  Submit a URL to scan. You can also set some options, like the
                  visibility level and custom headers. Accounts are limited to 1
                  new scan every 10 seconds and 8000 per month. If you need
                  more, please reach out.
            /accounts/{accountId}/urlscanner/scan/{scanId}:
              get:
                tags:
                  - URL Scanner
                summary: Get URL scan
                description: Get URL scan by uuid
            /accounts/{accountId}/urlscanner/scan/{scanId}/har:
              get:
                tags:
                  - URL Scanner
                summary: Get URL scan's HAR
                description: >-
                  Get a URL scan's HAR file. See HAR spec at
                  http://www.softwareishard.com/blog/har-12-spec/.
            /accounts/{accountId}/urlscanner/scan/{scanId}/screenshot:
              get:
                tags:
                  - URL Scanner
                summary: Get screenshot
                description: Get scan's screenshot by resolution (desktop/mobile/tablet).
            /accounts/{identifier}/access/apps:
              get:
                tags:
                  - Access applications
                summary: List Access applications
                description: Lists all Access applications in an account.
              post:
                tags:
                  - Access applications
                summary: Add an Access Application
                description: Adds a new application to Access.
            /accounts/{identifier}/access/apps/{app_id}:
              delete:
                tags:
                  - Access applications
                summary: Delete an Access application
                description: Deletes an application from Access.
              get:
                tags:
                  - Access applications
                summary: Get an Access application
                description: Fetches information about an Access application.
              put:
                tags:
                  - Access applications
                summary: Update an Access application
                description: Updates an Access application.
            /accounts/{identifier}/access/apps/{app_id}/revoke_tokens:
              post:
                tags:
                  - Access applications
                summary: Revoke application tokens
                description: Revokes all tokens issued for an application.
            /accounts/{identifier}/access/apps/{app_id}/user_policy_checks:
              get:
                tags:
                  - Access applications
                summary: Test Access policies
                description: >-
                  Tests if a specific user has permission to access an
                  application.
            /accounts/{identifier}/access/apps/{uuid}/ca:
              delete:
                tags:
                  - Access short-lived certificate CAs
                summary: Delete a short-lived certificate CA
                description: Deletes a short-lived certificate CA.
              get:
                tags:
                  - Access short-lived certificate CAs
                summary: Get a short-lived certificate CA
                description: Fetches a short-lived certificate CA and its public key.
              post:
                tags:
                  - Access short-lived certificate CAs
                summary: Create a short-lived certificate CA
                description: Generates a new short-lived certificate CA and public key.
            /accounts/{identifier}/access/apps/{uuid}/policies:
              get:
                tags:
                  - Access policies
                summary: List Access policies
                description: Lists Access policies configured for an application.
              post:
                tags:
                  - Access policies
                summary: Create an Access policy
                description: Create a new Access policy for an application.
            /accounts/{identifier}/access/apps/{uuid1}/policies/{uuid}:
              delete:
                tags:
                  - Access policies
                summary: Delete an Access policy
                description: Delete an Access policy.
              get:
                tags:
                  - Access policies
                summary: Get an Access policy
                description: Fetches a single Access policy.
              put:
                tags:
                  - Access policies
                summary: Update an Access policy
                description: Update a configured Access policy.
            /accounts/{identifier}/access/apps/ca:
              get:
                tags:
                  - Access short-lived certificate CAs
                summary: List short-lived certificate CAs
                description: Lists short-lived certificate CAs and their public keys.
            /accounts/{identifier}/access/bookmarks:
              get:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: List Bookmark applications
                description: Lists Bookmark applications.
            /accounts/{identifier}/access/bookmarks/{uuid}:
              delete:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Delete a Bookmark application
                description: Deletes a Bookmark application.
              get:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Get a Bookmark application
                description: Fetches a single Bookmark application.
              post:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Create a Bookmark application
                description: Create a new Bookmark application.
              put:
                tags:
                  - Access Bookmark applications (Deprecated)
                summary: Update a Bookmark application
                description: Updates a configured Bookmark application.
            /accounts/{identifier}/access/certificates:
              get:
                tags:
                  - Access mTLS authentication
                summary: List mTLS certificates
                description: Lists all mTLS root certificates.
              post:
                tags:
                  - Access mTLS authentication
                summary: Add an mTLS certificate
                description: Adds a new mTLS root certificate to Access.
            /accounts/{identifier}/access/certificates/{uuid}:
              delete:
                tags:
                  - Access mTLS authentication
                summary: Delete an mTLS certificate
                description: Deletes an mTLS certificate.
              get:
                tags:
                  - Access mTLS authentication
                summary: Get an mTLS certificate
                description: Fetches a single mTLS certificate.
              put:
                tags:
                  - Access mTLS authentication
                summary: Update an mTLS certificate
                description: Updates a configured mTLS certificate.
            /accounts/{identifier}/access/certificates/settings:
              get:
                tags:
                  - Access mTLS authentication
                summary: List all mTLS hostname settings
                description: List all mTLS hostname settings for this account.
              put:
                tags:
                  - Access mTLS authentication
                summary: Update an mTLS certificate's hostname settings
                description: Updates an mTLS certificate's hostname settings.
            /accounts/{identifier}/access/custom_pages:
              get:
                tags:
                  - Access custom pages
                summary: List custom pages
                description: List custom pages
              post:
                tags:
                  - Access custom pages
                summary: Create a custom page
                description: Create a custom page
            /accounts/{identifier}/access/custom_pages/{uuid}:
              delete:
                tags:
                  - Access custom pages
                summary: Delete a custom page
                description: Delete a custom page
              get:
                tags:
                  - Access custom pages
                summary: Get a custom page
                description: Fetches a custom page and also returns its HTML.
              put:
                tags:
                  - Access custom pages
                summary: Update a custom page
                description: Update a custom page
            /accounts/{identifier}/access/groups:
              get:
                tags:
                  - Access groups
                summary: List Access groups
                description: Lists all Access groups.
              post:
                tags:
                  - Access groups
                summary: Create an Access group
                description: Creates a new Access group.
            /accounts/{identifier}/access/groups/{uuid}:
              delete:
                tags:
                  - Access groups
                summary: Delete an Access group
                description: Deletes an Access group.
              get:
                tags:
                  - Access groups
                summary: Get an Access group
                description: Fetches a single Access group.
              put:
                tags:
                  - Access groups
                summary: Update an Access group
                description: Updates a configured Access group.
            /accounts/{identifier}/access/identity_providers:
              get:
                tags:
                  - Access identity providers
                summary: List Access identity providers
                description: Lists all configured identity providers.
              post:
                tags:
                  - Access identity providers
                summary: Add an Access identity provider
                description: Adds a new identity provider to Access.
            /accounts/{identifier}/access/identity_providers/{uuid}:
              delete:
                tags:
                  - Access identity providers
                summary: Delete an Access identity provider
                description: Deletes an identity provider from Access.
              get:
                tags:
                  - Access identity providers
                summary: Get an Access identity provider
                description: Fetches a configured identity provider.
              put:
                tags:
                  - Access identity providers
                summary: Update an Access identity provider
                description: Updates a configured identity provider.
            /accounts/{identifier}/access/keys:
              get:
                tags:
                  - Access key configuration
                summary: Get the Access key configuration
                description: Gets the Access key rotation settings for an account.
              put:
                tags:
                  - Access key configuration
                summary: Update the Access key configuration
                description: Updates the Access key rotation settings for an account.
            /accounts/{identifier}/access/keys/rotate:
              post:
                tags:
                  - Access key configuration
                summary: Rotate Access keys
                description: Perfoms a key rotation for an account.
            /accounts/{identifier}/access/logs/access_requests:
              get:
                tags:
                  - Access authentication logs
                summary: Get Access authentication logs
                description: >-
                  Gets a list of Access authentication audit logs for an
                  account.
            /accounts/{identifier}/access/organizations:
              get:
                tags:
                  - Zero Trust organization
                summary: Get your Zero Trust organization
                description: Returns the configuration for your Zero Trust organization.
              post:
                tags:
                  - Zero Trust organization
                summary: Create your Zero Trust organization
                description: Sets up a Zero Trust organization for your account.
              put:
                tags:
                  - Zero Trust organization
                summary: Update your Zero Trust organization
                description: Updates the configuration for your Zero Trust organization.
            /accounts/{identifier}/access/organizations/revoke_user:
              post:
                tags:
                  - Zero Trust organization
                summary: Revoke all Access tokens for a user
                description: Revokes a user's access across all applications.
            /accounts/{identifier}/access/seats:
              patch:
                tags:
                  - Zero Trust seats
                summary: Update a user seat
                description: >-
                  Removes a user from a Zero Trust seat when both `access_seat`
                  and `gateway_seat` are set to false.
            /accounts/{identifier}/access/service_tokens:
              get:
                tags:
                  - Access service tokens
                summary: List service tokens
                description: Lists all service tokens.
              post:
                tags:
                  - Access service tokens
                summary: Create a service token
                description: >-
                  Generates a new service token. **Note:** This is the only time
                  you can get the Client Secret. If you lose the Client Secret,
                  you will have to rotate the Client Secret or create a new
                  service token.
            /accounts/{identifier}/access/service_tokens/{uuid}:
              delete:
                tags:
                  - Access service tokens
                summary: Delete a service token
                description: Deletes a service token.
              put:
                tags:
                  - Access service tokens
                summary: Update a service token
                description: Updates a configured service token.
            /accounts/{identifier}/access/service_tokens/{uuid}/refresh:
              post:
                tags:
                  - Access service tokens
                summary: Refresh a service token
                description: Refreshes the expiration of a service token.
            /accounts/{identifier}/access/service_tokens/{uuid}/rotate:
              post:
                tags:
                  - Access service tokens
                summary: Rotate a service token
                description: >-
                  Generates a new Client Secret for a service token and revokes
                  the old one.
            /accounts/{identifier}/access/tags:
              get:
                tags:
                  - Access tags
                summary: List tags
                description: List tags
              post:
                tags:
                  - Access tags
                summary: Create a tag
                description: Create a tag
            /accounts/{identifier}/access/tags/{name}:
              delete:
                tags:
                  - Access tags
                summary: Delete a tag
                description: Delete a tag
              get:
                tags:
                  - Access tags
                summary: Get a tag
                description: Get a tag
              put:
                tags:
                  - Access tags
                summary: Update a tag
                description: Update a tag
            /accounts/{identifier}/access/users:
              get:
                tags:
                  - Zero Trust users
                summary: Get users
                description: Gets a list of users for an account.
            /accounts/{identifier}/access/users/{id}/active_sessions:
              get:
                tags:
                  - Zero Trust users
                summary: Get active sessions
                description: Get active sessions for a single user.
            /accounts/{identifier}/access/users/{id}/active_sessions/{nonce}:
              get:
                tags:
                  - Zero Trust users
                summary: Get single active session
                description: Get an active session for a single user.
            /accounts/{identifier}/access/users/{id}/failed_logins:
              get:
                tags:
                  - Zero Trust users
                summary: Get failed logins
                description: Get all failed login attempts for a single user.
            /accounts/{identifier}/access/users/{id}/last_seen_identity:
              get:
                tags:
                  - Zero Trust users
                summary: Get last seen identity
                description: Get last seen identity for a single user.
            /certificates:
              get:
                tags:
                  - Origin CA
                summary: List Certificates
                description: >-
                  List all existing Origin CA certificates for a given zone. Use
                  your Origin CA Key as your User Service Key when calling this
                  endpoint ([see above](#requests)).
              post:
                tags:
                  - Origin CA
                summary: Create Certificate
                description: >-
                  Create an Origin CA certificate. Use your Origin CA Key as
                  your User Service Key when calling this endpoint ([see
                  above](#requests)).
            /certificates/{certificate_id}:
              delete:
                tags:
                  - Origin CA
                summary: Revoke Certificate
                description: >-
                  Revoke an existing Origin CA certificate by its serial number.
                  Use your Origin CA Key as your User Service Key when calling
                  this endpoint ([see above](#requests)).
              get:
                tags:
                  - Origin CA
                summary: Get Certificate
                description: >-
                  Get an existing Origin CA certificate by its serial number.
                  Use your Origin CA Key as your User Service Key when calling
                  this endpoint ([see above](#requests)).
            /ips:
              get:
                tags:
                  - Cloudflare IPs
                summary: Cloudflare/JD Cloud IP Details
                description: >-
                  Get IPs used on the Cloudflare/JD Cloud network, see
                  https://www.cloudflare.com/ips for Cloudflare IPs or
                  https://developers.cloudflare.com/china-network/reference/infrastructure/
                  for JD Cloud IPs.
            /memberships:
              get:
                tags:
                  - User's Account Memberships
                summary: List Memberships
                description: List memberships of accounts the user can access.
            /memberships/{membership_id}:
              delete:
                tags:
                  - User's Account Memberships
                summary: Delete Membership
                description: Remove the associated member from an account.
              get:
                tags:
                  - User's Account Memberships
                summary: Membership Details
                description: Get a specific membership.
              put:
                tags:
                  - User's Account Memberships
                summary: Update Membership
                description: Accept or reject this account invitation.
            /organizations/{organization_id}/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get organization audit logs
                description: >-
                  Gets a list of audit logs for an organization. Can be filtered
                  by who made the change, on which zone, and the timeframe of
                  the change.
            /radar/annotations/outages:
              get:
                tags:
                  - Radar Annotations
                summary: Get latest Internet outages and anomalies.
            /radar/annotations/outages/locations:
              get:
                tags:
                  - Radar Annotations
                summary: Get the number of outages for locations.
            /radar/as112/summary/dnssec:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNSSEC Summary
                description: >-
                  Percentage distribution of DNS queries to AS112 by DNSSEC
                  support.
            /radar/as112/summary/edns:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 EDNS Summary
                description: >-
                  Percentage distribution of DNS queries, to AS112, by EDNS
                  support.
            /radar/as112/summary/ip_version:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 IP Version Summary
                description: >-
                  Percentage distribution of DNS queries to AS112 per IP
                  Version.
            /radar/as112/summary/protocol:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Protocol Summary
                description: Percentage distribution of DNS queries to AS112 per protocol.
            /radar/as112/summary/query_type:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 Query Types Summary
                description: Percentage distribution of DNS queries to AS112 by Query Type.
            /radar/as112/summary/response_codes:
              get:
                tags:
                  - Radar AS112
                summary: Get a summary of AS112 Response Codes
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Response Codes.
            /radar/as112/timeseries:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Queries Time Series
                description: Get AS112 queries change over time.
            /radar/as112/timeseries_groups/dnssec:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNSSEC Support Time Series
                description: >-
                  Percentage distribution of DNS AS112 queries by DNSSEC support
                  over time.
            /radar/as112/timeseries_groups/edns:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 EDNS Support Summary
                description: >-
                  Percentage distribution of AS112 DNS queries by EDNS support
                  over time.
            /radar/as112/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 IP Version Time Series
                description: >-
                  Percentage distribution of AS112 DNS queries by IP Version
                  over time.
            /radar/as112/timeseries_groups/protocol:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 DNS Protocol Time Series
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Protocol over time.
            /radar/as112/timeseries_groups/query_type:
              get:
                tags:
                  - Radar AS112
                summary: Get AS112 Query Types Time Series
                description: >-
                  Percentage distribution of AS112 DNS queries by Query Type
                  over time.
            /radar/as112/timeseries_groups/response_codes:
              get:
                tags:
                  - Radar AS112
                summary: Get a time series of AS112 Response Codes
                description: >-
                  Percentage distribution of AS112 dns requests classified per
                  Response Codes over time.
            /radar/as112/top/locations:
              get:
                tags:
                  - Radar AS112
                summary: Get top autonomous systems by AS112 DNS queries
                description: >-
                  Get the top locations by AS112 DNS queries. Values are a
                  percentage out of the total queries.
            /radar/as112/top/locations/dnssec/{dnssec}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations By DNS Queries DNSSEC Support
                description: Get the top locations by DNS queries DNSSEC support to AS112.
            /radar/as112/top/locations/edns/{edns}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations By EDNS Support
                description: Get the top locations, by DNS queries EDNS support to AS112.
            /radar/as112/top/locations/ip_version/{ip_version}:
              get:
                tags:
                  - Radar AS112
                summary: Get Top Locations by DNS Queries IP version
                description: Get the top locations by DNS queries IP version to AS112.
            /radar/attacks/layer3/summary:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks Summary
                description: >-
                  Percentage distribution of network protocols in layer 3/4
                  attacks over a given time period.
            /radar/attacks/layer3/summary/bitrate:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Bitrate Summary
                description: Percentage distribution of attacks by bitrate.
            /radar/attacks/layer3/summary/duration:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Durations Summary
                description: Percentage distribution of attacks by duration.
            /radar/attacks/layer3/summary/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get IP Versions Summary
                description: Percentage distribution of attacks by ip version used.
            /radar/attacks/layer3/summary/protocol:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Protocols Summary
                description: Percentage distribution of attacks by protocol used.
            /radar/attacks/layer3/summary/vector:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attack Vector Summary
                description: Percentage distribution of attacks by vector.
            /radar/attacks/layer3/timeseries:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attacks By Bytes Summary
                description: Get attacks change over time by bytes.
            /radar/attacks/layer3/timeseries_groups:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Network Protocol Time Series
                description: >-
                  Get a timeseries of the percentage distribution of network
                  protocols in Layer 3/4 attacks.
            /radar/attacks/layer3/timeseries_groups/bitrate:
              get:
                tags:
                  - Radar Attacks
                summary: Get Attacks By Bitrate Time Series
                description: Percentage distribution of attacks by bitrate over time.
            /radar/attacks/layer3/timeseries_groups/duration:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attack By Duration Time Series
                description: Percentage distribution of attacks by duration over time.
            /radar/attacks/layer3/timeseries_groups/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Target Industries Time Series
                description: Percentage distribution of attacks by industry used over time.
            /radar/attacks/layer3/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By IP Version Time Series
                description: >-
                  Percentage distribution of attacks by ip version used over
                  time.
            /radar/attacks/layer3/timeseries_groups/protocol:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Protocol Timeseries
                description: Percentage distribution of attacks by protocol used over time.
            /radar/attacks/layer3/timeseries_groups/vector:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Vector
                description: Percentage distribution of attacks by vector used over time.
            /radar/attacks/layer3/timeseries_groups/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 3 Attacks By Vertical Time Series
                description: Percentage distribution of attacks by vertical used over time.
            /radar/attacks/layer3/top/attacks:
              get:
                tags:
                  - Radar Attacks
                summary: >-
                  Get top attack pairs (origin and target locations) of Layer 3
                  attacks
                description: >-
                  Get the top attacks from origin to target location. Values are
                  a percentage out of the total layer 3 attacks (with billing
                  country). You can optionally limit the number of attacks per
                  origin/target location (useful if all the top attacks are from
                  or to the same location).
            /radar/attacks/layer3/top/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Industry of attack
                description: Get the Industry of attacks.
            /radar/attacks/layer3/top/locations/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get top origin locations of attack
                description: Get the origin locations of attacks.
            /radar/attacks/layer3/top/locations/target:
              get:
                tags:
                  - Radar Attacks
                summary: Get top target locations of attack
                description: Get the target locations of attacks.
            /radar/attacks/layer3/top/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Verticals of attack
                description: Get the Verticals of attacks.
            /radar/attacks/layer7/summary:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks Summary
                description: >-
                  Percentage distribution of mitigation techniques in Layer 7
                  attacks.
            /radar/attacks/layer7/summary/http_method:
              get:
                tags:
                  - Radar Attacks
                summary: Get HTTP Method Summary
                description: Percentage distribution of attacks by http method used.
            /radar/attacks/layer7/summary/http_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get HTTP Version Summary
                description: Percentage distribution of attacks by http version used.
            /radar/attacks/layer7/summary/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Ip Version Summary
                description: Percentage distribution of attacks by ip version used.
            /radar/attacks/layer7/summary/managed_rules:
              get:
                tags:
                  - Radar Attacks
                summary: Get Managed Rules Summary
                description: Percentage distribution of attacks by managed rules used.
            /radar/attacks/layer7/summary/mitigation_product:
              get:
                tags:
                  - Radar Attacks
                summary: Get Mitigation Product Summary
                description: Percentage distribution of attacks by mitigation product used.
            /radar/attacks/layer7/timeseries:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks Time Series
                description: >-
                  Get a timeseries of Layer 7 attacks. Values represent HTTP
                  requests and are normalized using min-max by default.
            /radar/attacks/layer7/timeseries_groups:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Mitigation Technique Time Series
                description: >-
                  Get a time series of the percentual distribution of mitigation
                  techniques, over time.
            /radar/attacks/layer7/timeseries_groups/http_method:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By HTTP Method Time Series
                description: >-
                  Percentage distribution of attacks by http method used over
                  time.
            /radar/attacks/layer7/timeseries_groups/http_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By HTTP Version Time Series
                description: >-
                  Percentage distribution of attacks by http version used over
                  time.
            /radar/attacks/layer7/timeseries_groups/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Target Industries Time Series
                description: Percentage distribution of attacks by industry used over time.
            /radar/attacks/layer7/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By IP Version Time Series
                description: >-
                  Percentage distribution of attacks by ip version used over
                  time.
            /radar/attacks/layer7/timeseries_groups/managed_rules:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Managed Rules Time Series
                description: >-
                  Percentage distribution of attacks by managed rules used over
                  time.
            /radar/attacks/layer7/timeseries_groups/mitigation_product:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Mitigation Product Time Series
                description: >-
                  Percentage distribution of attacks by mitigation product used
                  over time.
            /radar/attacks/layer7/timeseries_groups/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get Layer 7 Attacks By Vertical Time Series
                description: Percentage distribution of attacks by vertical used over time.
            /radar/attacks/layer7/top/ases/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get Top Origin Autonomous Systems By Layer 7 Attacks
                description: >-
                  Get the top origin Autonomous Systems of and by layer 7
                  attacks. Values are a percentage out of the total layer 7
                  attacks. The origin Autonomous Systems is determined by the
                  client IP.
            /radar/attacks/layer7/top/attacks:
              get:
                tags:
                  - Radar Attacks
                summary: >-
                  Get Top Attack Pairs (origin and target locations) By Layer 7
                  Attacks
                description: >-
                  Get the top attacks from origin to target location. Values are
                  a percentage out of the total layer 7 attacks (with billing
                  country). The attack magnitude can be defined by the number of
                  mitigated requests or by the number of zones affected. You can
                  optionally limit the number of attacks per origin/target
                  location (useful if all the top attacks are from or to the
                  same location).
            /radar/attacks/layer7/top/industry:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Industry of attack
                description: Get the Industry of attacks.
            /radar/attacks/layer7/top/locations/origin:
              get:
                tags:
                  - Radar Attacks
                summary: Get Top Origin Locations By Layer 7 Attacks
                description: >-
                  Get the top origin locations of and by layer 7 attacks. Values
                  are a percentage out of the total layer 7 attacks. The origin
                  location is determined by the client IP.
            /radar/attacks/layer7/top/locations/target:
              get:
                tags:
                  - Radar Attacks
                summary: Get layer 7 top target locations
                description: >-
                  Get the top target locations of and by layer 7 attacks. Values
                  are a percentage out of the total layer 7 attacks. The target
                  location is determined by the attacked zone's billing country,
                  when available.
            /radar/attacks/layer7/top/vertical:
              get:
                tags:
                  - Radar Attacks
                summary: Get top Verticals of attack
                description: Get the Verticals of attacks.
            /radar/bgp/hijacks/events:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP hijack events
                description: Get the BGP hijack events. (Beta)
            /radar/bgp/leaks/events:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP route leak events
                description: Get the BGP route leak events (Beta).
            /radar/bgp/routes/moas:
              get:
                tags:
                  - Radar BGP
                summary: Get MOASes
                description: >-
                  List all Multi-origin AS (MOAS) prefixes on the global routing
                  tables.
            /radar/bgp/routes/pfx2as:
              get:
                tags:
                  - Radar BGP
                summary: Get prefix-to-origin mapping
                description: Lookup prefix-to-origin mapping on global routing tables.
            /radar/bgp/routes/stats:
              get:
                tags:
                  - Radar BGP
                summary: 'Get BGP routing table stats '
                description: Get the BGP routing table stats (Beta).
            /radar/bgp/routes/timeseries:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP IP space time series
                description: >-
                  Gets time-series data for the announced IP space count,
                  represented as the number of IPv4 /24s and IPv6 /48s, for a
                  given ASN.
            /radar/bgp/timeseries:
              get:
                tags:
                  - Radar BGP
                summary: Get BGP time series
                description: >-
                  Gets BGP updates change over time. Raw values are returned.
                  When requesting updates of an autonomous system (AS), only BGP
                  updates of type announcement are returned.
            /radar/bgp/top/ases:
              get:
                tags:
                  - Radar BGP
                summary: Get top autonomous systems
                description: >-
                  Get the top autonomous systems (AS) by BGP updates
                  (announcements only). Values are a percentage out of the total
                  updates.
            /radar/bgp/top/ases/prefixes:
              get:
                tags:
                  - Radar BGP
                summary: Get list of ASNs ordered by prefix count
                description: >-
                  Get the full list of autonomous systems on the global routing
                  table ordered by announced prefixes count. The data comes from
                  public BGP MRT data archives and updates every 2 hours.
            /radar/bgp/top/prefixes:
              get:
                tags:
                  - Radar BGP
                summary: Get top prefixes
                description: >-
                  Get the top network prefixes by BGP updates. Values are a
                  percentage out of the total BGP updates.
            /radar/connection_tampering/summary:
              get:
                tags:
                  - Radar Connection Tampering
                summary: Get Connection Tampering Summary
                description: >-
                  Distribution of connection tampering types over a given time
                  period.
            /radar/connection_tampering/timeseries_groups:
              get:
                tags:
                  - Radar Connection Tampering
                summary: Get Connection Tampering Time Series
                description: Distribution of connection tampering types over time.
            /radar/datasets:
              get:
                tags:
                  - Radar Datasets
                summary: Get Datasets
                description: Get a list of datasets.
            /radar/datasets/{alias}:
              get:
                tags:
                  - Radar Datasets
                summary: Get Dataset csv Stream
                description: >-
                  Get the csv content of a given dataset by alias or id. When
                  getting the content by alias the latest dataset is returned,
                  optionally filtered by the latest available at a given date.
            /radar/datasets/download:
              post:
                tags:
                  - Radar Datasets
                summary: Get Dataset download url
                description: Get a url to download a single dataset.
            /radar/dns/top/ases:
              get:
                tags:
                  - Radar DNS
                summary: Get Top Autonomous Systems by DNS queries.
                description: >-
                  Get top autonomous systems by DNS queries made to Cloudflare's
                  public DNS resolver.
            /radar/dns/top/locations:
              get:
                tags:
                  - Radar DNS
                summary: Get Top Locations by DNS queries
                description: >-
                  Get top locations by DNS queries made to Cloudflare's public
                  DNS resolver.
            /radar/email/routing/summary/arc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get ARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per ARC
                  validation.
            /radar/email/routing/summary/dkim:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DKIM Validations Summary
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation.
            /radar/email/routing/summary/dmarc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DMARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation.
            /radar/email/routing/summary/encrypted:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Encrypted Summary
                description: Percentage distribution of emails by Encrypted
            /radar/email/routing/summary/ip_version:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Ip Version Summary
                description: Percentage distribution of emails by Ip Version.
            /radar/email/routing/summary/spf:
              get:
                tags:
                  - Radar Email Routing
                summary: Get SPF Validations Summary
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation.
            /radar/email/routing/timeseries_groups/arc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get ARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per Arc
                  validation over time.
            /radar/email/routing/timeseries_groups/dkim:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DKIM Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation over time.
            /radar/email/routing/timeseries_groups/dmarc:
              get:
                tags:
                  - Radar Email Routing
                summary: Get DMARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation over time.
            /radar/email/routing/timeseries_groups/encrypted:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Encrypted Time Series
                description: Percentage distribution of emails by Encrypted over time.
            /radar/email/routing/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Email Routing
                summary: Get Ip Version Time Series
                description: Percentage distribution of emails by Ip Version over time.
            /radar/email/routing/timeseries_groups/spf:
              get:
                tags:
                  - Radar Email Routing
                summary: Get SPF Validations Time Series
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation over time.
            /radar/email/security/summary/arc:
              get:
                tags:
                  - Radar Email Security
                summary: Get ARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per ARC
                  validation.
            /radar/email/security/summary/dkim:
              get:
                tags:
                  - Radar Email Security
                summary: Get DKIM Validations Summary
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation.
            /radar/email/security/summary/dmarc:
              get:
                tags:
                  - Radar Email Security
                summary: Get DMARC Validations Summary
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation.
            /radar/email/security/summary/malicious:
              get:
                tags:
                  - Radar Email Security
                summary: Get MALICIOUS Validations Summary
                description: Percentage distribution of emails classified as MALICIOUS.
            /radar/email/security/summary/spam:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPAM Summary
                description: >-
                  Proportion of emails categorized as either spam or legitimate
                  (non-spam).
            /radar/email/security/summary/spf:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPF Validations Summary
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation.
            /radar/email/security/summary/spoof:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPOOF Summary
                description: >-
                  Proportion of emails categorized as either spoof or legitimate
                  (non-spoof).
            /radar/email/security/summary/threat_category:
              get:
                tags:
                  - Radar Email Security
                summary: Get Threat Categories Summary
                description: >-
                  Percentage distribution of emails classified in Threat
                  Categories.
            /radar/email/security/summary/tls_version:
              get:
                tags:
                  - Radar Email Security
                summary: Get TLS Version Summary
                description: Percentage distribution of emails classified per TLS Version.
            /radar/email/security/timeseries_groups/arc:
              get:
                tags:
                  - Radar Email Security
                summary: Get ARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per Arc
                  validation over time.
            /radar/email/security/timeseries_groups/dkim:
              get:
                tags:
                  - Radar Email Security
                summary: Get DKIM Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DKIM
                  validation over time.
            /radar/email/security/timeseries_groups/dmarc:
              get:
                tags:
                  - Radar Email Security
                summary: Get DMARC Validations Time Series
                description: >-
                  Percentage distribution of emails classified per DMARC
                  validation over time.
            /radar/email/security/timeseries_groups/malicious:
              get:
                tags:
                  - Radar Email Security
                summary: Get MALICIOUS Validations Time Series
                description: >-
                  Percentage distribution of emails classified as MALICIOUS over
                  time.
            /radar/email/security/timeseries_groups/spam:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPAM Validations Time Series
                description: >-
                  Percentage distribution of emails classified as SPAM over
                  time.
            /radar/email/security/timeseries_groups/spf:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPF Validations Time Series
                description: >-
                  Percentage distribution of emails classified per SPF
                  validation over time.
            /radar/email/security/timeseries_groups/spoof:
              get:
                tags:
                  - Radar Email Security
                summary: Get SPOOF Validations Time Series
                description: >-
                  Percentage distribution of emails classified as SPOOF over
                  time.
            /radar/email/security/timeseries_groups/threat_category:
              get:
                tags:
                  - Radar Email Security
                summary: Get Threat Categories Time Series
                description: >-
                  Percentage distribution of emails classified in Threat
                  Categories over time.
            /radar/email/security/timeseries_groups/tls_version:
              get:
                tags:
                  - Radar Email Security
                summary: Get TLS Version Time Series
                description: >-
                  Percentage distribution of emails classified per TLS Version
                  over time.
            /radar/email/security/top/tlds:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Email Messages
                description: >-
                  Get the top TLDs by email messages. Values are a percentage
                  out of the total emails.
            /radar/email/security/top/tlds/malicious/{malicious}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Malicious Classification
                description: Get the TLDs by emails classified as malicious or not.
            /radar/email/security/top/tlds/spam/{spam}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Spam Classification
                description: Get the top TLDs by emails classified as Spam or not.
            /radar/email/security/top/tlds/spoof/{spoof}:
              get:
                tags:
                  - Radar Email Security
                summary: Get Top TLDs By Spoof Classification
                description: Get the TLDs by emails classified as spoof or not.
            /radar/entities/asns:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous systems
                description: Gets a list of autonomous systems (AS).
            /radar/entities/asns/{asn}:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous system information by AS number
                description: >-
                  Get the requested autonomous system information. A confidence
                  level below `5` indicates a low level of confidence in the
                  traffic data - normally this happens because Cloudflare has a
                  small amount of traffic from/to this AS). Population estimates
                  come from APNIC (refer to https://labs.apnic.net/?p=526).
            /radar/entities/asns/{asn}/rel:
              get:
                tags:
                  - Radar Entities
                summary: Get AS-level relationships by AS number
                description: Get AS-level relationship for given networks.
            /radar/entities/asns/ip:
              get:
                tags:
                  - Radar Entities
                summary: Get autonomous system information by IP address
                description: >-
                  Get the requested autonomous system information based on IP
                  address. Population estimates come from APNIC (refer to
                  https://labs.apnic.net/?p=526).
            /radar/entities/ip:
              get:
                tags:
                  - Radar Entities
                summary: Get IP address
                description: 'Get IP address information. '
            /radar/entities/locations:
              get:
                tags:
                  - Radar Entities
                summary: Get locations
                description: Get a list of locations.
            /radar/entities/locations/{location}:
              get:
                tags:
                  - Radar Entities
                summary: Get location
                description: >-
                  Get the requested location information. A confidence level
                  below `5` indicates a low level of confidence in the traffic
                  data - normally this happens because Cloudflare has a small
                  amount of traffic from/to this location).
            /radar/http/summary/bot_class:
              get:
                tags:
                  - Radar Http
                summary: Get Bot Class Summary
                description: >-
                  Percentage distribution of bot-generated traffic to genuine
                  human traffic, as classified by Cloudflare. Visit
                  https://developers.cloudflare.com/radar/concepts/bot-classes/
                  for more information.
            /radar/http/summary/device_type:
              get:
                tags:
                  - Radar Http
                summary: Get Device Type Summary
                description: >-
                  Percentage of Internet traffic generated by mobile, desktop,
                  and other types of devices, over a given time period.
            /radar/http/summary/http_protocol:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP protocols summary
                description: >-
                  Percentage distribution of traffic per HTTP protocol over a
                  given time period.
            /radar/http/summary/http_version:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP Versions Summary
                description: >-
                  Percentage distribution of traffic per HTTP protocol version
                  over a given time period.
            /radar/http/summary/ip_version:
              get:
                tags:
                  - Radar Http
                summary: Get IP Version Summary
                description: >-
                  Percentage distribution of Internet traffic based on IP
                  protocol versions, such as IPv4 and IPv6, over a given time
                  period.
            /radar/http/summary/os:
              get:
                tags:
                  - Radar Http
                summary: Get Operating Systems Summary
                description: >-
                  Percentage distribution of Internet traffic generated by
                  different operating systems like Windows, macOS, Android, iOS,
                  and others, over a given time period.
            /radar/http/summary/tls_version:
              get:
                tags:
                  - Radar Http
                summary: Get TLS Versions Summary
                description: >-
                  Percentage distribution of traffic per TLS protocol version,
                  over a given time period.
            /radar/http/timeseries_groups/bot_class:
              get:
                tags:
                  - Radar Http
                summary: Get Bot Classes Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  classified as automated or human. Visit
                  https://developers.cloudflare.com/radar/concepts/bot-classes/
                  for more information.
            /radar/http/timeseries_groups/browser:
              get:
                tags:
                  - Radar Http
                summary: Get User Agents Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top user agents.
            /radar/http/timeseries_groups/browser_family:
              get:
                tags:
                  - Radar Http
                summary: Get User Agent Families Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top user agents aggregated in families.
            /radar/http/timeseries_groups/device_type:
              get:
                tags:
                  - Radar Http
                summary: Get Device Types Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per device type.
            /radar/http/timeseries_groups/http_protocol:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP protocols Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per HTTP protocol.
            /radar/http/timeseries_groups/http_version:
              get:
                tags:
                  - Radar Http
                summary: Get HTTP Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per HTTP protocol version.
            /radar/http/timeseries_groups/ip_version:
              get:
                tags:
                  - Radar Http
                summary: Get IP Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per IP protocol version.
            /radar/http/timeseries_groups/os:
              get:
                tags:
                  - Radar Http
                summary: Get Operating Systems Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic of
                  the top operating systems.
            /radar/http/timeseries_groups/tls_version:
              get:
                tags:
                  - Radar Http
                summary: Get TLS Versions Time Series
                description: >-
                  Get a time series of the percentage distribution of traffic
                  per TLS protocol version.
            /radar/http/top/ases:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Requests
                description: >-
                  Get the top autonomous systems by HTTP traffic. Values are a
                  percentage out of the total traffic.
            /radar/http/top/ases/bot_class/{bot_class}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Bot Class
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested bot class. These two categories use Cloudflare's bot
                  score - refer to [Bot
                  Scores](https://developers.cloudflare.com/bots/concepts/bot-score)
                  for more information. Values are a percentage out of the total
                  traffic.
            /radar/http/top/ases/device_type/{device_type}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Device Type
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested device type. Values are a percentage out of the
                  total traffic.
            /radar/http/top/ases/http_protocol/{http_protocol}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Protocol
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested HTTP protocol. Values are a percentage out of the
                  total traffic.
            /radar/http/top/ases/http_version/{http_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By HTTP Version
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested HTTP protocol version. Values are a percentage out
                  of the total traffic.
            /radar/http/top/ases/ip_version/{ip_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By IP Version
                description: >-
                  Get the top autonomous systems, by HTTP traffic, of the
                  requested IP protocol version. Values are a percentage out of
                  the total traffic.
            /radar/http/top/ases/os/{os}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By Operating System
                description: >-
                  Get the top autonomous systems, by HTTP traffic, of the
                  requested operating systems. Values are a percentage out of
                  the total traffic.
            /radar/http/top/ases/tls_version/{tls_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Autonomous Systems By TLS Version
                description: >-
                  Get the top autonomous systems (AS), by HTTP traffic, of the
                  requested TLS protocol version. Values are a percentage out of
                  the total traffic.
            /radar/http/top/browser_families:
              get:
                tags:
                  - Radar Http
                summary: Get Top User Agents Families by HTTP requests
                description: >-
                  Get the top user agents aggregated in families by HTTP
                  traffic. Values are a percentage out of the total traffic.
            /radar/http/top/browsers:
              get:
                tags:
                  - Radar Http
                summary: Get Top User Agents By HTTP requests
                description: >-
                  Get the top user agents by HTTP traffic. Values are a
                  percentage out of the total traffic.
            /radar/http/top/locations:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP requests
                description: >-
                  Get the top locations by HTTP traffic. Values are a percentage
                  out of the total traffic.
            /radar/http/top/locations/bot_class/{bot_class}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Bot Class
                description: >-
                  Get the top locations, by HTTP traffic, of the requested bot
                  class. These two categories use Cloudflare's bot score - refer
                  to [Bot
                  scores])https://developers.cloudflare.com/bots/concepts/bot-score).
                  Values are a percentage out of the total traffic.
            /radar/http/top/locations/device_type/{device_type}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Device Type
                description: >-
                  Get the top locations, by HTTP traffic, of the requested
                  device type. Values are a percentage out of the total traffic.
            /radar/http/top/locations/http_protocol/{http_protocol}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP Protocol
                description: >-
                  Get the top locations, by HTTP traffic, of the requested HTTP
                  protocol. Values are a percentage out of the total traffic.
            /radar/http/top/locations/http_version/{http_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By HTTP Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested HTTP
                  protocol. Values are a percentage out of the total traffic.
            /radar/http/top/locations/ip_version/{ip_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By IP Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested IP
                  protocol version. Values are a percentage out of the total
                  traffic.
            /radar/http/top/locations/os/{os}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By Operating System
                description: >-
                  Get the top locations, by HTTP traffic, of the requested
                  operating systems. Values are a percentage out of the total
                  traffic.
            /radar/http/top/locations/tls_version/{tls_version}:
              get:
                tags:
                  - Radar Http
                summary: Get Top Locations By TLS Version
                description: >-
                  Get the top locations, by HTTP traffic, of the requested TLS
                  protocol version. Values are a percentage out of the total
                  traffic.
            /radar/netflows/timeseries:
              get:
                tags:
                  - Radar Netflows
                summary: Get NetFlows Time Series
                description: >-
                  Get network traffic change over time. Visit
                  https://en.wikipedia.org/wiki/NetFlow for more information on
                  NetFlows. 
            /radar/netflows/top/ases:
              get:
                tags:
                  - Radar Netflows
                summary: Get Top Autonomous Systems By Network Traffic
                description: >-
                  Get the top autonomous systems (AS) by network traffic
                  (NetFlows) over a given time period. Visit
                  https://en.wikipedia.org/wiki/NetFlow for more information.
            /radar/netflows/top/locations:
              get:
                tags:
                  - Radar Netflows
                summary: Get Top Locations By Network Traffic
                description: >-
                  Get the top locations by network traffic (NetFlows) over a
                  given time period. Visit https://en.wikipedia.org/wiki/NetFlow
                  for more information.
            /radar/quality/iqi/summary:
              get:
                tags:
                  - Radar Quality
                summary: Get IQI Summary
                description: >-
                  Get a summary (percentiles) of bandwidth, latency or DNS
                  response time from the Radar Internet Quality Index (IQI).
            /radar/quality/iqi/timeseries_groups:
              get:
                tags:
                  - Radar Quality
                summary: Get IQI Time Series
                description: >-
                  Get a time series (percentiles) of bandwidth, latency or DNS
                  response time from the Radar Internet Quality Index (IQI).
            /radar/quality/speed/histogram:
              get:
                tags:
                  - Radar Quality
                summary: Get Speed Tests Histogram
                description: >-
                  Get an histogram from the previous 90 days of Cloudflare Speed
                  Test data, split into fixed bandwidth (Mbps), latency (ms) or
                  jitter (ms) buckets.
            /radar/quality/speed/summary:
              get:
                tags:
                  - Radar Quality
                summary: Get Speed Tests Summary
                description: >-
                  Get a summary of bandwidth, latency, jitter and packet loss,
                  from the previous 90 days of Cloudflare Speed Test data.
            /radar/quality/speed/top/ases:
              get:
                tags:
                  - Radar Quality
                summary: Get Top Speed Test Autonomous Systems
                description: >-
                  Get the top autonomous systems by bandwidth, latency, jitter
                  or packet loss, from the previous 90 days of Cloudflare Speed
                  Test data.
            /radar/quality/speed/top/locations:
              get:
                tags:
                  - Radar Quality
                summary: Get Top Speed Test Locations
                description: >-
                  Get the top locations by bandwidth, latency, jitter or packet
                  loss, from the previous 90 days of Cloudflare Speed Test data.
            /radar/ranking/domain/{domain}:
              get:
                tags:
                  - Radar Ranking
                summary: Get Domains Rank details
                description: |-
                  Gets Domains Rank details. 
                      Cloudflare provides an ordered rank for the top 100 domains, but for the remainder it only provides ranking buckets
                      like top 200 thousand, top one million, etc.. These are available through Radar datasets endpoints.
            /radar/ranking/timeseries_groups:
              get:
                tags:
                  - Radar Ranking
                summary: Get Domains Rank time series
                description: >-
                  Gets Domains Rank updates change over time. Raw values are
                  returned.
            /radar/ranking/top:
              get:
                tags:
                  - Radar Ranking
                summary: Get Top or Trending Domains
                description: >-
                  Get top or trending domains based on their rank. Popular
                  domains are domains of broad appeal based on how people use
                  the Internet. Trending domains are domains that are generating
                  a surge in interest. For more information on top domains, see
                  https://blog.cloudflare.com/radar-domain-rankings/.
            /radar/search/global:
              get:
                tags:
                  - Radar Search
                summary: Search for locations, autonomous systems (AS) and reports.
                description: >-
                  Lets you search for locations, autonomous systems (AS) and
                  reports.
            /radar/traffic_anomalies:
              get:
                tags:
                  - Radar Traffic Anomalies
                summary: Get latest Internet traffic anomalies.
                description: >-
                  Internet traffic anomalies are signals that might point to an
                  outage,
                          These alerts are automatically detected by Radar and then manually verified by our team.
                          This endpoint returns the latest alerts.
                          
            /radar/traffic_anomalies/locations:
              get:
                tags:
                  - Radar Traffic Anomalies
                summary: Get top locations by total traffic anomalies generated.
                description: >-
                  Internet traffic anomalies are signals that might point to an
                  outage,
                          These alerts are automatically detected by Radar and then manually verified by our team.
                          This endpoint returns the sum of alerts grouped by location.
                          
            /radar/verified_bots/top/bots:
              get:
                tags:
                  - Radar Verified Bots
                summary: Get Top Verified Bots By HTTP Requests
                description: >-
                  Get top verified bots by HTTP requests, with owner and
                  category.
            /radar/verified_bots/top/categories:
              get:
                tags:
                  - Radar Verified Bots
                summary: Get Top Verified Bot Categories By HTTP Requests
                description: >-
                  Get top verified bot categories by HTTP requests, along with
                  their corresponding percentage, over the total verified bot
                  HTTP requests.
            /user:
              get:
                tags:
                  - User
                summary: User Details
              patch:
                tags:
                  - User
                summary: Edit User
                description: Edit part of your user details.
            /user/audit_logs:
              get:
                tags:
                  - Audit Logs
                summary: Get user audit logs
                description: >-
                  Gets a list of audit logs for a user account. Can be filtered
                  by who made the change, on which zone, and the timeframe of
                  the change.
            /user/billing/history:
              get:
                tags:
                  - User Billing History
                summary: Billing History Details
                description: Accesses your billing history object.
            /user/billing/profile:
              get:
                tags:
                  - User Billing Profile
                summary: Billing Profile Details
                description: Accesses your billing profile object.
            /user/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for a user
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of the user. You can filter the
                  results using several optional parameters.
              post:
                tags:
                  - IP Access rules for a user
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for all zones owned by the
                  current user.


                  Note: To create an IP Access rule that applies to a specific
                  zone, refer to the [IP Access rules for a
                  zone](#ip-access-rules-for-a-zone) endpoints.
            /user/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for a user
                summary: Delete an IP Access rule
                description: >-
                  Deletes an IP Access rule at the user level.


                  Note: Deleting a user-level rule will affect all zones owned
                  by the user.
              patch:
                tags:
                  - IP Access rules for a user
                summary: Update an IP Access rule
                description: >-
                  Updates an IP Access rule defined at the user level. You can
                  only update the rule action (`mode` parameter) and notes.
            /user/invites:
              get:
                tags:
                  - User's Invites
                summary: List Invitations
                description: Lists all invitations associated with my user.
            /user/invites/{invite_id}:
              get:
                tags:
                  - User's Invites
                summary: Invitation Details
                description: Gets the details of an invitation.
              patch:
                tags:
                  - User's Invites
                summary: Respond to Invitation
                description: Responds to an invitation.
            /user/load_balancers/monitors:
              get:
                tags:
                  - Load Balancer Monitors
                summary: List Monitors
                description: List configured monitors for a user.
              post:
                tags:
                  - Load Balancer Monitors
                summary: Create Monitor
                description: Create a configured monitor.
            /user/load_balancers/monitors/{monitor_id}:
              delete:
                tags:
                  - Load Balancer Monitors
                summary: Delete Monitor
                description: Delete a configured monitor.
              get:
                tags:
                  - Load Balancer Monitors
                summary: Monitor Details
                description: List a single configured monitor for a user.
              patch:
                tags:
                  - Load Balancer Monitors
                summary: Patch Monitor
                description: >-
                  Apply changes to an existing monitor, overwriting the supplied
                  properties.
              put:
                tags:
                  - Load Balancer Monitors
                summary: Update Monitor
                description: Modify a configured monitor.
            /user/load_balancers/monitors/{monitor_id}/preview:
              post:
                tags:
                  - Load Balancer Monitors
                summary: Preview Monitor
                description: >-
                  Preview pools using the specified monitor with provided
                  monitor details. The returned preview_id can be used in the
                  preview endpoint to retrieve the results.
            /user/load_balancers/monitors/{monitor_id}/references:
              get:
                tags:
                  - Load Balancer Monitors
                summary: List Monitor References
                description: Get the list of resources that reference the provided monitor.
            /user/load_balancers/pools:
              get:
                tags:
                  - Load Balancer Pools
                summary: List Pools
                description: List configured pools.
              patch:
                tags:
                  - Load Balancer Pools
                summary: Patch Pools
                description: >-
                  Apply changes to a number of existing pools, overwriting the
                  supplied properties. Pools are ordered by ascending `name`.
                  Returns the list of affected pools. Supports the standard
                  pagination query parameters, either `limit`/`offset` or
                  `per_page`/`page`.
              post:
                tags:
                  - Load Balancer Pools
                summary: Create Pool
                description: Create a new pool.
            /user/load_balancers/pools/{pool_id}:
              delete:
                tags:
                  - Load Balancer Pools
                summary: Delete Pool
                description: Delete a configured pool.
              get:
                tags:
                  - Load Balancer Pools
                summary: Pool Details
                description: Fetch a single configured pool.
              patch:
                tags:
                  - Load Balancer Pools
                summary: Patch Pool
                description: >-
                  Apply changes to an existing pool, overwriting the supplied
                  properties.
              put:
                tags:
                  - Load Balancer Pools
                summary: Update Pool
                description: Modify a configured pool.
            /user/load_balancers/pools/{pool_id}/health:
              get:
                tags:
                  - Load Balancer Pools
                summary: Pool Health Details
                description: Fetch the latest pool health status for a single pool.
            /user/load_balancers/pools/{pool_id}/preview:
              post:
                tags:
                  - Load Balancer Pools
                summary: Preview Pool
                description: >-
                  Preview pool health using provided monitor details. The
                  returned preview_id can be used in the preview endpoint to
                  retrieve the results.
            /user/load_balancers/pools/{pool_id}/references:
              get:
                tags:
                  - Load Balancer Pools
                summary: List Pool References
                description: Get the list of resources that reference the provided pool.
            /user/load_balancers/preview/{preview_id}:
              get:
                tags:
                  - Load Balancer Monitors
                summary: Preview Result
                description: >-
                  Get the result of a previous preview operation using the
                  provided preview_id.
            /user/load_balancing_analytics/events:
              get:
                tags:
                  - Load Balancer Healthcheck Events
                summary: List Healthcheck Events
                description: List origin health changes.
            /user/organizations:
              get:
                tags:
                  - User's Organizations
                summary: List Organizations
                description: Lists organizations the user is associated with.
            /user/organizations/{organization_id}:
              delete:
                tags:
                  - User's Organizations
                summary: Leave Organization
                description: Removes association to an organization.
              get:
                tags:
                  - User's Organizations
                summary: Organization Details
                description: Gets a specific organization the user is associated with.
            /user/subscriptions:
              get:
                tags:
                  - User Subscription
                summary: Get User Subscriptions
                description: Lists all of a user's subscriptions.
            /user/subscriptions/{identifier}:
              delete:
                tags:
                  - User Subscription
                summary: Delete User Subscription
                description: Deletes a user's subscription.
              put:
                tags:
                  - User Subscription
                summary: Update User Subscription
                description: Updates a user's subscriptions.
            /user/tokens:
              get:
                tags:
                  - User API Tokens
                summary: List Tokens
                description: List all access tokens you created.
              post:
                tags:
                  - User API Tokens
                summary: Create Token
                description: Create a new access token.
            /user/tokens/{token_id}:
              delete:
                tags:
                  - User API Tokens
                summary: Delete Token
                description: Destroy a token.
              get:
                tags:
                  - User API Tokens
                summary: Token Details
                description: Get information about a specific token.
              put:
                tags:
                  - User API Tokens
                summary: Update Token
                description: Update an existing token.
            /user/tokens/{token_id}/value:
              put:
                tags:
                  - User API Tokens
                summary: Roll Token
                description: Roll the token secret.
            /user/tokens/permission_groups:
              get:
                tags:
                  - Permission Groups
                summary: List Permission Groups
                description: Find all available permission groups.
            /user/tokens/verify:
              get:
                tags:
                  - User API Tokens
                summary: Verify Token
                description: Test whether a token works.
            /zones:
              get:
                tags:
                  - Zone
                summary: List Zones
                description: Lists, searches, sorts, and filters your zones.
              post:
                tags:
                  - Zone
                summary: Create Zone
            /zones/{identifier}/access/apps:
              get:
                tags:
                  - Zone-Level Access applications
                summary: List Access Applications
                description: List all Access Applications in a zone.
              post:
                tags:
                  - Zone-Level Access applications
                summary: Add an Access application
                description: Adds a new application to Access.
            /zones/{identifier}/access/apps/{app_id}:
              delete:
                tags:
                  - Zone-Level Access applications
                summary: Delete an Access application
                description: Deletes an application from Access.
              get:
                tags:
                  - Zone-Level Access applications
                summary: Get an Access application
                description: Fetches information about an Access application.
              put:
                tags:
                  - Zone-Level Access applications
                summary: Update an Access application
                description: Updates an Access application.
            /zones/{identifier}/access/apps/{app_id}/revoke_tokens:
              post:
                tags:
                  - Zone-Level Access applications
                summary: Revoke application tokens
                description: Revokes all tokens issued for an application.
            /zones/{identifier}/access/apps/{app_id}/user_policy_checks:
              get:
                tags:
                  - Zone-Level Access applications
                summary: Test Access policies
                description: >-
                  Tests if a specific user has permission to access an
                  application.
            /zones/{identifier}/access/apps/{uuid}/ca:
              delete:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Delete a short-lived certificate CA
                description: Deletes a short-lived certificate CA.
              get:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Get a short-lived certificate CA
                description: Fetches a short-lived certificate CA and its public key.
              post:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: Create a short-lived certificate CA
                description: Generates a new short-lived certificate CA and public key.
            /zones/{identifier}/access/apps/{uuid}/policies:
              get:
                tags:
                  - Zone-Level Access policies
                summary: List Access policies
                description: Lists Access policies configured for an application.
              post:
                tags:
                  - Zone-Level Access policies
                summary: Create an Access policy
                description: Create a new Access policy for an application.
            /zones/{identifier}/access/apps/{uuid1}/policies/{uuid}:
              delete:
                tags:
                  - Zone-Level Access policies
                summary: Delete an Access policy
                description: Delete an Access policy.
              get:
                tags:
                  - Zone-Level Access policies
                summary: Get an Access policy
                description: Fetches a single Access policy.
              put:
                tags:
                  - Zone-Level Access policies
                summary: Update an Access policy
                description: Update a configured Access policy.
            /zones/{identifier}/access/apps/ca:
              get:
                tags:
                  - Zone-Level Access short-lived certificate CAs
                summary: List short-lived certificate CAs
                description: Lists short-lived certificate CAs and their public keys.
            /zones/{identifier}/access/certificates:
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: List mTLS certificates
                description: Lists all mTLS certificates.
              post:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Add an mTLS certificate
                description: Adds a new mTLS root certificate to Access.
            /zones/{identifier}/access/certificates/{uuid}:
              delete:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Delete an mTLS certificate
                description: Deletes an mTLS certificate.
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Get an mTLS certificate
                description: Fetches a single mTLS certificate.
              put:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Update an mTLS certificate
                description: Updates a configured mTLS certificate.
            /zones/{identifier}/access/certificates/settings:
              get:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: List all mTLS hostname settings
                description: List all mTLS hostname settings for this zone.
              put:
                tags:
                  - Zone-Level Access mTLS authentication
                summary: Update an mTLS certificate's hostname settings
                description: Updates an mTLS certificate's hostname settings.
            /zones/{identifier}/access/groups:
              get:
                tags:
                  - Zone-Level Access groups
                summary: List Access groups
                description: Lists all Access groups.
              post:
                tags:
                  - Zone-Level Access groups
                summary: Create an Access group
                description: Creates a new Access group.
            /zones/{identifier}/access/groups/{uuid}:
              delete:
                tags:
                  - Zone-Level Access groups
                summary: Delete an Access group
                description: Deletes an Access group.
              get:
                tags:
                  - Zone-Level Access groups
                summary: Get an Access group
                description: Fetches a single Access group.
              put:
                tags:
                  - Zone-Level Access groups
                summary: Update an Access group
                description: Updates a configured Access group.
            /zones/{identifier}/access/identity_providers:
              get:
                tags:
                  - Zone-Level Access identity providers
                summary: List Access identity providers
                description: Lists all configured identity providers.
              post:
                tags:
                  - Zone-Level Access identity providers
                summary: Add an Access identity provider
                description: Adds a new identity provider to Access.
            /zones/{identifier}/access/identity_providers/{uuid}:
              delete:
                tags:
                  - Zone-Level Access identity providers
                summary: Delete an Access identity provider
                description: Deletes an identity provider from Access.
              get:
                tags:
                  - Zone-Level Access identity providers
                summary: Get an Access identity provider
                description: Fetches a configured identity provider.
              put:
                tags:
                  - Zone-Level Access identity providers
                summary: Update an Access identity provider
                description: Updates a configured identity provider.
            /zones/{identifier}/access/organizations:
              get:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Get your Zero Trust organization
                description: Returns the configuration for your Zero Trust organization.
              post:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Create your Zero Trust organization
                description: Sets up a Zero Trust organization for your account.
              put:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Update your Zero Trust organization
                description: Updates the configuration for your Zero Trust organization.
            /zones/{identifier}/access/organizations/revoke_user:
              post:
                tags:
                  - Zone-Level Zero Trust organization
                summary: Revoke all Access tokens for a user
                description: Revokes a user's access across all applications.
            /zones/{identifier}/access/service_tokens:
              get:
                tags:
                  - Zone-Level Access service tokens
                summary: List service tokens
                description: Lists all service tokens.
              post:
                tags:
                  - Zone-Level Access service tokens
                summary: Create a service token
                description: >-
                  Generates a new service token. **Note:** This is the only time
                  you can get the Client Secret. If you lose the Client Secret,
                  you will have to create a new service token.
            /zones/{identifier}/access/service_tokens/{uuid}:
              delete:
                tags:
                  - Zone-Level Access service tokens
                summary: Delete a service token
                description: Deletes a service token.
              put:
                tags:
                  - Zone-Level Access service tokens
                summary: Update a service token
                description: Updates a configured service token.
            /zones/{identifier}/dns_analytics/report:
              get:
                tags:
                  - DNS Analytics
                summary: Table
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /zones/{identifier}/dns_analytics/report/bytime:
              get:
                tags:
                  - DNS Analytics
                summary: By Time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.


                  See [Analytics API
                  properties](https://developers.cloudflare.com/dns/reference/analytics-api-properties/)
                  for detailed information about the available query parameters.
            /zones/{identifier}/subscription:
              get:
                tags:
                  - Zone Subscription
                summary: Zone Subscription Details
                description: Lists zone subscription details.
              post:
                tags:
                  - Zone Subscription
                summary: Create Zone Subscription
                description: Create a zone subscription, either plan or add-ons.
              put:
                tags:
                  - Zone Subscription
                summary: Update Zone Subscription
                description: Updates zone subscriptions, either plan or add-ons.
            /zones/{zone_id}:
              delete:
                tags:
                  - Zone
                summary: Delete Zone
                description: Deletes an existing zone.
              get:
                tags:
                  - Zone
                summary: Zone Details
              patch:
                tags:
                  - Zone
                summary: Edit Zone
                description: Edits a zone. Only one zone property can be changed at a time.
            /zones/{zone_id}/acm/total_tls:
              get:
                tags:
                  - Total TLS
                summary: Total TLS Settings Details
                description: Get Total TLS Settings for a Zone.
              post:
                tags:
                  - Total TLS
                summary: Enable or Disable Total TLS
                description: Set Total TLS Settings or disable the feature for a Zone.
            /zones/{zone_id}/activation_check:
              put:
                tags:
                  - Zone
                summary: Rerun the Activation Check
                description: >-
                  Triggeres a new activation check for a PENDING Zone. This can
                  be

                  triggered every 5 min for paygo/ent customers, every hour for
                  FREE

                  Zones.
            /zones/{zone_id}/analytics/latency:
              get:
                tags:
                  - Argo Analytics for Zone
                summary: Argo Analytics for a zone
            /zones/{zone_id}/analytics/latency/colos:
              get:
                tags:
                  - Argo Analytics for Geolocation
                summary: Argo Analytics for a zone at different PoPs
            /zones/{zone_id}/api_gateway/configuration:
              get:
                tags:
                  - API Shield Settings
                summary: Retrieve information about specific configuration properties
              put:
                tags:
                  - API Shield Settings
                summary: Set configuration properties
            /zones/{zone_id}/api_gateway/discovery:
              get:
                tags:
                  - API Shield API Discovery
                summary: >-
                  Retrieve discovered operations on a zone rendered as OpenAPI
                  schemas
                description: >-
                  Retrieve the most up to date view of discovered operations,
                  rendered as OpenAPI schemas
            /zones/{zone_id}/api_gateway/discovery/operations:
              get:
                tags:
                  - API Shield API Discovery
                summary: Retrieve discovered operations on a zone
                description: Retrieve the most up to date view of discovered operations
              patch:
                tags:
                  - API Shield API Discovery
                summary: Patch discovered operations
                description: Update the `state` on one or more discovered operations
            /zones/{zone_id}/api_gateway/discovery/operations/{operation_id}:
              patch:
                tags:
                  - API Shield API Discovery
                summary: Patch discovered operation
                description: Update the `state` on a discovered operation
            /zones/{zone_id}/api_gateway/operations:
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve information about all operations on a zone
              post:
                tags:
                  - API Shield Endpoint Management
                summary: Add operations to a zone
                description: >-
                  Add one or more operations to a zone. Endpoints can contain
                  path variables. Host, method, endpoint will be normalized to a
                  canoncial form when creating an operation and must be unique
                  on the zone. Inserting an operation that matches an existing
                  one will return the record of the already existing operation
                  and update its last_updated date.
            /zones/{zone_id}/api_gateway/operations/{operation_id}:
              delete:
                tags:
                  - API Shield Endpoint Management
                summary: Delete an operation
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve information about an operation
            /zones/{zone_id}/api_gateway/operations/{operation_id}/schema_validation:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve operation-level schema validation settings
                description: >-
                  Retrieves operation-level schema validation settings on the
                  zone
              put:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update operation-level schema validation settings
                description: Updates operation-level schema validation settings on the zone
            /zones/{zone_id}/api_gateway/operations/schema_validation:
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update multiple operation-level schema validation settings
                description: >-
                  Updates multiple operation-level schema validation settings on
                  the zone
            /zones/{zone_id}/api_gateway/schemas:
              get:
                tags:
                  - API Shield Endpoint Management
                summary: Retrieve operations and features as OpenAPI schemas
            /zones/{zone_id}/api_gateway/settings/schema_validation:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve zone level schema validation settings
                description: >-
                  Retrieves zone level schema validation settings currently set
                  on the zone
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update zone level schema validation settings
                description: Updates zone level schema validation settings on the zone
              put:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Update zone level schema validation settings
                description: Updates zone level schema validation settings on the zone
            /zones/{zone_id}/api_gateway/user_schemas:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve information about all schemas on a zone
              post:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Upload a schema to a zone
            /zones/{zone_id}/api_gateway/user_schemas/{schema_id}:
              delete:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Delete a schema
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve information about a specific schema on a zone
              patch:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Enable validation for a schema
            /zones/{zone_id}/api_gateway/user_schemas/{schema_id}/operations:
              get:
                tags:
                  - API Shield Schema Validation 2.0
                summary: Retrieve all operations from a schema.
                description: >-
                  Retrieves all operations from the schema. Operations that
                  already exist in API Shield Endpoint Management will be
                  returned as full operations.
            /zones/{zone_id}/argo/smart_routing:
              get:
                tags:
                  - Argo Smart Routing
                summary: Get Argo Smart Routing setting
              patch:
                tags:
                  - Argo Smart Routing
                summary: Patch Argo Smart Routing setting
                description: Updates enablement of Argo Smart Routing.
            /zones/{zone_id}/argo/tiered_caching:
              get:
                tags:
                  - Tiered Caching
                summary: Get Tiered Caching setting
              patch:
                tags:
                  - Tiered Caching
                summary: Patch Tiered Caching setting
                description: Updates enablement of Tiered Caching
            /zones/{zone_id}/bot_management:
              get:
                tags:
                  - Bot Settings
                summary: Get Zone Bot Management Config
                description: Retrieve a zone's Bot Management Config
              put:
                tags:
                  - Bot Settings
                summary: Update Zone Bot Management Config
                description: >
                  Updates the Bot Management configuration for a zone.


                  This API is used to update:

                  - **Bot Fight Mode**

                  - **Super Bot Fight Mode**

                  - **Bot Management for Enterprise**


                  See [Bot Plans](https://developers.cloudflare.com/bots/plans/)
                  for more information on the different plans
            /zones/{zone_id}/cache/cache_reserve:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Cache Reserve setting
                description: >-
                  Increase cache lifetimes by automatically storing all
                  cacheable files into Cloudflare's persistent object storage
                  buckets. Requires Cache Reserve subscription. Note: using
                  Tiered Cache with Cache Reserve is highly recommended to
                  reduce Reserve operations costs. See the [developer
                  docs](https://developers.cloudflare.com/cache/about/cache-reserve)
                  for more information.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Cache Reserve setting
                description: >-
                  Increase cache lifetimes by automatically storing all
                  cacheable files into Cloudflare's persistent object storage
                  buckets. Requires Cache Reserve subscription. Note: using
                  Tiered Cache with Cache Reserve is highly recommended to
                  reduce Reserve operations costs. See the [developer
                  docs](https://developers.cloudflare.com/cache/about/cache-reserve)
                  for more information.
            /zones/{zone_id}/cache/cache_reserve_clear:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Cache Reserve Clear
                description: >-
                  You can use Cache Reserve Clear to clear your Cache Reserve,
                  but you must first disable Cache Reserve. In most cases, this
                  will be accomplished within 24 hours. You cannot re-enable
                  Cache Reserve while this process is ongoing. Keep in mind that
                  you cannot undo or cancel this operation.
              post:
                tags:
                  - Zone Cache Settings
                summary: Start Cache Reserve Clear
                description: >-
                  You can use Cache Reserve Clear to clear your Cache Reserve,
                  but you must first disable Cache Reserve. In most cases, this
                  will be accomplished within 24 hours. You cannot re-enable
                  Cache Reserve while this process is ongoing. Keep in mind that
                  you cannot undo or cancel this operation.
            /zones/{zone_id}/cache/origin_post_quantum_encryption:
              get:
                tags:
                  - Origin Post-Quantum
                summary: Get Origin Post-Quantum Encryption setting
                description: >-
                  Instructs Cloudflare to use Post-Quantum (PQ) key agreement
                  algorithms when connecting to your origin. Preferred instructs
                  Cloudflare to opportunistically send a Post-Quantum keyshare
                  in the first message to the origin (for fastest connections
                  when the origin supports and prefers PQ), supported means that
                  PQ algorithms are advertised but only used when requested by
                  the origin, and off means that PQ algorithms are not
                  advertised
              put:
                tags:
                  - Origin Post-Quantum
                summary: Change Origin Post-Quantum Encryption setting
                description: >-
                  Instructs Cloudflare to use Post-Quantum (PQ) key agreement
                  algorithms when connecting to your origin. Preferred instructs
                  Cloudflare to opportunistically send a Post-Quantum keyshare
                  in the first message to the origin (for fastest connections
                  when the origin supports and prefers PQ), supported means that
                  PQ algorithms are advertised but only used when requested by
                  the origin, and off means that PQ algorithms are not
                  advertised
            /zones/{zone_id}/cache/regional_tiered_cache:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Regional Tiered Cache setting
                description: >-
                  Instructs Cloudflare to check a regional hub data center on
                  the way to your upper tier. This can help improve performance
                  for smart and custom tiered cache topologies.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Regional Tiered Cache setting
                description: >-
                  Instructs Cloudflare to check a regional hub data center on
                  the way to your upper tier. This can help improve performance
                  for smart and custom tiered cache topologies.
            /zones/{zone_id}/cache/tiered_cache_smart_topology_enable:
              delete:
                tags:
                  - Smart Tiered Cache
                summary: Delete Smart Tiered Cache setting
                description: Remvoves enablement of Smart Tiered Cache
              get:
                tags:
                  - Smart Tiered Cache
                summary: Get Smart Tiered Cache setting
              patch:
                tags:
                  - Smart Tiered Cache
                summary: Patch Smart Tiered Cache setting
                description: Updates enablement of Tiered Cache
            /zones/{zone_id}/cache/variants:
              delete:
                tags:
                  - Zone Cache Settings
                summary: Delete variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
              get:
                tags:
                  - Zone Cache Settings
                summary: Get variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change variants setting
                description: >-
                  Variant support enables caching variants of images with
                  certain file extensions in addition to the original. This only
                  applies when the origin server sends the 'Vary: Accept'
                  response header. If the origin server sends 'Vary: Accept' but
                  does not serve the variant requested, the response will not be
                  cached. This will be indicated with BYPASS cache status in the
                  response headers.
            /zones/{zone_id}/certificate_authorities/hostname_associations:
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: List Hostname Associations
                description: List Hostname Associations
              put:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Replace Hostname Associations
                description: Replace Hostname Associations
            /zones/{zone_id}/client_certificates:
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: List Client Certificates
                description: >-
                  List all of your Zone's API Shield mTLS Client Certificates by
                  Status and/or using Pagination
              post:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Create Client Certificate
                description: Create a new API Shield mTLS Client Certificate
            /zones/{zone_id}/client_certificates/{client_certificate_id}:
              delete:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Revoke Client Certificate
                description: >-
                  Set a API Shield mTLS Client Certificate to pending_revocation
                  status for processing to revoked status.
              get:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Client Certificate Details
                description: Get Details for a single mTLS API Shield Client Certificate
              patch:
                tags:
                  - API Shield Client Certificates for a Zone
                summary: Reactivate Client Certificate
                description: >-
                  If a API Shield mTLS Client Certificate is in a
                  pending_revocation state, you may reactivate it with this
                  endpoint.
            /zones/{zone_id}/custom_certificates:
              get:
                tags:
                  - Custom SSL for a Zone
                summary: List SSL Configurations
                description: >-
                  List, search, and filter all of your custom SSL certificates.
                  The higher priority will break ties across overlapping
                  'legacy_custom' certificates, but 'legacy_custom' certificates
                  will always supercede 'sni_custom' certificates.
              post:
                tags:
                  - Custom SSL for a Zone
                summary: Create SSL Configuration
                description: Upload a new SSL certificate for a zone.
            /zones/{zone_id}/custom_certificates/{custom_certificate_id}:
              delete:
                tags:
                  - Custom SSL for a Zone
                summary: Delete SSL Configuration
                description: Remove a SSL certificate from a zone.
              get:
                tags:
                  - Custom SSL for a Zone
                summary: SSL Configuration Details
              patch:
                tags:
                  - Custom SSL for a Zone
                summary: Edit SSL Configuration
                description: >-
                  Upload a new private key and/or PEM/CRT for the SSL
                  certificate. Note: PATCHing a configuration for sni_custom
                  certificates will result in a new resource id being returned,
                  and the previous one being deleted.
            /zones/{zone_id}/custom_certificates/prioritize:
              put:
                tags:
                  - Custom SSL for a Zone
                summary: Re-prioritize SSL Certificates
                description: >-
                  If a zone has multiple SSL certificates, you can set the order
                  in which they should be used during a request. The higher
                  priority will break ties across overlapping 'legacy_custom'
                  certificates.
            /zones/{zone_id}/custom_hostnames:
              get:
                tags:
                  - Custom Hostname for a Zone
                summary: List Custom Hostnames
                description: List, search, sort, and filter all of your custom hostnames.
              post:
                tags:
                  - Custom Hostname for a Zone
                summary: Create Custom Hostname
                description: >-
                  Add a new custom hostname and request that an SSL certificate
                  be issued for it. One of three validation methods—http, txt,
                  email—should be used, with 'http' recommended if the CNAME is
                  already in place (or will be soon). Specifying 'email' will
                  send an email to the WHOIS contacts on file for the base
                  domain plus hostmaster, postmaster, webmaster, admin,
                  administrator. If http is used and the domain is not already
                  pointing to the Managed CNAME host, the PATCH method must be
                  used once it is (to complete validation).
            /zones/{zone_id}/custom_hostnames/{custom_hostname_id}:
              delete:
                tags:
                  - Custom Hostname for a Zone
                summary: Delete Custom Hostname (and any issued SSL certificates)
              get:
                tags:
                  - Custom Hostname for a Zone
                summary: Custom Hostname Details
              patch:
                tags:
                  - Custom Hostname for a Zone
                summary: Edit Custom Hostname
                description: >-
                  Modify SSL configuration for a custom hostname. When sent with
                  SSL config that matches existing config, used to indicate that
                  hostname should pass domain control validation (DCV). Can also
                  be used to change validation type, e.g., from 'http' to
                  'email'.
            /zones/{zone_id}/custom_hostnames/fallback_origin:
              delete:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Delete Fallback Origin for Custom Hostnames
              get:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Get Fallback Origin for Custom Hostnames
              put:
                tags:
                  - Custom Hostname Fallback Origin for a Zone
                summary: Update Fallback Origin for Custom Hostnames
            /zones/{zone_id}/custom_ns:
              get:
                tags:
                  - Account-Level Custom Nameservers Usage for a Zone
                summary: Get Account Custom Nameserver Related Zone Metadata
                description: |
                  Get metadata for account-level custom nameservers on a zone.
              put:
                tags:
                  - Account-Level Custom Nameservers Usage for a Zone
                summary: Set Account Custom Nameserver Related Zone Metadata
                description: >
                  Set metadata for account-level custom nameservers on a zone.


                  If you would like new zones in the account to use account
                  custom nameservers by default, use PUT /accounts/:identifier
                  to set the account setting use_account_custom_ns_by_default to
                  true.
            /zones/{zone_id}/dcv_delegation/uuid:
              get:
                tags:
                  - DCV Delegation
                summary: Retrieve the DCV Delegation unique identifier.
                description: >-
                  Retrieve the account and zone specific unique identifier used
                  as part of the CNAME target for DCV Delegation.
            /zones/{zone_id}/dns_records:
              get:
                tags:
                  - DNS Records for a Zone
                summary: List DNS Records
                description: List, search, sort, and filter a zones' DNS records.
              post:
                tags:
                  - DNS Records for a Zone
                summary: Create DNS Record
                description: >
                  Create a new DNS record for a zone.


                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
            /zones/{zone_id}/dns_records/{dns_record_id}:
              delete:
                tags:
                  - DNS Records for a Zone
                summary: Delete DNS Record
              get:
                tags:
                  - DNS Records for a Zone
                summary: DNS Record Details
              patch:
                tags:
                  - DNS Records for a Zone
                summary: Update DNS Record
                description: >
                  Update an existing DNS record.

                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
              put:
                tags:
                  - DNS Records for a Zone
                summary: Overwrite DNS Record
                description: >
                  Overwrite an existing DNS record.

                  Notes:

                  - A/AAAA records cannot exist on the same name as CNAME
                  records.

                  - NS records cannot exist on the same name as any other record
                  type.

                  - Domain names are always represented in Punycode, even if
                  Unicode
                    characters were used when creating the record.
            /zones/{zone_id}/dns_records/export:
              get:
                tags:
                  - DNS Records for a Zone
                summary: Export DNS Records
                description: >-
                  You can export your [BIND
                  config](https://en.wikipedia.org/wiki/Zone_file "Zone file")
                  through this endpoint.


                  See [the
                  documentation](https://developers.cloudflare.com/dns/manage-dns-records/how-to/import-and-export/
                  "Import and export records") for more information.
            /zones/{zone_id}/dns_records/import:
              post:
                tags:
                  - DNS Records for a Zone
                summary: Import DNS Records
                description: >-
                  You can upload your [BIND
                  config](https://en.wikipedia.org/wiki/Zone_file "Zone file")
                  through this endpoint. It assumes that cURL is called from a
                  location with bind_config.txt (valid BIND config) present.


                  See [the
                  documentation](https://developers.cloudflare.com/dns/manage-dns-records/how-to/import-and-export/
                  "Import and export records") for more information.
            /zones/{zone_id}/dns_records/scan:
              post:
                tags:
                  - DNS Records for a Zone
                summary: Scan DNS Records
                description: >-
                  Scan for common DNS records on your domain and automatically
                  add them to your zone. Useful if you haven't updated your
                  nameservers yet.
            /zones/{zone_id}/dnssec:
              delete:
                tags:
                  - DNSSEC
                summary: Delete DNSSEC records
                description: Delete DNSSEC.
              get:
                tags:
                  - DNSSEC
                summary: DNSSEC Details
                description: Details about DNSSEC status and configuration.
              patch:
                tags:
                  - DNSSEC
                summary: Edit DNSSEC Status
                description: Enable or disable DNSSEC.
            /zones/{zone_id}/firewall/access_rules/rules:
              get:
                tags:
                  - IP Access rules for a zone
                summary: List IP Access rules
                description: >-
                  Fetches IP Access rules of a zone. You can filter the results
                  using several optional parameters.
              post:
                tags:
                  - IP Access rules for a zone
                summary: Create an IP Access rule
                description: >-
                  Creates a new IP Access rule for a zone.


                  Note: To create an IP Access rule that applies to multiple
                  zones, refer to [IP Access rules for a
                  user](#ip-access-rules-for-a-user) or [IP Access rules for an
                  account](#ip-access-rules-for-an-account) as appropriate.
            /zones/{zone_id}/firewall/access_rules/rules/{identifier}:
              delete:
                tags:
                  - IP Access rules for a zone
                summary: Delete an IP Access rule
                description: >-
                  Deletes an IP Access rule defined at the zone level.


                  Optionally, you can use the `cascade` property to specify that
                  you wish to delete similar rules in other zones managed by the
                  same zone owner.
              patch:
                tags:
                  - IP Access rules for a zone
                summary: Update an IP Access rule
                description: >-
                  Updates an IP Access rule defined at the zone level. You can
                  only update the rule action (`mode` parameter) and notes.
            /zones/{zone_id}/firewall/waf/packages/{package_id}/groups:
              get:
                tags:
                  - WAF rule groups
                summary: List WAF rule groups
                description: >-
                  Fetches the WAF rule groups in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/groups/{group_id}:
              get:
                tags:
                  - WAF rule groups
                summary: Get a WAF rule group
                description: >-
                  Fetches the details of a WAF rule group.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF rule groups
                summary: Update a WAF rule group
                description: >-
                  Updates a WAF rule group. You can update the state (`mode`
                  parameter) of a rule group.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/rules:
              get:
                tags:
                  - WAF rules
                summary: List WAF rules
                description: >-
                  Fetches WAF rules in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/firewall/waf/packages/{package_id}/rules/{rule_id}:
              get:
                tags:
                  - WAF rules
                summary: Get a WAF rule
                description: >-
                  Fetches the details of a WAF rule in a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF rules
                summary: Update a WAF rule
                description: >-
                  Updates a WAF rule. You can only update the mode/action of the
                  rule.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_id}/hold:
              delete:
                tags:
                  - Zone Holds
                summary: Remove Zone Hold
                description: >-
                  Stop enforcement of a zone hold on the zone, permanently or
                  temporarily, allowing the

                  creation and activation of zones with this zone's hostname.
              get:
                tags:
                  - Zone Holds
                summary: Get Zone Hold
                description: >-
                  Retrieve whether the zone is subject to a zone hold, and
                  metadata about the hold.
              post:
                tags:
                  - Zone Holds
                summary: Create Zone Hold
                description: >-
                  Enforce a zone hold on the zone, blocking the creation and
                  activation of zones with this zone's hostname.
            /zones/{zone_id}/hostnames/settings/{setting_id}:
              get:
                tags:
                  - Per-Hostname TLS Settings
                summary: List TLS setting for hostnames
                description: >-
                  List the requested TLS setting for the hostnames under this
                  zone.
            /zones/{zone_id}/hostnames/settings/{setting_id}/{hostname}:
              delete:
                tags:
                  - Per-Hostname TLS Settings
                summary: Delete TLS setting for hostname
                description: Delete the tls setting value for the hostname.
              put:
                tags:
                  - Per-Hostname TLS Settings
                summary: Edit TLS setting for hostname
                description: Update the tls setting value for the hostname.
            /zones/{zone_id}/keyless_certificates:
              get:
                tags:
                  - Keyless SSL for a Zone
                summary: List Keyless SSL Configurations
                description: List all Keyless SSL configurations for a given zone.
              post:
                tags:
                  - Keyless SSL for a Zone
                summary: Create Keyless SSL Configuration
            /zones/{zone_id}/keyless_certificates/{keyless_certificate_id}:
              delete:
                tags:
                  - Keyless SSL for a Zone
                summary: Delete Keyless SSL Configuration
              get:
                tags:
                  - Keyless SSL for a Zone
                summary: Get Keyless SSL Configuration
                description: Get details for one Keyless SSL configuration.
              patch:
                tags:
                  - Keyless SSL for a Zone
                summary: Edit Keyless SSL Configuration
                description: >-
                  This will update attributes of a Keyless SSL. Consists of one
                  or more of the following:  host,name,port.
            /zones/{zone_id}/load_balancers:
              get:
                tags:
                  - Load Balancers
                summary: List Load Balancers
                description: List configured load balancers.
              post:
                tags:
                  - Load Balancers
                summary: Create Load Balancer
                description: Create a new load balancer.
            /zones/{zone_id}/load_balancers/{load_balancer_id}:
              delete:
                tags:
                  - Load Balancers
                summary: Delete Load Balancer
                description: Delete a configured load balancer.
              get:
                tags:
                  - Load Balancers
                summary: Load Balancer Details
                description: Fetch a single configured load balancer.
              patch:
                tags:
                  - Load Balancers
                summary: Patch Load Balancer
                description: >-
                  Apply changes to an existing load balancer, overwriting the
                  supplied properties.
              put:
                tags:
                  - Load Balancers
                summary: Update Load Balancer
                description: Update a configured load balancer.
            /zones/{zone_id}/logpush/datasets/{dataset_id}/fields:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List fields
                description: >-
                  Lists all fields available for a dataset. The response result
                  is an object with key-value pairs, where keys are field names,
                  and values are descriptions.
            /zones/{zone_id}/logpush/datasets/{dataset_id}/jobs:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List Logpush jobs for a dataset
                description: Lists Logpush jobs for a zone for a dataset.
            /zones/{zone_id}/logpush/edge:
              get:
                tags:
                  - Instant Logs jobs for a zone
                summary: List Instant Logs jobs
                description: Lists Instant Logs jobs for a zone.
              post:
                tags:
                  - Instant Logs jobs for a zone
                summary: Create Instant Logs job
                description: Creates a new Instant Logs job for a zone.
            /zones/{zone_id}/logpush/jobs:
              get:
                tags:
                  - Logpush jobs for a zone
                summary: List Logpush jobs
                description: Lists Logpush jobs for a zone.
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Create Logpush job
                description: Creates a new Logpush job for a zone.
            /zones/{zone_id}/logpush/jobs/{job_id}:
              delete:
                tags:
                  - Logpush jobs for a zone
                summary: Delete Logpush job
                description: Deletes a Logpush job.
              get:
                tags:
                  - Logpush jobs for a zone
                summary: Get Logpush job details
                description: Gets the details of a Logpush job.
              put:
                tags:
                  - Logpush jobs for a zone
                summary: Update Logpush job
                description: Updates a Logpush job.
            /zones/{zone_id}/logpush/ownership:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Get ownership challenge
                description: Gets a new ownership challenge sent to your destination.
            /zones/{zone_id}/logpush/ownership/validate:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Validate ownership challenge
                description: Validates ownership challenge of the destination.
            /zones/{zone_id}/logpush/validate/destination/exists:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Check destination exists
                description: Checks if there is an existing job with a destination.
            /zones/{zone_id}/logpush/validate/origin:
              post:
                tags:
                  - Logpush jobs for a zone
                summary: Validate origin
                description: Validates logpull origin with logpull_options.
            /zones/{zone_id}/managed_headers:
              get:
                tags:
                  - Managed Transforms
                summary: List Managed Transforms
                description: Fetches a list of all Managed Transforms.
              patch:
                tags:
                  - Managed Transforms
                summary: Update status of Managed Transforms
                description: Updates the status of one or more Managed Transforms.
            /zones/{zone_id}/origin_tls_client_auth:
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: List Certificates
              post:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Upload Certificate
                description: >-
                  Upload your own certificate you want Cloudflare to use for
                  edge-to-origin communication to override the shared
                  certificate. Please note that it is important to keep only one
                  certificate active. Also, make sure to enable zone-level
                  authenticated origin pulls by making a PUT call to settings
                  endpoint to see the uploaded certificate in use.
            /zones/{zone_id}/origin_tls_client_auth/{certificate_id}:
              delete:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Delete Certificate
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Get Certificate Details
            /zones/{zone_id}/origin_tls_client_auth/hostnames:
              put:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Enable or Disable a Hostname for Client Authentication
                description: >-
                  Associate a hostname to a certificate and enable, disable or
                  invalidate the association. If disabled, client certificate
                  will not be sent to the hostname even if activated at the zone
                  level. 100 maximum associations on a single certificate are
                  allowed. Note: Use a null value for parameter *enabled* to
                  invalidate the association.
            /zones/{zone_id}/origin_tls_client_auth/hostnames/{hostname}:
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Get the Hostname Status for Client Authentication
            /zones/{zone_id}/origin_tls_client_auth/hostnames/certificates:
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: List Certificates
              post:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Upload a Hostname Client Certificate
                description: >-
                  Upload a certificate to be used for client authentication on a
                  hostname. 10 hostname certificates per zone are allowed.
            /zones/{zone_id}/origin_tls_client_auth/hostnames/certificates/{certificate_id}:
              delete:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Delete Hostname Client Certificate
              get:
                tags:
                  - Per-hostname Authenticated Origin Pull
                summary: Get the Hostname Client Certificate
                description: >-
                  Get the certificate by ID to be used for client authentication
                  on a hostname.
            /zones/{zone_id}/origin_tls_client_auth/settings:
              get:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Get Enablement Setting for Zone
                description: >-
                  Get whether zone-level authenticated origin pulls is enabled
                  or not. It is false by default.
              put:
                tags:
                  - Zone-Level Authenticated Origin Pulls
                summary: Set Enablement for Zone
                description: >-
                  Enable or disable zone-level authenticated origin pulls.
                  'enabled' should be set true either before/after the
                  certificate is uploaded to see the certificate in use.
            /zones/{zone_id}/page_shield:
              get:
                tags:
                  - Page Shield
                summary: Get Page Shield settings
                description: Fetches the Page Shield settings.
              put:
                tags:
                  - Page Shield
                summary: Update Page Shield settings
                description: Updates Page Shield settings.
            /zones/{zone_id}/page_shield/connections:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield connections
                description: Lists all connections detected by Page Shield.
            /zones/{zone_id}/page_shield/connections/{connection_id}:
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield connection
                description: Fetches a connection detected by Page Shield by connection ID.
            /zones/{zone_id}/page_shield/policies:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield policies
                description: Lists all Page Shield policies.
              post:
                tags:
                  - Page Shield
                summary: Create a Page Shield policy
                description: Create a Page Shield policy.
            /zones/{zone_id}/page_shield/policies/{policy_id}:
              delete:
                tags:
                  - Page Shield
                summary: Delete a Page Shield policy
                description: Delete a Page Shield policy by ID.
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield policy
                description: Fetches a Page Shield policy by ID.
              put:
                tags:
                  - Page Shield
                summary: Update a Page Shield policy
                description: Update a Page Shield policy by ID.
            /zones/{zone_id}/page_shield/scripts:
              get:
                tags:
                  - Page Shield
                summary: List Page Shield scripts
                description: Lists all scripts detected by Page Shield.
            /zones/{zone_id}/page_shield/scripts/{script_id}:
              get:
                tags:
                  - Page Shield
                summary: Get a Page Shield script
                description: Fetches a script detected by Page Shield by script ID.
            /zones/{zone_id}/pagerules:
              get:
                tags:
                  - Page Rules
                summary: List Page Rules
                description: Fetches Page Rules in a zone.
              post:
                tags:
                  - Page Rules
                summary: Create a Page Rule
                description: Creates a new Page Rule.
            /zones/{zone_id}/pagerules/{pagerule_id}:
              delete:
                tags:
                  - Page Rules
                summary: Delete a Page Rule
                description: Deletes an existing Page Rule.
              get:
                tags:
                  - Page Rules
                summary: Get a Page Rule
                description: Fetches the details of a Page Rule.
              patch:
                tags:
                  - Page Rules
                summary: Edit a Page Rule
                description: Updates one or more fields of an existing Page Rule.
              put:
                tags:
                  - Page Rules
                summary: Update a Page Rule
                description: >-
                  Replaces the configuration of an existing Page Rule. The
                  configuration of the updated Page Rule will exactly match the
                  data passed in the API request.
            /zones/{zone_id}/pagerules/settings:
              get:
                tags:
                  - Available Page Rules settings
                summary: List available Page Rules settings
                description: >-
                  Returns a list of settings (and their details) that Page Rules
                  can apply to matching requests.
            /zones/{zone_id}/purge_cache:
              post:
                tags:
                  - Zone
                summary: Purge Cached Content
                description: >
                  ### Purge All Cached Content

                  Removes ALL files from Cloudflare's cache. All tiers can purge
                  everything.


                  ### Purge Cached Content by URL

                  Granularly removes one or more files from Cloudflare's cache
                  by specifying URLs. All tiers can purge by URL.


                  To purge files with custom cache keys, include the headers
                  used to compute the cache key as in the example. If you have a
                  device type or geo in your cache key, you will need to include
                  the CF-Device-Type or CF-IPCountry headers. If you have lang
                  in your cache key, you will need to include the
                  Accept-Language header.


                  **NB:** When including the Origin header, be sure to include
                  the **scheme** and **hostname**. The port number can be
                  omitted if it is the default port (80 for http, 443 for
                  https), but must be included otherwise.


                  ### Purge Cached Content by Tag, Host or Prefix

                  Granularly removes one or more files from Cloudflare's cache
                  either by specifying the host, the associated Cache-Tag, or a
                  Prefix. Only Enterprise customers are permitted to purge by
                  Tag, Host or Prefix.


                  **NB:** Cache-Tag, host, and prefix purging each have a rate
                  limit of 30,000 purge API calls in every 24 hour period. You
                  may purge up to 30 tags, hosts, or prefixes in one API call.
                  This rate limit can be raised for customers who need to purge
                  at higher volume.
            /zones/{zone_id}/rulesets:
              get:
                tags:
                  - Zone Rulesets
                summary: List zone rulesets
                description: Fetches all rulesets at the zone level.
              post:
                tags:
                  - Zone Rulesets
                summary: Create a zone ruleset
                description: Creates a ruleset at the zone level.
            /zones/{zone_id}/rulesets/{ruleset_id}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset
                description: Deletes all versions of an existing zone ruleset.
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone ruleset
                description: Fetches the latest version of a zone ruleset.
              put:
                tags:
                  - Zone Rulesets
                summary: Update a zone ruleset
                description: Updates a zone ruleset, creating a new version.
            /zones/{zone_id}/rulesets/{ruleset_id}/rules:
              post:
                tags:
                  - Zone Rulesets
                summary: Create a zone ruleset rule
                description: >-
                  Adds a new rule to a zone ruleset. The rule will be added to
                  the end of the existing list of rules in the ruleset by
                  default.
            /zones/{zone_id}/rulesets/{ruleset_id}/rules/{rule_id}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset rule
                description: Deletes an existing rule from a zone ruleset.
              patch:
                tags:
                  - Zone Rulesets
                summary: Update a zone ruleset rule
                description: Updates an existing rule in a zone ruleset.
            /zones/{zone_id}/rulesets/{ruleset_id}/versions:
              get:
                tags:
                  - Zone Rulesets
                summary: List a zone ruleset's versions
                description: Fetches the versions of a zone ruleset.
            /zones/{zone_id}/rulesets/{ruleset_id}/versions/{ruleset_version}:
              delete:
                tags:
                  - Zone Rulesets
                summary: Delete a zone ruleset version
                description: Deletes an existing version of a zone ruleset.
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone ruleset version
                description: Fetches a specific version of a zone ruleset.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint:
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone entry point ruleset
                description: >-
                  Fetches the latest version of the zone entry point ruleset for
                  a given phase.
              put:
                tags:
                  - Zone Rulesets
                summary: Update a zone entry point ruleset
                description: Updates a zone entry point ruleset, creating a new version.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions:
              get:
                tags:
                  - Zone Rulesets
                summary: List a zone entry point ruleset's versions
                description: Fetches the versions of a zone entry point ruleset.
            /zones/{zone_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions/{ruleset_version}:
              get:
                tags:
                  - Zone Rulesets
                summary: Get a zone entry point ruleset version
                description: Fetches a specific version of a zone entry point ruleset.
            /zones/{zone_id}/secondary_dns/force_axfr:
              post:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Force AXFR
                description: Sends AXFR zone transfer request to primary nameserver(s).
            /zones/{zone_id}/secondary_dns/incoming:
              delete:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Delete Secondary Zone Configuration
                description: >-
                  Delete secondary zone configuration for incoming zone
                  transfers.
              get:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Secondary Zone Configuration Details
                description: Get secondary zone configuration for incoming zone transfers.
              post:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Create Secondary Zone Configuration
                description: >-
                  Create secondary zone configuration for incoming zone
                  transfers.
              put:
                tags:
                  - Secondary DNS (Secondary Zone)
                summary: Update Secondary Zone Configuration
                description: >-
                  Update secondary zone configuration for incoming zone
                  transfers.
            /zones/{zone_id}/secondary_dns/outgoing:
              delete:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Delete Primary Zone Configuration
                description: Delete primary zone configuration for outgoing zone transfers.
              get:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Primary Zone Configuration Details
                description: Get primary zone configuration for outgoing zone transfers.
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Create Primary Zone Configuration
                description: Create primary zone configuration for outgoing zone transfers.
              put:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Update Primary Zone Configuration
                description: Update primary zone configuration for outgoing zone transfers.
            /zones/{zone_id}/secondary_dns/outgoing/disable:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Disable Outgoing Zone Transfers
                description: >-
                  Disable outgoing zone transfers for primary zone and clears
                  IXFR backlog of primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/enable:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Enable Outgoing Zone Transfers
                description: Enable outgoing zone transfers for primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/force_notify:
              post:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Force DNS NOTIFY
                description: >-
                  Notifies the secondary nameserver(s) and clears IXFR backlog
                  of primary zone.
            /zones/{zone_id}/secondary_dns/outgoing/status:
              get:
                tags:
                  - Secondary DNS (Primary Zone)
                summary: Get Outgoing Zone Transfer Status
                description: Get primary zone transfer status.
            /zones/{zone_id}/settings:
              get:
                tags:
                  - Zone Settings
                summary: Get all Zone settings
                description: Available settings for your user in relation to a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Edit zone settings info
                description: Edit settings for a zone.
            /zones/{zone_id}/settings/0rtt:
              get:
                tags:
                  - Zone Settings
                summary: Get 0-RTT session resumption setting
                description: Gets 0-RTT session resumption setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change 0-RTT session resumption setting
                description: Changes the 0-RTT session resumption setting.
            /zones/{zone_id}/settings/advanced_ddos:
              get:
                tags:
                  - Zone Settings
                summary: Get Advanced DDOS setting
                description: >-
                  Advanced protection from Distributed Denial of Service (DDoS)
                  attacks on your website. This is an uneditable value that is
                  'on' in the case of Business and Enterprise zones.
            /zones/{zone_id}/settings/always_online:
              get:
                tags:
                  - Zone Settings
                summary: Get Always Online setting
                description: >-
                  When enabled, Cloudflare serves limited copies of web pages
                  available from the [Internet Archive's Wayback
                  Machine](https://archive.org/web/) if your server is offline.
                  Refer to [Always
                  Online](https://developers.cloudflare.com/cache/about/always-online)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Always Online setting
                description: >-
                  When enabled, Cloudflare serves limited copies of web pages
                  available from the [Internet Archive's Wayback
                  Machine](https://archive.org/web/) if your server is offline.
                  Refer to [Always
                  Online](https://developers.cloudflare.com/cache/about/always-online)
                  for more information.
            /zones/{zone_id}/settings/always_use_https:
              get:
                tags:
                  - Zone Settings
                summary: Get Always Use HTTPS setting
                description: >-
                  Reply to all requests for URLs that use "http" with a 301
                  redirect to the equivalent "https" URL. If you only want to
                  redirect for a subset of requests, consider creating an
                  "Always use HTTPS" page rule.
              patch:
                tags:
                  - Zone Settings
                summary: Change Always Use HTTPS setting
                description: >-
                  Reply to all requests for URLs that use "http" with a 301
                  redirect to the equivalent "https" URL. If you only want to
                  redirect for a subset of requests, consider creating an
                  "Always use HTTPS" page rule.
            /zones/{zone_id}/settings/automatic_https_rewrites:
              get:
                tags:
                  - Zone Settings
                summary: Get Automatic HTTPS Rewrites setting
                description: Enable the Automatic HTTPS Rewrites feature for this zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change Automatic HTTPS Rewrites setting
                description: Enable the Automatic HTTPS Rewrites feature for this zone.
            /zones/{zone_id}/settings/automatic_platform_optimization:
              get:
                tags:
                  - Zone Settings
                summary: Get Automatic Platform Optimization for WordPress setting
                description: >
                  [Automatic Platform Optimization for
                  WordPress](https://developers.cloudflare.com/automatic-platform-optimization/)

                  serves your WordPress site from Cloudflare's edge network and
                  caches

                  third-party fonts.
              patch:
                tags:
                  - Zone Settings
                summary: Change Automatic Platform Optimization for WordPress setting
                description: >
                  [Automatic Platform Optimization for
                  WordPress](https://developers.cloudflare.com/automatic-platform-optimization/)

                  serves your WordPress site from Cloudflare's edge network and
                  caches

                  third-party fonts.
            /zones/{zone_id}/settings/brotli:
              get:
                tags:
                  - Zone Settings
                summary: Get Brotli setting
                description: >-
                  When the client requesting an asset supports the Brotli
                  compression algorithm, Cloudflare will serve a Brotli
                  compressed version of the asset.
              patch:
                tags:
                  - Zone Settings
                summary: Change Brotli setting
                description: >-
                  When the client requesting an asset supports the Brotli
                  compression algorithm, Cloudflare will serve a Brotli
                  compressed version of the asset.
            /zones/{zone_id}/settings/browser_cache_ttl:
              get:
                tags:
                  - Zone Settings
                summary: Get Browser Cache TTL setting
                description: >-
                  Browser Cache TTL (in seconds) specifies how long
                  Cloudflare-cached resources will remain on your visitors'
                  computers. Cloudflare will honor any larger times specified by
                  your server.
                  (https://support.cloudflare.com/hc/en-us/articles/200168276).
              patch:
                tags:
                  - Zone Settings
                summary: Change Browser Cache TTL setting
                description: >-
                  Browser Cache TTL (in seconds) specifies how long
                  Cloudflare-cached resources will remain on your visitors'
                  computers. Cloudflare will honor any larger times specified by
                  your server.
                  (https://support.cloudflare.com/hc/en-us/articles/200168276).
            /zones/{zone_id}/settings/browser_check:
              get:
                tags:
                  - Zone Settings
                summary: Get Browser Check setting
                description: >-
                  Browser Integrity Check is similar to Bad Behavior and looks
                  for common HTTP headers abused most commonly by spammers and
                  denies access to your page.  It will also challenge visitors
                  that do not have a user agent or a non standard user agent
                  (also commonly used by abuse bots, crawlers or visitors).
                  (https://support.cloudflare.com/hc/en-us/articles/200170086).
              patch:
                tags:
                  - Zone Settings
                summary: Change Browser Check setting
                description: >-
                  Browser Integrity Check is similar to Bad Behavior and looks
                  for common HTTP headers abused most commonly by spammers and
                  denies access to your page.  It will also challenge visitors
                  that do not have a user agent or a non standard user agent
                  (also commonly used by abuse bots, crawlers or visitors).
                  (https://support.cloudflare.com/hc/en-us/articles/200170086).
            /zones/{zone_id}/settings/cache_level:
              get:
                tags:
                  - Zone Settings
                summary: Get Cache Level setting
                description: >-
                  Cache Level functions based off the setting level. The basic
                  setting will cache most static resources (i.e., css, images,
                  and JavaScript). The simplified setting will ignore the query
                  string when delivering a cached resource. The aggressive
                  setting will cache all static resources, including ones with a
                  query string.
                  (https://support.cloudflare.com/hc/en-us/articles/200168256).
              patch:
                tags:
                  - Zone Settings
                summary: Change Cache Level setting
                description: >-
                  Cache Level functions based off the setting level. The basic
                  setting will cache most static resources (i.e., css, images,
                  and JavaScript). The simplified setting will ignore the query
                  string when delivering a cached resource. The aggressive
                  setting will cache all static resources, including ones with a
                  query string.
                  (https://support.cloudflare.com/hc/en-us/articles/200168256).
            /zones/{zone_id}/settings/challenge_ttl:
              get:
                tags:
                  - Zone Settings
                summary: Get Challenge TTL setting
                description: >-
                  Specify how long a visitor is allowed access to your site
                  after successfully completing a challenge (such as a CAPTCHA).
                  After the TTL has expired the visitor will have to complete a
                  new challenge. We recommend a 15 - 45 minute setting and will
                  attempt to honor any setting above 45 minutes.
                  (https://support.cloudflare.com/hc/en-us/articles/200170136).
              patch:
                tags:
                  - Zone Settings
                summary: Change Challenge TTL setting
                description: >-
                  Specify how long a visitor is allowed access to your site
                  after successfully completing a challenge (such as a CAPTCHA).
                  After the TTL has expired the visitor will have to complete a
                  new challenge. We recommend a 15 - 45 minute setting and will
                  attempt to honor any setting above 45 minutes.
                  (https://support.cloudflare.com/hc/en-us/articles/200170136).
            /zones/{zone_id}/settings/ciphers:
              get:
                tags:
                  - Zone Settings
                summary: Get ciphers setting
                description: Gets ciphers setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change ciphers setting
                description: Changes ciphers setting.
            /zones/{zone_id}/settings/development_mode:
              get:
                tags:
                  - Zone Settings
                summary: Get Development Mode setting
                description: >-
                  Development Mode temporarily allows you to enter development
                  mode for your websites if you need to make changes to your
                  site. This will bypass Cloudflare's accelerated cache and slow
                  down your site, but is useful if you are making changes to
                  cacheable content (like images, css, or JavaScript) and would
                  like to see those changes right away. Once entered,
                  development mode will last for 3 hours and then automatically
                  toggle off.
              patch:
                tags:
                  - Zone Settings
                summary: Change Development Mode setting
                description: >-
                  Development Mode temporarily allows you to enter development
                  mode for your websites if you need to make changes to your
                  site. This will bypass Cloudflare's accelerated cache and slow
                  down your site, but is useful if you are making changes to
                  cacheable content (like images, css, or JavaScript) and would
                  like to see those changes right away. Once entered,
                  development mode will last for 3 hours and then automatically
                  toggle off.
            /zones/{zone_id}/settings/early_hints:
              get:
                tags:
                  - Zone Settings
                summary: Get Early Hints setting
                description: >-
                  When enabled, Cloudflare will attempt to speed up overall page
                  loads by serving `103` responses with `Link` headers from the
                  final response. Refer to [Early
                  Hints](https://developers.cloudflare.com/cache/about/early-hints)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Early Hints setting
                description: >-
                  When enabled, Cloudflare will attempt to speed up overall page
                  loads by serving `103` responses with `Link` headers from the
                  final response. Refer to [Early
                  Hints](https://developers.cloudflare.com/cache/about/early-hints)
                  for more information.
            /zones/{zone_id}/settings/email_obfuscation:
              get:
                tags:
                  - Zone Settings
                summary: Get Email Obfuscation setting
                description: >-
                  Encrypt email adresses on your web page from bots, while
                  keeping them visible to humans.
                  (https://support.cloudflare.com/hc/en-us/articles/200170016).
              patch:
                tags:
                  - Zone Settings
                summary: Change Email Obfuscation setting
                description: >-
                  Encrypt email adresses on your web page from bots, while
                  keeping them visible to humans.
                  (https://support.cloudflare.com/hc/en-us/articles/200170016).
            /zones/{zone_id}/settings/fonts:
              get:
                tags:
                  - Zone Settings
                summary: Get Cloudflare Fonts setting
                description: >
                  Enhance your website's font delivery with Cloudflare Fonts.
                  Deliver Google Hosted fonts from your own domain,

                  boost performance, and enhance user privacy. Refer to the
                  Cloudflare Fonts documentation for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Cloudflare Fonts setting
                description: >
                  Enhance your website's font delivery with Cloudflare Fonts.
                  Deliver Google Hosted fonts from your own domain,

                  boost performance, and enhance user privacy. Refer to the
                  Cloudflare Fonts documentation for more information.
            /zones/{zone_id}/settings/h2_prioritization:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP/2 Edge Prioritization setting
                description: |
                  Gets HTTP/2 Edge Prioritization setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP/2 Edge Prioritization setting
                description: |
                  Gets HTTP/2 Edge Prioritization setting.
            /zones/{zone_id}/settings/hotlink_protection:
              get:
                tags:
                  - Zone Settings
                summary: Get Hotlink Protection setting
                description: >-
                  When enabled, the Hotlink Protection option ensures that other
                  sites cannot suck up your bandwidth by building pages that use
                  images hosted on your site. Anytime a request for an image on
                  your site hits Cloudflare, we check to ensure that it's not
                  another site requesting them. People will still be able to
                  download and view images from your page, but other sites won't
                  be able to steal them for use on their own pages.
                  (https://support.cloudflare.com/hc/en-us/articles/200170026).
              patch:
                tags:
                  - Zone Settings
                summary: Change Hotlink Protection setting
                description: >-
                  When enabled, the Hotlink Protection option ensures that other
                  sites cannot suck up your bandwidth by building pages that use
                  images hosted on your site. Anytime a request for an image on
                  your site hits Cloudflare, we check to ensure that it's not
                  another site requesting them. People will still be able to
                  download and view images from your page, but other sites won't
                  be able to steal them for use on their own pages.
                  (https://support.cloudflare.com/hc/en-us/articles/200170026).
            /zones/{zone_id}/settings/http2:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP2 setting
                description: Value of the HTTP2 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP2 setting
                description: Value of the HTTP2 setting.
            /zones/{zone_id}/settings/http3:
              get:
                tags:
                  - Zone Settings
                summary: Get HTTP3 setting
                description: Value of the HTTP3 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change HTTP3 setting
                description: Value of the HTTP3 setting.
            /zones/{zone_id}/settings/image_resizing:
              get:
                tags:
                  - Zone Settings
                summary: Get Image Resizing setting
                description: >
                  Image Resizing provides on-demand resizing, conversion and
                  optimisation

                  for images served through Cloudflare's network. Refer to the

                  [Image Resizing
                  documentation](https://developers.cloudflare.com/images/)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Image Resizing setting
                description: >
                  Image Resizing provides on-demand resizing, conversion and
                  optimisation

                  for images served through Cloudflare's network. Refer to the

                  [Image Resizing
                  documentation](https://developers.cloudflare.com/images/)

                  for more information.
            /zones/{zone_id}/settings/ip_geolocation:
              get:
                tags:
                  - Zone Settings
                summary: Get IP Geolocation setting
                description: >-
                  Enable IP Geolocation to have Cloudflare geolocate visitors to
                  your website and pass the country code to you.
                  (https://support.cloudflare.com/hc/en-us/articles/200168236).
              patch:
                tags:
                  - Zone Settings
                summary: Change IP Geolocation setting
                description: >-
                  Enable IP Geolocation to have Cloudflare geolocate visitors to
                  your website and pass the country code to you.
                  (https://support.cloudflare.com/hc/en-us/articles/200168236).
            /zones/{zone_id}/settings/ipv6:
              get:
                tags:
                  - Zone Settings
                summary: Get IPv6 setting
                description: >-
                  Enable IPv6 on all subdomains that are Cloudflare enabled. 
                  (https://support.cloudflare.com/hc/en-us/articles/200168586).
              patch:
                tags:
                  - Zone Settings
                summary: Change IPv6 setting
                description: >-
                  Enable IPv6 on all subdomains that are Cloudflare enabled. 
                  (https://support.cloudflare.com/hc/en-us/articles/200168586).
            /zones/{zone_id}/settings/min_tls_version:
              get:
                tags:
                  - Zone Settings
                summary: Get Minimum TLS Version setting
                description: Gets Minimum TLS Version setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Minimum TLS Version setting
                description: Changes Minimum TLS Version setting.
            /zones/{zone_id}/settings/minify:
              get:
                tags:
                  - Zone Settings
                summary: Get Minify setting
                description: >-
                  Automatically minify certain assets for your website. Refer to
                  [Using Cloudflare Auto
                  Minify](https://support.cloudflare.com/hc/en-us/articles/200168196)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Minify setting
                description: >-
                  Automatically minify certain assets for your website. Refer to
                  [Using Cloudflare Auto
                  Minify](https://support.cloudflare.com/hc/en-us/articles/200168196)
                  for more information.
            /zones/{zone_id}/settings/mirage:
              get:
                tags:
                  - Zone Settings
                summary: Get Mirage setting
                description: >
                  Automatically optimize image loading for website visitors on
                  mobile

                  devices. Refer to our [blog
                  post](http://blog.cloudflare.com/mirage2-solving-mobile-speed)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Mirage setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/mirage2-solving-mobile-speed)
                  for more information.
            /zones/{zone_id}/settings/mobile_redirect:
              get:
                tags:
                  - Zone Settings
                summary: Get Mobile Redirect setting
                description: >-
                  Automatically redirect visitors on mobile devices to a
                  mobile-optimized subdomain. Refer to [Understanding Cloudflare
                  Mobile
                  Redirect](https://support.cloudflare.com/hc/articles/200168336)
                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Mobile Redirect setting
                description: >-
                  Automatically redirect visitors on mobile devices to a
                  mobile-optimized subdomain. Refer to [Understanding Cloudflare
                  Mobile
                  Redirect](https://support.cloudflare.com/hc/articles/200168336)
                  for more information.
            /zones/{zone_id}/settings/nel:
              get:
                tags:
                  - Zone Settings
                summary: Get Network Error Logging setting
                description: |
                  Enable Network Error Logging reporting on your zone. (Beta)
              patch:
                tags:
                  - Zone Settings
                summary: Change Network Error Logging setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/nel-solving-mobile-speed) for
                  more information.
            /zones/{zone_id}/settings/opportunistic_encryption:
              get:
                tags:
                  - Zone Settings
                summary: Get Opportunistic Encryption setting
                description: Gets Opportunistic Encryption setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Opportunistic Encryption setting
                description: Changes Opportunistic Encryption setting.
            /zones/{zone_id}/settings/opportunistic_onion:
              get:
                tags:
                  - Zone Settings
                summary: Get Opportunistic Onion setting
                description: >-
                  Add an Alt-Svc header to all legitimate requests from Tor,
                  allowing the connection to use our onion services instead of
                  exit nodes.
              patch:
                tags:
                  - Zone Settings
                summary: Change Opportunistic Onion setting
                description: >-
                  Add an Alt-Svc header to all legitimate requests from Tor,
                  allowing the connection to use our onion services instead of
                  exit nodes.
            /zones/{zone_id}/settings/orange_to_orange:
              get:
                tags:
                  - Zone Settings
                summary: Get Orange to Orange (O2O) setting
                description: >
                  Orange to Orange (O2O) allows zones on Cloudflare to CNAME to
                  other

                  zones also on Cloudflare.
              patch:
                tags:
                  - Zone Settings
                summary: Change Orange to Orange (O2O) setting
                description: >
                  Orange to Orange (O2O) allows zones on Cloudflare to CNAME to
                  other

                  zones also on Cloudflare.
            /zones/{zone_id}/settings/origin_error_page_pass_thru:
              get:
                tags:
                  - Zone Settings
                summary: Get Enable Error Pages On setting
                description: >-
                  Cloudflare will proxy customer error pages on any 502,504
                  errors on origin server instead of showing a default
                  Cloudflare error page. This does not apply to 522 errors and
                  is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Enable Error Pages On setting
                description: >-
                  Cloudflare will proxy customer error pages on any 502,504
                  errors on origin server instead of showing a default
                  Cloudflare error page. This does not apply to 522 errors and
                  is limited to Enterprise Zones.
            /zones/{zone_id}/settings/origin_max_http_version:
              get:
                tags:
                  - Zone Cache Settings
                summary: Get Origin Max HTTP Version Setting
                description: >-
                  Origin Max HTTP Setting Version sets the highest HTTP version
                  Cloudflare will attempt to use with your origin. This setting
                  allows Cloudflare to make HTTP/2 requests to your origin.
                  (Refer to [Enable HTTP/2 to
                  Origin](https://developers.cloudflare.com/cache/how-to/enable-http2-to-origin/),
                  for more information.). The default value is "2" for all plan
                  types except ENT where it is "1"
              patch:
                tags:
                  - Zone Cache Settings
                summary: Change Origin Max HTTP Version Setting
                description: >-
                  Origin Max HTTP Setting Version sets the highest HTTP version
                  Cloudflare will attempt to use with your origin. This setting
                  allows Cloudflare to make HTTP/2 requests to your origin.
                  (Refer to [Enable HTTP/2 to
                  Origin](https://developers.cloudflare.com/cache/how-to/enable-http2-to-origin/),
                  for more information.). The default value is "2" for all plan
                  types except ENT where it is "1"
            /zones/{zone_id}/settings/polish:
              get:
                tags:
                  - Zone Settings
                summary: Get Polish setting
                description: >
                  Automatically optimize image loading for website visitors on
                  mobile

                  devices. Refer to our [blog
                  post](http://blog.cloudflare.com/polish-solving-mobile-speed)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Polish setting
                description: >-
                  Automatically optimize image loading for website visitors on
                  mobile devices. Refer to our [blog
                  post](http://blog.cloudflare.com/polish-solving-mobile-speed)
                  for more information.
            /zones/{zone_id}/settings/prefetch_preload:
              get:
                tags:
                  - Zone Settings
                summary: Get prefetch preload setting
                description: >-
                  Cloudflare will prefetch any URLs that are included in the
                  response headers. This is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change prefetch preload setting
                description: >-
                  Cloudflare will prefetch any URLs that are included in the
                  response headers. This is limited to Enterprise Zones.
            /zones/{zone_id}/settings/proxy_read_timeout:
              get:
                tags:
                  - Zone Settings
                summary: Get Proxy Read Timeout setting
                description: |
                  Maximum time between two read operations from origin.
              patch:
                tags:
                  - Zone Settings
                summary: Change Proxy Read Timeout setting
                description: |
                  Maximum time between two read operations from origin.
            /zones/{zone_id}/settings/pseudo_ipv4:
              get:
                tags:
                  - Zone Settings
                summary: Get Pseudo IPv4 setting
                description: Value of the Pseudo IPv4 setting.
              patch:
                tags:
                  - Zone Settings
                summary: Change Pseudo IPv4 setting
                description: Value of the Pseudo IPv4 setting.
            /zones/{zone_id}/settings/response_buffering:
              get:
                tags:
                  - Zone Settings
                summary: Get Response Buffering setting
                description: >-
                  Enables or disables buffering of responses from the proxied
                  server. Cloudflare may buffer the whole payload to deliver it
                  at once to the client versus allowing it to be delivered in
                  chunks. By default, the proxied server streams directly and is
                  not buffered by Cloudflare. This is limited to Enterprise
                  Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Response Buffering setting
                description: >-
                  Enables or disables buffering of responses from the proxied
                  server. Cloudflare may buffer the whole payload to deliver it
                  at once to the client versus allowing it to be delivered in
                  chunks. By default, the proxied server streams directly and is
                  not buffered by Cloudflare. This is limited to Enterprise
                  Zones.
            /zones/{zone_id}/settings/rocket_loader:
              get:
                tags:
                  - Zone Settings
                summary: Get Rocket Loader setting
                description: >
                  Rocket Loader is a general-purpose asynchronous JavaScript
                  optimisation

                  that prioritises rendering your content while loading your
                  site's

                  Javascript asynchronously. Turning on Rocket Loader will
                  immediately

                  improve a web page's rendering time sometimes measured as Time
                  to First

                  Paint (TTFP), and also the `window.onload` time (assuming
                  there is

                  JavaScript on the page). This can have a positive impact on
                  your Google

                  search ranking. When turned on, Rocket Loader will
                  automatically defer

                  the loading of all Javascript referenced in your HTML, with no

                  configuration required. Refer to

                  [Understanding Rocket
                  Loader](https://support.cloudflare.com/hc/articles/200168056)

                  for more information.
              patch:
                tags:
                  - Zone Settings
                summary: Change Rocket Loader setting
                description: >
                  Rocket Loader is a general-purpose asynchronous JavaScript
                  optimisation

                  that prioritises rendering your content while loading your
                  site's

                  Javascript asynchronously. Turning on Rocket Loader will
                  immediately

                  improve a web page's rendering time sometimes measured as Time
                  to First

                  Paint (TTFP), and also the `window.onload` time (assuming
                  there is

                  JavaScript on the page). This can have a positive impact on
                  your Google

                  search ranking. When turned on, Rocket Loader will
                  automatically defer

                  the loading of all Javascript referenced in your HTML, with no

                  configuration required. Refer to

                  [Understanding Rocket
                  Loader](https://support.cloudflare.com/hc/articles/200168056)

                  for more information.
            /zones/{zone_id}/settings/security_header:
              get:
                tags:
                  - Zone Settings
                summary: Get Security Header (HSTS) setting
                description: Cloudflare security header for a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change Security Header (HSTS) setting
                description: Cloudflare security header for a zone.
            /zones/{zone_id}/settings/security_level:
              get:
                tags:
                  - Zone Settings
                summary: Get Security Level setting
                description: >-
                  Choose the appropriate security profile for your website,
                  which will automatically adjust each of the security settings.
                  If you choose to customize an individual security setting, the
                  profile will become Custom.
                  (https://support.cloudflare.com/hc/en-us/articles/200170056).
              patch:
                tags:
                  - Zone Settings
                summary: Change Security Level setting
                description: >-
                  Choose the appropriate security profile for your website,
                  which will automatically adjust each of the security settings.
                  If you choose to customize an individual security setting, the
                  profile will become Custom.
                  (https://support.cloudflare.com/hc/en-us/articles/200170056).
            /zones/{zone_id}/settings/server_side_exclude:
              get:
                tags:
                  - Zone Settings
                summary: Get Server Side Exclude setting
                description: >-
                  If there is sensitive content on your website that you want
                  visible to real visitors, but that you want to hide from
                  suspicious visitors, all you have to do is wrap the content
                  with Cloudflare SSE tags. Wrap any content that you want to be
                  excluded from suspicious visitors in the following SSE tags:
                  <!--sse--><!--/sse-->. For example: <!--sse-->  Bad visitors
                  won't see my phone number, 555-555-5555 <!--/sse-->. Note: SSE
                  only will work with HTML. If you have HTML minification
                  enabled, you won't see the SSE tags in your HTML source when
                  it's served through Cloudflare. SSE will still function in
                  this case, as Cloudflare's HTML minification and SSE
                  functionality occur on-the-fly as the resource moves through
                  our network to the visitor's computer.
                  (https://support.cloudflare.com/hc/en-us/articles/200170036).
              patch:
                tags:
                  - Zone Settings
                summary: Change Server Side Exclude setting
                description: >-
                  If there is sensitive content on your website that you want
                  visible to real visitors, but that you want to hide from
                  suspicious visitors, all you have to do is wrap the content
                  with Cloudflare SSE tags. Wrap any content that you want to be
                  excluded from suspicious visitors in the following SSE tags:
                  <!--sse--><!--/sse-->. For example: <!--sse-->  Bad visitors
                  won't see my phone number, 555-555-5555 <!--/sse-->. Note: SSE
                  only will work with HTML. If you have HTML minification
                  enabled, you won't see the SSE tags in your HTML source when
                  it's served through Cloudflare. SSE will still function in
                  this case, as Cloudflare's HTML minification and SSE
                  functionality occur on-the-fly as the resource moves through
                  our network to the visitor's computer.
                  (https://support.cloudflare.com/hc/en-us/articles/200170036).
            /zones/{zone_id}/settings/sort_query_string_for_cache:
              get:
                tags:
                  - Zone Settings
                summary: Get Enable Query String Sort setting
                description: >-
                  Cloudflare will treat files with the same query strings as the
                  same file in cache, regardless of the order of the query
                  strings. This is limited to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change Enable Query String Sort setting
                description: >-
                  Cloudflare will treat files with the same query strings as the
                  same file in cache, regardless of the order of the query
                  strings. This is limited to Enterprise Zones.
            /zones/{zone_id}/settings/ssl:
              get:
                tags:
                  - Zone Settings
                summary: Get SSL setting
                description: >-
                  SSL encrypts your visitor's connection and safeguards credit
                  card numbers and other personal data to and from your website.
                  SSL can take up to 5 minutes to fully activate. Requires
                  Cloudflare active on your root domain or www domain. Off: no
                  SSL between the visitor and Cloudflare, and no SSL between
                  Cloudflare and your web server  (all HTTP traffic). Flexible:
                  SSL between the visitor and Cloudflare -- visitor sees HTTPS
                  on your site, but no SSL between Cloudflare and your web
                  server. You don't need to have an SSL cert on your web server,
                  but your vistors will still see the site as being HTTPS
                  enabled. Full:  SSL between the visitor and Cloudflare --
                  visitor sees HTTPS on your site, and SSL between Cloudflare
                  and your web server. You'll need to have your own SSL cert or
                  self-signed cert at the very least. Full (Strict): SSL between
                  the visitor and Cloudflare -- visitor sees HTTPS on your site,
                  and SSL between Cloudflare and your web server. You'll need to
                  have a valid SSL certificate installed on your web server.
                  This certificate must be signed by a certificate authority,
                  have an expiration date in the future, and respond for the
                  request domain name (hostname).
                  (https://support.cloudflare.com/hc/en-us/articles/200170416).
              patch:
                tags:
                  - Zone Settings
                summary: Change SSL setting
                description: >-
                  SSL encrypts your visitor's connection and safeguards credit
                  card numbers and other personal data to and from your website.
                  SSL can take up to 5 minutes to fully activate. Requires
                  Cloudflare active on your root domain or www domain. Off: no
                  SSL between the visitor and Cloudflare, and no SSL between
                  Cloudflare and your web server  (all HTTP traffic). Flexible:
                  SSL between the visitor and Cloudflare -- visitor sees HTTPS
                  on your site, but no SSL between Cloudflare and your web
                  server. You don't need to have an SSL cert on your web server,
                  but your vistors will still see the site as being HTTPS
                  enabled. Full:  SSL between the visitor and Cloudflare --
                  visitor sees HTTPS on your site, and SSL between Cloudflare
                  and your web server. You'll need to have your own SSL cert or
                  self-signed cert at the very least. Full (Strict): SSL between
                  the visitor and Cloudflare -- visitor sees HTTPS on your site,
                  and SSL between Cloudflare and your web server. You'll need to
                  have a valid SSL certificate installed on your web server.
                  This certificate must be signed by a certificate authority,
                  have an expiration date in the future, and respond for the
                  request domain name (hostname).
                  (https://support.cloudflare.com/hc/en-us/articles/200170416).
            /zones/{zone_id}/settings/ssl_recommender:
              get:
                tags:
                  - Zone Settings
                summary: Get SSL/TLS Recommender enrollment setting
                description: >
                  Enrollment in the SSL/TLS Recommender service which tries to
                  detect and

                  recommend (by sending periodic emails) the most secure SSL/TLS
                  setting

                  your origin servers support.
              patch:
                tags:
                  - Zone Settings
                summary: Change SSL/TLS Recommender enrollment setting
                description: >
                  Enrollment in the SSL/TLS Recommender service which tries to
                  detect and

                  recommend (by sending periodic emails) the most secure SSL/TLS
                  setting

                  your origin servers support.
            /zones/{zone_id}/settings/tls_1_3:
              get:
                tags:
                  - Zone Settings
                summary: Get TLS 1.3 setting enabled for a zone
                description: Gets TLS 1.3 setting enabled for a zone.
              patch:
                tags:
                  - Zone Settings
                summary: Change TLS 1.3 setting
                description: Changes TLS 1.3 setting.
            /zones/{zone_id}/settings/tls_client_auth:
              get:
                tags:
                  - Zone Settings
                summary: Get TLS Client Auth setting
                description: >-
                  TLS Client Auth requires Cloudflare to connect to your origin
                  server using a client certificate (Enterprise Only).
              patch:
                tags:
                  - Zone Settings
                summary: Change TLS Client Auth setting
                description: >-
                  TLS Client Auth requires Cloudflare to connect to your origin
                  server using a client certificate (Enterprise Only).
            /zones/{zone_id}/settings/true_client_ip_header:
              get:
                tags:
                  - Zone Settings
                summary: Get True Client IP setting
                description: >-
                  Allows customer to continue to use True Client IP (Akamai
                  feature) in the headers we send to the origin. This is limited
                  to Enterprise Zones.
              patch:
                tags:
                  - Zone Settings
                summary: Change True Client IP setting
                description: >-
                  Allows customer to continue to use True Client IP (Akamai
                  feature) in the headers we send to the origin. This is limited
                  to Enterprise Zones.
            /zones/{zone_id}/settings/waf:
              get:
                tags:
                  - Zone Settings
                summary: Get Web Application Firewall (WAF) setting
                description: >-
                  The WAF examines HTTP requests to your website.  It inspects
                  both GET and POST requests and applies rules to help filter
                  out illegitimate traffic from legitimate website visitors. The
                  Cloudflare WAF inspects website addresses or URLs to detect
                  anything out of the ordinary. If the Cloudflare WAF determines
                  suspicious user behavior, then the WAF will 'challenge' the
                  web visitor with a page that asks them to submit a CAPTCHA
                  successfully  to continue their action. If the challenge is
                  failed, the action will be stopped. What this means is that
                  Cloudflare's WAF will block any traffic identified as
                  illegitimate before it reaches your origin web server.
                  (https://support.cloudflare.com/hc/en-us/articles/200172016).
              patch:
                tags:
                  - Zone Settings
                summary: Change Web Application Firewall (WAF) setting
                description: >-
                  The WAF examines HTTP requests to your website.  It inspects
                  both GET and POST requests and applies rules to help filter
                  out illegitimate traffic from legitimate website visitors. The
                  Cloudflare WAF inspects website addresses or URLs to detect
                  anything out of the ordinary. If the Cloudflare WAF determines
                  suspicious user behavior, then the WAF will 'challenge' the
                  web visitor with a page that asks them to submit a CAPTCHA
                  successfully  to continue their action. If the challenge is
                  failed, the action will be stopped. What this means is that
                  Cloudflare's WAF will block any traffic identified as
                  illegitimate before it reaches your origin web server.
                  (https://support.cloudflare.com/hc/en-us/articles/200172016).
            /zones/{zone_id}/settings/webp:
              get:
                tags:
                  - Zone Settings
                summary: Get WebP setting
                description: >-
                  When the client requesting the image supports the WebP image
                  codec, and WebP offers a performance advantage over the
                  original image format, Cloudflare will serve a WebP version of
                  the original image.
              patch:
                tags:
                  - Zone Settings
                summary: Change WebP setting
                description: >-
                  When the client requesting the image supports the WebP image
                  codec, and WebP offers a performance advantage over the
                  original image format, Cloudflare will serve a WebP version of
                  the original image.
            /zones/{zone_id}/settings/websockets:
              get:
                tags:
                  - Zone Settings
                summary: Get WebSockets setting
                description: >-
                  Gets Websockets setting. For more information about
                  Websockets, please refer to [Using Cloudflare with
                  WebSockets](https://support.cloudflare.com/hc/en-us/articles/200169466-Using-Cloudflare-with-WebSockets).
              patch:
                tags:
                  - Zone Settings
                summary: Change WebSockets setting
                description: >-
                  Changes Websockets setting. For more information about
                  Websockets, please refer to [Using Cloudflare with
                  WebSockets](https://support.cloudflare.com/hc/en-us/articles/200169466-Using-Cloudflare-with-WebSockets).
            /zones/{zone_id}/settings/zaraz/config:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz configuration
                description: >-
                  Gets latest Zaraz configuration for a zone. It can be preview
                  or published configuration, whichever was the last updated.
                  Secret variables values will not be included.
              put:
                tags:
                  - Zaraz
                summary: Update Zaraz configuration
                description: Updates Zaraz configuration for a zone.
            /zones/{zone_id}/settings/zaraz/default:
              get:
                tags:
                  - Zaraz
                summary: Get default Zaraz configuration
                description: Gets default Zaraz configuration for a zone.
            /zones/{zone_id}/settings/zaraz/export:
              get:
                tags:
                  - Zaraz
                summary: Export Zaraz configuration
                description: >-
                  Exports full current published Zaraz configuration for a zone,
                  secret variables included.
            /zones/{zone_id}/settings/zaraz/history:
              get:
                tags:
                  - Zaraz
                summary: List Zaraz historical configuration records
                description: >-
                  Lists a history of published Zaraz configuration records for a
                  zone.
              put:
                tags:
                  - Zaraz
                summary: Restore Zaraz historical configuration by ID
                description: >-
                  Restores a historical published Zaraz configuration by ID for
                  a zone.
            /zones/{zone_id}/settings/zaraz/history/configs:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz historical configurations by ID(s)
                description: >-
                  Gets a history of published Zaraz configurations by ID(s) for
                  a zone.
            /zones/{zone_id}/settings/zaraz/publish:
              post:
                tags:
                  - Zaraz
                summary: Publish Zaraz preview configuration
                description: Publish current Zaraz preview configuration for a zone.
            /zones/{zone_id}/settings/zaraz/workflow:
              get:
                tags:
                  - Zaraz
                summary: Get Zaraz workflow
                description: Gets Zaraz workflow for a zone.
              put:
                tags:
                  - Zaraz
                summary: Update Zaraz workflow
                description: Updates Zaraz workflow for a zone.
            /zones/{zone_id}/speed_api/availabilities:
              get:
                tags:
                  - Observatory
                summary: Get quota and availability
                description: >-
                  Retrieves quota for all plans, as well as the current zone
                  quota.
            /zones/{zone_id}/speed_api/pages:
              get:
                tags:
                  - Observatory
                summary: List tested webpages
                description: Lists all webpages which have been tested.
            /zones/{zone_id}/speed_api/pages/{url}/tests:
              delete:
                tags:
                  - Observatory
                summary: Delete all page tests
                description: >-
                  Deletes all tests for a specific webpage from a specific
                  region. Deleted tests are still counted as part of the quota.
              get:
                tags:
                  - Observatory
                summary: List page test history
                description: Test history (list of tests) for a specific webpage.
              post:
                tags:
                  - Observatory
                summary: Start page test
                description: Starts a test for a specific webpage, in a specific region.
            /zones/{zone_id}/speed_api/pages/{url}/tests/{test_id}:
              get:
                tags:
                  - Observatory
                summary: Get a page test result
                description: Retrieves the result of a specific test.
            /zones/{zone_id}/speed_api/pages/{url}/trend:
              get:
                tags:
                  - Observatory
                summary: List core web vital metrics trend
                description: >-
                  Lists the core web vital metrics trend over time for a
                  specific page.
            /zones/{zone_id}/speed_api/schedule/{url}:
              delete:
                tags:
                  - Observatory
                summary: Delete scheduled page test
                description: Deletes a scheduled test for a page.
              get:
                tags:
                  - Observatory
                summary: Get a page test schedule
                description: Retrieves the test schedule for a page in a specific region.
              post:
                tags:
                  - Observatory
                summary: Create scheduled page test
                description: Creates a scheduled test for a page.
            /zones/{zone_id}/ssl/analyze:
              post:
                tags:
                  - Analyze Certificate
                summary: Analyze Certificate
                description: >-
                  Returns the set of hostnames, the signature algorithm, and the
                  expiration date of the certificate.
            /zones/{zone_id}/ssl/certificate_packs:
              get:
                tags:
                  - Certificate Packs
                summary: List Certificate Packs
                description: For a given zone, list all active certificate packs.
            /zones/{zone_id}/ssl/certificate_packs/{certificate_pack_id}:
              delete:
                tags:
                  - Certificate Packs
                summary: Delete Advanced Certificate Manager Certificate Pack
                description: For a given zone, delete an advanced certificate pack.
              get:
                tags:
                  - Certificate Packs
                summary: Get Certificate Pack
                description: For a given zone, get a certificate pack.
              patch:
                tags:
                  - Certificate Packs
                summary: >-
                  Restart Validation for Advanced Certificate Manager
                  Certificate Pack
                description: >-
                  For a given zone, restart validation for an advanced
                  certificate pack.  This is only a validation operation for a
                  Certificate Pack in a validation_timed_out status.
            /zones/{zone_id}/ssl/certificate_packs/order:
              post:
                tags:
                  - Certificate Packs
                summary: Order Advanced Certificate Manager Certificate Pack
                description: For a given zone, order an advanced certificate pack.
            /zones/{zone_id}/ssl/certificate_packs/quota:
              get:
                tags:
                  - Certificate Packs
                summary: Get Certificate Pack Quotas
                description: For a given zone, list certificate pack quotas.
            /zones/{zone_id}/ssl/universal/settings:
              get:
                tags:
                  - Universal SSL Settings for a Zone
                summary: Universal SSL Settings Details
                description: Get Universal SSL Settings for a Zone.
              patch:
                tags:
                  - Universal SSL Settings for a Zone
                summary: Edit Universal SSL Settings
                description: Patch Universal SSL Settings for a Zone.
            /zones/{zone_id}/ssl/verification:
              get:
                tags:
                  - SSL Verification
                summary: SSL Verification Details
                description: Get SSL Verification Info for a Zone.
            /zones/{zone_id}/ssl/verification/{certificate_pack_id}:
              patch:
                tags:
                  - SSL Verification
                summary: Edit SSL Certificate Pack Validation Method
                description: >-
                  Edit SSL validation method for a certificate pack. A PATCH
                  request will request an immediate validation check on any
                  certificate, and return the updated status. If a validation
                  method is provided, the validation will be immediately
                  attempted using that method.
            /zones/{zone_id}/url_normalization:
              get:
                tags:
                  - URL Normalization
                summary: Get URL normalization settings
                description: Fetches the current URL normalization settings.
              put:
                tags:
                  - URL Normalization
                summary: Update URL normalization settings
                description: Updates the URL normalization settings.
            /zones/{zone_id}/workers/filters:
              get:
                tags:
                  - Worker Filters (Deprecated)
                summary: List Filters
              post:
                tags:
                  - Worker Filters (Deprecated)
                summary: Create Filter
            /zones/{zone_id}/workers/filters/{filter_id}:
              delete:
                tags:
                  - Worker Filters (Deprecated)
                summary: Delete Filter
              put:
                tags:
                  - Worker Filters (Deprecated)
                summary: Update Filter
            /zones/{zone_id}/workers/routes:
              get:
                tags:
                  - Worker Routes
                summary: List Routes
                description: Returns routes for a zone.
              post:
                tags:
                  - Worker Routes
                summary: Create Route
                description: Creates a route that maps a URL pattern to a Worker.
            /zones/{zone_id}/workers/routes/{route_id}:
              delete:
                tags:
                  - Worker Routes
                summary: Delete Route
                description: Deletes a route.
              get:
                tags:
                  - Worker Routes
                summary: Get Route
                description: >-
                  Returns information about a route, including URL pattern and
                  Worker.
              put:
                tags:
                  - Worker Routes
                summary: Update Route
                description: Updates the URL pattern or Worker associated with a route.
            /zones/{zone_id}/workers/script:
              delete:
                tags:
                  - Worker Script (Deprecated)
                summary: Delete Worker
                description: >-
                  Delete your Worker. This call has no response body on a
                  successful delete.
              get:
                tags:
                  - Worker Script (Deprecated)
                summary: Download Worker
                description: >-
                  Fetch raw script content for your worker. Note this is the
                  original script content, not JSON encoded.
              put:
                tags:
                  - Worker Script (Deprecated)
                summary: Upload Worker
                description: Upload a worker, or a new version of a worker.
            /zones/{zone_id}/workers/script/bindings:
              get:
                tags:
                  - Worker Binding (Deprecated)
                summary: List Bindings
                description: List the bindings for a Workers script.
            /zones/{zone_identifier}/analytics/colos:
              get:
                tags:
                  - Zone Analytics (Deprecated)
                summary: Get analytics by Co-locations
                description: >-
                  This view provides a breakdown of analytics data by
                  datacenter. Note: This is available to Enterprise customers
                  only.
            /zones/{zone_identifier}/analytics/dashboard:
              get:
                tags:
                  - Zone Analytics (Deprecated)
                summary: Get dashboard
                description: >-
                  The dashboard view provides both totals and timeseries data
                  for the given zone and time period across the entire
                  Cloudflare network.
            /zones/{zone_identifier}/available_plans:
              get:
                tags:
                  - Zone Rate Plan
                summary: List Available Plans
                description: Lists available plans the zone can subscribe to.
            /zones/{zone_identifier}/available_plans/{plan_identifier}:
              get:
                tags:
                  - Zone Rate Plan
                summary: Available Plan Details
                description: Details of the available plan that the zone can subscribe to.
            /zones/{zone_identifier}/available_rate_plans:
              get:
                tags:
                  - Zone Rate Plan
                summary: List Available Rate Plans
                description: Lists all rate plans the zone can subscribe to.
            /zones/{zone_identifier}/custom_pages:
              get:
                tags:
                  - Custom pages for a zone
                summary: List custom pages
                description: Fetches all the custom pages at the zone level.
            /zones/{zone_identifier}/custom_pages/{identifier}:
              get:
                tags:
                  - Custom pages for a zone
                summary: Get a custom page
                description: Fetches the details of a custom page.
              put:
                tags:
                  - Custom pages for a zone
                summary: Update a custom page
                description: Updates the configuration of an existing custom page.
            /zones/{zone_identifier}/email/routing:
              get:
                tags:
                  - Email Routing settings
                summary: Get Email Routing settings
                description: >-
                  Get information about the settings for your Email Routing
                  zone.
            /zones/{zone_identifier}/email/routing/disable:
              post:
                tags:
                  - Email Routing settings
                summary: Disable Email Routing
                description: >-
                  Disable your Email Routing zone. Also removes additional MX
                  records previously required for Email Routing to work.
            /zones/{zone_identifier}/email/routing/dns:
              get:
                tags:
                  - Email Routing settings
                summary: Email Routing - DNS settings
                description: >-
                  Show the DNS records needed to configure your Email Routing
                  zone.
            /zones/{zone_identifier}/email/routing/enable:
              post:
                tags:
                  - Email Routing settings
                summary: Enable Email Routing
                description: >-
                  Enable you Email Routing zone. Add and lock the necessary MX
                  and SPF records.
            /zones/{zone_identifier}/email/routing/rules:
              get:
                tags:
                  - Email Routing routing rules
                summary: List routing rules
                description: Lists existing routing rules.
              post:
                tags:
                  - Email Routing routing rules
                summary: Create routing rule
                description: >-
                  Rules consist of a set of criteria for matching emails (such
                  as an email being sent to a specific custom email address)
                  plus a set of actions to take on the email (like forwarding it
                  to a specific destination address).
            /zones/{zone_identifier}/email/routing/rules/{rule_identifier}:
              delete:
                tags:
                  - Email Routing routing rules
                summary: Delete routing rule
                description: Delete a specific routing rule.
              get:
                tags:
                  - Email Routing routing rules
                summary: Get routing rule
                description: Get information for a specific routing rule already created.
              put:
                tags:
                  - Email Routing routing rules
                summary: Update routing rule
                description: >-
                  Update actions and matches, or enable/disable specific routing
                  rules.
            /zones/{zone_identifier}/email/routing/rules/catch_all:
              get:
                tags:
                  - Email Routing routing rules
                summary: Get catch-all rule
                description: Get information on the default catch-all routing rule.
              put:
                tags:
                  - Email Routing routing rules
                summary: Update catch-all rule
                description: >-
                  Enable or disable catch-all routing rule, or change action to
                  forward to specific destination address.
            /zones/{zone_identifier}/filters:
              delete:
                tags:
                  - Filters
                summary: Delete filters
                description: Deletes one or more existing filters.
              get:
                tags:
                  - Filters
                summary: List filters
                description: >-
                  Fetches filters in a zone. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - Filters
                summary: Create filters
                description: Creates one or more filters.
              put:
                tags:
                  - Filters
                summary: Update filters
                description: Updates one or more existing filters.
            /zones/{zone_identifier}/filters/{id}:
              delete:
                tags:
                  - Filters
                summary: Delete a filter
                description: Deletes an existing filter.
              get:
                tags:
                  - Filters
                summary: Get a filter
                description: Fetches the details of a filter.
              put:
                tags:
                  - Filters
                summary: Update a filter
                description: Updates an existing filter.
            /zones/{zone_identifier}/firewall/lockdowns:
              get:
                tags:
                  - Zone Lockdown
                summary: List Zone Lockdown rules
                description: >-
                  Fetches Zone Lockdown rules. You can filter the results using
                  several optional parameters.
              post:
                tags:
                  - Zone Lockdown
                summary: Create a Zone Lockdown rule
                description: Creates a new Zone Lockdown rule.
            /zones/{zone_identifier}/firewall/lockdowns/{id}:
              delete:
                tags:
                  - Zone Lockdown
                summary: Delete a Zone Lockdown rule
                description: Deletes an existing Zone Lockdown rule.
              get:
                tags:
                  - Zone Lockdown
                summary: Get a Zone Lockdown rule
                description: Fetches the details of a Zone Lockdown rule.
              put:
                tags:
                  - Zone Lockdown
                summary: Update a Zone Lockdown rule
                description: Updates an existing Zone Lockdown rule.
            /zones/{zone_identifier}/firewall/rules:
              delete:
                tags:
                  - Firewall rules
                summary: Delete firewall rules
                description: Deletes existing firewall rules.
              get:
                tags:
                  - Firewall rules
                summary: List firewall rules
                description: >-
                  Fetches firewall rules in a zone. You can filter the results
                  using several optional parameters.
              patch:
                tags:
                  - Firewall rules
                summary: Update priority of firewall rules
                description: Updates the priority of existing firewall rules.
              post:
                tags:
                  - Firewall rules
                summary: Create firewall rules
                description: Create one or more firewall rules.
              put:
                tags:
                  - Firewall rules
                summary: Update firewall rules
                description: Updates one or more existing firewall rules.
            /zones/{zone_identifier}/firewall/rules/{id}:
              delete:
                tags:
                  - Firewall rules
                summary: Delete a firewall rule
                description: Deletes an existing firewall rule.
              get:
                tags:
                  - Firewall rules
                summary: Get a firewall rule
                description: Fetches the details of a firewall rule.
              patch:
                tags:
                  - Firewall rules
                summary: Update priority of a firewall rule
                description: Updates the priority of an existing firewall rule.
              put:
                tags:
                  - Firewall rules
                summary: Update a firewall rule
                description: Updates an existing firewall rule.
            /zones/{zone_identifier}/firewall/ua_rules:
              get:
                tags:
                  - User Agent Blocking rules
                summary: List User Agent Blocking rules
                description: >-
                  Fetches User Agent Blocking rules in a zone. You can filter
                  the results using several optional parameters.
              post:
                tags:
                  - User Agent Blocking rules
                summary: Create a User Agent Blocking rule
                description: Creates a new User Agent Blocking rule in a zone.
            /zones/{zone_identifier}/firewall/ua_rules/{id}:
              delete:
                tags:
                  - User Agent Blocking rules
                summary: Delete a User Agent Blocking rule
                description: Deletes an existing User Agent Blocking rule.
              get:
                tags:
                  - User Agent Blocking rules
                summary: Get a User Agent Blocking rule
                description: Fetches the details of a User Agent Blocking rule.
              put:
                tags:
                  - User Agent Blocking rules
                summary: Update a User Agent Blocking rule
                description: Updates an existing User Agent Blocking rule.
            /zones/{zone_identifier}/firewall/waf/overrides:
              get:
                tags:
                  - WAF overrides
                summary: List WAF overrides
                description: >-
                  Fetches the URI-based WAF overrides in a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              post:
                tags:
                  - WAF overrides
                summary: Create a WAF override
                description: >-
                  Creates a URI-based WAF override for a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/overrides/{id}:
              delete:
                tags:
                  - WAF overrides
                summary: Delete a WAF override
                description: >-
                  Deletes an existing URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              get:
                tags:
                  - WAF overrides
                summary: Get a WAF override
                description: >-
                  Fetches the details of a URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              put:
                tags:
                  - WAF overrides
                summary: Update WAF override
                description: >-
                  Updates an existing URI-based WAF override.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/packages:
              get:
                tags:
                  - WAF packages
                summary: List WAF packages
                description: >-
                  Fetches WAF packages for a zone.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/firewall/waf/packages/{identifier}:
              get:
                tags:
                  - WAF packages
                summary: Get a WAF package
                description: >-
                  Fetches the details of a WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
              patch:
                tags:
                  - WAF packages
                summary: Update a WAF package
                description: >-
                  Updates a WAF package. You can update the sensitivity and the
                  action of an anomaly detection WAF package.


                  **Note:** Applies only to the [previous version of WAF managed
                  rules](https://developers.cloudflare.com/support/firewall/managed-rules-web-application-firewall-waf/understanding-waf-managed-rules-web-application-firewall/).
            /zones/{zone_identifier}/healthchecks:
              get:
                tags:
                  - Health Checks
                summary: List Health Checks
                description: List configured health checks.
              post:
                tags:
                  - Health Checks
                summary: Create Health Check
                description: Create a new health check.
            /zones/{zone_identifier}/healthchecks/{identifier}:
              delete:
                tags:
                  - Health Checks
                summary: Delete Health Check
                description: Delete a health check.
              get:
                tags:
                  - Health Checks
                summary: Health Check Details
                description: Fetch a single configured health check.
              patch:
                tags:
                  - Health Checks
                summary: Patch Health Check
                description: Patch a configured health check.
              put:
                tags:
                  - Health Checks
                summary: Update Health Check
                description: Update a configured health check.
            /zones/{zone_identifier}/healthchecks/preview:
              post:
                tags:
                  - Health Checks
                summary: Create Preview Health Check
                description: Create a new preview health check.
            /zones/{zone_identifier}/healthchecks/preview/{identifier}:
              delete:
                tags:
                  - Health Checks
                summary: Delete Preview Health Check
                description: Delete a health check.
              get:
                tags:
                  - Health Checks
                summary: Health Check Preview Details
                description: Fetch a single configured health check preview.
            /zones/{zone_identifier}/logs/control/retention/flag:
              get:
                tags:
                  - Logs Received
                summary: Get log retention flag
                description: Gets log retention flag for Logpull API.
              post:
                tags:
                  - Logs Received
                summary: Update log retention flag
                description: Updates log retention flag for Logpull API.
            /zones/{zone_identifier}/logs/rayids/{ray_identifier}:
              get:
                tags:
                  - Logs Received
                summary: Get logs RayIDs
                description: >-
                  The `/rayids` api route allows lookups by specific rayid. The
                  rayids route will return zero, one, or more records (ray ids
                  are not unique).
            /zones/{zone_identifier}/logs/received:
              get:
                tags:
                  - Logs Received
                summary: Get logs received
                description: >-
                  The `/received` api route allows customers to retrieve their
                  edge HTTP logs. The basic access pattern is "give me all the
                  logs for zone Z for minute M", where the minute M refers to
                  the time records were received at Cloudflare's central data
                  center. `start` is inclusive, and `end` is exclusive. Because
                  of that, to get all data, at minutely cadence, starting at
                  10AM, the proper values are:
                  `start=2018-05-20T10:00:00Z&end=2018-05-20T10:01:00Z`, then
                  `start=2018-05-20T10:01:00Z&end=2018-05-20T10:02:00Z` and so
                  on; the overlap will be handled properly.
            /zones/{zone_identifier}/logs/received/fields:
              get:
                tags:
                  - Logs Received
                summary: List fields
                description: >-
                  Lists all fields available. The response is json object with
                  key-value pairs, where keys are field names, and values are
                  descriptions.
            /zones/{zone_identifier}/rate_limits:
              get:
                tags:
                  - Rate limits for a zone
                summary: List rate limits
                description: Fetches the rate limits for a zone.
              post:
                tags:
                  - Rate limits for a zone
                summary: Create a rate limit
                description: >-
                  Creates a new rate limit for a zone. Refer to the object
                  definition for a list of required attributes.
            /zones/{zone_identifier}/rate_limits/{id}:
              delete:
                tags:
                  - Rate limits for a zone
                summary: Delete a rate limit
                description: Deletes an existing rate limit.
              get:
                tags:
                  - Rate limits for a zone
                summary: Get a rate limit
                description: Fetches the details of a rate limit.
              put:
                tags:
                  - Rate limits for a zone
                summary: Update a rate limit
                description: Updates an existing rate limit.
            /zones/{zone_identifier}/snippets:
              get:
                tags:
                  - Zone Snippets
                summary: All Snippets
            /zones/{zone_identifier}/snippets/{snippet_name}:
              delete:
                tags:
                  - Zone Snippets
                summary: Delete Snippet
              get:
                tags:
                  - Zone Snippets
                summary: Snippet
              put:
                tags:
                  - Zone Snippets
                summary: Put Snippet
            /zones/{zone_identifier}/snippets/{snippet_name}/content:
              get:
                tags:
                  - Zone Snippets
                summary: Snippet Content
            /zones/{zone_identifier}/snippets/snippet_rules:
              get:
                tags:
                  - Zone Snippets
                summary: Rules
              put:
                tags:
                  - Zone Snippets
                summary: Put Rules
            /zones/{zone_identifier}/ssl/recommendation:
              get:
                tags:
                  - SSL/TLS Mode Recommendation
                summary: SSL/TLS Recommendation
                description: Retrieve the SSL/TLS Recommender's recommendation for a zone.
            /zones/{zone_identifier}/waiting_rooms:
              get:
                tags:
                  - Waiting Room
                summary: List waiting rooms
                description: Lists waiting rooms.
              post:
                tags:
                  - Waiting Room
                summary: Create waiting room
                description: Creates a new waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete waiting room
                description: Deletes a waiting room.
              get:
                tags:
                  - Waiting Room
                summary: Waiting room details
                description: Fetches a single configured waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch waiting room
                description: Patches a configured waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Update waiting room
                description: Updates a configured waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events:
              get:
                tags:
                  - Waiting Room
                summary: List events
                description: Lists events for a waiting room.
              post:
                tags:
                  - Waiting Room
                summary: Create event
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Creates an event for a waiting room. An event takes place
                  during a specified period of time, temporarily changing the
                  behavior of a waiting room. While the event is active, some of
                  the properties in the event's configuration may either
                  override or inherit from the waiting room's configuration.
                  Note that events cannot overlap with each other, so only one
                  event can be active at a time.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events/{event_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete event
                description: Deletes an event for a waiting room.
              get:
                tags:
                  - Waiting Room
                summary: Event details
                description: Fetches a single configured event for a waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch event
                description: Patches a configured event for a waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Update event
                description: Updates a configured event for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/events/{event_id}/details:
              get:
                tags:
                  - Waiting Room
                summary: Preview active event details
                description: >-
                  Previews an event's configuration as if it was active.
                  Inherited fields from the waiting room will be displayed with
                  their current values.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/rules:
              get:
                tags:
                  - Waiting Room
                summary: List Waiting Room Rules
                description: Lists rules for a waiting room.
              post:
                tags:
                  - Waiting Room
                summary: Create Waiting Room Rule
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Creates a rule for a waiting room.
              put:
                tags:
                  - Waiting Room
                summary: Replace Waiting Room Rules
                description: >-
                  Only available for the Waiting Room Advanced subscription.
                  Replaces all rules for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/rules/{rule_id}:
              delete:
                tags:
                  - Waiting Room
                summary: Delete Waiting Room Rule
                description: Deletes a rule for a waiting room.
              patch:
                tags:
                  - Waiting Room
                summary: Patch Waiting Room Rule
                description: Patches a rule for a waiting room.
            /zones/{zone_identifier}/waiting_rooms/{waiting_room_id}/status:
              get:
                tags:
                  - Waiting Room
                summary: Get waiting room status
                description: "Fetches the status of a configured waiting room. Response fields include:\n1. `status`: String indicating the status of the waiting room. The possible status are:\n\t- **not_queueing** indicates that the configured thresholds have not been met and all users are going through to the origin.\n\t- **queueing** indicates that the thresholds have been met and some users are held in the waiting room.\n\t- **event_prequeueing** indicates that an event is active and is currently prequeueing users before it starts.\n2. `event_id`: String of the current event's `id` if an event is active, otherwise an empty string.\n3. `estimated_queued_users`: Integer of the estimated number of users currently waiting in the queue.\n4. `estimated_total_active_users`: Integer of the estimated number of users currently active on the origin.\n5. `max_estimated_time_minutes`: Integer of the maximum estimated time currently presented to the users."
            /zones/{zone_identifier}/waiting_rooms/preview:
              post:
                tags:
                  - Waiting Room
                summary: Create a custom waiting room page preview
                description: "Creates a waiting room page preview. Upload a custom waiting room page for preview. You will receive a preview URL in the form `http://waitingrooms.dev/preview/<uuid>`. You can use the following query parameters to change the state of the preview:\n1. `force_queue`: Boolean indicating if all users will be queued in the waiting room and no one will be let into the origin website (also known as queueAll).\n2. `queue_is_full`: Boolean indicating if the waiting room's queue is currently full and not accepting new users at the moment.\n3. `queueing_method`: The queueing method currently used by the waiting room.\n\t- **fifo** indicates a FIFO queue.\n\t- **random** indicates a Random queue.\n\t- **passthrough** indicates a Passthrough queue. Keep in mind that the waiting room page will only be displayed if `force_queue=true` or `event=prequeueing` — for other cases the request will pass through to the origin. For our preview, this will be a fake origin website returning \"Welcome\". \n\t- **reject** indicates a Reject queue.\n4. `event`: Used to preview a waiting room event.\n\t- **none** indicates no event is occurring.\n\t- **prequeueing** indicates that an event is prequeueing (between `prequeue_start_time` and `event_start_time`).\n\t- **started** indicates that an event has started (between `event_start_time` and `event_end_time`).\n5. `shuffle_at_event_start`: Boolean indicating if the event will shuffle users in the prequeue when it starts. This can only be set to **true** if an event is active (`event` is not **none**).\n\nFor example, you can make a request to `http://waitingrooms.dev/preview/<uuid>?force_queue=false&queue_is_full=false&queueing_method=random&event=started&shuffle_at_event_start=true`\n6. `waitTime`: Non-zero, positive integer indicating the estimated wait time in minutes. The default value is 10 minutes.\n\nFor example, you can make a request to `http://waitingrooms.dev/preview/<uuid>?waitTime=50` to configure the estimated wait time as 50 minutes."
            /zones/{zone_identifier}/waiting_rooms/settings:
              get:
                tags:
                  - Waiting Room
                summary: Get zone-level Waiting Room settings
              patch:
                tags:
                  - Waiting Room
                summary: Patch zone-level Waiting Room settings
              put:
                tags:
                  - Waiting Room
                summary: Update zone-level Waiting Room settings
            /zones/{zone_identifier}/web3/hostnames:
              get:
                tags:
                  - Web3 Hostname
                summary: List Web3 Hostnames
              post:
                tags:
                  - Web3 Hostname
                summary: Create Web3 Hostname
            /zones/{zone_identifier}/web3/hostnames/{identifier}:
              delete:
                tags:
                  - Web3 Hostname
                summary: Delete Web3 Hostname
              get:
                tags:
                  - Web3 Hostname
                summary: Web3 Hostname Details
              patch:
                tags:
                  - Web3 Hostname
                summary: Edit Web3 Hostname
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list:
              get:
                tags:
                  - Web3 Hostname
                summary: IPFS Universal Path Gateway Content List Details
              put:
                tags:
                  - Web3 Hostname
                summary: Update IPFS Universal Path Gateway Content List
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list/entries:
              get:
                tags:
                  - Web3 Hostname
                summary: List IPFS Universal Path Gateway Content List Entries
              post:
                tags:
                  - Web3 Hostname
                summary: Create IPFS Universal Path Gateway Content List Entry
            /zones/{zone_identifier}/web3/hostnames/{identifier}/ipfs_universal_path/content_list/entries/{content_list_entry_identifier}:
              delete:
                tags:
                  - Web3 Hostname
                summary: Delete IPFS Universal Path Gateway Content List Entry
              get:
                tags:
                  - Web3 Hostname
                summary: IPFS Universal Path Gateway Content List Entry Details
              put:
                tags:
                  - Web3 Hostname
                summary: Edit IPFS Universal Path Gateway Content List Entry
            /zones/{zone}/spectrum/analytics/aggregate/current:
              get:
                tags:
                  - Spectrum Aggregate Analytics
                summary: Get current aggregated analytics
                description: >-
                  Retrieves analytics aggregated from the last minute of usage
                  on Spectrum applications underneath a given zone.
            /zones/{zone}/spectrum/analytics/events/bytime:
              get:
                tags:
                  - Spectrum Analytics (By Time)
                summary: Get analytics by time
                description: >-
                  Retrieves a list of aggregate metrics grouped by time
                  interval.
            /zones/{zone}/spectrum/analytics/events/summary:
              get:
                tags:
                  - Spectrum Analytics (Summary)
                summary: Get analytics summary
                description: >-
                  Retrieves a list of summarised aggregate metrics over a given
                  time period.
            /zones/{zone}/spectrum/apps:
              get:
                tags:
                  - Spectrum Applications
                summary: List Spectrum applications
                description: >-
                  Retrieves a list of currently existing Spectrum applications
                  inside a zone.
              post:
                tags:
                  - Spectrum Applications
                summary: Create Spectrum application using a name for the origin
                description: >-
                  Creates a new Spectrum application from a configuration using
                  a name for the origin.
            /zones/{zone}/spectrum/apps/{app_id}:
              delete:
                tags:
                  - Spectrum Applications
                summary: Delete Spectrum application
                description: Deletes a previously existing application.
              get:
                tags:
                  - Spectrum Applications
                summary: Get Spectrum application configuration
                description: >-
                  Gets the application configuration of a specific application
                  inside a zone.
              put:
                tags:
                  - Spectrum Applications
                summary: >-
                  Update Spectrum application configuration using a name for the
                  origin
                description: >-
                  Updates a previously existing application's configuration that
                  uses a name for the origin.
    contact:
      - FN: Support
        url: https://support.cloudflare.com/
        email: ''
    overlays:
      - type: API Evangelist Ratings
        url: overlays/cloudflare-openapi-api-evangelist-ratings.yml
      - type: APIs.io Search
        url: overlays/cloudflare-openapi-search.yml
    aid: cloudflare:cloudflare-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---