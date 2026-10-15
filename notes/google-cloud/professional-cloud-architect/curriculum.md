# Google Cloud Certified - Professional Cloud Architect 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Cloud Architect (PCA)
- **公式試験ガイド**: [Professional Cloud Architect 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_cloud_architect_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Cloud Architect | Google Cloud Certification](https://cloud.google.com/learn/certification/cloud-architect?hl=ja)
- **公式学習パス**: [Google Skills - Cloud Architect Learning Path](https://www.skills.google/paths/13?hl=ja)
- **最終更新日**: 2026-10-13

---

## 1. 試験の概要と基本スペック

Professional Cloud Architect は、Google Cloud テクノロジーを活用して、ビジネス目標を推進する堅牢、安全、スケーラブル、高効率、費用対効果、高可用性、かつ柔軟性の高いソリューションを設計、開発、管理する最高峰の実務アーキテクト能力を客観的に評価・認定するプロフェッショナル資格です。

エンタープライズクラウド戦略、ソリューション設計、ワークロード移行アプローチ、デプロイとオーケストレーション、リソース最適化、Well-Architected Framework（オペレーショナル エクセレンス、セキュリティ、信頼性、パフォーマンス最適化、コスト最適化、サステナビリティ）の実践的適用が問われます。さらに、昨今の改訂（Version 6.1+）により、Gemini Enterprise Agent Platform、Agent Builder、AI Hypercomputer、Model Garden、Model Armor などの生成 AI ソリューションや最新の AI/ML ワークフロー統合に関する深いアーキテクチャ設計能力が試験全体に織り込まれています。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: クラウド アーキテクチャに関する 3 年以上の実務経験、および Google Cloud を使用したソリューションの設計・管理に関する 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 6 セクションで構成されています。アーキテクチャの設計と計画（約 25%）、インフラの管理・プロビジョニング（約 17.5%）、セキュリティとコンプライアンス（約 17.5%）が中核をなし、さらにプロセス改善（約 15%）、実装管理（約 12.5%）、オペレーショナル エクセレンス（約 12.5%）が網羅的に評価されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | クラウド ソリューション アーキテクチャの設計と計画 | 約 25.0% | Well-Architected Framework, ビジネス・技術要件分析, 機能/非機能要件, BCP/DR, コスト最適化, 外部システム統合, マイグレーション戦略 (Migration Center, 評価, 依存関係, ライセンス), 将来性評価, AI/ML ソリューション統合 (Gemini LLM, Agent Builder, Model Garden) | 完了 |
| **Section 2** | クラウド ソリューション インフラストラクチャの管理とプロビジョニング | 約 17.5% | ハイブリッド・マルチクラウド ネットワーキング (Cloud Interconnect, Cloud VPN, Cross-Cloud Interconnect, NCC), VPC 設計・共有 VPC, Cloud Load Balancing, PSC, ストレージ選定 (Cloud Storage, Filestore, Cloud SQL, AlloyDB, Spanner, Bigtable, Firestore), コンピュート (Compute Engine, GKE, Cloud Run, VMware Engine), ML/生成 AI ワークフロー (Gemini Enterprise Agent Platform, Pipelines, AI Hypercomputer, GPU/TPU 最適化, Google AI APIs) | 完了 |
| **Section 3** | セキュリティとコンプライアンスを考慮した設計 | 約 17.5% | IAM・リソース階層, 職掌分散 (SoD), データセキュリティ (Cloud KMS, CMEK, Secret Manager), セキュリティ統制 (VPC SC, コンテキストアウェア アクセス, 組織ポリシー, 階層型ファイアウォール), 安全なリモートアクセス (IAP, サービス アカウント借用, Chrome Enterprise Premium, Workload Identity 連携), ソフトウェアサプライチェーン (Binary Authorization, Artifact Registry), AI セキュリティ (Model Armor, Sensitive Data Protection), 法規制・コンプライアンス (HIPAA, PCI-DSS, GDPR, SOC 2, Cloud Audit Logs) | 完了 |
| **Section 4** | 技術プロセスやビジネス プロセスの分析と改善 | 約 15.0% | SDLC・CI/CD (Cloud Build, Cloud Deploy), トラブルシューティング・根本原因分析 (RCA), テストフレームワーク, サービスカタログ・プロビジョニング, 障害復旧 (DR プラン・RTO/RPO), ステークホルダー管理・チェンジマネジメント, 組織スキル準備, コスト・リソース最適化 (CapEx/OpEx, FinOps, CUD, 予算アラート), ビジネス継続性 | 完了 |
| **Section 5** | 実装の管理 | 約 12.5% | アプリケーション・インフラのデプロイ支援, API 管理・統制 (Apigee, Cloud Endpoints), 負荷/単体/統合テストフレームワーク, 移行・管理ツール, Gemini Cloud Assist, プログラマティック操作 (Cloud Shell, Cloud Code, Google Cloud SDK [gcloud, gsutil, bq], クラウドエミュレータ, Terraform / IaC, Google API クライアントライブラリ) | 完了 |
| **Section 6** | ソリューションとオペレーション エクセレンスの確保 | 約 12.5% | Well-Architected オペレーション エクセレンスの柱, Google Cloud Observability (Cloud Monitoring, Cloud Logging, Cloud Trace, Cloud Profiler, ベンチマーク, アラート戦略, SLO/SLI/SLA, エラーバジェット), デプロイ・リリース管理 (Canary, Blue/Green, Rolling), サポート体制・エスカレーション, 品質管理, 本番信頼性検証 (カオスエンジニアリング, ペネトレーションテスト, 負荷テスト) | 完了 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: クラウド ソリューション アーキテクチャの設計と計画 (約 25%)
- **出題の狙い**: ビジネス要件（KPI、ROI、BCP、コスト、規制）および技術要件（高可用性、スケーラビリティ、パフォーマンス、低遅延）を包括的に分析し、Well-Architected Framework に基づく堅牢な多層分散アーキテクチャを設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: ビジネス要件を満たすインフラ設計（機能/非機能要件、事業継続計画、コスト最適化、外部連携、データ移動、トレードオフ評価、配置戦略、KPI/ROI 測定、セキュリティ・オブザーバビリティ考慮）
  - Task 1.2: 技術要件を満たすインフラ設計（Well-Architected 原則、高可用性と自動フェイルオーバー、伸縮性、パフォーマンスとレイテンシ、Gemini Cloud Assist の活用、バックアップ/リカバリ）
  - Task 1.3: ネットワーク・ストレージ・コンピューティングの総合設計（オンプレ/マルチクラウド接続、生成 AI/ML 連携 [Gemini, Agent Builder, AI Hypercomputer]、クラウドネイティブネットワーキング [VPC, PSC, LB]、ストレージ選択、コンピュートマッピング [GKE, Cloud Run, GCE]）
  - Task 1.4: 移行計画の策定（Migration Center、依存関係計画、ワークロードテスト、ライセンス・財務インパクト判断）
  - Task 1.5: 将来のソリューション向上想定（クラウド技術革新、ビジネス進化、クラウドファーストアプローチ）
- **重要キーワード**: Google Cloud Well-Architected Framework, Non-functional Requirements, BCP / Disaster Recovery, Migration Center, 7 Rs of Cloud Migration, Dedicated Interconnect, Private Service Connect, Gemini LLM, Agent Builder, AI Hypercomputer, Spot VMs, Cloud Run, GKE

#### Section 2: クラウド ソリューション インフラストラクチャの管理とプロビジョニング (約 17.5%)
- **出題の狙い**: ハイブリッド/マルチクラウドにまたがるネットワークトポロジ、ストレージ・データベース、コンピューティングリソース、およびエンドツーエンドの ML/生成 AI ワークフローを安全かつスケーラブルに構成・管理する能力を検証します。
- **主要タスク**:
  - Task 2.1: ネットワークトポロジの構成（オンプレミス拡張、マルチクラウド拡張、侵入防止・アクセス制御・ファイアウォール、VPC 設計、グローバル/リージョンロードバランサ）
  - Task 2.2: ストレージシステムの構成（ストレージ割り当て、データ処理・コンピューティングプロビジョニング、アクセス管理、データ転送・レイテンシ最適化、ライフサイクル・保持・容量増大計画、データ保護）
  - Task 2.3: コンピューティングシステムの構成（リソースプロビジョニング、スポット VM vs 標準、GCE / GKE / Cloud Run / VMware Engine のネットワーク構成、オーケストレーション、パッチ管理）
  - Task 2.4: Gemini Enterprise Agent Platform によるエンドツーエンド ML ワークフロー（Pipelines 自動化、データ統合、AI Hypercomputer、GPU / TPU A3 / TPU v5p 最適化、大規模分散トレーニング）
  - Task 2.5: 事前構築済みソリューション・API の構成（Google AI APIs [Search, Conversation, Vision, Audio, Video]、Gemini Enterprise [AI エージェント, NotebookLM]、Model Garden 統合）
- **重要キーワード**: Network Connectivity Center (NCC), Cross-Cloud Interconnect, Cloud Armor, Cloud Load Balancing, Cloud Storage Autoclass, Cloud Spanner Multi-Region, Bigtable Multi-Cluster, GKE Autopilot, Cloud Run, Agent Platform Pipelines, AI Hypercomputer (TPU v5p, GPU H100/B200), Model Garden

#### Section 3: セキュリティとコンプライアンスを考慮した設計 (約 17.5%)
- **出題の狙い**: ゼロトラストセキュリティモデル、リソース階層、職掌分散、データ保護（暗号化・KMS・機密コンピューティング）、ネットワーク境界防御（VPC SC）、安全なアクセス制御、AI セキュリティ（Model Armor）、およびグローバル法規制コンプライアンスを設計・実装する能力を検証します。
- **主要タスク**:
  - Task 3.1: セキュリティの設計（IAM 条件付きバインディング、組織・フォルダ・プロジェクト階層、職掌分散、Cloud KMS / CMEK / EKM、シークレット管理、VPC Service Controls、コンテキストアウェア アクセス、組織ポリシー、階層型ファイアウォール、Identity-Aware Proxy [IAP]、サービスアカウント権限借用、Chrome Enterprise Premium、Workload Identity 連携、Binary Authorization、Model Armor、Sensitive Data Protection）
  - Task 3.2: コンプライアンスの設計（医療記録 HIPAA / HITRUST、児童プライバシー COPPA、データ主権 / GDPR、PCI-DSS、SOC 1/2/3、Cloud Audit Logs [管理アクティビティ、データアクセス、システムイベント]）
- **重要キーワード**: Zero Trust, Resource Hierarchy, IAM Recommender, Separation of Duties, Cloud KMS / CMEK / Cloud HSM, VPC Service Controls (Service Perimeter), Context-Aware Access, Identity-Aware Proxy (IAP), Workload Identity Federation, Binary Authorization, Model Armor, Sensitive Data Protection, Cloud Audit Logs, HIPAA, PCI-DSS, GDPR

#### Section 4: 技術プロセスやビジネス プロセスの分析と改善 (約 15%)
- **出題の狙い**: SDLC、CI/CD パイプライン、テスト自動化、障害復旧計画、ポストモーテム根本原因分析などの技術プロセスと、チェンジマネジメント、ステークホルダー調整、FinOps / コスト最適化（CapEx から OpEx への転換）、ビジネス継続性などのビジネスプロセスを最適化する能力を検証します。
- **主要タスク**:
  - Task 4.1: 技術プロセスの分析と定義（SDLC、CI/CD [Cloud Build, Cloud Deploy]、トラブルシューティングと根本原因分析 [RCA / ポストモーテム]、テストと検証 [Canary, Blue/Green, 負荷テスト]、サービスカタログ [Service Catalog]、障害復旧計画 [RTO / RPO]）
  - Task 4.2: ビジネスプロセスの分析と定義（ステークホルダー管理、チェンジマネジメント、チーム評価とスキル準備、意思決定プロセス、カスタマーサクセスマネジメント、コスト最適化 [CapEx vs OpEx, FinOps, 予算アラート, CUD]、ビジネス継続性 [BCP]）
- **重要キーワード**: SDLC, Cloud Build, Cloud Deploy, Postmortem without Blame, Root Cause Analysis (RCA), RTO vs RPO, Disaster Recovery Strategies (Cold / Warm / Hot / Multi-Site Active-Active), FinOps, CapEx to OpEx, Committed Use Discounts (CUD), Cost Anomaly Detection, Change Management

#### Section 5: 実装の管理 (約 12.5%)
- **出題の狙い**: 開発チームおよび運用チームに対し、アプリケーションのデプロイ、API 管理（Apigee）、テストフレームワーク、データ移行、IaC（Terraform）、プログラマティック操作（CLI / SDK / API）、および Gemini Cloud Assist を活用した実装支援を主導する能力を検証します。
- **主要タスク**:
  - Task 5.1: 導入成功に向けたチーム支援（デプロイ手法、Apigee API 管理 [API キー、OAuth、クォータ、レート制限、アナリティクス]、テストフレームワーク、データ/システム移行ツール、Gemini Cloud Assist によるトラブルシューティングと IaC 生成）
  - Task 5.2: プログラマティックな操作（Cloud Shell、Cloud Code、Google Cloud SDK [gcloud, gsutil, bq]、クラウドエミュレータ [Bigtable, Spanner, Pub/Sub, Firestore]、IaC [Terraform, Google Cloud Provider, Config Connector]、Google API アクセスベストプラクティス [指数バックオフ, レート制限, OAuth トークン]、クライアントライブラリ）
- **重要キーワード**: Apigee API Management, API Gateway, Gemini Cloud Assist, Terraform, Google Cloud Provider, Config Connector, Cloud Shell, Cloud Code, gcloud CLI, Cloud Emulators, Exponential Backoff, Google Cloud Client Libraries

#### Section 6: ソリューションとオペレーション エクセレンスの確保 (約 12.5%)
- **出題の狙い**: Google Cloud Well-Architected Framework のオペレーション エクセレンスの柱に基づき、可観測性（オブザーバビリティ）、SLO/SLI/SLA 管理、エラーバジェット運用、リリースエンジニアリング、カオスエンジニアリング、および高信頼性テストを本番環境で実践する能力を検証します。
- **主要タスク**:
  - Task 6.1: Well-Architected Framework オペレーション エクセレンスの柱（自動化、標準化、継続的改善、インシデント管理）
  - Task 6.2: Google Cloud Observability ソリューション（Cloud Monitoring, Cloud Logging, Cloud Trace, Cloud Profiler, ベンチマーク, アラート戦略 [バーンレートアラート, ページャー疲弊防止], SLO / SLI / SLA / エラーバジェット運用）
  - Task 6.3: デプロイとリリース管理（Canary, Blue/Green, ローリングアップデート, 自動ロールバック）
  - Task 6.4: 本番運用のサポートと支援（ランブック自動化, インシデントコマンド体制）
  - Task 6.5: 品質管理方法の評価（静的解析, コードレビュー, 品質ゲート）
  - Task 6.6: 本番環境での信頼性確保（カオスエンジニアリング, ペネトレーションテスト, 負荷テスト, 障害注入テスト）
- **重要キーワード**: Well-Architected Operational Excellence, Google Cloud Observability, Cloud Monitoring, Cloud Logging, Cloud Trace, Cloud Profiler, SLO / SLI / SLA, Error Budget, Burn Rate Alerting, Canary Deployment, Chaos Engineering, Load Testing, Penetration Testing

---

## 4. 公式 4 大ケーススタディ（事例紹介）の概要と学習の手引き

Professional Cloud Architect 認定試験では、試験問題の約 20%〜30% において架空のエンタープライズ企業を舞台としたケーススタディ問題が出題されます。試験本番では 4 つの事例紹介の中からランダムで 2 つが提示され、各企業の前提条件や制約に基づくアーキテクチャの意思決定能力が問われます。

> [!IMPORTANT]
> **公式ケーススタディ案内・本文の熟読に関する推奨事項**:
> ここで紹介する内容は各企業の事業概要および主要な検討ポイントの要約（サマリー）です。本番試験では、各企業の「既存の技術環境（サーバー台数、OS、DB、ストレージ容量等）」「ビジネス目標」「技術的要件」「最高責任者（CEO / CTO / CFO 等）の発言・懸念」など、非常に細部の前提条件を踏まえたトレードオフ判断が問われます。
> 必ず受験前に、Google Cloud 公式サイトで公開されている各事例紹介の公式ドキュメント全文（PDF / Web ページ）を隅々まで精読・熟読し、企業ごとの制約条件を完全にインプットしておくことを強く推奨します。

### 1. Altostrat Media
- **事業概要**: 大規模なポッドキャスト、ニュース配信、ドキュメンタリー映像などの膨大なメディアライブラリを保有・配信するグローバルデジタルメディア企業。
- **課題と検討ポイント**:
  - オンプレミス CMS の老朽化とスケーラビリティの限界解消
  - 動画・音声トランスコーディングパイプラインの自動化とコスト最適化
  - マルチモーダル生成 AI（Gemini モデル）によるメタデータ自動抽出、文字起こし、要約、個別化レコメンデーション
  - オンプレミスアーカイブと Google Cloud 間の大容量プライベートハイブリッド接続（Dedicated Interconnect）
  - GKE Enterprise（Anthos）によるマルチクラスタ運用と Cloud Run によるイベント駆動処理
- **公式ドキュメント**: [Altostrat Media 事例紹介（公式試験案内）](https://cloud.google.com/learn/certification/guides/cloud-architect)

### 2. Cymbal Retail
- **事業概要**: 急激な成長を遂げているマルチブランド展開のオンライン小売事業者（EC プラットフォーム）。膨大かつ複雑な商品カタログを多数のサプライヤーから収集・展開。
- **課題と検討ポイント**:
  - サプライヤーから送られる非構造化生データ（テキスト・画像）からの商品説明・属性タグ自動生成（カタログエンリッチメント）
  - Vertex AI Search and Conversation（Discovery AI）を活用した対話型コマースとセマンティック検索
  - オンプレミスおよび複数クラウドに散在する異種データベース（MySQL, SQL Server, Redis, MongoDB）の統合
  - Datastream / Database Migration Service によるリアルタイム CDC 連携
  - Sensitive Data Protection による顧客個人情報（PII）・クレジットカード情報の自動検出とトークン化
- **公式ドキュメント**: [Cymbal Retail 事例紹介（公式試験案内）](https://cloud.google.com/learn/certification/guides/cloud-architect)

### 3. EHR Healthcare
- **事業概要**: 多数の病院、クリニック、保険会社に電子健康記録（EHR）ソリューションを提供する大手医療ヘルスケア IT サービスプロバイダー。
- **課題と検討ポイント**:
  - 患者ポータルおよび医療情報システムの 24/365 高可用性（ダウンタイムゼロ / 99.999% SLA）の達成
  - HIPAA、HITRUST 等の厳格な規制コンプライアンスと患者保健情報（PHI）の厳格な保護
  - VPC Service Controls によるデータ持ち出し（漏洩）防止境界の確立
  - Cloud KMS（CMEK）による保管時暗号化および Confidential VM（機密コンピューティング）によるメモリ上暗号化
  - Cloud Healthcare API（FHIR ストア、DICOM ストア）による標準規格連携と相互運用性
- **公式ドキュメント**: [EHR Healthcare 事例紹介（公式試験案内）](https://cloud.google.com/learn/certification/guides/cloud-architect)

### 4. KnightMotives Automotive
- **事業概要**: 世界各地でコネクテッドカーおよびフリート管理サービスを展開するグローバル自動車メーカー。数十万台の車両から常時テレメトリデータを収集。
- **課題と検討ポイント**:
  - 世界中を走行する数十万台の車両から毎秒送信される膨大なテレメトリデータ（毎秒数十万件のメッセージ）のリアルタイム取り込みと予知保全
  - Cloud Pub/Sub + Cloud Dataflow + Cloud Bigtable（時系列 NoSQL）による超低レイテンシストリーミング基盤
  - 欧州 GDPR をはじめとする各国のデータ主権・地域別規制（データ越境移転制限）の遵守
  - Vertex AI Agent Builder を用いた自然言語車両診断アシスタントおよび車載エッジ推論（TensorFlow Lite）
  - Apigee による外部パートナー（損害保険会社、正規ディーラー）向けセキュア API ガバナンス・レート制限
- **公式ドキュメント**: [KnightMotives Automotive 事例紹介（公式試験案内）](https://cloud.google.com/learn/certification/guides/cloud-architect)
