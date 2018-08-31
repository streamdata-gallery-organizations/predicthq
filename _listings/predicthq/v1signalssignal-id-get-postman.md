{
  "info": {
    "name": "PredictHQ Retrieve A Signal",
    "_postman_id": "30c8088f-b9b9-4964-a960-4ac2619322d7",
    "description": "This action returns a Signal according to the unique identifier you provide.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Signals",
      "item": [
        {
          "id": "a1eb96e7-cb28-4b73-88e1-ed2678da4fba",
          "name": "V1SignalsAnalysisBySignalIdGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.predicthq.com",
              "path": [
                "v1/signals/:signal_id/analysis/"
              ],
              "variable": [
                {
                  "id": "signal_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This action returns a complete analysis of your Signal, which includes what your actual figures were, what could be expected, and what was in excess in terms of **demand**, **lead time** and **duration** and can be explained using events. Note that lead time (`lead`) and duration (`span`) analysis are only available when an `initiated` and `completed` dates are provided with data points, respectively.\n\nTo retrieve a list of events that we estimate impacted your business at a specific date in the past, use the `signal.id` and `signal.explain` parameters with the events endpoint.\n\nAlternatively, to retrieve a list of predicted events that we estimate will impact your business in the future, use the `signal.id` parameter and the date range you wish a prediction for using `active` or `start`.\n\nSee the events endpoint for more details.\n\nThe `significance` parameter corresponds to percentage of variation in your data that is considered normal when computing excess that can be attributed to events. If you were to look at a normal distribution, it would correspond to the percentage of values that lie within a band around the mean.\n\nAs an example:\n- ~68.27% = 1 standard deviation from the mean\n- ~95.45% = 2 standard deviations from the mean\n- ~99.73% = 3 standard deviations from the mean\n\nA high `significance` means that only extreme spikes and troughs will be attributed to events. We use 50% as a default, which corresponds to ~0.68 standard deviations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "63e9a890-3658-4085-9d1d-3e0b71e7b72f"
            }
          ]
        },
        {
          "id": "7cf28113-3399-4e6f-a7f0-569e4b972204",
          "name": "V1SignalsBySignalIdGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.predicthq.com",
              "path": [
                "v1/signals/:signal_id/"
              ],
              "variable": [
                {
                  "id": "signal_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This action returns a Signal according to the unique identifier you provide."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f48ad492-e929-4917-ab6e-64d5acaecdab"
            }
          ]
        }
      ]
    }
  ]
}