# Google Cloud Certified - Associate Data Practitioner 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Associate Data Practitioner (ADP)
- **公式試験ガイド**: [Associate Data Practitioner 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/associate_data_practitioner_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Associate Data Practitioner | Google Cloud Certification](https://cloud.google.com/learn/certification/associate-data-practitioner)
- **公式学習パス**: [Google Skills - Associate Data Practitioner Certification](https://www.skills.google/paths/1336?hl=ja)
- **最終更新日**: 2026-10-12

---

## 1. 試験の概要と基本スペック

Associate Data Practitioner は、Google Cloud 上でデータを安全に保護・管理し、データの取り込み、変換、パイプライン管理、分析、機械学習（基礎的タスク）、および可視化を効果的に遂行できる実務能力を客観的に評価・認定する資格です。

データアナリスト、ビジネスアナリスト、BI（Business Intelligence）専門家、マーケター、ならびにクラウドデータ分析の実務を担う初級〜中級のエンジニアを対象としています。深いプログラミング言語スキルや複雑な分散インフラの構築経験は必須とされず、IaaS（Infrastructure as Service）、PaaS（Platform as a Service）、SaaS（Software as a Service）などのクラウドコンピューティングの基本概念を理解した上で、Google Cloud のマネージドデータサービスを自在に組み合わせてビジネス課題を解決できる能力が求められます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $125（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: Google Cloud データサービスを用いた 6 か月以上の実務経験、またはクラウドデータ分析に関する基礎知識が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 4 セクションで構成されています。データの準備と取り込み（最大 30%）とデータ分析・プレゼンテーション（最大 27%）で全体の半数以上を占め、さらにデータマネジメント（最大 25%）、データパイプラインのオーケストレーション（最大 18%）が問われます。データライフサイクル全体にわたるマネージドサービスの選定・活用基準が網羅されています。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | データの準備と取り込み | 30% 以下 | ETL / ELT / ETLT、データ品質評価、データクリーニング、Cloud Data Fusion、BigQuery SQL、Dataflow、Storage Transfer Service、Transfer Appliance、Database Migration Service、BigQuery Data Transfer Service、データ形式（CSV, JSON, Parquet, Avro）、ストレージ選定（Cloud Storage, BigQuery, Cloud SQL, Spanner, Bigtable, Firestore）、ロケーション設計（リージョン/デュアル/マルチ/ゾーン） |
| **Section 2** | データ分析とプレゼンテーション | 27% 以下 | BigQuery SQL（集計・分析関数）、Jupyter ノートブック（Colab Enterprise）、ビジネス課題の解決、Looker vs Looker Studio、LookML パラメータ・データモデル、BigQuery ML（CREATE MODEL, EVALUATE, PREDICT）、AutoML、Vertex AI リモート接続（事前トレーニング済み LLM / Gemini）、ML プロジェクトライフサイクル、Model Registry |
| **Section 3** | データ パイプラインのオーケストレーション | 18% 以下 | データ変換ツール選定（Dataproc / Managed Service for Apache Spark, Dataflow, Cloud Data Fusion, Cloud Composer / Managed Service for Apache Airflow, Dataform）、ELT vs ETL 評価、BigQuery スケジュールされたクエリ、Cloud Scheduler、Workflows、Eventarc、Dataflow ジョブ UI 監視、Cloud Logging / Cloud Monitoring、Pub/Sub イベントドリブン取り込み |
| **Section 4** | データ マネジメント | 25% 以下 | IAM 最小権限（基本ロール vs 事前定義ロール vs 権限）、Cloud Storage アクセス制御（公開 vs プライベート vs 均一なバケットレベルのアクセス）、BigQuery データ共有（データセット共有, 承認済みビュー, Analytics Hub）、Cloud Storage ストレージクラス（Standard, Nearline, Coldline, Archive）、オブジェクト ライフサイクル管理、BigQuery テーブル/パーティション有効期限、Cloud SQL / Cloud Storage バックアップ・復元・HA、暗号化（GMEK vs CMEK vs CSEK）、Cloud KMS、保存時/転送時暗号化 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: データの準備と取り込み（30% 以下）
- **出題の狙い**: さまざまなソースシステムから Google Cloud 環境へデータを安定的かつ効率的に取り込み、分析可能な状態へ整形・クリーニングするための適切なツール選定とストレージ設計能力を検証します。
- **主要タスク**:
  - Task 1.1: データの準備と処理（ETL、ELT、ETLT の概念と使い分け、Storage Transfer Service や Transfer Appliance 等のデータ転送ツールの選択、データ品質評価、Cloud Data Fusion、BigQuery、SQL、Dataflow を用いたデータクリーニング）
  - Task 1.2: データを抽出して適切な Google Cloud ストレージ システムに読み込む（ファイル形式の比較 [CSV, JSON, Apache Parquet, Apache Avro, RDBMS テーブル]、抽出ツールの選定 [Dataflow, BigQuery Data Transfer Service, Database Migration Service, Cloud Data Fusion]、ストレージソリューションの選定 [Cloud Storage, BigQuery, Cloud SQL, Firestore, Bigtable, Spanner]、データストレージロケーションタイプ [リージョン, デュアルリージョン, マルチリージョン, ゾーン]、構造化・半構造化・非構造化データの分類、ロードツールの活用 [gcloud, bq CLI, Storage Transfer Service, BigQuery Data Transfer Service, クライアントライブラリ]）
- **重要キーワード**: ETL vs ELT vs ETLT, Storage Transfer Service, Transfer Appliance, Dataflow, Cloud Data Fusion, BigQuery Data Transfer Service (DTS), Database Migration Service (DMS), Parquet vs Avro vs CSV/JSON, Cloud Storage, BigQuery, Cloud SQL, Spanner, Bigtable, Firestore, Regional / Dual-region / Multi-region / Zonal, bq load

#### Section 2: データ分析とプレゼンテーション（27% 以下）
- **出題の狙い**: BigQuery と Colab Enterprise（Jupyter ノートブック）を用いた探索的データ分析、Looker / Looker Studio を用いた効果的なデータ可視化とダッシュボード構築、ならびに BigQuery ML や生成 AI（Vertex AI リモートモデル）を活用した基礎的な機械学習モデルの構築・推論能力を検証します。
- **主要タスク**:
  - Task 2.1: BigQuery と Jupyter ノートブックを使用して、データの傾向、パターン、分析情報を特定する（BigQuery での SQL クエリ定義・実行、レポート生成と分析情報の抽出、Colab Enterprise / Jupyter ノートブックによるデータ分析・可視化、ビジネス上の疑問に対する回答導出）
  - Task 2.2: ビジネス要件に基づいて、Looker でデータを可視化し、ダッシュボードを作成する（ダッシュボードの作成・変更・共有、各種分析ユースケースにおける Looker と Looker Studio の比較・選定、簡単な LookML パラメータ [view, explore, dimension, measure] の操作によるデータモデル変更）
  - Task 2.3: ML モデルを定義、トレーニング、評価、使用する（BigQuery ML と AutoML を使用したモデル開発のユースケース特定、BigQuery のリモート接続を使用した Google 事前トレーニング済み LLM [Gemini] の呼び出し、標準的な ML プロジェクトの計画 [データ収集、学習、評価、予測]、SQL による BigQuery ML モデル作成・評価・推論 [CREATE MODEL, ML.EVALUATE, ML.PREDICT]、Vertex AI Model Registry によるモデルの一元管理）
- **重要キーワード**: BigQuery SQL, Colab Enterprise, Looker vs Looker Studio, LookML (view, explore, dimension, measure), BigQuery ML (CREATE MODEL, ML.EVALUATE, ML.PREDICT), AutoML, Remote Connection (Cloud Resource Connection), Vertex AI LLM (Gemini), Model Registry

#### Section 3: データ パイプラインのオーケストレーション（18% 以下）
- **出題の狙い**: 単発のデータ処理を安定的かつ反復可能なワークフローとして自動化・スケジュール化し、異常発生時に迅速に対処できるようモニタリングおよびログ監視を行うパイプライン構築能力を検証します。
- **主要タスク**:
  - Task 3.1: シンプルなデータ パイプラインを設計、実装する（ビジネス要件に基づく変換ツールの選択 [Dataproc / Managed Service for Apache Spark, Dataflow, Cloud Data Fusion, Cloud Composer / Managed Service for Apache Airflow, Dataform]、ELT と ETL のユースケース評価、基本変換パイプラインの実装プロダクト選定）
  - Task 3.2: 基本的なデータ処理タスクのスケジュール設定、自動化、モニタリングを行う（スケジュールされたクエリの作成と管理 [BigQuery, Cloud Scheduler, Cloud Composer]、Dataflow ジョブ UI を使用した進行状況モニタリング、Cloud Logging と Cloud Monitoring でのログ・メトリクス分析、データオーケストレーションツールの選択 [Cloud Composer, スケジュールされたクエリ, Dataproc ワークフロー テンプレート, Workflows]、Pub/Sub から BigQuery へのイベントドリブンデータ取り込み、Eventarc トリガーの活用 [Dataform, Dataflow, Cloud Run functions, Cloud Run, Cloud Composer]）
- **重要キーワード**: Dataproc, Dataflow, Cloud Data Fusion, Cloud Composer (Apache Airflow), Dataform, BigQuery Scheduled Queries, Cloud Scheduler, Workflows, Eventarc, Pub/Sub BigQuery Subscription, Dataflow Monitoring UI, Cloud Logging, Cloud Monitoring

#### Section 4: データ マネジメント（25% 以下）
- **出題の狙い**: Google Cloud 上のデータ資産に対して、適切なアクセス制御、最小権限の付与、データのライフサイクル管理、高可用性（HA）と障害復旧（DR）の確保、および暗号化をはじめとするセキュリティとデータプライバシー規制の遵守を実現するガバナンス能力を検証します。
- **主要タスク**:
  - Task 4.1: アクセス制御とガバナンスを構成する（IAM による最小権限アクセスの原則、基本ロール・事前定義ロール・個別データサービス権限の区別 [BigQuery, Cloud Storage]、Cloud Storage のアクセス制御方式 [公開, プライベート, 均一なバケットレベルのアクセス]、BigQuery データ共有 [データセット共有, 承認済みビュー, Analytics Hub] の使い分け）
  - Task 4.2: ライフサイクル管理を構成する（アクセス頻度と保持要件に応じた Cloud Storage クラス [Standard, Nearline, Coldline, Archive] の決定、経過期間に応じた自動削除・クラス移行ルールの構成、BigQuery テーブルおよびパーティションの有効期限設定、アーカイブサービスの評価）
  - Task 4.3: Cloud Storage と Cloud SQL のデータの高可用性と障害復旧の戦略を特定する（マネージドバックアップと復元ソリューションの比較、レプリケーションの適用判断、プライマリとセカンダリのロケーションタイプ [リージョン, デュアルリージョン, マルチリージョン, ゾーン] の区別）
  - Task 4.4: セキュリティ対策を適用し、データ プライバシー規制を遵守する（暗号鍵の管理方式 [Google 管理の暗号鍵 GMEK, 顧客管理の暗号鍵 CMEK, 顧客指定の暗号鍵 CSEK] のユースケース特定、Cloud KMS の役割、転送時暗号化と保存時暗号化の違い、機密データの保護）
- **重要キーワード**: IAM (Least Privilege), Uniform Bucket-Level Access, BigQuery Dataset Sharing, Authorized Views, Analytics Hub, Cloud Storage Classes (Standard, Nearline, Coldline, Archive), Object Lifecycle Management, Partition Expiration, Cloud SQL Automated Backups & HA, Cross-Region Replication, GMEK vs CMEK vs CSEK, Cloud KMS, Encryption at Rest / in Transit, Sensitive Data Protection (Cloud DLP)
