# CAP Theorem: Revisited

**Source:** https://robertgreiner.com/cap-theorem-revisited/
**Section:** Technologies

---

## Key Insights
- Networks are unreliable by default - network failures happen frequently and unexpectedly, making partition tolerance mandatory in distributed systems
- CAP theorem forces binary choice: CP (Consistency + Partition tolerance) vs AP (Availability + Partition tolerance) - you cannot avoid choosing
- CP systems: Return timeouts/errors during partitions, choose when business requires atomic reads/writes
- AP systems: Return potentially stale data during partitions, accept writes for later processing, choose when business tolerates eventual consistency
- Network partitions are external factors beyond software control; response to partitions is a deliberate software design decision
- Object-oriented programming assumptions (shared memory, reliability) break down completely in network programming
- The consistency/availability tradeoff must be decided at architecture phase - getting it wrong can doom the application before first deployment

## Bottom Line
CAP theorem in practice means choosing between returning errors during network failures (CP) or returning stale data (AP), since partition tolerance is mandatory in any real distributed system.