---
description: Enabling SpeechKit player on Google’s Accelerated Mobile Pages (AMP)
---

# SpeechKit on AMP

## Adding embed code to your AMP template

To enable the SpeechKit player on AMP, you must add our AMP-specific embed code into your your article template. Copy the snippet below into your AMP template, replacing **\[project-id\]** with your own **Project ID**.

```markup
<amp-iframe id="speechkit-io-iframe" frameborder="0" scrolling="no" 
    sandbox="allow-scripts allow-same-origin allow-popups" 
    src="https://app.speechkit.io/api/v2/projects/[project-id]/podcasts/iframe.html" 
    layout="fixed-height" height="43px" width="auto" >
    <amp-img width="643" height="150" layout="responsive" 
    src="https://s3-eu-west-1.amazonaws.com/speechkit-js/logo.svg" placeholder></amp-img>
</amp-iframe>
```

{% hint style="info" %}
If necessary, you can add _width/height_ attributes on the amp-iframe to better suit your page. You may also want to add a _style_ attribute to the iframe, where you can add margins or other make other style changes to the iframe style.
{% endhint %}

There may be cases where the player will not render, for example, an article that has not yet been processed. In these instances, there will be an empty space where the player has failed to load. Due to AMP restrictions we cannot hide an amp-iframe \(as we do with the normal iframe\).   
  
Hence, to make sure there is not an empty space in these cases, this you will need to add a javascript function to show/hide the amp-frame. \(This must be added on the publisher side due to AMP security restrictions\). 

The function needs to make a request to the SpeechKit API and check the relevant audio is present. The iframe can then be shown/hidden, depending on the response. 

The following snippet of code will generate the request URL needed to check if the audio is available, simply substitute **\[project-id\]** for your **Project ID**:

```javascript
const sAPIBaseUrl = 'https://app.speechkit.io/api/v2/projects/';
const sProjectID = '[project-id]';
const sPageUrl = window.location.href.split(/[?#]/)[0];
const sRequestUrl = sAPIBaseUrl + sProjectID + '/podcasts/search?url=' + encodeURIComponent(sPageUrl);
```

When you make a request to the _sRequestUrl_, it will return a _200 JSON_ response for an existing audio article, or a _404 Not Found_ response for an article that can't be found. You can then show/hide the iframe according to this response.

