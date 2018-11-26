## 促销列表
### 接口地址：
/promotions/list
### 请求类型：get
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| promotion_id | 是 | Number | 促销id |
| page | 否 | Number | 页数 |
####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | array | 返回数据 |

####  content：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| activityType | String | 促销活动类别(reduce：满减，return：满返，discount：多件多折，wholesale：X元n件，limit：限时特价，quantity：限量秒杀，give：买n免1) |
| promotions | array | 促销活动信息 |
| goods | array | 促销商品信息 |
| coupons | array | 促销优惠券(仅满返优惠券有此参数) |
| currency_same | boolean | 货币是否一致 |
| total_page | Number | 总页数 |

####  promotions：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| promotion_start | String | 促销活动开始时间 |
| promotion_end | String | 促销活动结束时间 |
| promotion_msg | String | 促销活动说明 |
| promotion_h5_banner | String | 促销活动H5 banner图 |
| promotion_pc_banner | String | 促销活动PC banner图 |

####  goods：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 商品id |
| img | String | 商品图片 |
| name | String | 商品名称 |
|  currency_symbol  | String | 货币符号 |
| origin_price | float | 商品原价 |
| price | float | 商品价格 |
| prom_price | float | 促销价格 |
| stock | Number | 商品库存 |

####  coupons：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 优惠券id |
| type  | Int | 优惠券类型(1-面额 2-折扣) |
| currency_symbol  | String |货币符号 |
| price | float | 优惠券面额/折扣 |
| use_price | float | 优惠券使用条件 |
| startdate | String | 开始时间 |
| enddate | String | 结束时间 |
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "goods": [
            {
                "id": 294,
                "img": "http://cucoe.oss-us-west-1.aliyuncs.com/product/000001000001/5b97c013e60ef.jpg",
                "name": "CS",
                "currency_symbol":"$",
                "origin_price": 40,
                "price": 20,
                "stock": 85
            }
        ],
        "coupons": [
            {
                "id": 65,
                "type": 2,
                "currency_symbol":"$",
                "price": 9,
                "use_price": "90.00"
                "startdate": "2018-09-13 16:05:00",
                "enddate": "2018-10-31 16:05:06"
            },{
                "id": 66,
                "type": 1,
                "currency_symbol":"$",
                "price": "10.00",
                "use_price": "90.00"
                "startdate": "2018-10-05 16:05:00",
                "enddate": "2018-10-12 16:05:06"
            }
        ],
        "promotions": {
            "promotion_start": "2018-09-12 15:38:38",
            "promotion_end": "2018-10-31 15:38:51",
            "promotion_msg": "满¥100减¥10",
            "promotion_h5_banner": "http://cucoe.oss-us-west-1.aliyuncs.com/promotion/5bcdcbc33c86e.jpg",
            "promotion_pc_banner": "http://cucoe.oss-us-west-1.aliyuncs.com/promotion/5bcdcbc33c86e.jpg"
        },
        "activityType": "reduce",
        "total_page": 1
    }
}
```