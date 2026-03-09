![GitHub stars](https://img.shields.io/github/stars/phuryn/pm-skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/CONTRIBUTING.md)

# PM Skills Marketplace: より良いプロダクト判断のための AI オペレーティングシステム

> 82 の PM スキルと 46 のワークフローを 13 プラグインに収録。Claude Code、Cowork、その他の AI アシスタントに対応。ディスカバリーから戦略、実行、ローンチ、グロースまで — さらに 5 段階の Fit Journey（CPF → PSF → SPF → PMF → GTM）付き。

![プラグイン概要](.docs/images/plugins-overview.webp)

Claude Code および Cowork 向けに設計。スキルは他の AI アシスタントでも利用可能。

---

## これは何？（初めての方へ）

PM Skills Marketplace は、Claude（Anthropic の AI アシスタント）に **プロダクトマネジメントの専門知識** を追加するプラグイン集です。

普通に Claude に質問すると汎用的な回答が返ってきますが、このプラグインをインストールすると、Teresa Torres、Marty Cagan、Alberto Savoia といった PM の第一人者のフレームワークやベストプラクティスに基づいた **構造的なアウトプット** を返してくれるようになります。

### 主要な用語

| 用語 | 意味 | 具体例 |
|------|------|--------|
| **スキル（Skill）** | Claude に特定の PM 知識を教えるファイル。会話中に自動で読み込まれる | `opportunity-solution-tree` — Teresa Torres の OST フレームワーク |
| **コマンド（Command）** | `/` で始まるショートカット。複数のスキルを組み合わせたワークフロー | `/discover` — アイデア出し → 仮説整理 → 優先順位付け → 実験設計を一気に実行 |
| **プラグイン（Plugin）** | 関連するスキルとコマンドをまとめたパッケージ | `pm-product-discovery` — ディスカバリー関連の 13 スキル + 5 コマンド |
| **マーケットプレイス（Marketplace）** | プラグインの集合体。一括インストールで全プラグインが使える | `pm-skills` — 13 プラグインすべてを含む |

### 始める前に必要なもの

- **Claude Pro / Team / Enterprise** のいずれかのプラン（無料プランではプラグインを利用できません）
- **Claude Cowork** または **Claude Code** のいずれか

> **Claude Cowork とは？**
> Anthropic が提供するデスクトップアプリです。プラグインのインストールや `/command` の実行が GUI（画面操作）で行えます。プログラミング経験がない方にはこちらがおすすめです。
>
> **Claude Code とは？**
> ターミナル（コマンドライン）から Claude を操作する CLI ツールです。開発者向け。以下のコマンドでインストールできます：
> ```bash
> npm install -g @anthropic-ai/claude-code
> ```
> ※ Node.js 18 以上が必要です。

---

## まずはここから

プラグインをインストールしたら（[インストール方法はこちら](#インストール)）、すぐにコマンドを試してみましょう。

| やりたいこと | コマンド | 入力例 |
|------------|---------|-------|
| 新しいアイデアを検証したい | `/discover` | `/discover リモートチーム向けAI議事録ツール` |
| 戦略を整理したい | `/strategy` | `/strategy B2B代理店向けプロジェクト管理ツール` |
| PRD を書きたい | `/write-prd` | `/write-prd アラート疲れを軽減するスマート通知` |
| ローンチを計画したい | `/plan-launch` | `/plan-launch 中規模エンジニアチーム向けAIコードレビュー` |
| 指標を定義したい | `/north-star` | `/north-star フリーランスとクライアントの双方向マーケットプレイス` |
| プロダクトの適合性を段階的に検証したい | `/run-cpf` | `/run-cpf 中小企業向けAI経費管理ツール` |

> **ヒント**: コマンドを実行すると、最後に「次にやるべきこと」が提案されます。提案に従って次のコマンドを実行するだけで、PM ワークフロー全体を進められます。

このプロジェクトが役に立ったら、リポジトリに ⭐ をお願いします。

---

## なぜ PM Skills Marketplace？

汎用の AI はテキストを返すだけ。PM Skills Marketplace は **構造** を返します。

各スキルには実証済みの PM フレームワーク — ディスカバリー、仮説マッピング、優先順位付け、戦略立案 — が組み込まれており、ステップバイステップでガイドしてくれます。Teresa Torres、Marty Cagan、Alberto Savoia の知見が、本棚の上ではなく、日々のワークフローに組み込まれます。

結果：より速いドキュメントではなく、**より良いプロダクト判断**。

---

## 仕組み（スキル、コマンド、プラグイン）

### スキル（Skills）

マーケットプレイスの構成要素です。各スキルは Claude に特定の PM タスクのための専門知識、分析フレームワーク、またはガイド付きワークフローを提供します。一部のスキルは複数のコマンドが共有する再利用可能な基盤としても機能します。

スキルは会話の文脈に応じて **自動的に** 読み込まれます。明示的に呼び出す必要はありません。必要な場合（例：汎用知識よりスキルを優先させたい場合）は、`/plugin-name:skill-name` または `/skill-name` で強制読み込みできます。

### コマンド（Commands）

`/command-name` で呼び出すワークフローです。1 つ以上のスキルを連鎖させてエンドツーエンドのプロセスを実行します。例えば `/discover` は 4 つのスキルを連鎖します：アイデア出し → 仮説特定 → 優先順位付け → 実験設計。

### プラグイン（Plugins）

関連するスキルとコマンドをインストール可能なパッケージにまとめたものです。各プラグインは PM の特定領域 — ディスカバリー、戦略、実行など — をカバーします。マーケットプレイスをインストールすると、13 プラグインすべてが一度に利用可能になります。

![スキルの仕組み](.docs/images/how-skills-work.webp)

コマンドはスキルを使います。一部のスキルは複数のコマンドから参照されます。`prioritization-frameworks` や `opportunity-solution-tree` のように、コマンドなしでも Claude が必要に応じて自動参照するスタンドアロンのスキルもあります。

コマンドは PM ワークフローに沿って連鎖するよう設計されています。コマンド完了後に次のコマンドが提案されるので、プロンプトに従うだけです。

---

## インストール

### Claude Cowork（非エンジニア向け推奨）

> **Cowork がまだの方**: [claude.ai](https://claude.ai) からデスクトップアプリをダウンロード・インストールしてください。

**手順：**

1. Cowork を起動する
2. 左下の **Customize** をクリック
3. **Browse plugins** → **Personal** → **+** をクリック
4. **Add marketplace from GitHub** を選択
5. `NRKZOZW/pm-skills-optimiezed` と入力して Enter

これで 13 プラグインすべてが自動的にインストールされます。コマンド（`/discover`、`/strategy` など）とスキルの両方が使えるようになります。

![Claude Cowork での PM Skills インストール](.docs/images/pm-skills-install.gif)

> **インストールの確認方法**: チャット入力欄で `/` と入力してください。利用可能なコマンド一覧が表示されます。`/discover` や `/strategy` が表示されればインストール成功です。

### Claude Code（CLI / 開発者向け）

> **Claude Code がまだの方**: ターミナルで以下を実行してインストールしてください（Node.js 18 以上が必要です）：
> ```bash
> npm install -g @anthropic-ai/claude-code
> ```

**手順：**

```bash
# ステップ 1: マーケットプレイスを追加
claude plugin marketplace add NRKZOZW/pm-skills-optimiezed

# ステップ 2: コアプラグインをインストール
claude plugin install pm-product-discovery@pm-skills
claude plugin install pm-product-strategy@pm-skills
claude plugin install pm-execution@pm-skills
claude plugin install pm-market-research@pm-skills
claude plugin install pm-data-analytics@pm-skills
claude plugin install pm-marketing-growth@pm-skills
claude plugin install pm-go-to-market@pm-skills
claude plugin install pm-toolkit@pm-skills

# ステップ 3（任意）: Fit Journey プラグインをインストール
claude plugin install pm-journey-cpf@pm-skills
claude plugin install pm-journey-psf@pm-skills
claude plugin install pm-journey-spf@pm-skills
claude plugin install pm-journey-pmf@pm-skills
claude plugin install pm-journey-gtm@pm-skills
```

> **インストールの確認方法**: `claude` を起動し、`/discover テスト` と入力してみてください。ディスカバリーワークフローが始まれば成功です。

### 他の AI アシスタント（スキルのみ）

`skills/*/SKILL.md` ファイルはユニバーサルなスキルフォーマットに従っており、対応するツールであればどれでも使えます。コマンド（`/slash-commands`）は Claude 専用です。

| ツール | 使い方 | 対応範囲 |
|--------|--------|---------|
| **Gemini CLI** | スキルフォルダを `.gemini/skills/` にコピー | スキルのみ |
| **Cursor** | スキルフォルダを `.cursor/skills/` にコピー | スキルのみ |
| **Codex CLI** | スキルフォルダを `.codex/skills/` にコピー | スキルのみ |
| **Kiro** | スキルフォルダを `.kiro/skills/` にコピー | スキルのみ |

```bash
# 例: Gemini CLI 用に全スキルをコピー
for plugin in pm-*/; do
  cp -r "$plugin/skills/"* ~/.gemini/skills/ 2>/dev/null
done
```

---

## 使い方ガイド（インストール後）

### 基本：コマンドを使う

チャット入力欄に `/command-name` と入力するだけです。

```
/discover AI議事録ツール リモートチーム向け
```

Claude がステップバイステップで対話的にガイドし、必要に応じて質問してきます。

### 中級：スキルを直接使う

特定のフレームワークだけ使いたい場合は、スキル名を指定して呼び出すか、自然言語で質問するだけで OK です。

```
/pm-product-discovery:opportunity-solution-tree
```

または、普通に質問するだけでも：

```
ユーザーアクティベーション改善のための Opportunity Solution Tree を作って
```

Claude が自動的に関連するスキルを検出して適用します。

### 上級：コマンドを連鎖させる

コマンドは PM ワークフローに沿って連鎖するよう設計されています。実行後の提案に従うだけで、ディスカバリーからローンチまでシームレスに進められます。

```
/discover → /strategy → /write-prd → /plan-launch
```

各コマンドの終了時に次のステップが提案されるので、それに従うだけです。

### Fit Journey：エンドツーエンドのプロダクト検証

Fit Journey プラグインを使うと、プロダクトの適合性を 5 段階で検証できます。各ステージで GO / PIVOT / KILL の判定が出ます。

```
/run-cpf 中小企業向けAI経費管理ツール
  ↓ GO 判定が出たら
/run-psf 中小企業向けAI経費管理ツール
  ↓ GO 判定が出たら
/run-spf → /run-pmf → /run-gtm
```

---

## プラグイン一覧

### コア PM プラグイン（8 プラグイン）

<details>
<summary><strong>1. pm-product-discovery</strong> — アイデア出し、実験設計、仮説検証、OST、インタビュー（13 スキル、5 コマンド）</summary>

**スキル（13）：**

- `brainstorm-ideas-existing` — 既存プロダクト向けの多視点アイデア出し（PM、デザイナー、エンジニア）
- `brainstorm-ideas-new` — 新規プロダクトの初期ディスカバリー向けアイデア出し
- `brainstorm-experiments-existing` — 既存プロダクトの仮説を検証する実験の設計
- `brainstorm-experiments-new` — 新規プロダクト向けリーンスタートアップのプレトタイプ設計（Alberto Savoia）
- `identify-assumptions-existing` — 価値・ユーザビリティ・実現可能性・事業性のリスキーな仮説を特定
- `identify-assumptions-new` — GTM・戦略・チームを含む 8 つのリスクカテゴリーで仮説を特定
- `prioritize-assumptions` — インパクト × リスクのマトリクスで仮説を優先順位付け
- `prioritize-features` — インパクト・工数・リスク・戦略適合性に基づく機能の優先順位付け
- `analyze-feature-requests` — 顧客の機能リクエストをテーマと戦略適合性で分析・分類
- `opportunity-solution-tree` — Opportunity Solution Tree（Teresa Torres）を構築 — 成果 → 機会 → ソリューション → 実験
- `interview-script` — JTBD の深掘り質問付き構造化インタビュースクリプトの作成
- `summarize-interview` — インタビュー書き起こしを JTBD・満足度シグナル・アクションアイテムに要約
- `metrics-dashboard` — North Star・インプット指標・アラート閾値を含むプロダクト指標ダッシュボードの設計

**コマンド（5）：**

- `/discover` — フルディスカバリーサイクル：アイデア出し → 仮説マッピング → 優先順位付け → 実験設計
- `/brainstorm` — 多視点アイデア出し（`ideas|experiments` × `existing|new`）
- `/triage-requests` — 機能リクエストの分析と優先順位付け
- `/interview` — インタビュースクリプトの準備またはトランスクリプトの要約（`prep|summarize`）
- `/setup-metrics` — プロダクト指標ダッシュボードの設計

**使用例：**

スキル：
- `AIライティングアシスタントのアイデアで最もリスキーな仮説は何？`
- `ユーザーアクティベーション改善のための Opportunity Solution Tree を作って`
- `エンタープライズ顧客からの12件の機能リクエストを優先順位付けして [CSV添付]`

コマンド：
- `/discover リモートチーム向けAI議事録ツール`
- `/brainstorm experiments existing — オンボーディングフローの離脱を減らしたい`
- `/interview prep — エンタープライズバイヤーの調達ワークフローについてインタビュー予定`

</details>

<details>
<summary><strong>2. pm-product-strategy</strong> — ビジョン、ビジネスモデル、価格戦略、競合分析（12 スキル、5 コマンド）</summary>

プロダクト戦略、ビジョン、ビジネスモデル、価格戦略、マクロ環境分析。ビジョン策定から競合環境スキャンまでの戦略ツールキット。

**スキル（12）：**

- `product-strategy` — 包括的な 9 セクションのプロダクト戦略キャンバス（ビジョン → 防御力）
- `startup-canvas` — プロダクト戦略（9 セクション）+ ビジネスモデルを統合したスタートアップキャンバス — BMC やリーンキャンバスの代替
- `product-vision` — インスピレーションを与え、達成可能でエモーショナルなプロダクトビジョンの策定
- `value-proposition` — 6 パートの JTBD バリュープロポジション（Who, Why, What before, How, What after, Alternatives）
- `lean-canvas` — スタートアップ・新規プロダクト向けリーンキャンバス
- `business-model` — 9 つの構成要素を含むビジネスモデルキャンバス
- `monetization-strategy` — 3〜5 つのマネタイズ戦略のブレスト + 検証実験
- `pricing-strategy` — 価格モデル、競合分析、WTP、価格弾力性
- `swot-analysis` — アクション可能な提案付き SWOT 分析
- `pestle-analysis` — マクロ環境分析：政治、経済、社会、技術、法律、環境
- `porters-five-forces` — 競争力分析（競合、供給者、買い手、代替品、新規参入）
- `ansoff-matrix` — 市場と製品をまたぐ成長戦略マッピング

**コマンド（5）：**

- `/strategy` — 9 セクションのプロダクト戦略キャンバスを作成
- `/business-model` — ビジネスモデルの探索（`lean|full|startup|value-prop|all`）
- `/value-proposition` — 6 パート JTBD テンプレートでバリュープロポジションを設計
- `/market-scan` — SWOT + PESTLE + Porter's + Ansoff を統合したマクロ環境分析
- `/pricing` — 競合分析と実験付きの価格戦略を設計

**使用例：**

スキル：
- `マーケットプレイス型スタートアップに最適なのはリーンキャンバス？BMC？スタートアップキャンバス？`
- `非ネイティブ英語話者向けAIライティングツールのバリュープロポジションを設計して`
- `プロジェクト管理 SaaS 市場の Porter's Five Forces 分析をやって`

コマンド：
- `/strategy B2B代理店向けプロジェクト管理ツール`
- `/business-model startup — 非ネイティブ英語話者向けAIライティングツール`
- `/value-proposition エンタープライズ向けSaaSオンボーディングツール`

</details>

<details>
<summary><strong>3. pm-execution</strong> — PRD、OKR、ロードマップ、スプリント、振り返り、リリースノート、ステークホルダー管理（15 スキル、10 コマンド）</summary>

日常のプロダクトマネジメント：PRD、OKR、ロードマップ、スプリント、振り返り、リリースノート、プレモーテム、ステークホルダー管理、ユーザーストーリー、優先順位付けフレームワーク。

**スキル（15）：**

- `create-prd` — 8 セクションの包括的な PRD テンプレート
- `brainstorm-okrs` — 全社目標に整合したチームレベル OKR
- `outcome-roadmap` — 機能リストをアウトカムフォーカスのロードマップに変換
- `sprint-plan` — キャパシティ推定、ストーリー選択、リスク特定付きスプリント計画
- `retro` — 構造化されたスプリント振り返りファシリテーション
- `release-notes` — チケット・PRD・変更履歴からユーザー向けリリースノートを作成
- `pre-mortem` — Tigers/Paper Tigers/Elephants 分類によるリスク分析
- `stakeholder-map` — Power × Interest グリッドとコミュニケーション計画
- `summarize-meeting` — ミーティングのトランスクリプト → 決定事項 + アクションアイテム
- `user-stories` — 3 C's と INVEST 基準に従ったユーザーストーリー
- `job-stories` — ジョブストーリー：[状況] のとき、[動機] したい、[成果] のために
- `wwas` — Why-What-Acceptance 形式のプロダクトバックログアイテム
- `test-scenarios` — ハッピーパス、エッジケース、エラー処理のテストシナリオ
- `dummy-dataset` — CSV、JSON、SQL、Python 形式のリアルなダミーデータセット
- `prioritization-frameworks` — 9 つの優先順位付けフレームワークのリファレンスガイド（Opportunity Score、ICE、RICE、MoSCoW、Kano など）

**コマンド（10）：**

- `/write-prd` — 機能アイデアや課題から PRD を作成
- `/plan-okrs` — チームレベル OKR のブレスト
- `/transform-roadmap` — 機能ベースのロードマップをアウトカムフォーカスに変換
- `/sprint` — スプリントライフサイクル（`plan|retro|release`）
- `/pre-mortem` — PRD またはローンチ計画のプレモーテムリスク分析
- `/meeting-notes` — ミーティングのトランスクリプトを構造化ノートに要約
- `/stakeholder-map` — ステークホルダーのマッピングとコミュニケーション計画の作成
- `/write-stories` — 機能をバックログアイテムに分解（`user|job|wwa`）
- `/test-scenarios` — ユーザーストーリーからテストシナリオを生成
- `/generate-data` — リアルなダミーデータセットを作成

**使用例：**

スキル：
- `50 件のバックログにはどの優先順位付けフレームワークが最適？`
- `プラットフォーム移行プロジェクトのステークホルダーをマッピングして`
- `Opportunity Score、ICE、RICE の違いは？`

コマンド：
- `/write-prd アラート疲れを軽減するスマート通知システム`
- `/sprint retro — 前回のスプリントのノートはこちら`
- `/write-stories job — 「チームダッシュボード」機能をジョブストーリーに分解して`

</details>

<details>
<summary><strong>4. pm-market-research</strong> — ペルソナ、セグメンテーション、ジャーニーマップ、市場規模、競合分析（7 スキル、3 コマンド）</summary>

ユーザーリサーチと競合分析：ペルソナ、セグメンテーション、ジャーニーマップ、市場規模推定、競合分析、フィードバック分析。

**スキル（7）：**

- `user-personas` — リサーチデータから精緻なユーザーペルソナを作成
- `market-segments` — デモグラフィック、JTBD、プロダクト適合性で 3〜5 つの顧客セグメントを特定
- `user-segmentation` — フィードバックデータから行動・JTBD・ニーズに基づくユーザーセグメンテーション
- `customer-journey-map` — ステージ、タッチポイント、感情、ペインポイントを含むエンドツーエンドのジャーニーマップ
- `market-sizing` — トップダウンとボトムアップの両アプローチによる TAM、SAM、SOM
- `competitor-analysis` — 競合の強み・弱みと差別化の機会
- `sentiment-analysis` — ユーザーフィードバックからのセンチメント分析とテーマ抽出

**コマンド（3）：**

- `/research-users` — ペルソナ構築、ユーザーセグメンテーション、カスタマージャーニーマッピング
- `/competitive-analysis` — 競合環境の分析
- `/analyze-feedback` — ユーザーフィードバックからのセンチメント分析とセグメントインサイト

**使用例：**

スキル：
- `米国市場における AI コードレビューツールの TAM/SAM/SOM を推定して`
- `EC サイトのチェックアウトフローのカスタマージャーニーマップを作って`
- `このアンケート回答者を行動とニーズでセグメンテーションして [CSV添付]`

コマンド：
- `/research-users フィットネスアプリの 12 人のユーザーインタビューデータがあります`
- `/competitive-analysis デザインツール市場における Figma の競合`
- `/analyze-feedback Q4 の NPS 回答 200 件がこちら [ファイル添付]`

</details>

<details>
<summary><strong>5. pm-data-analytics</strong> — SQL 生成、コホート分析、A/B テスト分析（3 スキル、3 コマンド）</summary>

PM のためのデータ分析：SQL クエリ生成、コホート分析、A/B テスト分析。

**スキル（3）：**

- `sql-queries` — 自然言語から SQL を生成（BigQuery、PostgreSQL、MySQL）
- `cohort-analysis` — コホート別のリテンション曲線、機能採用率、エンゲージメントトレンド
- `ab-test-analysis` — 統計的有意性、サンプルサイズ検証、出荷/延長/停止の推奨

**コマンド（3）：**

- `/write-query` — 自然言語から SQL クエリを生成
- `/analyze-cohorts` — ユーザーエンゲージメントデータのコホート分析
- `/analyze-test` — A/B テスト結果の分析

**使用例：**

スキル：
- `2% の MDE で 95% の信頼度を得るにはどれくらいのサンプルが必要？`
- `サブスクリプションアプリで追跡すべきリテンション指標は？`

コマンド：
- `/write-query Q4 2025 の国別月間アクティブユーザーを表示（BigQuery）`
- `/analyze-test チェックアウトフローの A/B テスト結果がこちら [CSV添付]`
- `/analyze-cohorts 1 月 vs 2 月にサインアップしたユーザーの週次リテンション`

</details>

<details>
<summary><strong>6. pm-go-to-market</strong> — ビーチヘッドセグメント、ICP、メッセージング、グロースループ、GTM モーション、バトルカード（6 スキル、3 コマンド）</summary>

Go-to-Market 戦略：ビーチヘッドセグメント、理想的な顧客プロファイル、メッセージング、グロースループ、GTM モーション、競合バトルカード。

**スキル（6）：**

- `gtm-strategy` — チャネル、メッセージング、成功指標、ローンチ計画を含むフル GTM 戦略
- `beachhead-segment` — 最初のビーチヘッド市場セグメントの特定
- `ideal-customer-profile` — デモグラフィック、行動、JTBD、ニーズを含む ICP
- `growth-loops` — 持続可能なグロースループ（フライホイール）の設計
- `gtm-motions` — GTM モーションとツールの評価（プロダクトレッド、セールスレッドなど）
- `competitive-battlecard` — 異議対応とウィン戦略付きの営業用バトルカード

**コマンド（3）：**

- `/plan-launch` — ビーチヘッドからローンチ計画までのフル GTM 戦略
- `/growth-strategy` — グロースループの設計と GTM モーションの評価
- `/battlecard` — 競合バトルカードの作成

**使用例：**

スキル：
- `開発者生産性ツールに最適なビーチヘッドセグメントは？`
- `フリーミアムティアのある B2B SaaS のグロースループを設計して`
- `AI 人事スクリーニングプラットフォームの ICP を定義して`

コマンド：
- `/plan-launch 中規模エンジニアチーム向けAIコードレビューツール`
- `/battlecard 当社CRM vs Salesforce（SMB市場）`
- `/growth-strategy フリーランスとスタートアップをつなぐ双方向マーケットプレイス`

</details>

<details>
<summary><strong>7. pm-marketing-growth</strong> — マーケティングアイデア、ポジショニング、バリュープロップ、ネーミング、North Star メトリクス（5 スキル、2 コマンド）</summary>

プロダクトマーケティングとグロース：マーケティングアイデア、ポジショニング、バリュープロポジションステートメント、プロダクトネーミング、North Star メトリクス。

**スキル（5）：**

- `marketing-ideas` — チャネルとメッセージング付きのクリエイティブでコスパの良いマーケティングアイデア
- `positioning-ideas` — 競合と差別化されたプロダクトポジショニング
- `value-prop-statements` — マーケティング・営業・オンボーディング向けバリュープロポジションステートメント
- `product-name` — ブランド価値とターゲットに合ったプロダクト名のブレスト
- `north-star-metric` — ビジネスゲーム分類付きの North Star Metric + インプット指標

**コマンド（2）：**

- `/market-product` — マーケティングアイデア、ポジショニング、バリュープロップ、プロダクト名のブレスト
- `/north-star` — North Star Metric と関連インプット指標の定義

**使用例：**

スキル：
- `Notion と差別化する 5 つのポジショニング案をブレストして`
- `双方向マーケットプレイスに良い North Star Metric は？`
- `営業チームのピッチデッキ用バリュープロップステートメントを作って`

コマンド：
- `/market-product EC マネージャー向け B2B 分析ダッシュボード`
- `/north-star フリーランスとクライアントをつなぐ双方向マーケットプレイス`

</details>

<details>
<summary><strong>8. pm-toolkit</strong> — レジュメレビュー、法務文書、校正（4 スキル、5 コマンド）</summary>

コア PM 業務以外の PM ユーティリティ：レジュメレビュー、法務文書、校正。

**スキル（4）：**

- `review-resume` — 10 のベストプラクティスに基づく PM レジュメレビューとカスタマイズ（XYZ+S 公式、キーワード、構成）
- `draft-nda` — 法域に適した条項付き秘密保持契約書（NDA）
- `privacy-policy` — GDPR/CCPA 準拠のプライバシーポリシー
- `grammar-check` — 文法、論理、フローのチェックと修正

**コマンド（5）：**

- `/review-resume` — 包括的な PM レジュメレビュー
- `/tailor-resume` — 特定の求人票に合わせたレジュメのカスタマイズ
- `/draft-nda` — NDA の起草
- `/privacy-policy` — プライバシーポリシーの起草
- `/proofread` — 文法、論理、フローのチェック

**使用例：**

スキル：
- `PM レジュメをベストプラクティスに照らしてレビューして [PDF添付]`
- `このプロダクトアナウンスの文法とわかりやすさをチェックして`

コマンド：
- `/review-resume [PM レジュメを添付]`
- `/tailor-resume [レジュメ + 求人票を添付]`
- `/proofread Q1 投資家アップデートのドラフトがこちら`

</details>

### Fit Journey プラグイン（5 プラグイン）

プロダクトの成長段階に沿って、適合性を段階的に検証するプラグイン群です。各ステージで GO / PIVOT / KILL の判定を行い、次のステージに進むべきかを判断します。

```
CPF（Customer Problem Fit）— 顧客が本当に解決すべき課題を持っているか検証
 → PSF（Problem Solution Fit）— ソリューションが課題を解決するか検証
   → SPF（Solution Product Fit）— MVP が価値を提供するか検証
     → PMF（Product Market Fit）— プロダクトマーケットフィットを測定・達成
       → GTM（Go To Market）— スケールと市場展開
```

<details>
<summary><strong>9. pm-journey-cpf</strong> — Customer Problem Fit：顧客が本当に解決すべき課題を持っているか検証（4 スキル、2 コマンド）</summary>

市場調査、顧客ディスカバリー、ペルソナ作成、課題バリデーションをガイドします。

**スキル（4）：**

- `customer-discovery-plan` — 顧客インタビュー実施のための構造化アプローチ
- `empathy-map` — 顧客の視点と動機を理解するフレームワーク
- `problem-statement` — 構造化テンプレートを使ったテスト可能な課題仮説の作成
- `problem-validation` — 顧客リサーチを通じた課題ステートメントの検証

**コマンド（2）：**

- `/run-cpf` — フル Customer Problem Fit 検証サイクル（課題仮説 → 顧客ディスカバリー → GO/PIVOT/KILL 判定）
- `/validate-problem` — 特定の課題ステートメントの品質基準に対する検証

**使用例：**

- `/run-cpf 中小企業向けAI経費管理ツール`
- `/validate-problem "SMBオーナーは手動のレシート分類に週5時間以上費やしている"`

</details>

<details>
<summary><strong>10. pm-journey-psf</strong> — Problem Solution Fit：ソリューションの定義と検証（3 スキル、2 コマンド）</summary>

バリュープロポジション設計、アイデア出し、プロトタイピング、ソリューション受容性テストをガイドします。

**スキル（3）：**

- `value-proposition-canvas` — 顧客のジョブ、ペイン、ゲインをバリュープロポジションにマッピング（Strategyzer）
- `prototype-test-plan` — プロトタイプテスト計画の設計と実行
- `solution-validation` — テストを通じたソリューションコンセプトの検証フレームワーク

**コマンド（2）：**

- `/run-psf` — フル Problem Solution Fit 検証サイクル（ソリューション発想 → プロトタイピング → 検証）
- `/design-experiment` — ソリューションの仮説を検証する実験の設計

**使用例：**

- `/run-psf レシート写真によるAI経費分類`
- `/design-experiment ユーザーは手動確認なしでAI分類された経費を信頼するか？`

</details>

<details>
<summary><strong>11. pm-journey-spf</strong> — Solution Product Fit：MVP の構築と検証（3 スキル、2 コマンド）</summary>

MVP スコーピング、要件定義、KPI 設定、スプリント計画、ユーザーフィードバック分析をガイドします。

**スキル（3）：**

- `mvp-scoping` — ユーザーストーリーマッピング、最もリスキーな仮説テスト、MoSCoW 優先順位付けで MVP スコープを定義
- `kpi-framework` — MVP 成功のための KPI の定義と追跡
- `feedback-loop` — 開発中にユーザーインサイトを収集するフィードバックメカニズムの確立

**コマンド（2）：**

- `/run-spf` — フル Solution Product Fit 検証サイクル（MVP スコーピング → ユーザーフィードバック → 価値検証）
- `/scope-mvp` — 明確な成功基準付きの MVP スコーピング

**使用例：**

- `/run-spf AI経費管理アプリ — レシート写真撮影 + 自動分類`
- `/scope-mvp プロジェクト管理ツールのリアルタイムコラボ機能`

</details>

<details>
<summary><strong>12. pm-journey-pmf</strong> — Product Market Fit：PMF の測定と達成（4 スキル、2 コマンド）</summary>

PMF 測定、グロースハック、コアバリューの深化、価格最適化をガイドします。

**スキル（4）：**

- `pmf-measurement` — 包括的な PMF スコアカード（Sean Ellis テスト、リテンション曲線、NPS、エンゲージメント深度、収益シグナル）
- `pmf-survey` — PMF サーベイの設計と実施
- `growth-hacking` — グロースループの特定とスケールのためのフレームワーク
- `core-value-deepening` — コアプロダクトバリューの採用深化

**コマンド（2）：**

- `/run-pmf` — フル Product Market Fit 検証サイクル（PMF 測定 → 価格最適化）
- `/measure-pmf` — プロダクトが PMF を達成しているかの評価

**使用例：**

- `/run-pmf 経費アプリは3ヶ月で500アクティブユーザー`
- `/measure-pmf Sean Ellis で40%が「非常にがっかり」だがリテンションは横ばい`

</details>

<details>
<summary><strong>13. pm-journey-gtm</strong> — Go To Market：プロダクトのスケール（3 スキル、2 コマンド）</summary>

GTM 戦略、クロスファンクショナルアラインメント、ユニットエコノミクス最適化、スケーリングロードマップをガイドします。

**スキル（3）：**

- `unit-economics` — CAC、LTV、LTV:CAC 比率、回収期間、貢献利益、チャネル ROI の詳細分析
- `cross-functional-alignment` — 営業、マーケティング、オペレーション、プロダクトの GTM 実行アラインメント
- `scaling-roadmap` — スケールド・グロースのためのロードマップ構築

**コマンド（2）：**

- `/run-gtm` — フル Go To Market 検証サイクル（GTM 戦略 → スケーリング実行）
- `/check-unit-economics` — ユニットエコノミクスの分析と収益性ギャップの診断

**使用例：**

- `/run-gtm 経費アプリを SMB からミッドマーケットに展開`
- `/check-unit-economics CAC=$120, LTV=$450, payback=4mo, churn=6%`

</details>

---

## よくある質問（FAQ）

<details>
<summary><strong>Q: 無料プランでも使えますか？</strong></summary>

いいえ。プラグイン機能は Claude Pro / Team / Enterprise プランでのみ利用できます。

</details>

<details>
<summary><strong>Q: コマンドが認識されません</strong></summary>

1. プラグインが正しくインストールされているか確認してください
2. Cowork の場合：チャット入力欄で `/` を入力し、コマンド一覧が表示されるか確認
3. Claude Code の場合：`claude plugin list` でインストール済みプラグインを確認
4. それでも動かない場合：Cowork / Claude Code を再起動してみてください

</details>

<details>
<summary><strong>Q: スキルとコマンドの違いは？</strong></summary>

- **スキル**：Claude が自動的に参照する知識ベース。会話の文脈に応じて読み込まれます。明示的に呼び出すこともできます
- **コマンド**：`/` で始めるワークフロー。複数のスキルを組み合わせて段階的にガイドしてくれます

迷ったら `/command-name` でコマンドを使うのが簡単です。

</details>

<details>
<summary><strong>Q: 英語以外でも使えますか？</strong></summary>

はい。コマンドの入力やプロダクトの説明は日本語など任意の言語で入力できます。Claude は入力言語に合わせて回答します。

</details>

<details>
<summary><strong>Q: Fit Journey プラグインと Core プラグインの違いは？</strong></summary>

- **Core プラグイン**（8個）：個別の PM タスクに特化（PRD を書く、OKR を作る、競合分析する、など）
- **Fit Journey プラグイン**（5個）：プロダクトの成長段階に沿った検証フレームワーク（CPF → PSF → SPF → PMF → GTM）

Core はタスク単位、Fit Journey はフェーズ単位で使い分けてください。

</details>

<details>
<summary><strong>Q: 特定のプラグインだけインストールできますか？</strong></summary>

はい。Claude Code では `claude plugin install プラグイン名@pm-skills` で個別にインストールできます。Cowork ではマーケットプレイス単位でのインストールとなり、13 プラグインすべてが入ります。

</details>

<details>
<summary><strong>Q: 社内の機密情報を入力しても大丈夫？</strong></summary>

Claude のデータ取り扱いポリシーに従います。Claude Pro の場合、入力データはモデルのトレーニングには使われません。詳細は [Anthropic のプライバシーポリシー](https://www.anthropic.com/privacy) を確認してください。Team / Enterprise プランではより厳密なデータ保護が適用されます。

</details>

---

## About

このマーケットプレイスはプロダクトマネジメントの実践と AI の進化に合わせて継続的に更新されます。

以下の著者の知見に基づいてスキルが設計されています：

- Teresa Torres — [*Continuous Discovery Habits*](https://www.amazon.com/Continuous-Discovery-Habits-Discover-Products/dp/1736633309/)
- Marty Cagan — [*INSPIRED*](https://www.amazon.com/INSPIRED-Create-Tech-Products-Customers/dp/1119387507/) / [*TRANSFORMED*](https://www.amazon.com/dp/1119697336/)
- Alberto Savoia — [*The Right It*](https://www.amazon.com/Right-Many-Ideas-Yours-Succeed/dp/0062884654)
- Dan Olsen — [*The Lean Product Playbook*](https://www.amazon.com/dp/1118960874/)
- Roger L. Martin — [*Playing to Win*](https://www.amazon.com/Playing-Win-Expanded-Bonus-Articles/dp/B0F25SDYWV/)
- Ash Maurya — [*Running Lean*](https://www.amazon.com/dp/B004J4XGN6/)
- Strategyzer — [*Business Model Generation*](https://www.amazon.com/dp/0470876417/) / [*Value Proposition Design*](https://www.amazon.com/dp/1118968050/)
- Christina Wodtke — [*Radical Focus*](https://www.amazon.com/Radical-Focus-Achieving-Important-Objectives/dp/0996006052)
- Anthony W. Ulwick — [*Jobs to Be Done*](https://jobs-to-be-done-book.com/)
- Alistair Croll & Benjamin Yoskovitz — [*Lean Analytics*](https://www.amazon.com/Lean-Analytics-Better-Startup-Faster/dp/1449335675/)
- Sean Ellis — [*Hacking Growth*](https://www.amazon.com/Hacking-Growth-Fastest-Growing-Companies-Breakout/dp/045149721X/)
- Maja Voje — [*Go-To-Market Strategist*](https://gtmstrategist.com/)

Paweł Huryn（[The Product Compass Newsletter](https://www.productcompass.pm)）によるキュレーション。

## コントリビューション

[CONTRIBUTING.md](CONTRIBUTING.md) を参照してください。

## Windows の既知の問題

Cowork が不安定で VM を起動できない場合（[claude-code/issues/27010](https://github.com/anthropics/claude-code/issues/27010)）、以下を試してください：

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

90% のケースで問題が解決します。
残りの 10%：services.msc を開き、「Claude」サービスを手動で開始してください。

## ライセンス

MIT — [LICENSE](LICENSE) を参照。
