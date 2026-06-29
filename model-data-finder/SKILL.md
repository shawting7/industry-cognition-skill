---
name: model-data-finder
description: "Build leader-anchored data packs and target-company model inference for industry memos using both IPO prospectus/listing-document data and latest annual-report data. Use after an industry, company, or new business model has been defined and Codex needs listed leader narratives, prospectus-era full historical numbers, latest annual-report calibration, comparable-company unit economics, proxy ranges, target-company inferred formula numbers, or analysis of which variables and environmental differences could change the business model. Use especially with industry-cognition when a memo has a formula but needs anchor data from leading public companies plus inferred numbers for a specific company, segment, startup, or undisclosed business."
---

# Model Data Finder

## Overview

Use this skill to bridge from leading-company facts to target-company inference. The goal is not merely to "find data"; the goal is to use listed leaders as numerical anchors, then infer what must be true for a specific company, segment, or new business model to work.

Do not write a second industry memo. Produce a compact data-and-inference layer that can be inserted into an industry memo.

## Core Taste

- Start from leader narratives and leader data. A model needs a reality anchor before it can infer a new business.
- Use a double anchor for each important leader: the IPO prospectus or listing document for the original business theory, and the latest annual report for reality calibration.
- Extract enough prospectus-era data and latest annual-report data to make the model visible, not just one convenient number.
- Use the leader's own reporting definitions before normalizing metrics.
- Treat the target company as an inference problem: what is directly disclosed, what can be proxied, what must be assumed, and what variables differ from the leader.
- Distinguish four labels clearly: **reported**, **derived**, **proxy**, and **inferred**.
- Missing target data is not the end of the work. Use leader data to bracket the model, then say which assumptions drive the inference.
- Never present inferred numbers as company disclosure.
- End with what changes the business judgment: scale, monetization, cost curve, working capital, regulation, user behavior, supply density, or competitive structure.

## Decision Tree

1. **Target has direct data**: build the target formula with reported and derived numbers, then compare with leaders.
2. **Target lacks direct data but leader anchors are strong**: build a leader model, map target variables to leader variables, and produce inferred ranges with assumptions.
3. **Target lacks direct data and leader anchors are weak**: build the best leader data pack available, then output a variable-difference map instead of fake ranges.
4. **The task is only a quick scan**: list the model variables and the best anchor companies to search later.

## Workflow

### 1. Restate The Target Model

Start from the formula in the industry memo. Rewrite it into measurable variables.

Example:

```text
target profit ~= active customers or merchants
              * frequency
              * average order value
              * monetization or gross margin
              + ancillary revenue
              - fulfillment / delivery / operations cost
              - incentives / subsidies
              - sales / support
              - working-capital, inventory, or risk cost
              - fixed platform cost
```

### 2. Select Leader Anchors

Choose anchors deliberately:

- **Primary leader**: the closest listed company or segment with the same economic mechanism.
- **Adjacent leader**: a neighboring model that reveals a cost line, margin structure, or profit pool.
- **Regional contrast**: a similar business in another market with different regulation, density, labor, or consumer behavior.
- **Mature-state anchor**: a company that shows what economics look like after scale.

Prefer public companies with filings over private-company commentary. Explain why each anchor matters.

### 3. Collect The Double Anchor Filing Set

For every important leader, try to collect two documents:

1. **Prospectus anchor**: IPO prospectus, S-1, 424B4, listing document, or earliest full public filing. This shows the company's original business definition, market theory, historical growth, key metrics, customer/supplier structure, revenue model, cost structure, and risk map.
2. **Latest annual-report anchor**: latest 10-K, 20-F, annual report, or full-year results. This shows what the business became after scale, competition, regulation, M&A, capital allocation, and reporting changes.

Do not skip the prospectus when it is available. The prospectus often contains the fullest explanation of the business model and historical operating data. Do not use the latest annual report alone unless the prospectus is unavailable or irrelevant.

### 4. Extract A Complete Prospectus Data Pack

From the prospectus/listing document, extract:

- Original industry definition and category framing.
- Market size/TAM frame and what it includes or excludes.
- Historical financials, usually 2-3 years if available.
- Historical operating metrics: users, merchants, orders, GMV/GTV/GOV, stores, customers, suppliers, SKUs, cohorts, retention, utilization, or other category-specific KPIs.
- Revenue model: who pays, pricing, take rate, commissions, fees, advertising, subscription, supplier rebates, software, financing, or services.
- Cost structure: COGS, fulfillment, labor, procurement, sales and marketing, incentives, technology, operations, support, depreciation, logistics, warehousing, inventory, payment, risk.
- Unit-economics proxies: contribution margin, gross margin, order economics, payback, revenue per customer/merchant/order, AOV, frequency.
- Segment structure and geographic/customer mix.
- Risk factors that reveal the model's fragility.
- Use of proceeds and strategy, because it shows what capital is needed to prove.

### 5. Extract The Latest Annual-Report Calibration

From the latest annual report or full-year filing, extract:

- Current scale: revenue, GMV/GTV/GOV, order volume, users, merchants, locations, customers, stores, or units.
- Current segment reporting and whether the original business has been reclassified.
- Current margin bridge: gross profit, contribution profit, adjusted EBITDA, operating profit, free cash flow.
- Current cost drivers and whether scale improved or worsened them.
- Mix shift: product, geography, customer, category, ads, services, marketplace vs first-party, high-margin vs low-margin.
- Capital intensity: capex, working capital, inventory, receivables, payables, debt, leases, M&A.
- Management language drift: new words, missing words, changed KPIs.
- Risk factor changes versus the prospectus story.

### 6. Build The Leader Evolution Bridge

Compare the prospectus anchor with the latest annual-report anchor:

```text
Metric / narrative | Prospectus anchor | Latest annual report | Change | Meaning for model
```

Ask:

- Which part of the original story survived?
- Which metric became more or less important?
- Did the profit pool move from transaction revenue to ads, software, services, financing, membership, or private-label?
- Did scale improve gross margin, contribution margin, operating margin, or working capital?
- Did the company stop reporting a metric? If yes, treat that as a signal.

### 7. Extract A Complete Leader Data Pack

For the most relevant leader, extract the fullest practical set of numbers:

- Scale: revenue, GMV/GTV/GOV, order volume, customers, merchants, stores, locations, users, or units.
- Price/frequency: AOV, ARPU, purchase frequency, revenue per unit, revenue per customer, basket size.
- Monetization: take rate, net revenue margin, gross margin, commission, ads, merchant services, subscription, software, payment, supplier rebates.
- Cost curve: fulfillment, labor, procurement, hosting/inference, warehousing, delivery, sales, support, subsidies, incentives, spoilage, returns.
- Margin bridge: gross profit, contribution profit, adjusted EBITDA, operating profit, free cash flow.
- Capital intensity: capex, inventory, working capital, receivables, payables, debt, leases.
- Operating structure: segment reporting, language drift, risk factors, and management's chosen proof metrics.

Use this table shape:

```text
Company | Filing / period | Reported metric | Value | Unit | Formula role | Label | Source | Caveat
```

### 8. Build The Leader Formula

Convert the leader's numbers into a formula or unit-economics bridge.

Examples:

```text
revenue ~= volume * AOV * take_rate
gross_profit ~= revenue * gross_margin
operating_profit ~= revenue * operating_margin
contribution_profit_per_order ~= contribution_profit / orders
working_capital_need ~= inventory + receivables - payables
```

Show derived calculations transparently. Avoid false precision.

When possible, build two formulas:

- **Prospectus formula**: what the business looked like at listing or early public disclosure.
- **Current formula**: what the business looks like in the latest annual report.

The gap between them is often the strongest evidence for how the model actually scales.

### 9. Map Leader Variables To The Target

Build a target inference map:

```text
Target variable | Leader anchor | Target disclosed? | Inference method | Difference variable | Confidence
```

Difference variables are the heart of the work. Common differences:

- Market density and delivery distance.
- Labor cost, supply availability, and regulation.
- Merchant margin tolerance and bargaining power.
- User willingness to pay, AOV, frequency, and substitution behavior.
- Category mix, SKU complexity, cold chain, inventory risk, or perishability.
- Platform ecosystem advantage: traffic, ads, membership, payments, financing, merchant tools.
- Competitive structure: incumbent strength, subsidy intensity, multi-homing, switching cost.
- Stage: launch, scaling, mature, or consolidation.

### 10. Infer Target Formula Numbers

Only infer after the anchor model is visible. Use ranges when appropriate:

