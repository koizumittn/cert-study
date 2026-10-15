# Google Cloud Certified - Professional Cloud Network Engineer 学習カリキュラム＆出題範囲ロードマップ

- **対象資格**: Google Cloud Certified - Professional Cloud Network Engineer
- **公式試験ガイド**: [Professional Cloud Network Engineer 認定試験ガイド (日本語版)](https://services.google.com/fh/files/misc/professional_cloud_network_engineer_exam_guide_japanese.pdf?hl=ja)
- **公式試験ページ**: [Professional Cloud Network Engineer | Google Cloud Certification](https://cloud.google.com/learn/certification/cloud-network-engineer?hl=ja)
- **公式学習パス**: [Google Skills - Network Engineer Learning Path](https://www.cloudskillsboost.google/paths/13)
- **最終更新日**: 2026-10-15

---

## 1. 試験の概要と基本スペック

Professional Cloud Network Engineer は、Google Cloud におけるネットワークアーキテクチャの設計、実装、管理、運用、およびトラブルシューティングを包括的に遂行できる能力を認定するプロフェッショナル資格です。

Virtual Private Cloud（VPC）の設計、動的ルーティング（Cloud Router / BGP）、ネットワークセキュリティ（Cloud NGFW、Google Cloud Armor、Secure Web Proxy）、ロードバランシング（Application Load Balancer / Network Load Balancer）、Cloud DNS、Cloud NAT、ハイブリッドおよびマルチクラウド相互接続（Cloud Interconnect、HA-VPN、Cross-Cloud Interconnect、Network Connectivity Center）、Google Kubernetes Engine（GKE）ネットワーク設計、ならびに Google Cloud Observability と Network Intelligence Center を用いたネットワーク運用の診断・モニタリングに関する高度な実務能力が厳密に評価されます。

- **試験時間**: 120 分（2 時間）
- **出題問題数**: 50〜60 問
- **出題形式**: 択一選択問題（4 肢中 1 つ選択）、複数選択問題（5 肢以上中 2 つ以上選択）
- **受験料**: $200（税別）
- **合否判定**: 合格 / 不合格（スケールドスコアや正答率は非開示）
- **前提知識**: 3 年以上の業界実務経験（Google Cloud を使用したネットワークソリューションの設計・構築・運用管理に関する 1 年以上の実務経験を含む）が推奨されます。

---

## 2. 出題分野（Section）と出題比率一覧

本試験は全 6 セクションで構成されています。VPC ネットワークの設計と計画（24%）、マネージドネットワークサービスの構成（21%）、VPC ネットワークの実装（19%）が約 64% を占めており、これらに加えてハイブリッド/マルチクラウド接続（15%）、ネットワークセキュリティ（14%）、ネットワーク運用・トラブルシューティング（13%）が網羅的に評価されます。

| セクション番号 | セクション名 / 出題分野 | 出題比率 | 主要対象サービス・コンセプト | ステータス |
| :--- | :--- | :--- | :--- | :--- |
| **Section 1** | Google Cloud VPC ネットワークの設計と計画 | 約 24.0% | スタンドアロン VPC / 共有 VPC、VPC ピアリング、Private Service Connect (PSC)、ネットワーク階層（プレミアム vs スタンダード）、IP アドレス管理（BYOIP、PAP、PDP、Private NAT、IPv6）、サードパーティ NVA 挿入、ハイブリッド接続設計、GKE ネットワーク設計 | 完了 |
| **Section 2** | VPC ネットワークの実装 | 約 19.0% | サブネット作成・拡張、共有 VPC 構成、プライベート Google アクセス、Vertex AI 接続、動的ルーティング（グローバル vs リージョン）、ポリシーベースルート、ネクストホップ内部ロードバランサ、Network Connectivity Center (NCC) VPC スポーク、GKE VPC ネイティブクラスタ、Dataplane V2、IP マスカレード | 完了 |
| **Section 3** | マネージドネットワークサービスの構成 | 約 21.0% | 外部/内部 アプリケーションロードバランサ、ネットワークロードバランサ、NEG (Serverless / Internet / Hybrid / Zonal)、トラフィック管理（URL マップ、加重ルーティング、ミラーリング）、GKE Gateway API / Ingress、Cloud CDN（オリジン、キャッシュ無効化、署名付き URL）、Cloud DNS（ルーティングポリシー、DNSSEC、スプリットホライズン、DNS ピアリング） | 完了 |
| **Section 4** | ハイブリッドおよびマルチクラウドネットワークの相互接続の構成と実装 | 約 15.0% | Dedicated Interconnect、Partner Interconnect (L2/L3)、Cross-Cloud Interconnect、Interconnect 経由 HA-VPN、高可用性トポロジ (99.9% / 99.99% SLA)、HA-VPN、Classic VPN、Cloud Router (BGP、MED、BFD、カスタムアドバタイズ)、NCC ハイブリッドスポーク、Router Appliance | 完了 |
| **Section 5** | ネットワークオペレーションの管理、モニタリング、トラブルシューティング | 約 13% | Cloud Monitoring / Cloud Logging、接続ドレインとフェイルオーバー、BGP ピアリングトラブルシューティング、VPC フローログ、Packet Mirroring、Network Intelligence Center (Network Topology、Connectivity Tests、Performance Dashboard、Firewall Insights、Network Analyzer、Flow Analyzer) | 完了 |
| **Section 6** | クラウドネットワークセキュリティソリューションの構成、実装、管理 | 約 14% | Google Cloud Armor (WAF ルール、DDoS 対策、Adaptive Protection、レート制限、Bot 管理、Threat Intelligence)、Cloud NGFW (Essentials / Standard / Enterprise、L7 検査、階層型ポリシー、タグ/サービスアカウント)、Cloud NAT、Secure Web Proxy、Multi-NIC NVA、Cloud IDS、Packet Mirroring | 完了 |

---

## 3. セクション別詳細タスクおよび学習ロードマップ

#### Section 1: Google Cloud Virtual Private Cloud（VPC）ネットワークの設計と計画 (約 24%)
- **出題の狙い**: エンタープライズ規模のワークロード要件に基づき、高可用性・拡張性・回復力・分離性を備えた VPC ネットワークアーキテクチャ、IP アドレス設計、ハイブリッド接続戦略、GKE ネットワークトポロジを包括的に設計する能力を検証します。
- **主要タスク**:
  - Task 1.1: 全体的なネットワークアーキテクチャを設計する（高可用性・フェイルオーバー・DR・スケール考慮、DNS トポロジ設計、ロードバランサ選定、ハイブリッド接続設計、GKE ネットワーキング計画、共有 VPC 環境での IAM ロール設計、マネージドサービス接続計画 [PSA、PSC、サーバーレス VPC アクセス]、ネットワークティア選定 [プレミアム vs スタンダード]）
  - Task 1.2: VPC ネットワークを設計する（VPC タイプ選定 [スタンドアロン vs 共有 VPC]、ネットワーク相互接続方式選定 [VPC ピアリング、NCC メッシュ/スター、PSC]、IPAM 戦略 [サブネット、IPv6、BYOIP / PAP / PDP、Private NAT、非 RFC 1918]、グローバル vs リージョン環境、MTU サイズ決定、サードパーティ NVA 挿入計画）
  - Task 1.3: 復元力とパフォーマンスに優れたハイブリッドおよびマルチクラウドネットワークを設計する（Dedicated / Partner Interconnect、Cloud VPN、SD-WAN、Cross-Cloud Interconnect、Direct Peering vs Verified Peering Provider、複数リージョン HA/DR、オンプレミスから複数 VPC / Google サービスへのプライベートアクセス、IP 重複回避、DNS 転送戦略、MTU 最適化、MACsec / IPsec 暗号化）
  - Task 1.4: Google Kubernetes Engine（GKE）を設計する（パブリック vs プライベートクラスタ/ノードプール、コントロールプレーンエンドポイント設計、プライマリ/セカンダリサブネット範囲、RFC 1918 / 非 RFC 1918 / PUPI、IPv6 計画、GKE ロードバランシング設計、ノードプール構成）
- **重要キーワード**: Shared VPC, VPC Network Peering, Private Service Connect (PSC), Network Connectivity Center (NCC), Premium Tier / Standard Tier, BYOIP (PAP/PDP), Private NAT, GKE VPC-native, IP Masquerade, Cloud Router Dynamic Routing

#### Section 2: VPC ネットワークの実装 (約 19%)
- **出題の狙い**: 設計されたアーキテクチャに基づき、VPC、サブネット、高度なルーティングポリシー、NCC トポロジ、および GKE クラスタネットワークを正確にプロビジョニング・実装する実務能力を検証します。
- **主要タスク**:
  - Task 2.1: VPC を構成する（VPC リソース作成、VPC ピアリング構成、共有 VPC およびサービスプロジェクト共有、プライベート Google アクセス構成、Vertex AI 接続構成、サブネット CIDR 拡張、VPC Service Controls 境界連携）
  - Task 2.2: VPC ルーティングを構成する（静的 vs 動的ルーティング、グローバル/リージョン動的ルーティング、ネットワークタグと優先度によるルーティング、ネクストホップ内部ロードバランサ、ピアリングカスタムルート交換、ポリシーベースルーティング [PBR]）
  - Task 2.3: Network Connectivity Center を構成する（VPC スポーク、ハイブリッドスポーク、プロデューサースポーク、スター/メッシュトポロジ、Private NAT と PSC 伝播、CIDR 範囲フィルタリング、モニタリング）
  - Task 2.4: Google Kubernetes Engine クラスタの構成と保守を行う（エイリアス IP を使用した VPC ネイティブクラスタ、共有 VPC 連携、プライベートクラスタ/プライベートコントロールプレーン、承認済みネットワーク、Dataplane V2、SNAT / IP マスカレードポリシー、ネットワークポリシー、Pod/Service 追加範囲のデプロイ）
- **重要キーワード**: Subnet Expansion, Shared VPC Service Projects, Private Google Access, Global Dynamic Routing, Policy-Based Routes (PBR), Next-Hop Internal Load Balancer, NCC VPC Spokes, Dataplane V2, GKE Authorized Networks, IP Masquerade Agent

#### Section 3: マネージドネットワークサービスの構成 (約 21%)
- **出題の狙い**: グローバルおよびリージョンの各種ロードバランサ、Cloud CDN、Cloud DNS を適切に構成し、トラフィックの最適化、高可用性配信、低レイテンシキャッシュ、および名前解決を実装する能力を検証します。
- **主要タスク**:
  - Task 3.1: ロードバランシングを構成する（外部/内部、リージョン/グローバル、アプリケーション/プロキシ/パススルーの選定、NEG [Zonal, Serverless, Internet, Hybrid]、MIG、分散方式、セッションアフィニティ、キャパシティスケーリング、URL マップ、ヘルスチェック、グローバルアクセス、GKE Gateway API / Ingress、高度なトラフィック管理 [トラフィック分割、ミラーリング、URL 書換え]）
  - Task 3.2: Cloud CDN を構成する（バックエンド統合 [MIG, Cloud Storage, Cloud Run, 外部 NEG]、キャッシュモード、キャッシュ無効化、署名付き URL / 署名付き Cookie による認可配信）
  - Task 3.3: Cloud DNS を構成する（パブリック/プライベートゾーン、Cloud DNS への移行、ルーティングポリシー [位置情報ポリシー, 加重ラウンドロビン, フェイルオーバーポリシー]、DNSSEC、DNS 転送、スプリットホライズン DNS、プロジェクト間バインディング、DNS ピアリング、GKE Cloud DNS / ExternalDNS オペレーター）
- **重要キーワード**: Application Load Balancer (Global/Regional), Network Load Balancer (Proxy/Passthrough), Network Endpoint Groups (NEGs), GKE Gateway API, Cloud CDN, Cache Invalidation, Signed URLs, Cloud DNS Routing Policies, DNSSEC, Split-Horizon DNS, DNS Peering

#### Section 4: ハイブリッドおよびマルチクラウドネットワークの相互接続の構成と実装 (約 15%)
- **出題の狙い**: オンプレミスデータセンターおよび他社クラウド（AWS、Azure 等）と Google Cloud を低遅延・高スループットかつ堅牢に相互接続し、BGP 動的ルーティングや NCC を用いて安定したエンタープライズ通信網を構築する能力を検証します。
- **主要タスク**:
  - Task 4.1: Cloud Interconnect を構成する（Dedicated Interconnect、Partner Interconnect [L2 / L3]、Cross-Cloud Interconnect、VLAN アタッチメント、Interconnect 経由 HA-VPN、99.9% および 99.99% SLA トポロジの実装）
  - Task 4.2: サイト間 IPsec VPN を構成する（オンプレミス接続用 HA-VPN、VPC 間接続用 HA-VPN、Classic VPN [ルートベース / ポリシーベース]）
  - Task 4.3: Cloud Router を構成する（BGP 属性 [ASN, MED, ルート優先度, リンクローカル IP, MD5 認証]、BFD [双方向フォワーディング検出]、カスタムアドバタイズルート、カスタム学習ルート、最適パス選択モード）
  - Task 4.4: Network Connectivity Center を構成する（ハイブリッドスポーク [VPN / VLAN]、サイト間データ転送、Router Appliance [RA]、トランジットネットワークルーティングの最適化とトラブルシューティング）
- **重要キーワード**: Dedicated Interconnect, Partner Interconnect, Cross-Cloud Interconnect, HA-VPN, 99.99% Availability Architecture, Cloud Router, BGP MED, BFD, Router Appliance (RA), NCC Site-to-Site Data Transfer

#### Section 5: ネットワークオペレーションの管理、モニタリング、トラブルシューティング (約 13%)
- **出題の狙い**: Google Cloud Observability および Network Intelligence Center を駆使して、ネットワーク性能・遅延・パケットロス・構成ミスを迅速に特定・可視化し、接続障害を根本原因から解決する運用能力を検証します。
- **主要タスク**:
  - Task 5.1: ロギングとモニタリングに Google Cloud Observability を使用する（VPN, Cloud Router, VPC-SC, Cloud NGFW, VPC フローログ, Cloud DNS, Cloud NAT, NCC における Cloud Logging 有効化、指標モニタリング・アラート作成）
  - Task 5.2: 接続の維持管理とその問題のトラブルシューティングを行う（ALB トラフィックドレイン/リダイレクト、VPN 障害対応、Interconnect 障害対応、BGP ピアリング障害対応、VPC フローログ / ファイアウォールログ / Packet Mirroring 解析）
  - Task 5.3: Network Intelligence Center を使用した、ネットワークに関する一般的な問題のモニタリングとトラブルシューティングを行う（Network Topology による可視化、Connectivity Tests による構成検証・パケットドロップ診断、Performance Dashboard による遅延/パケットロス特定、Firewall Insights によるシャドウルール検出・過剰ルール最適化、Network Analyzer による設定ミス・クォータ警告検出、Flow Analyzer によるトラフィック傾向分析）
- **重要キーワード**: Network Intelligence Center, Connectivity Tests, Network Topology, Performance Dashboard, Firewall Insights, Network Analyzer, Flow Analyzer, VPC Flow Logs, Packet Mirroring, Connection Draining

#### Section 6: クラウドネットワークセキュリティソリューションの構成、実装、管理 (約 14%)
- **出題の狙い**: 多層防御の観点から、エッジ（Cloud Armor）、境界（Cloud NGFW / Secure Web Proxy）、内部（Micro-segmentation / IDS / Packet Mirroring）の各層で強固なセキュリティ制御を構成・管理する能力を検証します。
- **主要タスク**:
  - Task 6.1: Google Cloud Armor ポリシーを構成する（エッジおよびバックエンドセキュリティポリシー、OWASP Top 10 WAF ルール、DDoS 対策、Adaptive Protection、レート制限、Bot 管理 [reCAPTCHA Enterprise 統合]、Google Threat Intelligence）
  - Task 6.2: Cloud Next Generation Firewall（NGFW）ポリシーと VPC ファイアウォールルールを構成、管理する（Cloud NGFW 階層型ポリシー、リージョン/グローバルポリシー、NGFW ティア [Essentials, Standard, Enterprise]、Enterprise L7 パケット検査 / IPS、タグ/セキュアタグ/サービスアカウントによるマイクロセグメンテーション、VPC ルールからの移行、ファイアウォールロギング）
  - Task 6.3: パブリック Cloud NAT と Secure Web Proxy を使用してインターネット下り（外向き）トラフィックを構成して保護する（Cloud NAT 自動/手動 IP 割り当て、静的/動的ポート割り当て、Secure Web Proxy による TLS インスペクションと URL フィルタリング）
  - Task 6.4: セルフマネージドのネットワークパケットインスペクション、IDS、Packet Mirroring を構成する（マルチ NIC VM による NVA 検査、内部ロードバランサをネクストホップとする冗長構成、ポリシーベースルート、Cloud IDS による脅威検出、Packet Mirroring によるパケットキャプチャ）
- **重要キーワード**: Google Cloud Armor, WAF (OWASP), Cloud NGFW Enterprise, Layer 7 Packet Inspection, Hierarchical Firewall Policies, Secure Web Proxy, Cloud NAT Dynamic Port Allocation, Multi-NIC NVA, Next-Hop ILB, Cloud IDS, Packet Mirroring

---

## 4. 推奨学習リソース＆公式ハンズオン・ラボ一覧

### 公式ドキュメント＆アーキテクチャフレームワーク
- [Google Cloud Architecture Framework: システム設計 - ネットワーキング](https://cloud.google.com/architecture/framework/system-design/networking?hl=ja)
- [Google Cloud VPC ドキュメント](https://cloud.google.com/vpc/docs?hl=ja)
- [Cloud Load Balancing の概要](https://cloud.google.com/load-balancing/docs?hl=ja)
- [Cloud Interconnect ドキュメント](https://cloud.google.com/network-connectivity/docs/interconnect?hl=ja)
- [Network Intelligence Center ドキュメント](https://cloud.google.com/network-intelligence-center/docs?hl=ja)
- [Google Cloud Armor の概要](https://cloud.google.com/armor/docs?hl=ja)
- [Cloud NGFW の概要](https://cloud.google.com/firewall/docs?hl=ja)

### 公式ハンズオンラボ（Google Skills / Cloud Skills Boost）
1. **Network Performance and Optimization (Skill Badge)**
   - 複数の VPC、内部ロードバランサ、ルーティング最適化、VPC フローログの実機分析。
2. **Build and Secure Networks in Google Cloud (Skill Badge)**
   - 共有 VPC、Cloud Armor WAF ルール、Cloud NAT、VPC ファイアウォールルールの構成。
3. **Implement Cloud Security Fundamentals on Google Cloud (Skill Badge)**
   - Network Intelligence Center の Connectivity Tests、Cloud IDS、Packet Mirroring を用いたセキュリティ監視。
4. **Networking Fundamentals in Google Cloud (Course / Lab)**
   - VPC ネットワーク作成、Cloud Router、Cloud DNS、HA-VPN の設定検証。
