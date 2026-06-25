# Bayt.com Scraper

Extract structured data from [Bayt.com](https://Bayt.com) — job listings from Bayt.com. Get title, company, salary, career level, description, and more from the leading MENA job board.

**[Bayt.com Scraper on Apify →](https://apify.com/blackfalcondata/bayt-scraper?fpr=1h3gvi)**


## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.



## 🚀 How to use this actor

> ### 💚 $5 free Apify credits — every month
> No credit card required. No commitment. Cancel anytime.

### 👉 [Sign up free on Apify →](https://console.apify.com/sign-up?fpr=1h3gvi)

1. **Click sign up** — pick GitHub, Google, or email; takes ~30 seconds
2. **Open this actor** — input is pre-filled with a working example
3. **Click Start** — export results as JSON, CSV, or Excel

Your **$5 monthly platform credit** is enough to run this actor right away — and again every month — scraping typically several hundred to several thousand results per run, depending on your input.


---

## Key features











**Search with filters** — Search by keyword and location. Filter by 🌍 country, 💼 employment type, 📈 career level, and more.

**Detail enrichment** — Fetch full job descriptions, salary data, contact information for each listing.

**Incremental mode** — Only get new or changed listings since your last run. Content hash per listing — no duplicates, no re-processing.

**Change classification** — Track unchanged, expired, cross-run repost detection across runs. Build audit trails of how listings evolve over time.

**Compact output** — Emit core fields only (AI-agent / MCP-friendly). Keeps response size small for LLM workflows.

**Description truncation** — Cap description length per listing to control output size and cost.

**Result cap** — Stop after N listings (up to 1.000). Set to 0 for the full catalog.

**Export anywhere** — Download as JSON, CSV, or Excel. Stream via Apify API, webhooks, or integrations with Make, Zapier, Airbyte, Keboola.

**Structured data** — Every listing returns the same schema with consistent field naming. All fields always present — `null` when unavailable, never omitted.

---

## Use cases











**Data pipeline automation**
Integrate with your ETL pipeline to collect structured listings from bayt.com on a schedule. Export to CSV, JSON, or directly to your database. Use compact mode to control output size.

**Market research**
Monitor listings, track trends, and analyze market dynamics with structured, deduplicated data from bayt.com.

**Change monitoring**
Run daily or hourly in incremental mode to capture only new, updated, or expired listings. Perfect for price-tracking, churn analysis, and alerting pipelines.

**Compensation benchmarking**
Aggregate salary ranges across roles, industries, and locations on bayt.com to inform pricing decisions, hiring plans, or candidate negotiations.

**Lead generation**
Extract employer contact details alongside listings to build outreach lists for recruiters, staffing agencies, or B2B sales teams.

**AI / LLM training data**
Structured JSON per listing is ready for RAG pipelines, embeddings, and agent workflows. Compact mode trims tokens for LLM context windows.

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


## Output fields

Every listing returns the same 33-field schema. Missing values are `null` — never omitted.

- `jobId`
- `title`
- `company`
- `companyUrl`
- `companyLogoUrl`
- `location`
- `city`
- `country`
- `salaryText`
- `salaryCurrency`
- `salaryMin`
- `salaryMax`
- `salaryPeriod`
- `employmentType`
- `careerLevel`
- `yearsOfExperience`
- `industry`
- `companySize`
- `description`
- `skills`
- `nationality`
- `gender`
- `directApply`
- `totalOpenings`
- `isRemote`
- `isExternal`
- `url`
- `applyUrl`
- `postedDate`
- `validThrough`
- `portalUrl`
- `scrapedAt`
- `source`


## Sample output

One object per listing. Here is a real example from a production run:

```json
{
  "jobId": "bc6c5b5dc3adc830cf326f7cf8ab2799ba070c499227c12d90757463ea84989f",
  "title": "Private Executive Assistant (Arabic–English Bilingual)",
  "company": "FYM Catering LLC",
  "companyUrl": "https://www.bayt.com/en/company/fym-catering-llc-2295393/",
  "companyLogoUrl": null,
  "location": "Dubai, UAE",
  "city": "Dubai",
  "country": "AE",
  "salaryText": "AED 7,407 - AED 11,111",
  "salaryCurrency": "USD",
  "salaryMin": 2000,
  "salaryMax": 3000
}
```

*Truncated — full records contain 33 fields. See Output fields for the complete schema.*


**[Try Bayt.com Scraper - Jobs from the Middle East now — $5 free credit, no credit card →](https://apify.com/blackfalcondata/bayt-scraper?fpr=1h3gvi)**


## Pricing

Pay only for what you extract. No subscription required — Apify's free $5 credit covers thousands of results.

| Event | Price (USD) |
| --- | --- |
| Actor Start | $0.01 |
| Result | $0.002 |

See the [actor on Apify](https://apify.com/blackfalcondata/bayt-scraper?fpr=1h3gvi) for current pricing.

---

## Related products by Black Falcon Data











- [StepStone Scraper](https://apify.com/blackfalcondata/stepstone-scraper?fpr=1h3gvi) — Job listings from 18 European portals
- [Indeed Job Scraper](https://apify.com/blackfalcondata/indeed-job-scraper?fpr=1h3gvi) — Indeed job listings with salary data
- [LinkedIn Jobs Scraper](https://apify.com/blackfalcondata/linkedin-jobs-scraper?fpr=1h3gvi) — World's largest professional network — global job listings, no login required
- [Glassdoor Job Scraper](https://apify.com/blackfalcondata/glassdoor-job-scraper?fpr=1h3gvi) — Glassdoor listings with company ratings
- [Arbeitsagentur Scraper](https://apify.com/blackfalcondata/arbeitsagentur-scraper?fpr=1h3gvi) — Germany's official job portal (1M+ listings)
- [SEEK Scraper](https://apify.com/blackfalcondata/seek-scraper?fpr=1h3gvi) — Australia & NZ's largest job board

---


## About Black Falcon Data

Black Falcon Data builds production-grade web scrapers for job boards and marketplace data. Browse our full actor catalog at [www.blackfalcondata.com](https://www.blackfalcondata.com).

---

## Getting started with Apify

New to Apify? [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=1h3gvi) — no credit card required.

1. [Sign up free](https://console.apify.com/sign-up?fpr=1h3gvi) — $5 credit included
2. Open the actor and paste your input
3. Click Start — results download as JSON, CSV, or Excel

Need more volume? [See pricing](https://apify.com/pricing?fpr=1h3gvi).

---

---

*Last updated: 2026 03*
