---
title: ReproHacking at Opencon London 2017 Doathon
author: Anna
date: '2017-12-21'
slug: reprohacking-at-opencon-london-2017-doathon
categories:
  - Post
tags:
  - event
  - opencon
  - reprohack
subtitle: ''
summary: ''
authors: []
lastmod: '2017-12-21T19:32:28+01:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []

---

Building on the success of last year’s [**#Reprohack2016**](https://annakrystalli.shinyapps.io/OpenConBerlin_reprohack/) for the Berlin OpenCon satellite event, I rejoined the team of organisers ([Laura Wheeler](https://twitter.com/laurawheelers), [Jon Tennant](https://twitter.com/Protohedgehog) and [Tony Ross-Hellauer](https://twitter.com/tonyR_H) ) and teamed up with [Peter Kraker](https://twitter.com/PeterKraker?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor) to develop the hackday for this year’s [**OpenCon London 2017**](https://www.eventbrite.co.uk/e/opencon-london-2017-open-for-what-tickets-38036414941#).  

To allow better reflection on this year's theme, “Open for what?”, we expanded the format to two tracks, opening up the scope for both projects and participants. **One track retained the ReproHack format from last year, the other, a broader track, offered the opportunity for leads of any type of open science project to [submit them for work](https://annakrystalli.shinyapps.io/OpenConLondon_Doathon/)**. Projects were not constrained to coding and you didn't have to code to take part in the session - anyone with an interest in creative contribution to open science in whichever capacity was welcome. 

On the day, after a round of introductions and sharing our motivations for attending, we reviewed the submissions and knuckled down.

<br>

### ReproHacking

The original ReproHack was inspired by **Owen Petchey’s [Reproducible Research in Ecology, Evolution, Behaviour, and Environmental Studies course](https://github.com/opetchey/RREEBES)**, where students attempt to reproduce the analysis and figures of a paper from the raw data, so we wanted to attempt the same. They take a few months over a number of sessions though, so, given our time constraints, we focused on reproducing papers that have also published the code behind them. This year we had a whole day, which gave us more time to dig deeper into the materials, moving beyond evaluating them for reproducibility, to how understandable, even how reusable they were. While fewer, we still had some [excellent submissions](https://annakrystalli.shinyapps.io/OpenConLondon_Doathon/) to choose from.

**I'm pleased to report that two of the three papers attempted were succesfully reproduced!**  

<br>

# ***

I was particulalrly impressed with the paper [**Andrew Ajube**](https://www.linkedin.com/in/andrewajube/) tackled: 

> [The State of OA: A large-scale analysis of the prevalence and impact of Open Access articles](https://peerj.com/preprints/3119/)
*Piwowar et. al*

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Successfully reproduced our results earlier thanks to <a href="https://twitter.com/annakrystalli?ref_src=twsrc%5Etfw">@annakrystalli</a> and Andrew, and just now mentioned in <a href="https://twitter.com/catmacOA?ref_src=twsrc%5Etfw">@catmacOA</a>&#39;s talk. <a href="https://t.co/qkaOTySt7W">https://t.co/qkaOTySt7W</a> <a href="https://twitter.com/hashtag/OpenCon?src=hash&amp;ref_src=twsrc%5Etfw">#OpenCon</a> <a href="https://t.co/ymVoydy93p">pic.twitter.com/ymVoydy93p</a></p>&mdash; Lisa Matthias (@l_matthia) <a href="https://twitter.com/l_matthia/status/933070982025240576?ref_src=twsrc%5Etfw">November 21, 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>



Under very minimal supervision and never having used R or Rstudio before, he managed to reproduce **an analysis in an rmarkdown [vignette](http://r-pkgs.had.co.nz/vignettes.html)**]. I think this speaks volumes, to the power of the tools and approaches we have freely available to us, of following best practice (well described in this epic Jenny Bryan [blog post](https://www.tidyverse.org/articles/2017/12/workflow-vs-script/) on **project-oriented workflows**), the effort the producers went to, and of course, genuine engagement by Andrew. It can work and it is rewarding!

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Let it be known that Andrew Ajube, the participant that reproduced it had never used <a href="https://twitter.com/hashtag/rstats?src=hash&amp;ref_src=twsrc%5Etfw">#rstats</a>, <a href="https://twitter.com/rstudio?ref_src=twsrc%5Etfw">@rstudio</a> or rmd before but still managed to reproduce it w/ only minimal guidance from me. <br><br>Kudos to you the producers! <a href="https://twitter.com/hashtag/OpenConLondon?src=hash&amp;ref_src=twsrc%5Etfw">#OpenConLondon</a> <a href="https://twitter.com/hashtag/ReproHack17?src=hash&amp;ref_src=twsrc%5Etfw">#ReproHack17</a> <a href="https://t.co/4WE2cXOetn">https://t.co/4WE2cXOetn</a></p>&mdash; annakrystalli (@annakrystalli) <a href="https://twitter.com/annakrystalli/status/933075390154887169?ref_src=twsrc%5Etfw">November 21, 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


<br>

# ***

I worked with [Marios Andreou](https://twitter.com/mariosge90?lang=en) on a very well curated paper, submitted by [Ben Marwick](https://twitter.com/benmarwick?lang=en). 

> [The archaeology, chronology and stratigraphy of Madjedbebe (Malakunanja II): a site in northern Australia with early occupation](http://www.sciencedirect.com/science/article/pii/S0047248415000846?via%3Dihub)
*Clarkson et. al*

The paper offered two options to reproduce the work. A completely self-contained archive version in a docker container, which Marios spun up and reproduced the analysis in, in no time. I opted for the second option, [installing the analysis as a package](https://rmflight.github.io/posts/2014/07/analyses_as_packages.html). It did require a bit of manual dependency managing but, this was documenteted in the [**analysis repository README**](https://github.com/benmarwick/1989-excavation-report-Madjedbebe) on github. This meant that all functionality developed for the analysis was available for me to explore. Presenting the [analysis in a vignette](https://github.com/benmarwick/1989-excavation-report-Madjedbebe/blob/master/vignettes/analysis-of-dates-lithics-shell-from-1989-excavations.Rmd) also made it’s inner working much more penetrable and allowed us to [interactively edit it to get a better feel of the data](https://opencon-london.github.io/OpenCon_London-Doathon/marwick_archaelogy_repro/analysis-of-dates-lithics-shell-from-1989-excavations.nb.html) and how the analysis functions worked. Ultimately, not only could we reproduce the science in the paper (open for transparency), we could also satisfy ourselves with what the code was doing (open for robustness) and reuse the code (open for resuse). The only step further would be to make the functionality more generalisable.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Woah! Successful double reproduction at <a href="https://twitter.com/hashtag/OpenCon?src=hash&amp;ref_src=twsrc%5Etfw">#OpenCon</a> - <a href="https://twitter.com/Scrumblebee?ref_src=twsrc%5Etfw">@Scrumblebee</a> <a href="https://twitter.com/annakrystalli?ref_src=twsrc%5Etfw">@annakrystalli</a> <a href="https://twitter.com/mariosge90?ref_src=twsrc%5Etfw">@mariosge90</a> congrats!! <a href="https://twitter.com/hashtag/openbiscuits?src=hash&amp;ref_src=twsrc%5Etfw">#openbiscuits</a> <a href="https://t.co/9Wp4AsFevz">pic.twitter.com/9Wp4AsFevz</a></p>&mdash; Jon Tennant (@Protohedgehog) <a href="https://twitter.com/Protohedgehog/status/932969845242695685?ref_src=twsrc%5Etfw">November 21, 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


At the end of the session we collected some feedback about the experience, reflecting on reproducibility, the tools and approaches used, documentation and reusability. Here's the [feedback we had for Ben's work](https://github.com/annakrystalli/write-ups/blob/master/assets/OpenCon_ReproHack%20feedback_form.pdf).


As calls for openness are maturing, it's good to push beyond why open? to indeed, open how? open when? open for what? Different approaches to **how** a study is made "reproducible" has implications on **what** the openness can achieve downstream. It's probably a good time to start clarifying the remit of different approaches. 

<br>

### Do-athoning

On the do-athon side there were a couple of cool projects. Peter and [Ali Smith](https://twitter.com/40_thieves?ref_src=twsrc%5Etfw&ref_url=http%3A%2F%2F127.0.0.1%3A46498%2Frmd_output%2F1%2F) worked on **Visual data discovery in Open Knowledge Maps**,  adapting their knowledge mapping framework, Head Start, to the specific requirements of data discovery.


<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">We&#39;re trying an agile approach to <a href="https://twitter.com/hashtag/OpenConLondon?src=hash&amp;ref_src=twsrc%5Etfw">#OpenConLondon</a> hack! First feedback session.<a href="https://twitter.com/40_thieves?ref_src=twsrc%5Etfw">@40_thieves</a> talking us through work on their <a href="https://twitter.com/hashtag/openscience?src=hash&amp;ref_src=twsrc%5Etfw">#openscience</a> project, adapting <a href="https://twitter.com/OK_Maps?ref_src=twsrc%5Etfw">@OK_Maps</a> approach to dataset search! <a href="https://t.co/TPk12yejzF">pic.twitter.com/TPk12yejzF</a></p>&mdash; annakrystalli (@annakrystalli) <a href="https://twitter.com/annakrystalli/status/932945063365300224?ref_src=twsrc%5Etfw">November 21, 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


Tony, [Lisa Mattias](https://twitter.com/l_matthia) and Jon continued work on the, open to anyone, hyper-collaborative drafting of the [**"Foundations for Open Science Strategy Development"**](https://docs.google.com/document/d/1un3N3JsvfodSxW3FMAoOMHaESPMzJSBr7kcrxWjoEnE/edit#) document, started at the [OpenCon 2017 Do-athon](https://github.com/sparcopen/doathon/issues/24).

<br>

### Agile hacking

One thing I love about hacks is that you never know quite what skills you’re gonna get in the room. In our case, we got scrumaster [Sven Ihnken](https://www.linkedin.com/in/sven-ihnken-4153b525/) offering to help us navigate the day. We’ve actually been agile working for the passed few months with the nascent shef dataviz team and I find it a productive way to work. So an agile hack seemed a worthy experiment. I personally thought it worked really well. It was nice to split up the day into shorter sprints and review progress around the room half way. And Sven did do a great job “buzzing” around the room, keeping us focused and engaged and ultimately, getting all our tasks from doing to done!

# ***

<br>

At the end of the day, we shared what we'd worked on, and settled in for the main Opencon London evening event. As the event talks went through more traditional remits of OpenCon, from public engagement to open access to literature and data, it just reiterated to me that each strand of openness is yet another way to invite people in to science. For me, inviting people all the way in, into your code and data, your entire workflow, is the bravest and most rewarding of all!