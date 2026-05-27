# GadgetReviewLab — Claude向け運営ガイド

> **Claudeへ：** セッション開始時にまずここを読む。終了前に必ずここを更新してコミット。
> 詳細ルールは [docs/content-guide.md](docs/content-guide.md)、記事一覧は [docs/articles.md](docs/articles.md) を参照。

---

## セッション引き継ぎ（最終更新: 2026-05-28 セッション12）

### 現在の状態スナップショット

| 項目 | 状態 |
|------|------|
| 記事数 | **53本**（posts/配下） |
| Google Search Console | ✅ 登録済み・HTMLタグ確認・サイトマップ送信済み |
| Amazon Associates | ⏳ 審査中（2026-05-23 申請） |
| 楽天アフィリエイト | ✅ 登録済み・ウィジェット設置済み（ID: `543b8391.aa707548.543b8392.c9ec69a5`） |
| X (Twitter) | ⏳ 未開設（セットアップガイド作成済み: docs/x-setup.md） |
| 独自ドメイン | ❌ 未取得（Associates通過後に検討） |
| Google Analytics | ✅ 設定済み（測定ID: G-BP0F280FVR・hugo.toml [services.googleAnalytics] に設定済み） |
| 最終デプロイ | 2026-05-28（全記事テンプレート統一・クイックピックス＋ランクショートコード全適用） |

### 次のアクション（優先度順）

| 優先度 | アクション | 理由 |
|--------|-----------|------|
| 🔴 高 | Amazon Associates 審査結果確認 | 通過すれば全53本が収益化開始 |
| 🔴 高 | X (Twitter) アカウント開設 | docs/x-setup.md にプロフィール・投稿テンプレート準備済み |
| 🟡 中 | 全記事に楽天リンクを追加 | 主要記事以外に楽天カード未追加のものが多い |
| 🟡 中 | `washing-machine-ranking.md` のランクショートコード対応 | 構造が特殊（ドラム式・縦型に分割）でスキップ中 |
| 🟢 低 | 独自ドメイン取得 | Associates通過後に検討 |
| 🟢 低 | GSCでCTR低い記事のタイトル改善 | GSCデータ蓄積後（1〜2ヶ月後） |

### 直近セッションで実施したこと（2026-05-28 セッション12）

- **全ランキング記事テンプレート統一（計15記事）**：
  - セッション11で上位5記事完了済み→残り15記事を今セッションで実施
  - 対象：`hair-iron`・`microwave`・`air-purifier-humidifier`・`gaming-keyboard`・`portable-power-station`・`dehumidifier`・`humidifier`・`electric-pressure-cooker`・`vacuum-cleaner`・`dishwasher`・`hot-plate`・`smartphone`・`water-server`・`fan-circulator`・`washing-machine`
  - **クイックピックスボックス**（rawhtml quick-picks div）を全記事冒頭に追加
  - **ランクショートコード**（`{{% rank rank="1|2|3" %}}...{{% /rank %}}`）を1〜3位に追加
  - `washing-machine-ranking.md` はドラム式・縦型に分割された特殊構造のためランクショートコードをスキップ（クイックピックスのみ追加）
  - 絵文字メダル（🥇🥈🥉）・`第N位：` prefix を各記事の形式に合わせて追加
  - **Amazonカードが上部にある形式**（microwave・air-purifier-humidifier・portable-power-station・dishwasher・hot-plate・smartphone・water-server・fan-circulator）の `{{% /rank %}}` はスペックテーブル末尾に配置

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
