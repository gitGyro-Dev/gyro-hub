# Gyro Hub 日本語版

> Gyro Ecosystem と Gyro Project Cycle の公式入口。

Gyro Hub は、Gyro Project 全体の入口であり、進捗・成果・論文・PoC・開発ツール・公開情報をつなぐための Project Hub です。

Gyro は、完全一致ではなく、構造化された観測の中で安定した振る舞いがどのように成立するかを扱う研究開発エコシステムです。

Gyro が問うのは、

> これは完全に同一か？

ではなく、

> ズレがあっても、構造は安定して保たれているか？

です。

---

## Gyro Project Cycle

Gyro Hub は、単なるREADMEやDashboardではありません。

Gyro Project 全体を継続的に育てるための、次の研究サイクルを管理・可視化する入口です。

```text
Brainstorm
↓
Hypothesis / Idea
↓
X / Communication
↓
GitHub Documentation
↓
PoC / Prototype
↓
Paper / Release
↓
Feedback
↓
Refinement
↓
Brainstorm
```

この循環によって、初期アイデアを、ドキュメント、PoC、論文、リリース、フィードバック、次の研究へと発展させます。

---

## Gyro Ecosystem

```text
                 Gyro Hub
                     |
   +-----------------+-----------------+
   |                 |                 |
Gyro Logic       GyroOS          GyroAuth
   |                 |                 |
   +-----------------+-----------------+
                     |
         Gyro Developer Tools
                     |
 Papers • DOI • Releases • Demos • X • Feedback
```

---

## 主要プロジェクト

| Project | 役割 | Repository |
|---------|------|------------|
| Gyro Logic | 理論基盤 | [gitGyro-Dev/gyrologic](https://github.com/gitGyro-Dev/gyrologic) |
| GyroOS | Runtime / 実装アーキテクチャ | [gitGyro-Dev/gyroos](https://github.com/gitGyro-Dev/gyroos) |
| GyroAuth | Stability-based Authentication 応用 | [gitGyro-Dev/gyroauth](https://github.com/gitGyro-Dev/gyroauth) |
| Gyro Developer Tools | GitHub運用・開発支援ツール | [gitGyro-Dev/gyro-dev-tools](https://github.com/gitGyro-Dev/gyro-dev-tools) |
| Gyro Hub | Project Hub / 全体入口 | [gitGyro-Dev/gyro-hub](https://github.com/gitGyro-Dev/gyro-hub) |

---

## レイヤー構造

| Layer | Project | 説明 |
|-------|---------|------|
| Theory | Gyro Logic | Gyroの概念・数理・理論基盤を定義する |
| Runtime | GyroOS | Gyroの概念をRuntimeアーキテクチャとして実装する |
| Application | GyroAuth | Stability-based Selection を認証に応用する |
| Development | Gyro Developer Tools | GitHub操作、リリース、運用、自動化を支援する |
| Hub | Gyro Hub | 全体をつなぐ入口・Project Hub・Dashboard基盤 |

固定原則として、Gyro Logic → GyroOS → GyroAuth の関係を維持します。

```text
Gyro Logic = Theory
GyroOS     = Runtime
GyroAuth   = Application
```

上位は下位に依存せず、下位は上位を実装します。

---

## Hub内の主要ページ

| Page | 目的 |
|---|---|
| [README.md](README.md) | 英語版入口 |
| [Projects](projects.md) | プロジェクト一覧 |
| [Papers](papers.md) | 論文・DOI・公開成果 |
| [Roadmap](roadmap.md) | 今後の開発・研究方針 |
| [Dashboard](dashboard.md) | 現在のProject状況 |
| [Research Cycle](research_cycle.md) | Gyro Project Cycle の説明 |
| [Artifacts](artifacts.md) | 成果物の成熟度管理 |
| [Weekly](weekly.md) | 週次レポートの構成 |
| [Links](links.md) | 外部リンク集 |

---

## 各媒体の役割

Gyro Project では、媒体ごとの役割を分けます。

```text
Gyro Hub
= 人が見る入口 / Project Hub / 運営ハブ

Dashboard
= 現在地を表示する画面

dashboard.json
= システム間で使う共通データ

GitHub
= 最新版の研究 / Single Source of Truth

Paper / Jxiv / Zenodo
= 成熟した成果の公開

X
= 途中成果、問い、PoC、研究過程の発信

Google Drive
= 保存先 / Archive

NotebookLM
= Knowledge Hub

Developer Toolkit
= 情報収集・同期・自動生成
```

重要なのは、Dashboardを情報源にしないことです。

Dashboardは状態を持たず、Developer Toolkit が生成した `dashboard.json` を読み、`dashboard.md` や将来のWeb Dashboard / GyroOS Dashboard に展開します。

```text
Gyro Developer Tools / Gyro Commands
↓
dashboard.json
├─ dashboard.md
├─ GitHub Pages
├─ Web Dashboard
└─ GyroOS Dashboard
```

---

## Artifact Lifecycle

Gyro Hub では、媒体ではなく「成果物」の成熟度を管理します。

```text
Idea
↓
Note
↓
PoC
↓
Documentation
↓
Paper
↓
Release
↓
Feedback
↓
Revision / Next Idea
```

たとえば、Boundary-aware Runtime は、Idea → Documentation → PoC → Paper候補 のように発展していきます。

---

## Gyro Weekly

Gyro Weekly は、週次の研究・開発ログです。

```text
Dashboard = 現在地
Weekly    = 今週の流れ
Roadmap   = 今後の方向
```

Weeklyでは、以下を記録します。

- GitHub更新
- PoC
- 論文・DOI
- X投稿
- Brainstorm
- Issue / Feedback
- 今週の判断
- 次週予定
- Open Questions

将来的には Gyro Developer Tools から自動生成することを想定します。

---

## 現在の状況

| Project | Status |
|---------|--------|
| Gyro Logic | Released |
| GyroOS | In Design |
| GyroAuth | PoC Available / Publication Track |
| Gyro Developer Tools | In Development |
| Gyro Hub | Project Cycle Setup |

---

## 現在の公開成果

| Project | Medium | DOI |
|---|---|---|
| Gyro Logic | Jxiv English | 10.51094/jxiv.4159 |
| Gyro Logic | Jxiv Japanese | 10.51094/jxiv.4597 |
| Gyro Logic | Zenodo v2.4 | 10.5281/zenodo.19674375 |

---

## 次に進めること

現時点の次アクションは以下です。

1. `dashboard.json` の初期Schemaを安定させる
2. `data/` ディレクトリを追加する
3. 初回 `weekly/2026-W27.md` を作成する
4. Gyro Developer Tools から `dashboard.json` を生成できるようにする
5. Jxiv / Zenodo / DOI のPublication同期フローを整理する
6. Artifact Tracking を拡張する

---

## 最終目標

Gyro Hub の目的は、Gyro Project を単なるGitHubリポジトリ群や論文一覧ではなく、継続的に研究を育てる Research Platform として運用することです。

Gyro Hub は、理論、Runtime、応用、PoC、論文、GitHub、X、Google Drive、NotebookLM、Developer Toolkit、Feedback をつなぎ、Gyro Project Cycle を回すための中心入口になります。
