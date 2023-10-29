---
tags:
  - software-development/design-principles
see also:
  - "[[SOLID]]"
  - "[[Single Responsibility Principle]]"
  - "[[Open Closed Principle]]"
  - "[[Liskov Substitution Principle]]"
  - "[[Interface Segregation Principle]]"
  - "[[Dependency Inversion Principle]]"
---
> Classes should be open for extension but closed for modification

- The main idea of this principle is to keep existing code from breaking when you implement new features
- A class is **open** if you can extend it, produce a subclass and do whatever you want with it — add new methods or fields, override base behaviours etc.
- If a class is already developed, tested, reviewed, and included in some framework or otherwise used in an app, trying to mess with its code is risky. It should be **closed** for modification.
- A child class shouldn’t be responsible for the parent’s issues.