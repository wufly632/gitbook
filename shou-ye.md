## H5首页
### 接口地址
/home
### 请求方式：post
### 请求参数：
参数 | 类型 | 必选 | 说明
---|---|---|---
| <span style="color:red">currency_code</span> | String | 否 | 货币编码（默认USD） |
| page | number | 是 | 页码 |
### 返回参数：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息 成功：success 失败：'失败信息'|
| content | Object | 返回数据  |
### content:
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| banners | Array | banner数据 |
| icons | Array | 类目导航 |
| diypage | string | 自定义页面模块 |
| goods | Array | 结果商品数据 |
| <span style="color:red">currency_symbol</span> | String | 货币符号 |
| total_page | Int | 总页数 |
| flash_sale | Object |闪购|
| activities | Array |首页活动|
#### flash_sale:
|参数 |  类型 | 说明|
| :--- |:---:| :---|
|promotion_name|string|促销名称|
|promotion_id|String|促销ID|
|good_list|array|商品列表|
|end_at|int|结束剩余秒数|
##### good_list
|参数 |  类型 | 说明|
| :--- |:---:| :---|
|id|int|商品ID|
|img|string|图片|
|name|string|商品名称|
|currency_symbol|string|货币符号|
|origin_price|float|原始价格|
|price|float|价格
|stock|int|库存|
|privilege|int|折扣|
|rebate|float|返利|
#### activites
|参数 |  类型 | 说明|
| :--- |:---:| :---|
|content|object|左边位信息|
|type|int|类型1一张图，3三张图|

### 返回示例：
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "banners": [
            {
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "url": "http://m.cucoe.net/home"
            },{
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "url": "http://m.cucoe.net/home"
            }
        ],
        "icons": [
            {
                "title": "women",
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "cate": 1498
            },{
                "title": "Shoes",
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "cate": 1498
            }
        ],
        "goods": [
            {
                "id": 294,
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "orign_price": 40,
                "price": 20,
                "stock": 85,
                "rebate": 2.00
            },{
                "id": 294,
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "orign_price": 40,
                "price": 20,
                "stock": 85,
                "rebate": 2.00
            }
        ],
        "flash_sale": {
          "promotion_id": 4,
          "promotion_name": "特价",
          "good_list": [
            {
              "id": 100136,
              "img": "http:\/\/cucoe.oss-us-west-1.aliyuncs.com\/product\/000001000060\/5bd0327a83b4c.jpg",
              "name": "Multi-Function Electric Stick",
              "currency_symbol": "$",
              "origin_price": 25,
              "price": 20,
              "stock": 3938,
              "privilege": 20,
              "rebate": 0.00
            },
            {
              "id": 100144,
              "img": "http:\/\/cucoe.oss-us-west-1.aliyuncs.com\/product\/000001000063\/5bd0412c8512e.jpg",
              "name": "Outdoor Camouflage Tent",
              "currency_symbol": "$",
              "origin_price": 33.6,
              "price": 28,
              "stock": 3985,
              "privilege": 17,
              "rebate": 3.08
            }
          ],
          "end_at": 1435369
        },
        "activities": [
          {
            "content": [
              {
                "src": "http:\/\/www.lte.com\/uploads\/banners\/5bf5138551413.png",
                "link": "http:\/\/www.waiwaimall.com",
                "show": true,
                "title": "waiwaimall"
              },
              {
                "src": "http:\/\/www.lte.com\/uploads\/banners\/5bf5138551413.png",
                "link": "http:\/\/www.waiwaimall.com",
                "show": false,
                "title": "waiwaimall"
              },
              {
                "src": "http:\/\/www.lte.com\/uploads\/banners\/5bf5138551413.png",
                "link": "http:\/\/www.waiwaimall.com",
                "show": true,
                "title": "waiwaimall"
              }
            ],
            "type": 3
          },
          {
            "content": [
              {
                "src": "http:\/\/www.lte.com\/uploads\/banners\/5bf5139703af6.png",
                "link": "http:\/\/www.waiwaimall.com",
                "show": true,
                "title": "waiwaimall"
              }
            ],
            "type": 1
          }
        ]
        "currency_symbol": "$",
        "diypage": "",
        "total_page": 1
    }
}
```