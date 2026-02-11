# How to Scope a New Feature

**Source:** https://www.prodify.group/blog/how-to-scope-a-new-feature
**Section:** Project management


---

While consulting with a client last year, one of the challenges I helped the team with was their process of planning and releasing new features. In particular, they wanted to get better at:
- Identifying success metrics for new features before any work started to ensure alignment
- Understanding how a new feature was going to be released - what was first, second, third, etc. and which specific customers might use / buy that feature?
- Measuring the impact of a feature after it was released
The Ticket Template
With that in mind, I created a template for new features, which can be broken down into its different phases, which are borrowed from the way Google releases features. (My manager at Opower came from Google, so I got a flavor for their product management style.)
Planning Phase
- Document customer job-to-be-done / problem and customer success metrics and goals [Product]
- Conduct / compile relevant user research and data analytics [Product and Design]
- Draft press release / blog post (for internal use only) [Product and Marketing]
- Determine pricing strategy (premium feature/cost vs included in SaaS subscription) with customer / prospect level projections [Sales]
- Document business success metrics and goals (revenue, retention, strategic progress, etc) [Product]
- Identify Alpha, Beta and GA customers or prospects with sales / customer success [Product]
- Document envisioned UX and break that down into Alpha, Beta and GA UX [Product, Design and Engineering]
- Document technical architecture design to support GA UX [Engineering]
Alpha Phase
- Document Alpha goal(s) / exit criteria [Product]
- Build and Test Alpha [Engineering]
- Launch Alpha [Engineering]
- Update documentation [Customer Success]
- Collect Alpha feedback [Design]
- Prioritize critical Alpha feedback [Product]
- Address any critical Alpha feedback [Design and Engineering]
- Update Beta UX designs with any medium-priority feedback [Design]
- Measure Alpha goal(s) and decide as a group whether to move to Early Access [Product]
Beta Phase
- Document Beta goal(s) / exit criteria [Product]
- Build and Test Beta [Engineering]
- Launch Beta [Engineering]
- Update documentation [Customer Success]
- Incorporate feedback into GA UX designs [Design]
- Measure Beta goal(s) and decide as a group whether to move to GA [Product]
General Availability (GA) Phase
- Build and Test GA [Engineering]
- Launch GA [Engineering]
- Update documentation [Customer Success]
- Update product change log [Customer Success]
- Create sales enablement content [Marketing]
- Update product marketing content [Marketing ]
- Update demo environment [Engineering]
- Market product launch (press release, event, etc.) [Marketing]
Post General Availability Phase
- Document whether feature / product met customer goals [Product]
- Document whether feature / product met goals [Product]
- Review goal progress internally [Product]
- Hold feature / product retrospective with product, engineering, design, customer success, marketing and sales to document lessons learned for future features / products [Product]
An Example: Chuckwagon's 5-Star Average Reviews
In our example Chuckwagon roadmap, we called out that one initiative in planning was to get an average of 5-star from 100 reviews in the app store to convince prospects the app was worth downloading and trying. Let's look at how we'd use this feature ticket template for that work.
In the planning phase, I'd do a few things:
- Remind the team that based on the above outcome KPI pyramid, the goal of 5-star average reviews is to increase revenue by increasing the Download Rate KPI in the bottom left. I might also note a hypothesis that if people saw a well-reviewed app they'd be more likely to try the app and upgrade to a paid subscription, although those are not the key success metrics for this body of work.
- I'd draft a press release with a headline like "New Chuckwagon App Lets You Plan Meals for the Week in 3 Minutes" (highlighting the customer outcome metric of time savings) along with some content explaining how personalized the meal plan is, how the recommendation engine works and 2-3 excerpts from 5-star app reviews.
- Analyze product usage behavior to understand who our active users are and what commonalities they might have (household size, zip code, age, etc).
- Interview users to understand whether they'd give the app 5 stars and if not, why that is. Then, I'd compile the top 3-5 areas to improve so we know what needs to change to get to 5 star reviews.
- Here's how I'd likely break the work up:
- Alpha: The biggest assumption here is that having 5-star reviews (or an average of 4.5+ stars) will increase the Download Rate KPI, which is # of downloads / # of unique visitors to our page in the App Store / Google Play. For this stage, I'd set the exit criteria as:
- 4.5+ average reviews with 5-8 reviews (and I'd just manually request the reviews from existing users who seem to be fanatics)
- 15% lift in Download Rate KPI
- Beta: From the Alpha, we should have some evidence that a high rating will increase Download Rate, I want to think about how to scale the process of requesting a review from users who I think will give us 5 stars. So, I'd spend 1-2 months addressing feedback from user interviews then build a simple automated review request experience. The exit criteria here would be:
- 4.5 average reviews with 20-30 reviews, garnered through no more than 1,000 users who participated in this beta (that means that 3% of beta users wrote a review)
- 15-20% lift in Download Rate KPI - on par with what we saw in the Alpha (no decline)
- General Availability: roll out the Beta experience of asking for reviews to all users (this could happen via email or in-app messaging to a targeted set of active users who are most likely to leave a 5-star review)
- I'd sketch out some mockups or ask design to do so for each phase above, and put the phases on a single slide to show stakeholders the progression of the UX.
Closing Thoughts
This template builds on the "Invest Proportionate to Confidence" concept we use when executing a roadmap - the general idea is that you must have quantitative and qualitative evidence to justify spending more time on a change to your customer journey.
Note: this post is an excerpt from a Google Doc we have in The Library. The document clients have access to also includes color commentary / links for these phases as well as an example user story ticket, with acceptance criteria. For information on becoming a Prodify client and gaining access to all of The Library, please contact us.