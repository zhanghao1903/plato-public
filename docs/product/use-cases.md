# Plato Use Cases

Plato is best suited for work where the user has an outcome in mind but wants
the system to make the work structure visible before acting.

Each example below follows the same task-first loop:

```text
goal -> plan -> review -> run -> inspect result and audit
```

## 1. Plan A Personal Website

User goal:

> Help me create a simple personal website.

What Plato should do:

- ask for missing context if needed;
- draft a plan with content, layout, implementation, and review tasks;
- let the user refine tasks before publishing;
- show results and changed files after work.

Why it fits Plato:

The user may not know the exact pages, stack, or order of work. A visible plan
is more useful than a single long answer.

## 2. Turn A Rough Idea Into Tasks

User goal:

> I want to build a small tool for collecting and summarizing online research.

What Plato should do:

- clarify the target source, output format, and schedule;
- split the idea into planning, implementation, validation, and review tasks;
- expose assumptions before execution.

Why it fits Plato:

The hard part is not writing one answer. The hard part is shaping the work so
the user can judge whether it is the right work.

## 3. Draft Courseware Or Learning Material

User goal:

> Create an HTML courseware page for a seventh-grade biology lesson.

What Plato should do:

- ask about audience, chapter, and teaching style;
- draft a plan for outline, slides/pages, examples, quiz, and review;
- keep the final content tied to tasks and evidence.

Why it fits Plato:

Non-technical users can work from the educational outcome while Plato turns it
into structured work.

## 4. Prepare A Safe File-Change Plan

User goal:

> I want to clean up this project, but I do not want accidental changes.

What Plato should do:

- inspect context when available;
- propose tasks before changing files;
- pause for confirmation on risky operations;
- let the user inspect changed files and audit evidence.

Why it fits Plato:

This is where the Control Plane and Trust Plane matter most: the user needs to
know what will happen and what happened afterward.

## 5. Review A Result Before Continuing

User goal:

> Check what changed and tell me whether the result is good enough.

What Plato should do:

- summarize task outcomes;
- surface changed files, warnings, and missing evidence;
- suggest whether to accept, revise, retry, or stop.

Why it fits Plato:

The product should not end with "done." It should help the user decide what the
result means.

## 6. Break A Bug Fix Into Reviewable Steps

User goal:

> Fix this bug without breaking unrelated behavior.

What Plato should do:

- identify likely investigation tasks;
- separate diagnosis, fix, test, and review;
- ask when context is missing;
- keep the audit trail available after the fix.

Why it fits Plato:

Bug fixing benefits from task boundaries and traceability because users need to
understand both the fix and the evidence.

## Availability Notes

The current `0.1.0` public release is an early local release candidate. Use
these examples as product direction and evaluation scenarios. Check
[Release status](release-status.md) before treating a feature shown in a
screenshot or example as generally available.
