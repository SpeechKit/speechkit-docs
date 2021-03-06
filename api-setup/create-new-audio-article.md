---
description: Create a new audio article within a specific project.
---

# Create a new audio article

{% api-method method="post" host="https://app.speechkit.io/api/v3" path="/projects/{project\_id}/audio" %}
{% api-method-summary %}
Post a new audio article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to add new audio articles to your project.  
All requests must include a **Content-Type** header of **application/json**.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="integer" required=true %}
ID of the project you wish to add audio to
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="metadata" type="object" required=false %}
Any custom data related to the audio article
{% endapi-method-parameter %}

{% api-method-parameter name="external\_id" type="string" required=false %}
Your own internal ID
{% endapi-method-parameter %}

{% api-method-parameter name="body" type="string" required=true %}
Text content of your article \(max 100000 chars\)
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
Title for the audio edition
{% endapi-method-parameter %}

{% api-method-parameter name="author" type="string" required=false %}
Author of the article
{% endapi-method-parameter %}

{% api-method-parameter name="article\_url" type="string" required=false %}
Web page \(URL\) where the article is located
{% endapi-method-parameter %}

{% api-method-parameter name="api\_key" type="string" required=true %}
Your API key
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Audio successfully created within the project.
{% endapi-method-response-example-description %}

```
{
  "id": 999,
  "external_id": "123-a",
  "state": "unprocessed",
  "media": [
    {
      "id": 999,
      "content_type": "mp3",
      "url": []
    }
  ],
  "deleted": false,
  "metadata" :{
    "key": string
  }
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
Invalid API key.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Wrong project ID.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
If you are using the API to both create and retrieve your audio, we advise including a unique **external\_id** with your request that relates to the content, so you can easily retrieve the audio when necessary using this same ID.
{% endhint %}

For example requests, responses and to test your API calls, check out our [API Explorer](https://staging-app.speechkit.io/api/documentation).

