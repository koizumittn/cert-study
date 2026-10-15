# Google Cloud Certified - Professional Cloud Security Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Cloud Security Engineer
- **公式試験ガイド**: [Professional Cloud Security Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_cloud_security_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Cloud Security Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/cloud-security-engineer?hl=ja)
- **公式学習パス**: [Google Skills - Security Engineer Learning Path](https://www.cloudskillsboost.google/paths/15)
- **最終更新日**: 2026-10-14

---

## 1. 試験の概要と基本スペック

Professional Cloud Security Engineer は、Google Cloud において安全なワークロードと強固なセキュリティアーキテクチャを設計・実装・運用・管理できる能力を認定するプロフェッショナル資格です。

セキュリティに関するベストプラクティス、業界標準のコンプライアンス要件、および Google Cloud 固有の高度なセキュリティ技術（Zero Trust 原則、BeyondCorp、VPC Service Controls、Cloud KMS / CMEK / EKM、Security Command Center、Sensitive Data Protection、Binary Authorization 等）を駆使し、クラウド環境における脅威防御、インシデント検知・対応、アクセス制御、データ保護、規制遵守を包括的に遂行する実務能力が厳密に評価されます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: 3 年以上の業界実務経験（セキュリティ運用の実務経験 1 年以上を含む）、および Google Cloud を使用した本番環境ソリューションの設計・構築・運用管理に関する 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 5 セクションで構成されています。アクセスの構成（25%）、確実なデータ保護（23%）、通信の保護と境界保護の確立（20%）、オペレーションの管理（20%）が試験の約 90% を占めており、これらを支えるコンプライアンス要件のサポート（12%）が網羅的に評価されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | アクセスの構成 | 約 25.0% | Cloud Identity, GCDS, SSO (SAML / OAuth 2.0), 2 段階認証, Workforce Identity 連携, サービスアカウント（キーレス化, 短期認証情報, 権限借用, Workload Identity 連携）, Cloud IAM（事前定義/カスタムロール, IAM 条件, 拒否ポリシー, Access Context Manager, ポリシーインテリジェンス）, リソース階層（組織・フォルダ・プロジェクト・組織ポリシー） | 未着手 |
| **Section 2** | 通信の保護と境界保護の確立 | 約 20.0% | 境界セキュリティ（階層型ファイアウォールポリシー, Cloud Armor WAF, IAP, Certificate Authority Service, Secure Web Proxy, Cloud DNS SEC）, 境界セグメント（VPC, Shared VPC, VPC ピアリング, N 層分離, VPC Service Controls [境界, 境界ブリッジ, Egress/Ingress ルール]）, プライベート接続（HA-VPN, Cloud Interconnect, MACsec, プライベート Google アクセス, Private Service Connect, Cloud NAT） | 未着手 |
| **Section 3** | 確実なデータ保護 | 約 23.0% | センシティブデータ保護（Sensitive Data Protection / Cloud DLP, PII 検査/秘匿化, 継続的プロファイリング, 仮名化, フォーマット保持暗号化 [FPE]）, データストアアクセス制限（BigQuery, Cloud Storage, Cloud SQL）, Secret Manager, VM メタデータ保護, 暗号化管理（デフォルト暗号化, CMEK, Cloud HSM, Cloud EKM, オブジェクトライフサイクル）, Confidential Computing（Confidential VM / GKE）, AI セキュリティ＆プライバシー（Vertex AI セキュリティ, トレーニングデータ/モデル保護） | 未着手 |
| **Section 4** | オペレーションの管理 | 約 20.0% | セキュリティ自動化（CI/CD パイプライン脆弱性スキャン, Artifact Analysis, Binary Authorization, VM / コンテナのベースイメージ強化・パッチ管理, Security Health Analytics カスタムモジュール）, ロギング・モニタリング・検知（Cloud Logging, VPC フローログ, Packet Mirroring, Cloud IDS, ログ分析, ログシンク・集約シンク, Cloud Audit Logs, Security Command Center [SCC Enterprise / Premium, イベント脅威検出, 異常検出, 脆弱性管理, ガバナンス]） | 未着手 |
| **Section 5** | コンプライアンス要件のサポート | 約 12.0% | 規制要件（PCI DSS, HIPAA, FedRAMP, GDPR, 責任共有モデル）, データとサービスのリージョン化, 規制遵守のための制御（Assured Workloads, 組織ポリシー制約, アクセスの透明性 [Access Transparency], アクセス承認 [Access Approval]） | 未着手 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: アクセスの構成 (約 25%)
- **出題の狙い**: エンタープライズの ID 管理基盤を確立し、ユーザー・サービスアカウント・外部 ID のセキュアな認証および最小権限の認可制御を実装する能力を検証します。
- **主要タスク**:
  - Task 1.1: Cloud Identity を管理する（Google Cloud Directory Sync [GCDS] とサードパーティコネクタの構成、特権管理者アカウントの管理、ユーザーライフサイクル管理プロセスの自動化、プログラムによるアカウント・グループ管理、Workforce Identity 連携）
  - Task 1.2: サービスアカウントを管理する（デフォルトサービスアカウントの保護・無効化、サービスアカウント要件の特定、作成・無効化・承認、サービスアカウントキーの使用制限・監査、有効期間の短い認証情報 [Short-lived credentials]、Workload Identity 連携、サービスアカウントの権限借用 [Impersonation]）
  - Task 1.3: 認証を管理する（パスワードおよびセッション管理ポリシー、SAML 2.0 / OAuth 2.0 シングルサインオン、2 段階認証プロセス [2SV / セキュリティキー] の適用）
  - Task 1.4: 認可制御を管理、実装する（IAM 事前定義/カスタムロールによる職掌分散 [SoD]、IAM と ACL、IAM 条件 [IAM Conditions]、IAM 拒否ポリシー [Deny Policies]、リソースレベルでの ID ロール設計、Access Context Manager によるコンテキスト認識アクセス、ポリシーインテリジェンス [IAM Recommender] による権限最適化、グループベースのアクセス管理）
  - Task 1.5: リソース階層を定義する（大規模組織の作成と階層管理、組織ポリシー [Organization Policies] の一元管理、階層を通じた権限継承の制御）
- **重要キーワード**: Cloud Identity, GCDS, Workforce Identity Federation, Workload Identity Federation, Service Account Impersonation, Short-lived Credentials, IAM Roles, IAM Conditions, IAM Deny Policies, Access Context Manager, Policy Intelligence, Organization Policies

#### Section 2: 通信の保護と境界保護の確立 (約 20%)
- **出題の狙い**: ゼロトラストおよび多層防御の原則に基づき、パブリック / プライベートネットワークの境界を厳密に分離・保護し、不正侵入やデータ持ち出し（Data Exfiltration）を遮断するネットワークアーキテクチャを設計・実装する能力を検証します。
- **主要タスク**:
  - Task 2.1: 境界セキュリティを設計して構成する（階層型ファイアウォールポリシー、Identity-Aware Proxy [IAP]、Cloud Load Balancing、Certificate Authority Service [CAS]、プライベート IP vs パブリック IP の分離設計、Google Cloud Armor による WAF / DDoS 防御、Secure Web Proxy のデプロイ、Cloud DNSSEC、API 利用制限と継続的モニタリング）
  - Task 2.2: 境界セグメントを構成する（VPC ネットワーク・共有 VPC・VPC ピアリング・ファイアウォールルールのセキュリティプロパティ、N 層アプリケーションのセグメンテーション、VPC Service Controls による境界 [Service Perimeters]、境界ブリッジ、Ingress / Egress ルール）
  - Task 2.3: プライベート接続を確立する（共有 VPC、VPC ピアリング、オンプレミス向けプライベート Google アクセス、HA-VPN、Cloud Interconnect [MACsec / IPsec]、プライベート Google アクセス / 制限付き Google アクセス、Private Service Connect [PSC]、Cloud NAT によるセキュアな送信トラフィック確立）
- **重要キーワード**: Hierarchical Firewall Policies, Google Cloud Armor, Identity-Aware Proxy (IAP), Certificate Authority Service (CAS), Secure Web Proxy, DNSSEC, VPC Service Controls (VPC SC), Private Service Connect (PSC), Private Google Access, HA-VPN, Cloud Interconnect (MACsec), Cloud NAT

#### Section 3: 確実なデータ保護 (約 23%)
- **出題の狙い**: データのライフサイクル（保存中、転送中、使用中）全体にわたって最高レベルの暗号化とアクセス制御を適用し、機密情報の漏洩・損失を防ぐとともに、AI / ML ワークロードのプライバシーと完全性を維持する能力を検証します。
- **主要タスク**:
  - Task 3.1: センシティブデータを保護し、データ損失を防止する（個人情報 [PII] の自動検出と秘匿化、Sensitive Data Protection による構造化・非構造化データの継続的プロファイリング、仮名化 [Pseudonymization]、フォーマット保持暗号化 [FPE]、BigQuery [行・列レベルセキュリティ]・Cloud Storage・Cloud SQL のアクセス制限、Secret Manager によるシークレット保護、コンピュートメタデータの保護）
  - Task 3.2: 保存データ、転送中のデータ、使用中のデータの暗号化を管理する（Google デフォルト暗号化、顧客管理暗号鍵 [CMEK]、Cloud HSM、Cloud External Key Manager [Cloud EKM] の選定と鍵ライフサイクル管理、Cloud Storage オブジェクトライフサイクル、Confidential Computing [Confidential VM / GKE] による使用中データの暗号化）
  - Task 3.3: AI におけるセキュリティとプライバシーを計画する（AI / ML システムのセキュリティ管理実装によるデータ・モデルの不正使用防止、Vertex AI / IaaS / PaaS でホストされた学習モデルのセキュリティ要件定義）
- **重要キーワード**: Sensitive Data Protection (Cloud DLP), De-identification, Format-Preserving Encryption (FPE), Column/Row-level Security, Secret Manager, Google Default Encryption, CMEK, Cloud HSM, Cloud EKM, Confidential Computing, AI/ML Model Protection

#### Section 4: オペレーションの管理 (約 20%)
- **出題の狙い**: CI/CD パイプラインにおけるサプライチェーンセキュリティの自動化、集中ロギング・ネットワークトラフィック検査、および Security Command Center を軸とした脅威の早期検知・インシデントレスポンスを実装する能力を検証します。
- **主要タスク**:
  - Task 4.1: インフラストラクチャとアプリケーションのセキュリティを自動化する（CI/CD パイプラインでの脆弱性スキャン・CVE 検出、Binary Authorization による署名付きコンテナデプロイ強制、ゴールデン VM イメージの作成・強化・パッチ管理、コンテナイメージの検証・強化・パッチ管理、Security Health Analytics カスタムモジュールによるポリシー・ドリフト検出）
  - Task 4.2: ロギング、モニタリング、検出を構成する（ファイアウォールルールロギング、VPC フローログ、Packet Mirroring、Cloud IDS、ログ分析、セキュリティインシデントのロギング・監視・修復自動化、ログへの最小権限アクセス設計、外部 SIEM [Splunk, Datadog 等] へのログエクスポート、Cloud Audit Logs [Admin Activity, Data Access, System Event, Policy Denied] の分析、ログシンク・集約シンク、Security Command Center の構成・モニタリング）
- **重要キーワード**: Binary Authorization, Vulnerability Scanning (Artifact Analysis), Security Health Analytics (SHA), VPC Flow Logs, Packet Mirroring, Cloud IDS, Cloud Audit Logs, Aggregated Log Sinks, Security Command Center (SCC), Event Threat Detection

#### Section 5: コンプライアンス要件のサポート (約 12%)
- **出題の狙い**: クラウドの責任共有モデルを正しく評価し、規制業界（金融、医療、公共等）に適合するデータ主権・ロケーション制限・運用ガバナンスコントロールを設計・適用する能力を検証します。
- **主要タスク**:
  - Task 5.1: クラウドの規制要件を決定する（コンピュート、データ、ネットワーク、ストレージのコンプライアンス懸念事項特定、責任共有モデルの評価、データとサービスのリージョン化 [Resource Location Restriction]、規制遵守のための制御 [Assured Workloads, 組織ポリシー, アクセスの透明性 / Access Transparency, アクセス承認 / Access Approval]、Google Cloud 規制準拠環境の選定）
- **重要キーワード**: Shared Responsibility Model, Assured Workloads, Data Residency, Resource Location Restriction, Access Transparency, Access Approval, Compliance Frameworks (PCI-DSS, HIPAA, FedRAMP, GDPR, SOC 2)

---

## 4. 推奨学習リソース＆公式ハンズオン・ラボ一覧

### 公式ドキュメント＆アーキテクチャフレームワーク
- [Google Cloud Architecture Framework: セキュリティ、プライバシー、コンプライアンス](https://cloud.google.com/architecture/framework/security?hl=ja)
- [Google Cloud セキュリティのベスト プラクティス ガイド](https://cloud.google.com/docs/security/best-practices?hl=ja)
- [BeyondCorp Enterprise 公式ドキュメント](https://cloud.google.com/beyondcorp-enterprise/docs?hl=ja)
- [VPC Service Controls のベスト プラクティス](https://cloud.google.com/vpc-service-controls/docs/best-practices?hl=ja)
- [Cloud Key Management Service (KMS) のディープダイブ](https://cloud.google.com/kms/docs?hl=ja)
- [Security Command Center 公式ドキュメント](https://cloud.google.com/security-command-center/docs?hl=ja)

### 公式ハンズオンラボ（Google Skills / Cloud Skills Boost）
1. **Security Best Practices in Google Cloud (Skill Badge)**
   - IAM、VPC ファイアウォール、Cloud KMS、Cloud Storage 暗号化を実機演習。
2. **Mitigate Threats and Vulnerabilities with Security Command Center (Skill Badge)**
   - Security Command Center を有効化し、Security Health Analytics や Event Threat Detection を用いた脆弱性・脅威の検出と修復を検証。
3. **Build and Secure Networks in Google Cloud (Skill Badge)**
   - 共有 VPC、Cloud Armor、Identity-Aware Proxy (IAP) の境界セキュリティを構成。
4. **Protect Sensitive Data with Cloud Logging, Cloud KMS, and Sensitive Data Protection (Skill Badge)**
   - 機密データのマスキング、Cloud KMS による暗号鍵管理、監査ログの集約を実機構築。
