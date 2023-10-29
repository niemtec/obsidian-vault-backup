---
tags:
  - book
  - software-development
see also:
---
# Clean Code

Code could never be replaced or gotten rid of because it represents the details of the requirements. At some level these details cannot be abstracted away and so must be specified — which is what programming is.

> “Code is really the language in which we ultimately express the requirements”

We might create languages that are closer to requirements and tools to help us convert those requirements into formal structures, but we will never eliminate the necessary precision — so there will always be code.

## Bad Code

> “Later equals never” (LeBlanc’s Law)

We have all felt the relief of a program working and decided that a _*working*_ mess is better than nothing. Leaving bad code behind to be cleaned up later only that _*later equals never*_.

## The Total Cost of Owning a Mess

- **No change is trivial**. Every addition or modification to the system requires that the tangles, twists and knots be “understood” so that more tangles, twists and knots can be added. Over time the mess becomes so big that they cannot be cleaned up.
- Spending time keeping your code clean is not just cost effective (as less time has to be wasted on trying to understand the messy code) but it is also a matter of professional survival.
- It is unprofessional for programmers to bend to the will of managers who do not understand the risks of making messes.

## What is “Clean Code”?

> “The logic should be straightforward to make it hard for bugs to hide, the dependencies minimal to ease maintenance, error handling complete according to an articulated strategy, and performance close to optimal so as not to tempt people to make the code messy with unprincipled optimisations. Clean code does one thing well.”
> (Bjorne Stroustrup)

The metaphor of broken windows: a building with broken windows looks like nobody cares about it. So other people stop caring. They allow more windows to become broken. Eventually they actively break them.

Clean code is practiced through close attention to detail.

> “Clean code is simple and direct. Clean code reads like well-written prose. Clean code never obscures the designer’s intent but rather is full of crisp abstractions and straightforward lines of control.”
> (Grady Booch)

The discipline of Test Driven Development has quickly become one of the most fundamental disciplines. Code without tests is not clean. Regardless of how elegant it is, how readable or accessible, if it hath not tests, it be unclean.

