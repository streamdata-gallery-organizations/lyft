{
  "info": {
    "name": "Lyft Get the ride detail of a given ride ID",
    "_postman_id": "ef3c40f3-3938-411d-9d4a-ebb289fcd432",
    "description": "Get the status of a ride along with information about the driver, vehicle and price of a given ride ID",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "3abf5be2-5920-4010-bad2-2408912f930e",
          "name": "GetRide",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lyft.com",
              "path": [
                "v1",
                "rides/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get the status of a ride along with information about the driver, vehicle and price of a given ride ID\n"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec4b0885-8318-4861-93be-d0243acd80ff"
            }
          ]
        }
      ]
    }
  ]
}