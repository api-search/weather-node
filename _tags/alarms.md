---
name: Alarms
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alarms.png
url: https://example.com/apis/alarms.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alarms
apis:
  - name: iotevents-data
    description: >-
      <p>IoT Events monitors your equipment or device fleets for failures or
      changes in operation, and triggers actions when such events occur. You can
      use IoT Events Data API commands to send inputs to detectors, list
      detectors, and view or update a detector's status.</p> <p> For more
      information, see <a
      href="https://docs.aws.amazon.com/iotevents/latest/developerguide/what-is-iotevents.html">What
      is IoT Events?</a> in the <i>IoT Events Developer Guide</i>.</p>
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
            title: iotevents-data
          paths:
            /alarms/acknowledge:
              POST:
                summary: BatchAcknowledgeAlarm
                description: >-
                  <p>Acknowledges one or more alarms. The alarms change to the
                  <code>ACKNOWLEDGED</code> state after you acknowledge
                  them.</p>
                tags:
                  - Batches
                  - Acknowledge
                  - Alarm
                  - Alarms
                  - Acknowledge
            /detectors/delete:
              POST:
                summary: BatchDeleteDetector
                description: >-
                  <p>Deletes one or more detectors that were created. When a
                  detector is deleted, its state will be cleared and the
                  detector will be removed from the list of detectors. The
                  deleted detector will no longer appear if referenced in the <a
                  href="https://docs.aws.amazon.com/iotevents/latest/apireference/API_iotevents-data_ListDetectors.html">ListDetectors</a>
                  API call.</p>
                tags:
                  - Batches
                  - Delete
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
            /alarms/disable:
              POST:
                summary: BatchDisableAlarm
                description: >-
                  <p>Disables one or more alarms. The alarms change to the
                  <code>DISABLED</code> state after you disable them.</p>
                tags:
                  - Batches
                  - Disable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
            /alarms/enable:
              POST:
                summary: BatchEnableAlarm
                description: >-
                  <p>Enables one or more alarms. The alarms change to the
                  <code>NORMAL</code> state after you enable them.</p>
                tags:
                  - Batches
                  - Enable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
            /inputs/messages:
              POST:
                summary: BatchPutMessage
                description: >-
                  <p>Sends a set of messages to the IoT Events system. Each
                  message payload is transformed into the input you specify
                  (<code>"inputName"</code>) and ingested into any detectors
                  that monitor that input. If multiple messages are sent, the
                  order in which the messages are processed isn't guaranteed. To
                  guarantee ordering, you must send messages one at a time and
                  wait for a successful response.</p>
                tags:
                  - Batches
                  - Put
                  - Messages
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
            /alarms/reset:
              POST:
                summary: BatchResetAlarm
                description: >-
                  <p>Resets one or more alarms. The alarms return to the
                  <code>NORMAL</code> state after you reset them.</p>
                tags:
                  - Batches
                  - Reset
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
            /alarms/snooze:
              POST:
                summary: BatchSnoozeAlarm
                description: >-
                  <p>Changes one or more alarms to the snooze mode. The alarms
                  change to the <code>SNOOZE_DISABLED</code> state after you set
                  them to the snooze mode.</p>
                tags:
                  - Batches
                  - Snooze
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /detectors:
              POST:
                summary: BatchUpdateDetector
                description: >-
                  <p>Updates the state, variable values, and timer settings of
                  one or more detectors (instances) of a specified detector
                  model.</p>
                tags:
                  - Batches
                  - Update
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /alarms/{alarmModelName}/keyValues/:
              GET:
                summary: DescribeAlarm
                description: <p>Retrieves information about an alarm.</p>
                tags:
                  - Describe
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}/keyValues/:
              GET:
                summary: DescribeDetector
                description: >-
                  <p>Returns information about the specified detector
                  (instance).</p>
                tags:
                  - Describe
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /alarms/{alarmModelName}:
              GET:
                summary: ListAlarms
                description: >-
                  <p>Lists one or more alarms. The operation returns only the
                  metadata associated with each alarm.</p>
                tags:
                  - Lists
                  - Alarms
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}:
              GET:
                summary: ListDetectors
                description: <p>Lists detectors (the instances of a detector m
                tags:
                  - Lists
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Value
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents-data
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---