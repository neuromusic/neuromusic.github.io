---
title: in the future, the scientific literature will follow you
author: Justin Kiggins
layout: post
permalink: /2012/08/16/in-the-future-the-scientific-literature-will-follow-you/
disqus: True
dsq_thread_id:
  - 812088237
categories:
  - General
tags:
  - featured
  - following the literature
  - ideas
  - scientific publishing
image: 2012/08/future.jpg
---
Of the 1+ million new scientific papers published each year, **which ones should a scientist read**?

Its obvious that any single researcher can&#8217;t read them all. Nor do we want to&#8230; the overwhelming majority aren&#8217;t relevant to us or our work. We limit what we read and we employ variety of methods to chose what new research we do read&#8230; a strategic foraging task utilizing a hodge-podge set of tools, including subscribing to journals or RSS feeds, saved Pubmed searches

But times are a-changin&#8217; for academic publishing and some of the changes are very similar to [those in journalism][2]:

> The publisher of a major international newspaper once told me that he delivers “the five or six things I absolutely have to know this morning.” But there was always a fundamental problem with that idea, which the Internet has made starkly obvious: There is far more that matters than any one of us can follow. In most cases, the limiting factor in journalism is not what was reported but the attention we can pay to it.

The goal of *personalized news*—news that is tailored specificially to me—[is hot but unrealized][3]. I recently came across an article by [Jonathan Stray][4] proposing [three principles that ought to govern personalized news: *interest, effects,** ***and *agency*.][2]

> You should see a story if:
> 
> 1.  You specifically go looking for it.
> 2.  It affects you or any of your communities.
> 3.  There is something you might be able to do about it.

This got me thinking about what these principles mean for &#8220;following the literature&#8221;. In particular, how would one develop a strategy for research literature discovery (typically known as &#8220;following the literature&#8221;) that embodies these principles, where the **literature follows the researcher**?

## Interest

> **Anyone who wants to know should be able to know.** From a product point of view, this translates into good search and subscription features. Search is particularly important because it makes it easy to satisfy your curiosity, closing the gap between wondering and knowing.

This is perhaps the most obvious minimal requirement&#8230; to be able to find things that I&#8217;m looking for. This is a passive feature of a system for research literature discovery&#8230; I take the action. I decide when I want to know about something. I search for &#8220;Lastname et al, 2003&#8243; after seeing the reference at the bottom of a figure in a presentation. I go hunting for a recent paper that someone mentioned to me at the coffee cart.

There are already some very good tools out there for this. Pubmed & Google Scholar are my go-to sources. So, for scientists at least,* I&#8217;m going to consider this a problem basically solved and move on&#8230;

## Effects

> **I should know about things that will affect me.** Local news organizations always did this, by covering what was of interest to their particular geographic community. But each of us is a member of many different communities now, mostly defined by identity or interest and not geography. Each way of seeing communities gives us a different way of understanding who might be affected by something happening in the world.

Did I get scooped? Did someone cite my work? Is there a new paper that changes the way I interpret my not-yet-published results?

These are harder, more time consuming questions to answer by relying exclusively on a search-based interface. Historically, these questions would have been answered by subscribing to specialized &#8220;society journals&#8221;&#8230; The Journal of Obscure Sub-Subfield. More common today are custom filters and saved searches. For example, [here&#8217;s Bradley Voytek&#8217;s strategy][5]:

> *   PubMed&#8217;s &#8220;MyNCBI&#8221; <a href="http://www.ncbi.nlm.nih.gov/sites/myncbi/" target="_blank">saved searches</a> for specific authors and keywords
> *   <a href="http://www.google.com/alerts" target="_blank">Google alerts</a> for the same
> *   RSS feeds or email alerts for my favorite dozen or so journals
> *   RSS feeds for [arXiv.org][6], <a href="http://researchblogging.org/" target="_blank">Research Blogging</a>, as well as a mix of science and tech blogs

Similarly, Drugmonkey [polled his readers a while back on how they keep abreast of the literature][7]. The responses [(summarized here)][8] include everything from tools like [pubcrawler][9] to relying on blogs, journal RSS feeds, to making graduate students do it.

Its obvious that everyone is looking out for papers that will affect them&#8230; but can we do better? All of these together are (1) cludgy, (2) require a lot of time and effort to setup and tailor, and (3) require the researcher to *already know what will affect them*. To a certain extent, the third isn&#8217;t a huge problem&#8230; its obvious that my collaborators&#8217; and competitors&#8217; work will affect me and a huge part of our role as scientists in knowing what the state of the field is and how it will affect our work.

But what about the &#8220;[unknown unknowns][10]&#8220;?

