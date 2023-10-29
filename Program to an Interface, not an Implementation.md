---
tags:
  - software-development/design-patterns
see also:
---
- You should program to an interface, not an implementation of a class. This will lead to the code depending on abstractions and not concrete classes.
- You can tell that the design is flexible enough if you can easily extend it without breaking any existing code.

- There's a flexible way to establish collaboration between objects:
  1.  Determine what exactly one object needs from the other: which methods does it execute?
  2.  Describe these methods in a new interface or abstract class
  3.  Make the class that is a dependency implement this interface
  4.  Make the second class dependent on this interface rather than on the concrete class