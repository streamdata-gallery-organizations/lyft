{
  "info": {
    "name": "Lyft The user's general info",
    "_postman_id": "28af33e2-47f7-4496-9a7a-0d4386b05fa6",
    "description": "The v1 of this endpoint returns the user's ID, v2 will return more general info about the user. We require authentication for this endpoint, so we extract the user ID from the access token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "73756a38-dc53-4926-ba0d-63e12317c054",
          "name": "GetProfile",
          "request": {
            "url": "http://api.lyft.com/v1/profile",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The v1 of this endpoint returns the user's ID, v2 will return more general info about the user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5fb50786-1951-49ec-98d8-6ad33de9f71d"
            }
          ]
        }
      ]
    }
  ]
}