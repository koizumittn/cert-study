# Google Cloud Certified - Professional Cloud Database Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Cloud Database Engineer (PCDBE)
- **公式試験ガイド**: [Professional Cloud Database Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_cloud_database_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Cloud Database Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/cloud-database-engineer?hl=ja)
- **公式学習パス**: [Google Skills - Database Engineer Learning Path](https://www.skills.google/)
- **最終更新日**: 2026-10-13

---

## 1. 試験の概要と基本スペック

Professional Cloud Database Engineer は、ビジネス要件や技術要件をスケーラブルで復元力が高く、費用効果の高いクラウドデータベースソリューションに変換し、Google Cloud 上でデータベースを設計、作成、管理、移行、トラブルシューティングできる高度な実務能力を客観的に評価・認定するプロフェッショナル資格です。

リレーショナルデータベース（Cloud SQL, AlloyDB for PostgreSQL, Spanner）および NoSQL / 分散データベース（Bigtable, Firestore, Memorystore）、さらにはベクトル検索や生成 AI ワークロードを支えるデータベース技術を網羅し、高可用性（HA）、障害復旧（DR）、クエリ最適化、ゼロダウンタイム移行、セキュリティ、パフォーマンスチューニングに関する深いエンジニアリング能力が問われます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: データベース管理・設計に関する 5 年以上の実務経験、および Google Cloud 上でのデータベース構築・運用に関する 2 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 4 セクションで構成されています。データベースソリューションの設計（約 32%）と管理・運用（約 25%）で全体の半数以上を占め、さらにデータ移行（約 23%）とスケーラブルな高可用性デプロイ（約 20%）が問われます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | 革新的でスケーラブルな高可用性クラウド データベース ソリューションを設計する | 約 32% | Cloud SQL (MySQL / PostgreSQL / SQL Server), AlloyDB for PostgreSQL, Cloud Spanner, Cloud Bigtable, Firestore, Memorystore, ベアメタル / GCE セルフマネージド, ベクトル検索 (pgvector, Spanner Vector Search), プライベート接続 (PSC / VPC Peering), セッションプーラー (PgBouncer), CMEK / IAM, 監査ログ |
| **Section 2** | 複数のデータベース技術にまたがるソリューションを管理する | 約 25% | IAM データベース認証, Cloud Monitoring / Logging, Query Insights, Key Visualizer, データベースロック / スロークエリ分析, 自動バックアップ / オンデマンドバックアップ, PITR (Point-in-Time Recovery), RTO / RPO, インポート / エクスポート, スケールアップ / スケールアウト, クエリ最適化 (EXPLAIN ANALYZE), Cloud Scheduler 自動化, メジャー / マイナーアップグレード |
| **Section 3** | データ ソリューションを移行する | 約 23% | Database Migration Service (DMS), Datastream, Spanner Migration Tool (SMT), 移行戦略 (ダウンタイム最小限 / ニアゼロ / オフライン), CDC (Change Data Capture), リバースレプリケーション / 切り戻し計画, DDL / DML 変換, 外部 DB 移行 (オンプレミス, AWS RDS, 異種 DB 移行) |
| **Section 4** | Google Cloud にスケーラブルな高可用性データベースをデプロイする | 約 20% | 高可用性 (HA) 構成 (Cloud SQL Regional HA, AlloyDB Regional HA, Spanner Multi-Region, Bigtable Multi-Cluster), フェイルオーバーテスト, リードレプリカ / クロスリージョンレプリカ, Terraform / IaC プロビジョニング自動化, HA / DR モニタリング |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: 革新的でスケーラブルな高可用性クラウド データベース ソリューションを設計する（約 32%）
- **出題の狙い**: ビジネス要件（レイテンシ、スループット、整合性モデル、予算、コンプライアンス）に基づき、最適な Google Cloud データベースサービスを選択し、容量計画、接続トポロジ、暗号化、セキュリティ、および生成 AI 統合を含むアーキテクチャを設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: 関連する変数を分析して、データベースの容量と使用計画を実行する（ワークロード指標と将来予測に基づくサイジング、マシンタイプやストレージ [SSD / HDD / Hyperdisk] のコストと性能のトレードオフ評価、コンピューティングとストレージの独立調整 [Spanner PU / AlloyDB ストレージ自動拡張]）
  - Task 1.2: 要件に沿って、データベースの高可用性と障害復旧のオプションを評価する（マルチリージョン、リージョン、ゾーンデプロイ戦略のトレードオフ評価、可用性要件に応じたメンテナンス時間枠と通知の定義）
  - Task 1.3: アプリケーションがデータベースに接続する方法を決定する（ネットワーク構成 [Private Service Connect, Private Services Access, Cloud SQL Auth Proxy]、鍵管理 [Cloud KMS / CMEK]、セッションプーラー [PgBouncer, ProxySQL] の選定理由、Cloud Audit Logs による監査ポリシー評価）
  - Task 1.4: Google Cloud で適切なデータベース ソリューションを評価する（マネージド vs 非マネージド [セルフマネージド, ベアメタル, Google マネージド, ネイティブ, パートナー]、SQL vs NoSQL [構造化, 半構造化, 非構造化, ベクトル]、コスト比較分析、依存関係評価、規制・コンプライアンス要件 [HIPAA, PCI-DSS]、組織ポリシーの統制、ハイブリッド / フェデレーション構成、生成 AI・LLM ユースケース [ベクトル埋め込みと類似検索]）
- **重要キーワード**: Cloud SQL, AlloyDB for PostgreSQL, Cloud Spanner, Cloud Bigtable, Firestore, Memorystore, Private Service Connect (PSC), Cloud SQL Auth Proxy, PgBouncer, CMEK, Cloud Audit Logs, pgvector, Spanner Vector Search, Zonal / Regional / Multi-Region Architecture, Maintenance Windows

#### Section 2: 複数のデータベース技術にまたがるソリューションを管理する（約 25%）
- **出題の狙い**: 稼働中の複数データベースシステムにおいて、IAM を用いたセキュアなアクセス制御、パフォーマンス監視、ボトルネック・障害のトラブルシューティング、バックアップ・リカバリ（PITR）、コストとスループットの継続的最適化、および定期保守の自動化を遂行する実務能力を検証します。
- **主要タスク**:
  - Task 2.1: データベースの接続とアクセス管理に関する考慮事項を決定する（IAM ポリシーによる接続制御 [Cloud SQL インスタンス閲覧者/クライアント]、IAM データベース認証とビルトイン認証の管理）
  - Task 2.2: データベースのモニタリングとトラブルシューティングのオプションを構成する（スロークエリ、行ロック/テーブルロック、不足インデックスの特定 [Query Insights, Spanner Key Visualizer]、基本指標 [CPU, RAM, ストレージ, IOPS] の調査、割り当て [Quotas] の監視と引き上げ申請、リソース競合調査、アラートポリシー設定）
  - Task 2.3: データベースのバックアップと復元のソリューションを設計する（スケジュール設定された自動バックアップとオンデマンドバックアップ、インポート/エクスポート構成 [mysqldump, pg_dump, CSV, Avro]、RTO / RPO / PITR の設計、データ保持ポリシーの管理）
  - Task 2.4: Google Cloud でデータベースのコストとパフォーマンスを最適化する（スケールアップ vs スケールアウト、ワークロードに応じたインスタンススケーリング [Spanner PU, AlloyDB リードプール]、レプリケーション戦略、確約利用割引 [CUD] 等によるコスト最適化、クエリ実行計画分析 [EXPLAIN ANALYZE] によるクエリ最適化）
  - Task 2.5: 一般的なデータベース タスクを自動化する（インデックス再構築・統計情報更新・VACUUM などのメンテナンス自動化、Cloud Scheduler + Workflows によるエクスポートのスケジュール化、メジャー / マイナーバージョンアップグレード管理、SLA / SLO モニタリング）
- **重要キーワード**: IAM Database Authentication, Query Insights, Key Visualizer, Lock Contention, Cloud Monitoring Alerts, Automated Backups, Point-in-Time Recovery (PITR), RTO vs RPO, Import / Export, Scale-up vs Scale-out, Spanner Processing Units (PU), AlloyDB Read Pool, EXPLAIN ANALYZE, Vacuum / Index Maintenance, Committed Use Discounts (CUD)

#### Section 3: データ ソリューションを移行する（約 23%）
- **出題の狙い**: オンプレミスや他社クラウドで稼働するデータベースから Google Cloud のマネージドデータベースへ、ダウンタイムを最小限に抑えつつ安全に移行するための移行計画策定、CDC レプリケーション、異種間スキーマ変換、および切り戻し（フォールバック）を確実に実行する能力を検証します。
- **主要タスク**:
  - Task 3.1: データの移行とレプリケーションを設計、実装する（移行戦略 [ニアゼロダウンタイム, メンテナンスウィンドウ移行, オフライン一括移行]、Google Cloud から移行元へのリバースレプリケーションによるフォールバック計画、スキーマ変換 [DDL / DML 変換, Spanner Migration Tool]、適切な移行ツールの特定 [Database Migration Service (DMS), Datastream, Striim 等]）
- **重要キーワード**: Database Migration Service (DMS), Datastream, Change Data Capture (CDC), Continuous Replication, Reverse Replication, Fallback Strategy, Spanner Migration Tool (SMT), Homogeneous vs Heterogeneous Migration, pg_dump / mysqldump, Minimal Downtime Migration

#### Section 4: Google Cloud にスケーラブルな高可用性データベースをデプロイする（約 20%）
- **出題の狙い**: エンタープライズレベルのサービス可用性（99.99% 以上）を担保するため、リージョン内・リージョン間の冗長構成を正しくプロビジョニングし、自動フェイルオーバー動作の検証、リードレプリカによる読み取り負荷分散、IaC（Terraform）による構成自動化、および高可用性監視を実装する能力を検証します。
- **主要タスク**:
  - Task 4.1: コンセプトを適用して Google Cloud にスケーラビリティと可用性が高いデータベースを実装する（高可用性ソリューションのプロビジョニング [Cloud SQL Regional HA, AlloyDB Regional HA, Spanner Multi-Region, Bigtable Multi-Cluster]、定期的な HA / DR フェイルオーバーテストの実施、マルチリージョンレプリケーション設定、リードレプリカのデプロイとオートスケール、Terraform 等によるプロビジョニング自動化、高可用性モニタリングの構成）
- **重要キーワード**: Regional HA (Primary & Standby), Multi-Region Spanner, Bigtable Multi-Cluster Replication, Failover Testing, Read Replicas, Cross-Region Read Replicas, Terraform Provisioning, Automated Failover, Availability Monitoring
