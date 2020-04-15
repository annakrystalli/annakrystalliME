---
title: ReproHacking at CCMcr19
author: Anna
date: '2019-08-07'
slug: reprohacking-at-ccmcr19
categories:
  - Post
tags:
  - reprohack
  - event
  - CarpentryConnect
subtitle: ''
summary: ''
authors: []
lastmod: '2019-08-07T18:41:55+01:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

***This post was first published on the [Software Sustainability Institute blog](https://www.software.ac.uk/blog/2019-08-07-reprohacking-carpentryconnect-manchester-2019)***

It was great to be at [CarpentryConnect Manchester 2019](https://software.ac.uk/ccmcr19) a few weeks ago. Not only did I join a fantastic group of people who are a joy to spend time with, extremely knowledgeable and generous with that knowledge, but, with such a focus on active learning, it was also the perfect event for running the first **ReproHack** in the series and gathering feedback to guide future development. 

## What's a ReproHack?


<img src="/2019-07-01-reprohacking-at-ccmcr19/index_files/reprohack-landscape-lowres.png" alt="" width="50%"/>



Reprohacks are **one day reproducibility hackathons where participants reproduce papers  from published code and data**. While I've been part of [running two of these](https://rse.shef.ac.uk/blog/opencon-london/) since 2016 as part of [OpenCon](https://www.opencon2018.org/) satellite events,  returning to ReproHacking and taking it to the next level is the focus of my [2019 Software Sustainability Institute Fellowship](https://rse.shef.ac.uk/blog/ssi-fellowships-2019/).


## The run-up

In their current format, ReproHacks begin with a call for authors to propose their papers for reproduction. With a little help from friends and supporters of the initiative we managed to get [**18 papers proposed**](https://sheffield-university.shinyapps.io/ReproHack_CCMcr/), which is good going! One observation I'd make about the papers proposed is that, although papers were from across domains, the majority of them were coded in R. Not sure what to make of this and don't want to read too much into it. It is no secret that I live in a giant #rstats bubble. I did try to engage other research communities as much as I could but I may well just not have been successful. I do wonder however whether work across the R research community to formalise how code, data and papers is brought together in [a research compendium](https://peerj.com/preprints/3192/) and [build tools to support this](https://github.com/benmarwick/rrtools) are paying off.

I was also really excited about interest in the ReproHack in general. In particular, I was contacted by Nicolas Rougier of [ReScience C](http://rescience.github.io/), an online journal publishing open source replications of already-published research. While replications are a step above reproductions, requiring variation in technical details (for example, using different software, running a simulation from different initial conditions, etc.), they are nontheless the most useful if reproducibility has already been verified. With that in mind, a proposal worth exploring was made to create a new “reproducibility report” category. 

I also heard from Cassio Amorim, the creator of [scigen.report](https://scigen.report/), a web portal through which reproducers can log the status of their efforts against a paper's DOI! Both initiatives provide really exciting avenues for producing useful outputs during ReproHacks, creating incentives for participants and a way for findings to be logged for the benefit of the research community. We are [working on integrating them into the ReproHack workflow](https://github.com/reprohack/reprohack-hq/issues/6) and welcome feedback and ideas!


The most exciting development for me, however, was that [Florencia D'Andrea](https://rladies.org/argentina-rladies/name/maria-dandrea/), a postdoc at the National Agricultural Technology Institute of Argentina joined the team! She has already helped loads by reviewing and preparing materials, contributing ideas and most importantly just being there to bounce ideas off and plan future directions.

## On the day

First and foremost, we had a brilliant time on the day! We got a total of 11 participants passing through which I was really happy with, given the diversity and quality of the multiple sessions running in parallel.


### Hacking the ReproHack

Part of this first session was to crowdsource ideas and decide on strategy and next generation infrastructure for making ReproHacks reproducible. I was really pleased to have [Radovan Bast](https://bast.fr/) of the University of Tromsø/[Code Refinery](https://coderefinery.org/) helping with this. We've been [sketching out plans](https://github.com/reprohack/reprohack-hq/issues/10) and hope to collocate for a sprint on materials in the autumn. 

### Reprohacking

Finally, the main activity of the day was of course reproducing papers! I'm pleased to report that the majority of papers attempted were reproduced, and the stumbling blocks we did come across were instructive in their own way.

#### Automation is great, but storytelling is even better!

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Huge thanks to <a href="https://twitter.com/EnviroKaty?ref_src=twsrc%5Etfw">@EnviroKaty</a> for submitting a fab 🦋 🦋🦋 paper to the <a href="https://twitter.com/hashtag/CCMcr19?src=hash&amp;ref_src=twsrc%5Etfw">#CCMcr19</a> <a href="https://twitter.com/hashtag/ReproHack?src=hash&amp;ref_src=twsrc%5Etfw">#ReproHack</a>! I had loads of fun reproducing the analysis for this really cool paper <a href="https://t.co/v1ww2D5xhg">https://t.co/v1ww2D5xhg</a> <a href="https://t.co/r8rYMAMvPm">pic.twitter.com/r8rYMAMvPm</a></p>&mdash; Jessica Ward (@JKRWard) <a href="https://twitter.com/JKRWard/status/1144254546841165827?ref_src=twsrc%5Etfw">June 27, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

One general observation is that participants mostly enjoyed working with papers that brought them closer to the analysis, most notably through the use of [literate programming](https://en.wikipedia.org/wiki/Literate_programming). The more they felt walked through the materials, the more they felt they understood the analysis, what the code was doing and got ideas on how to reuse. 

> Awesome work, I had a lot of fun reproducing the analysis and investigating the paper. I'm now looking forward to playing around with the code for wrangling inaturalist data!!
> --- Jessica Ward on _["Comparisons of Citizen Science Data-Gathering Approaches to Evaluate Urban Butterfly Diversity"](https://www.mdpi.com/2075-4450/9/4/186)_ submitted by Kathleen Prudic

> It was great working with someone else's markdown script - the .Rmd file itself was written in a really clear and transparent manner with lots of helpful comments and signposting as to what each chunk of analysis did.  
> --- Andrew Stewart on _["Comparing theory-driven and data-driven attractiveness models using images of real women’s faces"](https://psyarxiv.com/vhc5k)_ submitted by Ben Jones

In this respect, another paper attempted with a fully automated workflow that went from a single command to a fresh copy of the pdf of the paper, while easily the most robust setup in terms of reproducibility, provided little opportunity for participants to be introduced to the code and analysis. So it's important to consider not only if something is reproducible but what the aim of the reproducibility is? Validation that the code produces the same results? An opportunity to examine and understand the code itself? The ability to reuse it?

#### A need for appropriate infrastructure

The day also highlighted the requirement of appropriate archiving of materials. Attempts to access  the code and data published alongside nature communications article [_"Sea level regulated tetrapod diversity dynamics through the Jurassic/Cretaceous interval"_](https://www.nature.com/articles/ncomms12737) on their platform lead initially to a 404 error. 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">In the intro talk to the <a href="https://twitter.com/hashtag/ReproHack?src=hash&amp;ref_src=twsrc%5Etfw">#ReproHack</a> we stress that reproducibility is hard.<br><br>We weren&#39;t quite expecting this! <a href="https://t.co/48CtrYP45g">https://t.co/48CtrYP45g</a></p>&mdash; annakrystalli (@annakrystalli) <a href="https://twitter.com/annakrystalli/status/1144176149859377152?ref_src=twsrc%5Etfw">June 27, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Following that, the error changed to "Service Unavailable" and after a couple of hours or so it was fixed, but without a single word of engagement from the publishers themselves about it. 

While I don't want to make too big a deal of this, mistakes do happen, it does make me wonder whether traditional publishers are actually taking this seriously, especially given the 6,000 EUR price tag attached to publication of this particular paper. **Reproducibility IS hard** and it bothers me to think that while authors go through the painstaking effort of making their work reproducible, publishers aren't also upping their game. Ultimately it shows that engaging with the materials is necessary if reproducibility is not to become just a tick-boxing exercise that nobody checks.

It also feeds into an important point regarding standardisation of access to such materials raised by a participant in the [event collaborative notepad](https://hackmd.io/baMxPe7wQPmEmZDNMkDEJg) which I share here as an open ended question:

> I am wondering if there is any automated way to pull the data and code from supplementary or additional files. Should the scientific community start to recommend some regulations and formats to smooth the way of how/where these kinds of data are made available and beneficial?
> --- Manal Albahlal, University of Manchester 


#### tl;dr

Overall, I feel that efforts like the ReproHack, which aim to engage people with the published raw materials behind the science are an important vehicle for showing the value of the practice, evaluating the current state of approaches and using that to inform best practice going forward, not only for reproducibility but also for reuse, transparency and ultimately for spreading knowledge, understanding and capacity more broadly. 

P.S. If you are interested in running a ReproHack or helping out, please check out our [reprohack-hq](https://github.com/reprohack/reprohack-hq) repository or say hello in our [gitter](https://gitter.im/reprohack/community) channel.

