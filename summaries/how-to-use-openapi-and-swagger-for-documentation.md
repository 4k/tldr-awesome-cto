# How to Use OpenAPI and Swagger for Documentation

**Source:** https://blog.readme.com/how-to-use-openapi-and-swagger-spec-for-documentation/
**Section:** Related stuff

---

## Key Insights

**Core Problem & Solution:**
- Manual API documentation is the biggest developer headache (2019 Postman survey) - becomes outdated, inaccurate, and neglected
- OpenAPI/Swagger solves this by providing machine-readable API descriptions that auto-generate always-current documentation

**Key Technical Differences:**
- Swagger 2.0 (2014) became OpenAPI 2.0 (identical format, starts with `swagger: "2.0"`)
- OpenAPI 3.0+ (2017) is current standard (starts with `openapi: "3.0.0"`)
- OpenAPI 3.0 added "components" section for flexibility and webhook support via "callbacks"

**Automation Opportunities:**
- Generate documentation that deploys with API changes
- Contract testing: validate API responses match specifications automatically
- Auto-generate server stubs, SDKs, mock servers, and code samples in multiple languages
- Integrate into CI/CD pipelines for continuous validation

**Implementation Best Practices:**
- Choose YAML (more human-readable) or JSON (familiar to web devs) - both convertible
- Use REST patterns: organize around resources, use HTTP methods for actions, standard status codes
- Maintain consistent naming conventions (singular vs plural, capitalization)
- Write meaningful descriptions and summaries for human readers
- Start with templates, use editor plugins with linters for syntax checking

**Generation from Existing APIs:**
- Framework-specific tools: `zero-rails_openapi` (Rails), `falcon-apispec` (Python)
- Traffic analysis tools like Optic can generate specs from live API calls

## Bottom Line

OpenAPI specifications solve API documentation hell by creating machine-readable contracts that automatically generate always-current docs while enabling extensive automation for testing, code generation, and CI/CD integration.