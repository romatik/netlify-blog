---
title: 'rstudio::conf 2020 Review: Part 3'
author: Misha Balyasin
date: '2020-03-01'
slug: rstudio-conf-2020-review-part-3
categories:
  - meta
tags:
  - rstudioconf
  - overview
  - conference
subtitle: ''
---

All talks can be found here: https://resources.rstudio.com/rstudio-conf-2020. I've picked 30 talks in total, so will split them into 3 parts with 10 talks each.

Part 1 is [here](https://www.mishabalyasin.com/2020/02/16/rstudio-conf-2020-review-part-1/)

Part 2 is [here](https://www.mishabalyasin.com/2020/02/22/rstudio-conf-2020-review-part-2/)

1. [Interactivity and programming in the `tidyverse` by Lionel Henry](https://resources.rstudio.com/rstudio-conf-2020/interactivity-and-programming-in-the-tidyverse-lionel-henry)

Talk by Lionel about the tension that exists between interactive and programmatic uses of functions with `tidyeval`. One major point in his talk and other talks from `tidyverse` team is movement of `rlang` to lower and lower levels, meaning that if you are using `!!` and `rlang::quo`, then you need to learn quite a bit to use them correctly. However, if you are "regular" useR, then you might be able to get by with `{{` and `.data`/`.env` instead. This reflects the gradual nature of replacing user-facing features of `tidyeval` with higher and higher abstractions that should make lives of R programmers easier.

2. [Azure Pipelines and GitHub Actions by Jim Hester](https://resources.rstudio.com/rstudio-conf-2020/azure-pipelines-and-github-actions-jim-hester)

With recent MS acquisition of GitHub, they are continuing the "embrace" stage of their strategy. What GitHub Actions allows you to do is to run your builds on multiple platforms at the same time (macOS, Windows and multiple flavors of Linux). Both Circle CI and Travis CI didn't allow for this flexibility, so you'd include Appveyor to just run your stuff on Windows. With GH Actions you eliminate all of this overhead AND you get multiple concurrent jobs for free (for academic, open source work at least). Sounds too good to be true, right? Well, let's see in couple of years if it is still as good as it is now. 

But regardless of what will happen down the line, `usethis` already ships with all the machinery you need to setup your package on GH, so you could start using GH actions with just few commands.

3. [Asynchronous programming in R by Winston Chang](https://resources.rstudio.com/rstudio-conf-2020/asynchronous-programming-in-r-winston-chang)

The talk is not so much about asynchronous programming as it is about `later` package that, e.g., `shiny` uses to do all the reactive stuff we all love about it. So if you are doing something like this (or parallelism, threading, etc.) - definitely take a look at `later` and this talk.

4. [`vctrs`: Creating custom vector classes with the `vctrs` package by Jesse Sadler](https://resources.rstudio.com/rstudio-conf-2020/vctrs-creating-custom-vector-classes-with-the-vctrs-package-jesse-sadler)

Entertaining talk about how to create your own S3 class using `vctrs` package. `vctrs` provides you with robust framework and a path to follow if you want to have S3 class that has lots of useful properties: coercing, comparison, conversion etc. There are also couple of GH repos where this process is delineated even more clearly, so if you are thinking about creating your own S3 class, give `vctrs` and this talk a go.

5. [`future`: simple async, parallel and distributed processing in R by Henrik Bengtsson](https://resources.rstudio.com/rstudio-conf-2020/future-simple-async-parallel-amp-distributed-processing-in-r-whats-next-henrik-bengtsson)

If you are thinking about doing async, parallel or distributed processing in R, then you should use `future`. In my experience, there is no other package that does as much and as feature-rich. In this talk Henrik mentioned that warnings and messages will now pass through futures and (the moment everyone waited for) you now have ability to have progress bars! And you could do use `beepr` to add sound! Awesome stuff, as usual.

6. [Getting things logged by Gergely Daroczi](https://resources.rstudio.com/rstudio-conf-2020/getting-things-logged-gergely-daroczi)

Fast overview of `logger` package that actually convinced me to take a much closer look at it. Last time I checked it out, it was pretty bare-bones, but Gergely added bunch of very useful functionality (e.g., tracking all input variables in Shiny app), so could be a good fit for some of the projects.

7. [Lightning talk "Lessons about R I learned from my cat" by Amanda Gadrow](https://resources.rstudio.com/rstudio-conf-2020/lightning-talk-amanda-gadrow)

Main point of the talk: be lazy. Well, not exactly like that, but that's an important thing to keep in mind when working on a project. Make life of future you as worry-free as possible by structuring your code, improving readability and being more consistent overall.

8. [Lightning talk "`livecode`: broadcast your live coding" by Colin Rundel](https://resources.rstudio.com/rstudio-conf-2020/lightning-talk-colin-rundel)

Nifty package that allows you to share your R session with multiple users interactively. It's just a beginning for this package, but it already can do quite a few things.

9. [Lightning talk "Datasets in Reproducible Research with `pins`" by Javier Luraschi](https://resources.rstudio.com/rstudio-conf-2020/lightning-talk-javier-luraschi)

`pins` package allows to offload handling of remote resources to that package. What that means is that you can "pin" remote dataset and `pins` will figure out if you already downloaded this package and use local version instead. This concept works other way around since you can share your dataset with others and package will take care of uploading it to the board.

10. [Lightning talk "Rproject templates to automate and standardize your workflow" by Caroline Ledbetter](https://resources.rstudio.com/rstudio-conf-2020/lightning-talk-caroline-ledbetter)

Another relatively obscure, but potentially incredibly useful feature of RStudio - you can create a template for new projects and share it in your organization. If there is information that absolutely every project should have then with this you can make sure that people won't forget a) what they need to add and b) actually do it. 
