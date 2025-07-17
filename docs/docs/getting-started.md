---
layout: default
title: はじめに
parent: ドキュメント
nav_order: 1
---

# はじめに

Sample Pages へようこそ！このガイドでは、基本的な使い方について説明します。

## 前提条件

- Git の基本的な知識
- Markdown の基本的な知識
- GitHub アカウント

## インストール

1. このリポジトリをクローンします：
   ```bash
   git clone https://github.com/sawasige/sample-pages.git
   cd sample-pages
   ```

2. 必要な依存関係をインストールします：
   ```bash
   cd docs
   bundle install
   ```

3. ローカルで開発サーバーを起動します：
   ```bash
   bundle exec jekyll serve
   ```

## 基本的な使い方

### ページの作成

新しいページを作成するには、`docs/` フォルダに新しい Markdown ファイルを作成します。

```markdown
---
layout: default
title: ページタイトル
nav_order: 順序
---

# ページタイトル

ここにコンテンツを書きます。
```

### ナビゲーション

ナビゲーションの順序は YAML フロントマターの `nav_order` で制御できます。

### 子ページの作成

親ページの下に子ページを作成するには：

```markdown
---
layout: default
title: 子ページ
parent: 親ページ
nav_order: 1
---
```

これで基本的なセットアップは完了です！
