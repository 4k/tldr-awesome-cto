# Microservices – Please, don’t

**Source:** https://riak.com/posts/technical/microservices-please-dont/
**Section:** Architecture

---

## Key Insights

- **Domain understanding is prerequisite**: Only consider microservices when you deeply understand your domain boundaries, dependencies, and request workflows. If still figuring out the domain, microservices cause more harm than good.

- **Network calls are slower than in-process**: Performance gains from microservices are often due to new language/tech stack, not the architecture. Network latency always exceeds co-resident code calls.

- **Start with internal service modules**: Build cleanly defined modules in monolithic code first, then extract to separate services only when true need arises over time.

- **Distributed transactions add complexity**: Cross-service data operations require handling multiple failure modes (application + network level) and coordinating recovery strategies for each.

- **Scaling works equally for monoliths**: You can create logical clusters of monolithic apps (API servers, dashboards, background jobs) and scale them independently - same benefit as microservices.

- **Local development overhead**: Running multiple services locally requires maintaining Docker configs and complex test setups as the system grows.

- **Team coordination friction**: Bugs spanning services require multiple team synchronization. Engineers in isolated codebases develop "not my problem" syndrome vs. shared codebase collaboration.

- **Monitoring becomes critical**: Need comprehensive data across all services to debug performance issues and errors in distributed systems.

- **Business value justification required**: Delaying revenue-generating features for architectural changes needs clear ROI demonstration to business stakeholders.

## Bottom Line

Microservices solve organizational problems, not technical ones - start with well-designed internal service modules in a monolith and only extract when you have deep domain knowledge and demonstrable business need.