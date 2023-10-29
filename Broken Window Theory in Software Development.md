---
tags:
  - software-development
---
> “Visible signs of crime, anti-social behaviour and civil disorder create an urban environment that encourages further crime and disorder, including serious crimes. The theory suggests that policing methods that target minor crimes such as vandalism, public drinking, and fare evasion help to create an atmosphere of order and lawfulness, thereby preventing more serious crimes.”
> (Broken Window Theory, 1982)

If you have a building with many windows and someone breaks one, you are meant to hold the culprit responsible and fix the damage as soon as possible. If you do not take action, because the window does not seem important, other people might be tempted to break more windows as there are no consequences of doing so.
In time, more windows will get broken at which point it will be too difficult and expensive to fix them or prevent any further destruction

> "Prevention is better than cure" (Desiderius Erasmus #C15)

- This translates to software engineering given that any person who contributes to a mess that presents some visible issues isn't really changing the system, instead they are contributing to the propagation of those issues through replication and imitation.
- This law is sometimes disputed as leading to perfectionism or imposing costly habits/behaviours within delivery teams, but no project is going to be perfect.
  - Given time and money constraints these issues might not be "worth fixing" at which point it is important to be honest about it, deciding to leave something the way it is (correct but not perfect) for the sake of progress is a practical and efficient way of doing things.
  - The software we build might not do everything perfectly, but what it does, it can do really well.
- Limiting the scope to a reasonable standard is a great way to ensure teams have the time they need to get the important stuff right.

## Broken Window Theory Flow

### 1. Good System
New project starts with intrinsically clean setup.

### 2. A "window" is broken
Due to high pressure to deliver or a normal lack of knowledge people make mistakes. This is a normal part of the process and team knowledge growth.

### 3. No measures are taken
Technical debt is either not discovered during code reviews or is accepted with the elusive promise that it will be fixed at a later date.

### 4. More "windows get broken"
Issues propagate in the code through imitation, repetition, and copying code containing bad practice. (Particularly prominent for new developers who might know any better)

### 5. A broken system
The system begins manifesting rigidity and fragility. Changing it now would become a highly costly exercise, requiring significant time and resources to repair.

> [!NOTE] Loss of Will
> In the Broken Window Theory, people lose the will to fight entropy because they perceive that no one else cares.
