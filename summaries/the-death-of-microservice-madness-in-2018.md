# The Death of Microservice Madness in 2018

**Source:** https://www.dwmkerr.com/the-death-of-microservice-madness-in-2018/
**Section:** Architecture

---

## Key Insights

- Microservices create 3x complexity explosion: developers must run multiple services locally, operators manage hundreds vs. few services, devops teams need container orchestration expertise
- Poor boundary definition kills independence: services that look separate on paper often have hidden dependencies, requiring coordinated deployments of service groups
- State management destroys stateless benefits: schema changes in databases affect multiple services simultaneously, forcing synchronized rollouts and rollback cascades
- Communication complexity scales exponentially: network calls multiply failure points, requiring retry logic and asynchronous patterns that reintroduce distributed state problems
- Versioning becomes dependency hell: tracking which service versions work together becomes unmanageable, similar to node modules conflicts but with live services
- Distributed transactions are painful: ACID properties across microservices require complex orchestration or accepting eventual consistency
- Orchestration platforms are monoliths in disguise: Kubernetes clusters become single points of failure requiring their own complex management
- Networking complexity follows Tesler's Law: virtual networking, load balancing, and DNS complexity gets hidden but resurfaces during runtime issues

**Decision Framework Questions:**
- Can your team actually operate distributed systems?
- Are your domain boundaries truly independent?
- Do you need distributed transactions?
- Can you handle eventual consistency?
- Do you have container orchestration expertise?

## Bottom Line

Microservices trade development complexity for operational complexity - only worth it if you have serious distributed systems expertise and truly independent domain boundaries.