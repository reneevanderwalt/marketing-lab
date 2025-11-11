---
title: Responsive Two-Column Email Design - A How-To Guide
pubDate: 2025-03-14
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'Responsive Two-Column Email Design: A How-To Guide'
description: |
  Learn how to create a visually appealing two-column reversed (Z-pattern) section in email templates for mobile responsiveness using Dynamics Customer Insights - Journeys. A step-by-step guide with HTML adjustments and styling tips included!
tags: ["email marketing"]
---

Since the moment I first touched email HTML, I learned that nothing is what it seems! You create a beautiful email in Customer Insights - Journeys and feel amazed by your own creativity. But the moment you hit send, you receive a thousand different versions of the very thing you just created. Outlook doesn’t support custom fonts, Gmail cuts off your email after a certain size, and the list goes on.

One of the things I hate the most is when a desktop two-column Z-pattern looks like this 👇:

![Two-column Z-pattern section](/assets/images/blog/two-column-mobile-design/Two-column-z-patterned-section.png)

But the mobile version looks like this 👇:

![Ugly mobile version of Z-pattern](/assets/images/blog/two-column-mobile-design/Ugly-mobile-version-of-z-pattern.png)

<span style="font-size: 48px;">😭😤👿</span>

So let’s fix this! And trust me, this is a really short blog 😉

### Step-by-Step Approach

#### Step 1 - Setting Up Your Desktop Version

In your email template, create Z-pattern two-column sections and add your images and text to the columns.

#### Step 2 - Adjusting the HTML

Thanks to the user-friendly email HTML editor, we can easily locate the HTML code for the columns. Open the HTML editor and click on the left column containing the text. In the first blue-highlighted `td` element, add the class `bottom`, as shown in the image below.

![Left column of lower section](/assets/images/blog/two-column-mobile-design/Select-left-column-and-add-bottom.png)

Next, select the right column containing the image. In the first blue-highlighted `td` element, add the class `top`, as shown below.

![Right column of lower section](/assets/images/blog/two-column-mobile-design/Select-right-column-and-add-top.png)

#### Step 3 - Adjusting the `<style>` Section

When you open the HTML of the email, you won’t see the final HTML and styling of the email. After you hit publish, Dynamics automatically adds extra lines of code for mobile responsiveness and Outlook compatibility. (This is why you need to copy the **actual** HTML code when <a href="https://marketing-lab.nl/work/sustainability-in-email-marketing">measuring the carbon footprint of your email</a>.)

To enhance mobile responsiveness, we need to modify the media query. Add the following code before the closing `</style>` tag in your `<style>` section:

```css
@media only screen and (max-width: 768px) {
    .multi tbody tr th.top { 
        display: table-header-group !important; 
        width: 100% !important; 
    }

    .multi tbody tr th.bottom { 
        display: table-footer-group !important; 
        width: 100% !important; 
    }
}
```

Your email HTML code should now look like this:

![Adjusted HTML in the style section](/assets/images/blog/two-column-mobile-design/HTML-style-adjusted.png)

#### Step 4 - Test Your Work

Save your email and send yourself a test email or <a href="https://marketing-lab.nl/work/how-to-send-live-test-email">live test</a> to review the mobile results.

![Pretty mobile version](/assets/images/blog/two-column-mobile-design/Pretty-mobile-version-of-z-pattern.png)

<span style="font-size: 48px;">🤓😁🤩</span>

#### Step 5 - Create a Content Block

I highly recommend creating a content block for this section. This allows you to easily reuse them in your templates, with the HTML adjustments already in place.

### Wrap-Up

If you're using this two-column reversed (Z-pattern) section in your email templates, you now know how to make it look great on mobile devices too! This applies to all two-column sections, by the way, so if you use the 1/3 - 2/3 two-column section, you can apply the same technique! Good luck 🍀