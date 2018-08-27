swagger: "2.0"
x-collection-name: Heroku
x-complete: 1
info:
  title: Heroku
  description: manage-your-heroku-apps-configs-collaborators--resources
  version: "1"
host: api.heroku.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /addons:
    parameters:
      summary: Parameters Addons
      description: Parameters addons.
      operationId: parametersAddons
      x-api-path-slug: addons-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - ons
    get:
      summary: Get Addons
      description: List all available addons.
      operationId: getAddons
      x-api-path-slug: addons-get
      parameters:
      - in: header
        name: Accept
        description: Content type
      - in: query
        name: Accept
        description: Content type
      responses:
        200:
          description: OK
      tags:
      - ons
  /apps/{app}/addons:
    parameters:
      summary: Parameter Application Addons
      description: Parameter application addons.
      operationId: parametersAppsAppAddons
      x-api-path-slug: appsappaddons-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameter
      - Application
      - ons
    get:
      summary: Get Application Addons
      description: List addons installed on an app.
      operationId: getAppsAppAddons
      x-api-path-slug: appsappaddons-get
      parameters:
      - in: header
        name: Accept
        description: Content type
      - in: query
        name: Accept
        description: Content type
      - in: query
        name: app
        description: The app name
      - in: path
        name: app
      responses:
        200:
          description: OK
      tags:
      - Application
      - ons
  /apps/{app}/addons/{addon}:
    parameters:
      summary: Parameters Applications Addons
      description: Parameters applications addons.
      operationId: parametersAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Applications
      - ons
    post:
      summary: Add Application Addons
      description: Install an addon to an app.
      operationId: postAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-post
      parameters:
      - in: header
        name: Accept
        description: Content type
      - in: query
        name: Accept
        description: Content type
      - in: query
        name: addon
        description: the addon name
      - in: path
        name: addon
      - in: query
        name: app
        description: The app name
      - in: path
        name: app
      responses:
        200:
          description: OK
      tags:
      - Application
      - ons
    put:
      summary: Put Application Addons
      description: Upgrade an addon to an app.
      operationId: putAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-put
      parameters:
      - in: header
        name: Accept
        description: Content type
      - in: query
        name: Accept
        description: Content type
      - in: query
        name: addon
        description: the addon name
      - in: path
        name: addon
      - in: query
        name: app
        description: The app name
      - in: path
        name: app
      responses:
        200:
          description: OK
      tags:
      - Put
      - Application
      - ons
    delete:
      summary: Delete Applications Addons
      description: Uninstall an addon from an app.
      operationId: deleteAppsAppAddonsAddon
      x-api-path-slug: appsappaddonsaddon-delete
      parameters:
      - in: header
        name: Accept
        description: Content type
      - in: query
        name: Accept
        description: Content type
      - in: query
        name: addon
        description: the addon name
      - in: path
        name: addon
      - in: query
        name: app
        description: The app name
      - in: path
        name: app
      responses:
        200:
          description: OK
      tags:
      - Applications
      - ons