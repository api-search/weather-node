---
name: Archives
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/archives.png
url: https://example.com/apis/archives.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Archives
apis:
  - name: glacier
    description: >-
      <p> Amazon S3 Glacier (Glacier) is a storage solution for "cold data."</p>
      <p>Glacier is an extremely low-cost storage service that provides secure,
      durable, and easy-to-use storage for data backup and archival. With
      Glacier, customers can store their data cost effectively for months,
      years, or decades. Glacier also enables customers to offload the
      administrative burdens of operating and scaling storage to AWS, so they
      don't have to worry about capacity planning, hardware provisioning, data
      replication, hardware failure and recovery, or time-consuming hardware
      migrations.</p> <p>Glacier is a great storage choice when low storage cost
      is paramount and your data is rarely retrieved. If your application
      requires fast or frequent access to your data, consider using Amazon S3.
      For more information, see <a href="http://aws.amazon.com/s3/">Amazon
      Simple Storage Service (Amazon S3)</a>.</p> <p>You can store any kind of
      data in any format. There is no maximum limit on the total amount of data
      you can store in Glacier.</p> <p>If you are a first-time user of Glacier,
      we recommend that you begin by reading the following sections in the
      <i>Amazon S3 Glacier Developer Guide</i>:</p> <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/amazonglacier/latest/dev/introduction.html">What
      is Amazon S3 Glacier</a> - This section of the Developer Guide describes
      the underlying data model, the operations it supports, and the AWS SDKs
      that you can use to interact with the service.</p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/amazonglacier/latest/dev/amazon-glacier-getting-started.html">Getting
      Started with Amazon S3 Glacier</a> - The Getting Started section walks you
      through the process of creating a vault, uploading archives, creating jobs
      to download archives, retrieving the job output, and deleting
      archives.</p> </li> </ul>
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
            title: glacier
          paths:
            /{accountId}/vaults/{vaultName}/multipart-uploads/{uploadId}:
              PUT:
                summary: UploadMultipartPart
                description: >-
                  <p>This operation uploads a part of an archive. You can upload
                  archive parts in any order. You can also upload them in
                  parallel. You can upload up to 10,000 parts for a multipart
                  upload.</p> <p>Amazon Glacier rejects your upload part request
                  if any of the following conditions is true:</p> <ul> <li> <p>
                  <b>SHA256 tree hash does not match</b>To ensure that part data
                  is not corrupted in transmission, you compute a SHA256 tree
                  hash of the part and include it in your request. Upon
                  receiving the part data, Amazon S3 Glacier also computes a
                  SHA256 tree hash. If these hash values don't match, the
                  operation fails. For information about computing a SHA256 tree
                  hash, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/checksum-calculations.html">Computing
                  Checksums</a>.</p> </li> <li> <p> <b>Part size does not
                  match</b>The size of each part except the last must match the
                  size specified in the corresponding
                  <a>InitiateMultipartUpload</a> request. The size of the last
                  part must be the same size as, or smaller than, the specified
                  size.</p> <note> <p>If you upload a part whose size is smaller
                  than the part size you specified in your initiate multipart
                  upload request and that part is not the last part, then the
                  upload part request will succeed. However, the subsequent
                  Complete Multipart Upload request will fail.</p> </note> </li>
                  <li> <p> <b>Range does not align</b>The byte range value in
                  the request does not align with the part size specified in the
                  corresponding initiate request. For example, if you specify a
                  part size of 4194304 bytes (4 MB), then 0 to 4194303 bytes (4
                  MB - 1) and 4194304 (4 MB) to 8388607 (8 MB - 1) are valid
                  part ranges. However, if you set a range value of 2 MB to 6
                  MB, the range does not align with the part size and the upload
                  will fail. </p> </li> </ul> <p>This operation is idempotent.
                  If you upload the same part multiple times, the data included
                  in the most recent request overwrites the previously uploaded
                  data.</p> <p>An AWS account has full permission to perform all
                  operations (actions). However, AWS Identity and Access
                  Management (IAM) users don't have any permissions by default.
                  You must grant them explicit permission to perform specific
                  actions. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p> For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/uploading-archive-mpu.html">Uploading
                  Large Archives in Parts (Multipart Upload)</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-upload-part.html">Upload
                  Part </a> in the <i>Amazon Glacier Developer Guide</i>.</p>
                tags:
                  - Uploads
                  - Multipart
                  - Part
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
            /{accountId}/vaults/{vaultName}/lock-policy:
              POST:
                summary: InitiateVaultLock
                description: >-
                  <p>This operation initiates the vault locking process by doing
                  the following:</p> <ul> <li> <p>Installing a vault lock policy
                  on the specified vault.</p> </li> <li> <p>Setting the lock
                  state of vault lock to <code>InProgress</code>.</p> </li> <li>
                  <p>Returning a lock ID, which is used to complete the vault
                  locking process.</p> </li> </ul> <p>You can set one vault lock
                  policy for each vault and this policy can be up to 20 KB in
                  size. For more information about vault lock policies, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock-policy.html">Amazon
                  Glacier Access Control with Vault Lock Policies</a>. </p>
                  <p>You must complete the vault locking process within 24 hours
                  after the vault lock enters the <code>InProgress</code> state.
                  After the 24 hour window ends, the lock ID expires, the vault
                  automatically exits the <code>InProgress</code> state, and the
                  vault lock policy is removed from the vault. You call
                  <a>CompleteVaultLock</a> to complete the vault locking process
                  by setting the state of the vault lock to <code>Locked</code>.
                  </p> <p>After a vault lock is in the <code>Locked</code>
                  state, you cannot initiate a new vault lock for the vault.</p>
                  <p>You can abort the vault locking process by calling
                  <a>AbortVaultLock</a>. You can get the state of the vault lock
                  by calling <a>GetVaultLock</a>. For more information about the
                  vault locking process, <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html">Amazon
                  Glacier Vault Lock</a>.</p> <p>If this operation is called
                  when the vault lock is in the <code>InProgress</code> state,
                  the operation returns an <code>AccessDeniedException</code>
                  error. When the vault lock is in the <code>InProgress</code>
                  state you must call <a>AbortVaultLock</a> before you can
                  initiate a new vault lock policy. </p>
                tags:
                  - Initiate
                  - Vault
                  - Locks
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
            /{accountId}/vaults/{vaultName}/tags?operation=add:
              POST:
                summary: AddTagsToVault
                description: >-
                  <p>This operation adds the specified tags to a vault. Each tag
                  is composed of a key and a value. Each vault can have up to 10
                  tags. If your request would cause the tag limit for the vault
                  to be exceeded, the operation throws the
                  <code>LimitExceededException</code> error. If a tag already
                  exists on the vault under a specified key, the existing key
                  value will be overwritten. For more information about tags,
                  see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/tagging.html">Tagging
                  Amazon S3 Glacier Resources</a>. </p>
                tags:
                  - Add
                  - Tags
                  - To
                  - Vault
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
            /{accountId}/vaults/{vaultName}/lock-policy/{lockId}:
              POST:
                summary: CompleteVaultLock
                description: >-
                  <p>This operation completes the vault locking process by
                  transitioning the vault lock from the <code>InProgress</code>
                  state to the <code>Locked</code> state, which causes the vault
                  lock policy to become unchangeable. A vault lock is put into
                  the <code>InProgress</code> state by calling
                  <a>InitiateVaultLock</a>. You can obtain the state of the
                  vault lock by calling <a>GetVaultLock</a>. For more
                  information about the vault locking process, <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-lock.html">Amazon
                  Glacier Vault Lock</a>. </p> <p>This operation is idempotent.
                  This request is always successful if the vault lock is in the
                  <code>Locked</code> state and the provided lock ID matches the
                  lock ID originally used to lock the vault.</p> <p>If an
                  invalid lock ID is passed in the request when the vault lock
                  is in the <code>Locked</code> state, the operation returns an
                  <code>AccessDeniedException</code> error. If an invalid lock
                  ID is passed in the request when the vault lock is in the
                  <code>InProgress</code> state, the operation throws an
                  <code>InvalidParameter</code> error.</p>
                tags:
                  - Complete
                  - Vault
                  - Locks
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
            /{accountId}/vaults/{vaultName}:
              GET:
                summary: DescribeVault
                description: >-
                  <p>This operation returns information about a vault, including
                  the vault's Amazon Resource Name (ARN), the date the vault was
                  created, the number of archives it contains, and the total
                  size of all the archives in the vault. The number of archives
                  and their total size are as of the last inventory generation.
                  This means that if you add or remove an archive from a vault,
                  and then immediately use Describe Vault, the change in
                  contents will not be immediately reflected. If you want to
                  retrieve the latest inventory of the vault, use
                  <a>InitiateJob</a>. Amazon S3 Glacier generates vault
                  inventories approximately daily. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-inventory.html">Downloading
                  a Vault Inventory in Amazon S3 Glacier</a>. </p> <p>An AWS
                  account has full permission to perform all operations
                  (actions). However, AWS Identity and Access Management (IAM)
                  users don't have any permissions by default. You must grant
                  them explicit permission to perform specific actions. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p>For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/retrieving-vault-info.html">Retrieving
                  Vault Metadata in Amazon S3 Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-vault-get.html">Describe
                  Vault </a> in the <i>Amazon Glacier Developer Guide</i>. </p>
                tags:
                  - Describe
                  - Vault
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
            /{accountId}/vaults/{vaultName}/archives/{archiveId}:
              DELETE:
                summary: DeleteArchive
                description: >-
                  <p>This operation deletes an archive from a vault. Subsequent
                  requests to initiate a retrieval of this archive will fail.
                  Archive retrievals that are in progress for this archive ID
                  may or may not succeed according to the following
                  scenarios:</p> <ul> <li> <p>If the archive retrieval job is
                  actively preparing the data for download when Amazon S3
                  Glacier receives the delete archive request, the archival
                  retrieval operation might fail.</p> </li> <li> <p>If the
                  archive retrieval job has successfully prepared the archive
                  for download when Amazon S3 Glacier receives the delete
                  archive request, you will be able to download the output.</p>
                  </li> </ul> <p>This operation is idempotent. Attempting to
                  delete an already-deleted archive does not result in an
                  error.</p> <p>An AWS account has full permission to perform
                  all operations (actions). However, AWS Identity and Access
                  Management (IAM) users don't have any permissions by default.
                  You must grant them explicit permission to perform specific
                  actions. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p> For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/deleting-an-archive.html">Deleting
                  an Archive in Amazon Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-archive-delete.html">Delete
                  Archive</a> in the <i>Amazon Glacier Developer Guide</i>. </p>
                tags:
                  - Delete
                  - Archive
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
            /{accountId}/vaults/{vaultName}/access-policy:
              PUT:
                summary: SetVaultAccessPolicy
                description: >-
                  <p>This operation configures an access policy for a vault and
                  will overwrite an existing policy. To configure a vault access
                  policy, send a PUT request to the <code>access-policy</code>
                  subresource of the vault. An access policy is specific to a
                  vault and is also called a vault subresource. You can set one
                  access policy per vault and the policy can be up to 20 KB in
                  size. For more information about vault access policies, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-access-policy.html">Amazon
                  Glacier Access Control with Vault Access Policies</a>. </p>
                tags:
                  - Sets
                  - Vault
                  - Access
                  - Policies
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
            /{accountId}/vaults/{vaultName}/notification-configuration:
              PUT:
                summary: SetVaultNotifications
                description: >-
                  <p>This operation configures notifications that will be sent
                  when specific events happen to a vault. By default, you don't
                  get any notifications.</p> <p>To configure vault
                  notifications, send a PUT request to the
                  <code>notification-configuration</code> subresource of the
                  vault. The request should include a JSON document that
                  provides an Amazon SNS topic and specific events for which you
                  want Amazon S3 Glacier to send notifications to the topic.</p>
                  <p>Amazon SNS topics must grant permission to the vault to be
                  allowed to publish notifications to the topic. You can
                  configure a vault to publish a notification for the following
                  vault events:</p> <ul> <li> <p>
                  <b>ArchiveRetrievalCompleted</b> This event occurs when a job
                  that was initiated for an archive retrieval is completed
                  (<a>InitiateJob</a>). The status of the completed job can be
                  "Succeeded" or "Failed". The notification sent to the SNS
                  topic is the same output as returned from <a>DescribeJob</a>.
                  </p> </li> <li> <p> <b>InventoryRetrievalCompleted</b> This
                  event occurs when a job that was initiated for an inventory
                  retrieval is completed (<a>InitiateJob</a>). The status of the
                  completed job can be "Succeeded" or "Failed". The notification
                  sent to the SNS topic is the same output as returned from
                  <a>DescribeJob</a>. </p> </li> </ul> <p>An AWS account has
                  full permission to perform all operations (actions). However,
                  AWS Identity and Access Management (IAM) users don't have any
                  permissions by default. You must grant them explicit
                  permission to perform specific actions. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p>For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/configuring-notifications.html">Configuring
                  Vault Notifications in Amazon S3 Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-vault-notifications-put.html">Set
                  Vault Notification Configuration </a> in the <i>Amazon Glacier
                  Developer Guide</i>. </p>
                tags:
                  - Sets
                  - Vault
                  - Notifications
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
            /{accountId}/vaults/{vaultName}/jobs/{jobId}:
              GET:
                summary: DescribeJob
                description: >-
                  <p>This operation returns information about a job you
                  previously initiated, including the job initiation date, the
                  user who initiated the job, the job status code/message and
                  the Amazon SNS topic to notify after Amazon S3 Glacier
                  (Glacier) completes the job. For more information about
                  initiating a job, see <a>InitiateJob</a>. </p> <note> <p>This
                  operation enables you to check the status of your job.
                  However, it is strongly recommended that you set up an Amazon
                  SNS topic and specify it in your initiate job request so that
                  Glacier can notify the topic after it completes the job.</p>
                  </note> <p>A job ID will not expire for at least 24 hours
                  after Glacier completes the job.</p> <p>An AWS account has
                  full permission to perform all operations (actions). However,
                  AWS Identity and Access Management (IAM) users don't have any
                  permissions by default. You must grant them explicit
                  permission to perform specific actions. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p> For more information about using this
                  operation, see the documentation for the underlying REST API
                  <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-describe-job-get.html">Describe
                  Job</a> in the <i>Amazon Glacier Developer Guide</i>. </p>
                tags:
                  - Describe
                  - Jobs
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
            /{accountId}/policies/data-retrieval:
              PUT:
                summary: SetDataRetrievalPolicy
                description: >-
                  <p>This operation sets and then enacts a data retrieval policy
                  in the region specified in the PUT request. You can set one
                  policy per region for an AWS account. The policy is enacted
                  within a few minutes of a successful PUT operation.</p> <p>The
                  set policy operation does not affect retrieval jobs that were
                  in progress before the policy was enacted. For more
                  information about data retrieval policies, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/data-retrieval-policy.html">Amazon
                  Glacier Data Retrieval Policies</a>. </p>
                tags:
                  - Sets
                  - Data
                  - Retrieval
                  - Policies
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
            /{accountId}/vaults/{vaultName}/jobs/{jobId}/output:
              GET:
                summary: GetJobOutput
                description: >-
                  <p>This operation downloads the output of the job you
                  initiated using <a>InitiateJob</a>. Depending on the job type
                  you specified when you initiated the job, the output will be
                  either the content of an archive or a vault inventory.</p>
                  <p>You can download all the job output or download a portion
                  of the output by specifying a byte range. In the case of an
                  archive retrieval job, depending on the byte range you
                  specify, Amazon S3 Glacier (Glacier) returns the checksum for
                  the portion of the data. You can compute the checksum on the
                  client and verify that the values match to ensure the portion
                  you downloaded is the correct data.</p> <p>A job ID will not
                  expire for at least 24 hours after Glacier completes the job.
                  That a byte range. For both archive and inventory retrieval
                  jobs, you should verify the downloaded size against the size
                  returned in the headers from the <b>Get Job Output</b>
                  response.</p> <p>For archive retrieval jobs, you should also
                  verify that the size is what you expected. If you download a
                  portion of the output, the expected size is based on the range
                  of bytes you specified. For example, if you specify a range of
                  <code>bytes=0-1048575</code>, you should verify your download
                  size is 1,048,576 bytes. If you download an entire archive,
                  the expected size is the size of the archive when you uploaded
                  it to Amazon S3 Glacier The expected size is also returned in
                  the headers from the <b>Get Job Output</b> response.</p> <p>In
                  the case of an archive retrieval job, depending on the byte
                  range you specify, Glacier returns the checksum for the
                  portion of the data. To ensure the portion you downloaded is
                  the correct data, compute the checksum on the client, verify
                  that the values match, and verify that the size is what you
                  expected.</p> <p>A job ID does not expire for at least 24
                  hours after Glacier completes the job. That is, you can
                  download the job output within the 24 hours period after
                  Amazon Glacier completes the job.</p> <p>An AWS account has
                  full permission to perform all operations (actions). However,
                  AWS Identity and Access Management (IAM) users don't have any
                  permissions by default. You must grant them explicit
                  permission to perform specific actions. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p>For conceptual information and the
                  underlying REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/vault-inventory.html">Downloading
                  a Vault Inventory</a>, <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive.html">Downloading
                  an Archive</a>, and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-job-output-get.html">Get
                  Job Output </a> </p>
                tags:
                  - Get
                  - Jobs
                  - Output
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
            /{accountId}/vaults/{vaultName}/jobs:
              GET:
                summary: ListJobs
                description: >-
                  <p>This operation lists jobs for a vault, including jobs that
                  are in-progress and jobs that have recently finished. The List
                  Job operation returns a list of these jobs sorted by job
                  initiation time.</p> <note> <p>Amazon Glacier retains recently
                  completed jobs for a period before deleting them; however, it
                  eventually removes completed jobs. The output of completed
                  jobs can be retrieved. Retaining completed jobs for a period
                  of time after they have completed enables you to get a job
                  output in the event you miss the job completion notification
                  or your first attempt to download it fails. For example,
                  suppose you start an archive retrieval job to download an
                  archive. After the job completes, you start to download the
                  archive but encounter a network error. In this scenario, you
                  can retry and download the archive while the job exists.</p>
                  </note> <p>The List Jobs operation supports pagination. You
                  should always check the response <code>Marker</code> field. If
                  there are no more jobs to list, the <code>Marker</code> field
                  is set to <code>null</code>. If there are more jobs to list,
                  the <code>Marker</code> field is set to a non-null value,
                  which you can use to continue the pagination of the list. To
                  return a list of jobs that begins at a specific job, set the
                  marker request parameter to the <code>Marker</code> value for
                  that job that you obtained from a previous List Jobs
                  request.</p> <p>You can set a maximum limit for the number of
                  jobs returned in the response by specifying the
                  <code>limit</code> parameter in the request. The default limit
                  is 50. The number of jobs returned might be fewer than the
                  limit, but the number of returned jobs never exceeds the
                  limit.</p> <p>Additionally, you can filter the jobs list
                  returned by specifying the optional <code>statuscode</code>
                  parameter or <code>completed</code> parameter, or both. Using
                  the <code>statuscode</code> parameter, you can specify to
                  return only jobs that match either the
                  <code>InProgress</code>, <code>Succeeded</code>, or
                  <code>Failed</code> status. Using the <code>completed</code>
                  parameter, you can specify to return only jobs that were
                  completed (<code>true</code>) or jobs that were not completed
                  (<code>false</code>).</p> <p>For more information about using
                  this operation, see the documentation for the underlying REST
                  API <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-jobs-get.html">List
                  Jobs</a>. </p>
                tags:
                  - Lists
                  - Jobs
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
            /{accountId}/vaults/{vaultName}/multipart-uploads:
              GET:
                summary: ListMultipartUploads
                description: >-
                  <p>This operation lists in-progress multipart uploads for the
                  specified vault. An in-progress multipart upload is a
                  multipart upload that has been initiated by an
                  <a>InitiateMultipartUpload</a> request, but has not yet been
                  completed or aborted. The list returned in the List Multipart
                  Upload response has no guaranteed order. </p> <p>The List
                  Multipart Uploads operation supports pagination. By default,
                  this operation returns up to 50 multipart uploads in the
                  response. You should always check the response for a
                  <code>marker</code> at which to continue the list; if there
                  are no more items the <code>marker</code> is
                  <code>null</code>. To return a list of multipart uploads that
                  begins at a specific upload, set the <code>marker</code>
                  request parameter to the value you obtained from a previous
                  List Multipart Upload request. You can also limit the number
                  of uploads returned in the response by specifying the
                  <code>limit</code> parameter in the request.</p> <p>Note the
                  difference between this operation and listing parts
                  (<a>ListParts</a>). The List Multipart Uploads operation lists
                  all multipart uploads for a vault and does not require a
                  multipart upload ID. The List Parts operation requires a
                  multipart upload ID since parts are associated with a single
                  upload.</p> <p>An AWS account has full permission to perform
                  all operations (actions). However, AWS Identity and Access
                  Management (IAM) users don't have any permissions by default.
                  You must grant them explicit permission to perform specific
                  actions. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p>For conceptual information and the
                  underlying REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/working-with-archives.html">Working
                  with Archives in Amazon S3 Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-multipart-list-uploads.html">List
                  Multipart Uploads </a> in the <i>Amazon Glacier Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Multipart
                  - Uploads
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
            /{accountId}/provisioned-capacity:
              POST:
                summary: PurchaseProvisionedCapacity
                description: >-
                  <p>This operation purchases a provisioned capacity unit for an
                  AWS account. </p>
                tags:
                  - Purchase
                  - Provisioned
                  - Capacity
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
                  - Provisioned
                  - Capacity
            /{accountId}/vaults/{vaultName}/tags:
              GET:
                summary: ListTagsForVault
                description: >-
                  <p>This operation lists all the tags attached to a vault. The
                  operation returns an empty map if there are no tags. For more
                  information about tags, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/tagging.html">Tagging
                  Amazon S3 Glacier Resources</a>.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Vault
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
                  - Provisioned
                  - Capacity
                  - Tags
            /{accountId}/vaults:
              GET:
                summary: ListVaults
                description: >-
                  <p>This operation lists all vaults owned by the calling user's
                  account. The list returned in the response is ASCII-sorted by
                  vault name.</p> <p>By default, this operation returns up to 10
                  items. If there are more vaults to list, the response
                  <code>marker</code> field contains the vault Amazon Resource
                  Name (ARN) at which to continue the list with a new List
                  Vaults request; otherwise, the <code>marker</code> field is
                  <code>null</code>. To return a list of vaults that begins at a
                  specific vault, set the <code>marker</code> request parameter
                  to the vault ARN you obtained from a previous List Vaults
                  request. You can also limit the number of vaults returned in
                  the response by specifying the <code>limit</code> parameter in
                  the request. </p> <p>An AWS account has full permission to
                  perform all operations (actions). However, AWS Identity and
                  Access Management (IAM) users don't have any permissions by
                  default. You must grant them explicit permission to perform
                  specific actions. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p>For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/retrieving-vault-info.html">Retrieving
                  Vault Metadata in Amazon S3 Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-vaults-get.html">List
                  Vaults </a> in the <i>Amazon Glacier Developer Guide</i>. </p>
                tags:
                  - Lists
                  - Vaults
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
                  - Provisioned
                  - Capacity
                  - Tags
            /{accountId}/vaults/{vaultName}/tags?operation=remove:
              POST:
                summary: RemoveTagsFromVault
                description: >-
                  <p>This operation removes one or more tags from the set of
                  tags attached to a vault. For more information about tags, see
                  <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/tagging.html">Tagging
                  Amazon S3 Glacier Resources</a>. This operation is idempotent.
                  The operation will be successful, even if there are no tags
                  attached to the vault. </p>
                tags:
                  - Removes
                  - Tags
                  - From
                  - Vault
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
                  - Provisioned
                  - Capacity
                  - Tags
                  - Tags
            /{accountId}/vaults/{vaultName}/archives:
              POST:
                summary: UploadArchive
                description: >-
                  <p>This operation adds an archive to a vault. This is a
                  synchronous operation, and for a successful upload, your data
                  is durably persisted. Amazon S3 Glacier returns the archive ID
                  in the <code>x-amz-archive-id</code> header of the response.
                  </p> <p>You must use the archive ID to access your data in
                  Amazon S3 Glacier. After you upload an archive, you should
                  save the archive ID returned so that you can retrieve or
                  delete the archive later. Besides saving the archive ID, you
                  can also index it and give it a friendly name to allow for
                  better searching. You can also use the optional archive
                  description field to specify how the archive is referred to in
                  an external index of archives, such as you might create in
                  Amazon DynamoDB. You can also get the vault inventory to
                  obtain a list of archive IDs in a vault. For more information,
                  see <a>InitiateJob</a>. </p> <p>You must provide a SHA256 tree
                  hash of the data you are uploading. For information about
                  computing a SHA256 tree hash, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/checksum-calculations.html">Computing
                  Checksums</a>. </p> <p>You can optionally specify an archive
                  description of up to 1,024 printable ASCII characters. You can
                  get the archive description when you either retrieve the
                  archive or get the vault inventory. For more information, see
                  <a>InitiateJob</a>. Amazon Glacier does not interpret the
                  description in any way. An archive description does not need
                  to be unique. You cannot use the description to retrieve or
                  sort the archive list. </p> <p>Archives are immutable. After
                  you upload an archive, you cannot edit the archive or its
                  description.</p> <p>An AWS account has full permission to
                  perform all operations (actions). However, AWS Identity and
                  Access Management (IAM) users don't have any permissions by
                  default. You must grant them explicit permission to perform
                  specific actions. For more information, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/using-iam-with-amazon-glacier.html">Access
                  Control Using AWS Identity and Access Management
                  (IAM)</a>.</p> <p> For conceptual information and underlying
                  REST API, see <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/uploading-an-archive.html">Uploading
                  an Archive in Amazon Glacier</a> and <a
                  href="https://docs.aws.amazon.com/amazonglacier/latest/dev/api-archive-post.html">Upload
                  Archive</a> in the <i>Amazon Glacier Developer Guide
                tags:
                  - Uploads
                  - Archive
                  - Identifiers
                  - Vaults
                  - Vault
                  - Names
                  - Multipart
                  - Uploads
                  - Uploads
                  - Locks
                  - Policies
                  - Tags
                  - Archives
                  - Archive
                  - Access
                  - Notifications
                  - Configurations
                  - Jobs
                  - Jobs
                  - Policies
                  - Data
                  - Retrieval
                  - Output
                  - Provisioned
                  - Capacity
                  - Tags
                  - Tags
    overlays:
      - type: APIs.io Search
        url: overlays/glacier-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/glacier-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:glacier
  - aid: twilio:twilio-voice-api
    name: Twilio Voice API
    description: >-
      Build custom voice call experiences for your applications to reach
      customers around the world.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/en-us/voice
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/en-us/voice
      - type: OpenAPI
        data:
          info:
            title: Twilio - Voice
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Archives/{Date}/Calls/{Sid}:
              description: 'TODO: Resource-level docs'
              delete:
                description: >-
                  Delete an archived call record from Bulk Export. Note: this
                  does not also delete the record from the Voice API.
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
            /v1/ByocTrunks:
              description: >-
                BYOC Trunks allow you to bring your own voice carrier to Twilio,
                enabling your calls to use our Programmable Voice APIs.
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
            /v1/ByocTrunks/{Sid}:
              description: >-
                BYOC Trunks allow you to bring your own voice carrier to Twilio,
                enabling your calls to use our Programmable Voice APIs.
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
              delete:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
            /v1/ConnectionPolicies:
              description: >-
                Connection Policy for sending traffic to your communications
                infrastructure.
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
            /v1/ConnectionPolicies/{Sid}:
              description: >-
                Connection Policy for sending traffic to your communications
                infrastructure.
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
              delete:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
            /v1/ConnectionPolicies/{ConnectionPolicySid}/Targets:
              description: >-
                Network element entry points into your communications
                infrastructure
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
            /v1/ConnectionPolicies/{ConnectionPolicySid}/Targets/{Sid}:
              description: >-
                Network element entry points into your communications
                infrastructure
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
              delete:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
            /v1/DialingPermissions:
              description: 'TODO: Resource-level docs'
            /v1/DialingPermissions/Countries/{IsoCode}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve voice dialing country permissions identified by the
                  given ISO country code
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
            /v1/DialingPermissions/Countries:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve all voice dialing country permissions for this
                  account
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
            /v1/DialingPermissions/BulkCountryUpdates:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Create a bulk update request to change voice dialing country
                  permissions of one or more countries identified by the
                  corresponding [ISO country
                  code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
            /v1/DialingPermissions/Countries/{IsoCode}/HighRiskSpecialPrefixes:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Fetch the high-risk special services prefixes from the country
                  resource corresponding to the [ISO country
                  code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
            /v1/Settings:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve voice dialing permissions inheritance for the
                  sub-account
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
              post:
                description: >-
                  Update voice dialing permissions inheritance for the
                  sub-account
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
            /v1/IpRecords:
              description: >-
                IP Records hold information about the IP addresses and ranges
                ([CIDR](https://tools.ietf.org/html/rfc4632) blocks) that your
                traffic will be associated with.
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
            /v1/IpRecords/{Sid}:
              description: >-
                IP Records hold information about the IP addresses and ranges
                ([CIDR](https://tools.ietf.org/html/rfc4632) blocks) that your
                traffic will be associated with.
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
              delete:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
            /v1/SourceIpMappings:
              description: >-
                With Source IP Mappings, Twilio can recognize your SIP requests
                based on where they are sent from. The Request-URI no longer has
                to have the FQDN (Fully Qualified Domain Name) of your SIP
                Domain.
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
                  - Source
                  - Mappings
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
                  - Source
                  - Mappings
            /v1/SourceIpMappings/{Sid}:
              description: >-
                With Source IP Mappings, Twilio can recognize your SIP requests
                based on where they are sent from. The Request-URI no longer has
                to have the FQDN (Fully Qualified Domain Name) of your SIP
                Domain.
              get:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
                  - Source
                  - Mappings
              post:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
                  - Source
                  - Mappings
              delete:
                description: ''
                tags:
                  - Archives
                  - Date
                  - Calls
                  - Sid
                  - Byoc
                  - Trunks
                  - Connection
                  - Policies
                  - Policy
                  - Targets
                  - Dialing
                  - Permissions
                  - Countries
                  - Iso
                  - Code
                  - Bulk
                  - Country
                  - Updates
                  - High
                  - Risk
                  - Special
                  - Prefixes
                  - Settings
                  - Ip
                  - Records
                  - Source
                  - Mappings
          tags:
            - name: VoiceV1ArchivedCall
            - name: VoiceV1BulkCountryUpdate
            - name: VoiceV1ByocTrunk
            - name: VoiceV1ConnectionPolicy
            - name: VoiceV1ConnectionPolicyTarget
            - name: VoiceV1Country
            - name: VoiceV1HighriskSpecialPrefix
            - name: VoiceV1IpRecord
            - name: VoiceV1Settings
            - name: VoiceV1SourceIpMapping
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. Use it with caution.
            - name: Preview
              description: >-
                PLEASE NOTE that this is a Preview product that is subject to
                change. Use it with caution. If you currently do not have
                developer preview access, please contact https://www.twilio
    overlays:
      - type: APIs.io Search
        url: overlays/voice-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/voice-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---