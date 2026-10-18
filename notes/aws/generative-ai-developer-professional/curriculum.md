# AWS Certified Generative AI Developer - Professional (AIP-C01) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Generative AI Developer - Professional
- **試験コード**: AIP-C01
- **公式試験ガイド**: [AWS Certified Generative AI Developer - Professional (AIP-C01) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/ai-professional-01/ai-professional-01.html)
- **最終更新日**: 2026-10-07

---

## 1. 試験の概要と基本スペック

AWS Certified Generative AI Developer - Professional (AIP-C01) は、生成 AI (GenAI) デベロッパーを対象とし、基盤モデル (FM) を本番環境のエンタープライズアプリケーションやビジネスワークフローへセキュア、高可用、かつコスト効率よく統合・実装・運用する専門的能力を客観的に証明するプロフェッショナル認定資格です。

- **試験時間**: 180 分
- **出題問題数**: 75 問（採点対象: 65 問 / 未採点テスト設問: 10 問）
- **出題形式**: 択一選択問題、複数選択問題
- **合格基準点**: 100〜1,000 点中 750 点以上
- **前提知識・実務経験**: AWS またはオープンソース技術を用いた本番環境アプリケーション構築 2 年以上の経験、AI/ML またはデータエンジニアリングの経験、GenAI ソリューション実装 1 年以上の実務経験。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 |
| :--- | :--- | :--- | :--- |
| **Domain 1** | 基盤モデルの統合、データ管理、コンプライアンス | 31% | Amazon Bedrock, Knowledge Bases, OpenSearch Service, pgvector, Titan Embeddings, Prompt Flows, Data Automation, Step Functions |
| **Domain 2** | 実装と統合 | 26% | Strands Agents, AWS Agent Squad, Model Context Protocol (MCP), ReAct, Bedrock Streaming API, API Gateway, EventBridge, CodePipeline |
| **Domain 3** | AI の安全性、セキュリティ、ガバナンス | 20% | Bedrock Guardrails, SageMaker Model Cards, Lake Formation, Macie, Comprehend PII, VPC Endpoints, IAM, CloudTrail |
| **Domain 4** | GenAI アプリケーションの運用効率と最適化 | 12% | プロンプトキャッシング, セマンティックキャッシュ, コンテキストプルーニング, バッチ推論, プロビジョンドスループット, CloudWatch, X-Ray |
| **Domain 5** | テスト、検証、トラブルシューティング | 11% | Bedrock Model Evaluation, LLM-as-a-judge, RAG評価, エージェント評価, ゴールデンデータセット, CloudWatch Logs Insights |

---

## 3. ドメイン別タスクおよび学習ロードマップ

### Domain 1: 基盤モデルの統合、データ管理、コンプライアンス (31%)
- **Task 1.1**: 要件を分析し、GenAI ソリューションを設計する（包括的アーキテクチャ設計、PoC検証、AWS Well-Architected Framework Generative AI Lens）
- **Task 1.2**: FM を選定して設定する（モデル評価基準、動的モデル切り替え/AppConfig、レジリエント設計/サーキットブレーカー/クロスリージョン推論、SageMaker LoRA/アダプターデプロイ/Model Registry）
- **Task 1.3**: FM 消費のためのデータ検証と処理パイプラインを実装する（Glue Data Quality、Data Wrangler、マルチモーダルデータ処理パイプライン、入力フォーマット変換、Comprehend によるエンティティ抽出）
- **Task 1.4**: ベクトルストアソリューションを設計して実装する（Bedrock Knowledge Bases、OpenSearch Service Neural プラグイン、pgvector、メタデータフレームワーク、シャーディング/マルチインデックス、増分同期・リアルタイム更新）
- **Task 1.5**: FM 拡張のための検索メカニズムを設計する（チャンク化戦略、Titan 埋め込みモデル選定、ハイブリッド検索、Bedrock リランカー、クエリ拡張/分解/変換、MCP クライアント統合）
- **Task 1.6**: プロンプトエンジニアリングとプロンプト管理を実装する（Bedrock Prompt Management、会話履歴/DynamoDB、プロンプトガバナンス、思考連鎖/CoT、Bedrock Prompt Flows）

### Domain 2: 実装と統合 (26%)
- **Task 2.1**: エージェンティック AI ソリューションとツール統合を実装する（Strands Agents、AWS Agent Squad、MCP サーバー/クライアント、ReAct パターン、Step Functions 停止条件、Human-in-the-Loop）
- **Task 2.2**: モデルデプロイ戦略を実施する（オンデマンド呼び出し、Bedrock プロビジョンドスループット、SageMaker エンドポイント、モデルカスケード）
- **Task 2.3**: エンタープライズ統合アーキテクチャを設計し実装する（レガシー API 連携、EventBridge イベント駆動、ID フェデレーション、AWS Outposts/Wavelength、GenAI ゲートウェイ/CI/CD）
- **Task 2.4**: FM API 統合を実装する（同期/非同期 SQS、Bedrock ストリーミング API、WebSocket/SSE、エクスポネンシャルバックオフ、動的モデルルーティング）
- **Task 2.5**: GenAI アプリケーションインターフェイスと拡張機能を実装する（ストリーミング UI/Amplify、Bedrock Prompt Flows、CRM/業務システム連携、Bedrock Data Automation、Amazon Q Developer）

### Domain 3: AI の安全性、セキュリティ、ガバナンス (20%)
- **Task 3.1**: 入力と出力の安全コントロールを実装する（Bedrock Guardrails、毒性検出、ハルシネーション抑制/グラウンディング、多層防御、プロンプトインジェクション/ジェイルブレイク防御）
- **Task 3.2**: データセキュリティとプライバシーコントロールを実装する（VPC エンドポイント、IAM、Lake Formation、Macie/Comprehend PII 検出・マスキング、S3 ライフサイクル）
- **Task 3.3**: AI ガバナンスとコンプライアンスのメカニズムを実装する（SageMaker Model Cards、Glue データリネージュ、CloudTrail 監査ログ、ドリフト/ポリシー違反検知）
- **Task 3.4**: 責任ある AI の原則を実装する（推論トレース表示、公平性評価/A/B テスト、Bedrock Guardrails ポリシー準拠）

### Domain 4: GenAI アプリケーションの運用効率と最適化 (12%)
- **Task 4.1**: コスト最適化とリソース効率化の戦略を実施する（トークン効率/プロンプト圧縮、階層型モデル選定、プロンプトキャッシング、セマンティックキャッシュ）
- **Task 4.2**: アプリケーションのパフォーマンスを最適化する（レイテンシ最適化、ストリーミング、ハイブリッド検索チューニング、バッチ推論、推論パラメータ/Temperature/Top-P 最適化）
- **Task 4.3**: GenAI アプリケーションのモニタリングシステムを実装する（CloudWatch トークン追跡/異常検知、Bedrock モデル呼び出しログ、X-Ray トレース、ツール/エージェント監視、ベクトルストア運用監視）

### Domain 5: テスト、検証、トラブルシューティング (11%)
- **Task 5.1**: GenAI の評価システムを実装する（関連性/正確性/一貫性/流暢さ、Bedrock Model Evaluation、LLM-as-a-judge、RAG 評価、エージェント評価フレームワーク）
- **Task 5.2**: GenAI アプリケーションをトラブルシューティングする（コンテキストオーバーフロー診断、動的チャンク化、API 統合エラー解決、検索品質ドリフト診断、プロンプト回帰診断）
