# AWS Certified AI Practitioner (AIF-C01) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified AI Practitioner
- **試験コード**: AIF-C01
- **公式試験ガイド**: [AWS Certified AI Practitioner (AIF-C01) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/ai-practitioner-01/ai-practitioner-01.html)
- **最終更新日**: 2026-10-04

---

## 1. 試験の概要と基本スペック

AWS Certified AI Practitioner (AIF-C01) は、人工知能 (AI)、機械学習 (ML)、および生成 AI (GenAI) の基本概念と、AWS 上での実践的な AI サービス活用に関する基礎的な知識・判断力を実証する認定資格です。
従来の機械学習モデルと最新の基盤モデル (FM) の特性を見極め、ビジネス課題に対して最適な AI アーキテクチャを安全かつ倫理的に適用する能力が問われます。

- **試験時間**: 120 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題、複数選択問題、並べ替え問題、内容一致問題
- **合格基準点**: 100〜1,000 点中 700 点以上
- **前提知識**: AWS クラウドおよび AI/ML 技術に関する 6 か月未満の実務・学習経験。モデル開発やコーディングの実装経験は必須とされず、ビジネスへの適用判断が中心となります。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Domain 1** | AI と ML の基礎 | 20% | Amazon SageMaker AI, Rekognition, Comprehend, Transcribe, Polly, Lex, 教師あり/なし学習, 推論種別 | 完了 |
| **Domain 2** | GenAI の基礎 | 24% | Amazon Bedrock, Bedrock AgentCore, Transformer, トークン/埋め込み, FMライフサイクル, エージェンティックAI | 完了 |
| **Domain 3** | 基盤モデルの応用 | 28% | Bedrock Knowledge Bases, Prompt Engineering, OpenSearch Service, RAG, ファインチューニング, 評価指標 | 完了 |
| **Domain 4** | 責任ある AI に関するガイドライン | 14% | Amazon Bedrock Guardrails, SageMaker Model Cards, SageMaker Clarify, バイアス・公平性, HITL | 完了 |
| **Domain 5** | AI ソリューションのセキュリティ、コンプライアンス、ガバナンス | 14% | AWS IAM, AWS KMS, Amazon Macie, AWS PrivateLink, CloudTrail, AWS Config, AWS 責任共有モデル | 完了 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

### Domain 1: AI と ML の基礎 (20%)
- **Task 1.1**: AI の基本的な概念と用語を説明する（AI/ML/深層学習/LLM/GenAI/エージェンティックAIの境界、推論パターン、データ種別、学習アプローチ）
- **Task 1.2**: AI の実用的なユースケースを特定する（価値創出領域、AI不適格ユースケースの特定、課題タイプに応じた手法選定、マネージドAIサービスの選定、従来ML vs FMの判断）
- **Task 1.3**: AI/ML 開発ライフサイクルについて説明する（パイプライン構成、FMの調達元、推論ホスティング方式、MLOps基礎、モデル評価メトリクスとビジネスメトリクス）

### Domain 2: GenAI の基礎 (24%)
- **Task 2.1**: 生成 AI (GenAI) の基本概念を説明する（トークン、チャンク化、埋め込み、ベクトル、トランスフォーマー、基盤モデル、トークン課金体系、コンテキストエンジニアリング、エージェンティックAIとMCP）
- **Task 2.2**: ビジネス上の問題の解決に GenAI を使用する場合の可能性と制限を理解する（適応性とコンテンツ生成の強み、ハルシネーション・非決定性・ブラックボックスの制約、モデル選定要素、ビジネスROI指標）
- **Task 2.3**: GenAI アプリケーションを構築するための AWS インフラストラクチャとテクノロジーについて説明する（Amazon Bedrock、SageMaker AI、SageMaker JumpStart、Bedrock AgentCore、Trainium/Inferentia、コスト・可用性・レイテンシのトレードオフ）

### Domain 3: 基盤モデルの応用 (28%)
- **Task 3.1**: 基盤モデル (FM) を使用するアプリケーションの設計上の考慮事項を説明する（モデル選定基準、推論パラメータ、RAGアーキテクチャ、ベクトルDB選定、モデル適応の梯子、AIエージェント連携）
- **Task 3.2**: 効果的なプロンプトエンジニアリング手法を選択する（プロンプト構成、Zero-shot / Few-shot / Chain-of-Thought、ベストプラクティス、敵対的攻撃リスク、Bedrock Prompt Management）
- **Task 3.3**: FM のトレーニングとファインチューニングのプロセスを説明する（事前学習、ファインチューニング、継続的事前学習、蒸留、RLHF、学習用データセット準備）
- **Task 3.4**: FM のパフォーマンスを評価する方法を説明する（HITL評価、ROUGE / BLEU / BERTScore / LLM-as-a-judge、Bedrock Model Evaluation、ビジネスKPI整合性）

### Domain 4: 責任ある AI に関するガイドライン (14%)
- **Task 4.1**: 責任ある AI システムの開発について説明する（公平性、バイアス、堅牢性、透明性、環境持続可能性、法的リスク・知的財産保護、Amazon Bedrock Guardrailsによる保護、SageMaker Clarify）
- **Task 4.2**: 透明性の高い説明可能なモデルの重要性を認識する（説明可能性とブラックボックスの対比、Amazon SageMaker Model Cards、安全性 vs 透明性のトレードオフ、人間中心設計）

### Domain 5: AI ソリューションのセキュリティ、コンプライアンス、ガバナンス (14%)
- **Task 5.1**: AI システムを保護する方法を説明する（IAMロール・最小権限、KMS暗号化、Amazon Macieによる機密データ保護、AWS PrivateLink閉域接続、プロンプトインジェクション防御、RAGグラウンディング、AI操作監査ログ）
- **Task 5.2**: AI システムのガバナンスとコンプライアンス規制を認識する（AWS 責任共有モデル、AWS CloudTrail、AWS Config、AWS Artifact、データライフサイクル・レジデンシー統制、生成AIセキュリティスコーピングマトリックス）