See: [[The Boyscout Rule]]/[[Beck's Rules of Simple Code]]

# Meaningful Names

- You should use **intention-revealing names** such as `int daysSinceCreation`, the name should answer all the big questions. It should tell you why it exists, what it does, and how it is used. (If a name requires a comment, then the name does not reveal its intent)

* You should \*_avoid disinformation, that is to say leaving false clues which obscure the meaning of your code, even if an abbreviation looks good it might be disinformative.
     - Some names can also offer false clues, for example `accountList` shouldn’t be called that \_\_unless_\* is is actually a `List`.
     - The word “list” has meaning of its own and implies a certain structure and if the container holding the accounts is not actually a list, it may lead to false conclusions.
* You must **make meaningful distinctions** between entities so that the programmer knows which one to use, avoid using meaningless words like “info” or “data”.

- Use **pronounceable names** rather than mushing together letters for the sake of shorter acronyms. If it cannot be said during a conversation without sounding silly then it should be renamed.

* Use **searchable names** meaning that if a variable or constant might be used in multiple places in a body of code, it should have a search-friendly name that is easily distinguishable from the rest (rather than ambiguous single-letter variable names).
* **Classes and objects should have a noun name\*** not a verb-based name
* \*_Methods should have a verb name since they are used to \_\_do_\* things with. Accessors, mutators and predicates should be named for their values and prefixed with `get`, `set`, and `is`.
* Pick \***\*one word for one abstract concept\*\*** and stick with it, it can be confusing to have `fetch`, `retrieve` and `get` as equivalent methods of different classes since they all imply the same action.
     - A consistent lexicon is a great boon to the programmers who must use your code.

> “The hardest thing about choosing good names is that it requires good descriptive skills and a shared cultural background. This is a teaching issue rather than a technical, business, or management issue. As a result many people in this field don’t learn to do it very well.”

# Functions

## Small

- Functions should be small. Smaller than small. Typically functions shouldn’t be longer than 20 lines.
- They should not be large enough to hold nested structures which implies that the indent of a function shouldn’t be greater than one or two levels.

## Do One thing

- Functions should do one thing. They should do it well. They should do it only.
- Statements within the function should be at the same level of [[abstraction]], mixing [[abstraction]] levels causes confusion.

## Use Descriptive Names

- Choosing a good name is half the battle in getting small functions that do one thing — the smaller and more focussed a function is, the easier it is to choose a descriptive name.
- Don’t be afraid to make a name long. **A long descriptive name is better than a short enigmatic name**. A long descriptive name is better than a long descriptive comment.

> “You know you are working on clean code when each routine turns out to be pretty much what you expected” (Ward’s Principle)
> The Stepdown Rule

> We want the code to read like a top-down narrative.

> Every function should be followed by those at the next level of [[abstraction]] so that we can read the program descending one level of [[abstraction]] at a time.

## Function Arguments

- The ideal number of arguments for a function is zero ([[Niladic Functions]]). Next comes one ([[Monadic Functions]]), followed closely by two ([[Dyadic Functions]]). Three arguments ([[Triadic Functions]]) should be avoided where possible. More than three ([[Polyadic Functions]]) requires very special justification—and then shouldn’t be used anyway.
- Arguments are even harder from a testing point of view. Imagine the difficulty of writing all the test cases to ensure that all the various combinations of arguments work properly.
     - If there are no arguments, this is trivial.
     - If there’s one argument, it’s not too hard. With two arguments the problem gets a bit more challenging.
     - With more than two arguments, testing every combination of appropriate values can be daunting.
- **Flag arguments are ugly**. Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this function does more than one thing.
- When a function seems to need more than two or three arguments, it is likely that some of those arguments ought to be wrapped into a class of their own.

## Verbs and Keywords

- Choosing good names for a function can go a long way toward explaining the intent of the function and the order and intent of the arguments. In the case of a monad, the function and argument should form a very nice verb/noun pair.

## Have no Side Effects

- Side effects are lies — your function promises to do one thing, but it also does other hidden things.
- Sometimes it will make unexpected changes to the variables of its own class. Sometimes it will make them to the parameters passed into the function or to system globals.
- In either case they are devious and damaging mistruths that often result in strange temporal couplings and order dependencies

## Command Query Separation

- Functions should either do something or answer something, but **not both**.
- Either your function should change the state of an object, or it should return some information about that object.

## Switch Statements

- A `switch` statement with just two cases is larger than it should be and it’s hard to make a switch statement do just one thing
- We can make sure that the statements are buried in a low-level class and isn’t repeated, this is done through [[polymorphism]]
- The **solution** is to bury the `switch` statement in an [[abstract factory]]

## Prefer Exceptions to Error Codes

- Returning error codes from command functions is a subtle violation of [[Command Query Separation]].
- It promotes commands being used as expressions in the predicates of `if` statements.
- When you return an error code, you create the problem that the caller must deal with the error immediately.
- On the other hand, if you use exceptions instead of returned error codes, then the error processing code can be separated from the happy path code

> Functions should do one thing. Error handing is one thing. Thus, a function that handles errors should do nothing else.

> This implies that if the keyword `try` exists in a function, it should be the very first word in the function and that there should be nothing after the `catch/finally` blocks.

---

Every system is built from domain-specific language designed by programmers to describe that system.

Functions are the verbs of that languages and classes are the nouns.

The art of programming is, and always has been, the art of language design.

Master developers think of systems as stories to be told rather than programs to be written.

# Comments

Nothing can be quite so helpful as a well-placed comment. Nothing can clutter up a module more than frivolous dogmatic comments. Nothing can be quite so damaging as an old crufty comment that propagates lies and misinformation.

We use comments to compensate our failures to express ourselves in code.

Code is the only source of truth, the older a comment is the farther way it is from the code that describes it, always aim to explain the intent in code where possible (often its a matter of creating a function that says the same thing as the comment).

## Good Comments

Sometimes comments _can_ be beneficial. These are known as _legal comments_ and may include:

- Legal copy such as copyright or authorship notes (though try to keep these as short as possible)
- Explanation of [[Regular Expressions]] pattern that we are matching for
- Providing some kind of useful information about the intent behind a decision
- Warnings of consequences related to changes or functionality misuse

### TODO Comments

It is sometimes reasonable to leave TODO notes, they are jobs that the programmer thinks should be done but for some reason can’t be implemented at the moment.

This could include reminders to remove deprecated features, reminders to make a change that is dependent on a planned event etc. However, it is **not** an excuse to leave bad code in the system.

# Formatting
