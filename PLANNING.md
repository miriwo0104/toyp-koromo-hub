# ころもサイト 企画・方向性メモ

## ハブページ（完成済み）

- URL：https://toyp-koromo.com
- ホスティング：GitHub Pages
- リポジトリ：github.com/miriwo0104/toyp-koromo-hub
- デザイン：ナチュラル系（design-c）を採用
- GA4測定ID：G-RHJBLSEVLV（ころも用Googleアカウント）
- SNSリンク：YouTube / TikTok / Instagram
- ボタンクリック計測・UTM対応済み

---

## アカウント管理

| サービス | アカウント |
|---|---|
| GitHub | エンジニア個人アカウント（miriwo0104） |
| Cloudflare | エンジニア個人アカウント |
| Google Analytics（GA4） | ころも用Googleアカウント |

---

## 次フェーズ：お出かけ情報サイト

### チャンネルコンセプト

> 「あなたの知りたいがここにある」
>
> わんこ同伴のお出かけ・お泊りは事前情報が不足しがち。
> ワクチン証明の要否・アメニティの実態・HPと現地の差など、
> 行ってみないとわからない情報を動画＋Webで発信する。

### やりたいこと

- 施設・スポットを地図上にピン表示
- 旅行工程をルートとして表示（1日目：A→B→C など）
- 施設ごとの紹介動画リンク
- 施設ごとの実態情報（ペット同伴条件・アメニティ・注意事項など）

### 参考サイト

- https://zundahouse-hotelmap.pages.dev/
  - YouTuberが紹介した宿泊施設を地図から検索できるサイト
  - Next.js SSG + 地図ライブラリ構成

### 規模感

- 旅行工程：約20件
- 更新者：エンジニア（自分）が直接ファイル編集でOK（管理画面不要）

### 技術スタック案

| 項目 | 採用候補 | 理由 |
|---|---|---|
| フレームワーク | Next.js（SSG） | 参考サイトと同構成・実績あり |
| 地図 | Leaflet.js | 完全無料・OpenStreetMap使用 |
| データ管理 | JSONファイル | 20件程度なら十分・シンプル |
| ホスティング | Cloudflare Pages | 無料・ドメイン管理と一元化できる |

### ランニングコスト

| 項目 | 費用 |
|---|---|
| ドメイン（toyp-koromo.com） | 年約1,600円 |
| Cloudflare Pages | 無料 |
| Leaflet.js | 無料 |
| **合計** | **年約1,600円のみ** |

### データ構造イメージ

```json
// trips.json（旅行工程）
{
  "id": "trip-001",
  "title": "箱根わんこ旅",
  "date": "2026-03-01",
  "spots": ["spot-001", "spot-002"],
  "youtube_url": "https://..."
}

// spots.json（施設情報）
{
  "id": "spot-001",
  "name": "〇〇ホテル",
  "lat": 35.xxx,
  "lng": 139.xxx,
  "pet_conditions": "小型犬のみ・ワクチン証明必要",
  "amenity_notes": "HPより実態は狭め",
  "photos": ["./images/spot-001-1.jpg"],
  "youtube_url": "https://..."
}
```

### 画面構成イメージ

1. **地図画面**：全スポットにピン表示 → クリックで施設詳細ポップアップ
2. **旅行一覧画面**：工程ごとにルート表示 → 動画リンク付き

### 今後の検討事項

- ハブページをGitHub PagesからCloudflare Pagesに移行するか
- フィルタリング機能の有無（エリア・ペット可否など）
- 施設ページと旅行工程ページの関係性（1施設が複数旅行に登場するケースの扱い）
