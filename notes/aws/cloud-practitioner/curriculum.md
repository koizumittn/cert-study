# AWS Certified Cloud Practitioner (CLF-C02) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Cloud Practitioner
- **試験コード**: CLF-C02
- **公式試験ガイド**: [AWS Certified Cloud Practitioner (CLF-C02) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html)
- **最終更新日**: 2026-10-04

---

## 1. 試験の概要と基本スペック

AWS Certified Cloud Practitioner は、AWS クラウドに関する全体的な知識と理解を実証するファウンデーショナルレベルの認定資格です。エンジニアだけでなく、プロジェクトマネージャー、セールス、財務、IT調達担当者など、クラウド関連業務に関わるあらゆるビジネスパーソンに推奨されます。

- **試験時間**: 90 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（4肢中1つ選択）、複数選択問題（5肢以上中2つ以上選択）
- **合格基準点**: 100〜1,000 点のスケールドスコアで 700 点以上
- **前提知識**: AWS クラウドの設計・実装・運用に関する 6 か月程度の基礎的な知識、またはクラウドに関わる実務経験が推奨されます。なお、コーディング、詳細なアーキテクチャ設計、詳細なトラブルシューティング、負荷テストなどは本試験の出題範囲外です。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | ドメイン名 / 出題分野 | 出題比率 | 主要対象サービス・ツール | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Domain 1** | クラウドのコンセプト | 24% | AWS Well-Architected Framework, AWS CAF, クラウドの6大利点, クラウド移行戦略 (7R), クラウドエコノミクス | 完了 |
| **Domain 2** | セキュリティとコンプライアンス | 30% | AWS 責任共有モデル, AWS IAM, IAM Identity Center, AWS Artifact, GuardDuty, AWS WAF, AWS Shield, KMS | 完了 |
| **Domain 3** | クラウドテクノロジーとサービス | 34% | Amazon EC2, AWS Lambda, Amazon ECS/EKS, Amazon S3, Amazon EBS, Amazon RDS, Amazon DynamoDB, Amazon VPC, Route 53, CloudFront | 完了 |
| **Domain 4** | 請求、料金、サポート | 12% | AWS 料金モデル, AWS Pricing Calculator, AWS Cost Explorer, AWS Budgets, AWS Organizations (一括請求), AWS サポートプラン | 完了 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

#### Domain 1: クラウドのコンセプト (24%)
- **出題の狙い**: AWS クラウドの価値提案（高可用性、俊敏性、弾力性、グローバル展開）、オンプレミスに対する優位性、AWS Well-Architected Framework の 6 つの柱、AWS クラウド導入フレームワーク (AWS CAF)、およびクラウドエコノミクス（CapEx から OpEx への転換、TCO、規模の経済）の理解を検証します。
- **主要タスク**:
  - Task 1.1: AWS クラウドの利点を定義する（デプロイ速度、グローバルリーチ、俊敏性、弾力性、規模の経済）
  - Task 1.2: AWS クラウドの設計原則を特定する（Well-Architected Framework の 6 つの柱）
  - Task 1.3: AWS クラウドへの移行の利点と戦略を理解する（AWS CAF の 6 つの視点、クラウド移行 7R 戦略）
  - Task 1.4: クラウドエコノミクスのコンセプトを理解する（固定費 vs 変動費、オンプレミス TCO、BYOL vs ライセンス込み、サイジング最適化）
- **重要キーワード**: CapEx to OpEx, Economies of Scale, Well-Architected Framework (6 Pillars), AWS CAF, Migration Strategies (7R), Right Sizing, BYOL

#### Domain 2: セキュリティとコンプライアンス (30%)
- **出題の狙い**: AWS 責任共有モデルにおける責任分担（サービスモデルごとの差異を含む）、IAM による厳格なアクセス制御（ルートユーザー保護、最小権限、MFA）、コンプライアンス確認リソース、および多層防御を実現する AWS セキュリティサービスの選定能力を検証します。
- **主要タスク**:
  - Task 2.1: AWS の責任共有モデルを理解する（インフラ側の責任 vs 顧客側の責任、EC2・RDS・Lambda における境界変化）
  - Task 2.2: AWS クラウドのセキュリティ、ガバナンス、コンプライアンスのコンセプトを理解する（AWS Artifact、暗号化、CloudWatch/CloudTrail/Config による監査）
  - Task 2.3: AWS アクセス管理機能を特定する（IAM ユーザー/グループ/ロール/ポリシー、ルートユーザー保護、MFA、IAM Identity Center）
  - Task 2.4: セキュリティのためのコンポーネントとリソースを特定する（AWS WAF、Shield、GuardDuty、Inspector、Security Hub、KMS、Secrets Manager）
