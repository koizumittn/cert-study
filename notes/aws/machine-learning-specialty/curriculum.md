# AWS Certified Machine Learning - Specialty (MLS-C01) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Machine Learning - Specialty
- **試験コード**: MLS-C01
- **公式試験ガイド**: [AWS Certified Machine Learning - Specialty (MLS-C01) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/machine-learning-specialty-01/machine-learning-specialty-01.html)
- **最終更新日**: 2026-10-11

---

## 1. 試験の概要と基本スペック

AWS Certified Machine Learning - Specialty (MLS-C01) は、AWS クラウドにおける機械学習 (ML) ソリューションの設計、実装、デプロイ、保守を行う専門能力を検証するスペシャリティレベルの認定資格です。
データパイプラインの構築から探索的データ分析 (EDA)、特徴量エンジニアリング、機械学習アルゴリズムの選定とハイパーパラメータチューニング、分散トレーニング、推論エンドポイントのホスティング、そして監視とセキュリティに至る、機械学習ライフサイクル全体の実践的設計・トラブルシューティング能力が評価されます。

- **試験時間**: 180 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（1つの正解）、複数選択問題（2つ以上の正解）
- **合格基準点**: 100〜1,000 点中 750 点以上
- **推奨される前提知識**: 
  - AWS クラウドでの ML/深層学習ワークロードの開発、設計、実行に関する実務経験 1〜2 年以上
  - 基本的な機械学習アルゴリズム（線形モデル、ツリー系モデル、深層学習、クラスタリング、時系列分析、異常検知など）の基礎数理およびハイパーパラメータ最適化に関する知識
  - ML パイプラインの最適化、モデル評価（ROC-AUC、混同行列、F1 スコア、RMSE など）、および運用ベストプラクティスに関する経験

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Domain 1** | データエンジニアリング | 20% | Amazon S3, AWS Glue, Amazon EMR (Hadoop/Spark), Amazon Kinesis Data Streams, Amazon Data Firehose, Amazon Managed Service for Apache Flink, AWS Batch | 完了 |
| **Domain 2** | 探索的データ分析 | 24% | データサニタイズ（欠損値・外れ値処理）, 特徴量エンジニアリング（One-Hot, ビニング, TF-IDF, PCA）, Amazon SageMaker Ground Truth, 統計分析・可視化（相関, 箱ひげ図, エルボー図） | 完了 |
| **Domain 3** | モデリング | 36% | SageMaker 組み込みアルゴリズム（XGBoost, Linear Learner, DeepAR, RCF, BlazingText 等）, ハイパーパラメータ最適化 (AMT), 分散学習, モデル評価メトリクス (ROC-AUC, 混同行列, F1, RMSE) | 完了 |
| **Domain 4** | 機械学習の実装とその運用 | 20% | SageMaker 推論エンドポイント（リアルタイム, バッチ変換, MME, A/Bテスト）, AWS マネージド AI サービス（Rekognition, Comprehend, Transcribe, Polly, Textract, Lex）, CloudWatch, SageMaker Model Monitor, VPC, KMS, IAM | 完了 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

### Domain 1: データエンジニアリング (20%)
- **Task 1.1: ML 用のデータリポジトリを作成する**
  - データソースの特定（ログ、トランザクション、IoT、外部データセットなど）
  - ストレージメディアの選定（Amazon S3、Amazon EFS、Amazon EBS、Amazon FSx）
  - S3 のデータ階層化、暗号化、パーティショニング、およびアクセス制御
- **Task 1.2: データ取り込みソリューションを特定および実装する**
  - バッチロードとストリーミングのユースケース判別
  - ストリーミング取り込み基盤（Amazon Kinesis Data Streams, Amazon Data Firehose）
  - 低レイテンシストリーム処理（Amazon Managed Service for Apache Flink）
  - 外部データからのバッチ取り込みとオーケストレーション
- **Task 1.3: データ変換ソリューションを特定および実装する**
  - サーバーレス ETL 処理（AWS Glue、Glue ジョブブックマーク、DynamicFrame）
  - 分散処理フレームワーク（Amazon EMR、Apache Spark、Hadoop、Hive、MapReduce）
  - バッチコンピューティング処理（AWS Batch）

### Domain 2: 探索的データ分析 (24%)
- **Task 2.1: モデリング用のデータをサニタイズおよび準備する**
  - 欠損値の特定と補完手法（平均値/中央値/最頻値補完、モデル予測補完、行削除）
  - 外れ値の検出と処理（IQR 法、Z スコア、クリッピング、トリミング）
  - テキスト前処理（ストップワード除去、ステミング、レマタイゼーション、トークン化）
  - データ拡張（画像反転/回転、テキスト同義語置換）
  - ラベリング戦略と Amazon SageMaker Ground Truth / Amazon Mechanical Turk
