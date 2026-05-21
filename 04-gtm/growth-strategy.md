# Growth Strategy Document

**Product:** Nemesis Craft Market  
**Team:** Nemesis  
**Lab:** Lab 9 -- Growth Modeling  
**Date:** 21 May 2026

---

## Activation Metric

A creator is activated when they **publish at least 1 product listing** (firing the `listing_completed` event) **within 48 hours of completing account signup.**

- **Specific action:** Taps "Publish Listing" on the Create Listing screen, triggering the `listing_completed` event
- **Specific number threshold:** 1 completed and published listing
- **Specific time window:** Within 48 hours of account creation

**Why this action indicates real value:**  
Our prototype and design decisions are built around one insight: handmade creators know how to make products but feel uncertain about how to structure the selling process online. A creator who publishes a listing within 48 hours of signup has successfully navigated the full creator activation flow (Marketplace → My Studio → Create Listing → Publish Listing) and experienced the core value of the platform. They now have a live product visible to buyers. Every `listing_completed` event directly grows the marketplace inventory, which is our North Star Metric. A creator who signs up but never publishes a listing has received zero value and generates zero value for buyers.

Our current data: [Assumption: activation rate of 28% based on usability testing of the prototype; will replace with live event data once deployment is live.]

---

## Acquisition Channels

### Channel 1 (Primary): Organic — Instagram and TikTok Handmade Creator Communities

**Type:** Organic

**Why this channel fits our product and audience:**  
Our user interviews showed that handmade creators, specifically those selling crochet items, jewelry, press-on nails, and accessories, spend significant time on Instagram Reels and TikTok discovering and sharing craft content. The hashtag ecosystems around #handmade, #crochetshop, #handmadejewelry, and #smallbusiness have tens of millions of posts and active daily engagement. Creators in this space already document their making process online; showing them how to turn that content into listings on Nemesis is a natural extension of behaviour they already do. This channel requires no paid spend — it requires consistent content output from the team showing the product in use (creator publishes a listing, buyer receives handmade item, etc.).

Crucially, our ICP is already on these platforms and already consumes craft marketplace content. The community exists; we are inserting into it.

**Why we are not prioritising paid advertising as Channel 1:**  
We do not have a marketing budget large enough to compete with Etsy-level paid acquisition. Paid search for terms like "sell handmade products online" is dominated by established players. Our cost-per-click would be high relative to our current conversion data. Paid ads become viable once we have a proven activation rate and enough lifetime value data to justify the spend. For Sprint 2, organic community content is the highest-leverage, lowest-cost option.

**Priority ranking rationale:** Highest reach, zero direct cost, and matches where our ICP already spends time.

---

### Channel 2 (Secondary): Sales — Direct Outreach to Local Craft Fair Vendors and University Craft Communities

**Type:** Sales

**Why this channel fits our product and audience:**  
Tbilisi has an active craft fair and handmade market scene (e.g., Dry Bridge market, weekend pop-up craft fairs, university student markets). Vendors at these events are already selling handmade products but have no digital storefront — they rely entirely on physical presence, which limits their customer base to whoever walks past their stall. These vendors are a high-intent audience: they are already making, already selling, and already understand that more visibility equals more sales. A 5-minute conversation at a craft fair, showing the app and offering to help set up their first listing on the spot, is a direct path to `listing_completed`.

Additionally, KIU and other Tbilisi universities have craft and small-business student communities. A targeted in-person pitch at a student market event or student organisation meetup reaches multiple potential creators in one session.

**Why this is Channel 2 not Channel 1:**  
Sales outreach is high-conversion but low-scale and time-intensive. It does not compound. Once we have covered the main Tbilisi craft fair circuit, the addressable audience from in-person outreach is exhausted. Organic content compounds over time; sales outreach does not.

**Priority ranking rationale:** High conversion rate for supply-side creators, directly produces `listing_completed` events, but limited by team bandwidth and physical geography.

---

### Channel 3 (Tertiary): Viral — Shareable Listing Card

**Type:** Viral

**Status:** Designed, not yet built.

**Why this channel fits our product:**  
Every published listing already has a shareable URL. The loop works like this: a creator publishes a listing (activation event fires) → creator shares their listing card to Instagram Stories or WhatsApp to promote their product → a viewer sees the listing → they tap through, discover the Nemesis platform, browse other listings, and are shown a "Sell your own crafts" CTA → new creator signs up. The loop converts buyers into potential creators, and each activated creator generates their own listing share. This is not yet built as a designed "share this listing" feature — it relies on organic creator behaviour. A designed Share button with a branded card template would formalise it.

We will not include viral as a primary acquisition driver in M1–M2. We model it from M3 onward once the shareable listing card feature is shipped, with K estimated at 0.15 (see Loops and Moats document).

**Why we are not using paid social or affiliate channels in Sprint 2:**  
No budget, no conversion data sufficient to justify spend, and our product is pre-revenue. Affiliate programs require a commission structure we have not built.

---

## Priority Ranking

| Rank | Channel | Type | Rationale |
|------|---------|------|-----------|
| 1 | Instagram/TikTok organic content | Organic | Zero cost, highest reach, audience already present |
| 2 | Craft fair and university in-person outreach | Sales | High conversion, directly produces activation events |
| 3 | Shareable listing card (viral loop) | Viral | Compounds over time but requires feature build first |

---

## Sprint 2 Focus

We will go deep on Channel 1 (organic) and Channel 2 (sales) simultaneously. The split of effort is:
- 60% of creator-facing time on organic content (3 posts per week across Instagram and TikTok, targeting handmade creator hashtags)
- 40% of creator-facing time on in-person outreach (2 craft fair visits or campus events per week, targeting Tbilisi vendors)

Goal by end of Sprint 2: **25 creators with at least 1 published listing** (`listing_completed` fired 25 times by distinct users).
