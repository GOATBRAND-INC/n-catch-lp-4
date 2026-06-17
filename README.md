# N-Catch ランディングページ — 開発引き継ぎ

シングルページのLP（静的HTML）です。ビルド工程・フレームワークなし。
`index.html` をブラウザで開けばそのまま表示されます。

## ファイル構成

```
index.html              本体（HTML / CSS / JS すべて内包）
logo-ncatch.png         ロゴ（ヘッダー・ファーストビュー）
rice-field-bg-v2.png    ファーストビュー背景（稲穂）
mascot-fly.png          マスコット・上部（飛行ポーズ）
mascot-web.png          マスコット・下部（クロージング）
product-pouch-v3.png    製品パッケージ画像（背景透過）
```

## 技術メモ

- **CSS / JS は `index.html` 内に直接記述**（外部CSS/JSファイルなし）。
- **フォント**: Google Fonts を `<link>` で読み込み
  - Shippori Mincho B1（見出し・明朝）
  - Zen Kaku Gothic New（本文・ゴシック）
  - JetBrains Mono（英数ラベル）
- **動画**: YouTube 埋め込み（`youtube-nocookie.com`）。動画ID = `snNj7VubZ-c`
- **スクロール演出**: `IntersectionObserver` による reveal アニメーション（`index.html` 内のスクリプト）。
- **レスポンシブ**: モバイル対応済み（メディアクエリ `860px` / `600px` 等）。

## 外部リンク / 依存

- 公式ページ: https://phyto.jp/n-catch/
- 紹介動画: https://www.youtube.com/watch?v=snNj7VubZ-c
- Google Fonts（表示にネット接続が必要）

## 配置（デプロイ）

静的ホスティングにそのまま置けます（Netlify / Vercel / S3 / 通常のWebサーバー等）。
ルートに `index.html` と画像5点を同階層で配置してください。
