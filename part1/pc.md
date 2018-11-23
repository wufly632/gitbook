## PC首页
### 接口地址
/pc/home
### 请求方式：post
### 请求参数：
参数 | 类型 | 必选 | 说明
---|---|---|---
| currency_code | String | 否 | 货币编码（默认USD） |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息 成功：success 失败：'失败信息'|
| content | Object | 返回数据  |
### content:
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| banners | Array | banner数据 |
| daily | Array | daily delection 商品数据 |
| storey | Array | 促销广告信息 |
| goods | Array | 结果商品数据 |
| <span style="color:red">currency_symbol</span> | String | 货币符号 |
| total_page | Int | 总页数 |
#### daily：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 商品ID |
| name | string | 商品标题 |
| img | string | 商品主图 |
| price | number | 商品售价 |
| origin_price | number | 商品原价 |
| rebate | number | 商品返利 |
| stock | number | 库存 |
#### storey [object]:
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| storey_title | string | 标题 |
| storey_url | string | 链接 |
| storey_left | Array | 促销左侧信息 |
| storey_right | Array | 促销右侧信息 |
##### storey_left：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| img | string | 图片 |
| url | string | 链接 |
##### storey_right：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 商品ID |
| name | string | 商品标题 |
| img | string | 商品主图 |
| price | number | 商品售价 |
| origin_price | number | 商品原价 |
| rebate | number | 商品返利 |
| stock | number | 库存 |
### 返回示例
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
        "daily": [
            {
                "id": 294,
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "price": 20,
                "origin_price": 24.00,
                "rebate": 5,
                "stock": 85
            },{
                "id": 294,
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "price": 20,
                "origin_price": 24.00,
                "rebate": 5,
                "stock": 85
            }
        ],
        "storey": [
            {
                "storey_title": "HOME & LIVING",
                "storey_url": "/categories/search?cate=334",
                "storey_left": [
                    {
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/0.png",
                        "url": "/categories/search?cate=334"
                    },,{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/1.png",
                        "url": "/categories/search?cate=334"
                    },{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/2.png",
                        "url": "/categories/search?cate=334"
                    },{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/3.png",
                        "url": "/categories/search?cate=334"
                    },{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/4.png",
                        "url": "/categories/search?cate=334"
                    }
                ],
                "storey_right": [
                    {
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "price": 20,
                        "origin_price": 24.00,
                        "rebate": 5,
                        "stock": 85
                    },{
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "price": 20,
                        "origin_price": 24.00,
                        "rebate": 5,
                        "stock": 85
                    }
                ]
            },{
                "storey_title": "DIGTAL",
                "storey_url": "/categories/search?cate=799",
                "storey_left": [
                    {
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/01.png",
                        "url": "/categories/search?cate=334"
                    },,{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/12.png",
                        "url": "/categories/search?cate=334"
                    },{
                        "img": "https://cucoe.oss-us-west-1.aliyuncs.com/home/22.png",
                        "url": "/categories/search?cate=334"
                    }
                ],
                "storey_right": [
                    {
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "price": 20,
                        "origin_price": 24.00,
                        "rebate": 5,
                        "stock": 85
                    },{
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "price": 20,
                        "origin_price": 24.00,
                        "rebate": 5,
                        "stock": 85
                    }
                ]
            }
        ],
        "goods":[
            {
                "id":100047,
                "name":"Selfie Stick",
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000046/5bcef6d40b8dd.jpg",
                "price":5.5,
                "origin_price": 10.00,
                "rebate": 1,
                "stock":20000
            },
            {
                "id":100046,
                "name":"Foldable Mirror Selfie Stick",
                "img":"http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000045/5bcef5d39826c.jpg",
                "price":6,
                "origin_price": 10.00,
                "rebate": 1,
                "stock":160000
            }
        ],
        "currency_symbol": "$",
        "total_page": 1
    }
}
```