# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-26 セッション8）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **39本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定 |
| 最終デプロイ | 2026-05-26（電気圧力鍋ランキング記事追加） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全39本が収益化開始 |
| 🟡 中 | Google Analytics 設定 | 流入状況を把握してSEO改善に活かす |
| 🟡 中 | プロジェクターおすすめランキング記事追加 | ホームシアター需要・高単価アフィリエイト |
| 🟡 中 | ヘアアイロンおすすめランキング記事追加 | 女性ユーザー獲得・Dyson等高単価商品 |
| 🟡 中 | 炊飯器おすすめランキング記事追加 | electric-pressure-cooker記事から内部リンク先として需要あり |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-26 セッション8）

- **新記事追加**：electric-pressure-cooker-ranking.md（電気圧力鍋おすすめランキング10選）
  - シロカ SP-4D151/ティファール クックフォーミー6L/パナソニック SR-MP300/アイリスオーヤマ LT-NA40/タイガー COK-A220/シャープ ホットクック KN-HW24G/クイジナート CPC-600J/ドウシシャ マルチポット/アンドマット SR-PD101/ブラウン MultiQuick 10製品掲載
  - 選び方4ポイント（容量・調理モード・操作性・手入れのしやすさ）
  - 用途別まとめ表・よくある質問3問・内部リンク4本（electric-kettle/coffee-maker/refrigerator/washing-machine）
- docs/articles.md の記事一覧を38本→39本に更新

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
