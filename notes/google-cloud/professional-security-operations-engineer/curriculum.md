# Google Cloud Certified - Professional Security Operations Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Security Operations Engineer
- **試験コード**: PSOE
- **公式試験ガイド**: [Professional Security Operations Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_security_operations_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Security Operations Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/security-operations-engineer?hl=ja)
- **最終更新日**: 2026-10-17

---

## 1. 試験の概要と基本スペック

Professional Security Operations Engineer は、Google Cloud 上のワークロード、エンドポイント、マルチクラウド・オンプレミスを含むハイブリッドインフラに対するセキュリティ脅威を検知、監視、分析、調査し、迅速に対応・封じ込め・修復できる SOC（Security Operations Center）エンジニアおよびセキュリティ運用プロフェッショナルの能力を認定する資格です。

本試験では、Google Security Operations（旧 Chronicle SIEM および Siemplify SOAR を統合した Google SecOps プラットフォーム）、Security Command Center（SCC Enterprise / Premium）、Google Threat Intelligence（GTI / Mandiant / VirusTotal）を中核ツールとし、テレメトリーの優先順位付けと正規化（UDM: Unified Data Model）、YARA-L 2.0 による高度な相関検出ルールの開発、プロアクティブな脅威ハンティングと RetroHunt、SOAR プレイブックによるインシデントレスポンスの自動化、およびケース管理ライフサイクルの遂行能力が厳格に評価されます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **言語**: 日本語、英語
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: セキュリティ業界での 3 年以上の実務経験（Google Cloud セキュリティツールを使用した 1 年以上の運用・設計経験を含む）が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 6 セクションで構成されています。検出エンジニアリング（22%）、インシデント対応（21%）、脅威ハンティング（19%）の 3 分野が全体の 6 割以上を占め、これらを支えるプラットフォーム運用（14%）、データマネジメント（14%）、オブザーバビリティ（10%）が包括的に出題されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | プラットフォーム運用 | 約 14.0% | Google Security Operations (SecOps), Security Command Center (SCC Enterprise/Premium), Google Threat Intelligence (GTI), Cloud IDS, Cloud Audit Logs, Cloud IAM (SecOps/SCC ロール), Workforce Identity 連携, API キー / サービスアカウント自動化認証 |
| **Section 2** | データマネジメント | 約 14.0% | Chronicle Forwarder, Ingestion API, Cloud Logging シンク, UDM (Unified Data Model), デフォルト / カスタムパーサー, Parser Extension, Grok, ログ正規化, Log Types, Namespaces, ログコスト最適化・フィルタリング, エンティティコンテキスト, エイリアシング |
| **Section 3** | 脅威ハンティング | 約 19.0% | UDM Search, ログ分析 (Log Analytics / BigQuery), ログエクスプローラ, UEBA (ユーザー行動分析), GTI IOC 検索, SCC Toxic Combinations (有害な組み合わせ), エンティティリスクスコア, RetroHunt (遡及ハンティング), 脅威仮説検証 |
| **Section 4** | 検出エンジニアリング | 約 22.0% | YARA-L 2.0 構文 (events, match, condition, options), 複数イベント時間窓相関, 参照リスト (Reference Lists), キュレーテッド検出 (Curated Detections), SCC Security Health Analytics (SHA), SCC Event Threat Detection (ETD) カスタムモジュール, Entity Graph, 誤検知削減・除外ルール |
| **Section 5** | インシデント対応 | 約 21.0% | フォレンジック証拠保全 (ディスクスナップショット, メモリダンプ), ネットワーク隔離 (VPC / 防火壁), IAM トークン失効, GTI アーティファクト分析, Google SecOps SOAR プレイブック (ブロック, トリガー, アクション, コネクタ), ケース管理ステージ, エスカレーション・シフト引き継ぎ |
| **Section 6** | オブザーバビリティ | 約 10.0% | セキュリティ KPI / メトリクス (MTTD, MTTR, インジェストスループット), Google SecOps SIEM/SOAR ダッシュボード, Looker Studio 連携, Cloud Monitoring / Cloud Logging アラート, 健全性監視, サイレントソース (Silent Sources) 検知 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: プラットフォーム運用 (約 14%)
- **出題の狙い**: SOC 運用における基盤セキュリティプラットフォーム（Google SecOps, SCC, GTI 等）のアーキテクチャを理解し、各ツールの役割分担・統合設計、および最小権限に基づく認証・認可とアクセスガバナンスを確立する能力を検証します。
- **主要タスク**:
  - Task 1.1: 検出と対応の強化（テレメトリーソース [SCC, Google SecOps, GTI, Cloud IDS 等] の優先順位付け、セキュリティツールの統合、重複機能を持つツールの使い分けと正当化、カバレッジギャップの特定と脅威軽減、自動化ツールの評価）
  - Task 1.2: アクセスの構成（SCC および Google SecOps におけるユーザーとサービスアカウントの認証、IAM ロール・権限による機能アクセス制御、データアクセス制御、Cloud Audit Logs の構成と分析、セキュリティツール内での API 自動化認証、Workforce Identity 連携による ID プロビジョニング）
