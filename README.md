# Certification Study Notes

クラウドベンダー認定資格の実践学習ノート・試験対策ドキュメントを蓄積・管理するリポジトリです。
AI エージェントスキルパイプライン（`my-skills`）と連携し、体系的かつ論理明晰な学習資産を構築します。

---

## 1. Directory Structure

```text
cert-study/
├── .agents/
│   ├── AGENTS.md          # ワークスペース行動規範・エージェント規約
│   └── skills.json        # my-skills のスキルマスターを参照するマニフェスト
├── notes/                 # 資格別学習ノート格納ディレクトリ
│   └── <vendor>/          # クラウドベンダー別（例: google-cloud, aws）
│       └── <cert>/        # 資格別（例: cloud-ops-engineer-associate）
│           ├── images/    # 板書風グラレコ・図解画像格納ディレクトリ
│           ├── README.md  # 完全版対策ガイド（本体）
│           └── curriculum.md # 学習ロードマップ・進捗管理
├── templates/             # ノート作成標準テンプレート
│   └── exam-guide-template.md # セクション完結型・網羅的シナリオ対応の基本ひな型
├── cert-study.code-workspace # マルチルートワークスペース定義（my-skills との連携）
└── README.md              # 本ファイル
```

---

## 2. Features & Differentiation

本リポジトリで作成される学習ノートは、以下の4大要素により圧倒的な付加価値と実務即応力を担保します。

1. **ピラミッド原則による最高峰の論理構造**: 全体像から MECE な細分化へ導くトップダウン展開と、縦の因果関係（So What? / Why So?）の徹底。
2. **構造化実践シナリオ（状況/対応/結果/解説）**: 単なる機能説明にとどまらず、前提制約（状況）・選定アクション（対応）・技術的効果（結果）・代替案の棄却理由を含む深層論理（解説）により、実務でのアーキテクチャ設計・意思決定能力を育成。
3. **要約スライド挿絵（板書風グラレコ）**: カリスマ講師の板書・スケッチノート風インフォグラフィックによる視覚的直感理解。
4. **公式一次情報 & 実機ハンズオン**: 公式ドキュメントおよび AWS Skill Builder / Google Cloud Skills Boost 等のラボ環境の体系的リンク。

---

## 3. Document Catalog

| ベンダー | 資格名 | 試験コード | ガイドリンク | カリキュラム |
| :--- | :--- | :--- | :--- | :--- |
| **AWS** | AWS Certified Cloud Practitioner | CLF-C02 | [完全対策ガイド](./notes/aws/cloud-practitioner/README.md) | [ロードマップ](./notes/aws/cloud-practitioner/curriculum.md) |
| **AWS** | AWS Certified AI Practitioner | AIF-C01 | [完全対策ガイド](./notes/aws/ai-practitioner/README.md) | [ロードマップ](./notes/aws/ai-practitioner/curriculum.md) |
| **AWS** | AWS Certified Solutions Architect - Associate | SAA-C03 | [完全対策ガイド](./notes/aws/solutions-architect-associate/README.md) | [ロードマップ](./notes/aws/solutions-architect-associate/curriculum.md) |
| **AWS** | AWS Certified Developer - Associate | DVA-C02 | [完全対策ガイド](./notes/aws/developer-associate/README.md) | [ロードマップ](./notes/aws/developer-associate/curriculum.md) |
| **AWS** | AWS Certified CloudOps Engineer - Associate | SOA-C03 | [完全対策ガイド](./notes/aws/cloud-ops-engineer-associate/README.md) | [ロードマップ](./notes/aws/cloud-ops-engineer-associate/curriculum.md) |
| **AWS** | AWS Certified Data Engineer - Associate | DEA-C01 | [完全対策ガイド](./notes/aws/data-engineer-associate/README.md) | [ロードマップ](./notes/aws/data-engineer-associate/curriculum.md) |
| **AWS** | AWS Certified Machine Learning Engineer - Associate | MLA-C02 | [完全対策ガイド](./notes/aws/machine-learning-engineer-associate/README.md) | [ロードマップ](./notes/aws/machine-learning-engineer-associate/curriculum.md) |
| **AWS** | AWS Certified Solutions Architect - Professional | SAP-C02 | [完全対策ガイド](./notes/aws/solutions-architect-professional/README.md) | [ロードマップ](./notes/aws/solutions-architect-professional/curriculum.md) |
| **AWS** | AWS Certified DevOps Engineer - Professional | DOP-C02 | [完全対策ガイド](./notes/aws/devops-engineer-professional/README.md) | [ロードマップ](./notes/aws/devops-engineer-professional/curriculum.md) |
| **AWS** | AWS Certified Generative AI Developer - Professional | AIP-C01 | [完全対策ガイド](./notes/aws/generative-ai-developer-professional/README.md) | [ロードマップ](./notes/aws/generative-ai-developer-professional/curriculum.md) |
| **AWS** | AWS Certified AI Business Strategist | AIB-C01 | [完全対策ガイド](./notes/aws/ai-business-strategist/README.md) | [ロードマップ](./notes/aws/ai-business-strategist/curriculum.md) |
| **AWS** | AWS Certified Security - Specialty | SCS-C03 | [完全対策ガイド](./notes/aws/security-specialty/README.md) | [ロードマップ](./notes/aws/security-specialty/curriculum.md) |
| **AWS** | AWS Certified Machine Learning - Specialty | MLS-C01 | [完全対策ガイド](./notes/aws/machine-learning-specialty/README.md) | [ロードマップ](./notes/aws/machine-learning-specialty/curriculum.md) |



