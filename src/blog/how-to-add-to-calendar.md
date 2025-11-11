---
title: How To - Dynamic Add to Calendar link
pubDate: 2024-06-10
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'How To - Dynamic Add to Calendar link'
description: |
  Using an Add to Calendar Link in Customer Insights - Journeys
tags: ["email marketing", "event marketing", "events how to"]
---

Organizing multiple events per year can be quite challenging, especially when setting up different journeys, emails, and segments. However, you can reuse some content and make it dynamic. In this “How-to” post, I will show you step-by-step how to make your confirmation email with an Add-to-Calendar link dynamic. You can also check out the <a href="#how-to-video">video</a> at the bottom of this page.

This Add-to-Calendar link  is easy to add, but can make a big improvement on your <a href="https://marketing-lab.nl/work/seven-tips-to-prevent-no-shows">no-show rate</a>. No time to waste!

## Step 0 - Prepare Your Calendar Content

It is convenient for registrants to add the calendar item to their calendar, but it holds little value if it's empty. To enhance your Calendar Item, go to the Additional Information tab on your event and scroll down. Here, you can add all extra details about your event. If you have selected a Building on your Event as well, make sure to add the address details, because they are shown in the location of the Calendar Item as well.

![Calendar content](/assets/images/blog/how-to-add-to-calendar/Calendar_content.png)

## Step 1 - Set Up Your Confirmation Email

Set up your confirmation email as usual. Make sure to include a button or, less preferably, a text link.

![Create your email](/assets/images/blog/how-to-add-to-calendar/Creat_your_email.png)

## Step 2 - Create an "Add to Calendar" Link

Ensure the URL type is an "Add to Calendar" link.

![Make the button an Add to calendar button](/assets/images/blog/how-to-add-to-calendar/Button_link_to.png)

## Step 3 - Make the Link Dynamic

Set the field ‘Select Event/Event registration’ to **From other source**.

![Set the Event to Other source](/assets/images/blog/how-to-add-to-calendar/From_other_source.png)

## Step 4 - Select the Correct Attribute

Use the ‘Event’ from the Trigger ‘Marketing Event Registration Created’ by using the Marketing Event Registration entity.

![Select the correct field](/assets/images/blog/how-to-add-to-calendar/Select_the_correct_field.png)

## Step 5 - Use It in a Journey

The final step is to create the Journey by using the Marketing Event Registration Created trigger and specifying your event.

![Create the Journey](/assets/images/blog/how-to-add-to-calendar/Final_journey.png)

## Results

And here you can see the results in your registrants' calendar!

![Calendar item in Outlook](/assets/images/blog/how-to-add-to-calendar/Calendar_item_outlook.png)

## Next Steps

Now you know how to build your own dynamic Add-to-Calendar link. There are many other options you can make dynamic in this email, such as:

- Event name
- Event dates
- Event location
- Event speakers

## How to Video

<video width="100%" controls>
<source src="/assets/images/blog/how-to-add-to-calendar/How-to-add-to-calendar-link.mp4" type="video/mp4">
</video>