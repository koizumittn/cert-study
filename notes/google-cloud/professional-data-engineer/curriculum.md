# Google Cloud Certified - Professional Data Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Data Engineer (PDE)
- **公式試験ガイド**: [Professional Data Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_data_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Data Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/data-engineer?hl=ja)
- **公式学習パス**: [Google Skills - Data Engineer Learning Path](https://www.skills.google/paths/18?hl=ja)
- **最終更新日**: 2026-10-14

---

## 1. 試験の概要と基本スペック

Professional Data Engineer は、さまざまなアプリケーションやビジネスシステムのデータを収集、変換、保存、配信することで、データドリブンな意思決定を可能にする最高峰の実務データエンジニアリング能力を客観的に評価・認定するプロフェッショナル資格です。

セキュリティ、スケーラビリティ、耐障害性、パフォーマンス、費用対効果を最適化しながら、エンタープライズ規模の堅牢なデータインフラストラクチャを設計・構築する能力が問われます。昨今のシラバス改訂により、従来のバッチ・ストリーミングパイプライン（Dataflow, Dataproc, Pub/Sub）やレイクハウス（BigQuery, BigLake, Dataplex）の設計・運用に加え、Dataform による SQL パイプラインオーケストレーション、生成 AI・LLM 向けデータ準備（BigQuery ML、ベクトル埋め込み、RAG パイプライン）、Analytics Hub による安全なデータ共有、BigQuery Editions とスロット予約管理といった最新機能が試験全体に色濃く反映されています。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: データ エンジニアリングに関する 3 年以上の実務経験、および Google Cloud を使用したソリューションの設計・構築・管理に関する 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 5 セクションで構成されています。データの取り込みと処理（25%）、データ処理システムの設計（22%）、データの保存（20%）が中核をなし、さらにデータワークロードの管理と自動化（18%）、分析用データの準備と使用（15%）が網羅的に評価されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | データ処理システムの設計 | 約 22.0% | Cloud IAM, 暗号化 (CMEK/CSEK), Cloud KMS, 機密データ保護 (Cloud DLP / Sensitive Data Protection), データ主権, ガバナンスアーキテクチャ (プロジェクト・データセット・テーブル階層), マルチ環境運用, Dataform, Dataflow, Cloud Data Fusion, プロンプト設計, パイプラインオーケストレーション, ACID/可用性トレードオフ, データ検証, マルチクラウドポータビリティ, 移行ツール (BigQuery DTS, Database Migration Service, Datastream, Transfer Appliance) |
| **Section 2** | データの取り込みと処理 | 約 25.0% | パイプライン計画 (ソース・シンク・変換ロジック), ネットワーク基礎 (Private Service Connect, VPC ピアリング, 限定公開の Google アクセス), Dataflow (Apache Beam, ウィンドウ処理, 透かし, 遅延データ, トリガー), Dataproc (Spark, Hadoop エコシステム), Cloud Data Fusion, BigQuery パイプライン, Pub/Sub, Kafka, AI によるデータ拡充, バッチ/ストリーミング統合, Cloud Composer (Airflow), Workflows, CI/CD パイプライン |
| **Section 3** | データの保存 | 約 20.0% | ストレージ選定 (BigQuery, BigLake, AlloyDB, Bigtable, Cloud Spanner, Cloud SQL, Cloud Storage, Firestore, Memorystore), データアクセスパターン分析, コストとパフォーマンス最適化, ライフサイクル管理, データウェアハウス設計 (データモデリング, スタースキーマ/スノーフレーク, 非正規化, ネスト＆反復フィールド), データレイク設計 (Cloud Storage, BigLake, オープンフォーマット Parquet/ORC/Iceberg), データプラットフォーム設計 (Dataplex, Dataplex Catalog, データメッシュ, 連合ガバナンス) |
| **Section 4** | 分析用データの準備と使用 | 約 15.0% | 可視化向けデータ準備 (Looker, Looker Studio), フィールド事前計算, BigQuery BI Engine, マテリアライズドビュー, クエリ最適化・トラブルシューティング (EXPLAIN, 実行ステージ, スロット消費, シャッフル), 動的データマスキング, 行・列レベルセキュリティ, AI/ML データ準備 (BigQuery ML, ベクトル埋め込み, 生成 AI・LLM 連携, RAG パイプライン), データ共有統制 (Analytics Hub, BigQuery Sharing) |
| **Section 5** | データ ワークロードの管理と自動化 | 約 18.0% | リソース最適化 (永続クラスタ vs 一時的ジョブクラスタ, Dataproc サーバーレス), 自動化と反復性 (Cloud Composer DAG, 依存関係, 再試行設計), BigQuery キャパシティ管理 (エディション: Standard/Enterprise/Enterprise Plus, 予約スロット, オートスケーリング, ベースライン), インタラクティブクエリ vs バッチクエリ, オブザーバビリティ (Cloud Monitoring, Cloud Logging, BigQuery Information Schema, 管理パネル), 障害復旧 (マルチリージョン/ゾーン, レプリケーション, フェイルオーバー) |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: データ処理システムの設計 (約 22%)
- **出題の狙い**: ビジネス要件、セキュリティ要件、コンプライアンス要件、およびデータライフサイクル要件を満たすスケーラブルで耐障害性に優れたデータ基盤アーキテクチャを全体設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: セキュリティとコンプライアンスを考慮した設計（Cloud IAM, 最小権限, 組織ポリシー, CMEK/CSEK による鍵管理, 機密データ保護, データ主権, マルチ環境分離, プロジェクト・データセット階層設計）
  - Task 1.2: 信頼性と確実性を考慮した設計（Dataform によるデータクリーニング・検証, Dataflow / Cloud Data Fusion, プロンプトエンジニアリングによるクエリ生成, 障害復旧・フォールトトレランス, ACID と可用性のトレードオフ判断）
  - Task 1.3: 柔軟性とポータビリティを考慮した設計（将来のビジネス要件へのマッピング, マルチクラウド・データ所在地要件, データのステージング, メタデータカタログ化, ガバナンス）
  - Task 1.4: データ移行の設計（関係者ニーズ分析, 移行計画・検証, BigQuery Data Transfer Service, Database Migration Service, Datastream による CDC, Transfer Appliance）
- **重要キーワード**: Cloud IAM, Cloud KMS, CMEK, Sensitive Data Protection (Cloud DLP), Data Sovereignty, Dataform, Cloud Data Fusion, ACID, CAP Theorem, BigQuery Data Transfer Service, Database Migration Service (DMS), Datastream, Transfer Appliance

#### Section 2: データの取り込みと処理 (約 25%)
- **出題の狙い**: バッチおよびリアルタイムストリーミングの双方において、多種多様なデータソースからデータを収集・変換・拡充し、下流のストレージや分析基盤へ効率的かつ確実に配信するデータパイプラインを構築・運用する能力を検証します。
- **主要タスク**:
  - Task 2.1: データパイプラインの計画（ソース・シンク定義, 変換・オーケストレーションロジック, プライベート接続・ネットワーキング, 暗号化）
  - Task 2.2: パイプラインの構築（Dataflow, Apache Beam, Dataproc, Spark, Hadoop, Cloud Data Fusion, BigQuery, Pub/Sub, Kafka, ウィンドウ処理, ウォーターマーク, 遅延データ処理, AI によるデータエンリッチメント）
  - Task 2.3: パイプラインのデプロイと運用化（Cloud Composer による Airflow DAG オーケストレーション, Workflows による軽量オーケストレーション, CI/CD パイプライン自動化）
- **重要キーワード**: Dataflow, Apache Beam, PCollection, ParDo, Sliding/Fixed/Session Windows, Watermark, Late Data & Allowed Lateness, Exactly-Once Processing, Dataproc Serverless, Spark Structured Streaming, Pub/Sub (Ordering Keys, Dead Letter Queue), Cloud Composer, Workflows, Cloud Build

#### Section 3: データの保存 (約 20%)
- **出題の狙い**: アクセスパターン、クエリ頻度、レイテンシ要件、トランザクション特性、およびコストに基づいて最適なストレージ・データベースサービスを選定し、スケーラブルなデータウェアハウス、データレイク、および連合データプラットフォームを設計する能力を検証します。
- **主要タスク**:
  - Task 3.1: ストレージシステムの選択（BigQuery, BigLake, AlloyDB, Bigtable, Cloud Spanner, Cloud SQL, Cloud Storage, Firestore, Memorystore のアクセスパターン別選定, コストとパフォーマンス計画, ライフサイクル管理）
  - Task 3.2: データウェアハウスの計画（データモデリング, スタースキーマ/スノーフレーク, 非正規化と構造体/配列型, パーティショニングとクラスタリングの設計）
  - Task 3.3: データレイクの使用（Cloud Storage バケット設計, オブジェクトライフサイクル, Parquet/ORC/Iceberg などのオープンフォーマット, レイク管理とモニタリング）
  - Task 3.4: データプラットフォームを考慮した設計（Dataplex による分散レイクハウス管理, Dataplex Catalog によるアセット検出, データメッシュアーキテクチャ, 集中統制と自律ドメインの連携ガバナンス）
- **重要キーワード**: BigQuery, BigLake, Bigtable (Row Key Design, Hotspotting Prevention), Cloud Spanner (TrueTime, Multi-Region), AlloyDB, Cloud Storage (Lifecycle Rules, Autoclass), Partitioning & Clustering, Dataplex, Dataplex Catalog, Data Mesh, Federated Governance

#### Section 4: 分析用データの準備と使用 (約 15%)
- **出題の狙い**: ビジネスインテリジェンス（BI）、データ探索、および機械学習・AI モデル向けに、安全かつ高パフォーマンスにデータを加工・最適化・共有する能力を検証します。
- **主要タスク**:
  - Task 4.1: 可視化用データの準備（Looker / Looker Studio 連携, 集計フィールド事前計算, BigQuery BI Engine インメモリキャッシュ, マテリアライズドビュー, 実行プラン EXPLAIN 分析とクエリチューニング, 動的データマスキング, 行・列レベルセキュリティ）
  - Task 4.2: AI と ML のためのデータの準備（BigQuery ML によるモデル作成・評価, 特徴量エンジニアリング, ベクトル埋め込み生成 `ML.GENERATE_EMBEDDING`, 非構造化データ準備, Vertex AI 統合, RAG パイプライン設計）
  - Task 4.3: データの共有（組織内外へのデータセット共有, ガバナンスルール定義, Analytics Hub によるデータエクスチェンジとリスティング, ゼロコピー共有）
- **重要キーワード**: BigQuery BI Engine, Materialized Views, Query Plan & Execution Stages, Slot Contention, Dynamic Data Masking, Policy Tags, Column-level Security, Row-level Security, BigQuery ML, `ML.GENERATE_EMBEDDING`, Vector Search, RAG (Retrieval-Augmented Generation), Analytics Hub

#### Section 5: データ ワークロードの管理と自動化 (約 18%)
- **出題の狙い**: データワークロードの運用効率、コスト、信頼性を最大化するために、コンピュートリソースのサイジング、スケーリング、オーケストレーション、オブザーバビリティ、および障害復旧を包括的に管理・最適化する能力を検証します。
- **主要タスク**:
  - Task 5.1: リソースの最適化（コスト最小化と SLA 遵守のバランス, 永続クラスタ vs 一時的ジョブベースクラスタ, Dataproc サーバーレスの活用）
  - Task 5.2: 自動化と反復性の設計（Cloud Composer DAG の冪等性・リトライ設計, ワークフロースケジューリング, 障害通知）
  - Task 5.3: ビジネス要件に基づくワークロードの最適化（BigQuery エディション [Standard, Enterprise, Enterprise Plus], スロット予約 [Reservations], ベースラインスロットとオートスケーリング, インタラクティブクエリ vs バッチクエリ）
  - Task 5.4: プロセスのモニタリングとトラブルシューティング（Cloud Monitoring / Logging によるパイプライン監視, BigQuery 管理パネル, INFORMATION_SCHEMA 分析, 割り当て [Quotas] と課金アラートの対処）
  - Task 5.5: 障害への意識の持続と影響の軽減（フォールトトレラント設計, マルチリージョン・マルチゾーン展開, データ破損・欠落対策, データベースのフェイルオーバーとレプリケーション）
- **重要キーワード**: Dataproc Serverless, Ephemeral Clusters, Cloud Composer Airflow DAGs, Idempotency, BigQuery Editions (Standard, Enterprise, Enterprise Plus), Slot Reservations, Autoscaling Slots, INFORMATION_SCHEMA.JOBS_BY_*, Cloud Monitoring & Logging, RTO / RPO, High Availability (HA) & Disaster Recovery (DR)

---

## 4. 推奨ハンズオンラボ（Google Skills）

実務での手触り感と試験対策を直結させるため、以下の厳選ハンズオンラボの受講を強く推奨します。

1. **Build a Data Warehouse with BigQuery (Skill Badge)**
   - リンク: [Google Skills - Build a Data Warehouse with BigQuery](https://www.skills.google/course_templates/624?hl=ja)
   - 実践内容: パーティショニング、クラスタリング、マテリアライズドビューの作成とクエリパフォーマンス検証。
2. **Engineer Data in Google Cloud (Skill Badge)**
   - リンク: [Google Skills - Engineer Data in Google Cloud](https://www.skills.google/course_templates/626?hl=ja)
   - 実践内容: Dataflow によるバッチ・ストリーミングパイプライン構築、Dataproc での Spark 実行、BigQuery ML の構築。
3. **Build and Manage Cloud Data Pipelines with Cloud Data Fusion and Dataflow (Skill Badge)**
   - リンク: [Google Skills - Build and Manage Cloud Data Pipelines](https://www.skills.google/course_templates/627?hl=ja)
   - 実践内容: Cloud Data Fusion によるノーコードパイプライン作成、Dataflow の高度なウィンドウ処理と変換。
4. **Data Catalog and Dataplex Fundamentals**
   - リンク: [Google Skills - Dataplex Hands-on Lab](https://www.skills.google/course_templates/630?hl=ja)
   - 実践内容: Dataplex レイク・ゾーンの作成、アセット登録、自動メタデータ検出とデータ品質ルールの設定。
