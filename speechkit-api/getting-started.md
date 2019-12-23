---
description: Introduction to the SpeechKit API
---

# Getting Started

#### 

![](../.gitbook/assets/api-flow-diagram-1.svg)

If you are using the API for the first time, this page is written to guide you through the process and help you understand how the API works and which endpoints to use. 

The diagram above shows how you can interact with the API to create and retrieve content for your website. There are 5 stages within a simple integration, as shown in the diagram and detailed below:

1. **Prepare the content** Before using the API to create audio, you should make sure your content is in a suitable format to be processed. We recommend submitting content in **HTML** format, as the markup will provide context, to help us to better process the text into audio. However, you can also submit your content as **Markdown** or **plain text** __if you prefer. For plain text, use the characters `\n\n` __to signify a new paragraph. 
2. **Create the audio** Once you are confident your content is ready to submit to the API you can use the [Create a new audio edition](create-new-audio-edition.md) endpoint to create your audio. Simply send your prepared content via a **POST** request. For a successful request, you will receive a response containing details of the newly created audio edition, such as the audio status, which will be **unprocessed** at this point. 
3. **Processing** You may need to wait up to 60 seconds for the audio to be processed within our system. You can see the status of audio editions in the dashboard or by creating a GET request _\(see next step\)_. 
4. **Retrieve your content** You are now able to retrieve your audio with a **GET** request - see the  [Fetch an audio edition by ID](fetch-audio-edition-by-id.md) page for detailed steps on how to do this.  
5. **Embed the audio** The response will contain the information and audio URLs you will need to embed the audio.

If you have any further questions regarding the API or our endpoints you can contact us at [support@speechkit.io](mailto:support@speechkit.io).

