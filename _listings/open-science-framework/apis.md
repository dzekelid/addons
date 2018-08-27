---
name: Open Science Framework
x-slug: open-science-framework
description: OSF provides free and open source project management support for researchers
  across the entire research lifecycle. As a collaboration tool, OSF helps researchers
  work on projects privately with a limited number of collaborators and make parts
  of their projects public, or make all the project publicly accessible for broader
  dissemination. As a workflow system, OSF enables connections to the many services
  researchers already use to streamline their process and increase efficiency. As
  a flexible repository, it can store and archive research data, protocols, and materials.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: AddOns
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/apis.md
specificationVersion: "0.14"
apis:
- name: Open Science Framework - List all addons
  x-api-slug: addons-get
  description: |-
    A paginated list of addons configurable with the OSF
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 addons. Each resource in the array is a separate addon object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    This request should never return an error.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/addons-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/addons-get-openapi.md
- name: Open Science Framework - List all addons
  x-api-slug: nodesnode-idaddons-get
  description: |-
    A paginated list of addons connected to the given node or project.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of at most 10 addon objects. Each resource in the array is a separate addon object and contains the full representation of the addon, meaning additional requests to a addon's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddons-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddons-get-openapi.md
- name: Open Science Framework - Retrieve an addon
  x-api-slug: nodesnode-idaddonsprovider-get
  description: |-
    Retrieve details of an individual addon connected to this node.
    #### Permissions
    NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
    Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.
    #### Returns
    Returns a JSON object with a `data` key containing the details of the requested addon, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddonsprovider-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddonsprovider-get-openapi.md
- name: Open Science Framework - Update an addon
  x-api-slug: nodesnode-idaddonsprovider-patch
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddonsprovider-patch-openapi.md
- name: Open Science Framework - List all addon folders
  x-api-slug: nodesnode-idaddonsproviderfolders-get
  description: |-
    A paginated list of folders retrieved from the associated third-party (provider) service.
    #### Permissions
    Folders are visible only to the user that authorized the addon.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of addon folder objects. Each resource in the array is a separate addon folder object and contains the full representation of the addon folder, meaning additional requests to a addon folder's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/nodesnode-idaddonsproviderfolders-get-openapi.md
- name: Open Science Framework - List all user addons
  x-api-slug: usersuser-idaddons-get
  description: |-
    A paginated list of authorized user addons

    #### Permissions

    User addons are visible only to the user that authorized the addon.

    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 addons. Each resource in the array is a separate addon object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.

    Attempting to request the accounts for an addon that is not enabled will result in a **404 Not Found** response.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddons-get-openapi.md
- name: Open Science Framework - Retrieve a user addon
  x-api-slug: usersuser-idaddonsprovider-get
  description: |-
    Retrieves the details of an authorized user addon

    #### Permissions

    User addons are visible only to the user that authorized the addon.

    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested user addon, if the request was successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.

    Attempting to request the accounts for an addon that is not enabled will result in a **404 Not Found** response.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddonsprovider-get-openapi.md
- name: Open Science Framework - List all addon accounts
  x-api-slug: usersuser-idaddonsprovideraccounts-get
  description: |-
    A paginated list of addon accounts authorized by this user.

    #### Permissions

    Addon accounts are visible only to the user that authorized the account.

    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of at most 10 addon account objects. Each resource in the array is a separate  addon account object and contains the full representation of the addon account.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddonsprovideraccounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddonsprovideraccounts-get-openapi.md
- name: Open Science Framework - Retrieve an addon account
  x-api-slug: usersuser-idaddonsprovideraccountsaccount-id-get
  description: |-
    Retrieves the details of an addon account

    #### Permissions

    Addon accounts are visible only to the user that authorized the account.

    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested addon account, if the request was successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Research, Science, API Provider, Profiles, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddonsprovideraccountsaccount-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/addons/master/_listings/open-science-framework/usersuser-idaddonsprovideraccountsaccount-id-get-openapi.md
x-common:
- type: x-website
  url: https://cos.io
- type: x-api-gallery
  url: http://open.fintech.api.gallery.streamdata.io
- type: x-api-stack
  url: http://open.science.framework.stack.network
- type: x-github
  url: https://github.com/OSFramework
- type: x-twitter
  url: https://twitter.com/OSFramework
- type: x-website
  url: http://osf.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---