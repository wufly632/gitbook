## 优惠券列表
### 接口地址
/personal/coupons
### 请求类型： post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | Number | 页数,默认为1 |
### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | array | 返回数据 ,[{},{}] |
#### content : (object)
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| total_page | Number | 总页数 |
| coupons | Array | 优惠券数据 |
#### coupons：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| currency_symbol | String | 货币符号 |
| price | Float | 优惠券金额 |
| use_price | Float | 使用条件 |
| startdate | String | 开始时间 |
| enddate | String | 过期时间 |
| datestatus | Int | 优惠券状态 1-可用 2-未开始 3-已过期未使用 4-已使用|
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "total_page": 1,
        "coupons": [
            {
                "currency_symbol": "$",
                "price": 30,
                "use_price": 100,
                "startdate": "2017-05-05 12:12:12",
                "enddate": "2017-12-05 12:12:12",
                "datestatus": 1
            },
            {
                "currency_symbol": "$",
                "price": 50,
                "use_price": 200,
                "startdate": "2017-05-05 12:12:12",
                "enddate": "2017-12-05 12:12:12",
                "datestatus": 1
            }
        ]
    }
}
```