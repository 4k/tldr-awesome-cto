# Trunk Based Development

**Source:** https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development
**Section:** Development process

---

## Key Insights

- **Core practice**: Developers merge small, frequent updates to main branch (trunk) rather than long-lived feature branches
- **Required for CI/CD**: Trunk-based development is mandatory for true continuous integration - automated builds/tests can't work effectively with isolated, lengthy feature branches
- **Daily merge requirement**: High-performing teams merge branches to trunk at least once daily to maintain release cadence
- **3-branch rule**: Keep maximum of 3 active branches in repository; delete branches immediately after merging
- **Small batch commits**: Keep changes to few lines of code/commits to minimize cognitive overhead and enable rapid decision-making
- **Feature flags over branches**: Wrap new features in inactive code paths on main branch rather than creating separate feature branches
- **Automated testing stack**: Unit/integration tests run on merge; full end-to-end tests run in later pipeline stages
- **Immediate code review**: Review code synchronously, not asynchronously - use automated test results as first-pass validation
- **Green trunk assumption**: Main branch must always be stable and deploy-ready at any commit
- **Build optimization**: Use caching layers and optimized test stubs to maintain fast execution times
- **Eliminates code freezes**: Properly implemented trunk-based development removes need for planned integration phases

## Bottom Line
Trunk-based development enables high-performing teams to deploy daily by forcing small, frequent merges with automated testing, while traditional long-lived branches create integration complexity that breaks CI/CD.