# Filings Reading Guide

Use this file when an industry study depends on IPO prospectuses, annual reports, 10-K/20-F filings, HKEX documents, or cross-market listed-company comparisons.

## Collecting Filings

Prefer original disclosure files over summaries. Use official regulator and exchange sources first:

- United States: SEC EDGAR for S-1, 424B4, 10-K, 10-Q, 20-F, and 6-K.
- Hong Kong: HKEXnews for annual reports, listing documents, announcements, and prospectuses.
- China A-share: CNINFO and exchange disclosure pages.
- Other markets: use the local official disclosure system when available.

When batch downloading is useful, consider `Eric-KY-Zhang/Filings-Atlas` as a reference tool or workflow inspiration. It is a Windows desktop tool for downloading original official disclosure PDFs across A-share, Hong Kong, United States, Korea, Taiwan, Japan, United Kingdom, and Singapore markets. Its scope is intentionally narrow: it downloads original filings and does not extract financial statements, calculate ratios, produce Excel workbooks, provide investment advice, or bypass private systems.

Repository: https://github.com/Eric-KY-Zhang/Filings-Atlas

Treat this separation as the default operating model:

```text
filing tool = get original materials
industry-cognition = read, compare, model, and form commercial judgment
```

## Filing Set For One Industry

For one industry, build a filing set before analysis:

1. **Category leader**: The clearest listed company in the target industry.
2. **Adjacent leader**: A company that defines a neighboring business model.
3. **Regional contrast**: A company in another geography with different regulation, consumer behavior, or market structure.
4. **Historical anchor**: An older prospectus or annual report that shows how the category was first narrated.
5. **Current update**: The latest annual report, quarterly update, or investor presentation.

For each company, try to collect:

- IPO prospectus or S-1/424B4/listing document.
- Latest annual report or 10-K/20-F.
- Latest investor presentation or earnings transcript when available.
- Segment notes, key metrics, and risk factors.

## Key Number Extraction

Extract numbers into a model-ready base, not into a pile of interesting facts. Every number must keep:

- Source company and filing.
- Filing date and reporting period.
- Page, table, section, or exact source location when available.
- Unit and currency.
- Original label used by the company.
- Your normalized label.
- Definition and calculation notes.
- Whether it is company-reported, third-party market estimate, or your derived estimate.
- Confidence and caveat.

Separate two classes of numbers:

### Market Judgment Numbers

Use these numbers to judge market size, penetration, cycle, and competitive structure:

- TAM/SAM/SOM or addressable-market estimate.
- Total category spend, transaction value, user population, merchant/supplier base, inventory base, or installed base.
- Online penetration, digitalization rate, adoption rate, frequency, retention, or repeat behavior.
- Category growth rate, historical CAGR, expected CAGR, and management's market-growth assumptions.
- Regional split, city-tier split, customer segment split, or use-case split.
- Leader market share, top-N concentration, multi-homing, churn, supplier concentration, or customer concentration.
- Regulation, subsidy, labor, procurement, fulfillment, or payment constraints that change market expansion speed.

Do not accept a TAM at face value. Ask:

- What is included and excluded?
- Is it revenue, gross transaction value, spend, volume, users, or profit pool?
- Is the company using a top-down market report or bottom-up operating data?
- Does the TAM match the company's actual monetization path?
- Which smaller market would be more honest for the next 3-5 years?

### Business And Financial Model Numbers

Use these numbers to build the simplest model that explains the business:

- Volume: orders, trips, transactions, users, active customers, active merchants, suppliers, seats, workloads, devices, listings, or usage.
- Price/AOV/ARPU: average order value, average booking value, revenue per user, revenue per merchant, subscription price, fee per transaction, or take rate proxy.
- Monetization: revenue, take rate, net revenue margin, commission, service fees, subscription, advertising, merchant services, software, payment, financing, or marketplace fees.
- Cost drivers: fulfillment, labor, courier/driver payments, procurement, hosting, model inference, payment processing, customer support, sales and marketing, incentives, subsidies, content, hardware, depreciation, and regulatory costs.
- Margin bridge: gross margin, contribution profit, contribution margin, segment profit, adjusted EBITDA, operating profit, free cash flow, and cash conversion.
- Balance-sheet/capital needs: capex, working capital, inventory, receivables, payables, debt, leases, SBC, and M&A consideration.
- Cohort/unit proxies: retention, payback, LTV/CAC, customer acquisition cost, contribution per order, profit per user, revenue per employee, utilization, fill rate, loss ratio, attach rate, or ad load.

Tie each number to the minimal model:

```text
market size ~= target users or transactions * frequency * price
revenue ~= volume * price_or_AOV * monetization_rate
gross profit ~= revenue - direct_variable_costs
contribution profit ~= gross profit - incentives - sales/marketing - operations directly tied to volume
operating profit ~= contribution profit - fixed platform costs - G&A - R&D
free cash flow ~= operating cash flow - capex - working capital needs
```

Adapt the formula to the category. For marketplace businesses, use GMV/GTV, take rate, order volume, AOV, incentive cost, fulfillment cost, and ads. For SaaS, use customers, seats/workloads, ARPU, gross margin, sales efficiency, retention, and payback. For ecommerce/retail, use GMV/revenue, gross margin, inventory turns, fulfillment, marketing, and working capital. For AI products, add inference cost, model/API cost, human-in-the-loop cost, automation rate, and gross margin after compute.

## Extraction Workflow

Use this workflow before writing the memo:

1. **Build the metric dictionary**: list the company's exact metric names and definitions.
2. **Extract the raw table**: keep original values, periods, units, and labels.
3. **Normalize only after extraction**: convert currencies, periods, and units in a separate normalized column.
4. **Map to model drivers**: tag each number as market, volume, price, monetization, cost, margin, capital, cohort, or risk.
5. **Compare across companies carefully**: do not equate GMV, GOV, GTV, bookings, revenue, or net revenue unless definitions match.
6. **Calculate derived metrics transparently**: show formulas for take rate, AOV, revenue per order, contribution per order, margin as percent of GMV/GTV, and growth rates.
7. **Flag missing numbers**: if a company stops reporting a metric, treat that as a signal and mention the missingness.
8. **Select only decision-grade numbers for the memo**: include numbers that change the industry definition, minimal model, competitive judgment, or trend view.

Use rough derived numbers when useful, but label them as derived estimates. Avoid false precision.

For the main memo, do not spread numbers across many disconnected tables. Pick one anchor company, put its numbers directly into the minimal formula, and use the wider company set to validate whether the formula is robust.

## Model-Ready Number Table

Use this table shape when extracting from filings:

```text
Company | Filing | Period | Original metric | Normalized metric | Value | Unit/currency | Source location | Definition | Model driver | Confidence | Caveat
```

Use this compact table shape in the final memo:

```text
Number | Why it matters | Source | Caveat
```

Prefer a small set of powerful numbers over a large table that does not change judgment.

## How To Read An IPO Prospectus

Read a prospectus as the company's most complete commercial self-description at the time it needed the market to understand the business.

Do not read it front to back by default. Read in this order:

1. **Business Overview**: Identify how the company defines the category, customer, product, network, and value proposition.
2. **Industry Overview / Market Opportunity**: Extract the company's chosen TAM frame. Ask what it includes, excludes, and needs the reader to believe.
3. **Business Model / Revenue Model**: Identify who pays, for what, how take rate or pricing works, and what must scale.
4. **Key Operating Metrics**: Find the few non-financial metrics that explain the business better than revenue alone.
5. **Management Discussion / MD&A**: Track the bridge from operating metrics to revenue, margin, cash flow, and investment needs.
6. **Risk Factors**: Treat risks as the negative-space map of the business model: regulation, concentration, competition, supply, demand, unit economics, platform dependence, and governance.
7. **Use of Proceeds / Strategy**: Understand what the company needs capital to prove.
8. **Financial Statements and Notes**: Use notes to understand revenue recognition, segment reporting, cost classification, customer concentration, stock compensation, leases, and contingent liabilities.

Questions to answer:

- What old industry is this company trying to reclassify?
- What must be true for the TAM to be real?
- Which metric is the company's chosen proof of product-market fit?
- Which cost line reveals the real operating constraint?
- Where does scale help, and where does scale create more variable cost?
- Which risk factor would break the investment story if it worsened?

## How To Read An Annual Report

Read an annual report as a current-state update: what the business has become after reality, competition, regulation, and capital allocation.

Read in this order:

1. **Segment Reporting**: Identify the real business units and profit pools. Segment reporting often reveals the business better than the product narrative.
2. **Key Metrics and Non-GAAP Reconciliations**: Compare operating metrics, gross transaction value, orders, users, take rate, contribution profit, adjusted EBITDA, free cash flow, and margin bridges.
3. **Revenue and Cost Drivers**: Tie each revenue line to the operating variable that creates it. Tie each cost line to the operational bottleneck.
4. **Margin Evolution**: Look for evidence of scale economies, mix shift, pricing power, advertising/merchant-service leverage, or cost discipline.
5. **Cash Flow and Capital Allocation**: Separate accounting profitability from cash generation. Note buybacks, M&A, debt, capex, and SBC.
6. **Risk Factor Changes**: Compare current risks with the IPO story. New or expanded risks often show where the business model is under pressure.
7. **Acquisitions and New Segments**: Ask whether M&A extends the model, fixes a weakness, or buys growth.
8. **Management Language Drift**: Compare wording across years. A shift from "food delivery" to "local commerce" or "merchant platform" is an industry-definition signal.

Questions to answer:

- What has changed since the IPO story?
- Is growth coming from volume, price, take rate, mix shift, ads, geography, M&A, or accounting presentation?
- Is margin improving because the model is better, because investment is slowing, or because the company is shifting to higher-margin revenue?
- Which segment subsidizes another segment?
- What does management stop emphasizing?
- What new word appears repeatedly this year?

## Prospectus vs Annual Report

Use the contrast deliberately:

- **Prospectus**: the company's theory of the market.
- **Annual report**: the market's feedback on that theory.
- **Prospectus risk factors**: what might break.
- **Annual report risk changes**: what actually started breaking or mattered more.
- **Prospectus metrics**: what the company wanted investors to watch.
- **Annual report metrics**: what the business now needs investors to accept.

The best industry insight often comes from the gap between the IPO story and the mature-company reporting structure.

## Extracted Notes Template

For each filing, extract notes in this shape:

```text
Company:
Filing:
Year / filing date:

Industry definition used by company:
Customer / supply-side definition:
Revenue model:
Key operating metrics:
Cost structure:
Segment structure:
Unit-economics proxy:
Market judgment numbers:
Business model numbers:
Competition framing:
Risk factors that matter:
Management language worth noticing:
Implication for industry definition:
Implication for minimal model:
Open questions:
```

Keep extracted notes factual. Put judgment in the industry memo, not in the raw notes.
