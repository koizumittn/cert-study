# AWS Certified Security - Specialty (SCS-C03) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Security - Specialty
- **試験コード**: SCS-C03
- **公式試験ガイド**: [AWS Certified Security - Specialty (SCS-C03) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/security-specialty-03/security-specialty-03.html)
- **最終更新日**: 2026-10-11

---

## 1. 試験の概要と基本スペック

AWS Certified Security - Specialty (SCS-C03) は、AWS クラウド環境におけるワークロード、データ、インフラストラクチャ、およびアカウント群を包括的に保護するためのセキュリティソリューションの設計、実装、運用、トラブルシューティング能力を検証するスペシャリティレベルの認定資格です。

本試験（SCS-C03）は前バージョンの SCS-C02 から大幅に刷新され、脅威検知とログ管理の再統合、インシデント対応の独立ドメイン化、最新のゼロトラストアーキテクチャ（AWS Verified Access, Amazon Verified Permissions, IAM Roles Anywhere）、生成 AI ワークロードの保護（Amazon Bedrock ガードレール, GenAI OWASP Top 10）、リソース制御ポリシー（RCP）、および Open Cybersecurity Schema Framework (OCSF) を活用した統合セキュリティデータレイク運用など、現代の高度なクラウドセキュリティ要件が網羅されています。

- **試験時間**: 170 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（1つの正解）、複数選択問題（2つ以上の正解）
- **合格基準点**: 100〜1,000 点中 750 点以上
- **推奨される前提知識**:
  - AWS セキュリティサービスおよび機能に関する 2 年以上の設計・実装・運用実務経験
  - AWS 共有責任モデル、多層防御（Defense in Depth）、ゼロトラスト原則の深い理解
  - データ暗号化、暗号鍵ライフサイクル管理（AWS KMS, CloudHSM）、アイデンティティフェデレーション、およびネットワーク境界防御に関する実践的知見

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 |
| :--- | :--- | :--- | :--- |
| **Domain 1** | 検知（Detection） | 16% | Amazon GuardDuty, AWS Security Hub, Amazon Security Lake, AWS CloudTrail, Amazon CloudWatch Logs Insights, Amazon Macie, AWS Config Conformance Packs, Route 53 Resolver DNS Firewall |
| **Domain 2** | インシデント対応（Incident Response） | 14% | Amazon Detective, Automated Forensics Orchestrator for Amazon EC2, AWS Systems Manager (OpsCenter, Automation), AWS Step Functions, AWS Lambda, AWS Shield Advanced, AWS Fault Injection Service (FIS) |
| **Domain 3** | インフラストラクチャセキュリティ（Infrastructure Security） | 18% | AWS WAF, AWS Shield, Amazon CloudFront, AWS Network Firewall, セキュリティグループ, ネットワーク ACL, AWS Verified Access, EC2 Image Builder, Amazon Inspector, Amazon Bedrock Guardrails |
| **Domain 4** | アイデンティティおよびアクセス管理（Identity and Access Management） | 20% | AWS IAM, AWS IAM Identity Center, AWS STS, IAM Roles Anywhere, Amazon Cognito, Amazon Verified Permissions (Cedar 言語), IAM Access Analyzer, Permissions Boundaries, セッションポリシー |
| **Domain 5** | データ保護（Data Protection） | 18% | AWS KMS (CMK, BYOK, XKS), AWS CloudHSM, AWS Private Certificate Authority, S3 Object Lock, S3 バケットポリシー, AWS Secrets Manager, CloudWatch Logs データ保護ポリシー, Nitro Enclaves |
| **Domain 6** | セキュリティの基盤とガバナンス（Security Foundations and Governance） | 14% | AWS Organizations, AWS Control Tower, サービスコントロールポリシー (SCP), リソース制御ポリシー (RCP), AWS Firewall Manager, AWS RAM, AWS Config, AWS Audit Manager, AWS Artifact |

---

## 3. SCS-C02 から SCS-C03 への主要改定ポイント

1. **ドメイン構成の再編**:
   - SCS-C02 の「脅威検知とインシデント対応」「セキュリティログとモニタリング」が、SCS-C03 では **Domain 1: 検知 (16%)** と **Domain 2: インシデント対応 (14%)** に明確に分離・再編成。
   - ログ収集・分析・トラブルシューティングが Domain 1（検知）に集約され、Domain 2 はトリアージ・フォレンジック・自動封じ込め・根本原因分析に特化。
   - Domain 6 が「マネジメントとセキュリティガバナンス」から **「セキュリティの基盤とガバナンス」** に改称。
