# 応募主張の根拠照合 v0.1 — 2026-11-24
Jxiv DOI直接取得不可。GitHub投稿原稿・README・コード・保存出力を静的に照合。公開PDF同一性、再実行、独立先行研究調査は未了。新規性・性能の証明ではない。

## A GyroAuth
提案: State Convergenceに基づく認証と、将来の認証基準更新の独立評価。候補と採用を分離。
実装根拠: release notesのN1 正当な新端末 DEFER→ACCEPT、P1 直接採用による基準拡大とguarded FREEZE、C1 単一Evidence源の侵害時FREEZE。AUTH_STABLE + FREEZE。app/vnext/main.py は別のmockで四認証状態を扱う。実運用なし。
比較軸: RBA/継続認証との差を評価基準の更新統制に置く。既存のguarded adaptation全般に対する新規性は未確認。
仮説: 実環境でのpoisoning耐性、誤拒否率、プライバシー、低負荷。
根拠: https://github.com/gitGyro-Dev/gyroauth/blob/main/paper/guarded_criterion_trajectories_submission_en.md
https://github.com/gitGyro-Dev/gyroauth/blob/main/release_candidates/gyroauth/v2.1.0/release_notes.md
DOI https://doi.org/10.51094/jxiv.5671 （README公開記載）

## B Trajectory Security
提案: valid events != stable trajectory。Boundary/Negative Definition、Trajectory Detection、Stability Responseの三層。本人性でなくログイン後の操作列評価。
実装: demo.py は合成ログを時刻順にまとめ、7種のルールベースDeviationと重み、exp(-delta)、固定閾値で対応候補を出力。保存results.json: normal 1.0 continue、suspicious .6219 challenge、attack .0669 isolate。実際の隔離やMFAは実行せず、リアルタイム監視でもない。三層全部の実装とは言わない。
比較軸: 個別許可と操作列許容性の区別、三層の統一的定式化。UEBA/EDR/SOARにも類似機能あり。少量データでの優位・閾値不要は未証明（現コードは明示閾値）。
仮説: 未知攻撃への有効性、誤検知削減、実製品連携、原因不明の状態のみからの推定。
根拠: https://github.com/gitGyro-Dev/gyroauth/tree/main/examples/trajectory_vulnerability_response （paper_jp.md, demo.py, outputs/results.json）
DOI https://doi.org/10.51094/jxiv.5440

## C GyroOS
提案: bounded execution、canonical runtime ownership、read-only projection、non-canonical inspection、external consumerの責任分離。一要求一Process。StabilityとOperator Responseを分離。
実装: poc/run_poc.py は共通ProcessExecutorでCONTINUE、RESLICE準備、DEFER（pending record）、ADJUST、JUMPのシナリオを検査。明示したPoCポリシー入力による選択であり、普遍自律判断ではない。README/投稿原稿では単一ホストSQLite、明示参照Inspectionを記載。
比較軸: OODA/MAPE-K/状態機械にも保留・再観測可能。差はcanonical履歴所有と読み取り専用観測、評価/応答/継続の契約分離の組合せ。性能比較なし。
仮説: AIエージェントへの適用・安全性、実用上の利益、汎用OS。追加デモは未実施。日本語論文はREADME上準備予定。
根拠: https://github.com/gitGyro-Dev/gyroos/blob/main/paper/gyroos_v4_jxiv_submission_en.md
https://github.com/gitGyro-Dev/gyroos/blob/main/poc/run_poc.py
https://doi.org/10.51094/jxiv.5842

## D Gyro Logic
提案: Structure→Slice→Stability。局所表出、局所単位化（事象終了と別）、Stability Scene（終端・スカラーへ還元しない）、文脈Tracing（ログや状態列と別）、Incorporated Readability。
成果: 探索的形式schemaと数学諸分野比較。論文は新規実証データなし、strict minimality・普遍Stability metric・一般Tracing algorithm・完全公理化を主張しない。
比較軸: 既存数学の部分モデルを否定せず、上記区別を同時に保持する形式化。既存論理で不可能とは言わない。
仮説: 領域横断妥当性、実行可能な形式化、認知・多次元計算機応用。
根拠: https://github.com/gitGyro-Dev/gyrologic/blob/main/paper/minimal_formal_model_submission_jp_v2.md
https://doi.org/10.51094/jxiv.6894

## 次のゲート
A/B/C主軸、D挑戦枠（未決定）。Aは基準更新、Bは操作列と対応、Cは実行契約、Dは局所成立の形式化を中心にv0.2を作成。既存技術との差は設計上の比較軸として記述し、独立先行研究調査と再実行は残件。公開済み範囲のみ使用。
