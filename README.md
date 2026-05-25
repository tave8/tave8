# Giuseppe Tavella

I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

I own the full stack.

*I write code that humans have pleasure to read*. I love designing systems and abstractions that make life easier. 

I'm a problem-solver:
- Background jobs are harder than they look. [I built the whole system from scratch](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/jobs/job_library/JobManager.java) — scheduler, lifecycle, retries, the works.
- Forgot password sounds simple until you think about it for five minutes. [I thought about it for longer](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/business/auth/ForgotPasswordService.java).
- "Is this time slot available?" is a deceptively hard question. [I wrote a spec](https://github.com/tave8/availability-algorithm).
- State transitions are easy to get wrong and painful to debug. [I made it impossible to get wrong](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/helpers/StateTransitionHelper.java).
- Matrix traversal looks complex. [Zigzag in 3 lines says otherwise](https://github.com/tave8/matrix-traverser-python/blob/main/examples/zigzag_pattern.py).
- Typewriting effect looks like magic. [It isn't](https://github.com/tave8/typewriter). [Demo](https://typewriter-green.vercel.app).
- Calling APIs directly from components works until it doesn't. [I built an abstraction layer](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/APIHelper.ts). [Here's how I use it](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/AuthAPI.ts).
- Backend shouldn't know where `/dashboard` lives on the frontend. [So I made it not care](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/config/FrontendRoutes.java). The controller just calls `frontendRoutes.emailVerificationSuccess()` and moves on. [See it in action](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/api/controllers/auth/VerifyEmailController.java).


*Give me a challenge, not a task* - is how I live my work life.

## What I'm building

**ZeroChiamate CRM** — built solo, from scratch.

Java + Spring Boot backend, React + TypeScript frontend, PostgreSQL, 
deployed on Cloudflare Pages and Railway.

Some things I built that I'm proud of:
- A background job system from scratch — scheduler, manager, executor pattern
- AI-powered contract discrepancy detection using Anthropic's API
- Stripe billing — subscriptions, trials, webhooks, full lifecycle
- Shift conflict detection using interval overlap algorithms
- Schema migrations across 3 environments with Flyway
- Algorithm to solve matrix and maze traversal problems

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
