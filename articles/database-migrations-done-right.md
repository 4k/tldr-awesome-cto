# Database Migrations Done Right

**Source:** https://www.brunton-spall.co.uk/post/2014/05/06/database-migrations-done-right/
**Section:** Data


---

Database migrations done right
Published on 2014-05-06 19:20:24 +0000The rule is simple. You should never tie database migrations to application deploys or vice versa. By minimising dependencies you enable faster, easier and cleaner deployments
I thought this was well understood, and accepted by most developers. However a comment on a recent article I read reminded me that not everybody understands this, and I was also told recently by a coworker that things that I might think are “obvious”, may well not be to people who don’t have my background or context, so blog about them.
There are perceived to be lots of problems around how database schemas should be upgraded. Many developers make changes locally to their developer database and code at the same time. Then when it comes to time to release, they think that they can’t possibly separate the code and database changes from each other.
This is caused by the combination of the two concerns during their work, and sometimes by a lack of systems to support a better way of working.
I believe that in order to achieve this kind of easy separation, you need two things:
- The ability to work on small tasks at a time
- The ability to release your changes into production speedily
So how do you go about writing these magical schema changes?
Well Scott Ambler has written an excellent book, Refactoring Databases, which gives you most of the patterns necessary to achieve this. The book wasn’t intended with this in mind, so covers a lot of other stuff, but you can find patterns in there for breaking down changes into small chunks easily.
These patterns often break the change into multiple database and application deployments. For example, the pattern of adding a non-nullable column to a database schema could require:
- schema change to add a nullable column
- update the software to write to the nullable column and handle nulls on read
- perform data migration to update the null columns to have the correct data
- execute a schema change to set the column to not-nullable
- remove the null-handling code from the app
If you can execute schema changes or deploy code around once a week or fortnight, then executing that process could take you two months. If you can make these changes hours or minutes apart, then this is a couple of days work for a developer at most.
The application of these patterns requires understanding that you need to make very small changes, each released to live as fast as possible and with as quick feedback as you can get.
We can apply all of the database refactoring patterns by following one pretty simple principle:
Every change you make must be backward compatible with the rest of the system
So looking back at our add non-null column change we can identify it like this:
- Add nullable column to database - System keeps adding rows, nulls are fine, reads ignore the null
- Code change to write correct value to new rows, and handle reading unexpected nulls - Database doesn’t change, now we have some null rows and some rows with data
- Run data migration to fill the other columns - This might be a script, or a bit of code in the application, either way your app doesn’t care about any row, it handles data and nulls just fine
- Add the non-null constraint - The database now has no nulls and your new code is writing the correct data.
- Remove the code that handles the null case - it won’t happen anymore.
If you apply this rule you free up the ability to do rolling deployments of your servers, you can apply changes as fast as you need, and you gain a lot more control over your release process.
It does however require thinking about the changes, and breaking them down into the units of deliverable work (or tasks), and executing them in sequence. That’s hard for many teams to do if their workflow and supporting systems are designed around big releases.
However, once you do it, you’ll make releases of software much easier (simpler deployments = shorter cycle times = faster throughput generally), and you’ll find that thinking about the tasks in this way is actually much easier.
Final thought, is there anytime I wouldn’t do this? I’ve long said that greenfield projects that are in the early stages don’t need to do this, but these days I’m not so sure. The added benefit we gain from breaking our changes down this way, in terms of the increased throughput, I suspect very early on in development starts to pay dividends, so I’d start working this way pretty early on in the software lifecycle.
Addendum 1
Simon Jones, below, asked some useful questions, and I replied to him with quite a long response that covers some important points. It’s worth reading in full, but a couple of the main points I made were:
- You should be using a database migration tool for executing the change scripts in a reliable, repeatable way. I’ve used DBDeploy but there are others out there.
- ORM’s that combine the schema and code together inseparably are evil and should be avoided.
Oh and I realised that I forgot to mention to various people who I’ve discussed this topic at length with over the past few years, @philwils, @tackers, @steppenwells and @russss.
Addedum 2
Philip Wills pointed out on twitter that I clean forgot to explain one of the key benefits of doing this, and that is to reduce deploy time complexity. There’s enough stuff to cover there that I’ll probably do a second post to explain why you should do it, now that I discussed how to.