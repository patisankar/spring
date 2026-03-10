Senior Java / Spring Boot Engineer Interview
========
- How does auto-config works in spring boot?

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
Let’s break it down in the way interviewers expect 👇

🔹 1️⃣ HashMap stores data in key–value pairs
But internally, it uses an array of buckets.

🔹 2️⃣ When you put(key, value):

* The hashCode() of the key is calculated
* That hash is converted into an index
* The value is stored in that bucket on the calculated index

🔹 3️⃣ What if two keys get the same index? (Collision)
This is where many candidates struggle.

Before Java 8 → LinkedList was used.
After Java 8 → If collisions exceed a threshold, it converts into a Balanced Tree (Red-Black Tree) for better performance.

🔹 4️⃣ Why is HashMap fast?
Average time complexity:
O(1) for get() and put()

But in worst case (many collisions), it can go to O(log n).

🔹 5️⃣ Important Interview Points Most People Forget:

* HashMap is NOT synchronized
* It allows one null key and multiple null values
* Performance depends on proper hashCode() and equals() implementation

💡 Interview Tip:
If you explain collisions + Java 8 tree optimization clearly, you instantly stand out from average candidates.

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


