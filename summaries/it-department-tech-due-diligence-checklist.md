# IT Department Tech Due Diligence Checklist

**Source:** https://gist.github.com/raphaelbauer/b31d49d91a0af6c1106bfc8ef4bf6d13
**Section:** Due Diligence

---

## Key Insights

**Team Structure & Accountability**
- Cross-functional dev teams with engineering leads managing max 3 teams
- OKRs required at team and individual level, aligned with 3-tier roadmaps (sprint/1yr/3yr)
- Anonymous confidence voting for realistic schedules (Weinberg method)
- Bi-weekly 1-hour cross-team sync meetings mandatory

**Metrics & Performance**
- Track 3 core productivity metrics: lead time, release frequency, mean time to restore (from "Accelerate")
- Monthly team happiness surveys to identify weak spots early
- User interaction tracking as acceptance criteria for all features
- Actively shut down unused/low-usage features

**Knowledge & Risk Management**
- Pre-mortems for projects, post-mortems for failures at all levels
- Documented single points of failure with active mitigation plans
- Quarterly "Love4TheSystems" days for tech debt/updates
- Backup/restore drills for all critical services

**Development Practices**
- Pull requests with 4-eyes principle, minimal scope (no formatting mixed with logic)
- Trunk-based development with feature flags for true continuous delivery
- Tech radar for technology guidance and reduction
- Test pyramid strategy with mandatory tests for all PRs, hotfixes, bugfixes

**Organizational Health**
- Purpose-driven work with clear "why" for all employees
- No single points of failure in teams or knowledge
- Inner source practices to prevent cross-team blocking
- Structured onboarding/offboarding processes

## Bottom Line
Due diligence should focus on measurable team performance metrics, documented processes that eliminate single points of failure, and organizational structures that enable autonomous feature delivery.