# OrangeByte Site 編集ガイド

このファイルは、**今後ほかの人やAIが読んでも一貫した編集ができる**ように作った運用ガイドです。

## 1. サイトの目的

- 個人開発したアプリの紹介
- 各アプリの使い方（ガイド）の提供
- 開発状況を発信するブログ運用
- 最小限のプロフィール（About）

## 2. 情報構造（サイトマップ）

- `/` トップ
- `/apps/` Apps一覧
- `/apps/<app-slug>/` 各アプリ詳細
- `/apps/<app-slug>/docs/<feature-slug>/` 各機能の使い方ページ
- `/blog/` Blog一覧
- `/blog/devlog/` 開発ログ一覧
- `/blog/tech/` 技術記事一覧
- `/blog/<category-slug>/<post-slug>/` 各記事
- `/about/` About

## 3. URLルール（重要）

- URLは**英小文字スラッグ**を使う  
  スラッグ = URL用の短い名前（例: `prompt-generator`）
- 空白や日本語はURLに直接使わない  
  理由: 文字化けのような表示（URLエンコード）を避けるため
- 末尾スラッシュ付きで統一  
  例: `/apps/prompt-generator/docs/feature-a/`

### 例

- 表示名: `Prompt Generator`  
  URL: `/apps/prompt-generator/`
- 表示名: `機能A`  
  URL: `/apps/prompt-generator/docs/feature-a/`

## 4. デザイン方針

- 全体トーン: **シンプル・見やすい**
- ベース色: 白系
- アクセント色: オレンジ（`--accent: #f47c20`）
- 文字サイズ: やや小さめ（1画面で見える情報量を優先）
- 共通スタイル: `/style.css` を必ず利用

## 5. 共通レイアウトルール

- ヘッダーは全ページ共通
  - ロゴ: `OrangeByte`
  - ナビ: `Apps / Blog / About`
- セクションは `section-block` で区切る
- カードは `card` クラスを使う
- フッターは全ページで同じ文言を使う

## 6. コンテンツ運用ルール

- アプリページ:
  - まずアプリ概要を書く
  - 次にDocsページへのリンクを置く
- Docsページ:
  - 機能単位で分ける
  - 手順は短く、順番がわかるように書く
- ブログページ:
  - `devlog`（開発ログ）と `tech`（技術記事）を分ける
  - 日付と要点を明記する
- About:
  - 長文にしない
  - 方針と活動内容を簡潔に書く

## 7. ページ追加時の手順

1. ディレクトリを作る（例: `apps/new-app/`）
2. `index.html` を作る
3. 共通ヘッダー・フッター・`/style.css` リンクを入れる
4. 親ページからリンクを追加する
5. URLスラッグがルールに合っているか確認する

## 8. 編集チェックリスト

- リンク切れがない
- ナビが `Apps / Blog / About` で統一されている
- URLに空白・日本語を使っていない
- 色・余白・カードのトーンが他ページと一致している
- スマホ表示でもレイアウトが崩れない

## 9. 現在の主要URL

- `/`
- `/apps/`
- `/apps/prompt-generator/`
- `/apps/prompt-generator/docs/feature-a/`
- `/apps/prompt-generator/docs/feature-b/`
- `/apps/prompt-archive/`
- `/apps/prompt-archive/docs/search/`
- `/apps/coffee-timer/`
- `/apps/coffee-timer/docs/brew-mode/`
- `/blog/`
- `/blog/devlog/`
- `/blog/tech/`
- `/about/`
