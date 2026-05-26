# Giuseppe Tavella

I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

One of the few remaining developers who still reads text more than emojis... Which is why you'll see no emojis 😉

I'm a problem-solver, and I own the full stack. Think that's impossible?
- Background jobs are harder than they look. [I built the whole system from scratch](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/jobs/job_library/JobManager.java) — scheduler, lifecycle, retries, the works.
- Forgot password sounds simple until you think about it for five minutes. [I thought about it for longer](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/business/auth/ForgotPasswordService.java). [Diagram](https://github.com/tave8/operavion-crm-backend/blob/main/forgot_password.drawio.png).
- "Is this time slot available?" is a deceptively hard question. [I wrote a spec](https://github.com/tave8/availability-algorithm).
- Your code shouldn't know whether you're using Resend, SendGrid, or carrier pigeon. [I designed the email layer so it doesn't](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/email/EmailService.java). [Turns out it was a pigeon](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/integrations/resend/ResendAPIService.java).
- State transitions are easy to get wrong and painful to debug. [I made it impossible to get wrong](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/helpers/StateTransitionHelper.java). Imagine [modeling a billing subscription](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/entities/companies/Company.java#L164C1-L217C6) without it.
- Matrix traversal looks complex. [Zigzag in 3 lines says otherwise](https://github.com/tave8/matrix-traverser-python/blob/main/examples/zigzag_pattern.py).
- Calling APIs directly from components works until it doesn't. [I built an abstraction layer](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/APIHelper.ts). [Here's how I use it](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/AuthAPI.ts).
- Backend shouldn't know where `/dashboard` lives on the frontend. [So I made it not care](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/config/FrontendRoutes.java). The controller just calls `frontendRoutes.emailVerificationSuccess()` and moves on. [See it in action](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/api/controllers/auth/VerifyEmailController.java#L48C3-L59C9). [Frontend re-routes](https://github.com/tave8/operavion-crm-frontend/blob/main/src/components/ShortcutPage.tsx).
- Typewriting effect looks like magic. [It isn't](https://github.com/tave8/typewriter/blob/main/example.js). [Demo](https://typewriter-green.vercel.app).
- Searching while typing fires too many requests. [I built a library that waits until you stop](https://github.com/tave8/typing-delayer/blob/main/dist/script.js). The hard part wasn't the delay — it was making sure `this` points where you expect it in the callback.

*Give me a challenge, not a task* - is how I live my work life.

## What I'm building

**ZeroChiamate CRM** — built solo, from scratch.

Java + Spring Boot backend, React + TypeScript frontend, PostgreSQL, 
deployed on Cloudflare Pages and Railway.

Some things I built that I'm proud of:
- AI-powered contract discrepancy detection using Anthropic's API
- Stripe billing — subscriptions, trials, webhooks, full lifecycle
- Schema migrations across 3 environments with Flyway

## Work experience

Backend developer at Italia Lavoro — built the invoicing and agenda systems.
My SQL financial analysis algorithms are used by the company's administration
for sales, salaries, employee performance and regional expansion analysis.

## Languages

Italian (native) · English (fluent) · German (fluent) 

Plus Spanish, French, Romanian (yep, I'm polyglot, *wusstest du das nicht?*).

## Stack

Java · Spring Boot · PostgreSQL 

React · TypeScript · JavaScript · Bootstrap · HTML · CSS 

I've also worked with Python (algorithms) and PHP (building a CRM)

## Links
- GitHub: github.com/tave8
- ZeroChiamate: [https://zerochiamate.com]
