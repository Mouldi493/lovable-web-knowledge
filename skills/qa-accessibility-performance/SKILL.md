---
name: qa-accessibility-performance
description: Use before launch or after meaningful frontend changes to verify functionality, responsive behavior, accessibility, performance and critical user journeys.
---

# QA, Accessibility and Performance

## Functional QA
Verify:
- navigation
- links
- buttons
- forms
- validation
- success/error states
- drawers/modals
- filters/search
- account flows
- checkout/signup/contact path
- external integrations relevant to the task

## Responsive QA
Check representative widths:
- small mobile
- large mobile
- tablet
- laptop
- large desktop

Look for:
- overflow
- clipped content
- wrong stacking order
- oversized typography
- broken sticky elements
- inaccessible CTAs
- bad image crops
- unusable tap targets

## Accessibility
Check:
- semantic headings
- landmarks
- keyboard navigation
- focus visibility
- labels
- alternative text
- contrast
- reduced motion
- error messages
- dialog behavior

## Performance
Inspect:
- image/video size
- lazy loading
- font loading
- layout shift
- excessive JavaScript
- long main-thread tasks
- unnecessary network calls
- render-blocking assets

## Browser quality
Check the console for new errors.
Check network failures for critical assets or API calls.

## Content QA
Verify:
- no placeholder copy
- no invented proof
- consistent pricing
- correct contact details
- correct legal/policy links when required
- no broken characters
- no contradictory CTA wording

## Launch gate
Do not call a site finished until the primary user journey works on mobile and desktop.

Report:
- what was tested
- what passed
- what failed
- what remains unverified
