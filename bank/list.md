## 银行卡列表
### 接口地址
/cards/list
### 请求类型：post
### 请求参数：
| 参数 | 必填 | 类型 | 说明 |
|:---|:---:|:---:|:---|
| token | 是 | String | 用户登录信令 |
| page | 否 | number | 页码 |
###  返回参数：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| status | Number | 状态码 |
| msg | String | 失败信息   成功：空 |
| content | Object | 返回信息 |
### content：（object）
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| cards | Array | 结果商品数据 |
| total_page | Int | 总页数 |
### cards：
|参数 |  类型 | 说明|
| :--- |:---:| :---|
| id | number | 银行卡ID |
| number | string | 银行卡号 |
| is_default | Boolean | 是否是默认支付卡 |
### 返回示例
```
{
    "status": 200,
    "msg": "success",
    "content": {
        "total_page": 2,
        "cards":[
            {
                "id": 1,
                "number": "6217000134989987",
                "is_default": true
            },{
                "id": 1,
                "number": "6217000132289987",
                "is_default": false
            }
        ]
    }
}
```