## 地址信息
### 接口地址：
/address/info
### 请求类型：post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| address_id | 是 | string | 地址ID |
| token | 是 | String | 用户登录信令 |
### 返回参数：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | Object | 返回数据 |
### content:
| address_id | umber | 地址ID |
| firstname | String | 收货人姓名 必填最大长度250字符 |
| lastname | String | 收货人姓名 必填最大长度250字符|
| iphone | String | 收货人的联系电话 |
| country | string | 国家 最大长度50字符 |
| state | string | 州/省/区域 最大长度250字符 |
| city | string | 城市 最大长度250字符 |
| postalcode | String | 邮政编码 最大长度50字符 |
| street | String | 详细地址 最大长度1000字符 |
| suburb | String | 详细地址 最大长度1000字符 |
| default | Boolean | 是否为默认地址，默认为false |
### 返回示例：
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "address_id": 1,
        "firstname": "hao",
        "lastname": "long",
        "iphone": "13003630068",
        "country": "china",
        "state": "zhejiang",
        "city": "hangzhou",
        "street": "jiangganqu",
        "suburb": "jiuhelu",
        "postalcode": "030016",
        "default": false
    }
}
```