- **重要キーワード**: Shared Responsibility Model, AWS IAM, Root User, MFA, IAM Identity Center, AWS Artifact, AWS KMS, AWS CloudTrail, AWS Config, Amazon GuardDuty, AWS WAF, AWS Shield

#### Domain 3: クラウドテクノロジーとサービス (34%)
- **出題の狙い**: AWS グローバルインフラストラクチャ（リージョン、AZ、エッジ）の構造と利点、各種デプロイモデルとアクセス手法、ならびにコンピュート、ストレージ、データベース、ネットワーク、AI/ML、分析、アプリケーション統合などの主要サービスの適切な位置づけとユースケースの特定能力を検証します。
- **主要タスク**:
  - Task 3.1: AWS クラウドでのデプロイと運用の方法を定義する（コンソール、CLI、SDK、IaC/CloudFormation、デプロイモデル）
  - Task 3.2: AWS のグローバルインフラストラクチャを定義する（リージョン、アベイラビリティーゾーン、エッジロケーション、低レイテンシー、DR）
  - Task 3.3: AWS のコンピューティングサービスを特定する（Amazon EC2、AWS Lambda、Amazon ECS/EKS、AWS Fargate、ELB、Auto Scaling）
  - Task 3.4: AWS データベースサービスを特定する（Amazon RDS、Amazon Aurora、Amazon DynamoDB、Amazon ElastiCache、AWS DMS）
  - Task 3.5: AWS のネットワークサービスを特定する（Amazon VPC、サブネット、セキュリティグループ、ネットワーク ACL、Route 53、Direct Connect、VPN）
  - Task 3.6: AWS ストレージサービスを特定する（Amazon S3、Amazon EBS、Amazon EFS、Amazon FSx、AWS Storage Gateway、AWS Backup）
  - Task 3.7: AWS の人工知能および機械学習 (AI/ML) サービスと分析サービスを特定する（Amazon SageMaker、Lex、Rekognition、Athena、Glue、Kinesis）
  - Task 3.8: 試験対象内のその他の AWS サービスカテゴリを特定する（Amazon SQS/SNS/EventBridge、Amazon Connect/SES、Developer Tools、WorkSpaces）
- **重要キーワード**: Region, Availability Zone (AZ), Edge Location, EC2, Lambda, Fargate, ECS/EKS, S3, EBS, EFS, RDS, Aurora, DynamoDB, VPC, Route 53, CloudFront, Direct Connect, CloudFormation

#### Domain 4: 請求、料金、サポート (12%)
- **出題の狙い**: Amazon EC2 をはじめとするコンピューティング購入オプション（オンデマンド、Savings Plans、リザーブド、スポット）、データ転送料金の特性、コスト見積もり・可視化・予算管理ツール、AWS Organizations による一括請求の仕組み、および AWS サポートプランの機能差分の特定能力を検証します。
- **主要タスク**:
  - Task 4.1: AWS 料金モデルを比較する（オンデマンド、Savings Plans、リザーブドインスタンス、スポットインスタンス、専有ホスト、データ転送料金）
  - Task 4.2: 請求、予算、コスト管理のためのリソースを理解する（AWS Pricing Calculator、AWS Cost Explorer、AWS Budgets、一括請求、コスト配分タグ）
  - Task 4.3: AWS の技術リソースと AWS サポートオプションを特定する（AWS サポートプラン 5種、AWS Trusted Advisor、AWS Health Dashboard、AWS Marketplace）
- **重要キーワード**: On-Demand, Savings Plans, Reserved Instances, Spot Instances, AWS Pricing Calculator, AWS Cost Explorer, AWS Budgets, Consolidated Billing, AWS Support Plans (Basic/Developer/Business/Enterprise), Trusted Advisor

---
