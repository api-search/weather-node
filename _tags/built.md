---
name: Built
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/built.png
url: https://example.com/apis/built.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Built
apis:
  - name: models.lex.v2
    description: <p/>
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
            title: models.lex.v2
          paths:
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchcreate:
              PUT:
                summary: BatchCreateCustomVocabularyItem
                description: >-
                  <p>Create a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Create
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchdelete:
              POST:
                summary: BatchDeleteCustomVocabularyItem
                description: >-
                  <p>Delete a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Delete
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchupdate:
              PUT:
                summary: BatchUpdateCustomVocabularyItem
                description: >-
                  <p>Update a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Update
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/:
              PUT:
                summary: UpdateBotLocale
                description: >-
                  <p>Updates the settings that a bot has for a specific
                  locale.</p>
                tags:
                  - Update
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/:
              POST:
                summary: ListBots
                description: <p>Gets a list of available bots.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
            /bots/{botId}/botaliases/:
              POST:
                summary: ListBotAliases
                description: <p>Gets a list of aliases for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Aliases
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/botversions/{botVersion}/botlocales/:
              POST:
                summary: ListBotLocales
                description: <p>Gets a list of locales for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/replicas/:
              POST:
                summary: ListBotReplicas
                description: <p>The action to list the replicated bots.</p>
                tags:
                  - Lists
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /bots/{botId}/botversions/:
              POST:
                summary: ListBotVersions
                description: >-
                  <p>Gets information about all of the versions of a bot.</p>
                  <p>The <code>ListBotVersions</code> operation returns a
                  summary of each version of a bot. For example, if a bot has
                  three numbered versions, the <code>ListBotVersions</code>
                  operation returns for summaries, one for each numbered version
                  and one for the <code>DRAFT</code> version.</p> <p>The
                  <code>ListBotVersions</code> operation always returns at least
                  one version, the <code>DRAFT</code> version.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /exports/:
              POST:
                summary: ListExports
                description: >-
                  <p>Lists the exports for a bot, bot locale, or custom
                  vocabulary. Exports are kept in the list for 7 days.</p>
                tags:
                  - Lists
                  - Exports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/:
              POST:
                summary: ListIntents
                description: <p>Get a list of intents that meet the specified criteria.</p>
                tags:
                  - Lists
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
            /policy/{resourceArn}/:
              PUT:
                summary: UpdateResourcePolicy
                description: >-
                  <p>Replaces the existing resource policy for a bot or bot
                  alias with a new one. If the policy doesn't exist, Amazon Lex
                  returns an exception.</p>
                tags:
                  - Update
                  - Resources
                  - Policies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
            /policy/{resourceArn}/statements/:
              POST:
                summary: CreateResourcePolicyStatement
                description: >-
                  <p>Adds a new resource policy statement to a bot or bot alias.
                  If a resource policy exists, the statement is added to the
                  current resource policy. If a policy doesn't exist, a new
                  policy is created.</p> <p>You can't create a resource policy
                  statement that allows cross-account access.</p>
                tags:
                  - Create
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/:
              POST:
                summary: ListSlots
                description: <p>Gets a list of slots that match the specified criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/:
              POST:
                summary: ListSlotTypes
                description: >-
                  <p>Gets a list of slot types that match the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
            /testsets/{testSetId}/testsetdiscrepancy:
              POST:
                summary: CreateTestSetDiscrepancyReport
                description: >-
                  <p>Create a report that describes the differences between the
                  bot and the test set.</p>
                tags:
                  - Create
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
            /createuploadurl/:
              POST:
                summary: CreateUploadUrl
                description: >-
                  <p>Gets a pre-signed S3 write URL that you use to upload the
                  zip archive when importing a bot or a bot locale. </p>
                tags:
                  - Create
                  - Uploads
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/:
              PUT:
                summary: UpdateBot
                description: <p>Updates the configuration of an existing bot. </p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/botaliases/{botAliasId}/:
              PUT:
                summary: UpdateBotAlias
                description: <p>Updates the configuration of an existing bot alias.</p>
                tags:
                  - Update
                  - Bot
                  - Alias
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
            /bots/{botId}/replicas/{replicaRegion}/:
              GET:
                summary: DescribeBotReplica
                description: >-
                  <p>Monitors the bot replication status through the UI
                  console.</p>
                tags:
                  - Describe
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/:
              GET:
                summary: DescribeBotVersion
                description: <p>Provides metadata about a version of a bot.</p>
                tags:
                  - Describe
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary:
              DELETE:
                summary: DeleteCustomVocabulary
                description: >-
                  <p>Removes a custom vocabulary from the specified locale in
                  the specified bot.</p>
                tags:
                  - Delete
                  - Custom
                  - Vocabularies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /exports/{exportId}/:
              PUT:
                summary: UpdateExport
                description: >-
                  <p>Updates the password used to protect an export zip
                  archive.</p> <p>The password is not required. If you don't
                  supply a password, Amazon Lex generates a zip file that is not
                  protected by a password. This is the archive that is available
                  at the pre-signed S3 URL provided by the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_DescribeExport.html">DescribeExport</a>
                  operation.</p>
                tags:
                  - Update
                  - Export
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /imports/{importId}/:
              GET:
                summary: DescribeImport
                description: <p>Gets information about a specific import.</p>
                tags:
                  - Describe
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/:
              PUT:
                summary: UpdateIntent
                description: <p>Updates the settings for an intent.</p>
                tags:
                  - Update
                  - Intent
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /policy/{resourceArn}/statements/{statementId}/:
              DELETE:
                summary: DeleteResourcePolicyStatement
                description: >-
                  <p>Deletes a policy statement from a resource policy. If you
                  delete the last statement from a policy, the policy is
                  deleted. If you specify a statement ID that doesn't exist in
                  the policy, or if the bot or bot alias doesn't have a policy
                  attached, Amazon Lex returns an exception.</p>
                tags:
                  - Delete
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/{slotId}/:
              PUT:
                summary: UpdateSlot
                description: <p>Updates the settings for a slot.</p>
                tags:
                  - Update
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/{slotTypeId}/:
              PUT:
                summary: UpdateSlotType
                description: <p>Updates the configuration of an existing slot type.</p>
                tags:
                  - Update
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /testsets/{testSetId}:
              PUT:
                summary: UpdateTestSet
                description: <p>The action to update the test set.</p>
                tags:
                  - Update
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /bots/{botId}/utterances/:
              DELETE:
                summary: DeleteUtterances
                description: >-
                  <p>Deletes stored utterances.</p> <p>Amazon Lex stores the
                  utterances that users send to your bot. Utterances are stored
                  for 15 days for use with the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, and then stored indefinitely for use in improving
                  the ability of your bot to respond to user input..</p> <p>Use
                  the <code>DeleteUtterances</code> operation to manually delete
                  utterances for a specific session. When you use the
                  <code>DeleteUtterances</code> operation, utterances stored for
                  improving your bot's ability to respond to user input are
                  deleted immediately. Utterances stored for use with the
                  <code>ListAggregatedUtterances</code> operation are deleted
                  after 15 days.</p>
                tags:
                  - Delete
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/:
              PUT:
                summary: UpdateBotRecommendation
                description: <p>Updates an existing bot recommendation request.</p>
                tags:
                  - Update
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations/{generationId}:
              GET:
                summary: DescribeBotResourceGeneration
                description: >-
                  <p>Returns information about a request to generate a bot
                  through natural language description, made through the
                  <code>StartBotResource</code> API. Use the
                  <code>generatedBotLocaleUrl</code> to retrieve the Amazon S3
                  object containing the bot locale configuration. You can then
                  modify and import this configuration.</p>
                tags:
                  - Describe
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/metadata:
              GET:
                summary: DescribeCustomVocabularyMetadata
                description: >-
                  <p>Provides metadata information about a custom
                  vocabulary.</p>
                tags:
                  - Describe
                  - Custom
                  - Vocabularies
                  - Metadata
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
            /testexecutions/{testExecutionId}:
              GET:
                summary: DescribeTestExecution
                description: <p>Gets metadata information about the test execution.</p>
                tags:
                  - Describe
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
            /testsetdiscrepancy/{testSetDiscrepancyReportId}:
              GET:
                summary: DescribeTestSetDiscrepancyReport
                description: >-
                  <p>Gets metadata information about the test set discrepancy
                  report.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /testsetgenerations/{testSetGenerationId}:
              GET:
                summary: DescribeTestSetGeneration
                description: >-
                  <p>Gets metadata information about the test set
                  generation.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generate:
              POST:
                summary: GenerateBotElement
                description: <p>Generates sample utterances for an intent.</p>
                tags:
                  - Generate
                  - Bot
                  - Elements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
            /testexecutions/{testExecutionId}/artifacturl:
              GET:
                summary: GetTestExecutionArtifactsUrl
                description: >-
                  <p>The pre-signed Amazon S3 URL to download the test execution
                  result artifacts.</p>
                tags:
                  - Get
                  - Tests
                  - Execution
                  - Artifacts
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
            /bots/{botId}/aggregatedutterances/:
              POST:
                summary: ListAggregatedUtterances
                description: >-
                  <p>Provides a list of utterances that users have sent to the
                  bot.</p> <p>Utterances are aggregated by the text of the
                  utterance. For example, all instances where customers used the
                  phrase "I want to order pizza" are aggregated into the same
                  line in the response.</p> <p>You can see both detected
                  utterances and missed utterances. A detected utterance is
                  where the bot properly recognized the utterance and activated
                  the associated intent. A missed utterance was not recognized
                  by the bot and didn't activate an intent.</p> <p>Utterances
                  can be aggregated for a bot alias or for a bot version, but
                  not both at the same time.</p> <p>Utterances statistics are
                  not generated under the following conditions:</p> <ul> <li>
                  <p>The <code>childDirected</code> field was set to true when
                  the bot was created.</p> </li> <li> <p>You are using slot
                  obfuscation with one or more slots.</p> </li> <li> <p>You
                  opted out of participating in improving Amazon Lex.</p> </li>
                  </ul>
                tags:
                  - Lists
                  - Aggregated
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botaliases/:
              POST:
                summary: ListBotAliasReplicas
                description: >-
                  <p>The action to list the replicated bots created from the
                  source bot alias.</p>
                tags:
                  - Lists
                  - Bot
                  - Alias
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/:
              PUT:
                summary: StartBotRecommendation
                description: >-
                  <p>Use this to provide your transcript data, and to start the
                  bot recommendation process.</p>
                tags:
                  - Start
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations:
              POST:
                summary: ListBotResourceGenerations
                description: <p>Lists the generation requests made for a bot locale.</p>
                tags:
                  - Lists
                  - Bot
                  - Resources
                  - Generations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botversions/:
              POST:
                summary: ListBotVersionReplicas
                description: >-
                  <p>Contains information about all the versions replication
                  statuses applicable for Global Resiliency.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/intents/:
              POST:
                summary: ListBuiltInIntents
                description: >-
                  <p>Gets a list of built-in intents provided by Amazon Lex that
                  you can use in your bot. </p> <p>To use a built-in intent as a
                  the base for your own intent, include the built-in intent
                  signature in the <code>parentIntentSignature</code> parameter
                  when you call the <code>CreateIntent</code> operation. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_CreateIntent.html">CreateIntent</a>.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/slottypes/:
              POST:
                summary: ListBuiltInSlotTypes
                description: >-
                  <p>Gets a list of built-in slot types that meet the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/list:
              POST:
                summary: ListCustomVocabularyItems
                description: >-
                  <p>Paginated list of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Lists
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
            /imports/:
              PUT:
                summary: StartImport
                description: >-
                  <p>Starts importing a bot, bot locale, or custom vocabulary
                  from a zip archive that you uploaded to an S3 bucket.</p>
                tags:
                  - Start
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
            /bots/{botId}/analytics/intentmetrics:
              POST:
                summary: ListIntentMetrics
                description: >-
                  <p>Retrieves summary metrics for the intents in your bot. The
                  following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentMetric.html">AnalyticsIntentMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can specify
                  only one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
            /bots/{botId}/analytics/intentpaths:
              POST:
                summary: ListIntentPaths
                description: >-
                  <p>Retrieves summary statistics for a path of intents that
                  users take over sessions with your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> <li> <p>
                  <code>intentPath</code> – Define an order of intents for which
                  you want to retrieve metrics. Separate intents in the path
                  with a forward slash. For example, populate the
                  <code>intentPath</code> field with
                  <code>/BookCar/BookHotel</code> to see details about how many
                  times users invoked the <code>BookCar</code> and
                  <code>BookHotel</code> intents in that order.</p> </li> </ul>
                  <p>Use the optional <code>filters</code> field to filter the
                  results.</p>
                tags:
                  - Lists
                  - Intent
                  - Paths
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
            /bots/{botId}/analytics/intentstagemetrics:
              POST:
                summary: ListIntentStageMetrics
                description: >-
                  <p>Retrieves summary metrics for the stages within intents in
                  your bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentStageMetric.html">AnalyticsIntentStageMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can only
                  specify one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Stage
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/intents:
              POST:
                summary: ListRecommendedIntents
                description: >-
                  <p>Gets a list of recommended intents provided by the bot
                  recommendation that you can use in your bot. Intents in the
                  response are ordered by relevance.</p>
                tags:
                  - Lists
                  - Recommended
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/analytics/sessions:
              POST:
                summary: ListSessionAnalyticsData
                description: >-
                  <p>Retrieves a list of metadata for individual user sessions
                  with your bot. The <code>startDateTime</code> and
                  <code>endDateTime</code> fields are required. These fields
                  define a time range for which you want to retrieve results. Of
                  the optional fields, you can organize the results in the
                  following ways:</p> <ul> <li> <p>Use the <code>filters</code>
                  field to filter the results and the <code>sortBy</code> field
                  to specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Sessions
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
            /bots/{botId}/analytics/sessionmetrics:
              POST:
                summary: ListSessionMetrics
                description: >-
                  <p>Retrieves summary metrics for the user sessions with your
                  bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsSessionMetric.html">AnalyticsSessionMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Sessions
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
            /tags/{resourceARN}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a bot, bot alias, or bot channel.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
            /testexecutions/{testExecutionId}/results:
              POST:
                summary: ListTestExecutionResultItems
                description: <p>Gets a list of test execution result items.</p>
                tags:
                  - Lists
                  - Tests
                  - Execution
                  - Results
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
            /testexecutions:
              POST:
                summary: ListTestExecutions
                description: <p>The list of test set executions.</p>
                tags:
                  - Lists
                  - Tests
                  - Executions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
            /testsets/{testSetId}/records:
              POST:
                summary: ListTestSetRecords
                description: <p>The list of test set records.</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Records
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
            /testsets:
              POST:
                summary: ListTestSets
                description: <p>The list of the test sets</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterances:
              POST:
                summary: ListUtteranceAnalyticsData
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves a list of metadata for
                  individual user utterances to your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results and the <code>sortBy</code> field to
                  specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Utterances
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterancemetrics:
              POST:
                summary: ListUtteranceMetrics
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves summary metrics for the
                  utterances in your bot. The following fields are required:</p>
                  <ul> <li> <p> <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsUtteranceMetric.html">AnalyticsUtteranceMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Utterances
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/associatedtranscripts:
              POST:
                summary: SearchAssociatedTranscripts
                description: >-
                  <p>Search for associated transcripts that meet the specified
                  criteria.</p>
                tags:
                  - Search
                  - Associated
                  - Transcripts
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/startgeneration:
              PUT:
                summary: StartBotResourceGeneration
                description: >-
                  <p>Starts a request for the descriptive bot builder to
                  generate a bot locale configuration based on the prompt you
                  provide it. After you make this call, use the
                  <code>DescribeBotResourceGeneration</code> operation to check
                  on the status of the generation and for the
                  <code>generatedBotLocaleUrl</code> when the generation is
                  complete. Use that value to retrieve the Amazon S3 object
                  containing the bot locale configuration. You can then modify
                  and import this configuration.</p>
                tags:
                  - Start
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsets/{testSetId}/testexecutions:
              POST:
                summary: StartTestExecution
                description: <p>The action to start test set execution.</p>
                tags:
                  - Start
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsetgenerations:
              PUT:
                summary: StartTestSetGeneration
                description: <p>The action to start the generation of test set.</p>
                tags:
                  - Start
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/stopbotrecommendation:
              PUT:
                summary: StopBotRecommendation
                description: <p>Stop an already running Bot Recommendation re
                tags:
                  - Stop
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
                  - Stopbotrecommendati
    overlays:
      - type: APIs.io Search
        url: overlays/modelslexv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/modelslexv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:modelslexv2
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---