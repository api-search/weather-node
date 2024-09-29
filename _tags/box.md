---
name: Box
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/box.png
url: https://example.com/apis/box.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Box
apis:
  - aid: box:box-files-api
    name: Box Files API
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
            title: Box Files API
          paths:
            /files/{file_id}:
              get:
                summary: Get file information
                tags:
                  - Get
                  - File
                  - Information
                  - Files
                  - File_id
                description: Retrieves the details about a file.
              post:
                summary: Restore file
                tags:
                  - Restore
                  - File
                  - Files
                  - File_id
                description: >-
                  Restores a file that has been moved to the trash.


                  An optional new parent ID can be provided to restore the file
                  to in case the

                  original folder has been deleted.
              put:
                summary: Update file
                tags:
                  - Update
                  - File
                  - Files
                  - File_id
                description: |-
                  Updates a file. This can be used to rename or move a file,
                  create a shared link, or lock a file.
              delete:
                summary: Delete file
                tags:
                  - Delete
                  - File
                  - Files
                  - File_id
                description: |-
                  Deletes a file, either permanently or by moving it to
                  the trash.

                  The the enterprise settings determine whether the item will
                  be permanently deleted from Box or moved to the trash.
            /files/{file_id}/content:
              get:
                summary: Download file
                tags:
                  - Download
                  - File
                  - Files
                  - File_id
                  - Content
                description: Returns the contents of a file in binary format.
              post:
                tags:
                  - Upload
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                summary: Upload file version
                description: |-
                  Update a file's content. For file sizes over 50MB we recommend
                  using the Chunk Upload APIs.

                  # Request body order

                  The `attributes` part of the body must come **before** the
                  `file` part. Requests that do not follow this format when
                  uploading the file will receive a HTTP `400` error with a
                  `metadata_after_file_contents` error code.
            /files/content:
              options:
                summary: Preflight check before upload
                tags:
                  - Preflight
                  - Check
                  - Before
                  - Upload
                  - Files
                  - File_id
                  - Content
                description: |-
                  Performs a check to verify that a file will be accepted by Box
                  before you upload the entire file.
              post:
                tags:
                  - Upload
                  - File
                  - Files
                  - File_id
                  - Content
                summary: Upload file
                description: >-
                  Uploads a small file to Box. For file sizes over 50MB we
                  recommend

                  using the Chunk Upload APIs.


                  # Request body order


                  The `attributes` part of the body must come **before** the

                  `file` part. Requests that do not follow this format when

                  uploading the file will receive a HTTP `400` error with a

                  `metadata_after_file_contents` error code.
            /files/upload_sessions:
              post:
                summary: Create upload session
                tags:
                  - Create
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for a new file.
            /files/{file_id}/upload_sessions:
              post:
                summary: Create upload session for existing file
                tags:
                  - Create
                  - Upload
                  - Session
                  - For
                  - Existing
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for an existing file.
            /files/upload_sessions/{upload_session_id}:
              get:
                summary: Get upload session
                tags:
                  - Get
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Return information about an upload session.
              put:
                summary: Upload part of file
                tags:
                  - Upload
                  - Part
                  - Of
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Updates a chunk of an upload session for a file.
              delete:
                summary: Remove upload session
                tags:
                  - Remove
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: |-
                  Abort an upload session and discard all data uploaded.

                  This cannot be reversed.
            /files/upload_sessions/{upload_session_id}/parts:
              get:
                summary: List parts
                tags:
                  - List
                  - Parts
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                description: |-
                  Return a list of the chunks uploaded to the upload
                  session so far.
            /files/upload_sessions/{upload_session_id}/commit:
              post:
                summary: Commit upload session
                tags:
                  - Commit
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                description: |-
                  Close an upload session and create a file from the
                  uploaded chunks.
            /files/{file_id}/copy:
              post:
                summary: Copy file
                description: Creates a copy of a file.
                tags:
                  - Copy
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
            /files/{file_id}/thumbnail.{extension}:
              get:
                summary: Get file thumbnail
                description: >-
                  Retrieves a thumbnail, or smaller image representation, of a
                  file.


                  Sizes of `32x32`,`64x64`, `128x128`, and `256x256` can be
                  returned in

                  the `.png` format and sizes of `32x32`, `160x160`, and
                  `320x320`

                  can be returned in the `.jpg` format.


                  Thumbnails can be generated for the image and video file
                  formats listed

                  [found on our community site][1].


                  [1]:
                  https://community.box.com/t5/Migrating-and-Previewing-Content/File-Types-and-Fonts-Supported-in-Box-Content-Preview/ta-p/327
                tags:
                  - Get
                  - File
                  - Thumbnail
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
            /files/{file_id}/collaborations:
              get:
                summary: List file collaborations
                description: |-
                  Retrieves a list of pending and active collaborations for a
                  file. This returns all the users that have access to the file
                  or have been invited to the file.
                tags:
                  - List
                  - File
                  - Collaborations
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
            /files/{file_id}/comments:
              get:
                summary: List file comments
                description: Retrieves a list of comments for a file.
                tags:
                  - List
                  - File
                  - Comments
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
            /files/{file_id}/tasks:
              get:
                summary: List tasks on file
                description: |-
                  Retrieves a list of all the tasks for a file. This
                  endpoint does not support pagination.
                tags:
                  - List
                  - Tasks
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
            /files/{file_id}/trash:
              get:
                summary: Get trashed file
                tags:
                  - Get
                  - Trashed
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: >-
                  Retrieves a file that has been moved to the trash.


                  Please note that only if the file itself has been moved to the

                  trash can it be retrieved with this API call. If instead one
                  of

                  its parent folders was moved to the trash, only that folder

                  can be inspected using the

                  [`GET /folders/:id/trash`](e://get_folders_id_trash) API.


                  To list all items that have been moved to the trash, please

                  use the [`GET
                  /folders/trash/items`](e://get-folders-trash-items/)

                  API.
              delete:
                summary: Permanently remove file
                tags:
                  - Permanently
                  - Remove
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: |-
                  Permanently deletes a file that is in the trash.
                  This action cannot be undone.
            /files/{file_id}/versions:
              get:
                summary: List all file versions
                tags:
                  - List
                  - All
                  - File
                  - Versions
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                description: >-
                  Retrieve a list of the past versions for a file.


                  Versions are only tracked by Box users with premium accounts.
                  To fetch the ID

                  of the current version of a file, use the `GET /file/:id` API.
            /files/{file_id}/versions/{file_version_id}:
              get:
                summary: Get file version
                tags:
                  - Get
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Retrieve a specific version of a file.

                  Versions are only tracked for Box users with premium accounts.
              delete:
                summary: Remove file version
                tags:
                  - Remove
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Move a file version to the trash.

                  Versions are only tracked for Box users with premium accounts.
              put:
                summary: Restore file version
                tags:
                  - Restore
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Restores a specific version of a file after it was deleted.
                  Don't use this endpoint to restore Box Notes,
                  as it works with file formats such as PDF, DOC,
                  PPTX or similar.
            /files/{file_id}/versions/current:
              post:
                summary: Promote file version
                tags:
                  - Promote
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                description: >-
                  Promote a specific version of a file.


                  If previous versions exist, this method can be used to

                  promote one of the older versions to the top of the version
                  history.


                  This creates a new copy of the old version and puts it at the

                  top of the versions history. The file will have the exact same
                  contents

                  as the older version, with the the same hash digest, `etag`,
                  and

                  name as the original.


                  Other properties such as comments do not get updated to their

                  former values.


                  Don't use this endpoint to restore Box Notes,

                  as it works with file formats such as PDF, DOC,

                  PPTX or similar.
            /files/{file_id}/metadata:
              get:
                summary: List metadata instances on file
                tags:
                  - List
                  - Metadata
                  - Instances
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                description: Retrieves all metadata for a given file.
            /files/{file_id}/metadata/enterprise/securityClassification-6VMVochwUWo:
              get:
                summary: Get classification on file
                tags:
                  - Get
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Retrieves the classification metadata instance that

                  has been applied to a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              post:
                summary: Add classification to file
                tags:
                  - Add
                  - Classification
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Adds a classification to a file by specifying the label of the

                  classification to add.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              put:
                summary: Update classification on file
                tags:
                  - Update
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Updates a classification on a file.


                  The classification can only be updated if a classification has
                  already been

                  applied to the file before. When editing classifications, only
                  values are

                  defined for the enterprise will be accepted.
              delete:
                summary: Remove classification from file
                tags:
                  - Remove
                  - Classification
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Removes any classifications from a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
            /files/{file_id}/metadata/{scope}/{template_key}:
              get:
                summary: Get metadata instance on file
                tags:
                  - Get
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the instance of a metadata template that has been
                  applied to a

                  file.
              post:
                summary: Create metadata instance on file
                tags:
                  - Create
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Applies an instance of a metadata template to a file.


                  In most cases only values that are present in the metadata
                  template

                  will be accepted, except for the `global.properties` template
                  which accepts

                  any key-value pair.
              put:
                summary: Update metadata instance on file
                tags:
                  - Update
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Updates a piece of metadata on a file.


                  The metadata instance can only be updated if the template has
                  already been

                  applied to the file before. When editing metadata, only values
                  that match

                  the metadata template schema will be accepted.


                  The update is applied atomically. If any errors occur during
                  the

                  application of the operations, the metadata instance will not
                  be changed.
              delete:
                summary: Remove metadata instance from file
                tags:
                  - Remove
                  - Metadata
                  - Instance
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: Deletes a piece of file metadata.
            /files/{file_id}/metadata/global/boxSkillsCards:
              get:
                summary: List Box Skill cards on file
                tags:
                  - List
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: >-
                  List the Box Skills metadata cards that are attached to a
                  file.
              post:
                summary: Create Box Skill cards on file
                tags:
                  - Create
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Applies one or more Box Skills metadata cards to a file.
              put:
                summary: Update Box Skill cards on file
                tags:
                  - Update
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Updates one or more Box Skills metadata cards to a file.
              delete:
                summary: Remove Box Skill cards from file
                tags:
                  - Remove
                  - Box
                  - Skill
                  - Cards
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Removes any Box Skills cards metadata from a file.
            /files/{file_id}/watermark:
              get:
                summary: Get watermark on file
                tags:
                  - Get
                  - Watermark
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Retrieve the watermark for a file.
              put:
                summary: Apply watermark to file
                tags:
                  - Apply
                  - Watermark
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Applies or update a watermark on a file.
              delete:
                summary: Remove watermark from file
                tags:
                  - Remove
                  - Watermark
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Removes the watermark from a file.
            /files/{file_id}#get_shared_link:
              get:
                summary: Get shared link for file
                tags:
                  - Get
                  - Shared
                  - Link
                  - For
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                description: Gets the information for a shared link on a file.
            /files/{file_id}#add_shared_link:
              put:
                summary: Add shared link to file
                tags:
                  - Add
                  - Shared
                  - Link
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                description: Adds a shared link to a file.
            /files/{file_id}#update_shared_link:
              put:
                summary: Update shared link on file
                tags:
                  - Update
                  - Shared
                  - Link
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                description: Updates a shared link on a file.
            /files/{file_id}#remove_shared_link:
              put:
                summary: Remove shared link from file
                tags:
                  - Remove
                  - Shared
                  - Link
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                description: Removes a shared link from a file.
            /retention_policy_assignments/{retention_policy_assignment_id}/files_under_retention:
              get:
                summary: Get files under retention
                tags:
                  - Get
                  - Files
                  - Under
                  - Retention
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                description: >-
                  Returns a list of files under retention for a retention policy
                  assignment.
            /legal_hold_policy_assignments/{legal_hold_policy_assignment_id}/files_on_hold:
              get:
                summary: List current file versions for legal hold policy assignment
                tags:
                  - List
                  - Current
                  - File
                  - Versions
                  - For
                  - Legal
                  - Hold
                  - Policy
                  - Assignment
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                  - Files_on_hold
                description: >-
                  Get a list of current file versions for a legal hold

                  assignment.


                  In some cases you may want to get previous file versions
                  instead. In these

                  cases, use the `GET 
                  /legal_hold_policy_assignments/:id/file_versions_on_hold`

                  API instead to return any previous versions of a file for this
                  legal hold

                  policy assignment.


                  Due to ongoing re-architecture efforts this API might not
                  return all file

                  versions held for this policy ID. Instead, this API will only
                  return the

                  latest file version held in the newly developed architecture.
                  The `GET

                  /file_version_legal_holds` API can be used to fetch current
                  and past versions

                  of files held within the legacy architecture.


                  The `GET /legal_hold_policy_assignments?policy_id={id}` API
                  can be used to

                  find a list of policy assignments for a give
    overlays:
      - type: APIs.io Search
        url: overlays/files-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/files-openapi-api-evangelist-ratings.yml
  - aid: box:box-skill-invocations-api
    name: Box Skill Invocations API
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
            title: Box Skill Invocations API
          paths:
            /skill_invocations/{skill_id}:
              put:
                summary: Update all Box Skill cards on file
                tags:
                  - Update
                  - All
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Skill_invocations
                  - Skill_id
                description: >-
                  An alternative method that can be used to overwrite and update
                  all Box Skill

                  metadata card
    overlays:
      - type: APIs.io Search
        url: overlays/skill-invocations-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/skill-invocations-openapi-api-evangelist-ratings.yml
  - aid: box:box-sign-templates-api
    name: Box Sign Templates API
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
            title: Box Sign Templates API
          paths:
            /sign_templates:
              get:
                summary: List Box Sign templates
                tags:
                  - List
                  - Box
                  - Sign
                  - Templates
                  - Sign_templates
                description: Gets Box Sign templates created by a user.
            /sign_templates/{template_id}:
              get:
                summary: Get Box Sign template by ID
                tags:
                  - Get
                  - Box
                  - Sign
                  - Template
                  - By
                  - Sign_templates
                  - Template_id
                description: Fetches details of a specific Box Si
    overlays:
      - type: APIs.io Search
        url: overlays/sign-templates-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sign-templates-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---