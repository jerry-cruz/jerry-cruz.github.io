---
layout: post
title:  "Monty Hall Problem"
date:   2018-05-05 19:27:00
categories: probability
---

The [Monty Hall Problem](https://en.wikipedia.org/wiki/Monty_Hall_problem) is a famous probability problem that a lot of people (including [Paul Erdős](https://en.wikipedia.org/wiki/Paul_Erd%C5%91s) ) seem to get wrong. It goes by other names like the three prisoners problem, and has been the source of some controversy; see the wikipedia link above for some history.

In this post, I will solve the problem using a Bayesian approach. I believe doing so will give insight into why many people seem to get it wrong.

# Problem Statement
In some solutions I've seen, the solution highly depends on stating the problem exactly right. This problem, however, is a real-world problem so I will state it with real-world ambiguity. A rigorous Bayasian approach will allow us to properly handle any uncertainty. We can later discuss any changes to the solution when particular uncertainties are resolved. Here it is:

> You are on a game show with Monty Hall (the host)
