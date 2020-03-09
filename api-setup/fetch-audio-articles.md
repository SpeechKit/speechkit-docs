---
description: >-
  Retrieve a list of audio articles for a specific project, using the project_id
  identifier.
---

# Fetch audio articles from a project

{% api-method method="get" host="https://staging-app.speechkit.io/api/v3" path="/projects/{project\_id}/audio" %}
{% api-method-summary %}
Get audio articles within a project
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to retrieve a list of audio articles from a specified project.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="integer" required=true %}
Project ID of the project you wish to query.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="api\_key" type="string" required=true %}
Your API key.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Audio successfully retrieved.
{% endapi-method-response-example-description %}

```
[
  {
    "id": 123456,
    "external_id": "b123409-dca0-4c91-b160-a6123333ee1",
    "state": "processed",
    "media": [
      {
        "id": 123456,
        "content_type": "m3u8",
        "url": "https://speechkit-staging.s3.amazonaws.com/audio/projects/123/podcasts/123456/media/1.m3u8"
      },
      {
        "id": 123456,
        "content_type": "mp3",
        "url": "https://speechkit-staging.s3.amazonaws.com/audio/projects/123/podcasts/123456/media/1.mp3"
      }
    ],
    "deleted": false
  },
  
  {
    "id": 123456,
    "external_id": "b123409-dca0-4c91-b160-a6123333ee1",
    "state": "processed",
    "media": [
      {
        "id": 123456,
        "content_type": "m3u8",
        "url": "https://speechkit-staging.s3.amazonaws.com/audio/projects/123/podcasts/123456/media/1.m3u8"
      },
      {
        "id": 123456,
        "content_type": "mp3",
        "url": "https://speechkit-staging.s3.amazonaws.com/audio/projects/123/podcasts/123456/media/1.mp3"
      }
    ],
    "deleted": false
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Invalid request.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid API key.
{% endapi-method-response-example-description %}

```
{
  "code": 20,
  "message": "The authentication token was not recognised"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a project with specified **project\_id.**
{% endapi-method-response-example-description %}

```
{
  "code": 30,
  "message": "Object not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

For example requests, responses and to test your API calls, check out our [API Explorer](https://staging-app.speechkit.io/api/documentation).

