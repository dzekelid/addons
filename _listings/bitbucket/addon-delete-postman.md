{
  "info": {
    "name": "Bitbucket Delete Add On",
    "_postman_id": "b442d029-71e2-43b9-884b-be0d54dfd1a6",
    "description": "Delete addon",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Addon",
      "item": [
        {
          "id": "7877b51e-14f9-4e30-ada8-83f1770b4683",
          "name": "deleteAddon",
          "request": {
            "url": "http://api.bitbucket.org/2.0/addon",
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete addon"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6a2478e-8f04-4593-853e-ce51df04656c"
            }
          ]
        }
      ]
    }
  ]
}