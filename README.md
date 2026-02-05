# Fluxia コーポレートサイト（静的）

## 概要
- 純HTML/CSS/JSで構成した1ページ完結の静的サイトです。
- GitHub Pagesでの公開を前提に、ビルド不要でそのまま動作します。
- 将来のCloudflare Pages移行を想定し、一般的な静的サイト構成で整理しています。

## ファイル構成
```
./
├── index.html
├── assets/
│   ├── css/styles.css
│   ├── js/main.js
│   └── img/
├── robots.txt
└── sitemap.xml
```

## GitHub Pages 公開手順
1. このリポジトリをGitHubへpushします。
2. GitHubの「Settings」→「Pages」へ移動します。
3. 「Build and deployment」>「Source」で `Deploy from a branch` を選択します。
4. Branchは `main`、フォルダは `/ (root)` を選択して保存します。
5. 数分後に公開URLへアクセスします。

## Cloudflare Pages 移行メモ
- ビルド不要のため、Cloudflare Pagesの「Build command」は空欄でOKです。
- 「Output directory」は `/`（ルート）を指定します。
- `sitemap.xml` と `robots.txt` のURLを新ドメインに差し替えてください。

## サイト編集ポイント
- `index.html`
  - ヒーロー/各セクションの文言や順番を編集します。
  - お問い合わせフォームURLは `https://example.com` を実URLに差し替えます。
- `assets/css/styles.css`
  - `:root` のCSS変数で色や余白を調整できます。
- `assets/js/main.js`
  - ナビゲーションの開閉と、現在セクションの強調表示を管理します。

## プレースホルダの差し替え
- OG画像: `assets/img/og-placeholder.svg`
- favicon: `assets/img/favicon.svg`
- ロゴ: `assets/img/fluxia-logo.svg`
- フォームURL: `https://example.com`
- サイトURL: `https://example.com`（`sitemap.xml`/`robots.txt`/`index.html`）
