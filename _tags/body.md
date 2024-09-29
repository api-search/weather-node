---
name: Body
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/body.png
url: https://example.com/apis/body.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Body
apis:
  - name: robomaker
    description: >-
      <p>This section provides documentation for the AWS RoboMaker API
      operations.</p>
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
            title: robomaker
          paths:
            /batchDeleteWorlds:
              POST:
                summary: BatchDeleteWorlds
                description: <p>Deletes one or more worlds in a batch operation.</p>
                tags:
                  - Batches
                  - Delete
                  - Worlds
                  - Delete
                  - Worlds
            /batchDescribeSimulationJob:
              POST:
                summary: BatchDescribeSimulationJob
                description: <p>Describes one or more simulation jobs.</p>
                tags:
                  - Batches
                  - Describe
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
            /cancelDeploymentJob:
              POST:
                summary: CancelDeploymentJob
                description: >-
                  <p>Cancels the specified deployment job.</p> <important>
                  <p>This API will no longer be supported as of May 2, 2022. Use
                  it to remove resources that were created for Deployment
                  Service.</p> </important>
                tags:
                  - Cancel
                  - Deployments
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
            /cancelSimulationJob:
              POST:
                summary: CancelSimulationJob
                description: <p>Cancels the specified simulation job.</p>
                tags:
                  - Cancel
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
            /cancelSimulationJobBatch:
              POST:
                summary: CancelSimulationJobBatch
                description: >-
                  <p>Cancels a simulation job batch. When you cancel a
                  simulation job batch, you are also cancelling all of the
                  active simulation jobs created as part of the batch. </p>
                tags:
                  - Cancel
                  - Simulations
                  - Jobs
                  - Batches
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
            /cancelWorldExportJob:
              POST:
                summary: CancelWorldExportJob
                description: <p>Cancels the specified export job.</p>
                tags:
                  - Cancel
                  - Worlds
                  - Export
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
            /cancelWorldGenerationJob:
              POST:
                summary: CancelWorldGenerationJob
                description: <p>Cancels the specified world generator job.</p>
                tags:
                  - Cancel
                  - Worlds
                  - Generation
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
            /createDeploymentJob:
              POST:
                summary: CreateDeploymentJob
                description: >-
                  <p>Deploys a specific version of a robot application to robots
                  in a fleet.</p> <important> <p>This API is no longer supported
                  and will throw an error if used.</p> </important> <p>The robot
                  application must have a numbered
                  <code>applicationVersion</code> for consistency reasons. To
                  create a new version, use
                  <code>CreateRobotApplicationVersion</code> or see <a
                  href="https://docs.aws.amazon.com/robomaker/latest/dg/create-robot-application-version.html">Creating
                  a Robot Application Version</a>. </p> <note> <p>After 90 days,
                  deployment jobs expire and will be deleted. They will no
                  longer be accessible. </p> </note>
                tags:
                  - Create
                  - Deployments
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
            /createFleet:
              POST:
                summary: CreateFleet
                description: >-
                  <p>Creates a fleet, a logical group of robots running the same
                  robot application.</p> <important> <p>This API is no longer
                  supported and will throw an error if used.</p> </important>
                tags:
                  - Create
                  - Fleets
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
            /createRobot:
              POST:
                summary: CreateRobot
                description: >-
                  <p>Creates a robot.</p> <important> <p>This API is no longer
                  supported and will throw an error if used.</p> </important>
                tags:
                  - Create
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
            /createRobotApplication:
              POST:
                summary: CreateRobotApplication
                description: <p>Creates a robot application. </p>
                tags:
                  - Create
                  - Robots
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
            /createRobotApplicationVersion:
              POST:
                summary: CreateRobotApplicationVersion
                description: <p>Creates a version of a robot application.</p>
                tags:
                  - Create
                  - Robots
                  - Applications
                  - Versions
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createSimulationApplication:
              POST:
                summary: CreateSimulationApplication
                description: <p>Creates a simulation application.</p>
                tags:
                  - Create
                  - Simulations
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createSimulationApplicationVersion:
              POST:
                summary: CreateSimulationApplicationVersion
                description: >-
                  <p>Creates a simulation application with a specific revision
                  id.</p>
                tags:
                  - Create
                  - Simulations
                  - Applications
                  - Versions
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createSimulationJob:
              POST:
                summary: CreateSimulationJob
                description: >-
                  <p>Creates a simulation job.</p> <note> <p>After 90 days,
                  simulation jobs expire and will be deleted. They will no
                  longer be accessible. </p> </note>
                tags:
                  - Create
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createWorldExportJob:
              POST:
                summary: CreateWorldExportJob
                description: <p>Creates a world export job.</p>
                tags:
                  - Create
                  - Worlds
                  - Export
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createWorldGenerationJob:
              POST:
                summary: CreateWorldGenerationJob
                description: <p>Creates worlds using the specified template.</p>
                tags:
                  - Create
                  - Worlds
                  - Generation
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
            /createWorldTemplate:
              POST:
                summary: CreateWorldTemplate
                description: <p>Creates a world template.</p>
                tags:
                  - Create
                  - Worlds
                  - Templates
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deleteFleet:
              POST:
                summary: DeleteFleet
                description: >-
                  <p>Deletes a fleet.</p> <important> <p>This API will no longer
                  be supported as of May 2, 2022. Use it to remove resources
                  that were created for Deployment Service.</p> </important>
                tags:
                  - Delete
                  - Fleets
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deleteRobot:
              POST:
                summary: DeleteRobot
                description: >-
                  <p>Deletes a robot.</p> <important> <p>This API will no longer
                  be supported as of May 2, 2022. Use it to remove resources
                  that were created for Deployment Service.</p> </important>
                tags:
                  - Delete
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deleteRobotApplication:
              POST:
                summary: DeleteRobotApplication
                description: <p>Deletes a robot application.</p>
                tags:
                  - Delete
                  - Robots
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deleteSimulationApplication:
              POST:
                summary: DeleteSimulationApplication
                description: <p>Deletes a simulation application.</p>
                tags:
                  - Delete
                  - Simulations
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deleteWorldTemplate:
              POST:
                summary: DeleteWorldTemplate
                description: <p>Deletes a world template.</p>
                tags:
                  - Delete
                  - Worlds
                  - Templates
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /deregisterRobot:
              POST:
                summary: DeregisterRobot
                description: >-
                  <p>Deregisters a robot.</p> <important> <p>This API will no
                  longer be supported as of May 2, 2022. Use it to remove
                  resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Deregister
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeDeploymentJob:
              POST:
                summary: DescribeDeploymentJob
                description: >-
                  <p>Describes a deployment job.</p> <important> <p>This API
                  will no longer be supported as of May 2, 2022. Use it to
                  remove resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Describe
                  - Deployments
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeFleet:
              POST:
                summary: DescribeFleet
                description: >-
                  <p>Describes a fleet.</p> <important> <p>This API will no
                  longer be supported as of May 2, 2022. Use it to remove
                  resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Describe
                  - Fleets
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeRobot:
              POST:
                summary: DescribeRobot
                description: >-
                  <p>Describes a robot.</p> <important> <p>This API will no
                  longer be supported as of May 2, 2022. Use it to remove
                  resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Describe
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeRobotApplication:
              POST:
                summary: DescribeRobotApplication
                description: <p>Describes a robot application.</p>
                tags:
                  - Describe
                  - Robots
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeSimulationApplication:
              POST:
                summary: DescribeSimulationApplication
                description: <p>Describes a simulation application.</p>
                tags:
                  - Describe
                  - Simulations
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeSimulationJob:
              POST:
                summary: DescribeSimulationJob
                description: <p>Describes a simulation job.</p>
                tags:
                  - Describe
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeSimulationJobBatch:
              POST:
                summary: DescribeSimulationJobBatch
                description: <p>Describes a simulation job batch.</p>
                tags:
                  - Describe
                  - Simulations
                  - Jobs
                  - Batches
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeWorld:
              POST:
                summary: DescribeWorld
                description: <p>Describes a world.</p>
                tags:
                  - Describe
                  - Worlds
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeWorldExportJob:
              POST:
                summary: DescribeWorldExportJob
                description: <p>Describes a world export job.</p>
                tags:
                  - Describe
                  - Worlds
                  - Export
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeWorldGenerationJob:
              POST:
                summary: DescribeWorldGenerationJob
                description: <p>Describes a world generation job.</p>
                tags:
                  - Describe
                  - Worlds
                  - Generation
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /describeWorldTemplate:
              POST:
                summary: DescribeWorldTemplate
                description: <p>Describes a world template.</p>
                tags:
                  - Describe
                  - Worlds
                  - Templates
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
            /getWorldTemplateBody:
              POST:
                summary: GetWorldTemplateBody
                description: <p>Gets the world template body.</p>
                tags:
                  - Get
                  - Worlds
                  - Templates
                  - Body
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
            /listDeploymentJobs:
              POST:
                summary: ListDeploymentJobs
                description: >-
                  <p>Returns a list of deployment jobs for a fleet. You can
                  optionally provide filters to retrieve specific deployment
                  jobs.</p> <important> <p>This API will no longer be supported
                  as of May 2, 2022. Use it to remove resources that were
                  created for Deployment Service.</p> </important>
                tags:
                  - Lists
                  - Deployments
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
            /listFleets:
              POST:
                summary: ListFleets
                description: >-
                  <p>Returns a list of fleets. You can optionally provide
                  filters to retrieve specific fleets.</p> <important> <p>This
                  API will no longer be supported as of May 2, 2022. Use it to
                  remove resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Lists
                  - Fleets
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
            /listRobotApplications:
              POST:
                summary: ListRobotApplications
                description: >-
                  <p>Returns a list of robot application. You can optionally
                  provide filters to retrieve specific robot applications.</p>
                tags:
                  - Lists
                  - Robots
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
            /listRobots:
              POST:
                summary: ListRobots
                description: >-
                  <p>Returns a list of robots. You can optionally provide
                  filters to retrieve specific robots.</p> <important> <p>This
                  API will no longer be supported as of May 2, 2022. Use it to
                  remove resources that were created for Deployment Service.</p>
                  </important>
                tags:
                  - Lists
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
            /listSimulationApplications:
              POST:
                summary: ListSimulationApplications
                description: >-
                  <p>Returns a list of simulation applications. You can
                  optionally provide filters to retrieve specific simulation
                  applications. </p>
                tags:
                  - Lists
                  - Simulations
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
            /listSimulationJobBatches:
              POST:
                summary: ListSimulationJobBatches
                description: >-
                  <p>Returns a list simulation job batches. You can optionally
                  provide filters to retrieve specific simulation batch jobs.
                  </p>
                tags:
                  - Lists
                  - Simulations
                  - Jobs
                  - Batches
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
            /listSimulationJobs:
              POST:
                summary: ListSimulationJobs
                description: >-
                  <p>Returns a list of simulation jobs. You can optionally
                  provide filters to retrieve specific simulation jobs. </p>
                tags:
                  - Lists
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes the specified tags from the specified AWS RoboMaker
                  resource.</p> <p>To remove a tag, specify the tag key. To
                  change the tag value of an existing tag key, use <a
                  href="https://docs.aws.amazon.com/robomaker/latest/dg/API_TagResource.html">
                  <code>TagResource</code> </a>. </p>
                tags:
                  - Untag
                  - Resources
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
            /listWorldExportJobs:
              POST:
                summary: ListWorldExportJobs
                description: <p>Lists world export jobs.</p>
                tags:
                  - Lists
                  - Worlds
                  - Export
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
            /listWorldGenerationJobs:
              POST:
                summary: ListWorldGenerationJobs
                description: <p>Lists world generator jobs.</p>
                tags:
                  - Lists
                  - Worlds
                  - Generation
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
            /listWorldTemplates:
              POST:
                summary: ListWorldTemplates
                description: <p>Lists world templates.</p>
                tags:
                  - Lists
                  - Worlds
                  - Templates
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /listWorlds:
              POST:
                summary: ListWorlds
                description: <p>Lists worlds.</p>
                tags:
                  - Lists
                  - Worlds
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /registerRobot:
              POST:
                summary: RegisterRobot
                description: >-
                  <p>Registers a robot with a fleet.</p> <important> <p>This API
                  is no longer supported and will throw an error if used.</p>
                  </important>
                tags:
                  - Register
                  - Robots
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /restartSimulationJob:
              POST:
                summary: RestartSimulationJob
                description: <p>Restarts a running simulation job.</p>
                tags:
                  - Restart
                  - Simulations
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /startSimulationJobBatch:
              POST:
                summary: StartSimulationJobBatch
                description: >-
                  <p>Starts a new simulation job batch. The batch is defined
                  using one or more <code>SimulationJobRequest</code> objects.
                  </p>
                tags:
                  - Start
                  - Simulations
                  - Jobs
                  - Batches
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /syncDeploymentJob:
              POST:
                summary: SyncDeploymentJob
                description: >-
                  <p>Syncrhonizes robots in a fleet to the latest deployment.
                  This is helpful if robots were added after a deployment.</p>
                  <important> <p>This API will no longer be supported as of May
                  2, 2022. Use it to remove resources that were created for
                  Deployment Service.</p> </important>
                tags:
                  - Sync
                  - Deployments
                  - Jobs
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /updateRobotApplication:
              POST:
                summary: UpdateRobotApplication
                description: <p>Updates a robot application.</p>
                tags:
                  - Update
                  - Robots
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /updateSimulationApplication:
              POST:
                summary: UpdateSimulationApplication
                description: <p>Updates a simulation application.</p>
                tags:
                  - Update
                  - Simulations
                  - Applications
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
            /updateWorldTemplate:
              POST:
                summary: UpdateWorldTemplate
                description: <p>Updates a world tem
                tags:
                  - Update
                  - Worlds
                  - Templates
                  - Delete
                  - Worlds
                  - Describe
                  - Simulations
                  - Jobs
                  - Deployments
                  - Batches
                  - Worlds
                  - Export
                  - Generation
                  - Fleets
                  - Robots
                  - Applications
                  - Versions
                  - Templates
                  - Body
                  - Jobs
                  - Fleets
                  - Applications
                  - Robots
                  - Batches
                  - ARN
                  - Templates
    overlays:
      - type: APIs.io Search
        url: overlays/robomaker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/robomaker-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:robomaker
  - name: Confluence API
    description: >-
      This is the reference for the Confluence Cloud REST API. This API is the
      primary way to get and modify data in Confluence Cloud, whether you are
      developing an app or any other integration. Use it to interact with
      Confluence entities, like pages and blog posts, spaces, users, groups, and
      more.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: The Confluence Cloud REST API
          externalDocs:
            description: >-
              The online and complete version of the Confluence Cloud REST API
              docs.
            url: https://developer.atlassian.com/cloud/confluence/rest/
          tags:
            - name: Audit
              description: ''
            - name: Analytics
              description: ''
            - name: Content
              description: ''
            - name: Content - attachments
              description: ''
            - name: Content body
              description: ''
            - name: Content - children and descendants
              description: ''
            - name: Content - macro body
              description: ''
            - name: Content comments
              description: ''
            - name: Content labels
              description: ''
            - name: Content permissions
              description: ''
            - name: Content properties
              description: ''
            - name: Content restrictions
              description: ''
            - name: Content states
              description: ''
            - name: Content versions
              description: ''
            - name: Content watches
              description: ''
            - name: Dynamic modules
              description: ''
            - name: Experimental
              description: >-
                APIs in this section can change without any prior deprecation
                notice.
            - name: Group
              description: >-
                **[WARNING](https://support.atlassian.com/user-management/docs/create-and-update-groups/)
                The standard Atlassian group names are default names only and
                can be edited or deleted.**  For example, an admin or Atlassian
                support could delete the default group jira-software-users or
                rename it to jsw-users at any point.
            - name: Inline tasks
              description: ''
            - name: Label info
              description: ''
            - name: Long-running task
              description: ''
            - name: Relation
              description: ''
            - name: Search
              description: ''
            - name: Settings
              description: ''
            - name: Space
              description: ''
            - name: Space permissions
              description: ''
            - name: Space properties
              description: ''
            - name: Space settings
              description: ''
            - name: Templates
              description: ''
            - name: Themes
              description: ''
            - name: Users
              description: ''
            - name: User properties
              description: ''
          paths:
            /wiki/rest/api/audit:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Get audit records
                description: >-
                  Returns all records in the audit log, optionally for a certain
                  date range.

                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              post:
                tags:
                  - Create
                  - Audit
                  - Record
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Create audit record
                description: >-
                  Creates a record in the audit log.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/export:
              get:
                tags:
                  - Export
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                summary: Export audit records
                description: >-
                  Exports audit records as a CSV file or ZIP file.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/retention:
              get:
                tags:
                  - Get
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Get retention period
                description: >-
                  Returns the retention period for records in the audit log. The
                  retention

                  period is how long an audit record is kept for, from creation
                  date until

                  it is deleted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              put:
                tags:
                  - Sets
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Set retention period
                description: >-
                  Sets the retention period for records in the audit log. The
                  retention period

                  can be set to a maximum of 1 year.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/since:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - For
                  - Time
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                summary: Get audit records for time period
                description: >-
                  Returns records from the audit log, for a time period back
                  from the current

                  date. For example, you can use this method to get the last 3
                  months of records.


                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/content:
              get:
                tags:
                  - Get
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Get content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a Confluence instance.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
              post:
                tags:
                  - Create
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Create content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new piece of content or publishes an existing draft.


                  To publish a draft, add the `id` and `status` properties to
                  the body of the request.

                  Set the `id` to the ID of the draft and set the `status` to
                  'current'. When the

                  request is sent, a new piece of content will be created and
                  the metadata from the

                  draft will be transferred into it.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the

                  space that the content will be created in, and permission to
                  view the draft if publishing a draft.
            /wiki/rest/api/content/archive:
              post:
                tags:
                  - Archive
                  - Pages
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                summary: Archive pages
                description: >-
                  Archives a list of pages. The pages to be archived are
                  specified as a list of content IDs.

                  This API accepts the archival request and returns a task ID.

                  The archival process happens asynchronously.

                  Use the /longtask/<taskId> REST API to get the copy task
                  status.


                  Each content ID needs to resolve to page objects that are not
                  already in an archived state.

                  The content IDs need not belong to the same space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Archive' permission for each of the pages in the
                  corresponding space it belongs to.
            /wiki/rest/api/content/blueprint/instance/{draftId}:
              put:
                tags:
                  - Publish
                  - Shared
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish shared draft
                description: >-
                  Publishes a shared draft of a page created from a blueprint.


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
              post:
                tags:
                  - Publish
                  - Legacy
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish legacy draft
                description: >-
                  Publishes a legacy draft of a page created from a blueprint.
                  Legacy drafts

                  will eventually be removed in favor of shared drafts. For now,
                  this method

                  works the same as [Publish shared
                  draft](#api-content-blueprint-instance-draftId-put).


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
            /wiki/rest/api/content/search:
              get:
                tags:
                  - Search
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Search content by CQL
                description: >-
                  Returns the list of content that matches a Confluence Query
                  Language

                  (CQL) query. For information on CQL, see:

                  [Advanced searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Example initial call:

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.

                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
            /wiki/rest/api/content/{id}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Get content by ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a single piece of content, like a page or a blog post.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Update
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Update content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a piece of content. Use this method to update the
                  title or body

                  of a piece of content, change the status, change the parent
                  page, and more.


                  Note, updating draft content is currently not supported.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Delete content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Moves a piece of content to the space's trash or purges it
                  from the trash,

                  depending on the content's type and status:


                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `current`,

                  it will be trashed.

                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `trashed`,

                  the content will be purged from the trash and deleted
                  permanently. Note,

                  you must also set the `status` query parameter to `trashed` in
                  your request.

                  - If the content's type is `comment`, it will be deleted

                  permanently without being trashed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/pageTree:
              delete:
                tags:
                  - Delete
                  - Page
                  - Trees
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                summary: Delete page tree
                description: >-
                  Moves a pagetree rooted at a page to the space's trash:


                  - If the content's type is `page` and its status is `current`,
                  it will be trashed including

                  all its descendants.

                  - For every other combination of content type and status, this
                  API is not supported.


                  This API accepts the pageTree delete request and returns a
                  task ID.

                  The delete process happens asynchronously.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the `/longtask/<taskId>` REST API to get the copy task status.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/child:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                summary: Get content children
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a map of the direct children of a piece of content. A
                  piece of content

                  has different types of child content, depending on its type.
                  These are

                  the default parent-child content type relationships:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Apps can override these default relationships. Apps can also
                  introduce

                  new content types that create new parent-child content
                  relationships.


                  Note, the map will always include all child content types that
                  are valid

                  for the content. However, if the content has no instances of a
                  child content

                  type, the map will contain an empty array for that child
                  content type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{pageId}/move/{position}/{targetId}:
              put:
                tags:
                  - Move
                  - Page
                  - To
                  - New
                  - Locations
                  - Relative
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                summary: Move a page to a new location relative to a target page
                description: >-
                  Move a page to a new location relative to a target page:


                  * `before` - move the page under the same parent as the
                  target, before the target in the list of children

                  * `after` - move the page under the same parent as the target,
                  after the target in the list of children

                  * `append` - move the page to be a child of the target


                  Caution: This API can move pages to the top level of a space.
                  Top-level pages are difficult to find in the UI

                  because they do not show up in the page tree display. To avoid
                  this, never use `before` or `after` positions

                  when the `targetId` is a top-level page.
            /wiki/rest/api/content/{id}/child/attachment:
              get:
                tags:
                  - Get
                  - Attachments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Get attachments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the attachments for a piece of content.


                  By default, the following objects are expanded: `metadata`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create or update attachment
                description: >-
                  Adds an attachment to a piece of content. If the attachment
                  already exists

                  for the content, then the attachment is updated (i.e. a new
                  version of the

                  attachment is created).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a piece of

                  content (id='123') with a comment and `minorEdits`=true. If
                  the 'example.txt'

                  file already exists, it will update it with a new version of
                  the attachment.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X PUT \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create attachment
                description: >-
                  Adds an attachment to a piece of content. This method only
                  adds a new

                  attachment. If you want to update an existing attachment, use

                  [Create or update
                  attachments](#api-content-id-child-attachment-put).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a container

                  (id='123') with a comment and `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}:
              put:
                tags:
                  - Update
                  - Attachment
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Update attachment properties
                description: >-
                  Updates the attachment properties, i.e. the non-binary data of
                  an attachment

                  like the filename, media-type, comment, and parent container.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/data:
              post:
                tags:
                  - Update
                  - Attachment
                  - Data
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                summary: Update attachment data
                description: >-
                  Updates the binary data of an attachment, given the attachment
                  ID, and

                  optionally the comment and the minor edit field.


                  This method is essentially the same as [Create or update
                  attachments](#api-content-id-child-attachment-put),

                  except that it matches the attachment ID rather than the name.


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command updates an attachment (id='att456')
                  that is attached

                  to a piece of content (id='123') with a comment and
                  `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment/att456/data
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/download:
              get:
                tags:
                  - Get
                  - To
                  - Download
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                summary: Get URI to download attachment
                description: >-
                  Redirects the client to a URL that serves an attachment's
                  binary data.
            /wiki/rest/api/content/{id}/child/comment:
              get:
                tags:
                  - Get
                  - Content
                  - Comments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                summary: Get content comments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the comments on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/child/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                summary: Get content children by type
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all children of a given type, for a piece of content.

                  A piece of content has different types of child content,
                  depending on its type:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  Note, this method only returns direct children. To return
                  children at all

                  levels, use [Get descendants by
                  type](#api-content-id-descendant-type-get).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/descendant:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants
                description: >-
                  Returns a map of the descendants of a piece of content. This
                  is similar

                  to [Get content children](#api-content-id-child-get), except
                  that this

                  method returns child pages at all levels, rather than just the
                  direct

                  child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  The map will always include all descendant types that are
                  valid for the content.

                  However, if the content has no instances of a descendant type,
                  the map will

                  contain an empty array for that descendant type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/descendant/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants by type
                description: >-
                  Returns all descendants of a given type, for a piece of
                  content. This is

                  similar to [Get content children by
                  type](#api-content-id-child-type-get),

                  except that this method returns child pages at all levels,
                  rather than just

                  the direct child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/history:
              get:
                tags:
                  - Get
                  - Content
                  - History
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get content history
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the most recent update for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: Permission to view the content.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get macro body by macro ID
                description: >-
                  Returns the body of a macro in storage format, for the given
                  macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters. This method is mainly used by Cloud
                  apps.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - The
                  - Representation
                  - Synchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                summary: >-
                  Get macro body by macro ID and convert the representation
                  synchronously
                description: >-
                  Returns the body of a macro in format specified in path, for
                  the given macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/async/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - Representation
                  - Asynchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                summary: >-
                  Get macro body by macro ID and convert representation
                  Asynchronously
                description: >-
                  Returns Async Id of the conversion task which will convert the
                  macro into a content body of the desired format.

                  The result will be available for 5 minutes after completion of
                  the conversion.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/label:
              get:
                tags:
                  - Get
                  - Labels
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Get labels for content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the labels on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Add labels to content
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Using
                  - Queries
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content using query parameter
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from
                  content](#api-content-id-label-label-delete)

                  except that the label name is specified via a query parameter.


                  Use this method if the label name has "/" characters, as

                  [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  does not accept "/" characters for the label name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/label/{label}:
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  except that the label name is specified via a path parameter.


                  Use this method if the label name does not have "/"
                  characters, as the path

                  parameter does not accept "/" characters for security reasons.
                  Otherwise,

                  use [Remove label from content using query
                  parameter](#api-content-id-label-delete).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/notification/child-created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for page
                description: >-
                  Returns the watches for a page. A user that watches a page
                  will receive

                  receive notifications when the page is updated.


                  If you want to manage watches for a page, use the following
                  `user` methods:


                  - [Get content watch status for
                  user](#api-user-watch-content-contentId-get)

                  - [Add content watch](#api-user-watch-content-contentId-post)

                  - [Remove content
                  watch](#api-user-watch-content-contentId-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/notification/created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for space
                description: >-
                  Returns all space watches for the space that the content is
                  in. A user that

                  watches a space will receive receive notifications when any
                  content in the

                  space is updated.


                  If you want to manage watches for a space, use the following
                  `user` methods:


                  - [Get space watch status for
                  user](#api-user-watch-space-spaceKey-get)

                  - [Add space watch](#api-user-watch-space-spaceKey-post)

                  - [Remove space watch](#api-user-watch-space-spaceKey-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/pagehierarchy/copy:
              post:
                tags:
                  - Copy
                  - Page
                  - Hierarchy
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy page hierarchy
                description: >-
                  Copy page hierarchy allows the copying of an entire hierarchy
                  of pages and their associated properties, permissions and
                  attachments.
                   The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.
                   The titleOptions object defines the rules of renaming page titles during the copy;
                   for example, search and replace can be used in conjunction to rewrite the copied page titles.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the /longtask/<taskId> REST API to get the copy task status.
            /wiki/rest/api/content/{id}/copy:
              post:
                tags:
                  - Copy
                  - Single
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy single page
                description: >-
                  Copies a single page and its associated properties,
                  permissions, attachments, and custom contents.
                   The `id` path parameter refers to the content ID of the page to copy. The target of the page to be copied
                   is defined using the `destination` in the request body and can be one of the following types.

                    - `space`: page will be copied to the specified space as a root page on the space
                    - `parent_page`: page will be copied as a child of the specified parent page
                    - `existing_page`: page will be copied and replace the specified page

                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the space that the content
                  will be copied in and permission to update the content if
                  copying to an `existing_page`.
            /wiki/rest/api/content/{id}/permission/check:
              post:
                tags:
                  - Checks
                  - Content
                  - Permissions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                summary: Check content permissions
                description: >-
                  Check if a user or a group can perform an operation to the
                  specified content. The `operation` to check

                  must be provided. The user’s account ID or the ID of the group
                  can be provided in the `subject` to check

                  permissions against a specified user or group. The following
                  permission checks are done to make sure that the

                  user or group has the proper access:


                  - site permissions

                  - space permissions

                  - content restrictions


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission) if checking permission for self,

                  otherwise 'Confluence Administrator' global permission is
                  required.
            /wiki/rest/api/content/{id}/property:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Get content properties
                description: >-
                  Returns the properties for a piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Create content property
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content property for
                  key](#api-content-id-property-key-post)

                  except that the key is specified in the request body instead
                  of as a

                  path parameter.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/property/{key}:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Get content property
                description: >-
                  Returns a content property for a piece of content. For more
                  information, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              put:
                tags:
                  - Update
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Update content property
                description: >-
                  Updates an existing content property. This method will also
                  create a new

                  property for a piece of content, if the property key does not
                  exist and

                  the property version is 1. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Create content property for key
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content
                  property](#api-content-id-property-post)

                  except that the key is specified as a path parameter instead
                  of in the

                  request body.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Delete content property
                description: >-
                  Deletes a content property. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/restriction:
              get:
                tags:
                  - Get
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Get restrictions
                description: >-
                  Returns the restrictions on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Update
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Update restrictions
                description: >-
                  Updates restrictions for a piece of content. For each
                  operation specified in the request, it removes

                  any existing restrictions on the content for that operation,
                  and replaces them with the restrictions in the request.

                  Note: Not specifying an operation will ignore restrictions of
                  that type, and passing an empty list for an operation

                  will remove all existing restrictions of that type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              post:
                tags:
                  - Add
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Add restrictions
                description: >-
                  Adds restrictions to a piece of content. Note, this does not
                  change any

                  existing restrictions on the content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Delete
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Delete restrictions
                description: >-
                  Removes all restrictions (read and update) on a piece of
                  content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation:
              get:
                tags:
                  - Get
                  - Restrictions
                  - By
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions by operation
                description: >-
                  Returns restrictions on a piece of content by operation. This
                  method is

                  similar to [Get restrictions](#api-content-id-restriction-get)
                  except that

                  the operations are properties of the return object, rather
                  than items in

                  a results array.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}:
              get:
                tags:
                  - Get
                  - Restrictions
                  - For
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions for operation
                description: >-
                  Returns the restictions on a piece of content for a given
                  operation (read

                  or update).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/group/{groupName}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Get content restriction status for group
                description: >-
                  Deprecated, use [Get content restriction status for group via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-get).

                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `admins` group,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Add group to content restriction
                description: >-
                  Deprecated, use [Add group to content restriction via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-put).

                  Adds a group to a content restriction. That is, grant read or
                  update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Remove group from content restriction
                description: >-
                  Deprecated, use [Remove group from content restriction by
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-user-delete).

                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/byGroupId/{groupId}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Get content restriction status for group
                description: >-
                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `123456` group id,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/byGroupId/123456`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Add group to content restriction
                description: >-
                  Adds a group to a content restriction by Group Id. That is,
                  grant read or update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Remove group from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/user:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Get content restriction status for user
                description: >-
                  Returns whether the specified content restriction applies to a
                  user.

                  For example, if a page with `id=123` has a `read` restriction
                  for a user with an account ID of

                  `384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`, the following
                  request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/user?accountId=384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`


                  Note that a response of `true` does not guarantee that the
                  user can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Users
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Add user to content restriction
                description: >-
                  Adds a user to a content restriction. That is, grant read or
                  update

                  permission to the user for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Users
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Remove user from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: Get content state
                description: >-
                  Gets the current content state of the draft or current version
                  of content. To specify the draft version, set

                  the parameter status to draft, otherwise archived or current
                  will get the relevant published state.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Sets
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Set the content state of a content and publishes a new version
                  of the content.
                description: >-
                  Sets the content state of the content specified and creates a
                  new version

                  (publishes the content without changing the body) of the
                  content with the new state.


                  You may pass in either an id of a state, or the name and color
                  of a desired new state.

                  If all 3 are passed in, id will be used.

                  If the name and color passed in already exist under the
                  current user's existing custom states, the existing state will
                  be reused.

                  If custom states are disabled in the space of the content
                  (which can be determined by getting the content state space
                  settings of the content's space)

                  then this set will fail.


                  You may not remove a content state via this PUT request. You
                  must use the DELETE method. A specified state is required in
                  the body of this request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Removes the content state of a content and publishes a new
                  version.
                description: >-
                  Removes the content state of the content specified and creates
                  a new version

                  (publishes the content without changing the body) of the
                  content with the new status.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state/available:
              get:
                tags:
                  - Gets
                  - Available
                  - Content
                  - States
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                summary: Gets available content states for content.
                description: >-
                  Gets content states that are available for the content to be
                  set as.

                  Will return all enabled Space Content States.

                  Will only return most the 3 most recently published custom
                  content states to match UI editor list.

                  To get all custom content states, use the /content-states
                  endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/version:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Get content versions
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the versions for a piece of content in descending
                  order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              post:
                tags:
                  - Restore
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Restore content version
                description: >-
                  Restores a historical version to be the latest version. That
                  is, a new version

                  is created with the content of the historical version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/version/{versionNumber}:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Get content version
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a version for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              delete:
                tags:
                  - Delete
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Delete content version
                description: >-
                  Delete a historical version. This does not delete the changes
                  made to the

                  content in that version, rather the changes for the deleted
                  version are

                  rolled up into the next version. Note, you cannot delete the
                  current version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content-states:
              put:
                tags:
                  - Bulk
                  - Sets
                  - Content
                  - States
                  - Of
                  - Many
                  - Contents
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Bulk set content state of many contents
                description: >-
                  Creates a long running task that sets content state of draft
                  or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state set
                  via this endpoint.
              get:
                tags:
                  - Get
                  - Custom
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Get Custom Content States
                description: >-
                  Get custom content states that authenticated user has created.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have user authentication.
            /wiki/rest/api/content-states/delete:
              post:
                tags:
                  - Bulk
                  - Removes
                  - Content
                  - States
                  - From
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Bulk remove content states from content
                description: >-
                  Creates a long running task that Removes content state from
                  draft or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state
                  removed via this endpoint.
            /wiki/rest/api/content-states/task/{taskId}:
              get:
                tags:
                  - Get
                  - Update
                  - 'On'
                  - Long
                  - Running
                  - Tasks
                  - For
                  - Settings
                  - Of
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Get update on long running task for setting of content state.
                description: >-
                  Get Status of long running task that was previously created to
                  set or remove content states from content.

                  User must first create a task by passing in details to
                  /wiki/rest/api/content-states PUT or DELETE endpoints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have created long running task
            /wiki/rest/api/contentbody/convert/{to}:
              post:
                tags:
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Convert content body
                description: >-
                  Converts a content body from one format to another format.


                  Supported conversions:


                  - storage: view, export_view, styled_view, editor

                  - editor: storage

                  - view: none

                  - export_view: none

                  - styled_view: none


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{to}:
              post:
                tags:
                  - Asynchronously
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Asynchronously convert content body
                description: >-
                  Converts a content body from one format to another format
                  asynchronously.

                  Returns the asyncId for the asynchronous task.


                  Supported conversions:


                  - storage: export_view


                  No other conversions are supported at the moment.

                  Once a conversion is completed, it will be available for 5
                  minutes at the result endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{id}:
              get:
                tags:
                  - Get
                  - Asynchronously
                  - Converted
                  - Content
                  - Body
                  - From
                  - The
                  - Identifiers
                  - Or
                  - Current
                  - Status
                  - Of
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: >-
                  Get asynchronously converted content body from the id or the
                  current status of the task.
                description: >-
                  Returns the asynchronous content body for the corresponding id
                  if the task is complete 

                  or returns the status of the task.


                  After the task is completed, the result can be obtained for 5
                  minutes, or until an identical conversion request is made
                  again,

                  with allowCache query param set to false.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/inlinetasks/search:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Search
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                summary: Get inline tasks based on search parameters
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline tasks based on the search query.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only tasks

                  in contents that the user has permission to view are returned.
            /wiki/rest/api/inlinetasks/{inlineTaskId}:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get inline task based on global ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline task based on the global ID.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content associated with the task.
              put:
                tags:
                  - Update
                  - Inline
                  - Tasks
                  - Given
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Update inline task given global ID
                description: >-
                  Updates an inline tasks status given its global ID


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content associated with the task.
            /wiki/rest/api/label:
              get:
                tags:
                  - Get
                  - Labels
                  - Information
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get label information
                description: >-
                  Returns label information and a list of contents associated
                  with the label.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only contents

                  that the user is permitted to view is returned.
            /wiki/rest/api/group:
              get:
                tags:
                  - Get
                  - Groups
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get groups
                description: >-
                  Returns all user groups. The returned groups are ordered
                  alphabetically in

                  ascending order by group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - New
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Create new user group
                description: >-
                  Creates a new user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/by-name:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/by-id:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group id.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupName}:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/{groupName}/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/picker:
              get:
                tags:
                  - Search
                  - Groups
                  - By
                  - Partial
                  - Queries
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Search groups by partial query
                description: Get search results of groups by partial query provided.
            /wiki/rest/api/group/userByGroupId:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - By
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Add member to group by groupId
                description: >-
                  Adds a user as a member in a group represented by its groupId


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Using
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Remove member from group using group id
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupId}/membersByGroupId:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/user:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Add member to group
                description: >-
                  Adds a user as a member in a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Remove member from group
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/longtask:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running tasks
                description: >-
                  Returns information about all active long-running tasks (e.g.
                  space export),

                  such as how long each task has been running and the percentage
                  of each task

                  that has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/longtask/{id}:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running task
                description: >-
                  Returns information about an active long-running task (e.g.
                  space export),

                  such as how long it has been running and the percentage of the
                  task that

                  has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}:
              get:
                tags:
                  - Find
                  - Target
                  - Entities
                  - Related
                  - To
                  - Source
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find target entities related to a source entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all content that the
                  current user

                  has an 'ignore' relationship with:

                  `GET
                  /wiki/rest/api/relation/ignore/from/user/current/to/content`

                  Note, 'ignore' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}/{targetKey}:
              get:
                tags:
                  - Find
                  - Relationships
                  - From
                  - Source
                  - To
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find relationship from source to target
                description: >-
                  Find whether a particular type of relationship exists from a
                  source

                  entity to a target entity. Note, relationships are one way.


                  For example, you can use this method to find whether the
                  current user has

                  selected a particular page as a favorite (i.e. 'save for
                  later'):

                  `GET
                  /wiki/rest/api/relation/favourite/from/user/current/to/content/123`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
              put:
                tags:
                  - Create
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Create relationship
                description: >-
                  Creates a relationship between two entities (user, space,
                  content). The

                  'favourite' relationship is supported by default, but you can
                  use this method

                  to create any type of relationship between two entities.


                  For example, the following method creates a 'sibling'
                  relationship between

                  two pieces of content:

                  `GET
                  /wiki/rest/api/relation/sibling/from/content/123/to/content/456`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Delete relationship
                description: >-
                  Deletes a relationship between two entities (user, space,
                  content).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  For favourite relationships, the current user can only delete
                  their own

                  favourite relationships. A space administrator can delete
                  favourite

                  relationships for any user.
            /wiki/rest/api/relation/{relationName}/to/{targetType}/{targetKey}/from/{sourceType}:
              get:
                tags:
                  - Find
                  - Source
                  - Entities
                  - Related
                  - To
                  - Target
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find source entities related to a target entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all users that have a
                  'collaborator'

                  relationship to a piece of content with an ID of '1234':

                  `GET
                  /wiki/rest/api/relation/collaborator/to/content/1234/from/user`

                  Note, 'collaborator' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/search:
              get:
                tags:
                  - Search
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search content
                description: >-
                  Searches for content using the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  **Note that CQL input queries submitted through the
                  `/wiki/rest/api/search` endpoint no longer support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.** 

                  See this [deprecation
                  notice](https://developer.atlassian.com/cloud/confluence/deprecation-notice-search-api/)
                  for more details.


                  Example initial call:

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.


                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the entities. Note, only entities that the
                  user has

                  permission to view will be returned.
            /wiki/rest/api/search/user:
              get:
                tags:
                  - Search
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search users
                description: >-
                  Searches for users using user-specific queries from the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Note that CQL input queries submitted through the
                  `/wiki/rest/api/search/user` endpoint only support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.


                  Note that some user fields may be set to null depending on the
                  user's privacy settings.

                  These are: email, profilePicture, displayName, and timeZone.
            /wiki/rest/api/settings/lookandfeel:
              get:
                tags:
                  - Get
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Get look and feel settings
                description: >-
                  Returns the look and feel settings for the site or a single
                  space. This

                  includes attributes such as the color scheme, padding, and
                  border radius.


                  The look and feel settings for a space can be inherited from
                  the global

                  look and feel settings or provided by a theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  None
              put:
                tags:
                  - Select
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Select look and feel settings
                description: >-
                  Sets the look and feel settings to the default (global)
                  settings, the

                  custom settings, or the current theme's settings for a space.

                  The custom and theme settings can only be selected if there is
                  already

                  a theme set for a space. Note, the default space settings are
                  inherited

                  from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/custom:
              post:
                tags:
                  - Update
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Update look and feel settings
                description: >-
                  Updates the look and feel settings for the site or for a
                  single space.

                  If custom settings exist, they are updated. If no custom
                  settings exist,

                  then a set of custom settings is created.


                  Note, if a theme is selected for a space, the space look and
                  feel settings

                  are provided by the theme and cannot be overridden.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Reset look and feel settings
                description: >-
                  Resets the custom look and feel settings for the site or a
                  single space.

                  This changes the values of the custom settings to be the same
                  as the

                  default settings. It does not change which settings (default
                  or custom)

                  are selected. Note, the default space settings are inherited
                  from the

                  current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/selected:
              put:
                tags:
                  - Sets
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                summary: Set look and feel settings
                description: >-
                  Sets the look and feel settings to either the default settings
                  or the

                  custom settings, for the site or a single space. Note, the
                  default

                  space settings are inherited from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/systemInfo:
              get:
                tags:
                  - Get
                  - Systems
                  - Info
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                summary: Get system info
                description: >-
                  Returns the system information for the Confluence Cloud
                  tenant. This

                  information is used by Atlassian.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/settings/theme:
              get:
                tags:
                  - Get
                  - Themes
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get themes
                description: >-
                  Returns all themes, not including the default theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/selected:
              get:
                tags:
                  - Get
                  - Global
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get global theme
                description: >-
                  Returns the globally assigned theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/{themeKey}:
              get:
                tags:
                  - Get
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get theme
                description: >-
                  Returns a theme. This includes information about the theme
                  name,

                  description, and icon.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/space:
              get:
                tags:
                  - Get
                  - Spaces
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Get spaces
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all spaces. The returned spaces are ordered
                  alphabetically in

                  ascending order by space key.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Note, the returned list will only contain spaces that the
                  current user

                  has permission to view.
              post:
                tags:
                  - Create
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Create space
                description: >-
                  Creates a new space. Note, currently you cannot set space
                  labels when

                  creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/_private:
              post:
                tags:
                  - Create
                  - Private
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create private space
                description: >-
                  Creates a new space that is only visible to the creator. This
                  method is

                  the same as the [Create space](#api-space-post) method with
                  permissions

                  set to the current user only. Note, currently you cannot set
                  space

                  labels when creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space. This includes information like the name,
                  description,

                  and permissions, but not the content in the space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space
                description: >-
                  Updates the name, description, or homepage of a space.


                  -   For security reasons, permissions cannot be updated via
                  the API and

                  must be changed via the user interface instead.

                  -   Currently you cannot set space labels when updating a
                  space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space
                description: >-
                  Deletes a space. Note, the space will be deleted in a long
                  running task.

                  Therefore, the space may not be deleted yet when this method
                  has

                  returned. Clients should poll the status link that is returned
                  in the

                  response until the task completes.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content:
              get:
                tags:
                  - Get
                  - Content
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a space. The returned content is
                  grouped by type

                  (pages then blogposts), then ordered by content ID in
                  ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/permission:
              post:
                tags:
                  - Add
                  - New
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new permission to space
                description: >-
                  Adds new permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/custom-content:
              post:
                tags:
                  - Add
                  - New
                  - Custom
                  - Content
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new custom content permission to space
                description: >-
                  Adds new custom content permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Only apps can access this REST resource and only make
                  changes to the respective app permissions.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/{id}:
              delete:
                tags:
                  - Removes
                  - Space
                  - Permission
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Remove a space permission
                description: >-
                  Removes a space permission. Note that removing Read Space
                  permission for a user or group will remove all

                  the space permissions for that user or group.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Types
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content by type for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content of a given type, in a space. The returned
                  content is

                  ordered by content ID in ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/property:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space properties
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all properties for the given space. Space properties
                  are a key-value storage associated with a space.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/property/{key}:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a space property. Note, you cannot update the key of a
                  space

                  property, only the value.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property for key
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property. This is the same as `POST

                  /wiki/rest/api/space/{spaceKey}/property` but the key for the
                  property is passed as a

                  path parameter, rather than in the request body.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Deletes a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/settings:
              get:
                tags:
                  - Get
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space settings
                description: >-
                  Returns the settings of a space. Currently only the

                  `routeOverrideEnabled` setting can be returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space settings
                description: >-
                  Updates the settings for a space. Currently only the

                  `routeOverrideEnabled` setting can be updated.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/state:
              get:
                tags:
                  - Get
                  - Space
                  - Suggested
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space suggested content states
                description: >-
                  Get content states that are suggested in the space.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space view permission
            /wiki/rest/api/space/{spaceKey}/state/settings:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Settings
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content state settings for space
                description: >-
                  Get object describing whether content states are allowed at
                  all, if custom content states or space content states

                  are restricted, and a list of space content states allowed for
                  the space if they are not restricted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space admin permission
            /wiki/rest/api/space/{spaceKey}/state/content:
              get:
                tags:
                  - Get
                  - Content
                  - In
                  - Space
                  - With
                  - Given
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content in space with given content state
                description: >-
                  Finds paginated content with 


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space View Permission
            /wiki/rest/api/space/{spaceKey}/theme:
              get:
                tags:
                  - Get
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space theme
                description: >-
                  Returns the theme selected for a space, if one is set. If no
                  space

                  theme is set, this means that the space is inheriting the
                  global look

                  and feel settings.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Sets
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Set space theme
                description: >-
                  Sets the theme for a space. Note, if you want to reset the
                  space theme to

                  the default Confluence theme, use the 'Reset space theme'
                  method instead

                  of this method.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Reset space theme
                description: >-
                  Resets the space theme. This means that the space will inherit
                  the

                  global look and feel settings


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/watch:
              get:
                tags:
                  - Get
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get space watchers
                description: Returns a list of watchers of a space
            /wiki/rest/api/space/{spaceKey}/label:
              get:
                tags:
                  - Get
                  - Space
                  - Labels
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get Space Labels
                description: >-
                  Returns a list of labels associated with a space. Can provide
                  a prefix as well as other filters to

                  select different types of labels.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Add labels to a space
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Remove label from a space
                description: ''
            /wiki/rest/api/template:
              put:
                tags:
                  - Update
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Update content template
                description: >-
                  Updates a content template. Note, blueprint templates cannot
                  be updated

                  via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to update a space template or
                  'Confluence Administrator'

                  global permission to update a global template.
              post:
                tags:
                  - Create
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Create content template
                description: >-
                  Creates a new content template. Note, blueprint templates
                  cannot be created via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to create a space template or
                  'Confluence Administrator'

                  global permission to create a global template.
            /wiki/rest/api/template/blueprint:
              get:
                tags:
                  - Get
                  - Blueprints
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                summary: Get blueprint templates
                description: >-
                  Returns all templates provided by blueprints. Use this method
                  to retrieve

                  all global blueprint templates or all blueprint templates in a
                  space.


                  Note, all global blueprints are inherited by each space. Space
                  blueprints

                  can be customised without affecting the global blueprints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view blueprints for the
                  space and permission

                  to access the Confluence site ('Can use' global permission) to
                  view global blueprints.
            /wiki/rest/api/template/page:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content templates
                description: >-
                  Returns all content templates. Use this method to retrieve all
                  global

                  content templates or all content templates in a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
            /wiki/rest/api/template/{contentTemplateId}:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content template
                description: >-
                  Returns a content template. This includes information about
                  template,

                  like the name, the space or blueprint that the template is in,
                  the body

                  of the template, and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
              delete:
                tags:
                  - Removes
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Remove template
                description: >-
                  Deletes a template. This results in different actions
                  depending on the

                  type of template:


                  - If the template is a content template, it is deleted.

                  - If the template is a modified space-level blueprint
                  template, it reverts

                  to the template inherited from the global-level blueprint
                  template.

                  - If the template is a modified global-level blueprint
                  template, it reverts

                  to the default global-level blueprint template.

                   Note, unmodified blueprint templates cannot be deleted.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:
                          'Admin' permission for the space to delete a space template or 'Confluence Administrator'
                          global permission to delete a global template.
            /wiki/rest/api/user:
              get:
                tags:
                  - Get
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get user
                description: >-
                  Returns a user. This includes information about the user, such
                  as the

                  display name, account ID, profile picture, and more. The
                  information returned may be

                  restricted by the user's profile visibility settings.


                  **Note:** to add, edit, or delete users in your organization,
                  see the

                  [user management REST
                  API](/cloud/admin/user-management/about/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/anonymous:
              get:
                tags:
                  - Get
                  - Anonymous
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                summary: Get anonymous user
                description: >-
                  Returns information about how anonymous users are represented,
                  like the

                  profile picture and display name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/current:
              get:
                tags:
                  - Get
                  - Current
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                summary: Get current user
                description: >-
                  Returns the currently logged-in user. This includes
                  information about

                  the user, like the display name, userKey, account ID, profile
                  picture,

                  and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/memberof:
              get:
                tags:
                  - Get
                  - Group
                  - Memberships
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                summary: Get group memberships for user
                description: >-
                  Returns the groups that a user is a member of.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/bulk:
              get:
                tags:
                  - Get
                  - Multiple
                  - Users
                  - Using
                  - Ids
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get multiple users using ids
                description: >-
                  Returns user details for the ids provided in request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/content/{contentId}:
              get:
                tags:
                  - Get
                  - Content
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get content watch status
                description: >-
                  Returns whether a user is watching a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add content watcher
                description: >-
                  Adds a user as a watcher to a piece of content. Choose the
                  user by doing

                  one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove content watcher
                description: >-
                  Removes a user as a watcher from a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/label/{labelName}:
              get:
                tags:
                  - Get
                  - Labels
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get label watch status
                description: >-
                  Returns whether a user is watching a label. Choose the user by
                  doing one

                  of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add label watcher
                description: >-
                  Adds a user as a watcher to a label. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove label watcher
                description: >-
                  Removes a user as a watcher from a label. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get space watch status
                description: >-
                  Returns whether a user is watching a space. Choose the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add space watcher
                description: >-
                  Adds a user as a watcher to a space. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Space
                  - Watch
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove space watch
                description: >-
                  Removes a user as a watcher from a space. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email address
                description: >-
                  Returns a user's email address. This API is only available to
                  apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email/bulk:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - In
                  - Batches
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email addresses in batch
                description: >-
                  Returns user email addresses for a set of accountIds. This API
                  is only available to apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  Any accounts which are not available will not be included in
                  the result.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /atlassian-connect/1/app/module/dynamic:
              get:
                tags:
                  - Get
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Get modules
                description: >-
                  Returns all modules registered dynamically by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              post:
                tags:
                  - Register
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Register modules
                description: >-
                  Registers a list of modules. For the list of modules that
                  support dynamic registration, see [Dynamic
                  modules](https://developer.atlassian.com/cloud/confluence/dynamic-modules/).


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              delete:
                tags:
                  - Removes
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Remove modules
                description: >-
                  Remove all or a list of modules registered by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
            /wiki/rest/api/analytics/content/{contentId}/views:
              get:
                tags:
                  - Get
                  - Views
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                summary: Get views
                description: Get the total number of views a piece of content has.
            /wiki/rest/api/analytics/content/{contentId}/viewers:
              get:
                tags:
                  - Get
                  - Viewers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get viewers
                description: >-
                  Get the total number of distinct viewers a piece of content
                  has.
            /wiki/rest/api/user/{userId}/property:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user properties
                description: >-
                  Returns the properties for a user as list of property keys.
                  For more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/{userId}/property/{key}:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user property
                description: >-
                  Returns the property corresponding to `key` for a user. For
                  more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              put:
                tags:
                  - Update
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Update user property
                description: >-
                  Updates a property for the given user. Note, you cannot update
                  the key of a user property, only the value.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - Users
                  - Properties
                  - By
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Create user property by key
                description: >-
                  Creates a property for a user. For more information  about
                  user properties, see [Confluence entity properties]

                  (https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  `Note:` the number of properties which could be created per
                  app in a tenant for each user might be

                  restricted by fixed system limits.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Delete user property
                description: >-
                  Deletes a property for the given user.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
          x-atlassian-narrative:
            documents:
              - title: About
                anchor: about
                body: >-
                  This is the reference for the Confluence Cloud REST API. This
                  API is the primary way to get and

                  modify data in Confluence Cloud, whether you are developing an
                  app or any other integration.

                  Use it to interact with Confluence entities, like pages and
                  blog posts, spaces, users, groups,

                  and more.
              - title: Authentication and authorization
                anchor: auth
                body: >-
                  **Authentication:** If you are building a Cloud app,
                  authentication is implemented via JWT or OAuth 2.0, depending
                  on what you are building (see [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)).
                  Otherwise, if you are authenticating directly against the REST
                  API, the REST API supports basic auth (see [Basic auth for
                  REST
                  APIs](https://developer.atlassian.com/cloud/confluence/basic-auth-for-rest-apis/)).


                  **Authorization:** If you are building a Cloud app,
                  authorization can be implemented by
                  [scopes](https://developer.atlassian.com/cloud/confluence/scopes/)
                  or by [OAuth 2.0 user
                  impersonation](https://developer.atlassian.com/cloud/confluence/oauth-2-jwt-bearer-tokens-for-apps).
                  Otherwise, if you are making calls directly against the REST
                  API, authorization is based on the user used in the
                  authentication process.


                  See [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)
                  for more details on authentication and authorization.
              - title: Status codes
                anchor: status-code
                body: >-
                  The Confluence REST API uses the [standard HTTP status
                  codes](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html).


                  Responses that return an error status code will also return a
                  response body, similar to the following:

                  ```json

                  {
                    "statusCode": 404,
                    "data": {
                      "authorized": false,
                      "valid": false,
                      "errors": [
                        {
                          "message": {
                            "translation": "This is an example error message.",
                            "args": []
                          }
                        }
                      ],
                      "successful": false
                    },
                    "message": "This is an example error message."
                  }

                  ```
              - title: Using the REST API
                anchor: using
                body: >-
                  **Expansion:** The Confluence REST API uses resource
                  expansion: some parts of a resource are not returned unless
                  explicitly specified. This simplifies responses and minimizes
                  network traffic.


                  To expand part of a resource in a request, use the `expand`
                  query parameter and specify the entities to be expanded. If
                  you need to expand nested entities, use the `.` dot notation.
                  For example, the following request will expand information
                  about the requested content's space and labels:

                  ```

                  GET /wiki/rest/api/content/{id}?expand=space,metadata.labels

                  ```

                  **Pagination:** The Confluence REST API uses pagination: a
                  method that returns a response with multiple objects can only
                  return a limited number at one time. This limits the size of
                  responses and conserves server resources.


                  Use the 'limit' and 'start' query parameters to specify
                  pagination:


                  - `limit` is the number of objects to return per page. This
                  may be restricted by system limits.

                  - `start` is the index of the first item returned in the page
                  of results. The base index is 0.


                  For example, the following request will return ten content
                  objects, starting from the fifth object.

                  ```

                  GET /wiki/rest/api/content?start=4&limit=10

                  ```

                  **Special headers:**


                  - `X-Atlassian-Token: no-check` request header must be
                  specified for methods

                  that are protected from Cross Site Request Forgery (XSRF/CSRF)
                  attacks. This is

                  stated in the method description, if required. For more
                  information, see this

                  [KB
                  article](https://confluence.atlassian.com/cloudkb/xsrf-check-failed-when-calling-cloud-apis-826874382.html).
              - title: Capabilities
                anchor: capabilities
                body: >-
                  **Webhooks:** A webhook is a user-defined callback over HTTP.
                  You can use Confluence webhooks to notify your app or web
                  application when certain events occur in Confluence. For
                  example, when a page is created or updated. To learn more, see
                  [Webhooks](https://developer.atlassian.com/cloud/confluence/modules/webhook/).


                  **Content properties:** Content properties are a key-value
                  storage associated with a piece of Confluence content. If you
                  are building an app, this is one form of persistence that you
                  can use. You can use the Confluence REST API to get, update,
                  and delete content properties. To learn more, see [Content
                  properties in the REST
                  API](https://developer.atlassian.com/cloud/confluence/content-properties/).


                  **CQL:** The Confluence Query Language (CQL) allows you to
                  perform complex searches for content using an SQL-like syntax
                  in the `search` resource. To learn more, see [Advanced
                  searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-
      - type: Postman Collection
        url: >-
          https://developer.atlassian.com/cloud/confluence/confcloud.1.postman.json
      - type: Authentication
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#auth
      - type: Status Codes
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#status-code
      - type: Capabilities
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#capabilities
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json?_v=1.6660.0-0.1294.0-openapi-search.yml
      - type: APIs.io Search
        url: overlays/confluence-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/confluence-openapi-api-evangelist-ratings.yml
    aid: atlassian:confluence-api
  - aid: box:box-workflows-api
    name: Box Workflows API
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.box.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.box.com/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Box Workflows API
          paths:
            /workflows:
              get:
                summary: List workflows
                tags:
                  - List
                  - Workflows
                  - Workflows
                description: >-
                  Returns list of workflows that act on a given `folder ID`, and

                  have a flow with a trigger type of `WORKFLOW_MANUAL_START`.


                  You application must be authorized to use the `Manage Box
                  Relay` application

                  scope within the developer console in to use this endpoint.
            /workflows/{workflow_id}/start:
              post:
                summary: Starts workflow based on request body
                tags:
                  - Starts
                  - Workflow
                  - Based
                  - 'On'
                  - Request
                  - Body
                  - Workflows
                  - Workflow_id
                  - Start
                description: >-
                  Initiates a flow with a trigger type of
                  `WORKFLOW_MANUAL_START`.


                  You application must be authorized to use the `Manage Box
                  Relay` application

                  scope within the develo
    overlays:
      - type: APIs.io Search
        url: overlays/workflows-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workflows-openapi-api-evangelist-ratings.yml
  - name: FactSet Analytics Datastore API
    description: >-
      Request pre-calculated Portfolio Analytics data saved in FactSet's
      Analytics Datastore, via deterministic URLs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/analytics-datastore-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Analytics Datastore API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            url: https://developer.factset.com/api-catalog/analytics-datastore-api
            description: API Documentation
          tags:
            - name: Mappings
              description: >-
                Retrieves a mapping with a Location header to redirect to the
                underlying data
            - name: Objects
              description: Retrieves Objects and their underlying data
            - name: Documents
              description: Retrieves Document metadata and URL locations to underlying data
          paths:
            /analytics/pub-datastore/swivel/v1/{document}/{accountId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Raw
                  - T/
                  - Output
                  - Created
                  - By
                  - Publisher
                  - Service.
                  - Id
                  - Date
                summary: >-
                  Redirects to the raw PPT/PDF output created by the Publisher
                  service.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - A/
                  - Data
                  - Represented
                  - In
                  - Stach
                  - Format,
                  - With
                  - 'No'
                  - As
                  - Of
                  - Date
                  - Specified.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                summary: >-
                  Redirects to the underlying PA/SPAR data represented in a
                  Stach format, with no as of date specified.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - A/
                  - Data
                  - Represented
                  - In
                  - Stach
                  - Format.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                summary: >-
                  Redirects to the underlying PA/SPAR data represented in a
                  Stach format.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}/{configId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - Insight/
                  - Vault
                  - Data
                  - In
                  - Stach
                  - Format.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                summary: >-
                  Redirects to the underlying Insight/Vault data in a Stach
                  format.
                description: "The inclusion of a configId in the path indicates this is for Insight/Vault mappings only, as PA/SPAR mappings do not support the concept of configuration id.\r\n\r\nTakes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/cargo/v1/groups/{groupId}/objects/{objectId}:
              get:
                tags:
                  - Gets
                  - An
                  - Object
                  - Given
                  - D.
                  - In
                  - This
                  - Case
                  - Retrieved
                  - From
                  - Mapping
                  - Location
                  - Header,
                  - Data
                  - Response
                  - Body.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                summary: >-
                  Gets an object given an ID. In this case ID retrieved from
                  mapping Location header, object data in response body.
                description: "Raw object data can be found in the response body. This can be either the mapped PDF/PPT or STACH json, depending on the mapping. https://pages.github.factset.com/analytics-reporting/stachschema/#/ \r\n\nOptional request header \"accept-encoding\", with allowed values of \"br\" and \"gzip\". If accept-encoding is passed, the response is compressed."
            /analytics/pub-datastore/tag-search/v1/documents/search:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Documents
                  - That
                  - User
                  - Has
                  - Access
                  - To.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                summary: Gets a list of Documents that a user has access to.
                description: "Retrieves metadata around documents stored in the Analytics Datastore Service. Each Document will have a 'url' property which will act as a re-direct to the underlying document data\r\n\r\nThis end point supports pagination and filtering through the use of the request body listed below.\r\n\r\nTo discover what tags are available to filter on, see GET /tags and GET /tags/{name}/values to retrieve these filter values.\r\n\r\nSimilarly, to discover what product types are available to filter on, see POST /product-types/search to retrieve a list of product types."
            /analytics/pub-datastore/tag-search/v1/tags:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Tag
                  - Definitions
                  - For
                  - The
                  - User.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                summary: Gets a list of tag definitions for the user.
                description: >-
                  Tag definitions consist of a name and a type. Use this end
                  point to see a list of pre-existing tags that can be used to
                  filter on the Documents end point.
            /analytics/pub-datastore/tag-search/v1/tags/{name}:
              get:
                tags:
                  - Get
                  - Single
                  - Tag
                  - Definition
                  - Based
                  - 'On'
                  - Its
                  - Name
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                summary: Get a single tag definition based on its name
                description: Retrieve a tag definition based on its name
            /analytics/pub-datastore/tag-search/v1/tags/{name}/values:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Tag
                  - Values
                  - For
                  - The
                  - Given
                  - Name
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                  - Values
                summary: Gets a list of tag values for the given name
                description: >-
                  Returns a list of tag values depending on the name provided.
                  Supports filtering on additional tag name value pairs, which
                  operates as an 'AND' where the Document must have the tag name
                  specified in the path AND the filtered parameter.
            /analytics/pub-datastore/tag-search/v1/product-types/search:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Product
                  - Types
                  - That
                  - User
                  - Has
                  - Access
                  - To.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                  - Values
                  - Product
                  - Types
                summary: Gets a list of product types that a user has access to.
                description: >-
                  Retrieves a list of product types that have been specified
                  across all documents th
    overlays:
      - type: APIs.io Search
        url: overlays/analytics-datastore-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/analytics-datastore-openapi-api-evangelist-ratings.yml
    aid: factset:factset-analytics-datastore-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---