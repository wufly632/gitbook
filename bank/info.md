## 银行卡信息
### 接口地址
/cards/info
### 请求方式：post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| card_id | 是 | String | 银行卡ID |
### 返回参数：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空 |
| content | String | 返回信息 |
### content：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| card | Object | 银行卡信息 |
| address | Object | 账单地址信息 |
### card：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | Number | 银行卡ID |
| number | String | 银行卡号 |
| exp | String | 银行卡到期时间 |
| cvc | string | 安全码 |
| is_default | Boolean | 是否是默认付款卡 |
### address：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| firstname | String | 银行卡持有人姓名 |
| lastname | String | 银行卡持有人姓名 |
| iphone | String | 银行卡持有人的联系电话 |
| country | string | 国家 最大长度50字符 |
| state | string | 州/省/区域 最大长度250字符 |
| city | string | 城市 最大长度250字符 |
| postalcode | String | 邮政编码 最大长度50字符 |
| street | String | 详细地址 最大长度1000字符 |
| suburb | String | 详细地址 最大长度1000字符 |
| email | String | 账单邮箱地址 |
### 返回示例：
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "card":{
            "id": 1,
            "number": "6217000134989987",
            "exp":"06/23",
            "cvc":686,
            "is_default":true
        },
        "address":{
            "firstname": "hao",
            "lastname": "long",
            "iphone": "13003630068",
            "country": "china",
            "state": "zhejiang",
            "city": "hangzhou",
            "street": "jiangganqu",
            "suburb": "jiuhelu",
            "postalcode": "030016",
            "email":"long.hao@cucoe.com"
        }
    }
}
```