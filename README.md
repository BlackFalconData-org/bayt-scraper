# Bayt.com Scraper

Extract structured data from [Bayt.com](https://Bayt.com) — job listings from Bayt.com. Get title, company, salary, career level, description, and more from the leading MENA job board.

**[Bayt.com Scraper - Jobs from the Middle East on Apify →](https://apify.com/blackfalcondata/bayt-scraper)**

---

## Key features




**Search with filters** — Search by keyword and location. Filter by country, employment type, career level, and more.

**Detail enrichment** — Fetch full job descriptions, salary data for each listing.

**Incremental mode** — Only get new or changed listings since your last run. Content hash per listing — no duplicates, no re-processing.

---

## Use cases




**Data pipeline automation**
Integrate with your ETL pipeline to collect structured listings from bayt.com on a schedule. Export to CSV, JSON, or directly to your database. Use compact mode to control output size.

**Market research**
Monitor listings, track trends, and analyze market dynamics with structured, deduplicated data from bayt.com.

---

## Quick start

```json
{
  "query": "software engineer",
  "maxResults": 50,
  "includeDetails": true
}
```

---

## Input parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `query` | string | — | Job search keywords (e.g. 'software engineer', 'marketing'). |
| `country` | enum | `"INTERNATIONAL"` | Which country to search in. |
| `location` | string | — | City or region (e.g. 'Dubai', 'Riyadh'). |
| `employmentType` | enum | — | Filter by employment type. |
| `careerLevel` | enum | — | Filter by career level. |
| `datePosted` | enum | — | Filter by posting recency. |
| `maxResults` | integer | `50` | Maximum total results to return (0 = unlimited). |
| `includeDetails` | boolean | `true` | Fetch full job detail pages (description, skills, salary breakdown, preferred candidate). |
| `descriptionMaxLength` | integer | `0` | Truncate description to N characters. 0 = no truncation. |
| `compact` | boolean | `false` | Core fields only (for AI-agent and MCP workflows). |
| `incrementalMode` | boolean | `false` | Only output new or changed jobs compared to previous run. |
| `stateKey` | string | — | Stable identifier for the tracked search universe. |

---

## FAQ

**Is it legal to scrape Bayt.com?**
Web scraping of publicly available data is generally legal. This actor only accesses publicly visible information that any visitor can see. Always review the target site's terms of service for your specific use case.

**Which countries does Bayt.com cover?**
Bayt.com is the leading job board for the MENA region — Middle East and North Africa. It covers UAE, Saudi Arabia, Egypt, Kuwait, Qatar, Bahrain, Oman, Jordan, Lebanon, and more.

**How does incremental mode work?**
Each listing gets a content hash. On subsequent runs, only new or changed listings are emitted — saving time, compute, and storage. Set `incrementalMode: true` and provide a stable `stateKey` to track a specific search query across runs.

**What is compact mode for?**
Compact mode returns only the core fields (title, company, location, URL, salary) with no full description. It is designed for AI agent and MCP workflows where token budget is limited.

**How do I get full job descriptions?**
Set `includeDetails: true` (the default). The actor fetches each detail page and extracts the full description, skills required, career level, and employer profile.

**Can I filter by salary or career level?**
Yes — use the `careerLevel` and `employmentType` enum filters. Salary filters are not exposed as a direct input parameter but are available via keyword search.

---

## Known limitations

- Bayt.com enforces rate limits on rapid sequential requests. The actor respects these automatically via built-in request throttling.
- Job listings that require a login to view full details (e.g. salary negotiation, hidden employer names) cannot be accessed — only publicly visible data is extracted.
- Search results are limited to what Bayt.com's search engine returns. Very broad queries may return fewer results than expected due to platform-side pagination caps.
- Some fields (salary, phone, contact email) are only present on a subset of listings where the employer chooses to disclose them.

---

## Related products by Black Falcon Data




- [StepStone Scraper](https://github.com/BlackFalconData-org/stepstone-scraper) — Job listings from 18 European portals
- [Indeed Job Scraper](https://github.com/BlackFalconData-org/indeed-job-scraper) — Indeed job listings with salary data
- [Glassdoor Job Scraper](https://github.com/BlackFalconData-org/glassdoor-job-scraper) — Glassdoor listings with company ratings

---

*Last updated: 2026 03*
