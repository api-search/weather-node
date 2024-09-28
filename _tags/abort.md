---
name: Abort
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/abort.png
url: https://example.com/apis/abort.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Abort
apis:
  - name: omics
    description: >-
      <p>This is the <i>AWS HealthOmics API Reference</i>. For an introduction
      to the service, see <a
      href="https://docs.aws.amazon.com/omics/latest/dev/">What is AWS
      HealthOmics?</a> in the <i>AWS HealthOmics User Guide</i>.</p>
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
            title: omics
          paths:
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/abort:
              DELETE:
                summary: AbortMultipartReadSetUpload
                description: <p> Stops a multipart upload. </p>
                tags:
                  - Abort
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
            /share/{shareId}:
              GET:
                summary: GetShare
                description: <p> Retrieves the metadata for a share. </p>
                tags:
                  - Get
                  - Share
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
            /sequencestore/{sequenceStoreId}/readset/batch/delete:
              POST:
                summary: BatchDeleteReadSet
                description: <p>Deletes one or more read sets.</p>
                tags:
                  - Batches
                  - Delete
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
            /import/annotation/{jobId}:
              GET:
                summary: GetAnnotationImportJob
                description: <p>Gets information about an annotation import job.</p>
                tags:
                  - Get
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
            /run/{id}/cancel:
              POST:
                summary: CancelRun
                description: <p>Cancels a run.</p>
                tags:
                  - Cancel
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
            /import/variant/{jobId}:
              GET:
                summary: GetVariantImportJob
                description: <p>Gets information about a variant import job.</p>
                tags:
                  - Get
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/complete:
              POST:
                summary: CompleteMultipartReadSetUpload
                description: >-
                  <p> Concludes a multipart upload once you have uploaded all
                  the components. </p>
                tags:
                  - Complete
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
            /annotationStore:
              POST:
                summary: CreateAnnotationStore
                description: <p>Creates an annotation store.</p>
                tags:
                  - Create
                  - Annotations
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
            /annotationStore/{name}/version:
              POST:
                summary: CreateAnnotationStoreVersion
                description: <p> Creates a new version of an annotation store. </p>
                tags:
                  - Create
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
            /sequencestore/{sequenceStoreId}/upload:
              POST:
                summary: CreateMultipartReadSetUpload
                description: <p> Begins a multipart read set upload. </p>
                tags:
                  - Create
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
            /referencestore:
              POST:
                summary: CreateReferenceStore
                description: <p>Creates a reference store.</p>
                tags:
                  - Create
                  - References
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
            /runGroup:
              GET:
                summary: ListRunGroups
                description: <p>Retrieves a list of run groups.</p>
                tags:
                  - Lists
                  - Runs
                  - Groups
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
            /sequencestore:
              POST:
                summary: CreateSequenceStore
                description: <p>Creates a sequence store.</p>
                tags:
                  - Create
                  - Sequence
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
            /share:
              POST:
                summary: CreateShare
                description: >-
                  <p> Creates a share offer that can be accepted outside the
                  account by a subscriber. The share is created by the owner and
                  accepted by the principal subscriber. </p>
                tags:
                  - Create
                  - Share
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
            /variantStore:
              POST:
                summary: CreateVariantStore
                description: <p>Creates a variant store.</p>
                tags:
                  - Create
                  - Variants
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
            /workflow:
              GET:
                summary: ListWorkflows
                description: <p>Retrieves a list of workflows.</p>
                tags:
                  - Lists
                  - Workflows
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
            /annotationStore/{name}:
              POST:
                summary: UpdateAnnotationStore
                description: <p>Updates an annotation store.</p>
                tags:
                  - Update
                  - Annotations
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
            /annotationStore/{name}/versions/delete:
              POST:
                summary: DeleteAnnotationStoreVersions
                description: >-
                  <p> Deletes one or multiple versions of an annotation store.
                  </p>
                tags:
                  - Delete
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
            /referencestore/{referenceStoreId}/reference/{id}:
              GET:
                summary: GetReference
                description: <p>Gets a reference file.</p>
                tags:
                  - Get
                  - References
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /referencestore/{id}:
              GET:
                summary: GetReferenceStore
                description: <p>Gets information about a reference store.</p>
                tags:
                  - Get
                  - References
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /run/{id}:
              GET:
                summary: GetRun
                description: <p>Gets information about a workflow run.</p>
                tags:
                  - Get
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /runGroup/{id}:
              POST:
                summary: UpdateRunGroup
                description: <p>Updates a run group.</p>
                tags:
                  - Update
                  - Runs
                  - Group
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{id}:
              GET:
                summary: GetSequenceStore
                description: <p>Gets information about a sequence store.</p>
                tags:
                  - Get
                  - Sequence
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /variantStore/{name}:
              POST:
                summary: UpdateVariantStore
                description: <p>Updates a variant store.</p>
                tags:
                  - Update
                  - Variants
                  - Store
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /workflow/{id}:
              POST:
                summary: UpdateWorkflow
                description: <p>Updates a workflow.</p>
                tags:
                  - Update
                  - Workflows
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /annotationStore/{name}/version/{versionName}:
              POST:
                summary: UpdateAnnotationStoreVersion
                description: >-
                  <p> Updates the description of an annotation store version.
                  </p>
                tags:
                  - Update
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{sequenceStoreId}/readset/{id}:
              GET:
                summary: GetReadSet
                description: <p>Gets a file from a read set.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
            /sequencestore/{sequenceStoreId}/activationjob/{id}:
              GET:
                summary: GetReadSetActivationJob
                description: <p>Gets information about a read set activation job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
            /sequencestore/{sequenceStoreId}/exportjob/{id}:
              GET:
                summary: GetReadSetExportJob
                description: <p>Gets information about a read set export job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
            /sequencestore/{sequenceStoreId}/importjob/{id}:
              GET:
                summary: GetReadSetImportJob
                description: <p>Gets information about a read set import job.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
            /sequencestore/{sequenceStoreId}/readset/{id}/metadata:
              GET:
                summary: GetReadSetMetadata
                description: <p>Gets details about a read set.</p>
                tags:
                  - Get
                  - Read
                  - Sets
                  - Metadata
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /referencestore/{referenceStoreId}/importjob/{id}:
              GET:
                summary: GetReferenceImportJob
                description: <p>Gets information about a reference import job.</p>
                tags:
                  - Get
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /referencestore/{referenceStoreId}/reference/{id}/metadata:
              GET:
                summary: GetReferenceMetadata
                description: <p>Gets information about a genome reference's metadata.</p>
                tags:
                  - Get
                  - References
                  - Metadata
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /run/{id}/task/{taskId}:
              GET:
                summary: GetRunTask
                description: <p>Gets information about a workflow run task.</p>
                tags:
                  - Get
                  - Runs
                  - Tasks
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
            /import/annotations:
              POST:
                summary: ListAnnotationImportJobs
                description: <p>Retrieves a list of annotation import jobs.</p>
                tags:
                  - Lists
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
            /annotationStore/{name}/versions:
              POST:
                summary: ListAnnotationStoreVersions
                description: <p> Lists the versions of an annotation store. </p>
                tags:
                  - Lists
                  - Annotations
                  - Store
                  - Versions
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
            /annotationStores:
              POST:
                summary: ListAnnotationStores
                description: <p>Retrieves a list of annotation stores.</p>
                tags:
                  - Lists
                  - Annotations
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
            /sequencestore/{sequenceStoreId}/uploads:
              POST:
                summary: ListMultipartReadSetUploads
                description: >-
                  <p> Lists multipart read set uploads and for in progress
                  uploads. Once the upload is completed, a read set is created
                  and the upload will no longer be returned in the respone. </p>
                tags:
                  - Lists
                  - Multipart
                  - Read
                  - Sets
                  - Uploads
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
            /sequencestore/{sequenceStoreId}/activationjobs:
              POST:
                summary: ListReadSetActivationJobs
                description: <p>Retrieves a list of read set activation jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
            /sequencestore/{sequenceStoreId}/exportjobs:
              POST:
                summary: ListReadSetExportJobs
                description: <p>Retrieves a list of read set export jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
            /sequencestore/{sequenceStoreId}/importjobs:
              POST:
                summary: ListReadSetImportJobs
                description: <p>Retrieves a list of read set import jobs.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/parts:
              POST:
                summary: ListReadSetUploadParts
                description: >-
                  <p> This operation will list all parts in a requested
                  multipart upload for a sequence store. </p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Uploads
                  - Parts
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
            /sequencestore/{sequenceStoreId}/readsets:
              POST:
                summary: ListReadSets
                description: <p>Retrieves a list of read sets.</p>
                tags:
                  - Lists
                  - Read
                  - Sets
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
            /referencestore/{referenceStoreId}/importjobs:
              POST:
                summary: ListReferenceImportJobs
                description: <p>Retrieves a list of reference import jobs.</p>
                tags:
                  - Lists
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
            /referencestores:
              POST:
                summary: ListReferenceStores
                description: <p>Retrieves a list of reference stores.</p>
                tags:
                  - Lists
                  - References
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
            /referencestore/{referenceStoreId}/references:
              POST:
                summary: ListReferences
                description: <p>Retrieves a list of references.</p>
                tags:
                  - Lists
                  - References
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
            /run/{id}/task:
              GET:
                summary: ListRunTasks
                description: <p>Retrieves a list of tasks for a run.</p>
                tags:
                  - Lists
                  - Runs
                  - Tasks
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
            /run:
              POST:
                summary: StartRun
                description: >-
                  <p>Starts a workflow run. To duplicate a run, specify the
                  run's ID and a role ARN. The remaining parameters are copied
                  from the previous run.</p> <p>The total number of runs in your
                  account is subject to a quota per Region. To avoid needing to
                  delete runs manually, you can set the retention mode to
                  <code>REMOVE</code>. Runs with this setting are deleted
                  automatically when the run quoata is exceeded.</p>
                tags:
                  - Start
                  - Runs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
            /sequencestores:
              POST:
                summary: ListSequenceStores
                description: <p>Retrieves a list of sequence stores.</p>
                tags:
                  - Lists
                  - Sequence
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
            /shares:
              POST:
                summary: ListShares
                description: <p> Lists all shares associated with an account. </p>
                tags:
                  - Lists
                  - Shares
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
            /import/variants:
              POST:
                summary: ListVariantImportJobs
                description: <p>Retrieves a list of variant import jobs.</p>
                tags:
                  - Lists
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
            /variantStores:
              POST:
                summary: ListVariantStores
                description: <p>Retrieves a list of variant stores.</p>
                tags:
                  - Lists
                  - Variants
                  - Stores
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
            /import/annotation:
              POST:
                summary: StartAnnotationImportJob
                description: <p>Starts an annotation import job.</p>
                tags:
                  - Start
                  - Annotations
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/activationjob:
              POST:
                summary: StartReadSetActivationJob
                description: >-
                  <p>Activates an archived read set. To reduce storage charges,
                  Amazon Omics archives unused read sets after 30 days.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Activation
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/exportjob:
              POST:
                summary: StartReadSetExportJob
                description: <p>Exports a read set to Amazon S3.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Export
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /sequencestore/{sequenceStoreId}/importjob:
              POST:
                summary: StartReadSetImportJob
                description: <p>Starts a read set import job.</p>
                tags:
                  - Start
                  - Read
                  - Sets
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /referencestore/{referenceStoreId}/importjob:
              POST:
                summary: StartReferenceImportJob
                description: <p>Starts a reference import job.</p>
                tags:
                  - Start
                  - References
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
            /import/variant:
              POST:
                summary: StartVariantImportJob
                description: <p>Starts a variant import job.</p>
                tags:
                  - Start
                  - Variants
                  - Import
                  - Jobs
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
                  - Variants
            /sequencestore/{sequenceStoreId}/upload/{uploadId}/part:
              PUT:
                summary: UploadReadSetPart
                description: >-
                  <p> This operation uploads a specific part of a read set. If
                  you upload a new part using a previously used part number, the
                  previously uploaded part will be overwri
                tags:
                  - Uploads
                  - Read
                  - Sets
                  - Part
                  - Store
                  - Identifiers
                  - Uploads
                  - Abort
                  - Readsets
                  - Batches
                  - Delete
                  - Runs
                  - Cancel
                  - Complete
                  - Names
                  - Versions
                  - Reference Store
                  - Group
                  - Sequence Stores
                  - Share
                  - Workflows
                  - Versions
                  - References
                  - Activation Jobs
                  - Export Jobs
                  - Import Jobs
                  - Metadata
                  - Import
                  - Annotations
                  - Stores
                  - Uploads
                  - Activation Jobs
                  - Export Jobs
                  - Import JObs
                  - Parts
                  - Readsets
                  - Reference Store
                  - References
                  - Tasks
                  - Sequence Stores
                  - Shares
                  - ARN
                  - Variants
                  - Annotations
                  - Variants
                  - Pa
    overlays:
      - type: APIs.io Search
        url: overlays/omics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/omics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:omics
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---