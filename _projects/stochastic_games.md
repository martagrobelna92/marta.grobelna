---
layout: page
title: Concurrent Stochastic Games
description: Algorithms with guaranteed precision for decision-making under uncertainty with multiple agents
img: assets/img/CSGs.jpg
importance: 2
category: work
related_publications: true
---

## The problem

Many real systems involve several independent agents that act at the same time, while the outcome also depends on chance: robots sharing a workspace, a controller facing an unpredictable environment, or a defender reacting to an attacker. Concurrent stochastic games are the mathematical model for such situations. A central question is: what is the best probability with which one agent can reach a goal, no matter what the other agent does?

## Why existing methods fall short

The method used most in practice is value iteration. It starts from a lower estimate of this probability and improves it step by step. Traditionally, it stops once two consecutive estimates are close to each other. This rule gives no guarantee about how far the result is from the true answer, and the error can in fact be large. For safety-critical applications, that is not good enough.

## What I developed

Together with Jan Křetínský and Maximilian Weininger, I developed the first value-iteration algorithm for concurrent stochastic games with a guaranteed precision {% cite lics25 %}. Besides the lower estimate, the algorithm also computes an upper estimate that converges to the true value, so the answer is always enclosed between the two. The algorithm stops only when both estimates are within the requested precision. It can also be stopped at any time and still reports how precise its current answer is.

I developed the theory, proved the algorithm correct, and implemented it in Java as an extension of the [PRISM](https://www.prismmodelchecker.org) probabilistic model checker. The games can have millions of states, and every iteration requires solving a linear program for each state. I formulated these problems in AMPL and solved them with Gurobi and other solvers through the AMPL Java API, after first prototyping the method in MATLAB.

## Ongoing work

- **Faster recomputation.** In a second project, we developed hot-starting and incremental value iteration for Markov decision processes. When a model changes, the algorithm reuses earlier results while keeping its precision guarantees. On several benchmarks, this speeds up the computation by multiple orders of magnitude. The paper is under review.
- **New algorithms.** I am developing bounded strategy iteration and a new quadratic-programming formulation for concurrent stochastic games.
- **Partial information.** I am extending these methods to partially observable Markov decision processes, where agents cannot see the full state of the system.

## Technologies

Java, PRISM, AMPL, Gurobi, linear and quadratic programming, MATLAB
