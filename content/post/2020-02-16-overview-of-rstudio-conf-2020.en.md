---
title: 'rstudio::conf 2020 Review: Part 1'
author: Misha Balyasin
date: '2020-02-16'
tags:
  - rstudioconf
  - overview
  - conference
categories:
  - meta
slug: rstudio-conf-2020-review-part-1
---

All talks can be found here: https://resources.rstudio.com/rstudio-conf-2020. I've picked 30 talks in total, so will split them into 3 parts with 10 talks each.

Part 2 is [here]()

Part 3 is [here]()

1. [Object of type closure in not subsettable by Jenny Bryan](https://resources.rstudio.com/rstudio-conf-2020/object-of-type-closure-is-not-subsettable-jenny-bryan)

This talk by Jenny Bryan is another gentle introduction of R community to more software-oriented practices. Specifically, how do you fix an error? It might seem like an innocuous question, but it has a lot of complexity to it. The steps you need to take are rather simple, though:

- Restart.
- Create reprex (don't forget about "minimal" part of reprex!).
- Debug.
- Add test for future self to not introduce the same error again.

I'm particularly fond of the second step with reprex since I'm spending some time on RStudio Community and it's constant struggle for people who are willing to spend their time to help out, but they can't without something as simple as reprex. If you find yourself in such a situation, take a gander at [reprex's website](https://reprex.tidyverse.org/).

2. [Styling Shiny apps with SASS and bootstrap 4 by Joe Cheng](https://resources.rstudio.com/rstudio-conf-2020/styling-shiny-apps-with-sass-and-bootstrap-4-joe-cheng)

In my very limited experience of building Shiny apps I've already came across the situation where it's a major pain in the back to change colors. Every single time you need to fiddle with them, I would think that it's great that I'm a data scientist and not a front-end developer. But it turns out front-end developers already solved this problem with, e.g., SASS compilers that allow changing colors in Bootstrap with setting variables and running compiler on it. This means that changing just one variable changes everything about how your app looks like in a consistent manner.

There is also a cool way to run shiny app with self-updating backend where you can change variables and see what it does for your app. All in all - very useful (if surprisingly belated) addition to already impressive range of tools that Shiny provides.

3. [Total tidy tuning techniques by Max Kuhn](https://resources.rstudio.com/rstudio-conf-2020/total-tidy-tuning-techniques-max-kuhn)

This talk is about `tune` package that is yet another building block in `tidymodels` family of packages (my presentation about state of that in March, 2019 - [here](https://www.mishabalyasin.com/2019/03/03/touring-the-tidyverse-tidymodels/)). I'm really enjoying seeing all of the (relatively) small improvements that come out of `tidymodels` team and with each new addition the workflow that they propose look more and more solid. I especially liked the `.notes` column that collects all the warnings/errors/etc from the fitting of the model as it shows that authors spend a lot of time around the topic (I mean, with Max Kuhn it goes without saying, but still).

4. [State of the tidyverse by Hadley Wickham](https://resources.rstudio.com/rstudio-conf-2020/state-of-the-tidyverse-hadley-wickham)

State of the union address from Hadley about how things are going and where. One interesting thing for me personally is post-mortem of tidy evaluation that, apparently, wasn't introduced in a way conducive to learning. In order to understand how it works you'd need to learn bunch of theory (you can take a look here where I made a presentation about it - [tidy eval](https://www.mishabalyasin.com/2018/11/30/touring-the-tidyverse-tidyeval/)). The tension comes from the fact that in your "normal" life you rarely need all of it, so forcing it on people was a mistake. Similarly, `purrr` will become less visible since it requires learning a bit more than you need day-to-day. Personally, those two things are probably my favorite places of `tidyverse`, but I can see the point that Hadley made. Also, they are not going away, just becoming a bit less in your face for newcomers.

5. [Practical plumber patterns by James Blair](https://resources.rstudio.com/rstudio-conf-2020/practical-plumber-patterns-james-blair)

`plumber` is a nifty little package that is deeply integrated into RStudio Connect. But even without it, it allows data scientists to quickly create REST API endpoint to expose whatever you are doing to a wider world. James went over couple of scenarios of such interaction together with how it could be solved using `plumber` functionality. I've used this package in the past and even then it worked fairly well, but with newer and newer features it becomes even more user-friendly.

6. [3D ggplots with rayshader by Dr. Tyler Morgan-Wall](https://resources.rstudio.com/rstudio-conf-2020/3d-ggplots-with-rayshader-dr-tyler-morgan-wall)

Entertaining presentation by creator of `rayshader` package where he showed a lot of crazy stuff that you can do entirely in R. Some (most) of the examples are really cool. Obviously, it works best for maps, but in one demo Tyler showed how you can visualize Earth and Moon orbiting around each other. It probably took multiple hours to render, but result is stunning.

7. [We're hitting R a million times a day so we made a talk about it by Heather Nolis and Dr. Jacqueline Nolis](https://resources.rstudio.com/rstudio-conf-2020/we-re-hitting-r-a-million-times-a-day-so-we-made-a-talk-about-it-heather-nolis-dr-jacqueline-nolis)

Data engineer and data scientist from T-Mobile shared their experiences about how to put R into production. There are a lot of interesting tidbits, but one that I've enjoyed hearing about the most is the fact that they lean heavily on Shiny to actually showcase their work to stakeholders. This is something that, for example, is not as common at my current workplace, but I can definitely see how beneficial it is whenever I do manage to sneak a little bit of Shiny into the mix.

8. [Deploying end-to-end Data Science with Shiny, Plumber and Pins by Alex Gold](https://resources.rstudio.com/rstudio-conf-2020/deploying-end-to-end-data-science-with-shiny-plumber-and-pins-alex-gold)

Despite the name of the talk, brunt of the presentation was about new package from RStudio called `pins`. Basically, `pins` is a way to share R objects between multiple people. That's basically it. For data sharing it's probably better to use DB's, but if you want to share, e.g., recipe from `recipes` package, then `pins` can be handy.

9. [renv: Project Environments to R by Kevin Ushey](https://resources.rstudio.com/rstudio-conf-2020/renv-project-enviromemnts-for-r-kevin-ushey)

`renv` is a spiritual successor to `packrat`. Just like tidy evaluation above, `packrat` was a bit ahead of its time since it did provide a way to handle dependencies in R projects, but it did so in a rather convoluted way. `renv` is a new version that supposed to fix most mistakes `packrat` did. From multiple unrelated people I've already heard that `renv` is indeed MUCH easier to use and overall delivers on this promise. So, good job Kevin :).

10. [Accelerating Analytics with Apache Arrow by Neal Richardson](https://resources.rstudio.com/rstudio-conf-2020/accelerating-analytics-with-apache-arrow-neal-richardson)

`arrow` is another cool project that tries to create "modern data frame". It does so with bindings in multiple languages and often times it's really efficient. In the latest (0.16.1 as of this writing) it no longer requires system dependencies on Linux and I just tried and it installed without any issue. Like `tidymodels`, `arrow` is far from done, but it is cool to see steady incremental progress that comes out of Ursa Labs.
