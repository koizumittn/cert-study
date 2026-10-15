# Google Cloud Certified - Cloud Digital Leader 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Cloud Digital Leader
- **公式試験ガイド**: [Cloud Digital Leader 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/102926_cloud_digital_leader_exam_guide_japanese.pdf?hl=ja)
- **最終更新日**: 2026-10-12

---

## 1. 試験の概要と基本スペック

Cloud Digital Leader は、Google Cloud の中核的なプロダクトやサービスの機能と、それらが組織にもたらすメリットを明確に説明でき、一般的なビジネスユースケースやクラウドソリューションが企業をどのように支えるかを理解していることを認定するファウンデーショナルレベルの資格です。

- **試験時間**: 90 分
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題、複数選択問題
- **合否判定**: 合格 / 不合格（スコア非開示）
- **前提知識**: クラウドコンピューティングの基礎概念、デジタル変革（DX）の推進動機、Google Cloud プロダクトとサービスの基本的な機能・ユースケースに関する理解。プログラミングや複雑なアーキテクチャ設計・CLI運用経験は不要です。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全6セクションで構成されており、各セクションがほぼ均等（セクション1〜5が約18%ずつ、セクション6が約10%）に配分されています。ビジネス価値・データ・AI・インフラ・セキュリティ・運用の全領域にわたるバランスの取れた理解が求められます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | Google Cloud によるデジタル トランスフォーメーション | 約 18% | クラウドの価値提案（CapEx to OpEx、Agility、Elasticity）、IaaS/PaaS/SaaS、オープン標準、AI Hypercomputer、グローバルネットワーク | 完了 |
| **Section 2** | Google Cloud によるデータ トランスフォーメーションの探求 | 約 18% | Cloud Storage、Cloud SQL、Cloud Spanner、Bigtable、BigQuery、Looker、Pub/Sub、Dataflow、データガバナンス | 完了 |
| **Section 3** | Google Cloud の AI を活用したイノベーション | 約 18% | Gemini、Agent Platform（Agent Studio）、事前トレーニング済みAPI（Vision/Translation/Speech-to-Text）、BigQuery ML、AI Hypercomputer、責任あるAI | 完了 |
| **Section 4** | Google Cloud によるインフラストラクチャとアプリケーションのモダナイゼーション | 約 18% | クラウド移行戦略（リフト＆シフト/リプラットフォーム/リファクタリング）、Compute Engine、GKE、Cloud Run、Cloud Run functions、Apigee、マルチクラウド（Omni） | 完了 |
| **Section 5** | Google Cloud で実現する信頼とセキュリティ | 約 18% | 責任共有モデル、多層防御、ゼロトラスト、IAM、Cloud Armor、Security Command Center、Google Security Operations、Google Threat Intelligence、Model Armor | 完了 |
| **Section 6** | Google Cloud Operations を使用したスケーリング | 約 10% | リソース階層（組織/フォルダ/プロジェクト）、Cloud Billing レポート、予算アラート、Spot VM、Cloud Monitoring、Cloud Logging、SRE（SLI/SLO/SLA） | 完了 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: Google Cloud によるデジタル トランスフォーメーション（約 18%）
- **出題の狙い**: クラウドがビジネスにもたらす根本的な変革、オンプレミスとクラウドの価値提案の違い、クラウドアーキテクチャおよびサービスモデル（IaaS/PaaS/SaaS）のトレードオフ、Google Cloud 固有の差別化要因（オープン性、AIインフラ、グローバルネットワーク）の理解を検証します。
- **主要タスク**:
  - Task 1.1: クラウドがビジネスに革命を起こす理由とその方法を説明する（DXの動機・障壁、CapEx から OpEx、オープン性とオープン標準、Google Cloud の差別化要因）
  - Task 1.2: クラウドの基本コンセプトについて説明する（パブリック/プライベート/ハイブリッド/マルチクラウド、グローバルネットワーク、リージョン/ゾーン/エッジ、IaaS/PaaS/SaaS の責任境界とトレードオフ）
- **重要キーワード**: CapEx to OpEx, Business Agility, Elasticity, Vendor Lock-in, Open Source, IaaS/PaaS/SaaS, Region / Zone / Edge, Global Private Network

#### Section 2: Google Cloud によるデータ トランスフォーメーションの探求（約 18%）
- **出題の狙い**: データがデジタルトランスフォーメーションおよびAI活用で果たす役割、データライフサイクルとガバナンス、構造化・非構造化データに応じた最適な Google Cloud データストア選定、ならびにリアルタイム分析・BIによるデータの民主化の価値を検証します。
- **主要タスク**:
  - Task 2.1: 組織のデジタルトランスフォーメーションにおいてデータが果たす本質的な役割について説明する（DB/DWH/データレイクの違い、データサプライチェーン、データガバナンス、オープン性）
  - Task 2.2: ビジネス上のさまざまなユースケースに対し、最適な Google Cloud データマネジメントプロダクトを決定する（Cloud Storage 階層、Cloud SQL、Cloud Spanner、Bigtable、Firestore、AlloyDB）
  - Task 2.3: スマートアナリティクス、BIツール、ストリーミング分析がビジネスユースケースに価値をもたらす仕組みを検証する（Looker、BigQuery、Pub/Sub、Dataflow、Dataproc）
- **重要キーワード**: Database / Data Warehouse / Data Lake, Cloud Storage (Standard/Nearline/Coldline/Archive), Cloud SQL vs Cloud Spanner, Bigtable, BigQuery, Looker, Pub/Sub, Dataflow

