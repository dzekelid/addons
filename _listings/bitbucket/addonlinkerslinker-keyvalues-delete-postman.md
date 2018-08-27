{
  "info": {
    "name": "Bitbucket Delete Add On Linkers Linker Key Values",
    "_postman_id": "92ae63e9-4b21-48af-a921-c0c23e91d417",
    "description": "Delete addon linkers linker key values",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "a8ddfb66-0c52-456d-b4d0-affdcaab451e",
          "name": "deleteAddonLinkersLinkerKeyValues",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "addon/linkers/:linker_key/values"
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
              "id": "da950194-6362-4203-94a5-2040d09f632e"
            }
          ]
        }
      ]
    }
  ]
}