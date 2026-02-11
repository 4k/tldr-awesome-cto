# How to Write a Postmortem

**Source:** https://web.archive.org/web/20210618014202/https://blog.serverdensity.com/how-to-write-a-postmortem/
**Section:** Development process


---

How to Write a Postmortem
By
David Mytton,
CEO & Founder of Server Density.
Published on the 13th January, 2016.
When sufficiently elaborate systems begin to scale it’s only a matter of time for some sort of failure to happen.
Failure sucks, at the time, but there are significant learnings to be had. Taking the time to extract every last bit of insight from failure, is an invaluable exercise. We’d be robbing ourselves of that gift if we skipped postmortems.
So, despite the grim sounding name, we appreciate postmortems here at Server Density (and we’re in good company, it seems).
Keep reading to find out why.
Postmortems restore focus
When faced with service interruptions, we drop everything in our hands and perform operational backflips 24×7 until the service is restored for all customers.
This type of activity classifies as “important” and “urgent” (see quadrant 1 of the “Eisenhower Decision Matrix“).
When the outage is over, however, we need to consciously shift our focus back to what’s “important” and “not urgent” (see quadrant 2). If we don’t then we risk spending time on distractions and busywork (quadrants 3 and 4).
The discipline of writing things down requires us to take a pause, collect our thoughts and draft an impartial, sober, and fearless account of what happened, how we dealt with it, what we learned and what steps we’re taking to fix it.
Postmortems restore confidence
Right from the beginning, we decided we wanted to treat our customers the same way we wanted to be treated. Generally speaking, enterprise companies (Github, Google Cloud, Amazon, et cetera) have more engaged and invested technical audiences who want to know the details of what’s going on. Amazon, for example, offers some great postmortems. We wanted to offer something similar.
Communicating detailed postmortems helps restore our credibility with our users. It demonstrates that someone is investing time on their product. That they care enough to sit down and think things through.
When it comes to service interruption, over-communication is a good thing. As is transparency, i.e. acknowledging problems on time and throwing the public light of accountability on all remaining issues until they’re resolved. Going public provides all the incentives we need to fix problems.
How we write postmortems
Our postmortems start their lives as long posts on our internal Jira Incident Response page.
Internal outages might not affect our customers but they do take a toll on our engineering team (for example, server failovers waking someone up). We treat those with the same priority and focus. As advocates of HumanOps, we’re all about having the right systems in place so that operational issues don’t spill over into our personal time and impact our wellbeing.
In case of an actual service outage, we replicate the same postmortem to our dedicated status page (we filter out obvious security specifics). Here is a case that started from Jira (see above) and graduated to our status page:
Postmortem timing
While the crisis is still unfolding we publish short status updates at regular intervals. We stick to the facts, including scope of impact and possible workarounds. We update the status page even if it’s just to say “we’re still looking into it.”
It usually takes a week, from issue resolution to the point when we’re ready to author a full postmortem. That timeframe affords us the opportunity to do a number of things:
- Rule out the possibility of follow-up incidents. Ensure the problem is fixed.
- Speak to all internal teams and external providers, compare notes with everyone and agree on what went wrong. Mind you, getting in touch with all the right people is not always easy. The outage might’ve occurred over the weekend or during local holidays or the engineer might be on their off-call day.
- Decide on a timeline for implementing strategic changes to our process, infrastructure, provider selection, product, et cetera.
Postmortem content
Postmortems are no different to other types of written communication. To be effective, their content needs a story and a timeline:
- What was the root cause? What turn of events led to the server failover? What roadworks cut what fiber? What DNS failures happened, and where? Keep in mind that a root cause may’ve set things in motion months before any outage took place.
- What steps did we take to identify and isolate the issue? How long did it take for us to triangulate it, and is there anything we could do to shorten that time?
- Who / what services bore the brunt of the outage?
- How did we fix it?
- What did we learn? How will those learnings advise our process, product, and strategy?
Who writes a postmortem
Our status updates are published by whoever is leading the incident response or happens to be on call. It’s usually either the ops or the support team.
Once the issue is resolved, the same people will be expected to draft a postmortem on Jira for everyone to comment and discuss. Once that review is complete, as the CEO, I will then publish that postmortem onto our dedicated public page.
Summary
Successful outage resolutions go hand in hand with comprehensive postmortems. If you don’t take the time to document things properly, you rob your team from the opportunity to learn. This opens up the possibility of repeating the same mistakes. You also miss out on an opportunity to grow as a company.
What about you? How do you deal with failure? Do you write a postmortem, and who is accountable for it?