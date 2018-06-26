{
  "info": {
    "name": "PredictHQ Retrieve Events Calendar",
    "_postman_id": "13f3639c-83f4-41ed-8b9c-32334849a319",
    "description": "This endpoint accepts the same parameters as the ones described in Retrieve All Events and can be used to get a calendar view of all matching events that are available to your account.\n\nEach day in the calendar contains aggregate counts of all _active_ events for that day.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Events",
      "item": [
        {
          "id": "9f5d9d1e-c5a9-47b0-bcd3-d2d136ae7a10",
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
              "id": "7f7e16ff-e5c9-4edf-9ce7-846fc9ab129e"
            }
          ]
        }
      ]
    }
  ]
}