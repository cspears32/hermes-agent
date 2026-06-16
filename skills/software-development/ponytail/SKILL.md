---
name: ponytail
description: Enforces YAGNI and minimal code generation. Prevents AI over-engineering, verbosity, and scaffolding.
category: software-development
---
# Ponytail: The Lazy Senior Developer Principle

## Core Heuristic
"The best code is the code you never wrote."

## Trigger Conditions
- Before writing new code, planning architecture, or reviewing PRs.
- When the prompt involves adding features, refactoring, or setting up new projects.

## Mandatory Rules
1. **Strict YAGNI**: Do not implement features, edge cases, or abstractions "just in case" they might be needed later. Implement *only* what is explicitly requested.
2. **Minimal Surface Area**: Prefer a single, well-named function over a class. Prefer the standard library over introducing new dependencies.
3. **Zero Scaffolding**: Do not leave `TODO` comments, placeholder functions, or boilerplate. If it is not being implemented now, it does not exist.
4. **Ruthless Deletion**: When refactoring, delete dead code immediately. Do not comment it out or leave it "for reference".
5. **Verbosity Penalty**: Explanations must be extremely concise. No "Here is the code that does X" or "Let me know if you need further adjustments". Deliver the artifact and stop.

## Pitfalls to Avoid
- **Over-abstraction**: Creating interfaces, factories, or base classes for a single implementation.
- **Defensive Over-engineering**: Adding complex error handling, retries, or middleware for trivial, deterministic operations unless explicitly required.
- **Test Bloat**: Writing exhaustive tests for trivial getters/setters or pure data-transfer objects unless explicitly mandated.

## Verification Step
Before finalizing any code output, ask internally: "Can this be deleted, simplified, or merged with an existing component without losing explicitly requested functionality?" If yes, do it.