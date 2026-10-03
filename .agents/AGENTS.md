# Certification Study Workspace

## 1. Purpose
本ワークスペースは、クラウドベンダー認定資格（Google Cloud、AWS 等）の実践的学習ドキュメントおよび対策ノートを作成・管理・運用するための専用リポジトリです。
`my-skills` リポジトリの認定学習パイプラインを活用し、最高品質の学習資産を体系的に蓄積します。

---

## 2. Agent Guidelines & Principles
本ワークスペースで作業するエージェントは、以下の原則を厳格に順守してください。

1. **Pipeline Execution**:
   - 学習ドキュメントの生成・推敲時は、読み込まれている `cert-study-director` を軸として各専門スキル（`concept-summarizer`, `scenario-generator`, `logical-reviewer`, `graphic-recorder`, `link-checker` 等）を協調・発火させてください。

2. **Template Adherence**:
   - 新規の試験ガイド・対策ノートを作成する際は、必ず `templates/exam-guide-template.md` の章立て・構造規約を準拠してください。

3. **Directory & File Standard**:
   - 成果物はすべて `notes/<vendor>/<cert>/` 配下に配置します（例: `notes/google-cloud/cloud-architect/`、`notes/aws/solutions-architect-associate/`）。
   - **フラットなファイル配置**: `<cert>/` 直下にコンテンツ用のサブフォルダは切らず、試験ガイドや要点解説などの Markdown コンテンツ（例: `exam-guide.md` 等）を直下にフラット配置します。
   - **画像リソースの集約**: 生成された板書風グラレコや図解画像は、該当資格フォルダ内の `images/`（例: `notes/<vendor>/<cert>/images/`）に集約し、Markdown から相対パス（`./images/...`）で参照します。画像ファイル名は `01-topic-name.png` のように連番とハイフン区切りの半角英数字で統一します。

4. **Quality Standards**:
   - **ピラミッド原則**: 結論先行（Top-down）、縦の論理（So What? / Why So?）、横の論理（MECE）を厳格に維持します。
   - **Gherkin 構文（深層 Because 句）**: 実践シナリオは Given / When / Then / Because で構成し、「採用理由」に加えて「なぜ他の有力代替案では要件を満たせないのか（棄却理由）」を必ず明記します。
   - **一次情報の正確性**: 公式ドキュメントやアーキテクチャフレームワークのリンクを必ず掲載します。

5. **Tone & Manner (No Emoji Policy)**:
   - 装飾用・アイコン用の絵文字（🚀, 👤, 💡 等）は一切出力せず、知的で誠実なプロフェッショナル敬体（です・ます調）を徹底します。

6. **Formatting Hygiene**:
   - 全角スペースの混入を厳禁とし、半角スペースインデントで構文を統一します。
