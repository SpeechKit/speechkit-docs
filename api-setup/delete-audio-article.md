---
description: Delete an audio article by ID
---

# Delete an audio article

{% api-method method="delete" host="https://app.speechkit.io/api/v3" path="/projects/{project\_id}/audio/{audio\_id}" %}
{% api-method-summary %}
Delete audio edition
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to delete a specific audio article.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="integer" required=true %}
ID of your project
{% endapi-method-parameter %}

{% api-method-parameter name="audio\_id" type="integer" required=true %}
ID or external\_id of the audio
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="api\_key" type="string" required=true %}
Your API key
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully deleted.
{% endapi-method-response-example-description %}

```
{
  "id": 999,
  "external_id": "123-a",
  "state": "processed",
  "media": [
    {
      "id": 999,
      "content_type": "mp3",
      "url": "http://link.to/the/file.mp3"
    }
  ],
  "deleted": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid API keyFor example requests, responses and to test your API calls, check out our API Explorer.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Invalid project ID or audio ID.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

For example requests, responses and to test your API calls, check out our [API Explorer](https://staging-app.speechkit.io/api/documentation).

