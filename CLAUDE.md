# ガジェットレビューラボ — Claude向け運営ガイド

---

## 🔄 セッション引き継ぎ（最終更新: 2026-05-24 セッション3）

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **31本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-23（記事31本体制） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全31本の記事が収益化開始 |
| 🟡 中 | NASおすすめランキング記事作成 | 高単価・ニッチ低競合 |
| 🟡 中 | ロボット掃除機比較記事作成（Roomba vs Eufy vs Roborock） | 詳細比較で差別化 |
| (中) | 既存記事の品質補完（内部リンク・CTA・CSS） | Amazon審査通過に向けコンテンツ品質向上が必要 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | 既存記事のアクセス解析→リライト | GSCデータが溜まってから（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-24 セッション3）

- Audit_AI監査指摘に基づき、既存記事の品質改善を作業（8項目）
- CLAUDE.mdの記事数誤記を31本に修正
- electric-toothbrush-ranking・smartwatch-rankingに「あわせて読みたい」内部リンクを追加
- タイトル5本の「最新」欠落を修正（robot-vacuum-ranking他）
- air-purifier-rankingの6～8位を詳細評価文＋Amazonリンク付きに充実
- Amazonカードにダークモード対応CSSを追加（amazon.css）
- cover imageが空文字の記事8本のフロントマターから空フィールドを削除

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
| `coffee-maker-ranking.md` | コーヒーメーカー ランキング8選（全自動・カプセル・ドリップ比較） | ranking |
| `gaming-chair-ranking.md` | ゲーミングチェア ランキング8選（DXRacer・AKRacing・Secretlab比較） | ranking |
| `electric-bicycle-ranking.md` | 電動自転車 ランキング8選（パナソニック・ヤマハ・ブリヂストン比較） | ranking |
| `wired-earphone-ranking.md` | 有線イヤホン ランキング10選（高音質・コスパ・SHURE・final比較） | ranking |
| `smartwatch-comparison.md` | Apple Watch vs Galaxy Watch vs Pixel Watch 3ブランド比較 | comparison |
| `home-theater-speaker-ranking.md` | ホームシアタースピーカー ランキング8選（Sonos・Bose・JBL・ヤマハ比較） | ranking |

## 次に書くべき記事（優先順）

1. 冷蔵庫おすすめランキング（Panasonic・日立・三菱比較）
2. 洗濯機おすすめランキング（縦型・ドラム式・乾燥機能比較）
3. ゲーミングPC周辺機器まとめ（デスク環境セット提案記事）
4. ウォーターサーバーおすすめランキング
5. 加湿器おすすめランキング（シャープ・パナソニック比較）

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
