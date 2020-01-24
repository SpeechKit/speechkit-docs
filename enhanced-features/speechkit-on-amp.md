---
description: Enabling SpeechKit player on Google’s Accelerated Mobile Pages (AMP)
---

# SpeechKit on AMP

## Adding embed code to your AMP template

To enable the SpeechKit player on AMP, you must add our AMP-specific embed-code to your your template file.

Copy the snippet below into your AMP template, replacing **\[project-id\]** with your own **Project ID**.

{% code title="HTML Snippet:" %}
```bash
<amp-iframe id="speechkit-io-iframe" sandbox="allow-scripts allow-same-origin allow-popups" 
src="https://app.speechkit.io/api/v2/projects/[project-id]/podcasts/iframe.html" 
layout="fixed-height" frameborder="0" scrolling="no" height="43px" width="auto" >
<amp-img width="643" height="150" layout="responsive" 
src="https://s3-eu-west-1.amazonaws.com/speechkit-js/logo.svg" placeholder></amp-img></amp-iframe>
```
{% endcode %}

There may be cases where the audio hasn't yet been ingested and in these instances, there will be an empty space where the player has failed to load. 

Due to AMP restrictions, we cannot remove or hide iframe \(as we do normally\), hence, we recommend publishers add an additional javascript function alongside the iframe snippet that will perform this step.

The javascript snippet should check the audio exists by making a simple request to the SpeechKit API and if that request returns a 404, the amp-iframe can be removed or hidden.

The following snippet of code will generate the request URL needed, simply substitute **\[project-id\]** for your **Project ID**:

```bash
const sAPIBaseUrl = 'https://app.speechkit.io/api/v2/projects/';
const sProjectID = '[project-id]';
const sPageUrl = window.location.href.split(/[?#]/)[0];
const sRequestUrl = sAPIBaseUrl + sProjectID + '/podcasts/search?url=' + encodeURIComponent(sPageUrl);
```

When you make a request to the _sRequestUrl_, it will return a _200 JSON_ response for an existing audio article, or a _404 Not Found_ response for an article that can't be found. You can then show/hide the iframe according to this response.

