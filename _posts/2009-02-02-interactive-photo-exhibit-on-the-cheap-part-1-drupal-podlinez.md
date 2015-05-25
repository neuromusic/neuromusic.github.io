---
title: 'Interactive photo exhibit on the cheap, part 1: Drupal &#038; Podlinez'
author: Justin Kiggins
layout: post
permalink: /2009/02/02/interactive-photo-exhibit-on-the-cheap-part-1-drupal-podlinez/
dsq_thread_id:
  - 680509125
categories:
  - General
tags:
  - Drupal
  - Howto
  - Podcast
  - Podlinez
  - portfolio
image: 2008/10/fuse06.jpg
---
In April 2008, [COAR][1] launched a photo exhibit with artist [Eliza Gregory][2]. Titled &#8220;[FUSE: Portraits of Refugee Households in Metropolitan Phoenix][3],&#8221; the exhibit sought to raise awareness in the community regarding Phoenicians&#8217; newest neighbors. From the summary of the exhibit:

> FUSE is a portrait exhibit of the complex worlds of resettled refugees in the Phoenix metro area. It fosters critical thinking on who refugees are and how, through sharing experiences, the Phoenix metro community can seek common ground. The photographs validate the struggles and triumphs of these families, portraying them in a way that cultivates a deeper sense of belonging in the community.

In order to support this effort, I helped put together an integrated system, allowing audience members to engage on a more direct level with the portraits.

Using podcasts of interview clips with the refugee subjects of the photos allowed us replicate on a very tight budget what would be quite expenisive with a proprietary museum guide system. With [Podlinez][4], audience members could also call a phone number printed next to the portrait in order to hear the podcast.