- **Task 2.2: 特徴量エンジニアリングを実行する**
  - カテゴリカル変数の変換（One-Hot Encoding、Label Encoding、Target Encoding）
  - 数値変数のスケーリングと変換（Min-Max スケーリング、標準化 Z スコア、対数変換、ビニング）
  - テキスト特徴量抽出（Bag of Words、TF-IDF、N-gram、Word2Vec / 埋め込み）
  - 次元削減手法（主成分分析 PCA、t-SNE）
- **Task 2.3: ML のデータを分析および視覚化する**
  - 記述統計量の解釈（平均、分散、歪度、尖度、p 値）
  - データの可視化手法（散布図、ヒストグラム、箱ひげ図、時系列プロット、ヒートマップ）
  - クラスター分析と評価（k-means、階層型クラスタリング、エルボー図、シルエットスコア）

### Domain 3: モデリング (36%)
- **Task 3.1: 特定の ML 問題を適切な機械学習フレームワークおよびアプローチへと落とし込む**
  - 教師あり学習、教師なし学習、強化学習の判別
  - 回帰、二値分類、多クラス分類、クラスタリング、時系列予測、異常検知の定式化
- **Task 3.2: 特定の問題に対して適切なモデルを選択する**
  - Amazon SageMaker 組み込みアルゴリズムの選定：
    - 表形式データ: XGBoost、Linear Learner
    - テキスト・NLP: BlazingText (Word2Vec / Text Classification)、Object2Vec、Sequence-to-Sequence
    - 時系列: DeepAR
    - 異常検知: Random Cut Forest (RCF)、IP Insights
    - 画像処理: Image Classification、Object Detection、Semantic Segmentation
    - 教師なし/クラスタリング: K-Means、PCA、Factorization Machines、LDA、NTM
  - カスタムコードの持ち込み（Script Mode、BYOC: Bring Your Own Container）
- **Task 3.3: 機械学習モデルをトレーニングする**
  - SageMaker トレーニングジョブの構成（入力データチャネル: File Mode vs Pipe Mode vs Fast File Mode）
  - 分散トレーニング戦略（データ並列化 vs モデル並列化）
  - スポットインスタンス（Managed Spot Training）とチェックポイントによるコスト最適化
- **Task 3.4: ハイパーパラメータの最適化を実行する**
  - 自動モデルチューニング (AMT) と探索戦略（ベイズ最適化 vs ランダム探索）
  - 早期停止 (Early Stopping) の活用
  - 過学習防止と正則化技術（L1/L2 正則化、ドロップアウト、最大深度制約）
  - 学習率、バッチサイズ、エポック数の最適化
- **Task 3.5: ML モデルを評価する**
  - 評価指標の解釈：
    - 分類モデル: 混同行列、Accuracy、Precision、Recall、F1 スコア、ROC 曲線、AUC、PR 曲線
    - 回帰モデル: RMSE、MAE、MAPE、決定係数 (R^2)
    - 予測確率の閾値調整（ビジネス要件に基づく False Positive vs False Negative のトレードオフ）
  - バイアス・バリアンスのトレードオフ（過学習 vs 未学習の診断と対策）
  - 交差検証 (k-分割交差検証、層化抽出)
  - オフライン評価とオンライン評価 (A/B テスト)

### Domain 4: 機械学習の実装とその運用 (20%)
- **Task 4.1: パフォーマンス、可用性、スケーラビリティ、レジリエンス、耐障害性を備えた ML ソリューションを構築する**
  - SageMaker ホスティングアーキテクチャのマルチ AZ 冗長化
  - 推論エンドポイントの Auto Scaling 設定（ターゲット追跡スケーリング）
  - 適切なインスタンスタイプ選定（CPU vs GPU vs AWS Inferentia）
- **Task 4.2: 特定の問題に対して適切な ML サービスと特徴を推奨し、実装する**
  - AWS 高度 AI サービスの活用：
    - 自然言語: Amazon Comprehend、Amazon Translate
    - 音声: Amazon Transcribe、Amazon Polly
    - 画像・動画: Amazon Rekognition
    - ドキュメント解析: Amazon Textract
    - 対話型ボット: Amazon Lex
    - 検索・Q&A: Amazon Kendra、Amazon Q
- **Task 4.3: 基本的な AWS セキュリティプラクティスを ML ソリューションに適用する**
  - AWS Identity and Access Management (IAM) ロールと最小権限の原則
  - VPC ネットワーク分離（VPC 内でのノートブック・学習・推論実行、VPC エンドポイント/PrivateLink）
  - データの暗号化（保管時: AWS KMS / 転送時: TLS）
  - データマスキングと機密情報 (PII) の保護
- **Task 4.4: ML ソリューションをデプロイし、運用可能にする**
  - 推論デプロイメントパターンの選定（リアルタイム推論、バッチ変換、非同期推論、サーバーレス推論）
  - マルチモデルエンドポイント (MME) によるコスト削減
  - 安全な本番更新手法（Blue/Green デプロイ、カナリアデプロイ、A/B テスト）
  - Amazon SageMaker Model Monitor によるドリフト監視（データ品質ドリフト、モデル品質ドリフト）
  - AWS CloudTrail と Amazon CloudWatch によるログ監視とアラート
