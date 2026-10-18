# AWS Certified Machine Learning Engineer - Associate (MLA-C02) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Machine Learning Engineer - Associate
- **試験コード**: MLA-C02
- **公式試験ガイド**: [AWS Certified Machine Learning Engineer - Associate (MLA-C02) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/machine-learning-engineer-associate-02/machine-learning-engineer-associate-02.html)
- **最終更新日**: 2026-10-04

---

## 1. 試験の概要と基本スペック

AWS Certified Machine Learning Engineer - Associate (MLA-C02) は、AWS クラウドを使用した機械学習 (ML) および人工知能 (AI) ソリューションとパイプラインの構築、運用化、デプロイ、保守に関する実践的能力を検証する認定資格です。
従来の機械学習モデル（表形式データ、分類・回帰、クラスタリング等）に加えて、生成 AI (GenAI)、基盤モデル (FM)、エージェンティックワークフロー (Agentic Workflows)、検索拡張生成 (RAG)、および最新の MLOps / LLMOps 実践における設計・実装・運用スキルが包括的に評価されます。

- **試験時間**: 130 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（1つの正解）、複数選択問題（2つ以上の正解）
- **合格基準点**: 100〜1,000 点中 720 点以上
- **推奨される前提知識**: 
  - Amazon SageMaker AI や Amazon Bedrock をはじめとする AWS サービスを利用した ML エンジニアリングの実務経験 1 年以上
  - バックエンド開発、DevOps、データエンジニアリング、データサイエンス分野における実務経験 1 年以上
  - 従来の機械学習（Scikit-learn, XGBoost, PyTorch, TensorFlow）と生成 AI / 基盤モデル（Transformer, RAG, AI エージェント）の双方に関する実践的知識

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 |
| :--- | :--- | :--- | :--- |
| **Domain 1** | ML と AI のためのデータの準備 | 28% | S3, Glue, Glue DataBrew, Glue Data Quality, EMR Spark, SageMaker Data Wrangler, Feature Store, Kinesis, Flink, OpenSearch Service (Vector Search), pgvector, Ground Truth, Clarify (Bias) |
| **Domain 2** | ML モデルと基盤モデル (FM) の開発 | 24% | Bedrock (FM Selection), SageMaker AI (組み込みアルゴリズム, Script Mode, AMT), 分散トレーニング, MLflow, Bedrock Evaluation, LLM-as-a-judge, Clarify (Explainability), NLPメトリクス (ROUGE/BLEU/BERTScore) |
| **Domain 3** | ML と AI のワークフローのデプロイとオーケストレーション | 24% | SageMaker 推論エンドポイント (Real-time, Serverless, Async, Batch Transform), Bedrock Provisioned Throughput, Bedrock Agents & AgentCore, Bedrock Knowledge Bases (RAG, Rerank), CodePipeline, SageMaker Pipelines, Model Registry |
| **Domain 4** | ML と AI のソリューションの運用、モニタリング、保護 | 24% | CloudWatch GenAI Observability, SageMaker Model Monitor (Data/Model Drift), Bedrock AgentCore Observability, X-Ray, EC2/Inf2/G5 インスタンス選定, Bedrock Guardrails, IAM, KMS, VPC PrivateLink, Inspector |

---

## 3. MLA-C01 から MLA-C02 への主要改定ポイント

MLA-C02 は、前世代（MLA-C01）と比較して、特に生成 AI、基盤モデル (FM)、および自律型エージェント (Agentic AI) の運用エンジニアリングが大幅に強化されています。

1. **エージェンティック AI とオーケストレーションの本格導入**:
   - Amazon Bedrock Agents および AgentCore のデプロイ、ツール連携プロトコル、エージェントステート管理の実装
   - オーケストレーション障害の検知、ストリーミング切断（Truncated Streaming）、ツール呼び出し失敗の監視
2. **RAG (検索拡張生成) とベクトルデータベースのライフサイクル**:
   - Amazon Bedrock Knowledge Bases、Amazon OpenSearch Service、Amazon RDS (pgvector) の設定とインデックス最適化
   - チャンキング戦略、ハイブリッド検索、再ランク付け (Rerank)、ナレッジベース同期パイプライン
3. **基盤モデルの評価・テストフレームワーク**:
   - Amazon Bedrock Model Evaluation、LLM-as-a-judge、NLP 評価メトリクス（ROUGE, BLEU, BERTScore）の実装
   - Amazon Bedrock Prompt Management を活用したプロンプトのバージョニングとテスト自動化
