# Crawlomatic Data Engine ⚡

> **High-Performance Web Extraction & Technographics Infrastructure**  
> Powering enterprise web data collection, technographics scanning, and B2B market intelligence with zero proxy setup.

[![Apify Partner](https://img.shields.io/badge/Apify%20Store-View%20Catalog-brightgreen?logo=apify)](https://apify.com/misterkhan)
[![Website](https://img.shields.io/badge/Website-crawlomatic.com-blue)](https://crawlomatic.com)
[![Engine](https://img.shields.io/badge/Engine-Thin%20Rust%20%2B%20CDP-orange)](https://crawlomatic.com)

---

## 🚀 Featured B2B Scrapers & Data APIs

All scrapers run on the **Crawlomatic Rust Engine**, featuring automatic residential/ISP proxy routing, 6-WAF challenge solvers (Cloudflare, DataDome, PerimeterX, Kasada, Akamai, AWS WAF), and Pay-Per-Event (PPE) pricing.

### 💼 B2B Software & Customer Reviews
- **[G2 Reviews Scraper](https://github.com/crawlomatic/g2-reviews-scraper)** — Extract 1–5 star ratings, pros & cons, business problems solved, and reviewer titles from G2.com.
- **[Capterra Reviews Scraper](https://github.com/crawlomatic/capterra-reviews-scraper)** — Software reviews, ratings, pros/cons, and pricing feedback from Gartner Digital Markets.
- **[Trustpilot Reviews Scraper](https://github.com/crawlomatic/trustpilot-reviews-scraper)** — Customer sentiment, verified reviews, and brand ratings.

### 👔 Jobs, Recruiting & Talent Intelligence
- **[Indeed Jobs Scraper](https://github.com/crawlomatic/indeed-jobs-scraper)** — Real-time job postings, compensation, company metadata, and hiring locations.
- **[Glassdoor Jobs & Reviews Scraper](https://github.com/crawlomatic/glassdoor-jobs-scraper)** — Job openings, employee reviews, salaries, and CEO approval ratings.

### 🛍️ E-Commerce & Luxury Market Intelligence
- **[Shopify Products Scraper](https://github.com/crawlomatic/shopify-products-scraper)** — Fast-path catalog extraction (prices, variants, images, inventory) from any Shopify store.
- **[Chrono24 Listings Scraper](https://github.com/crawlomatic/chrono24-listings-scraper)** — Secondary market luxury watch listings, dealer prices, specs, and conditions.

### 🏡 Real Estate & Commercial Property
- **[Zillow Real Estate Scraper](https://github.com/crawlomatic/zillow-real-estate-scraper)** — For-sale, rentals, sold homes, and MLS data across the US.
- **[Realtor.com Scraper](https://github.com/crawlomatic/realtor-com-scraper)** — US property listings, school ratings, and agent data.
- **[Redfin Scraper](https://github.com/crawlomatic/redfin-scraper)** — Market listings, property history, and walk scores.
- **[Rightmove UK Scraper](https://github.com/crawlomatic/rightmove-uk-scraper)** — UK residential homes, floorplans, and council tax data.
- **[Zoopla UK Scraper](https://github.com/crawlomatic/zoopla-uk-scraper)** — UK properties for sale/rent and Zed-Index estimates.
- **[BizBuySell Scraper](https://github.com/crawlomatic/bizbuysell-business-scraper)** — Businesses for sale, franchise opportunities, EBITDA, and broker leads.

### 📍 Local Leads & Advertising Intelligence
- **[Google Maps Places Scraper](https://github.com/crawlomatic/google-maps-places-scraper)** — Local business leads, addresses, phones, and review counts.
- **[Facebook Ad Library Scraper](https://github.com/crawlomatic/facebook-ads-library-scraper)** — Competitor active ads, creatives, copy, and spend signals.
- **[Website Tech Stack Scanner](https://github.com/crawlomatic/website-tech-stack-scanner)** — Detect 6,000+ technologies, CMS, analytics, pixels, and CDNs.
- **[Universal Web Unblocker](https://github.com/crawlomatic/universal-web-unblocker-api)** — Autonomous AI extractor solving anti-bot challenges on any site.

### 🏨 Travel & Vacation Rentals
- **[Booking.com Reviews Scraper](https://github.com/crawlomatic/booking-reviews-scraper)** — Verified guest reviews, hotel ratings, and traveler breakdowns.
- **[Airbnb Reviews Scraper](https://github.com/crawlomatic/airbnb-reviews-scraper)** — Guest reviews, host ratings, and stay cleanliness scores.
- **[Vrbo Reviews Scraper](https://github.com/crawlomatic/vrbo-reviews-scraper)** — Vacation rental traveler feedback and ratings.

---

## ⚡ How to Integrate

All Crawlomatic actors are available on the **[Apify Store](https://apify.com/misterkhan)** and can be invoked with standard SDKs:

### Python
```bash
pip install apify-client
```

```python
from apify_client import ApifyClient

client = ApifyClient("YOUR_APIFY_TOKEN")
run = client.actor("misterkhan/g2-reviews-scraper").call(run_input={
    "startUrls": [{"url": "https://www.g2.com/products/slack/reviews"}],
    "maxItems": 25
})

items = client.dataset(run["defaultDatasetId"]).list_items().items
print(f"Extracted {len(items)} items!")
```

### Node.js
```bash
npm install apify-client
```

```javascript
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: 'YOUR_APIFY_TOKEN' });
const run = await client.actor('misterkhan/g2-reviews-scraper').call({
    startUrls: [{ url: 'https://www.g2.com/products/slack/reviews' }],
    maxItems: 25
});

const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(`Extracted ${items.length} items!`);
```

---

## 🌐 Links & Resources

- 🌐 **Platform Website:** [crawlomatic.com](https://crawlomatic.com)
- 🛒 **Apify Store Hub:** [apify.com/misterkhan](https://apify.com/misterkhan)
- 📧 **Enterprise Support:** support@crawlomatic.com
