{
  "info": {
    "name": "Bitbucket Delete Add On Linkers Linker Key Values",
    "_postman_id": "fe1da959-e51d-4492-bd1f-56bfa221cb48",
    "description": "Delete addon linkers linker key values",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "5d9720e7-f23f-4d68-aa10-d1616fc1b54a",
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
              "id": "13a43d5a-192a-486e-8534-1d521ef737f4"
            }
          ]
        }
      ]
    }
  ]
}