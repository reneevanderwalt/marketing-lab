---
title: How To - Personal Event Calendar
pubDate: 2024-07-19
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'How To - Personal Event Calendar'
description: |
  Email the Sessions Registered in Customer Insights - Journeys
tags: ["event marketing", "email marketing", "events how to"]
---

When organizing events with multiple sessions, you want to ensure that registrants can create their own agendas. I have already <a href="https://marketing-lab.nl/work/session-registrations-how-to">written a post</a> on how to set up the event, but now I will look into communicating to registrants about their agendas. You can also check out the <a href="#how-to-video">video</a> at the bottom of this page.

So, we know how to <a href="https://marketing-lab.nl/work/how-to-create-event-reminder-journey">set up a reminder journey</a> for registrants; now let's take a look at how to add a personal agenda to these emails, so you can increase engagement and <a href="https://marketing-lab.nl/work/seven-tips-to-prevent-no-shows">lower your no-show rate</a>.

## Step 0 - Prepare Your Email Content

Set up your confirmation and reminder messages as usual. These can be emails, text messages, or push notifications.

## Step 1 - Let's Create a List

In the email, go to personalize and add a new list.

![Add a list in the personalize menu of the meail](/assets/images/blog/how-to-create-personalized-agenda/Add_list_to_email.png)

Set the list entity to session registrations from the event registration entity.

![Select the session registration entity from the event registration entity](/assets/images/blog/how-to-create-personalized-agenda/Select_Session_Registration_entity.png)

We want to sort them by start time of the session, so the sessions are in chronological order. However, we can only select fields from the session registration entity, which does not include the session start time. So, there are two solutions to this problem:

1. Create a field start time on the session registration entity and fill this with a Cloud Flow
2. There already is a N:N relation between sessions and event registrations, so use a Cloud Flow to create records based on the registered sessions

In both scenarios we use a different setup of the list, as you can see in the example below.

![Set up the list personalization based on session registrations or sessions](/assets/images/blog/how-to-create-personalized-agenda/List_item.jpg)

|     Step        |    Session Registrations                                              | Sessions                                         |
| :-------------- | :-------------------------------------------------------------------- | :----------------------------------------------- | 
| **List entity** | Session registrations from event registration entity                  | Sessions from event registration entity          |
| **Order by**    | Session start time (name of the field you created)                    | Start time                                       |
| **Columns**     | Use the advanced options to select the fields from the session entity | Select the needed fields from the session entity |


## Step 2 - Paste the Code

After you've created the list, you can copy the code and paste it in your email. You can adjust the order of the fields and add extra text to provide a good reading sentence.

![The list code copied into the email](/assets/images/blog/how-to-create-personalized-agenda/List_copied_in_email.png)

## Results

This is what the email looks like:

![Final email](/assets/images/blog/how-to-create-personalized-agenda/Final_email_result.png)

## How to Video

<video width="100%" controls>
<source src="/assets/images/blog/how-to-create-personalized-agenda/how-to-create-personalized-agenda.mp4" type="video/mp4">
</video>