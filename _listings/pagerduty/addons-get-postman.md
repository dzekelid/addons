{
  "info": {
    "name": "PagerDuty List installed add-ons",
    "_postman_id": "3e757a97-a7e4-4402-ae3d-d734a6a29636",
    "description": "List all of the add-ons installed on your account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Folder",
      "item": [
        {
          "id": "575ac69f-0f88-436f-bdd6-77bcd6dd1e95",
          "name": "list-people-and-integrations-associated-with-a-given-team",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "teams/:teamId/people"
              ],
              "variable": [
                {
                  "id": "teamId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List people and integrations associated with a given team."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c62c0be-6848-4b25-8846-7f428f4f1547"
            }
          ]
        }
      ]
    },
    {
      "name": "APIs",
      "item": [
        {
          "id": "74a6d18b-016f-4cf2-9e60-f9b15dc4261d",
          "name": "rest-api-reference",
          "request": {
            "url": "http://example.com/api/api_reference",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "REST API Reference."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0b7b77a-98f7-44dd-ae4b-fc8a0cfa95e5"
            }
          ]
        }
      ]
    },
    {
      "name": "Abilities",
      "item": [
        {
          "id": "920e65e5-b634-4610-b858-19d2ecd4ea2b",
          "name": "list-all-of-your-accounts-abilities-by-name",
          "request": {
            "url": "http://example.com/api/abilities",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all of your account's abilities, by name."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2d61cff4-5270-414d-bee5-1eac0e7f8bb6"
            }
          ]
        },
        {
          "id": "3e8954a9-5903-439d-942b-d06247b752e4",
          "name": "test-whether-your-account-has-a-given-ability",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "abilities/:id"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Test whether your account has a given ability."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f038007-9fb9-4d3d-9461-726da8e53b78"
            }
          ]
        }
      ]
    },
    {
      "name": "AddOns",
      "item": [
        {
          "id": "05ef5382-40ba-49ad-a9ab-44839a9d7891",
          "name": "list-all-of-the-addons-installed-on-your-account",
          "request": {
            "url": "http://example.com/api/addons?filter=%7B%7D&No Name=%7B%7D&service_ids=%5B%7B%7D%5D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all of the add-ons installed on your account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34afe382-6d7b-4419-9e76-585fc7517854"
            }
          ]
        }
      ]
    }
  ]
}