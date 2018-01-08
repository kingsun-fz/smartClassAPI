## 智慧教室接口说明

[TOC]

### 1. 获取教材数据

- Method API
>  **GET [api/book/list](#)**

- 请求参数

| 请求参数      |     参数类型 |   参数说明   |
| ----------- | ------------|----------- |
| BookType    | Int,可为空   |  教材类型    |
| Subject     | Int,可为空   |  科目ID     |
| Edition     | Int,可为空   |  版本ID     |
| UserID      | string,可为空|  用户ID     |

- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 0,
  "message": "操作正确",
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

### 2. 获取教材目录列表

- Method API
> GET **[api/book/cata/{id}](#)**

- 请求参数

| 请求参数      |     参数类型    |   参数说明  |
| ----------- |  ------------ |----------- |
| bookID      | Integer,不可为空 |  教材ID    |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":[
             {
                 "ID":"1",
                 "CodeName":"M1",
                 "Child":[
                     {
                         "ID":"2",
                         "CodeName":"U1"
                     }
                 ]
             }
    ]
}
```
### 3. 获取电子教材配置文件
- Method API
> GET **[api/book/deploy/{id}](#)**

- 请求参数

| 请求参数      |     参数类型    |   参数说明  |
| ----------- |  ------------ |----------- |
| bookID      | Integer,不可为空 |  教材ID    |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":{
        "id":"",
        "url":"http://xxx/TextBookHandler.ashx?OP=getDBjs&BookID=xxx"
  }
}
```
### 4. 获取用户备课数据
- Method API
> GET **[api/prelesson](#)**

- 请求参数

| 请求参数      |     参数类型    |   参数说明   |
| ----------- | ------------   |----------- |
| UserID      | string,不可为空  |  用户ID    |
| UserType    | Integer,不可为空 |  用户类型   |
| BookID      | Integer,不可为空 |  教材ID    |
| Pages       | Json,不可为空    |  页码数组   |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":[
        {
            "page":"1",
            "conent":"xxxxxx"
        }
  ]
}
```

### 5. 获取用户教学地图数据
- Method API
> GET **[api/map](#)**

- 请求参数

| 请求参数      |     参数类型    |   参数说明   |
| ----------- | ------------   |----------- |
| UserID      | string,不可为空  |  用户ID     |
| UserType    | Integer,不可为空 |  用户类型    |
| BookID      | Integer,不可为空 |  教材ID     |
| Cata        | Integer,不可为空 |  目录ID     |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":{
      "cata":"1",
      "conent":"xxxxxx"
  }
}
```
### 6. 保存备课数据
- Method API
> POST **[api/prelesson](#)**

- 请求参数

| 请求参数      |     参数类型     |   参数说明                     |
| ----------- | ------------    |-----------                    |
| UserID      | string,不可为空  |  用户ID                        |
| UserType    | Integer,不可为空 |  用户类型                       |
| BookID      | Integer,不可为空 |  教材ID                        |
| Content     | String,不可为空  |  Page和备课数据的二维数组Json     |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```
### 7. 保存教学地图数据
- Method API
> POST **[api/map](#)**

- 请求参数

| 请求参数      |     参数类型 |   参数说明   |
| ----------- | ------------|-----------  |
| UserID      | string,不可为空  |  用户ID                        |
| UserType    | Integer,不可为空 |  用户类型                       |
| BookID      | Integer,不可为空 |  教材ID                        |
| Content     | String,不可为空  |  Cata和教学地图数据的二维数组Json  |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确"
}
```
### 8. 获取资源列表
- Method API
> GET **[api/resource](#)**

- 请求参数

| 请求参数        |     参数类型 |   参数说明    |
| -----------   | ------------|-----------  |
| CataParentID  | Integer        |  一级目录ID,配合CataChildID使用时,不能为空  |
| CataChildID   | Integer        |  子级目录ID,配合CataParentID使用          |
| SubjectID     | Integer        |  科目ID,配合KeyWord使用时不能为空          |
| KeyWord       | String         |  关键字,配合SubjectID使用时不能为空         |
| PageIndex     | Integer,不可为空 |  当前页                                 |
| PageSize      | Integer,不可为空 |  当前页显示数量                          |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":{
      "TypeList":[
             {"ID":1,"CodeName":"类型1"},
             {"ID":1,"CodeName":"类型2"},
             {"ID":1,"CodeName":"类型3"}
      ],
      "ResourceList":[
             {"ID":1,"Title":"资源1"},
             {"ID":1,"Title":"资源2"},
             {"ID":1,"Title":"资源3"}
      ],
      "Total":300
  }
}
```
### 9. 获取资源信息
- Method API
> GET **[api/resource/{id}](#)**

- 请求参数

| 请求参数      |     参数类型 |   参数说明   |
| ----------- | ------------|-----------  |
| rid         | Long,不可为空 |  资源UID   |

- 返回参数

| 返回参数      |     参数类型 |   参数说明   |
| ----------- | ------------| ----------- |
| success     |   boolean   |  请求成功与否  |
| code        |   Integer   |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例

```js
{
  "success": true,
  "code": 200,
  "message": "操作正确",
  "data":{
    "ID":"xxxxxxxx",
    "Title":"xxxx",
    "FileID":"xxxxxxx",
    "Type":"xx"
  }
}
```
