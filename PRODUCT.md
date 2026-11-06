# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack
Existing app: React, TypeScript and Tailwind CSS 4 (Vite). Tailwind only, no other UI libraries.

## Users
**Primary:** Contoso Insurance customers who look at their own policies in My Contoso. They want to know where they stand, usually without insurance knowledge, often on a phone.

**Secondary:** Contoso customer service staff. They see the same page when they help a customer on the phone, so the page must work as a shared view that both sides can read out and follow.

## Product Purpose
My Contoso answers one question: "What am I covered for, and what do I pay?" For each policy it shows the cover, the deductible and the premium, plus the total premium per month.

Success: a customer understands their insurance in under a minute, and customer service can answer questions about it without switching systems.

## Positioning
One plain-language page per customer that is both the self-service answer and the screen customer service uses on a call. There is no second system and no separate staff view.

## Operating Context
- Customer-facing web app, designed mobile-first.
- There is no sign-in yet. The demo selects the customer with a query parameter, for example `?customer=C1001`.
- Data is synthetic and comes from `data/policy-admin-export.csv` and `data/coverage-feed.json`.
- Customer service uses the same page, usually while on the phone with the customer.

## Capabilities and Constraints
- Shows each policy's cover, deductible and premium, and the total premium per month.
- **Privacy:** a customer only ever sees their own policies. The browser never receives another customer's data.
- Synthetic data only. Never use real personal data.
- Open decisions: real authentication (none yet) and how the two data sources are reconciled in production.
- The repository may not yet contain the app code or `data/` files; this record describes the product as intended.

## Brand Commitments
- Name: Contoso Insurance; the product is My Contoso.
- Voice: clear, reassuring and honest. Plain language at CEFR B1 level, no insurance jargon. Terms such as "deductible" are explained where they appear.

## Evidence on Hand
- `data/policy-admin-export.csv` and `data/coverage-feed.json`: synthetic policy data.
- No testimonials, customer numbers, benchmarks or press exist. Do not invent them.

## Product Principles
1. **Answer the question first.** What is covered and what it costs comes before everything else.
2. **Plain words.** Say it the way a person would on the phone; explain any term that cannot be avoided.
3. **Honest and reassuring.** Show limits and costs clearly. Reassure with clarity, not with softened facts.
4. **One page for two readers.** The customer and the staff member see the same thing and can follow each other.
5. **Own data only.** Privacy is a product rule, not a feature: data for other customers never reaches the browser.

## Accessibility & Inclusion
WCAG 2.2 AA. Mobile-first, readable and operable by people with no insurance background and by people on assistive technology.

## Workflow
Build path: code-first. Live mode setup is skipped.
