{
  "info": {
    "name": "Bitbucket Get Add On Linkers Linker Key Values",
    "_postman_id": "2a9444e9-7d9a-45ec-bc0f-775af4145914",
    "description": "Get addon linkers linker key values",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "fe322740-c27d-4e5f-8139-7543588eeac5",
          "name": "getAddonLinkersLinkerKeyValues",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "addon/linkers/:linker_key/values/"
              ],
              "variable": [
                {
                  "id": "linker_key",
                  "value": "linker_key",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get addon linkers linker key values"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "33d90111-486c-472d-8247-daf609460473"
            }
          ]
        },
        {
          "id": "d7b37ba8-cd27-4d65-8587-4557469b079f",
          "name": "deleteAddonLinkersLinkerKeyValues",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "addon/linkers/:linker_key/values/"
              ],
              "variable": [
                {
                  "id": "linker_key",
                  "value": "linker_key",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete addon linkers linker key values"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "46671851-c090-4d2e-aca2-1a09ace0e36a"
            }
          ]
        }
      ]
    }
  ]
}