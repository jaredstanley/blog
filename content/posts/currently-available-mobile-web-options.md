---
title: The Currently-Available Mobile Web Options
description: The mobile space is still largely undefined and proprietary and is changing all the time.
month: 12
day: 03
year: 2012
---
The mobile space is still largely undefined and proprietary and is changing all the time.
Following up on this post, I want to discuss all the different mobile solutions available today.

<br>


## Some Stats & Definitions
The mobile arena is so fragmented that I want try to wade through the terminology and base the discussion on some defined parameters:

<br>

### Offline Mobile Web Apps:
Websites that are accessible via the browser, and once bookmarked on the phone are accessible whether the phone is connected to the internet or not.

<br>

### Tablet vs Phone vs Desktop vs Laptop:

I’m going to group these in to two categories:

<br>

1. **Phones:** I’m grouping tablets in with phones.

2. **Computers:** I’m grouping laptops in with desktop computers.

<br>

(“Preposterous! Tablets and laptops should be in the same category! They’re essentially the same thing! That classification won’t include the tablet/laptop hybrids omg!!!”.) It’s not a precise division but for all intents and purposes this will suffice for this article.
This grouping is based on access and use:
**Phones/Tablets** are sometimes wi-fi connected, sometimes cell-service connected, and sometimes offline. In general they are used to consume content.
**Desktops/Laptops** are in general always connected, and used in one place. They are used to both produce and consume content.

<br>

### Smartphone vs Feature Phone:

[Roughly half](http://www.comscore.com/Press_Events/Press_Releases/2012/8/comScore_Reports_June_2012_U.S._Mobile_Subscriber_Market_Share) of (U.S.) mobile users are on [smartphones](http://en.wikipedia.org/wiki/Smartphone); the other half use [feature phones](http://en.wikipedia.org/wiki/Featurephone). Smartphones for purposes of this post are defined as a phone that can browse online content; feature phones are everything else. We will only discuss smartphones(remember, I’m including tablets in here as well). FYI I’m only talking about half of the population of one country; this is the population that many of the clients I work with want to reach so that’s who i’m focused on here.

<br>

### Accessing Content
Pretty much 100% of developers ever have sat with a client and had to respond to this statement:

<br>

*“WE NEED AN APP.”*

<br>

Whether they’re referring to a mobile app or a native app or a facebook app or a web app or whatever else, for some reason everybody thinks they need an app. 
<br>
1.Think of idea 
2.Build app 
3.PROFIT!

<br>

People want their customers/users to access their content via their smartphone via the internet.
Smartphone users can access content via the internet through the browser or through a native app directly.
Here are the good and bad about each:

<br>

**Website:** Just a regular website. Just a normal website that loads into a phone’s browser pretty much just like it loads into a desk-/laptop’s browser.
<br>
*GOOD:* Inexpensive – no additional effort beyond building a website is required
<br>
*BAD:* Site doesn’t work that well on mobile. Everything is shrunk to fit, you have to zoom and pan around to read anything.

<br>

**(Mobile-Optimized) Website:** same as above, but the content is formatted differently to be easier to read/use on a smaller screen.
<br>
*GOOD:* Same content delivered to desktop users, but presented so it’s easier to read on a smaller device(bigger buttons, etc).
<br>
*BAD:* Additional development time, additional IA/UX time(your site’s existing ten nav items, each w their own drop-downs doesn’t just automagically work on a teeny screen), additional design/UI time. THEN you gotta make sure it works on the androids and the iphones etc etc. All this = more $$, and then you still have technical limitations(ie you can’t have a smoothly-animating game that ppl are used to on their phones, or have access the camera functionality or access to much of the other hardware that makes the phone so cool. *note that you do have some access to things like geo-location etc, but understand you’re limited).

<br>

**(Native/Mobile) Application:** a file downloaded from the internet(usually via store/marketplace etc).
<br>
*GOOD:* Same as the Mobile-Optimized site, plus you have the ability to access all of the hardware APIs(read: 3D games, photo-editing capabilities, etc), easier to monetize. Indexed in ‘app stores’ so that’s potentially good in terms of findability, legitimacy, etc.
<br>
*BAD:* Same as the Mobile-Optimized site x10. You need a developer with a specialized skillset(ie objective-C w app-store approval experience). Must first be downloaded from an app store(iOS), and once you’re done you still only have one type of device completed.

<br>

TODO: explain Sencha/Titanium/other write-once-deploy-everywhere hybrid apps – good in some situations but kind of end up being master of none – show best examples and how they’re not very good.

<br>

TODO: explain html5 and how steve jobs lied! and how it doesn’t just solve mobile.
(Caveat time: Laptops can be carried around, and can be used to work offline. Keyboards can be purchased to connect to tablets, and you can awesome albums via GarageBand on a tablet.
I would 1.argue that if you’re doing these things exclusively that you’re an outlier and 2.remind you that these definitions are necessary to discuss this mobile space so I’m going with them here. The tablet/laptop hybrids would then technically share both categories…)

<br>