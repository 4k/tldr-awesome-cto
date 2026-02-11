# Technology Due Diligence Checklist

**Source:** https://akfpartners.com/growth-blog/technical-due-diligence-checklists
**Section:** Due Diligence


---

AKF has been conducting technology due diligence on behalf of our investor and strategic acquirer customers for over 15 years. Along this journey we developed a checklist to help guide the process. This checklist has evolved with the ever-changing technology landscape but the tool itself has remained a valuable foundation to comprehensively understanding the capability and scalability of any technology product offering and organization.
While the checklist is a useful tool, it must also be combined with an end-to-end approach to optimize the discussion with the organization being evaluated and therefore result in accurate and useful findings. To help guide the process of conducting the due diligence interactions, we have also summarized key elements to our approach in a separate post. Some of the terminology below refers to AKF models and a quick visit to the AKF Scale Cube will help orient you for the scalability question sections.
AI/ML: Strategy
- Does the company have a clear AI/ML strategy aligned with product goals?
- Does product management effectively integrate AI/ML into its planning and delivery process?
- How well does the organization understand and manage AI/ML vendor or cloud platform lock-in risks?
AI/ML: Execution
- Are relevant data sources identified, accessible, and governed for AI use?
- Is the model lifecycle (from experimentation to deployment) standardized?
- Are models monitored for performance degradation and drift in production?
- Are models evaluated for bias, fairness, and ethical risk?
- Are AI/ML systems and data protected against misuse or attacks?
- Is model inference optimized for latency, scale, and cost?
- Are modern, scalable ML platforms/tools being used effectively?
- Are AI/ML practices aligned with regulatory standards (GDPR, HIPAA, etc.)?
- How effectively does the organization manage the cost of AI/ML systems across development and production?
- Is there a defined process for retraining models based on performance or data shifts?
- Are ethical risks from AI system behavior understood and managed?
- Are third-party models/tools used responsibly and with awareness of risk?
- Are AI/ML systems released using experimentation and controlled exposure?
AI/ML: Differentiation
- Are data scientists, engineers, and domain experts effectively collaborating and learning?
- Are Large Language Models (LLMs) used appropriately and grounded in verifiable data?
- Are models explainable and interpretable to internal and external stakeholders?
- Are AI/ML systems adapted based on customer usage and feedback?
SCALABILITY: AKF Scale Cube X-AXIS
- Are load balancers or ELBs used to distribute requests across multiple end points?
- Is session state stored in the browser or a separate tier?
- Read/Write Databases: Is there an appropriate separation of reads and writes using master/slave databases (or other AKF Scale Cube X-Axis capabilities - e.g. NoSQL Quoroms)?
- Are object caches utilized - if so, how and why?
- Are authentication and authorization services synchronized and available to all environments/regions?
- How is edge caching (CDN/browser caching) being leveraged?
SCALABILITY: AKF Scale Cube Y-AXIS
- Are services (i.e. login, signup, checkout) separated across different servers?
- Is data sharded across different datbases - Does each service have its own separate data store?
- Are services sized appropriately with consideration of needs (e.g. availability, frequency of change, dependencies, skillsets)?
SCALABILITY: AKF Scale Cube Z-AXIS
- Are endpoints (web, app servers) dedicated to a subset of similar data (i.e. users, SKU, content)?
- Are databases dedicated to only a subset of similar data?
- How do you handle multi or all-tenant in your implementation (services & data)?
- How do you handle data residency requirements - and are you required to do so for GDPR or other reasons?
FAULT ISOLATION (SWIM LANES)
- Are only asynchronous calls being made across services?
- Do you isolate data with respect to domains/services?
- Does logical architecture enforce the separation of function/areas of concern?
- Is there any specific area or areas where a failure will cause an outage (single-points of failure –SPOFs)?
- Is your data tier resilient to logical corruption (durable snapshots, intra-database rollback) or being unavailable?
- How do you use multiple data centers (cloud regions and availabilty zones) to implement disaster recovery strategies?
- Are data centers (if colo or owned DCs) located in geographically low-risk areas?
COST-EFFECTIVENESS
- Does the application use stored procedures (SPROCs, PROCs)? If so, is there business logic contained within the SPROCs?
- Are the web, application, and database servers on physically separate tiers or separate virtual instances?
- How do you scale for demand? Are auto-scaling techniques used?
- What third-party technologies are part of the system? How do they impact time-to-market, cost, and latency?
- If self-hosted - describe the hardware sizes across the major components/tiers of the application (goldfish vs. thouroughbreds/cattle, not pets). If cloud-hosted - describe the instance sizes used for workloads including the DB(s).
- Do you use virtualization, and if so, what are your objectives in using it?
- Are data centers located in low-cost areas (if colo or owned DCs)?
- What traffic is routed through a Firewall/WAF?
- How time-intensive/expensive would it be for you to use a different public cloud provider?
- Do you have code specific to a customer? If so, what customer-specific code/data structures exist? How many versions of your software do you deploy and support?
- Current platform as a service (PaaS) - how did you make the decisions on what PaaS service to leverage?
- Future PaaS usage - How are you thinking about evolving your use of PaaS based on the future?
PRODUCT MANAGEMENT PROCESS
- Is there a product management team or owner that can decide to add, delay, or deprecate features?
- Does the product management team have ownership of business goals?
- Does the team develop success criteria, OKRs, KPIs, or customer feedback loops that help to inform feature decisions?
- Does the team use an iterative discovery process to validate market value and achieve goals?
- Are leading and lagging indicators defined for each major project, and what is the process to track, validate, and rebase or revisit the metrics?
PDLC PROCESS
- Are leading and lagging indicators defined for each major project, and what is the process to track, validate, and rebase or revisit the metrics?
- Does the team use any relative sizing method to estimate effort for features/story cards?
- Does the team utilize a velocity measure to improve team time-to-market?
- Does the team use Agile burndown, metrics, and retrospectives to measure the progress and performance of iterations?
- How does the team measure engineering efficiency and who owns and drives these improvements?
- Does the team perform estimates and measure actual against predicted?
- Is there an Agile Definition of Done in place? Does it measure customer adoption of features, or just releasing of code into production?
DEVELOPMENT PROCESS
- Does the team use an approach that allows for easy identification and use of a prod bug fix branch for rapid deployment?
- Does the team use a feature-branch approach? Can a single feature/engineer block a release?
- In your public cloud architecture, how do you build and provision a new server/environment/region?
- Does the team have documented coding standards and if so - how are they taught and applied?
- Are engineers conducting code reviews with defined standards or have automation in the development pipeline that validates against the standards?
- Is open-source licensing actively managed and tracked? If so, how? Is it automated?
- Are engineers writing unit tests (code coverage)?
- Is the automated testing coverage greater than 75%?
- Does the team utilize continuous integration?
- Is load and performance testing conducted before releasing to a significant portion of users or is the testing built into the development pipeline?
- Does the team deploy small payloads frequently versus larger payloads less-frequently?
- Does the team utilize continuous deployment?
- Is any containerization (e.g. Docker) and orchestration (Kubernetes) in place?
- Are feature flags, where a feature is enabled or disabled outside of a code release, in use?
- Does the team have a mechanism that can be used to roll back (wire on/off .DDL/DML scripted and tested, additive persistence tier, no "select *")?
- How does the team define technical debt?
- Is tech debt tracked and prioritized on an ongoing basis? (Is there a defined percentage of each Sprint dedicated to reducing tech debt?)
- How are issues found in production, backlogged bugs, as well as technical debt addressed in the product lifecycle?
- Does the team utilize a Joint Application Design process for large features that brings together engineering and ops for a solution or do they have experientially diverse teams?
- Does the team have documented architectural principles that are followed?
- Does the team utilize an Architecture Review Board where large features are reviewed to uphold architectural principles?
OPERATIONS PROCESS
- Describe application logging in place. Where are the logs stored? Are they centralized and searchable? Who has access to the logs?
- Are customer experience (business) metrics used for monitoring to determine if a problem exists?
- Are system-level monitors and metrics used to determine where and what the problem may be?
- Are synthetic monitors in use against your key transaction flows? (How do you find out what is wrong before your customers do?)
- Are incidents centrally logged with appropriate details?
- Are problems separated from incidents and centrally logged?
- Is there any differentiation in the severity of issues? How do you escalate appropriate severity incidents to teams/leaders/the business?
- Are alerts sent in real-time to the appropriate owners and subject matter experts for diagnosis and resolution?
- Is there a single location where all production changes (code and infrastructure) are logged and available when diagnosing a problem?
- Are postmortems conducted on significant problems and are actions identified assigned and driven to completion?
- Do you measure time to close problems fully?
- Is availability measured in true customer impact?
- Are quality of service (QoS) meetings held where customer complaints, incidents, SLA reports, postmortem scheduling and other necessary information reviewed/updated regularly?
- Do operational look-back meetings occur either monthly or quarterly where themes are identified for architectural improvements?
- Does the team know how much headroom is left in the infrastructure or how much time until capacity is exceeded?
- How do customer-reported problems flow from support to product engineering teams?
- How do you simulate faults in the system? (i.e. Choas Monkey)
ORGANIZATION KNOWLEDGE AND ALIGNMENT
- Do architects have both engineering/development and infrastructure experience?
- How do you onboard and develop team members?
- Are teams perpetually being evaluated and upgraded (i.e. seed, feed, weed)? How do you handle poor performers?
- Are teams aligned with services or features that are in pods or swim lanes?
- Are Agile teams able to act autonomously with a satisfactory TTM?
- Are teams comprised of members with all of the skills necessary to achieve their goals?
- Does leadership think about availability as a feature by setting aside investment for debt and scaling?
- Have architects designed for graceful failures by thinking about AKF scale cube concepts?
- Does the client have a satisfactory engineer to QA tester ratio?
- Does the team think strategically about talent sourcing - both level and location?
- What percentage of your QA team performs automation?
SECURITY
- Is there a set of approved and published information security policies used by the organization?
- Has an individual who has final responsibility for information security been designated?
- Are security responsibilities clearly defined across teams (i.e., distributed vs completely centralized)?
- Are the organization's security objectives and goals shared and aligned across the organization? (Or does everyone put to the CISO or InfoSec team?)
- Has an ongoing security awareness and training program for all employees been implemented?
- Is a complete inventory of all data assets maintained with owners designated?
- Has a data categorization system been established and classified in terms of legal/regulatory requirements (PCI, HIPAA, SOX, etc.), value, sensitivity, etc.?
- Has an access control policy been established which allows users access only to network and network services required to perform their job duties?
- Are the access rights of all employees and external party users to information and information processing facilities removed upon termination of their employment, contract or agreement?
- Is multi-factor authentication used for access to systems where the confidentiality, integrity or availability of data stored has been deemed critical or essential?
- Is access to source code restricted to only those who require access to perform their job duties?
- Are the development and testing environments separate from the production/operational environment (i.e., they don't share servers, are on separate network segments, etc.)?
- Are network vulnerability scans run frequently (at least quarterly) and vulnerabilities assessed and addressed based on risk to the business?
- Are application vulnerability scans (penetration tests) run frequently (at least annually or after significant code changes) and vulnerabilities assessed and addressed based on risk to the business?
- Are all data classified as sensitive, confidential or required by law/regulation (i.e., PCI, PHI, PII, etc.) encrypted in transit?
- Is testing of security functionality carried out during development?
- Are rules regarding information security included and documented in code development standards?
- Has an incident response plan been documented and tested at least annually?
- Are encryption controls being used in compliance with all relevant agreements, legislation and regulations? (i.e., data in use, in transit and at rest)
- Do you have a process for ranking and prioritizing security risks?
- Do you have an IDS (Intrusion Detection System) solution implemented? How about an IPS (Intrusion Protection System)
Why the Changes?
Technology evolves, engineers innovate, and entrepreneurs create. A static checklist will not improve with age like wine. Keep your eyes out for future blog posts discussing more details about our changes.
Want to learn more?
Contact us, we would be happy to discuss how we have helped hundreds of clients over the years.