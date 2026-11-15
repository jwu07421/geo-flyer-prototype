# GEO-ready Digital Flyer Prototype

Public demo: https://jwu07421.github.io/geo-flyer-prototype/

This is an academic prototype for the CUHK MSc FinTech industrial project (FTEC5910) with Mailaverse. It is a post-generation GEO demonstration, not an official Mailaverse production site.


# Mailaverse GEO Flyer Website Prototype

This folder contains a small static website prototype of Hong Kong local offer flyer pages.

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

## Visible pages and structured data

The public pages are written as a Traditional Chinese Hong Kong promotions directory. Offer facts stay visible in ordinary consumer copy, including the title, flyer image, offer details, key facts, optional FAQ, merchant information, source link and review date.

JSON-LD is embedded in each page `<head>` as `application/ld+json` and is not shown on the visible page. The structured data uses a Schema.org `@graph` (WebSite / WebPage / BreadcrumbList, plus ItemList on the homepage or the merchant Offer entity on detail pages) and preserves Schema.org merchant and offer fields together with Mailaverse-specific extension fields.

## Testing Method

1. Open `index.html` locally or the public GitHub Pages URL.
2. Open a flyer detail page and confirm that structured data is not rendered as visible page copy.
3. Use Google Rich Results Test or Schema Markup Validator on the public URL (or the page source) to inspect the JSON-LD in the document head.
4. Record which standard fields are detected and which project-specific fields remain custom extensions.

## Current Test Pages

The current prototype includes six flyer types:

- Senior dining offer: 八方雲集.
- Retail event promotion: AEON x 日清の出前一丁.
- Local restaurant opening offer: 爭鮮 SUSHI EXPRESS.
- Cashback workflow: 囍筷.
- Cashback with rebate cap and local transit signal: The Madhouse.
- Mid-Autumn recycling coupon: 信和集團.

These examples are selected because they show different schema mapping needs, including membership requirement, event-like redemption mechanics, local address signals, cashback rate, rebate cap, coupon quota, redemption workflow, audience personas, and seasonal semantic triggers.
