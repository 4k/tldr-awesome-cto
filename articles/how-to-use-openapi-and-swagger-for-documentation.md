# How to Use OpenAPI and Swagger for Documentation

**Source:** https://blog.readme.com/how-to-use-openapi-and-swagger-spec-for-documentation/
**Section:** Related stuff


---

How to Use OpenAPI and Swagger for Documentation
Excellent API documentation experiences stem from proper use of an OpenAPI or Swagger API description file. In this guide, we explain Swagger and OpenAPI, how to create an OpenAPI or Swagger description for an API, and how to use the OpenAPI Specification to yield documentation that’s continuously up-to-date and automated!
HTTP API descriptions, like those described in the OpenAPI Specification, end up being helpful in a variety of ways for your development teams, but also your broader users.
The challenge: Manually creating comprehensive and accurate documentation is difficult. It’s a chore to produce, especially when it exists as a task to be done separate from the original code creation. API documentation is easily neglected and becomes outdated. New endpoints go undocumented, which unfortunately means they will never exist in the minds of most developers. Even worse, if API response data changes, there’s no way for developers to learn what to expect from each request.
A developer’s experience with an unfamiliar API is dictated by its documentation. The API’s reference guide provides the first impression of quality and consistency. The reference guide is the source of truth that developers return to whenever there’s a serious issue or question about an API’s functioning, and therefore must be painstakingly managed.
Enter: Swagger and OpenAPI.
Swagger and OpenAPI are specifications to describe HTTP APIs (the most common type of API). These machine-readable formats define everything a developer needs to integrate with an API: authentication, endpoints, HTTP methods, request data, response fields, and detailed error codes. They’re easy to create and can be used in many forms of automation. We’ll explore the ways to use OpenAPI and Swagger in the remainder of this guide.
Key advantages of API description formats like Swagger and OpenAPI include:
- Easier documentation management, comprehensive by nature
- Allow automated testing for API validity
- Easier sharing and publication of API specifications
OpenAPI common terms and definitions
If you’re new to this topic you’ll see many unfamiliar terms used throughout this guide and on the web as you research Swagger and OpenAPI specifications. We’ve gathered the essential definitions in this brief glossary so you can reference your knowledge before you begin.
- Definition: The document, in either Swagger or OpenAPI format, that defines a specific API.
- Description: Another term for an API definition, which describes a specific API.
- Documentation: The human-readable API reference, getting started guides, tutorials, and any other content used to introduce an API to a developer.
- OAS: OpenAPI Specification. (See OpenAPI.)
- OpenAPI: A specification which declares a syntax for the human and machine-readable API descriptions.
- OpenAPI document: Another term for the OpenAPI flavor of API definition.
- OpenAPI file: An individual OpenAPI document.
- OpenAPI Initiative: The industry-wide working group that maintains the OpenAPI format.
- Specification: A set of rules that defines the format for OpenAPI and Swagger.
- Swagger: The original API description format, which later became OpenAPI. Also, SmartBear’s line of tools to interact with Swagger and OpenAPI files.
- Swagger file: Another term for the Swagger flavor of API definition.
- Version 2: The shorthand for Swagger 2.0 and OpenAPI 2.0, which are two names for the same specification format.
- Version 3: The shorthand for OpenAPI 3.0 (and more recent minor versions), the most recent OpenAPI specification.
What are Swagger and OpenAPI?
Swagger and OpenAPI are API description formats that provide a common framework for teams to build and document APIs. These machine-readable definitions open up many opportunities at each stage of the API lifecycle.
A Swagger document describes your APIs so you can keep them documented, test their validity, and share the expected results within your company and beyond.
OpenAPI for documentation (and more)
The biggest API headache developers cite is inaccurate and outdated documentation (2019 Postman API survey). It is difficult, sometimes impossible, to integrate an API that is poorly documented. Unfortunately, many developers avoid writing documentation, or aren’t comprehensive when they do so.
OpenAPI solves out-of-date documentation headaches by offering a standardized format that makes it easy to generate documentation that always matches the architecture of the API.
When an API changes, you can automatically generate rendered documentation based on the data contained in the underlying Swagger/OAS API description. When documentation is in sync with your API description, developers won’t worry about whether your documentation is accurate. Your developers can spend more time coding and less time documenting. Even better, since API descriptions are machine readable, you can make use of many automated tools.
OpenAPI descriptions can be written in either YAML, or JSON. These notation formats were chosen because they are designed to be both easy for a human to read and write, and easy for software to parse.
Here’s an example API description in YAML format that describes a ReadMe GET operation to retrieve docs by their slug (name):
Paths:
/docs/{slug}:
get:
summary: Returns the doc with this slug
operationId: getDoc
parameters:
- name: slug
in: path
required: true
description: Slug of doc. must be lowercase, and replace spaces with hyphens.
type: string
A ReadMe API endpoint described in the YAML format
Documentation is the most visible output of OpenAPI and Swagger definitions, but there are many more applications. Engineers can use the same OpenAPI or Swagger file that generated the docs to set up continuous integration and other testing.
As an API provider, imagine how great it feels to always know your documentation will match your API when you deploy! When you use an OpenAPI or Swagger definition, you can automatically generate documentation and check its validity as part of your deploy process.
API definitions: Swagger set the standard
In the early 2010s, building APIs was like the Wild West. Most companies didn’t have defined processes for how new APIs were added. Instead, each group or even individual engineers built them to their own specifications. They would produce whatever documentation they could, but often they were onto the next project. API documentation was often minimal, outdated, and missing important information needed to integrate. Over time, the API developer community realized a need to create standardized formats for describing APIs according to useful conventions.
The industry arrived at an API definition workflow after years of developer frustration. Prior to Swagger, engineers attempted to cobble together tooling or, more likely, went without.
Other description formats coexist with Swagger, including API Blueprint and RAML, but Swagger succeeded by rallying a community behind it, including some early tooling. SmartBear Software acquired Swagger in 2015 and hired Tony Tam to lead a commercial product line around the format, establishing paid tools like SwaggerHub.
The acquisition validated the importance of API descriptions, but at the time, it raised questions about whether the format would continue to be independent from the paid service provider.
The OpenAPI initiative leads the way
After Swagger became the de facto standard for API definition, the industry recognized the need for a vendor-neutral option. In 2016, developer community leaders, including SmartBear, created the OpenAPI Initiative (OAI).
Now part of the Linux Foundation, the OAI includes members from many large tech companies and API thought leaders.
The OAI oversees the future of OpenAPI as a data format. A technical steering committee collaborates with the broader community to determine the vision for the format.
Swagger vs OpenAPI: What’s the Difference?
The overlap between Swagger and OpenAPI Specification causes a lot of confusion. These are two separate, but very much related, specifications for describing APIs. SmartBear owns the Swagger name, but the current specification is now governed by the OAI.
The last version of the Swagger data format was Swagger 2.0, released in 2014. SmartBear then donated the Swagger 2.0 specification to become the initial version of the OpenAPI specification (also designated 2.0).
OpenAPI 3.0 was released in 2017 and is the current major version.
The initial version of OpenAPI is designated 2.0 to indicate it is identical to Swagger 2.0. You can recognize this because the first line of its YAML-format description will read:
swagger: "2.0"
The entire OpenAPI 2.0 format is identical to Swagger 2.0, right down to the heading that identifies it as “swagger!”
The most recent major version is OpenAPI 3.0, released in 2017. You can easily identify it based on the first line of its YAML:
openapi: "3.0.0"
The OAI leaders who guide OpenAPI made a lot of improvements with the third version of the specification. Most notably, a “components” section provides flexibility in describing many approaches to HTTP APIs. These components, which include request and response bodies, also add a way to describe webhooks with “callbacks.” Additionally, the way of describing API hosts and base paths is simplified into a single object made of components.
How to use Swagger and OpenAPI
Many tools exist for Swagger, and it’s still widely supported despite OpenAPI 3.0 superseding it as the latest format in 2017. The best tools will accept multiple formats, so you should be able to bring either a Swagger 2.0 an OpenAPI 3.0 document to modern tooling.
The biggest advantage of an API description is that your documentation will always be up-to-date. You’ll ensure that anyone using your API sees the absolute latest functionality. You can also use the Swagger or OpenAPI definition to test your APIs, to be certain that what is in your description (and what gets generated as documentation) matches your deployment. Finally, since API descriptions are machine readable, there are several other utilities you can generate using the definition, including servers and SDKs.
Keep API documentation updated
Once you have a Swagger or OpenAPI file, you can use it to ensure your documentation is always accurate. The description format provides the structure that becomes your API reference. This part of your documentation can be generated every time the API changes and can be hosted alongside the rest of your documentation.
Our best practices for writing API docs suggest some good ways to get started, including “autodoc” tools to generate your reference. These can be built into continuous integration pipelines, described later in this guide. Essentially, you can deploy updated docs along with your API.
Test API contracts
Another common use of Swagger and OpenAPI documents is to confirm your API behaves the way you say it does. API definitions are also sometimes called contracts because they describe exactly what the API provider agrees will be included. You can run sample calls against your API—either in development or production—and make sure each request returns the expected response.
For example, your API description may declare the following fields in JSON:
{
"id": 8675309,
"name": "Jenny",
"status": "available"
}
But the API may actually provide a different response:
{
"pet_id": 8675309,
"name": "Jenny",
"status": 1
}
The errors might not be immediately obvious when examined by eye. Using an automated diff tool, you can quickly discover what’s amiss.
In this case, the diffing tool shows that id
became pet_id
. The status
field, which we expected to be a string, was implemented as an integer. When problems like these are discovered early, you can ensure the API is developed according to the contract—or, make the appropriate edits in your API definition so that the documentation will match the implementation.
Generate Servers, SDKs, and Sample Code
It turns out when something is machine readable, there are all sorts of automated activities that become possible. In addition to documentation and contract testing, you can:
- Stub out code to help build your API
- Create mock servers for front-end testing
- Generate wrapper libraries or SDKs in multiple languages
- Build code samples automatically
OpenAPI descriptions allow you to make your documentation far more than a simple API reference.
The screenshot below shows a starter Python code snippet that ReadMe automatically generated from a single API description file. Also generated from the same description were equivalent snippets for JavaScript, Ruby, Node, and cURL (not shown).
When you give developers the code in their own language with personalized sample code, they are a simple copy-and-paste away from their first “hello world” success with your API!
How to write an OpenAPI description
You’ve seen there’s a lot you can do with a Swagger or OpenAPI file. Now you’ll want to create your own! Since it’s plain text format, you can use any text editor. However, it makes sense to use one that knows the syntax of the API description format you’re using. In addition, it can be helpful to begin with a template so you don’t have to start from scratch (we’ve got one for you!).
Use JSON or YAML
When you write your OpenAPI or Swagger docs, you can choose from either of two formats: JSON or YAML. Both will use the same data structure (determined by the Swagger or OpenAPI specification), but each will have a different syntax representation. JSON may look familiar to most web developers and it is the most common format used to return actual API results. YAML may also look familiar, as it’s often used in configuration files.
YAML uses whitespace and minimal markup, which can make it more human-readable compared to JSON.
Below is an example OpenAPI 3 YAML description, showing the header and one path/response.
openapi: "3.0.0"
info:
version: 1.0.0
title: Swagger Petstore
license:
name: MIT
servers:
- url: http://petstore.swagger.io/v1
paths:
/pets:
get:
summary: List all pets
operationId: listPets
tags:
- pets
parameters:
- name: limit
in: query
description: How many items to return at one time (max 100)
required: false
schema:
type: integer
format: int32
responses:
'200':
description: A paged array of pets
headers:
x-next:
description: A link to the next page of responses
schema:
type: string
content:
application/json:
schema:
$ref: "#/components/schemas/Pets"
JSON is the more common format for data exchange, but is less human-readable. Here’s the same OpenAPI 3 description fomatted using JSON:
{
"openapi": "3.0.0",
"info": {
"version": "1.0.0",
"title": "Swagger Petstore",
"license": {
"name": "MIT"
}
},
"servers": [
{
"url": "http://petstore.swagger.io/v1"
}
],
"paths": {
"/pets": {
"get": {
"summary": "List all pets",
"operationId": "listPets",
"tags": [
"pets"
],
"parameters": [
{
"name": "limit",
"in": "query",
"description": "How many items to return at one time (max 100)",
"required": false,
"schema": {
"type": "integer",
"format": "int32"
}
}
],
"responses": {
"200": {
"description": "A paged array of pets",
"headers": {
"x-next": {
"description": "A link to the next page of responses",
"schema": {
"type": "string"
}
}
},
"content": {
"application/json": {
"schema": {
"$ref": "#/components/schemas/Pets"
}
}
}
}
}
}
}
}
}
Modern programming languages and their respective web frameworks can readily consume JSON objects, and this is a major reason for why many API providers adopt the JSON format. Most web developers are familiar with JSON syntax thanks to its resemblance to Javascript.
Neither YAML or JSON are immune to human error, but editors with linters will catch the most common errors.
You can convert files between JSON and YAML, so feel free to choose whichever format is preferable for you and your team.
Your favorite code editor
Your current development environment or text editor will include YAML and JSON syntax highlighting and may already include Swagger and OpenAPI syntax support as well. Look for plugins, which can help with syntax suggestions or checking for errors as you write your API description. Alternatively, you can use existing open source or web-based tools.
For example, the VSCode editor has an open source linter plugin to check YAML and JSON files against Swagger and OpenAPI specifications.
Shown above is an example of an in-editor linter program which will raise errors and flag conventions for cleaner code. You can click each error to go to the line where the issue originated. In the screenshot, we accidentally misspelled description
, resulting in the linter raising missing required property errors on line 48 with the typo.
With most editors, you can edit either OpenAPI or Swagger files in YAML, with syntax help and built-in linting. When finished, you can programmatically convert YAML to the equivalent JSON.
OpenAPI template
To get started with an OpenAPI file, it can be helpful to start with a basic outline that includes the essential syntax. Then you can step through each line and make edits to include the proper details from your API.
You don’t have to start from scratch! Here’s a template OpenAPI definition:
openapi: "3.0.0"
info:
version: 1.0.0 // Version of your API
title: Your API Title
description: An API description template
contact:
name: Your Name
email: [email protected]
url: http://example.com
license:
name: License Name
url: http://example.com/license-url
servers:
- url: http://api.example.com
paths:
/your_endpoint:
get:
description: |
Multi-line description
of your API endpoint
operationId: yourOperation
parameters:
- name: your_param
in: query
description: Description of your param
required: false
schema:
type: string
responses:
'200':
description: Your success description
This template doesn’t include complete coverage of all possible OpenAPI fields, but it’s useful as starter code. In most cases you’ll want to add your own response schemas and reusable components. You can dig into the OAS specification itself or see our OpenAPI and Swagger examples below.
Once you have an initial framework for your API described, you can complete coverage for the remainder of your API.
Generate OpenAPI from an existing API
If you already have an API in production, you can benefit from documenting it in an OpenAPI file. To save yourself some time, look for some ways you can generate the descriptions from your code or live traffic.
If your API is built in a common framework, such as Falcon (Python) or Rails (Ruby), your code already has everything needed to create a Swagger or OpenAPI description. Look for an existing project that creates an API definition based on an existing API. For example, zero-rails_openapi gem
is a Rails solution and falcon-apispec
does the same for Falcon.
There could be many reasons it’s not possible to reference source code. In that case, you might use a service like Optic to listen to live API traffic. After reviewing live requests and responses, Optic can output an OpenAPI or Swagger file.
Swagger and OpenAPI best practices
When describing HTTP APIs, you want to keep an overall developer experience in mind. If your documentation is going to be comprehensive, your Swagger or OpenAPI definition must also have full API coverage. If the API is still in development, it’s also a good time to ensure you’re following API design best practices in naming fields and using HTTP methods.
Adopt REST patterns
Even before you write descriptions for your endpoints, you’ll need to decide which are needed and how they’re named. With thousands of HTTP APIs available to developers, there’s no reason to get super creative with how yours is designed. Look to established conventions rather than adopting an unnecessarily unique take. Developers are comfortable with these patterns, as they’ve experienced them across many APIs. The more similar you can be to something they’ve seen before, the easier time they’ll have integrating with your API.
Representational State Transfer (REST) is an architectural style often used by HTTP APIs. While most don’t adopt the patterns wholesale, there are three big criteria to keep in mind for your API:
- Organize your API around resources
- Use HTTP methods to communicate actions
- Rely upon standard HTTP status codes
The RESTful approach to APIs came out of a time that heavily relied upon remote procedure calls (RPC). In these approaches, led by SOAP APIs, you might make a call to a getPets
procedure, similar to how a local function is called in code.
Instead, REST uses a pets
resource. To retrieve the list of pets, you would use the HTTP GET verb on the /pets
endpoint. The success or failure of that call would be returned as the HTTP status code 200 if it worked and most often a 400-level error if it didn’t.
One positive side effect, which comes through in your Swagger or OpenAPI definition, is that the actions for each resource are naturally grouped together. They’ll also likely call upon the same components, such as the Pet schema in this example. The REST convention and API description formats encourage straightforward designs that improve developer experiences. However, it still takes some effort on your part to keep the interface uniform.
Start with friendly descriptions
Your API definition includes technical details of the API, but there are also human-readable areas throughout the document. These description
and summary
fields are used throughout the definition. An endpoint requires a summary of how each HTTP method is used. Parameters and responses within those also need descriptions. The words used here are important—they’ll be output with documentation and read by every developer who uses the API.
When these fields are blank or—perhaps worse—use unhelpful placeholder text, your documentation will suffer. Put yourself in the place of someone using the API. You’d want to know the purpose of each endpoint and context around the expected inputs and outputs.
For an example of bad documentation, this OpenAPI snippet will create documentation without a summary or description for the user:
paths:
/pets:
get:
summary:
operationId: getPets
tags:
- pets
parameters:
- name: limit
in: query
description:
required: false
schema:
type: integer
format: int32
Better documentation includes a summary and description with useful info on how one would use the endpoint.
paths:
/pets:
get:
summary: Retrieve a list of pets, up to the passed limit (if included, otherwise 10)
operationId: getPets
tags:
- pets
parameters:
- name: limit
in: query
description: The number of pets to retrieve (maximum 100)
required: false
schema:
type: integer
format: int32
API descriptions are most useful for being machine readable, but you can’t completely forget the human who will be consuming the API.
Be consistent with naming
The endpoints for your API could work just fine with meaningless names. Similarly, the fields in your parameters and results don’t technically need human-readable labels. But you don’t typically see API calls like /c109b523f7?755ef5=100
. People can’t hold the purpose of this call in their heads long enough to copy it from docs to code.
Naming within your API matters
In a RESTful approach to API design, you’re organizing your API around resources. A common naming tactic is to use nouns for resources. Should these nouns be singular or plural? There’s a hot debate, but most practitioners can agree on one thing: you should make a choice and stick with it the same way for your API (and all your APIs, if possible). That means, if you are adding orders to your API, you’d choose /orders
over /order
to match the existing /pets
endpoint.
You also want to strive for consistency in naming fields. If you use a limit
parameter on one endpoint, you wouldn’t use max_returned
for another endpoint. Also consider capitalization and punctuation in field names. You wouldn’t want petName
and Pet_ID
fields in the same API. Choose a naming convention and stick with it.
These “rules” aren’t about appeasing perfection. They’re there to help developers have a seamless experience with your API. When names are predictable, sometimes developers won’t even need to reference your documentation to make a tweak to their code.
Continuous integration and delivery
Finally, let’s talk about what happens after your Swagger and OpenAPI definitions are created. You need some way to generate documentation. Ideally, this process would happen automatically. Otherwise, you could go to all this work to describe your API and still end up with outdated documentation!
Many software teams use a continuous integration (CI) pipeline as part of their development workflow. Here, when changes to code are introduced, tests automatically run against the changed code to check for issues. Similarly, when those changes are accepted, teams can automatically deploy the code to a staging environment for further testing, or directly to production if the team has adopted continuous delivery (CD) practices.
Your Swagger or OpenAPI files can use similar processes to keep documentation and other API resources updated. In fact, if your API description is stored alongside your API code, your documentation can be deployed alongside the API it supports.
There are various CI/CD tools, so the exact implementation depends upon your toolset and workflow. ReadMe handles this internally by first generating an OpenAPI file from code with every deploy. We use our swagger-inline library to create the API description, then upload it to our hosted documentation with the rdme Node package.
No matter your workflow, the result should be the same: auto-generated documentation every time the API changes.
Swagger and OpenAPI tools
We’ve already mentioned several ways to use Swagger and OpenAPI files. Because they are machine-readable formats, there are endless ways you could use them. Developers have already created many open source projects based around API descriptions. Pick your use case and check out some tools to give your Swagger and OpenAPI projects a boost.
Generate documentation
The easiest way to see how your OpenAPI or Swagger file looks as documentation is to generate it with ReadMe. You can add a URL to the query string to see it live. Or use our Swagger upload form and simply paste in your Swagger or OpenAPI URL (such as a raw GitHub reference).
To generate a basic reference locally for your OpenAPI project, you might start with an open source tool. There are a handful listed on OpenAPI.tools.
You can render a preview of your API Reference in ReadMe using the form below!
Stub out your code
Whether it is a temporary end to your API while you design the next phase, or a permanent end to each of your API points, here are a few links to help you tie up all your loose ends. The documentation for each package will be very helpful to get you started or keep you going:
- The Node.js package oas-tools, is the OpenAPI 3.0 go-to, as it is an update to swagger-tools and openapi-backend. All three have their uses though, as the last two may be especially useful if you are working on or updating an existing project written in Swagger 1.0, or 2.0.
- If you are writing in Python, falcon-heavy will be your go-to.
- PHP users can find what they need from api-platform or by checking out fusio.
You can find more server implementations at https://openapi.tools/#server.
Test your APIs
When you or your team feel your design is ready for an API testing session, check out these packages:
- OpenAPI Enforcer is another popular choice that works with both OpenAPI 2.0 and 3.0.
- Committee for Ruby is a validator for JSON Schema, OpenAPI 2.0, and OpenAPI 3.0 specific to recent Ruby (versions 2.4+).
These tools should help you understand and troubleshoot your project as it cycles through its various starts and finishes.
Swagger and OpenAPI examples
Many companies maintain Swagger or OpenAPI files to describe their APIs and build documentation. At ReadMe, 85% of customers have an API reference, typically generated directly from an API description file like the ones reviewed above. We’ve gathered some examples of public API definitions so you can learn from what’s already been published.
Swagger Petstore
A classic example is the Swagger Petstore API definition. You can find it in multiple formats and specification versions:
- Swagger / OpenAPI 2.0 YAML and JSON
- OpenAPI 3.0 YAML and JSON
- Expanded example YAML and JSON
- Callback example YAML and JSON
While useful to see these hypothetical examples, you might prefer to see how live APIs have used OpenAPI and Swagger.
API descriptions in production
Most Swagger and OpenAPI files live in private code repositories and behind firewalls. However, there are many examples of public APIs that also publish an API definition. Here are a few to review:
- ReadMe YAML and JSON
- SendGrid YAML and JSON
- Uber YAML and JSON (Swagger / OpenAPI 2.0 format)
- US Patent and Trademark YAML and JSON
That’s just a sampling of what’s available. ReadMe maintains a curated list of example API descriptions.
Still need more examples? Try out this Google search to query the web for “OpenAPI” files with with filetype:YAML.
OpenAPI and future versions of OAS
It’s clear that API descriptions are here to stay. Thousands of companies depend upon these machine-readable definitions. OpenAPI is the next version of Swagger, but they co-exist. We may see other formats rise in popularity and there will certainly be new versions of OpenAPI.
OpenAPI versions
In addition to OpenAPI 2.0 (the backward-compatible Swagger 2.0 format) and OpenAPI 3.0, there are other versions to consider now and into the future.
The current version of OpenAPI (as of June 2020) is version 3.0.3. This version was released in February 2020, following version 3.0.2 (October 2018), 3.0.1 (December 2017), and 3.0.0 (July 2017).
The OpenAPI 3.1.0 release candidate was announced on June 18, 2020. While considered a minor version based on semantic versioning (previous releases were considered patches), the next version has a number of candidate features that warrant the version update. The most significant changes are:
- A new top-level element for describing webhooks that are registered, and managed out of band.
- Support for identifying API licenses using the standard SPDX identifier.
- The PathItems object is now optional to make it simpler to create reusable libraries of components. Reusable PathItems can be described in the components object. There is also support for describing APIs secured using client certificates.
There is discussion within the community about whether the changes within OpenAPI are so large that a major version change to OpenAPI 4.0 would be more appropriate.
With OpenAPI likely to fully adopt JSON Schema with its next release, some features are not fully backward compatible. Regardless of the version number, there will be some effort required to ensure that OpenAPI documents are supported throughout the ecosystem.
Alternatives to OpenAPI
Before OpenAPI existed, there were already some API description formats. Often these formats were championed by organizations with supported tooling.
Some well-known alternative HTTP API description formats include:
- Swagger, which later became OpenAPI
- RAML, based on YAML, which calls itself a “modeling language”
- API Blueprint, a Markdown-like syntax, now part of Oracle
Other related formats include:
- GraphQL, a data query language with an alternative API.
- JSON Schema, a vocabulary for describing JSON data (used in OpenAPI)
- AsyncAPI, a format for event-driven architectures
Swagger solved the problem of documentation out of sync with deployed code, and became the de facto API description format when developers recognized its utility. Machine-readable API definitions opened up a lot of doors to automation for API providers and consumers. The industry has rallied around the OpenAPI format as its successor to Swagger, but any format could overtake it by solving developer problems better.
Generate (beautiful) documentation
For the foreseeable future, OpenAPI remains the standard API description format for defining your API. There are many ways it can be used to improve your APIs, most notably to automatically generate documentation.
The simplicity of the OpenAPI format helps you focus on the details that matter most within your API. When those descriptions translate into beautiful documentation like API references generated by ReadMe, you’ll give developers a much better integration experience. Even better, the documentation will always be in sync with your API, removing one of the biggest developer headaches.
Once you’ve got your hands on an OpenAPI file, try uploading it to ReadMe! We’ll host a beautiful reference guide for your API, for free.