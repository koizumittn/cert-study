# AWS Certified Solutions Architect - Associate (SAA-C03) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Solutions Architect - Associate
- **試験コード**: SAA-C03
- **公式試験ガイド**: [AWS Certified Solutions Architect - Associate (SAA-C03) Exam Guide](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html)
- **最終更新日**: 2026-10-04

---

## 1. 試験の概要と基本スペック

AWS Certified Solutions Architect - Associate は、ビジネス要件および技術要件を正確に理解し、AWS の広範なサービス群を組み合わせて最適なクラウドアーキテクチャを設計・提案する能力を認定する資格です。

- **試験時間**: 130 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（4肢中1つ選択）、複数選択問題（5肢以上中2つ以上選択）
- **合格基準点**: 100〜1,000 点のスケールドスコアで 720 点以上
- **前提知識**: AWS 上での分散システム設計・導入・評価に関する 1 年以上の実務経験、またはクラウドアーキテクチャに関する同等の実践的理解が推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | ドメイン名 / 出題分野 | 出題比率 | 主要対象サービス・ツール |
| :--- | :--- | :--- | :--- |
| **Domain 1** | セキュアなアーキテクチャの設計 | 30% | AWS IAM, IAM Identity Center, AWS Organizations (SCP), AWS KMS, AWS Secrets Manager, Systems Manager Parameter Store, Amazon VPC, セキュリティグループ, ネットワークACL, VPC エンドポイント, AWS WAF, AWS Shield, Amazon GuardDuty, AWS CloudTrail |
| **Domain 2** | レジリエントなアーキテクチャの設計 | 26% | Amazon SQS (標準/FIFO), Amazon SNS, Amazon EventBridge, AWS Step Functions, AWS Auto Scaling, Elastic Load Balancing (ALB/NLB), Amazon Route 53, Amazon RDS (Multi-AZ), Amazon Aurora, AWS Backup, DR 4大戦略 |
| **Domain 3** | 高パフォーマンスなアーキテクチャの設計 | 24% | Amazon S3, Amazon EBS (gp3/io2), Amazon EFS, Amazon FSx, Amazon EC2 インスタンスファミリー, EC2 配置グループ, AWS Lambda, Amazon ECS/EKS, Amazon DynamoDB (DAX), Amazon ElastiCache, Amazon CloudFront, AWS Global Accelerator, Amazon Kinesis |
| **Domain 4** | コストを最適化したアーキテクチャの設計 | 20% | S3 ライフサイクルルール, S3 Intelligent-Tiering, AWS Compute Optimizer, Savings Plans, スポットインスタンス, Aurora Serverless v2, DynamoDB オンデマンド, Gateway型 VPC エンドポイント, AWS Cost Explorer, AWS Budgets |

---

## 3. ドメイン別タスクおよび学習ロードマップ

#### Domain 1: セキュアなアーキテクチャの設計 (30%)
- **出題の狙い**: IAM による厳格なアイデンティティ統制、Organizations によるマルチアカウントガバナンス、ネットワーク境界防御、およびデータの保存時・転送時暗号化と監査を多層的に実装する能力を検証します。
- **主要タスク**:
  - Task 1.1: AWS リソースへのセキュアなアクセスを設計する（IAM Identity Center, クロスアカウント AssumeRole, Organizations SCP, 属性ベースアクセス制御 (ABAC)）
  - Task 1.2: セキュアなワークロードとアプリケーションを設計する（VPC サブネット設計, セキュリティグループ, NACL, AWS WAF, Shield, VPC エンドポイント, Secrets Manager, Parameter Store）
  - Task 1.3: 適切なデータセキュリティ管理を判断する（AWS KMS 暗号化キー管理, S3 バケットポリシー, S3 Object Lock, 転送時 TLS 暗号化, CloudTrail, GuardDuty, Macie）
- **重要キーワード**: IAM Identity Center, AssumeRole, Service Control Policies (SCP), Security Groups vs NACLs, VPC Endpoints (Gateway / Interface), AWS WAF, AWS Secrets Manager, KMS (SSE-KMS / SSE-S3), S3 Object Lock, CloudTrail

