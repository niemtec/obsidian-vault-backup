---
tags:
  - book-notes
  - software-development
  - programming
---
# Chapter 1 - A Pragmatic Philosophy

Being a **Pragmatic Programmer** is about adopting an attitude, a style, and a philosophy of approaching problems and their solutions. They think beyond the immediate problem, placing it in larger context. They seek out larger context useful to make intelligent compromises and informed decisions.

## Control

Software development is a career of control, the skills are in demand, knowledge crosses geographic boundaries, remote work is possible.

Software Engineers have agency. Does the work environment suck? Is the job boring? Try to fix it, but don’t try forever.

> “You can change your organisation or change your organisation” (Martin Fowler)

## Responsibility

Being pragmatic is about being responsible for yourself and your actions in terms of career advancement, learning and education, your project, and day-to-day work. It’s about taking charge of your own career and not be afraid to admit ignorance or error.

We can be proud of our abilities, but we must own up to our shortcomings — our ignorance and our mistakes.

### Team Trust

Your team needs to be able to trust and rely on you — and you need to be comfortable relying on each other.

In a healthy environment based in trust you can safely speak your mind, present ideas and rely on your team members who can, in turn, rely on you.

## Taking Responsibility

You make a commitment to ensure that something is done right, but you don’t necessarily have direct control over every aspect of it. Apart from doing your own personal best, you must understand the situation and analyse the risks that are beyond your control.

You have the right **\*\***\*\*\*\***\*\***not**\*\***\*\*\*\***\*\*** to take responsibility for impossible situations, or one where risks are too great, or ethical implications too sketchy. You’ll have to make a call based on your own values and judgement.

When you **do** accept responsibility for an outcome, you should expect to be held accountable for it. When you make a mistake (as we all do) admit it honestly and try to offer options.

Don’t blame someone or something else, or make up an excuse. It is up to you to provide solutions, not excuses.

> [!Tip]
> Provide options, don't make excuses

Before approaching anyone stop and listen to yourself, talk to the rubber duck on your monitor. Does the excuse sound reasonable, or stupid? How’s it going to sound? Instead of excuses, provide options.

Don’t say it **can’t be done**, explain what **can be done** to salvage the situation.

## Knowledge Portfolio

Your knowledge and experience are your most important professional assets, but they are **expiring** assets. Knowledge becomes out of date as new technology emerges, changing market forces may render your experience obsolete or irrelevant.

> [!tip]
> Your ability to learn new things is your most important strategic asset.

Managing your knowledge portfolio effectively: 1. Serious investors invest regularly (as a habit) 2. Diversification is the key to long-term success 3. Smart investors balance their portfolios between conservative and high-risk, high-reward investments 4. Investors try to buy low and sell high for maximum return 5. Portfolios should be reviewed and rebalanced periodically

### Building Your Portfolio

**Invest Regularly**: continuous investment, even if it's just a small amount, provides larger benefits over time. (Plan to use a consistent time and place, away from interruptions).

**Diversify**: the more _different_ things you know, the more valuable you are. Don't stop at your current technology, the more you are comfortable with, the better you will be able to adjust to change. (Don't forget the _other_ skills you need, including those in non-technical areas)

**Manage Risk**: don't put all your technical eggs in one basket

**Buy low, sell high**: learning an emerging technology before it becomes popular can be hard but often carries high payoff

**Review and rebalance**: this is a very dynamic industry, the hot technology you started investigating last month might be stone cold by now

### Goals

**Learn at least one new language every year**: different languages solve the same problems in different ways, by learning several different approaches, you can help broaden your thinking and avoid getting stuck in a rut

**Read nontechnical books too**: computers are used by _people_ — people whose needs you are trying to satisfy. You work with people, are employed by people, and get hacked by people. _Don't forget the human side of the equation, as that requires an entirely different skillset._

**Participate in groups and meetups**: isolation can be deadly to our career; find out what people are working on outside of your company. Don't just go and listen: actively participate.

> [!NOTE]
> It's important to continue investing. Once you feel comfortable with some new language or bit of technology, move on. Learn another one.

It doesn't matter if you use any of these technologies directly, the process of learning will expand your thinking and open you to new possibilities and ways of doing things.

Cross-pollination of ideas is important; try to apply the lessons you've learned to your current project. Even if your project doesn't use that technology, you can borrow some ideas.

### Critical Thinking

You need to think **critically** about what you read and hear, the knowledge in your portfolio should be accurate and unswayed by either vendor or media hype.

Beware of zealots who insist that their dogma provides the only answer — it may or may not be applicable to you and your project.

**Ask the "Five Whys"**: ask "why?" at least five times, dig deep and you might be able to get closer to a root cause this way.

**Who does this benefit?**: _follow the money_, it might be a helpful path to analyse. The benefits to someone else or another organisation may be aligned with your own (or not!)

**What's the context?**: everything operates in its own context, which is why universal solutions don't often work. ("Best practice", best for who?)

**When or Where would this work?**: don't stop with first order thinking (what will happen next), bust use second-order thinking (what will happen after that?)

## Communicate

Plan what you want to say. Write an outline. Then ask yourself "does this communicate what I want to say to my audience in a way that works for them?" Refine it until it does.

> [!NOTE]
> English is just another programming language

You need to work out what the priorities of your audience are. Make what you're saying relevant in time, as well as in content. Sometimes all it takes is the simple question "is this a good time to talk about... ?"

There's one way you must use if you want people to listen to you: _listen to them_. Even in a situation where you have all the information, if you don't listen to them, they won't listen to you.

Turn meetings into dialogs and you'll make your point more effectively. Who knows, you might even learn something.

