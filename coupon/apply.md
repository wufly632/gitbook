## 优惠券兑换
### 接口地址
/coupons/apply
### 请求方式：post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| key | 是 | string | 优惠券领取口令 |
### 返回参数：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息   成功：success   失败：'失败信息'|
| content | Object | 优惠券信息 |
### 返回示例：
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "coupons": [
            {
                "id": 85,
                "price": 10,
                "use_price": 90,
                "startdata": "2018-09-13 16:05:00",
                "enddate": "2018-10-31 16:05:06"
            },
            {
                "id": 86,
                "price": 43,
                "use_price": 11,
                "startdata": "2018-10-21 04:07:21",
                "enddate": "2018-10-28 04:07:21"
            }
        ]
    }
}
```