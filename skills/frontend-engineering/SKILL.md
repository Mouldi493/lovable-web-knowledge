---
name: frontend-engineering
description: Use for implementing or refactoring Lovable web projects with React, TypeScript, Tailwind, shadcn/ui and related frontend patterns.
---

# Frontend Engineering

## Principles
Prefer correctness, maintainability and simplicity over novelty.

## TypeScript
- Keep types explicit at boundaries.
- Avoid unnecessary any.
- Do not use unsafe casts merely to silence errors.
- Reuse domain types.
- Model loading, error and empty states explicitly.

## React
- Keep components focused.
- Extract reusable behavior when repetition is real.
- Avoid giant monolithic page components.
- Avoid premature abstractions.
- Keep effects for actual side effects.
- Clean up subscriptions, timers and listeners.
- Preserve state ownership close to where it matters.

## Data and forms
- Validate external/user data.
- Show useful loading and error states.
- Prevent duplicate submissions when relevant.
- Keep form errors close to the affected field.
- Do not silently fail.

## Tailwind/shadcn
- Prefer existing design tokens and component conventions.
- Extend primitives rather than forking many near-identical components.
- Keep utility classes readable.
- Avoid arbitrary values everywhere when tokens can express the system.

## Accessibility
- Use semantic elements.
- Buttons perform actions; links navigate.
- Make interactive elements keyboard accessible.
- Keep visible focus styles.
- Label form controls.
- Use ARIA only when semantic HTML is insufficient.

## Performance
- Avoid unnecessary rerenders and heavy client libraries.
- Split expensive code only when it improves real load behavior.
- Size media appropriately.
- Reserve dimensions to avoid layout shift.
- Defer non-critical work.

## Security basics
- Never expose secrets in client code.
- Treat all user-controlled content as untrusted.
- Use server-side authorization for protected operations.
- Do not rely on hidden UI as security.

## Existing codebases
Before changing architecture:
- inspect current patterns
- understand dependencies
- identify the narrowest safe change
- avoid unrelated rewrites

## Completion
Run available:
- type checks
- lint
- tests
- production build

Fix introduced errors before declaring completion.
