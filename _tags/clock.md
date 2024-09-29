---
name: Clock
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/clock.png
url: https://example.com/apis/clock.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Clock
apis:
  - name: simspaceweaver
    description: >-
      <p>SimSpace Weaver (SimSpace Weaver) is a service that you can use to
      build and run large-scale spatial simulations in the Amazon Web Services
      Cloud. For example, you can create crowd simulations, large real-world
      environments, and immersive and interactive experiences. For more
      information about SimSpace Weaver, see the <i> <a
      href="https://docs.aws.amazon.com/simspaceweaver/latest/userguide/">SimSpace
      Weaver User Guide</a> </i>.</p> <p>This API reference describes the API
      operations and data types that you can use to communicate directly with
      SimSpace Weaver.</p> <p>SimSpace Weaver also provides the SimSpace Weaver
      app SDK, which you use for app development. The SimSpace Weaver app SDK
      API reference is included in the SimSpace Weaver app SDK documentation.
      This documentation is part of the SimSpace Weaver app SDK distributable
      package.</p>
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
            title: simspaceweaver
          paths:
            /createsnapshot:
              POST:
                summary: CreateSnapshot
                description: >-
                  <p>Creates a snapshot of the specified simulation. A snapshot
                  is a file that contains simulation state data at a specific
                  time. The state data saved in a snapshot includes entity data
                  from the State Fabric, the simulation configuration specified
                  in the schema, and the clock tick number. You can use the
                  snapshot to initialize a new simulation. For more information
                  about snapshots, see <a
                  href="https://docs.aws.amazon.com/simspaceweaver/latest/userguide/working-with_snapshots.html">Snapshots</a>
                  in the <i>SimSpace Weaver User Guide</i>. </p> <p>You specify
                  a <code>Destination</code> when you create a snapshot. The
                  <code>Destination</code> is the name of an Amazon S3 bucket
                  and an optional <code>ObjectKeyPrefix</code>. The
                  <code>ObjectKeyPrefix</code> is usually the name of a folder
                  in the bucket. SimSpace Weaver creates a <code>snapshot</code>
                  folder inside the <code>Destination</code> and places the
                  snapshot file there.</p> <p>The snapshot file is an Amazon S3
                  object. It has an object key with the form: <code>
                  <i>object-key-prefix</i>/snapshot/<i>simulation-name</i>-<i>YYMMdd</i>-<i>HHmm</i>-<i>ss</i>.zip</code>,
                  where: </p> <ul> <li> <p> <code> <i>YY</i> </code> is the
                  2-digit year</p> </li> <li> <p> <code> <i>MM</i> </code> is
                  the 2-digit month</p> </li> <li> <p> <code> <i>dd</i> </code>
                  is the 2-digit day of the month</p> </li> <li> <p> <code>
                  <i>HH</i> </code> is the 2-digit hour (24-hour clock)</p>
                  </li> <li> <p> <code> <i>mm</i> </code> is the 2-digit
                  minutes</p> </li> <li> <p> <code> <i>ss</i> </code> is the
                  2-digit seconds</p> </li> </ul>
                tags:
                  - Create
                  - Snapshots
                  - Snapshots
            /deleteapp:
              DELETE:
                summary: DeleteApp
                description: <p>Deletes the instance of the given custom app.</p>
                tags:
                  - Delete
                  - Applications
                  - Snapshots
                  - Deleteapp
            /deletesimulation:
              DELETE:
                summary: DeleteSimulation
                description: >-
                  <p>Deletes all SimSpace Weaver resources assigned to the given
                  simulation.</p> <note> <p>Your simulation uses resources in
                  other Amazon Web Services. This API operation doesn't delete
                  resources in other Amazon Web Services.</p> </note>
                tags:
                  - Delete
                  - Simulations
                  - Snapshots
                  - Deleteapp
                  - Simulations
            /describeapp:
              GET:
                summary: DescribeApp
                description: <p>Returns the state of the given custom app.</p>
                tags:
                  - Describe
                  - Applications
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
            /describesimulation:
              GET:
                summary: DescribeSimulation
                description: <p>Returns the current state of the given simulation.</p>
                tags:
                  - Describe
                  - Simulations
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
            /listapps:
              GET:
                summary: ListApps
                description: >-
                  <p>Lists all custom apps or service apps for the given
                  simulation and domain.</p>
                tags:
                  - Lists
                  - Applications
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
            /listsimulations:
              GET:
                summary: ListSimulations
                description: >-
                  <p>Lists the SimSpace Weaver simulations in the Amazon Web
                  Services account used to make the API call.</p>
                tags:
                  - Lists
                  - Simulations
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes tags from a SimSpace Weaver resource. For more
                  information about tags, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html">Tagging
                  Amazon Web Services resources</a> in the <i>Amazon Web
                  Services General Reference</i>.</p>
                tags:
                  - Untag
                  - Resources
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
            /startapp:
              POST:
                summary: StartApp
                description: >-
                  <p>Starts a custom app with the configuration specified in the
                  simulation schema.</p>
                tags:
                  - Start
                  - Applications
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
            /startclock:
              POST:
                summary: StartClock
                description: <p>Starts the simulation clock.</p>
                tags:
                  - Start
                  - Clock
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
                  - Start Clock
            /startsimulation:
              POST:
                summary: StartSimulation
                description: >-
                  <p>Starts a simulation with the given name. You must choose to
                  start your simulation from a schema or from a snapshot. For
                  more information about the schema, see the <a
                  href="https://docs.aws.amazon.com/simspaceweaver/latest/userguide/schema-reference.html">schema
                  reference</a> in the <i>SimSpace Weaver User Guide</i>. For
                  more information about snapshots, see <a
                  href="https://docs.aws.amazon.com/simspaceweaver/latest/userguide/working-with_snapshots.html">Snapshots</a>
                  in the <i>SimSpace Weaver User Guide</i>.</p>
                tags:
                  - Start
                  - Simulations
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
                  - Start Clock
                  - Start Simulation
            /stopapp:
              POST:
                summary: StopApp
                description: >-
                  <p>Stops the given custom app and shuts down all of its
                  allocated compute resources.</p>
                tags:
                  - Stop
                  - Applications
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
                  - Start Clock
                  - Start Simulation
                  - Stop APplication
            /stopclock:
              POST:
                summary: StopClock
                description: <p>Stops the simulation clock.</p>
                tags:
                  - Stop
                  - Clock
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
                  - Start Clock
                  - Start Simulation
                  - Stop APplication
                  - Stop Clock
            /stopsimulation:
              POST:
                summary: StopSimulation
                description: >-
                  <p>Stops the given simulation.</p> <important> <p>You can't
                  restart a simulation after you stop it. If you want to restart
                  a simulation, then you must stop it, delete it, and start a
                  new instance of it.</p> </
                tags:
                  - Stop
                  - Simulations
                  - Snapshots
                  - Deleteapp
                  - Simulations
                  - Describeapp
                  - Simulations
                  - Applications
                  - Simulations
                  - Resources
                  - ARN
                  - Start Application
                  - Start Clock
                  - Start Simulation
                  - Stop APplication
                  - Stop Clock
                  - Stopsimulati
    overlays:
      - type: APIs.io Search
        url: overlays/simspaceweaver-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/simspaceweaver-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:simspaceweaver
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---