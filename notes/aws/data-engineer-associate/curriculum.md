# AWS Certified Data Engineer - Associate (DEA-C01) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Data Engineer - Associate
- **試験コード**: DEA-C01
- **公式試験ガイド**: [AWS Certified Data Engineer - Associate (DEA-C01) Exam Guide](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/data-engineer-associate-01/data-engineer-associate-01.html)
- **最終更新日**: 2026-10-06

---

## 1. 試験の概要と基本スペック

AWS Certified Data Engineer - Associate は、データエンジニアリングの実務において、データの取り込みから保存、変換、パイプライン運用、セキュリティ、ガバナンスに至るライフサイクル全体を適切に構築・最適化する能力を検証します。

- **試験時間**: 130 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **合格基準点**: 100〜1,000 点のスケールドスコアで 720 点以上
- **前提知識**: データの取り込み、変換、モデリング、セキュリティ、ガバナンス、スキーマ設計における 2〜3 年相当のデータエンジニアリング実務経験と、1〜2 年以上の AWS サービスの実務経験が推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | ドメイン名 / 出題分野 | 出題比率 | 主要対象サービス・ツール | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Domain 1** | データの取り込みと変換 | 34% | Amazon Kinesis Data Streams, Amazon Kinesis Data Firehose, Amazon MSK, AWS Glue (ETL / Streaming), Amazon EMR, AWS Lambda, AWS Step Functions, Amazon MWAA, Amazon AppFlow, AWS DMS | 完了 |
| **Domain 2** | データストア管理 | 26% | Amazon S3, Amazon Redshift, AWS Lake Formation, Amazon DynamoDB, Amazon RDS / Aurora, Amazon OpenSearch Service, AWS Glue Data Catalog, Apache Iceberg | 完了 |
| **Domain 3** | データ運用とサポート | 22% | Amazon Athena, AWS Glue Data Quality, AWS Glue DataBrew, Amazon QuickSight, Amazon CloudWatch Logs Insights, AWS CloudTrail, Amazon EventBridge, Amazon SNS | 完了 |
| **Domain 4** | データセキュリティとガバナンス | 18% | AWS Lake Formation (LF-TBAC), AWS IAM, AWS KMS, AWS Secrets Manager, Amazon Macie, AWS CloudTrail Lake, AWS Config, Amazon Redshift データ共有 | 完了 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

#### Domain 1: データの取り込みと変換 (34%)
- **出題の狙い**: ストリーミング・バッチ双方の多様なデータソースから効率的にデータを取り込み、スケーラブルな分散処理基盤で変換・整形し、信頼性の高いワークフローとしてオーケストレーションする能力を検証します。
- **主要タスク**:
  - Task 1.1: データ取り込みの実行（ストリーミング [Kinesis, MSK]、バッチ [S3, Glue, EMR, AppFlow]、CDC [AWS DMS]、ファンイン/ファンアウト、スロットリング緩和、再現性）
  - Task 1.2: データの変換と処理（コンテナ最適化 [ECS, EKS]、JDBC/ODBC 接続、データ統合、フォーマット変換 [.parquet, .orc]、コスト最適化、LLM 統合）
  - Task 1.3: データパイプラインのオーケストレーション（AWS Step Functions、Amazon MWAA、AWS Glue ワークフロー、障害通知 [SNS, SQS]、サーバーレスワークフロー）
  - Task 1.4: プログラミングの概念の応用（Python/SQL/Scala、分散コンピューティング、Lambda 同時実行・EFS マウント、AWS SAM / CloudFormation による IaC デプロイ）
- **重要キーワード**: Amazon Kinesis Data Streams, Amazon Kinesis Data Firehose, Amazon Managed Streaming for Apache Kafka (Amazon MSK), AWS Glue (DynamicFrame), Amazon EMR, AWS Step Functions, Amazon MWAA, AWS DMS (CDC), Apache Parquet

