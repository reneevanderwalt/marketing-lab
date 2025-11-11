---
title: Working With Multiple Email Addresses in Customer Insights - Journeys
pubDate: 2025-03-28
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'Working With Multiple Email Addresses in Customer Insights - Journeys'
description: |
  Learn how to effectively manage multiple email addresses in Dynamics Customer Insights - Journeys. Discover best practices for emailing, consent management, matching rules, and tracking email interactions to optimize your email marketing strategy.
tags: ["email marketing", "gdpr"]
---

In some cases, a single contact may have multiple email addresses—such as a personal email and a business or student email. However, they remain the same contact!

**Key Considerations**

1. 💌 Emailing
2. 🔒 Consent
3. 🔗 Matching
4. 📬 Email interactions

Let's dive in!

#### The Contact

By default, the Contact entity includes three email address fields. Additional custom email fields can also be created if necessary.

This applies to Leads as well! Now, let’s discuss the impact on **emailing**.

##### 💌 Emailing

To send emails to different email addresses associated with a contact, we must adjust the **Audience Configuration** settings to select additional email fields.

Select Email Address 2 and Email Address 3 as additional email fields in the Audience Configuration.

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Setting-up-multiple-email-addresses-in-audience-configuration.png)

Now, when creating a Journey, we can choose from multiple email addresses.

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Select-the-email-address-field-in-the-email-in-the-journey.png)

But before sending emails, we need a **consent** record.

##### 🔒 Consent

To send an email, a consent record is typically required. The communication tab on the Contact entity displays the contactability of each email address rather than just the contact as a whole.

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Multiple-email-address-fields-on-the-communication-tab.png)

A contact who accesses the Preference Page from an email (regardless of which address received the message) can manage consent for all their associated email addresses.

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Multiple-email-address-fields-in-the-subscription-center.png)

**Consent Consistency & Shared Email Addresses**

1. Different email addresses may have different contactability statuses. Consider whether consent should remain consistent across them.
2. What if two contacts share the same email address? For example, Contact 1’s Email Address 2 matches Contact 2’s Email Address 1. This could allow them to alter each other’s contactability.
3. These scenarios require careful consideration when implementing consent management strategies.

Next, let’s talk about **matching rules** for form submissions.

##### 🔗 Matching

When using Marketing or Event Registration Forms in Dynamics Customer Insights - Journeys, it's crucial to configure Matching Rules properly. If multiple email address fields are used, determine whether to apply multiple Matching Rules. The contact should be matched based on the corresponding email address field used in the form.

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Mutliple-matching-rules.png)

This step is straightforward but easily overlooked!

Finally, let's discuss **email interactions**.

##### 📬 Email Interactions

To test this, I created a Journey that sent three different emails to the contact’s three email addresses. Here are the results:

![Dynamics Customer Insights - Audience Configuration for the Contact](/assets/images/blog/working-with-multiple-email-addresses-in-ci-j/Opens-of-different-email-addresses-for-different-emails.png)

On the Contact record, you can view email interaction results for all email addresses. However, you cannot directly see which email address each email was sent to.

A Power BI dashboard can help visualize this data. Check step 1 of <a href="https://marketing-lab.nl/work/ci-j-interaction-data-in-ci-d">this blog post</a> to learn how to set one up.

If multiple Contacts share an email address, email interactions are not shared across them. The relationship between an email interaction and a Contact is not based on the email address.

Is this a good or bad thing?

It depends on your scenario!

#### Wrap-Up

So here you have it, a good overview of the things to do and to consider when you are working with multiple email addresses.