---
title: From Head to Toe - Where to Place Your Web Version Link?
pubDate: 2024-01-19
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'From Head to Toe - Where to Place Your Web Version Link?'
description: |
  Ensure a seamless experience with web version links in emails. Choose strategic placement for optimal user engagement and test based on CTR.
tags: ["email marketing"]
---

If you are using Outbound Marketing and considering a move to Real Time Marketing, you may have encountered some missing pieces. In the last release (1.1.35296.99), one of these missing pieces finally arrived in Real Time Marketing: adding the web version link to your Real Time Marketing emails. <a href="https://meganvwalker.com/view-in-browser-for-realtime-emails-option/" target="_blank">Megan V. Walker wrote a blog</a> on how to add this to your email; now, I will explain how to use this link in your email.

## What is a web version

An email is an HTML file. Now, with the dynamic content we can add to the email, the HTML actually differs per Contact.

Here is some HTML for an email addressed to myself.

![HTML of email addressed to Renee](/assets/images/blog/web-version/HTML_personalized_for_Renee.png)

This is the same email but with different HTML tailored for an email addressed to Sara.

![HTML of email addressed to Sara](/assets/images/blog/web-version/HTML_personalized_for_Sara.png)

These individual versions of the email HTML are sent to our email addresses. However, as we all know, some content is not “nicely” shown in some email clients. To make sure people can see a really nice version of your email, you can add a web version link -  a link to an HTML file in which all your nicely designed email code is displayed correctly and opened in a browser. This is always a good fallback to have in your email.

## Where to place your web version link

As Megan explained how to insert your web version link in a Real Time Marketing email, it is time to take a look at the position of your web version link, because you can do a couple of things.

### Place it in the header of your email

This is maybe the most common position to place the web version link.

![Example of web version link in Mailgun Email](/assets/images/blog/web-version/Mailgun_Header_Web_Version.png)
![Example of web version link in ActiveCampaign Email](/assets/images/blog/web-version/ActiveCampaign_Header_Web_Version.png)
![Example of web version link in Rijksmuseum Email](/assets/images/blog/web-version/Rijksmuseum_Header_Web_Version.png)
![Example of web version link in KLM Email](/assets/images/blog/web-version/KLM_Header_Web_Version.png)

### Place it in the footer of your email

Another position to place the web version link is in the footer of your email.

![Example of web version link in Atlassian Email](/assets/images/blog/web-version/Atlassian_Footer_Web_Version.png)
![Example of web version link in Litmus Email](/assets/images/blog/web-version/Litmus_Footer_Web_Version.png)

### Where interactivity happens

If you are a really cool email designer, you can do things like adding an image carousel or adding music to your email. But you know it wont work in many email clients. To make sure you have a fallback and give all the receivers the same experience, you can use the web version link to ensure they get the music or image carousel as well.

This is an example from Litmus in which they added a music file that you can play from within your email (love this, by the way). When I opened the email via Apple Mail on my iPhone, I was able to play the music directly (see AND hear the video).

<iframe width="560" height="315" src="https://www.youtube.com/embed/PbBkQ-CJMxU?si=eYgPaO1lgccWi6ZT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

However, when I opened the same email on Windows Mail on my Windows computer, I was directed towards the web version, where I could still play the music from within the ‘email.’

<iframe width="560" height="315" src="https://www.youtube.com/embed/PG9PI2jmpXk?si=jfVLV_O7r1sxk3mh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

So, if you are using interactivity in your email that not all your recipients can experience, make sure to add a compelling CTA towards the web version. This ensures they can still experience it.

## What works best?

That is something you need to test, but what would be the measure to determine the best position? In my opinion, it would be overall CTR, and compare the number of clicks you get on the web version link in both emails. If you see differences, you can decide on CTR which version worked best.

## Two final tips

1. For a better user experience, it might be a good idea to place the web version link in the header of your email. If your readers are experiencing rendering issues, they are highly likely to see them within the first scroll. So it is kind, and good for user experience, to place the web version link in the header. As a result, they don’t have to scroll all the way down through a poorly rendered email to find the web version link in the footer.
2. If you do decide to place the web version in the header of your email, please make sure you have a decent preheader so your email does not look like this in our inbox.

![Example of wrong pre header text English](/assets/images/blog/web-version/PreHeader_Text_English.png)

Dutch version

![Example of wrong pre header text Nederlands](/assets/images/blog/web-version/PreHeader_Text_Nederlands.png)