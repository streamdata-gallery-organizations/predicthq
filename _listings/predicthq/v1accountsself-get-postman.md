{
  "info": {
    "name": "PredictHQ Retrieve Account Details",
    "_postman_id": "fb34c7e7-da5c-463a-ab1a-c40ba611daab",
    "description": "If you need your account details for whatever reason, it's really easy to get them.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "4592894d-6dc0-4ece-9ecd-c4c46f55c959",
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
              "id": "41febc16-93fe-4200-9605-1035de131bbf"
            }
          ]
        }
      ]
    }
  ]
}