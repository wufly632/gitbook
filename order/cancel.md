## 订单取消
### 接口地址
/orders/cancel
### 请求类型：post
### 请求参数
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| order_id | 是 | String | 订单ID |

### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空 失败：'失败信息'|
| content | '' | 返回数据 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": ""
}
```