# Global Web/Product Standards

## Core principle
Build websites and web apps as business assets, not collections of attractive sections. Every decision should support a clear user goal, business objective, conversion path, usability, maintainability, and performance.

## Before building
- Inspect all available project context before asking questions: existing code, files, screenshots, copy, brand assets, URLs, analytics, product information, and requirements.
- Never ask the user to repeat information that is already available.
- For a brand-new website, do not start coding immediately. First establish the website type, primary objective, target audience, main offer, primary CTA, brand direction, existing assets, trust/proof, competitors, SEO/geographic scope, required functionality, content status, and technical constraints.
- Ask discovery questions one at a time. Skip irrelevant questions. Stop asking once enough information exists to make strong decisions.
- Summarize the agreed direction into a concise Website Brief before implementation.

## Product and conversion thinking
- Define one primary conversion for every marketing website or landing page.
- Structure pages around user intent: problem → desired outcome → solution/mechanism → proof → objections → action.
- Every major section must earn its place by improving understanding, trust, desire, navigation, SEO, or conversion.
- Do not add sections just because they are common.
- Avoid competing primary CTAs.
- Never fabricate testimonials, ratings, customer counts, certifications, awards, guarantees, scarcity, urgency, press mentions, partner logos, or performance claims.

## Copywriting
- Write clear, specific, human copy.
- Headlines must communicate value, not merely sound clever.
- Prefer concrete outcomes, mechanisms, proof, and objections over vague superlatives.
- Avoid generic AI language, corporate filler, empty hype, and repetitive rhetorical formulas.
- Adapt voice to the brand and audience.
- Preserve strong existing copy when editing rather than rewriting everything unnecessarily.
- For local businesses, include real service and geographic intent naturally.
- For ecommerce, translate specifications into customer benefits without inventing claims.
- Keep CTA labels explicit and action-oriented.

## Design quality
- Commit to one coherent visual direction instead of mixing unrelated trends.
- Build a reusable design system before multiplying sections: typography, color tokens, spacing, radii, borders, shadows, containers, buttons, cards, inputs, responsive behavior, and interaction language.
- Avoid the generic AI-site look: excessive gradients, random glassmorphism, neon glows, oversized pill cards everywhere, decorative blobs with no role, identical feature-card grids, arbitrary bento layouts, and gratuitous animation.
- Use visual hierarchy deliberately.
- Use whitespace, typography, contrast, imagery, and composition before adding decorative effects.
- Do not copy reference sites. Extract principles and synthesize a distinct result.
- Reuse genuine brand/product assets before generating replacements.

## Responsive and accessibility
- Treat mobile as a first-class experience, not a final patch.
- Verify hero, navigation, CTAs, typography, cards, forms, galleries, sticky elements, checkout/signup paths, tap targets, spacing, and horizontal overflow.
- Use semantic HTML and meaningful landmarks.
- Maintain readable contrast and focus states.
- Ensure keyboard-accessible interactions.
- Give informative images useful alt text.
- Respect reduced-motion preferences.
- Do not use color alone to communicate state.

## Frontend engineering
- Prefer TypeScript with strict typing.
- Avoid unnecessary any; validate external data at boundaries.
- Prefer simple reusable components over giant page components or premature abstraction.
- Reuse existing project patterns when they are sound.
- Avoid unnecessary dependencies.
- Keep changes focused and reversible.
- For existing projects, inspect the current stack before introducing new patterns.
- Use Tailwind/shadcn conventions when the project already uses them.

## Performance
- Optimize for fast perceived and actual load.
- Keep media appropriately sized and compressed.
- Lazy-load non-critical media when appropriate.
- Avoid large client-side libraries for trivial effects.
- Prevent layout shifts by reserving media dimensions.
- Treat Core Web Vitals as constraints, not afterthoughts.

## Motion
- Motion should clarify hierarchy, state, feedback, or perceived quality.
- Prefer subtle purposeful transitions.
- Avoid animation simply to make a site feel expensive.
- Respect reduced motion.

## SEO and discoverability
- Use one clear page intent.
- Create useful titles, descriptions, headings, internal links, and structured content.
- Do not generate thin pages at scale.
- For local businesses, represent genuine locations/services with unique useful content.
- Add structured data only when it accurately reflects visible content.
- Make important entities, products, services, pricing, FAQs, and proof easy for both search engines and AI systems to understand.

## Ecommerce
- Prioritize product clarity, value perception, proof, objections, variant/pack clarity, delivery/returns confidence, mobile buying experience, cart friction, and repeat purchase opportunities.
- Product galleries must show the real product clearly.
- Important purchase information must appear before excessive storytelling.
- Do not use fake countdowns, fake low-stock messages, or fabricated reviews.

## SaaS
- Communicate the promise quickly.
- Show the product, not only abstract visuals.
- Explain use cases and the path to value.
- Reduce signup friction.
- Make pricing/packaging understandable.
- Design onboarding around the first meaningful outcome.

## Analytics and experimentation
- Define the primary conversion and supporting funnel events.
- Do not claim tracking works without verifying events.
- Use A/B testing only with a real hypothesis and enough traffic to learn something.
- Never invent analytics results.

## Testing and completion
Before declaring meaningful work complete, verify what is proportionate to the change:
- build/type checks
- console errors
- key links and navigation
- forms
- responsive behavior
- major interactions
- signup/checkout/contact flow when applicable
- accessibility basics
- visual consistency
- performance-sensitive areas

Never claim success merely because code was generated.

## External actions and cost safety
- Do not publish, deploy, send messages, purchase anything, run paid ads, spend credits, or trigger paid generation unless explicitly authorized.
- Before paid image/video generation, state the best available cost estimate and get approval.
- Prefer the cheapest method that can realistically meet the required quality unless maximum quality is explicitly requested.

## Communication
- Be concise and decision-oriented.
- Surface blockers immediately.
- Do not ask unnecessary questions.
- When enough information exists, continue autonomously instead of repeatedly asking for permission.