- **重要キーワード**: Google Security Operations (SecOps), Security Command Center (SCC), Google Threat Intelligence (GTI), Cloud IDS, Cloud IAM, Workforce Identity Federation, Service Account, Cloud Audit Logs, Functional Access vs Data Access

#### Section 2: データマネジメント (約 14%)
- **出題の狙い**: 膨大かつ多様なマルチクラウド・オンプレミスのセキュリティログを効率的に収集・正規化し、Google SecOps の UDM（Unified Data Model）スキーマへのマッピング、パーサーカスタマイズ、およびログインジェストコストの最適化を設計・実装する能力を検証します。
- **主要タスク**:
  - Task 2.1: セキュリティツールへのログの取り込み（ログ取り込み手法 [Chronicle Forwarder, Ingestion API, Cloud Logging シンク, Pub/Sub] の選定、取り込み機能の構成、検出・対応に必要なログの評価、デフォルトパーサーの評価、Parser Extension / カスタムパーサーによるログ拡張、UDM への正規化手法、ログタイプと Namespaces の評価、取り込みコスト管理とログフィルタリング）
  - Task 2.2: ユーザー、アセット、エンティティのコンテキストにおけるベースラインの特定（脅威インテリジェンス情報の特定、イベントログとエンティティデータの区別、エイリアシングフィールドを用いたイベントとエンティティデータの一致評価、エンティティコンテキストの拡充）
- **重要キーワード**: Unified Data Model (UDM), Chronicle Forwarder, Ingestion API, Parser Extensions, Grok Parser, Namespaces, Event vs Entity Data, Aliasing, Entity Context, Ingestion Cost Management

#### Section 3: 脅威ハンティング (約 19%)
- **出題の狙い**: 受動的なアラート監視にとどまらず、仮説立案に基づき環境全体の膨大なテレメトリーを横断探索して潜伏する高度な脅威（APT、侵入後の水平展開）をあぶり出し、脅威インテリジェンスや RetroHunt を駆使して過去の侵害を特定するプロアクティブな追跡能力を検証します。
- **主要タスク**:
  - Task 3.1: 環境全体での脅威ハンティングの実行（UDM Search クエリの開発、ユーザー行動分析 [UEBA] による異常行動特定、ログエクスプローラ / ログ分析 / BigQuery / Google SecOps を駆使したネットワーク・エンドポイント調査、インシデント対応チームとの連携、SCC / GTI データに基づく脅威仮説の立案）
  - Task 3.2: 脅威ハンティングへの脅威インテリジェンスの活用（履歴ログ内での IOC 探索、GTI と SCC Toxic Combinations による攻撃パターン特定、エンティティリスクスコア分析、新規ルールや IOC による RetroHunt [遡及ハンティング] の実行、プロアクティブな脅威探索）
- **重要キーワード**: UDM Search, Threat Hunting Hypothesis, Log Analytics (BigQuery), User and Entity Behavior Analytics (UEBA), Indicators of Compromise (IOC), RetroHunt, Toxic Combinations, Google Threat Intelligence (GTI), Entity Risk Score

#### Section 4: 検出エンジニアリング (約 22%)
- **出題の狙い**: 組織固有のリスクプロファイルに応じた高精度な脅威検出ルールを自律開発し、YARA-L 2.0 による複数イベント相関・時間窓条件の設計、キュレーテッドルールの調整、および誤検知（False Positive）を最小化してアラート品質を最大化する能力を検証します。
- **主要タスク**:
  - Task 4.1: リスクを検出して脅威を特定するメカニズムの開発と実装（脅威インテリジェンスの調整、YARA-L 2.0 検出ルールの設計・実装 [events, match, condition, options]、タイムラインを跨いだ不審行動相関、参照リスト [Reference Lists] によるリスクスコアリング、キュレーテッド検出ルールのカスタマイズ、SCC Security Health Analytics / ポスチャー管理との連携、外れ値・低頻度アクティビティ検知、Entity Graph によるコンテキスト強化、SCC Event Threat Detection カスタム検出の構成）
  - Task 4.2: 検出に必要な脅威インテリジェンスの活用（IOC リスクレベルに基づくアラートスコアリング、最新 IOC を用いた自動検出照合、アラート頻度測定と除外ルール設計による誤検知削減）
- **重要キーワード**: YARA-L 2.0, Detection Engine, Reference Lists, Curated Detections, Sliding Window, Match Section, Event Threat Detection (ETD) Custom Modules, Entity Graph, Alert Scoring, False Positive Tuning

