{
  "info": {
    "name": "Lyft Available drivers nearby",
    "_postman_id": "bdb56ca5-3455-49b0-bb4c-b588122312fb",
    "description": "The drivers endpoint returns a list of nearby drivers' lat and lng at a given location.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "e9a511e3-086b-4486-83ef-f5c33d4617ac",
          "name": "GetDrivers",
          "request": {
            "url": "http://api.lyft.com/v1/drivers?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The drivers endpoint returns a list of nearby drivers' lat and lng at a given location"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "24408416-bd9a-4abb-bfa6-8ad68f1efa65"
            }
          ]
        }
      ]
    }
  ]
}