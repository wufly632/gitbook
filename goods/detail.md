## 商品详情
### 请求类型：get
### 接口地址：
/products/detail
####  请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| id | 是 | Number | 商品ID |
| token | 否 | string | 登录 |
|  currency_code | 否 | String | 货币编码 |
####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | object | 返回数据 |

####  data：（object）(查到商品信息)
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| code | Number | 货号 |
| max_integral | Number | 最多可获得积分 |
| name | String | 商品名称 |
| summary | String | 店铺卖点 |
| video | string | 小视频 |
| category_path | array | 商品类目路径 |
| coupon | array | 店铺优惠券 |
| style | array | 款式，具体见style表 |
|  currency_symbol | String | 货币符号 |
| prop | array | 非关键属性 |
| images | array | 详情图片 |
| num | Number | 活动商品剩余数量(只限于限量秒杀活动) |
| promotion | object | 活动详情 |

####  style：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | String | SKU的id |
| name | String | 属性名称 如'颜色' |
| value | String | 属性值 如'蓝色' |
| icon | String | sku主图 |
| sub | array | 第二个销售属性信息 如[object,object] |
| img | array | 款式图片 |
| price | Number | 价格 |
| origin_price | Number | 原价 |
| discount | String | 优惠比例 |
| prom_price | Number | 优惠价格(只有促销活动为限时特价、限量秒杀时该字段存在) |
| stock | Number | 库存 |

#### promotion：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | String | 活动ID |
| rule | String | 活动规则 |
| start_at | String | 活动开始时间 |
| end_at | String | 活动结束时间 |

#### coupon：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|    
| id | number | 优惠券ID |
| type | Int | 券类型 （1-面额，2-折扣）|
| currency_symbol | String | 货币符号 |
| price | Float | 优惠券金额 |
| use_price | Float | 使用条件 |
| startdate | String | 开始时间 |
| enddate | String | 过期时间 |
| datestatus | Int | 优惠券状态 1-可领取 2-已领取 3-已领完 |
#### sub : （object）
| 参数 | 类型 | 说明 |
| :--- |:---:| :---|
| id | String | SKO的id |
| name | String | 属性名称 如'颜色' |
| value | String | 属性值 如'蓝色' |
| icon | String | sku主图 |
| sub | array | 第三个销售属性信息 如[object,object] |
| img | array | 款式图片 |
| price | Number | 价格 |
| origin_price | Number | 原价 |
| discount | String | 优惠比例 |
| prom_price | Number | 优惠价格(只有促销活动为限时特价、限量秒杀时该字段存在) |
| stock | Number | 库存 |

```
{
    "status": 200,
    "msg": "success",
    "content": {
        "code": "CS0001",
        "name": "test",
        "summary": "test",
        "images": null,
        "video":"",
        "category_path": ["Digital", "Cellular Phone", "Mobile Phone Cases"]，
        "max_integral": 20,
        "return_ratio": "20%",
        "promotion": {
            "role": "",
            "start_at": "2018-09-12 15:38:38",
            "end_at": "2018-10-31 15:38:51"
        },
        "coupon": [
            {
                "id": 20,
                "price": "$10",
                "use_price": "$100",
                "startdate": "2018-09-12 16:05:16",
                "enddate": "2018-09-12 16:05:16",
                "datestatus": 1
            }
        ],
        "style": [
            {
                "id": 1,
                "name": "color",
                "value": "red1",
                "icon": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "img": [
                    "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg"
                ],
                "price": "20.00",
                "origin_price": "15.00",
                "discount": "31%",
                "prom_price": 0,
                "stock": 50,
                "sub": [
                    {
                        "id": 1,
                        "name": "size",
                        "value": "0-3y",
                        "icon": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "img": [
                            "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg"
                        ],
                        "price": "20.00",
                        "origin_price": "15.00",
                        "discount": "31%",
                        "prom_price": 0,
                        "stock": 50,
                        "sub": []
                    },
                    {
                        "id": 2,
                        "name": "size",
                        "value": "3-6y",
                        "icon": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                        "img": [
                            "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg"
                        ],
                        "price": "20.00",
                        "origin_price": "15.00",
                        "discount": "31%",
                        "prom_price": 0,
                        "stock": 50,
                        "sub": []
                    }
                ]
            }
        ],
        "prop": {
            "Clothing version": "修身",
            "size": "0-3y"
        }
    }
}
```