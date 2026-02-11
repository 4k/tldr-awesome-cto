# How I Write Tests

**Source:** https://blog.nelhage.com/2016/12/how-i-test/
**Section:** Architecture

---

## Key Insights

- Work module-at-a-time: Design units testable with minimal dependencies, complete both module and tests before moving to next component
- Avoid manual testing urge: When tempted to run binary by hand, pause and write automated test instead - manual tests only verify current state, automated tests remain valid indefinitely
- Write reusable "fakes": Standalone implementations of component interfaces (e.g., in-memory S3, email outbox) that work across multiple tests vs ad-hoc stubbing
- Design miniformats for test data: Create human-readable textual representations of domain objects/inputs to avoid constructing complex objects in code repeatedly
- Build testing "zoos": Data-driven test harnesses where new test cases = adding data files in familiar format, no additional code (inspired by GCC's `{dg-*}` directive system)
- HTTP proxy example: Pasted entire HTTP requests/responses into files for automated replay testing by stubbing entropy and using standard initial database state
- Regression test everything: Every bug found (even mid-development typos you catch yourself) should become a test to create ratchet effect on bug types
- Testing tools investment: If testing in code is hard/frustrating, build tooling to make it easier - tests are important codebase features

## Bottom Line
Invest heavily in testing infrastructure and treat every bug as a permanent test case to create a ratchet effect that prevents regression while making future testing easier.