# Google Cloud Certified - Professional Cloud Developer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Cloud Developer (PCD)
- **公式試験ガイド**: [Professional Cloud Developer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_cloud_developer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Cloud Developer | Google Cloud Certification](https://cloud.google.com/learn/certification/cloud-developer?hl=ja)
- **公式学習パス**: [Google Skills - Cloud Developer Learning Path](https://www.skills.google/paths/19?hl=ja)
- **最終更新日**: 2026-10-13

---

## 1. 試験の概要と基本スペック

Professional Cloud Developer は、Google が推奨するツール、ランタイム、およびベストプラクティスを活用して、スケーラブル、高可用性、安全、かつ信頼性の高いクラウドネイティブ アプリケーションを設計、構築、テスト、デプロイ、統合する実務開発者能力を客観的に評価・認定するプロフェッショナル資格です。

クラウドネイティブ アプリケーションの全体設計、最新のコンテナランタイム（Cloud Run、Google Kubernetes Engine [GKE]）、マネージドデータストア（Cloud SQL、AlloyDB、Spanner、Bigtable、Firestore、Cloud Storage）、CI/CD パイプライン（Cloud Build、Artifact Registry、Binary Authorization）、イベント駆動アーキテクチャ（Pub/Sub、Eventarc、Workflows）、API 管理（Apigee）、オブザーバビリティ（Google Cloud Observability、Cloud Trace、Error Reporting）、および最新の開発ツール（Gemini Cloud Assist、AI コーディングアシスタント、MCP サーバー、Cloud Workstations）の実践的適用が網羅的に問われます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スコア非開示）
- **前提知識**: クラウド アーキテクチャおよびクラウドネイティブ アプリケーション開発に関する 3 年以上の実務経験、および Google Cloud を使用したソリューションの構築・管理に関する 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 4 セクションで構成されています。アプリケーション設計（約 32%）を最重要基盤とし、構築とテスト（約 23%）、デプロイ構成（約 24%）、サービス統合とオブザーバビリティ（約 21%）がバランス良く問われます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | スケーラビリティ、安全性、信頼性に優れたクラウド ネイティブなアプリケーションの設計 | 約 32.0% | プラットフォーム選定 (Cloud Run, GKE, GCE), 地理的冗長性・レイテンシ, ロードバランサ, キャッシュ (Memorystore), API設計 (REST, gRPC), 非同期/イベント駆動 (Pub/Sub, Eventarc, Workflows, Cloud Tasks, Cloud Scheduler), トラフィック分割 (Canary, Blue/Green), セキュリティ (IAM, IAP, Secret Manager, Cloud KMS, Workload Identity 連携, Cloud SQL/AlloyDB Auth Proxy, Cloud Service Mesh), ストレージ選定・スキーマ設計 (Cloud Storage, Cloud SQL, AlloyDB, Spanner, Bigtable, Firestore, BigQuery) | 完了 |
| **Section 2** | アプリケーションの構築とテスト | 約 23.0% | 開発環境 (Google Cloud CLI エミュレータ, Cloud SDK, Cloud Code, Cloud Shell, Cloud Workstations, Gemini Cloud Assist, MCP サーバー統合), ビルド自動化 (Cloud Build, Artifact Registry, ビルド来歴 / Provenance), セキュリティ検証 (Binary Authorization), テスト自動化 (AI コーディングアシスタントによる単体テスト, Cloud Build 統合テスト) | 完了 |
| **Section 3** | デプロイのためのクラウドネイティブ アプリケーションの構成 | 約 24.0% | Cloud Run デプロイ (ソースデプロイ, コンテナデプロイ, Eventarc/Pub/Sub トリガー, イベントレシーバ), API 管理・保護 (Apigee), GKE デプロイ (コンテナデプロイ, Kubernetes ヘルスチェック [Liveness, Readiness, Startup], HorizontalPodAutoscaler [HPA], スケーリング指標) | 完了 |
| **Section 4** | アプリケーションと Google Cloud サービスの統合 | 約 21.0% | データストア統合 (Cloud SQL, Firestore, Cloud Storage, 接続プール・コネクタ), Pub/Sub メッセージング (パブリッシャー/サブスクライバー実装), Google Cloud API 呼び出し (クライアントライブラリ, gRPC/REST, 一括処理, 戻り値制限/フィールドマスク, ページネーション, キャッシュ, 指数バックオフ, サービスアカウント認証), トラブルシューティング・オブザーバビリティ (Cloud Monitoring, Cloud Logging, Cloud Trace 分散トレース, Error Reporting, AI 支援オブザーバビリティ) | 完了 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: スケーラビリティ、安全性、信頼性に優れたクラウド ネイティブなアプリケーションの設計 (約 32%)
- **出題の狙い**: 要件（スループット、レイテンシ、ステートレス/ステートフル、整合性、コンプライアンス）に合致する最適なコンピュート・ストレージ・メッセージング基盤を選定し、疎結合かつ耐障害性の高い多層分散アーキテクチャを安全に設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: 高パフォーマンスのアプリケーションと API を設計する（プラットフォーム選定 [Compute Engine, GKE, Cloud Run], コンテナ構築・リファクタリング, 地理的冗長性とレイテンシ設計, ロードバランサ選定, セッションアフィニティ, Memorystore キャッシュ, REST vs gRPC API 設計, Apigee/API Gateway によるレート制限・認証, Pub/Sub・Eventarc・Workflows・Cloud Tasks・Cloud Scheduler による非同期連携・オーケストレーション, トラフィック分割戦略）
  - Task 1.2: 安全なアプリケーションを設計する（Cloud Storage ライフサイクル・保持ポリシー・バケットロック, IAP, Web Security Scanner, Artifact Analysis, Security Command Center, Secret Manager, Cloud KMS, Workload Identity 連携, ADC / OAuth 2.0 / JWT / Cloud SQL Auth Proxy / AlloyDB Auth Proxy / WIF, サービスアカウント IAM 最小権限, Cloud Service Mesh, ダイレクト VPC 外向き, プライベートサービスアクセス, Binary Authorization）
  - Task 1.3: データを保存してアクセスする（データ量・性能要件に基づくストレージ選定, AlloyDB / Spanner / Bigtable / Firestore のスキーマ設計, 結果整合性と強整合性レプリケーションの影響, Cloud Storage 署名付き URL, BigQuery へのストリーミング/バッチ書き込み）
- **重要キーワード**: Cloud Run, GKE, Memorystore, gRPC vs REST, Workflows, Cloud Tasks, Eventarc, Pub/Sub, Workload Identity 連携, Cloud SQL Auth Proxy, AlloyDB Auth Proxy, Direct VPC egress, Cloud Service Mesh, Binary Authorization, Spanner, Bigtable, Firestore, Strong Consistency vs Eventual Consistency, Signed URLs

#### Section 2: アプリケーションの構築とテスト (約 23%)
- **出題の狙い**: ローカル開発環境の最適化から、エミュレータを活用したテスト、AI 支援ツールや MCP サーバーの統合、Cloud Build を活用したセキュアなコンテナビルド・来歴管理・自動テストまでの効率的な開発ライフサイクルを確立する能力を検証します。
- **主要タスク**:
  - Task 2.1: 開発環境を設定する（Google Cloud CLI エミュレータ [Pub/Sub, Firestore, Cloud Storage, Spanner], Cloud SDK, Cloud Code, Gemini Cloud Assist, Cloud Shell, Cloud Workstations, AI コーディングアシスタント, MCP サーバー統合）
  - Task 2.2: 構築する（Cloud Build と Artifact Registry によるコンテナビルド・保存, ビルド来歴 [Build Provenance] の構成, Binary Authorization 連携）
  - Task 2.3: テストする（AI コーディングアシスタントを利用した単体テスト作成, Cloud Build での自動統合テスト実行）
- **重要キーワード**: Google Cloud CLI Emulators, Cloud Workstations, Cloud Code, Gemini Cloud Assist, Model Context Protocol (MCP), Cloud Build (cloudbuild.yaml), Artifact Registry, Build Provenance (SLSA), Binary Authorization Attestation, Integration Testing

#### Section 3: デプロイのためのクラウドネイティブ アプリケーションの構成 (約 24%)
- **出題の狙い**: コンテナ化されたワークロードを Cloud Run および GKE に最適にデプロイし、イベントトリガー、API 公開・セキュリティ、ヘルスチェック、自動スケーリングメカニズムを適切に構成・運用する能力を検証します。
- **主要タスク**:
  - Task 3.1: アプリケーションを Cloud Run にデプロイする（ソースコードからのデプロイ [Buildpacks], Eventarc / Pub/Sub トリガー連携, イベントレシーバ設定, Apigee による API バージョニング・公開・保護）
  - Task 3.2: コンテナを GKE にデプロイする（コンテナ化アプリのデプロイ, Kubernetes ヘルスチェック [Liveness, Readiness, Startup Probe], HorizontalPodAutoscaler [HPA] 構成, カスタム・外部指標スケーリング）
- **重要キーワード**: Cloud Run, Google Cloud Buildpacks, Eventarc Triggers, Push Subscription, Apigee API Management, GKE Autopilot / Standard, Liveness Probe, Readiness Probe, Startup Probe, HorizontalPodAutoscaler (HPA), Metrics Server, Custom Metrics Adapter

#### Section 4: アプリケーションと Google Cloud サービスの統合 (約 21%)
- **出題の狙い**: Google Cloud データストアやメッセージングサービスとの効率的な連携コードを実装し、Google Cloud API のベストプラクティス（リトライ、ページング、帯域最適化）を適用するとともに、Cloud Observability による分散トレースや障害解析を遂行する能力を検証します。
- **主要タスク**:
  - Task 4.1: アプリケーションにデータサービスとストレージサービスを統合する（Cloud SQL, Firestore, Cloud Storage への接続管理・コネクションプール, データ読み書き, Pub/Sub パブリッシャー・サブスクライバークライアント実装）
  - Task 4.2: Google Cloud API を使用する（Service Usage API による有効化, Cloud クライアントライブラリ, REST / gRPC, バッチ処理リクエスト, フィールドマスク [FieldMask] による戻り値制限, ページネーション [pageToken / nextPageToken], キャッシュ, 指数バックオフ付き再試行 [Exponential Backoff with Jitter], サービスアカウント認証）
  - Task 4.3: トラブルシューティングとオブザーバビリティ（Google Cloud Observability [Monitoring, Logging, Trace] のコード計装, OpenTelemetry 連携, 問題特定・解決, Error Reporting による例外集約・アラート, Trace ID によるマイクロサービス間スパン伝播, AI を活用したログ分析・根本原因特定）
- **重要キーワード**: Google Cloud Client Libraries, Connection Pooling, FieldMask, Pagination (pageToken), Exponential Backoff with Jitter, Cloud Logging, Cloud Monitoring, Cloud Trace, Trace Context (traceparent), Error Reporting, OpenTelemetry, Gemini Cloud Assist for Observability
