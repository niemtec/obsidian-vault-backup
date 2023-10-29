---
tags:
  - programming/definition
---
A function with **two** arguments. Harder to understand than a [[Monadic Functions]].

> `writeField(name)` is easier to understand than `writeField(output-Stream, name)`

The meaning of both might appear clear, the first glides past the eye easily presenting its meaning.

The second requires a short pause until you learn to ignore the first parameter (`output-Stream`) — which results in problems because **we should never ignore any part of code**. The parts we ignore are where the bugs will hide.