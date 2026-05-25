# Giuseppe Tavella

I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

*I write code that humans have pleasure to read* - machines already know how.

```java
private int processNextItems(JobName jobName, JobExecutor<?> executor) {
    
    int countNextItems = 0;
    
    JobExecutionItem<?> nextItem = executor.getNextItem();

    // if there's no next item to process, we stop the entire job
    while(nextItem != null) {

        // ********************
        // ADD NEW JOB EXECUTION WITH INCOMPLETE STATE
        // ********************

        // add a job execution to the DB, before 
        // processing this item
        JobExecution currentJobExecution = this.jobExecutionService.addNewJobExecution(
                jobName,
                nextItem.getItemId()
        );
        
        // holds the exception itself, 
        // if any was raised during processing
        RuntimeException errorDuringProcessing = null;
```

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
