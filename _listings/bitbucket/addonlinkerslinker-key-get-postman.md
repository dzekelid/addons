{
  "info": {
    "name": "Bitbucket Get Add On Linkers Linker Key",
    "_postman_id": "84bae93b-fb3d-47c5-99a7-e34e2fd7ad08",
    "description": "Get addon linkers linker key",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "32c45c80-ffa8-420c-be87-616bb4b241ce",
          "name": "getAddonLinkersLinkerKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "addon/linkers/:linker_key"
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
            "description": "Get addon linkers linker key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90e139a2-7af2-44d1-b4af-54f18659760f"
            }
          ]
        }
      ]
    }
  ]
}