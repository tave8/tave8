# Giuseppe Tavella

I'm a backend developer building ZeroChiamate, a CRM SaaS for service businesses.

*I write code that humans have pleasure to read*. I love designing systems. 

Some examples:
- [Background Job System](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/infrastructure/jobs/job_library/JobManager.java) 
- [Forgot Password System](https://github.com/tave8/operavion-crm-backend/blob/main/src/main/java/giuseppetavella/zero_chiamate/domain/business/auth/ForgotPasswordService.java)


Check out examples of my system design, code style:

, something like:

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
...
```

That was from my Background Job System.

Or from my Forgot Password System: 

```java
@Transactional
public void verifyAuthorizationCodeWhenClick(UUID codeId) 
{

    try {
        
        // the code must exist
        ForgotPasswordCode code = this.findById(codeId);
        
        // the code must be non-expired
        this.requireNotExpiredCode(code, SET_PASSWORD_TTL);
        
        // the code must be usable 
        this.requireUsableCode(code);
        
        // the code must be not clicked
        this.requireNotClickedCode(code);
        
        // the code must belong to a user that exists
        User owner = this.usersService.findById(code.getUser().getId());
        
        // the code must belong to a user with verified email
        this.requireVerifiedEmail(owner);
        
        // ALL CONTROLS PASSED ********
        
        // mark code as clicked
        this.forgotPasswordRepository.markCodeAsClicked(code);
        
        // mark all other codes of this owner as unusable,
        // except this code
        this.forgotPasswordRepository.markAllCodesAsUnusableExcept(owner, code);
...
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
