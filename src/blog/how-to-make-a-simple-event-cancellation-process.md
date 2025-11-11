---
title: How To - Event Cancellation Process
pubDate: 2024-07-21
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'How To - Event Cancellation Process'
description: |
  Create a simple cancellation process in Customer Insights - Journeys
tags: ["event marketing", "email marketing", "events how to"]
---

We know how to <a href="https://marketing-lab.nl/work/how-to-create-event-reminder-journey">set up a reminder journey</a> for registrants, but what if a registrant wants to cancel because they can no longer attend? For events with a large number of registrants, setting up a simple cancellation process might be a good idea as it can <a href="https://marketing-lab.nl/work/seven-tips-to-prevent-no-shows">lower your no-show rate</a>.

There are many possibilities to address this; we will look at the most simple one: sending an email to a specific address.

## Step 0 - Prepare Your Email Content

Set up your confirmation and reminder messages as usual. These can be emails, text messages, or push notifications.

## Step 1 - Create a Mailto Link

Next, create the URL to send an email to a specific email address, preferably to an inbox accessible by the event manager. The link consists of three elements:

1. The email address
2. The subject line of the email
3. The body of the email

In this example, I want registrants to send an email to `info@marketing-lab.nl`, with the subjectline 'Event registration cancellation with registration ID {EventRegistrationID}' and the email body *Dear reader, I am cancelling my event registration for {EVENT NAME}. Kind regards, {FirstName}*.

The link for the above email will look like this

```go
mailto:info@marketing-lab.nl?subject=Event%20registration%20cancellation%20with%20ID%20{{EventRegistrationID}}&body=Dear%20reader,%0AI%20am%20cancelling%20my%20event%20registration%20for%20{{EventName}}.%0AKind%20regards,%0A{{FirstName}}
```

In the subject line and body of the mail, you use `%20` elements for spacings and `%0A` for new lines. You can use dynamic content as shown in the example above. 

## Step 2 - Paste the Link

Use this link in the URL field of a text link or a button. If you are using dynamic fields as in the example above, ensure that all dynamic fields are set to the correct attributes in the Personalize menu.

![The list code copied into the email](/assets/images/blog/how-to-make-a-simple-event-cancellation-process/adding-mailto-url-to-link.png)

## Results

This is what the email looks like when you click on the cancellation link:

![Final email](/assets/images/blog/how-to-make-a-simple-event-cancellation-process/mail-after-clicking-mail-to-link-with-content-provided-in-link.png)

## What Else?

You can add CC and BCC email addresses as well to your mailto link. Check <a href="https://yoast.com/developer-blog/guide-mailto-links/" target="_blank">this post</a> from YOAST on how to set this up.