4. **生成 AI のコスト・オブザーバビリティ・多層防御**:
   - CloudWatch 生成 AI オブザーバビリティ、トークン消費・埋め込み計算コストの可視化
   - Amazon Bedrock Guardrails による拒否トピック、有害単語、個人情報 (PII) マスキング、プロンプトインジェクション防御

---

## 4. ドメイン別タスクおよび学習ロードマップ

### Domain 1: ML と AI のためのデータの準備 (28%)
- **Task 1.1: データを収集して保存する**
  - 多様なデータソース（S3, EBS, EFS, RDS, DynamoDB, OpenSearch Service）からの効率的抽出
  - コスト・性能・コンプライアンスに基づくストレージ選定と容量トラブルシューティング
  - ストリーミング取り込み（Amazon Kinesis, Amazon Managed Service for Apache Flink）
  - 最適フォーマット選定（Apache Parquet, JSON, CSV, ORC）とマルチソースデータ結合（AWS Glue, Spark）
  - スケーラブルなベクトルデータベースのセットアップ（OpenSearch Service, pgvector, S3）
  - マルチモーダルデータ（テキスト、画像、音声）の取り込み・保存と SageMaker Feature Store への登録
- **Task 1.2: データ変換、特徴量エンジニアリング、前処理を実行する**
  - AWS 変換ツール（AWS Glue, Glue DataBrew, EMR Spark, SageMaker Data Wrangler）の選定とパイプライン構築
  - SageMaker Feature Store によるオフライン・オンライン特徴量管理
  - ストリーミングデータ変換（AWS Lambda, Spark Streaming）
  - 数値・カテゴリカル特徴量エンジニアリング（標準化、スケーリング、ビニング、One-Hot Encoding、ログ変換）
  - テキストおよび画像データの埋め込み（Embedding）モデル適用と数値表現化
  - 高度なテキスト前処理（トークン化、正規化、語幹抽出、ストップワード除去）
  - RAG アプリケーション向けドキュメント処理（固定長/セマンティックチャンキング、メタデータ付与）
  - データのマスキング、編集、匿名化（PII 除去）
  - FM ファインチューニング、継続的事前学習、モデル蒸留のためのデータセット整形（プロンプト・補完ペア、JSONL）
- **Task 1.3: データ品質を検証し、バイアスを管理する**
  - AWS Glue Data Quality および DataBrew を用いたデータプロファイリングと検証ルール設定
  - Amazon SageMaker Ground Truth を活用したデータラベリング・注釈パイプライン
  - 訓練データのバイアスソース特定と軽減手法（データセット分割、層化抽出、データ拡張）
  - 数値・テキスト・画像アセットに対するバイアスメトリクス計測（不均衡比率、条件付き受容率等）
  - クラス不均衡の是正（SMOTE、アンダーサンプリング、クラス重み付け損失）
  - AI トレーニングデータの整合性検証（プロンプト-レスポンスペア検証、コンテンツ安全性スクリーニング）
  - データクリーニング（外れ値検出、欠損値補完、重複排除）

### Domain 2: ML モデルと基盤モデル (FM) の開発 (24%)
- **Task 2.1: ML と AI のソリューションに適したモデリングアプローチを選択する**
  - タスク要件・性能基準に基づく Amazon Bedrock FM（Claude, Titan, Llama 等）の選定
  - FM のカスタマイズ戦略判断（Prompt Engineering vs RAG vs Fine-tuning vs Continued Pre-training）
  - 従来の機械学習、深層学習、基盤モデル、マネージド AI サービスの比較検討とトレードオフ判断
  - マネージド AI サービス（Textract, Rekognition, Comprehend, Transcribe, Polly, Lex）の適応
  - RAG アーキテクチャパターンの選定（ベーシック RAG、アドバンスト RAG、エージェント連携 RAG）
  - 精度、推論レイテンシ、トレーニング時間、インフラコストのトレードオフ評価
- **Task 2.2: ML と AI のソリューションのモデルをトレーニング、ファインチューニング、カスタマイズする**
  - Amazon SageMaker AI 組み込みアルゴリズム（XGBoost, Linear Learner, Image Classification, DeepAR 等）の選定と適用
  - SageMaker スクリプトモードによるカスタム学習（PyTorch, TensorFlow, Hugging Face）
  - 自動モデルチューニング (AMT) によるベイズ最適化ハイパーパラメータ探索
  - トレーニング時間短縮技術（早期停止 Early Stopping、SageMaker 分散データ並列・モデル並列）
  - 過学習 (Overfitting)・未学習 (Underfitting)・壊滅的忘却 (Catastrophic Forgetting) の防止技術（正則化、ドロップアウト、LoRA/PEFT）
  - アンサンブル学習および複数モデルのパイプライン統合
  - 基本ハイパーパラメータ調整（Learning Rate, Batch Size, Epochs, Warmup Steps）
  - 検索コンポーネント（ベクトル検索、BM25）および埋め込みモデルのファインチューニング
