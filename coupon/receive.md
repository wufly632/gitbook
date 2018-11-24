## 优惠券领取
### 接口地址
/coupons/receive
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| id | 是 | string | 要领取的优惠券ID |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息   成功：success   失败：'失败信息'|
| content | String | success |
```
{
    "status": 200,
    "msg": "success",
    "content": "success"
}
```