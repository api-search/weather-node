---
name: Choice
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/choice.png
url: https://example.com/apis/choice.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Choice
apis:
  - name: FactSet BookBuilder API
    description: >-
      The BookBuilder API is a powerful tool that quickly combines FactSet’s
      detailed reports for companies of interest into polished pdfs that can be
      read, saved down, and shared with others.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/bookbuilder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/bookbuilder-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/bookbuilder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/bookbuilder-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/bookbuilder-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/bookbuilder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: BookBuilder
          tags: []
          paths:
            /v1/book-list:
              get:
                tags:
                  - Check
                  - Out
                  - The
                  - Books
                  - That
                  - Are
                  - In
                  - Book
                  - Library
                  - V1
                  - Book
                  - List
                summary: Check out the books that are in the book library
                description: >-
                  Retrieves the list of books that were previously created and
                  are available in the client's book library
            /v1/template-list:
              get:
                tags:
                  - Retrieves
                  - The
                  - List
                  - Of
                  - Templates
                  - That
                  - Are
                  - Available
                  - V1
                  - Book
                  - List
                  - Template
                summary: Retrieves the list of templates that are available
                description: >-
                  A template is a predefined list of content to be compiled in a
                  PDF. This end point works without any parameters and retrieves
                  the list of templates available for the user. Templates need
                  to defined/created in FactSet workstation.
            /v1/create-template/:
              post:
                tags:
                  - Kick
                  - 'Off'
                  - Request
                  - To
                  - Create
                  - Template
                  - With
                  - Reports
                  - Of
                  - Your
                  - Choice
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                summary: >-
                  Kick off request to create template with reports of your
                  choice
                description: >-
                  This end point retrieves template name and template_id of the
                  template you create. All the book options such as name of the
                  template, type, and reports can be specified in the request
                  body. Please refer to the documentation for valid section ids
                  and report ids.
            /v1/create-book:
              post:
                tags:
                  - Kicks
                  - 'Off'
                  - Request
                  - To
                  - Create
                  - Book
                  - With
                  - Reports
                  - Of
                  - Your
                  - Choice
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                summary: Kicks off request to create a book with reports of your choice
                description: >-
                  This end point retrieves book name and book_id for the PDF
                  book you create. All the book options such as name of the
                  book, ticker, pagination options, and reports can be specified
                  in the request body. Please refer to the documentation for
                  valid section ids and report ids.
            /v1/create-book-from-template:
              post:
                tags:
                  - Kicks
                  - 'Off'
                  - Request
                  - To
                  - Create
                  - Book
                  - With
                  - Template
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                  - From
                summary: Kicks off request to create a book with template
                description: >-
                  This endpoint retrieves book status, book name, and book ID
                  for ticker requested in JSON format. This end-point excepts
                  ticker and template_id as inputs. If the template_id input is
                  not used, a book will be created with FactSet's default
                  template.</br></br>Please try out the below template ids to
                  quickly get the FactSet curated books</br></br>Company Quick
                  Book - <b>g_20210415065838185</b></br>Post-Earnings Call -
                  <b>g_20210415070044785</b> </br>Public Information Book(PIB) -
                  <b>g_20210415070353151</b></br></br> Take a look at the
                  example books attached under API documentation
                  below.</br></br>If you are scheduling Post Earnings Call
                  curated book, please note that in contains Corrected
                  Transcript that takes a little while to be available.</br>
                  </br>Once a Raw Transcript is published, FactSet's editors
                  review the call to produce a Corrected Transcript. They listen
                  to the entire audio file again to confirm that all of the
                  terms and numbers are correctly transcribed. FactSet aims to
                  publish a Corrected Transcript within six times the length of
                  the event, measured from the beginning of the event. That
                  means for a typical one-hour call, FactSet will produce a
                  Corrected Transcript within approximately five hours of the
                  call's completion. Visit [OA
                  13208](https://my.apps.factset.com/oa/pages/13208)
            /v1/download-api-book-aws/{book_id}:
              get:
                tags:
                  - Retrieves
                  - Book
                  - In
                  - Format
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                  - From
                  - Download
                  - Api
                  - Aws
                  - Book_id
                summary: Retrieves book in PDF format
                description: >-
                  This endpoint uses the BookId returned from any of the request
                  above. Returns the URL to load the book for the book ID
                  requested. The URL will be in JSON format, the final book will
                  be in PDF format. <br><br> NOTE -- The execution of this
                  endpoint requires an extra step within the developer portal
                  due to authentication limitations. When using the actual API,
                  a successful response for this endpoint will be the PDF book
                  rather than the URL to the PDF. <br><br><b><i>The actual
                  endpoint is </b><font
                  color=blue>https://api.factset.com/book-builder-api/v1/download-api-book/{book_id}</font></i>
            /v1/upload-custom-document:
              post:
                tags:
                  - Upload
                  - Custom
                  - Document
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                  - From
                  - Download
                  - Api
                  - Aws
                  - Book_id
                  - Upload
                  - Custom
                  - Document
                summary: Upload a custom document
                description: >-
                  Upload any thrid-party documents that need to be included in
                  the final PDF. Once uploaded, the successful response will be
                  a unique fileurl that can be used to add the files to the PDF
                  output using the create-book endpoint. Supported files include
                  Powerpoint, Word, RTF and PDF. The total size should not
                  exceed 250MB and each file should not exceed 10MB.
            /v1/custom-upload-list:
              get:
                tags:
                  - Check
                  - Out
                  - The
                  - Documents
                  - Uploaded
                  - Before
                  - To
                  - Use
                  - Them
                  - In
                  - Creating
                  - Books
                  - V1
                  - Book
                  - List
                  - Template
                  - Create
                  - From
                  - Download
                  - Api
                  - Aws
                  - Book_id
                  - Upload
                  - Custom
                  - Document
                summary: >-
                  Check out the documents uploaded before to use them in
                  creating books
                description: >-
                  Retrieves the list of documents uploaded before using the
                  endpoint "/upload-custom-document". The documents uploaded are
                  available for 30 days from th
    overlays:
      - type: APIs.io Search
        url: overlays/bookbuilder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/bookbuilder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-bookbuilder-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---