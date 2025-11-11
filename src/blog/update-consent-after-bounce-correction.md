---
title: Update Consent After Bounce Correction
pubDate: 2025-01-31
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'Update Consent After Bounce Correction'
description: |
  Learn how to update consent records after correcting bounced email addresses in Dynamics Customer Insights - Journeys. Follow our step-by-step guide to streamline your email marketing compliance process.
tags: ["email marketing", "gdpr"]
---

After reading this <a href="https://www.ameyholden.com/articles/email-bounce-lead-contact-view-form-dynamics-365-customer-insights-journeys" target="_blank">cool blog from Amey Holden</a>, my brain went into turbo mode. What happens after the correction?

This is what my amazing colleagues <a href="https://www.linkedin.com/in/dal%C3%AD-verschuuren-85a031102/" target="_blank"> Dalí</a>, <a href="https://www.linkedin.com/in/lotte-oudejans-343021147/" target="_blank">Lotte</a>, <a href="https://www.linkedin.com/in/nracorreia/" target="_blank">Nuno</a>, <a href="https://www.linkedin.com/in/marcovanderheyden/" target="_blank">Marco</a>, <a href="https://www.linkedin.com/in/robbertjacobs/" target="_blank">Robbert</a>, and I started thinking about. The email address that bounced must have received an email to bounce, right? So, it probably has some consent records attached to it. What if we automagically *transfer* these records to the corrected email address? 🪄 That's what we have built together, and I have the pleasure of showing you how!

### Updating Consent

Our starting point is the "Email Address Bounce Review Required" field on the contact. If this changes to 'No,' it means the email address has been updated to the correct one.

We start with a modified "Email Address Bounce Review Required" field on the contact.

![When a Contact is Updated](/assets/images/blog/update-consent-after-bounce-correction/When-a-Contact-is-Updated.png)

We then check if the field value equals 'No.'

![Check the value of Email Address Bounce Review Required equals NO](/assets/images/blog/update-consent-after-bounce-correction/Check-the-Value-of-Email-Address-Bounce-Review-Required.png)

Next, we list all the contact point consent records for the bounced email address (we used an additional field for this).

![List all Contact Point Consent Records for the Bounced Email Address](/assets/images/blog/update-consent-after-bounce-correction/List-All-Contact-Point-Consents-for-the-Contact.png) 

We then check if there are any contact point consent records listed.

![Check if there are any rows listed](/assets/images/blog/update-consent-after-bounce-correction/Check-If-There-Are-Rows-Listed.png)

This is the expression we used.

```go
length(outputs('List_All_Contact_Point_Consents_for_the_Contact')?['body/value'])
```
For each row, we check whether it is a **purpose** or **topic** contact point consent record. See the <a href="https://learn.microsoft.com/en-us/dynamics365/customer-insights/journeys/consent-record-creation" target="_blank">Microsoft documentation</a> on this as well.

![Check whether the consent record is a purpose or topic record](/assets/images/blog/update-consent-after-bounce-correction/Check-The-Contact-Point-Consent-Type.png)

Finally, we create new contact point consent records for the new email address.

![Create a Purpose Contact Point Consent Record](/assets/images/blog/update-consent-after-bounce-correction/Create-New-Purpose-Contact-Point-Consent-for-Contact.png)

For creating a topic contact point consent record, it should look like this.

![Create a Topic Contact Point Consent Record](/assets/images/blog/update-consent-after-bounce-correction/Create-New-Topic-Contact-Point-Consent-for-Contact.png)

Here is what the entire flow looks like!

![The complete Cloud Flow](/assets/images/blog/update-consent-after-bounce-correction/Final-Flow-To-Update-Consent-After-Bounce-Correction.png)

### Some Nice Adjustments to Consider

This is just a basic setup. You could refine it to make it look and work better ✨. Consider the following:
1. What if the 'corrected' email address is already in the system with an existing contact?
2. What if the 'corrected' email address already has contact point consent records attached to it?
3. Make the creation of these records optional; give the user the option not to create these records.
4. Should we make it a plug-in instead of a Cloud Flow?

### Special Thanks!

I want to give a special thanks to my colleagues who helped me build this cool flow. Big shout out to: <a href="https://www.linkedin.com/in/dal%C3%AD-verschuuren-85a031102/" target="_blank"> Dalí</a>, <a href="https://www.linkedin.com/in/lotte-oudejans-343021147/" target="_blank">Lotte</a>, <a href="https://www.linkedin.com/in/nracorreia/" target="_blank">Nuno</a>, <a href="https://www.linkedin.com/in/marcovanderheyden/" target="_blank">Marco</a> and <a href="https://www.linkedin.com/in/robbertjacobs/" target="_blank">Robbert</a>!

Thanks to <a href="https://www.linkedin.com/in/timo-bax-ab09572/" target="_blank">Timo</a> for the opportunity to get this group together in a mini-hackathon!

And to <a href="https://www.linkedin.com/in/amey-holden/" target="_blank">Amey</a>, for providing the starting point for this blog post!