# トイプーころものおでかけ日記 — ハブページ

GitHub Pages でホスティングするリンクハブページです。

## ファイル構成

```
hub-site/
├── design-a.html   ふんわり可愛い系（パステル・丸みUI）
├── design-b.html   シンプルモダン系（ホワイト基調・すっきり）
├── design-c.html   ナチュラル系（アースカラー・旅行・自然）
├── CNAME           GitHub Pages 独自ドメイン設定ファイル
└── README.md       本ファイル
```

採用するデザインのファイルを **`index.html`** にリネーム（またはコピー）してから GitHub Pages に公開してください。

---

## 差し替え箇所一覧

各 HTML ファイルに共通のプレースホルダーが埋め込まれています。テキストエディタで一括置換してください。

### 画像

| プレースホルダー | 内容 |
|---|---|
| `PLACEHOLDER_IMAGE_URL` | ころもの顔・アイキャッチ画像の URL またはパス（例: `./images/koromo.jpg`）|

### YouTube

| プレースホルダー | 内容 |
|---|---|
| `PLACEHOLDER_YOUTUBE_URL` | チャンネル URL（例: `https://www.youtube.com/@xxxx`）|
| `PLACEHOLDER_YOUTUBE_HANDLE` | チャンネルハンドル（例: `@xxxx`）|

### TikTok

| プレースホルダー | 内容 |
|---|---|
| `PLACEHOLDER_TIKTOK_URL` | プロフィール URL（例: `https://www.tiktok.com/@xxxx`）|
| `PLACEHOLDER_TIKTOK_HANDLE` | ハンドル名（例: `@xxxx`）|

### Instagram

| プレースホルダー | 内容 |
|---|---|
| `PLACEHOLDER_INSTAGRAM_URL` | プロフィール URL（例: `https://www.instagram.com/xxxx`）|
| `PLACEHOLDER_INSTAGRAM_HANDLE` | ユーザー名（例: `@xxxx`）|

---

## CNAME（独自ドメイン）

`CNAME` ファイル内の `PLACEHOLDER_YOUR_DOMAIN.com` を取得済みのドメイン名に書き換えてください。

```
your-domain.com
```

独自ドメインを使わない場合は CNAME ファイルを削除してください。

---

## GitHub Pages への公開手順

1. このディレクトリを GitHub リポジトリにプッシュする
2. リポジトリの **Settings → Pages** を開く
3. Source を `Deploy from a branch`、Branch を `main`（または `master`）の `/ (root)` に設定する
4. 独自ドメインを使う場合は Custom domain 欄にドメイン名を入力し、DNS の CNAME レコードを `<username>.github.io` に向ける
