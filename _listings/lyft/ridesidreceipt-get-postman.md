{
  "info": {
    "name": "Lyft Get the receipt of the rides.",
    "_postman_id": "0e8eed4e-155e-4a6a-a3aa-1c66117ccc04",
    "description": "Get the receipt information of a processed ride by providing the ride id. Receipts will only be available to view once the payment has been processed. In the case of canceled ride, cancellation penalty is included if applicable.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "transportation",
      "item": [
        {
          "id": "4145a1fb-8f98-410f-b572-7ab0666cd7e7",
          "name": "GetRideReceipt",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lyft.com",
              "path": [
                "v1",
                "rides/:id/receipt"
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
            "description": "Get the receipt information of a processed ride by providing the ride id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43be525d-f167-4a67-b659-f05b1539acfc"
            }
          ]
        }
      ]
    }
  ]
}