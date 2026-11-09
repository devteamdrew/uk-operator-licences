# UK Operator Licence Scraper – HGV & Bus Operators (DVSA VOL)

Export every GB HGV (goods vehicle) and bus/coach (PSV) operator licence from the Traffic Commissioners' VOL register: operator, company number, vehicles and trailers authorised, operating centres, transport managers, licence type. Filter by area, postcode, fleet size. Official OGL data, no key.

**[Run it on Apify →](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=hero)** (pay per result, free Apify account to start)


**UK Operator Licences Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Lead generation for suppliers to hauliers and coach firms: fuel cards, telematics, tachograph analysis, insurance, tyres, truck finance
- Find new HGV operators each week (schedule with incremental mode and sort by newest)
- Map fleets by postcode for depot, workshop or truck-stop site selection
- Recruitment of HGV drivers and transport managers
- Enrich Companies House data with fleet size

## Data source

The Traffic Commissioners' goods and public service vehicle operator licence records (Vehicle Operator Licensing, VOL), published weekly every Sunday on data.gov.uk by the DVSA under the Open Government Licence v3.0. No login, no key.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=quickstart) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "trafficAreas": [
    "North West of England"
  ],
  "licenceCategories": [
    "goods"
  ],
  "minVehicles": 5,
  "maxItems": 20
}
```

## FAQ

**Where does the data come from?**
The Traffic Commissioners' public operator licence register (VOL), exported weekly by the DVSA under the Open Government Licence.

**What do the licence types mean?**
Standard National and Standard International licences carry goods for hire or reward (in GB only, or also abroad); Restricted licences carry the holder's own goods. P-licences are buses and coaches (PSV).

**How do I find new operators?**
Leave sort on `newest` (licence numbers are issued sequentially) and turn on incremental mode on a weekly schedule: you only get licences you haven't seen before.

**Does it include personal data?**
Transport manager and director/partner names are published on the register; turn `includePeople` off to drop them. Sole traders are excluded by default.

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/uk-operator-licences` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=pricing) for current pay-per-result pricing.

## Sample data

Browse real sample rows, download a free CSV sample and see ready-made feeds at [rowsift.co.uk](https://rowsift.co.uk/operator-licences/?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=sample-data).

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [UK Companies House Scraper – Companies & Directors](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [SEC EDGAR Scraper – 10-K, 10-Q & 8-K Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [arXiv Scraper – Paper Search, Abstracts & Authors](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [UK Public Tenders Scraper – Contracts Finder & Find a Tender](https://apify.com/devteamdrew/uk-public-tenders?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [CQC Care Homes & Providers Scraper – Ratings & UK Care Leads](https://apify.com/devteamdrew/uk-cqc-care-providers?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [SAM.gov Contract Opportunities Scraper – US Federal Tenders](https://apify.com/devteamdrew/sam-gov-opportunities?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)
- [USAspending Federal Awards Scraper – Contracts & Grants](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=uk-operator-licences&utm_content=more)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
