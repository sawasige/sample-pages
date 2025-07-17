---
layout: default
title: API リファレンス
nav_order: 3
has_children: true
description: "API の使い方について"
---

# API リファレンス

このセクションでは、API の使い方について説明します。

## 概要

Sample Pages では、以下の API を提供しています：

- REST API
- GraphQL API
- WebSocket API

## 認証

API を使用するには、認証が必要です。

```bash
curl -H "Authorization: Bearer YOUR_TOKEN" \
  https://api.example.com/v1/users
```

## レスポンス形式

すべての API レスポンスは JSON 形式で返されます：

```json
{
  "success": true,
  "data": {
    "id": 1,
    "name": "Sample User"
  },
  "message": "Success"
}
```

## エラーハンドリング

エラーが発生した場合：

```json
{
  "success": false,
  "error": {
    "code": "INVALID_REQUEST",
    "message": "Invalid request parameters"
  }
}
```

詳細については、各 API のドキュメントを参照してください。
