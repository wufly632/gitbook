## 银行卡编辑
### 接口地址：
/cards/edit
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| card_id | 是 | String  | 订单号 |
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
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": ""
}
```