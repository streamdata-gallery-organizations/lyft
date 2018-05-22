{
  "info": {
    "name": "Lyft List rides",
    "_postman_id": "b6095c4d-5ea5-4b55-9f54-9eb97a06a65f",
    "description": "Get a list of past & current rides for this passenger.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "df1964e2-1292-4f8e-b84b-dce30e016fcd",
          "name": "GetRides",
          "request": {
            "url": "http://api.lyft.com/v1/rides?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of past & current rides for this passenger"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb308d28-e83b-4390-80ed-013ef195fc0e"
            }
          ]
        }
      ]
    }
  ]
}