#### Domain 2: データストア管理 (26%)
- **出題の狙い**: コスト、レイテンシ、クエリパターンに応じた最適なストレージサービスを選定し、カタログ化、データライフサイクル管理、およびスキーマ進化（モデリング）を設計する能力を検証します。
- **主要タスク**:
  - Task 2.1: データストアの選択（Redshift、EMR、Lake Formation、RDS、DynamoDB、MemoryDB、OpenSearch、ベクトルインデックス [HNSW, IVF]、Apache Iceberg、Redshift フェデレーテッドクエリ）
  - Task 2.2: データカタログシステムの理解（AWS Glue Data Catalog、クローラー、パーティション同期、Apache Hive メタストア）
  - Task 2.3: データのライフサイクルの管理（S3 ライフサイクルポリシー、S3 バージョニング、DynamoDB TTL、Redshift COPY / UNLOAD、データ消去要件）
  - Task 2.4: データモデルとスキーマの進化の設計（Redshift スター/スノーフレークスキーマ、ソートキー・分散キー、DynamoDB シングルテーブル設計、AWS SCT、データリネージュ）
- **重要キーワード**: Amazon S3 (Storage Classes), Amazon Redshift (RA3, Spectrum, Federated Query), Apache Iceberg, AWS Glue Data Catalog, DynamoDB TTL, Partitioning & Compression (Snappy/Parquet), Vector Index (HNSW/IVF)

#### Domain 3: データ運用とサポート (22%)
- **出題の狙い**: データ処理の自動化とアドホック分析を両立し、分散ログ・メトリクスを用いたパイプライン監視、トラブルシューティング、およびデータ品質検証を確実に実施する能力を検証します。
- **主要タスク**:
  - Task 3.1: AWS サービスを使用したデータ処理の自動化（Step Functions、MWAA、Glue ジョブ、Lambda、EventBridge スケジューラ）
  - Task 3.2: AWS サービスを使用したデータ分析（Amazon Athena、QuickSight、Glue DataBrew、Athena for Apache Spark、サーバーレス vs プロビジョンド比較）
  - Task 3.3: データパイプラインの保守とモニタリング（CloudWatch Logs Insights、CloudTrail API 追跡、EMR / Glue デバッグ、SNS アラート）
  - Task 3.4: データ品質の確保（AWS Glue Data Quality、品質ルールの自動定義、DataBrew プロファイリング、データスキュー対策）
- **重要キーワード**: Amazon Athena, AWS Glue Data Quality, AWS Glue DataBrew, Amazon QuickSight, CloudWatch Logs Insights, AWS CloudTrail, Data Skew (データスキュー), Salting (ソルト付与)

#### Domain 4: データセキュリティとガバナンス (18%)
- **出題の狙い**: 最小権限原則に基づく IAM 設計、Lake Formation による詳細アクセス制御、KMS エンベロープ暗号化、PII マスキング、クロスアカウントデータ共有、および監査ログ記録を実装する能力を検証します。
- **主要タスク**:
  - Task 4.1: 認証メカニズムの適用（VPC セキュリティグループ、IAM ロール、Secrets Manager 認証情報自動ローテーション、PrivateLink）
  - Task 4.2: 認可メカニズムの適用（カスタム IAM ポリシー、AWS Lake Formation 列・行レベル制御、Redshift ロール・オブジェクト権限）
  - Task 4.3: データ暗号化とマスキングの実行（AWS KMS CMK、エンベロープ暗号化、転送時暗号化 [TLS]、クロスアカウント暗号化、データマスキング・トークン化）
  - Task 4.4: 監査用のログの準備（AWS CloudTrail、CloudTrail Lake による SQL クエリ、CloudWatch Logs 保存、EMR/Athena ログ統合）
  - Task 4.5: データプライバシーとガバナンスの理解（Amazon Redshift データ共有、Amazon Macie PII 検出、AWS Config コンプライアンス、データ主権・リージョン制限）
- **重要キーワード**: AWS Lake Formation (LF-TBAC), AWS KMS, Customer Managed Keys (CMK), Envelope Encryption, AWS Secrets Manager, Amazon Macie, Amazon Redshift Data Sharing, AWS CloudTrail Lake, AWS Config

---
