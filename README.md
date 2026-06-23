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

---

# Industry Cognition Skill 中文版

一个给策略运营和行业研究使用的 Codex skill。

它的目标不是让 AI 更会写行业报告，而是让 AI 更会形成行业判断。

这里的审美很简单：少一点热点综述，多一点商业常识；少一点框架套话，多一点龙头参照；少一点“趋势来了”，多一点“哪个变量真的变了”。

## 研究审美

这个 skill 偏好的研究气质：

- **先问它是什么生意**：行业研究的第一步不是找新闻，而是定义行业。外卖是餐饮、电商、履约网络、广告平台，还是本地生活基础设施？不同定义会导向完全不同的指标。
- **龙头叙事优先**：行业定义不能只靠外部观察。先看代表性公司如何在招股书、年报、投资者材料和分部口径里描述自己。
- **公开市场材料是硬骨头**：招股书是公司讲清商业模式的时刻，年报是现实给这个叙事的反馈。二者之间的变化，往往比评论文章更有信息量。
- **数字必须进入公式**：关键数字不是为了堆表格。它必须能进入极简模型，改变对市场、成本、利润池或竞争格局的判断。
- **趋势只作为认知更新**：创业者、投资人、融资、产品 demo 都有价值，但它们只能回答一个问题：它是否改变了行业的核心变量？
- **小而硬，不求大而全**：好的输出应该像研究协议或判断骨架，不像百科式行业报告。

## 它拒绝什么

这个 skill 会尽量避免：

- 把行业研究写成新闻摘要。
- 把每个行业都解释成流量、补贴、私域或增长黑客。
- 用“赋能、生态、闭环、重构”这类词替代判断。
- 把融资新闻直接当成趋势。
- 逐章总结招股书，却没有形成商业判断。
- 列很多公司和数据，但没有回答“这到底是什么生意”。

## 研究协议

默认研究顺序：

```text
定义行业 -> 找龙头参照 -> 读招股书/财报 -> 建极简模型 -> 用创业/投资信号更新认知
```

更具体地说：

1. **定义行业**：列出 3-5 个候选定义，并说明每个定义下最重要的指标。
2. **找龙头参照**：选择上市龙头和相邻公司，用它们建立现实参照。
3. **读招股书/财报**：只抓四件事，宏观市场、用户需求、竞争环境、极简模型。
4. **建极简模型**：选择一家锚点公司，把真实数字代入公式。
5. **更新认知**：用创业者、投资人、融资和产品 demo 验证变量是否变化。

## 提问示例

适合这样问：

```text
用 $industry-cognition 研究餐饮供应链
```

```text
用 $industry-cognition 跑一次外卖研究协议
```

```text
用 $industry-cognition 看一个 AI 产品 demo 是否改变了某个行业变量
```

这个 skill 尤其适合这类问题：

- 外卖到底是一门什么生意？
- 餐饮供应链应该被理解成批发分销、餐饮工业化，还是连锁餐饮基础设施？
- AI agent 对某个 SaaS 行业到底改变了人力成本、交付方式，还是只是包装层？
- 招股书和年报里哪些数字能支撑市场判断和业务模型？

## 默认输出

默认输出不是完整行业报告，而是紧凑的判断骨架：

- **主问题**：这个行业到底是什么生意？
- **候选定义**：每个定义对应哪些关键指标？
- **龙头叙事**：上市公司如何描述自己和行业？
- **招股书/财报四件事**：宏观市场、用户需求、竞争环境、极简模型。
- **极简模型代入**：选一家锚点公司，把真实数字放进公式。
- **验证问题**：用更多龙头和相邻公司验证判断。
- **趋势更新**：创业、融资、投资人、产品 demo 只作为模型变量更新。
- **当前判断**：已知什么，推断什么，什么会改变结论。

## 安装

把这个仓库放到本地 Codex skills 目录：

```bash
git clone git@github.com:shawting7/industry-cognition-skill.git ~/.codex/skills/industry-cognition
```

如果已经存在同名 skill，可以先备份旧目录再替换。

## 仓库结构

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── filings-reading.md
    └── food-delivery.md
```

`SKILL.md` 是 skill 的主入口。`references/` 只在需要时加载，用来保存招股书/年报读法和外卖标准样例。

## 北极星问题

这个 skill 追求的不是“显得很懂”，而是逼近一个朴素但难的问题：

```text
这门生意为什么存在，靠什么扩张，在哪里赚钱，什么变化会让它变成另一门生意？
```