What if a system could leverage existing sources about what will affect me to predict which new papers I should know about? What if it could use a researcher&#8217;s publications, personal library of papers, and network of friends & colleagues to assess newly published papers for &#8220;likelihood of effect&#8221;?

A big breakthrough in this direction was launched recently with Google Scholar&#8217;s &#8220;My Updates&#8221; feature ([see Jonathan Eisen&#8217;s summary here][11]), which analyzes a researchers past publications to predict relevance of papers to them. One shortcoming of this approach is that its usefulness will be more limited for graduate students (especially those in their early years) who will have fewer publications to their names than a tenured professor.

A similar approach (still in Beta) is [Mendeley Suggest][12], which (apparently) leverages a user&#8217;s library, compares it with other users&#8217; libraries, and makes suggestions for relevant papers. Mendeley Suggest certainly brought a few papers to my attention that affect my work, but they were all 5-10 years old. Not exactly a great tool for keeping tabs on new papers. Practically speaking, a better approach might be to take something like the [ScipleRSS][13], which ranks the results of a batch of journal RSS feeds according to a set of weighted keywords, and use the Mendeley API to set the keyword weightings based on a users actual library ([if I ever have time, I&#8217;d like to actually do this][14]). Having access to the user&#8217;s use-statistics for the papers in their library, as well as social aspects (what papers were recently added by Mendeley contacts? by other users in Mendeley Groups?) could make such a prediction system even more powerful. Regardless of whether this is the best approach, there&#8217;s room for improvement here and Mendeley seems like a good place to start.

Beyond these emerging projects, its hard to imagine exactly where the future lies&#8230; if a system had enough data about you, your research, and the broader context you work in (say, your publications, grants, manuscripts, library, conference attendance info, which posters you stood in front of, the funding climate in your field), would it be able to make broader predictions for which papers would &#8220;affect&#8221; you? Would it be able to know that some paper in a totally different field solved a problem in a way that informed your own work, even though the research programs might not share any keywords?

Its not clear where the boundary is, but it is clear that this area is ready for some innovation, at least as it relates to improving the efficiency of alerting researchers to relevant new work.

## Agency

> Ultimately, I believe journalism must facilitate change. Otherwise, what’s the point? This translates to the idea of agency, the idea that someone can be empowered by knowing. But not every person can affect every thing, because people differ in position, capability, and authority. So my third principle is this: **Anyone who might be able to act on a story should see it.** This applies regardless of whether or not that person is directly affected, which makes it the most social and empathetic of these principles.

Science must also facilitate change&#8230; it must change the way that we view the world and thus, the way we respond to it. Our primary goal as scientists is to produce knowledge. But as [John Archibald Wheeler][15] described it, &#8220;We live on an island surrounded by a sea of ignorance. As our island of knowledge grows, so does the shore of our ignorance.&#8221; Every &#8220;answer&#8221; begets multiple more questions. (So really, we&#8217;re talking about a hyper-island in some multidimensional ocean) One of the primary challenges of a scientist is knowing in which direction to extend the island of knowledge.

And yet, all scientists are constrained by resources preventing us from extending the entire island at once. Not just money, but by the technical skills of trainees in the lab, the types of equipment that a lab has access to, the experiments that are available through collaborations. In deciding the direction that a lab should take (which projects to put into a grant, which ones to pilot, which grad students to accept), a researcher has to take all of these resource constraints into account, while recognizing the unique resources and opportunities available to determine the key areas where a lab can be productive.

Ultimately, the need for being able to have access to research we are interested in and to be alerted to research that affects us is meant to support this primary goal of producing new knowledge.

But could a research literature discovery system support this endeavor more directly through **ensuring that a scientist knows about research that they might be able to act on**?

There is a section in Michael Nielsen&#8217;s [*Reinventing Discovery*][16], where he imagines a future scenario in science:

>  You&#8217;re a theoretical physicist working at the California Institute of Technology (Caltech), in Pasadena. Each morning, you begin your work by sitting down at your computer, which presents to you a list of ten requests for your assistance, a list that&#8217;s been distilled especially for you from millions of such requests filed overnight by scientists around the world. Out of all those requests, these are the problems where you are likely to have maximal comparative advantage. Today, one of the requests immediately catches your eye. A materials scientist in Budapest, Hungary, has been working on a project to develop a new type of crystal. During the project an unanticipated difficulty has come up involving a very specialized type of problem: figuring out the behavior of particles as they [diffuse] on a triangular latticework. Unfortunately for the materials scientist, diffusion is a subject they don&#8217;t know much about. You, in turn, don&#8217;t know much about crystals, but you are an expert on the mathematics of diffusion, and in fact, you&#8217;ve previously solved several research problems similar to the problem puzzling the materials scientist. After mulling over the  diffusion problem for a few minutes, you&#8217;re sure that the problem will fall easily to mathematical techniques you know well, but which the materials scientist probably doesn&#8217;t know at all. [&#8230;]