Keeping people informed makes them far more forgiving of the occasional slip, and makes them feel that you haven't forgotten them.

# Chapter 2 - A Pragmatic Approach

## Good Design is Easier to Change

Good design means adaptability to the people who use it. For code, that means it must adapt by changing. [[ETC Principle]].

Working with the [[ETC Principle]] is about developing values that help you to make decisions: should you do this or that?

The premise in [[ETC Principle]] assumes that a person can tell which of the paths will be easier to change in the future, most of the time common sense is correct and you can make an educated guess.

Sometimes you won't have a clue, that's OK, in those cases fall back on the "easy to change" path: try to make what you write replaceable. That way whatever happens in the future the code won't be a roadblock.

> [!info]
> Writing replaceable code might seem counterintuitive, but it's what you should be doing all the time anyway. It's really just thinking about keeping the code decoupled and cohesive.

## The Evils of Duplication

As developers, we collect, organise, maintain, and harness knowledge. This knowledge is documented in specifications, we make it come alive in running code, and we use it to provide the checks needed during testing.

**Knowledge isn't stable**. It changes, rapidly. Your understanding of a requirement may change following a meeting.

Most people assume that maintenance begins when an application is released, that means fixing bugs and enhancing features. **They're wrong**. Developers are constantly in maintenance mode, our understanding changes daily. New requirements arrive and existing requirements evolve as we work on the project.

> [!NOTE] Maintenance
> Maintenance is not a discrete activity, but a routine part of the entire development process

## Don't Repeat Yourself

## [[Orthogonality]]

Orthogonality is a critical concept if you want to produce systems that are easy to design, build, test, and extend. Once you learn to apply the principle, you'll notice an immediate improvement in the quality of systems you produce.

In computing, the term signifies a decoupling, two or more things are orthogonal if changes in one do not affect any of the others.

Nonorthogonal systems (opposite of orthogonal systems) are inherently more complex to change and control. When components of any system are highly interdependent there is no such thing as a local fix.

> [!tip] Cohesion
> We want to design components that are self-contained: independent, with a single well-defined purpose. They're cohesive.

###

## Reversibility

Engineers prefer simple, singular solutions to problems. We don't want to make many critical, irreversible decisions which is why we stick to [[DRY]] principle, [[Decoupling]], and use of [[External Configuration]].

It is important to never assume that any decision is cast in stone and preparing for the contingencies that might arise.

> [!tip] It's all temporary
> Instead of carving decisions in stone, think of them more as being written in the sand on the beach. A big wave can come along and wipe them out at any time.

Always break your code into components even if you end up deploying them on a single massive server, this approach is a lot easier than taking a monolithic application and splitting it.

## Prototypes and Post-it Notes

- Post-it notes are great for prototyping dynamic things such as workflow and application logic

> [!example] Things to Prototype
>
> - Anything that carries risk
> - Anything that hasn't been tried before
> - Anything that is absolutely critical to the final system
> - Anything unproven, experimental, or doubtful
> - Anything you aren't comfortable with:
>   - Architecture
>   - New functionality in an existing system
>   - Structure or contents of external data
>   - Third-party tools or components
>   - Performance issues
>   - User interface design

### How to use prototypes

- **Correctness**: you may use dummy data where appropriate
- **Completeness**: prototype may function only in a very limited sense, perhaps with only one preselected piece of input data etc
- **Robustness**: error checking is likely to be incomplete or missing entirely
- **Style**: prototype code shouldn't have much in the way of comments or documentation

### Prototyping architecture

- You're looking for is how the system hangs together as a whole (deferring details)
  - Are the responsibilities of the major areas well defined and appropriate?
  - Are the collaborations between major components well defined?
  - Is coupling minimised?
  - Can you identify potential sources of duplication?
  - Are interface definitions and constraints acceptable?
  - Does every module have an access path to the data it needs during execution?
  - Does it have that access when it needs it?

> [!failure] How not to use prototypes
> You must make it **very** clear that this code is disposable, incomplete, and unable to be completed.
> If you feel that there is a strong possibility in your environment or culture that the prototype might be misinterpreted, you may be better off with the tracer bullet approach.

## Estimating

- By learning to estimate (and by developing this skill to the point where you have an intuitive feel for the magnitudes of things) you will be able to show an apparent magical ability to determine their feasibility
- Learning how to estimate can be hard, so you should try to draw on other people's experiences where you can
- The process of building a model can lead to discoveries of underlying patterns and processes that weren't apparent on the surface
- See [[PERT]]

# Chapter 3 - The Basic Tools

- Tools amplify your talent, the better your tools (and the better you know how to use them) the more productive you can be.
  - Start with a basic set of generally applicable tools but expect to add to your toolbox regularly.
- Many programmers make the mistake of adopting a single power tool and never leave its interface. You need to be comfortable beyond the limits imposed by your IDE.

## The Power of Plaintext

- As a developer your base material is knowledge. The gathering of requirements is gathering knowledge which is expressed in the designs, implementations, tests, and documents.
- Plaintext is is the most human-readable form of data (self-describing data) which will outlive any application that created it.

> [!note] Unix Philosophy
> Unix is famous for being designed around the philosophy of small, sharp tools, each intended to do one thing well. This philosophy is enabled by using a common underlying format—the line-oriented, plain-text file. Databases used for system administration (users and passwords, networking configuration, and so on) are all kept as plain-text files.

## Engineering Daybooks

- Engineers keep notebooks. They've been trained to keep a _daybook_, a kind of journal in which they record what they do, things they've learned, sketches of ideas, readings... basically anything to do with their work.
