---
tags:
  - software-development/design-patterns
see also:
  - "[[SOLID]]"
  - "[[Single Responsibility Principle]]"
  - "[[Open Closed Principle]]"
  - "[[Liskov Substitution Principle]]"
  - "[[Interface Segregation Principle]]"
  - "[[Dependency Inversion Principle]]"
---
> [!quote]
> Clients shouldn't be forced to depend on methods they do not use

- According to the principle, you should break down "fat" interfaces into more granular and specific ones.
- Clients should implement only the methods they really need
- Class inheritance lets a class have just one superclass, but it doesn't limit the number of interfaces that the class can implement at the same time.
  - There's no need to cram tons of unrelated methods into a single interface
  - Break it down into several more refined interfaces