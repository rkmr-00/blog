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

## ランキング記事の必須構成要素

ランキング記事の「ひな型」は `wireless-earphone-ranking.md`。新規作成時は `archetypes/ranking.md` を使用。

### 1. クイックピックボックス（記事冒頭）

冒頭リード文の直後・「## この記事でわかること」の前に配置。コンバージョン最大化のため**必須**。

```html
{{< rawhtml >}}
<div class="quick-picks">
  <p class="quick-picks-title">🏆 結論だけ知りたい方へ：[カテゴリ]おすすめTOP3</p>
  <ul class="quick-picks-list">
    <li>
      <span class="quick-pick-rank">1位</span>
      <span class="quick-pick-text"><strong>[用途]</strong>：[商品名] ｜ [30字以内キャッチ]</span>
      <a href="https://www.amazon.co.jp/dp/[ASIN]/?tag=merrydietes48-22" target="_blank" rel="nofollow noopener" class="quick-pick-btn">今すぐ確認 →</a>
    </li>
    <!-- 2位・3位も同形式 -->
  </ul>
</div>
{{< /rawhtml >}}
```

### 2. ランクショートコード（1〜3位）

1〜3位はビジュアルバッジ付きのカードで表示。`{{% rank %}}` は Markdown を内部で処理するため `{{%` 記法を使用。

```
{{% rank rank="1" %}}
### 商品名（キャッチコピー）

内容...

{{< amazon id="ASIN" title="商品名" badge="編集部ベストバイ2026" reviews="★X.X レビューX,XXX件以上" price="参考価格 約XX,XXX円前後" campaign="🏆 キャンペーン文" reason="購入を後押しする理由（80字以内）" >}}
{{< rakuten item_url="https://item.rakuten.co.jp/[shop]/[item]/" title="商品名" badge="楽天ポイント還元" reason="楽天ポイントで購入したい方はこちら！" >}}
{{% /rank %}}
```

4位以降は通常見出し（`### 第4位：...`）。ランクショートコード不要。

### 3. Amazonカードの書き方

```
{{< amazon id="ASIN番号" title="商品名" >}}
```

**全パラメータ（1位では全項目を使う）：**
- `id` — ASIN（Amazon商品URLの `/dp/XXXXXXXXXX/` の部分）
- `title` — 商品名
- `badge` — バッジテキスト（例：「編集部ベストバイ2026」）
- `reviews` — レビュー数（例：「★4.5 レビュー1,800件以上（2026年5月調査時点）」）
- `price` — 参考価格（例：「参考価格 約42,000円前後」）
- `campaign` — CTA文（例：「🏆 テレワーク1位・今すぐ確認」）
- `reason` — 購入理由（80字以内）

### 4. 楽天カードの書き方

```
{{< rakuten item_url="https://item.rakuten.co.jp/[shop]/[item]/" title="商品名" badge="楽天ポイント還元" reason="楽天ポイントを貯めている方はこちら！" >}}
```

**方法①：楽天商品URLから自動生成（推奨）**
- `item_url` — 楽天市場の商品ページURL（アフィリエイトURLを自動生成）
- `title` / `badge` / `reason` / `price` / `reviews` / `image` / `campaign` — オプション

**方法②：アフィリエイトツール生成URLを直接使用**
- `url` — 楽天アフィリエイトツールで生成したフルURL

### 5. check ショートコード（1位に必須）

```
{{< check >}}
- 編集部が実際に確認した点1
- 編集部が実際に確認した点2
{{< /check >}}
```

## Amazonリンクの書き方（簡易版）

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
│   ├── amazon.html                  # Amazonリンクショートコード
│   ├── rakuten.html                 # 楽天アフィリエイトショートコード
│   ├── rank.html                    # ランキングバッジ（1〜3位カード）
│   └── check.html                   # 編集部確認ボックス
├── assets/css/extended/
│   ├── amazon.css                   # Amazonカードのスタイル
│   └── rakuten.css                  # 楽天カードのスタイル（ブランドレッド）
├── archetypes/
│   ├── ranking.md                   # ランキング記事テンプレート
│   └── review.md                    # レビュー記事テンプレート
├── docs/
│   ├── content-guide.md             # 執筆ルール・SEO指針（本ファイル）
│   └── articles.md                  # 記事一覧・次に書くべき記事
└── themes/PaperMod/                 # テーマ（submodule）
```
