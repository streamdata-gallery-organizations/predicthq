{
  "info": {
    "name": "PredictHQ Requesting an Access Token",
    "_postman_id": "cc504f7a-0b1c-4298-b4c8-04b5d35134f9",
    "description": "When requesting an Access Token, use the `client_credentials` grant type, then request the scope or scopes you wish to have access to.\n\nThese scopes can be any or all of the following, separated by a space:\n  - `account` Grants access to the account endpoint.\n  - `events` Grants access to the events endpoint.\n  - `places` Grants access to the places endpoint.\n  - `signals` Grants access to the signals endpoint.\n\nPlease note that Access Tokens requested via the client_credentials grant type never expire.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth2",
      "item": [
        {
          "id": "77289115-88de-402b-b996-a131c155961f",
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
              "id": "ef854ddb-a967-4176-8396-c66f57d94f16"
            }
          ]
        },
        {
          "id": "97eb0c2d-f4e6-48f2-b71c-749fff0957e2",
          "name": "Oauth2TokenPost",
          "request": {
            "url": "http://api.predicthq.com/oauth2/token/",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "grant_type",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "scope",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "When requesting an Access Token, use the `client_credentials` grant type, then request the scope or scopes you wish to have access to.\n\nThese scopes can be any or all of the following, separated by a space:\n  - `account` Grants access to the account endpoint.\n  - `events` Grants access to the events endpoint.\n  - `places` Grants access to the places endpoint.\n  - `signals` Grants access to the signals endpoint.\n\nPlease note that Access Tokens requested via the client_credentials grant type never expire."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7ce30a7-96e5-4285-86a9-5a606870da4e"
            }
          ]
        }
      ]
    }
  ]
}