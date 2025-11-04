---
title: A/B Testing in Customer Insights - Journeys
pubDate: 2025-04-11
image:
    url: 'https://marketing-lab.nl/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Testing-In-Customer-Insights-Journeys.jpg'
    alt: 'A/B Testing in Customer Insights - Journeys'
description: |
  Learn how to run effective A/B tests in Microsoft Dynamics Customer Insights - Journeys.
tags: ["email marketing", "marketing strategy"]
---

I have many email addresses. They all come into my Apple Mail app on my iPhone. Sometimes, I’m registered for newsletters or commercial communications from companies with multiple email addresses. And occasionally, the results are fascinating—because I become part of a subject line A/B test.

I think A/B testing is a great way to test your content and your message. In Customer Insights - Journeys, we have multiple ways to do A/B testing, and I’m going to show you how—but first, let me explain *why* and *what* you can A/B test.

#### The WHY of A/B Testing

To tell you the truth, I’m a perfectionist. It shows in the fact that I don’t like making mistakes. BUT I’ve learned a lot from the mistakes I *have* made. That’s the most important thing about A/B testing—it’s not about proving your version (A) outperformed your colleague’s version (B). It’s about learning **why** you got the results you did.

When you look at the *why* behind your results, you gain a better understanding of your audience—how to shape your content, what it should look like, and what your audience truly needs.

So why would I recommend A/B testing? To gain deeper insight into what works in your marketing communications with different audience segments. In the end, that’s what leads to better marketing.

Just to give you a few behavior-based factors you can test with A/B testing:

| Behavior            | Insight                                                                 |
| :------------------ | :---------------------------------------------------------------------- |
| Timing              | Which days of the week or hours of the day work best for each audience |
| Channel             | Channel preferences, especially when combined with other behaviors      |
| Content Consumption | Are they skimming or reading in depth?                                 |
| Value Sensitivity   | Do they prefer discounts or added value?                               |
| Emotional Trigger   | Urgency and scarcity vs. aspirational messaging                         |
| Visual vs. Textual  | Do they prefer written content or visual appeal?                       |
| Decision Making     | Impulse-driven vs. thoughtful, considered decision-making              |

#### The WHAT of A/B Testing

Based on the behavior you’re looking to understand, there are many elements you can test:

| Content                   | Other                     |
| :------------------------ | :------------------------ |
| Message Type              | Send Time                 |
| Colors                    | Day of the Week           |
| Long vs. Short Content    | Number of Emails per Week |
| Images vs. Text-Only      | Channels                  |
| Buttons vs. Text Links    | Delay Between Emails      |
| From Name or Address      |                           |
| Use of Emojis             |                           |
| Subject Line              |                           |
| Pre-Header Text           |                           |

#### The HOW of A/B Testing in Customer Insights - Journeys

Now that we understand *why* and *what* to A/B test, let’s take a look at the *how*—the different options available in Customer Insights - Journeys.

##### 1. Content Testing

The simplest type of A/B test is Content Testing. You create two versions of your content—email, text, or push notification—and select both versions in your journey.

![Dynamics Customer Insights - Journeys: Content A/B Test Journey Setup](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Content-Test-Customer-Insights-Journeys.png)

##### 2. Channel Testing

Channel Testing is set up similarly, but instead of changing the content, you change the delivery channel. Be sure to keep other variables (like timing and message type) consistent.

![Dynamics Customer Insights - Journeys: Channel A/B Test Journey Setup](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Channel-Test-Customer-Insights-Journeys.png)

##### 3. Time Testing

Time Testing isn’t difficult either. In this case, we won’t use the A/B test element but instead use the Audience Split element. Then, set your timers to match your testing hypothesis.

![Dynamics Customer Insights - Journeys: Time A/B Test Journey Setup](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Timing-Test-Customer-Insights-Journeys.png)

##### 4. Funnel Testing

Funnel Testing also uses the Audience Split element. You can vary the delay between emails in lane 1 vs. lane 2 or change the number of emails sent in each lane.

![Dynamics Customer Insights - Journeys: Funnel A/B Test Journey Setup](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Funnel-Test-Customer-Insights-Journeys.png)

##### 5. Smart Testing

Smart Testing requires the A/B test element in your journey. While previous examples used a 50-50 split, Smart Testing allows you to define a control group and send the winning version to the remaining audience.

You can define the **Winning Metric** based on the behavior you want to understand. You also have the option to wait until statistical significance is reached—or to manually set a winner selection date and time.

> ⚠️ **Important:** If you choose statistical significance and no winner is found, the remaining audience will receive the email **30 days later**!

![Dynamics Customer Insights - Journeys: Smart A/B Test Journey Setup](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Smart-Test-Customer-Insights-Journeys.png)

#### The HOW of Interpreting A/B Test Results

When using the A/B Test element, you’ll receive your test results 4 hours after publishing. So be patient!

![Dynamics Customer Insights - Journeys - A/B Test Results](/assets/images/blog/ab-testing-in-customer-insights-journeys/AB-Test-Results-Customer-Insights-Journeys.png)

If you’re using the Audience Split element, you’ll get results sooner—but you’ll need to analyze them yourself. In these cases, I like to use <a href="https://vwo.com/tools/ab-test-significance-calculator/" target="_blank">this free tool</a> to check if my A/B test results are statistically significant. 🤓

Is the result of an A/B test final? Not at all—because people change, trends shift, and behavior evolves. Keep testing if you want to stay ahead!

#### Wrap-Up

You now have everything you need to start A/B testing today—and to gain deeper insights into your various audiences. 

Need help coming up with a strong A/B test scenario or interpreting your results? Or maybe you have the data but aren't sure what to do with it? Just [send me an email](mailto:renee@vanderwalt.eu) and I’ll be happy to help!
