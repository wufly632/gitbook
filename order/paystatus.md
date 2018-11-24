## 支付状态
### 接口地址：
/payment/status
### 请求类型：post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| order_id | 是 | String | 订单号 |
####  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空 |
| content | Object |  |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "orderstatus": "success",
        "order_id": "1227208457113441162",
        "currency_symbol":"$",
        "price": "90"
    }
}
```