2. **最新クラウドセキュリティ技術の追加**:
   - **生成 AI アプリケーションの保護とガードレール**: Task 3.2.7（Amazon Bedrock Guardrails、GenAI OWASP Top 10 for LLM Applications 対応）。
   - **オープン標準セキュリティ基盤**: Task 3.1.4（Open Cybersecurity Schema Framework [OCSF] 形式によるデータ取り込み、Amazon Security Lake）。
   - **組織規模のリソース境界制御**: Task 6.1.3（リソース制御ポリシー [RCP: Resource Control Policies]）。
   - **ゼロトラスト認証・認可**: Task 4.1 / 4.2（Amazon Verified Permissions、IAM Roles Anywhere、AWS Verified Access）。
   - **分散環境・機密コンピューティングの暗号化**: Task 5.1.3（Amazon EMR、Amazon EKS、SageMaker AI のノード間暗号化、Nitro 暗号化）。
   - **機密データマスキング機能**: Task 5.3.4（CloudWatch Logs データ保護ポリシー、SNS メッセージデータ保護）。
   - **鍵管理の厳格化**: Task 5.3.2 / 5.3.3（インポートキー [BYOK] と AWS 生成キーの完全比較、外部キーストア [XKS]）。

---

## 4. ドメイン別タスクおよび学習ロードマップ

### Domain 1: 検知（Detection） (16%)
- **Task 1.1: AWS アカウントまたは組織のモニタリングおよびアラート戦略を設計・実装する**
  - ワークロードの監視要件分析とリソースヘルスチェック
  - セキュリティイベントの集約（Amazon GuardDuty, AWS Security Hub, Amazon Macie）
  - 異常検知メトリクス・ダッシュボード・アラート構築
  - AWS Config 適合パックおよび Systems Manager State Manager による継続的コンプライアンス評価
- **Task 1.2: ロギングソリューションを設計・実装する**
  - CloudTrail 組織証跡、CloudWatch Logs 集中集約、VPC フローログ、Route 53 リゾルバーログの設計
  - Amazon Security Lake による OCSF 形式ログデータレイクの構築
  - CloudWatch Logs Insights, Amazon Athena, OpenSearch Service によるログの解析・正規化・相関分析
- **Task 1.3: セキュリティモニタリング、ロギング、およびアラートのトラブルシューティング**
  - Lambda、API Gateway、CloudFront、CloudWatch エージェントのログ欠損・権限不足の診断と修正

### Domain 2: インシデント対応（Incident Response） (14%)
- **Task 2.1: インシデント対応計画を設計およびテストする**
  - Systems Manager OpsCenter および Jupyter / SageMaker ノートブックによるインシデントランブック設計
  - 爆発半径（Blast Radius）の最小化設計とアクセスプロビジョニング
  - AWS Fault Injection Service (FIS) および AWS Resilience Hub による対応計画の検証
  - Systems Manager Automation、Automated Forensics Orchestrator for Amazon EC2、Step Functions による自動封じ込め・修復
- **Task 2.2: セキュリティイベントに対応する**
  - フォレンジック証拠（EBS スナップショット、メモリダンプ、ログ）の保全と完全性確保
  - セキュリティ検知結果の検証、影響範囲およびスコープの特定
  - ネットワーク隔離（セキュリティグループ切断、隔離用 NACL 適用）とバックアップ復旧
  - Amazon Detective によるグラフベース根本原因分析（RCA）

### Domain 3: インフラストラクチャセキュリティ（Infrastructure Security） (18%)
- **Task 3.1: ネットワークエッジサービスのセキュリティコントロールを設計・実装・トラブルシューティングする**
  - AWS WAF ルール（マネージドルール、レート制限、地理的制限、ボット制御、OWASP Top 10 防御）
  - Amazon CloudFront セキュリティヘッダーポリシーおよびオリジンアクセス制御 (OAC)
  - AWS Shield Standard / Advanced による L3/L4/L7 DDoS 防御と Cost Protection
  - OCSF 形式でのエッジログ連携およびサードパーティ WAF 統合
- **Task 3.2: コンピュートワークロードのセキュリティコントロールを設計・実装・トラブルシューティングする**
  - EC2 Image Builder によるゴールデン AMI およびコンテナイメージの自動強化・パイプライン適用
  - インスタンスプロファイル、サービスロール、実行ロールの最小権限設計
  - Amazon Inspector による EC2、ECR コンテナ、Lambda の脆弱性スキャン
  - Systems Manager Patch Manager によるパッチ自動適用
  - Systems Manager Session Manager および EC2 Instance Connect による安全なリモート管理
  - Amazon Bedrock Guardrails および GenAI OWASP Top 10 for LLM Applications による生成 AI 保護
- **Task 3.3: ネットワークセキュリティコントロールを設計およびトラブルシューティングする**
  - セキュリティグループ（ステートフル）とネットワーク ACL（ステートレス）の適切な階層設計
  - AWS Network Firewall によるステートフルインスペクション、ドメインフィルタリング、IPS/IDS
  - AWS Verified Access による VPN レス・ゼロトラストアプローチ
  - ハイブリッド接続保護（AWS Direct Connect MACsec, AWS Site-to-Site VPN, IPsec）
  - Network Access Analyzer によるネットワーク経路検証

