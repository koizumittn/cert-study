# AWS Certified Solutions Architect - Professional (SAP-C02) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Solutions Architect - Professional
- **試験コード**: SAP-C02
- **公式試験ガイド**: [AWS Certified Solutions Architect - Professional (SAP-C02) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/solutions-architect-professional-02/solutions-architect-professional-02.html)
- **最終更新日**: 2026-10-06

---

## 1. 試験の概要と基本スペック

AWS Certified Solutions Architect - Professional は、組織規模の複雑な要件を評価し、AWSサービス群を戦略的に統合して、可用性、耐障害性、パフォーマンス、セキュリティ、コスト効率を極限まで最適化したソリューションをエンドツーエンドで設計・主導する能力を検証する試験です。

- **試験時間**: 180 分
- **出題問題数**: 75 問（採点対象: 65 問 / 未採点テスト設問: 10 問）
- **出題形式**: 択一選択問題（4肢中1つ選択）、複数選択問題（5肢以上中2つ以上選択）
- **合格基準点**: 100〜1,000 点のスケールドスコアで 750 点以上
- **前提知識**: AWS 上での大規模クラウドソリューション設計・実装・運用における 2 年以上の実務経験、および AWS Certified Solutions Architect - Associate (SAA) 相当の知識が強く推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | ドメイン名 / 出題分野 | 出題比率 | 主要対象サービス・ツール |
| :--- | :--- | :--- | :--- |
| **Domain 1** | 複雑な組織に対応するソリューションの設計 | 26% | AWS Organizations, AWS Control Tower, IAM Identity Center, SCP, AWS Transit Gateway, AWS Direct Connect, Route 53 Resolver, AWS Network Firewall, AWS RAM, AWS Security Hub, Amazon GuardDuty, AWS Cost Categories |
| **Domain 2** | 新しいソリューションのための設計 | 29% | Route 53 ARC, Amazon Aurora Global Database, DynamoDB Global Tables, S3 Multi-Region Access Points, AWS Step Functions, Amazon EventBridge, AWS CodePipeline, CodeDeploy, Elastic Load Balancing, AWS WAF, AWS KMS |
| **Domain 3** | 既存のソリューションの継続的な改善 | 25% | AWS Compute Optimizer, Amazon DevOps Guru, AWS X-Ray, Amazon CloudWatch Synthetics, AWS Config, Auto Scaling 予測スケーリング, Amazon OpenSearch Service, ElastiCache, S3 Intelligent-Tiering, Savings Plans |
| **Domain 4** | ワークロードの移行とモダナイゼーションの加速 | 20% | AWS Application Migration Service (MGN), AWS Database Migration Service (DMS), AWS Schema Conversion Tool (SCT), AWS DataSync, AWS Snowball Edge, AWS Transfer Family, AWS App2Container, Amazon EKS, AWS Lambda |

---

## 3. ドメイン別タスクおよび学習ロードマップ

#### Domain 1: 複雑な組織に対応するソリューションの設計 (26%)
- **出題の狙い**: エンタープライズ規模のマルチアカウント構造、集中型ハイブリッドネットワーク、セキュリティ境界の集中管理、および組織横断のコスト配分戦略を包括的に設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: ネットワーク接続戦略の設計（AWS Transit Gateway, Direct Connect, DX Gateway, Route 53 Resolver, 集中型 Egress/Ingress VPC）
  - Task 1.2: セキュリティコントロールの規定（AWS Organizations SCP, サービスリンクロール, AWS IAM Identity Center, AWS KMS クロスアカウントキー共有, AWS RAM）
  - Task 1.3: 信頼性と耐障害性に優れたアーキテクチャの設計（マルチアカウント障害分離、集中ロギング、AWS Backup クロスアカウント・クロスリージョン保護）
  - Task 1.4: マルチアカウント AWS 環境の設計（AWS Control Tower ガードレール、OU 階層設計、アカウント発行ファクトリー (AFT)）
  - Task 1.5: コスト最適化と可視化戦略の決定（AWS Cost Categories, AWS Budgets, コスト配分タグの一元統制、Savings Plans 共有と除外設定）
- **重要キーワード**: AWS Organizations, SCP (Service Control Policies), AWS Control Tower, AWS Transit Gateway, Direct Connect Gateway, Route 53 Resolver Rules / Outbound Endpoints, AWS RAM (Resource Access Manager), 集中型 Egress 検査 VPC, Gateway Load Balancer (GWLB), AWS Network Firewall, 集中ログアカウント

