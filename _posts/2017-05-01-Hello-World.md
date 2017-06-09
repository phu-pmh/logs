---
layout: post
title: "Hello World"
description: "Greetings"
date: 2017-05-01
tags: [General]
comments: true
share: true
mathjax: true
---

Hello World!
Nothing here yet, but thanks for visiting!  

မဂၤလာပါ။


In vanilla supervised learning the objective is to maximize \\( \sum\_i \log p(y\_i \mid x\_i) \\) where \\(x\_i, y\_i \\) are training examples (such as images and their labels). Policy gradients is exactly the same as supervised learning with two minor differences: 1) We don't have the correct labels \\(y\_i\\) so as a "fake label" we substitute the action we happened to sample from the policy when it saw \\(x\_i\\), and 2) We modulate the loss for each example multiplicatively based on the eventual outcome, since we want to increase the log probability for actions that worked and decrease it for those that didn't. So in summary our loss now looks like \\( \sum\_i A\_i \log p(y\_i \mid x\_i) \\), where \\(y\_i\\) is the action we happened to sample and \\(A_i\\) is a number that we call an **advantage**. In the case of Pong, for example, \\(A\_i\\) could be 1.0 if we eventually won in the episode that contained \\(x\_i\\) and -1.0 if we lost. This will ensure that we maximize the log probability of actions that led to good outcome and minimize the log probability of those that didn't. So reinforcement learning is exactly like supervised learning, but on a continuously changing dataset (the episodes), scaled by the advantage, and we only want to do one (or very few) updates based on each sampled dataset.

-- Karpathy's blog
