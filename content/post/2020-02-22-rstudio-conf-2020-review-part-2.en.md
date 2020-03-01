---
title: 'rstudio::conf 2020 Review: Part 2'
author: Misha Balyasin
date: '2020-02-22'
tags:
  - rstudioconf
  - overview
  - conference
categories:
  - meta
slug: rstudio-conf-2020-review-part-2
---

All talks can be found here: https://resources.rstudio.com/rstudio-conf-2020. I've picked 30 talks in total, so will split them into 3 parts with 10 talks each.

Part 1 is [here](https://www.mishabalyasin.com/2020/02/16/rstudio-conf-2020-review-part-1/)

Part 3 is [here](https://www.mishabalyasin.com/2020/03/01/rstudio-conf-2020-review-part-3/)

1. [What's new in TensorFlow for R by Daniel Falbel](https://resources.rstudio.com/rstudio-conf-2020/whats-new-in-tensorflow-for-r-daniel-falbel)

Short and to the point overview of current lay of the land when it comes to TensorFlow bindings in R. There is a number of packages that are covering various areas of TF ecosystem with even more packages planned for release in a near future. One interesting question about adding support for PyTorch in the future and it seems like it's not a priority at the moment and unlikely to come from RStudio.

2. [Putting fun in functional data by Dani Chu](https://resources.rstudio.com/rstudio-conf-2020/putting-the-fun-in-functional-data-a-tidy-pipeline-to-identify-routes-in-nfl-tracking-data-dani-chu)

Entertaining talk about how you can use tracking data for clustering of NFL plays. The most interesting part for me was more about the fact that actual tools that they've used come almost directly from R4DS book, so it kinda validates the approach that RStudio at large has been doing - breed adoption of R tools through concerted effort of producing high-quality education materials. `gganimate` also had a cameo showing how powerful animation can be.

3. [Updates on Spark, MlFlow by Javier Luraschi](https://resources.rstudio.com/rstudio-conf-2020/updates-on-spark-mlflow-and-the-broader-ml-ecosystem-javier-luraschi)

Another whirlwind of an update about Spark and MlFlow from one of the main contributor/developer of the package. It's always good to see that pace of the project is actually speeding up with new extensions and bigger and bigger scope. 

4. [Using Jupyter with RStudio Server Pro by Karl Feinauer](https://resources.rstudio.com/rstudio-conf-2020/using-jupyter-with-rstudio-server-pro-karl-feinauer)

If you ever wanted to launch Jupyter Notebook in RStudio Server Pro - now you can! Personally, I dislike Jupyter Notebooks quite a lot, but obviously not everyone holds the same position, so it makes sense to have it available. It's also interesting to see an integration with RStudio Connect where you can easily publish your Jupyter Notebooks and share it with wider organization.

5. [How RMarkdown changed my life by Rob Hyndman](https://resources.rstudio.com/rstudio-conf-2020/how-rmarkdown-changed-my-life-rob-hyndman)

An ode to RMarkdown. As I'm writing this in markdown that eventually will be published to a website running `blogdown`, I'd say I'm in the same boat, but if you ever need convincing that RMarkdown is the way - watch this talk.

6. [List columns in data.table by Tyson S. Barrett](https://resources.rstudio.com/rstudio-conf-2020/list-columns-in-data-table-tyson-s-barrett)

If you want to use `dplyr` with `data.table` then there is `dtplyr`. But what if you want to use `tidyr` with `data.table`? Then there is a `tidyfast` package that implements `nest`ing and `unnest`ing using `data.table` as a backend. As is often the case, using `data.table` allows you to improve both speed and memory consumption, so if you are finding yourself struggling on either of these fronts, then `data.table` can be a way to go.

7. [Technical debt is a social problem by Gordon Shotwell](https://resources.rstudio.com/rstudio-conf-2020/technical-debt-is-a-social-problem-gordon-shotwell-2)

Deeply thought out talk about how to repay technical debt in a most sustainable way possible. Whole talk is definitely worth watching, but the main idea is that as a person writing code you should take responsibility to create delightful code. How to define what "delightful" means is not easy, but Gordon gives bunch of helpful tips to do so. It is also another talk that is not talking about R in any way since lessons learned apply to literally every single person who ever opened text editor and wrote even a single line of code. It is actually quite cool to see that there are more and more talks that talk about this topic at rstudio::conf since R has a (sometimes deserved) reputation of language that produces difficult to maintain code. 

8. [One RMarkdown document - fourteen demos by Yihui Xie](https://resources.rstudio.com/rstudio-conf-2020/one-r-markdown-document-fourteen-demosyihui-xie)

If you have anxiety about running live demos during presentation, then you probably should not watch this presentation. Yihui showed how same document with minimal modifications can be used in 14 different output formats live on stage.

9. [Spruce up your ggplot2 visualization with formatted text by Claus Wilke](https://resources.rstudio.com/rstudio-conf-2020/spruce-up-your-ggplot2-visualizations-with-formatted-text-claus-wilke)

I think, this talk can be summarized with this:

![](https://imgs.xkcd.com/comics/tasks.png)

Except instead of identifying a bird, we are adding (gasp!) text formatting to `ggplot`'s. It's funny how seemingly innocuous things need to have so much effort put into them, but here we are. You can now put this: "Part of this is in *italics*" in your `ggplot` labels.

10. [Best practices for programming with ggplot2 by Dewey Dunnington](https://resources.rstudio.com/rstudio-conf-2020/best-practices-for-programming-with-ggplot2-dewey-dunnington)

Programming with `ggplot2` is probably not that different from programming in R in general. One obvious difference is that visual differences are more difficult to detect, but this where package like `vdiffr` can help you.
