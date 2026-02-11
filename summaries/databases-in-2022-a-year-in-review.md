# Databases in 2022: A Year in Review

**Source:** https://ottertune.com/blog/2022-databases-retrospective/
**Section:** Data

---

## Key Insights

**Funding Reality Check:**
- Database funding dried up in H2 2022 after massive rounds in H1 ($110M+ rounds for Timescale, Voltron Data, Dbt Labs, Starburst)
- Gartner predicts 50% of independent DBMS vendors will fail by 2025
- Companies with billion-dollar valuations are too expensive for acquisition; major cloud providers already have competing offerings
- Survivors will likely be companies that enhance existing DBMSs rather than replace them

**Technical Developments:**
- Google AlloyDB: PostgreSQL with separated compute/storage, WAL processing in storage layer
- Snowflake Unistore: "Hybrid tables" for lower-latency transactions
- Oracle MySQL Heatwave: In-memory vectorized OLAP engine, now available on AWS
- Meta Velox: C++ execution engine (not full DBMS) for building other systems
- InfluxDB IOx: Complete rewrite using DataFusion/Apache Arrow, ditched MMAP

**Blockchain Assessment:**
- FTX (and other crypto exchanges) ran on PostgreSQL, not blockchain databases
- Blockchain transaction latencies: tens of seconds vs. milliseconds for traditional DBMSs
- AWS concluded in 2016 that blockchains were "solution looking for a problem"
- IBM's 2018 blockchain commercial marked technology's peak hype

**Industry Consolidation:**
- Execution frameworks (Velox, DataFusion, Polars) will commoditize OLAP capabilities within 5 years
- Key differentiators will shift to UI/UX and query optimization rather than raw performance
- All modern analytical DBMSs benefit from MonetDB research lineage (Snowflake, DuckDB ancestry)

## Bottom Line
The database industry faces a harsh consolidation period where half of independent vendors will likely fail by 2025, while technical differentiation shifts from performance to user experience as execution engines become commoditized.