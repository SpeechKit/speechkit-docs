---
description: Example embed code for implementing the player on your website
---

# Embedding the player

To add the player to your website, simply insert the snippet below into your article template, replacing **\[project-id\]** with your own **Project ID**.

```markup
<iframe allowfullscreen="false" data-src="
https://app.speechkit.io/api/v2/projects/[PROJECT_ID]/podcasts/iframe.html
" frameborder="0" id="speechkit-io-iframe" scrolling="no" style="display: none"></iframe>
<script src="
https://cdn.jsdelivr.net/npm/@speechkit/speechkit-audio-player@latest/dist/speechkit-iframe-helper.js
" type="text/javascript"></script>
```

{% hint style="info" %}
If your website is enabled for Google AMP, you will need to include a different code snippet into your AMP article template. Our [SpeechKit on AMP](https://docs.speechkit.io/enhanced-features/speechkit-on-amp) page will help guide you through this process.
{% endhint %}

