# Microsoft Azure in Plain English

**Source:** https://web.archive.org/web/20190508145128/https://www.expeditedssl.com/azure-in-plain-english
**Section:** Technologies


---

The Wayback Machine - https://web.archive.org/web/20190508145128/https://www.expeditedssl.com/azure-in-plain-english
Plain English
Hey, have you heard of the new Azure services: Elasticville, StorageWart and API Gatesian? Of course not, I just made those up.
Just like we'd previously made up but then eventually explained a bunch of Amazon's Web Services in Plain English. We're back to help explain Microsoft's Azure ecosystem.
Web + Apps Developer ServicesIf you're setting up a web app, these are mostly what you'd end up using. |
||
|---|---|---|
Service Fabric |
||
| Should have been called Azure Microservice |
Use this to Have a class in your code? Make it a Microservice! Deploy it to the Service Fabric! Ask for a raise. |
It's like AWS Lambda, AWS API Gateway |
App Service > Web Apps |
||
| Should have been called Azure PAAS, Used to be "Azure Websites" |
Use this to Run stuff but don't worry about the sysadmin'ing. |
It's like Heroku, Modulus, AWS ElasticBeanstalk, CloudFoundry |
Cloud Services |
||
| Should have been called Azure IAAS |
Use this to Run stuff but worry a fair amount about configuration and patching. |
It's like AWS EC2 |
Virtual Machines |
||
| Should have been called You can't believe its not a real server |
Use this to Brag to your Devops friends that you'd recommend baremetal if you had your way, but the new CTO says you have to get all "cloudy" |
It's like Linode, Rackspace VPS |
Visual Studio Team Services |
||
| Should have been called Source Control CI |
Use this to Build apps with other people: shared source control and continuous integration |
It's like Github, Jenkins, CodeShip, BitBucket, AWS CodeCommit |
DevTest Labs |
||
| Should have been called QA Virtual Machines |
Use this to Spin up Virtual Machines according to a recipe you set for testing. |
It's like Dockerish, Chef or Puppetish |
Application Insights |
||
| Should have been called Crash, Burn and Report |
Use this to Monitor performance and exceptions happening in ASP.NET or J2EE apps. Get notified of errors, get logs. |
It's like Honeybadger, Exception.io |
Scheduler |
||
| Should have been called Cron the Barbarian |
Use this to Run small jobs that must be repeated at set intervals. Helpful to not have to keep a VM running all the time just for scheduling recurring tasks. |
It's like Heroku Background Jobs, Cron |
Storage ServicesAzure has a singular service called 'Storage' that's all these services and a few that they are depend on. |
||
Blob Storage |
||
| Should have been called Large File Storage |
Use this to Put uploaded images, log files, pirated bollywood films or whatever your app calls for in an infinite hard drive. |
It's like AWS S3, Rackspace Cloud Files |
Table Storage |
||
| Should have been called Database Storage |
Use this to Somewhere in between traditional SQL and pure NoSQL data storage. |
It's like DynamoDB |
Queue Storage |
||
| Should have been called Queue |
Use this to Connect services in a simple message queue arrangement. |
It's like AWS SQS, RabbitMQ, Sidekiq |
File Storage |
||
| Should have been called Attached File Storage |
Use this to Bring over apps to Azure that are dependent on a local (mountable) file system and you can't use Blob Storage. |
It's like AWS EBS |
StorSimple |
||
| Should have been called The more complex version of 'Storage' |
Use this to It's like 'Storage' but moves files up and down from Azure according to rules you set. It makes it seem like Azure Storage is part of your local network. |
It's like AWS Storage Gateway |
Search |
||
| Should have been called FullText Search |
Use this to Do full text search of file, web or whatever other text based objects you have around. |
It's like AWS CloudSearch, ElasticSearch |
Document DB |
||
| Should have been called JSON DB |
Use this to Store JSON NoSQL structured data - in general store more data, more simply than you would with relational SQL. |
It's like DynamoDB, MongoDB |
SQL Database |
||
| Should have been called SQL Database |
Use this to Save all the app data you'll collect into tables and set them up to have not in the biblical sense "relations". |
It's like Heroku Postgres |
Redis Cache |
||
| Should have been called Redis |
Use this to Store frequently used data in convenient structures. It's like Memcached but without the legacy of LiveJournal clutched around it. |
It's like Redis2Go, RedisGreen |
Azure Management ServicesAzure gets complex, these services help tame that complexity. |
||
Automation |
||
| Should have been called Cloud Shell |
Use this to Automate Azure services with Powershell - the langage of the Windows Server Gods. |
It's like AWS Cloudformation |
Operational Insights |
||
| Should have been called Log Reader |
Use this to Collect, combine and search logs for issues or troubleshooting. |
It's like Splunk |
KeyVault |
||
| Should have been called Hardware Security Module |
Use this to Keep encryption keys in secure storage, accessible only when used. |
It's like AWS KMS |
Security Center |
||
| Should have been called Policy Minder |
Use this to Establish policies for Azure services and alert and report when they aren't met. |
|
Mobile App Developer ServicesThese are the services that only work for mobile developers. |
||
App Service > Mobile Apps |
||
| Should have been called Baby's got Backend As A Service |
Use this to Authenticate, send messages and store network data for mobile platforms. |
It's like Heroku, Urban Airship, Parse |
App Service > API Apps |
||
| Should have been called Azure API Proxy |
Use this to Build an API to Azure services and a SDK for multiple client languages (PHP, Node, Java, ASP.NET) |
It's like AWS API Gateway |
API Management |
||
| Should have been called API Big Boss |
Use this to Control the traffic and limits of what is passed through an API. |
It's like AWS API Gateway |
Notification Hubs |
||
| Should have been called Azure Push Notifications |
Use this to Send push notifications to iOS, Android, Windows and Kindle. Ok, now that even Kindle is supported, I just feel bad for making fun of Blackberry previously. |
It's like AWS SNS, UrbanAirship |
Mobile Engagement |
||
| Should have been called Mobile Analytics (which unfortunately AWS scooped up first) |
Use this to Get real time analytics of what gets people to buy coin-doubler bonuses in your mobile panda bowling game. |
It's like AWS Mobile Analytics, Flurry |
Media and CDN ServicesDeliver content faster, and make videos playable on different devices. |
||
Encoding |
||
| Should have been called It's a good name, but wish they had called it 'VHS' for some retro charm. |
Use this to Encode videos into formats useful for things like viewing on mobile, web, 4K HomeTheater demos, etc. |
It's like AWS ElasticTranscoder |
Media Player |
||
| Should have been called RealPlayer(TM) |
Use this to Actually embed the videos without you having to figure out which player and encodings work for each client platform. |
|
Media Indexer |
||
| Should have been called Closed Captioner |
Use this to Auto generate text from audio and video files. Search this text or use it for auto generated captions. |
|
Content Protection |
||
| Should have been called Azure DRM |
Use this to Protect your cat videos from copyright infringers and piraters. |
|
Live and On Demand Streaming |
||
| Should have been called McStreamey |
Use this to Handle mass live playback of video along with making sure only the right people are watching and that they've hopefully already paid you. |
|
Content Delivery Network |
||
| Should have been called A(zure)kami |
Use this to Speed delivery of your sites, files, videos to the people requesting them. |
It's like Cloudfront, MaxCDN |
Networking ServicesDepending on what you're doing you might use these to improve performance or security. |
||
Virtual Network |
||
| Should have been called Network Expander |
Use this to Make it seem like new Azure services just happened to show up on your internal company network. Bring your own IP address. |
It's like AWS VPC |
Express Route |
||
| Should have been called Pretty good |
Use this to Push TBs a day up to Azure without overloading your mom's cable modem? Get a dedicated line into Azure. |
It's like AWS Direct Connect |
VPN Gateway |
||
| Should have been called Can't afford Express Route |
Use this to Setup a VPN between your datacenter and Azure to put traffic over. |
It's like OpenVPN |
Traffic Manager |
||
| Should have been called Geo Load Balancer |
Use this to Improve performance by putting traffic to datacenters closer to requests and smart failover when a DC catches on fire. |
It's like AWS ELB |
Load Balancer |
||
| Should have been called Local Load Balancer |
Use this to Split traffic between multiple servers/services |
It's like AWS ELB |
Application Gateway |
||
| Should have been called Web Load Balancer |
Use this to Load balance web servers. comes packed with all the HTTP optimized load balancing goodies: SSL terminating, Cookie Affiity setting a growing developer needs. |
It's like AWS ELB |
DNS |
||
| Should have been called Yuuuuuuuup it's DNS |
Use this to Make a joke about a guy named John CNAMEa! |
It's like DNSimple, Route 53, GoDaddy |
Enterprise / Corporate ServicesServices for business and networks. |
||
RemoteApp |
||
| Should have been called Apps on Cloud |
Use this to Put an app on Azure and give users a RDP session to it. |
It's like Citrix |
BizTalk |
||
| Should have been called App Communicator |
Use this to Connect both Azure Enteprise apps (like SAS or Peoplesoft) together. That sounds like fun. |
|
Service Bus |
||
| Should have been called Network Message Queue |
Use this to Dump commands and data into queuing service that lets you connect lots of devices, servers or client together for better and smoother processing. |
It's like RabbitMQ, AWS SQS |
Backup |
||
| Should have been called Better'n Tape |
Use this to Keep a data center disaster from wiping out all your backups. Sick of swapping tapes, keeping them offsite and accidently recording hot mixes over the incremental accounting backups? |
It's like Glacier, Backblaze |
Site Recovery |
||
| Should have been called Plan B |
Use this to Keep a replicated version of your critical network apps on standby in Azure. |
It's like AWS CloudConfig |
Active Directory |
||
| Should have been called Hybridactive Directory |
Use this to Setup an Active Directory As A Service that can sync to your Enterprise AD or replace it entirely |
|
Big Data ServicesServices to ingest, manipulate and massage data to do your will. |
||
Batch |
||
| Should have been called Bunch-of-VMs.bat |
Use this to Do lots of stuff at once on a bunch of systems, but not all the time. Also, use the word parallel more than a middle school geometry teacher. |
It's like AWS Elastic Map Reduce |
App Service > Logic Apps |
||
| Should have been called Cloud Lego Flowchart |
Use this to Hook together different pieces to build a cloud workflow for your data. |
It's like IFTTT, Zapier |
SQL Data Warehouse |
||
| Should have been called That'll do SQL Data Warehouse, that'll do. |
Use this to Load up data into the giant SQL Server of your dreams and query it six ways from Sunday (which I guess would be Saturday?) |
It's like AWS Redshift |
Data Lake Analytics |
||
| Should have been called UberSQL Data Warehouse |
Use this to Hold Exabytes of Data (don't worry how much that is, if you had that much data you'd know). |
|
Data Lake Store |
||
| Should have been called ETL Query |
Use this to Extract, Transform and Load all your Datawarehouse data with Hadoop. |
It's like AWS ElasticMap Reduce |
HDInsight |
||
| Should have been called Apache Apps |
Use this to Assure your boss that the names: Pig, Hive, HBase, Storm, Spark are not the new Avengers Movie superhero lineup. |
|
Machine Learning |
||
| Should have been called Cortana AI Edition |
Use this to Figure out what non-gamers think of all the Cortana branding: "Whatasa cortada - some kind of hot chocolate mexican drink?" Also use this to get on an AI's good side before the Singularity. |
It's like AWS Machine Learning |
Stream Analytics |
||
| Should have been called Real Time Analytics |
Use this to Collect thousands of analytics streams simultaneously. |
It's like AWS Kinesis |
Data Factory |
||
| Should have been called Data Pipeline |
Use this to Schedule when and how data is moved between services. |
It's like AWS DataPipeline |
Data Catalog |
||
| Should have been called Data Sharing |
Use this to Let anybody in your organization get to some of the data you put into the other Data Services. It's like a SQL View for cross service data. |
It's like Chartio |
IoT ServicesLots of devices scattered around your house that need patched. |
||
IoT Hub |
||
| Should have been called Pretty good name and it's not like some SOC will know what to call it anyway. |
Use this to Central system for managing how many smart egg monitors are connected to your new smart-egg-monitor.com service. Handles authorization, updates and communications in a central way. |
It's like AWS IOT |