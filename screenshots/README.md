# screenshots/

このフォルダに以下のファイル名で PNG（または JPG）を配置すると、対応するスライド内のプレースホルダーが自動的に画像表示に差し替わります。

## 配置予定ファイル一覧（Part 4 ハンズオン用）

| ファイル名 | スライド | 内容 |
|------------|---------|------|
| `04-step1-rstudio-startup.png`     | Step 1 R/RStudio 準備 | 起動直後の 4 ペイン画面 |
| `04-step1-install-packages.png`    | Step 1 R/RStudio 準備 | install.packages("logistf") の Console 出力 |
| `04-step2-import-result.png`       | Step 2 データ読み込み | dim() / str() / head() の出力 |
| `04-step2-table-zerocell.png`      | Step 2 データ読み込み | table() でゼロセルを発見 |
| `04-step5-source-paste.png`        | Step 5 実行           | Source ペインへのコード貼り付け |
| `04-step5-error-handling.png`      | Step 5 実行           | エラーを AI に貼り付ける流れ |
| `04-step5-sessioninfo.png`         | Step 5 実行           | sessionInfo() の出力 |
| `04-glm-separation-warning.png`    | 通常 GLM で完全分離   | "fitted probabilities..." 警告と異常な係数 |
| `04-firth-summary.png`             | Firth 罰則付き回帰    | logistf() summary() ─ OR=13.45 等 |
| `04-roc-plot.png`                  | ROC 曲線              | pROC の plot() 結果 |

## 仕様

- ファイルが存在しない場合：プレースホルダー（点線枠 + 説明）が表示されます
- ファイルが存在する場合：自動的に `<img>` タグに差し替えられ、figcaption が下に表示されます
- スマホでも崩れないよう `width: 100%` で表示されます
- ファイル名は上記表のとおり厳密に一致させてください
- 推奨形式：PNG（解像度 1200-2400px 横幅）
- ファイルサイズ目安：1 枚 200-500 KB（大きすぎるとページ表示が遅くなります）
