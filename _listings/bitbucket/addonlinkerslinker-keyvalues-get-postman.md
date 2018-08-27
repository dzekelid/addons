{
  "info": {
    "name": "Bitbucket Get Add On Linkers Linker Key Values",
    "_postman_id": "d5fe9fbe-a1cf-4192-9434-56532c514e1f",
    "description": "Get addon linkers linker key values",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "43b4ffe2-35e1-4550-b4dd-090ed18c1634",
          "name": "getAddonLinkersLinkerKeyValues",
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
              "id": "b1fd3647-dd24-46f6-949b-e4b29213affe"
            }
          ]
        },
        {
          "id": "c56f70fc-9287-4654-96a4-7a5843c03d8e",
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
              "id": "3a470bd3-bf99-41cf-878b-33700afe1738"
            }
          ]
        }
      ]
    }
  ]
}