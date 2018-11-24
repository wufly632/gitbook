## 订单列表
### 接口地址
/orders/list
### 请求类型： post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | Number | 页数,默认为1 |
| status | 否 | Number | 筛选的状态 |

### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码   |
| msg | String | 失败信息 失败：'失败信息'|
| content | array | 返回数据 |

####  content：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| orders | array | 订单信息 |
| total_page | Number | 总页数 |
| status | Number | 筛选的状态 |

####  orders：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| orderid | String | 订单id |
| orderstatus | Number | 订单状态(订单状态 1-待付款 3-待发货 4-待收货 5-交易完成 6-交易取消) |
| ordertime | string | 下单时间 |
| paytime | int | 剩余支付时间（单位秒） |
|  currency_symbol | String | 货币符号 |
| total_amount | Number | 总价 |
| ordergoods | array | 订单商品信息 |

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

```
{
    "status": 200,
    "msg": "success",
    "content": {
        "orders": [
            {
                "orderid": "2222222222",
                "orderstatus": "1",
                "ordertime": "2017-05-05 12:12:12",
                "paytime": 2000,
                "currency_symbol": "$",
                "ordergoods": [
                    {
                        "id": "1",
                        "name": "HLA/海澜之家中腰牛仔裤男2017春季热卖猫须微弹男士裤子",
                        "img": "http://192.168.1.122:6006/goods/20170703/thumb/201707031126521499052412250.jpg",
                        "price": "150.00",
                        "num": "1",
                        "sku_value_ids": "1,3",
                        "sku_value": [
                            "颜色：蓝色",
                            "尺寸：3.2英寸"
                        ]
                    }
                ]
            },
            {
                "orderid": "1111111111",
                "orderstatus": "1",
                "ordertime": "2017-05-05 12:12:12",
                "paytime": 3000, 
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
        ],
        "total_page": 1,
        "status": 1
    }
}
```