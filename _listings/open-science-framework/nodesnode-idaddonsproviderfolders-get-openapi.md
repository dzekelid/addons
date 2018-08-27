---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework List all addon folders
  description: |-
    A paginated list of folders retrieved from the associated third-party (provider) service.
    #### Permissions
    Folders are visible only to the user that authorized the addon.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of addon folder objects. Each resource in the array is a separate addon folder object and contains the full representation of the addon folder, meaning additional requests to a addon folder's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /addons/:
    get:
      summary: List all addons
      description: |-
        A paginated list of addons configurable with the OSF
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of up to 10 addons. Each resource in the array is a separate addon object.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        This request should never return an error.
      operationId: addons_list
      x-api-path-slug: addons-get
      responses:
        200:
          description: OK
      tags:
      - Addons
  /nodes/{node_id}/addons/:
    get:
      summary: List all addons
      description: |-
        A paginated list of addons connected to the given node or project.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of at most 10 addon objects. Each resource in the array is a separate addon object and contains the full representation of the addon, meaning additional requests to a addon's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
      operationId: nodes_addons_list
      x-api-path-slug: nodesnode-idaddons-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
  /nodes/{node_id}/addons/{provider}/:
    get:
      summary: Retrieve an addon
      description: |-
        Retrieve details of an individual addon connected to this node.
        #### Permissions
        NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
        Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.
        #### Returns
        Returns a JSON object with a `data` key containing the details of the requested addon, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_addon_read
      x-api-path-slug: nodesnode-idaddonsprovider-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the addon
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
    patch:
      summary: Update an addon
      description: |-
        Updates a node addon by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

        Node addon can be updated with either a **PUT** or **PATCH** request. The `external_account_id`, `enabled`, and `folder_id` fields are mandatory in a **PUT**, and optional in **PATCH**. Non-string values will be accepted and stringified, however we make no promises about the stringification output.

        To delete or deauthorize a node addon, issue a **PUT** with all fields set to `null` or `False`, or a **PATCH** with enabled set `False`.
        #### Permissions
        NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
        Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.

        #### Returns
        Returns a JSON object with a `data` key containing the new representation of the updated node addon, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_node_addon_update
      x-api-path-slug: nodesnode-idaddonsprovider-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the addon
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
  /nodes/{node_id}/addons/{provider}/folders/:
    get:
      summary: List all addon folders
      description: |-
        A paginated list of folders retrieved from the associated third-party (provider) service.
        #### Permissions
        Folders are visible only to the user that authorized the addon.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of addon folder objects. Each resource in the array is a separate addon folder object and contains the full representation of the addon folder, meaning additional requests to a addon folder's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
      operationId: nodes_addons_folders_list
      x-api-path-slug: nodesnode-idaddonsproviderfolders-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the provider
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
      - Folders
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