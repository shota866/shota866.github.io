# Shota's Life Log

GitHub Pages で公開する、Astro 製の個人ホームページです。研究者サイトに寄せすぎず、趣味、旅行、日常、ブログ、写真の記録を中心にした明るいライフログとして作っています。

## ローカルで起動する方法

```bash
npm install
npm run dev
```

ブラウザで `http://localhost:4321` を開くと確認できます。

## ビルド方法

```bash
npm run build
```

ビルド結果は `dist/` に出力されます。

## GitHub Pages で公開する方法

1. GitHub リポジトリ `shota866.github.io` の `main` ブランチに push します。
2. `.github/workflows/deploy.yml` により GitHub Actions が自動でビルドとデプロイを実行します。
3. `astro.config.mjs` の `site` は `https://shota866.github.io` に設定済みです。

## ブログ記事の追加方法

1. `src/pages/blog/` に `.md` ファイルを追加します。
2. 先頭の frontmatter に `title` `description` `pubDate` `category` `tags` を書きます。
3. 本文を Markdown で書くと、`/blog` に自動で一覧表示されます。

既存のサンプル記事:

- `src/pages/blog/start-homepage.md`
- `src/pages/blog/dicomo2026.md`
- `src/pages/blog/fuji-climbing.md`
- `src/pages/blog/recent-favorites.md`

## 画像の追加方法

1. `public/assets/gallery/` に画像ファイルを追加します。
2. `src/pages/gallery.astro` の各アイテムに `image: "/assets/gallery/ファイル名.jpg"` を指定します。
3. 必要ならタイトルやキャプションも同じファイルで編集します。

## 各ページの編集場所

- Home: `src/pages/index.astro`
- Blog 一覧: `src/pages/blog.astro`
- Gallery: `src/pages/gallery.astro`

## 共通パーツ

- ヘッダー: `src/components/Header.astro`
- フッター: `src/components/Footer.astro`
- ブログカード: `src/components/BlogCard.astro`
- ギャラリーカード: `src/components/GalleryCard.astro`
- セクション見出し: `src/components/SectionTitle.astro`
- 共通レイアウト: `src/layouts/Layout.astro`
- 記事レイアウト: `src/layouts/BlogPostLayout.astro`
- 全体スタイル: `src/styles/global.css`