#### Domain 2: 新しいソリューションのための設計 (29%)
- **出題の狙い**: 新規ビジネス要件に基づき、マルチリージョン規模の耐障害性・ディザスタリカバリ、ダウンタイムゼロのデプロイパイプライン、セキュアなデータ保護、極低レイテンシのスケーラブルアーキテクチャをゼロベースで設計する能力を検証します。
- **主要タスク**:
  - Task 2.1: ビジネス要件を満たすデプロイ戦略の設計（Blue/Green デプロイ、カナリアデプロイ、AWS CodePipeline, AWS CodeDeploy, AWS CloudFormation StackSets）
  - Task 2.2: 事業継続性 (BCP) を確保するソリューションの設計（Route 53 ARC, Aurora Global Database, DynamoDB グローバルテーブル, S3 MRAP, アクティブ/アクティブ vs アクティブ/パッシブ DR）
  - Task 2.3: 要件に基づいたセキュリティコントロールの決定（AWS KMS レプリケーション, AWS Secrets Manager クロスリージョン同期, WAF レートベースルール, Cognito フェデレーション）
  - Task 2.4: 信頼性要件を満たす戦略の策定（SQS/SNS ファンアウト, EventBridge イベントバス, Step Functions 分散マップ, 回復力パターン）
  - Task 2.5: パフォーマンス目標を満たすソリューションの設計（CloudFront + Lambda@Edge / CloudFront Functions, Global Accelerator, ElastiCache クラスターモード, EFS / FSx）
  - Task 2.6: コスト最適化戦略の決定（サーバーレスファースト設計、Graviton プロセッサの採用、DynamoDB オンデマンド vs プロビジョンド選定）
- **重要キーワード**: Route 53 ARC (Application Recovery Controller), Amazon Aurora Global Database, DynamoDB Global Tables, S3 Multi-Region Access Points (MRAP), AWS CodeDeploy (Linear / Canary), CloudFormation StackSets, AWS Step Functions Distributed Map, Lambda@Edge vs CloudFront Functions, AWS Global Accelerator

#### Domain 3: 既存のソリューションの継続的な改善 (25%)
- **出題の狙い**: 稼働中システムのオブザーバビリティ、ボトルネック解消、セキュリティポスチャ強化、自動修復、およびプロアクティブなコスト適正化を推進する能力を検証します。
- **主要タスク**:
  - Task 3.1: 全体的な運用上の優秀性を高めるための戦略作成（Amazon DevOps Guru, CloudWatch Synthetics Canaries, EventBridge + Systems Manager オートメーションによる自律修復）
  - Task 3.2: セキュリティを向上させるための戦略決定（AWS Security Hub 検出結果の自動修復, Amazon GuardDuty, Amazon Inspector v2, IAM Access Analyzer, AWS Config ルール）
  - Task 3.3: パフォーマンスを改善するための戦略決定（AWS Compute Optimizer, X-Ray による分散トレーシング, RDS Performance Insights, ElastiCache によるリードキャッシュオフロード）
  - Task 3.4: 信頼性を向上させるための戦略決定（Auto Scaling 予測スケーリング, Route 53 ヘルスチェック最適化, 既存 DB の Multi-AZ / リードレプリカ昇格戦略）
  - Task 3.5: コスト最適化の機会の特定（S3 Intelligent-Tiering, 未使用 EBS ボリューム/古いスナップショット検出, Compute Savings Plans 最適化）
- **重要キーワード**: Amazon DevOps Guru, CloudWatch Synthetics, AWS Systems Manager Automation, AWS Security Hub, Amazon GuardDuty, AWS Config Conformance Packs, IAM Access Analyzer, AWS Compute Optimizer, AWS X-Ray, Auto Scaling Predictive Scaling, S3 Intelligent-Tiering

#### Domain 4: ワークロードの移行とモダナイゼーションの加速 (20%)
- **出題の狙い**: オンプレミス環境からの大規模データ移行、サーバー・DB のリホスト/リプラットフォーム、そしてクラウドネイティブなマイクロサービスへのモダナイゼーション（7R戦略）を計画・実行する能力を検証します。
- **主要タスク**:
  - Task 4.1: 移行可能な既存ワークロードとプロセスの選択（AWS Application Discovery Service, AWS Migration Hub, 7R (Rehost, Replatform, Refactor, Repurchase, Retain, Retire, Relocate) アセスメント）
  - Task 4.2: 既存ワークロードに対する最適な移行アプローチの決定（AWS Application Migration Service (MGN), AWS Database Migration Service (DMS), AWS SCT, AWS DataSync, Snow ファミリー）
  - Task 4.3: 既存ワークロードの新しいアーキテクチャの決定（VMware Cloud on AWS, オンプレミス Active Directory と AWS の連携, AWS Transfer Family）
  - Task 4.4: モダナイゼーションと機能強化の機会の特定（Strangler Fig パターンによる段階的モダナイゼーション, AWS App2Container, Amazon EKS / ECS 移行, イベント駆動型アーキテクチャへのリファクタリング）
- **重要キーワード**: AWS MGN (Application Migration Service), AWS DMS (Database Migration Service), AWS SCT (Schema Conversion Tool), AWS DataSync, AWS Snowball Edge / Snowcone, Strangler Fig (絞め殺し) パターン, 7R 移行戦略, AWS App2Container, VMware Cloud on AWS, AWS Transfer Family

---
