---
title: My Own Agenda – Session Registrations with Real-Time Marketing Forms
pubDate: 2024-02-02
image:
    url: 'http://localhost:4321/src/assets/images/posts/ab-testing-in-customer-insights-journeys.jpg'
    alt: 'My Own Agenda – Session Registrations with Real-Time Marketing Forms'
description: |
  Enhance user experience with personalized agendas. Follow 4 steps - feature switch, event setup, form usage, and customer journey creation. 
tags: ["landing pages", "event marketing", "events how to"]
---

Do you organize multiple events per year? And if you do, do you have multi-session events? Then, of course, you want registrants to schedule their own agenda and to capture this information directly in Dynamics Customer Insights. In the December release, we were finally enlightened with the feature switch for session registrations with forms. Want to know how it works?

## Steps in the process

There are four steps to achieve this:
1. The feature switch
2. Setting up the event
3. Using the registration form
4. Building the customer experience with a journey

## The Feature Switch
To access this functionality, you need to enable the feature switch in the Settings section of your Dynamics Customer Insights – Journey App.

![Set feature switch to yes](/assets/images/blog/session-registrations/Session_Registration_Feature_Switch.png)

When you do this, a couple of things happen in the background, but the most important one for us users is the creation of a new default event registration form, named “Default registration form with Sessions”.

## Setting up the Event

You can set up your event like you are used to. Fill out all the fields you need and create all the sessions you want. Here is an overview of an example event with multiple sessions at the same time.

![Overview of Event with multiple Sessions](/assets/images/blog/session-registrations/Overview_of_Event_With_Sessions.png)

To ensure registrants can schedule their own agenda on the form, we need to make sure that:

1. All the sessions are in live state.
2. The toggle “Allow registrants to create their own agenda” is set to yes. This toggle is available on the Agenda tab on your event.

![Set the toggle Allow registrants to create their own agenda to yes](/assets/images/blog/session-registrations/Allow_registrations_to_schedule_own_agenda.png)

### Set the Session in Live State
There are two ways to do that. You can do it directly from the quick create form by setting the “Publish status” to live.

![Use the Quick Create form to set the Session Live](/assets/images/blog/session-registrations/Quick_Create_Session.png)

Another way is directly from the session record and hitting the “Go live” button in the ribbon.

![Use the Go Live button on the session form](/assets/images/blog/session-registrations/Go_Live_button_session.png)

## Using the Registration Form

Enabling the feature switch creates a new registration form. Go to your Website and form tab on the event, and in the field “Registration form”, make sure you select the form “Default registration form with Sessions”.

![Set the correct registration form](/assets/images/blog/session-registrations/Set_Default_Registration_form.png)

### Changing the Registration Form
If you want to take a look at the form or make changes to this default form, read <a href="https://meganvwalker.com/finding-your-realtime-event-registration-forms/" target="_blank">this blog of Megan V. Walker</a> on where to find the form. The changes you can make on the form are:

1. Add or remove fields from the contact.
2. Change the styling of the form.
3. Update the display of the fields from the event entity.
4. Remove fields from the session entity.

One thing you cannot do is change the display of the session fields. For example, if you want to change the display of the session start time field to time only instead of date and time, you cannot do this (for now).

### Going Live

Once you’ve got everything in place, publish the event. A quick check-list:
- All your sessions are live
- Your toggle for “Allow registrants to create their own agenda” is set to yes
- You’ve selected the correct registration form
- You’ve published the event so the publish status is live

If you want to host the form on your page, you can now copy the script from the tab Website and form and paste it on your website.

## Building the Customer Experience with a Journey

Now the fun part begins, and you can build an entire customer experience with a journey, multiple emails, add-to-calendar buttons, QR codes, etc. Use <a href="https://paulinekolde.info/teams-webinar-lifecycle-journey/" target="_blank">this guest post</a> by Johannes Fleischhut on Pauline Kolde’s blog on how to set up such a journey.

## Some Final Thoughts

This is great news from Microsoft and again improves the event management functionalities in Dynamics Customer Insights. It is easy to set up, so you don’t have to worry about a lot of adjustments and can really improve the customer experience on event registration.

However, keep the following two things in mind:
1. You cannot change the session fields on the event registration form.
2. On the registration form, people can register themselves for multiple sessions at the same time. So they might have overlapping sessions in their schedules.