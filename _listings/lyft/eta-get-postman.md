{
  "info": {
    "name": "Lyft Pickup ETAs",
    "_postman_id": "fac8b23e-6fc4-4cad-88ff-1fd522a1121a",
    "description": "The ETA endpoint lets you know how quickly a Lyft driver can come get you",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "57dae4ef-b19b-4908-bae8-050601f3f041",
          "name": "GetETA",
          "request": {
            "url": "http://api.lyft.com/v1/eta?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The ETA endpoint lets you know how quickly a Lyft driver can come get you\n"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "174c6fab-adae-45f9-b537-1f861e6087b0"
            }
          ]
        }
      ]
    }
  ]
}