{
  "info": {
    "name": "Lyft Types of rides",
    "_postman_id": "52402955-2d5d-4483-9a7e-cdc018c21a84",
    "description": "The ride types endpoint returns information about what kinds of Lyft rides you can request at a given location.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "6d790697-e2a3-4648-89ae-710c8fc5c4cf",
          "name": "GetRideTypes",
          "request": {
            "url": "http://api.lyft.com/v1/ridetypes?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The ride types endpoint returns information about what kinds of Lyft rides you can request at a given location"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0421f5d-096e-408d-b567-cce7147387bd"
            }
          ]
        }
      ]
    }
  ]
}