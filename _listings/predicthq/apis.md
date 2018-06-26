---
name: PredictHQ
x-slug: predicthq
description: Event visibility yields higher returns & reduces operational costs. PredictHQ
  is the worlds largest source of intelligent event data making businesses smarter.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
x-kinRank: "7"
x-alexaRank: "292227"
tags: PredictHQ
created: "2018-06-26"
modified: "2018-06-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/apis.md
specificationVersion: "0.14"
apis:
- name: PredictHQ Retrieve Analysis
  x-api-slug: predicthq
  description: |-
    This action returns a complete analysis of your Signal, which includes what your actual figures were, what could be expected, and what was in excess in terms of **demand**, **lead time** and **duration** and can be explained using events. Note that lead time (`lead`) and duration (`span`) analysis are only available when an `initiated` and `completed` dates are provided with data points, respectively.

    To retrieve a list of events that we estimate impacted your business at a specific date in the past, use the `signal.id` and `signal.explain` parameters with the events endpoint.

    Alternatively, to retrieve a list of predicted events that we estimate will impact your business in the future, use the `signal.id` parameter and the date range you wish a prediction for using `active` or `start`.

    See the events endpoint for more details.

    The `significance` parameter corresponds to percentage of variation in your data that is considered normal when computing excess that can be attributed to events. If you were to look at a normal distribution, it would correspond to the percentage of values that lie within a band around the mean.

    As an example:
    - ~68.27% = 1 standard deviation from the mean
    - ~95.45% = 2 standard deviations from the mean
    - ~99.73% = 3 standard deviations from the mean

    A high `significance` means that only extreme spikes and troughs will be attributed to events. We use 50% as a default, which corresponds to ~0.68 standard deviations.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/analysis/
  tags: Signals,Signal,Analysis
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-idanalysis-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-idanalysis-get-openapi.md
- name: PredictHQ Retrieve A Signal
  x-api-slug: predicthq
  description: This action returns a Signal according to the unique identifier you
    provide.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/
  tags: Signals,Signal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-id-get-openapi.md
- name: PredictHQ Update a Signal
  x-api-slug: predicthq
  description: This action modifies a Signal according to the unique identifier you
    provide.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/
  tags: Signals,Signal
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-id-put-openapi.md
- name: PredictHQ Delete A Signal
  x-api-slug: predicthq
  description: This action will delete a Signal altogether along with the Data Points
    associated with it, according to the unique identifier you provide.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/
  tags: Signals,Signal
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-id-delete-openapi.md
- name: PredictHQ Search Places
  x-api-slug: predicthq
  description: |-
    Use the below parameters to search and filter all places. Places are sorted by relevance (location or text query proximity).

    A search requires at least one of the `q`, `id`, `country` or `location` parameters.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/places/
  tags: Places
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1places-get-openapi.md
- name: PredictHQ Create Data Points
  x-api-slug: predicthq
  description: |-
    Every Signal needs a series of Data Points for the API to do its job.

    Unlike the other endpoints, the Data Point sink accepts three content types for uploading your data:
    - `application/json`: A JSON array of Data Points.
    - `application/x-ldjson`: A list of JSON Data Points, one on each line.
    - `text/csv`: A list of Data Points with each column comma-separated, and column names on the first row.

    As a rule of thumb, you should limit the number of records you upload with any single request to 1,000. If you use the CSV format, make sure to repeat the CSV header with each call.

    The global rate limit applies, but to prevent any disruption on critical aspects of your systems, this endpoint will never respond with a `402 Payment Required` in case your subscription expires.

    When required details are missing for some Data Points, instead of rejecting the whole batch, the valid Data Points will be accepted, and the invalid ones will be returned as an array in the body of the response along with a description of the problem.
    If this is the case, the response code will be `202 Accepted` instead of `201 Created`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/sink/
  tags: Signals,Signal,Sink
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-idsink-post-openapi.md
- name: PredictHQ Revoking an Access Token
  x-api-slug: predicthq
  description: |-
    Access Tokens never expire so once you have it, it's yours for the life of your PredictHQ API subscription.

    However, if you think your token may have been compromised, you have the power to revoke it at any time.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////oauth2/revoke/
  tags: Oauth2,Revoke
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/oauth2revoke-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/oauth2revoke-post-openapi.md
- name: PredictHQ Retrieve Account Details
  x-api-slug: predicthq
  description: If you need your account details for whatever reason, it's really easy
    to get them.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/accounts/self/
  tags: Accounts,Self
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1accountsself-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1accountsself-get-openapi.md
- name: PredictHQ Retrieve All Signals
  x-api-slug: predicthq
  description: It's easy to get a list of all Signals that are associated with your
    account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/
  tags: Signals
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signals-get-openapi.md
- name: PredictHQ Create a Signal
  x-api-slug: predicthq
  description: Before you do anything else, you need to create a new Signal that represents
    a time series that's important to your business.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/
  tags: Signals
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signals-post-openapi.md
- name: PredictHQ Retrieve Events Calendar
  x-api-slug: predicthq
  description: |-
    This endpoint accepts the same parameters as the ones described in Retrieve All Events and can be used to get a calendar view of all matching events that are available to your account.

    Each day in the calendar contains aggregate counts of all _active_ events for that day.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/events/calendar/
  tags: Events,Calendar
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1eventscalendar-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1eventscalendar-get-openapi.md
- name: PredictHQ Retrieve Events Count
  x-api-slug: predicthq
  description: This endpoint accepts the same parameters as the ones described in
    Retrieve All Events and can be used to get aggregated counts of all matching events
    that are available to your account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/events/count/
  tags: Events,Count
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1eventscount-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1eventscount-get-openapi.md
- name: PredictHQ Retrieve All Events
  x-api-slug: predicthq
  description: Use the below parameters to search and filter all events that are available
    to your account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/events/
  tags: Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1events-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1events-get-openapi.md
- name: PredictHQ Requesting an Access Token
  x-api-slug: predicthq
  description: |-
    When requesting an Access Token, use the `client_credentials` grant type, then request the scope or scopes you wish to have access to.

    These scopes can be any or all of the following, separated by a space:
      - `account` Grants access to the account endpoint.
      - `events` Grants access to the events endpoint.
      - `places` Grants access to the places endpoint.
      - `signals` Grants access to the signals endpoint.

    Please note that Access Tokens requested via the client_credentials grant type never expire.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////oauth2/token/
  tags: Oauth2,Token
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/oauth2token-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/oauth2token-post-openapi.md
- name: PredictHQ Retrieve All Dimensions
  x-api-slug: predicthq
  description: This action returns a summary for each dimension of your Signal.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com////v1/signals/{signal_id}/dimensions/
  tags: Signals,Signal,Dimensions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-iddimensions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/v1signalssignal-iddimensions-get-openapi.md
- name: PredictHQ
  x-api-slug: predicthq
  description: Event visibility yields higher returns & reduces operational costs.
    PredictHQ is the worlds largest source of intelligent event data making businesses
    smarter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28211-predicthq.jpg
  humanURL: http://www.predicthq.com/
  baseURL: https://api.predicthq.com//
  tags: PredictHQ
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/predicthq/master/_listings/predicthq/openapi.md
x-common:
- type: x-website
  url: http://www.predicthq.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/predicthq
- type: x-email
  url: support@predicthq.com
- type: x-email
  url: 8Bsupport@predicthq.com
- type: x-email
  url: notices@predicthq.com
- type: x-github
  url: https://github.com/predicthq
- type: x-linkedin
  url: PredictHQ
- type: x-twitter
  url: https://twitter.com/PredictHQ
- type: x-website
  url: https://developer.predicthq.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---