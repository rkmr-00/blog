# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-26 セッション7）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **38本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-26（新記事2本追加・内部リンク8記事強化） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全38本が収益化開始 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟡 中 | プロジェクターおすすめランキング記事追加 | ホームシアター需要・高単価アフィリエイト |
| 🟡 中 | ヘアアイロンおすすめランキング記事追加 | 女性ユーザー獲得・Dyson等高単価商品 |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-26 セッション7）

- **新記事追加①**：humidifier-ranking.md（加湿器おすすめランキング10選・超音波/スチーム/気化式/ハイブリッド比較）
  - ダイニチ/シャープ/象印/パナソニック×2/ダイキン/三菱重工/バルミューダ/コロナ/アイリスオーヤマ 10製品掲載
- **新記事追加②**：vacuum-cleaner-ranking.md（掃除機おすすめランキング10選・スティック型/キャニスター型比較）
  - Dyson V15/パナソニック/マキタ/シャープ/東芝/日立/Dyson Ball Animal 3/アイリスオーヤマ/エレクトロラックス/三菱電機 10製品掲載
- **内部リンク強化（8記事更新）**：
  - air-purifier → humidifier 追加
  - fan-circulator → humidifier 追加
  - electric-kettle → humidifier 追加
  - water-server → humidifier 追加
  - cordless-vacuum → vacuum-cleaner 追加
  - robot-vacuum-ranking → vacuum-cleaner + cordless-vacuum 追加
  - robot-vacuum-comparison → vacuum-cleaner + cordless-vacuum 追加
  - washing-machine → vacuum-cleaner 追加
- hugo.toml ホーム文言の記事数更新: 36記事→38記事
- docs/articles.md の記事一覧を36本→38本に更新・次記事候補を更新

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
