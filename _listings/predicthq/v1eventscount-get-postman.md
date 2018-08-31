{
  "info": {
    "name": "PredictHQ Retrieve Events Count",
    "_postman_id": "d2724a02-bc82-4ab8-8b2d-b8ee9c870b08",
    "description": "This endpoint accepts the same parameters as the ones described in Retrieve All Events and can be used to get aggregated counts of all matching events that are available to your account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "9dc55066-1329-4fad-b36b-198b5f89f00f",
          "name": "V1AccountsSelfGet",
          "request": {
            "url": "http://api.predicthq.com/v1/accounts/self/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "If you need your account details for whatever reason, it's really easy to get them."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e07541a0-addc-4c89-809d-47726491cae8"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "ea2ed14c-ca5e-4c06-9015-57a61ff67c1d",
          "name": "V1EventsCountGet",
          "request": {
            "url": "http://api.predicthq.com/v1/events/count/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint accepts the same parameters as the ones described in Retrieve All Events and can be used to get aggregated counts of all matching events that are available to your account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdc86f94-d5a2-4bf2-864c-17b041a819c6"
            }
          ]
        }
      ]
    }
  ]
}