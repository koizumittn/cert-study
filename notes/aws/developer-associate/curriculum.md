# AWS Certified Developer - Associate (DVA-C02) 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: AWS Certified Developer - Associate
- **試験コード**: DVA-C02
- **公式試験ガイド**: [AWS Certified Developer - Associate (DVA-C02) 試験ガイド](https://docs.aws.amazon.com/ja_jp/aws-certification/latest/developer-associate-02/developer-associate-02.html)
- **最終更新日**: 2026-10-06

---

## 1. 試験の概要と基本スペック

AWS Certified Developer - Associate (DVA-C02) は、AWS クラウド環境におけるモダンアプリケーションの開発、テスト、パッケージング、CI/CD デプロイ、セキュリティ実装、およびオブザーバビリティ（監視・デバッグ・パフォーマンス最適化）に関する実践的なエンジニアリング能力を実証するアソシエイト中核認定資格です。

インフラ基盤の設計・運用にとどまらず、AWS SDK / CLI を駆使した API 連携、サーバーレス（AWS Lambda, Amazon API Gateway）、NoSQL（Amazon DynamoDB）、非同期メッセージング（Amazon SQS, SNS, EventBridge）、コンテナデプロイ、そして分散トレーシング（AWS X-Ray）の実装コードレベルの知識と判断力が問われます。

- **試験時間**: 130 分
- **出題問題数**: 65 問（採点対象: 50 問 / 未採点テスト設問: 15 問）
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **合格基準点**: 100〜1,000 点中 720 点以上
- **前提知識**: 1 種類以上の高水準プログラミング言語（Python, TypeScript, JavaScript, Java, Go, C# 等）の習熟、AWS の主要サービス API / SDK / CLI を使用したアプリケーション開発・保守における 1 年以上の実務経験が推奨されます。

---

## 2. 出題分野（Domain）と出題比率一覧

| ドメイン番号 | 出題分野（Domain） | 出題比率 | 主要対象サービス・技術要素 | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Domain 1** | AWS のサービスによる開発 | 32% | AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon SQS, Amazon SNS, Amazon EventBridge, AWS Step Functions, Amazon S3, Amazon Kinesis, Amazon Q Developer | 完了 |
| **Domain 2** | セキュリティ | 26% | AWS IAM, IAM ロール (AssumeRole), Amazon Cognito (User Pools / Identity Pools), AWS KMS (エンベロープ暗号化), AWS Secrets Manager, AWS Systems Manager Parameter Store | 完了 |
| **Domain 3** | デプロイ | 24% | AWS CodePipeline, AWS CodeBuild, AWS CodeDeploy, AWS SAM, AWS CloudFormation, AWS AppConfig, Amazon ECS / ECR, デプロイメント戦略 (カナリア, リニア, ブルー/グリーン) | 完了 |
| **Domain 4** | トラブルシューティングと最適化 | 18% | Amazon CloudWatch Logs / Metrics, CloudWatch Logs Insights, 埋め込みメトリクスフォーマット (EMF), AWS X-Ray, Lambda 同時実行制御, ElastiCache, DAX | 完了 |

---

## 3. ドメイン別タスクおよび学習ロードマップ

### Domain 1: AWS のサービスによる開発 (32%)
- **Task 1.1**: AWS でホストされているアプリケーション用のコードの開発（マイクロサービス/イベント駆動型/オーケストレーションアーキテクチャ、ステートフル vs ステートレス、疎結合設計、同期 vs 非同期、SDK リトライ・指数バックオフ、API リクエスト/レスポンス変換、Amazon Q Developer によるコーディング支援）
- **Task 1.2**: AWS Lambda 用コードの開発（VPC 内リソースアクセス、実行環境ライフサイクルと実行コンテキスト再利用、レイヤー・拡張機能、Lambda 送信先 vs DLQ、プロビジョンド同時実行、コールドスタート対策、ストリームデータバッチ処理）
- **Task 1.3**: アプリケーション開発でのデータストアの使用（DynamoDB パーティションキー設計・高カーディナリティ、強整合性 vs 結果整合性、Query vs Scan、GSI vs LSI、TTL、DynamoDB Streams、DAX キャッシュ）

### Domain 2: セキュリティ (26%)
- **Task 2.1**: アプリケーションと AWS のサービスの認証および/または認可の実装（Cognito ユーザープール vs ID プール、JWT/ベアラートークン検証、AWS STS AssumeRole、IAM ポリシーの最小権限原則、API Gateway オーソライザー）
- **Task 2.2**: AWS のサービスを使用した暗号化の実装（保存時 vs 転送時暗号化、AWS KMS カスタマーマネージドキー、エンベロープ暗号化メカニズム、SSE-S3 vs SSE-KMS vs クライアント側暗号化、自動キーローテーション、クロスアカウント KMS アクセス）
- **Task 2.3**: アプリケーションコードでの機密データの管理（PII/PHI のマスキング・サニタイズ、Secrets Manager によるシークレット自動ローテーション、Systems Manager Parameter Store の階層管理・SecureString、環境変数の安全な注入）

### Domain 3: デプロイ (24%)
- **Task 3.1**: AWS にデプロイするアプリケーションアーティファクトの準備（コンテナイメージビルド、依存関係パッケージング、AWS AppConfig による動的設定・フィーチャーフラグ）
- **Task 3.2**: 開発環境でのアプリケーションのテスト（ローカルテスト、モック API、API Gateway ステージ、AWS SAM ローカルエミュレーション、イベント駆動アプリケーションのテスト）
- **Task 3.3**: デプロイテストの自動化（JSON テストイベント、Lambda エイリアス、IaC テンプレート検証、Amazon Q Developer によるテストコード自動生成）
- **Task 3.4**: AWS の継続的インテグレーションおよび継続的デリバリー (CI/CD) サービスを使用したコードのデプロイ（CodePipeline、CodeBuild の `buildspec.yml`、CodeDeploy の `appspec.yml`、トラフィック移行型デプロイ [Canary / Linear]、ブルー/グリーンデプロイ、自動ロールバック）

### Domain 4: トラブルシューティングと最適化 (18%)
- **Task 4.1**: 根本原因分析の支援（CloudWatch Logs Insights によるクエリ分析、EMF による高解像度カスタムメトリクス生成、デプロイログのトレース、サービス統合障害の解析）
- **Task 4.2**: オブザーバビリティのためのコードの考案（構造化ロギング、AWS X-Ray 分散トレーシング、セグメントとサブセグメント、Annotations vs Metadata、サンプリングルール）
- **Task 4.3**: AWS のサービスと機能を使用したアプリケーションの最適化（Lambda 予約同時実行 vs プロビジョンド同時実行、ElastiCache / DAX によるキャッシュ多層化、SNS サブスクリプションフィルターポリシー、指数バックオフとジッター）
