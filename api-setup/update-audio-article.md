---
description: Update an audio edition by ID
---

# Update an audio article

{% api-method method="put" host="https://staging-app.speechkit.io/api/v3" path="/projects/{project\_id}/audio/{audio\_id}" %}
{% api-method-summary %}
Update audio edition 
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to update the details of a specific audio edition.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="integer" required=true %}
Project ID
{% endapi-method-parameter %}

{% api-method-parameter name="audio\_id" type="integer" required=true %}
ID or external\_id of the audio
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="api\_key" type="string" required=true %}
Your API key
{% endapi-method-parameter %}

{% api-method-parameter name="external\_id" type="string" required=false %}
Your own internal ID you can assign to the audio
{% endapi-method-parameter %}

{% api-method-parameter name="body" type="string" required=false %}
Main content of your audio \(max 10000 chars\)
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
Title for your audio
{% endapi-method-parameter %}

{% api-method-parameter name="author" type="string" required=false %}
Author of the article
{% endapi-method-parameter %}

{% api-method-parameter name="article\_url" type="string" required=false %}
Web page \(URL\) where the article is located
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Audio successfully updated.
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

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Invalid request.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid API Key.
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

