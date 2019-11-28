---
description: Create a new audio edition within a specific project.
---

# Create a new audio edition

{% api-method method="post" host="https://staging-app.speechkit.io/api/v3" path="/projects/{project\_id}/audio" %}
{% api-method-summary %}
Post a new audio edition
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="integer" required=true %}
ID of the project you wish to add audio to
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="external\_id" type="string" required=false %}
Your own internal ID
{% endapi-method-parameter %}

{% api-method-parameter name="body" type="string" required=true %}
Text content of your article, max 100000 chars
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

For example requests, responses and to test your API calls, check out our [API Explorer](https://staging-app.speechkit.io/api/documentation).

