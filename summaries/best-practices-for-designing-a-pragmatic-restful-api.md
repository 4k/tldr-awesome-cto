# Best Practices for Designing a Pragmatic RESTful API

**Source:** https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
**Section:** Architecture

---

## Key Insights

**API Design Principles:**
- API is a developer UI - prioritize pleasant experience over academic REST purity
- Use plural nouns for all endpoints (/tickets not /ticket) to avoid pluralization complexity
- Relations: nest dependent resources (/tickets/12/messages), use identifiers for independent relations

**Technical Standards:**
- SSL everywhere, no exceptions - throw hard errors on non-SSL requests, never redirect
- Version in URL (v1) not headers for browser explorability
- JSON only - XML adds verbosity with no real benefit
- snake_case is 20% easier to read than camelCase according to eye-tracking studies

**Query Parameters Framework:**
- Filtering: `?state=open`
- Sorting: `?sort=-priority,created_at` (minus = descending)
- Field limiting: `?fields=id,subject,updated_at`
- Embedding: `?embed=customer.name,assigned_user`

**Response Standards:**
- Pretty print by default - only 0.6% overhead with gzip (which saves 60%)
- Return full resource representation on POST/PUT/PATCH
- No envelopes by default unless JSONP (?envelope=true) or limited HTTP clients

**Pagination & Rate Limiting:**
- Use Link header for pagination (RFC 8288), not envelope data
- Rate limit headers: X-Rate-Limit-Limit, X-Rate-Limit-Remaining, X-Rate-Limit-Reset (seconds remaining, not timestamp)

**Authentication & Caching:**
- Token-based auth over HTTP Basic Auth (stateless)
- Use ETag or Last-Modified headers for HTTP caching
- Support method override via X-HTTP-Method-Override header for limited clients

**Error Handling:**
- Structured JSON errors with code, message, description
- Validation errors: top-level code + detailed errors array with field-specific codes

## Bottom Line
Design APIs as developer UIs with pragmatic choices over academic purity - use consistent patterns, clear documentation, and leverage HTTP standards while prioritizing ease of use and browser explorability.