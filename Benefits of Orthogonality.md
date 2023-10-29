---
tags:
  - software-development
see also:
  - "[[Orthogonality]]"
---
### Gain Productivity

It's easier to write relatively small, self-contained components than large blocks of code. Simpler components can be designed, coded, tested, and then forgotten.
If components have specific, well-defined, responsibilities, they can be combined with new components in ways that were not envisioned by their original implementors.

### Reduce Risk

Broken sections of code are isolated. Brokenness doesn't spread to other components in the system.
It's easier to slice out a broken component and put something new in its place.
The system is less fragile, small changes and fixes can be concentrated in a particular area and any problems generated are restricted to that area.

### Design

Systems should consist of a set of cooperating modules, each with implementation of functionality independent of the others. (Sometimes these components are organised into layers (i.e. [[Clean Architecture]]), each providing a level of [[abstraction]].)

A layered approach is a powerful way to design orthogonal systems because each layer uses only the abstractions provided by the layers below it you have great flexibility in changing underlying implementations without affecting code.

> [!tip] Just One
> Once you have your components mapped out, ask yourself: _If I change the requirements behind a function, how many modules will be affected?_. In an orthogonal system, the answer should be "one".

> [!question] Toolkits and Libraries
> When you bring in a toolkit, ask yourself whether it imposes changes on your code that shouldn't be there.

### Coding

- **Keep Your Code Decoupled**: write shy code — modules that don't reveal anything unnecessary to other modules and that don't rely on other modules' implementations. (Try the [[Law of Demeter]]).
- **Avoid Global Data**: every time your code references global data, it ties itself into the other components that share that data. In OOP context is often passed as parameters to objects' constructors. The [[Singleton Pattern]] is a way of ensuring that there is only one instance of an object of a particular class. (Be careful with singletons — they can also lead to unnecessary linkage)
- **Avoid Similar Functions**: you might come across functions that look similar, duplicate code is a symptom of structural problems. (See [[Strategy Pattern]] for better implementation)
