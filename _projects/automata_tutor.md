---
layout: page
title: Automata Tutor
description: Web platform that grades automata-theory exercises automatically, used by thousands of students worldwide
img: assets/img/at_logo_card.jpg
importance: 1
category: work
---

[Automata Tutor](https://automata-tutor.live-lab.fi.muni.cz) is a web platform that helps students learn automata theory and formal languages. Instructors build courses from a large set of exercise types, such as finite automata, regular expressions, context-free grammars and pushdown automata. Students submit solutions and get a grade immediately, together with clear feedback on why points were deducted.

## Why it matters

The introductory theoretical computer science course at TUM is mandatory for all computer science Bachelor's students, and it keeps growing: in 2023, more than 1,500 students registered. With roughly 500 homework submissions a week and only a handful of tutors, manual grading is no longer feasible. Automata Tutor gives every student individual feedback at that scale.

The tool is also used well beyond TUM. By 2024, it had more than 4,000 users in 174 courses at universities across Europe, the Americas, Africa and Asia. In a survey of 950 students, 76% said it was a valuable help for learning the course material.

## My role

Since September 2022, I have led the modernization of Automata Tutor. The original version was built over many years by changing student developers, without tests or documentation, and its servers crashed regularly and had to be restarted by hand.

- **Rebuilt the frontend from scratch** in Python/Flask, including 15 exercise types used in the TUM course.
- **Migrated the database** from H2 to MySQL (MariaDB) with a redesigned schema, together with a Master's student whose thesis I supervised.
- **Built the test infrastructure** with pytest fixtures and mock databases, within a Git-based CI/CD workflow.
- **Set up automated monitoring** with Nagios, so that failures are detected and administrators are alerted without waiting for user reports.
- **Wrote the documentation** for the new frontend and database.
- **Wrote a funding proposal** to TUM for the next development phase, covering the backend redesign, a move to Linux and an open-source release.
- **Currently guiding students** through the migration of the backend.

## Technologies

Python, Flask, MySQL/MariaDB, pytest, Git, CI/CD, Nagios, Linux

## Background

Automata Tutor was originally developed by Loris D'Antoni and colleagues and later continued at TUM. Its earlier version is described in the CAV 2020 paper [Automata Tutor v3](https://doi.org/10.1007/978-3-030-53291-8_1). The source code is not public yet, and an open-source release is planned.
