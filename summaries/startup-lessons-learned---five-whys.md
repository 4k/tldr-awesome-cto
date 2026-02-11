# Startup Lessons Learned - Five Whys

**Source:** http://www.startuplessonslearned.com/2008/11/five-whys.html
**Section:** Development process

---

## Key Insights
- Five Whys process: For each problem, ask "why" 5 times to reach root cause, then implement proportional fixes at each level
- Most technical problems trace back to human/process issues - bias toward technical solutions misses real causes
- Start with one team, one problem class, assign a "Five Whys master" to run post-mortems with all involved parties
- Email analysis company-wide in plain English - forces clear thinking and builds organizational learning
- Make investments proportional to problem severity - don't over-invest in small issues or under-invest in major ones
- Pareto principle built-in: recurring problems automatically focus effort on the 20% causing 80% of waste
- IMVU's 5-layer defense system evolved incrementally through Five Whys:
  - Individual sandboxes mimicking production
  - Comprehensive test suite with TDD
  - 100% CI on every checkin
  - Automated incremental deployment with health monitoring
  - Dynamic alerting based on historical patterns vs static thresholds
- Enabled dozens of daily production deployments without significant downtime
- Works with legacy code - team had "tens of thousands of lines" with no test coverage when starting
- Typical outcome: Engineer productivity on day one, investments in previously hard-to-justify improvements

## Bottom Line
Five Whys systematically converts recurring technical crises into incremental process improvements by tracing problems to their human/organizational root causes and making proportional investments in prevention.