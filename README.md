# Certification Study Notes

クラウドベンダー認定資格の実践学習ノート・試験対策ドキュメントを蓄積・管理するリポジトリです。
各資格の出題範囲に基づき、体系的かつ実践的な学習ドキュメントを提供します。

---

## 1. Directory Structure

```text
cert-study/
├── .agents/
│   ├── AGENTS.md          # ワークスペース行動規範・エージェント規約
│   └── skills.json        # エージェントスキル設定ファイル
├── notes/                 # 資格別学習ノート格納ディレクトリ
│   └── <vendor>/          # クラウドベンダー別（例: google-cloud, aws）
│       └── <cert>/        # 資格別（例: cloud-ops-engineer-associate）
│           ├── images/    # 板書風グラレコ・図解画像格納ディレクトリ
│           ├── README.md  # 完全版対策ガイド（本体）
│           └── curriculum.md # 学習ロードマップ・進捗管理
├── templates/             # ノート作成標準テンプレート
│   └── exam-guide-template.md # セクション完結型・網羅的シナリオ対応の基本ひな型
└── README.md              # 本ファイル
```

---

## 2. Features & AI-Assisted Content Notice

本リポジトリで提供される学習ノートは、実務即応性と効率的な学習を重視した以下の特徴を備えています。

1. **構造化実践シナリオ（状況/対応/結果/解説）**: 単なる機能説明にとどまらず、前提制約（状況）・選定アクション（対応）・技術的効果（結果）・代替案の棄却理由を含む論理的解説により、実務でのアーキテクチャ設計・意思決定能力を育成します。
2. **要約スライド挿絵（板書風グラレコ）**: 講義の板書・スケッチノート風インフォグラフィックによる視覚的な直感理解をサポートします。
3. **公式一次情報 & 実機ハンズオン連携**: 各分野の公式ドキュメントおよび AWS Skill Builder / Google Skills 等の公式ラボ環境への参照を体系的に整理しています。

### 免責事項・ご利用上の注意（Disclaimer）

本リポジトリのコンテンツは、生成AIを活用して作成・構成されています。

- **ハルシネーション（誤情報生成）のリスク**: 可能な限り正確な情報を掲載するよう配慮していますが、AIの特性上、誤った記述や最新の仕様・試験範囲との乖離（ハルシネーション）が含まれる可能性があります。
- **公式一次情報の確認**: 試験対策や実務適用にあたっては、必ず各クラウドベンダーが提供する最新の公式ドキュメントや試験ガイドを一次情報として併読・確認してください。
- **免責**: 本リポジトリの掲載情報によって生じたいかなる損害や合否結果についても、作成者は一切の責任を負いかねます。

---

## 3. Document Catalog

| ベンダー | 資格名 | 試験コード | ガイドリンク |
| :--- | :--- | :--- | :--- |
| **AWS** | AWS Certified Cloud Practitioner | CLF-C02 | [完全対策ガイド](./notes/aws/cloud-practitioner/README.md) |
| **AWS** | AWS Certified AI Practitioner | AIF-C01 | [完全対策ガイド](./notes/aws/ai-practitioner/README.md) |
| **AWS** | AWS Certified Solutions Architect - Associate | SAA-C03 | [完全対策ガイド](./notes/aws/solutions-architect-associate/README.md) |
| **AWS** | AWS Certified Developer - Associate | DVA-C02 | [完全対策ガイド](./notes/aws/developer-associate/README.md) |
| **AWS** | AWS Certified CloudOps Engineer - Associate | SOA-C03 | [完全対策ガイド](./notes/aws/cloud-ops-engineer-associate/README.md) |
| **AWS** | AWS Certified Data Engineer - Associate | DEA-C01 | [完全対策ガイド](./notes/aws/data-engineer-associate/README.md) |
| **AWS** | AWS Certified Machine Learning Engineer - Associate | MLA-C02 | [完全対策ガイド](./notes/aws/machine-learning-engineer-associate/README.md) |
| **AWS** | AWS Certified Solutions Architect - Professional | SAP-C02 | [完全対策ガイド](./notes/aws/solutions-architect-professional/README.md) |
| **AWS** | AWS Certified DevOps Engineer - Professional | DOP-C02 | [完全対策ガイド](./notes/aws/devops-engineer-professional/README.md) |
| **AWS** | AWS Certified Generative AI Developer - Professional | AIP-C01 | [完全対策ガイド](./notes/aws/generative-ai-developer-professional/README.md) |
| **AWS** | AWS Certified AI Business Strategist | AIB-C01 | [完全対策ガイド](./notes/aws/ai-business-strategist/README.md) |
| **AWS** | AWS Certified Security - Specialty | SCS-C03 | [完全対策ガイド](./notes/aws/security-specialty/README.md) |
| **AWS** | AWS Certified Machine Learning - Specialty | MLS-C01 | [完全対策ガイド](./notes/aws/machine-learning-specialty/README.md) |
| **Google Cloud** | Google Cloud Certified - Cloud Digital Leader | CDL | [完全対策ガイド](./notes/google-cloud/cloud-digital-leader/README.md) |
| **Google Cloud** | Google Cloud Certified - Generative AI Leader | GAIL | [完全対策ガイド](./notes/google-cloud/generative-ai-leader/README.md) |
| **Google Cloud** | Google Cloud Certified - Associate Cloud Engineer | ACE | [完全対策ガイド](./notes/google-cloud/associate-cloud-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Associate Google Workspace Administrator | AGWA | [完全対策ガイド](./notes/google-cloud/associate-google-workspace-administrator/README.md) |
| **Google Cloud** | Google Cloud Certified - Associate Data Practitioner | ADP | [完全対策ガイド](./notes/google-cloud/associate-data-practitioner/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud Database Engineer | PCDBE | [完全対策ガイド](./notes/google-cloud/professional-cloud-database-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud Architect | PCA | [完全対策ガイド](./notes/google-cloud/professional-cloud-architect/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud Developer | PCD | [完全対策ガイド](./notes/google-cloud/professional-cloud-developer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Data Engineer | PDE | [完全対策ガイド](./notes/google-cloud/professional-data-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud DevOps Engineer | PCDOE | [完全対策ガイド](./notes/google-cloud/professional-cloud-devops-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud Security Engineer | PCSE | [完全対策ガイド](./notes/google-cloud/professional-cloud-security-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Cloud Network Engineer | PCNE | [完全対策ガイド](./notes/google-cloud/professional-cloud-network-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Machine Learning Engineer | PMLE | [完全対策ガイド](./notes/google-cloud/professional-machine-learning-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Security Operations Engineer | PSOE | [完全対策ガイド](./notes/google-cloud/professional-security-operations-engineer/README.md) |
| **Google Cloud** | Google Cloud Certified - Professional Agentic Architect | PAA | [完全対策ガイド](./notes/google-cloud/professional-agentic-architect/README.md) |

