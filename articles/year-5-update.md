# Year 5 Update

**Source:** https://miguelcarranza.es/cto-year-5
**Section:** CTO Position
**Author:** Miguel Carranza

---

My role as a founder CTO: Year Five
Read time: 8 minutes.
It’s hard to believe that five years have already gone by since RevenueCat’s inception. In a matter of weeks, RevenueCat will become the company where I have worked the longest in my career. As Jason Lemkin says, it’s important to continuously reinvent the company and oneself every five years. It’s required to carry on and stay relevant the following five.
I had no doubts my role was going to evolve again. It has every single year, leading me to start this series of posts. But the remarkable part this year has been the internal transformation of RevenueCat. As we enter 2023, the company is more mature than ever before, with well-established processes, cross-functional teams, and leaders in key areas. The company has become a well-oiled machine, allowing us to deliver quality software at a faster pace. However, reaching this point was not without its challenges and it took a lot of hard work to get here.
Expectations vs reality
Last year, I had high hopes for revamping our onboarding, improving our delivery process, and strengthening our technical infrastructure. I am happy to report that significant progress has been made in all of these areas, even though I was minimally involved in these initiatives. This is a positive sign, as it indicates that the team was capable and I was no longer a bottleneck.
Team growth was another area I used to regularly report on. While we did not double the team this year, I don’t view this as a failure. At the start of the year, we were worried about not meeting our hiring goals, which led me to work closely with the recruiting team to remove bottlenecks. We managed to pick up momentum and had 208 interviews in March. However, in Q3, we decided to follow a more conservative approach and scale down hiring. This was a tough call for some, but the right decision in hindsight given the current macroeconomic conditions and increasing interest rates. It also allowed us to better focus and onboard new members.
| Metrics (EOY) | 2021 | 2022 (Planned) | 2022 (Actual) |
|---|---|---|---|
| Engineering Team | 17 | 34 | 25 (+47%) |
| Eng/product teams | 1 | 4 | 7 (+600%) |
| Developer Support Team | 5 | 10 | 7 (+40%) |
| Company size | 40 | 80 | 60 (+50%) |
| Countries | 10 | ?? | 12 (+20%) |
| Time zones | 7 | ?? | 8 (+14%) |
Highlights
- We started the year with only one cross-functional engineering team, with the plan of building another three. We ended with seven.
- We saw a slight improvement in the representation of female engineers, from 18% to 27%.
- We now operate using mature processes such as OKRs, 30/60/90 planning, customer issue triaging, cross-team calibrations, etc.
- We finally managed to meet in person, with two successful offsites and team meetings.
- The team made significant progress in future-proofing our infrastructure, with upgrades to our data platform, IOPs optimization, database upgrades, improved monitoring, and alarms.
- Our on-call processes were revamped, with the introduction of runbooks, shadowing, post-rotation reports, etc.
- We maintained SOC 2 compliance for the second year.
- We were featured at Google I/O!
- We had the first Hackathon in years and everyone had a blast.
- We had a major support breakdown but managed to fix it and come back stronger.
- I went on paternity leave and the company continued to thrive.
Lowlights
- Due to the focus on hiring and adapting to new processes, our shipping pace was slower in 2022 and some projects were killed before launch.
- Before our triaging and escalation processes were in place, customer needs would sometimes become a distraction to the teams or go unaddressed.
- There was some attrition. Whether it’s regretted or non-regretted, it’s never a good feeling.
- We experienced our worst outage in years.
- We were not able to dedicate sufficient resources to support entry-level developers.
- Building cross-functional teams required some reorganization and was generally successful, but some teams took longer to be productive, which even led to internal conflicts.
My day to day
The year started off with a double surprise for me and my wife - we found out we were having identical twins! But with the high-risk pregnancy, it was a rocky road ahead. Weekly ultrasounds and a few scares later, we welcomed home two beautiful, healthy baby girls.
This pregnancy may have prevented me from attending conferences and team retreats, but it also gave me the opportunity to prepare for my parental leave in a more conscious way. I knew the girls would come prematurely, so in Q2, I took every week as if it was my last. I made a few changes to my work routine to accommodate the upcoming leave
- I replaced weekly one-on-ones with my direct reports with office hours that could be requested by anyone in the company. They can be about anything: technical questions, historical decisions, company values, conflicts, etc.
- I documented everything from compliance to interviewing processes. Nothing that wasn’t common knowledge, but that we needed in writing.
- I removed myself from the critical path when interviewing candidates and trained other team members.
- I shifted my role from leading technical projects to being a technical consultant.
- I started working on internal tooling, which eventually became a new engineering team.
Regardless of the proactive preparation, having a VP of Engineering in place was what gave me peace of mind during my leave. In Q1, I worked closely with Bhavana providing context about the team and the expectations I had for her role. She took over all of my direct reports and brought in clear processes and expectations for the Engineering Managers. This gave me the leverage to focus on the big picture and tackle important issues as they came.
Coming back after my family leave
Returning from my 9 weeks of paternity leave, I was not sure what to expect. I wasn’t fully disconnected during my absence. I would talk with my co-founder every week, read emails and keep an eye on Slack, but for the rest of the team, I made myself unavailable on purpose. During this time, I started thinking that maybe, my job could be over. It’s a weird feeling for a founder. I managed to do the right thing, the company was operating just fine without me around. But would I have something impactful to do when I came back?
Oh boy, how wrong I was. My friend Jacob welcomed me back with open arms. There were new fires to fight!
Support Engineering
Our customer support was struggling, with our developer community and GitHub issues not receiving prompt responses. Half of the team was hired recently, we were not hitting our SLAs, and the morale was at an all-time low.
So, we made the decision to have the support team fall under engineering and report to me. This was natural given that the team consists of support engineers, who are technical. Doing tickets again was a rewarding experience. Interacting with customers and seeing the impact of our product on their businesses is a feeling that never gets old.
After talking with everyone on the team and doing a little bit of debugging, we came up with a new strategy:
- Split the team into “self-serve” and “sold” (which would work more closely with sales, success, and solutions engineering).
- Make Zendesk the operating system for the team, unifying all the other sources for tickets (GitHub issues, community,…). This prevents the overhead of context switching, also allowing centralized SLAs.
- Make the Support Engineering team more technical. Organize iOS development sessions as well as pair programming with engineers for customer-facing features.
- Work closely with product engineers to optimize triaging and escalation processes.
- Be more data-driven. Group ticket data in order to reduce the most common tickets by either improving our documentation, the product or building internal tools.
With these changes, we were able to quickly boost morale and improve response times.
2023: The Year of Shipping
In 2023, we will go back to the basics. We made investments to have the processes, teams, and leaders in place. We need to get our focus back to the two things that got us the initial traction obsessing with customers’ problems and shipping very fast.
We have a very aggressive revenue goal in our sights. To achieve this, we’re doubling down on product improvements for our larger accounts. We’ve neglected this aspect in the past, but that’s about to change with the creation of a new engineering team dedicated to go-to-market efforts. This team will work closely with the sales team and customers to quickly implement necessary improvements, sometimes even delivering same-day results. Like in the good old days. I’m personally excited about this balance between being responsive and long-term planning. Leading this team will allow me to get back into more technical work, stay in touch with customers, and set a positive example of fast shipping for the rest of the organization.
To ensure that our support workload increases at a manageable rate, we’ll be relying on internal tooling. I’ll also be spending more time conducting interviews again. We will continue to hire in 2023, but with a more limited headcount budget, every seat counts. We need to be selective to build the best team possible.
Learnings
- In 2022, we got the first batch of fully vested employees. I was a little bit nervous and honestly did not know what to expect. Maybe they’d miss the scrappy startup days and hate the new processes. Or maybe they would find a more profitable gig somewhere else. As of today, the first five are still working with us. It turns out that real startup people are the ones who not only enjoy the early stage but the ones who adapt and have a growth mindset.
- Maintaining compliance can become harder than getting certified for the first time.
- Setting up office hours was a perfect hack to recover a big chunk of my calendar. However, not everyone will be proactive in requesting them. I found that some people would schedule regularly, while others would never take advantage of them. It’s still important to have regular one-on-ones with key people.
- Moving support under engineering has proven to be a success and has strengthened the relationship between support and product. Investing in their technical skills not only made them more productive but opened up more career opportunities for the team.
- After a certain stage, it’s common to believe that the founders’ job is limited to building the organization. While that may be true to an extent, it’s crucial to stay connected with your users. This can be achieved through various channels like sales, interviews, or customer support, but the key is to truly listen to their pain points.
- My recent parental leave taught me that the workload for founders never truly goes away. Although executives can provide great support, it’s ultimately up to the founders to share the institutional knowledge and protect the company’s values. The real reasons for a founder to become replaceable are burnout, a lack of interest, an overinflated ego… or illegal stuff.
This one was, without a doubt, the most personal and hardest blog post to write of the series. To the point that I almost gave up. But the process reminded me of just how important it is to take a step back and reflect on the journey. This is only the beginning of a decade+ long adventure, and there’s still a lot of code to be shipped. I’ll see you again in 2024!
I hope this post was interesting. If you are facing similar challenges and want to connect and share experiences, please do not hesitate to reach out on Twitter or shoot me an email!
Special thanks to my co-founder Jacob for riding this emotional rollercoaster with me for half a decade, the whole RevenueCat team, and our valuable customers. I also need to express my eternal gratitude to all the CTOs and leaders that have been kind enough to share their experiences over these years. Shoutout to Peter Silberman, Alex Plugaru, Javi Santana, Pau Ramón, Matias Woloski, Tobias Balling, Jason Warner, and Will Larson. Our board members Anu Hariharan, Mark Fiorentino, Mark Goldberg, and the early believers Jason Lemkin, Andrew Maguire, and Nico Wittenborn.
Subscribe via RSS