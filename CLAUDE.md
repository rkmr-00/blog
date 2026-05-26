# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-26 セッション8）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **43本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ❌ 未設定（hugo.tomlにコメントアウト済み・測定ID取得後に有効化） |
| 最終デプロイ | 2026-05-26（新記事5本追加・内部リンク多数強化） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全43本が収益化開始 |
| 🔴 高 | Google Analytics 設定（GA4測定IDを取得してhugo.tomlのコメント解除） | 流入状況を把握してSEO改善に活かす。hugo.tomlに設定箇所は準備済み |
| 🟡 中 | 電子レンジ・オーブンレンジランキング記事追加 | 調理家電クラスターのさらなる強化 |
| 🟡 中 | ポータブル電源ランキング記事追加 | 防災需要・アウトドア需要・高単価 |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-26 セッション8）

- **PV増加戦略を立案**（strategy-aiによる調査）：除湿機・電気圧力鍋・ヘアアイロンを優先記事として特定
- **新記事追加①**：dehumidifier-ranking.md（除湿機おすすめランキング10選・梅雨シーズン需要狙い）
  - パナソニック/シャープ/コロナ/アイリスオーヤマ/ダイキン/三菱電機/東芝/シャープCV-S71/コイズミ/アイリスIJCP 10製品掲載
- **新記事追加②**：electric-pressure-cooker-ranking.md（電気圧力鍋おすすめランキング10選）
  - シロカ/ティファール/パナソニック/アイリスオーヤマ/タイガー/シャープホットクック/クイジナート/ドウシシャ/アンドマット/ブラウン 10製品掲載
- **新記事追加③**：hair-iron-ranking.md（ヘアアイロンおすすめランキング10選・女性ユーザー向け）
  - KINUJO/Dyson Corrale/パナソニック/リファ/クレイツ/ヴィダルサスーン/コイズミ/ラヴィス/テスコム/BaByliss 10製品掲載
- **内部リンク強化（5記事更新）**：
  - dryer-ranking → hair-iron-ranking 追加
  - air-purifier-ranking → dehumidifier-ranking 追加
  - humidifier-ranking → dehumidifier-ranking 追加
  - electric-kettle-ranking → electric-pressure-cooker-ranking 追加
  - coffee-maker-ranking → electric-pressure-cooker-ranking 追加
- **新記事追加④**：projector-ranking.md（プロジェクターおすすめランキング10選・ホームシアター/ポータブル/4K比較）
  - BenQ/Anker Nebula/エプソン/XGIMI/ソニー/Dangbei/ViewSonic 10製品掲載
- **新記事追加⑤**：rice-cooker-ranking.md（炊飯器おすすめランキング10選・圧力IH/IH/マイコン比較）
  - パナソニック/タイガー/象印/日立/シャープ/アイリスオーヤマ/山善 10製品掲載
- **内部リンク強化（4記事追加更新）**：
  - 4k-tv-ranking → projector-ranking 追加
  - home-theater-speaker-ranking → projector-ranking 追加
  - electric-pressure-cooker-ranking → rice-cooker-ranking 追加
  - refrigerator-ranking → rice-cooker-ranking 追加
- hugo.toml ホーム文言の記事数更新: 41記事→43記事
- docs/articles.md の記事一覧更新

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
