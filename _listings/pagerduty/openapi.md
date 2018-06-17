---
swagger: "2.0"
x-collection-name: PagerDuty
x-complete: 1
info:
  title: PagerDuty
  version: 1.0.0
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
    put:
      summary: Update an add-on
      description: Update an existing add-on.
      operationId: update-an-existing-addon
      x-api-path-slug: addonsid-put
      parameters:
      - in: body
        name: addon
        description: The add-on to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - AddOns
---