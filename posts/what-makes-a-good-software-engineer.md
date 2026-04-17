---
title: what makes a good software engineer
date: '2026-04-17T07:32:19.442Z'
tags: personal
updated: '2026-04-17T11:07:07.492Z'
---
Here are some traits that I think make a good software engineer.

- Generating good code
- Good testing framework
- Good documentation
- Handling ambiguity
- Thinking big picture
- Asking the right questions

## Generating good code
Being able to write simple, flexible, readable and functional code. Whether its hand-written or AI generated, at the end of the day the engineer is responsible for the code that they push out. Having good quality code is important for software that needs to last long. How flexible is it in handling new requirements? When debugging an issue, how easy is it for the engineer to read and understand the code? Does it actually function as intended? Did we cover all edge-cases? Does it meet all the functional and non-functional requirements? Requirement satisfaction would need to be confirmed through testing. With AI, code-output has increased exponentially, however it's important that we keep the code to the same high standards as we would when written by hand. This can be done by thorough code-reviews and rigorous testing.

## Good testing framework
Testing is very important. Unit tests should cover all the individual units of your code. The wider business logic of your code should be tested through integration testing. One of the tricky parts of integration testing is whether to mock or actually call dependencies. Tests are only valuable if they catch real problems before production does. A test suite that only covers the happy path gives a false sense of confidence. Invest time in covering failure cases, boundary conditions, and the scenarios that seem unlikely but are entirely possible. A good heuristic is to ask, for every production incident you encounter: could a test have caught this? If the answer is yes, write that test before you close the ticket.

## Good documentation
Over documentation is always better than under documentation. Especially with AI being able to summarize and find information from heaps of text, I think it will always benefit teams to have as much documentation as possible. There are a few categories of documentation I think matter most in practice.

Runbooks are operational guides that describe how to respond to specific situations — an alarm firing, a service degrading, a known failure mode. A well-written runbook means that any engineer, regardless of familiarity with a system, can follow a clear set of steps to either resolve an issue or safely escalate it. Without runbooks, institutional knowledge lives exclusively in the heads of the engineers who happened to be on-call when something broke. That knowledge walks out the door when people leave.

Design decision records capture the why behind architectural choices. Code tells you what a system does. Documentation tells you why it was built that way. When a new engineer joins and asks "why is this implemented like this?", the answer should not be "I'm not sure, that was before my time." Documenting the alternatives you considered, the trade-offs you weighed, and the constraints you were working under turns a one-time decision into a lasting reference.

Gap-filling documentation is the least glamorous but often the most valuable. Most codebases have areas where the documentation is stale, missing, or simply wrong. When you ramp up on a new system and find yourself spending hours piecing together how something works from reading code and asking colleagues, that is a signal. Write down what you figured out. Future engineers — including your future self — will benefit from it. Treating documentation as a living artifact, updated as part of normal development work, is far more sustainable than periodic documentation sprints that never happen.

## Handling ambiguity
One of the toughest parts about being a software engineer is the amount of ambiguity I have to deal with. Requirements are often incomplete, stakeholders don't always agree on the goal, and the problem space can shift mid-execution. Early in my career, I expected that enough upfront discussion would eventually produce a perfectly clear spec. That rarely happens.

What I've learned is that ambiguity isn't a problem to eliminate — it's a condition to navigate. The key is making your assumptions explicit. When I can't get a definitive answer, I document what I'm assuming and why, then validate those assumptions as early as possible through prototypes, proof-of-concepts, or direct customer feedback. This surfaces misalignment before it compounds into wasted implementation effort.

Closely tied to this is the ability to make reversible decisions under uncertainty. Not every decision needs to wait for complete information. Two-way door decisions — those that can be undone cheaply — should be made quickly. One-way door decisions warrant more caution and deliberate alignment before committing.

## Thinking big picture
As a software engineer I'm responsible for the end-to-end lifecycle of a project. Tunnel vision is an issue I actively try to guard against. It's easy to get absorbed in the immediate ticket — the specific bug, the specific feature — and lose sight of how your change fits into the larger system.

Thinking big picture means asking: How does this component interact with everything else? What happens when this service scales by 10x? If we make this design choice today, what doors does it close for us in two years? It also means caring about things that live outside your immediate codebase — monitoring, alerting, deployment safety, and the operational burden your software places on the team that maintains it.

In practice, this is a skill that develops by deliberately zooming out. Before starting implementation, I try to map dependencies, understand the data flow end-to-end, and identify what could go wrong downstream. Design documents are a useful forcing function here — the act of writing forces you to confront the gaps you would have glossed over otherwise.

## Asking the right questions
I used to work with a senior engineer who had this insane ability to always ask the right questions. "Why are we doing this?", "Do we even need to do this?", "What are the long-term consequences if we go with this solution?". By questioning all parts of the software development life-cycle, including the requirements themselves, we were able to really narrow down the scope of work to only what was absolutely necessary. This reduced complexity, protected us from scope-creep, made sure we covered all security, scalability, compatibility concerns, and even sometimes pivoted the requirements to capture the actual intended objectives.

## Conclusion
These traits do not exist in isolation. The best engineers I have worked with exercise them together and in proportion to the situation. A well-written feature that lacks tests is a liability. Thorough documentation without a big-picture understanding of the system produces documentation for the wrong things. Asking the right questions without the technical depth to act on the answers only gets you so far.

What ties all of these together is a sense of ownership. Treating the software you build as something you are responsible for long after it ships. That means caring about the engineer who has to debug it in the middle of the night, the customer experiencing it in production, and the teammate who has to extend it six months from now. In my experience, that orientation is what separates engineers who are technically capable from engineers who are genuinely excellent.
