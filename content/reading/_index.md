---
title: "Reading"
date: 2023-06-15T10:33:55+08:00
weight: 999
draft: false
---

## Design Pattern

### Law of Demeter

- Each unit should have only limited knowledge about other units: only units "closely" related to the current unit.
- Each unit should only talk to its friends; don't talk to strangers.
- **Only talk to your immediate friends.**

See also [Law of Demeter - Wikipedia](https://en.wikipedia.org/wiki/Law_of_Demeter)

### Open Closed Principle

You can ship an abstract parent class (closed for modification) as part of your binary library, but people can still extend the functionality by adding new child classes (open for extension).

See also:

- [Writing Testable Code](https://se-education.org/learningresources/contents/testing/writing-testable-code.html#rule-2-favor-polymorphism-over-conditionals)
- [Do polymorphism or conditionals promote better design?](https://stackoverflow.com/questions/234458/do-polymorphism-or-conditionals-promote-better-design/234491#234491)

## Microservices

- [Events on the Outside vs Events on the Inside](https://codesimple.blog/2021/03/14/events-on-the-outside-vs-events-on-the-inside/).

## Test

Favor Polymorphism Over Conditionals.

- [Writing Testable Code](https://se-education.org/learningresources/contents/testing/writing-testable-code.html)
