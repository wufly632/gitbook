## 订单详情
### 接口地址
/orders/detail
### 请求类型： post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| order_id | 是 | String | 订单ID |

### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空 失败：'失败信息'|
| content | array | 返回数据 |
####  content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| orderid | String | 订单id |
| orderstatus | Number | 订单状态(订单状态 1-待付款 3-待发货 4-待收货 5-交易完成 6-交易取消) |
| ordertime | string | 下单时间 |
| final_amount | Number | 总价 |
| shipping | Number | 运费 |
| paytime | int | 剩余支付时间（单位秒） |
|  currency_symbol | String | 货币符号 |
| ordergoods | array | 订单商品信息 |
| name | string | 收件人 |
| telephone | string | 联系人电话 |
| address | string | 详细地址 |
####  ordergoods：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 商品ID |
| name | string | 商品名称 |
| img | string | 商品图片 |
| price | Float | 商品价格 |
| num | Number | 商品数量 |
| sku_value_ids | Number | sku属性值ID |
| sku_value | array | 商品属性 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "orderid": "1111111111",
        "orderstatus": "1",
        "ordertime": "2017-05-05 12:12:12",
        "final_amount": "298",
        "shipping":"0.00",
        "name": "longyuan",
        "telephone": "13003630069",
        "address":"zhejiang hangzhou jiuhelu 19",
        "currency_symbol": "$",
        "ordergoods": [
            {
                "id": "5",
                "name": "型马潮牌破洞牛仔裤男 夏季韩版直筒小脚裤 做旧乞丐牛仔长裤男薄 ",
                "img": "http://192.168.1.122:6006/goods/20170718/thumb/201707181645191500367519172.jpg",
                "price": "169.00",
                "num": "1",
                "sku_value_ids": "5,9",
                "sku_value": [
                    "颜色：浅蓝",
                    "尺寸：4.5英寸"
                ]
            },
            {
                "id": "5",
                "name": "型马潮牌破洞牛仔裤男 夏季韩版直筒小脚裤 做旧乞丐牛仔长裤男薄 ",
                "img": "http://192.168.1.122:6006/goods/20170718/thumb/201707181645191500367519211.jpg",
                "price": "169.00",
                "num": "1",
                "sku_value_ids": "6,3",
                "sku_value": [
                    "颜色：黑色",
                    "尺寸：3.2英寸"
                ]
            }
        ]
    }
}
```