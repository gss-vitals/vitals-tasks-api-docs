#### 目錄

- [getProducts](#1-getProducts)
- [Authentication](#2-authentication)
  - [Browser-based authentication](#21-browser-based-authentication)
  - [Self-issued access tokens](#22-self-issued-access-tokens)
- [Resources](#3-resources)
  - [Users](#31-users)
  - [Publications](#32-publications)
  - [Posts](#33-posts)
  - [Images](#34-images)
- [Testing](#4-testing)

##

## 使用說明

透過以下 API 呼叫，您可以對應操作：

### 名稱
getProducts

### 描述
取得產品列表

### 調用
GET /products

### 請求參數
無

### 返回資料
| 名稱        | 類型    | 描述   |
| ------------ | ------- | ------ |
| id           | integer | 產品ID |
| name         | string  | 產品名稱 |
| price        | integer | 產品價格 |
| description  | string  | 產品描述 |
| image_url    | string  | 產品圖片 |

### 範例
```
GET /products
```
```
[
  {
    "id": 1,
    "name": "Apple iPhone 11 Pro",
    "price": 54800,
    "description": "The latest generation of Apple's flagship iPhone.",
    "image_url": "https://example.com/iphone11.jpg"
  },
  {
    "id": 2,
    "name": "Samsung Galaxy S10 Plus",
    "price": 49800,
    "description": "Samsung's latest premium smartphone.",
    "image_url": "https://example.com/s10.jpg"
  }
]
```
