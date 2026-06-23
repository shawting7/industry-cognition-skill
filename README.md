# Industry Cognition Skill

A Codex skill for strategy operators and industry researchers.

Its purpose is not to help AI write longer industry reports. It is to help AI form sharper industry judgment.

The taste is simple: less news roundup, more business common sense; less framework theater, more leader-based reference points; less "a new trend is coming", more "which business variable actually changed?"

## Taste

This skill prefers research that behaves like this:

- **Ask what business it really is**: Industry research does not start with news. It starts with definition. Is food delivery a restaurant business, ecommerce, an instant fulfillment network, an ad platform, or local commerce infrastructure? Each answer points to different metrics.
- **Start from leader narratives**: Industry definition should not come only from outside labels. Read how representative companies describe themselves in IPO prospectuses, annual reports, investor materials, segment reporting, and management language.
- **Treat public filings as hard material**: A prospectus is the moment when a company must explain its business model clearly. An annual report is reality's feedback on that narrative. The gap between the two is often more revealing than commentary.
- **Put numbers into formulas**: Key numbers are not collected to make tables look serious. They should enter a minimal model and change the judgment on market size, costs, profit pools, or competition.
- **Use trends only as cognition updates**: Founders, investors, financing events, and product demos are useful only when they answer one question: did this change a core variable of the business?
- **Prefer small and hard over broad and soft**: The default output should feel like a research protocol or judgment skeleton, not an encyclopedic industry report.

## What It Refuses

This skill tries to avoid:

- Turning industry research into news summarization.
- Explaining every industry through traffic, subsidies, private-domain growth, or growth hacks.
- Using words like "enablement", "ecosystem", "closed loop", or "disruption" as substitutes for judgment.
- Treating financing news as a trend by default.
- Summarizing a prospectus chapter by chapter without forming a commercial view.
- Listing many companies and numbers while failing to answer: what business is this, really?

## Research Protocol

Default sequence:

```text
define the industry -> find leader references -> read filings -> build a minimal model -> use startup and investor signals to update cognition
```

More concretely:

1. **Define the industry**: List 3-5 candidate definitions and identify the metrics that would matter under each definition.
2. **Find leader references**: Select listed leaders and adjacent companies as reality anchors.
3. **Read filings**: Extract only four things: macro market, user demand, competitive environment, and the simplest model.
4. **Build a minimal model**: Choose one anchor company and substitute real numbers into the formula.
5. **Update cognition**: Use founders, investors, financing events, and product demos to test whether any model variable changed.

## Example Questions

Good prompts:

```text
Use $industry-cognition to study restaurant supply chains.
```

```text
Use $industry-cognition to run a food delivery research protocol.
```

```text
Use $industry-cognition to judge whether an AI product demo changes an industry variable.
```

This skill is especially useful for questions like:

- What kind of business is food delivery, really?
- Should restaurant supply chains be understood as wholesale distribution, food industrialization, or chain-restaurant infrastructure?
- Does an AI agent change labor cost, delivery model, workflow ownership, or just the packaging layer in a SaaS category?
- Which prospectus and annual-report numbers can support market judgment and a business model?

## Expected Output

The default output is not a full industry report. It is a compact judgment skeleton:

- **Main question**: What business is this industry really in?
- **Candidate definitions**: Which metrics would matter under each definition?
- **Leader narratives**: How do listed companies describe themselves and the industry?
- **Four things from filings**: Macro market, user demand, competition, and minimal model.
- **Model with data**: Pick one anchor company and put real numbers into the formula.
- **Validation questions**: Use more leaders and adjacent companies to test the judgment.
- **Trend updates**: Treat startups, financing, investors, and demos only as model-variable updates.
- **Current view**: What is known, what is inferred, and what would change the conclusion.

## Install

Clone this repository into your local Codex skills directory:

```bash
git clone git@github.com:shawting7/industry-cognition-skill.git ~/.codex/skills/industry-cognition
```

If a skill with the same name already exists, back it up before replacing it.

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── filings-reading.md
    └── food-delivery.md
```

`SKILL.md` is the skill entry point. `references/` is loaded only when needed and contains the filing-reading guide and the food delivery calibration example.

## North Star

This skill is not trying to sound smart. It is trying to get closer to a plain but difficult question:

```text
Why does this business exist, how does it scale, where does it make money, and what would turn it into a different business?
```
