## 待入账
### 接口地址：
/personal/account
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | Number | 页数 |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空 |
| content | Object | 返回信息 |
#### content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| total_page | Number | 总页数 |
| accounts | Array | 收入列表 |
#### accounts：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| image | String | 用户头像 |
| type | String | 收入类型 |
| description | String | 描述 |
|  currency_symbol | String | 货币符号 |
| amount | Number | 金额 |
| date | String | 消费时间 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "total_page": 2,
        "accounts": [
            {
                "image": "http://www.baidu.com",
                "type": "Shopping Reward",
                "description": "You have placed an order for $123",
                "currency_symbol":"$",
                "amount": "20",
                "date": "2018-09-25 10:23:56"
            },{
                "image": "http://www.baidu.com",
                "type": "Reward by your fans‘ shopping",
                "description": "Your fan CoCo placed an order for $123",
                "currency_symbol":"$",
                "amount": "20",
                "date": "2018-09-25 10:23:56"
            }
        ]
    }
}
```