---
name: prelaunch-automatic-audit
description: Use immediately before publishing, deploying, handing off, or declaring a website/web app complete to run a structured automatic audit covering functionality, UX, mobile, accessibility, performance, SEO, conversion, content, tracking, security basics and release readiness.
---

# Prelaunch Automatic Audit

## Rule
A project is not ready to publish because it looks finished.

Before launch, run the full audit below and classify every finding.

Use three severities:
- BLOCKER — must fix before publication
- IMPORTANT — should fix before publication unless explicitly accepted
- POLISH — improvement that can safely wait

Do not silently ignore failed checks.

## 1. Build and runtime

Verify:
- production build succeeds
- TypeScript/type checks pass when configured
- lint passes or known exceptions are documented
- no unresolved import errors
- no broken environment-variable references
- no runtime crash on initial load
- no critical console errors

BLOCKER examples:
- build fails
- page crashes
- missing required environment variable
- uncaught exception on main path

## 2. Navigation and links

Test:
- logo/home link
- header navigation
- footer navigation
- primary CTA
- secondary CTA
- internal links
- external links
- legal links
- back/forward navigation when relevant

Check for:
- 404s
- wrong anchors
- placeholder hrefs
- "#"
- links opening incorrectly

## 3. Forms

Test every important form:
- contact
- quote
- signup
- login
- newsletter
- booking
- checkout-related forms

Verify:
- required fields
- invalid input
- error messages
- success state
- duplicate submission prevention
- data actually reaches the intended destination when testable
- form does not reset unexpectedly
- mobile keyboard/input types are appropriate

Never claim a form works unless its behavior was tested.

## 4. Primary user journey

Identify the project's main conversion path.

Examples:
- landing → lead form → success
- product → cart → checkout
- SaaS → signup → activation
- service page → quote request

Test it end to end.

Any break in the primary journey is a BLOCKER.

## 5. Mobile audit

Check at minimum:
- small mobile
- large mobile
- tablet
- laptop
- desktop

Verify:
- no horizontal overflow
- navigation usable
- CTA reachable
- text readable
- buttons/tap targets large enough
- cards stack correctly
- galleries work
- sticky elements do not cover content
- forms fit screen
- modal/drawer fits viewport
- images crop correctly

## 6. Accessibility audit

Check:
- one logical H1
- heading order
- landmarks
- button vs link semantics
- keyboard navigation
- visible focus
- form labels
- alt text
- color contrast
- reduced-motion support
- dialog focus behavior
- error messages understandable without color alone

Critical inaccessible navigation or form controls are IMPORTANT or BLOCKER depending on impact.

## 7. Performance audit

Inspect:
- oversized images
- oversized videos
- unnecessary JS
- duplicate dependencies
- render-blocking assets
- font loading
- third-party scripts
- layout shifts
- lazy loading
- long animations
- excessive network requests

Prioritize:
1. hero/LCP
2. layout stability
3. interaction responsiveness
4. media weight

Do not chase tiny performance wins while critical UX defects remain.

## 8. SEO audit

For indexable marketing pages, verify:
- title
- meta description
- canonical
- robots behavior
- H1
- heading structure
- descriptive URLs
- internal links
- social metadata when relevant
- sitemap/robots configuration where applicable
- structured data validity when present
- no accidental noindex

Check that important content is visible in HTML and understandable.

## 9. Local SEO audit

For local businesses verify:
- business name consistency
- service area
- phone/contact
- address when applicable
- service pages
- local relevance
- LocalBusiness schema when appropriate

Never publish fabricated locations.

## 10. Ecommerce audit

Check:
- product title
- price
- variants
- availability
- gallery
- add-to-cart
- cart quantity
- totals
- shipping messaging
- discounts
- upsells
- return policy links
- mobile sticky CTA
- checkout handoff

Verify no test products, fake reviews, placeholder prices or broken variants remain.

## 11. SaaS audit

Check:
- signup
- login
- logout
- password/reset flow when present
- empty states
- onboarding
- upgrade/pricing links
- plan limits
- error states
- protected routes
- mobile dashboard usability

## 12. Conversion audit

Verify:
- primary CTA is clear
- offer understandable quickly
- proof supports claims
- objections addressed
- forms not unnecessarily long
- no competing CTA clutter
- mobile conversion path usable
- no fake urgency/scarcity

## 13. Content audit

Search for:
- lorem ipsum
- placeholder copy
- "TODO"
- "Coming soon" that should not ship
- fake names
- demo metrics
- placeholder images
- inconsistent prices
- contradictory claims
- spelling errors
- encoding issues
- outdated contact details

## 14. Analytics and tracking

When analytics is part of the project, verify:
- analytics initializes
- primary conversion event fires
- add-to-cart/signup/form events fire when required
- duplicate events are not generated
- consent behavior is correct when required
- test/internal traffic handling when configured

Do not infer successful tracking from code presence alone.

## 15. Security basics

Check:
- no secrets in frontend code
- no service-role/admin keys exposed
- sensitive endpoints require authorization
- user input is validated
- dangerous HTML injection is avoided
- public/private data boundaries are respected

Any exposed secret is a BLOCKER.

## 16. Browser and error-state audit

Check:
- no obvious console errors
- no failed critical network requests
- 404 page exists when appropriate
- API errors produce usable states
- offline/slow behavior does not catastrophically break key UI

## 17. Final release report

Produce a concise report:

### BLOCKERS
List every must-fix issue.

### IMPORTANT
List issues that should be fixed before launch.

### POLISH
List safe post-launch improvements.

### VERIFIED
List checks that passed.

### UNVERIFIED
List anything that could not be tested and why.

## Publish gate

Do not publish or declare ready if BLOCKERS remain.

If only IMPORTANT/POLISH items remain, summarize them and let the user decide whether to proceed.

Never publish automatically unless the user explicitly authorized deployment/publication.
