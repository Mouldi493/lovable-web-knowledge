---
name: premium-motion-interactions
description: Use when a website or web app needs refined animations, microinteractions, transitions, loading states, scroll reveals or interaction polish without sacrificing performance or accessibility.
---

# Premium Motion and Interactions

## Principle
Motion should communicate state, hierarchy, continuity or feedback. It is not decoration by default.

## Good uses
Use motion for:
- menu open/close
- accordions
- tabs
- modal/drawer transitions
- hover/focus feedback
- form success/error
- loading/progress
- content reveal
- route/page transition
- spatial continuity
- product demonstration

## Timing
Keep interaction feedback fast.

Typical ranges:
- button/hover: 120–220ms
- small UI state: 160–280ms
- modal/drawer: 220–380ms
- large composed reveal: 350–700ms

These are defaults, not laws.

## Easing
Prefer natural acceleration/deceleration.
Avoid linear motion for most interface movement.

Keep easing consistent across the design system.

## Transform and opacity
Prefer performant properties such as:
- transform
- opacity

Avoid animating expensive layout properties continuously when a transform can achieve the same effect.

## Entrance animations
Do not animate every element individually.

Use:
- small grouped staggers
- consistent direction
- short travel distances
- hierarchy-driven sequencing

Content must remain understandable with animation disabled.

## Scroll reveals
Use when they support storytelling or hierarchy.

Avoid:
- excessive parallax
- scroll hijacking
- long delays
- content hidden until JavaScript fires
- effects that make reading harder

## Hover states
Hover should clarify interactivity.

Do not rely on hover as the only state because touch devices do not have it.

## Buttons
Useful feedback:
- subtle translate/scale
- color/contrast shift
- icon motion
- loading state
- success confirmation

Avoid large bouncy effects for ordinary actions.

## Menus and navigation
Maintain spatial continuity:
- dropdown emerges from trigger
- drawer comes from logical edge
- active state transition is clear
- background/header state changes remain readable

## Loading
Choose the lightest honest state:
- instant response → no loader
- short wait → subtle spinner/progress
- content fetch → skeleton only when it improves perceived structure
- long task → explicit progress/status

Avoid fake progress.

## Reduced motion
Respect `prefers-reduced-motion`.
Provide an immediate or simplified state when motion is reduced.

## Performance
- avoid dozens of simultaneous animations
- avoid permanent GPU-heavy effects
- test low-powered mobile behavior
- pause offscreen/nonessential animation where appropriate
- compress/optimize animated media

## Quality gate
Before keeping an animation, ask:
1. What does it communicate?
2. Does it improve orientation or perceived quality?
3. Is it still usable without it?
4. Does it remain smooth on mobile?
5. Does it respect reduced motion?

If the answer to #1 is "nothing," remove it.
