# ガジェットレビューラボ — Claude向け運営ガイド

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

## 次に書くべき記事（優先順）

1. スマートスピーカーおすすめランキング（Echo・HomePod比較）
2. タブレットおすすめランキング（iPad・Android・Fire HD比較）
3. ウェブカメラおすすめランキング（テレワーク・配信向け）
4. キーボードおすすめランキング（メカニカル・静音・テレワーク向け）
5. 空気清浄機おすすめランキング（花粉症・ペット向け）
6. ワイヤレス充電器おすすめランキング（Qi2・MagSafe対応）
7. ノートPCスタンドおすすめランキング（テレワーク向け）

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
