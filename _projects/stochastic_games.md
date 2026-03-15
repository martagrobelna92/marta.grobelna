---
layout: page
title: Concurrent Stochastic Games
description: Research project on concurrent stochastic games
img: assets/img/CSGs.jpg
importance: 1
category: work
related_publications: true
---


Why are Concurrent Stochastic Games Interessting?
-------------------------------------------------

A Concurrent Stochastic Game (CSG) is a powerful mathematical framework used to model systems where multiple independent agents make decisions simultaneously. Unlike sequential models, CSGs capture the "real-world" reality that actions happen in parallel and the outcome is often influenced by probabilistic events (uncertainty).

Verification of Concurrent Stochastic Games
-------------------------------------------

In this project, we focus on two-player concurrent stochastic games with reachability objectives. Specifically, we are developing new algorithms to estimate values, which refer to the supremum probabilities of reaching a target state.

The main output of this project is the paper titled "Stopping Criteria for Value Iteration on Concurrent Stochastic Reachability and Safety Games." Value Iteration (VI) is one method used to estimate these values. While it may require exponential time in the worst cases, VI typically outperforms other solution techniques, such as strategy iteration and mathematical programming, in practice. 

Traditionally, VI stops once two consecutive value estimates are epsilon-close to each other. However, this stopping criterion does not provide guarantees regarding the precision of the value estimates (i.e., how far the current estimate is from the true value). To address this issue, we aimed to not only under-approximate the values but also over-approximate them, effectively sandwiching the true values. The outcome of this approach is an anytime algorithm.








