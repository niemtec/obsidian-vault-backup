---
tags: 
see also:
  - "[[The Pragmatic Programmer]]"
---
- Often you might find the need to represent the same idea in more than one place, that is bad design, it is easy to forget all the places where this knowledge lives. It's not a question of whether you'll remember it, but a question of _when_ you will forget it.

> [!tip]
> Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

- [[DRY]] is about the duplication of knowledge, of intent. It's about expressing the same thing in two different places, possibly in two totally different ways.
- Commonly needed functionality or data that doesn't fall into an obvious area of responsibility can get implemented many times over.

> [!bug] Simple Test
> When some single facet of code has to change, do you find yourself making that change in multiple places or in different formats? Do you have to change code and documentation, or a DB schema and a structure that holds it? If so, your code is not DRY.

- Your goal is to foster an environment where it's easier to find and reuse existing stuff than to write it yourself. _If it isn't easy, people won't do it_.