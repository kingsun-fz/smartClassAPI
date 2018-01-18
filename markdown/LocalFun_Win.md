
## 智慧教室接口说明

[TOC]

### 状态码统一说明999999
- 0 成功

- 1XX 用户类型错误
    - 100 用户错误
    - 101 用户选择错误

- 2XX 网络类型错误
    - 200 网络错误

- 3XX 系统类型错误
    - 300 系统错误

- 4XX 其他类型错误
    - 400 未知错误


### 1. 获取教材数据

- Method API
>  **GET [api/book/list](#)**

- 请求参数

| 请求参数      |     参数类型    |   参数说明   |
| ----------- | ---------------|----------- |
| BookType    | String,可为空   |  教材类型    |
| Subject     | String,可为空   |  科目ID     |
| Edition     | String,可为空   |  版本ID     |
| UserID      | String,可为空   |  用户ID     |

- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   Boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 0,
  "message": "",
  "data":[
    {
        "ID":"1",
        "Subject":"语文",
        "EdiList":[
            {
                "ID":"27",
                "Edition":"人教版",
                "BookList":[
                    {
                        "ID":"207",
                        "Book":"人教版小学语文一年级下册"
                    }
                ]
            }
        ]
    }
  ]
}
```
