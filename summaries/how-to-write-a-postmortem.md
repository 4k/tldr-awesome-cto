# How to Write a Postmortem

**Source:** https://web.archive.org/web/20210618014202/https://blog.serverdensity.com/how-to-write-a-postmortem/
**Section:** Development process

---

## Key Insights

**Timing & Process**
- Wait 1 week between incident resolution and full postmortem publication to rule out follow-up incidents and gather all stakeholder input
- Publish short status updates during crisis at regular intervals, even if just "still investigating"
- Start with internal Jira incident page, then filter security details for public status page

**Content Structure Requirements**
- Root cause analysis (may trace back months before outage)
- Timeline of identification/isolation steps and duration
- Impact scope (who/what services affected)
- Resolution steps taken
- Lessons learned with specific process/product/strategy changes

**Ownership Model**
- Status updates: whoever leads incident response or is on-call (ops/support)
- Internal postmortem draft: same incident responders
- Public postmortem: CEO publishes after internal review complete

**Focus Management**
- Use postmortems to shift from "urgent/important" (outage response) back to "important/not urgent" work
- Prevents getting stuck in reactive quadrants 3-4 of Eisenhower Matrix

**Transparency Benefits**
- Over-communication restores customer confidence
- Public accountability creates incentives to fix problems
- Demonstrates investment and care to technical audiences

## Bottom Line
Wait a week post-incident, have responders draft internally with CEO publishing publicly, and treat postmortems as mandatory learning tools that shift focus from reactive firefighting back to strategic work.