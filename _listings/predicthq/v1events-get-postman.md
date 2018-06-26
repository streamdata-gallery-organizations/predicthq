{
  "info": {
    "name": "PredictHQ Retrieve All Events",
    "_postman_id": "21c2ba96-95f2-4116-a146-88028c7ba4cf",
    "description": "Use the below parameters to search and filter all events that are available to your account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Events",
      "item": [
        {
          "id": "d12fb4db-e3e6-4251-90b6-2113fe1e3ebd",
          "name": "V1EventsCalendarGet",
          "request": {
            "url": "http://api.predicthq.com/v1/events/calendar/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint accepts the same parameters as the ones described in Retrieve All Events and can be used to get a calendar view of all matching events that are available to your account.\n\nEach day in the calendar contains aggregate counts of all _active_ events for that day."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a65988b-6248-465c-b075-1424be3eb90c"
            }
          ]
        },
        {
          "id": "9958179c-8178-465f-b147-41df452f20bd",
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
              "id": "acc0b1d2-c13e-4709-a23f-1da456db8e39"
            }
          ]
        },
        {
          "id": "e21adbe4-70b5-4ec6-83ca-ffcbd530a3ad",
          "name": "V1EventsGet",
          "request": {
            "url": "http://api.predicthq.com/v1/events/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use the below parameters to search and filter all events that are available to your account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89b9a215-014b-468c-893c-b89c320779ce"
            }
          ]
        }
      ]
    }
  ]
}