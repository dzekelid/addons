---
swagger: "2.0"
x-collection-name: PagerDuty
x-complete: 0
info:
  title: PagerDuty List installed add-ons
  version: 1.0.0
  description: List all of the add-ons installed on your account.
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