#### Section 3: Google Cloud の AI を活用したイノベーション（約 18%）
- **出題の狙い**: AI/ML・生成AI・エージェント型AI（Agentic AI）の基本概念とビジネス価値、Google Cloud のAIソリューション選定基準（事前学習API、基盤モデルGemini、Agent Platform、カスタムML）、AI Hypercomputer のインフラ価値、および責任あるAI・AIセキュリティ（Model Armor）の理解を検証します。
- **主要タスク**:
  - Task 3.1: AI と ML の基本的なコンセプトとビジネス価値創出の仕組みを説明する（AI/ML/生成AI/エージェント型AI、データ品質の6大側面、説明可能なAI、責任あるAI）
  - Task 3.2: Google Cloud の AI サービスがビジネス価値を創出する方法を説明する（Gemini Enterprise Agent Platform、Agent Studio、事前トレーニング済みAPI、AI Hypercomputer [TPU/GPU]、BigQuery ML）
- **重要キーワード**: Agentic AI, Foundation Model (Gemini), Agent Platform / Agent Studio, Pre-trained APIs (Vision, Translation, Speech-to-Text), AI Hypercomputer (TPU/GPU), BigQuery ML, Responsible AI, Explainable AI, Model Armor

#### Section 4: Google Cloud によるインフラストラクチャとアプリケーションのモダナイゼーション（約 18%）
- **出題の狙い**: クラウド移行戦略（リフト＆シフト、リプラットフォーム、リファクタリング）、コンピューティング形態の進化（VM、コンテナ、サーバーレス）、最新アプリ開発（マイクロサービス、疎結合）、ハイブリッド/マルチクラウド展開、および API マネジメント（Apigee）によるビジネスエコノミー創出を検証します。
- **主要タスク**:
  - Task 4.1: 組織がクラウドに移行するうえで Google Cloud がどのように役立つかを説明する（移行戦略 [Rehost, Replatform, Refactor, Retain, Retire]、VM/コンテナ/サーバーレスの概念）
  - Task 4.2: Google Cloud のインフラストラクチャサービスの機能、ユースケース、ビジネス価値を説明する（Compute Engine、GKE、Cloud Run、Cloud Run functions、Spot VM、マルチクラウド [Omni, GKE Enterprise]）
  - Task 4.3: アプリケーション プログラミング インターフェース（API）が持つビジネス価値と Apigee の役割を説明する（APIの公開と収益化、Apigee API Management）
- **重要キーワード**: Migration Strategies (Lift & Shift / Replatform / Refactor), Compute Engine, GKE (Google Kubernetes Engine), Cloud Run, Cloud Run functions, Spot VM, BigQuery Omni / AlloyDB Omni / GKE Enterprise, Apigee API Management

#### Section 5: Google Cloud で実現する信頼とセキュリティ（約 18%）
- **出題の狙い**: サイバー脅威のランドスケープ、クラウドとオンプレミスのセキュリティ比較、責任共有モデル、ゼロトラストアーキテクチャ、Google の多層防御（カスタムハードウェアTitanからネットワーク・データ暗号化まで）、統合SecOps（Security Command Center、Google Security Operations、Google Threat Intelligence）、およびデジタル主権・データ所在地の理解を検証します。
- **主要タスク**:
  - Task 5.1: クラウドセキュリティの基本コンセプトを説明する（サイバー脅威、責任共有モデル、CIA三要素、ゼロトラスト、保存時/転送時/使用中暗号化、IAM、SecOps用語）
  - Task 5.2: 多層防御アプローチにより Google をセキュリティチームの一員に迎えるビジネス価値を説明する（AIスタック保護、Google Threat Intelligence [Mandiant + VirusTotal]、Security Command Center、Google Security Operations、Titan、Cloud Armor、Sensitive Data Protection、Confidential Computing、デジタル主権）
- **重要キーワード**: Shared Responsibility Model, Zero Trust (BeyondCorp), Encryption (At-rest, In-transit, In-use / Confidential Computing), Cloud IAM, Security Command Center (SCC), Google Security Operations, Google Threat Intelligence (Mandiant, VirusTotal), Model Armor, Digital Sovereignty

#### Section 6: Google Cloud Operations を使用したスケーリング（約 10%）
- **出題の狙い**: クラウド財務ガバナンス（FinOps、CapEx から OpEx、TCO）、リソース階層によるアクセス統制と費用配分、コスト管理ツール、フルスタックオブザーバビリティ（Cloud Monitoring、Cloud Logging、Trace、Profiler）、およびサイト信頼性エンジニアリング（SRE: SLI/SLO/SLA、エラーバジェット、ゴールデンシグナル）の理解を検証します。
- **主要タスク**:
  - Task 6.1: Google Cloud が組織のクラウド費用管理能力をどのようにサポートしているかを理解する（CapEx to OpEx、FinOps文化、リソース階層 [組織/フォルダ/プロジェクト]、Cloud Billing レポート、予算アラート、Dynamic Workload Scheduler、Spot VM）
  - Task 6.2: クラウドにおける最新の運用、信頼性、レジリエンスに関する基本コンセプトを説明する（Cloud Monitoring、Cloud Logging、Cloud Trace、レジリエンス設計、4つのゴールデンシグナル、SRE [SLI, SLO, SLA, エラーバジェット]）
- **重要キーワード**: CapEx to OpEx, TCO, Resource Hierarchy (Organization, Folder, Project, Resource), Cloud Billing Reports, Budget Alerts, Cloud Monitoring, Cloud Logging, Site Reliability Engineering (SRE), SLI / SLO / SLA, Error Budget, Golden Signals
