![GitHub stars](https://img.shields.io/github/stars/phuryn/pm-skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/CONTRIBUTING.md)

# PM Skills Marketplace: The AI Operating System for Better Product Decisions

> 82 PM skills and 46 chained workflows across 13 plugins. Claude Code, Cowork, and more. From discovery to strategy, execution, launch, and growth — plus a 5-stage Fit Journey (CPF → PSF → SPF → PMF → GTM).

![Plugin overview](.docs/images/plugins-overview.webp)

Designed for Claude Code and Cowork. Skills compatible with other AI assistants.

---

## What Is This? (For First-Time Users)

PM Skills Marketplace は、Claude（Anthropic の AI アシスタント）に **プロダクトマネジメントの専門知識** を追加するプラグイン集です。インストールすると、Claude がPM のフレームワークやベストプラクティスに基づいた構造的なアウトプットを返してくれるようになります。

### Key Concepts

| Term | What It Means | Example |
|------|--------------|---------|
| **Skill** | Claude に特定の PM 知識を教えるファイル。会話中に自動で読み込まれる | `opportunity-solution-tree` — Teresa Torres の OST フレームワーク |
| **Command** | `/` で始まるショートカット。複数のスキルを組み合わせたワークフロー | `/discover` — アイデア出し → 仮説整理 → 優先順位付け → 実験設計を一気に実行 |
| **Plugin** | 関連するスキルとコマンドをまとめたパッケージ | `pm-product-discovery` — ディスカバリー関連の 13 スキル + 5 コマンド |
| **Marketplace** | プラグインの集合体。一括インストールで全プラグインが使える | `pm-skills` — 13 プラグインすべてを含む |

### What You Need Before Starting

- **Claude Pro / Team / Enterprise** のいずれかのプラン（無料プランではプラグインを利用できません）
- **Claude Cowork**（デスクトップアプリ、非エンジニア向け推奨）または **Claude Code**（CLI ツール、開発者向け）

> **Claude Cowork って何？**
> Anthropic が提供するデスクトップアプリで、プラグインのインストールや `/command` の実行がGUIで行えます。
> **Claude Code って何？**
> ターミナルから Claude を操作する CLI ツールです。`npm install -g @anthropic-ai/claude-code` でインストールできます。

---

## Start Here

プラグインをインストールしたら、すぐにコマンドを試してみましょう。

| やりたいこと | コマンド | 入力例 |
|------------|---------|-------|
| 新しいアイデアを検証したい | `/discover` | `/discover リモートチーム向けAI議事録ツール` |
| 戦略を整理したい | `/strategy` | `/strategy B2B代理店向けプロジェクト管理ツール` |
| PRD を書きたい | `/write-prd` | `/write-prd アラート疲れを軽減するスマート通知` |
| ローンチを計画したい | `/plan-launch` | `/plan-launch 中規模エンジニアチーム向けAIコードレビュー` |
| 指標を定義したい | `/north-star` | `/north-star フリーランスとクライアントの双方向マーケットプレイス` |
| プロダクトの適合性を段階的に検証したい | `/run-cpf` | `/run-cpf 中小企業向けAI経費管理ツール` |

> **Tip**: コマンドを実行すると、最後に「次にやるべきこと」が提案されます。提案に従って次のコマンドを実行するだけで、PM ワークフロー全体を進められます。

If this project helps you, ⭐ the repo.

---

## Why PM Skills Marketplace?

Generic AI gives you text. PM Skills Marketplace gives you structure.

Each skill encodes a proven PM framework — discovery, assumption mapping, prioritization, strategy — and walks you through it step by step. You get the rigor of Teresa Torres, Marty Cagan, and Alberto Savoia built into your daily workflow, not sitting on a bookshelf.

The result: better product decisions, not just faster documents.

---

## How It Works (Skills, Commands, Plugins)

**Skills** are the building blocks of the marketplace. Each skill gives Claude domain knowledge, analytical frameworks, or a guided workflow for a specific PM task. Some skills also work as reusable foundations that multiple commands share.

Skills are loaded automatically when relevant to the conversation — no explicit invocation needed. If needed (e.g., prioritizing skills over general knowledge), you can **force loading skills** with `/plugin-name:skill-name` or `/skill-name` (Claude will add the prefix).

**Commands** are user-triggered workflows invoked with `/command-name`. They chain one or more skills into an end-to-end process. For example, `/discover` chains four skills together: brainstorm-ideas → identify-assumptions → prioritize-assumptions → brainstorm-experiments.

**Plugins** group related skills and commands into installable packages. Each plugin covers a PM domain — discovery, strategy, execution, and so on. Installing the marketplace gives you all 13 plugins at once.

![How skills work](.docs/images/how-skills-work.webp)

Commands use skills. Some skills serve multiple commands. Some skills (like `prioritization-frameworks` or `opportunity-solution-tree`) are standalone references that Claude draws on whenever relevant — no command needed.

Commands are designed to flow into each other, matching the PM workflow. After any command completes, it suggests relevant next commands — just follow the prompts.

---

## Installation

### Claude Cowork (recommended for non-developers)

> **Cowork がまだの方**: [claude.ai](https://claude.ai) からデスクトップアプリをダウンロード・インストールしてください。

1. Cowork を起動し、左下の **Customize** をクリック
2. **Browse plugins** → **Personal** → **+** をクリック
3. **Add marketplace from GitHub** を選択
4. `phuryn/pm-skills` と入力して Enter

All 13 plugins install automatically. You get both commands (`/discover`, `/strategy`, etc.) and skills.

![Installing PM Skills in Claude Cowork](.docs/images/pm-skills-install.gif)

> **インストール後の確認方法**: チャット入力欄で `/` と入力すると、利用可能なコマンド一覧が表示されます。`/discover` や `/strategy` が表示されればインストール成功です。

### Claude Code (CLI)

> **Claude Code がまだの方**: ターミナルで `npm install -g @anthropic-ai/claude-code` を実行してインストールしてください（Node.js 18+ が必要です）。

```bash
# Step 1: Add the marketplace
claude plugin marketplace add phuryn/pm-skills

# Step 2: Install individual plugins (core PM plugins)
claude plugin install pm-product-discovery@pm-skills
claude plugin install pm-product-strategy@pm-skills
claude plugin install pm-execution@pm-skills
claude plugin install pm-market-research@pm-skills
claude plugin install pm-data-analytics@pm-skills
claude plugin install pm-marketing-growth@pm-skills
claude plugin install pm-go-to-market@pm-skills
claude plugin install pm-toolkit@pm-skills

# Step 3 (optional): Install Fit Journey plugins
claude plugin install pm-journey-cpf@pm-skills
claude plugin install pm-journey-psf@pm-skills
claude plugin install pm-journey-spf@pm-skills
claude plugin install pm-journey-pmf@pm-skills
claude plugin install pm-journey-gtm@pm-skills
```

> **インストール後の確認方法**: `claude` を起動し、`/discover テスト` と入力してみてください。ディスカバリーワークフローが始まれば成功です。

### Other AI assistants (skills only)

The `skills/*/SKILL.md` files follow the universal skill format and work with any tool that reads it. Commands (`/slash-commands`) are Claude-specific.

| Tool | How to use | What works |
|------|-----------|------------|
| **Gemini CLI** | Copy skill folders to `.gemini/skills/` | Skills only |
| **Cursor** | Copy skill folders to `.cursor/skills/` | Skills only |
| **Codex CLI** | Copy skill folders to `.codex/skills/` | Skills only |
| **Kiro** | Copy skill folders to `.kiro/skills/` | Skills only |

```bash
# Example: copy all skills for Gemini CLI
for plugin in pm-*/; do
  cp -r "$plugin/skills/"* ~/.gemini/skills/ 2>/dev/null
done
```

---

## Usage Guide (How to Use After Installation)

### Basic: Use Commands

コマンドは `/command-name` の形式でチャットに入力するだけで使えます。

```
/discover AI-powered meeting summarizer for remote teams
```

Claude will walk you through each step interactively, asking clarifying questions as needed.

### Intermediate: Use Skills Directly

特定のフレームワークだけ使いたい場合は、スキル名を指定して呼び出すか、自然言語で質問するだけでOKです。

```
/pm-product-discovery:opportunity-solution-tree
```

Or simply ask:

```
Help me build an Opportunity Solution Tree for improving user activation
```

Claude automatically detects the relevant skill and applies it.

### Advanced: Chain Commands

コマンドは PM ワークフローに沿って連鎖するよう設計されています。実行後の提案に従うだけで、ディスカバリーから戦略、実行、ローンチまでシームレスに進められます。

```
/discover → /strategy → /write-prd → /plan-launch
```

### Fit Journey: End-to-End Product Validation

Fit Journey プラグインを使うと、プロダクトの適合性を CPF → PSF → SPF → PMF → GTM の 5 段階で検証できます。

```
/run-cpf 中小企業向けAI経費管理ツール
  ↓ GO判定が出たら
/run-psf 中小企業向けAI経費管理ツール
  ↓ GO判定が出たら
/run-spf → /run-pmf → /run-gtm
```

---

## Available Plugins

### Core PM Plugins (8 plugins)

<details>
<summary><strong>1. pm-product-discovery</strong> — Ideation, experiments, assumption testing, OSTs, interviews (13 skills, 5 commands)</summary>

**Skills (13):**

- `brainstorm-ideas-existing` — Multi-perspective ideation for existing products (PM, Designer, Engineer)
- `brainstorm-ideas-new` — Ideation for new products in initial discovery
- `brainstorm-experiments-existing` — Design experiments to test assumptions for existing products
- `brainstorm-experiments-new` — Design lean startup pretotypes for new products (Alberto Savoia)
- `identify-assumptions-existing` — Identify risky assumptions across Value, Usability, Viability, and Feasibility
- `identify-assumptions-new` — Identify risky assumptions across 8 risk categories including Go-to-Market, Strategy, and Team
- `prioritize-assumptions` — Prioritize assumptions using an Impact × Risk matrix with experiment suggestions
- `prioritize-features` — Prioritize a feature backlog based on impact, effort, risk, and strategic alignment
- `analyze-feature-requests` — Analyze and categorize customer feature requests by theme and strategic fit
- `opportunity-solution-tree` — Build an Opportunity Solution Tree (Teresa Torres) — outcome → opportunities → solutions → experiments
- `interview-script` — Create a structured customer interview script with JTBD probing questions
- `summarize-interview` — Summarize an interview transcript into JTBD, satisfaction signals, and action items
- `metrics-dashboard` — Design a product metrics dashboard with North Star, input metrics, and alert thresholds

**Commands (5):**

- `/discover` — Full discovery cycle: ideation → assumption mapping → prioritization → experiment design
- `/brainstorm` — Multi-perspective ideation (`ideas|experiments` × `existing|new`)
- `/triage-requests` — Analyze and prioritize a batch of feature requests
- `/interview` — Prepare an interview script or summarize a transcript (`prep|summarize`)
- `/setup-metrics` — Design a product metrics dashboard

**Examples:**

Skills:
- `What are the riskiest assumptions for our AI writing assistant idea?`
- `Help me build an Opportunity Solution Tree for improving user activation`
- `Prioritize these 12 feature requests from our enterprise customers [attach CSV]`

Commands:
- `/discover AI-powered meeting summarizer for remote teams`
- `/brainstorm experiments existing — We need to reduce churn in our onboarding flow`
- `/interview prep — We're interviewing enterprise buyers about their procurement workflow`

</details>

<details>
<summary><strong>2. pm-product-strategy</strong> — Vision, business models, pricing, competitive landscape (12 skills, 5 commands)</summary>

Product strategy, vision, business models, pricing, and macro environment analysis. Covers the full strategic toolkit from vision crafting through competitive landscape scanning.

**Skills (12):**

- `product-strategy` — Comprehensive 9-section Product Strategy Canvas (vision → defensibility)
- `startup-canvas` — Startup Canvas combining Product Strategy (9 sections) + Business Model — an alternative to BMC and Lean Canvas for new products
- `product-vision` — Craft an inspiring, achievable, and emotional product vision
- `value-proposition` — 6-part JTBD value proposition (Who, Why, What before, How, What after, Alternatives)
- `lean-canvas` — Lean Canvas business model for startups and new products
- `business-model` — Business Model Canvas with all 9 building blocks
- `monetization-strategy` — Brainstorm 3–5 monetization strategies with validation experiments
- `pricing-strategy` — Pricing models, competitive analysis, willingness-to-pay, and price elasticity
- `swot-analysis` — SWOT analysis with actionable recommendations
- `pestle-analysis` — Macro environment: Political, Economic, Social, Technological, Legal, Environmental
- `porters-five-forces` — Competitive forces analysis (rivalry, suppliers, buyers, substitutes, new entrants)
- `ansoff-matrix` — Growth strategy mapping across markets and products

**Commands (5):**

- `/strategy` — Create a complete 9-section Product Strategy Canvas
- `/business-model` — Explore business models (`lean|full|startup|value-prop|all`)
- `/value-proposition` — Design a value proposition using the 6-part JTBD template
- `/market-scan` — Macro environment analysis combining SWOT + PESTLE + Porter's + Ansoff
- `/pricing` — Design a pricing strategy with competitive analysis and experiments

**Examples:**

Skills:
- `Compare Lean Canvas vs Business Model Canvas vs Startup Canvas for my marketplace startup`
- `Design a value proposition for our AI writing assistant targeting non-native English speakers`
- `Run a Porter's Five Forces analysis for the project management SaaS market`

Commands:
- `/strategy B2B project management tool for agencies`
- `/business-model startup — AI writing tool for non-native English speakers`
- `/value-proposition SaaS onboarding tool for enterprise customers`

</details>

<details>
<summary><strong>3. pm-execution</strong> — PRDs, OKRs, roadmaps, sprints, retros, release notes, stakeholder management (15 skills, 10 commands)</summary>

Day-to-day product management: PRDs, OKRs, roadmaps, sprints, retrospectives, release notes, pre-mortems, stakeholder management, user stories, and prioritization frameworks.

**Skills (15):**

- `create-prd` — Comprehensive 8-section PRD template
- `brainstorm-okrs` — Team-level OKRs aligned with company objectives
- `outcome-roadmap` — Transform a feature list into an outcome-focused roadmap
- `sprint-plan` — Sprint planning with capacity estimation, story selection, and risk identification
- `retro` — Structured sprint retrospective facilitation
- `release-notes` — User-facing release notes from tickets, PRDs, or changelogs
- `pre-mortem` — Risk analysis with Tigers/Paper Tigers/Elephants classification
- `stakeholder-map` — Power × Interest grid with tailored communication plan
- `summarize-meeting` — Meeting transcript → decisions + action items
- `user-stories` — User stories following the 3 C's and INVEST criteria
- `job-stories` — Job stories: When [situation], I want to [motivation], so I can [outcome]
- `wwas` — Product backlog items in Why-What-Acceptance format
- `test-scenarios` — Test scenarios: happy paths, edge cases, error handling
- `dummy-dataset` — Realistic dummy datasets as CSV, JSON, SQL, or Python
- `prioritization-frameworks` — Reference guide to 9 prioritization frameworks (Opportunity Score, ICE, RICE, MoSCoW, Kano, etc.)

**Commands (10):**

- `/write-prd` — Create a PRD from a feature idea or problem statement
- `/plan-okrs` — Brainstorm team-level OKRs
- `/transform-roadmap` — Convert a feature-based roadmap into outcome-focused
- `/sprint` — Sprint lifecycle (`plan|retro|release`)
- `/pre-mortem` — Pre-mortem risk analysis on a PRD or launch plan
- `/meeting-notes` — Summarize a meeting transcript into structured notes
- `/stakeholder-map` — Map stakeholders and create a communication plan
- `/write-stories` — Break features into backlog items (`user|job|wwa`)
- `/test-scenarios` — Generate test scenarios from user stories
- `/generate-data` — Create realistic dummy datasets

**Examples:**

Skills:
- `Which prioritization framework should I use for a 50-item backlog?`
- `Map our stakeholders for the platform migration project`
- `What's the difference between Opportunity Score, ICE, and RICE?`

Commands:
- `/write-prd Smart notification system that reduces alert fatigue`
- `/sprint retro — Here are the notes from our last sprint`
- `/write-stories job — Break down the "team dashboard" feature into job stories`

</details>

<details>
<summary><strong>4. pm-market-research</strong> — Personas, segmentation, journey maps, market sizing, competitor analysis (7 skills, 3 commands)</summary>

User research and competitive analysis: personas, segmentation, journey maps, market sizing, competitor analysis, and feedback analysis.

**Skills (7):**

- `user-personas` — Create refined user personas from research data
- `market-segments` — Identify 3–5 customer segments with demographics, JTBD, and product fit
- `user-segmentation` — Segment users from feedback data based on behavior, JTBD, and needs
- `customer-journey-map` — End-to-end journey map with stages, touchpoints, emotions, and pain points
- `market-sizing` — TAM, SAM, SOM with top-down and bottom-up approaches
- `competitor-analysis` — Competitor strengths, weaknesses, and differentiation opportunities
- `sentiment-analysis` — Sentiment analysis and theme extraction from user feedback

**Commands (3):**

- `/research-users` — Build personas, segment users, and map the customer journey
- `/competitive-analysis` — Analyze the competitive landscape
- `/analyze-feedback` — Sentiment analysis and segment insights from user feedback

**Examples:**

Skills:
- `Estimate TAM/SAM/SOM for an AI code review tool in the US market`
- `Create a customer journey map for our e-commerce checkout flow`
- `Segment these survey respondents by behavior and needs [attach CSV]`

Commands:
- `/research-users We have interview data from 12 users of our fitness app`
- `/competitive-analysis Figma competitors in the design tool space`
- `/analyze-feedback Here's 200 NPS responses from Q4 [attach file]`

</details>

<details>
<summary><strong>5. pm-data-analytics</strong> — SQL generation, cohort analysis, A/B test analysis (3 skills, 3 commands)</summary>

Data analytics for PMs: SQL query generation, cohort analysis, and A/B test analysis.

**Skills (3):**

- `sql-queries` — Generate SQL from natural language (BigQuery, PostgreSQL, MySQL)
- `cohort-analysis` — Retention curves, feature adoption, and engagement trends by cohort
- `ab-test-analysis` — Statistical significance, sample size validation, and ship/extend/stop recommendations

**Commands (3):**

- `/write-query` — Generate SQL queries from natural language
- `/analyze-cohorts` — Cohort analysis on user engagement data
- `/analyze-test` — Analyze A/B test results

**Examples:**

Skills:
- `How large a sample do I need for 95% confidence with a 2% MDE?`
- `What retention metrics should I track for a subscription app?`

Commands:
- `/write-query Show me monthly active users by country for Q4 2025 (BigQuery)`
- `/analyze-test Here are the results from our checkout flow A/B test [attach CSV]`
- `/analyze-cohorts Weekly retention for users who signed up in January vs February`

</details>

<details>
<summary><strong>6. pm-go-to-market</strong> — Beachhead segments, ICPs, messaging, growth loops, GTM motions, battlecards (6 skills, 3 commands)</summary>

Go-to-market strategy: beachhead segments, ideal customer profiles, messaging, growth loops, GTM motions, and competitive battlecards.

**Skills (6):**

- `gtm-strategy` — Full GTM strategy: channels, messaging, success metrics, and launch plan
- `beachhead-segment` — Identify the first beachhead market segment
- `ideal-customer-profile` — ICP with demographics, behaviors, JTBD, and needs
- `growth-loops` — Design sustainable growth loops (flywheels)
- `gtm-motions` — Evaluate GTM motions and tools (product-led, sales-led, etc.)
- `competitive-battlecard` — Sales-ready battlecard with objection handling and win strategies

**Commands (3):**

- `/plan-launch` — Full GTM strategy from beachhead to launch plan
- `/growth-strategy` — Design growth loops and evaluate GTM motions
- `/battlecard` — Create a competitive battlecard

**Examples:**

Skills:
- `What's the best beachhead segment for a developer productivity tool?`
- `Design a growth loop for a B2B SaaS with a freemium tier`
- `Define our ICP for an AI-powered HR screening platform`

Commands:
- `/plan-launch AI code review tool targeting mid-size engineering teams`
- `/battlecard Our CRM vs Salesforce for the SMB market`
- `/growth-strategy Two-sided marketplace for connecting freelancers with startups`

</details>

<details>
<summary><strong>7. pm-marketing-growth</strong> — Marketing ideas, positioning, value props, naming, North Star metrics (5 skills, 2 commands)</summary>

Product marketing and growth: marketing ideas, positioning, value proposition statements, product naming, and North Star metrics.

**Skills (5):**

- `marketing-ideas` — Creative, cost-effective marketing ideas with channels and messaging
- `positioning-ideas` — Product positioning differentiated from competitors
- `value-prop-statements` — Value proposition statements for marketing, sales, and onboarding
- `product-name` — Product name brainstorming aligned to brand values and audience
- `north-star-metric` — North Star Metric + input metrics with business game classification

**Commands (2):**

- `/market-product` — Brainstorm marketing ideas, positioning, value props, and product names
- `/north-star` — Define your North Star Metric and supporting input metrics

**Examples:**

Skills:
- `Brainstorm 5 positioning angles that differentiate us from Notion`
- `What's a good North Star Metric for a two-sided marketplace?`
- `Generate value prop statements for our sales team's pitch deck`

Commands:
- `/market-product B2B analytics dashboard for e-commerce managers`
- `/north-star Two-sided marketplace connecting freelancers with clients`

</details>

<details>
<summary><strong>8. pm-toolkit</strong> — Resume review, legal documents, proofreading (4 skills, 5 commands)</summary>

PM utilities beyond core product work: resume review, legal documents, and proofreading.

**Skills (4):**

- `review-resume` — PM resume review and tailoring against 10 best practices (XYZ+S formula, keywords, structure)
- `draft-nda` — Non-Disclosure Agreement with jurisdiction-appropriate clauses
- `privacy-policy` — Privacy policy covering GDPR/CCPA compliance
- `grammar-check` — Grammar, logic, and flow checking with targeted fixes

**Commands (5):**

- `/review-resume` — Comprehensive PM resume review
- `/tailor-resume` — Tailor a resume to a specific job description
- `/draft-nda` — Draft an NDA
- `/privacy-policy` — Draft a privacy policy
- `/proofread` — Check grammar, logic, and flow

**Examples:**

Skills:
- `Review my PM resume against best practices [attach PDF]`
- `Check this product announcement for grammar and clarity`

Commands:
- `/review-resume [attach your PM resume]`
- `/tailor-resume [attach resume + paste job description]`
- `/proofread Here's the draft of our Q1 investor update`

</details>

### Fit Journey Plugins (5 plugins)

プロダクトの成長段階に沿って、適合性を段階的に検証するプラグイン群です。各ステージで GO / PIVOT / KILL の判定を行い、次のステージに進むべきかを判断します。

```
CPF (Customer Problem Fit)
 → PSF (Problem Solution Fit)
   → SPF (Solution Product Fit)
     → PMF (Product Market Fit)
       → GTM (Go To Market)
```

<details>
<summary><strong>9. pm-journey-cpf</strong> — Customer Problem Fit: validate that customers truly have a problem worth solving (4 skills, 2 commands)</summary>

Guides PMs through market research, customer discovery, persona creation, and problem validation.

**Skills (4):**

- `customer-discovery-plan` — Structured approach to conducting customer interviews
- `empathy-map` — Framework to understand customer perspectives and motivations
- `problem-statement` — Create testable problem hypotheses using structured templates
- `problem-validation` — Validate problem statements through customer research

**Commands (2):**

- `/run-cpf` — Run a full Customer Problem Fit validation cycle (problem hypothesis → customer discovery → GO/PIVOT/KILL decision)
- `/validate-problem` — Validate a specific problem statement against quality criteria

**Examples:**

- `/run-cpf AI-powered expense management tool for small businesses`
- `/validate-problem "SMB owners spend 5+ hours/week on manual receipt categorization"`

</details>

<details>
<summary><strong>10. pm-journey-psf</strong> — Problem Solution Fit: define and validate solutions (3 skills, 2 commands)</summary>

Guides PMs through value proposition design, ideation, prototyping, and solution acceptance testing.

**Skills (3):**

- `value-proposition-canvas` — Map customer jobs, pains, and gains to your value proposition (Strategyzer)
- `prototype-test-plan` — Design and execute prototype testing plans
- `solution-validation` — Framework for validating solution concepts through testing

**Commands (2):**

- `/run-psf` — Run a full Problem Solution Fit validation cycle (solution ideation → prototyping → validation)
- `/design-experiment` — Design an experiment to test solution assumptions

**Examples:**

- `/run-psf AI expense categorization using receipt photos`
- `/design-experiment Will users trust AI-categorized expenses without manual review?`

</details>

<details>
<summary><strong>11. pm-journey-spf</strong> — Solution Product Fit: build and validate your MVP (3 skills, 2 commands)</summary>

Guides PMs through MVP scoping, requirements definition, KPI setting, sprint planning, and user feedback analysis.

**Skills (3):**

- `mvp-scoping` — Define MVP scope using user story mapping, riskiest assumption testing, and MoSCoW prioritization
- `kpi-framework` — Define and track KPIs for MVP success
- `feedback-loop` — Establish feedback mechanisms to collect user insights during development

**Commands (2):**

- `/run-spf` — Run a full Solution Product Fit validation cycle (MVP scoping → user feedback → value validation)
- `/scope-mvp` — Scope an MVP with clear success criteria

**Examples:**

- `/run-spf AI expense management app — photo receipt capture + auto-categorization`
- `/scope-mvp Real-time collaboration feature for our project management tool`

</details>

<details>
<summary><strong>12. pm-journey-pmf</strong> — Product Market Fit: measure and achieve PMF (4 skills, 2 commands)</summary>

Guides PMs through PMF measurement, growth hacking, core value deepening, and pricing optimization.

**Skills (4):**

- `pmf-measurement` — Comprehensive PMF scorecard (Sean Ellis Test, retention curves, NPS, engagement depth, revenue signals)
- `pmf-survey` — Design and conduct PMF surveys
- `growth-hacking` — Framework for identifying and scaling growth loops
- `core-value-deepening` — Deepen adoption of core product value

**Commands (2):**

- `/run-pmf` — Run a full Product Market Fit validation cycle (PMF measurement → pricing optimization)
- `/measure-pmf` — Assess whether a product has achieved product-market fit

**Examples:**

- `/run-pmf Our expense app has 500 active users after 3 months`
- `/measure-pmf We have 40% "very disappointed" on Sean Ellis, but flat retention`

</details>

<details>
<summary><strong>13. pm-journey-gtm</strong> — Go To Market: scale your product (3 skills, 2 commands)</summary>

Guides PMs through GTM strategy, cross-functional alignment, unit economics optimization, and scaling roadmap.

**Skills (3):**

- `unit-economics` — Deep analysis of CAC, LTV, LTV:CAC ratio, payback period, contribution margin, and channel ROI
- `cross-functional-alignment` — Align sales, marketing, ops, and product on GTM execution
- `scaling-roadmap` — Build a roadmap for scaled growth

**Commands (2):**

- `/run-gtm` — Run a full Go To Market validation cycle (GTM strategy → scaling execution)
- `/check-unit-economics` — Analyze unit economics and diagnose profitability gaps

**Examples:**

- `/run-gtm Expanding our expense app from SMB to mid-market`
- `/check-unit-economics CAC=$120, LTV=$450, payback=4mo, churn=6%`

</details>

---

## FAQ

<details>
<summary><strong>Q: 無料プランでも使えますか?</strong></summary>

いいえ。プラグイン機能は Claude Pro / Team / Enterprise プランでのみ利用できます。

</details>

<details>
<summary><strong>Q: コマンドが認識されません</strong></summary>

1. プラグインが正しくインストールされているか確認してください
2. Cowork の場合: チャット入力欄で `/` を入力し、コマンド一覧が表示されるか確認
3. Claude Code の場合: `claude plugin list` でインストール済みプラグインを確認
4. それでも動かない場合: Cowork / Claude Code を再起動してみてください

</details>

<details>
<summary><strong>Q: スキルとコマンドの違いは?</strong></summary>

- **スキル**: Claude が自動的に参照する知識ベース。会話の文脈に応じて読み込まれます。明示的に呼び出すこともできます
- **コマンド**: `/` で始めるワークフロー。複数のスキルを組み合わせて段階的にガイドしてくれます

迷ったら `/command-name` でコマンドを使うのが簡単です。

</details>

<details>
<summary><strong>Q: 英語以外でも使えますか?</strong></summary>

はい。コマンドの入力やプロダクトの説明は日本語など任意の言語で入力できます。Claude は入力言語に合わせて回答します。

</details>

<details>
<summary><strong>Q: Fit Journey プラグインと Core プラグインの違いは?</strong></summary>

- **Core プラグイン** (8個): 個別の PM タスクに特化（PRD を書く、OKR を作る、競合分析する、など）
- **Fit Journey プラグイン** (5個): プロダクトの成長段階に沿った検証フレームワーク（CPF → PSF → SPF → PMF → GTM）

Core はタスク単位、Fit Journey はフェーズ単位で使い分けてください。

</details>

---

## About

This marketplace evolves with product practice and AI capabilities.

Selected skills based on the work of:

- Teresa Torres — [*Continuous Discovery Habits*](https://www.amazon.com/Continuous-Discovery-Habits-Discover-Products/dp/1736633309/)
- Marty Cagan — [*INSPIRED*](https://www.amazon.com/INSPIRED-Create-Tech-Products-Customers/dp/1119387507/) and [*TRANSFORMED*](https://www.amazon.com/dp/1119697336/)
- Alberto Savoia — [*The Right It*](https://www.amazon.com/Right-Many-Ideas-Yours-Succeed/dp/0062884654)
- Dan Olsen — [*The Lean Product Playbook*](https://www.amazon.com/dp/1118960874/)
- Roger L. Martin — [*Playing to Win*](https://www.amazon.com/Playing-Win-Expanded-Bonus-Articles/dp/B0F25SDYWV/)
- Ash Maurya — [*Running Lean*](https://www.amazon.com/dp/B004J4XGN6/)
- Strategyzer — [*Business Model Generation*](https://www.amazon.com/dp/0470876417/) and [*Value Proposition Design*](https://www.amazon.com/dp/1118968050/)
- Christina Wodtke — [*Radical Focus*](https://www.amazon.com/Radical-Focus-Achieving-Important-Objectives/dp/0996006052)
- Anthony W. Ulwick — [*Jobs to Be Done*](https://jobs-to-be-done-book.com/)
- Alistair Croll & Benjamin Yoskovitz — [*Lean Analytics*](https://www.amazon.com/Lean-Analytics-Better-Startup-Faster/dp/1449335675/)
- Sean Ellis — [*Hacking Growth*](https://www.amazon.com/Hacking-Growth-Fastest-Growing-Companies-Breakout/dp/045149721X/)
- Maja Voje — [*Go-To-Market Strategist*](https://gtmstrategist.com/)

Curated by Paweł Huryn from [The Product Compass Newsletter](https://www.productcompass.pm).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Known Issue on Windows

If your Cowork is unstable and can't start a VM ([claude-code/issues/27010](https://github.com/anthropics/claude-code/issues/27010)), try:

```powershell
$action = New-ScheduledTaskAction -Execute "powershell.exe" -Argument "-WindowStyle Hidden -Command `"if ((Get-Service CoworkVMService).Status -ne 'Running') { Start-Service CoworkVMService }`""

$trigger = New-ScheduledTaskTrigger -RepetitionInterval (New-TimeSpan -Minutes 1) -Once -At (Get-Date)

$settings = New-ScheduledTaskSettingsSet -AllowStartIfOnBatteries -DontStopIfGoingOnBatteries

Register-ScheduledTask -TaskName "CoworkVMServiceMonitor" `
  -Action $action `
  -Trigger $trigger `
  -Settings $settings `
  -RunLevel Highest `
  -User "SYSTEM"
```

It solves 90% of the issues on Windows.
The remaining 10%: open services.msc > start "Claude" service manually

## License

MIT — see [LICENSE](LICENSE).
