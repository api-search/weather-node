---
name: Concatenation
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/concatenation.png
url: https://example.com/apis/concatenation.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Concatenation
apis:
  - name: chime-sdk-media-pipelines
    description: >-
      <p>The Amazon Chime SDK media pipeline APIs in this section allow software
      developers to create Amazon Chime SDK media pipelines that capture,
      concatenate, or stream your Amazon Chime SDK meetings. For more
      information about media pipelines, see <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_Operations_Amazon_Chime_SDK_Media_Pipelines.html">Amazon
      Chime SDK media pipelines</a>. </p>
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
            title: chime-sdk-media-pipelines
          paths:
            /sdk-media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
            /sdk-media-concatenation-pipelines:
              POST:
                summary: CreateMediaConcatenationPipeline
                description: <p>Creates a media concatenation pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Concatenation
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
            /media-insights-pipelines:
              POST:
                summary: CreateMediaInsightsPipeline
                description: <p>Creates a media insights pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Insights
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
            /media-insights-pipeline-configurations:
              GET:
                summary: ListMediaInsightsPipelineConfigurations
                description: >-
                  <p>Lists the available media insights pipeline
                  configurations.</p>
                tags:
                  - Lists
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
            /sdk-media-live-connector-pipelines:
              POST:
                summary: CreateMediaLiveConnectorPipeline
                description: >-
                  <p>Creates a media live connector pipeline in an Amazon Chime
                  SDK meeting.</p>
                tags:
                  - Create
                  - Media
                  - Live
                  - Connectors
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
            /media-pipeline-kinesis-video-stream-pools:
              GET:
                summary: ListMediaPipelineKinesisVideoStreamPools
                description: <p>Lists the video stream pools in the media pipeline.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-stream-pipelines:
              POST:
                summary: CreateMediaStreamPipeline
                description: <p>Creates a streaming media pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Stream
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
            /media-insights-pipeline-configurations/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineConfiguration
                description: >-
                  <p>Updates the media insights pipeline's configuration
                  settings.</p>
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /sdk-media-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaPipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-pipeline-kinesis-video-stream-pools/{identifier}:
              PUT:
                summary: UpdateMediaPipelineKinesisVideoStreamPool
                description: >-
                  <p>Updates an Kinesis video stream pool in a media
                  pipeline.</p>
                tags:
                  - Update
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}:
              GET:
                summary: GetSpeakerSearchTask
                description: >-
                  <p>Retrieves the details of the specified speaker search
                  task.</p>
                tags:
                  - Get
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}:
              GET:
                summary: GetVoiceToneAnalysisTask
                description: <p>Retrieves the details of a voice tone analysis task.</p>
                tags:
                  - Get
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /sdk-media-pipelines:
              GET:
                summary: ListMediaPipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /tags:
              GET:
                summary: ListTagsForResource
                description: <p>Lists the tags available for a media pipeline.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
            /media-insights-pipelines/{identifier}/speaker-search-tasks?operation=start:
              POST:
                summary: StartSpeakerSearchTask
                description: >-
                  <p>Starts a speaker search task.</p> <important> <p>Before
                  starting any speaker search tasks, you must provide all
                  notices and obtain all consents from the speaker as required
                  under applicable privacy and biometrics laws, and as required
                  under the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks?operation=start:
              POST:
                summary: StartVoiceToneAnalysisTask
                description: >-
                  <p>Starts a voice tone analysis task. For more information
                  about voice tone analysis, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/voice-analytics.html">Using
                  Amazon Chime SDK voice analytics</a> in the <i>Amazon Chime
                  SDK Developer Guide</i>.</p> <important> <p>Before starting
                  any voice tone analysis tasks, you must provide all notices
                  and obtain all consents from the speaker as required under
                  applicable privacy and biometrics laws, and as required under
                  the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}?operation=stop:
              POST:
                summary: StopSpeakerSearchTask
                description: <p>Stops a speaker search task.</p>
                tags:
                  - Stop
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}?operation=stop:
              POST:
                summary: StopVoiceToneAnalysisTask
                description: <p>Stops a voice tone analysis task.</p>
                tags:
                  - Stop
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>The ARN of the media pipeline that you want to tag.
                  Consists of the pipeline's endpoint region, resource ID, and
                  pipeline ID.</p>
                tags:
                  - Tags
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: <p>Removes any tags from a media pipeline.</p>
                tags:
                  - Untag
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
            /media-insights-pipeline-status/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineStatus
                description: <p>Updates the status of a media insights pip
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Status
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-media-pipelines-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-media-pipelines-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-media-pipelines
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---