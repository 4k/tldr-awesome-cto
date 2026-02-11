# Top 10 System Design Interview Questions

**Source:** https://hackernoon.com/top-10-system-design-interview-questions-for-software-engineers-8561290f0444
**Section:** Hiring

---

## Key Insights

**Top 10 System Design Interview Questions:**

1. **URL Shortener (TinyURL/Bitly)**: Generate unique IDs at scale (thousands/second), handle redirects, support custom URLs, delete expired URLs, track click stats

2. **Video Streaming (YouTube/Netflix)**: Store/distribute petabytes of data, handle simultaneous streaming for massive audiences, real-time video stats, live commenting systems

3. **Chat Service (WhatsApp/Messenger)**: One-on-one vs group chat architecture, offline message handling, push notification triggers, end-to-end encryption implementation

4. **Social Network/Forum (Reddit/Quora)**: Post statistics tracking, user following systems, timeline/newsfeed generation algorithms

5. **File Storage (Dropbox/Google Drive)**: File upload/search/sharing workflows, permission management, collaborative document editing

6. **Social Media (Facebook/Twitter)**: Efficient post storage/search, newsfeed generation (often consumes entire interview), social graph management for celebrity-scale followings

7. **Ride Sharing (Uber/Lyft)**: Driver-rider matching algorithms, geolocation storage for millions of moving objects, handling millions of location updates/second

8. **Search Services (Web Crawler/Type-Ahead)**: Query storage and freshness, real-time suggestion matching, handling fast typing, web page prioritization, infinite crawling prevention

9. **API Rate Limiter**: Request limiting within time windows (e.g., 15 requests/second), distributed system rate limiting, soft vs hard throttling

10. **Proximity Service (Yelp)**: Location-based search, distance/review ranking, population density-aware data storage

## Bottom Line

System design interviews test scalability thinking through 10 core patterns: unique ID generation, data distribution, real-time messaging, social graphs, file systems, matching algorithms, search indexing, rate limiting, and geospatial queries.