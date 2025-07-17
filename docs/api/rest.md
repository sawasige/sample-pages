---
layout: default
title: REST API
parent: API リファレンス
nav_order: 1
---

# REST API

REST API の使用方法について説明します。

## ベース URL

```
https://api.example.com/v1
```

## エンドポイント

### ユーザー管理

#### GET /users

すべてのユーザーを取得します。

**リクエスト:**
```bash
curl -X GET https://api.example.com/v1/users \
  -H "Authorization: Bearer YOUR_TOKEN"
```

**レスポンス:**
```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com"
    }
  ]
}
```

#### POST /users

新しいユーザーを作成します。

**リクエストボディ:**
```json
{
  "name": "New User",
  "email": "newuser@example.com"
}
```

**レスポンス:**
```json
{
  "success": true,
  "data": {
    "id": 3,
    "name": "New User",
    "email": "newuser@example.com",
    "created_at": "2025-01-01T00:00:00Z"
  }
}
```

## エラーコード

| コード | 説明 |
|--------|------|
| 400 | Bad Request - リクエストが不正 |
| 401 | Unauthorized - 認証が必要 |
| 403 | Forbidden - アクセス権限がない |
| 404 | Not Found - リソースが見つからない |
| 500 | Internal Server Error - サーバーエラー |
