I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

Although I prefer working with Java and SQL, I'm also proficient in Python, TypeScript and PHP.

Ambiguity and high-ownership is how I function best.

---

## Things I've built and how I think

**A CRM reusable core**. A CRM isn't one feature — it's fifty features that need to compose. I designed ZeroChiamate's architecture so each new domain (billing, scheduling, geocoding, file storage, AI) slots in without touching what already works. The backend follows a strict package-by-feature layout with layered responsibilities: domain logic never leaks into infrastructure, integrations are swappable behind interfaces, and external services are isolated so the core doesn't know — or care — whether you're using Stripe, Resend, or Geoapify. [I designed the email layer so it doesn't know either](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/email/EmailService.java). The backend doesn't know where `/dashboard` lives on the frontend — [so I made it not care](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/config/FrontendRoutes.java). On the frontend, calling APIs directly from components works until it doesn't — [I built an abstraction layer](https://github.com/tave8/operavion-crm-frontend/blob/main/src/js/api/APIHelper.ts). Built solo, from scratch. 

**Appointments**. I wrote the internal agenda system in raw PHP and SQL — no frameworks — for a company with 120+ employees. It replaced Google Calendar + Excel. To quote them: "it was a mess." What makes me proud isn't the adoption — it's the dependency. Any incorrect logic would immediately affect the whole company and cause serious trouble with clients. That has never happened. I enjoy these responsibilities. It's where I give my best. Since then I've been fascinated with time-related algorithms, which years later led me to formalize aspects of this problem into a spec.

**Stats for CEO**. Responsible for the numbers a CEO looks at first thing in the morning to assess how the company is going and what decisions to take. I worked directly with sales, invoices, earnings, salaries, employee commissions — grouped by month, week, region, and custom metrics. My day was translating requirements like _"cross-reference the N invoice confirmations for each customer in the given month, only if the confirmation type was X, only if the customer met condition Y"_ into logically robust SQL. Months went by. No complaints about reliability, despite data scrutinized daily by the CEO. We can interpret that as _it just works_.

**Background jobs**. I was fed up having to learn a new framework for background jobs, so [I made my own](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/jobs/job_library/JobManager.java).

**Forgot password**. I have a natural skepticism towards abstractions — either I build my own, or I'll go deep into the bowels of the one I'm using. I designed a forgot password security system where the code reads like plain English. [See for yourself](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/business/auth/ForgotPasswordService.java).

**Algorithms**. Original solutions to classical problems. Matrix traversal looks complex. [Zigzag in 3 lines](https://github.com/tave8/matrix-traverser-python/blob/main/examples/zigzag_pattern.py). Find the exit of a maze where each cell's value must be strictly increasing, with N candidate cells at each step? [Still 3 lines](https://github.com/tave8/matrix-traverser-python/blob/main/examples/incremental_path_maze.py). Same [Matrix Traversal Engine](https://github.com/tave8/matrix-traverser-python/blob/main/src/core/MatrixTraverser.py). Verifying a palindrome linked list with one recursive function, no pre-computations, no extra passes — [recursion gives you the future for free](https://github.com/tave8/algorithms/tree/main/linked_list_palindrome_recursion), if you know how to freeze the present. Finding all nodes at distance K from a target in a binary tree: the trick isn't going down. [How I traversed unique nodes exactly once](https://github.com/tave8/algorithms/tree/main/find_nodes_distance_k).

**Access control**. I designed an access control system letting admins control every page of the CRM from a single central panel — enable or disable access to pages or portions of pages, per role, with one click. The ease of use reflects how much I care about UX.

**Personality**. What does it tell you about an individual that teaches themselves German from scratch — 1 hour a day, every day for 8 months, self-designed plan, 0 to fluent? I like doing the harder things. (I speak 6 languages.)

---

## What I'm building

**ZeroChiamate CRM** — built solo, from scratch.

Java + Spring Boot backend, React + TypeScript frontend, PostgreSQL,
deployed on Cloudflare Pages and Railway.

Some things I built that I'm proud of:
- AI-powered contract discrepancy detection using Anthropic's API
- Stripe billing — subscriptions, trials, webhooks, full lifecycle
- Schema migrations across 3 environments with Flyway

---

## Work experience

Backend developer at Italia Lavoro — built the invoicing and agenda systems.
My SQL financial analysis algorithms are used by the company's administration
for sales, salaries, employee performance and regional expansion analysis.

---

## Stack

Java · Spring Boot · PostgreSQL
React · TypeScript · JavaScript · Bootstrap · HTML · CSS
Python · PHP

---

## Languages

Italian (native) · English (fluent) · German (fluent)
Spanish · French · Romanian

---

## Links
- GitHub: github.com/tave8
- ZeroChiamate: https://zerochiamate.com