- **Task 2.3: ML と AI のシステムのパフォーマンスを分析および評価する**
  - 再現可能な実験管理（SageMaker AI 上の MLflow、Amazon Bedrock 評価、Bedrock Prompt Management）
  - モデルベースライン作成と性能ドリフト検出のセットアップ
  - シャドウバリアント (Shadow Deployment) による本番トラフィックでの性能検証
  - モデル説明可能性の解析（SageMaker Clarify、SHAP 値、特徴量アトリビューション）
  - モデル収束障害のデバッグ（勾配消失/爆発、損失関数の挙動解析）
  - 包括的評価手法（混同行列、ROC-AUC、PR-AUC、Log Loss、RMSE、MAPE）
  - 人間による評価（Human-in-the-Loop / Amazon A2I、テキスト品質評価）
  - NLP 評価メトリクス（ROUGE-1/2/L, BLEU, BERTScore, コサイン意味的類似度）
  - AI 評価フレームワーク（LLM-as-a-judge、毒性・ハルシネーション検証、バイアス検出）
  - RAG システム評価（忠実性 Faithfulness、回答関連性 Answer Relevance、コンテキスト適合性 Context Precision/Recall）

### Domain 3: ML と AI のワークフローのデプロイとオーケストレーション (24%)
- **Task 3.1: ML と AI のモデルタイプのデプロイインフラストラクチャを管理する**
  - 推論要件に応じたコンピューティング選定（SageMaker Real-time, Serverless, Asynchronous, Batch Transform）
  - マルチモデルエンドポイント (MME) およびマルチコンテナエンドポイント (MCE) によるリソース集約
  - 基盤モデルのホスティング選定（Amazon Bedrock オンデマンド / プロビジョンドスループット、SageMaker JumpStart）
  - AWS 外部で学習されたモデルのインポート（Amazon Bedrock Custom Model Import、SageMaker BYOM）
  - エージェントワークフローのデプロイ（Amazon Bedrock Agents、AgentCore、OpenAPI スキーマ定義、Action Group）
  - RAG システムの推論設定（ハイブリッド検索、Cohere Rerank 等の再ランク付け統合）
- **Task 3.2: 既存のアーキテクチャと要件に基づいて ML と AI のワークロードのリソースをプロビジョニングして設定する**
  - オンデマンド vs プロビジョンドリソースの最適化（コスト・コールドスタート・レイテンシの均衡）
  - コンテナイメージの構築と管理（Amazon ECR、SageMaker Deep Learning Containers）
  - VPC ネットワーク内へのセキュアなエンドポイント配置（AWS PrivateLink、インターフェイス VPC エンドポイント）
  - プログラマティックなデプロイ自動化（SageMaker Python SDK, Boto3, AWS CDK, CloudFormation）
  - 推論自動スケーリングポリシーの設定（TargetTrackingScaling, InvocationsPerInstance, GPUUtilization）
  - Amazon Bedrock ナレッジベースの作成・管理（ベクトルインデックス同期、OpenSearch Serverless 設定）
  - エージェントステート管理システムの実装（Amazon DynamoDB、AgentCore Session 管理）
  - GPU ワークロード向けスケーリング設定
- **Task 3.3: MLOps と AI のワークロードのための、自動オーケストレーション、継続的インテグレーションおよび継続的デリバリー (CI/CD) パイプラインを実装する**
  - デプロイ戦略の実装（Blue/Green デプロイ、カナリアデプロイ、リニアデプロイ）と CloudWatch アラーム連動の自動ロールバック
  - AWS デベロッパーツールの統合（AWS CodePipeline, CodeBuild, CodeDeploy, CodeConnections）
  - Amazon SageMaker Pipelines による再トレーニングパイプラインの自動化
  - CI/CD パイプライン内での自動テスト（ユニットテスト、データ検証テスト、モデル品質ゲート）
  - モデルのバージョン管理とガバナンス（Amazon SageMaker Model Registry、MLflow）
  - Amazon Bedrock Prompt Management によるプロンプトのバージョニングとテスト自動化
  - エージェント自動デプロイパイプラインとエージェントバージョニング（DRAFT とエイリアス）
  - RAG 更新サイクルおよびナレッジベース自動同期パイプライン（S3 イベント -> EventBridge -> Lambda/Step Functions）

