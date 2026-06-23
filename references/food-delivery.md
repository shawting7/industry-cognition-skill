# Food Delivery Research Protocol v0

Use this file as the calibration example for `industry-cognition`. The goal is not to memorize the food delivery industry. The goal is to see how the skill turns one category into a structured commercial inquiry.

## Main Question

Do not start with "how to operate food delivery." Start with:

> What kind of business is food delivery: online restaurant retail, local ecommerce, instant fulfillment, a three-sided marketplace, an advertising platform, or local commerce infrastructure?

The answer changes the model, metrics, reference companies, and strategic questions.

## 1. Define The Industry

Do not rush to a conclusion. List several candidate definitions, then ask what the key metrics should be if each definition is true:

- **Restaurant retail online**: The core demand is prepared food consumption moving online.
- **Local ecommerce**: The platform converts nearby offline supply into online transactions.
- **Instant fulfillment network**: The scarce asset is density, dispatch, courier supply, and reliable delivery time.
- **Three-sided marketplace**: Users, merchants, and couriers must all be balanced.
- **Local life infrastructure**: High-frequency food delivery becomes the entry point for in-store services, hotel/travel, instant retail, merchant ads, and local services.
- **Merchant operating system**: The platform monetizes demand generation, ads, SaaS-like tools, and merchant services beyond transaction commission.

For each definition, ask:

- If it is restaurant retail, do order frequency, restaurant supply, and AOV dominate?
- If it is local ecommerce, do local supply density, conversion, and basket expansion dominate?
- If it is instant fulfillment, do delivery time, courier utilization, order density, and cost per order dominate?
- If it is a three-sided marketplace, do subsidy pressure, matching liquidity, and multi-homing dominate?
- If it is local life infrastructure, do cross-sell, ads, membership, merchant tools, and adjacent categories dominate?

Definitions should be tested against leading-company narratives. Look for how Meituan, DoorDash, Uber, Deliveroo, Delivery Hero, Just Eat Takeaway, Wolt, and Instacart describe the category in prospectuses, annual reports, segment names, investor presentations, and management language.

## 2. Leader Reference Set

Use a leader and adjacent-company set:

- **China**: Meituan as the central listed reference. Use Alibaba Local Services/Ele.me only as an adjacent competitive reference because it is not a standalone listed entity.
- **United States**: DoorDash for food delivery and local commerce; Uber/Uber Eats for network reuse between mobility and delivery.
- **Europe/global**: Deliveroo, Delivery Hero, Just Eat Takeaway, and Wolt as market-structure and regional comparison points.
- **Adjacent categories**: Instacart for grocery/instant retail; Uber for logistics-network reuse; restaurant SaaS/POS companies for merchant-side profit pools.

Use official filings, prospectuses, annual reports, investor presentations, and earnings materials before using commentary.

Leaders are not included to admire the leader. They are included to establish reality anchors: how scale is built, where losses happen, where profit sits, and which narrative survives contact with public-market reporting.

## 3. Read Filings For Four Things

Read prospectuses and financial reports for four things:

1. **Macro market**: Is the TAM restaurant spend, delivery spend, local commerce, grocery, advertising, or total local life consumption?
2. **User demand**: Is the user buying convenience, time, certainty, selection, price, habit, or membership value?
3. **Competition**: Does the market compete on subsidies, courier density, merchant supply, delivery time, ads, membership, exclusive supply, or ecosystem bundling?
4. **Simple model**: Which operating variables explain the economics?

Prefer official entry points: SEC EDGAR for U.S.-listed companies, HKEXnews for Hong Kong filings, and company investor-relations pages for annual reports, investor decks, and transcripts.

## 4. Minimal Model With One Company's Data

Start with:

```text
profit ~= order volume * average order value * take rate
        + ads and merchant services revenue
        - courier and fulfillment cost
        - user subsidies
        - merchant incentives
        - acquisition and operations cost
        - technology, support, risk, and fixed costs
```

Then choose one anchor company and substitute real numbers from one filing. The point is not perfect valuation precision; it is seeing which variables drive the business.

Example shape:

```text
company:
period:

gross transaction value ~= orders * average order value
platform revenue ~= gross transaction value * net revenue margin
contribution profit ~= gross transaction value * contribution margin
adjusted EBITDA ~= gross transaction value * adjusted EBITDA margin

derived:
average order value ~= gross transaction value / orders
revenue per order ~= platform revenue / orders
contribution per order ~= contribution profit / orders
```

Use the company's own definitions for GOV/GTV/Bookings/GMV, revenue, contribution profit, adjusted EBITDA, orders, and users. Do not equate metrics across companies unless definitions match.

Then ask:

- Does order density lower cost per order?
- Can take rate rise, or is it capped by restaurant margins and regulation?
- Is advertising a better profit pool than commission?
- Does membership raise frequency and reduce subsidy dependence?
- Does instant retail improve AOV and frequency, or add fulfillment complexity?
- Does scale create a defensible local network, or does multi-homing keep competition intense?
- Where does profit sit: user fees, merchant commission, ads, logistics efficiency, software tools, or ecosystem cross-sell?

## 5. Trends As Cognition Updates

Treat new signals as model updates, not as conclusions:

- **AI**: dispatch optimization, customer service, personalized search, merchant tools, pricing, demand prediction, and content/ads generation.
- **Robotics/autonomy**: potential changes to courier cost, reliability, and delivery geography.
- **Instant retail**: category expansion from meals into grocery, convenience, pharmacy, and local SKUs.
- **Merchant stack**: POS, CRM, inventory, ads, and operating tools may move profit toward merchant services.
- **Consolidation**: M&A can indicate mature-market structure, capital discipline, or a need for scale density.

For every startup, demo, or financing event, ask which variable changes: demand, supply, courier cost, delivery reliability, merchant monetization, AOV, frequency, or advertising yield.

Financing information is allowed, but threshold it. Include a financing event only when the amount is meaningful, investor quality is high, founder interviews or product demos exist, and the company can explain a new model variable. DoorDash acquiring Deliveroo is an industry-structure signal; an ordinary funding press release is usually only a search lead.

## Standard Output Angle

A strong first judgment might look like:

> Food delivery is best understood as local ecommerce with instant fulfillment constraints. Its first profit pool is transaction monetization, but mature platforms increasingly seek better economics through advertising, membership, merchant services, and adjacent instant retail. The core question is whether density and local network effects can offset high variable fulfillment costs and persistent multi-sided subsidy pressure.

Use this as a tonal reference: concrete, commercially grounded, and open to revision.

## Generalizable Rule

For any industry, do not start by searching hot topics. Use this order:

```text
define the industry -> find leader references -> read filings -> build a minimal model -> use startup and investor signals to update cognition
```
