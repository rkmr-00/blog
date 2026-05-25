# ガジェットレビューラボ — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-26 セッション4）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **35本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-26（購買意欲スコア3エージェントR12で91.0達成・全ASIN整合修正） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全35本が収益化開始 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | 既存記事のアクセス解析→リライト | GSCデータが溜まってから（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-26 セッション4）

- 購買意欲スコアリングループ（Strategy/Design/Audit 各100点満点）R9→R12で平均91.0到達（目標90超クリア）
- ASIN整合修正: wireless-earphone / robot-vacuum / mobile-battery 全製品の説明文とASINを一致させた
- 景表法対応: urgency文言を煽り表現から中立的な在庫変動案内に変更、CSS背景色も赤→グレーに
- PR開示バナー追加: `layouts/single.html` オーバーライドで全記事トップに表示
- cover.html修正: `layouts/_partials/` → `layouts/partials/` に移動してカテゴリ別グラデーションを復活
- amazon.htmlショートコード: `reason`パラメータ追加（購入動機の一文を差し込み）
- gaming-setup-guide.md 追加（ゲーミングデスク環境ガイド）

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

**Amazonアフィリエイトで収益を得る**ことが唯一の目標。
収益ファネル：検索流入 → 記事熟読 → Amazonリンククリック → 購入

## 重要情報

| 項目 | 値 |
|------|----|
| Amazon アソシエイトID | `merrydietes48-22` |
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
- [ ] 独自ドメイン取得（審査通過後に検討）
