# Google Cloud Certified - Generative AI Leader 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Generative AI Leader（生成 AI リーダー）
- **公式試験ガイド**: [Generative AI Leader 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/generative_ai_leader_exam_guide_japanese.pdf?hl=ja)
- **公式学習ガイド**: [Generative AI Leader Study Guide (Workbook / 英語版)](https://services.google.com/fh/files/misc/generative_ai_leader_study_guide_english.pdf?hl=ja)
- **最終更新日**: 2026-10-12

---

## 1. 試験の概要と基本スペック

Google Cloud Certified 生成 AI リーダー（Generative AI Leader）は、生成 AI がどのように企業を変革し、組織内でどう戦略的に活用されているかを包括的に理解しているビジネス＆テクノロジーリーダーを認定する資格です。

Google Cloud の生成 AI プロダクトおよびサービス（Gemini、Agent Platform、Customer Engagement Suite、事前トレーニング済み API 群など）に関するビジネスレベルの知識を有し、技術チームと非技術チームの橋渡しとなって責任ある革新的な AI ソリューションの導入・ユースケース創出を主導する能力を評価します。本認定の主眼は戦略的リーダーシップ、ビジネス価値の最大化、ガバナンスとリスク管理であり、詳細なモデルコーディングや技術的実装そのものは対象外です。

- **試験時間**: 90 分
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題、複数選択問題
- **合否判定**: 合格 / 不合格（スコア非開示）
- **前提知識**: 生成 AI・機械学習の基本概念、ビジネス課題への適用判断、Google Cloud の主要生成 AI サービス（Gemini アプリ、Gemini Enterprise、Agent Platform、各種事前構築済み API）、プロンプトエンジニアリング、グラウンディング/RAG、および Google のセキュア AI フレームワーク（SAIF）や責任ある AI の原則に関する理解。プログラミングや低レイヤのモデル実装経験は不要です。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 4 セクションで構成されています。Google Cloud の生成 AI サービス群（約 35%）と基礎理論（約 30%）が試験の過半を占め、モデル出力改善技術（約 20%）およびビジネス戦略・セキュリティ（約 15%）から構成されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | 生成 AI の基礎 (Fundamentals of Generative AI) | 約 30% | AI/ML/生成AI/基盤モデルの定義、学習アプローチ（教師あり/なし/強化学習）、MLライフサイクル、データ品質・アクセシビリティ、構造化/非構造化データ、基盤モデル（Gemini, Gemma, Imagen, Veo）、生成AIの主要5レイヤ |
| **Section 2** | Google Cloud の生成 AI サービス (Google Cloud's Generative AI Offerings) | 約 35% | AI-Firstアプローチ、エンタープライズ基盤、AI Hypercomputer（TPU/GPU）、Geminiアプリ/Advanced/Gems、Gemini for Workspace、Gemini Enterprise / Gemini Notebook、Customer Engagement Suite（CCaaS, Conversational Agents, Agent Assist, Conversational Insights）、Agent Platform（Model Garden, Agent Search, AutoML）、エージェントツール（Extensions, Functions, Data Stores, Plugins）、各種事前構築済み API（Speech, Document, Translation, Vision, Video, Natural Language）、Agent Studio vs Google AI Studio |
| **Section 3** | 生成 AI モデル出力を改善する手法 (Techniques to Improve Gen AI Model Output) | 約 20% | 基盤モデルの限界（ナレッジカットオフ、ハルシネーション、バイアス、エッジケース）、改善手法（プロンプト、グラウンディング、RAG、ファインチューニング、HITL）、プロンプト手法（Zero/One/Few-shot、Role、Chaining、CoT、ReAct）、自社/サードパーティ/ワールドデータのグラウンディング、RAG API、サンプリングパラメータ（Temperature, Top-P, Safety Settings） |
| **Section 4** | 生成 AI ソリューションを成功に導くビジネス戦略 (Business Strategies for a Successful Gen AI Solution) | 約 15% | 導入検討要素（ニーズ分析: スケール、カスタマイズ、レイテンシ、プライバシー、接続性 / リソース: 人材、予算、時間）、戦略的アプローチ（Top-down × Bottom-up）、ビジネス影響度測定（ROI, KPI）、セキュア AI フレームワーク（SAIF）、多層防御（IAM, Security Command Center）、責任ある AI（透明性、説明可能性、バイアス・公平性、プライバシー・匿名化） |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: 生成 AI の基礎（約 30%）
- **出題の狙い**: 人工知能（AI）、機械学習（ML）、深層学習、生成 AI、基盤モデルの概念的包含関係、学習アプローチの相違、MLライフサイクルの各段階、AIにおけるデータの重要性（品質・構造・アクセシビリティ）、生成 AI ランドスケープの 5 レイヤ、および Google の主要基盤モデル（Gemini、Gemma、Imagen、Veo）の特性理解を検証します。
- **主要タスク**:
  - Task 1.1: 生成 AI の中心的なコンセプトとユースケースを説明する（AI/ML/生成AI/基盤モデル/マルチモーダル/拡散モデル/LLM、教師あり/教師なし/強化学習、MLライフサイクルの各ステージと対応ツール、基盤モデル選択基準、ビジネスユースケース分類: 作成・要約・検出・自動化）
  - Task 1.2: 生成 AI で使用されるさまざまなデータタイプと、それらがビジネスに与える影響を説明する（データ品質の特性: 完全性・整合性・関連性・可用性・費用・形式、構造化データ vs 非構造化データ、ラベル付き vs ラベルなしデータ）
  - Task 1.3: 生成 AI を取り巻く環境の主要な 5 レイヤと、それらがビジネスに与える影響を特定する（インフラストラクチャ、モデル、プラットフォーム、エージェント、アプリケーション）
  - Task 1.4: Google の基盤モデルのユースケースと強みを特定する（Gemini: マルチモーダル汎用モデル、Gemma: 軽量オープンモデル、Imagen: 高解像度画像生成モデル、Veo: 高品質動画生成モデル）
- **重要キーワード**: Artificial Intelligence (AI), Machine Learning (ML), Generative AI, Foundation Models, Multimodal, Diffusion Models, Large Language Models (LLMs), Supervised / Unsupervised / Reinforcement Learning, ML Lifecycle, Structured vs Unstructured Data, Data Quality & Accessibility, 5 Layers of Gen AI Landscape, Gemini, Gemma, Imagen, Veo

#### Section 2: Google Cloud の生成 AI サービス（約 35%）
- **出題の狙い**: Google の AI ファースト企業としての強み、エンタープライズ対応のセキュリティとガバナンス、専用インフラ（AI Hypercomputer、TPU、GPU）、業務生産性向上ツール（Gemini アプリ、Gemini Advanced、Gems、Gemini for Google Workspace、Gemini Enterprise、Gemini Notebook）、顧客接点改革（Customer Engagement Suite、CCaaS、Conversational Agents、Agent Assist、Conversational Insights）、開発者・企業向けプラットフォーム（Agent Platform、Model Garden、Agent Search、AutoML）、およびエージェントを支えるツール連携と事前構築済み API 群の適材適所の選定能力を検証します。
- **主要タスク**:
  - Task 2.1: 生成 AI 分野における Google Cloud の強みを説明する（AI ファーストのアプローチ、エンタープライズ対応 [責任性、安全性、プライバシー、スケーラビリティ]、包括的エコシステム、オープンアプローチ、AI Hypercomputer / TPU / GPU、AI 開発の民主化）
  - Task 2.2: AI を活用した業務を Google Cloud の事前構築済み生成 AI サービスで実現する方法を説明する（Gemini アプリ、Gemini Advanced、Gems、Gemini Enterprise、Gemini Notebook、Gemini for Google Workspace）
  - Task 2.3: Google Cloud の生成 AI サービスでカスタマーエクスペリエンスを向上させる方法を説明する（Agent Search、Google 検索グラウンディング、Customer Engagement Suite、Conversational Agents、Agent Assist、Conversational Insights、Google Cloud Contact Center as a Service [CCaaS]）
  - Task 2.4: Google Cloud で開発者による AI を活用した構築を促進する方法について説明する（Agent Platform、Model Garden、Agent Search、AutoML、事前構築済み RAG、RAG API、カスタムエージェント構築）
  - Task 2.5: 生成 AI エージェント用ツールの目的と種類を定義する（ツール分類: 拡張機能、関数、データストア、プラグイン、連携 Google Cloud サービス & 事前構築済み AI API: Speech-to-Text、Text-to-Speech、Translation、Document Translation、Document AI、Cloud Vision、Cloud Video Intelligence、Natural Language API、Cloud Storage、Cloud Run、Cloud Functions、Agent Studio vs Google AI Studio の使い分け）
- **重要キーワード**: AI-First Approach, AI Hypercomputer (TPU v5p/v5e, NVIDIA GPU), Gemini App & Gemini Advanced, Gems, Gemini Enterprise, Gemini Notebook, Gemini for Google Workspace, Customer Engagement Suite (CCaaS, Conversational Agents, Agent Assist, Conversational Insights), Agent Platform (Model Garden, Agent Search, AutoML), RAG API, Agent Tools (Extensions, Functions, Data Stores, Plugins), Pre-trained AI APIs (Speech, Document, Translation, Vision, Video, Natural Language), Agent Studio vs Google AI Studio

#### Section 3: 生成 AI モデル出力を改善する手法（約 20%）
- **出題の狙い**: 基盤モデル固有の限界（知識のカットオフ、ハルシネーション、データバイアス、エッジケース）を正しく認識し、ビジネス要件・精度要件に応じて最適な出力改善手法（プロンプトエンジニアリング、グラウンディング、RAG、ファインチューニング、人間参加型 [HITL]）を選択・適用する能力、およびモデルの継続的監視・サンプリングパラメータ制御の理解を検証します。
- **主要タスク**:
  - Task 3.1: 基盤モデルの限界に事前に対処する方法について説明する（限界の特定: データの依存関係、ナレッジカットオフ、バイアス、公平性、ハルシネーション、エッジケース。対策技術: グラウンディング、RAG、プロンプト、ファインチューニング、HITL [コンテンツモデレーション、高リスク判断、事前・事後レビュー]。継続的モニタリングと評価: モデル自動アップグレード、KPI、セキュリティパッチ、バージョニング [Model Registry]、ドリフトモニタリング [Model Monitoring]、Agent Platform Feature Store、Pipelines）
  - Task 3.2: プロンプトエンジニアリングの手法と、それがどうより良い結果につながるかについて説明する（プロンプトの定義と重要性、基本手法: ゼロショット、ワンショット、少数ショット [Few-shot]、ロールプロンプト、プロンプトチェーン。高度手法: Chain-of-Thought [CoT]、ReAct、メタプロンプティング。効率化: プロンプト再利用、Gems）
  - Task 3.3: グラウンディング手法とそのユースケースを特定する（自社データ、サードパーティデータ、ワールドデータによるグラウンディングの違い、RAGの4ステップ [検索、拡張、生成、反復]、Google Cloud のグラウンディングサービス [Agent Search、RAG API、Google 検索]、サンプリングパラメータ: トークン数、温度 [Temperature]、Top-P [Nucleus サンプリング]、安全性設定、出力の長さ）
- **重要キーワード**: Knowledge Cutoff, Hallucination, Bias & Fairness, Edge Cases, Grounding, Retrieval-Augmented Generation (RAG), Fine-Tuning, Human-in-the-Loop (HITL), Model Registry, Model Monitoring, Feature Store, Prompt Engineering (Zero-shot, Few-shot, Role, Prompt Chaining), Chain-of-Thought (CoT), ReAct (Reason + Act), Temperature, Top-P, Safety Settings

#### Section 4: 生成 AI ソリューションを成功に導くビジネス戦略（約 15%）
- **出題の狙い**: 組織において生成 AI を机上のPoCで終わらせず、持続可能なビジネス価値創出につなげるための導入戦略、ニーズとリソースの多面的評価、組織統合プロセス（トップダウンとボトムアップの融合）、効果測定指標、Google のセキュア AI フレームワーク（SAIF）に基づくセキュリティ対策、および責任ある AI（透明性、公平性、プライバシー、説明可能性）の原則に則ったガバナンス構築能力を検証します。
- **主要タスク**:
  - Task 4.1: 革新的な生成 AI ソリューションを適切に導入するための、Google Cloud で推奨されるステップを説明する（生成 AI ソリューション種別の把握、ニーズ検討項目 [スケール、カスタマイズ度、ユーザー対話、プライバシー、レイテンシ、接続性]、リソース評価 [人材、予算、期間]、ソリューション選定基準 [モダリティ、コンテキストウィンドウ、性能、可用性/信頼性]、組織統合アプローチ [トップダウン戦略ビジョン × ボトムアップ現場探索]、影響度測定手法 [ROI、業務時間削減、満足度向上]）
  - Task 4.2: 安全な AI と、AI システムを悪意のある攻撃や不正使用から保護することの重要性を定義する（MLライフサイクル全体のセキュリティ、Google セキュア AI フレームワーク [SAIF] の目的と6原則、Google Cloud セキュリティツール [安全設計インフラ、IAM、Security Command Center、ワークロードモニタリング]）
  - Task 4.3: ビジネスにおける責任ある AI の重要性を説明する（責任ある AI と透明性、Google AI 原則、プライバシー保護 [匿名化、仮名化]、データ品質・バイアス・公平性の管理、AI システムにおけるアカウンタビリティと説明可能性 [Explainability]）
- **重要キーワード**: Gen AI Strategy, Top-down & Bottom-up Approach, Solution Assessment (Needs & Resources), Business Impact & ROI, Secure AI Framework (SAIF), Cloud IAM, Security Command Center (SCC), Responsible AI, Google AI Principles, Transparency & Explainability, Bias & Fairness, Privacy (Anonymization, Pseudonymization), Accountability
