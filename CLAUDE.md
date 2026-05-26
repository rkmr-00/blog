# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-27 セッション9）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **51本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ✅ 設定済み（測定ID: G-BP0F280FVR・hugo.toml [services.googleAnalytics] に設定済み） |
| 最終デプロイ | 2026-05-27（新記事8本追加・内部リンク強化・記事数51本へ） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全51本が収益化開始 |
| 🟡 中 | スマートホーム入門ガイド記事追加 | スマートプラグ・スマートロック・スマートスピーカーの横断ガイド |
| 🟡 中 | コードレス掃除機vs有線掃除機 比較記事 | 検索需要が高い比較系コンテンツ |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-27 セッション9）

- **新記事追加①**：microwave-ranking.md（電子レンジ・オーブンレンジおすすめランキング10選）
  - パナソニック/日立/東芝/シャープ/アイリスオーヤマ/山善 10製品掲載
  - スチームオーブンレンジ・オーブンレンジ・単機能レンジの3タイプ比較
- **新記事追加②**：portable-power-station-ranking.md（ポータブル電源おすすめランキング10選）
  - EcoFlow/Jackery/Anker/BLUETTI 10製品掲載（防災・アウトドア・車中泊需要）
- **新記事追加③**：air-purifier-humidifier-ranking.md（空気清浄機加湿器一体型おすすめランキング10選）
  - ダイキン/シャープ/パナソニック/日立/アイリスオーヤマ 10製品掲載
  - ストリーマ・プラズマクラスター・ナノイーXの独自技術比較
- **新記事追加④**：gaming-keyboard-ranking.md（ゲーミングキーボードおすすめランキング10選）
  - Logicool/CORSAIR/Razer/SteelSeries/HHKB 10製品掲載（メカニカル・静音・テンキーレス）
- **新記事追加⑤**：smart-home-guide.md（スマートホーム入門ガイド・初心者向けデバイス5選）
  - SwitchBot/Amazon Echo/Philips Hue/TP-Link 5製品掲載
  - Google Home/Alexa/Apple HomeKitのプラットフォーム比較表
- **新記事追加⑥**：cordless-vs-corded-vacuum-comparison.md（コードレスvs有線掃除機 比較）
  - Dyson/パナソニック/マキタ/三菱/東芝/日立 6製品掲載・8項目比較表
- **新記事追加⑦**：dishwasher-ranking.md（食器洗い乾燥機おすすめランキング10選）
  - パナソニック/アイリスオーヤマ/Siemens/AEG/ハイアール/THANKO 10製品掲載
  - タンク式vs分岐水栓式・乾燥方式の比較
- **新記事追加⑧**：laptop-ranking.md（ノートパソコンおすすめランキング10選）
  - MacBook/Surface/ThinkPad/DELL XPS/HP/ASUS/Lenovo/Acer 10製品掲載（高単価・高affiliate単価）
- **内部リンク強化（16記事更新）**：
  - refrigerator/washing-machine → microwave-ranking 追加
  - electric-bicycle/fan-circulator → portable-power-station-ranking 追加
  - air-purifier/humidifier → air-purifier-humidifier-ranking 追加
  - gaming-mouse/keyboard → gaming-keyboard-ranking 追加
  - smart-plug/smart-lock → smart-home-guide 追加
  - cordless-vacuum/vacuum-cleaner → cordless-vs-corded-vacuum-comparison 追加
  - rice-cooker → dishwasher-ranking 追加
  - monitor/laptop-stand/tablet → laptop-ranking 追加
- hugo.toml ホーム文言の記事数更新: 43記事→51記事
- docs/articles.md の記事一覧更新（43本→51本）

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
