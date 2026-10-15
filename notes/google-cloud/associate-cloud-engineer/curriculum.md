# Google Cloud Certified - Associate Cloud Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Associate Cloud Engineer (ACE)
- **公式試験ガイド**: [Associate Cloud Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/associate_cloud_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式学習パス**: [Google Skills - Associate Cloud Engineer Certification](https://www.skills.google/paths/11?hl=ja)
- **最終更新日**: 2026-10-12

---

## 1. 試験の概要と基本スペック

Associate Cloud Engineer は、目標となるパフォーマンス指標を確実に達成するために、アプリケーション、サービス、インフラストラクチャのデプロイと保護、複数プロジェクトの運用のモニタリング、エンタープライズソリューションの管理を行う能力を評価・認定するアソシエイトレベルの資格です。

パブリッククラウドまたはオンプレミスのソリューションの実務経験があり、AIツール（Gemini Cloud Assist や Gemini CLI 等）を活用しながら一般的なプラットフォームベースのタスクを遂行し、Google Cloud 上で Google マネージドサービスまたはセルフマネージドサービスを利用するデプロイ済みソリューションの管理とスケーリングを担うエンジニアを対象としています。

- **試験時間**: 120 分
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題、複数選択問題
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: Google Cloud コンソールおよびコマンドライン インターフェース（gcloud CLI, gsutil, bq, kubectl）を用いた 6 か月以上の実務経験、またはクラウド全般に関する 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全4セクションで構成されており、ソリューションの計画・実装（セクション2）と正常な運用（セクション3）がそれぞれ最大30%と大きな割合を占めます。また、環境設定（セクション1）とアクセス・セキュリティ（セクション4）がそれぞれ最大20%を占め、設計から実務的なCLI運用・保守・権限統制に至る一貫したエンジニアリング能力が問われます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | クラウド ソリューション環境の設定 | 20% 以下 | リソース階層（組織/フォルダ/プロジェクト）、組織ポリシー、IAM基礎、Cloud Identity、API有効化、割り当て管理、ロケーション（リージョン/ゾーン）、Cloud Asset Inventory、Workforce Identity 連携、Cloud Billing（請求先アカウント、予算アラート、BigQueryエクスポート） | 完了 |
| **Section 2** | クラウド ソリューションの計画と実装 | 30% 以下 | Compute Engine、GKE（Autopilot/Standard/Private）、Cloud Run、Cloud Run functions、Gemini Enterprise Agent Platform、Persistent Disk / Hyperdisk、MIG、OS Login、VM Manager、Spot VM、GPU/TPU、Cloud SQL、Spanner、Bigtable、Firestore、AlloyDB、Cloud Storage、Filestore、VPC（共有VPC/ピアリング）、Cloud NGFW、Cloud VPN、Cloud Interconnect、Cloud Load Balancing、Network Service Tiers、Terraform、Config Connector、Gemini CLI | 完了 |
| **Section 3** | クラウド ソリューションの正常な運用 | 30% 以下 | Compute Engine管理（SSH/OS Login、スナップショット/イメージ）、GKE管理（kubectl、ノードプール、HPA/VPA、Autopilotリソース）、Cloud Run管理（リビジョンデプロイ、トラフィック分割、オートスケール）、Gemini Agent Platform ランタイム、Cloud Workstations、ストレージ管理（ライフサイクル、CMEK）、DB運用（クエリ、バックアップ/復元、Database Center）、VPCネットワーク管理（CIDR拡張、静的IP、静的ルート、Cloud DNS、Cloud NAT）、Cloud Monitoring（アラート、カスタム指標、Prometheus）、Cloud Logging（ログルーター、ログシンク、ログ分析）、Cloud Trace、Profiler、Ops エージェント、Active Assist | 完了 |
| **Section 4** | アクセスとセキュリティの構成 | 20% 以下 | IAMポリシー管理（基本/事前定義/カスタムロール、権限借用）、リソース階層のポリシー継承、サービス アカウント（Google管理/ユーザー管理、最小権限、キーレス短時間トークン）、GKE Workload Identity、Workforce Identity 連携 | 完了 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: クラウド ソリューション環境の設定（20% 以下）
- **出題の狙い**: エンタープライズ規模の Google Cloud 環境を安全かつ統制された状態で立ち上げるための基盤設定能力を検証します。リソース階層の設計、組織ポリシーの適用、Cloud Identity による ID 管理、ロケーション設計、および正確な課金管理・コストアラート設定の知識を評価します。
- **主要タスク**:
  - Task 1.1: クラウド プロジェクトとアカウントの設定（リソース階層の作成、組織ポリシー適用、IAM ロール付与、Cloud Identity ユーザー/グループ管理、API 有効化、Observability プロビジョニング、割り当ての評価と申請、スタンドアロン組織、クラウド ネットワーキング、リージョン/ゾーン可用性検証、Cloud Asset Inventory と Gemini Cloud Assist による分析、Workforce Identity 連携）
  - Task 1.2: 課金構成の管理（請求先アカウント作成、プロジェクトリンク、予算とアラートの設定、BigQuery への課金データエクスポート設定）
- **重要キーワード**: Resource Hierarchy (Organization, Folder, Project), Organization Policies, Cloud Identity, Quotas & Limits, Multi-region / Dual-region / Regional, Cloud Asset Inventory, Workforce Identity Federation, Cloud Billing Account, Billing Budgets & Alerts, Billing Export to BigQuery

#### Section 2: クラウド ソリューションの計画と実装（30% 以下）
- **出題の狙い**: ワークロード要件（スループット、ステートレス/ステートフル、可用性、コスト）に応じた最適なコンピュート、ストレージ、データベース、ネットワークリソースの選定および初期構築能力を検証します。また、Terraform などの IaC や AI 支援ツールを活用した現代的なプロビジョニング実践を評価します。
- **主要タスク**:
  - Task 2.1: コンピューティング リソースの計画と実装（Compute Engine, GKE [Autopilot/Standard/Private], Cloud Run, Cloud Run functions, Gemini Enterprise Agent Platform ランタイム選定、起動オプション、Persistent Disk / Hyperdisk、MIG、OS Login、VM Manager、Spot VM、kubectl、イベントドリブンアーキテクチャ [Eventarc, Pub/Sub]、GPU/TPU 選定）
  - Task 2.2: ストレージとデータ ソリューションの計画と実装（Cloud SQL, BigQuery, Firestore, Spanner, Bigtable, AlloyDB, Dataflow, Pub/Sub, Kafka, Memorystore、Cloud Storage [Standard/Nearline/Coldline/Archive]、Filestore, NetApp Volumes, Managed Lustre、データロード手法 [gsutil/gcloud storage, Storage Transfer Service]、マルチリージョン冗長性）
  - Task 2.3: ネットワーキング リソースの計画と実装（カスタム VPC、共有 VPC、VPC ピアリング、ファイアウォール ルール / Cloud NGFW [セキュアタグ/サービスアカウント]、Cloud VPN、Cloud Interconnect、Cloud Load Balancing [グローバル外部ALB, ネットワークLB等]、Network Service Tiers [Premium vs Standard]）
  - Task 2.4: ツールを活用したリソースの計画と実装（IaC [Terraform, Config Connector, Fabric FAST, Helm]、AI ツール [Gemini CLI, Google Antigravity, Gemini Cloud Assist, App Design Center]）
- **重要キーワード**: Compute Engine, GKE Autopilot, Cloud Run, Cloud Run functions, Hyperdisk, Managed Instance Groups (MIG), Spot VM, TPU vs GPU, Cloud Storage Classes, Storage Transfer Service, Cloud SQL vs Spanner vs Bigtable, Shared VPC vs VPC Peering, Cloud NGFW, Cloud Load Balancing (ALB / NLB), Network Service Tiers, Terraform, Config Connector

#### Section 3: クラウド ソリューションの正常な運用（30% 以下）
- **出題の狙い**: 稼働中ソリューションの継続的な健全性維持、スケーリング、更新、トラブルシューティング、バックアップ/リカバリ、およびオブザーバビリティ運用の実務能力を検証します。CLI（gcloud, kubectl）を用いた具体的な操作手順や診断思考が強く問われます。
- **主要タスク**:
  - Task 3.1: コンピューティング リソースの管理（SSH/OS Login 接続、Compute Engine スナップショット/カスタムイメージ管理、GKE クラスタ運用 [kubectl, ノードプール管理, HPA/VPA, Autopilot リソースリクエスト]、Cloud Run リビジョン更新/トラフィック分割 [Canary]/オートスケール、GPU/TPU アタッチ、Agent Platform ランタイム運用、Cloud Workstations）
  - Task 3.2: ストレージとデータ ソリューションの管理（Cloud Storage オブジェクト保護/ライフサイクルルール、各種DBクエリ実行、費用見積もり、DBバックアップ/復元、Dataflow/BigQuery ジョブ監視、Database Center、CMEK 暗号化）
  - Task 3.3: ネットワーキング リソースの管理（サブネット IPv4 CIDR 拡張、静的外部/内部 IP 予約、カスタム静的ルート追加、Cloud DNS、Cloud NAT、Cloud NGFW ポリシー管理）
  - Task 3.4: モニタリングとロギング（Cloud Monitoring アラート作成、カスタム指標、監査ログ構成 [VPC フローログ/ファイアウォールログ]、外部/BigQuery ログエクスポート [ログルーター/ログシンク]、Cloud Logging フィルタリング、Cloud Trace / Profiler / Query Insights、Ops エージェント、Managed Service for Prometheus、Gemini Cloud Assist / Active Assist）
- **重要キーワード**: gcloud compute / gcloud container / gcloud run, kubectl, Snapshot Lifecycle, HPA / VPA, Traffic Splitting, Lifecycle Management, Cloud KMS (CMEK), Subnet Expansion, Cloud NAT, Cloud DNS, Cloud Monitoring / Cloud Logging, Log Router & Sinks, Ops Agent, Managed Service for Prometheus, Active Assist (Recommender)

#### Section 4: アクセスとセキュリティの構成（20% 以下）
- **出題の狙い**: 最小権限の原則（PoLP）に基づくアクセス制御、組織階層全体の IAM ガバナンス、サービス アカウントのセキュアなライフサイクル管理、およびキーレス認証（Workload Identity / Workforce Identity）の設計・実装能力を検証します。
- **主要タスク**:
  - Task 4.1: IAM の管理（IAM ポリシーの表示と作成、組織階層でのロール付与とポリシー継承、基本/事前定義/カスタムロールの管理）
  - Task 4.2: サービス アカウントの管理（Google 管理 vs ユーザー管理サービス アカウント、最小権限適用、リソースへの紐付け、権限借用 [Service Account Token Creator]、短期有効認証情報、GKE Workload Identity、Workforce Identity 連携）
- **重要キーワード**: Principle of Least Privilege, Basic vs Predefined vs Custom Roles, Policy Inheritance, Service Accounts, Service Account Impersonation, Short-lived Credentials, GKE Workload Identity, Workforce Identity Federation
