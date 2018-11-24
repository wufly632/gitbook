## 商品列表
### 接口地址
/products/list
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
|  currency_code | 否 | String | 货币编码 |
| cate | 否 | Int | 类目id |
| title | 否 | String | 搜索关键词 |
| page | 否 | Int | 页码(默认为：1) |
| sort | 否 | String |sort字段的值有如下几种情况，price-a：按价格排序从低到高，price-d：按价格排序从高到低，sales：按销量排序（倒序），new：按上新时间排序（倒序） |
| minprice | 否 | number | 最低价格 |
| maxprice | 否 | number | 最高价格 |
| page | 否 | number | |
### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | array | 返回数据 ,[] |
### content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| goods | Array | 结果商品数据 |
| nav | Array | 面包屑导航 |
|  currency_symbol | String | 货币符号 |
| title | String | 类目名或搜索关键字 |
| total_goods | Int | 总商品数 |
| total_page | Int | 总页数 |
### goods：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Int | 商品id |

| name | String | 商品标题 |
| img | String | 商品主图 |
| origin_price | Float | 商品原价格 |
| price | Float | 商品价格 |
| stock | Number | 商品库存 |
| rebate | Float | 商品返现金额 |
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "goods": [
            {
                "id": 294,
                "currency_symbol":"$",
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "origin_price":40,
                "price": 20,
                "stock": 85,
                "rebate": "4.00"
            }
        ],
        "total_page": 1
    }
}
```