#### Section 5: インシデント対応 (約 21%)
- **出題の狙い**: セキュリティ侵害の発生時に被害拡大を即座に食い止める封じ込め、フォレンジック証拠保全、根本原因究明を指揮するとともに、Google SecOps SOAR を駆使した自動プレイブックの実装とケースライフサイクルを円滑に運用する能力を検証します。
- **主要タスク**:
  - Task 5.1: セキュリティインシデントの封じ込めと調査（フォレンジック証拠収集 [VM ディスクスナップショット, メモリダンプ]、SCC / SecOps アラート分析、ログ分析による侵入経路・影響範囲特定、感染アセットのネットワーク隔離 [Quarantine VPC / 防火壁]、IAM 認証情報失効、GTI によるアーティファクト分析、根本原因分析 [RCA]）
  - Task 5.2: 対応ハンドブックの構築、実装、使用（自動化適性の判断、脅威プロファイルに基づく自動拡充 [Enrichment] の優先順位付け、SecOps SOAR プレイブックの設計・実装 [トリガー, ブロック, コネクタ, 人手承認]、新規攻撃パターンに対応するプロセスの策定、通知連携）
  - Task 5.3: ケース管理ライフサイクルの実装（ケースステージの遷移管理、SLA とエスカレーションワークフローの実装、ケース引き継ぎ [Shift Handover] の標準化）
- **重要キーワード**: Incident Containment, Evidence Preservation, Forensic Snapshots, Network Isolation, Token Revocation, Root Cause Analysis (RCA), Google SecOps SOAR Playbooks, Playbook Blocks & Actions, Automated Enrichment, Case Lifecycle Management, Shift Handover

#### Section 6: オブザーバビリティ (約 10%)
- **出題の狙い**: SOC 運用の成熟度・脅威トレンドを経営層およびエンジニアリングチームへ可視化するダッシュボードとレポーティング基盤を構築し、セキュリティパイプライン自体の死活・ログ送信停止（サイレントソース）をプロアクティブに検知する監視体制を確立する能力を検証します。
- **主要タスク**:
  - Task 6.1: 分析情報を提供するダッシュボードとレポートの構築と保守（主要セキュリティ KPI [MTTD, MTTR, トリアージ時間, インジェストレート] の定義、SecOps SIEM/SOAR ダッシュボードおよび Looker Studio 連携、カスタムレポート生成）
  - Task 6.2: ヘルスモニタリングとアラートの構成（ログ収集パイプラインの健全性監視指標の特定、Cloud Monitoring / Cloud Logging による統合監視、しきい値アラートの設定、サイレントソース [Silent Sources: ログ欠落・送信停止] の検知と通知自動化）
- **重要キーワード**: Mean Time to Detect (MTTD), Mean Time to Respond (MTTR), SecOps Dashboards, Looker Studio, Pipeline Health Monitoring, Cloud Monitoring Alerts, Silent Sources Detection, Ingestion Metrics

---

## 4. 推奨学習リソース＆公式ハンズオン・ラボ一覧

### 公式ドキュメント＆アーキテクチャフレームワーク
- [Google Security Operations (SecOps) 公式ドキュメント](https://cloud.google.com/security-operations/docs)
- [Security Command Center (SCC) 公式ドキュメント](https://docs.cloud.google.com/security-command-center/docs)
- [Google Threat Intelligence (GTI) 公式ドキュメント](https://cloud.google.com/threat-intelligence/docs)
- [Chronicle YARA-L 2.0 言語構文リファレンス](https://cloud.google.com/security-operations/docs/detect/yara-l-2-0-overview)
- [Unified Data Model (UDM) フィールドディクショナリ](https://cloud.google.com/security-operations/docs/reference/udm-field-list)
- [Google Cloud ログ分析（Log Analytics）ガイド](https://docs.cloud.google.com/logging/docs/analyze/query-and-view)

### 公式ハンズオンラボ（Google Skills）
1. **Analyze Security Data with Google Security Operations (Skill Badge)**
   - Google SecOps の UDM Search、YARA-L 検出ルールの作成、アラートトリアージを実機演習。
2. **Mitigate Threats and Vulnerabilities with Security Command Center (Skill Badge)**
   - Security Command Center Enterprise / Premium を使用し、Security Health Analytics や Event Threat Detection による脆弱性・インシデント検知を検証。
3. **Automate Security Operations with Google SecOps SOAR (Hands-on Lab)**
   - Siemplify を統合した SecOps SOAR 上で、アラートの自動拡充（Enrichment）およびインシデント封じ込めプレイブックを構築・実行。
4. **Investigate Threats with Cloud Logging and Log Analytics (Hands-on Lab)**
   - BigQuery リンクされた Log Analytics を活用し、SQL による環境全体の脅威ハンティングと相関分析を実践。
