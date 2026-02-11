# Comparing Git workflows

**Source:** https://www.atlassian.com/git/tutorials/comparing-workflows
**Section:** Development process

---

## Key Insights

**Workflow Selection Criteria:**
- Scale with team size
- Easy error recovery/rollback capability  
- Minimal cognitive overhead for developers

**Centralized Workflow Mechanics:**
- Single `main` branch, no feature branches
- Developers clone central repo, commit locally, push when ready
- Use `git pull --rebase origin main` to avoid merge commits
- Best for: SVN migrations, small teams (scalability bottleneck with conflicts)

**Conflict Resolution Process:**
- `git pull --rebase` moves local commits to tip after syncing
- Resolves conflicts commit-by-commit vs. one massive merge
- `git rebase --abort` to escape if confused
- `git rebase --continue` after resolving each conflict

**Branch Strategy Guidelines:**
- Short-lived branches reduce merge conflicts and deployment risks
- Design workflow to prevent reverts proactively
- Match release schedule: frequent releases = stable main branch; infrequent = use tags
- Align branches with task tracking systems

**Alternative Workflows:**
- **Feature Branching**: Dedicated branch per feature, keeps main stable
- **Gitflow**: Strict branching model with specific branch roles for releases
- **Forking**: Each developer has server-side + local repo (vs. shared central)

**Implementation Commands:**
- `git init --bare` for central repo setup
- `git clone ssh://user@host/path/to/repo.git`
- `git pull --rebase origin main` (preferred over merge)

## Bottom Line
Choose Git workflows based on team size, release frequency, and error tolerance rather than technical complexity—centralized works for small teams but bottlenecks with scale.