### Domain 4: アイデンティティおよびアクセス管理（Identity and Access Management） (20%)
- **Task 4.1: 認証戦略を設計・実装・トラブルシューティングする**
  - AWS IAM Identity Center によるエンタープライズ IdP（SAML 2.0 / OIDC）連携と SSO
  - Amazon Cognito（ユーザープール、ID プール）によるモバイル/Web アプリ認証
  - AWS STS による一時的セキュリティ認証情報の発行（AssumeRole, AssumeRoleWithWebIdentity）
  - 認証障害のトラブルシューティング（CloudTrail イベント、SAML アサーションエラー、Directory Service 連携）
- **Task 4.2: 認可戦略を設計・実装・トラブルシューティングする**
  - ABAC（属性ベースアクセス制御）と RBAC（ロールベースアクセス制御）の設計と適用
  - 許可の境界（Permissions Boundaries）とセッションポリシーによる権限昇格防止
  - クロスアカウントアクセスのためのリソースベースポリシーと信頼ポリシー（Trust Policies）
  - Amazon Verified Permissions と Cedar ポリシー言語によるきめ細かな認可
  - IAM Roles Anywhere によるオンプレミスサーバーの X.509 証明書ベース認可
  - IAM Access Analyzer による未使用アクセス権限の検出と最小権限ポリシー自動生成

### Domain 5: データ保護（Data Protection） (18%)
- **Task 5.1: 転送中データのコントロールを設計・実装する**
  - ELB セキュリティポリシー（TLS 1.3 推奨、暗号スイート制御）
  - AWS PrivateLink および VPC エンドポイントによるプライベート通信強制
  - EMR、EKS、SageMaker AI、Nitro システムのクラスタノード間内部暗号化
- **Task 5.2: 保管中データのコントロールを設計・実装する**
  - 暗号化方式の選定（SSE-S3, SSE-KMS, SSE-C, クライアントサイド暗号化）
  - S3 Object Lock（合意モード / ガバナンスモード / リーガルホールド）による WORM ストレージ運用
  - S3 Glacier Vault Lock による変更不可アーカイブ
  - S3 ライフサイクルポリシー、AWS Backup による不変バックアップ（Vault Lock）とランサムウェア対策
- **Task 5.3: 機密データ、認証情報、シークレット、暗号鍵素材を保護するコントロールを設計・実装する**
  - AWS Secrets Manager による自動シークレットローテーション（Lambda 連携）
  - AWS KMS カスタマー管理型キー (CMK)、マルチリージョンキー、インポートキー素材 (BYOK) と AWS 生成キーの特性比較
  - 外部キーストア (XKS) による外部 HSM 連携
  - AWS Private Certificate Authority (Private CA) によるプライベート PKI 構築
  - CloudWatch Logs データ保護ポリシーおよび SNS メッセージデータ保護による機密情報マスキング

### Domain 6: セキュリティの基盤とガバナンス（Security Foundations and Governance） (14%)
- **Task 6.1: AWS アカウントを集中的にデプロイおよび管理する戦略を策定する**
  - AWS Organizations によるマルチアカウント階層化（OU 設計）
  - AWS Control Tower によるランディングゾーン構築とガードレール（予防的・発見的・プロアクティブ）
  - サービスコントロールポリシー (SCP) によるアカウントレベルの権限制約
  - リソース制御ポリシー (RCP) による組織内リソースへのアクセス境界制御
  - セキュリティサービスの委任管理者（Delegated Administrator）設定
  - ルートユーザー認証情報の保護、集中管理、MFA 強制、および緊急時ブレークグラス手順
- **Task 6.2: クラウドリソースの安全で一貫したデプロイ戦略を実装する**
  - AWS CloudFormation StackSets によるマルチアカウント・マルチリージョン安全配布
  - CloudFormation Guard および cfn-lint による IaC セキュリティ静的解析
  - AWS Firewall Manager による組織横断 WAF / Network Firewall / セキュリティグループ集中適用
  - AWS Resource Access Manager (AWS RAM) によるセキュアなリソース共有
- **Task 6.3: AWS リソースのコンプライアンスを評価する**
  - AWS Config ルールおよび修復アクション（SSM Automation）による自己修復
  - AWS Security Hub によるセキュリティ標準（CIS, AWS Foundational Security Best Practices）自動評価
  - AWS Audit Manager による監査証跡の自動収集とレポート生成
  - AWS Artifact によるコンプライアンスレポート（SOC, PCI DSS, ISO）の取得
  - AWS Well-Architected Tool（セキュリティの柱）によるリスク分析
