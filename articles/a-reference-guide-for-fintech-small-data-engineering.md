# A reference guide for fintech & small-data engineering

**Source:** https://medium.com/dangerous-engineering/a-reference-guide-for-fintech-small-data-engineering-bd65b9796d90
**Section:** Data


---

A reference guide for fintech & small-data engineering
--
I spent 2018 and the beginning of 2019 leading the Infrastructure teams at Gusto. Before moving on I composed a message to help future Gusto engineers — particularly those who are still in the first half-dozen years of their career and acting as technical leads— understand secure, domain-driven product engineering. This post is an adaptation of that message with some company details elided.
Most software engineering literature assumes you need to process data efficiently. The algorithm-focused, Google-style CS questions that dominate software interviews put particular focus on this — we test candidates on code that works well when data size increases.
In my time leading engineering teams at Square and Gusto I’ve found that this big-data approach to software engineering is a poor fit for many product companies. Rather, product scalability problems are along a different axis: Sprawling domains and massive schemas implementing those domains. These companies face three very specific, very hard problems:
- Correctly modeling the domain
- Creating clear interfaces between parts of the system
- Finding ways to continually accelerate product development speed
Secure, small-data product engineering
This problem isn’t unique to Gusto or Square — there’s a huge set of companies that have small amounts of critical data in complex domains. It’s every fintech company, every product company with a heavy operations arm, and any company trying to model an existing regulatory system.
Here’s a highly inaccurate but illustrative plot of how companies fall on this tradeoff of concerns:
If we’re building Twitter or Instagram we’ll need to process hexabytes of simple information. If we’re building Flexport or Gusto or even Square¹ we’ll be hard-pressed to even find terabytes of information. The scalability challenges are still very real, they’re just along the axes of domain complexity and security.
Welcome to small-data product engineering
If you’re at one of these small-data companies you can’t mitigate the core scalability problems by optimizing source code. Your company probably has enough folks working at that low, focused level. They need people to zoom out and address the whole system.
The three levels of engineering sophistication
There are three levels of sophistication an engineer grows through in their career:
- Working with code
- Working with applications
- Working with systems of applications
#1 Working with code
When we start our career we work with logic in a single method, function, or class. The skills at this level are extremely basic: Editing source code, expressing basic concepts in the given language, storing basic data, etc. This is where features are made.
#2 Working with applications
When we become senior we can work with a whole application at a time. We store lots of relational data and model complex business logic across many files and directories. This is where products are made.
#3 Working with systems of applications
And then we become grizzled veterans working with whole constellations of applications in multiple environments. At this level we perform major migrations, simplify dependencies within the distributed data model, and shepherd the whole multi-application system. This is where companies are made.
The way we work at each level is quite different. The phrase ‘refactoring’ usually applies to the level of source code and, less commonly, at the level of an application. The phrase ‘tech debt’ is more common for working with an application as we handle major framework upgrades and make the data model more expressive.
But at the level of systems both ‘refactoring’ and ‘tech debt’ are inappropriate concepts. At this level of the system there are only two activities you should permit yourself to do:
- Bring a system in line with its design
- Design a replacement system
Anything else is busywork.
Both of those activities assume that the thing we’re building is designed. For this reason, if you feel like a senior engineer your job is now primarily an engineering designer. You should design and help implement software systems that solve the Product team’s current and future needs. If you imagine your job is just the implementation you’ll miss the design step and the overall system won’t make sense.
Levels of PM sophistication
Speaking of Product, these same levels of sophistication apply to PMs. Early-career PMs can launch and steward features. This is valuable and helpful, though at this level the PM can introduce tension between product and engineering. Shipping a single feature quickly is just about never the best thing for the long term health of the interconnected product suite.
Mid-career PMs can launch and steward whole products. This is hugely valuable and here the tension between product and engineering is eased. The PM takes a long-term view of the whole feature-shipping cadence and can work with engineers to make calculated investments to increase shipping speed.
Late-career PMs can launch and steward entire product suites. At this level the PM takes responsibility for an entire ecosystem of engineering and product. They are natural allies to engineers and will often push for systemic simplifications and increased coherence between parts of the product suite — something that allows engineers to make dramatic simplifications to the underlying system.
Growing technology at a product company
If your product’s production dataset is smaller than a terabyte then you have no data. None. 100% of your data can fit on two iPhones. The solutions from Google, LinkedIn, and other big companies are useless here. Your peers are Square, Flexport, Gusto, Stripe, Coinbase, and any place with huge amounts of logic but small, critically important pieces of data.
Your problems give you four focus areas that are more important to you than to the average company:
- Prioritizing domain model correctness over computational efficiency
- Refactoring the data model early and often
- Ensuring data is encrypted by default everywhere except in your product’s memory space
- Separating data by sensitivity (PHI, PII, PCI) to empower your Security team
And straight-up disregard any blog post from a company that has any of the following:
- Lots of data
- A ridiculous amount of money
- Low security restrictions
Twitter can lose a tweet. LinkedIn can lose a ‘like’ on a post. Square can’t lose a payment. Gusto can’t lose an IRS filing.
So your problems are different. Instead of using something that works well when you process trillions of records per minute you need to use tools that are simple to operate and that support encryption powered by role-based access control (i.e. if service A produces data then service B can only decrypt A’s data if it’s allowed to).
Other small-data, security-conscious companies have solved these problems. But as of yet none of their in-house tools for securely handling data in prod have been open sourced². So you’ll have to just build something very simple and design it carefully.
How to select technologies
Which brings us to the rule for when to build technology in-house or use something that exists externally:
“If a problem is unique to your product offering then you may invent an appropriate solution. Otherwise go with an industry standard approach — and only use one approach at a time.”
Invent software that extends your competitive business advantage. And for everything else just use off-the-shelf tools. Your deployment system should look eerily similar to one of the top ten results for a generic search like “AWS deployment EC2”. Your cloud networking setup should look identical to the AWS official standardized architecture for PCI compliant systems. Your database tables should use the third normal form.
Performing Migrations
Note that last phrase in the above rule: “–and use only one approach at a time.” You’ll need a way to move from one version to another. This means you and your team need to get good at performing migrations.
Whether you’re making a tiny change to a database column or overhauling a major system all good migrations have five stages:
- Design the v2 and the path to get there
- Fix v1
- Implement v2
- Carefully migrate from v1 to v2 in atomic, safe steps
- Delete v1
Most teams forget steps #2 and #5. If v1 is poorly factored you’ll inevitably have to make significant changes to v1 before it’s in a shape to be migrated. Since we need to do that work anyway we might as well stop pretending v2 will rid us of v1. Fix v1 in place before you start building v2.
And don’t accept any migration that doesn’t have, as its last step, an act like “drop these tables” or “delete this code”. If you can’t actually replace the current thing don’t bother with the migration. Do it right or don’t do it.
What teams should ‘own’
Some companies allow teams to carve out juicy projects for themselves and prevent other folks from working on them. This kind of technical bureaucracy cuts through engineering morale like a hot knife through butter. Teams shouldn’t claim projects, they should claim problems. And they should accept as much help from any direction when solving those problems.
Don’t say “We’re going to roll out a new frontend technology” when you can say “We’re going to solve that adding new storage classes in the frontend is hard”. Then you can have an open debate across all interested stakeholders in how that problem should be solved. Once there’s agreement you start work and you gratefully accept commits from everybody.
No architecture astronautics
As Alyssa Henry (founder of AWS S3, Head of Engineering at Square) sometimes says: “The ideal system in your head is never as good as the working system in front of you.” Beware of architecture astronauts. And be even more wary of becoming one.
You can identify architecture astronautics when someone (including yourself) starts to believe that there’s a technological solution to poor design.
If I create a React component that mixes a signup form, account approval, and uploading a user’s avatar all in one Javascript function that’s just poor design. I cannot fix this problem by porting it to a new Javascript framework.
If I create an HTTP endpoint that performs five separate operations and also calls out to a different service multiple times — that’s poor design. That cannot be solved by introducing new service boundary technology.
The work of building long-term value is really hard but really simple: Decide what it is you’re actually trying to build and then implement that in the simplest way possible.
How to prioritize systemic fixes
Imagine putting sand into a jar, then pebbles, then big rocks. The big rocks don’t fit.
We have to do the big rocks first. When the right solution to a problem takes 10 engineers for a year then put 10 engineers on it for a year and make sure it’s solved well. And if it takes longer let it take longer. Don’t put 3 engineers on it for a quarter. That just adds sand to the jar. Small wins are great and easy to prioritize but at some point you need more in the jar than just sand.
Building a product platform for your customers
See: The four interfaces of SaaS product suites
If you have any customers then you’ve already solved one of the hardest problems. Now you can create and sell other products to your existing customer base — massively increasing the value of your company and your competitive advantage against competitors.
Unfortunately, you may have built your entire engineering system to support just your first product.
Service classes are an encapsulation of logic that separates the ‘what’ of its purpose from the ‘how’ of its implementation. Building a platform that allows you to rapidly compose new products for your existing customers is merely the small matter of creating interfaces that perform valuable product operations. Imagine a hundred single-purpose APIs in your system that allow you to move money, sign up customers, list resources belonging to those customers, etc. all encapsulated such that you can use each one in isolation.
Creating those APIs will allow product engineers to build products quickly on top of them, while folks working on the underlying platform carefully move data around behind the APIs. The two tracks of work don’t need to be coordinated — the API gives us a decoupling.
You can move from this:
To this:
You’ll know you’re on the right track if your product engineering teams spend less time coordinating with whatever teams work on the internal platform. An interface replaces enormous amounts of tightly-coupled planning.
How to think about security
Now that you’re working at the level of a whole system, let’s address security. No matter what engineering roles you’ve had you’ll do great security engineering work if you keep this one rule in mind:
Simplicity, correctness, security, scalability, and maintainability are all neighbors. When we’re far from one of them we’re far from all of them.
Twitter had trouble scaling in the early days. Nick Kallen popularized the idea that you can’t make something scale by adding “magic scaling sprinkles.” The same is true for correctness, maintainability, and security. You can’t bolt on correctness to a busted system. You can’t just “do security” for a quarter to prevent security breaches.
Security is, more than anything else, a result of a simple design implemented correctly. Something is either simple and obviously secure, simple and obviously insecure, or it’s too complex to ever make secure. Your security team can only help you after you’ve refactored your system into a thing that’s so obvious any new hire can immediately make sense of it.
If a company is valuable with small amounts of data then that data is likely very important. That means a data breach is worse for you than for other companies. Leaking sensitive data functionally ends your company . That’s bad, but the damage to your customers is even larger. Your data is people’s home addresses and names and bank accounts and personal preferences. A breach in your system means that data is now in the hands of the highest bidder. If you have git access to a system that might expose sensitive customer data it’s your professional responsibility to fix it. Don’t wait for your manager or CTO or PM to ‘allow’ you to fix it . Just fix it. These are people’s lives.
How to prioritize product work versus maintenance
There are two investment models for engineering:
- Creating new value
- minimizing the cost of existing value
Product engineering uses #1, platform/foundation/infrastructure engineering uses #2. If there’s a single leadership team trying to prioritize projects from both groups they will always pick maximizing new value. They’ll do this until the cost of that value is so high that it wipes out the gains.
The way around this is to determine how fast you’d like to go now versus how fast you’d like to go in the future. And use that model to fund the percentage of people you put on increasing value versus minimizing cost. These need to be separate leadership teams, each focused on just one of those investment models.
For many companies it works out like this:
- When you’re starting out you want 100% of people maximizing value because there may not be a tomorrow, much less a next year.
- When you’ve reached product market fit it’s important to switch this up and see if you can lose a year of value creation to gain a year of cost reductions — earning yourself a step-function for future growth.
- When you have a shot at becoming ecologically dominant in your industry it’s important to put nearly 100% of people on cost reductions until the competitive moat around you gets massive.
- Then, if you’re ecologically dominant you can add huge new headcount to do value creation.
This is a slider you can play with at any time to match the risk model of the company. But being unaware of the tradeoffs means you’ll either reduce cost without producing value (see: 90% of infrastructure/tools startups) or increase value until you choke yourself and a leaner competitor comes through and steals all your victories (see: every company that Amazon has annihilated).
If you’re an engineer on the side of the org that maximizes value then one of your main jobs is deciding when some component is so important that its cost needs to be minimized. Then you have to productionize that component and hand it over to the other side of the org.
If you’re an engineer on the cost-reduction side you need to consolidate all the technologies and make the whole system hum along with zero maintenance. You also need to help product engineers upgrade their best stuff until it’s in a shape that’s maintainable.
How to extract services from a monolith
Service extraction is now an entire field of engineering. But the basic rule here is simple: You cannot run from your poor domain modeling. No matter what application you send your poorly-factored code to the pain will only increase.
The problems with “let’s extract this into a microservice” are (1) there’s no such thing as a microservice and (2) you need to fix the data dependencies first or you’re in for a world of hurt.
That said, there are some simple patterns to follow that will help you as you extract things from a monolith into new applications (or parts of the monolith that are more separate).
Extract verbs, not nouns
You cannot extract User
to a service. What would that service do? Just give you the data from the users
table? Sounds like you’ve just moved a database table super far away from you. Have fun with that.
But if you extract the concept of, say, approving a user to a service then you’re simplifying things. The monolith used to know all the steps of how a user was approved. Now that you’ve extracted all that logic and the intermediate data to perform the approval, the monolith can just have an approved_at
timestamp. If anyone wants more data on the approval they can go to your new UserApprovals
service to look up the details.
Learn in public and only do high-quality work.
I’d like to leave you with one last exhortation. The best engineers I’ve ever worked with (like these) have two qualities I’ve observed:
- They never, ever do work that’s less than their best
- They learn in public, never hiding their process or their mistakes.
I’ve noticed that each engineer I know has roughly a specific speed at which they work. No matter how many hours we clock in our career the speed doesn’t really increase. And when we work at a higher level of quality the speed takes a hit, but only briefly. Then you’re back to full speed but you’re better.
Multiple times in my career I’ve made the decision to adopt a higher bar for my own work. Each time it slowed me for a bit but then I sped right back up. This, as far as I can tell, is how great software engineers get that way. Their brains aren’t different than yours or mine, they just have higher standards for themselves.
To that end:
- Put as much effort into naming things as possible. Never cut corners on naming, it’s basically the whole job.
- Always write code comments that are as expressive and clear as possible, including ASCII art drawings if necessary. When you edit any code, update the comments. This is more work but it’s higher value. Do the highest value work.
- Don’t leave
TODO
s in code unless you’ve tracked a ticket and link to the ticket in theTODO
. - Never fix a bug without fixing the underlying design flaw that allowed it to happen. Even if the real fix takes two weeks, do it. Any place that doesn’t let you fundamentally fix the system that you’re in charge of is a place you don’t want to work.
- Make data migrations as freely as you make code changes. If someone looks at your database they should not be able to guess at what your code used to be.
- Before you merge a PR ask yourself “If I had more time, could I do this better?”. Take the time, do it better. Anyone who’s frustrated by that can be frustrated. They’ll be very, very happy in 9 months when the software works well and you’ve grown a lot.
Many thanks to my dear friends at Gusto for my time there and for the opportunity to better articulate my approach to technical leadership.
[1] During the time of the Square IPO all of the data for the dozen-plus products still fit into a single MySQL database under one giant Rails app.
[2] Please tell me I’m wrong.