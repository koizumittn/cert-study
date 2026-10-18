# Google Cloud Certified - Associate Google Workspace Administrator 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Associate Google Workspace Administrator
- **公式試験ガイド**: [Associate Google Workspace Administrator 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/associate_google_workspace_administrator_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Associate Google Workspace Administrator | Google Cloud Certification](https://cloud.google.com/learn/certification/associate-google-workspace-administrator)
- **公式学習パス**: [Google Skills - Associate Google Workspace Administrator](https://www.skills.google/paths/24?hl=ja)
- **最終更新日**: 2026-10-12

---

## 1. 試験の概要と基本スペック

Associate Google Workspace Administrator は、組織内のチームメンバーによる安全かつ効果的なコラボレーションとコミュニケーションを実現するために、Google Workspace 環境の日常的な管理・運用を担当する管理者の能力を評価・認定する資格です。

管理コンソールを中心としたユーザー アカウントのライフサイクル管理、Gmail や Google ドライブなどのコアサービスの構成、組織部門（OU）とグループを活用したアクセス制御、データ ガバナンス（Google Vault や DLP）、セキュリティ ポリシーの適用、モバイルおよび Chrome ブラウザなどのエンドポイント管理、ならびに日常的に発生する一般的なトラブルシューティングに至る幅広い実務遂行能力が問われます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題、複数選択問題
- **受験料**: $125
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: Google Workspace 管理コンソールを使用した日常的な管理業務の実務経験（推奨 6 か月以上の管理者経験）

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 6 セクションで構成されています。ユーザー アカウント・ディレクトリ管理（22%）、コアサービス管理（20%）、セキュリティ ポリシーとアクセス制御（20%）が中核をなし、さらにトラブルシューティング（14%）、データ ガバナンス（14%）、エンドポイント管理（10%）がバランスよく出題されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト |
| :--- | :--- | :--- | :--- |
| **Section 1** | ユーザー アカウント、ドメイン、ディレクトリの管理 | 約 22% | ユーザー ライフサイクル、プロビジョニング、SAML SSO、GCDS、組織部門（OU）階層設計、Google グループ、動的グループ、セキュリティ グループ、プライマリ/セカンダリ ドメイン、ドメイン エイリアス、ビルディングと会議室リソース |
| **Section 2** | Workspace コアサービスの管理 | 約 20% | Gmail（MX、分割/二重配信、コンテンツ コンプライアンス、SPF/DKIM/DMARC、検疫）、Google ドライブ（共有ドライブ、信頼ルール、対象グループ、保存容量）、Google カレンダー、Google Meet、Google Chat、Gemini for Google Workspace、AppSheet / Apps Script |
| **Section 3** | データ ガバナンスとコンプライアンスの管理 | 約 14% | Google Vault（保持ルール、訴訟ホールド、検索/エクスポート）、データ損失防止（DLP）、ドライブの信頼ルール、Google データ エクスポート、データ リージョン（地理的保管場所）、データ分類とラベル |
| **Section 4** | セキュリティ ポリシーとアクセス制御の管理 | 約 20% | パスワード ポリシー、2 段階認証プロセス（2SV / パスキー）、コンテキストアウェア アクセス（CAA）、管理者ロールと権限委任、セキュリティ調査ツール、セキュリティ センター、監査ログ、Marketplace アプリ管理、SAML アプリ連携 |
| **Section 5** | エンドポイントの管理 | 約 10% | モバイル デバイス管理（基本管理 vs 高度な管理 vs サードパーティ EMM）、BYOD（仕事用プロファイル） vs 会社所有、リモートワイプ（アカウント ワイプ vs デバイス ワイプ）、Chrome ブラウザ クラウド管理（CBCM）、ブラウザ ポリシー、拡張機能管理 |
| **Section 6** | 一般的な問題のトラブルシューティング | 約 14% | 監査ログ分析、Google Workspace ステータス ダッシュボード、メール配信障害（SPF/DKIM/DMARC ヘッダー解析）、カレンダー同期障害、ドライブ権限/削除ファイル復元、Meet 品質管理ツール、HAR ファイル生成、Google サポート連携 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: ユーザー アカウント、ドメイン、ディレクトリの管理（約 22%）
- **出題の狙い**: 組織のアイデンティティ基盤を安全かつ効率的に構築・運用する能力を検証します。オンプレミス Active Directory や既存 IdP との連携（GCDS、SAML SSO）、組織部門（OU）による階層的ポリシー設計、グループを活用した権限管理、および複数ドメイン・会議室リソースの集中管理を評価します。
- **主要タスク**:
  - Task 1.1: ユーザー ライフサイクルの管理（手動作成、CSV 一括登録、GCDS による AD 連携同期、サードパーティ IdP 連携、SAML SSO 設定、ユーザー属性変更、一時停止・削除・復元・アーカイブ、データ所有権移行、ライセンス割り当て、パスワード強制変更）
  - Task 1.2: 組織部門（OU）の設計と作成（業務組織ではなくポリシー適用単位に基づく階層設計、OU の作成・移動・継承・オーバーライド管理）
  - Task 1.3: グループの管理（メーリング リスト、共同トレイ、動的グループによる属性ベース自動所属、セキュリティ グループによるアクセス制限）
  - Task 1.4: ドメインの管理（TXT レコードによるドメイン所有権証明、プライマリ ドメインとセカンダリ ドメインの使い分け、ドメイン エイリアス、MX レコード構成）
  - Task 1.5: ビルディングとリソースの管理（ビルディングと会議室の一括登録、定員・設備属性の設定、カレンダー自動予約ポリシーと権限設定）
- **重要キーワード**: GCDS (Google Cloud Directory Sync), SAML SSO, OU Hierarchy, Policy Inheritance & Override, Dynamic Groups, Security Groups, Primary vs Secondary Domain, Domain Alias, Buildings and Resources, Archived User (AU) License

#### Section 2: Workspace コアサービスの管理（約 20%）
- **出題の狙い**: 日常業務の中心となるコラボレーション ツールの動作仕様を深く理解し、ビジネス要件に合わせて安全かつ最適に構成する能力を検証します。メール ルーティングの高度な制御、共有ドライブのガバナンス、生成 AI（Gemini）の組織展開などを評価します。
- **主要タスク**:
  - Task 2.1: Gmail の構成（MX レコード、分割配信・二重配信ルーティング、コンテンツ コンプライアンス ルール、迷惑メール・フィッシング対策、SPF / DKIM / DMARC、メール検疫、コンプライアンス フッター、メールボックス委任、データ移行）
  - Task 2.2: Google ドライブとドキュメントの構成（外部共有制限、信頼ルール、対象グループ、共有ドライブの権限設計、ユーザー/OU 別ストレージ割り当て、パソコン版 Google ドライブ、ファイル オーナー権限移行、ドライブ ラベル、オフライン アクセス）
  - Task 2.3: Google カレンダーの構成（リソース カレンダー、外部共有オプション、予約ポリシー、サードパーティ会議ツール連携、不明な送信者からの招待ブロック）
  - Task 2.4: Google Meet の構成（OU 別有効化、主催者安全設定、録画・文字起こし設定、ライブ ストリーミング制御）
  - Task 2.5: Google Chat の構成（OU 別有効化、チャット履歴の保存設定、外部スペース参加制限、Chat アプリ制御）
  - Task 2.6: Gemini for Google Workspace の構成（Gemini ライセンス割り当て、OU 別有効化、アルファ機能の制御、利用状況モニタリング）
  - Task 2.7: Workspace 開発のサポート（AppSheet および Apps Script のユースケース特定、OU 別アクセス有効化）
- **重要キーワード**: Split Delivery vs Dual Delivery, Content Compliance Rules, SPF / DKIM / DMARC, Shared Drives, Target Audiences, Google Workspace Storage Limits, Drive Labels, Google Meet Safety Controls, Gemini for Google Workspace, AppSheet

#### Section 3: データ ガバナンスとコンプライアンスの管理（約 14%）
- **出題の狙い**: 企業のコンプライアンス要件、法的規制、知的財産保護を満たすデータ管理ポリシーを設計・運用する能力を検証します。Google Vault による証拠保全、DLP ルールによる情報漏洩防止、データの地理的保管場所の制御を評価します。
- **主要タスク**:
  - Task 3.1: Google Vault を使用した電子情報開示とデータ保持（デフォルト保持ルールとカスタム保持ルール、訴訟ホールドの適用、Vault 検索・エクスポート、監査レポート、アーカイブ ユーザー ライセンスの適用）
  - Task 3.2: データ損失防止（DLP）ルールの作成と管理（コンテンツ コンプライアンス ルールとの差異、機密データ検出機能 [クレジット カード、マイナンバー、正規表現]、警告・ブロック等の修復アクション、Gmail / ドライブ / Chat への適用）
  - Task 3.3: ドライブの信頼ルールの作成と管理（OU・グループ・外部ドメイン単位の共有許可/ブロック制御、ビジター共有の制限）
  - Task 3.4: 環境データの保存方法およびエクスポート方法（Google データ エクスポート ツールの運用、データ リージョン [地理的保管場所] の指定、コンプライアンス設定）
  - Task 3.5: データの分類（ドライブ ラベルと Gmail ラベルのユースケース、ユーザー手動分類、DLP 自動分類、AI 分類）
- **重要キーワード**: Google Vault, Retention Rules vs Litigation Holds, DLP (Data Loss Prevention), Predefined Detectors & Regex, Trust Rules, Data Regions (Geographic Storage), Google Takeout / Data Export Tool, Drive Labels

#### Section 4: セキュリティ ポリシーとアクセス制御の管理（約 20%）
- **出題の狙い**: ゼロトラスト セキュリティ原則に基づき、アカウント認証の堅牢化、コンテキストに応じたアクセス制御、最小権限の管理委任、およびセキュリティ インシデントの迅速な検知・調査を行う能力を検証します。
- **主要タスク**:
  - Task 4.1: ユーザー アクセスの保護（パスワード ポリシー、2 段階認証プロセス [2SV / パスキー / 物理キー] の強制、コンテキストアウェア アクセス [CAA: IP / デバイス状態 / 地理条件]、セキュリティ グループによる保護、カスタム管理者ロールの作成と権限委任）
  - Task 4.2: セキュリティ リスクの報告、監査、調査（セキュリティ調査ツールによるログ検索・修復アクション、セキュリティ センターの脅威分析、セキュリティの状況ページ、アクティビティ ルールとアラート）
  - Task 4.3: アプリケーションの有効化（Marketplace 許可リスト、Google Play アプリの配布制御、SAML / OIDC アプリ統合、追加 Google サービス [YouTube 等] の OU 制御、サードパーティ アプリのトークン失効、Chrome 拡張機能の集中配信）
- **重要キーワード**: 2-Step Verification (2SV), Passkeys, Context-Aware Access (CAA), Security Groups, Delegated Administration & Custom Admin Roles, Security Investigation Tool, Security Center, Marketplace Allowlist, SAML Application Integration

#### Section 5: エンドポイントの管理（約 10%）
- **出題の狙い**: 業務利用される多種多様な端末（スマートフォン、PC、Chrome ブラウザ）に対して、セキュリティと利便性を両立させたガバナンスを確立する能力を検証します。
- **主要タスク**:
  - Task 5.1: モバイル デバイスの管理（基本管理 vs 高度な管理 vs サードパーティ EMM の選定基準、画面ロック強制・暗号化、会社所有端末 vs BYOD [仕事用プロファイル]、アカウント ワイプ [企業データのみ削除] とデバイス ワイプ [完全初期化] の使い分け）
  - Task 5.2: Chrome ブラウザの管理（Chrome ブラウザ クラウド管理 [CBCM] への登録トークン配布、更新ポリシーとバージョン固定、拡張機能の許可・ブロック・自動インストール、オフライン ポリシー）
- **重要キーワード**: Basic Mobile Management vs Advanced Mobile Management, Work Profile (BYOD), Account Wipe vs Device Wipe, Chrome Browser Cloud Management (CBCM), Chrome Extension Policies

#### Section 6: 一般的な問題のトラブルシューティング（約 14%）
- **出題の狙い**: 現場で頻発するシステムトラブルに対して、体系的な切り分けアプローチと管理者ツールを駆使して迅速に原因を特定・解決する実践力を検証します。
- **主要タスク**:
  - Task 6.1: 問題の特定と診断（管理コンソール監査ログ、Workspace ステータス ダッシュボードでの障害確認、メール配信ログ検索）
  - Task 6.2: 一般的な問題の解決（アカウント ロック解除、SPF / DKIM / DMARC 設定不備によるメール不達や迷惑メール誤判定の解消、カレンダー同期不良、ドライブ共有権限トラブル、誤削除ファイルの復元 [ゴミ箱・Vault]、パソコン版ドライブのキャッシュ障害、Meet 品質管理ツールによるネットワーク遅延診断）
  - Task 6.3: サポート リソースの使用（再現手順の文書化、HAR ファイルの取得・解析、管理者ツールボックスの活用、Google サポートへのケース起票）
- **重要キーワード**: Audit Logs, Email Log Search (ELS), Message Header Analyzer, SPF / DKIM / DMARC Alignment, Calendar Sync Troubleshooting, Restore Deleted Drive Files, Meet Quality Tool, HAR File, Google Admin Toolbox
