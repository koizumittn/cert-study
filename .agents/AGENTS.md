# Certification Study Workspace

## 1. Purpose
本ワークスペースは、クラウドベンダー認定資格（Google Cloud、AWS 等）の実践的学習ドキュメントおよび対策ノートを作成・管理・運用するための専用リポジトリです。
`my-skills` リポジトリの認定学習パイプラインを活用し、最高品質の学習資産を体系的に蓄積します。

---

## 2. Agent Guidelines & Principles
本ワークスペースで作業するエージェントは、以下の原則を厳格に順守してください。

1. **Pipeline Execution & Single Source of Truth**:
   - 学習ドキュメントの生成・推敲時は、読み込まれている `cert-study-director` を軸として各専門スキル（`concept-summarizer`, `scenario-generator`, `logical-reviewer`, `graphic-recorder`, `link-checker` 等）を協調・発火させてください。
   - **スキルマスターの直接参照**: マルチワークスペース構成により、スキル定義および品質基準は `~/src/my-skills/skills/cert-study/` を Single Source of Truth（唯一の正本）として直接参照します。
   - `~/src/my-skills/skills/cert-study/references/study_guide_quality_standard.md` の設計標準を最上位の品質規範とします。外部ファイルへのアクセス制限（Operation not permitted 等）が発生した場合は、BypassSandbox を用いて確実に仕様を深掘りし、独自判断でのスキップは厳禁とします。

2. **Template Adherence & Encapsulated Sections (セクション完結型)**:
   - 新規の試験ガイド・対策ノートを作成する際は、必ず最新の `templates/exam-guide-template.md` の章立て・構造規約を準拠してください。
   - **概要・要点・シナリオの一体化**: 要点解説と実践シナリオを別の章に分離せず、必ず各出題セクション（Domain / Section）の内部に「セクション概要」「重要キーワード」「重要トピック」「実践シナリオ」「参考ドキュメント＆推奨ハンズオン」をすべてカプセル化して記述してください。
   - **タスク・ユースケース単位のシナリオ網羅**: 実践シナリオは代表例の数件にとどまらず、公式試験ガイドに定義された主要タスクおよびユースケース単位で網羅的（各タスク1〜2件以上）に作成してください。

3. **Directory & File Standard**:
   - 成果物はすべて `notes/<vendor>/<cert>/` 配下に配置します（例: `notes/google-cloud/professional-agentic-architect/`、`notes/aws/cloud-ops-engineer-associate/`）。
   - **フラットなファイル配置**: `<cert>/` 直下にコンテンツ用のサブフォルダは切らず、完全版ガイド（`complete-guide.md`）などの Markdown コンテンツを直下にフラット配置します。
   - **画像リソースの集約**: 生成された板書風グラレコや図解画像は、該当資格フォルダ内の `images/`（例: `notes/<vendor>/<cert>/images/`）に集約し、Markdown から相対パス（`./images/...`）で参照します。画像ファイル名は `01-topic-name.png` のように連番とハイフン区切りの半角英数字で統一し、画像内のテキストは日本語で明瞭に作成します。

4. **Quality Standards**:
   - **ピラミッド原則**: 結論先行（Top-down）、縦の論理（So What? / Why So?）、横の論理（MECE）を厳格に維持します。
   - **構造化実践シナリオ（状況 / 対応 / 結果 / 解説）**:
     - 成果物ドキュメントにはエージェントの内部指示用語である「Gherkin」を露出させず、日本語ラベル（`状況` / `対応` / `結果` / `解説`）に統一します。
     - `状況` は前提条件・ビジネス制約を常体で記述し、末尾は読点なしの「〜場合」で終止します。
     - `対応`（アクション）および `結果`（客観的結果）は常体で記述します。
     - `解説` のみを敬体（〜ためです。）とし、単なる機能説明ではなく「採用理由」に加えて「なぜ他の有力代替案では要件を満たせないのか（全代替案の棄却理由）」を必ず論理的に徹底解説します。
   - **一次情報の正確性**: 各セクション末尾に公式ドキュメントおよび推奨ハンズオン（AWS Skill Builder、Google Cloud Skills Boost 等）のリンクを必ず掲載します。

5. **Tone & Manner (No Emoji Policy)**:
   - 装飾用・アイコン用の絵文字（ロケット、電球、人物マーク等を含む一切の絵文字）は出力せず、知的で誠実なプロフェッショナル敬体（です・ます調）を徹底します。

6. **Formatting Hygiene**:
   - 全角スペースの混入を厳禁とし、半角スペースインデントで構文を統一します。
