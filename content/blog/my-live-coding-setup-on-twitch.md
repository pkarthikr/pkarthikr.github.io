+++
title = "My Live Coding Setup on Twitch"
date = "2020-08-23T16:11:39-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding",]
+++

It’s been close to 6 months since I started streaming my coding adventures on Twitch. I thought this would be a good time to sit down and write about my experience streaming on Twitch and what I have learned so far.

Numbers
-------

Till date, I have streamed for roughly 63 hours and have had ~270 hours of content being consumed. [Kevin Evans](https://twitter.com/kjevans2787) has been generous enough to subscribe to my stream, and that’s what contributes to a $7 figure (I am rich!). At some point, I aim to donate the money I earn through streaming to some charity, but thanks to the tax rules and conversion rates - it’s quite some time in the future.

Inspiration
-----------

Before I streamed on my personal channel, I used to be regularly streaming on [Amazon Alexa’s Twitch Channel](https://twitch.tv/amazonalexa) as a part of my work. But the streams I used to do on the official channel would be more prepared, and often would have at least a couple of weeks of preparation. On the contrary, my coding streams are totally unprepared and often me navigating uncharted territories.

I was initially apprehensive, as this would mean showcasing to the entire world that I need to google even the minor things (how do I add request interceptors, javascript splice method?). In this matters, [Jeff Blankenburg’s](https://twitch.tv/jeffblankenburg) streams provided the right motivation. I noticed when he used to get stuck, he would have the community help him and that gave me some confidence. After all, if _Jeff B_ can go wrong - I guess I can as well? :)

Content
-------

I started streaming about building Alexa Skills that I needed for myself and ended up building a few skills. As I use these skills in my daily life, I keep finding improvements and build on it in my streams. 

*   [Meal Planner](https://github.com/pkarthikr/alexa-meal-planner) - A Skill that plans our entire meal for the week.
*   [Voice Greetings](https://github.com/pkarthikr/voice-greetings) - A Skill that allows your friends to send you short and sweet audio messages wishing you.

I asked my audience what would they like to hear more through a Twitter poll and I saw a significant ask for exploring new Alexa Skills Kit APIs. So I sometimes explore a new API / release with just the public documentation. I’ve been able to cover the Timers API, Controls Framework and App to App Account Linking so far. These streams give me a way to look at our documentation / features from an outside developer’s perspective and take it back to the right team to highlight any improvements.

As I stream more, I plan to take up ideas beyond Alexa Skills and get my hobby project ideas up and running.

Schedule
--------

I did my first proper stream on 21st February and eased into a schedule in late March. I have been toying around with my schedule and am yet to find the right fit. I initially started doing late night streams (7:30 PM onwards) and found I would usually be very tired to focus on the streams.

The perfect time for me seems to be starting at 5:30 PM, but thanks to the pandemic - I am yet to find the right day to stream on. And people attending my streams have been gracious enough to let me experiment and continue to come back. I hope to figure out a schedule pretty soon.

Setup
-----

It is important to have a decent setup before you start streaming. Your mileage may vary a lot depending on the computer you have, so take a call based on your setup. I stream from my Macbook Pro - 15 inch (2018 model) along with an extended monitor. I use an Yeti Blue Mike in Space Gray for my recording and streaming process and found it to be really good for all my audio purposes. I used to use the inbuilt mike for recording, and switching to the Yeti has been a day-and-night level of difference in the audio quality. I had to play around with the different mike settings and the placement before you get the perfect audio quality.

For the camera, I use the Logitech C922 Camera. After the audio quality, the most amount of time I have spent went into getting the lighting and angle perfect so that my dark face seems visible and recognizable enough to the viewers.

For the background, Arpita had this idea of getting our bookshelf between our sofa along with some props in there. We got the A & K letterings from [Itsy Bitsy](https://itsybitsy.in/) and I turn them on during my streams. It’s just a good addition to my stream and no amount of green screen magic is going to beat that.

From what I’ve heard from other streamers, Streaming is way better on a powerful computer and with Windows as the Operating System. My current Mac has 16 GB RAM along with a 4 GB Radeon Pro Graphics Card and my streams are just fine. I do get the occasional hiccups here and there while streaming, but I’ve not seen a major difference and will continue to use my Mac for streaming purpose.

Here’s my streaming setup :

*   Macbook Pro - 15 inch, 2018 model
*   [Dell SE2416H Monitor](https://amzn.to/34Gu3nw)
*   [Apple Magic Keyboard](https://www.apple.com/shop/product/MLA22LL/A/magic-keyboard-us-english)
*   [Yeti Blue Mike - Space Grey](https://amzn.to/3baY8xD)
*   [Logitech C922 Camera](https://www.logitech.com/en-us/product/c922-pro-stream-webcam)
*   [Cable Manager](https://amzn.to/2RD2iqA)
*   [Callas Kitchen Stand](https://amzn.to/3l8oBS1)
*   [Lenovo USB Mouse](https://amzn.to/3gm0JGU)
*   [Amazon Basics Laptop Stand](https://amzn.to/32lB3oK)

Streamlabs
----------

I started out streaming with OBS, but soon ran into an issue where it would crash every time I opened Alexa Developer Console / AWS Console (which was a huge part of my stream). Luckily just around the time I started streaming, Streamlabs announced support for Mac OS, and that has luckily solved all my streaming issues. I start off the stream with a Starting soon scene that looks like this along with a peppy music track. This alerts followers that I am going live in a while and gives me some time to settle in before the stream (and set my hair).

Apart from this, I have a scene with just the cam view and another view to share my desktop along with picture in picture mode. Sometimes, I need to take a break between the stream to get some water (shoutout to HydroHomies) and I put on a scene for that. I manually switch between my scenes and do not use any streaming deck for the same. I do not understand the appeal of streaming decks but I guess they would be better suited once you have a huge audience following and want to jazz up your streams easily.

I recently setup a channel trailer and also added some panels for more information with the same design that I use for my scenes. All the designs were made by my wonderful partner, [Arpita](http://arpitakarthik.in/), who is a great illustrator and an UI/UX designer.

Engagement
----------

When it comes to engaging viewers, I loved Jeff’s idea of building a Casino bot that your viewers can chat with in the Twitch chat. There are quite a few ideas I have in mind to keep my viewers engaged - but all of them are work in progress and might see the light of the day after a while.

Streamlabs also allows you to setup GIFs to notify whenever a follow / raid / subscription event happens. I use that to thank new followers, any raiders & subscribers.

Apart from that, people who attend my streams sometimes help me out with debugging my code whenever I am stuck or ask questions, that I sometimes try and answer. One idea I’ve been toying with is to invite my viewers / other streaming friends to do pair programming sessions with and see what we can build together.

One other way to make streaming fun is by raiding other streamers (which is basically sending your viewers to another channel). This helps your viewers find other streamers and helps building a sense of community as well.

Here are a few streamers that I actively follow and would recommend you check out.

*   [LetMyPeopleCode](https://www.twitch.tv/letmypeoplecode)
*   [Jeff Blankenburg](https://www.twitch.tv/jeffblankenburg)
*   [Alison](https://www.twitch.tv/sprucemooseaaa)
*   [JoeMoCode](https://www.twitch.tv/joemocode)
*   [Justin Jeffress](https://www.twitch.tv/justjeffress)
*   [Goldzulu](https://www.twitch.tv/goldzulu)
*   [Sohan Maheshwar](https://www.twitch.tv/sohanmaheshwar)
*   [JBNunn](https://www.twitch.tv/jbnunn)
*   [Kevin Evans](https://www.twitch.tv/kevinevans)

Apart from these amazing streamers, there are a few folks like Oxygenbox, Akhilesh, Ashish and a host of others who hang out in my streams and make it quite interactive. They are the main reason why I find streaming quite a bit of fun.

What I love about streaming is, that it gives me the opportunity to stick to a consistent schedule to code and learn something new. And while doing so, I get to build a small community who are super interested in my work.

I’ve found streaming to be a good way to build content where I can explain my thought process and do monotonous things like installing libraries. Sometimes my viewers would enter into conversations, and we would have long unwinding conversations about random things. For any other filtered and prepared content, I intend to stick with my [Youtube Channel](https://www.youtube.com/channel/UC_3hmv5NVrruhuukWR6UFbQ) and this blog.

I hope you found this post informative and hopefully helps someone looking to stream an insight into how I do it. If you have any questions on streaming, reach out to me on [Twitter](https://twitter.com/pkarthikr) and I will be happy to help!
