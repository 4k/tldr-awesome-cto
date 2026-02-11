# 10 Modern Software Over-Engineering Mistakes

**Source:** https://medium.com/@rdsubhas/10-modern-software-engineering-mistakes-bc67fbef4fc8
**Section:** Architecture

---

## Key Insights

**Business Reality**
- Business requirements only diverge, never converge - in 15 years, author has never seen requirements stabilize
- Plan for 100 things, business will demand the 101st; solve 1,000 problems, they'll create 10,000 more

**Architecture Patterns**
- Vertically split business functionality before horizontal splitting - isolate actions rather than combining them
- Example: User profile system started as shared CRUD, ended with 13 different signup flows with no meaningful shared logic
- Duplication is better than wrong abstraction - only expose shared abstractions after seeing multiple similar use cases

**Anti-Patterns to Avoid**
- Generic everything: Generic Adapters, Query builders, Request handlers, etc. - perfect abstractions come with expiry dates
- Shallow wrappers: 1:1 library mirrors that require changes everywhere when underlying library changes
- Sandwich layers: Splitting cohesive actions into 10-20 meaningless layers for "testability"
- Tool-like quality application: Making everything "private final" or interfaces for all classes doesn't improve code

**Specific Examples**
- Enterprise FizzBuzz follows SOLID principles perfectly but takes gazillions of lines to print "Fizz Buzz"
- CMS built for "extensibility" - business people never used it, always needed developers anyway
- Magic database configurability file failed when client wanted to switch only half the models

**Estimation Impact**
- Bad estimation destroys quality before code is written - smart developers overestimate capability and take ugly shortcuts

**System Health**
- Healthy systems churn constantly - areas without commits for long periods are code smells
- Refactoring must be part of every story, no code is untouchable

## Bottom Line
Business requirements always diverge and perfect abstractions expire, so prioritize code that's easy to delete over code that's easy to extend.