```text
target_variable ~= leader_metric * adjustment_factor
```

Label every number:

- **reported**: target company disclosed it.
- **derived**: calculated from target disclosures.
- **proxy**: borrowed from leader or comparable company.
- **inferred**: estimated by applying adjustments to proxy or partial data.

Do not infer a full P&L if the assumptions are too weak. Infer the few variables that drive the judgment.

### 11. Judge Whether Variables Change

End with the answer the industry memo needs:

- Does the target have the same business model as the leader, or a materially different one?
- Which variables must be better than the leader for the target to work?
- Which variables are structurally worse?
- Does the target change the industry definition, the cost curve, the profit pool, or only the go-to-market path?
- What data would confirm or falsify the inference?

## Output Shape

Use this compact shape:

1. **龙头锚点**: leader companies and why they are the right anchors.
2. **招股书原始模型**: prospectus narrative, historical numbers, original metrics, and original formula.
3. **最新年报校准**: latest annual-report numbers, current segment structure, current formula, and margin/cost reality.
4. **龙头演化桥**: what changed from prospectus to latest annual report and what that means.
5. **目标公司映射**: target variables mapped to leader variables.
6. **目标公式推断**: inferred ranges or variable assumptions, clearly labeled.
7. **差异化变量**: what differs from the leader and why it matters.
8. **判断影响**: whether the data changes the industry memo's conclusion.
9. **待验证数据**: the shortest list of missing data that would most improve confidence.

Default to Chinese when the user writes Chinese.

## Proxy Guidance

Choose anchors by economic mechanism:

- **Marketplace**: DoorDash, Uber, Meituan, Delivery Hero, Instacart. Use GMV/GOV/GTV, orders, AOV, take rate, contribution margin, ads, incentives, fulfillment.
- **Food delivery/local commerce**: use order density, delivery cost, ads, membership, merchant services, instant retail mix.
- **B2B distribution / supply chain**: Sysco, US Foods, Performance Food Group. Use sales, gross margin, operating expense ratio, operating margin, inventory turns, receivables, payables, delivery density.
- **Restaurant supply / food industrialization**: use frozen food, condiment, central kitchen, and chain restaurant suppliers only when manufacturing or standardized SKU economics are relevant.
- **SaaS/software**: use ARR/revenue, customers, ARPU, gross margin, retention, sales efficiency, CAC payback, operating margin.
- **AI products**: use revenue/usage, gross margin after inference, model/API cost, human-in-the-loop cost, automation rate, seat/workload usage.
- **Retail/ecommerce**: use GMV/revenue, gross margin, fulfillment cost, inventory turns, return rate, marketing cost, working capital.

## Handling Undisclosed Targets

For targets without standalone disclosure:

1. State direct target data is unavailable.
2. Do not stop there.
3. Build the best leader anchor model.
4. Infer only the target variables that can be bounded by leader data and known environmental differences.
5. Treat non-disclosure as a signal about capital-market importance, but do not let it replace business-model inference.

## Example: Kuailv

For Meituan Kuailv / 快驴:

- Target direct data is limited because Meituan does not disclose Kuailv as an independent segment.
- Do not estimate Kuailv GMV or profit as if disclosed.
- Use mature foodservice distributors such as Sysco, US Foods, or Performance Food Group as mature-state B2B distribution anchors.
- For each anchor, prefer the IPO/listing-era filing plus latest annual report. If the IPO prospectus is not practical to obtain quickly, state the limitation and use the earliest available full filing as the historical anchor.
- Build the leader model first from both anchors: sales, gross margin, operating expense burden, operating margin, working capital, and inventory/receivables/payables.
- Then infer Kuailv's variables by comparing environment:
  - Chinese small restaurant fragmentation may improve customer count but worsen fulfillment density and sales/service cost.
  - Fresh/perishable SKU mix may worsen loss and cold-chain complexity.
  - Meituan's merchant relationship may lower acquisition cost but may not solve procurement price and credit risk.
  - If Kuailv has private-label or standardized SKU mix, margin upside may improve.

Good Kuailv output should say:

```text
Do not calculate Kuailv as if it disclosed a P&L. Use Sysco-like mature distribution economics as the anchor, then test whether Kuailv's China restaurant supply environment improves or worsens each variable.
```
