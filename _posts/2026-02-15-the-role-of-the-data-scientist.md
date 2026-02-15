---
layout: post
title: The Role of the Data Scientist
date: 2026-02-15
description: Reflections on what it means to be a data scientist in industry, bridging the gap between mathematical rigor and business impact.
tags: [data-science, industry, reflections]
categories: [opinion]
---

The title of "data scientist" has become one of the most broadly defined roles in the tech industry. Depending on who you ask, a data scientist might be building deep learning models, writing SQL queries, setting up A/B tests, or presenting dashboards to stakeholders. But what should the role really be about?

## Beyond prediction

In my experience, the most impactful work a data scientist can do goes beyond building predictive models. Prediction is just the first step. The real value lies in the **prescriptive** layer --- translating forecasts into actionable decisions. During my PhD, I worked on exactly this pipeline: first estimating demand using discrete choice models, then embedding those models into optimization routines to find the best assortment of products to offer.

This predictive-to-prescriptive pipeline is where Operations Research and Machine Learning meet, and where the most interesting problems live.

## The value of simplicity

One lesson I've learned working in industry is that **simple, explainable models often win**. Not because they're more accurate --- they usually aren't --- but because they're easier to trust, debug, and deploy. When a decision needs to be justified to a stakeholder who doesn't speak the language of gradients and loss functions, an interpretable model is worth its weight in gold.

This doesn't mean we should avoid complexity. It means we should reach for it only when it's justified by the data and the problem at hand.

## Dealing with data sparsity

Academic benchmarks often come with large, clean datasets. Industry rarely offers that luxury. In practice, you deal with:

- **Small samples**: not every product has thousands of transactions.
- **Missing data**: customers don't always tell you why they chose what they chose.
- **Non-stationarity**: the world changes, and your model needs to keep up.

This is what pushed me toward topics like Bayesian learning, low-rank models, and causal inference. These tools help you make robust decisions even when the data is scarce.

## Communication as a core skill

Finally, I believe that **communication is not a soft skill --- it's a core technical skill** for a data scientist. If you can't explain your model, your results, and your recommendations to a non-technical audience, then the work doesn't land. The best model in the world is useless if nobody acts on it.

The role of the data scientist, at its best, is to be the bridge between data and decisions. That requires not just technical depth, but the ability to translate complexity into clarity.
