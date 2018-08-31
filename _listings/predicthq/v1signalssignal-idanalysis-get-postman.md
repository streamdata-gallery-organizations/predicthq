{
  "info": {
    "name": "PredictHQ Retrieve Analysis",
    "_postman_id": "48407cff-73ea-466a-9c51-f8c266a39c70",
    "description": "This action returns a complete analysis of your Signal, which includes what your actual figures were, what could be expected, and what was in excess in terms of **demand**, **lead time** and **duration** and can be explained using events. Note that lead time (`lead`) and duration (`span`) analysis are only available when an `initiated` and `completed` dates are provided with data points, respectively.\n\nTo retrieve a list of events that we estimate impacted your business at a specific date in the past, use the `signal.id` and `signal.explain` parameters with the events endpoint.\n\nAlternatively, to retrieve a list of predicted events that we estimate will impact your business in the future, use the `signal.id` parameter and the date range you wish a prediction for using `active` or `start`.\n\nSee the events endpoint for more details.\n\nThe `significance` parameter corresponds to percentage of variation in your data that is considered normal when computing excess that can be attributed to events. If you were to look at a normal distribution, it would correspond to the percentage of values that lie within a band around the mean.\n\nAs an example:\n- ~68.27% = 1 standard deviation from the mean\n- ~95.45% = 2 standard deviations from the mean\n- ~99.73% = 3 standard deviations from the mean\n\nA high `significance` means that only extreme spikes and troughs will be attributed to events. We use 50% as a default, which corresponds to ~0.68 standard deviations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Signals",
      "item": [
        {
          "id": "63c2ad84-497e-4799-80fd-a72c2cadc82e",
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
              "id": "73c955f2-6dba-4909-acc4-6d3a03159cfe"
            }
          ]
        }
      ]
    }
  ]
}