Finally, audience members were also able to give feedback on the exhibit via SMS, which was compiled into a Twitter feed for the exhibit (I&#8217;ll describe this last piece later, in Part 2).

### Beyond the photographs: audio portraits via podcast

So, here is the basic outline of the system:

*   Audio interviews with the photographic subjects were performed by Rose Love Chou during photography sessions. Later, she selected and edited clips in consultation with Eliza Gregory & saved them as mp3 files.
*   COAR&#8217;s website already uses [Drupal][5] with the [CCK][6], [Views][7], & [Pathauto][8] modules among others. A few other modules needed to be installed, too, to handle the media files nicely. These were then setup to present a podcast and interactive pages online.
*   The podcast RSS feed was run through [Feedburner][9] to clean up downloads, and offer users who might not be familiar with podcasts a bit more guidance.
*   Feeds for each of the audio files were submitted to [Podlinez][10] to handle call-ins.
*   Donated mp3 players were preloaded with the audio portraits and left at the entrance to the exhibit.
*   Phone numbers were printed on the labels so that people could call and listen to the audio through their cell phone.

### Setting up the podcast in Drupal

I&#8217;m not going to go through the nitty gritty details of installing Drupal modules, but here is the list of modules we used for this system:

*   CCK
*   Views
*   Pathauto
*   Image_field
*   Imagecache
*   Token
*   Audio Field
*   Media Field Display

Drupal&#8217;s framework is incredibly flexible, allowing you to do amazing things with just a little bit of elbow grease. This was all done under Drupal 5, so I am not going to go into too much detail with the configuration because the details are probably out of date even though the concepts are still valid with the new CCK and views modules.

### The &#8220;portrait&#8221; content type

Drupal is built around nodes (units of content). For our purposes, we wanted a &#8220;portrait&#8221; to be our content type. Each content type will have a photo, a number (the title), and a caption. Some of the content will have an mp3 audioportrait as well.

So, we first create a new custom node type and called it **portrait**. Then, we add the following CCK fields: **photo** (an image field), **photo_caption** (a text field), and **audioportrait** (an audio field).

Next, we can go to pathauto settings and set the URL pattern for each portrait to be **fuse/portraits/[title] **

Now, to control the visual presentation of the content we can do a few things. First, we can use Imagecache to setup automatically resized versions of the uploaded photo. Then, we can go to the view option for the content type and change the presentation of each of the fields. For example, we can get rid of the labels for each field, set the image field display mode to the resized image_cache version, and set the display for the audioportrait to the Media Field Display. That last one will let the users play back the audio portrait right in the browser.

### The bread-and-butter: Views

Next, we use the views module to setup each of the views for the different modes of presentation. This is the key to the whole deal because it lets us build the actual feeds for the podcast and for Podlinez.

*   The **fullpage** view is simply a &#8220;full node&#8221; view set to only presenting one node per page. This uses the &#8220;full page&#8221; version of the node (and therefore, all of the display options we setup before) with &#8220;pagers&#8221; turned on so that the user has &#8220;next&#8221; and &#8220;previous&#8221; arrows at the bottom of the page.
*   The **podcast** view is a &#8220;table&#8221; view with the only the title and audioportrait fields displayed. We also add the &#8220;RSS: RSS Feed Selector&#8221; argument in order to present all of the portraits with audio in podcast form. Instructions for downloading the podcast was inserted into the header of the view. The podcast was also pre-loaded onto three mp3 players that were donated by local businesses.
*   The **podlinez** view is of the type &#8220;Views RSS: RSS Feed&#8221; tweaked to deal with Podlinez. Since Podlinez will only playback the most recent episode from a podcast, there is no way for the user to browse through all of the audioportraits. By allowing the portrait number to be passed as an argument to the view, each audioportrait gets &#8220;it&#8217;s own&#8221; single-episode podcast.

### Accessing the audio through Podlinez

Podlinez is a free service that lets you call a podcast from a phone. You simply submit the URL of the podcast feed and they kick back a phone number. They preface the podcast with a &#8220;brought to you by Podlinez&#8221; kind of ad. They cull the list of numbers periodically, though, so if no one calls your podcast for more than two weeks, you might lose your number. It was brought to my attention by [Casey Muller][11].

Since you have a list of feeds (one for each file) from the view you setup in Drupal, simply go to the Podlinez homepage and drop that URL into their phone number generator.

***Word of caution:**** Be sure to test your phone numbers before &#8220;going live&#8221; and printing panels with phone numbers on them. Sometimes the numbers that they give you don&#8217;t work. This can be particularly problematic if you are trying to throw this together at the last minute, hours before opening, like I was. I tried adding the feed again and it would tell me &#8220;We already have a phone number for that feed&#8221; and give me the non-working phone number. The tech people at Podlinez were quite helpful in taking down such numbers, but you should give yourself a few days before opening to get the kinks worked out.  
*

### Shouldv&#8217;e, could&#8217;ve, would&#8217;ve&#8230;

In hindsight there were a few things that I would pay closer attention to if I were to do this again:

*   **Podlinez is not perfectly reliable.** As mentioned above, some of the numbers didn&#8217;t work when I first added the feeds. Some stopped working a few weeks into the show.
*   **The donated mp3 players were of poor quality.** One stopped working after the first week. Another after two months. They were basically the cheapest ones that Best Buy was willing to give up when the team went hunting for in-kind donations.
*   **Needed to use better equipment for recordings.** To say the least, there were sound quality issues. By the time the audio has been digitized, compressed to mp3, recompressed by podlinez, squeezed through the cell phone signals into a museum with bad signal, & played out on a bad cell phone speaker, a soft spoken non-native English language speaker can be quite difficult to understand. The only way to fix this would have been to acquire the audio at a better signal-to-noise ratio, with professional audio equipment. That costs money, though.
*   **User interface wasn&#8217;t clear at the exhibit level.** Most people didn&#8217;t notice the phone numbers on the labels unless they were told. There was no graphic, no bold, no typeface changes at all to indicate that you could call the phone number and listen to a story from the person you were looking at in the photograph. All there was was a phone number underneath the description on around 2/3 of the photos.

### Stay tuned for Part 2&#8230;

I&#8217;ll post soon on Part 2 of this series, which will cover adding the &#8220;interactive&#8221; layer to the system: using 4INFO, Twitter, Yahoo Pipes, and a few other tools to let audiences respond to the exhibit in real time.

 [1]: http://www.coarweb.org "COAR: Community Outreach & Advocacy for Refugees"
 [2]: http://www.elizagregory.com/ "Eliza Gregory makes awesome photographic art"
 [3]: http://www.coarweb.org/fuse "FUSE: Portraits of Refugee Households in Metropolitan Phoenix"
 [4]: http://www.podlinez.com/ "podcasts via phone"
 [5]: http://drupal.org "Drupal rocks my socks"
 [6]: http://drupal.org/project/cck "CCK is lets you add specific fields to different pieces of content"
 [7]: http://drupal.org/project/views "Views lets you present different lists of content and, with CCK, different aspects of content"
 [8]: http://drupal.org/project/pathauto "Pathauto automates user-friendly URLs"
 [9]: http://www.feedburner.com/
 [10]: http://www.podlinez.com/
 [11]: http://casey0.com/