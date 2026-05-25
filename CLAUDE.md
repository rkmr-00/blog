# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-26 セッション6）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **36本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-26（PV増加施策：新記事2本追加・内部リンク強化） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全36本が収益化開始 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟡 中 | 加湿器おすすめランキング記事追加 | 秋冬に向けて早めに準備（先行インデックス狙い） |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-26 セッション6）

- PV増加施策を自律実施（内部リンク強化・新記事2本追加）
- **内部リンク整備**：gaming-setup-guide へのリンクをgaming-mouse/headset/chair/keyboardに追加（4記事）、smart-lockにsmart-plugリンク追加
- **新記事追加①**：fan-circulator-ranking.md（扇風機・サーキュレーターランキング10選・5月タイムリー記事）
- **新記事追加②**：water-server-ranking.md（ウォーターサーバーランキング8選・年間需要）
- **クロスリンク整備**：新記事から/への内部リンクを air-purifier/smart-plug/electric-kettle/coffee-maker/refrigerator に追加
- hugo.toml ホーム文言の記事数更新: 34記事→36記事

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
