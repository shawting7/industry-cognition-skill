---
name: industry-cognition
description: "Industry cognition research for strategy operators. Use when the user asks to understand an industry, category, company, business model, market shift, IPO prospectus, annual report, investor material, financing event, founder interview, AI product demo, or startup trend through commercial fundamentals: industry definition, leading-company reference points, prospectus and financial analysis, model-ready key number extraction, simple operating models, competitive structure, and trend signals from founders and investors."
---

# Industry Cognition

## Overview

Use this skill to build and update industry cognition, not to summarize news or produce generic operations tactics. Keep the core stable and the edge adaptive: business fundamentals do not change quickly, but technology, distribution, product form, and cost curves can redefine industry boundaries.

Default to Chinese output when the user writes in Chinese. Prefer clear commercial judgment, explicit assumptions, and rough quantitative ranges over abstract framework language.

## Core Taste

Follow these principles:

- Define the industry before analyzing it, but derive definitions from leading-company narratives, not only from outside labels. Compare how leaders describe themselves in prospectuses, annual reports, investor letters, and segment reporting.
- Use old and new reference points together. A new category needs a leading incumbent or adjacent listed company as the reality anchor.
- Treat IPO prospectuses, annual reports, investor presentations, and earnings call transcripts as the best commercial-model materials.
- Treat founders and investors as trend signals, not as facts by themselves.
- Use financing events as discovery leads only after thresholding for amount, investor quality, and available primary material.
- Build a simple model that makes market size, user demand, competitive structure, and cost behavior visible.
- Keep the memo small. Use a series of leading companies and trend signals to validate the core question, not to create an encyclopedic report.

Avoid:

- Generic operations playbooks.
- Treating every problem as subsidy, traffic, private-domain, or growth hacking.
- Summarizing documents chapter by chapter without forming judgment.
- Consulting jargon that hides weak evidence.
- Over-trusting X posts, podcasts, demo videos, or financing press releases.
- Calling something a trend before identifying which business variable changed.

## Modes

### Industry Memo

Use for a serious industry or category study. Structure the work around:

1. **Main Question**: Frame the study as "what business is this really?" rather than "how does this category operate?"
2. **Industry Definition**: State 3-5 competing definitions first. For each definition, ask: if this were true, which metrics should dominate?
3. **Leader Narratives**: Use representative leaders' prospectuses, annual reports, investor materials, and segment names to test how the industry is narrated by the companies most exposed to it. Notice language drift across time.
4. **Reference Companies**: Identify representative listed leaders and adjacent companies. Use them as reality anchors for metrics, costs, profit pools, and competitive dynamics.
5. **Primary Materials**: Read prospectuses, annual reports, 10-K/20-F filings, investor presentations, earnings call transcripts, and official operating metrics before relying on commentary.
6. **Four-Part Reading Frame**: Extract macro market, user demand, competitive environment, and the simplest financial/operating model that connects the first three.
7. **Key Number Base**: Extract only the numbers that change the market judgment or model. Keep source, year, unit, definition, and confidence attached to each number.
8. **Minimal Model With Data**: Express the business in a small formula or driver tree, then choose one anchor company and substitute real company numbers into the formula. Show derived metrics and caveats.
9. **Trend Signals**: Use startups, founder interviews, product demos, financing events, and investor discussions only to test whether the industry definition or model variables need updating.
10. **Judgment**: Separate what is known, what is inferred, what is uncertain, and what would change the conclusion.

### Quick Scan

Use when the user is just starting a category. Produce:

- 3-5 possible industry definitions.
- The leading-company narratives that would support or challenge each definition.
- Candidate leader and adjacent-company reference set.
- Key metrics to look for in filings under each definition.
- First-pass list of market and model numbers to extract.
- A first-pass simple model.
- Questions that would make the research sharper.

### Trend Update

Use when the user brings a financing event, product demo, founder interview, investor comment, or startup. Do not summarize it as news. Answer:

- What old industry or workflow is it trying to redefine?
- Which business variable may have changed: demand, supply, distribution, trust, cost, pricing, frequency, conversion, retention, or regulation?
- Which listed leaders or adjacent companies are the right reference points?
- What would confirm or falsify the signal?
- Does this update the industry definition, the model, or only the watchlist?

## Source Hierarchy

Prefer sources in this order:

1. Official exchange and regulator filings: SEC EDGAR, HKEXnews, company prospectuses, 10-K, 20-F, annual reports, and listing documents.
2. Company investor relations: shareholder letters, investor presentations, earnings transcripts, operating metrics, and audited financials.
3. Company-owned product material: official demo, docs, customer stories, pricing, product pages, and hiring pages.
4. Founder primary expression: interviews, podcasts, YouTube demos, long-form posts, and public talks.
5. High-signal investor expression: long-form memos, podcasts, YouTube interviews, and X posts from investors with relevant deal flow.
6. Financing databases and press coverage: use as discovery leads, then trace back to founder/investor/product materials.

Use current web search for recent companies, financing, demos, investors, or market events. Cite sources when presenting factual claims or current information.

For filing collection and filing-reading guidance, read `references/filings-reading.md` when the task involves IPO prospectuses, annual reports, 10-K/20-F filings, HKEX documents, SEC filings, or cross-market listed-company comparisons.

## Financing Signal Threshold

Treat financing as a lead, not a conclusion. Include a financing event only if it passes several of these tests:

- **Amount**: Seed or pre-A is usually at least USD 3-5M, unless the founder or investor is exceptional. Series A and later usually at least USD 10M.
- **Investor quality**: Led or joined by high-signal firms or angels with relevant category judgment.
- **Category novelty**: Shows a new industry definition, new workflow, new cost curve, new supply creation, or new distribution path.
- **Material availability**: Founder interview, product demo, official website, customer case, investor memo, podcast, or substantial thread exists.
- **Model relevance**: It can be mapped to a business variable in the industry model.
- **Cross-checkability**: There is enough public material to distinguish real traction from launch storytelling.

When a financing event passes the threshold, search for founder interviews and product demos before writing analysis.

## Investor And Founder Signals

Use investors as signal sources when their public expression helps interpret markets, cost curves, product shifts, or startup formation. Prefer original thinkers close to company formation over generic influencers.

Starter Silicon Valley investor watchlist:

- Sarah Guo and Elad Gil for AI applications, agents, AI infrastructure, and startup formation.
- Vinod Khosla for AI, frontier technology, robotics, healthcare, energy, and disruptive technology.
- Martin Casado for AI infrastructure, model economics, cloud, and developer platforms.
- Bill Gurley and Brad Gerstner for marketplaces, public markets, platform economics, and capital cycles.
- Andrew Chen for consumer, growth, networks, and platform behavior.
- Alex Rampell for fintech, marketplaces, and transaction businesses.
- Garry Tan and Y Combinator for early startup density and batch-level product signals.
- Mike Maples Jr. for category creation and early-market formation.
- Josh Wolfe for deep tech, robotics, defense, and hard-tech commercialization.
- Keith Rabois for marketplaces, SaaS, operating intensity, and company building.

Filter investor content for talking-book bias, portfolio promotion, political noise, and macro overreach.

## Output Shape

For an `industry memo`, use this shape unless the user asks otherwise:

1. **主问题**: Ask what business this industry really is.
2. **候选定义**: List 3-5 definitions. For each, state the metric that should matter if the definition is true.
3. **龙头叙事**: Use a small leader set to show how the category is described in filings and investor materials.
4. **招股书/财报只读四件事**: Macro market, user demand, competition, and the simple model.
5. **极简模型代入**: Show the full formula, then substitute one anchor company's real numbers. Label derived estimates clearly.
6. **需要验证的问题**: Use a series of leaders and adjacent companies to test scale, costs, monetization, and profit pools.
7. **趋势更新**: Include startups, financing, founders, investors, and demos only when they change a model variable.
8. **当前判断**: State what is known, what is inferred, and what would change the conclusion.

Keep the default memo compact. Move large filing extracts, long source tables, and company-by-company notes outside the main memo unless the user asks for them.

## Standard Example

For the food delivery / instant delivery / local life standard example, read `references/food-delivery.md` when:

- Calibrating how to apply this skill.
- The user asks about food delivery, instant delivery, local commerce, local life, DoorDash, Meituan, Uber Eats, Deliveroo, Delivery Hero, Instacart, or adjacent marketplace/logistics questions.
- A concrete example is needed before generalizing to another industry.

For prospectus and annual-report reading, read `references/filings-reading.md`.
