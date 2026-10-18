# Google Cloud Certified - Professional Agentic Architect 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Agentic Architect
- **試験コード**: PAA（Professional Agentic Architect）
- **公式試験ガイド**: [Professional Agentic Architect 認定試験ガイド (英語版)](https://services.google.com/fh/files/misc/professional_agentic_architect_exam_guide_english.pdf?hl=ja)
- **公式試験ページ**: [Professional Agentic Architect | Google Cloud Certification](https://cloud.google.com/learn/certification/agentic-architect?hl=ja)
- **最終更新日**: 2026-10-18

---

## 1. 試験の概要と基本スペック

Professional Agentic Architect は、Google Cloud 上で自律的かつ AI 駆動型のエージェントワークフローを設計、実装、評価、運用管理できる高度なアーキテクト能力を認定するプロフェッショナル資格です。

本認定試験では、従来の大規模言語モデル（LLM）を用いた単純なテキスト生成や単発プロンプティングの枠を超え、自律的な推論・ツール実行・ステート管理・マルチエージェント協調（A2A: Agent2Agent）を組み合わせた「エージェント型システム（Agentic Systems）」の総合的なアーキテクチャ設計力が問われます。信頼性（Reliability）、性能（Performance）、コスト効率（Cost）、セキュリティとガバナンス（Security & Governance）、およびスケーラビリティ（Scalability）を両立させ、ビジネス要件に応じた最適なエージェント実装アプローチを選択できる実践的な意思決定基準が検証されます。

- **試験時間**: 180 分（3 時間）
- **出題問題数**: 約 80 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $120（標準価格 $200 から 40% 割引、税別）
- **試験配信形式**: オンライン監視（遠隔受験）またはテストセンター監視（オンサイト受験）
- **認定有効期間**: 1 年間
- **提供言語**: 英語（English）
- **前提条件**: なし
- **推奨される実務経験**: クラウドソリューションの構築、テスト、デプロイ、管理に関する 3 年以上の実務経験（Google Cloud 上でのエージェント型ソリューション構築に関する 1 年以上の実務経験を含む）

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 5 つの出題分野（Section）で構成されています。中核となる「カスタムエージェントの開発（33%）」と「評価とデプロイ（22%）」の 2 セクションで全体の過半数（55%）を占め、これに「コーディングエージェントの活用（17%）」「セキュリティとガバナンス（15%）」「ローコードツールによるエージェント構築（13%）」が連動する、極めて高度かつ実務直結型の試験設計となっています。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・プロトコル |
| :--- | :--- | :--- | :--- |
| **Section 1** | ローコードツールによるエージェントの構築 (Building agents using low-code tools) | 約 13.0% | Gemini Enterprise Agent Designer、Customer Experience Agent Studio (CX Agent Studio)、Agent Search、ステートマシンワークフロー（Pages、Routes、Handlers）、プロンプトテンプレート（Few-shot、CoT）、マルチモーダルデータ統合 |
| **Section 2** | アプリケーション開発におけるコーディングエージェントの活用 (Using coding agents for application development) | 約 17.0% | Model Context Protocol (MCP) サーバー、Antigravity (CLI、SDK、IDE)、Claude Code on Google Cloud、セキュアサンドボックス（GKE、Cloud Workstations、Antigravity）、コードリファクタリング、脆弱性パッチ適用、Agents CLI、カスタムスキル、プラグイン、フック、サブエージェント |
| **Section 3** | カスタムエージェントの開発 (Developing custom agents) | 約 33.0% | Agent Development Kit (ADK)、Gemini LLMs、SLM vs LLM 選定、Agent Platform Memory Bank、マネージドセッション、Vector Search 1.0、Agent Retrieval、RAG パイプライン、Agent Identity、Agent Registry、Google Cloud MCP Servers、Agentic プロトコル（MCP、Agent2Agent [A2A]）、マルチエージェントオーケストレーション（並列、順次、グラフ構造） |
| **Section 4** | エージェントワークフローの評価とデプロイ (Evaluating and deploying agentic workflows) | 約 22.0% | ADK evalset、ゴールデンデータセット、Agent Platform Gen AI evaluation service、カスタムオートルーター (Autoraters)、ツール実行継続評価、デプロイランタイム選定（Agent Runtime [旧 Agent Engine]、Cloud Run、GKE）、ドリフト・推論ループトラブルシューティング、Cloud Logging、Cloud Trace、レイテンシ最適化 |
| **Section 5** | エージェントワークフローのセキュリティとガバナンス (Securing and governing agentic workflows) | 約 15.0% | OAuth 2.0 Auth Manager、Agent Identity、Principal Access Boundary (PAB) ポリシー、Agent Gateway（トラフィック監視・追跡）、Model Armor（プロンプトインジェクション防御、脱獄対策）、Agent Registry ポリシー適用、Human-in-the-Loop (HITL)、Sensitive Data Protection、アイデンティティ伝播 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: ローコードツールによるエージェントの構築 (~13%)
- **出題の狙い**: プログラミングコードを極力記述せず、Gemini Enterprise Agent Designer や CX Agent Studio などのローコード GUI ツールを活用して、決定論的な状態遷移フローとプロンプト駆動の自律推論を融合したエンタープライズエージェントを迅速に構築する能力を検証します。
- **主要タスク**:
  - Task 1.1: ローコードツールを用いたエージェントワークフローと振る舞いの構成（Gemini Enterprise Agent Designer および CX Agent Studio を用いたページ、遷移ルート、イベントハンドラーに基づくステートベースワークフローの構成、エージェントの振る舞いを制御するシステムインストラクションおよびコンソール内プロンプトテンプレート [Few-shot、Chain-of-Thought / CoT] の作成）
  - Task 1.2: エンタープライズデータと Gemini Enterprise の接続（社内独自データソースへのセキュアな接続と問い合わせ構成 [Agent Search]、構造化・非構造化マルチモーダルデータ [動画、音声、画像、ドキュメント] のエージェントワークフローへの取り込みと処理）
- **重要キーワード**: Gemini Enterprise Agent Designer, Customer Experience Agent Studio (CX Agent Studio), Pages, Transition Routes, Event Handlers, System Instructions, Few-shot Prompting, Chain-of-Thought (CoT), Agent Search, Multimodal Ingestion

#### Section 2: アプリケーション開発におけるコーディングエージェントの活用 (~17%)
- **出題の狙い**: Antigravity や Claude Code などのコーディングエージェントを開発ライフサイクルへ安全に組み込み、MCP サーバーや拡張機能（Skills、Plugins、Hooks、Rules）を用いて組織固有の開発プロセスに適合・自動化させる能力を検証します。
- **主要タスク**:
  - Task 2.1: コーディングエージェントの効果的な運用（Model Context Protocol [MCP] サーバー、カスタムスキル、外部ツールアクセスの構成、セキュアサンドボックス環境 [GKE、Cloud Workstations、Antigravity サンドボックス] でのエージェント実行、ソースコードのリファクタリング、実行時ランタイムの性能最適化、アプリケーション層の脆弱性パッチ適用）
  - Task 2.2: エンタープライズワークフローに合わせたコーディングエージェントのカスタマイズ（Antigravity を用いたスキル [Skills]、プラグイン [Plugins]、拡張フック [Extension Hooks]、ルール [Rules]、サブエージェント [Subagents] の作成、デプロイ済みエージェントの構築・スケール・ガバナンス・最適化を行う Agents CLI の連携拡張）
- **重要キーワード**: Model Context Protocol (MCP), Antigravity (CLI / SDK / App), Claude Code on Google Cloud, Secure Sandboxes (GKE, Cloud Workstations), Code Refactoring, Vulnerability Patching, Skills, Plugins, Extension Hooks, Rules, Subagents, Agents CLI

#### Section 3: カスタムエージェントの開発 (~33%)
- **出題の狙い**: Agent Development Kit (ADK) などのオープンソースライブラリを用いてコードベースで高機能なカスタムエージェントを実装し、ドメインナレッジの統合、セッション・メモリ管理、および A2A（Agent2Agent）や MCP プロトコルによる複数エージェント協調を設計するアーキテクト能力を検証します。
- **主要タスク**:
  - Task 3.1: コードによるエージェントワークフローの設計と構築（コスト、セキュリティ、エージェント構造を考慮した適切な言語モデルの選定と構成 [LLM vs SLM、セルフホスト vs SaaS、OSS vs 商用プロプライエタリ]、ADK を用いたカスタムエージェントの実装、セッションとメモリの構成 [Agent Platform Memory Bank、マネージドセッション]、Agents CLI を用いたスキル構成 [プラグイン、エージェントモード vs 人間モード]）
  - Task 3.2: エンタープライズドメイン知識の統合（Vector Search 1.0 および Agent Retrieval を用いた RAG パイプライン・ベクトル検索システムの設計・構成・管理 [埋め込みモデル、類似度スコアリング、リランカー]、Agent Identity によるエージェント実行権限の制御、Agent Registry や Google Cloud MCP サーバーを用いた機能統合 [マネージド DB 連携層、外部 SaaS・リモートサーバー接続]）
  - Task 3.3: エージェントワークフローのオーケストレーションと協調（MCP および Agent2Agent [A2A] プロトコルによるエージェント連携、マルチエージェントのハンドオフとワークフロー制御 [並列実行、順次実行、グラフ構造ワークフロー]、Agent Runtime、Agent Identity、Agent Registry、Agent Policies の統合管理）
- **重要キーワード**: Agent Development Kit (ADK), LLM vs SLM Selection, Agent Platform Memory Bank, Managed Sessions, Vector Search 1.0, Agent Retrieval, RAG Pipeline, Reranker, Agent Identity, Agent Registry, Google Cloud MCP Servers, Agentic Protocols (MCP, A2A), Multi-Agent Orchestration (Parallel, Sequential, Graph Workflows), Agent Runtime

#### Section 4: エージェントワークフローの評価とデプロイ (~22%)
- **出題の狙い**: エージェントの推論精度、検索品質、ツール呼び出しの成功率を定量・定性的に継続評価する仕組みを構築し、最適な実行基盤へのデプロイと運用時のボトルネック・異常検知を遂行する能力を検証します。
- **主要タスク**:
  - Task 4.1: 開発時および本番環境におけるエージェントの評価（エージェント評価用のテストデータセット作成 [ゴールデンデータ、プロンプト、エッジケース]、設定した成功基準に基づくツール実行精度の継続的評価パイプライン構築、評価フレームワークとツールの選定 [ADK evalset、Agent Platform Gen AI evaluation service、カスタムオートルーター / Autoraters]、ゴールデンデータセットを用いたエージェント応答品質および検索精度のベンチマーク評価）
  - Task 4.2: 本番ワークロードのデプロイとスケーリング（ユースケース、要件、コストに基づく最適なデプロイランタイムの選定 [Agent Runtime (旧 Agent Engine)、Cloud Run、GKE]、エージェント特有の障害トラブルシューティング [モデルやデータのドリフト、ツール呼び出し遅延、推論ループ / 思考ループ、システム障害]、パフォーマンス・信頼性・コストの継続監視と最適化 [論理エラー特定、レイテンシボトルネック解消、ハルシネーション抑制、Cloud Logging / Cloud Trace]）
- **重要キーワード**: Test Sets (Golden Dataset, Edge Cases), Tool Execution Evaluation, ADK evalset, Agent Platform Gen AI Evaluation Service, Custom Autoraters, Deployment Runtime (Agent Runtime, Cloud Run, GKE), Reasoning Loops, Tool Latency, Cloud Logging, Cloud Trace, Drift Detection

#### Section 5: エージェントワークフローのセキュリティとガバナンス (~15%)
- **出題の狙い**: 自律型エージェントによる外部 API 実行や社内データアクセスに伴うセキュリティリスクを多層的に防御し、アイデンティティ管理、トラフィック制御、コンテンツフィルタリング、および人間の介入（HITL）を組み合わせたガバナンス基盤を設計する能力を検証します。
- **主要タスク**:
  - Task 5.1: エージェントのセキュリティとガバナンスの構成（認証とセキュアなツール実行の実装 [OAuth 2.0 Auth Manager によるエージェントからツールへの API 呼び出し認可]、Agent Identity を用いたプリンシパルアクセス境界 [PAB: Principal Access Boundary] ポリシーの構成、Agent Gateway によるエージェントトラフィックの監視・追跡、Agent Registry および Model Armor を用いたエージェントガバナンスとポリシー強制）
  - Task 5.2: セキュアなエージェント挙動と実行の実装（適切な安全フレームワークとガードレールの設計 [Agent Gateway、Model Armor、Human-in-the-Loop / HITL]、データへのセキュアなアクセスとアイデンティティ伝播の構成 [Agent Gateway、Agent Registry、Sensitive Data Protection]）
- **重要キーワード**: Auth Manager (OAuth 2.0), Agent Identity, Principal Access Boundary (PAB), Agent Gateway, Model Armor, Agent Registry Policies, Human-in-the-Loop (HITL), Identity Propagation, Sensitive Data Protection (DLP), Prompt Injection / Jailbreak Mitigation

---

## 4. 推奨学習リソース＆公式ハンズオン・ラボ一覧

### 公式一次ドキュメント＆アーキテクチャガイド
- [Google Cloud Agentic Architecture Overview](https://cloud.google.com/learn/certification/agentic-architect?hl=ja): 資格公式概要
- [Professional Agentic Architect Exam Guide](https://services.google.com/fh/files/misc/professional_agentic_architect_exam_guide_english.pdf?hl=ja): 公式試験ガイド
- [Agent Development Kit (ADK) Documentation](https://docs.cloud.google.com/gemini-enterprise-agent-platform): ADK ライブラリとエージェント設計ガイド
- [Agent Runtime & Agent Platform Overview](https://docs.cloud.google.com/gemini-enterprise-agent-platform/scale): マネージドエージェント実行基盤
- [Model Context Protocol (MCP) Specification & Architecture](https://github.com/modelcontextprotocol): MCP 標準仕様
- [Vertex AI Model Armor Documentation](https://docs.cloud.google.com/model-armor/overview): 生成 AI セキュリティ・ガードレール
- [Vertex AI Search and Conversation Overview](https://docs.cloud.google.com/generative-ai-app-builder/docs): エンタープライズ検索と CX Studio

### 推奨実機ハンズオン・ラボ
- **Building Agents with Gemini Enterprise and CX Studio**:
  - **検証目標**: ページ遷移、インテント分岐、フォールバックイベントハンドラー、Agent Search のセキュア連携を GUI で検証。
- **Custom Agent Development with ADK and Memory Bank**:
  - **検証目標**: ADK を用いたステートフルエージェントの実装、セッション履歴の永続化、メモリバンクからのコンテキスト復元。
- **Multi-Agent Orchestration via MCP and A2A**:
  - **検証目標**: 複数の特化エージェント（リサーチャー、コーダー、レビューアー）を A2A プロトコルでオーケストレーションし、並列および順次ハンドオフを実行。
- **Continuous Evaluation with ADK evalset and Autoraters**:
  - **検証目標**: ゴールデンデータセットを用いたツール呼び出し正解率の自動測定、LLM-as-a-Judge による応答品質評価。
- **Securing Agents with Agent Gateway and Model Armor**:
  - **検証目標**: Agent Gateway によるプロンプトインジェクション攻撃の検知遮断、OAuth 2.0 Auth Manager を用いた外部 API トークン認可、HITL 承認フローの動作確認。
