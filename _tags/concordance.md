---
name: Concordance
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/concordance.png
url: https://example.com/apis/concordance.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Concordance
apis:
  - name: FactSet Concordance API
    description: >-
      The FactSet Concordance API helps our users discover the respective
      FactSet Entity & People identifier for a specific entity based off of a
      list of provided corresponding attributes, such as Names, URLs, and
      Location.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-concordance-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-concordance-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Concordance API
          tags:
            - name: Entity Match
              description: >-
                Retrieve a list of Entity Matches and Candidates for up to 25
                names.
            - name: Entity Match - Bulk
              description: >-
                Submit a file with a large list of entity names and attributes
                and retrieve decisions once mapped.
            - name: Universes
              description: Create, View, and Manage Universes where mappings are saved.
            - name: Mappings
              description: >-
                View all Saved Mappings in a Universe or update and save
                mappings made of ClientIds and Names to FactSet Entity Ids
            - name: Snowflake
              description: >-
                The response is formatted specifically for Snowflake environment
                and not used by consumers outside of Snowflake.
            - name: People Match
              description: Retrieve a list of People Matches.
            - name: People Mapping
              description: Used to save a single People Mapping to a given universe
          paths:
            /factset-concordance/v2/entity-match:
              get:
                summary: >-
                  Get Entity Candidates and Matches for a single name and
                  attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. Additional attributes can be supplied to narrow the
                  search, such as State, URL, and Entity Types. <p>**Max of 1
                  Name permitted in a single GET request.** Use the POST method
                  for /entity-match to fetch up to 25 names. Otherwise, use the
                  "Entity Match - Bulk" workflow to submit larger universes of
                  names to be concorded via a file.</p><p>
                tags:
                  - Get
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Single
                  - Name
                  - Attributes.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
              post:
                summary: >-
                  Get a list of Entity Candidates and Matches for a requested
                  list of up to 25 names and attributes.
                description: >
                  Finds the best candidate entities matching the given entity
                  name. If a `universeId` is provided, any match for an input
                  including a `clientId` will be saved to that universe.
                  Additional attributes can be supplied to narrow the search,
                  such as State, URL, and Entity Types. Finds the best candidate
                  entities matching the given company name. Additional
                  attributes can be supplied to narrow the search.  <p>**Max of
                  25 Names inputted.** Use the "Entity Match - Bulk" workflow to
                  submit larger universes of names to be concorded via a
                  file.</p><p> Supported types of Entities in which the names
                  can match to include -
                    * Corporations, Joint Ventures, and Holding Companies
                    * Fund Managers and various Fund Types (Open-end, Closed End, Hedge, Soverign Wealth, Pension, Exchange Traded, and more).</p>
                tags:
                  - Get
                  - List
                  - Of
                  - Entity
                  - Candidates
                  - And
                  - Matches
                  - For
                  - Requested
                  - Up
                  - To
                  - '25'
                  - Names
                  - Attributes.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
            /factset-concordance/v2/entity-task:
              post:
                summary: Input a file with names and attributes, creating a taskId.
                description: >
                  Upload a Comma-Separated List file (.csv / UTF-8 encoding)
                  with a list of names and attributes and receive a `taskId`.
                  The taskId is then used for reference in the
                  */entity-task-status* and */entity-decisions* endpoints to
                  receive results once the task is successful.<p>This is the
                  first step in the overall "Bulk" workflow. Use the
                  /entity-task-status endpoint to check the status.</p> <p> A
                  universeId must be included in request. If you do not have a
                  universe created, reference the `/universe` endpoint.
                tags:
                  - Input
                  - File
                  - With
                  - Names
                  - And
                  - Attributes,
                  - Creating
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
            /factset-concordance/v2/entity-task-status:
              get:
                summary: >-
                  Gets the status of the requested taskId or all tasks for a
                  User
                description: >
                  Pulls the **status** for ALL the Entity Tasks submitted by a
                  client within the last 30 days, and related details such as
                  task duration and decision rates. Specific Tasks can also be
                  retrieved by using the _taskId_ parameter.<p>Status types
                  include -
                    * PENDING - The task has not yet started.
                    * IN_PROGRESS - The task is submitted and decisions are in progress.
                    * SUCCESS - The task was successful! Move to the /entity-decisions endpoint to retrieve decisions.
                    * FAILURE - The task failed. Reach out to FactSet Support for assistance.
                    * BAD_REQUEST - The task creation was unsuccesfull. Typically occurs with an incorrect input file format or column headers.
                    * ABORTED - The task was aborted.
                tags:
                  - Gets
                  - The
                  - Status
                  - Of
                  - Requested
                  - Task
                  - Id
                  - Or
                  - All
                  - Tasks
                  - For
                  - User
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
            /factset-concordance/v2/entity-decisions:
              get:
                summary: Get the decisions of matches for the requested taskId.
                description: >
                  Retrieves the `Decision` objects for an Entity Task (taskId).
                  The decisions do not include all candidates, but rather the
                  results of concording the requested list of names included in
                  the input file. Mapped entities will include a FactSet Entity
                  Identifier (-E). Results will be saved to the `universeId`
                  specified in the input file.
                tags:
                  - Get
                  - The
                  - Decisions
                  - Of
                  - Matches
                  - For
                  - Requested
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
            /factset-concordance/v2/universe:
              post:
                summary: Create a new universe
                description: >
                  Create a new universe that is distinct from any existing
                  universe
                tags:
                  - Create
                  - New
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
            /factset-concordance/v2/entity-universe:
              get:
                summary: Retrieve all saved mappings within a requested universe
                description: |
                  Retrieves all entity mappings within a requested universe.
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
              post:
                summary: >-
                  Retrieve all saved mappings within a requested universe or
                  large list of client ids
                description: >
                  Retrieves all entity mappings that were saved in a given
                  universe. Supports filtering by a large number of `clientId`s
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Or
                  - Large
                  - List
                  - Of
                  - Client
                  - Ids
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
            /factset-concordance/v2/people-universe:
              get:
                summary: Retrieve all saved mappings within a requested universe
                description: |
                  Retrieves all people mappings within a requested universe.
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
              post:
                summary: >-
                  Retrieve all saved mappings within a requested universe or
                  large list of client ids
                description: >
                  Retrieves all people mappings that were saved in a given
                  universe. Supports filtering by a large number of `clientId`s
                tags:
                  - Retrieve
                  - All
                  - Saved
                  - Mappings
                  - Within
                  - Requested
                  - Universe
                  - Or
                  - Large
                  - List
                  - Of
                  - Client
                  - Ids
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
            /factset-concordance/v2/update-universe:
              post:
                summary: Update metadata for an existing universe
                description: |
                  Update metadata for an existing universe
                tags:
                  - Update
                  - Metadata
                  - For
                  - An
                  - Existing
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
            /factset-concordance/v2/universes:
              get:
                summary: Fetch metadata for universes
                description: >
                  Fetch information on active universes for the current user.
                  Optionally filter for a specific universe given a `universeId`
                tags:
                  - Fetch
                  - Metadata
                  - For
                  - Universes
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
            /factset-concordance/v2/entity-universe-statistics:
              get:
                summary: Get statistics on a given universe
                description: >
                  Get the total number of mappings in a universe, as well as the
                  number of mapped, unmapped and indeterminate mappings
                tags:
                  - Get
                  - Statistics
                  - 'On'
                  - Given
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
            /factset-concordance/v2/universe-statistics:
              get:
                summary: Get statistics on a given universe
                description: >
                  Get the total number of mappings in a universe, as well as the
                  number of mapped, unmapped and indeterminate mappings
                tags:
                  - Get
                  - Statistics
                  - 'On'
                  - Given
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
            /factset-concordance/v2/entity-mapping:
              post:
                summary: Saves a single-mapping specified by the client.
                description: >
                  Saves a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  clientName are required.
                tags:
                  - Saves
                  - Single-mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
            /factset-concordance/v2/people-mapping:
              post:
                summary: Saves a single-mapping specified by the client.
                description: >
                  Saves a single Concordance People Mapping to a given universe.
                  When making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  clientName are required.
                tags:
                  - Saves
                  - Single-mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
            /factset-concordance/v2/entity-mapping-delete:
              post:
                summary: Deletes mapping specified by the client.
                description: >
                  Delete a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  universeId are required.
                tags:
                  - Deletes
                  - Mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
            /factset-concordance/v2/people-mapping-delete:
              post:
                summary: Deletes mapping specified by the client.
                description: >
                  Delete a Concordance Mapping to the client universe. When
                  making a post, all exiting values are overwritten in the
                  database with the values passed in the request. clientId and
                  universeId are required.
                tags:
                  - Deletes
                  - Mapping
                  - Specified
                  - By
                  - The
                  - Client.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
            /factset-concordance/v2/snowflake-entity-match:
              post:
                summary: >-
                  Perform an entity search and return a snowflake-friendly
                  response. Up to 25 Names per request.
                description: >
                  Finds the best candidate entities matching the given company
                  name. Additional attributes can be supplied to narrow the
                  search. *This endpoint is used natively within Snowflake and
                  is not to be consumed directly by users. Reach out to your
                  FactSet Account team to learn more about Concordance in
                  Snowflake.*
                tags:
                  - Perform
                  - An
                  - Entity
                  - Search
                  - And
                  - Return
                  - Snowflake-friendly
                  - Response.
                  - Up
                  - To
                  - '25'
                  - Names
                  - Per
                  - Request.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/snowflake-entity-mapping:
              post:
                summary: Save entity mappings to a universe
                description: Manually save or update entity mappings with metadata
                tags:
                  - Save
                  - Entity
                  - Mappings
                  - To
                  - Universe
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-match:
              get:
                summary: >-
                  Find potential people matches given a person's name.People
                  matches can be retrieved using person's name and other
                  attributes like firstname, middlename and lastname.
                description: >
                  Finds the best people candidates matching the given name.
                  <p>**Max of 1 Name permitted in a single GET request.** Use
                  the POST method for /people-match to fetch up to 25 names.
                  Otherwise, use the "People Match - Bulk" workflow to submit
                  larger universes of names to be concorded via a file.</p><p>
                tags:
                  - Find
                  - Potential
                  - People
                  - Matches
                  - Given
                  - Person's
                  - Name.
                  - Can
                  - Be
                  - Retrieved
                  - Using
                  - Name
                  - And
                  - Other
                  - Attributes
                  - Like
                  - Firstname,
                  - Middlename
                  - Lastname.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
              post:
                summary: Find potential people matches given a person's name.
                description: >
                  Finds the best candidate people matching the given people
                  names. Additional attributes can be supplied to narrow the
                  search. If a `universeId` is provided, any match for an input
                  including a `clientId` will be saved to that universe.
                tags:
                  - Find
                  - Potential
                  - People
                  - Matches
                  - Given
                  - Person's
                  - Name.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-task:
              post:
                summary: Create a People Concordance Task.
                description: >
                  The "Bulk" workflow allows the user to create a People
                  Concordance Task. Uploading of a Comma-Separated List file
                  (.csv / UTF-8 encoding) with a list of names and attributes
                  and creation of a task id is mandatory to start the process.
                     The taskId is then used for reference in the /people-task-status and /people-decisions endpoints to receive results once the task is successful.The /people-task-status endpoint is to check the status of the Tasks as per the ids.
                      A universeId must be included in request. If you do not have a universe created, reference the /universe endpoint.The bulk workflow supports a two way approach for the user.
                    **The user can use these parameters in the following ways.**
                      1.Filling all the required fields including the `personNameColumn`.(do not include `firstNameColumn`,`lastNameColumn` & `middleNameColumn`)
                      2.Filling all the required fields excluding the `personNameColumn`.(Ensure atleast the `lastNameColumn` is filled)
                tags:
                  - Create
                  - People
                  - Concordance
                  - Task.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-task-status:
              get:
                summary: Get the Status of the People Tasks.
                description: >
                  Pulls the **status** for ALL the People Tasks submitted by a
                  client within the last 30 days, and related details such as
                  task duration and decision rates. Specific Tasks can also be
                  retrieved by using the _taskId_ parameter.<p>Status types
                  include -
                    * PENDING - The task has not yet started.
                    * IN_PROGRESS - The task is submitted and decisions are in progress.
                    * SUCCESS - The task was successful! Move to the /people-decisions endpoint to retrieve decisions.
                    * FAILURE - The task failed. Reach out to FactSet Support for assistance.
                    * BAD_REQUEST - The task creation was unsuccesfull. Typically occurs with an incorrect input file format or column headers.
                    * ABORTED - The task was aborted.
                tags:
                  - Get
                  - The
                  - Status
                  - Of
                  - People
                  - Tasks.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowflake
            /factset-concordance/v2/people-decisions:
              get:
                summary: Get the decisions of matches for the requested taskId.
                description: >
                  Retrieves the `Decision` objects for an People Task (taskId).
                  The decisions do not include all candidates, but rather the
                  results of concording the requested list of names included in
                  the input file. Mapped entities will include a FactSet Entity
                  Identifier (-E). Results will be saved to the `universeId`
                  specified in the input file.
                tags:
                  - Get
                  - The
                  - Decisions
                  - Of
                  - Matches
                  - For
                  - Requested
                  - Task
                  - Id.
                  - Factset
                  - Concordance
                  - V2
                  - Entity
                  - Match
                  - Task
                  - Status
                  - Decisions
                  - Universe
                  - People
                  - Update
                  - Universes
                  - Statistics
                  - Mapping
                  - Delete
                  - Snowfla
    overlays:
      - type: APIs.io Search
        url: overlays/concordance-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/concordance-openapi-api-evangelist-ratings.yml
    aid: factset:factset-concordance-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---