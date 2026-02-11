# Evolutionary Database Design

**Source:** https://martinfowler.com/articles/evodb.html
**Section:** Data

---

## Key Insights

**Core Process**
- Each database change must be captured as a migration script with sequential numbering, committed to version control alongside application code
- Never use schema editing tools for production changes - all alterations flow through migration scripts only
- Break large changes into smallest possible migrations - easier to debug, reverse, and compose together
- Track applied migrations via changelog table that migration tools update automatically

**Team Structure**
- DBAs must collaborate directly with developers, not through formal handoffs - sit together, use same communication channels, pair on complex changes
- Every developer gets their own database instance (separate schemas or VMs) to experiment freely without blocking others
- Database environments should be "phoenixes" - regularly destroyed and rebuilt to prevent drift

**Technical Architecture** 
- Database consists of both schema AND data - include standing/reference data and sample test data in version control
- All database changes are refactorings with 3 dimensions: schema change + data migration + application code update
- Use transition phases (views, triggers) for destructive changes in shared databases to support old and new access patterns simultaneously
- Separate all database access into clear layer using data source architectural patterns from P of EAA

**Automation & Integration**
- Developers integrate database changes daily via CI - pull mainline, resolve migration conflicts by renumbering, test, push
- Use tools like Flyway, Liquibase for automated migration application - same scripts run against dev, test, and production
- Migration conflicts resolved by renumbering sequence and testing against clean database
- Prefer real production data extracts over fictional test data from first iteration

**Scale Constraints**
- Proven on projects with 100+ people, 500+ tables, 24/7 uptime requirements
- Not yet solved: thousands of customized deployments, tens/hundreds of schemas per environment

## Bottom Line

Database schema evolution works at scale when every change is captured as a versioned migration script, developers get private database instances, and DBAs collaborate directly rather than gatekeep through formal processes.