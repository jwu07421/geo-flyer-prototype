# GEO-ready Digital Flyer Prototype

Public demo: https://jwu07421.github.io/geo-flyer-prototype/

This is an academic prototype for the CUHK MSc FinTech industrial project (FTEC5910) with Mailaverse. It is a post-generation GEO demonstration, not an official Mailaverse production site.


# Mailaverse GEO Flyer Website Prototype

This folder contains a small static website prototype for testing AI-readable flyer pages.

## Structure

- `index.html`: homepage listing selected flyer cards.
- `offers/offer_001_bafang.html`: flyer detail page for 八方雲集.
- `offers/offer_002_aeon.html`: flyer detail page for AEON.
- `offers/offer_003_sushi_express.html`: flyer detail page for 爭鮮 SUSHI EXPRESS.
- `offers/offer_004_hei_chop.html`: flyer detail page for 囍筷 33% cashback.
- `offers/offer_005_madhouse.html`: flyer detail page for The Madhouse 50% cashback.
- `offers/offer_006_sino_mooncake_recycling.html`: flyer detail page for 信和集團 mooncake tin recycling coupon.
- `assets/css/style.css`: shared page styling.
- `sitemap.xml`: list of prototype URLs for crawl discovery.
- `robots.txt`: basic crawler access policy and sitemap location.

## Prototype Purpose

The prototype tests whether selected flyer information can be represented as:

- visible semantic text for users and AI-assisted search;
- persona-oriented visible content showing who the offer may be relevant to, what they may search for, and which trigger words describe the context;
- direct question-and-answer sections that reflect natural search language;
- clear headings, lists, breadcrumbs and consistent page vocabulary;
- source links, update information and explicit data limitations as authority signals;
- embedded JSON-LD structured data for search engine readability;
- Schema.org-compatible fields plus Mailaverse-specific extension fields.

The prototype does not use keyword stuffing or hidden promotional text. Important information is placed in visible summaries, factual question-and-answer sections, image alt text and structured data. This keeps the semantic layer useful to people as well as machine-readable systems.

## Testing Method

1. Open `index.html` locally.
2. Click each flyer card to open its detail page.
3. Copy the detail page HTML into Google Rich Results Test using Code mode.
4. Copy the JSON-LD block into Schema Markup Validator.
5. Record which standard fields are detected and which project-specific fields remain custom extensions.

## Detail Page Structure

Each flyer detail page follows the same structure:

1. Breadcrumb navigation and a descriptive page title.
2. Original flyer image with descriptive alt text.
3. Visible semantic summary answering what the offer is.
4. Extracted merchant, offer, validity, redemption, audience and location fields.
5. Visible semantic persona section with a target audience, likely search question and trigger words.
6. Question-and-answer section covering user intent.
7. Source, update and limitation information.
8. JSON-LD in the page head for the merchant, offer and custom project fields.

## Current Test Pages

The current prototype includes six flyer types:

- Senior dining offer: 八方雲集.
- Retail event promotion: AEON x 日清の出前一丁.
- Local restaurant opening offer: 爭鮮 SUSHI EXPRESS.
- Cashback workflow: 囍筷.
- Cashback with rebate cap and local transit signal: The Madhouse.
- Mid-Autumn recycling coupon: 信和集團.

These examples are selected because they show different schema mapping needs, including membership requirement, event-like redemption mechanics, local address signals, cashback rate, rebate cap, coupon quota, redemption workflow, audience personas, and seasonal semantic triggers.
