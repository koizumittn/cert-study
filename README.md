# Certification Study Notes

クラウドベンダー認定資格の実践学習ノート・試験対策ドキュメントを蓄積・管理するリポジトリです。
AI エージェントスキルパイプライン（`my-skills`）と連携し、体系的かつ論理明晰な学習資産を構築します。

---

## 1. Directory Structure

```text
cert-study/
├── .agents/
│   ├── AGENTS.md          # ワークスペース行動規範・エージェント規約
│   └── skills.json        # my-skills から cert-study スキルを読み込むマニフェスト
├── notes/                 # 資格別学習ノート格納ディレクトリ
│   └── <vendor>/          # クラウドベンダー別（例: google-cloud, aws）
│       └── <cert>/        # 資格別（例: cloud-architect）
│           ├── images/    # 板書風グラレコ・図解画像格納ディレクトリ
│           └── *.md       # 試験ガイド・要点解説ノート（フラット配置）
├── templates/             # ノート作成標準テンプレート
│   └── exam-guide-template.md # 試験ガイド・要点解説の基本ひな型
└── README.md              # 本ファイル
```

---

## 2. Features & Differentiation

本リポジトリで作成される学習ノートは、以下の4大要素により圧倒的な付加価値と実務即応力を担保します。

1. **ピラミッド原則による最高峰の論理構造**: 全体像から MECE な細分化へ導くトップダウン展開と、縦の因果関係（So What? / Why So?）の徹底。
2. **Gherkin 構文による実践シナリオ**: Given / When / Then / Because により、実務でのアーキテクチャ設計・意思決定能力を育成。
3. **要約スライド挿絵（板書風グラレコ）**: カリスマ講師の板書・スケッチノート風インフォグラフィックによる視覚的直感理解。
4. **公式一次情報 & 実機ハンズオン**: 公式ドキュメントおよび Google Cloud Skills Boost 等のラボ環境の体系的リンク。
