{
  "info": {
    "name": "Lyft Cost estimates",
    "_postman_id": "1a61c8ad-03d6-43b8-aaa6-884251136529",
    "description": "Estimate the cost of taking a Lyft between two points.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "825dfdf1-b65f-47d8-9a4f-8e626142401f",
          "name": "GetCost",
          "request": {
            "url": "http://api.lyft.com/v1/cost?end_lat=%7B%7D&end_lng=%7B%7D&No Name=%7B%7D&start_lat=%7B%7D&start_lng=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Estimate the cost of taking a Lyft between two points"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bf66eb7e-2705-4c9a-89f0-6114e157e4c3"
            }
          ]
        }
      ]
    }
  ]
}