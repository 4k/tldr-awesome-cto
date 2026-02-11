# Testing in Production, the safe way

**Source:** https://medium.com/@copyconstruct/testing-in-production-the-safe-way-18ca102d0ef1
**Section:** Development process

---

## Key Insights

**Three Phases of Production**
- **Deploy**: Code runs in production but serves no user traffic. Enables zero-risk installation and testing against real production environment
- **Release**: Traffic gradually shifts to new version via canaries, monitoring error rates/latency for automated rollback
- **Post-release**: Live system verification through feature flags, A/B tests, chaos engineering

**Deploy Phase Testing**
- Integration testing in production using service discovery tags to isolate deployed vs released versions
- Test against production databases with whitelisted test accounts or mark test data with metadata flags
- **Shadowing**: Replay 100% production traffic against new service in fire-and-forget mode (works best for stateless services)
- **Tap-compare**: Run requests against both old/new versions, compare responses for correctness
- Load testing via traffic shifting - redirect production traffic to smaller clusters to find capacity limits

**Release Phase Practices**
- Monitor only 3-7 core metrics: error rate, request rate, latency (99th percentile)
- Automated canary rollback based on baseline comparison thresholds
- Traffic shaping: gradually shift from 1% → 100% production traffic over weeks

**Service Mesh Benefits**
- Sidecar proxies can inject test headers (X-ServiceB-Test) to signal upstream services
- Enables network-level contract testing without code changes

**Configuration Testing**
- Treat config pushes with same rigor as code deploys
- Use sticky canaries: deploy config to 1% users hitting small server subset first
- Static validation + programmatic checks for config files

**Chaos Engineering Prerequisites**
- Requires operational sophistication and established resilience baseline
- Treat as scientific discipline with precise experiments to identify hidden vulnerabilities

## Bottom Line
Testing in production requires fundamental system design changes but enables verification against real traffic patterns and environment conditions that staging environments cannot replicate.