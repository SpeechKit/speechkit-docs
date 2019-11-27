---
description: Use the SpeechKit plugin to generate audio for your Ghost articles.
---

# Ghost Project

### Sign up for SpeechKit <a id="sign-up-for-speechkit"></a>

Sign up for a SpeechKit account, and create a new project from the dashboard:![](https://mainframe.ghost.io/content/images/2019/09/SpeechKit-dashboard.png)

### Customise your settings <a id="customise-your-settings"></a>

Firstly choose a **Language**, **Title Voice** and **Paragraph Voice** to suit your project:![](https://lh6.googleusercontent.com/RO5GtHwHo9Y5jY-3AGcQHgtcGnaxh0kHRtFy2tHrqcBu-D-klkmxkGFRk9Ea-jvm6IIhvEBcPLVrmOTcc5husyg5ImbxX7EucpY4BAnxE0JswQSwhyE7iveU0dYniBW-FvOdrQNx)

Next, select **Ghost** as your connection method:

![](https://lh6.googleusercontent.com/ikZkL5Yk6pvbU11YOAc-B6a0ou2O4N312pGV_-TeaJBEO2HRELYdhqjQnYL8spSwdutYj55K-Ve_EguESUd1XYepv7IE-_tRTWP7zjujiRL_KD3Y000hG1ExdU6dTuJNtgyghgQR)

### Create a Custom Integration <a id="create-a-custom-integration"></a>

SpeechKit requires access to your content, to process the text into audio. To enable this you'll need to add a Ghost Content API key which permits access to public content on your site.

In Ghost Admin, head to the Integrations section and create a new custom integration:![](https://mainframe.ghost.io/content/images/2019/09/Custom-integrations-1.png)

Configure your custom integration and copy the Content API key:![](https://mainframe.ghost.io/content/images/2019/09/SpeechKit-Custom-Integration-in-Ghost.png)

Then head back to SpeechKit and paste your Ghost Content API key into your project:![](https://lh4.googleusercontent.com/Pj0dEeZWM1GoCxerv_WOi_IQwmYKaXB8WlQ7J5Ndh2Q6KV9sXhQOYU6aUoE3wb0JkVTQ5ACNGEui7-LQr8SuUdqkrDBIDO7FNPZsAcnDVo5pjWH8IycltfOV-DbuQ3cma6nxTqbp)

Once your custom integration is setup, you'll be provided with a code snippet in the SpeechKit dashboard:

![](https://lh5.googleusercontent.com/plZcsFQSFBM3z66SvB8F7ps64W6N8NGtIN9pv6svHz0OorgSnmb9jRvcBqGYkw0ThFjl-De004non5vofW6GDLw0jAGFIJC1vDewqi4WBvI8WxeTM21gFxQThf06jFOHW2IiAc66)

### Paste the snippet in Code Injection <a id="paste-the-snippet-in-code-injection"></a>

Copy provided JavaScript code snippet, then head over to the site wide **Code Injection** settings page within your Ghost admin panel and paste the snippet into the **Site Footer** section:![](https://lh6.googleusercontent.com/nRbCYUP6EZwLtQ14SZVres80EYGvhm8snLVJq3O4S657o9pMnt4yoszYzRAzc1yRJy0EZw8Y3NfrWjJtV528v0wvd8ucvh1-pTnOXHkNy9hIzzYtFJ2UT5bq9STiXszmNOMPFgHp)

{% hint style="success" %}
That's it - audio versions of your post will now be created and embedded on your site.
{% endhint %}

Once installed, SpeechKit will process each published article the first time it is viewed and create the corresponding audio article. Once the process has been triggered for a specific article, it can take 5 - 10 minutes for the player to initially appear within the content.

{% hint style="info" %}
The player will appear below the header in each article by default. If you would like to change the default position, you can edit your `post.hbs` template and add an empty div with the class **'speechkit-container'** where you would like to see the player.
{% endhint %}

