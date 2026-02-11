# Database Migrations Done Right

**Source:** https://www.brunton-spall.co.uk/post/2014/05/06/database-migrations-done-right/
**Section:** Data

---

## Key Insights
- Never tie database migrations to application deploys - treat as separate, independent operations
- Break schema changes into 5-step backward-compatible sequence: add nullable column → update app code → migrate data → add constraint → remove null-handling code
- Every database change must be backward compatible with existing system state
- Example: Adding non-null column requires 2 months if deploying weekly/fortnightly vs 2 days if deploying hourly/daily
- Use database migration tools (like DBDeploy) for reliable, repeatable script execution
- Avoid ORMs that inseparably combine schema and code changes
- Small, frequent releases enable faster feedback loops and higher throughput
- Rolling deployments become possible when migrations are decoupled from app deploys
- Pattern works even for greenfield projects due to increased development throughput benefits
- Requires ability to work on small tasks and release changes to production quickly
- Scott Ambler's "Refactoring Databases" provides comprehensive patterns for breaking down changes

## Bottom Line
Decouple database migrations from application deployments by making every schema change backward compatible, enabling faster releases and rolling deployments.