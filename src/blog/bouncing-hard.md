---
title: Bouncing Hard🦘
pubDate: 2023-11-07
image:
    url: 'https://marketing-lab.nl/assets/images/blog/bouncing-hard/Bouncing_Hard.jpg'
    alt: 'Bouncing Hard'
description: |
  The truth about Bounces, Blocks and Suppression Lists in Dynamics Customer Insights – Journeys 
tags: ["email marketing", "analytics"]

---


With Google and Yahoo announcing their new and stricter SPAM policy, the time is now to take a closer look at all your email data. Not just the fun stuff, like Click Through Rates and Form Conversion Rates, but more specifically the technical stuff. Things that are happening in the magic black box of Dynamics Customer Insights – Journeys (previously known as Marketing). In this blog I will help you understand how to interpret and deal with the outcomes of this magic black box!

![Bounce overview](/assets/images/blog/bouncing-hard/Bounce_overview.png)

## Terminology 

### Hard bounce 

In global standards, a hard bounce is an email returned to the sender due to a permanent error, like an invalid email address. This is extremely harmful for your domain reputation, so do anything in your power to prevent this. 

In Dynamics Customer Insights – Journeys, a hard bounced email address is directly added to the suppression list and remains there for six months. After six months, the email address becomes available again, but we advise you to keep them bounced. Create a nice bounce process in which you remove consent from bounced email addresses, to keep your list clean! 

### Soft bounce 

A soft bounce indicates a temporary delivery issue. For example, a full mailbox, server is temporarily unavailable, or the email account has been closed. After five soft bounces, Dynamics Customer Insights – Journeys sees the recipients email address as a hard bounce. After these five soft bounces, the recipient is added to the suppression list. 

### Block bounce = Other bounce 

A block bounce is a bounce reason other than soft or hard bounce but is extremely rare. Once a recipient gets a block bounce, they are directly added to the suppression list in Dynamics Customer Insights – Journeys. 

### Email feedback loop --> Marked as spam 

The recipient used their email client to mark the message as spam! This email address is added to the suppression list and will remain there forever. This is also known as the spam complaint rate. 

### Suppression list 

The suppression list exists of three parts: 
1. The hard bounces and 5th time soft bounces --> stay there during 6 months 
2. Spam complaints --> stay there forever 
3. Pattern suppression (done by the deliverability team of Microsoft) --> stay there forever 

## The sending process 

### Number of recipients 

This is the inflow from either a trigger or segment based journey. In the example below, there are 409 recipients entering the email tile. 

![Number of recipients](/assets/images/blog/bouncing-hard/Number_of_recipients.png)

### Blocked 

Blocked recipients will never receive an email from Dynamics Customer Insights - Journeys. So, before the emails are sent, the blocked recipients are removed. And that is due to one of the following reasons: 

![Blocked reason overview](/assets/images/blog/bouncing-hard/Blocked_reasons.png)

### Sent 

To the remaining recipients, Dynamics Customer Insights – Journeys will try to send the email. So, the number of sent emails equals:

**Number of recipients – blocked recipients = sent emails**

**409 – 5 = 404 emails**

![Sents overview](/assets/images/blog/bouncing-hard/Sents.png)

### Delivery failed 

When the emails are sent Dynamics Customer Insights – Journey receive bounce messages back from the email providers. This could be one of three bounce types: 

![Delivery failed reasons overview](/assets/images/blog/bouncing-hard/Delivery_failed_reasons.png)

Only the hard bounce and other (which is a block bounce) will be accounted for as not delivered. A soft bounce only accounts as a not delivered message when it is the fifth time the soft bounce appears. 

### Delivered 

After failed delivery recipients are removed, Dynamics Customer Insights – Journey gets the total number of actual delivered emails. 

**Sent emails – delivery failed (but only hard bounce, 5th time soft bounce and block bounce) = delivered emails**

**404 – 1 = 403** 

![Delivered overview](/assets/images/blog/bouncing-hard/Delivered.png)

## What to do with those bounces? 

There are a couple things you can do with these bounces. 

1. Email address field --> Wipe it clean (if it is not a required field) 
2. Do not bulk email field --> Set it to not allow 
3. Do not email field --> Set it to not allow 
4. Deactivate the contact record 
5. Consent records for email address --> Set it to opted out 

But what you could also do is the following: 

1. Change the email address to a good email address 
2. Set the Consent Records of the old email address to opted out 
3. Create new opted in Consent Records for the good email address 

And then you can email this Contact or Lead again, because the bounce was registered on the email address, not the Contact or Lead! 

## Wrap up 

The magic black box of Dynamics Customer Insights – Journeys is unveiled. You now can interpret the email statistics and know how to handle bounces.