Long story, short, you collaborate & everyone wins. This vision will require some major changes in the way science is done before it will be fully realized. However, a key principle here is that the theoretical physicist is alerted to a problem not based on her interests or whether his research program is affected by the work of the materials scientist in Budapest, but rather because she has **agency** in the topic. And we can similarly imagine a framework where a scientist is alerted to new publications not just because they are interested in the topic or because it affected them, but rather **because they are uniquely situated to do the next experiment**. Maybe they are an evolutionary anthropologist with a dataset, who could be alerted to [a recently published model of neandertal ancestry][17] that they were uniquely equipped to validate or invalidate. Or a molecular biologist with the perfect combination of reagents, gizmos, and trainees to try to replicate claims of a bacteria being able to survive on arsenic.

Is this possible? I think so. Stack Exchange is already aiming to [predict which users are best equipped to answer which questions][18] (a goal with striking similarities to Neilson&#8217;s imagined future for scientists). Imagine a system that has knowledge of a lab&#8217;s skills based on the CVs or Linkedin profiles of the members and the &#8220;Methods&#8221; sections of publications, combined with a detailed knowledge of the lab&#8217;s inventory (say, based on some lab management software like [Labguru][19] or [Quartzy][20]) and potential collaborations (based on past collaborations from the publication record and knowledge of the lab&#8217;s social network, pulled from [Mendeley][21] or Linkedin or [ResearchGate][22]). Then cross reference all of this against, say, the methods sections of recent publications&#8230; or better yet, against semantic analysis of post-publication peer-review commentary *about* a publication (which is where most of the ideas about the &#8220;next experiment&#8221; are likely to be found) such as [F1000][23], Twitter, [research blogs][24], [hypothes.is][24], etc.

The key here is that not only are scientists affected by what others publish, but we have the opportunity to produce research that affects the rest of the world. And maybe we can start building tools that help us know where to focus our energies and resources in order to do exactly that.

* * *

* It should be noted that the current model of scientific publishing puts up a barrier to the &#8220;Anyone who wants to know&#8221; part, as access is currently limited to institutional subscribers or those who are willing to pony up $30+ per article&#8230; which isn&#8217;t &#8220;anyone&#8221;. The key barrier here for scientific publishing is enabling &#8220;anyone who wants to know&#8221; to have access to scientific publications.

* * *

*&#8220;\_MG\_9934&#8243; CC-BY [RoyZilla92][1]*

 [1]: http://www.flickr.com/photos/rspg92/3922790133/
 [2]: http://www.niemanlab.org/2012/07/who-should-see-what-when-three-principles-for-personalized-news/
 [3]: http://www.quora.com/Why-Did-X-Fail/Why-have-personalized-news-startups-failed
 [4]: http://jonathanstray.com/
 [5]: http://blog.ketyov.com/2012/04/how-do-you-follow-scientific-literature.html
 [6]: http://arxiv.org/
 [7]: http://scientopia.org/blogs/drugmonkey/2010/09/28/on-keeping-abreast-of-the-literature-a-highly-loaded-poll-question/
 [8]: http://scientopia.org/blogs/drugmonkey/2010/09/28/on-keeping-abreast-of-the-literature-a-highly-loaded-poll-question/#comment-20650
 [9]: http://pubcrawler.gen.tcd.ie/
 [10]: http://en.wikipedia.org/wiki/There_are_known_knowns
 [11]: http://phylogenomics.blogspot.com/2012/08/wow-google-scholar-updates-big-step.html
 [12]: https://mystudiouslife.wordpress.com/2012/01/10/mendeley-v1-3-mendeley-suggest/
 [13]: http://sciple.org/scientific-rss-feeds-how-to-rank-them/
 [14]: https://github.com/neuromusic/sciple-rss
 [15]: http://en.wikipedia.org/wiki/John_Archibald_Wheeler
 [16]: ttp://www.amazon.com/gp/product/0691148902/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=0691148902&linkCode=as2&tag=pulsatance-20
 [17]: http://johnhawks.net/weblog/reviews/neandertals/neandertal_dna/neandertal-ancestry-iced-2012.html
 [18]: http://careers.stackoverflow.com/jobs/19463/stack-exchange-data-scientist-stack-exchange
 [19]: http://www.labguru.com/
 [20]: http://www.quartzy.com/
 [21]: http://www.mendeley.com/profiles/justin-kiggins/contacts/
 [22]: http://www.researchgate.net/
 [23]: http://f1000.com/
 [24]: http://hypothes.is/