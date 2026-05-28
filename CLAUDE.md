# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-28 セッション13）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **53本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 楽天アフィリエイト | ✅ 登録済み・19記事に楽天カード追加済み（ID: `543b8391.aa707548.543b8392.c9ec69a5`） |
| X (Twitter) | ⏳ 未開設（セットアップガイド作成済み: docs/x-setup.md） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ✅ 設定済み（測定ID: G-BP0F280FVR・hugo.toml [services.googleAnalytics] に設定済み） |
| 最終デプロイ | 2026-05-28（監査対応・楽天19記事追加・各種改善） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全53本が収益化開始 |
| 🔴 高 | X (Twitter) アカウント開設 | docs/x-setup.md にプロフィール・投稿テンプレート準備済み |
| 🟡 中 | 残り34記事に楽天リンクを追加 | 19記事完了・残りは中低優先度記事（ランキング・ガイド系） |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-28 セッション13）

- **監査（audit-ai）実施・問題対応**：
  - `dehumidifier-ranking.md` の不正ASIN 3件修正（B0CIJD-H20→B096TX3P28、B0CMJ-M120→B08718L27B、B0CIJCPJ140→B079MJ7BVZ）
  - `smart-home-guide.md` タイトル修正（「2026年版」→「2026年最新」に統一）
  - `docs/articles.md` 次記事候補を更新（エアコン・ミラーレスカメラ・ヘアドライヤーランキング追加）
- **楽天リンク追加（16記事）**：electric-bicycle・refrigerator・4k-tv・rice-cooker・washing-machine・tablet・air-purifier・projector・smartphone・smartwatch・monitor・gaming-chair・cordless-vacuum・home-theater-speaker・coffee-maker・dryer（合計19記事に楽天カード設置済み）
- **`washing-machine-ranking.md` ランクショートコード追加**：ドラム式TOP4・縦型TOP4それぞれにrank 1〜4を適用（特殊構造のため各カテゴリ内でrank="1"から振り直し）
- **比較記事4本にクイックピックス追加**：noise-cancelling-headphone-comparison・cordless-vs-corded-vacuum-comparison・robot-vacuum-comparison・smartwatch-comparison

### セッション終了時のチェックリスト

```
□ 状態スナップショットを最新に更新
□ 「次のアクション」の完了済みを消して新規追加
□ 「直近セッションで実施したこと」を上書き更新
□ 記事を追加した場合は docs/articles.md も更新
□ git add . && git commit -m "docs: セッション引き継ぎ更新" && git push
```

---

## ミッション

**アフィリエイトで収益を得る**ことが唯一の目標（Amazon + 楽天の二本柱）。
収益ファネル：検索流入 → 記事熟読 → Amazon/楽天リンククリック → 購入

## 重要情報

| 項目 | 値 |
|------|----|
| Amazon アソシエイトID | `merrydietes48-22` |
| 楽天アフィリエイトID | `543b8391.aa707548.543b8392.c9ec69a5` |
| 公開URL | https://rkmr-00.github.io/blog/ |
| GitHubリポジトリ | https://github.com/rkmr-00/blog |
| ローカルパス | `c:\work\blog` |

## デプロイ方法

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

## 未完了タスク

- [x] Google Search Console登録・サイトマップ送信（2026-05-23 完了）
- [ ] Amazon Associates 審査通過確認
- [ ] X (Twitter) アカウント開設（ガイド: docs/x-setup.md）
- [x] 楽天アフィリエイト登録完了（2026-05-27）・ウィジェット設置済み
- [ ] 楽天商品別リンクを主要記事に追加
- [ ] 独自ドメイン取得（Associates通過後に検討）
