## 用户未登录购物车数据
### 接口地址
/carts/show
### 请求类型 post
### 请求参数：
|参数 | 必填 | 类型 |  说明|
|:---|:---:|:---:|:---|
| good_info | 是 | [object] | 购物车商品信息 |
|  currency_code | 是 | String | 货币编码 |
### good_info : [object]
| good_id | 是 | number | 商品ID |
| sku_id | 是 | number | sku ID |
| num | 是 | number | 商品数量 |
### 请求参数示例：
```
{
    "good_info":[
        {
            "good_id":294,
            "sku_id":1,
            "num":3
        },{
            "good_id":294,
            "sku_id":2,
            "num":3
        }
    ],
    "currency_code":"USD"
}
```
#### 返回参数：
返回数据与购物车详情相同