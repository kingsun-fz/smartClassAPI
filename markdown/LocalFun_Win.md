
## 智慧教室接口说明

[TOC]

### 状态码统一说明
- 0 成功

- -1失败


### 1. 获取页面水滴json

- Method： callHostFunction
>**selBookPageData_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| Func      | string,不可为空  |  方法名    |
| UserID      | string,不可为空  |  用户ID    |
| BookID      | string,不可为空  |  教材ID    |
| Pages       | string,不可为空    |  页码数组 （6,7）  |

- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   Boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例
离线、在线

```js
{
  "success": true,
  "code": 0,
  "message": "",
  "data":[{
             "pageNum": 6,
             "imgSrc": "images/06.jpg",
             "btns": [
                 {
                     "id": "p_76",
                     "icoType": "6",
                     "randId": "1505813969790",
                     "isread": true,
                     "sourceUrl": "c6837bb1-ea95-4546-94b6-cb72bdd6f694",
                     "X": 540.6465126811594,
                     "Y": 341.0474788647343,
                     "title": "雅鲁藏布大峡谷-动画",
                     "comeFrom": "ModResource"
                 }
             ]
         },{
             "pageNum": 7,
             "imgSrc": "images/07.jpg",
             "btns": [
                 {
                     "id": "p_76",
                     "icoType": "6",
                     "randId": "1505813969790",
                     "isread": true,
                     "sourceUrl": "c6837bb1-ea95-4546-94b6-cb72bdd6f694",
                     "X": 540.6465126811594,
                     "Y": 341.0474788647343,
                     "title": "雅鲁藏布大峡谷-动画",
                     "comeFrom": "ModResource"
                 }
             ]
         }]
}
```
### 2. 获取互动课件配置首页html

- Method： callHostFunction
>**wareEntry_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| Func      | string,不可为空  |  方法名    |
| UserID      | string,不可为空  |  用户ID    |
| BookID      | int,不可为空  |  教材ID    |
| PageID      | int,不可为空  |  页码    |
| FileID      | string,不可为空  |  文件ID    |


- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   Boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例
离线

```js
{
  "success": true,
  "code": 0,
  "message": "",
  "data":"F:\GitWork\offline_win\SmarterClassroomWindows\bin\x86\Debug\Page\data\RJYW4A\resource\第一单元\950baed5-b7de-48dc-b00b-1a14713f6628\ren_mang\ren_mang.html"
}

```
在线
```js
{
	"code": 0,
	"data": "http:\/\/183.47.42.218:8888\/2017\/09\/09\/45d99f96-1320-484a-b49f-c62702f6cd3f\/ren_hui\/ren_hui.html",
	"message": "",
	"success": true
}
```

### 3. 获取电子书dbjs

- Method： callHostFunction
>**getDbJsById_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| Func      | string,不可为空  |  方法名    |
| UserID      | string,不可为空  |  用户ID    |
| BookID      | int,不可为空  |  教材ID    |

- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   Boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例
离线
```js
{
  "success": true,
  "code": 0,
  "message": "",
  "data":{
             "book": "人教版小学语文四年级上册",
             "pageSource": [

                 {
                     "pageId": -1,
                     "pageImg": "ml002/bg.jpg"
                 },
                 {
                     "pageId": 0,
                     "pageImg": "ml003/bg.jpg"
                 },
                 {
                     "pageId": 1,
                     "pageImg": "page001/bg.jpg"
                 },
                 {
                     "pageId": 2,
                     "pageImg": "page002/bg.jpg",
                     "buttons": {
                         "button": [
                             {
                                 "eventtype": 5,
                                 "subjectNum": 1,
                                 "itemNum": 0,
                                 "height": 44,
                                 "id": 1,
                                 "soundsrc": "page002/sound/p002001.mp3",
                                 "width": 116,
                                 "x": 338.667,
                                 "y": 81.3333
                             }

                         ]
                     }
                 }
             ]
         }
}
```
在线

