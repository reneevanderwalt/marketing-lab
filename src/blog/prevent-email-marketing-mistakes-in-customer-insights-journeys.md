---
title: InboxInspiration - Personalization Mistakes from My Inbox
pubDate: 2024-10-28
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'InboxInspiration: Personalization Mistakes from My Inbox'
description: |
  How to Prevent Three Common Email Marketing Mistakes in Customer Insights - Journeys
tags: ["email marketing"]
---

My inbox is sometimes the starting point of a new blog. It might be something I like, something I want to try in Dynamics Customer Insights - Journeys, or things I want to help fellow marketers avoid. This time, it falls under the last category.

In the past week, I received emails showcasing three common personalization mistakes in email marketing, all of which can be easily prevented—especially during the busy marketing seasons ahead. I'll walk you through these mistakes and show you how to avoid them in Customer Insights - Journeys! Plus, there's a bonus on what to absolutely avoid in email marketing.

## Using Merge Tags

The use of merge tags, a form of personalization,  is a widely used technique in email marketing. It's quite simple, but sometimes it can go wrong. In one example I received, the placeholder value [firstname] was meant to map to the recipient's first name but it didn’t work as intended.

![Not setting correct personalization field](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/No-correct-reference-to-personalization-field.png)

*Time is running out, [firstname]*

This issue can occur in Customer Insights - Journeys as well, especially if you create the main parts of your email content outside of the platform, for example in Excel. Issues may arise with elements like the subject line, sender name, and pre-header, leading to incorrect placeholders like [firstname] not being replaced with the actual first name merge tag in Customer Insights - Journeys.

### How to Use Merge Tags in Customer Insights - Journeys?

If you prefer to use external tools like Excel to set up your content, make sure you're using the correct variable settings there as well. Your Excel file should look something like the following example:

![Merge tag in Excel file](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Excel-file-with-correct-personalization.png)

When transferring content from Excel to your email in Customer Insights - Journeys, the system ensures that you can't publish your email without mapping all the placeholders to actual fields in Dynamics.

![Error in Customer Insights - Journeys when placeholder not set correctly](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Placeholder-name-not-set.png)

## Not Using Fallbacks

Another common mistake, similar to the first one, is failing to include a fallback for dynamic content. In the example below, no fallback was set, so the sentence begins with a comma instead of my first name.

![Missing first name field default](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Missing-first-name-default.png)

*, get the most out of your garden in October*

### How to Use Fallbacks for Merge Tags in Customer Insights - Journeys?

There are two ways to prevent this in Customer Insights - Journeys. The first is to set a default value for merge tags. For a first name, you could use various options such as:

- Art lover
- Marketing professional
- Reader
- Customer

Or, if you're using it in a salutation like "Hi" or "Hello {{firstname}}," you could opt for terms like:

- You
- There
- Y’all

This can be done in the Personalization tab of the email, as shown below:

![Default value of personalized field](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Default-value-for-personalized-field.png)

The second solution requires a bit more effort but works just as well. Create a non-personalized version of the message. Instead of saying “{{firstname}}, your ebook arrived,” you could simply say “Your ebook arrived.” This can be done using an inline conditional content piece with an {{IF}}/{{ELSE}} statement, as illustrated below:

![Inline condition in subjectline](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Inline-condition-with-personalization-field.png)

## Segmented Marketing

The next mistake involves segmented marketing. A couple of weeks ago, I received an email about vacation rental homes. The content promoted both autumn and Christmas breaks. I clicked on both links to check out the offers. Two weeks later, I received two emails at the same time: one with the subject line "Autumn in Holland" and the other "Christmas in Holland." It appears that they didn't exclude one segment from the other to create a proper hierarchy, or they made an error in their journey. Either way, this likely wasn’t intentional.

!['Same''email at same time](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Segmentation_mistake.png)

*Autumn in Holland - Christmas in Holland*

### Retargeting Campaign in Customer Insights - Journeys

How can you prevent this in Customer Insights - Journeys? There are several ways:

1. Exclude one segment from the other, and if there are multiple segments, create a hierarchy.
2. Exclude one segment within the journey of the other segment(s).
3. Create one comprehensive journey using the new "wait for segment tile" branch or, for now, use a wait-and-attribute tile.
4. Use element conditions in your email, so create one email, for two segments.

![Exclude one segment in the other](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Segment-exclusion-within-segment.png)

*Exclusion within segment*

![Exclude one segment in the other](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Segment-exclusion-within-journey.png)

*Exclusion within journey*

![Exclude one segment in the other](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Branching-within-journey.png)

*Branching within journey*

![Element conditions in email](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Element-conditions-in-email.png)

*Element conditions in one email*

## BONUS: Faking a Reply in Your Subject Line

The last point is not a mistake but an absolute "don't." This involves intentionally placing a fake "RE:" (or the Dutch equivalent "Antw:") in the subject line. It makes it appear as if you're receiving a reply to an email you had previously sent. This is a big no-no in email marketing.

![Fake reply by adding the Dutch alternative for RE: in the subject line](/assets/images/blog/prevent-email-marketing-mistakes-in-customer-insights-journeys/Absolute-dont-in-email-marketing-faking-reply.png)

*RE: Are you joining us for dinner in the coming period?*

## That’s a Wrap

Three mistakes and one absolute "don’t" from my own inbox! Remember to run thorough <a href="https://marketing-lab.nl/work/email-testing">email tests</a> before publishing your next journey!