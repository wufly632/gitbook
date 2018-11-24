## 购物车
### 接口地址：
/carts
### 请求类型：post
####  请求参数：
|参数 | 必填 | 类型 |  说明|
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| currency_code | 是 | String | 货币编码 |

####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码  |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | object | 返回数据

####  content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| goods | array | 购物车里的产品，见goods表 |
| promotion | array | 促销活动 |
| coupon | array | 优惠券,见voucher表 |
| integral | object | 积分，may：可用积分（Number），ratio：换算比例（float） |
| specialoffer | Number | 优惠金额 |
| currency_code | String | 货币符号 |
| token | string | token | 
####  coupon：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 优惠券id |
|  currency_symbol | String | 货币符号 |
| price | float | 优惠券面额 |
| use_price | float | 优惠券使用条件 |
| startdate | String | 开始时间 |
| enddate | String | 过期时间 |

####  promotion：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| promotion_id | Number | 促销活动id |
| promotion_msg | string | 门店促销活动说明 |
| goods | array | 促销活动商品 |

####  goods：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| cart_id | Number | 购物车id |
| id | Number | 产品id |
| name | float | 产品名称 |
| img | String | 产品图片 |
| is_sold_out | number | 是否售罄 |
| sku_id | Number | skuid |
| stock | Number | 库存 |
|  currency_symbol | String | 货币符号 |
| price | float | 商品价格 |
| origin_price | float | 商品原价 |
| num | Number | 用户选择的数量 |
| props | array | 属性，属性名称(String) |

#### 购物车示例代码
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "integral": 0,
        "goods": [
            {
                "cart_id": 228,
                "id": 294,
                "name": "test",
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "stock": 50,
                "sku_id": 1,
                "is_sold_out": 0,
                "origin_price": "40.00",
                "price": "20.00",
                "num": 4,
                "props": {
                    "Clothing version": "修身",
                    "size": "0-3y"
                }
            }
        ],
        "promotion": [
            {
                "promotion_id": 88,
                "promotion_msg": "再买20.00元,可享【满100元减10元】",
                "goods": [
                    {
                        "cart_id": 228,
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "stock": 50,
                        "sku_id": 1,
                        "is_sold_out": 0,
                        "origin_price": "40.00",
                        "price": "20.00",
                        "num": 4,
                        "props": {
                            "Clothing version": "修身",
                            "size": "0-3y"
                        }
                    }
                ]
            },
            {
                "promotion_id": 90,
                "promotion_msg": "再买20.00元,可享【满100元减10元】",
                "goods": [
                    {
                        "cart_id": 228,
                        "id": 294,
                        "name": "test",
                        "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "stock": 50,
                        "sku_id": 1,
                        "is_sold_out": 0,
                        "origin_price": "40.00",
                        "price": "20.00",
                        "num": 4,
                        "props": {
                            "Clothing version": "修身",
                            "size": "0-3y"
                        }
                    }
                ]
            }
        ],
        "specialoffer": "0.00",
        "coupon": [
            {
                "id": 81,
                "price": "$10",
                "use_price": "$100",
                "startdate": "2018-09-14 11:03:50",
                "endstae": "2018-09-30 11:04:08"
            }
        ],
        "token": "aegmnqrsvwxzABCDEFILOQRSVWX04569233",
        "currency_code":"$"
    }
}
```