# AWS Certified DevOps Engineer - Professional (DOP-C02) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified DevOps Engineer - Professional
- **試験コード**: DOP-C02
- **公式試験ガイド**: [AWS Certified DevOps Engineer - Professional (DOP-C02) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/devops-engineer-professional-02/devops-engineer-professional-02.html)
- **最終更新日**: 2026-10-07

---

## 1. 試験の概要と基本スペック

AWS Certified DevOps Engineer - Professional (DOP-C02) は、AWS 環境における分散システムのプロビジョニング、運用、管理、および自動化に関する最高峰の技術的能力を検証するプロフェッショナル認定資格です。
継続的インテグレーション・継続的デリバリー (CI/CD) パイプラインの設計・実装、Infrastructure as Code (IaC) によるインフラと構成管理の自動化、大規模環境の耐障害性と高可用性の確保、フルスタック・オブザーバビリティ（監視・ロギング・トレーシング）、イベント駆動型のインシデント自動修復、そしてエンタープライズ規模のセキュリティ統制とコンプライアンス自動監査に至るまで、クラウド運用自動化の全領域を網羅します。

- **試験時間**: 180 分
- **出題問題数**: 75 問（採点対象: 65 問 / 未採点テスト設問: 10 問）
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **合格基準点**: 100〜1,000 点中 750 点以上
- **前提知識**: AWS 環境のプロビジョニング、運用、管理に関する 2 年以上の実務経験、コード開発またはスクリプト作成の経験、高可用性・スケーラブル・自己修復システムの設計・運用実績が推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 |
| :--- | :--- | :--- | :--- |
| **Domain 1** | SDLC 自動化 (SDLC Automation) | 22% | AWS CodePipeline, AWS CodeBuild, AWS CodeDeploy, Amazon ECR, AWS CodeArtifact, EC2 Image Builder, デプロイ戦略 (Canary, Blue/Green, Linear) |
| **Domain 2** | 構成管理と Infrastructure as Code (IaC) | 17% | AWS CloudFormation, CloudFormation StackSets, AWS CDK, AWS Systems Manager, AWS Config, AWS Service Catalog, AWS Control Tower |
| **Domain 3** | 高回復力クラウドソリューション (Resilient Cloud Solutions) | 15% | Multi-AZ / Multi-Region, Amazon Route 53 ARC, Amazon Aurora Global Database, DynamoDB Global Tables, Auto Scaling, AWS Backup, AWS Fault Injection Simulator (FIS) |
| **Domain 4** | 監視とロギング (Monitoring and Logging) | 15% | Amazon CloudWatch, CloudWatch Logs Insights, CloudWatch Metric Streams, Amazon Data Firehose (旧 Amazon Data Firehose), AWS X-Ray, CloudWatch アノマリー検出, CloudWatch Synthetics |
| **Domain 5** | インシデントとイベント対応 (Incident and Event Response) | 14% | Amazon EventBridge, AWS Health, AWS Systems Manager OpsCenter, SSM Automation ランブック, AWS Step Functions, デプロイ自動ロールバック |
| **Domain 6** | セキュリティとコンプライアンス (Security and Compliance) | 17% | IAM Identity Center, ABAC / RBAC, AWS Organizations SCP, AWS KMS, AWS Secrets Manager, AWS Macie, Amazon GuardDuty, AWS Security Hub, Amazon Inspector, AWS Config 自動修復 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

### Domain 1: SDLC 自動化 (SDLC Automation) (22%)
- **Task 1.1**: CI/CD パイプラインの実装（マルチアカウント・マルチリージョン パイプライン設計、CodePipeline、クロスアカウントロール連携、CodeBuild 環境変数・Secrets Manager 統合、アーティファクト暗号化 S3 バケットポリシー）
- **Task 1.2**: CI/CD パイプラインへの自動テストの統合（単体テスト、統合テスト、負荷テスト、CodeBuild テストレポート統合、SonarQube などの SAST セキュリティ静的解析ゲート）
- **Task 1.3**: アーティファクトの構築と管理（Amazon ECR イメージタグイミュータビリティ、ECR 脆弱性スキャン、AWS CodeArtifact アップストリームリポジトリ設定、EC2 Image Builder パイプライン自動化）
- **Task 1.4**: インスタンス、コンテナ、サーバーレス環境向けデプロイ戦略の実装（CodeDeploy による Canary / Linear / Blue/Green、ECS ローリング vs ブルー/グリーン、Lambda エイリアス重み付けトラフィックシフト、CloudWatch アラーム連動自動ロールバック）

