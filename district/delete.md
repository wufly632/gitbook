## 地址删除
### 接口地址：
/address/delete
### 请求类型：post
### 请求参数：
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
            "id": 4,
            "recipients": "hao long",
            "address": "china zhejiang hangzhou jiuhelu ",
            "iphone": "1300363",
            "is_default": 0
        }
    ]
}
```