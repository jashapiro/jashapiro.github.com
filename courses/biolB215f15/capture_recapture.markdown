---
layout: Rmd
title: "Capture Recapture Lab"
pretitle: Biol B215
parent: index.html
tags: [R, tutorial, RStudio, BiolB215]
nav: teaching
---




## Introduction
Estimating the number of organisms in a region is easiest if the organisms don't move and are easy to find. In that case, you can either count them all, or randomly choose subregions to sample and  count the number of individuals in each of those, multiplying by the number of possible subregions. In that case, you would also be able to estimate a confidence interval based on the sampling error in your counts. If you are dealing with moving organisms, but ones that are easy to see, you can often do something similar: counting the number you see in a given area, possibly over time.

When the organisms are cryptic, mobile, or hard to find, you might only be able to find them by trapping them, and you might not have a good sense of how much of the region you had sampled, or what fraction of individuals in an area you were able to catch. In short, a single sample might have any number of relations to the total number of individuals in the population, ($N$).  In this case, you can employ the capture-recapture method. In your first trip, you capture some number of individuals, which we will call $M$ (for marked). These are then marked somehow (with paint, leg bands, clipping, or some other permanent mark) and returned to the region. After some time, you return and capture a second sample of individuals, $C$ (for capture), of which $R$ (for recapture) have the marks that you put on during the first trip. Assuming that no tags fell off, and no individuals left or entered the region (including by birth or death), then the fraction of individuals with marks in the second trapping should be equal to the fraction of the total population that you caught on the first trip. In other words:

$$\frac{M}{N} = \frac{R}{C}$$

With a quick rearrangement of that equation, we can estimate the population size $N$ from the number of individuals caught in the first round $M$, the number caught in the second round $C$, and the number of the second round that had already been captured $R$:

$$N=\frac{MC}{R}$$

This equation is not perfect, as you will see, and we will explore a some ways to improve this initial estimate of population size through the course of the lab.

## Lizards!
While it might be fun to actually do this experiment with real animals in the wild, doing so would take a lot more time than we have. So instead I have acquired a large number of small, colorful, plastic lizards which we will use as a stand-in for real lizards. They have a number of advantages: They are easy to catch, they don't run away, they don't bite, they have minimal dietary requirements, etc. Your ultimate task in this lab will be to estimate the number of toy lizards in a box by performing a capture-recapture experiment with them.

But first, have a look in the box. Without touching the lizards or talking to classmates, estimate how many lizards there are. Write down your estimate, and tell it to me so that I will have a record of everybody's estimates. At the end of this lab, we will compare these initial estimates to the estimates from the capture-recapture experiment. 

In addition to your point estimate, take out a piece of paper and make a sketch that indicates the your own feeling about the probability distribution for the number of lizards in the box. Put the number of lizards in the box on the x-axis, but don't worry about the exact scale on the y-axis for now: the relative heights should simply indicate how likely you think each value is relative to the others. If you don't have a strong sense of the number of lizards, this distribution might be quite wide and flat; if you are fairly confident in your guess it might be relatively peaked and narrow. 


## Designing a sampling strategy
Clearly, the more individuals captured in each phase of a capture-recapture experiment, the better your estimates of the population size will be, but we can't just expect unlimited resources for sampling.  There are always limits on the number of individuals you can capture, whether because of license limitations, time constraints, or simply the effort required to process each animal captured. With our docile toy lizards, we could just "catch" all of them and go to work counting, but I'm not going to let you do that. I am imposing a total class budget of **200** lizard captures, split however you like between the first and second "trappings". 

Since we only have one set of lizards, we will have to decide as a class what the best way to divide our effort to sample the lizards is. Take some time to discuss your thoughts with those around you, then we will talk about it as a group. We don't have to make a final decision quite yet, but we should have some ideas about *how* we would make this decision.

## Next
Before we actually perform the experiment, we will prepare some of the analysis methods that we will be using in `R`, and simulate some data to make sure that everything is working correctly.
**[Initial analysis and simulations of capture-recapture data](capture_recapture2.html)**

