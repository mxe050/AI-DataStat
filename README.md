# AI時代のデータ解析 ─ Yuasa 2002 を題材に

**再現性・ハルシネーション・倫理**を一気通貫で学ぶインタラクティブHTMLプレゼンテーション

🌐 **ライブデモ**：[https://mxe050.github.io/AI-DataStat/](https://mxe050.github.io/AI-DataStat/)

---

## 概要

2002年に発表された自身の論文（下顎埋伏智歯の抜歯困難度予測）を"生きた教材"として、AI時代の統計解析のあり方を学ぶ講演スライドです。

### 学習目標

1. **臨床研究の統計手法を批判的に評価する**（EPV・完全分離・Firth回帰）
2. **LLMハルシネーションの統計学的原因を理解する**（Kalai & Vempala 2024 の IIV 還元）
3. **AIで生成したRコードの検証方法を習得する**（Analyst-Inspector 方式）
4. **2002年と2026年の統計手法の違いを説明できる**
5. **AIを研究に使う際の倫理的開示義務を理解する**（AMEE Guide No.192）

---

## ファイル構成

| ファイル | 内容 |
|---------|------|
| `index.html` | メインのスライドアプリ（単一HTML、約140KB） |
| `yuasa2002md.txt` | 原論文（2002）のMarkdown全文 |
| `yuasa2002csv.txt` | 再構成した仮想データ（44症例、TSV形式） |
| `Yuasa2002難易度.xlsx` | Excel版データ |
| `yuasa2002_unlocked.pdf` | 原論文PDF |

---

## スライド構成（7パート・全40スライド）

| Part | テーマ | 含まれる内容 |
|------|--------|-------------|
| **Part 1** | リサーチクエスチョンとAI文献レビュー | PICO定義、AI検索プロンプト、ハルシネーション実例（Kalai Table 1） |
| **Part 2** | 題材論文の背景 | Pell & Gregory 分類の解剖学的SVG、Yuasa 2002 の2段階デザイン、Table 2-6 解説 |
| **Part 3** | 統計手法の批判的検討 | 5つの問題点、**🎮 完全分離インタラクティブ**、EPV曲線 |
| **Part 4** | ハルシネーションの科学 | Kalai IIV還元図、Singleton 概念、ベンチマーク採点表、エラー3類型 |
| **Part 5** | AI × R による再解析 | **📊 44症例データビューア**、Firth回帰実行、ROC曲線 |
| **Part 6** | AI使用の倫理と開示 | AMEE Guide No.192、TRIPOD+AI、開示フローチャート |
| **Part 7** | まとめと参考文献 | Take-home 11項目、詳細な書誌情報付き参考文献26件 |

---

## インタラクティブ機能

### 🎮 完全分離シミュレーター（Part 3）
スライダーで Control 群の Level C セル値を変化させると、オッズ比が対数軸グラフ上でリアルタイムに発散する様子を体感できます。

### 📊 仮想データビューア（Part 5）
再構成した44症例の全変数（Depth, Ramus, Spatial, RootCurvature, RootWidth 等）をテーブル形式で閲覧。Difficult群は色分け表示。

### 📈 ROC曲線・比較バーチャート（Part 5）
Chart.js によるインタラクティブなROC曲線と、原論文 vs 再解析結果の対数軸比較。

---

## 技術仕様

- **単一HTML**：依存関係は CDN の Chart.js と MathJax のみ
- **レスポンシブ**：PC（大きな文字・完全版）とスマートフォン（簡略版）で自動切り替え
- **ダークテーマ**：医学プレゼンでの投影に最適化
- **キーボード操作**：`←` / `→` / `Home` / `End` / `F`（フルスクリーン）
- **SVG図**：PICO概念図、研究タイムライン、Pell&Gregory解剖図、IIV還元図 など

---

## 参考文献（主要★）

### ハルシネーション理論

- ★★ **Kalai AT, Nachum O, Vempala SS, Zhang E.** Why Language Models Hallucinate. *arXiv* 2025; [arXiv:2509.04664](https://arxiv.org/abs/2509.04664)
- ★ **Kalai AT, Vempala SS.** Calibrated Language Models Must Hallucinate. *STOC 2024*:160-171. [DOI: 10.1145/3618260.3649777](https://doi.org/10.1145/3618260.3649777)
- ★ **Zeng Q et al.** An Analyst-Inspector Framework for Evaluating Reproducibility of LLMs in Data Science. *arXiv* 2025; [arXiv:2502.16395](https://arxiv.org/abs/2502.16395)

### 統計手法

- **Firth D.** Bias reduction of maximum likelihood estimates. *Biometrika* 1993;80(1):27-38.
- **Heinze G, Schemper M.** A solution to the problem of separation in logistic regression. *Stat Med* 2002;21(16):2409-2419.
- **Harrell FE Jr.** *Regression Modeling Strategies.* 2nd ed. Springer 2015.
- **Collins GS et al.** TRIPOD+AI statement. *BMJ* 2024;385:e078378.

### AI使用の倫理

- **Masters K et al.** When and how to disclose AI use in academic publishing: AMEE Guide No.192. *Med Teach* 2026;48(4):542-553.
- **Resnik DB, Hosseini M.** Disclosing AI use in scientific research and publication. *Account Res* 2026;33(2):2481949.

### 題材論文

- **Yuasa H, Kawai T, Sugiura M.** Classification of surgical difficulty in extracting impacted third molars. *Br J Oral Maxillofac Surg* 2002;40(1):26-31. [DOI: 10.1054/bjom.2001.0684](https://doi.org/10.1054/bjom.2001.0684) · PMID: 11883966

完全な参考文献リスト（26件）はスライド内 Part 7 をご覧ください。

---

## ローカルでの実行

```bash
git clone https://github.com/mxe050/AI-DataStat.git
cd AI-DataStat
# ブラウザで index.html を開くだけ
start index.html    # Windows
open index.html     # macOS
xdg-open index.html # Linux
```

サーバは不要です。ファイルを開くだけで動作します。

---

## ライセンス

本スライド・コードは教育目的で自由にご利用ください（MIT License相当）。
2002年原論文の著作権は British Association of Oral and Maxillofacial Surgeons に帰属します。

---

## 著者

**Hidemichi Yuasa** DDS PhD
- 原論文著者（2002）
- 本教材作成（2026）

## Acknowledgement

本スライドの作成にあたり、**Claude (Anthropic)** を用いて構成案の壁打ち・統計手法の検証・参考文献の整理を行いました。
すべての最終的な解釈・記載内容の責任は著者にあります（AMEE Guide No.192 に基づく開示）。
