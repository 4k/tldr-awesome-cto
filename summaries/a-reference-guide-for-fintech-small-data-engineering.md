# A reference guide for fintech & small-data engineering

**Source:** https://medium.com/dangerous-engineering/a-reference-guide-for-fintech-small-data-engineering-bd65b9796d90
**Section:** Data

---

## Key Insights

**Three Engineering Levels:**
- Code level: Individual methods/functions (features made here)
- Application level: Whole applications with complex business logic (products made here)  
- System level: Multiple applications across environments (companies made here)

**System-Level Work Rules:**
- Only two permitted activities: bring system in line with design OR design replacement system
- Everything else is busywork
- Senior engineers are primarily engineering designers, not just implementors

**Small-Data Company Characteristics:**
- Production dataset <1TB (fits on two iPhones)
- Focus domain model correctness over computational efficiency
- Encrypt data by default everywhere except product memory
- Separate data by sensitivity (PHI, PII, PCI)

**Technology Selection Rule:**
"If a problem is unique to your product offering then you may invent an appropriate solution. Otherwise go with an industry standard approach — and only use one approach at a time."

**Five-Stage Migration Process:**
1. Design v2 and path to get there
2. Fix v1 (most teams skip this)
3. Implement v2
4. Migrate v1→v2 in atomic steps
5. Delete v1 (most teams skip this)

**Security Principle:**
Simplicity, correctness, security, scalability, and maintainability are neighbors - when far from one, you're far from all.

**Service Extraction:**
- Extract verbs, not nouns
- Cannot extract "User" service - extract "UserApproval" operations instead
- Fix data dependencies first before extracting

**Investment Model Balance:**
- Startup: 100% value creation
- Product-market fit: Lose 1 year value creation to gain 1 year cost reduction
- Ecological dominance phase: Nearly 100% cost reduction until massive moat built

**Engineering Standards:**
- Never do work below your best quality
- Put maximum effort into naming
- No TODOs without tracked tickets
- Never fix bugs without fixing underlying design flaw
- Make data migrations as freely as code changes

## Bottom Line
Small-data companies with complex domains need engineers focused on system-level design and domain modeling correctness rather than computational efficiency, with security and simplicity as the primary architectural constraints.