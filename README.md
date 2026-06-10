# Road to Senior Dev <img width="49" height="64" alt="image" src="https://github.com/user-attachments/assets/fdbe1e4c-635e-45a0-80b9-2c93642c4849" />


This repository is a personal laboratory containing a series of progressive coding challenges. I am building these projects to drastically improve my architectural and backend engineering skills. 

My ultimate goal is to master complex, real-world system designs, transitioning from basic applications to highly scalable, resilient systems. I will be one of the greatest builders in the world :)

---

## Core Focus Areas
Every advanced exercise in this repository is designed to eventually incorporate the following real-world scenarios:
* **Web Services:** Building robust APIs with multiple endpoints and proper layer separation.
* **Database & Caching:** Mastering RDBMS (PostgreSQL) and Redis for high performance.
* **Concurrency:** Solving data integrity issues and Race Condition challenges under heavy load.
* **Asynchronous Processing:** Offloading heavy tasks to background workers using message queues.
* **Extreme Testing:** Ensuring reliability through rigid Unit Tests and real-world Integration Tests (using Testcontainers).

---

##  The Progression Matrix
To avoid being overwhelmed, I am tackling problems through a structured, 5-level progression system. 

### Level 1: Core Go & In-Memory APIs
* **What I expect to master:** HTTP routing, package structuring, interfaces, dependency injection, and pure Unit Testing using the standard `testing` package.
* **Scope:** No external databases. Data is handled in memory. 

### Level 2: Persistence & Integration Testing
* **What I expect to master:** Connecting Go to a relational database, executing SQL queries safely, managing migrations, and writing true Integration Tests.
* **Scope:** Introduction of PostgreSQL and `testcontainers-go` to spin up ephemeral databases during tests.

### Level 3: Concurrency & Race Conditions
* **What I expect to master:** Identifying and fixing data races under high concurrent traffic. Using `go test -race`, SQL transactions, isolation levels, and locking strategies (optimistic/pessimistic).
* **Scope:** Using Goroutines to write load-testing scripts that bombard the API to break it, then fixing the bottlenecks.

### Level 4: Asynchronous Processing & Queues
* **What I expect to master:** Decoupling the API response from data processing. Implementing Write-Behind caches, background workers, and Goroutine lifecycle management.
* **Scope:** Introduction of Redis. The API pushes jobs to a Redis queue and returns immediately, while async workers process the queue and update the Database.

### Level 5: Resilience (The Boss Level)
* **What I expect to master:** Making the system indestructible. Handling network failures, dead workers, and system restarts without losing data.
* **Scope:** Implementing Exponential Backoff retries, Dead Letter Queues, Circuit Breakers, and Graceful Shutdowns.

---

<img width="128" height="128" alt="image" src="https://github.com/user-attachments/assets/8ca12693-6da9-4be7-8e0c-5d93a61f269d" />

## 🤖 The AI Mentor Prompt Pattern
I use the following prompt with an LLM to generate custom, progressive challenges based on my current level. 

> **Role:** You are a Senior Backend Engineer mentoring me with practical coding challenges to improve my Go and system design skills.
> 
> **My Goal:** Build robust, scalable, and testable web services mastering Go, SQL Databases, Concurrency (Race Conditions), Redis, and Async processing.
> 
> **My Current State:**
> - Desired Progression Level: [e.g., Level 1: Core Go & In-Memory APIs]
> - Previously completed problems: [List what you've done to avoid repetition]
> 
> **Challenge Rules:**
> 1. DO NOT WRITE THE SOLUTION CODE. Only provide the requirements.
> 2. Strictly limit the scope to my "Desired Progression Level". Do not add Redis or Async if I am at Level 1 or 2.
> 3. Provide a realistic context (e.g., e-commerce, fintech, social network).
> 4. Specify exactly what and how I need to test.
> 
> **Required Output Format:**
> - **Scenario:** Real-world problem description.
> - **Technical Requirements:** Endpoints and stack to use.
> - **Learning Focus:** The core Go or architectural concept this targets.
> - **Testing Requirements:** Specific unit/integration tests to write.
> - **Edge Cases / Traps:** A hint about potential bugs (e.g., race conditions, concurrent writes) to watch out for.
