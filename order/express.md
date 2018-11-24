## 物流详情
### 接口地址
/orders/logDetail
### 请求类型： post
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| order_id | 是 | String | 订单ID |

### 返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息 成功：空 失败：'失败信息'|
| content | Object | 返回数据 |
### content：( Object )
| 参数 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| img | string | 订单商品主图 |
| items | number | 订单sku数量 | 
| status | string | 物流状态 |
| type | string | 物流类型 |
| number | string | 物流单号 |
| tel | string | 物流公司官方电话 |
| detail | Array | 物流详情 |
### detail: [object]
| 参数 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| img | string | 订单商品主图 |
| items | number | 订单sku数量 | 
| status | string | 物流状态 |
| type | string | 物流类型 |
| number | string | 物流单号 |
| tel | string | 物流公司官方电话 |
| detail | Array | 物流详情 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "img":"http://192.168.1.122:6006/goods/20170718/thumb/201707181645191500367519172.jpg",
        "items": 2,
        "status": "transit",
        "type": "Express",
        "number": "3900271506000",
        "tel": "88675",
        "detail": [
            {
                "date": "2018-04-14 15:12:00",
                "description": "Shipment delivered"
            },{
                "date": "2018-04-14 07:47:00",
                "description": "OUT FOR DELIVERY"
            }
        ]
    }
}
```