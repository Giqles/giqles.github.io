---
layout: default
title: Economics and Machine Learning resources
date: 2020-04-24 11:43 +0100
author: Adam Giles
comments: true
---
This is really a collection of resources for myself. It covers 
applications of machine learning methods to quantitative problems
in economics/econometrics. It doesn't cover the economics _of_ machine
learning or artificial intelligence.

It's broken down by resource type:

* [short courses](#short-courses)
* [lecture notes](#lecture-notes)
* [survey papers](#survey-papers)
* [software and tools](#software-and-tools)

I'll try and keep it updated &mdash; [let me know](/contact)
if any of the links get broken or you think there's something I should add!

## Short courses

### NBER Summer Institutes

The NBER summer institutes in econometrics from 2013 and 2015 are 
heavily ML related. Both include full videos of the lectures and downloadable
slides. The [2013](https://www.nber.org/econometrics_minicourse_2013/) series focuses 
on high dimensional data, including text-as-data. The [2015](https://www.nber.org/econometrics_minicourse_2015/) series focuses on more generic ML methods and 
applications to causal problems.

### Becker Friedman Institute

The Becker Friedman Institute at UChicago held an event _"Machine Learning: What's
in it for Economics?"_ in 2016. It covers a relatively broad set of topics including
some network analysis and choice modelling. The slides for the sessions are available
[here](https://bfi.uchicago.edu/event/machine-learning-whats-in-it-for-economics/), and
videos of the lectures are available [here](https://www.youtube.com/playlist?list=PLSSQ1ikQ6KGhTwxYcD05SW8_ZH4xnCBoX).

### Victor Chernozhukov Machine Learning and Econometrics course

This is a course run by Victor Chernozhukov at various institions. I went to a version at cemmap. 
I never figured out how to get updates on events from cemmap, but there is an old course page [online still](https://www.cemmap.ac.uk/event/id/1553). 
Not sure if this will be run again any time soon. If it is, it covers some basics
of machine learning methods and then applies them to typical treatment effect estimation problems.

## Lecture notes

### Susan Athey AEA course materials

Susan Athey hosts a [public google drive](https://drive.google.com/open?id=1SEEOMluxBcSAb_tsDYgcLFtOQaeWtkLp)
folder with a range of materials for different talks, and tutorials in `R` for 
some treatment effect methods. The `ate_tutorial.html` and `hte_tutorial.html`
are particularly useful.

### Victor Chernozhukov course materials

Victor Chernozhukov hosts a [public dropbox](https://www.dropbox.com/sh/zsklenvvb20k3hq/AABxx9gjbRKVymfCiNVEgM6_a?dl=0) 
containing a full set of course materials. Includes lecture notes, labs, and code. This is
the background material that's used for the course [discussed above](#victor-chernozhukov-machine-learning-and-econometrics-course).

## Survey papers

If you're not familiar with this as a topic area, these are probably the best place
to start. This is a series of Journal of Economic Perspectives papers. They're all
very readable and cover a good introduction to the basics of machine learning and
how it can be applied to quantitative economic problems.

I'd probably start with the first and the last, the middle two are a bit more technical.

* [Big Data: New tricks for Econometrics](https://www.aeaweb.org/articles?id=10.1257/jep.28.2.3) \[2014\]
* [High-Dimensional Methods and Inference on Structural and Treatment Effects](https://www.aeaweb.org/articles?id=10.1257/jep.28.2.29) \[2014\]
* [The State of Applied Econometrics: Causality and Policy Evaluation](https://www.aeaweb.org/articles?id=10.1257/jep.31.2.3) \[2017\]
* [Machine Learning: An Applied Econometric Approach](https://www.aeaweb.org/articles?id=10.1257/jep.31.2.87) \[2017\]

## Software and tools

You're almost certainly going to need to look outside `Stata` to implement
these methods in real world problems. Though the latest version of `Stata`
does offer tools for [high-dimensional inference using LASSO](https://www.stata.com/new-in-stata/lasso-inferential-methods/).

Below are some `R` and `python` packages I've found useful.

### Microsoft: ALICE

Microsoft makes the [ALICE/EconML](https://github.com/Microsoft/EconML) package for `python`.
It uses a consistent API to estimate treatment effects in a variety of settings, using
base learners from `scikit-learn`.

### Uber: CausalML

Uber makes the [CausalML](https://github.com/uber/causalml) package for `python`.
It focuses almost exclusively on heterogenous treatment effect estimation problems,
though it also provides interpretability tools for those problems.

There's also an Uber engineering [blogpost](https://eng.uber.com/causal-inference-at-uber/)
on similar topics.

### GRF-labs: grf and policytree

[GRF-labs](https://github.com/grf-labs) is a collection of researchers at Stanford. 
They made the `R` packages `grf` (or "generalised random forests"), and now `policytree`.
These are packages implementing various forest-based methods, mostly focusing on 
heterogenous treatment effect estimation and optimal policy choices.

These packages are extremely high-quality relative to most academic releases. (Which is
not intended as a slight on anyone! &mdash; it just isn't an academic's job to also be a
professional developer).

### HDM R package

This is an `R` package implementing various high-dimensional methods related to LASSO
estimation. The CRAN mirror of it is [here](https://github.com/cran/hdm). Personally
I found this quite buggy, to the point that I abandoned using it.
