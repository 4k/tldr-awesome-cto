# Design patterns for microservices

**Source:** https://azure.microsoft.com/en-us/blog/design-patterns-for-microservices/
**Section:** Architecture

---

## Key Insights

**Communication Patterns:**
- **Gateway Aggregation**: Combine multiple microservice calls into single request to reduce network chattiness
- **Backends for Frontends**: Create separate backend services per client type (desktop/mobile) to avoid conflicting requirements in single service
- **Gateway Routing**: Use single endpoint to route to multiple microservices, eliminating client endpoint management

**Resilience Patterns:**
- **Bulkhead**: Isolate critical resources (connection pools, memory, CPU) per service to prevent resource starvation and cascading failures
- **Ambassador**: Offload common connectivity tasks (monitoring, logging, routing, TLS) in language-agnostic way

**Migration Patterns:**
- **Anti-corruption Layer**: Implement façade between new and legacy systems to prevent legacy dependencies from limiting new application design
- **Strangler**: Replace legacy functionality incrementally with new services rather than big-bang migration

**Deployment Patterns:**
- **Sidecar**: Deploy helper components as separate containers/processes for isolation and encapsulation
- **Gateway Offloading**: Move shared functionality (SSL certificates) to API gateway instead of duplicating across services

**Implementation Considerations:**
- Each pattern addresses specific microservices challenges while maintaining service autonomy
- Patterns can be combined within single architecture
- Focus on increasing deployment velocity through service decomposition

## Bottom Line
These 9 patterns provide concrete solutions for common microservices challenges around communication, resilience, migration, and deployment while preserving the core benefit of independent service deployment.