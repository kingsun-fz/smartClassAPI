
## 智慧教室接口说明

[TOC]

### 状态码统一说明999999
- 0 成功

- -1失败


### 1. 获取页面水滴json

- Method： callHostFunction
>**getAllWare_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| s           | String,不可为空 |  方法ID和参数|

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
  "data":"{"pageNum":6,"imgSrc":"images/06.jpg","btns":[{"id":"p_76","icoType":"6","randId":"1505813969790","isread":true,"sourceUrl":"c6837bb1-ea95-4546-94b6-cb72bdd6f694","X":540.6465126811594,"Y":341.0474788647343,"title":"雅鲁藏布大峡谷-动画","comeFrom":"ModResource"},{"id":"p_71","icoType":"28","randId":"1516176667515","isread":false,"sourceUrl":"9b09b50d-6efc-4c7d-95da-4dd9415db984","X":558.3325030193237,"Y":432.0040006038647,"title":"雅鲁藏布大峡谷","comeFrom":"ModResource"},{"id":"p_78","icoType":"27","randId":"1516179499180","isread":false,"sourceUrl":"950baed5-b7de-48dc-b00b-1a14713f6628","X":669.5015851449275,"Y":314.5184933574879,"title":"茫-识字-鸟的天堂","comeFrom":"ModResource"}]}"
}
```
### 2. 获取互动课件配置首页html

- Method： callHostFunction
>**wareEntry_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| s           | String,不可为空 |  方法ID和参数|

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
  "data":"F:\GitWork\offline_win\SmarterClassroomWindows\bin\x86\Debug\Page\data\RJYW4A\resource\第一单元\950baed5-b7de-48dc-b00b-1a14713f6628\ren_mang\ren_mang.html"
}

```
### 3. 获取电子书dbjs

- Method： callHostFunction
>**getDbJs_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| s           | String,不可为空 |  方法ID和参数|

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
  "data":"var dbJson='{"book":"人教版小学语文四年级上册","pageSource":[{"pageId":-5,"pageImg":"fm001/bg.jpg"},{"pageId":-4,"pageImg":"fm002/bg.jpg"},{"pageId":-3,"pageImg":"fy001/bg.jpg"},{"pageId":-2,"pageImg":"ml001/bg.jpg"},{"pageId":-1,"pageImg":"ml002/bg.jpg"},{"pageId":0,"pageImg":"ml003/bg.jpg"},{"pageId":1,"pageImg":"page001/bg.jpg"},{"pageId":2,"pageImg":"page002/bg.jpg","buttons":{"button":[{"eventtype":5,"subjectNum":1,"itemNum":0,"height":44,"id":1,"soundsrc":"page002/sound/p002001.mp3","width":116,"x":338.667,"y":81.3333},{"eventtype":5,"subjectNum":1,"itemNum":0,"height":36,"id":2,"soundsrc":"page002/sound/p002002.mp3","width":488,"x":122.667,"y":190.667},{"eventtype":5,"subjectNum":1,"itemNum":0,"height":366.667,"id":3,"soundsrc":"page002/sound/p002003.mp3","width":620,"x":57.3333,"y":230.667}]}},{"pageId":3,"pageImg":"page003/bg.jpg","buttons":{"button":[{"eventtype":5,"subjectNum":1,"itemNum":0,"height":242.667,"id":1,"soundsrc":"page003/sound/p003001.mp3","width":612,"x":82.6667,"y":325.333},{"eventtype":5,"subjectNum":1,"itemNum":0,"height":241.333,"id":2,"soundsrc":"page003/sound/p003002.mp3","width":616,"x":78.6667,"y":572},{"eventtype":5,"subjectNum":1,"itemNum":0,"height":160,"id":3,"soundsrc":"page003/sound/p003003.mp3","width":608,"x":86.6667,"y":817.333}]}},{"pageId":4,"pageImg":"page004/bg.jpg"},{"pageId":5,"pageImg":"page005/bg.jpg"},{"pageId":186,"pageImg":"zfd001/bg.jpg"}]}';"
}

