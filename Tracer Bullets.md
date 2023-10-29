---
tags:
  - software-development
see also:
  - "[[The Pragmatic Programmer]]"
---
- When you are building something that hasn't been built before, tracer bullet development illustrates the approach where you need immediate feedback under actual conditions with a moving goal.
- We look for something that gets us from a requirement to some aspect of the final system quickly, visibly, and repeatably.
- Look for areas where you have doubts, and where you see the biggest risk then prioritise the development so that these are the first areas you code.
  ![[Pasted image 20230217220248.png]]
- Tracer code is **not disposable**, it is written to be kept. It contains all the error checking, structuring, documentation, and self-checking that any piece of production code has. It is simply not fully functional.
- It is consistent with the idea that a project is never finished, there will always be changes required and functions to add. It is an incremental approach.

### Advantages

- Users get to see something working early
- Developers build a structure to work in
  - Having worked out end-to-end interactions of the applications the team won't have to pull much out of thin air
- You have an integrated platform
  - Since the systems are end-to-end connected you have an environment where you can add new pieces of code once they have been unit-tested
- You will always have something to demo
- You have a better feel for progress
  - Developers tackle use cases one by one
  - It's easier to measure performance and to demonstrate progress to your user
  - Because individual development is smaller, you avoid creating those monolithic blocks of code that are reported as 95% complete week after week

> [!note]
> This technique is meant for situations where you are not 100% certain of where you are going, you shouldn't be surprised if your first couple of attempts miss.

- With a **prototype**, you are aiming to explore specific aspects of the final system. With a true prototype, you will throw away whatever you lashed together when trying out the concept and re-code it properly using the lessons you've learned
  - Tracer code approach addresses a different problem, you need to know how the application as a whole hangs together
  - You want to show users how the interactions will work in practice, and you want to give your developers an architectural skeleton on which to hang code