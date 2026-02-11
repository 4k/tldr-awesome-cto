# A successful Git branching model

**Source:** https://nvie.com/posts/a-successful-git-branching-model/
**Section:** Development process

---

## Key Insights

**Context-dependent applicability:**
- Git-flow designed for explicitly versioned software requiring multiple version support
- For continuous delivery web apps, use simpler workflows like GitHub flow instead
- Author explicitly warns against treating this as dogma after 10+ years

**Core branch structure:**
- Two infinite lifetime branches: `master` (production-ready) and `develop` (integration)
- Three supporting branch types with limited lifetimes: feature, release, hotfix
- Every commit to `master` = new production release by definition

**Feature branch rules:**
- Branch from: `develop`
- Merge to: `develop` 
- Use `--no-ff` flag to preserve feature history and enable easy rollbacks
- Exist only in developer repos, not origin

**Release branch workflow:**
- Branch from `develop` when ready for release
- Version number assigned at branch creation, not earlier
- Allows minor bug fixes and metadata preparation
- Must merge back to both `master` (tagged) and `develop`

**Hotfix branch process:**
- Branch from `master` for critical production fixes
- Merge back to both `master` and `develop` (or current release branch)
- Enables parallel work while fixing production issues

**Key technical details:**
- Always use `--no-ff` for merges to maintain branch history
- Tag all releases on `master` for future reference
- Central "truth" repo called `origin` despite Git's decentralized nature

## Bottom Line
Git-flow is a comprehensive branching model for versioned software requiring structured releases, but teams should choose simpler workflows for continuous delivery scenarios.