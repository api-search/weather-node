---
name: Automations
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/automations.png
url: https://example.com/apis/automations.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Automations
apis:
  - name: honeycode
    description: >-
      <p> Amazon Honeycode is a fully managed service that allows you to quickly
      build mobile and web apps for teams—without programming. Build Honeycode
      apps for managing almost anything, like projects, customers, operations,
      approvals, resources, and even your team. </p>
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
            title: honeycode
          paths:
            /workbooks/{workbookId}/tables/{tableId}/rows/batchcreate:
              POST:
                summary: BatchCreateTableRows
                description: >-
                  <p> The BatchCreateTableRows API allows you to create one or
                  more rows at the end of a table in a workbook. The API allows
                  you to specify the values to set in some or all of the columns
                  in the new rows. </p> <p> If a column is not explicitly set in
                  a specific row, then the column level formula specified in the
                  table will be applied to the new row. If there is no column
                  level formula but the last row of the table has a formula,
                  then that formula will be copied down to the new row. If there
                  is no column level formula and no formula in the last row of
                  the table, then that column will be left blank for the new
                  rows. </p>
                tags:
                  - Batches
                  - Create
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchdelete:
              POST:
                summary: BatchDeleteTableRows
                description: >-
                  <p> The BatchDeleteTableRows API allows you to delete one or
                  more rows from a table in a workbook. You need to specify the
                  ids of the rows that you want to delete from the table. </p>
                tags:
                  - Batches
                  - Delete
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchupdate:
              POST:
                summary: BatchUpdateTableRows
                description: >-
                  <p> The BatchUpdateTableRows API allows you to update one or
                  more rows in a table in a workbook. </p> <p> You can specify
                  the values to set in some or all of the columns in the table
                  for the specified rows. If a column is not explicitly
                  specified in a particular row, then that column will not be
                  updated for that row. To clear out the data in a specific
                  cell, you need to set the value as an empty string (""). </p>
                tags:
                  - Batches
                  - Update
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/rows/batchupsert:
              POST:
                summary: BatchUpsertTableRows
                description: >-
                  <p> The BatchUpsertTableRows API allows you to upsert one or
                  more rows in a table. The upsert operation takes a filter
                  expression as input and evaluates it to find matching rows on
                  the destination table. If matching rows are found, it will
                  update the cells in the matching rows to new values specified
                  in the request. If no matching rows are found, a new row is
                  added at the end of the table and the cells in that row are
                  set to the new values specified in the request. </p> <p> You
                  can specify the values to set in some or all of the columns in
                  the table for the matching or newly appended rows. If a column
                  is not explicitly specified for a particular row, then that
                  column will not be updated for that row. To clear out the data
                  in a specific cell, you need to set the value as an empty
                  string (""). </p>
                tags:
                  - Batches
                  - Upsert
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
            /workbooks/{workbookId}/tables/{tableId}/import/{jobId}:
              GET:
                summary: DescribeTableDataImportJob
                description: >-
                  <p> The DescribeTableDataImportJob API allows you to retrieve
                  the status and details of a table data import job. </p>
                tags:
                  - Describe
                  - Tables
                  - Data
                  - Import
                  - Jobs
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
            /screendata:
              POST:
                summary: GetScreenData
                description: >-
                  <p> The GetScreenData API allows retrieval of data from a
                  screen in a Honeycode app. The API allows setting local
                  variables in the screen to filter, sort or otherwise affect
                  what will be displayed on the screen. </p>
                tags:
                  - Get
                  - Screen
                  - Data
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
            /workbooks/{workbookId}/apps/{appId}/screens/{screenId}/automations/{automationId}:
              POST:
                summary: InvokeScreenAutomation
                description: >-
                  <p> The InvokeScreenAutomation API allows invoking an action
                  defined in a screen in a Honeycode app. The API allows setting
                  local variables, which can then be used in the automation
                  being invoked. This allows automating the Honeycode app
                  interactions to write, update or delete data in the workbook.
                  </p>
                tags:
                  - Invoke
                  - Screen
                  - Automation
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
            /workbooks/{workbookId}/tables/{tableId}/columns:
              GET:
                summary: ListTableColumns
                description: >-
                  <p> The ListTableColumns API allows you to retrieve a list of
                  all the columns in a table in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Columns
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
            /workbooks/{workbookId}/tables/{tableId}/rows/list:
              POST:
                summary: ListTableRows
                description: >-
                  <p> The ListTableRows API allows you to retrieve a list of all
                  the rows in a table in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
            /workbooks/{workbookId}/tables:
              GET:
                summary: ListTables
                description: >-
                  <p> The ListTables API allows you to retrieve a list of all
                  the tables in a workbook. </p>
                tags:
                  - Lists
                  - Tables
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p> The UntagResource API allows you to removes tags from an
                  ARN-able resource. Resource includes workbook, table, screen
                  and screen-automation. </p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
            /workbooks/{workbookId}/tables/{tableId}/rows/query:
              POST:
                summary: QueryTableRows
                description: >-
                  <p> The QueryTableRows API allows you to use a filter formula
                  to query for specific rows in a table. </p>
                tags:
                  - Queries
                  - Tables
                  - Rows
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
                  - Queries
            /workbooks/{workbookId}/tables/{tableId}/import:
              POST:
                summary: StartTableDataImportJob
                description: >-
                  <p> The StartTableDataImportJob API allows you to start an
                  import job on a table. This API will only return the id of the
                  job that was started. To find out the status of the import
                  request, you need to call the DescribeTableDataImportJob
                tags:
                  - Start
                  - Tables
                  - Data
                  - Import
                  - Jobs
                  - Identifiers
                  - Tables
                  - Tables
                  - Rows
                  - Batches
                  - Batches
                  - Batches
                  - Batches
                  - Import
                  - Jobs
                  - Screen Data
                  - Applications
                  - Applications
                  - Screens
                  - Screen
                  - Automations
                  - Automation
                  - Columns
                  - Lists
                  - ARN
                  - Que
    overlays:
      - type: APIs.io Search
        url: overlays/honeycode-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/honeycode-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:honeycode
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---