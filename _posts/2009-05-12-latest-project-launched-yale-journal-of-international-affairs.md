---
title: 'Latest project launched: Yale Journal of International Affairs'
author: Justin Kiggins
layout: post
permalink: /2009/05/12/latest-project-launched-yale-journal-of-international-affairs/
dsq_thread_id:
  - 680509115
categories:
  - General
tags:
  - design
  - Drupal
  - portfolio
  - website
image: 2009/05/yjia-home-screenshot.png
---
Earlier this week, I launched my latest project: a new website for the [Yale Journal of International Affairs][1].

I&#8217;m really excited about how it turned out. The journal, which is run entirely by grad students at Yale, had accidentally lost their old website last year due to some payment mistakes (oops!). So, we built a new one.

The needs of the site were pretty straightforward:

*   Publish news about the organization
*   Maintain a calendar of events
*   Keep an archive of the journal&#8217;s issues & articles
*   Make it as easy as possible for the staff to update everything without any technical knowledge

The site was built in [Drupal][2], using [CCK][3] (especially the node reference functionality) for the [Articles and Issues][4] and using [Views][5] to organize the content.

*   The [News][6] page is simply a page view which displays the latest News items at the top of the page.
*   The [Archive][4] takes advantage of the new &#8220;grid&#8221; display feature in Views, showing a teaser image and the title of each Issue.
*   The [Current Issue][7] page is a full node view of the most recent issue of the journal: this makes it really easy to access the latest issue of the journal at the same page.
*   The [homepage][1] is built with views and an assortment of Views-driven blocks (I had originally intended to use Panels to drive the frontpage, but it wasn&#8217;t stable yet when I was developing the site).
*   The [Events][8] are being displayed from 30boxes. Even though Drupal has modules for making events, 30boxes was an easy way to just pull

The theme was built on top of the [Zen theme][9]. It had been a few years since I had used the Zen theme as a starting-point for a Drupal site and it has definitely come a long way since 2005! I was really impressed with how solid the documentation was and, combined with [Firebug][10] and [MAMP][11], how easy it was to go from a visual design concept to a live site.

Special thanks to Diana Chu and the folks at YJIA for helping get everything together to launch this.

Take a look at the site, poke around, and let me know what you think!

[Yale Journal of International Affairs][1] [<http://yalejournal.org>]

 [1]: http://yalejournal.org
 [2]: http://drupal.org
 [3]: http://drupal.org/project/cck
 [4]: http://yalejournal.org/archive
 [5]: http://drupal.org/project/views
 [6]: http://yalejournal/news
 [7]: http://yalejournal.org/current-issue
 [8]: http://yalejournal/calendar
 [9]: http://drupal.org/project/zen
 [10]: http://getfirebug.com/
 [11]: http://www.mamp.info/