# Microsoft Azure in Plain English

**Source:** https://web.archive.org/web/20190508145128/https://www.expeditedssl.com/azure-in-plain-english
**Section:** Technologies

---

## Key Insights

**Service Naming/Positioning Patterns:**
- Azure renames core concepts: Web Apps = PaaS, Cloud Services = IaaS, Virtual Machines = traditional servers
- Many services are direct AWS competitors with confusing names (Service Fabric vs Lambda, Table Storage vs DynamoDB)

**Web/App Development Stack:**
- Service Fabric = microservices platform (AWS Lambda equivalent)
- App Service Web Apps = PaaS hosting (Heroku-like)
- Application Insights = APM for .NET/Java apps
- Visual Studio Team Services = integrated CI/CD + source control

**Storage Architecture:**
- Single "Storage" service encompasses: Blob (S3-like), Table (NoSQL), Queue (SQS-like), File (EBS-like)
- StorSimple adds automated tiering between local/cloud storage
- Redis Cache positioned as Memcached replacement

**Enterprise Integration:**
- BizTalk connects enterprise apps (SAP, PeopleSoft)
- Service Bus = enterprise message queuing
- Active Directory can sync with on-premise AD or replace entirely
- RemoteApp = Citrix-like app virtualization

**Big Data Pipeline:**
- Data Lake Store = Hadoop ETL processing
- Data Factory = scheduled data movement pipeline
- Stream Analytics = real-time analytics processing (Kinesis equivalent)
- HDInsight = managed Apache ecosystem (Pig, Hive, HBase, Storm, Spark)

**Mobile Backend Services:**
- Mobile Apps = full BaaS with auth, push, data storage
- Notification Hubs supports iOS, Android, Windows, Kindle push notifications

## Bottom Line
Azure mirrors AWS services but with Microsoft-centric naming and tighter Windows/Office integration, requiring translation between marketing names and actual functions.