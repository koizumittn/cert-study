# Certification Study Workspace

## 1. Purpose
本ワークスペースは、クラウドベンダー認定資格（Google Cloud、AWS 等）の実践的学習ドキュメントおよび対策ノートを作成・管理・運用するための専用リポジトリです。
`my-skills` リポジトリの認定学習パイプラインを活用し、最高品質の学習資産を体系的に蓄積します。

---

## 2. Agent Guidelines & Principles
本ワークスペースで作業するエージェントは、以下の原則を厳格に順守してください。

1. **Pipeline Execution**:
   - 学習ドキュメントの生成・推敲時は、読み込まれている `cert-study-director` を軸として各専門スキル（`concept-summarizer`, `scenario-generator`, `logical-reviewer`, `graphic-recorder`, `link-checker` 等）を協調・発火させてください。
2. **Directory Standard**:
   - 成果物はすべて `notes/<exam-name>/` 配下に Markdown 形式で整理します（例: `notes/google-cloud-pca/`）。
3. **Quality Standards**:
   - ピラミッド原則に基づく厳格な論理構造（縦の論理・横の論理）を維持します。
   - 実践シナリオは Gherkin 構文（Given/When/Then/Because）に基づき、なぜ代替案ではダメなのかの思考を追体験できる深層 Because 句を必ず含めます。
4. **Tone & Manner (No Emoji Policy)**:
   - 装飾用・アイコン用の絵文字（🚀, 👤 等）は一切出力せず、知的で誠実なプロフェッショナル敬体（です・ます調）を徹底します。
5. **Formatting Hygiene**:
   - 全角スペースの混入を厳禁とし、半角スペースインデントで構文を統一します。