```
### 4. 获取电子书目录

- Method： callHostFunction
>**getCatalog_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| s           | String,不可为空 |  方法ID和参数|

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
  "data":"[{"id":294266,"title":"第一单元","children":[{"id":304419,"title":"第一组","isFolder":false,"sord":0,"StartPage":1,"EndPage":1},{"id":294267,"title":"1 观潮","isFolder":false,"sord":1,"StartPage":2,"EndPage":5},{"id":294268,"title":"2* 雅鲁藏布大峡谷","isFolder":false,"sord":3,"StartPage":6,"EndPage":9},{"id":294269,"title":"3 鸟的天堂","isFolder":false,"sord":4,"StartPage":10,"EndPage":13},{"id":294270,"title":"4* 火烧云","isFolder":false,"sord":4,"StartPage":14,"EndPage":16},{"id":304420,"title":"词语盘点","isFolder":false,"sord":4,"StartPage":17,"EndPage":17},{"id":294271,"title":"语文园地一","isFolder":false,"sord":5,"StartPage":18,"EndPage":20}],"isFolder":true,"sord":52,"StartPage":1,"EndPage":20},{"id":294272,"title":"第二单元","children":[{"id":304422,"title":"第二组","isFolder":false,"sord":1,"StartPage":21,"EndPage":21},{"id":294273,"title":"5 古诗两首","children":[{"id":294274,"title":"题西林壁","isFolder":false,"sord":1,"StartPage":22,"EndPage":22},{"id":294275,"title":"游山西村","isFolder":false,"sord":2,"StartPage":23,"EndPage":24}],"isFolder":true,"sord":2,"StartPage":22,"EndPage":24},{"id":294276,"title":"6 爬山虎的脚","isFolder":false,"sord":3,"StartPage":25,"EndPage":27},{"id":294277,"title":"7 蟋蟀的住宅","isFolder":false,"sord":4,"StartPage":28,"EndPage":31},{"id":294278,"title":"8* 世界地图引出的发现","isFolder":false,"sord":5,"StartPage":32,"EndPage":34},{"id":304423,"title":"词语盘点","isFolder":false,"sord":5,"StartPage":35,"EndPage":35},{"id":294279,"title":"语文园地二","isFolder":false,"sord":7,"StartPage":36,"EndPage":39}],"isFolder":true,"sord":52,"StartPage":21,"EndPage":39},{"id":294280,"title":"第三单元","children":[{"id":304424,"title":"第三组","isFolder":false,"sord":1,"StartPage":40,"EndPage":40},{"id":294281,"title":"9 巨人的花园","isFolder":false,"sord":2,"StartPage":41,"EndPage":45},{"id":294282,"title":"10* 幸福是什么","isFolder":false,"sord":3,"StartPage":46,"EndPage":50},{"id":294283,"title":"11 去年的树","isFolder":false,"sord":4,"StartPage":51,"EndPage":53},{"id":294284,"title":"12* 小木偶的故事","isFolder":false,"sord":5,"StartPage":54,"EndPage":57},{"id":304425,"title":"词语盘点","isFolder":false,"sord":5,"StartPage":58,"EndPage":58},{"id":294285,"title":"语文园地三","isFolder":false,"sord":7,"StartPage":59,"EndPage":61}],"isFolder":true,"sord":52,"StartPage":40,"EndPage":61},{"id":294286,"title":"第四单元","children":[{"id":304426,"title":"第四组","isFolder":false,"sord":1,"StartPage":62,"EndPage":62},{"id":294287,"title":"13 白鹅","isFolder":false,"sord":2,"StartPage":63,"EndPage":66},{"id":294288,"title":"14* 白公鹅","isFolder":false,"sord":3,"StartPage":67,"EndPage":69},{"id":294289,"title":"15 猫","isFolder":false,"sord":4,"StartPage":70,"EndPage":73},{"id":294290,"title":"16* 母鸡","isFolder":false,"sord":5,"StartPage":74,"EndPage":76},{"id":304427,"title":"词语盘点","isFolder":false,"sord":5,"StartPage":77,"EndPage":77},{"id":294291,"title":"语文园地四","isFolder":false,"sord":7,"StartPage":78,"EndPage":80}],"isFolder":true,"sord":52,"StartPage":62,"EndPage":80},{"id":294292,"title":"第五单元","children":[{"id":304428,"title":"第五组","isFolder":false,"sord":1,"StartPage":81,"EndPage":81},{"id":294293,"title":"17 长城","isFolder":false,"sord":2,"StartPage":82,"EndPage":86},{"id":294294,"title":"18 颐和园","isFolder":false,"sord":3,"StartPage":87,"EndPage":90},{"id":294295,"title":"19* 秦兵马俑","isFolder":false,"sord":4,"StartPage":91,"EndPage":94},{"id":304429,"title":"词语盘点","isFolder":false,"sord":4,"StartPage":95,"EndPage":95},{"id":294296,"title":"语文园地五","isFolder":false,"sord":6,"StartPage":96,"EndPage":98}],"isFolder":true,"sord":52,"StartPage":81,"EndPage":98},{"id":294297,"title":"第六单元","children":[{"id":304436,"title":"第六组","isFolder":false,"sord":-10,"StartPage":99,"EndPage":99},{"id":294298,"title":"20 古诗两首","children":[{"id":294299,"title":"黄鹤楼送孟浩然之广陵","isFolder":false,"sord":1,"StartPage":100,"EndPage":100},{"id":294300,"title":"送元二使安西","isFolder":false,"sord":2,"StartPage":101,"EndPage":102}],"isFolder":true,"sord":-9,"StartPage":100,"EndPage":102},{"id":294301,"title":"21 搭石","isFolder":false,"sord":-9,"StartPage":103,"EndPage":105},{"id":294302,"title":"22 跨越海峡的生命桥","isFolder":false,"sord":-9,"StartPage":106,"EndPage":108},{"id":294303,"title":"23* 卡罗纳","isFolder":false,"sord":-9,"StartPage":109,"EndPage":112},{"id":294304,"title":"24* 给予是快乐的","isFolder":false,"sord":-9,"StartPage":113,"EndPage":115},{"id":294305,"title":"词语盘点","isFolder":false,"sord":-9,"StartPage":116,"EndPage":116},{"id":304437,"title":"语文园地六","isFolder":false,"sord":-8,"StartPage":117,"EndPage":119}],"isFolder":true,"sord":52,"StartPage":99,"EndPage":119},{"id":294306,"title":"第七单元","children":[{"id":304432,"title":"第七组","isFolder":false,"sord":1,"StartPage":120,"EndPage":120},{"id":294307,"title":"25 为中华之崛起而读书","isFolder":false,"sord":2,"StartPage":121,"EndPage":125},{"id":294308,"title":"26 那片绿绿的爬山虎","isFolder":false,"sord":3,"StartPage":126,"EndPage":130},{"id":294309,"title":"27* 乌塔","isFolder":false,"sord":4,"StartPage":131,"EndPage":133},{"id":294310,"title":"28* 尺有所短 寸有所长","isFolder":false,"sord":5,"StartPage":134,"EndPage":137},{"id":304433,"title":"词语盘点","isFolder":false,"sord":5,"StartPage":138,"EndPage":138},{"id":294311,"title":"语文园地七","isFolder":false,"sord":7,"StartPage":139,"EndPage":141}],"isFolder":true,"sord":52,"StartPage":120,"EndPage":141},{"id":294312,"title":"第八单元","children":[{"id":304434,"title":"第八组","isFolder":false,"sord":0,"StartPage":142,"EndPage":142},{"id":294313,"title":"29 呼风唤雨的世纪","isFolder":false,"sord":1,"StartPage":143,"EndPage":145},{"id":294314,"title":"30* 电脑的住宅","isFolder":false,"sord":2,"StartPage":146,"EndPage":147},{"id":294315,"title":"31 飞向蓝天的恐龙","isFolder":false,"sord":3,"StartPage":148,"EndPage":152},{"id":294316,"title":"32* 飞船上的特殊乘客","isFolder":false,"sord":4,"StartPage":153,"EndPage":155},{"id":304435,"title":"词语盘点","isFolder":false,"sord":4,"StartPage":156,"EndPage":156},{"id":294317,"title":"语文园地八","isFolder":false,"sord":6,"StartPage":157,"EndPage":159}],"isFolder":true,"sord":52,"StartPage":142,"EndPage":159},{"id":304438,"title":"选读课文","children":[{"id":304439,"title":"1 延安，我把你追寻","isFolder":false,"sord":1,"StartPage":160,"EndPage":161},{"id":304440,"title":"2 五彩池","isFolder":false,"sord":2,"StartPage":162,"EndPage":163},{"id":304441,"title":"3 小青石","isFolder":false,"sord":3,"StartPage":164,"EndPage":167},{"id":304442,"title":"4 麻雀","isFolder":false,"sord":4,"StartPage":168,"EndPage":169},{"id":304443,"title":"5 迷人的张家界","isFolder":false,"sord":5,"StartPage":170,"EndPage":172},{"id":304444,"title":"6 一个苹果","isFolder":false,"sord":6,"StartPage":173,"EndPage":175},{"id":304445,"title":"7 真实的高度","isFolder":false,"sord":7,"StartPage":176,"EndPage":177},{"id":304446,"title":"8 人造反光植物","isFolder":false,"sord":8,"StartPage":178,"EndPage":179}],"isFolder":true,"sord":52,"StartPage":160,"EndPage":179},{"id":304447,"title":"生字表（一）","isFolder":false,"sord":52,"StartPage":180,"EndPage":182},{"id":304448,"title":"生字表（二）","isFolder":false,"sord":52,"StartPage":183,"EndPage":185}]"
}

```
### 5. 获取教学地图

- Method： callHostFunction
>**getTeachMap_n**

- 请求参数

| 请求参数     |     参数类型    |   参数说明   |
| ----------- | --------------- |----------- |
| s           | String,不可为空 |  方法ID和参数|

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
  "data":"[{"stepName":"第一步：课堂导入","liList":[{"id":"p_20","pageNum":1,"sourceSrc":"bd1c19e7-b468-4092-98ec-c40827ea6ef6","sourcetype":"6","comeFrom":"ModResource","randId":"1516175282984","sourceName":"观潮-动画"},{"id":"p_53","pageNum":1,"sourceSrc":"8e2ad642-e8ff-4bed-8fd2-f9927aaca14c","sourcetype":"28","comeFrom":"ModResource","randId":"1516175287888","sourceName":"观潮"}]}]"
}

```
