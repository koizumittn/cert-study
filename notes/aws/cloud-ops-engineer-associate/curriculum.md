# AWS Certified CloudOps Engineer - Associate (SOA-C03) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified CloudOps Engineer - Associate
- **試験コード**: SOA-C03
- **公式試験ガイド**: [AWS Certified CloudOps Engineer - Associate (SOA-C03) Exam Guide](https://docs.aws.amazon.com/aws-certification/latest/sysops-administrator-associate-03/sysops-administrator-associate-03.md)
- **最終更新日**: 2026-10-04

---

## 1. 試験の概要と基本スペック

AWS Certified CloudOps Engineer - Associate は、AWS 上でワークロードを安全かつ効率的にデプロイ、管理、運用し、AWS Well-Architected Framework に準拠した高可用・耐障害性環境を維持する能力を認定するプロフェッショナル認定資格です。

- **試験時間**: 130 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（Multiple Choice: 4肢中1つ選択）、複数選択問題（Multiple Response: 5肢以上中2つ以上選択）。※旧形式で一時期導入されていた「実技試験（Exam Labs）」は含まれません。
- **合格基準点**: 100〜1,000 点のスケールドスコアで 720 点以上
- **前提知識**: AWS 上でのデプロイ、運用、ネットワーキング、セキュリティに関する 1 年程度の実務経験、またはシステム管理者等の運用ロールでの 1 年以上の経験が推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | ドメイン名 / 出題分野 | 出題比率 | 主要対象サービス・ツール |
| :--- | :--- | :--- | :--- |
| **Domain 1** | 監視、ロギング、分析、修復、およびパフォーマンス最適化 | 22% | Amazon CloudWatch, CloudWatch Agent, CloudTrail, EventBridge, Systems Manager Automation, EBS, S3, RDS |
| **Domain 2** | 信頼性とビジネス継続性 | 22% | AWS Auto Scaling, Elastic Load Balancing, Route 53, Multi-AZ, AWS Backup, DR 4大戦略 |
| **Domain 3** | デプロイ、プロビジョニング、およびオートメーション | 22% | AWS CloudFormation, AWS CDK, StackSets, EC2 Image Builder, Systems Manager (Patch / Run Command) |
| **Domain 4** | セキュリティとコンプライアンス | 16% | AWS Organizations, SCP, AWS Config, IAM Identity Center, AWS KMS, Secrets Manager, GuardDuty, Security Hub |
| **Domain 5** | ネットワーキングとコンテンツ配信 | 18% | Amazon VPC, VPC エンドポイント, AWS PrivateLink, Route 53 Resolver DNS Firewall, AWS Network Firewall, CloudFront |

---

## 3. ドメイン別タスクおよび学習ロードマップ

#### Domain 1: 監視、ロギング、分析、修復、およびパフォーマンス最適化 (22%)
- **出題の狙い**: システム全体の可観測性を確立し、アラートの誤検知を抑えつつ EventBridge や Systems Manager による自動修復パイプラインを構築する能力、ならびにコンピュート・ストレージ・DBのパフォーマンスとコストを最適化する能力を検証します。
- **主要タスク**:
  - Task 1.1: AWS 監視・ロギングサービスを使用したメトリクス、アラーム、フィルターの実装（CloudWatch Agent、複合アラーム、クロスアカウントダッシュボード、SNS）
  - Task 1.2: 監視および可用性メトリクスを使用した問題の特定と修復（パフォーマンス分析、EventBridge ルーティング、SSM Automation ランブック）
  - Task 1.3: コンピュート、ストレージ、データベースリソースのパフォーマンス最適化戦略の実装（EBS 最適化、S3 パフォーマンス、EFS/FSx/S3 Files、RDS Performance Insights、EC2 配置グループ）
- **重要キーワード**: CloudWatch Agent, Composite Alarms, Cross-Account Observability, EventBridge Rules, SSM Automation, gp3/io2, S3 Multipart/Transfer Acceleration, Performance Insights, Placement Groups

#### Domain 2: 信頼性とビジネス継続性 (22%)
- **出題の狙い**: 単一障害点を排除した高可用性（HA）環境の維持と、ビジネス目標（RTO / RPO）に応じたディザスタリカバリ（DR）戦略の選定・フェイルオーバー運用の自動化能力を検証します。
- **主要タスク**:
  - Task 2.1: スケーラビリティと伸縮性の実装（コンピュートスケーリング、CloudFront/ElastiCache キャッシング、RDS/DynamoDB スケーリング）
  - Task 2.2: 高可用性と耐障害性環境の実装（ELB ヘルスチェック、Route 53 ヘルスチェック、Multi-AZ 構成）
  - Task 2.3: バックアップと復元戦略の実装（AWS Backup による一元管理、PITR、ストレージバージョニング、DR 4大戦略の運用）
- **重要キーワード**: Auto Scaling Groups, Elastic Load Balancing, Route 53 Health Checks, RDS Multi-AZ, AWS Backup Vault, Point-in-time Recovery (PITR), Backup & Restore, Pilot Light, Warm Standby, Multi-Region Active/Active

#### Domain 3: デプロイ、プロビジョニング、およびオートメーション (22%)
- **出題の狙い**: クラウドインフラをコード（IaC）として宣言的・プログラム的に管理し、マルチアカウントへの一括展開、デプロイ障害の安全なロールバック、および OS パッチ適用の自動化を統制する能力を検証します。
- **主要タスク**:
  - Task 3.1: クラウドリソースのプロビジョニングと保守（EC2 Image Builder、CloudFormation、AWS CDK、デプロイ障害修復、StackSets、Terraform）
  - Task 3.2: 既存リソースの管理の自動化（Systems Manager Patch Manager / Run Command / State Manager、イベント駆動自動化、AWS DevOps Agent）
- **重要キーワード**: AWS CloudFormation, AWS CDK, StackSets, EC2 Image Builder, Drift Detection, Rollback Configuration, SSM Patch Manager, Maintenance Windows, Event-Driven Automation

#### Domain 4: セキュリティとコンプライアンス (16%)
- **出題の狙い**: 組織全体へのセキュリティポリシーの強制、継続的なコンプライアンス監査、暗号化キーおよび機密情報の安全なライフサイクル管理を設計・運用する能力を検証します。
- **主要タスク**:
  - Task 4.1: セキュリティおよびコンプライアンスツールとポリシーの実装と管理（IAM 機能、アクセス監査・シミュレーター、AWS Organizations / SCP、AWS Config Conformance Packs）
  - Task 4.2: データおよびインフラストラクチャを保護するための戦略の実装（データ分類、KMS 保存時暗号化、ACM 転送時暗号化、Secrets Manager、GuardDuty / Security Hub）
- **重要キーワード**: Service Control Policies (SCPs), AWS Config Conformance Packs, IAM Identity Center, AWS KMS Key Policies, AWS Secrets Manager Rotation, Amazon GuardDuty, AWS Security Hub

#### Domain 5: ネットワーキングとコンテンツ配信 (18%)
- **出題の狙い**: 安全なハイブリッド・プライベートネットワークの構成、多層ネットワーク防御（WAF、Network Firewall、DNS Firewall）、およびネットワーク障害時のログ分析・トラブルシューティング能力を検証します。
- **主要タスク**:
  - Task 5.1: ネットワーキング機能と接続性の実装と最適化（VPC 構成要素、Egress-only IGW、PrivateLink / VPC エンドポイント、ネットワーク保護サービス監査）
  - Task 5.2: ドメイン、DNS サービス、コンテンツ配信の構成（Route 53 Resolver、ルーティングポリシー、クエリログ、CloudFront、Global Accelerator）
  - Task 5.3: ネットワーク接続の問題のトラブルシューティング（VPC 設定障害、VPC フローログ / 各種アクセスログ分析、CloudFront キャッシュ修復、CloudWatch Network Monitor）
- **重要キーワード**: VPC Endpoints (Gateway vs Interface), AWS PrivateLink, Route 53 Resolver DNS Firewall, AWS Network Firewall, Egress-Only Internet Gateway, VPC Flow Logs, CloudWatch Network Monitor

---
