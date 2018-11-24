## 货币列表
### 接口地址：
/currency
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空 |
| content | Object |  |

#### content：（object）stripe支付返回
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| currency_code | String | 货币编码 |
| currency_symbol | String | 货币符号 |
| flag | String | 国旗 |
| threshold | float | 包邮门槛 |
| fare | float | 运费 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "currency": [
            {
                "currency_code":"CNY",
                "currency_symbol":"￥",
                "flag":"http://patpatdev.s3.amazonaws.com/national_flag/58eb6beda1e35/1491823597.png",
                "threshold":19,
                "fare":10
            },
            {
                "currency_code":"USD",
                "currency_symbol":"$",
                "flag":"http://patpatdev.s3.amazonaws.com/national_flag/58eb6beda1e35/1491823597.png",
                "threshold":19,
                "fare":10
            }
        ]
    }
}
```