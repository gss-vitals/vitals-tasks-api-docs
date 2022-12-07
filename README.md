#### 目錄

- [基本欄位](#基本欄位) 
- [即將截止與已逾期的任務](#1-即將截止與已逾期的任務) 
- [我指派的任務](#2-我指派的任務) 
- [指派給我的任務](#3-指派給我的任務) 
- [任務狀態統計](#4-任務狀態統計)

##

### 基本欄位
所有 API 呼叫時皆需傳入下方三個參數，並且固定回傳下方格式

### 請求參數 
| 名稱         | 是否必填 | 類型    | 描述   | 
| ------------ | ------- | ------- | --------------------------------- |
| ApiKey      | 是 | string | 填入申請的 ApiKey |
| TenantId    | 是 | string  | 填入 TenantId |
| LoginId        | 是 | string | 填入 LoginId |

### 返回資料
| 名稱        | 類型    | 描述   |
| ------------ | ------- | ------ |
| ResultStatus           | boolean | 是否成功呼叫 |
| ExceptionType         | string  | 錯誤訊息類別 |
| ResultMessage        | string | 錯誤訊息原因 |
| Body  | jsonObject  | 詳細資料 |

##

### 1. 即將截止與已逾期的任務
取得即將截止與已逾期的任務

### 呼叫方式
POST /api/task/expired

### 請求參數 Body
| 名稱        | 是否必填| 類型    | 描述   |
| ------------ | ------- | ------- | ------------------------------------------------------ |
| Status       | 是 | integer | 狀態 0:未完成 1:已完成 |
| ParticipantType | 是 | array  | 1:負責人 2:指派者 3:協同指派者 4:協同負責人 5:閱覽者 |
| ExpiredDateStart | 是   | string | 截止起日 格式為:2022-12-31T23:59 |
| ExpiredDateEnd | 是   | string | 截止迄日 格式為:2022-12-31T23:59 |
| CurrentPage | 是  | integer | 目前頁數 |
| PageCount | 是  | integer | 每頁筆數 |

### 返回資料 Body
| 名稱        | 類型    | 描述   |
| ------------ | ------- | ------ |
| TotalCount           | integer | 總筆數 |
| XXX         | XXX  | XXXX |

### 範例
```
POST /api/task/expired?ApiKey=8578cd8ca7274af0ac48cd13aa6f531c&TenantId=default&LoginId=willy_chang
```
```
{
    "Status":1,
    "ParticipantType": [1, 2],
    "ExpiredDateStart": "2019-02-02T00:00",
    "ExpiredDateEnd": "2052-03-13T00:00",
    "CurrentPage": 1,
    "PageCount":10
}
```

##

### 2. 我指派的任務
取得我指派的任務

##

### 3. 指派給我的任務
取得指派給我的任務

##

### 4. 任務狀態統計
取得任務狀態統計
