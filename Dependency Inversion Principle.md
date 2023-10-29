---
tags:
  - software-development/design-principles
see also:
  - "[[Single Responsibility Principle]]"
  - "[[Open Closed Principle]]"
  - "[[Liskov Substitution Principle]]"
  - "[[Interface Segregation Principle]]"
  - "[[Dependency Inversion Principle]]"
  - "[[Abstraction]]"
  - "[[SOLID]]"
---
> [!quote]
> High-level classes shouldn't depend on low-level classes. Both should depend on abstractions. Abstractions shouldn't depend on details. Details should depend on abstractions.

- **Low-level classes** implement basic operations such as working with a disk, transferring data, connecting etc.
- **High-level classes** contain complex business logic that directs low-level classes to do something

- You need to describe interfaces for low-level operations that high-level classes rely on, preferably in business terms.
- You can make high-level classes dependent on those interfaces, instead of on concrete low-level classes. This dependency will be much softer than the original one.
- Once low-level classes implement these interfaces, they become dependent on the business logic level, reversing the direction of the original dependency