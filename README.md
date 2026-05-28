# Giuseppe Tavella

I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

How to make me happy? *Give me a challenge, not a task*.

My nature is ***building across the full stack***. I'm not looking for a standard job. I'm looking for early stage startups where I can have ownership and build end to end.

Below you find some problems I solved and how I reason.

## Backend & System design
- Background jobs are harder than they look. [I built the whole system from scratch](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/jobs/job_library/JobManager.java) — scheduler, lifecycle, retries, the works.
- Forgot password sounds simple until you think about it for five minutes. [I thought about it for longer](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/business/auth/ForgotPasswordService.java).
- "Is this time slot available?" is a deceptively hard question. [I wrote a spec](https://github.com/tave8/availability-algorithm).
- Your code shouldn't know whether you're using Resend, SendGrid, or carrier pigeon. [I designed the email layer so it doesn't](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/email/EmailService.java). [Turns out it was a pigeon](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/integrations/resend/ResendAPIService.java).
- Backend shouldn't know where `/dashboard` lives on the frontend. [So I made it not care](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/config/FrontendRoutes.java). The controller just calls `frontendRoutes.emailVerificationSuccess()` and moves on. [See it in action](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/api/controllers/auth/VerifyEmailController.java#L48C3-L59C9). [Frontend re-routes](https://github.com/tave8/operavion-crm-frontend/blob/main/src/components/ShortcutPage.tsx).
- State transitions are easy to get wrong and painful to debug. [I made it impossible to get wrong](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/helpers/StateTransitionHelper.java). Imagine [modeling a billing subscription](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/entities/companies/Company.java#L164C1-L217C6) without it.
- You'll see me design imperfect systems, in the middle of my thinking process. [More system designs](https://github.com/tave8/algorithms/tree/main).
  
## Algorithms 
- Matrix traversal looks complex. [Zigzag in 3 lines says otherwise](https://github.com/tave8/matrix-traverser-python/blob/main/examples/zigzag_pattern.py). Find the exit of a maze where each cell's value must be strictly increasing, with N candidate cells at each step? [Still 3 lines of code](https://github.com/tave8/matrix-traverser-python/blob/main/examples/incremental_path_maze.py). Yep, that's the same [Matrix Traversal Engine](https://github.com/tave8/matrix-traverser-python/blob/main/src/core/MatrixTraverser.py).
- Verifying a palindrome Linked List with recursion sounds straightforward. The catch: one recursive function, no pre-computations, no extra passes. The insight is that [recursion gives you the future for free](https://github.com/tave8/algorithms/tree/main/linked_list_palindrome_recursion) — if you know how to freeze the present.
- Find all nodes at distance K from a target in a binary tree. The trick isn't going down — every developer does that. [How I've traversed unique nodes exactly once](https://github.com/tave8/algorithms/tree/main/find_nodes_distance_k).
  
## Frontend
- Calling APIs directly from components works until it doesn't. [I built an abstraction layer](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/APIHelper.ts). [Here's how I use it](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/AuthAPI.ts).
- Typewriting effect looks like magic. [It isn't](https://github.com/tave8/typewriter/blob/main/example.js). [Demo](https://typewriter-green.vercel.app).
- Searching while typing fires too many requests. [I built a library that waits until you stop](https://github.com/tave8/typing-delayer/blob/main/dist/script.js). The hard part wasn't the delay — it was making sure `this` points where you expect it in the callback.

I'm not looking for a standard junior/mid developer role. I'm looking for early stage startups where I can have ownership and build end to end.


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
