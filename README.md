# Awesome CTO — Distilled

> 153 articles from [awesome-cto](https://github.com/kuchin/awesome-cto), fetched, read by AI, and ruthlessly compressed into pure signal. No fluff, no intros, no "in today's fast-paced world..." — just the insights that matter.

## What is this?

The [awesome-cto](https://github.com/kuchin/awesome-cto) repo (32k+ ⭐) is a legendary collection of articles for CTOs and engineering leaders. The problem? Nobody has time to read them all.

This repo solves that. Every article was:

1. **Fetched** — scraped and converted to clean text
2. **Distilled** — summarized by AI (Claude, Anthropic) with a single directive: _extract only actionable insights, concrete frameworks, specific numbers, and non-obvious lessons. Kill everything else._
3. **Organized** — grouped by topic, linked back to originals

The result is a browsable knowledge base you can read in an afternoon instead of a month.

📖 **[Read everything in one file →](summaries/ALL_SUMMARIES.md)**

## How This Was Made

A Python script using:
- **[trafilatura](https://github.com/adbar/trafilatura)** for article extraction (best-in-class boilerplate removal)
- **[Anthropic Message Batches API](https://docs.anthropic.com/en/docs/build-with-claude/batch-processing)** for parallel summarization with Claude
- A system prompt tuned for ruthless distillation — no summaries, just signal

The tool is available at [`awesome_cto_fetcher.py`](awesome_cto_fetcher.py) if you want to run it yourself or adapt it for other awesome-* lists.

## Articles Index

### CTO Position
| Article | Source |
|---------|--------|
| [How my role as CTO has changed as we've grown to 100 engineers](summaries/how-my-role-as-cto-has-changed-as-weve-grown-to-100-engineers.md) | [medium.com](https://medium.com/gusto-engineering/how-my-role-as-cto-has-changed-as-weve-grown-to-100-engineers-b16a8a6b1a88) |
| [The Different CTO Roles](summaries/the-different-cto-roles.md) | [allthingsdistributed.com](https://www.allthingsdistributed.com/2007/07/the_different_cto_roles.html) |
| [Your first 90 days as CTO or VP Engineering](summaries/your-first-90-days-as-cto-or-vp-engineering.md) | [lethain.com](https://lethain.com/first-ninety-days-cto-vpe/) |
| [How to spend your first 30 days in a new senior-level role](summaries/how-to-spend-your-first-30-days-in-a-new-senior-level-role.md) | [larahogan.me](https://larahogan.me/blog/first-30-days-new-role/) |
| [Evolution of my role as a founder CTO](summaries/evolution-of-my-role-as-a-founder-cto.md) | [miguelcarranza.es](https://miguelcarranza.es/cto) |
| [Year 4 Update](summaries/year-4-update.md) | [miguelcarranza.es](https://miguelcarranza.es/cto-year-4) |
| [#define CTO](summaries/define-cto.md) | [blog.gregbrockman.com](https://blog.gregbrockman.com/figuring-out-the-cto-role-at-stripe) |
| [VP Engineering vs CTO](summaries/vp-engineering-vs-cto.md) | [avc.com](https://avc.com/2011/10/vp-engineering-vs-cto/) |
| [Three Golden Rules to Finding a CTO](summaries/three-golden-rules-to-finding-a-cto.md) | [rudebaguette.com](https://www.rudebaguette.com/2011/12/01/three-golden-rules-to-finding-a-cto/) |
| [Year 5 Update](summaries/year-5-update.md) | [miguelcarranza.es](https://miguelcarranza.es/cto-year-5) |
| [Becoming a CTO](summaries/becoming-a-cto.md) | [web.archive.org](https://web.archive.org/web/20171128214925/https://juokaz.com/blog/becoming-a-cto) |

### Hiring
| Article | Source |
|---------|--------|
| [Why Can't Programmers.. Program?](summaries/why-cant-programmers-program.md) | [blog.codinghorror.com](https://blog.codinghorror.com/why-cant-programmers-program/) |
| [We Hire the Best, Just Like Everyone Else](summaries/we-hire-the-best-just-like-everyone-else.md) | [blog.codinghorror.com](https://blog.codinghorror.com/we-hire-the-best-just-like-everyone-else/) |
| [Getting the Interview Phone Screen Right](summaries/getting-the-interview-phone-screen-right.md) | [blog.codinghorror.com](https://blog.codinghorror.com/getting-the-interview-phone-screen-right/) |
| [The Joel Test: 12 Steps to Better Code](summaries/the-joel-test-12-steps-to-better-code.md) | [joelonsoftware.com](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/) |
| [The Guerrilla Guide to Interviewing](summaries/the-guerrilla-guide-to-interviewing.md) | [joelonsoftware.com](https://www.joelonsoftware.com/2006/10/25/the-guerrilla-guide-to-interviewing-version-30/) |
| [Improving Our Engineering Interview Process](summaries/improving-our-engineering-interview-process.md) | [medium.com](https://medium.com/foursquare-direct/improving-our-engineering-interview-process-106173ba25a9) |
| [Hitting the High Notes](summaries/hitting-the-high-notes.md) | [joelonsoftware.com](https://www.joelonsoftware.com/2005/07/25/hitting-the-high-notes/) |
| [Lessons from Keith Rabois: How to Become a Magnet for Talent](summaries/lessons-from-keith-rabois-how-to-become-a-magnet-for-talent.md) | [delian.io](https://delian.io/lessons-5) |
| [Trouble hiring senior engineers? It's probably you](summaries/trouble-hiring-senior-engineers-its-probably-you.md) | [hiringengineersbook.com](https://hiringengineersbook.com/post/trouble-hiring/) |
| [Lessons from Keith Rabois: How to Interview an Executive](summaries/lessons-from-keith-rabois-how-to-interview-an-executive.md) | [delian.io](https://delian.io/lessons-2) |
| [Visualizing Tech Company Layoffs in 2022](summaries/visualizing-tech-company-layoffs-in-2022.md) | [visualcapitalist.com](https://www.visualcapitalist.com/visualizing-tech-company-layoffs-in-2022/) |
| [The Real 11 Reasons I Don't Hire You](summaries/the-real-11-reasons-i-dont-hire-you.md) | [charity.wtf](https://charity.wtf/2019/10/18/the-real-11-reasons-i-dont-hire-you/) |
| [How To Hire World-Class Engineers](summaries/how-to-hire-world-class-engineers.md) | [angel.co](https://angel.co/blog/how-to-hire-world-class-engineers) |
| [Top 10 System Design Interview Questions](summaries/top-10-system-design-interview-questions.md) | [hackernoon.com](https://hackernoon.com/top-10-system-design-interview-questions-for-software-engineers-8561290f0444) |
| [GitLab Talent Acquisition Framework](summaries/gitlab-talent-acquisition-framework.md) | [about.gitlab.com](https://about.gitlab.com/handbook/hiring/talent-acquisition-framework/) |

### People Management
| Article | Source |
|---------|--------|
| [The mythical 10x programmer](summaries/the-mythical-10x-programmer.md) | [antirez.com](http://antirez.com/news/112) |
| [The Engineer/Manager Pendulum](summaries/the-engineermanager-pendulum.md) | [charity.wtf](https://charity.wtf/2017/05/11/the-engineer-manager-pendulum/) |
| [12 manager readmes from top tech companies](summaries/12-manager-readmes-from-top-tech-companies.md) | [hackernoon.com](https://hackernoon.com/12-manager-readmes-from-silicon-valleys-top-tech-companies-26588a660afe) |
| [non-violent communication](summaries/non-violent-communication.md) | [review.firstround.com](https://review.firstround.com/power-up-your-team-with-nonviolent-communication-principles) |
| [Design Patterns for Managing Up](summaries/design-patterns-for-managing-up.md) | [queue.acm.org](https://queue.acm.org/detail.cfm?id=3308563) |
| [Should I Become a Manager?](summaries/should-i-become-a-manager.md) | [capwatkins.com](https://capwatkins.com/blog/should-i-become-a-manager) |
| [A Review Process](summaries/a-review-process.md) | [capwatkins.com](https://capwatkins.com/blog/a-review-process) |
| [44 Engineering Management Lessons](summaries/44-engineering-management-lessons.md) | [defmacro.org](https://www.defmacro.org/2014/10/03/engman.html) |
| [On-boarding Software Engineers](summaries/on-boarding-software-engineers.md) | [medium.com](https://medium.com/@odedmagger/on-boarding-software-engineers-10-techniques-to-get-it-right-927cb73e3dab) |
| [A Tactical Guide to Managing Up](summaries/a-tactical-guide-to-managing-up.md) | [review.firstround.com](https://review.firstround.com/a-tactical-guide-to-managing-up-30-tips-from-the-smartest-people-we-know) |
| [Principles of Engineering Management](summaries/principles-of-engineering-management.md) | [medium.com](https://medium.com/swlh/principles-of-engineering-management-c9cae1b34a8b) |
| [The Secret To Discussing Pay With Employees](summaries/the-secret-to-discussing-pay-with-employees.md) | [officevibe.com](https://www.officevibe.com/blog/secret-to-discussing-pay-with-employees) |
| [A MANAGER’S BILL OF RESPONSIBILITIES (AND RIGHTS)](summaries/a-managers-bill-of-responsibilities-and-rights.md) | [charity.wtf](https://charity.wtf/2019/10/30/a-managers-bill-of-responsibilities-and-rights/) |
| [The Manager FAQ](summaries/the-manager-faq.md) | [seebs.net](https://www.seebs.net/faqs/manager.html) |
| [Hold Your Team Accountable](summaries/hold-your-team-accountable.md) | [dave-bailey.com](https://www.dave-bailey.com/blog/accountability-dial) |
| [Lessons from Keith Rabois: How to be an Effective Executive](summaries/lessons-from-keith-rabois-how-to-be-an-effective-executive.md) | [delian.io](https://delian.io/lessons-3) |
| [Maker's Schedule, Manager's Schedule](summaries/makers-schedule-managers-schedule.md) | [paulgraham.com](http://www.paulgraham.com/makersschedule.html) |
| [Compensation Best Practices](summaries/compensation-best-practices.md) | [payscale.com](https://www.payscale.com/cbpr) |
| [The Power of Performance Reviews](summaries/the-power-of-performance-reviews.md) | [firstround.com](https://firstround.com/review/the-power-of-performance-reviews-use-this-system-to-become-a-better-manager/) |
| [After Being A Manager, Can I Be Happy As A Cog?](summaries/after-being-a-manager-can-i-be-happy-as-a-cog.md) | [charity.wtf](https://charity.wtf/2019/11/23/questionable-advice-after-being-a-manager-can-i-be-happy-as-a-cog/) |
| [Hacking team communications](summaries/hacking-team-communications.md) | [noamelf.com](https://noamelf.com/posts/hacking-team-communications/) |
| [Increment: Teams](summaries/increment-teams.md) | [increment.com](https://increment.com/teams/) |
| [Draw The Owl and Other Company Values You Didn’t Know You Should Have](summaries/draw-the-owl-and-other-company-values-you-didnt-know-you-should-have.md) | [firstround.com](https://firstround.com/review/draw-the-owl-and-other-company-values-you-didnt-know-you-should-have/) |
| [10,000 Hours with Reid Hoffman: What I Learned](summaries/10000-hours-with-reid-hoffman-what-i-learned.md) | [casnocha.com](https://casnocha.com/reid-hoffman-lessons) |
| [Meetings for an effective eng organization](summaries/meetings-for-an-effective-eng-organization.md) | [lethain.com](https://lethain.com/eng-org-meetings/) |
| [How to build a startup engineering team](summaries/how-to-build-a-startup-engineering-team.md) | [increment.com](https://increment.com/teams/how-to-build-a-startup-engineering-team/) |
| [7 Ways to Set Up a New Hire for Success](summaries/7-ways-to-set-up-a-new-hire-for-success.md) | [hbr.org](https://hbr.org/2019/05/7-ways-to-set-up-a-new-hire-for-success) |
| [Individuals matter](summaries/individuals-matter.md) | [danluu.com](https://danluu.com/people-matter/) |
| [Mandate Levels](summaries/mandate-levels.md) | [cutlefish.substack.com](https://cutlefish.substack.com/p/tbm-2752-mandate-levels) |
| [Step by step guide to building high performing teams](summaries/step-by-step-guide-to-building-high-performing-teams.md) | [mm-coaches.notion.site](https://mm-coaches.notion.site/Step-by-step-guide-to-building-high-performing-teams-a1d3c70c031144738943e043933d3267) |
| [The One Key to Dealing with Senior Executives: Answer the Question!](summaries/the-one-key-to-dealing-with-senior-executives-answer-the-question.md) | [kellblog.com](https://kellblog.com/2012/01/17/the-one-key-to-dealing-with-senior-executives-answer-the-question/) |
| [Hug your manager](summaries/hug-your-manager.md) | [buttondown.email](https://buttondown.email/cote/archive/hug-your-manager/) |
| [Cycle times](summaries/cycle-times.md) | [boz.com](https://boz.com/articles/cycle-times) |
| [Adapting to Endure / Crisis management](summaries/adapting-to-endure-crisis-management.md) | [sequoiacap.com](https://www.sequoiacap.com/adapting-to-endure-2022/) |

### Career growth
| Article | Source |
|---------|--------|
| [Reverse Interviewing — How to interview a company as well as they interview you](summaries/reverse-interviewing-how-to-interview-a-company-as-well-as-they-interview-you.md) | [fishmanafnewsletter.com](https://www.fishmanafnewsletter.com/p/how-to-reverse-interview) |
| [Software Engineers Growth framework](summaries/software-engineers-growth-framework.md) | [prontopro.engineering](https://prontopro.engineering/blog/software-engineer-growth-framework) |
| [The Reverse Interview: How To Choose Your Next Company](summaries/the-reverse-interview-how-to-choose-your-next-company.md) | [reforge.com](https://www.reforge.com/blog/reverse-interview) |
| [Career Growth Frameworks in Software Engineering: A Review](summaries/career-growth-frameworks-in-software-engineering-a-review.md) | [web.archive.org](https://web.archive.org/web/20210123114037/https://medium.com/better-programming/career-growth-frameworks-in-software-engineering-a-review-4aa6c59a9cf6) |

### Project management
| Article | Source |
|---------|--------|
| [Evidence Based Scheduling](summaries/evidence-based-scheduling.md) | [joelonsoftware.com](https://www.joelonsoftware.com/2007/10/26/evidence-based-scheduling/) |
| [The Secret to a Great Planning Process — Lessons from Airbnb and Eventbrite](summaries/the-secret-to-a-great-planning-process-lessons-from-airbnb-and-eventbrite.md) | [review.firstround.com](https://review.firstround.com/the-secret-to-a-great-planning-process-lessons-from-airbnb-and-eventbrite) |
| [Measuring an engineering organization](summaries/measuring-an-engineering-organization.md) | [lethain.com](https://lethain.com/measuring-engineering-organizations/) |
| [How Big Tech Runs Tech Projects and the Curious Absence of Scrum](summaries/how-big-tech-runs-tech-projects-and-the-curious-absence-of-scrum.md) | [newsletter.pragmaticengineer.com](https://newsletter.pragmaticengineer.com/p/project-management-in-tech) |
| [How to Scope a New Feature](summaries/how-to-scope-a-new-feature.md) | [prodify.group](https://www.prodify.group/blog/how-to-scope-a-new-feature) |
| [What TPMs Do and What Software Engineers Can Learn From Them](summaries/what-tpms-do-and-what-software-engineers-can-learn-from-them.md) | [newsletter.pragmaticengineer.com](https://newsletter.pragmaticengineer.com/p/what-tpms-do) |

### Handbooks
| Article | Source |
|---------|--------|
| [The Atlassian Team Playbook](summaries/the-atlassian-team-playbook.md) | [atlassian.com](https://www.atlassian.com/team-playbook) |
| [GitLab Team Handbook](summaries/gitlab-team-handbook.md) | [about.gitlab.com](https://about.gitlab.com/handbook/) |

### Development process
| Article | Source |
|---------|--------|
| [Trunk Based Development](summaries/trunk-based-development.md) | [atlassian.com](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development) |
| [Comparing Git workflows](summaries/comparing-git-workflows.md) | [atlassian.com](https://www.atlassian.com/git/tutorials/comparing-workflows) |
| [Why You Should Learn to Stop Worrying and Love Technical Debt](summaries/why-you-should-learn-to-stop-worrying-and-love-technical-debt.md) | [marker.medium.com](https://marker.medium.com/why-you-should-learn-to-stop-worrying-and-love-technical-debt-55bb5684f94c) |
| [A successful Git branching model](summaries/a-successful-git-branching-model.md) | [nvie.com](https://nvie.com/posts/a-successful-git-branching-model/) |
| [Writing User Stories, Examples and Templates In Agile Methodologies](summaries/writing-user-stories-examples-and-templates-in-agile-methodologies.md) | [yodiz.com](http://www.yodiz.com/blog/writing-user-stories-examples-and-templates-in-agile-methodologies/) |
| [Startup Lessons Learned - Five Whys](summaries/startup-lessons-learned---five-whys.md) | [startuplessonslearned.com](http://www.startuplessonslearned.com/2008/11/five-whys.html) |
| [Testing in Production, the safe way](summaries/testing-in-production-the-safe-way.md) | [medium.com](https://medium.com/@copyconstruct/testing-in-production-the-safe-way-18ca102d0ef1) |
| [On Call Rotations: How Best to Wake Devs Up in the Middle of the Night](summaries/on-call-rotations-how-best-to-wake-devs-up-in-the-middle-of-the-night.md) | [thenewstack.io](https://thenewstack.io/call-rotations-best-wake-devs-middle-night/) |
| [It’s Time to Rethink Technical Debt Management](summaries/its-time-to-rethink-technical-debt-management.md) | [sealights.io](https://www.sealights.io/blog/its-time-to-rethink-technical-debt-management/) |
| [How to Write a Postmortem](summaries/how-to-write-a-postmortem.md) | [web.archive.org](https://web.archive.org/web/20210618014202/https://blog.serverdensity.com/how-to-write-a-postmortem/) |

### Architecture
| Article | Source |
|---------|--------|
| [Microservices – Please, don’t](summaries/microservices-please-dont.md) | [riak.com](https://riak.com/posts/technical/microservices-please-dont/) |
| [Shrinking microservices to functions](summaries/shrinking-microservices-to-functions.md) | [highscalability.com](https://highscalability.com/blog/2017/3/27/faster-networks-cheaper-messages-microservices-functions-edg.html) |
| [10 Modern Software Over-Engineering Mistakes](summaries/10-modern-software-over-engineering-mistakes.md) | [medium.com](https://medium.com/@rdsubhas/10-modern-software-engineering-mistakes-bc67fbef4fc8) |
| [Best Practices for Designing a Pragmatic RESTful API](summaries/best-practices-for-designing-a-pragmatic-restful-api.md) | [vinaysahni.com](https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api) |
| [HackerNews discussion](summaries/hackernews-discussion.md) | [news.ycombinator.com](https://news.ycombinator.com/item?id=33601658) |
| [The Death of Microservice Madness in 2018](summaries/the-death-of-microservice-madness-in-2018.md) | [dwmkerr.com](https://www.dwmkerr.com/the-death-of-microservice-madness-in-2018/) |
| [How I Write Tests](summaries/how-i-write-tests.md) | [blog.nelhage.com](https://blog.nelhage.com/2016/12/how-i-test/) |
| [HackerNews discussion](summaries/hackernews-discussion.md) | [news.ycombinator.com](https://news.ycombinator.com/item?id=12508655) |
| [Design patterns for microservices](summaries/design-patterns-for-microservices.md) | [azure.microsoft.com](https://azure.microsoft.com/en-us/blog/design-patterns-for-microservices/) |
| [Accentuate the negative: making the non-perfect decision. Technical decision making](summaries/accentuate-the-negative-making-the-non-perfect-decision-technical-decision.md) | [leaddev.com](https://leaddev.com/technical-decision-making/accentuate-negative-making-non-perfect-decision) |
| [The Single Most Important Internal Email in the History of Amazon](summaries/the-single-most-important-internal-email-in-the-history-of-amazon.md) | [web.archive.org](https://web.archive.org/web/20221127150918/https://pulseasync.com/operators/frameworks-for-remote-working/) |

### Technologies
| Article | Source |
|---------|--------|
| [CAP Theorem: Revisited](summaries/cap-theorem-revisited.md) | [robertgreiner.com](https://robertgreiner.com/cap-theorem-revisited/) |
| [JS: The Right Way](summaries/js-the-right-way.md) | [jstherightway.org](http://jstherightway.org) |
| [Big-O explained in plain English](summaries/big-o-explained-in-plain-english.md) | [stackoverflow.com](https://stackoverflow.com/a/487278/472433) |
| [SaaS CTO Security Checklist](summaries/saas-cto-security-checklist.md) | [web.archive.org](https://web.archive.org/web/20230324072622/https://www.goldfiglabs.com/guide/saas-cto-security-checklist/) |
| [Microsoft Azure in Plain English](summaries/microsoft-azure-in-plain-english.md) | [web.archive.org](https://web.archive.org/web/20190508145128/https://www.expeditedssl.com/azure-in-plain-english) |

### Data
| Article | Source |
|---------|--------|
| [A reference guide for fintech & small-data engineering](summaries/a-reference-guide-for-fintech-small-data-engineering.md) | [medium.com](https://medium.com/dangerous-engineering/a-reference-guide-for-fintech-small-data-engineering-bd65b9796d90) |
| [Database Migrations Done Right](summaries/database-migrations-done-right.md) | [brunton-spall.co.uk](https://www.brunton-spall.co.uk/post/2014/05/06/database-migrations-done-right/) |
| [Evolutionary Database Design](summaries/evolutionary-database-design.md) | [martinfowler.com](https://martinfowler.com/articles/evodb.html) |
| [Building a data team at a mid-stage startup: a short story](summaries/building-a-data-team-at-a-mid-stage-startup-a-short-story.md) | [erikbern.com](https://erikbern.com/2021/07/07/the-data-team-a-short-story.html) |
| [Building a data science team](summaries/building-a-data-science-team.md) | [fastdatascience.com](https://fastdatascience.com/building-a-data-science-team/) |
| [How to Structure a Data Science Team](summaries/how-to-structure-a-data-science-team.md) | [altexsoft.com](https://www.altexsoft.com/blog/datascience/how-to-structure-data-science-team-key-models-and-roles/) |
| [Databases in 2022: A Year in Review](summaries/databases-in-2022-a-year-in-review.md) | [ottertune.com](https://ottertune.com/blog/2022-databases-retrospective/) |
| [Managing Data Science Teams](summaries/managing-data-science-teams.md) | [dominodatalab.com](https://www.dominodatalab.com/resources/field-guide/managing-data-science-teams/) |

### Startups
| Article | Source |
|---------|--------|
| [85 Things I learned being a CEO](summaries/85-things-i-learned-being-a-ceo.md) | [hackernoon.com](https://hackernoon.com/85-things-i-learned-being-a-ceo-4c25fc1c7b99) |
| [YC’s Series A Diligence Checklist](summaries/ycs-series-a-diligence-checklist.md) | [blog.ycombinator.com](https://blog.ycombinator.com/ycs-series-a-diligence-checklist/) |
| [What’s the Second Job of a Startup CEO?](summaries/whats-the-second-job-of-a-startup-ceo.md) | [blog.ycombinator.com](https://blog.ycombinator.com/the-second-job-of-a-startup-ceo/) |

### Due Diligence
| Article | Source |
|---------|--------|
| [A Guide to Surviving Tech Due Diligence](summaries/a-guide-to-surviving-tech-due-diligence.md) | [circleci.com](https://circleci.com/resources/tech-due-diligence/) |
| [IT Department Tech Due Diligence Checklist](summaries/it-department-tech-due-diligence-checklist.md) | [gist.github.com](https://gist.github.com/raphaelbauer/b31d49d91a0af6c1106bfc8ef4bf6d13) |
| [Technology Due Diligence Checklist](summaries/technology-due-diligence-checklist.md) | [akfpartners.com](https://akfpartners.com/growth-blog/technical-due-diligence-checklists) |

### Money / Finance
| Article | Source |
|---------|--------|
| [Options vs Cash](summaries/options-vs-cash.md) | [danluu.com](https://danluu.com/startup-options/) |
| [How To Invest In Startups](summaries/how-to-invest-in-startups.md) | [blog.samaltman.com](https://blog.samaltman.com/how-to-invest-in-startups) |
| [Equity 101 for Software Engineers at Big Tech and Startups](summaries/equity-101-for-software-engineers-at-big-tech-and-startups.md) | [blog.pragmaticengineer.com](https://blog.pragmaticengineer.com/equity-for-software-engineers/) |
| [Framework for balancing and budgeting engineering resourcing](summaries/framework-for-balancing-and-budgeting-engineering-resourcing.md) | [medium.com](https://medium.com/engineering-operations/a-framework-for-balancing-and-budgeting-engineering-resourcing-d0cce0e6911c) |
| [IPOs and Beyond: A Guide to Exit Options for Companies](summaries/ipos-and-beyond-a-guide-to-exit-options-for-companies.md) | [future.a16z.com](https://future.a16z.com/ipos-and-beyond-a-guide-to-exit-options-for-companies/) |
| [Option grants at seed](summaries/option-grants-at-seed.md) | [indexventures.com](https://www.indexventures.com/rewardingtalent/option-grants-at-seed) |
| [A Guide to Seed Fundraising](summaries/a-guide-to-seed-fundraising.md) | [blog.ycombinator.com](https://blog.ycombinator.com/how-to-raise-a-seed-round/) |
| [Negotiate the right deal with suppliers](summaries/negotiate-the-right-deal-with-suppliers.md) | [infoentrepreneurs.org](https://www.infoentrepreneurs.org/en/guides/negotiate-the-right-deal-with-suppliers/) |
| [Strategic Procurements 10 Commandments for Managing the Buying Process](summaries/strategic-procurements-10-commandments-for-managing-the-buying-process.md) | [strategicdynamicsfirm.com](https://strategicdynamicsfirm.com/strategic-procurements-10-commandments-managing-hospital-buying-process/) |
| [Financial Planning & Analysis @ GitLab](summaries/financial-planning-analysis-gitlab.md) | [about.gitlab.com](https://about.gitlab.com/handbook/finance/financial-planning-and-analysis/) |

### Related stuff
| Article | Source |
|---------|--------|
| [Knowledge-Sharing Architects As An Alternative to Coding Architects](summaries/knowledge-sharing-architects-as-an-alternative-to-coding-architects.md) | [ithare.com](http://ithare.com/knowledge-sharing-architects-as-an-alternative-to-coding-architects/) |
| [Ten Rules for Negotiating a Job Offer](summaries/ten-rules-for-negotiating-a-job-offer.md) | [haseebq.com](https://haseebq.com/my-ten-rules-for-negotiating-a-job-offer/) |
| [Undervalued Software Engineering Skills: Writing Well](summaries/undervalued-software-engineering-skills-writing-well.md) | [blog.pragmaticengineer.com](https://blog.pragmaticengineer.com/on-writing-well/) |
| [DevOps: Bringing development and operations together](summaries/devops-bringing-development-and-operations-together.md) | [atlassian.com](https://www.atlassian.com/devops) |
| [The Pyramid Principle](summaries/the-pyramid-principle.md) | [medium.com](https://medium.com/lessons-from-mckinsey/the-pyramid-principle-f0885dd3c5c7) |
| [Senior Engineer’s Checklist](summaries/senior-engineers-checklist.md) | [medium.com](https://medium.com/@littleblah/my-top-25-items-in-a-senior-engineers-checklist-c8e9f9f6e3c2) |
| [Salary Negotiation: Make More Money, Be More Valued](summaries/salary-negotiation-make-more-money-be-more-valued.md) | [kalzumeus.com](https://www.kalzumeus.com/2012/01/23/salary-negotiation/) |
| [Falsehoods Programmers Believe About Names](summaries/falsehoods-programmers-believe-about-names.md) | [kalzumeus.com](https://www.kalzumeus.com/2010/06/17/falsehoods-programmers-believe-about-names/) |
| [How to Prepare a Talk](summaries/how-to-prepare-a-talk.md) | [deconstructconf.com](https://www.deconstructconf.com/blog/how-to-prepare-a-talk) |
| [How to Use OpenAPI and Swagger for Documentation](summaries/how-to-use-openapi-and-swagger-for-documentation.md) | [blog.readme.com](https://blog.readme.com/how-to-use-openapi-and-swagger-spec-for-documentation/) |
| [HackerNews discussion](summaries/hackernews-discussion.md) | [news.ycombinator.com](https://news.ycombinator.com/item?id=12197795) |

### Product
| Article | Source |
|---------|--------|
| [What Makes a Great Product Manager](summaries/what-makes-a-great-product-manager.md) | [hackernoon.com](https://hackernoon.com/what-makes-a-great-product-manager-3c1d03b90356) |
| [Product North Star Metric](summaries/product-north-star-metric.md) | [amplitude.com](https://amplitude.com/blog/product-north-star-metric) |
| [The Secrets Of Creative Thinking](summaries/the-secrets-of-creative-thinking.md) | [lemonade.com](https://www.lemonade.com/blog/creative-thinking-hacks/) |
| [How to Hire a Product Manager](summaries/how-to-hire-a-product-manager.md) | [kennorton.com](https://www.kennorton.com/essays/productmanager.html) |
| [Red Oceans: How to Find Profitable Startup Ideas](summaries/red-oceans-how-to-find-profitable-startup-ideas.md) | [capitalandgrowth.org](https://capitalandgrowth.org/answers/Article/3143488/How-to-Find-Profitable-Business-Ideas) |
| [Shape Up: Stop Running in Circles and Ship Work that Matters](summaries/shape-up-stop-running-in-circles-and-ship-work-that-matters.md) | [basecamp.com](https://basecamp.com/shapeup) |
| [If You Don’t Think You Need a VP of Product...](summaries/if-you-dont-think-you-need-a-vp-of-product.md) | [saastr.com](https://www.saastr.com/if-you-dont-think-you-need-a-vp-of-product-marketing-etc-then-you-havent-worked-with-a-great-one/) |
| [Product vs. Feature Teams](summaries/product-vs-feature-teams.md) | [svpg.com](https://svpg.com/product-vs-feature-teams/) |
| [Execution at Facebook](summaries/execution-at-facebook.md) | [productlife.to](https://productlife.to/p/-execution-at-facebook) |
| [8 Product Hurdles Every Founder Must Clear](summaries/8-product-hurdles-every-founder-must-clear.md) | [review.firstround.com](https://review.firstround.com/8-product-hurdles-every-founder-must-clear-this-pm-turned-founder-shares-his-playbooks) |
| [The Top 10 Deliverables of Product Managers](summaries/the-top-10-deliverables-of-product-managers.md) | [sachinrekhi.com](https://www.sachinrekhi.com/top-10-deliverables-of-product-managers) |
| [How to Write Your First Strategic Roadmap](summaries/how-to-write-your-first-strategic-roadmap.md) | [ganotnoa.com](https://ganotnoa.com/how-to-write-your-first-strategic-roadmap-part-1/) |
| [Most Startups Should Be Deer Hunters](summaries/most-startups-should-be-deer-hunters.md) | [bothsidesofthetable.com](https://bothsidesofthetable.com/most-startups-should-be-deer-hunters-7fdecf58f4f6) |

### Marketing
| Article | Source |
|---------|--------|
| [Developer Marketing Guide](summaries/developer-marketing-guide.md) | [devmarketingguide.com](https://www.devmarketingguide.com) |
| [How today's fastest growing B2B businesses found their first ten customers](summaries/how-todays-fastest-growing-b2b-businesses-found-their-first-ten-customers.md) | [lennysnewsletter.com](https://www.lennysnewsletter.com/p/how-todays-fastest-growing-b2b-businesses) |
| [SaaS Email Marketing Handbook](summaries/saas-email-marketing-handbook.md) | [saasemailmarketing.net](https://saasemailmarketing.net) |

### More links
| Article | Source |
|---------|--------|
| [foundr - Advices from founders](summaries/foundr---advices-from-founders.md) | [foundr.com](https://foundr.com/articles) |
| [Socal CTO](summaries/socal-cto.md) | [socalcto.com](https://www.socalcto.com/2011/09/startup-cto.html) |
| [CTO Insights Podcast](summaries/cto-insights-podcast.md) | [ctoinsights.adevait.com](https://ctoinsights.adevait.com/) |

### Books
| Article | Source |
|---------|--------|
| [Startup CTO's Handbook](summaries/startup-ctos-handbook.md) | [github.com](https://github.com/ZachGoldberg/Startup-CTO-Handbook/) |


## What's Not Included

Some links from the original list couldn't be fetched or aren't articles:
- 🔒 **Paywalled** — LinkedIn, Quora, some Medium articles
- 📊 **Non-articles** — Google Sheets, Figma templates, Miro boards, calculators
- 🐙 **GitHub repos** — These are tool collections, not articles (linked in original list)
- 📄 **PDFs** — Valve handbook, Google engineering paper, etc.
- 🐦 **Tweets** — Can't extract meaningful content
- ❌ **Dead links** — Some articles from 2007-2015 are gone



## Credits

- **Source list:** [kuchin/awesome-cto](https://github.com/kuchin/awesome-cto) (CC0 licensed)
- **All original articles** belong to their respective authors — links to originals are included in every summary
- **Summaries** are original AI-generated distillations, not reproductions

## Contributing

Found a broken summary? Have a better distillation? PRs welcome.

Want to add articles not in the original list? Open an issue — I'll batch-process additions periodically.

## License

MIT — Do whatever you want with the summaries. Original articles remain property of their authors.
