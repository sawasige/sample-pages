# Sample Pages

[just-the-docs](https://just-the-docs.github.io/just-the-docs/) テーマを使用した GitHub Pages のサンプルサイトです。

## 🚀 デプロイ済みサイト

- **本番環境**: [https://sawasige.github.io/sample-pages](https://sawasige.github.io/sample-pages)
- **プレビュー**: プルリクエストごとに GitHub Pages で自動生成

## 📁 構成

```
sample-pages/
├── docs/                    # Jekyll サイトのソース
│   ├── _config.yml         # Jekyll 設定
│   ├── Gemfile            # Ruby 依存関係
│   ├── index.md           # ホームページ
│   ├── docs/              # ドキュメントページ
│   └── api/               # API リファレンス
├── .github/workflows/      # GitHub Actions
│   ├── deploy.yml         # 本番デプロイ
│   ├── pr-preview.yml     # プレビューデプロイ
│   └── cleanup-preview.yml # プレビュー削除
└── README.md
```

## 🔧 事前設定

### GitHub Pages の設定（必須）

1. リポジトリの **Settings** > **Pages** に移動
2. **Source** を「**GitHub Actions**」に設定
3. 設定を保存

### GitHub Pages 環境の設定（プレビュー用）

プルリクエストのプレビュー機能を使用するには：

1. リポジトリの **Settings** > **Environments** に移動
2. **New environment** で「**github-pages-preview**」を作成
3. 必要に応じて保護ルールを設定

## 🛠️ ローカル開発

```bash
# リポジトリをクローン
git clone https://github.com/sawasige/sample-pages.git
cd sample-pages

# 依存関係をインストール
cd docs
bundle install

# 開発サーバーを起動
bundle exec jekyll serve
```

サイトは `http://localhost:4000` で確認できます。

## 📝 ページの追加

新しいページを追加するには：

1. `docs/` フォルダに新しい `.md` ファイルを作成
2. YAML フロントマターを追加：

```markdown
---
layout: default
title: ページタイトル
nav_order: 順序
---

# ページタイトル

コンテンツをここに記述
```

## 🚀 デプロイ機能

### 本番デプロイ
- `main` ブランチの `docs/` フォルダに変更をプッシュすると自動デプロイ
- GitHub Pages の標準機能を使用

### プレビュー機能
- `docs/` フォルダに変更があるプルリクエストで自動プレビュー生成
- GitHub Pages の環境機能を使用してプレビューサイトを作成
- プルリクエストに自動でプレビューリンクをコメント
- プルリクエストがクローズされると自動でプレビューサイトを削除

## 🎨 カスタマイズ

テーマやスタイルのカスタマイズは `docs/_config.yml` で行います。

詳細は [just-the-docs のドキュメント](https://just-the-docs.github.io/just-the-docs/) を参照してください。