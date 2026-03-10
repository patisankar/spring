Senior Java / Spring Boot Engineer Interview
========
How does auto-config works in spring boot
==========
Spring Boot auto-configuration automatically configures beans based on:

Classpath contents

Existing beans in the context

Application properties

Environment conditions

The goal is:

“Convention over configuration” — configure sensible defaults, allow override when needed.

**Followup question:**

Spring Boot startup can be divided into 7 major phases:

Create SpringApplication

Prepare environment

Create ApplicationContext

Apply initializers

Load bean definitions

Refresh context (core Spring lifecycle)

Execute runners

### Why does @Transactional sometimes “not work”? List 4 real causes.
Self-Invocation
Method Visibility (Private / Protected Methods)
Wrong Exception Type (Rollback Not Triggered)
Called Outside Spring Context 

### What is the difference between:

Filter

Interceptor

AOP advice

### How does Spring manage bean lifecy
[Ref](https://medium.com/@aravindcsebe/understanding-spring-bean-life-cycle-a-complete-guide-91f8ddc3d70e)

### SIngle table  vs join table inheritance?
[Transaction](https://medium.com/@AlexanderObregon/controlling-transaction-boundaries-with-transactional-propagation-and-isolation-explained-976eb35f368)

[Spring batch](https://medium.com/@meet2sudhakar/here-are-the-key-technical-advantages-of-using-the-spring-batch-framework-from-a-developers-7410d795ce60)
### How does Hashmap works
HashMap is implemented as an array of buckets where each bucket stores entries using a linked list, and in JDK 8+, it converts to a red-black tree when collisions exceed a threshold. It uses the key’s hashCode to compute an index using bitwise operations for O(1) average time complexity. It resizes when the load factor exceeds 0.75 and is not thread-safe.

### How do you handle:

Partial failures?

Idempotency?

Retries?

Consistency?

Strategies for Handling Data Consistency


[Retry](https://www.geeksforgeeks.org/system-design/retries-strategies-in-distributed-systems)
[Cosistency](https://www.linkedin.com/pulse/how-handle-data-consistency-microservices-environment-vintageglobal-rei5e/)





[AuthN/AuthZ (OAuth2/JWT/mTLS)](https://medium.com/@SyntaxSageNik/authentication-mechanisms-f58ded267f5c)

Data protection (PII, encryption)

Auditability and non-repudiation

Rate limiting / throttling

Idempotency


