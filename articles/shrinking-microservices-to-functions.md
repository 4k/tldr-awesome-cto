# Shrinking microservices to functions

**Source:** https://highscalability.com/blog/2017/3/27/faster-networks-cheaper-messages-microservices-functions-edg.html
**Section:** Architecture


---

RmFzdGVyIE5ldHdvcmtzICsgQ2hlYXBlciBNZXNzYWdlcyA9PiBNaWNyb3NlcnZpY2VzID0+IEZ1 bmN0aW9ucyA9PiBFZGdl
When Adrian Cockroft—the guy who helped put the loud in Cloud through his energetic evangelism of Cloud Native and Microservice architectures—talks about what’s next, it pays to listen. And you can listen, here’s a fascinating forward looking talk he gave at microXchg 2017: Shrinking Microservices to Functions. It’s typically Cockroftian: understated, thoughtful, and full of insight drawn from experience.
Adrian makes a compelling case that the same technology drivers, faster networking and cheaper messaging, that drove the move to Microservices are now driving the move to Functions.
The payoffs are all those you’ve no doubt heard about Serverless for some time, but Adrian develops them in an interesting way. He traces how architectures have evolved over time. Take a look at my gloss of his talk for more details.
What’s next after Functions? Adrian talks about pushing Lambda functions to the edge. A topic I’m excited about and have been interested in for sometime, though I didn’t quite see it playing out like this.
Datacenters disappear. Functions are not running in an AWS region anymore, code is placed near the customer using a CDN at CDN endpoints. Now you have a fully distributed, at the edge, low latency, milliseconds from the customer way of running code. Now you can build architectures that are partly in the datacenter, partly at the edge, and partly at the customer premises. And since this is AWS, it’s all, of course, built around Lambda. AWS Greengrass and Snowball Edge are peeks into what the future might look like.
There’s a hidden tension here. Once you put code at the edge you violate two of Lambda’s key assumptions: functions are composed using scalable backend services; low latency messaging. The edge will have a high latency path back to services in the datacenter, so how do you make a function based distributed application at the edge? Does edge computing argue for a more retro architecture with fewer messages back to a more monolithic core?
Or does edge computing require something completely different? Here’s one thought as to what that something completely different might look like: Datanet: A New CRDT Database That Let's You Do Bad Bad Things To Distributed Data.
Now, let’s see the future by first taking a tour of the past….
From Monoliths, to Microservices, to Functions
Ye Olden Days
10 or so years ago
Mostly 1 gbps network.
State of the art was a monolithic Java application connected to a big relational database.
Systems were decomposed using Web Services that exchange XML messages.
Sending XML over a slow network had high overhead. Just parsing XML is slow.
Since web services were slow the resulting architecture featured large servers with a relatively low number of messages exchanged between them.
The slowness of the system meant a request couldn’t hit more than two or three services before returning a reply, so it was difficult to decompose a monolith into smaller services.
Now
Network is 25 gbps.
Messages are Avro, gRPC, etc, which are 100x more efficient than XML.
Combining the faster network with better message formats means we’re 100x to 1000x more efficient at sending messages between servers. (Historical note: we’ve always had cheap messaging on Unix, people just forgot that when they went insane with XML.)
Now it’s possible to break an architecture up into many smaller services because it’s possible to make 100 microservices calls and return a reply within latency bounds.
Microservices became possible because of a technology change. A system could be broken up into smaller services where every service has a single responsibility.
Now it’s possible to a go a step further by breaking up microservices into the separate functions making up those services.
We can afford to connect all these functions together because messaging has become cheaper.
Five Epochs of Delivering Code
How much code do you want to put in something? How long does it take to build and deliver that code?
Ye Olden Days
Go to a vendor, buy a machine, put it in a datacenter, then code could be delivered to it.
Delivering code was a manual complex project all on its own.
There was some automation, but generally highly handcrafted release procedures.
Releases were every 6 months or a year and it was a complicated process that required a lot of testing to make sure everything would work.
Age of Agile - First Wave of DevOps
Code delivery sped up, with releases happening every two weeks.
Automation was needed to make it possible to release code that fast.
First wave of DevOps. Automation was put in place to get stuff done quicker. Chef and Puppet were used to update an array of machines with new code.
Second Wave of DevOps - Cloud, API, Developer Driven
-
Still have a problem: what if you need more machines?
-
This is where the cloud comes in: building elastic systems, the ability to provision on demand. Scale down when not using machines. Pay for what you use.
-
The cloud put an API between development and operations.
-
Developers work against a platform API to get stuff done.
-
Developers were able to drive operations by automating as much as possible.
-
Using APIs + elastic + developer driven it was possible to create Blue-Green deploys:
-
A new software release is rolled out on a new set of machines.
-
New software is run side-by-side.
-
When it’s verified the new build works the old machines are terminated.
-
No need to use Chef or Puppet. The Netflix architecture never needed them. Just deploy new stuff and create things from scratch instead of updating in place.
-
This is the idea of Immutable Infrastructure.
-
-
This sped up things a lot. It also enabled smaller pieces because the cost of delivery isn’t 6 months, it’s a day or a few hours.
-
The number of people needed to come together shrunk. An individual developer creating an individual microservice could use automation to roll it out as needed.
Standardizing Components Around Containers
This phase started a few years ago.
When deploying a new auto-scale group the instances take a few minutes to boot up completely and you pay by the hour. Deployments can take minutes to hours.
Works well for diurnal traffic patterns, where it gets busy during the day and quiet at night, it’s relatively easy to predict these patterns and auto-scale appropriately.
What happens when a website is hit by a big spike in load, say, driven by a TV advertisement? You need to respond quickly, yet you don’t know how big the load will be.
First step to deal with spiky loads was to move to containers. Containers start in a about a second, so deployment has moved from minutes to seconds.
Using containers it’s possible to build finer grained microservices.
Containers started to become standardized. Everyone is running the same Redis or Nginx containers, whichever is most recent on DockerHub.
Standardized well debugged services in containers are replacing custom components. Why compile software from scratch when you can use a component debugged by hundreds of people?
First Phase of Serverless
This phase started two years ago.
Code is written, but isn’t deployed until it’s called. It’s just sitting there, ready to be deployed, but not running anywhere. When a request comes in the code must be deployed and started.
Startup time is pretty fast for Javascript or Python. 100s of milliseconds.
Once warmed up launch times are are in the 10s of milliseconds.
You stop paying when you stop using it.
Gone from being able to deploy in seconds, but needing a fleet of deployment machines, to having no machines and deploying in 10s or100s of milliseconds, and paying in 100 millisecond units.
If you are running a million requests per second use containers because your machines always need to be up and running. There are a lot of workloads where traffic comes and goes and is spiky.
Reduced memory usage. There are a lot of different functions inside a microservice or a monolith. Some of those functions don’t get called very much. They still use memory even though they are not being used. By breaking a system into functions they use memory only when they are being used, so the average memory footprint drops.
Cost for CPU goes down because you only pay for what you use (in 100 msec units).
How long does it take to put your code in production? The answer is now 100 msecs.
Building blocks are now not containers, they are services, like DynamoDB. These services are just sitting there and take little effort to use.
Applications can now be developed in a very short period of time. At an Amazon re:Invent, Hackathon teams of four people were able to build complete complex systems in twelve hours. They weren’t just prototypes, they could be deployed in production at scale because they were built on Lambda. All the groups were using Lambda.
Incredibly quick build times is an interesting new capability. When moving applications from a datacenter you can consider rewriting them from scratch using Lambda. You don’t have to fork-lift old applications over.
Second Phase of Serverless: Event Driven Infrastructure
The cloud infrastructure itself started emitting events that can be consumed by Lambda functions. Creating a new instance, for example, can trigger a Lambda function.
This makes a new level of automation possible. It’s the new bash scripting for your infrastructure, only the scripts that are event driven Lambda functions.
This is a new event driven infrastructure where events can be chained together. For example: when there’s a new machine use a Lambda function to attach a volume to it; or cleanup up after an instance dies.
Third Phase of Serverless: Lambda Functions at the Edge
Radical departure that people aren’t understanding yet.
Datacenters disappear. Functions are not running in an AWS region, code is placed near the customer using a CDN at the CDN endpoints.
Now you have a fully distributed, at the edge, low latency, milliseconds from the customer way of running code, using the same Lambda programming model as everywhere else. (Note: you are very limited in what you can do now at the edge on AWS).
Edge computing dovetails with IoT. You have a thing and you want to program that thing. Project Greengrass lets you put a function in that thing.
Now you can build architectures that are partly in the datacenter, partly at the edge, partly at the customer premises.
Snowball Edge is a 50 pound region in a box. It has Lambda in it along with 100TB of storage. It’s programmed on your console in the cloud and the box is delivered on site. Microservices can be distributed to a plane, boat, bottom of a cell tower, or back room of a store.
Functions can be pushed everywhere with the same programming model.
Organizational Implications
The problems for senior management are almost all people problems. The only thing they can change is who to hire, how they are organized, and the budgets they are given. You can tell them to use a certain technology, but they should really pick that themselves.
New way of organizing groups. If you want a certain architecture you need to do an inverse-Conway maneuver: setup groups to be roughly the partitioning you want and assume those groups will set up services that talk to each other.
New way of working. In the new world you have a group of developers and a product manager that is a team. Amazon calls these Two Pizza teams and it’s one of the reasons AWS is able to scale their engineering organization. Small cellular groups need to be given the freedom and independence to build something.
If your organization is set up as a bunch silos going to a microservices model will produce a distributed monolith.
Most of those having problems with microservices you’ll find that a team doesn’t have complete responsibility. A bit of work is done at one place, then handed off to India, then handed off to another group.
If you have teams scattered around the world each team should fully own a microservice and change it themselves. You should be able to completely own and modify a microservice without going outside a timezone. Hopefully you are all in one room or at least on the same chat session.
What you are building is a high trust team. This is key. A lot of large organizations are inherently low trust organizations. When everyone knows each other, trusts each other, you can operate very effectively.
Low trust interfaces between groups are the APIs and SLAs. This goes for using a service like Google Maps or a team implementing another microservice in the same room. High trust is within your team.
Worried About AWS Lock-in?
Don’t worry, be happy. Customers are saying it's so fast to build on Lambda you should just build it and not worry that it’s an AWS only feature.
If It only took a week to build then if you need to move it that will only be a week too.
Lambda functions encapsulate the core of your business logic and business logic is fairly easy to move around.
Don’t worry about reuse anymore, think about how easy code is to replace.