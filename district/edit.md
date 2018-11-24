## 地址修改
### 接口地址：
/address/edit
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| address_id | 是 | string | 地址ID |
| firstname | 是 | String | 收货人姓名 必填最大长度250字符 |
| lastname | 是 | String | 收货人姓名 必填最大长度250字符|
| iphone | 是 | String | 收货人的联系电话 |
| country | 是 | string | 国家 最大长度50字符 |
| state | 是 | string | 州/省/区域 最大长度250字符 |
| city | 是 | string | 城市 最大长度250字符 |
| postalcode | 否 | String | 邮政编码 最大长度50字符 |
| street | 是 | String | 详细地址 最大长度1000字符 |
| suburb | 否 | String | 详细地址 最大长度1000字符 |
| default | 否 | Boolean | 是否为默认地址，默认为false |
| token | 是 | String | 用户登录信令 |

####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | [Object] | 返回数据 |
#### content : [object]
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | number | 地址ID |
| recipients | String | 收件人 |
| address | String  | 收件地址 |
| iphone | Number  | 收件人手机号 |
| is_default| number | 是否是默认地址：1是，0否 |
```
{
    "status": 200,
    "msg": "success",
    "content": [
        {
            "id": 1,
            "recipients": "hao long",
            "address": "china zhejiang hangzhou jiangganqu jiuhelu",
            "iphone": "13003630068",
            "is_default": 0
        },
        {
            "id": 5,
            "recipients": "hao long",
            "address": "china zhejiang hangzhou jiuhelu ",
            "iphone": "1300363",
            "is_default": 1
        }
    ]
}
```