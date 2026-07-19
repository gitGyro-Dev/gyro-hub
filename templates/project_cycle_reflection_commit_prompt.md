# Commit-based Project Cycle Reflection Prompt Template

このテンプレートは、Gyro Logic、GyroOS、GyroAuthなどの担当スレッドで一定の成果・設計変更・公開準備が発生した際に使用する。

目的は、長いReflection全文を毎回Project Cycleスレッドへ貼り付ける代わりに、担当リポジトリへReflection文書をコミットし、Project Cycleへコミット情報を引き渡すことである。

---

## 使用プロンプト

```text
@GitHub

このスレッドで今回まとまった成果について、Project Cycle Reflectionを作成し、担当リポジトリへコミットしてください。

## 目的

- 今回の成果・判断・未確定事項を構造化して保存する
- Gyro Project Cycle / Gyro Hubへ正確に引き継ぐ
- Reflection本文とGitHub上の確定内容を一致させる
- Project Cycle側がコミットSHAから内容を確認できるようにする

## 保存先

担当リポジトリの既存文書体系を確認し、最も適切な場所へ保存してください。

候補：

- `docs/`
- `project_cycle/`
- `reflections/`

既存の番号体系や命名規則がある場合は、それを優先してください。

推奨ファイル名：

`Project_Cycle_Reflection_YYYYMMDD.md`

または、既存の番号体系がある場合：

`NN_Project_Cycle_Reflection_YYYYMMDD.md`

## Reflection本文の構成

# Project Cycle Reflection

## 0. Commit Context

- Repository:
- Branch:
- Reflection Date:
- Related Commit / PR:
- Summary:

## 1. Hubへ反映する内容

### Dashboard更新

- 現在フェーズ
- 完了事項
- 進行中事項
- 次の主要作業

### Weeklyへ記録する内容

- 今回の成果
- 重要な判断
- 未確定事項
- 次の研究・実装・公開作業

### Roadmap変更

- 完了したMilestone
- 新規Milestone
- 優先順位変更
- Deferred / Cancelled項目

### Artifact追加・更新

- Artifact名
- 状態
- 保存場所
- 依存関係
- 次の作業

### Links追加・更新

- 関連文書
- 論文
- DOI
- Release
- README
- その他の参照先

## 2. Developer Toolkitへ反映する内容

### 自動化候補

### JSON項目候補

### CLIコマンド候補

### Dashboard生成改善案

### 文書・定義・スキーマ検証候補

注意：

- Toolkitは理論や仕様を決定しない
- 未確定項目はExperimental / Candidateと明記する
- Canonical Schemaへの追加可否を明記する

## 3. GitHub更新内容・更新候補

### 今回完了した更新

### 次回更新候補

### 更新しなかったものと理由

対象例：

- README.md
- README_jp.md
- docs/
- paper/
- examples/
- release_candidates/
- workflow
- tests

## 4. 次回 Gyro Project Cycle で扱う内容

優先順位付きで記載する。

1.
2.
3.

## 5. Layer Consistency Check

次の責務境界を確認する。

```text
Gyro Logic
↓
GyroOS
↓
GyroAuth
```

- Gyro LogicのCoreを変更したか
- GyroOSのRuntime責務を変更したか
- GyroAuthの応用概念を下位層へ混在させていないか
- Project Cycleが理論を変更していないか
- Developer Toolkitが定義を決定していないか

判定：

```text
責務の混在なし
```

問題がある場合は、その内容を具体的に記載する。

## 6. Repository Structure

- 新規ファイル
- 更新ファイル
- 移動・削除ファイル
- 文書依存関係
- docs_index / README参照更新の要否

## 7. Canonical / Candidate Boundary

今回の内容を次に分類する。

- Canonical
- Integrated but Provisional
- Candidate
- Experimental
- Deferred
- Rejected

未確定の数式・定義・JSON項目・Response・CLI・API状態を、Canonicalとして記載しない。

## Core Principle

Coreを変更していない場合：

```text
Structure
↓
Slice
↓
Stability
```

Layerを変更していない場合：

```text
Gyro Logic
↓
GyroOS
↓
GyroAuth
```

Project Cycleは運営・統合・可視化を担当し、理論を変更しない。
Developer Toolkitは検証・生成・監査・自動化を支援し、理論や仕様を決定しない。

## GitHub処理

1. Reflection文書を担当リポジトリへ保存する
2. 必要な関連文書だけを同じ作業単位で更新する
3. コミットする
4. コミット後、次の形式だけを最終出力する

```text
Repository:
<owner/repository>

Commit:
<full commit SHA>

Message:
<commit message>

Reflection:
<repository-relative path>

Summary:
<1〜3行の要約>
```

Project Cycle側は、このコミットSHAからReflection本文と実際の変更内容を確認する。

Reflection全文をチャットへ再掲する必要はない。
ただし、GitHubへコミットできなかった場合は、Reflection全文をチャットへ出力する。
```

---

## Project Cycleスレッドへの引継ぎ形式

担当スレッドからProject Cycleスレッドへは、原則として次だけを貼り付ける。

```text
@GitHub

Project Cycle Reflectionを確認し、Hubへの反映要否を判断してください。

Repository:
gitGyro-Dev/<repository>

Commit:
<full commit SHA>

Message:
<commit message>

Reflection:
<repository-relative path>
```

## 運用上の例外

次の場合はReflection全文も貼り付ける。

- GitHubへまだコミットしていない段階でレビューを受けたい
- Reflection文書だけでは判断できない補足事情がある
- GitHub接続または読み取りに失敗した
- コミットにReflection以外の大量変更が含まれ、対象範囲を明示する必要がある
- Project Cycle側で文言や分類を先に相談したい

## 推奨原則

```text
担当スレッド
↓
Reflection文書を担当リポジトリへコミット
↓
Commit SHA / Message / Reflection pathをProject Cycleへ送付
↓
Project Cycleが実ファイルと変更差分を確認
↓
Dashboard / Weekly / Roadmap / Artifacts / Linksへ反映
```
