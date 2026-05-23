# ガジェットレビューラボ — Claude向け運営ガイド

---

## 🔄 セッション引き継ぎ（最終更新: 2026-05-23 セッション2）

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **26本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-23（記事26本体制） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全26本の記事が収益化開始 |
| 🟡 中 | NASおすすめランキング記事作成 | 高単価・ニッチ低競合 |
| 🟡 中 | ロボット掃除機比較記事作成（Roomba vs Eufy vs Roborock） | 詳細比較で差別化 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | 既存記事のアクセス解析→リライト | GSCデータが溜まってから（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-23 セッション2）

- 11本記事追加（モニター・ドライヤー・スマートロック・NAS・ロボット掃除機比較・コードレス掃除機・スマートプラグ・ゲーミングヘッドセット・電気ケトル・4Kテレビランキング）
- 既存記事9本（keyboard・webcam・laptop-stand・smart-speaker・portable-ssd・robot-vacuum・gaming-mouse・air-purifier等）に内部リンク追加

### セッション終了時のチェックリスト（Claude用）

```
□ 上の「状態スナップショット」を最新に更新
□ 「次のアクション」を完了済みを消して新規追加
□ 「直近セッションで実施したこと」を上書き更新
□ git add CLAUDE.md && git commit -m "docs: セッション引き継ぎ更新" && git push
```

---

## ミッション

**Amazonアフィリエイトで収益を得る**ことが唯一の目標。
ガジェット・家電ニッチ。収益ファネルは「検索流入 → 記事熟読 → Amazonリンククリック → 購入」。

## 重要情報（変更時はここを更新）

| 項目 | 値 |
|------|----|
| Amazon アソシエイトID | `merrydietes48-22` |
| 公開URL | https://rkmr-00.github.io/blog/ |
| GitHubリポジトリ | https://github.com/rkmr-00/blog |
| ローカルパス | `c:\work\blog` |
| Amazon審査状況 | 申請中（2026-05-23時点） |

## デプロイ方法

記事を作成・編集したら以下だけでよい。GitHub Actionsが自動でビルド・公開する（約20秒）。

```powershell
git add .
git commit -m "記事追加: タイトル"
git push
```

ローカル確認：
```powershell
$env:PATH = [System.Environment]::GetEnvironmentVariable("PATH", "Machine") + ";" + [System.Environment]::GetEnvironmentVariable("PATH", "User")
hugo server
# → http://localhost:1313/blog/
```

## コンテンツ作成ルール

### 記事の種類と優先度

| 種類 | 優先度 | 理由 |
|------|--------|------|
| ランキング記事 | 最高 | 「おすすめ ランキング」は購買意図が高く最もコンバージョンしやすい |
| 比較記事 | 高 | 「A vs B」「AとBどっち」は購入直前の検索 |
| 購入ガイド | 中 | ロングテールキーワードで安定流入 |
| 単品レビュー | 中 | 指名検索で成約率高いが流入量は少ない |

### ファイル命名・配置

```
content/posts/[キーワード]-[記事タイプ].md
例: wireless-earphone-ranking.md
    robot-vacuum-guide.md
    iphone-case-review.md
```

### フロントマター必須項目

```yaml
---
title: "【2026年最新】〇〇おすすめランキング｜〜で比較"
date: YYYY-MM-DD
draft: false
categories: ["ranking"]  # ranking / review / comparison / guide
tags: ["商品カテゴリ", "おすすめ", "ランキング"]
description: "120字程度のメタディスクリプション。キーワードを自然に含める。"
---
```

### Amazonリンクの書き方

```
{{< amazon id="ASIN番号" title="商品名" >}}
```

ASINはAmazon商品URLの `/dp/XXXXXXXXXX/` の部分。

### SEOライティング指針

- タイトルに「【2026年最新】」「おすすめ」「ランキング」を含める
- 冒頭200字以内に主要キーワードを入れる
- H2見出しにサブキーワードを含める
- 記事末尾に必ずAmazonリンクを入れる（CTAとして機能）
- 文字数目安：ランキング記事3,000字以上・レビュー2,000字以上

## 現在の記事一覧