#### Domain 2: レジリエントなアーキテクチャの設計 (26%)
- **出題の狙い**: システムの単一障害点（SPOF）を排除し、コンポーネント間を疎結合化して自動スケーリングおよびフェイルオーバーを実現する高可用性・耐障害性環境を設計する能力を検証します。
- **主要タスク**:
  - Task 2.1: スケーラブルな疎結合アーキテクチャを設計する（SQS 標準/FIFO, SNS ファンアウト, EventBridge, Step Functions, API Gateway, サーバーレスマイクロサービス）
  - Task 2.2: 高可用性および/または耐障害性のあるアーキテクチャを設計する（Multi-AZ ALB / ASG, RDS Multi-AZ, Aurora レプリカ, Route 53 フェイルオーバー/レイテンシルーティング, DR 4大戦略, AWS Backup, S3 CRR）
- **重要キーワード**: SQS (Standard / FIFO / DLQ), SNS Fanout, EventBridge Event Bus, Step Functions, Multi-AZ Deployments, Auto Scaling Group, Route 53 Health Checks, Disaster Recovery (Backup & Restore, Pilot Light, Warm Standby, Multi-Region Active-Active)

#### Domain 3: 高パフォーマンスなアーキテクチャの設計 (24%)
- **出題の狙い**: ワークロードの計算・ストレージ・データベース・ネットワークの要求仕様に応じ、スループットとレイテンシを極限まで最適化するサービス選定とアーキテクチャパターンを設計する能力を検証します。
- **主要タスク**:
  - Task 3.1: 高パフォーマンスでスケーラブルなストレージソリューションを選択する（S3 プレフィックス最適化, S3 Transfer Acceleration, EBS gp3 / io2 Block Express, EFS, FSx for Lustre / Windows）
  - Task 3.2: 高パフォーマンスで伸縮自在なコンピューティングソリューションを設計する（EC2 インスタンスタイプ選定, クラスター配置グループ, ENA/EFA, Auto Scaling ターゲット追跡, Lambda, Fargate, ECS/EKS）
  - Task 3.3: 高パフォーマンスなデータベースソリューションを選択する（Amazon Aurora リードレプリカ / Global Database, DynamoDB + DAX, ElastiCache Redis / Memcached）
  - Task 3.4: 高パフォーマンスでスケーラブルなネットワークアーキテクチャを選択する（Amazon CloudFront, AWS Global Accelerator, Direct Connect, Transit Gateway）
  - Task 3.5: 高パフォーマンスなデータ取り込みと変換のソリューションを選択する（Amazon Kinesis Data Streams / Data Firehose, AWS Glue, Amazon EMR）
- **重要キーワード**: EBS io2 Block Express, FSx for Lustre, Cluster Placement Groups, Graviton, Aurora Global Database, DynamoDB Accelerator (DAX), ElastiCache, CloudFront OAC, Global Accelerator, Kinesis Data Streams

#### Domain 4: コストを最適化したアーキテクチャの設計 (20%)
- **出題の狙い**: パフォーマンスや信頼性を損なうことなく、ストレージ階層化、コンピュート購入オプション、データベースサイジング、ネットワーク転送料金の最適化を通じて総所有コスト（TCO）を最小化する能力を検証します。
- **主要タスク**:
  - Task 4.1: コストを最適化したストレージソリューションを設計する（S3 Intelligent-Tiering, S3 ライフサイクルルール, EBS gp2 から gp3 移行, バックアップ保持期間最適化）
  - Task 4.2: コストを最適化したコンピューティングソリューションを設計する（Compute Savings Plans vs スポットインスタンス vs オンデマンド, AWS Compute Optimizer, EC2 休止状態）
  - Task 4.3: コストを最適化したデータベースソリューションを設計する（Aurora Serverless v2, DynamoDB オンデマンド vs プロビジョンド, RDS 予約インスタンス）
  - Task 4.4: コストを最適化したネットワークアーキテクチャを設計する（S3 Gateway型 VPC エンドポイントによる NAT ゲートウェイトラフィック削減, 同一 AZ 通信, CloudFront キャッシュによるデータ転送量削減）
- **重要キーワード**: S3 Intelligent-Tiering, S3 Glacier Deep Archive, Compute Savings Plans, Spot Instances, AWS Compute Optimizer, Aurora Serverless v2, DynamoDB On-Demand, S3 Gateway Endpoint, Data Transfer Costs

---
