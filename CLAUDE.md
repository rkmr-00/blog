# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-27 セッション9）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **45本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ✅ 設定済み（測定ID: G-BP0F280FVR・hugo.toml [services.googleAnalytics] に設定済み） |
| 最終デプロイ | 2026-05-27（新記事2本追加・内部リンク強化・記事数45本へ） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全45本が収益化開始 |
| 🟡 中 | 空気清浄機加湿器一体型ランキング記事追加 | ダイキン・シャープ・パナソニック比較 |
| 🟡 中 | ゲーミングキーボードランキング記事追加 | 既存のゲーミングカテゴリ強化 |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-27 セッション9）

- **新記事追加①**：microwave-ranking.md（電子レンジ・オーブンレンジおすすめランキング10選）
  - パナソニック/日立/東芝/シャープ/アイリスオーヤマ/山善 10製品掲載
  - スチームオーブンレンジ・オーブンレンジ・単機能レンジの3タイプ比較
  - 内部リンク4本：rice-cooker-ranking / electric-pressure-cooker-ranking / electric-kettle-ranking / refrigerator-ranking
- **新記事追加②**：portable-power-station-ranking.md（ポータブル電源おすすめランキング10選）
  - EcoFlow/Jackery/Anker/BLUETTI 10製品掲載（防災・アウトドア・車中泊需要）
  - 容量・出力・充電速度・重さで比較・用途別選び方を詳解
  - 内部リンク4本：electric-bicycle-ranking / smart-plug-ranking / cordless-vacuum-ranking / fan-circulator-ranking
- **内部リンク強化（既存記事へ追加）**：
  - refrigerator-ranking → microwave-ranking 追加
  - washing-machine-ranking → microwave-ranking 追加
  - electric-bicycle-ranking → portable-power-station-ranking 追加
  - fan-circulator-ranking → portable-power-station-ranking 追加
- **Google Analytics 設定確認**：G-BP0F280FVR が hugo.toml に反映済み（前セッションで設定完了）
- hugo.toml ホーム文言の記事数更新: 43記事→45記事
- docs/articles.md の記事一覧更新（43本→45本）

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
