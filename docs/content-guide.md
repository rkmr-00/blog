# コンテンツ作成ガイド

記事執筆時に参照する固定ルール集。変更する場合はここを更新する。

---

## 記事の種類と優先度

| 種類 | 優先度 | 理由 |
|------|--------|------|
| ランキング記事 | 最高 | 「おすすめ ランキング」は購買意図が高く最もコンバージョンしやすい |
| 比較記事 | 高 | 「A vs B」「AとBどっち」は購入直前の検索 |
| 購入ガイド | 中 | ロングテールキーワードで安定流入 |
| 単品レビュー | 中 | 指名検索で成約率高いが流入量は少ない |

## ファイル命名・配置

```
content/posts/[キーワード]-[記事タイプ].md
例: wireless-earphone-ranking.md
    robot-vacuum-guide.md
    iphone-case-review.md
```

## フロントマター必須項目

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

## Amazonリンクの書き方

```
{{< amazon id="ASIN番号" title="商品名" >}}
```

ASINはAmazon商品URLの `/dp/XXXXXXXXXX/` の部分。

## SEOライティング指針

- タイトルに「【2026年最新】」「おすすめ」「ランキング」を含める
- 冒頭200字以内に主要キーワードを入れる
- H2見出しにサブキーワードを含める
- 記事末尾に必ずAmazonリンクを入れる（CTAとして機能）
- 各ランキング製品に個別の評価文を100字以上書く（テーブル1行まとめ禁止）
- 「あわせて読みたい」セクションで内部リンクを最低2本設置する
- 文字数目安：ランキング記事3,000字以上・レビュー2,000字以上

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
├── docs/
│   ├── content-guide.md             # 執筆ルール・SEO指針（本ファイル）
│   └── articles.md                  # 記事一覧・次に書くべき記事
└── themes/PaperMod/                 # テーマ（submodule）
```
