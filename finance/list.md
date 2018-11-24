## 交易流水
### 接口地址
/personal/finance
### 请求类型： post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空   失败：'失败信息'|
| content | array | 返回数据 ,[{},{}] |

####  content：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
|  currency_symbol | String | 货币符号 |
| money | Float | 可用余额 |
| finances | Array | 余额明细 |
| total_page | Number | 总页数 |

####  finances：（[object]）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
|  currency_symbol | String | 货币符号 |
| amount | Float | 交易金额 |
| operate_type | String | 操作类型 |
| operate_description | String | 操作描述 |
| created_at | String | 交易时间 |
```
{
    "status": true,
    "msg": "success",
    "content": {
        "money": "10.00",
        "currency_symbol":"$",
        "finance": [
            {
                "currency_symbol":"$",
                "amount": "40.00",
                "operate_type": "Shopping Consumption",
                "operate_description":"You spend $40 on shopping",
                "created_at": "2017-07-05 15:06:40"
            },
            {
                "currency_symbol":"$",
                "amount": "120.00",
                "operate_type": "Shopping Reward",
                "operate_description":"You have placed on order for $123",
                "created_at": "2017-07-05 15:06:40"
            }
        ],
        "total_page": 1
    }
}
```