```js
{
	"code": 0,
	"data": "var DBJsonPath='Course\/TextBook\/RJYW4A';var dbJson='{\"book\":\"人教版小学语文四年级上册\",\"pageSource\":[{\"pageId\":-5,\"pageImg\":\"fm001\/bg.jpg\"},{\"pageId\":1,\"pageImg\":\"page001\/bg.jpg\"},{\"pageId\":2,\"pageImg\":\"page002\/bg.jpg\",\"buttons\":{\"button\":[{\"eventtype\":5,\"subjectNum\":1,\"itemNum\":0,\"height\":44,\"id\":1,\"soundsrc\":\"page002\/sound\/p002001.mp3\",\"width\":116,\"x\":338.667,\"y\":81.3333},{\"eventtype\":5,\"subjectNum\":1,\"itemNum\":0,\"height\":36,\"id\":2,\"soundsrc\":\"page002\/sound\/p002002.mp3\",\"width\":488,\"x\":122.667,\"y\":190.667},{\"eventtype\":5,\"subjectNum\":1,\"itemNum\":0,\"height\":366.667,\"id\":3,\"soundsrc\":\"page002\/sound\/p002003.mp3\",\"width\":620,\"x\":57.3333,\"y\":230.667}]}},{\"pageId\":186,\"pageImg\":\"zfd001\/bg.jpg\"}]}';",
	"message": "",
	"success": true
}
```

### 4. 获取电子书目录

- Method： callHostFunction
>**getCatalogByBookId_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| Func      | string,不可为空  |  方法名    |
| UserID      | string,不可为空  |  用户ID    |
| BookID      | int,不可为空  |  教材ID    |

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
         "id": 294266,
         "title": "第一单元",
         "children": [
             {
             "id": 304419,
             "title": "第一组",
             "isFolder": false,
             "sord": 0,
             "StartPage": 1,
             "EndPage": 1
             },
             {
             "id": 294267,
             "title": "1 观潮",
             "isFolder": false,
             "sord": 1,
             "StartPage": 2,
             "EndPage": 5
             }
         ],
         "isFolder": true,
         "sord": 52,
         "StartPage": 21,
         "EndPage": 39
         },
         {
         "id": 294292,
         "title": "第五单元",
         "children": [

         {
         "id": 294296,
         "title": "语文园地五",
         "isFolder": false,
         "sord": 6,
         "StartPage": 96,
         "EndPage": 98
         }
         ],
         "isFolder": true,
         "sord": 52,
         "StartPage": 81,
         "EndPage": 98
         }
      ]
}

```
在线
```js
{
	"code": 0,
	"data": "[{\"id\":294266,\"title\":\"第一单元\",\"children\":[{\"id\":304419,\"title\":\"第一组\",\"isFolder\":false,\"sord\":0,\"StartPage\":1,\"EndPage\":1},{\"id\":294267,\"title\":\"1 观潮\",\"isFolder\":false,\"sord\":1,\"StartPage\":2,\"EndPage\":5},{\"id\":294268,\"title\":\"2* 雅鲁藏布大峡谷\",\"isFolder\":false,\"sord\":3,\"StartPage\":6,\"EndPage\":9},{\"id\":304446,\"title\":\"8 人造反光植物\",\"isFolder\":false,\"sord\":8,\"StartPage\":178,\"EndPage\":179}],\"isFolder\":true,\"sord\":51,\"StartPage\":160,\"EndPage\":179},{\"id\":304447,\"title\":\"生字表（一）\",\"isFolder\":false,\"sord\":51,\"StartPage\":180,\"EndPage\":182},{\"id\":304448,\"title\":\"生字表（二）\",\"isFolder\":false,\"sord\":51,\"StartPage\":183,\"EndPage\":185}]",
	"message": "",
	"success": true
}
```

### 5. 获取教学地图

- Method： callHostFunction
>**getCurTeachMap_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| Func      | string,不可为空  |  方法名    |
| UserID      | string,不可为空  |  用户ID    |
| BookID      | int,不可为空  |  教材ID    |
| UnitID      | int,不可为空  |  单元ID    |

- 返回参数

| 返回参数      |     参数类型 |   参数说明    |
| ----------- | ------------| ----------- |
| success     |   Boolean   |  请求成功与否  |
| code        |   Int       |  执行结果code |
| message     |   String    |  执行结果消息  |
| data        |   Json      |  返回数据     |

- 返回示例
离线、在线

```js
{
  "success": true,
  "code": 0,
  "message": "",
  "data":[
             {
                 "stepName": "第一步：课堂导入",
                 "liList": [
                 {
                 "id": "p_20",
                 "pageNum": 1,
                 "sourceSrc": "bd1c19e7-b468-4092-98ec-c40827ea6ef6",
                 "sourcetype": "6",
                 "comeFrom": "ModResource",
                 "randId": "1516175282984",
                 "sourceName": "观潮-动画"
             },
             {
                 "id": "p_53",
                 "pageNum": 1,
                 "sourceSrc": "8e2ad642-e8ff-4bed-8fd2-f9927aaca14c",
                 "sourcetype": "28",
                 "comeFrom": "ModResource",
                 "randId": "1516175287888",
                 "sourceName": "观潮"
                 }
                 ]
             }
         ]
}

```
