## 用户中心（PC）
### 接口地址：
/pc/personal/index
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
|  currency_code | 否 | String| 货币编码|

###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | number | 状态码  200 |
| msg | String | 失败信息   成功：success   失败：'失败信息'|
| content | object | 返回数据 |

####  content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| img | String | 用户头像 |
| username | String | 用户名称 |
| integral | Number | 积分 |
| card | Number | 用户优惠券数量 |
|  currency_symbol | String | 货币符号 |
| money | Number | 用户余额 |
| income | Number | 累计收入 |
| wait_account | Number | 待入账金额 |
| fans | Number | 粉丝数 |
| order_unpay | number | 未支付订单数 |
| order_ship | number | 已发货订单 |
| order_all | number | 订单数 |
#### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "img":"http://192.168.1.122:6006/",
        "username": "iykf",
        "integral": "0",
        "money": "0.00",
        "card": "2",
        "income": "230.46",
        "wait_account": "12.5",
        "funs": 20,
        "order_unpay": 2,
        "order_ship": 4,
        "order_all":10
    }
}
```