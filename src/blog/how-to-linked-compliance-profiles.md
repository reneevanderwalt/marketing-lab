---
title: How To - Linked Compliance Profiles
pubDate: 2024-11-07
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'How To - Linked Compliance Profiles'
description: |
  A Hidden Gem in Customer Insights - Journeys
tags: ["email marketing", "gdpr"]
---

One feature that I think hasn’t received much attention is the option to use multiple linked compliance profiles. I’ve used it for several use cases, and by the end of this blog, you’ll understand what it is, when to use it, and of course, how to set it up! Let’s dive in.

## What is a Linked Compliance Profile

A linked compliance profile reuses the consent previously captured in an existing compliance profile. This means that linked compliance profiles **share** their purposes, enforcement models, and topics. If I add a topic to compliance profile #1, all linked compliance profiles inherit the new topic.

Another key point: contact point consent records are **not related** to a compliance profile but **only** to a purpose or purpose/topic combination. So, consent for a commercial purpose in compliance profile #1 also applies to all linked compliance profiles!

The only elements that compliance profiles don’t share are their preference page and company address, which can lead to some interesting use cases.

## Use Cases for Multiple Linked Compliance Profiles

Now that we understand linked compliance profiles, let’s explore some effective use cases.

### Use Case #1 - Multiple Languages

If you’re working in an organization with an audience that communicates in multiple languages, linked compliance profiles can be very useful, especially when all purposes and topics must stay consistent.

For example, if you communicate in both Dutch and English, set up two linked compliance profiles, one for each language. Configure the content of one preference page in English and the other in Dutch.

When creating emails for your audience, select the appropriate compliance profile to ensure they see the preference page in their chosen language.

### Use Case #2 - Variable Consent Options

If you work with multiple topics, you can typically use a single preference page. However, if you want to prevent (potential) customers from opting out of all topics at once, linked compliance profiles are helpful.

For instance, your audience might have different roles or privileges for receiving certain topics. However, if they opt out of the commercial purpose, you want them to fully opt-out. So, set up multiple linked compliance profiles—one for each role or privilege—and configure each preference page with the topics relevant to that role or privilege.

When sending emails, selecting the right compliance profile ensures they only see the topics they’re eligible to view. This setup is especially useful when someone gains a new privilege, as their commercial purpose consent is already in place!

### Use Case #3 - Multiple Physical Addresses

This scenario is described in <a href="http://marketing-lab.nl/work/working-with-multiple-physical-addresses-in-compliance-profile">this helpful blog</a>.

## How To Set This Up?

It’s great to discuss these scenarios, but how does it work in practice?

## Step 1 - Set Up the First Compliance Profile

First, set up your *default* compliance profile. Configure all enforcement models for each purpose and create topics as needed.

## Step 2 - Create a New Compliance Profile

Create a new compliance profile, ensuring you check the “Use previously captured consent” box and select your default compliance profile.

![Create linked compliance profile](/assets/images/blog/how-to-linked-compliance-profiles/Set-up-linked-compliance-profile-multi-langual.png)

## Step 3 - Adjust Preference Pages

Modify the preference pages or company address field as desired.

## Step 4 - Start Collecting Consent

Start collecting consent, by creating forms or loading consent. Be aware that, when you create a form, segment, email or load consent you need to select a compliance profile. It does not really matter which compliance profile you select, since the contact point consent does **not** link to a compliance profile!

Begin collecting consent by creating forms or loading consent data. Remember that when you create a form, segment, or email or load consent, you need to select a compliance profile. It doesn’t matter which compliance profile you choose, as contact point consent does not relate to a specific compliance profile, only purpose and/or topic do!

## Wrap-Up

You now know how to create multiple linked compliance profiles and the scenarios where they can be particularly useful! Let's get to work.