### Domain 4: ML と AI のソリューションの運用、モニタリング、保護 (24%)
- **Task 4.1: ML と AI のモデルの推論とパフォーマンスをモニタリングする**
  - 本番モデルのパフォーマンス監視（Amazon CloudWatch 生成 AI オブザーバビリティ、Bedrock モデル評価）
  - SageMaker Model Monitor による 4 大ドリフト検出（Data Quality, Model Quality, Bias Drift, Feature Attribution Drift）
  - 本番環境での A/B テストとトラフィックルーティング監視（Production Variants）
  - エージェントのオーケストレーション監視（ルーティング障害、切り取られたストリーミング Truncated Streaming、ツール呼び出しタイムアウト/例外）
  - FM 固有のメトリクス監視（Latency, Token Count, Error Rates, Throttling）
- **Task 4.2: ML と AI のインフラストラクチャのコストとパフォーマンスを最適化および管理する**
  - 推論インスタンスファミリーの適正化（AWS Inferentia / Inf2, GPU / G5, CPU / C6i/C7g）
  - オブザーバビリティツールの活用（Amazon CloudWatch、Amazon Bedrock AgentCore Observability、AWS X-Ray）
  - コスト最適化ツールの活用（AWS Cost Explorer, AWS Budgets, Compute Optimizer, Savings Plans, スポットインスタンス）
  - 基盤モデル推論コストの最適化（Prompt Caching、バッチ推論、モデル蒸留）
  - AI 固有のコストパターン監視（入力/出力トークン比率、埋め込み計算コスト、OpenSearch ベクトルストレージ容量最適化）
- **Task 4.3: ML と AI のワークロードとモデルエンドポイントのセキュリティを確保する**
  - CI/CD パイプラインのセキュリティ検証（Amazon CodeGuru Reviewer/Security、Amazon Inspector によるコンテナ脆弱性スキャン）
  - 最小権限の IAM ポリシーおよび実行ロール設計（SageMaker Execution Role, Bedrock Invocation Role）
  - 包括的監査・コンプライアンスログ（AWS CloudTrail による API 履歴記録、AWS Config による設定ドリフト検知）
  - VPC 閉域ネットワークアーキテクチャ（インターネット非公開サブネット、S3/Bedrock/SageMaker 向け VPC エンドポイント、セキュリティグループ統制）
  - 生成 AI 固有の脅威対策（プロンプトインジェクション、データ抽出攻撃、ハルシネーション悪用）
  - FM アクセスの認証方式選定（IAM 認証、Bedrock API キー / STS 一時クレデンシャル）
  - Amazon Bedrock Guardrails の実装（拒否トピック、有害コンテンツフィルター、PII マスキング、コンテキストグラウンディング検証）

---

## 5. 推奨学習ロードマップとマイルストーン

1. **Phase 1: データエンジニアリングと特徴量基盤 (Domain 1: 28%)**
   - S3 / Glue / EMR Spark によるデータパイプライン構築
   - SageMaker Feature Store、Data Wrangler による前処理とバイアス管理（Clarify）
   - テキスト/画像のベクトル埋め込みと OpenSearch Service / pgvector への格納
2. **Phase 2: モデル開発・カスタマイズ・評価 (Domain 2: 24%)**
   - 組み込みアルゴリズムとスクリプトモード、AMT によるハイパーパラメータ探索
   - Amazon Bedrock FM 選定と適応判断（Prompt vs RAG vs Fine-tuning）
   - モデル評価メトリクス（ROUGE/BLEU/BERTScore）と Bedrock Evaluation / LLM-as-a-judge 実装
3. **Phase 3: デプロイ・オーケストレーション・MLOps (Domain 3: 24%)**
   - SageMaker 4大推論エンドポイント（Real-time, Serverless, Async, Batch）の使い分け
   - Bedrock Agents / AgentCore によるツール連携・ステート管理
   - Bedrock Knowledge Bases による高度な RAG パイプライン（チャンキング・再ランク付け）
   - SageMaker Pipelines、Model Registry、CodePipeline による自動 CI/CD・ロールバック
4. **Phase 4: 運用監視・コスト最適化・多層防御 (Domain 4: 24%)**
   - SageMaker Model Monitor によるデータ/モデルドリフト自動検知
   - Bedrock AgentCore Observability / CloudWatch によるストリーミング障害・ツール例外追跡
   - インスタンス選定（Inf2 / G5）と Prompt Caching によるコスト削減
   - VPC PrivateLink 閉域化と Amazon Bedrock Guardrails によるセーフガード構築
