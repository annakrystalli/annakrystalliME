---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "rrtools: Tools for Writing Reproducible Research in R"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2018-04-06T17:30:17+00:00
lastmod: 2020-04-13T15:43:17+01:00
featured: false
draft: false
event: Sheffield R Users Group meetup
event_url: https://www.meetup.com/SheffieldR-Sheffield-R-Users-Group/events/249186869/
location: The Red Deer, Sheffield UK
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/annakrystalli
url_code: ""
url_pdf: ""
url_slides: "http://annakrystalli.me/talks/rrtools.html"
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

[`Rrtools`](https://github.com/benmarwick/rrtools) builds on functionality offered by packages like `devtools` and `usethis` adapting and extending them to a research context. The package provides guidance, templates, and functions for making a basic compendium suitable for doing reproducible research with R and a convenient starting point for writing a journal article, report, or thesis.

Useful features:

- A template for doing scholarly writing in a literate programming environment using R Markdown (http://rmarkdown.rstudio.com/) and bookdown (https://bookdown.org/home/about.html).

- Isolation of your computational environment in a container using Docker (https://www.docker.com/what-docker)

- Package dependency versioning using MRAN (https://mran.microsoft.com/documents/rro/reproducibility/),

- Continuous Integration (testing) using Travis (https://docs.travis-ci.com/user/for-beginners).

In this joint session, I gave an overview of the philosophy, key functions and resulting compendium structure while Dan Olner walked us through using the tools to convert an existing research project to a reproducible research compendium.