| ファイル | タイトル概要 | カテゴリ |
|---------|------------|---------|
| `wireless-earphone-ranking.md` | ワイヤレスイヤホン ランキング10選 | ranking |
| `robot-vacuum-ranking.md` | ロボット掃除機 ランキング8選 | ranking |
| `mobile-battery-guide.md` | モバイルバッテリー 選び方・7選 | guide/ranking |
| `smartwatch-ranking.md` | スマートウォッチ ランキング10選 | ranking |
| `noise-cancelling-headphone-comparison.md` | NCヘッドホン比較（Sony vs Bose vs Apple） | comparison/ranking |
| `portable-ssd-ranking.md` | ポータブルSSD ランキング8選 | ranking |
| `gaming-mouse-ranking.md` | ゲーミングマウス ランキング10選 | ranking |
| `electric-toothbrush-ranking.md` | 電動歯ブラシ ランキング8選 | ranking |
| `smart-speaker-ranking.md` | スマートスピーカー ランキング7選 | ranking |
| `tablet-ranking.md` | タブレット ランキング10選 | ranking |
| `webcam-ranking.md` | ウェブカメラ ランキング8選 | ranking |
| `keyboard-ranking.md` | キーボード ランキング10選 | ranking |
| `air-purifier-ranking.md` | 空気清浄機 ランキング8選 | ranking |
| `wireless-charger-ranking.md` | ワイヤレス充電器 ランキング8選 | ranking |
| `laptop-stand-ranking.md` | ノートPCスタンド ランキング8選 | ranking |
| `monitor-ranking.md` | モニター ランキング10選（テレワーク・ゲーミング・4K） | ranking |
| `dryer-ranking.md` | ドライヤー ランキング8選（Dyson・パナソニック比較） | ranking |
| `smart-lock-ranking.md` | スマートロック ランキング8選（賃貸OK・後付け） | ranking |
| `nas-ranking.md` | NAS ランキング8選（Synology・QNAP・Buffalo比較） | ranking |
| `robot-vacuum-comparison.md` | ルンバvsユーフィvsロボロック 3ブランド徹底比較 | comparison |
| `cordless-vacuum-ranking.md` | コードレス掃除機 ランキング8選（Dyson・パナソニック・マキタ比較） | ranking |
| `smart-plug-ranking.md` | スマートプラグ ランキング8選（節電・スマートホーム入門） | ranking |
| `gaming-headset-ranking.md` | ゲーミングヘッドセット ランキング10選（PS5・PC・Switch対応） | ranking |
| `electric-kettle-ranking.md` | 電気ケトル ランキング8選（バルミューダ・デロンギ・タイガー比較） | ranking |
| `4k-tv-ranking.md` | 4Kテレビ ランキング10選（Sony・Samsung・LG・パナソニック比較） | ranking |

## 次に書くべき記事（優先順）

1. コーヒーメーカーおすすめランキング（全自動・カプセル式・ドリップ）
2. 電動自転車おすすめランキング（Panasonic・YAMAHA・ブリヂストン比較）
3. イヤホンおすすめランキング（有線・高音質・コスパ）
4. ゲーミングチェアおすすめランキング（DXRacer・AKRacing比較）
5. スマートウォッチ比較（Apple Watch vs Galaxy Watch vs Pixel Watch）

## 未完了タスク

- [x] Google Search Console登録・サイトマップ送信（2026-05-23 完了・HTMLタグ確認済み）
- [ ] Amazon Associates 審査通過確認
- [ ] 独自ドメイン取得（審査通過後に検討）

## ディレクトリ構成

```
c:\work\blog\
├── hugo.toml                        # サイト設定
├── content/
│   ├── posts/                       # ブログ記事
│   ├── about.md                     # Aboutページ
│   └── privacy.md                   # プライバシーポリシー
├── layouts/shortcodes/
│   └── amazon.html                  # Amazonリンクショートコード
├── assets/css/extended/
│   └── amazon.css                   # Amazonリンクのスタイル
├── archetypes/
│   ├── ranking.md                   # ランキング記事テンプレート
│   └── review.md                    # レビュー記事テンプレート
└── themes/PaperMod/                 # テーマ（submodule）
```
