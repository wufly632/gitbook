## 购物车提交（支付确认页面）

### 接口地址：

/carts/checkout

### 请求类型：post

#### 请求参数：

| 参数 | 必填 | 类型 | 说明 |
| :--- | :---: | :---: | :--- |
| token | 是 | String | 用户登录信令 |
| coupon\_id | 是 | String或者null | 优惠券id 没有则为空 |
| integral | 是 | Boolean | 积分是否选择 ture或者false |
| currency\_code | 是 | String | 货币编码 |

#### 返回参数：（object）

| 参数 | 类型 | 说明 |
| :--- | :---: | :--- |
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息' |
| content | object | 返回数据 |

#### content：（object）

| 参数 | 类型 | 说明 |
| :--- | :---: | :--- |
| user\_address | Array | 用户的默认地址，如果没有返回空，详情见user\_address表 |
| cards | Array | 银行卡列表 |
| currency\_symbol | String | 货币符号 |
| money | float | 用户余额 |
| price | float | 支付金额 |
| shipping | Number | 运费 |
| order\_time | number | 下单时间 |
| ordergoods | array | 订单商品信息 |

#### user\_address：\[object\]

| 参数 | 类型 | 说明 |
| :--- | :---: | :--- |
| id | number | 地址ID |
| recipients | String | 收件人 |
| address | String | 收件地址 |
| iphone | Number | 收件人手机号 |
| is\_default | number | 是否是默认地址：1是，0否 |

```
{
    "status": 200,
    "msg": "success",
    "content": {
        "user_address": [
            {
                "id": 1,
                "recipients": "hao long",
                "address": "china zhejiang hangzhou jiangganqu jiuhelu",
                "iphone": "13003630068",
                "is_default": 1
            }
        ],
        "cards":[
            {
                "id": 1,
                "number": "6217000134989987"
            },{
                "id": 1,
                "number": "6217000132289987"
            }
        ],
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
        ],
        "currency_symbol":"$",
        "money": "0.00",
        "price": "90.00",
        "shipping": "0.00"
    }
}
```



