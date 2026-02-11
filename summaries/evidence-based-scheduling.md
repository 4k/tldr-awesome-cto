# Evidence Based Scheduling

**Source:** https://www.joelonsoftware.com/2007/10/26/evidence-based-scheduling/
**Section:** Project management

---

## Key Insights

**Core EBS Method:**
- Break tasks into 16-hour maximum chunks to force detailed design thinking
- Track actual time vs. estimates to calculate "velocity" (estimate/actual) for each developer
- Use Monte Carlo simulation with historical velocities to generate probability curves, not single dates
- Run 100+ scenarios using randomly selected velocities from each developer's history

**Velocity Patterns:**
- Perfect estimator: {1, 1, 1, 1...} - mythical
- Bad estimator: {0.1, 0.5, 1.7, 13.0...} - creates wide probability curves
- Common estimator: {0.6, 0.5, 0.6, 0.7...} - consistent underestimation, narrow curves

**Interruption Handling:**
- Don't track interruptions separately - just keep clock running on original task
- EBS automatically accounts for unpredictable delays through velocity history
- Produces correct schedules regardless of tracking method

**Project Management Rules:**
- Only programmers doing the work create estimates
- Charge bug fixes to original task time
- Never let managers pressure for shorter estimates
- Schedule = box of blocks: get bigger box or remove blocks, can't shrink blocks
- Build buffer for: new features, competition response, integration, debugging, usability testing, beta

**Feature Prioritization:**
- Forced cuts due to realistic schedules eliminate low-value features
- Without schedules, developers do easy/fun features first, important ones get delayed
- Excel 5 example: "deferred" features were actually worthless upon later review

## Bottom Line

Evidence-Based Scheduling uses historical velocity data and Monte Carlo simulation to generate realistic probability curves for ship dates, forcing better feature prioritization and preventing the chronic optimism that destroys software schedules.