### Domain 2: 構成管理と Infrastructure as Code (IaC) (17%)
- **Task 2.1**: クラウドインフラストラクチャおよび再利用可能コンポーネントの定義（AWS CloudFormation テンプレート設計、ネストされたスタック、エクスポート/クロススタック参照、AWS CDK L2/L3 コンストラクト、CloudFormation モジュール、AWS Service Catalog ポートフォリオ共有）
- **Task 2.2**: マルチアカウントまたはマルチリージョン環境におけるアカウント作成・オンボーディング・保護自動化の展開（AWS Organizations、AWS Control Tower ガードレール、CloudFormation StackSets サービスマネージドデプロイ、Account Factory for Terraform [AFT]）
- **Task 2.3**: 複雑なタスクおよび大規模環境向け自動化ソリューションの設計・構築（AWS Systems Manager State Manager による構成ドリフト防止、Patch Manager パッチベースライン自動適用、SSM Run Command、Step Functions + Lambda オーケストレーション）

### Domain 3: 高回復力クラウドソリューション (Resilient Cloud Solutions) (15%)
- **Task 3.1**: 回復力およびビジネス要件を満たす高可用性ソリューションの実装（Multi-AZ アーキテクチャ、クロスリージョン展開、Amazon Aurora Global Database、DynamoDB グローバルテーブル、Route 53 ルーティングポリシー）
- **Task 3.2**: ビジネス要件を満たすスケーラブルなソリューションの実装（EC2 Auto Scaling 予測スケーリング・ターゲット追跡、ECS Capacity Providers、ALB クロスゾーン負荷分散、ElastiCache Redis キャッシュ多層化、SQS 疎結合バッファリング）
- **Task 3.3**: RTO および RPO 要件を満たす自動復旧プロセスの実装（パイロットライト、ウォームスタンバイ、アクティブ/アクティブ DR 戦略、AWS Backup クロスアカウント・クロスリージョンボールト、Aurora レプリカ昇格自動化、AWS Fault Injection Simulator [FIS] カオス実験）

### Domain 4: 監視とロギング (Monitoring and Logging) (15%)
- **Task 4.1**: ログとメトリクスの収集、集約、ストレージの設定（CloudWatch エージェント集中配信、CloudWatch Metric Filters、Metric Streams + Amazon Data Firehose によるリアルタイム S3 出力、KMS CMK 暗号化、ライフサイクル保持期間）
- **Task 4.2**: ログとメトリクスの監査、監視、分析による問題検出（CloudWatch Logs Insights クエリ構文、CloudWatch アノマリー検出アラーム、AWS X-Ray セグメント・サブセグメント・サンプリングルール、QuickSight 可視化）
- **Task 4.3**: 複雑な環境における監視とイベント管理の自動化（EventBridge ルールによるメトリクス・ログイベント駆動処理、ECS / EKS オートスケーラー連携、Route 53 / ALB ヘルスチェック自動フェイルオーバー）

### Domain 5: インシデントとイベント対応 (Incident and Event Response) (14%)
- **Task 5.1**: イベントに応じた処理、通知、アクションのためのイベントソース管理（AWS Health イベント、CloudTrail API 呼び出し、CloudWatch アラームをトリガーとする EventBridge バス統合、SNS / SQS / Step Functions ファンアウト）
- **Task 5.2**: イベントに応じた構成変更の実装（AWS Config 非準拠検知時の Systems Manager Automation ランブック自動実行、非準拠リソースの自動修復、Security Group 不正ルールの即時削除）
- **Task 5.3**: システムおよびアプリケーション障害のトラブルシューティング（CodePipeline / CodeDeploy デプロイ失敗ログの解析、CloudWatch Synthetics Canary による API エラー根本原因分析、Systems Manager OpsCenter によるインシデント統合トリアージ）

### Domain 6: セキュリティとコンプライアンス (Security and Compliance) (17%)
- **Task 6.1**: 大規模環境におけるアイデンティティおよびアクセス管理手法の実装（IAM Identity Center による SSO 統合、属性ベースアクセス制御 [ABAC]、IAM ポリシー最小権限設計、AWS Secrets Manager 自動シークレットローテーション）
- **Task 6.2**: セキュリティ統制およびデータ保護の自動化の適用（AWS Organizations SCP によるガードレール強制、AWS KMS エンベロープ暗号化、Amazon Macie による PII 検出、AWS Network Firewall、AWS WAF 自動ブロックルール）
- **Task 6.3**: セキュリティ監視および監査ソリューションの実装（AWS Config ルールと継続的ドリフト検出、Amazon GuardDuty 脅威検知、AWS Security Hub 統合スコアリング、Amazon Inspector 脆弱性自動評価）
