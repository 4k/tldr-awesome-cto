# Shrinking microservices to functions

**Source:** https://highscalability.com/blog/2017/3/27/faster-networks-cheaper-messages-microservices-functions-edg.html
**Section:** Architecture

---

## Key Insights

**Network/Messaging Evolution Enables Architectural Shifts:**
- Network speeds increased 25x (1 gbps → 25 gbps) while message formats (Avro, gRPC vs XML) became 100x more efficient
- Combined effect: 100-1000x improvement in inter-service communication efficiency
- This enables breaking monoliths into 100+ microservices within latency bounds

**Five Deployment Evolution Phases:**
- Phase 1: Manual 6-month releases
- Phase 2: Agile 2-week cycles with Chef/Puppet
- Phase 3: Cloud APIs + Blue-Green deploys (immutable infrastructure)
- Phase 4: Container standardization (seconds deployment, predictable components)
- Phase 5: Serverless (100ms deployment, pay-per-100ms usage)

**Serverless Economics:**
- Memory usage drops significantly—unused functions in monoliths/microservices still consume memory
- Hackathon teams built production-ready systems in 12 hours using Lambda
- Rewriting from scratch often faster than migration

**Edge Computing Challenge:**
- Edge violates Lambda's core assumptions: scalable backend services + low latency messaging
- High latency back to datacenter creates architectural tension
- Solution unclear—may require fundamentally different approaches

**Organizational Design (Inverse Conway Maneuver):**
- Structure teams to match desired architecture
- Two Pizza teams with full microservice ownership within single timezone
- High trust within teams, low trust interfaces (APIs/SLAs) between teams
- Scattered global teams produce distributed monoliths

**AWS Lock-in Strategy:**
- Build fast, don't worry about vendor lock-in
- If Lambda app takes 1 week to build, migration also takes ~1 week
- Business logic easily portable, focus on replacement speed over reuse

## Bottom Line
The same technology forces (faster networks + cheaper messaging) that enabled microservices are now enabling functions, with edge computing as the next frontier requiring new architectural paradigms.