---
title: "Extended AD and YouTube"
date: 2024-11-12
---

# Making YouTube Embedded Videos Accessible

I've been reflecting on how often large sites, like YouTube, serve as the go-to platform for video hosting. Many users leverage YouTube to host videos for their own websites rather than actively trying to grow a YouTube channel. This approach makes sense since it’s a cost-effective way to host videos on a reliable platform. However, one significant drawback comes to mind: YouTube still lacks built-in support for Audio Descriptions, a key accessibility feature.

In considering possible solutions to improve accessibility, I came up with an idea that I developed with some assistance from ChatGPT. The result is a small project that doesn't just meet standard accessibility requirements but actually surpasses them. We’re not stopping at basic Level A or even Level AA compliance—we’re aiming straight for Level AAA with Extended Audio Descriptions. [Success Criterion 1.2.7 Extended Audio Description (Prerecorded) (Level AAA)](https://www.w3.org/WAI/WCAG21/Understanding/extended-audio-description-prerecorded.html) - you've met your match!

For those unfamiliar, Extended Audio Descriptions are a step up from the standard. While regular Audio Descriptions are constrained to brief pauses in dialogue, Extended Audio Descriptions go further by pausing the video when necessary to allow for fuller descriptions of visual elements. This approach provides a more comprehensive description of on-screen content, ensuring users don’t miss important details. Although it can be more disruptive to the flow of the video, it significantly enhances the experience for those relying on these descriptions.

Here's my little project: [Javascript Extended Audio Descriptions](https://certreq.dev/JavascriptExtendedAudioDescription/). We're taking the [YouTube IFrame Player API](https://developers.google.com/youtube/iframe_api_reference) and the [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) and making them dance together. It's still a little buggy. The Web Speech API doesn't like to load very quickly. Use the Test Voice button a couple of times until it reads the test text. Then use the external Audio Description Play button to start the video. I don't have a way to hide the YouTube Play button, and I didn't want to prevent the user from using any other YouTube provided controls such as Closed Captioning.

If any coders out there want to help me improve this project, check out the [GitHub repository](https://github.com/danielwestfall/JavascriptExtendedAudioDescription). Or if you have any thoughts or ideas you'd like to contribute, please reach out to me at <missinglinkaccessibility@gmail.com>.
