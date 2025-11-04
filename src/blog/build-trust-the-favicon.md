---
title: Build Trust - The Favicon
pubDate: 2024-02-12
image:
    url: 'https://marketing-lab.nl/assets/images/blog/build-trust-the-favicon/Build_Trust_The_Favicon.jpg'
    alt: 'Build Trust With the Favicon'
description: |
  Building trust with just a really small image and four lines of code in your Dynamics Customer Insights - Journeys output.
tags: ["email marketing", "landing pages"]
---


Reputation is one of the (email) marketing “buzzwords” of the moment. With the new inbox regulations of Yahoo and Google, building trust is more important than ever. There are several ways to build trust with your (potential) customers, especially in the inbox! However, in this blog post, I will take a look at building trust after reaching the inbox by using the favicon in two places in Dynamics Customer Insights – Journeys. Same technique, same outcome, two use cases 😊

## The favicon

Favicon, one of those words that you can pronounce in two ways, either ‘favicon’ or ‘fav icon’. Choose your pick 😉 It is a combination of the words ‘favorite’ and ‘icon’.
A favicon is the image that you see next to your webpage title in a web browser. It gives the visitor a feeling of trust when it visits your website, because it recognizes your logo. 

![Browser with three tabs and favicons](/assets/images/blog/build-trust-the-favicon/Browser_with_three_tabs_and_favicons.png)

It also serves as a convenient search attribute in your favorites list!

![Favorites with favicons](/assets/images/blog/build-trust-the-favicon/Favorite_bar_with_favicons.png)

## The technique

There are a lot of <a href="https://www.emergeagency.com/insights/detail/the-essentials-of-favicons/" target="_blank">possibilities for the size of the favicon</a>, but taking a look at the two use cases we have, we will focus on the following four sizes:

1.	32x32 > Standard for most desktop browsers
2.	180x180 > iOS preferred
3.	192x192 > Google Developer Web App Manifest Recommendation
4.  270x270 > Chrome Web Store icon & Small Windows 8 Star Screen Icon

So you need to create four PNG images of your logo in the above sizes and save them on your website. Nearly all of the times, you can find these images in the header of the html of your homepage, so you don’t need to create them again.

Now we need to create four lines of code:

```go
<link rel="icon" href="/favicon-32x32.png" sizes="32x32" />
<link rel="icon" href="/favicon-192x192.png" sizes="192x192" />
<link rel="apple-touch-icon" href="/favicon-180x180.png" />
<meta name="msapplication-TileImage" content="/favicon-270x270.png" />
```

This code can be used in the following two use cases.

## Use case #1

### Your Real Time Marketing Preference Center

If you take a look at your Preference Center in your web browser, you’ll probably see something like this:

![Preference center without favicon](/assets/images/blog/build-trust-the-favicon/Preference_center_without_favicon.png)

That is not what we want!

So open the HTML editor of your Preference Center in your Compliancy Profile. Paste the four lines of code, above the `<style>` section of your HTML, so it looks like this:

![Preference Center HTML with four lines of favicon code](/assets/images/blog/build-trust-the-favicon/Preference_center_html_editor.png)

By the way, if you want to change the title "Preference Center" in your web browser tab, please adjust the text between the `<title></title>` elements as well.

So here is the comparison:

![Preference Center comparison of favicons](/assets/images/blog/build-trust-the-favicon/Comparison_Preference_Center_Favicon.png)

I know what I would prefer, especially since the URL of these Preference Centers are not branded (<a href="https://learn.microsoft.com/en-us/dynamics365/release-plan/2024wave1/customer-insights/dynamics365-customer-insights-journeys/boost-customer-confidence-campaign-performance-branded-links-emails-content" target="_blank">yet</a>).

## Use case #2

### Your Real Time Marketing Emails

Since the December update, it is (finally) possible to add a web version link to your Real Time Marketing Emails. Read the <a href="https://meganvwalker.com/view-in-browser-for-realtime-emails-option/" target="_blank">blog post of Megan V Walker</a> on how to do this and read a <a href="https://marketing-lab.nl/from-head-to-toe-where-to-place-web-version-link">previous post of mine</a> on best practices when it comes to the web version link.

Now that it is possible, let’s take a look at your web version Emails in your web browser. You probably will see something like this:

![Web version of email without favicon](/assets/images/blog/build-trust-the-favicon/No_favicon_in_web_version.png)

Like the Preference Center, we don’t want this here either. So let’s copy the four lines of code again, open up the HTML editor and paste the code before the `<style>` section, so it looks like this:

![Email HTML editor with four lines of code](/assets/images/blog/build-trust-the-favicon/Email_html_editor.png)

By the way, your email subject line is automatically added as the title of your web version page, so you don’t have to change this manually.

Here is the comparison of the web version of your email. Looks way better right?

![Web Version comparison](/assets/images/blog/build-trust-the-favicon/Comparison_Web_Version_Favicon.png)

## How about Use Case #3?

### Standalone Real Time Marketing Forms

Unfortunately, we cannot change the favicon of the standalone Real Time Marketing Forms. As we take a look at the HTML of these standalone pages (right mouse click > ‘View page source’) , you can see that the script is embedded on this URL and not the actual HTML.

![Actual HTML of Marketing Form](/assets/images/blog/build-trust-the-favicon/Actual_HTML_of_Standalone_Marketing_Form.png)

Therefore, the favicon is not placed on this page, and we cannot use this technique here ☹

## Wrap up

By adding four lines of code to your Preference Center and your Real Time Marketing Email, you build more trust. A small image making a big impact. You’re my favorite, favicon!
