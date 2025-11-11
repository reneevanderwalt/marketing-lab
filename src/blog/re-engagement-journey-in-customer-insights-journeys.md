---
title: How to Run a Re-Engagement Campaign in Dynamics Customer Insights - Journeys
pubDate: 2025-05-06
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'How to Run a Re-Engagement Campaign in Dynamics Customer Insights - Journeys'
description: |
  Discover how to set up a re-engagement campaign in Microsoft Dynamics Customer Insights – Journeys. Improve deliverability, increase engagement, and clean your email list with step-by-step strategies.
tags: ["email marketing", "marketing strategy", "customer journeys"]
---

I have been talking to a lot of marketers in the past 15 years. There are two things that scare them the most:

1. Hitting send on an email  
2. Eliminating contacts from their list

To feel more confident when sending emails, check out [this blog post](https://marketing-lab.nl/work/email-testing) I wrote a couple of months ago. If you're scared of the second thing, dare to keep on reading!

#### Why You Shouldn't Be Scared of Email List Cleaning

The list is sacred in email marketing. Actually, it’s called a Segment now 😉. It’s your go-to when you want to:

- Drive more sales  
- Introduce a new product  
- Update customers about your business hours  
- Promote your latest event  

It’s important—I get it!

**BUT...**

What’s truly important? The message itself? Or the fact that people actually read or interact with it?

Besides low open and click-through rates damaging your domain reputation and deliverability, how effective is your campaign if no one engages?

In Dynamics Customer Insights - Journeys, you pay per email sent. So sending to inactive users not only fails to earn revenue—it costs you money.

#### How to Clean Your Email List with a Re-Engagement Campaign

Cleaning your list is, in my opinion, one of the most essential practices in email marketing. I'm not saying to immediately eliminate unengaged contacts—there are several steps to try first.

1. **Gather more preferences**  
   Even if they aren’t engaging, let them update their communication preferences. Use Topics in your Compliance Profile.

2. **The “We Miss You” message**  
   Let them know you’ve noticed the inactivity. This is your final chance to bring them back!

3. **Removal from list—not the database**  
   Explain that you’ll unsubscribe them after a certain period unless they take action. Keep them in your database for future use.

---

### Key Considerations Before Launching a Re-Engagement Campaign

#### What Does Engagement Mean?

Engagement varies by business type. Here are common engagement criteria:

1. Last email open date *(use with caution—it's often unreliable)*  
2. Last email click date  
3. Last purchase/order date  
4. Last support case or service interaction  
5. Last website visit  

You can also **combine conditions**:  
> *Last email click more than 6 months ago AND last purchase more than 12 months ago*

#### Timing Is Everything

Look at your **average frequency**:
- How often do you send newsletters?
- How long between purchases or interactions?

This helps determine when someone becomes “unengaged.”

💡 Tip: Check how many people will fall into your segment before launching. You don’t want 80% of your list in a re-engagement flow!

---

### How to Build a Re-Engagement Campaign in Dynamics Customer Insights - Journeys

#### Step 1: Prepare Your Content

I won’t dive into design, but check [Really Good Emails](https://reallygoodemails.com/categories/winback) for excellent win-back inspiration.

Consider creating **multiple messages in a funnel format** to improve results.

#### Step 2: Prepare Your Segment

Time for the fun part! Here’s an example setup:
- Contacts who received at least 12 emails in the past 12 months
- Contacts who didn’t click any email in the last 6 months

Use the **Behavioral section** in the segment builder.

![Email Engagement Segment in Dynamics Customer Insights - Journeys](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Email-Engagment-In-Segment.png)

Add "Email Delivered" criteria and set to 12 interactions over the past 12 months:

![Email Delivered Criteria](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Email-Deliverd-Interactions.png)

Remove the specific email filter to apply to *all* email sends:

![Remove Email Filter](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Remove-Email-Element-Email-Delivered.png)

Next, add "Email Clicked" set to **less than 1** interaction in the last 6 months. Set the condition to **But not**:

![Final Re-engagement Segment](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Final-Re-Engagement-Segment.png)

#### Step 3: Build Your Journey

We’ll send three emails spaced seven days apart. If the contact clicks any link, they exit the journey.

Start with the segment. Choose:

1. **One-time journey**: members join once  
2. **Repeating journey**: members rejoin regularly  

If you want contacts to re-enter after becoming inactive again (e.g., three years later), choose **option 2** and set up your segment accordingly:

![Repeatable Segment Logic](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Addition-To-Segment.png)

Otherwise, use a one-time journey:

![Journey Start](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Journey-Start.png)

Send your three emails, spaced by seven days. Exit the series upon any link click:

![Email Series in Journey](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Series-In-Journey.png)

If no clicks occur after the three emails plus seven days, trigger a **commercial opt-in removal** via Custom Trigger and Cloud Flow:

![Final Steps in Journey](/assets/images/blog/re-engagement-campaign-in-customer-insights-journeys/Final-Steps-In-Journey.png)

Once someone clicks, they’re back in your newsletter segment 🥳.

---

### Additional Tips to Boost Engagement

Depending on your business, you can enhance the re-engagement flow with:
- A discount or exclusive offer  
- Fresh content they may have missed  
- Highlight product improvements  
- Show personalized product recommendations  

💡 And don't forget to [A/B test your content](https://marketing-lab.nl/work/ab-testing-in-customer-insights-journeys)!

Also, consider **excluding** these contacts:
1. Those currently in a welcome series  
2. High-volume support case customers  
3. Recently added contacts (last 30–60 days)

---

### Wrap-Up

You now know how to create a re-engagement campaign using Dynamics Customer Insights - Journeys. From list cleaning to automated journeys and opt-out flows, it’s all about **maximizing value and minimizing waste**.

Need help fine-tuning your criteria, timings, or content ideas? Just [send me an email](mailto:renee@vanderwalt.eu)—I'd be happy to help!