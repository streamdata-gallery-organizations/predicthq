{
  "info": {
    "name": "PredictHQ Revoking an Access Token",
    "_postman_id": "c2fb8b15-8a05-4863-afc9-dbc17612f918",
    "description": "Access Tokens never expire so once you have it, it's yours for the life of your PredictHQ API subscription.\n\nHowever, if you think your token may have been compromised, you have the power to revoke it at any time.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth2",
      "item": [
        {
          "id": "de5c08de-cb18-4c8e-a4fd-42474bd71b9e",
          "name": "Oauth2RevokePost",
          "request": {
            "url": "http://api.predicthq.com/oauth2/revoke/",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "token",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "token_type_hint",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Access Tokens never expire so once you have it, it's yours for the life of your PredictHQ API subscription.\n\nHowever, if you think your token may have been compromised, you have the power to revoke it at any time."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2097cf08-ea5e-41cb-86af-5cb993136318"
            }
          ]
        }
      ]
    }
  ]
}