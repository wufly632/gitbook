## 去支付(购物车支付)
### 接口地址：
/orders/cartPay
### 请求类型：post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| type	| 是 | Number | 订单来源(1：PC端，2：H5，4：APP) |
| coupon_id | 是 | String或者null | 优惠券id 没有则为空 |
| integral | 是 | Boolean | 积分是否选择 | ture或者false |
| currency_code | 是 | String | 货币编码 |
| date | 否 | string | 用户本地时间 |
| address_id | 是 | Number  | 地址id |
| balance | 是 | Boolean  | 是否使用余额 ture或者false |
| pay_type | 是 | Number  | 支付方式 2-paypal 3-stripe |
| source | 否 | string | 支付资源（当支付方式为stripe时必填）|
| number | 否 | string | 银行卡号 |
| exp | 否 | string | 银行卡到期时间，格式：月/年 |
| cvc | 否 | string | 银行卡安全码 |
| is_default | 否 | Boolean | 是否为默认银行卡 |
| firstname | 否 | String | 银行卡持有人姓名 必填最大长度250字符 |
| lastname | 否 | String | 银行卡持有人姓名 必填最大长度250字符|
| iphone | 否 | String | 银行卡持有人的联系电话 |
| country | 否 | string | 国家 最大长度50字符 |
| state | 否 | string | 州/省/区域 最大长度250字符 |
| city | 否 | string | 城市 最大长度250字符 |
| postalcode | 否 | String | 邮政编码 最大长度50字符 |
| street | 否 | String | 详细地址 最大长度1000字符 |
| suburb | 否 | String | 详细地址 最大长度1000字符 |
| email | 否 | String | 账单邮箱 |

####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空   失败：'失败信息'|
| content | array | 返回信息 |

#### content：（object）paypal支付返回
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| payUrl | string | 支付链接（paypal支付返回） |
| orderType | string | 订单类型 order-普通订单 |
| orderId | string |  订单号 |
#### content：（object）stripe支付返回
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| orderType | String | 订单类型 order-普通订单 |
| orderId | String | 订单号 |
| price | float | 支付金额（普通订单返回） |
#### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "orderId": "1227208457113410162",
        "orderType": "order",
        "payUrl": "https://www.sandbox.paypal.com/cgi-bin/webscr?cmd=_express-checkout&token=EC-2S5396037N451730C"
    }
}
```