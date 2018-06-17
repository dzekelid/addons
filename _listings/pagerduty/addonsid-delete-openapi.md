---
swagger: "2.0"
x-collection-name: PagerDuty
x-complete: 0
info:
  title: PagerDuty Delete an add-on
  version: 1.0.0
  description: Remove an existing add-on.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /addons:
    get:
      summary: List installed add-ons
      description: List all of the add-ons installed on your account.
      operationId: list-all-of-the-addons-installed-on-your-account
      x-api-path-slug: addons-get
      parameters:
      - in: query
        name: filter
        description: Filters the results, showing only add-ons of the given type
      - in: query
        name: No Name
      - in: query
        name: service_ids[]
        description: Filters the results, showing only add-ons for the given services
      responses:
        200:
          description: OK
      tags:
      - AddOns
    post:
      summary: Install an add-on
      description: Install an add-on for your account.
      operationId: install-an-addon-for-your-account
      x-api-path-slug: addons-post
      parameters:
      - in: body
        name: addon
        description: The add-on to be installed
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - AddOns
  /addons/{id}:
    get:
      summary: Get an add-on
      description: Get details about an existing add-on.
      operationId: get-details-about-an-existing-addon
      x-api-path-slug: addonsid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - AddOns
    delete:
      summary: Delete an add-on
      description: Remove an existing add-on.
      operationId: remove-an-existing-addon
      x-api-path-slug: addonsid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - AddOns
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---