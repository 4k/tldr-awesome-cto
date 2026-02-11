# Technology Due Diligence Checklist

**Source:** https://akfpartners.com/growth-blog/technical-due-diligence-checklists
**Section:** Due Diligence

---

## Key Insights

**AI/ML Evaluation Framework:**
- Assess AI/ML strategy alignment with product goals and vendor lock-in risks
- Verify standardized model lifecycle from experimentation to deployment
- Check for bias/fairness evaluation, performance monitoring, and ethical risk management
- Evaluate model explainability, LLM grounding in verifiable data, and customer feedback adaptation

**AKF Scale Cube Assessment:**
- X-Axis: Load balancing, session state separation, read/write database split, object caching, CDN usage
- Y-Axis: Service separation (login, signup, checkout), data sharding per service, appropriate service sizing
- Z-Axis: Data subset dedication, multi-tenant handling, data residency compliance

**Critical Fault Isolation Checks:**
- Only asynchronous cross-service calls allowed
- Identify single points of failure (SPOFs)
- Multi-datacenter disaster recovery implementation
- Data tier resilience to corruption and unavailability

**Development Process Benchmarks:**
- Automated test coverage >75%
- Unit test code coverage tracking
- Small, frequent deployments vs. large payloads
- Dedicated tech debt percentage per sprint
- Feature flag implementation for rollback capability

**Operations Monitoring Requirements:**
- Centralized, searchable logging with access controls
- Customer experience metrics for problem detection
- Synthetic monitors on key transaction flows
- Real-time alerting to appropriate owners
- Postmortem processes with assigned completion tracking

**Security Baseline:**
- Multi-factor authentication for critical systems
- Quarterly network vulnerability scans, annual penetration tests
- Encryption for sensitive data in transit/rest/use
- Separate dev/test/production environments
- Source code access restricted to job requirements only

## Bottom Line
This comprehensive 100+ point checklist covers AI/ML strategy through security fundamentals, providing a systematic framework for evaluating technology scalability, fault tolerance, and operational maturity during due diligence.