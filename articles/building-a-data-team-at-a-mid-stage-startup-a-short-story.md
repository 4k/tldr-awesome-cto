# Building a data team at a mid-stage startup: a short story

**Source:** https://erikbern.com/2021/07/07/the-data-team-a-short-story.html
**Section:** Data


---

Building a data team at a mid-stage startup: a short story
I guess I should really call this a parable.
The backdrop is: you have been brought in to grow a tiny data team (~4 people) at a mid-stage startup (~$10M annual revenue), although this story could take place at many different types of companies.
It's a made up story based on n-th hand experiences (for n ≤ 3), and quite opinionated. It's a story about teams and organization, not the tech itself. As a minor note, I deliberately use the term “data scientist” to mean something very broad.
July 1: morning
It's your first day as head of the data team at SuperCorp! The CEO gave a quick but passionated pitch during your interview process how the world is changing and how the company needs to keep up with all the crazy data stuff going on. They whole exec team is super psyched.
The first few hours, you get access to all the major systems. You start browsing around in the Git repo and discover some interesting code. It looks like a neural network for churn prediction. You start to parse through the code but you're interrupted by a calendar notification that you have a 30 minute intro meeting with the Chief Marketing Officer.
The CMO is super energetic. “We're so excited you're here”, she says. “I recently talked to my buddy at HyperCorp who runs marketing and they are working with a vendor to use AI for user segmentation. Pretty cool! I can't wait for you to sink your teeth into it.” After a bit of chit chat, you start to probe into the data practices of the marketing team. “How is the customer acquisition cost looking”, you ask? “Well…", the CMO says, “pretty awesome actually. Our data scientist ran the numbers, and our online ad cost per click keeps going down.”
You're a bit confused because you were told all data scientists would report into the data team, but apparently other functions have their own data scientists? You make a note to follow up.
The CMO continues: “The real problem is that the growth team aren't converting all the traffic we're driving to the site.”
You ask if there's a dashboard to look at to see the conversion funnel but the CMO says it's the growth team's job to convert the leads.
Later that day, you spend time with some of the product managers. There's just been a big redesign of the start page and the lead PM of that effort is really excited because the number of user registrations went up by 14%. You ask them if the difference is statistically significant but you get a blank stare back. “That's not my job to figure out, that's your team”, the PM says. “Last time we asked them, they said they didn't have the data, and it would take months for them to get it.”
For whatever reason, you can tell that the product manager has more to say, so you let her continue
“Besides, amazing stuff isn't built on incremental changes. We decided not to A/B test this change because sometimes you need to make big bets that takes you out of your local maxima. Steve Jobs didn't A/B launching the iPhone! My team crushed it delivering this launch two days before the deadline and that's what matters!”
You try to look busy by scribbling down some notes in your notebook.
You spend the rest of the day talking to your new team. It's a small team of only three people, but you have been given a budget to grow it to 10 by the end of the year. The people in your team are clearly excited by your arrival. They walk you through what they built so far. There's the neural network for churn prediction that you saw earlier. There's a notebook with an implementation of a whole recommendation system for finding related items to buy. There's a lot more stuff, some of it quite cool.
You notice a a lot of the code starts with very complicated preprocessing steps, where data has to be fetched from many different systems. There appears to be several scripts that have to be run manually in the right order to run some of these things.
You ask the team why they haven't been launced in production. The data team looks frustrated. “When we talk to the engineers, they say it's a very large project to get this to production-level. The product managers have put it on the backlog, but they keep pushing it off because other things keep coming up. We need executive support for this.”
July 1: afternoon
Later in the day, you talk to the head of supply chain. He doesn't seem as excited as the CMO. “Frankly, I don't know if I need help from the data team”. he says. “We don't have those types of problems. What I need is business analysts. I have a whole team, and they are spending hours and hours every day working on a very complex model. They don't even have time to answer basic questions I have. I have a whole spreadsheet full of questions I'm dying for answers to.”
You look at the spreadsheet and discover things like: What's the conversion rate of customers who filed a support ticket and got a ticket resolution in <1h versus the conversion rate for the customers who got a ticket resolution in >= 1h? Break down by order value in buckets of $100 intervals.
When you ask about the “model”, it turns out it's a very complex thing in Google Sheets with lots of VLOOKUPs and data that has to be copy-pasted into the right tab in the right format. The data is updated daily and the output of the model determines the team priorities for the day. Not just that, but they rely on the spreadsheet to calculate payments to the vendors.
You go home that day and pour a large glass of whiskey.
What's happening so far?
This is basically a (somewhat cynical) depiction of things that may happen at a lot of companies early in the data maturity stage:
- Lack of data, and fragmented data
- The product is poorly instrumented so data often doesn't exist in the first place
- A fragmentation of data systems, with data spread out over many different ones
- Brittle business processes driven by data but with little or no automation
- An unclear expectation of what the data team's job is supposed to be
- Data scientists hired to do R&D and figure out some way to deploy AI or whatever — as a result not having any clear business goal
- Data team complaining about it being hard to productionize ML, yet the product team doesn't really seem to care about the feature
- People in need of “English-to-SQL translators”
- A product team not trained to be data driven
- Product managers not thinking about data as a tool for building better features
- A lack of alignment between what product teams want to build versus what data teams have
- A culture that fundamentally is at odds with being data driven
- A culture of celebrating shipping, versus celebrating measurable progress and learnings
- To the extent teams actually use metrics, they are inconsistent, poorly measured, and in some cases at conflict with other teams
- No data leadership
- A fractured data org with various data people reporting into other functional areas
- Other departments not getting the help they need, so they work around the data team and hire lots of analysts
- Lack of standardizations of toolchain and best practice
Wow! This is depressing! Let's talk about what you can actually do to break out of this.
July 8
The next week you start setting a new direction for the data team. One of the people in the data team turns out to have a bit more experience with infrastructure, so you put him in charge of setting up a centralized data warehouse. Right now, you just need the fastest route to get data into one place. The plan is basically to just dump the production database tables into the data warehouse every hour.
It turns out the framework you use for ad tracking on the frontend makes it easy to export the huge event logs into the data warehouse, so you set that up as well.
You make a mental note that this is tech debt you're going to have to revisit later.
Fig 1: Extremely crude distillation of how the data gets into the data warehouse
You work with the recruiting team to define a profile for a generalist data role, that emphasizes core software skills, but with a generalist attitude and a deep empathy for business needs. For now, you remove all the mentions of artificial intelligence and machine learning from the job posting.
You spend a bit more time with the various data people that do not report to you. The data scientist in the marketing team is a young person and you can tell she's super excited to talk to you. “I've always wanted to become a data scientist, and I can't wait to learn from you” she says.
Later that day, you call your friend who runs a coding bootcamp and ask them if they have any great SQL training classes. They have, so you set something up for later that month.
You start working on a presentation for the product team about A/B testing and how it works. You showcase many examples of tests with unexpected outcomes from your previous experience, and you make parts of the presentation a bit interactive where the audience has to guess whether test or control won.
You track down the CEO's executive assistant and get some time on her calendar later that week. Your goal is to figure out a few metrics she wants reported on weekly in an automatic email.
Later that week, you talk to a few of the business analysts in the supply chain team and you realize they are also reasonable people, but they seemed scarred from previous interactions with the data team.
One of them has experience using SQL in his past job. He has a question for you about conversion rates that you realize should be possible to answer with the few tables that are already replicated to the data warehouse, so you give him access and tell him to give it a shot. You don't really know what to expect but figure it's worth a shot.
You set up weekly 1:1s with a number of key people across the org that need data. The point is to find data gaps and opportunities and dispatch it to the data scientists. Some of your data scientists are a bit disappointed since the research work needs to get deprioritized. “We need to focus on delivering business value as quickly as possible”, you say, but you add that “we might get back to the machine learning stuff soon… let's see”.
September 1: morning
It's been three months, but you feel like you're starting to make progress with some of the stuff. In your weekly 1:1s with various stakeholders, you keep finding huge blind spots and opportunities for data to make a difference. You use these things as a forcing function for a lot of core platform work. In particular, many pipelines need to be built to produce “derived” datasets. There's a high upfront cost of those analyses, but subsequent analyses are much easier once the right datasets have been built.
You have started opening up access to the data warehouse internally to other teams in other departments. Some of the people are starting to pick up SQL and doing a lot of basic analyses themselves. An early win is that one of the junior product managers discovers that the conversion rate on iOS Safari is extremely bad. It turns out there's a frontend bug with local storage that's a one-liner to fix.
When you're thinking about all the progress you've made already, you're suddenly interrupted by an email from the head of supply chain. He's pissed. Apparently nothing is working with their model and it's a big problem for them.
You immediately send a Slack message to the person you know there. He's the business analyst who eagerly started writing SQL when you gave him access. It's super stressed. “The table in the database changed, and suddenly our SQL query we use to populate the spreadsheet generates nonsense output”.
When you look at the SQL query, you almost spit out your coffee. It's a 500 lines long query. The author of the query seems apologetic but at the same time a bit annoyed. “We kept coming to you several times asking for help with these questions”, he says, “and you told us you didn't have resources, so we built it ourselves”.
The data scientist in your team who gets assigned the monster SQL query isn't happy. “That team is stupid for writing those queries… we told them this would happen. These MBA types are useless. Besides, I was hired to work on machine learning, not to debug SQL queries”, he says. You're desperate so you try to dangle a carrot in front of him. “Please try to do what you can, and I promise we'll find some cool machine learning problem for you later this month”, you say.
September 1: afternoon
Later that day, you're in a meeting going through recent launches. The product manager of the checkout team goes through a major overhaul of the credit card flow. But when you ask him if they saw any improvements on relevant metrics, he is confused. “We haven't had time to look into that”, he says. You're disappointed because just a crude analysis would have been very easy to do for one of the data scientists.
At least, later that day you feel a bit better. The data scientist in the marketing team emails you and says she's talked to her manager. The CMO is totally fine if she reports to you, but makes it clear that “I need her 100% of the time dedicated to marketing.” You loop in the HR and asks them to make the updates in the internal systems to do the management change. Even though she's obviously very junior, you have been impressed with her ability to grasp complex business problems.
You wrap up work that day at 9pm and pour a big glass of red wine for yourself. The bottle is already open and you don't want the wine to go to waste, so you drink the rest of it too.
What's happening?
You're starting to lay the most basic foundation of what is most critically needed: all the important data, in the same place, easily queryable. Opening up SQL access and training other teams to use it means a lot of the “SQL translation” goes away.
The flipside is, some teams will go too far with their newfound freedom. It's tempting to prevent this by putting very strict guardrails on access to data, but this can often have more drawbacks. People are generally mostly rational, and do things that generate positive ROI for the business, but they might not understand what the data team can build for them. That's your job to demonstrate!
Similarly, with the checkout team you see something similar: there was a simple analysis your team could have done, but didn't happen, because that team didn't know who to ask.
These are primarily organizational challenges. Teams don't know how to work with the data team. You're probably a bottleneck, even though you don't realize it. Other teams will build around the data team. Lots of “simple” analyses are not getting done.
What I think makes most sense to push for is a centralization the reporting structure, but keeping the work management decentralized.
Why? Primarily because it creates a much tighter feedback loop between data and decisions. If every question has to go through a central bottleneck, transaction costs will be high. On the other hand, you don't want to decentralize the management. Strong data people want to report into a manager who understands data, not into a business person.
Fig 2: Data team with centralized backlog and centralized management
Instead, push out the resource management to other teams. Given them a handful of data people to work with, and let them work with them. Those data people will be able to iterate much more quicker, and will also develop valuable domain skills. This reduces the need for other teams to work around the data team and hire their own resources.
Fig 3: Data team with decentralized backlog but centralized management
A good thing is to some extent your results drive organizational centralization in itself: the junior data scientists in the marketing team moves into your team because she wants to work for you.
September 2
Your data team at this point has grown to six people. One of them is super busy with the infrastructure related to the data warehouse. For the other five, you assign each one of them to a team:
- One of them is assigned to the onboarding product team.
- The second is assigned to the supply chain team
- The third is assigned to the checkout team.
- You already have the data scientist from the marketing team working on marketing
- The final person is assigned to support the CEO and helping with investor/board decks
You send out an email to a large group of people outlining this change, and make it very clear who people should work with for their data needs. As you hire people going forward, you are planning to assign them to different teams throughout the company. Mostly product/engineering teams, but in some cases other teams.
January 3
You start the day with a frustrating email. One of your data scientists has decided to leave. “I'm going to AcmeCorp to join their new machine learning team”, he writes. You're not going to try to persuade him to stay. Frankly, he hasn't seemed particularly happy for a while, and you don't have much work he would be excited about.
You have a bunch of new people in the team that are more excited. Most of them are people who know a bit of software engineering, a bit of SQL, but most importantly have a deep desire to find interesting insights in the data. You think of them as “data journalists” because their goal is to find “the scoop” in the data.
One particular member of your team is working directly with the onboarding team. She talks to her product manager pretty much every day and the team loves her for the insights she's discovered. For instance, there was a big friction point where the onboarding flow asked for the customer's address even though it wasn't needed. Removing that step increased conversion rate by 21% in a subsequent A/B test. It wasn't easy to find this initially because the data model in the database was very complex and she had to build a set of ETL jobs to “flatten” the data into tables that are easier to query. But a bunch of Python jobs chained together did the trick.
Later that day, there's a quarterly review of all the major projects that happened. It's a big deal, and the CEO is in the room. She's excited about all the progress that's happening.
When the turn comes to the growth initiatives, the lead PM presents a new splashy landing page redesign that they launched. The PM points out several times that the team of 20 engineers was working overtime to hit the deadline and they did it. She walks everyone through the amazing job the designers did. It's beautiful. The CMO was very involved with the product because they made a big bet on direct mail as a part of the redesign. Everyone looks at the CEO to see what she thinks.
She's quiet for a while but then opens her mouth. “What are the metrics so far? Do we know if the customer acquisition cost went down?” she says, and you smile to yourself, because you've been hoping for this question.
The PM who put together this slide says they actually ran an A/B test and there are numbers in the appendix of the presentation. It shows a jumbled picture. Some of the metrics went up, and some went down. There's no result that shows a significant outcome. There's a table summarizing some early numbers for customer acquisition costs but the numbers look quite bad. The CMO emphasizes that the numbers are “still baking” and that for this type of campaigns, it can take many months for the users to transact.
You send a Slack message on your phone to someone in the data team that they should do a cohort plot of these things instead next time.
What's going on?
The good news is that the product team is starting to experiment with A/B tests. The bad news is that it's ignoring the results and that projects seem mostly driven by milestones and artificial deadlines. The excellent news is the CEO is pushing for teams to use data as the truth.
Once there is an organizational pressure to be more data driven, this is a time to accelerate the way the data team works with other teams. In particular, people at the highest level will start to focus more on metrics, and it's your responsibility that the data team works with them on it. One simple thing that goes a long way is to work with every team and make sure they have their own dashboard with the top set of metrics they care about.
Fig 4: Different services for different layers of the org drives the most progress
April 1
Almost all of the old machine learning work done by the data team has gone nowhere with one exception. One of the data scientists who works with the inventory product team gets really interested in the earlier work on recommendations. She's one of the new team members you hired, who has a bit more of a generalist background. She picks up the notebook with the recommendation system work, and is able to turn it into a small Flask app deployed internally.
The product manager for the inventory team is ecstatic when she sees it. “How do we ship it?” she asks. One of the metrics the team tracks is average order value and she thinks this could drive big improvements.
A quick estimation reveals it's still a big problem to make it scale, but your data scientist has an idea. “What if we only launch it for 1% of all customers?” She says. “We could have it powered by a dumb cron job and pregenerate all the recommendations in a database. I think I can hack something together in a few days.” Everyone's excited about it so she gets started.
You have been spending a bit more time with the supply chain team and discovered a lot more gigantic SQL queries used for various business-critical things. They break a lot but your team is rewriting a lot of it into proper pipelines run by code. The head of supply chain wants more of your team. “Once you started getting involved, my team of business analysts are getting so much more done,” he says. “I'd do anything for you to hire more data scientists to support me!”
OK, what's happening here?
First of all, there's a glimmer of hope for some of the cool machine learning work. It seems like the product team is finally excited about launching the recommendation system as a small test. It was previously stuck because the product engineering team couldn't estimate the work and didn't want to commit to it, but the data team didn't have the practical software skills to bring it to something where the work of productionizing it is more tangible.
What resolved this was the data team taking it one step further and actually building a demo. Not just does it bring it close to production, it also shows the potential in a more clear way.
It's easy for data teams to feel defeatist when these projects stall, like they were hired to do this cool AI stuff, but now the executive support went away. In practice I think it's more common they just didn't take it upon themselves to get the work to a place where it demonstrates value and is reasonably easy to ship.
The other thing is, note what's happening with the supply chain team. The journey is roughly:
- That team started out with their own “business analysts” (outside the data team) but need the data team to run queries for them to get data
- Those business analysts are starting to run queries themselves with the help of the data team
- They start to build up “shadow tech debt” (in this case monster SQL queries) which first causes a bunch of friction with the data team
- The data team starts embedding into the team and helping them get to a better place
- Because of the embedding, the need for business analysts goes down and data scientists goes up
Note that you took on a lot of “tech debt” earlier when you started dumping the production database tables straight into the data warehouse. Data consumers downstream will have SQL queries that break a lot. Over time, you're going to have to add some sort of layer in between, that takes the raw data from the production database and translates it into various derived datasets that are more stable and easier to query. This will be a LOT of work to do right. It's probably also needed for security reasons: you need to strip out lots of PII in the production data.
July 1
It's planning meeting for Q3. Previously, these have often turn into big debates about what “bets” the company is making for the next few quarters. This time, you start by going through the company's high level key results. Each team then has sub-metrics that constitute a more granular breakdown of the top level metrics.
It's clear that your work with the product management team has paid off. The PMs often justify their investment in various projects by talking about what they learned running tests, or what they discovered in the data.
A major win is that one of your data scientists working with the checkout team discovered a major bug where users would hit the back button at the confirmation page which would cause the cart object to end up in a bad state. When they fixed this, there was a dramatic improvement in conversion rate.
Another insight has been that traffic from different ad campaigns have very different conversion profiles once they land on the site. It turned out some campaigns had very cheap clicks but converted terrible. Some other campaigns were quite expensive but those users convert extremely well.
Since you're now tracking the UTM parameters and tying it to the account creation, you can now measure the conversion rate from ad click to purchase. This wasn't possible before all the data was brought into the same data warehouse and normalized so you can query it easily. Working with the marketing team, the main KPI is now end-to-end customer acquisition cost, rather than cost per click.
Another exciting news is that the 1% recommendation system test has done exceptionally well. Even though it's a very substantial project to scale it up to 100% of users, the CEO greenlights the project.
Of course, all outcomes aren't positive. There's been a lot of tests that didn't work out. One of the first slides describes a test you ran where shipping is baked into the price rather than charged separately.
It's quiet in the room for a while until the CEO starts talking. “What did you learn from this?,” she asks. This leads to an engaging conversation where the outcome is to run a series of follow-up experiments to get to the bottom of what happened.
You go home that night and pop a champagne.
What just happened?
You made it. You have transformed the organization to be truly data-native. The data team works cross functionally with lots of different stakeholders. Data and insights is used for planning. Data is used to drive business value and not a standalone lab with unclear goals. The company is working in an iterative way instead of big “waterfall” style planning, with quick data-driven feedback cycles. Metrics are defined in such a way that people feel a responsibility for generating business value. The data culture is driven both from above (the CEO pushing for it) as well as from below (people in the trenches). It's OK to fail if at least you learned something from it.
Congratulations — you deserve that champagne!