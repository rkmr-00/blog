# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-28 セッション14）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **53本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 楽天アフィリエイト | ✅ 登録済み・**全53記事に楽天カード追加済み**（ID: `543b8391.aa707548.543b8392.c9ec69a5`） |
| X (Twitter) | ✅ 開設済み（@GadgetReview_jp）・hugo.tomlにソーシャルアイコン追加済み |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ✅ 設定済み（測定ID: G-BP0F280FVR・hugo.toml [services.googleAnalytics] に設定済み） |
| 最終デプロイ | 2026-05-28（プロジェクト全体整備・楽天全記事追加・X連携） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全53本が収益化開始 |
| 🔴 高 | X (@GadgetReview_jp) で記事告知ツイート開始 | アカウント開設済み・docs/x-setup.md に投稿テンプレート準備済み |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |
| 🟢 低 | 新規記事追加（エアコン・ミラーレスカメラ・ヘアドライヤー） | docs/articles.md に候補あり |

### 直近セッションで実施したこと（2026-05-28 セッション14）

- **プロジェクト全体整備（精査・整備）**：
  - X (@GadgetReview_jp) 開設対応：hugo.toml にソーシャルアイコン追加・docs/x-setup.md 更新
  - layouts/single.html：PR開示バナーに楽天アフィリエイトを追記
  - about.md：楽天開示・X SNSセクション追加
  - privacy.md：アフィリエイトプログラム開示を Amazon+楽天両方に更新
  - gaming-setup-guide.md・smart-home-guide.md にクイックピックス追加
- **楽天リンク全記事完了（34記事追加）**：air-purifier-humidifier・dehumidifier・dishwasher・electric-kettle・electric-pressure-cooker・electric-toothbrush・fan-circulator・gaming-headset・gaming-keyboard・gaming-mouse・hair-iron・humidifier・smart-lock・smart-plug・water-server・wired-earphone・nas・noise-cancelling-headphone-comparison・portable-ssd・robot-vacuum-comparison・smart-home-guide・smart-speaker・webcam・wireless-charger・cordless-vs-corded-vacuum-comparison・keyboard・laptop-stand・microwave・mobile-battery-guide・portable-power-station・hot-plate・smartwatch-comparison・vacuum-cleaner・gaming-setup-guide（**全53記事に楽天カード設置完了**）

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
- [x] X (Twitter) アカウント開設（@GadgetReview_jp・2026-05-28 完了）
- [x] 楽天アフィリエイト登録完了（2026-05-27）・ウィジェット設置済み
- [x] 楽天商品別リンクを全記事に追加（2026-05-28 全53記事完了）
- [ ] 独自ドメイン取得（Associates通過後に検討）
