# Google Cloud Certified - Professional Machine Learning Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Machine Learning Engineer
- **公式試験ガイド**: [Professional Machine Learning Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_machine_learning_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Machine Learning Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/machine-learning-engineer?hl=ja)
- **公式学習パス**: [Google Skills - Machine Learning Engineer Learning Path](https://www.skills.google/paths/17)
- **最終更新日**: 2026-10-15

---

## 1. 試験の概要と基本スペック

Professional Machine Learning Engineer は、Google Cloud のマネージドサービスおよび一般的な機械学習（ML）アプローチを駆使し、ビジネス課題を解決するスケーラブルで高信頼な AI / ML ソリューションを設計、構築、評価、運用化（MLOps）、最適化できる高度な専門能力を認定するプロフェッショナル資格です。

本試験では、従来の予測 AI（表形式データ、時系列予測、画像分類、自然言語処理等）から最新の生成 AI（Gemini、Imagen、基盤モデルのファインチューニング、プロンプト・コンテキストエンジニアリング、RAG アーキテクチャ）に至るまで、幅広い AI ワークロードをカバーします。ローコード開発（BigQuery ML、AutoML）から、分散トレーニング（GPU / TPU、データ並列・モデル並列）、エンドツーエンドの MLOps パイプラインオーケストレーション（Vertex AI Pipelines、Cloud Composer、Ray on Vertex AI）、推論サービング（バッチ・オンライン、カスタム予測ルーチン）、そして本番運用におけるモデルモニタリング（ドリフト検知、スキュー防止）や AI セキュリティ・責任ある AI（Model Armor、Explainable AI、バイアス対策）までの包括的な実務意思決定能力が問われます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: 3 年以上の業界実務経験（Google Cloud を使用したスケーラブルな ML / AI ソリューションの設計・構築・運用管理に関する 1 年以上の実務経験を含む）が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 6 セクションで構成されています。プロトタイプのスケーリング（21%）、サービングとスケーリング（20%）、パイプライン自動化（18%）、プロトタイピング（16%）の 4 分野で全体の約 75% を占めており、これらにローコード AI 開発（13%）と運用モニタリング・セキュリティ（13%）が加わる極めて実践的な構成となっています。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | ローコード AI ソリューションの構築 | 約 13.0% | BigQuery ML、AutoML、事前トレーニング済み AI API（Vision、Document AI、Translate）、Model Garden、Gemini 基盤モデル、コンテキストキャッシング、プロンプト最適化 |
| **Section 2** | モデルのプロトタイピングとテスト | 約 16.0% | BigQuery、Dataflow、Dataproc、Vertex AI Feature Store、Sensitive Data Protection (DLP)、Vertex AI Workbench、Colab Enterprise、Vertex AI Experiments、Vertex AI ML Metadata、モデル評価指標、LLM-as-a-Judge、AutoSxS |
| **Section 3** | プロトタイプの ML モデルへのスケーリング | 約 21.0% | Vertex AI Custom Training、Tabular Workflows、Kubeflow on GKE、分散トレーニング（データ並列、モデル並列）、GPU（L4 / A100 / H100）、TPU（v4 / v5e / v5p）、Vertex AI Vizier、PEFT / LoRA ファインチューニング |
| **Section 4** | モデルのサービングとスケーリング | 約 20.0% | Vertex AI Endpoints、Vertex AI Batch Prediction、Cloud Run、GKE、ビルド済みコンテナ / カスタム予測ルーチン（CPR）、Model Registry、A/B テスト / カナリア展開、プライベートエンドポイント（PSC）、推論最適化（量子化、TensorRT） |
| **Section 5** | ML パイプラインの自動化とオーケストレーション | 約 18.0% | Vertex AI Pipelines (Kubeflow Pipelines SDK)、TFDV / TFT / TFMA、Cloud Composer (Apache Airflow)、Ray on Vertex AI、再トレーニングポリシー、CI/CD/CT 自動化（Cloud Build、Artifact Registry） |
| **Section 6** | AI ソリューションのモニタリング | 約 13.0% | Vertex AI Model Monitoring、データドリフト、コンセプトドリフト、トレーニングサービングスキュー、Explainable AI（SHAP、Integrated Gradients）、Model Armor、Prompt Injection 対策、責任ある AI（Fairness） |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: ローコード AI ソリューションの構築 (約 13%)
- **出題の狙い**: 高度なコーディングやスクラッチ開発を行わずに、BigQuery ML、AutoML、事前トレーニング済み API、および Model Garden の基盤モデルを活用して、迅速かつ高精度にビジネス課題を解決するローコード AI ソリューションを設計・実装する能力を検証します。
- **主要タスク**:
  - Task 1.1: BigQuery ML または AutoML を使用した ML モデルの開発（分類、回帰、時系列予測 [ARIMA+]、クラスタリング [K-means]、行列分解、特徴量エンジニアリング [TRANSFORM 句、ML.FEATURE_INFO]、予測生成 [ML.PREDICT、ML.GENERATE_TEXT]、AutoML トレーニング、BigQuery での Gemini モデルのチューニング）
  - Task 1.2: Google Cloud AI API または基盤モデルを使用した AI ソリューションの構築（Model Garden からのタスク別モデル評価・選定、業界固有 API [Document AI、Vision API、Translate API、Speech-to-Text] の適用、Gemini / Imagen / Veo を活用したソリューション構築、費用・レイテンシ・可用性を考慮した Gemini 最適化 [プロンプト設計、コンテキストキャッシング、モデル蒸留、クォータ管理]）
- **重要キーワード**: BigQuery ML (CREATE MODEL, TRANSFORM, ML.EVALUATE), Vertex AI AutoML, Model Garden, Foundation Models (Gemini, Imagen, Veo), Context Caching, Document AI, Vision API, Low-Code ML

#### Section 2: モデルのプロトタイピングとテスト (約 16%)
- **出題の狙い**: 探索的データ分析（EDA）、特徴量エンジニアリング、セキュアなノートブック環境でのプロトタイプ開発、および予測 AI / 生成 AI モデルの厳密な定量的・定性的テストと実験管理を遂行する能力を検証します。
- **主要タスク**:
  - Task 2.1: ML 用データの探索と前処理（表形式、テキスト、画像データの整理と探索、データ前処理ツールの選定 [BigQuery SQL、Dataflow、Dataproc / Spark、Python]、Vertex AI Feature Store での特徴量管理と統合、データプライバシー確保と機密情報 [PII] の保護 [Sensitive Data Protection / Cloud DLP、トークン化、匿名化]）
  - Task 2.2: ノートブックを使用したモデルのプロトタイピング（Vertex AI Workbench、Colab Enterprise、セキュリティとガバナンス [VPC Service Controls、IAM、アイドルシャットダウン]、PyTorch / scikit-learn / JAX を用いたモデル開発、Model Garden の基盤モデル / OSS モデルを用いたプロトタイプ作成）
  - Task 2.3: ML テストのトラッキングと実行（実験トラッキング環境の選定 [Vertex AI Experiments、Vertex AI Pipelines、Kubeflow Pipelines]、予測 AI と生成 AI の評価 [ROC-AUC、PR-AUC、F1 スコア、RMSE、MAE、LLM-as-a-Judge、AutoSxS、Gen AI Evaluation Service、ROUGE、BLEU]、モデルアーティファクト・バージョン・リネージの追跡と比較 [Vertex AI ML Metadata]）
- **重要キーワード**: Vertex AI Workbench, Colab Enterprise, Sensitive Data Protection (DLP), Vertex AI Feature Store, Vertex AI Experiments, Vertex AI ML Metadata, Model Evaluation Metrics, LLM-as-a-Judge, AutoSxS

#### Section 3: プロトタイプの ML モデルへのスケーリング (約 21%)
- **出題の狙い**: プロトタイプ検証済みのモデルを、コスト、レイテンシ、スループット、説明可能性を考慮して本番水準の大規模分散トレーニング環境へとスケーリングさせるアーキテクチャ設計および実装能力を検証します。
- **主要タスク**:
  - Task 3.1: 費用、複雑さ、レイテンシ、スケーラビリティを考慮したモデル構築（モデルタイプの選定 [ARIMA+、DNN、Boosted Trees、Transformer、LLM]、プロダクト選定 [AutoML、BigQuery ML、Vertex AI Custom Training]、デプロイ戦略、解釈可能性要件に応じたモデル手法の選定）
  - Task 3.2: モデルのトレーニング（Cloud Storage / BigQuery 上のトレーニングデータパイプラインへの取り込み、Vertex AI SDK を用いたカスタムトレーニングジョブ、GKE 上の Kubeflow、Tabular Workflows、トレーニング失敗のトラブルシューティング [OOM、勾配消失/爆発、I/O ネック]、ハイパーパラメータチューニング [Vertex AI Vizier、早期停止]、基盤モデルのファインチューニング [PEFT、LoRA、RLHF、蒸留]）
  - Task 3.3: トレーニングに適したハードウェアの選択（CPU、GPU [NVIDIA L4、A100、H100]、TPU [v4、v5e、v5p] の特性評価、分散トレーニング戦略 [データ並列: MirroredStrategy / DDP、モデル並列 / パイプライン並列: Megatron-LM / FSDP] の実装）
- **重要キーワード**: Vertex AI Custom Training, Vertex AI Vizier, Tabular Workflows, Kubeflow on GKE, TPU Pods / GPU Multi-Node, Data Parallelism vs Model Parallelism, Parameter-Efficient Fine-Tuning (PEFT/LoRA), Model Distillation

#### Section 4: モデルのサービングとスケーリング (約 20%)
- **出題の狙い**: トレーニング済みモデルを低遅延・高スループットかつ安全にサービングし、トラフィック変動に応じた自動スケーリングや無停止ロールアウトを実現する推論インフラストラクチャを構築・運用する能力を検証します。
- **主要タスク**:
  - Task 4.1: モデルのサービング（Vertex AI Endpoints、Model Garden、Cloud Run、GKE を用いたバッチ推論およびリアルタイムオンライン推論のデプロイ、ビルド済みコンテナとカスタム予測ルーチン [CPR] によるパッケージング、Vertex AI Model Registry によるバージョン管理、モデルロールアウト戦略 [A/B テスト、カナリアリリース、トラフィック分割]、推論前処理・後処理ロジックの実装）
  - Task 4.2: オンラインモデルサービングのスケーリング（Vertex AI Feature Store を用いたオンライン特徴量低レイテンシサービング、パブリックエンドポイントとプライベートエンドポイント [PSC / VPC ピアリング] の設計、アクセラレータ選定 [CPU、L4 GPU、エッジ]、スループットに応じたバックエンド自動スケーリング設定、本番推論最適化 [量子化 (INT8/FP8)、TensorRT、vLLM、TGI]）
- **重要キーワード**: Vertex AI Endpoints, Model Registry, Custom Prediction Routines (CPR), Traffic Splitting (A/B Testing, Canary), Private Service Connect (PSC), Batch Prediction, Online Feature Serving, Inference Optimization (Quantization, TensorRT)

#### Section 5: ML パイプラインの自動化とオーケストレーション (約 18%)
- **出題の狙い**: データの検証、前処理、トレーニング、評価、デプロイに至る一連の ML ライフサイクルをパイプラインとしてコード化し、ドリフト検知やコード変更に連動して自律的に再トレーニングとデプロイを実行する堅牢な MLOps 仕組みを構築する能力を検証します。
- **主要タスク**:
  - Task 5.1: エンドツーエンドの ML パイプラインの開発（データとモデルの検証 [TFDV、TFMA、スキーマ逸脱検知]、マネージドオーケストレーション [Vertex AI Pipelines、Kubeflow Pipelines SDK、Cloud Composer / Apache Airflow、Ray on Vertex AI]、トレーニングとサービング間の一貫したデータ前処理の保証 [TensorFlow Transform (TFT)、Dataflow]）
  - Task 5.2: モデル再トレーニングの自動化（再トレーニングトリガーポリシーの策定 [スケジュール、ドリフト検知、性能低下アラート]、CI/CD/CT パイプラインの構築 [Cloud Build、Artifact Registry、Vertex AI Pipelines、GitHub / GitLab 連携]）
- **重要キーワード**: Vertex AI Pipelines, Kubeflow Pipelines (KFP) SDK, Cloud Composer, TensorFlow Data Validation (TFDV), TensorFlow Transform (TFT), Ray on Vertex AI, Continuous Training (CT), CI/CD/CT (Cloud Build)

#### Section 6: AI ソリューションのモニタリング (約 13%)
- **出題の狙い**: 本番運用中のモデルパフォーマンス、データ整合性、AI セキュリティリスク、および説明可能性を継続的に監視・診断し、信頼性とコンプライアンスを維持する運用能力を検証します。
- **主要タスク**:
  - Task 6.1: AI ソリューションに対するリスクの特定（AI セキュリティツール [Model Armor、安全フィルタ、正規表現] を用いたデータ漏洩・悪意あるプロンプト [Prompt Injection、Jailbreak] の防御、責任ある AI [Responsible AI] の準拠とバイアスモニタリング、Vertex AI Explainable AI による特徴アトリビューション [Integrated Gradients、Sampled Shapley、XRAI]）
  - Task 6.2: AI ソリューションのモニタリング、テスト、トラブルシューティング（Vertex AI Model Monitoring による推論データとベースラインの継続比較、一般的な劣化事象の検出 [トレーニングサービングスキュー、データドリフト、コンセプトドリフト、特徴アトリビューションドリフト]、統計距離指標 [L-infinity、Jensen-Shannon]、生成 AI ソリューションの評価とモニタリング [ハルシネーション、毒性、グラウンディング検証]）
- **重要キーワード**: Vertex AI Model Monitoring, Data Drift, Concept Drift, Training-Serving Skew, Model Armor, Prompt Injection Defense, Explainable AI (Feature Attributions), Responsible AI, Grounding Evaluation

---

## 4. 推奨学習リソース＆公式ハンズオン・ラボ一覧

### 公式ドキュメント＆アーキテクチャフレームワーク
- [Google Cloud Architecture Framework: AI と機械学習](https://docs.cloud.google.com/docs/ai-ml?hl=ja#ai,-generative-ai,-and-ml-products-by-use-case)
- [Vertex AI の概要ドキュメント](https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning?hl=ja)
- [BigQuery ML の概要](https://docs.cloud.google.com/bigquery/docs/bqml-introduction?hl=ja)
- [Vertex AI Pipelines の概要](https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning/pipelines/introduction?hl=ja)
- [Vertex AI Model Monitoring の概要](https://docs.cloud.google.com/gemini-enterprise-agent-platform/machine-learning/model-monitoring/overview?hl=ja)
- [Generative AI on Vertex AI ドキュメント](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models?hl=ja)
- [Vertex AI Model Armor の概要](https://docs.cloud.google.com/model-armor/overview?hl=ja)

### 公式ハンズオンラボ（Google Skills）
1. **Machine Learning Engineer Learning Path (Skill Boost Path)**
   - BigQuery ML、Vertex AI AutoML、Custom Training、Pipelines、Model Monitoring を網羅する公式学習パス。
2. **Build and Deploy Machine Learning Solutions on Vertex AI (Skill Badge)**
   - Vertex AI Workbench、カスタムコンテナを用いたトレーニング、Model Registry への登録、エンドポイントサービングの実機演習。
3. **Build Real World Machine Learning Workflows with Dataprep and BigQuery ML (Skill Badge)**
   - BigQuery ML を使用した特徴量エンジニアリング、分類・回帰モデルの構築、バッチ推論の実装。
4. **Automating Machine Learning Pipelines with Vertex AI Pipelines (Lab)**
   - Kubeflow Pipelines SDK を用いたパイプライン構築、アーティファクト管理、モデル再トレーニング自動化の検証。
5. **Inspect Rich Documents with Gemini Multimodal and Document AI (Skill Badge)**
   - Document AI と Gemini マルチモーダルモデルを統合した高度なドキュメント解析パイプラインの実践。
