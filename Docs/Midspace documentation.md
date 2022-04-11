# Introducing: Your Midspace Virtual Conference

Setting up an academic conference can be overwhelming—we know! When virtual conferences became the norm, event planners everywhere collectively skipped a heartbeat. We promise that setting up your virtual conference in Midspace won't be another headache for you.

This article will give you a brief overview of the core elements that make up your conference in Midspace. Here we'll define our terminology to help you visualize how your conference will look in the virtual world.

## 🧑 People

What would a conference be without people? There are two main categories of people in a Midspace conference: program people and registrants.

**Program people** are the people who contribute to your conference. This can include conference organizers, authors of content being presented, presenters of an event, or program chairs. A person doesn't need to be an attendee of your conference (AKA, a "registrant") to be a program person. For example, an author of a paper who will not be present at your conference would be a program person, but not a registrant.

**Registrants** are any people who are attending your conference. This includes any program people who will be present at your conference, too! Note that this would *not* include the author of a paper who won't be attending the conference.

## 📅 Events

Perhaps unsurprisingly, a conference's program schedule is made up of **events**. An event can be configured to have your attendees watch a live-streamed presentation, interact with selected content (like viewing a paper), participate in a Q&A, join a social gathering, and much more! Registrants can view and join your conference's events at the click of a button by using the calendar view in Midspace. Events are shown as blocks on the calendar that display a description of each event. If you know how to use Outlook or Google Calendar, then you know how to use the Midspace calendar. (If not, don't worry—it's easy!). Each event will have its own dedicated page where registrants can join in to watch, participate in interactive sessions, and access any media that the presenters have shared.

### Event Modes

There are endless options to customize what types of events will be in your conference. If this sounds overwhelming, no need to fear! We've come up with a few templates called "event modes" to guide you. Event modes are common event styles that can be implemented in your conference. Events are mainly characterized by the interaction between the attendees and the program people. The table below shows the most popular modes.

| Mode         | Description                                                  |
| ------------ | ------------------------------------------------------------ |
| Presentation | Attendees watch a livestreamed video of presenters speaking on camera (or sharing content, such as a slideshow, from their screen) |
| Q&A          | Attendees ask presenters questions through the chatroom, and presenters answer questions live on video |
| Video chat   | Attendees join a single video chat to socialize or discuss a topic |
| Exhibition   | Attendees join parallel video chats to discuss related pieces of content that are part of an exhibition |
| Video player | A pre-recorded video is shown to attendees to watch at their own pace (unlike a livestream) |
| None         | Combine different types of content and media for a custom event! |

**Note**: Event modes are not an actual UI element of Midspace—rather, they are concepts that can be implemented in a conference.

## 📃 Content

Papers, abstracts, presentations, and more! **Content** is the media that is associated with your conference's events. This can be an abstract, text, videos, images, slides, a website link, or something else. Content can be uploaded to a conference by the program people who are presenting it by using Midspace's submissions system. As a conference organizer, you can designate which program people should upload content for a particular event.

<div style="page-break-after: always;"></div>

# Setting up your Conference

The first step to setting up your conference is importing your existing program and registrant information using our import tool (think *people* and *events*). If you don't have any existing information to import, that's OK! Every element of your conference can be added manually within the Manage menu in Midspace. We recommend using the import tool since it's the fastest way to manifest your conference vision into (virtual) reality!

## Using the Importer

To import your conference, you'll need to create a .csv file. If you're not sure what that means, no worries! We'll walk you through the steps. The first step is to download the importer template by clicking the download button at the top of this page (you can select the option for Google Sheets or Microsoft Excel—choose whichever you prefer). Once you've done that, keep reading below and follow the steps to fill in the information about your conference.

> Advanced users can also choose to provide us with a JSON file containing your conference data that has been exported from another program. If this is you, please reach out to our support center for more info.

### Sessions

A conference's program schedule is made up of events, but in the import template we use the term "sessions". We'll go more into this later, but to put it simply, a session is an event on your conference's calendar that contains one or more related sub-events placed back-to-back on the schedule. (If you can't wait to learn more, check out [this article](example.com) about sessions, events, and presentations.)

The image below shows an example of the import file in Google Sheets for a conference called Insomniac Symposium 2022. It's a pretty short conference—there's only one session!

![an example import file in Google Sheets](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220322134912436.png)

Let's zoom in on our session. The title is "Presentations on Sleep Science". It starts on March 3rd, 2022, and has a duration of 90 minutes.

![the Session section of the import file](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220322135135941.png)

Once we import this file into Midspace, the session will appear as a block on the conference's calendar, pictured below.

![a session displayed on the Midspace calendar](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220328171753173.png)

### Presentations

As mentioned previously, a session is an event that is made up of one or more sub-events. These sub-events are labelled as "Presentations" in the import template. Below you can see that "Presentations on Sleep Science" is a session that contains two presentations and one Q&A.

![the presentation section of the import file](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220325170123478.png)

You should add this information to each presentation in your import file:

- **Title**: the name of your presentation
- **Type**: a label which describes what type on content is being presented
- **Duration**: the length of the presentation in minutes. *Be careful!* The durations of all presentations in a session must be equal to the total time length of that session
- **Abstract**: (optional). Here you can include an abstract for a paper being presented or a description of the presentation

>  Nothing is permanent! If you decide to change any of this information later, you can edit it after you import your file to Midspace.

After you give a title for each presentation, next you should select a type for each presentation. To learn about the different types of presentations, check out our documentation for [Content](../Midspace/Notes/Documentation/Midspace%20Concepts/Content.md).

![a dropdown menu for selecting the presentation type](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220325170419035.png)

In your conference, information about each presentation within a session will show on the information page for that session. Navigate to the information page by clicking on that session in the schedule and clicking "Find out more".

![the information menu for a session](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220322141131534.png)

![the top of the information page for a session](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220322141210539.png)

![the bottom of the information page for a session](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220322141216178.png)

### Speakers and Authors

Each presentation in a session can have program people added to it. These are the speakers and authors associated with that presentation. If a presentation has more than one speaker, a semicolon (;) should be used to separate each entry.

![the speakers and authors section of the import file](Midspace%20documentation.assets/Using%20the%20Importer.assets/image-20220325172451223.png)

<div style="page-break-after: always;"></div>