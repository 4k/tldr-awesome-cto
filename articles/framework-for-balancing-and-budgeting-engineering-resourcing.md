# Framework for balancing and budgeting engineering resourcing

**Source:** https://medium.com/engineering-operations/a-framework-for-balancing-and-budgeting-engineering-resourcing-d0cce0e6911c
**Section:** Money / Finance


---

A framework for balancing and budgeting engineering resourcing
--
Matt Eccleston formerly served as VP of Engineering and Growth at Dropbox, and from 2013–2019 helped the company scale from hundreds to thousands of employees. Prior to that, Matt spent 13 years in various Engineering leadership positions at VMware, helping it scale from tens to tens of thousands. Matt now advises late stage startups as part of ICONIQ Growth’s Technical Advisory Board. Balancing and budgeting engineering resourcing as a company scales is one of the most frequent topics that comes up.
As an engineering organization grows, different types of questions and challenges start to emerge around the investments in time and people your organization is making and the return on those investments that come from the ever increasing engineering team.
Many mid-size startup heads of Engineering start to find themselves in the spot of trying to explain to the board why with their larger team they’re still not able to do all the things that they’d like, which leads to questions on where all the people in the org are going, and inevitably subsequent lower value conversations that get into the weeds of internal engineering processes and frameworks and the like in order to even tee up a justification for headcount. Or the discussion with the CEO and heads of Product Mgmt. and Marketing about how if we staff the full set of projects asked for we are dangerously mortgaging the future. Despite the effort to drive these conversations and educate parties on the complexity of, and challenges faced by engineering, doing so more often than not fails to fully align all parties on this.
Worse, in my experience this ‘failure’ typically isn’t experienced as direct, open conflict but more often, a false or at best partial alignment that results in a “ok, that’s fine for now, but we’d like you to report on the following metrics in the future” and a framework being handed to the head of Engineering to follow that the head of Engineering then frets over as neither valuable nor representative of the actual challenges faced.
A better solution of course is to have a framework in place before the need becomes urgent that allows the company to talk about, and prioritize engineering investments in a way that makes sense for engineering internally, and also is understandable for the rest of the business stakeholders, and that can focus the conversation on the levers and choices the business truly has, and avoids frustrating circular debates taking place at the wrong altitude.
So what this post covers is the sketch of an investment framework for engineering we used successfully at Dropbox during the several years leading up to the IPO as we needed to get more rigorous about our product roadmap and its velocity, and our engineering headcount and growth rates. It worked well for us as described, though since organizations and their challenges vary, it can also serve as a starting point, that can be adapted and improved, or simply to serve as inspiration to design an analogous framework to handle the specific challenges and quirks of your company.
Goals
So to set the stage, we had several problems we really wanted this framework to help with:
Annual strategic planning
Where were we investing last year, did that work well? What changes do we want to make this year? Has technical debt become a straight jacket for us? Is customer satisfaction suffering? Do we have a critical need as a business to get new capabilities to market in a specific time frame? Do we need to get more out of the massive army of engineers we’ve hired? The answer inevitably every year was yes! yes! yes! yes! to all of these. But we needed help teeing up a meaningful discussion at the company level about how to balance and set our priorities across these, and not let the one or two hot button topics steal all the oxygen (and people) away from the others.
Using the framework ultimately allowed us to, one year, set a company goal around “Refocusing on our (existing) customers” and another goal across a multi-year period on multi-site resiliency and the deep-internal to engineering projects across the infrastructure and application stack to achieve it. Both of these goals were very large lifts for many teams across engineering, but were also meaningful board level conversations when framed this way.
Team and group level alignment on priorities
Like many companies, we had a good amount of variability across teams and groups on the quality and persuasive powers of the various engineering and product leaders. This would lead to some teams to over-rotate on product roadmap at the exclusion of all else, and others to err towards over-rotating towards projects geared towards a payoff in future internal productivity.
We also had challenges aligning the more product oriented teams with those focused on internal infrastructure and tooling. By their very charters there was often a tension across those teams when it came to inter-team dependencies (a good example was our migration from coffeescript to typescript driven by our web platform team, that needed support from almost all product teams).
With this framework we were able to decentralize much of the conflict resolution around priorities and ongoing oversight of these types of challenges.
Transparency
A third challenge we had was an ability to talk about engineering to a company-wide audience in a way that was understandable, defensible, and illuminating. There was, similar to I suspect a lot of tech companies, real tension and skepticism (either visible or as hidden undercurrents) of engineering from other departments. Engineering has a very large and expensive headcount, and due to the nature of the work lacks the easily measurable and highly predictable nature of a sales or marketing organization, and this often raises the specter of mismanagement due to Engineering’s nature as a very expensive largely opaque box.
This framework allowed us to shine a light into this box, and achieve stronger alignment across different departments as to what engineering was taking on, and was viewed in a very positive light with all kinds of soft benefits. Trust was increased across departments and some of the mechanisms and politics that people and organizations used to compensate for lack of trust started to subside.
So without further ado let’s talk about the framework we used…
The framework
The framework was pretty simple to summarize. We categorized all engineering investment into 4 buckets (1 mandatory and 3 elective). And across the elective buckets, we set a rule of thumb target (at the overall engineering org level) for a 60%, 20%, 20% investment split across them.
The buckets are:
- Keep the lights on (KTLO)
- Elective investments
- Build new stuff (for customers) ~60%
- Improve existing stuff (for customers) ~20%
- Increase your productivity (not customer visible) ~20%
We’d set the targets annually, and ask teams to monitor and report on their investment breakdowns and associated roadmaps across these categories quarterly.
In this system, the categories are critical to get right. it’s important that the buckets are mutually exclusive and collectively exhaustive (MECE) of the work engineering is doing. It’s also important that they can succinctly map on to the type of value they deliver back to the business. So let’s flesh out their definitions a bit more each in turn.
Keeping the lights on (KTLO) vs. Elective investment
The first thing to be crisp about is what is truly mandated vs. elective investment. The reason for the focus on this distinction is it’s usually safe (and simplifying) to assume most companies are interested in “keeping the lights on” and preserving their current book of business. Companies rarely make a different strategic choice about funding for KTLO. So if you can define the work that is required to support just keeping the lights on, you can usually limit investment level discussion of it to simply what % of overall investment is going to that category and not get bogged down in the nuts and bolts of whats required to do so.
But it’s critical to have an honest baseline and be rigorously minimal about what is truly in this bucket, otherwise there’s a lot of room for “gaming” of the framework, which erodes the value and the trust that can be placed on it. So for our purposes we zoomed out to how a business focused audience such as our board or investors might define “keeping the lights on”, and defined it as the “minimum tasks to maintain the current level of service in the eyes of our customers”. This means maintaining the current service/product(s), but it does not mean building anything new, nor does it include investments to improve internal productivity (we’ll have different categories for those).
Following from that definition, this would typically include work in service of:
- maintaining current security posture (e.g. regular audits, administering bug bounty programs)
- maintaining current levels of service uptime (e.g. on call duties)
- service and ticket monitoring and troubleshooting
- addressing functional defects reported by customers
- regular/routine internal procedures (e.g. build and push duties which aren’t automated)
- staying up to date with external dependencies
- browsers, libraries, platforms, web services, partner changes, hardware etc.
Elective Investment bucket #1 — Building new stuff
The first and largest elective investment is building new stuff (or new marketable product capabilities if you want to get formal). This is the focus of most growth oriented companies and their engineering teams. These are the things that if built will allow new customers to be acquired, or expand the footprint within existing customers (customer acquisition and upsell). These are the things that people outside of engineering are most interested to see on roadmaps, that get mentioned in marketing material, and that provide differentiation.
This bucket is rooted in what can be explained to a customer as a new thing the product/service can do, that they will hopefully find valuable, that it couldn’t do before.
This does not include work that will be customer invisible, or functionality that might be a customer visible improvement but might be otherwise expected within the current set of capabilities (more on this in the next section).
Work in this category is typically:
- Adding a new product
- Adding a new feature
- Adding a new sub-feature
- Supporting a new platform or partner application (e.g. Alexa or Chromebooks)
Elective Investment bucket #2 — Improving existing stuff
While new capabilities are expected to drive customer acquisition and expansion, improving existing stuff (improving the quality of the product) is a category rooted in customer satisfaction. Customer satisfaction plays a key role in retention but also can boost conversion and even customer acquisition over the long run through strengthening reputation and brand.
This work is not creating the features that get someone to select your product or service in the first place, it is the work that ensures the product delivers on customer expectations around those capabilities they were looking for when they selected your product or service.
Work in this category would include:
- Customer requested improvements especially around putting a product into production
- Better performance and resource utilization (speed, scale, cost, battery life etc.)
- Iterations to improve adoption, retention and quality of life (e.g. better onboarding, usability)
- Increased product reliability and faster / more effective incident response
- Improved security posture of your product
Elective Investment bucket #3 — Increase your productivity
The last elective bucket has no direct customer facing surface area. Its motivation is ultimately internal to the company, in improving the productivity of the organization (often focused on the engineering org though can impact partner orgs like customer support easily as well). Productivity here formally means work output delivered by the organization per unit time per the size of the organization, or simply “more bang for your buck”. This may mean every engineer is X% more productive, or that the organizations throughput is increased by releasing more quickly, or that the % of KTLO work for the organization as a whole is reduced. In all cases it is allowing the organization to do more with same headcount.
Some categories this would include are:
- Better developer tooling, telemetry and support
- Testing automation
- Code restructuring
- Framework upgrade efforts that are motivated by reducing time to develop future projects
- Work to reduce the size of the KTLO bucket in the future (e.g. automation, elimination of toil)
Buckets summary
So to recap our four buckets:
- Keep the lights on (KTLO)
- Elective investments
- Build new stuff ~60%
- Improve existing stuff ~20%
- Increase your productivity ~20%
In our experience these truly can and do encompass all of the work that a reasonably large engineering organization is doing. There are of course corner cases, and if you roll such a framework out, you can initially expect to have to do some work educating and adjudicating on how certain projects fit into the framework, e.g. projects that span bucket types. At the same time, our experience was having projects to snap to this framework forced beneficial clarity from various project teams on exactly what their goals were. This led to better goal setting and KPI selection as a side benefit of rolling it out.
Tips on Operationalizing this
So the last thing to touch on is some tips on how we operationalized this framework.
Initial roll-out
First spend some quality time with engineering and product leadership getting their feedback, buy-in and clarifying ambiguity (an offsite can work well for this).
Communicate it broadly within engineering and product teams to define the framework for them (concrete examples help a lot), and define what it does (and doesn’t) mean for them, and how the broader organization intends to use it to make decisions. Perhaps the most critical point in this bucket is that the 60/20/20 ratio (or whatever you settle on) isn’t intended to describe every teams’ breakdowns, but to reflect the investments of the engineering org as a whole once it’s all rolled up. And of course, it’s a good time to remind that perfect accounting here is a non-goal. Good enough does the trick just fine.
Communicate the framework broadly beyond engineering to all partner organizations (we included this in an all hands that covered our roadmap, as a reframing of how we think about our roadmap).
Strategic Planning
The goal here is to align on the elective bucket allocations. Is 60/20/20 the right balance for our company for the next year? We’d typically begin the process with reviewing the previous allocation (even at the initial rollout we were able bucketize the previous year’s work well enough), discuss key points of what got done and what didn’t get done against our goals, and propose allocations for the coming year, highlighting any proposed changes based on our preliminary understanding of company level goals and priorities. This led to conversations around whether we had an aligned set of priorities, and if not what adjustments would be needed. These adjustments would either need to come in the form of changing the allocation, or reallocating future headcount growth to or from engineering.
Once we had alignment on the bucket allocation, this would roll into preliminary budget and headcount setting for the year.
In practice, we never ended up going too far away from the base 60/20/20 guidelines after all was said and done. We’d see some drifting up to 25% and down to 15% depending on the year, but rarely too far beyond that. To be clear, there are cases where further drift is warranted, but expect those cases to be somewhat exceptional.
For the KTLO %, it’s harder to provide as clear a rule of thumb that’s appropriate for different companies since the % can vary a lot based on structural factors around your engineering stack, maturity and growth rate. However it should be consistent enough within a given company to monitor and manage the trend. You should also definitely take heed to your initial reaction when you do this calculation for your team. If the KTLO % alarms you, good! Tee up the business trade-offs around investing to improve it (productivity bucket) vs. other elective investments, and bring them forward. That’s exactly what a healthy strategic planning conversation should include.
Group and team level review (Quarterly)
To have traction, the framework can’t appear at annual planning and disappear for the rest of the year. What worked well for us was asking teams to report on their allocation across these buckets on a quarterly basis. This was done as a relatively lightweight process led by the engineering directors and typically compiled by a program manager, and would consist of a roll-up and readout (typically attached to another existing forum with the team) of the expected vs. actual allocation in the previous quarter, and the expectation for next quarter.
These were typically low drama and relatively quick readouts, but served to re-enforce the strategy, and on occasion surface the conversations and provide feedback needed to the directors or their teams to make adjustments in future quarters so we could manage the engineering allocation globally for the year. But in our experience the simple existence of the framework itself and requiring teams to measure and communicate its targets did 95% of the work at the executive level.
Within groups and individual teams we also noticed that just the existence of the framework put a useful stake in the ground that all of these classes of work were important and needed to be consciously accounted for. We also saw directors align among themselves better and take action, for example when they saw their “keep the lights on” bucket was too high as a %, or how their lower allocations related to customer service ticket volume problems they handled.
All in all, it was a relatively lightweight framework for the teams to adopt.
Here’s an example of what a roll-up might look like just to make it concrete:
As a reminder KTLO % is out of Group size, and elective category %s are out of [Group Size - KTLO] as per the framework philosophy.
And here’s an example of how we’d talk about our roadmap:
So that’s it. For us, this framework turned out to be a pretty simple, reasonably light-weight and ultimately effective way to help tame some of the problems we were facing as we scaled. I hope this can prove helpful for you as well!