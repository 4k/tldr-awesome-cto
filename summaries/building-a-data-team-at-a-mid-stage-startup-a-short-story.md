# Building a data team at a mid-stage startup: a short story

**Source:** https://erikbern.com/2021/07/07/the-data-team-a-short-story.html
**Section:** Data

---

## Key Insights

**Organizational Structure:**
- Embed data scientists into specific functional teams (marketing, product, supply chain) with centralized management but decentralized backlog
- Avoid central bottleneck by giving teams dedicated data resources while maintaining unified reporting structure
- Data scientists reporting to business leaders creates misalignment; they need managers who understand data

**Quick Wins Strategy:**
- Start with crude data warehouse (dump production tables hourly) to get all data in one place fast
- Open SQL access to business teams with basic training - eliminates "English-to-SQL translator" bottleneck  
- Focus on "data journalists" who find business insights over ML researchers initially
- Build demos/prototypes (like Flask app) to make ML work tangible for product teams

**Common Mid-Stage Startup Problems:**
- Fragmented data across systems, poor instrumentation
- Data scientists doing R&D with no clear business goals
- Product teams celebrating shipping over measurable outcomes
- Business analysts building "shadow tech debt" (500-line SQL queries, complex spreadsheets)
- Teams hiring around dysfunctional data org

**Success Metrics:**
- CEO pushing for data-driven decisions from top
- Product managers justifying projects with test results/data insights
- Teams tracking end-to-end metrics (customer acquisition cost vs cost-per-click)
- Failed experiments generating learnings, not blame

**Hiring Profile:**
- Emphasize software skills + business empathy over AI/ML credentials
- Look for generalists who can build practical solutions

## Bottom Line

Transform from isolated ML research team to embedded business partners by centralizing data infrastructure fast, embedding data scientists in functional teams, and focusing on practical insights over sophisticated models until the organization becomes truly data-native.